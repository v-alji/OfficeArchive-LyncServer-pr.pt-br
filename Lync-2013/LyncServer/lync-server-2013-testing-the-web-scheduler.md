---
title: 'Lync Server 2013: testando o Agendador da Web'
description: 'Lync Server 2013: testando o Web scheduler.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the Web scheduler
ms:assetid: 58e34058-1afa-42e3-9096-c4ea1954c237
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727304(v=OCS.15)
ms:contentKeyID: 63969603
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6512bf074078005eac66d1e4f5cd3d8ba2dc4bc7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439720"
---
# <a name="testing-the-web-scheduler-in-lync-server-2013"></a><span data-ttu-id="8f929-103">Testando o Agendador da Web no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8f929-103">Testing the Web scheduler in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8f929-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8f929-104">

<span> </span></span></span>

<span data-ttu-id="8f929-105">_**Tópico da última modificação:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="8f929-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f929-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="8f929-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="8f929-107">Diário</span><span class="sxs-lookup"><span data-stu-id="8f929-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f929-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="8f929-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="8f929-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8f929-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f929-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="8f929-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="8f929-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="8f929-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="8f929-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet <strong>Test-CsWebScheduler</strong> .</span><span class="sxs-lookup"><span data-stu-id="8f929-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsWebScheduler</strong> cmdlet.</span></span> <span data-ttu-id="8f929-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="8f929-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebScheduler&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="8f929-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f929-114">Description</span></span>

<span data-ttu-id="8f929-115">O cmdlet **Test-CsWebScheduler** permite que você determine se um usuário específico pode agendar uma reunião usando o Web scheduler.</span><span class="sxs-lookup"><span data-stu-id="8f929-115">The **Test-CsWebScheduler** cmdlet enables you to determine whether a specific user can schedule a meeting using the Web Scheduler.</span></span> <span data-ttu-id="8f929-116">O Web Scheduler permite que os usuários que não estão executando o Outlook agendem reuniões online.</span><span class="sxs-lookup"><span data-stu-id="8f929-116">The Web Scheduler enables users who are not running Outlook to schedule online meetings.</span></span> <span data-ttu-id="8f929-117">Entre outras coisas, esse novo recurso (que incorpora a funcionalidade encontrada na ferramenta do Agendador da Web incluída com o Microsoft Lync Server 2010 Resource Kit) permite que os usuários:</span><span class="sxs-lookup"><span data-stu-id="8f929-117">Among other things, this new feature (which incorporates the functionality found in the Web Scheduler tool that was included with the Microsoft Lync Server 2010 resource kit) enables users to:</span></span>

  - <span data-ttu-id="8f929-118">Agendar uma nova reunião online.</span><span class="sxs-lookup"><span data-stu-id="8f929-118">Schedule a new online meeting.</span></span>

  - <span data-ttu-id="8f929-119">Listar todas as reuniões agendadas por ele ou ela.</span><span class="sxs-lookup"><span data-stu-id="8f929-119">List all meetings that he or she has scheduled.</span></span>

  - <span data-ttu-id="8f929-120">Exibir/modificar uma reunião existente.</span><span class="sxs-lookup"><span data-stu-id="8f929-120">View/modify an existing meeting.</span></span>

  - <span data-ttu-id="8f929-121">Excluir uma reunião existente.</span><span class="sxs-lookup"><span data-stu-id="8f929-121">Delete an existing meeting.</span></span>

  - <span data-ttu-id="8f929-122">Envie um convite por email para os participantes da reunião usando um servidor de email SMTP pré-configurado.</span><span class="sxs-lookup"><span data-stu-id="8f929-122">Send an email invitation to meeting participants by using a preconfigured SMTP mail server.</span></span>

  - <span data-ttu-id="8f929-123">Ingressar em uma conferência existente.</span><span class="sxs-lookup"><span data-stu-id="8f929-123">Join an existing conference.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="8f929-124">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="8f929-124">Running the test</span></span>

