---
title: 'Lync Server 2013: testando a publicação de presença do usuário e a inscrição'
description: 'Lync Server 2013: testando a publicação de presença do usuário e a inscrição.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing user presence publishing and subscribing
ms:assetid: 27694c71-8e63-4aa4-b49f-fa06ccb81949
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743832(v=OCS.15)
ms:contentKeyID: 63969587
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 90913f270fbd034ca4d2ea7cf3b93c255fc95c66
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439706"
---
# <a name="testing-user-presence-publishing-and-subscribing-in-lync-server-2013"></a><span data-ttu-id="9153e-103">Testando a publicação de presença do usuário e a inscrição no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9153e-103">Testing user presence publishing and subscribing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9153e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9153e-104">

<span> </span></span></span>

<span data-ttu-id="9153e-105">_**Tópico da última modificação:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="9153e-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9153e-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="9153e-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="9153e-107">Diário</span><span class="sxs-lookup"><span data-stu-id="9153e-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9153e-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="9153e-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="9153e-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9153e-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9153e-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="9153e-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="9153e-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="9153e-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="9153e-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsPresence.</span><span class="sxs-lookup"><span data-stu-id="9153e-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsPresence cmdlet.</span></span> <span data-ttu-id="9153e-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9153e-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPresence&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="9153e-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9153e-114">Description</span></span>

<span data-ttu-id="9153e-115">Test-CsPresence é usado para determinar se um par de usuários de teste podem fazer logon no Lync Server e, em seguida, trocar informações de presença.</span><span class="sxs-lookup"><span data-stu-id="9153e-115">Test-CsPresence is used to determine whether a pair of test users can log on to Lync Server and then exchange presence information.</span></span> <span data-ttu-id="9153e-116">Para fazer isso, o cmdlet primeiro registra os dois usuários no sistema.</span><span class="sxs-lookup"><span data-stu-id="9153e-116">To do this, the cmdlet first logs the two users on to the system.</span></span> <span data-ttu-id="9153e-117">Se os dois logons forem bem-sucedidos, o primeiro usuário de teste pedirá receber informações de presença do segundo usuário.</span><span class="sxs-lookup"><span data-stu-id="9153e-117">If both logons succeed, the first test user then asks to receive presence information from the second user.</span></span> <span data-ttu-id="9153e-118">O segundo usuário publica essas informações e Test-CsPresence verifica se as informações foram transmitidas com êxito para o primeiro usuário.</span><span class="sxs-lookup"><span data-stu-id="9153e-118">The second user publishes this information, and Test-CsPresence verifies that the information was successfully transmitted to the first user.</span></span> <span data-ttu-id="9153e-119">Após a troca de informações de presença, os dois usuários de teste são desconectados do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9153e-119">After the exchange of presence information, the two test users are then logged off from Lync Server.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="9153e-120">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="9153e-120">Running the test</span></span>

<span data-ttu-id="9153e-121">O cmdlet Test-CsPresence pode ser executado usando um par de contas de teste pré-configuradas (consulte Configurando contas de teste para executar testes do Lync Server) ou as contas de dois usuários que estão habilitados para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9153e-121">The Test-CsPresence cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="9153e-122">Para executar essa verificação usando contas de teste, basta especificar o FQDN do pool do servidor do Lync que está sendo testado.</span><span class="sxs-lookup"><span data-stu-id="9153e-122">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="9153e-123">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="9153e-123">For example:</span></span>

    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="9153e-124">Para executar essa verificação usando contas de usuário reais, você deve criar dois objetos de credenciais do Windows PowerShell (objetos que contêm o nome da conta e a senha) para cada conta.</span><span class="sxs-lookup"><span data-stu-id="9153e-124">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="9153e-125">Em seguida, você deve incluir esses objetos de credenciais e os endereços SIP das duas contas ao chamar Test-CsPresence:</span><span class="sxs-lookup"><span data-stu-id="9153e-125">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsPresence:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com" -PublisherSipAddress "sip:kenmyer@litwareinc.com" -PublisherCredential $credential1 -SubscriberSipAddress "sip:davidlongmire@litwareinc.com" -SubscriberCredential $credential2

<span data-ttu-id="9153e-126">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsPresence](https://docs.microsoft.com/powershell/module/skype/Test-CsPresence) .</span><span class="sxs-lookup"><span data-stu-id="9153e-126">For more information, see the Help documentation for the [Test-CsPresence](https://docs.microsoft.com/powershell/module/skype/Test-CsPresence) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="9153e-127">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="9153e-127">Determining success or failure</span></span>

<span data-ttu-id="9153e-128">Se os usuários especificados puderem trocar informações de presença, você receberá uma saída semelhante a isso, com a propriedade Result marcada como **Success:**</span><span class="sxs-lookup"><span data-stu-id="9153e-128">If the specified users can exchange presence information, then you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="9153e-129">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="9153e-129">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="9153e-130">Resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="9153e-130">Result : Success</span></span>

<span data-ttu-id="9153e-131">Latência: 00:00:06.3280315</span><span class="sxs-lookup"><span data-stu-id="9153e-131">Latency : 00:00:06.3280315</span></span>

<span data-ttu-id="9153e-132">Erros</span><span class="sxs-lookup"><span data-stu-id="9153e-132">Error :</span></span>

<span data-ttu-id="9153e-133">Correto</span><span class="sxs-lookup"><span data-stu-id="9153e-133">Diagnosis :</span></span>

<span data-ttu-id="9153e-134">Se os dois usuários não puderem trocar informações de presença, o resultado será mostrado como uma falha, e informações adicionais serão gravadas nas propriedades de erro e diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="9153e-134">If the two users can't exchange presence information, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="9153e-135">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="9153e-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="9153e-136">Resultado: falha</span><span class="sxs-lookup"><span data-stu-id="9153e-136">Result : Failure</span></span>

<span data-ttu-id="9153e-137">Latência: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9153e-137">Latency : 00:00:00</span></span>

<span data-ttu-id="9153e-138">Erro: 404, não encontrado</span><span class="sxs-lookup"><span data-stu-id="9153e-138">Error : 404, Not Found</span></span>

<span data-ttu-id="9153e-139">Diagnóstico: ErrorCode = 4005, Source = ATL-cs-001.litwareinc.com,</span><span class="sxs-lookup"><span data-stu-id="9153e-139">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="9153e-140">Motivo = o URI de destino não está habilitado para SIP ou não</span><span class="sxs-lookup"><span data-stu-id="9153e-140">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="9153e-141">Existem.</span><span class="sxs-lookup"><span data-stu-id="9153e-141">exist.</span></span>

<span data-ttu-id="9153e-142">Microsoft. RTC. Signaling. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="9153e-142">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="9153e-143">Por exemplo, a saída anterior informa que o teste falhou porque pelo menos uma das duas contas de usuário não é válida: a conta não existe ou não foi habilitada para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9153e-143">For example, the previous output states that the test failed because at least one of the two user accounts is not valid: either the account does not exist or it has not been enabled for Lync Server.</span></span> <span data-ttu-id="9153e-144">Você pode verificar se as contas existem e determinar se elas estão habilitadas para o Lync Server, executando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="9153e-144">You can verify that the accounts exist, and determine whether they are enabled for Lync Server, by running a command similar to this:</span></span>

    "sip:kenmyer@litwareinc.com", "sip:davidlongmire@litwareinc.com" | Get-CsUser | Select-Object SipAddress, Enabled

<span data-ttu-id="9153e-145">Se Test-CsPresence falhar, talvez você queira executar novamente o teste, desta vez, incluindo o parâmetro Verbose:</span><span class="sxs-lookup"><span data-stu-id="9153e-145">If Test-CsPresence fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="9153e-146">Quando o parâmetro Verbose estiver incluído, Test-CsPresence retornará uma conta passo a passo de cada ação que tentou verificar quando verificou a capacidade do usuário especificado para fazer logon no Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9153e-146">When the Verbose parameter is included, Test-CsPresence will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="9153e-147">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="9153e-147">For example:</span></span>

<span data-ttu-id="9153e-148">A solicitação de registro foi atingida contra desconhecido</span><span class="sxs-lookup"><span data-stu-id="9153e-148">Registration Request hit against Unknown</span></span>

<span data-ttu-id="9153e-149">Atividade ' Register ' concluída em ' 0, 345791 ' segundos.</span><span class="sxs-lookup"><span data-stu-id="9153e-149">'Register' activity completed in '0.0345791' secs.</span></span>

<span data-ttu-id="9153e-150">Atividade "SelfSubscribeActivity" iniciada.</span><span class="sxs-lookup"><span data-stu-id="9153e-150">'SelfSubscribeActivity' activity started.</span></span>

<span data-ttu-id="9153e-151">Atividade ' SelfSubscribeActivity ' concluída em ' 0, 41174 ' segundos.</span><span class="sxs-lookup"><span data-stu-id="9153e-151">'SelfSubscribeActivity' activity completed in '0.0041174' secs.</span></span>

<span data-ttu-id="9153e-152">Atividade "SubscribePresence" iniciada.</span><span class="sxs-lookup"><span data-stu-id="9153e-152">'SubscribePresence' activity started.</span></span>

<span data-ttu-id="9153e-153">Atividade ' SubscribePresence ' concluída em ' 0, 38764 ' segundos.</span><span class="sxs-lookup"><span data-stu-id="9153e-153">'SubscribePresence' activity completed in '0.0038764' secs.</span></span>

<span data-ttu-id="9153e-154">Atividade "PublishPresence" iniciada.</span><span class="sxs-lookup"><span data-stu-id="9153e-154">'PublishPresence' activity started.</span></span>

<span data-ttu-id="9153e-155">A notificação de presença de uma exceção não é recebida dentro de 25 segundos. "</span><span class="sxs-lookup"><span data-stu-id="9153e-155">An exception 'Presence notification is not received within 25 secs.'</span></span> <span data-ttu-id="9153e-156">ocorrido ruing o fluxo de trabalho Microsoft. RTC. SyntheticTransactions. workflows. STPresenceWorkflow Execution.</span><span class="sxs-lookup"><span data-stu-id="9153e-156">occurred ruing Workflow Microsoft.Rtc.SyntheticTransactions.Workflows.STPresenceWorkflow execution.</span></span>

<span data-ttu-id="9153e-157">O fato de que a notificação de presença não foi recebida dentro de 25 segundos pode indicar que problemas de rede estão impedindo que as informações sejam trocadas.</span><span class="sxs-lookup"><span data-stu-id="9153e-157">The fact that the presence notification was not received within 25 seconds might indicate that network issues are preventing information from being exchanged.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="9153e-158">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="9153e-158">Reasons why the test might have failed</span></span>

<span data-ttu-id="9153e-159">Veja a seguir alguns motivos comuns para que Test-CsPresence possam falhar:</span><span class="sxs-lookup"><span data-stu-id="9153e-159">Here are some common reasons why Test-CsPresence might fail:</span></span>

  - <span data-ttu-id="9153e-160">Você especificou uma conta de usuário incorreta.</span><span class="sxs-lookup"><span data-stu-id="9153e-160">You specified an incorrect user account.</span></span> <span data-ttu-id="9153e-161">Você pode verificar se existe uma conta de usuário executando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="9153e-161">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="9153e-162">A conta de usuário é válida, mas a conta não está habilitada no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9153e-162">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="9153e-163">Para verificar se uma conta de usuário está habilitada para o Lync Server, execute um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="9153e-163">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="9153e-164">Se a propriedade Enabled estiver definida como false, isso significa que o usuário não está habilitado no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9153e-164">If the Enabled property is set to False that means that the user is currently not enabled for Lync Server.</span></span>

<span data-ttu-id="9153e-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9153e-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