<span data-ttu-id="8f929-125">O exemplo a seguir verifica o Agendador da Web para o conjunto de atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="8f929-125">The following example verifies the Web Scheduler for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="8f929-126">Esse comando funcionará apenas se os usuários de teste estiverem definidos para o pool atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="8f929-126">This command will work only if test users are defined for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="8f929-127">Se eles tiverem, o comando determinará se o primeiro usuário de teste pode agendar uma reunião online usando o Web scheduler.</span><span class="sxs-lookup"><span data-stu-id="8f929-127">If they have, then the command will determine whether the first test user can schedule an online meeting using the Web Scheduler.</span></span>

<span data-ttu-id="8f929-128">Se os usuários de teste não estiverem definidos, o comando falhará porque não saberá qual usuário deve fazer logon.</span><span class="sxs-lookup"><span data-stu-id="8f929-128">If test users are not defined, then the command will fail because it won't know which user to log on as.</span></span> <span data-ttu-id="8f929-129">Se você não definiu usuários de teste para um pool, deve incluir o parâmetro UserSipAddress e as credenciais do usuário que o comando deve usar quando tentar fazer logon.</span><span class="sxs-lookup"><span data-stu-id="8f929-129">If you have not defined test users for a pool, then you must include the UserSipAddress parameter and the credentials of the user the command should use when trying to log on.</span></span>

    Test-CsWebScheduler -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="8f929-130">Os comandos mostrados no próximo exemplo testam a capacidade de um usuário específico (litwareinc \\ kenmeyer) agendar uma reunião online usando o Web scheduler.</span><span class="sxs-lookup"><span data-stu-id="8f929-130">The commands shown in the next example test the ability of a specific user (litwareinc\\kenmeyer) to schedule an online meeting using the Web scheduler.</span></span> <span data-ttu-id="8f929-131">Para fazer isso, o primeiro comando do exemplo usa o cmdlet **Get-Credential** para criar um objeto de credencial da interface de linha de comando do Windows PowerShell que contém o nome e a senha do usuário Ken Meyer.</span><span class="sxs-lookup"><span data-stu-id="8f929-131">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Ken Meyer.</span></span> <span data-ttu-id="8f929-132">(Como o nome de logon litwareinc \\ kenmeyer está incluído como um parâmetro, a caixa de diálogo solicitação de credenciais do Windows PowerShell exige que o administrador digite a senha da conta Ken Meyer.) O objeto Credential resultante é armazenado em uma variável chamada $cred 1.</span><span class="sxs-lookup"><span data-stu-id="8f929-132">(Because the logon name litwareinc\\kenmeyer is included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Ken Meyer account.) The resulting credential object is then stored in a variable named $cred1.</span></span>

<span data-ttu-id="8f929-133">Em seguida, o segundo comando verifica se este usuário pode fazer logon no pool atl-cs-001.litwareinc.com e agendar uma reunião online.</span><span class="sxs-lookup"><span data-stu-id="8f929-133">The second command then checks whether this user can log on to the pool atl-cs-001.litwareinc.com and schedule an online meeting.</span></span> <span data-ttu-id="8f929-134">Para executar essa tarefa, o cmdlet **Test-CsWebScheduler** é chamado, juntamente com três parâmetros: TargetFqdn (o FQDN do pool de registrador); Usercredential (o objeto do Windows PowerShell que contém as credenciais de usuário de pilar Alverca); e UserSipAddress (o endereço SIP correspondente às credenciais de usuário fornecidas).</span><span class="sxs-lookup"><span data-stu-id="8f929-134">To run this task, the **Test-CsWebScheduler** cmdlet is called, together with three parameters: TargetFqdn (the FQDN of the Registrar pool); UserCredential (the Windows PowerShell object that contains Pilar Ackerman’s user credentials); and UserSipAddress (the SIP address that corresponds to the supplied user credentials).</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    
    Test-CsWebScheduler -TargetFqdn "atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="8f929-135">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="8f929-135">Determining success or failure</span></span>

<span data-ttu-id="8f929-136">Se o Web Scheduler estiver configurado corretamente, você receberá uma saída semelhante a isso, com a propriedade Result marcada como **Success**:</span><span class="sxs-lookup"><span data-stu-id="8f929-136">If the web scheduler is configured correctly , you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="8f929-137">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="8f929-137">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="8f929-138">URI de destino: https://atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="8f929-138">Target Uri : https:// atl-cs-001.litwareinc.com.</span></span>

<span data-ttu-id="8f929-139">litwareinc.com:443/Scheduler</span><span class="sxs-lookup"><span data-stu-id="8f929-139">litwareinc.com:443/Scheduler</span></span>

<span data-ttu-id="8f929-140">Resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="8f929-140">Result : Success</span></span>

<span data-ttu-id="8f929-141">Latência: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="8f929-141">Latency : 00:00:00</span></span>

<span data-ttu-id="8f929-142">Mensagem de erro:</span><span class="sxs-lookup"><span data-stu-id="8f929-142">Error Message :</span></span>

<span data-ttu-id="8f929-143">Correto</span><span class="sxs-lookup"><span data-stu-id="8f929-143">Diagnosis :</span></span>

<span data-ttu-id="8f929-144">Se o Web Scheduler não estiver configurado corretamente, o resultado será mostrado como uma **falha**, e informações adicionais serão gravadas nas propriedades de erro e diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="8f929-144">If the web scheduler is not configured correctly, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="8f929-145">Aviso: falha ao ler o número da porta do registrador para o número da porta de dados totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="8f929-145">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="8f929-146">FQDN (nome de domínio).</span><span class="sxs-lookup"><span data-stu-id="8f929-146">domain name (FQDN).</span></span> <span data-ttu-id="8f929-147">Usando o número da porta do registrador padrão.</span><span class="sxs-lookup"><span data-stu-id="8f929-147">Using default Registrar port number.</span></span> <span data-ttu-id="8f929-148">Extremamente</span><span class="sxs-lookup"><span data-stu-id="8f929-148">Exception:</span></span>

<span data-ttu-id="8f929-149">System. InvalidOperationException: nenhum cluster correspondente localizado na topologia.</span><span class="sxs-lookup"><span data-stu-id="8f929-149">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="8f929-150">como</span><span class="sxs-lookup"><span data-stu-id="8f929-150">at</span></span>

<span data-ttu-id="8f929-151">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="8f929-151">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="8f929-152">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="8f929-152">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="8f929-153">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="8f929-153">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="8f929-154">URI de destino:</span><span class="sxs-lookup"><span data-stu-id="8f929-154">Target Uri :</span></span>

<span data-ttu-id="8f929-155">Resultado: falha</span><span class="sxs-lookup"><span data-stu-id="8f929-155">Result : Failure</span></span>

<span data-ttu-id="8f929-156">Latência: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="8f929-156">Latency : 00:00:00</span></span>

<span data-ttu-id="8f929-157">Mensagem de erro: nenhum cluster correspondente localizado na topologia.</span><span class="sxs-lookup"><span data-stu-id="8f929-157">Error Message : No matching cluster found in topology.</span></span>

<span data-ttu-id="8f929-158">Correto</span><span class="sxs-lookup"><span data-stu-id="8f929-158">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="8f929-159">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="8f929-159">Reasons why the test might have failed</span></span>

<span data-ttu-id="8f929-160">Aqui estão alguns motivos comuns pelos quais **Test-CsWebScheduler** pode falhar:</span><span class="sxs-lookup"><span data-stu-id="8f929-160">Here are some common reasons why **Test-CsWebScheduler** might fail:</span></span>

  - <span data-ttu-id="8f929-161">Um valor de parâmetro incorreto foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="8f929-161">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="8f929-162">Se usado, os parâmetros opcionais devem ser configurados corretamente ou o teste falhará.</span><span class="sxs-lookup"><span data-stu-id="8f929-162">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="8f929-163">Execute o comando novamente sem os parâmetros opcionais e veja se isso é bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8f929-163">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="8f929-164">Esse comando falhará se o Web Scheduler estiver configurado incorretamente ou ainda não foi implantado.</span><span class="sxs-lookup"><span data-stu-id="8f929-164">This command will fail if the Web Scheduler is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8f929-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f929-165">See Also</span></span>


[<span data-ttu-id="8f929-166">Set-CsWebServer</span><span class="sxs-lookup"><span data-stu-id="8f929-166">Set-CsWebServer</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServer)  
  

<span data-ttu-id="8f929-167"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8f929-167"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

