---
title: 'Lync Server 2013: testando a capacidade de um usuário para fazer logon no Lync Server'
description: 'Lync Server 2013: testando a capacidade de um usuário para fazer logon no Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the ability of a user to log on to Lync Server
ms:assetid: d9cd0f9b-6ef2-4050-a4ca-263c5afa93ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743841(v=OCS.15)
ms:contentKeyID: 63969655
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8b86ae3e490af0b361799ed5fb3f56ed4de42c82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389961"
---
# <a name="testing-the-ability-of-a-user-to-log-on-to-lync-server-2013"></a><span data-ttu-id="cb244-103">Testar a capacidade de um usuário para fazer logon no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cb244-103">Testing the ability of a user to log on to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cb244-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cb244-104">

<span> </span></span></span>

<span data-ttu-id="cb244-105">_**Tópico da última modificação:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="cb244-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb244-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="cb244-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="cb244-107">Diário</span><span class="sxs-lookup"><span data-stu-id="cb244-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb244-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="cb244-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="cb244-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb244-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb244-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="cb244-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="cb244-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="cb244-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="cb244-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsRegistration.</span><span class="sxs-lookup"><span data-stu-id="cb244-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsRegistration cmdlet.</span></span> <span data-ttu-id="cb244-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="cb244-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsRegistration&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="cb244-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb244-114">Description</span></span>

<span data-ttu-id="cb244-115">O cmdlet Test-CsRegistration permite que você verifique se os usuários em sua organização podem fazer logon no Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cb244-115">The Test-CsRegistration cmdlet enables you to verify that users in your organization can log on to Lync Server.</span></span> <span data-ttu-id="cb244-116">Ao executar Test-CsRegistration, o cmdlet tenta se conectar a um usuário de teste ao Lync Server e, se tiver êxito, desconectará o usuário de teste do sistema.</span><span class="sxs-lookup"><span data-stu-id="cb244-116">When you run Test-CsRegistration, the cmdlet attempts to sign in a test user to Lync Server and then, if it is successful, disconnects that test user from the system.</span></span> <span data-ttu-id="cb244-117">Tudo isso acontece sem qualquer interação do usuário e sem afetar os usuários reais.</span><span class="sxs-lookup"><span data-stu-id="cb244-117">All of this happens without any user interaction, and without affecting any actual users.</span></span> <span data-ttu-id="cb244-118">Por exemplo, suponha que o sip:kenmyer@litwareinc.com da conta de teste corresponda a um usuário real que tenha uma conta real do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cb244-118">For example, suppose that the test account sip:kenmyer@litwareinc.com corresponds to a real user who has a real Lync Server account.</span></span> <span data-ttu-id="cb244-119">Nesse caso, o teste será realizado sem qualquer interrupção no Ken Myer verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="cb244-119">In that case, the test will be conducted without any disruption to the real Ken Myer.</span></span> <span data-ttu-id="cb244-120">Quando a conta de teste de Ken Myer é desconectada do sistema, Ken Myer a pessoa permanecerá conectada.</span><span class="sxs-lookup"><span data-stu-id="cb244-120">When the Ken Myer test account logs off from the system, Ken Myer the person will remain logged on.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="cb244-121">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="cb244-121">Running the test</span></span>

<span data-ttu-id="cb244-122">O cmdlet Test-CsRegistration pode ser executado usando uma conta de teste pré-configurada (consulte Configurando contas de teste para executar testes do Lync Server) ou a conta de qualquer usuário habilitado para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cb244-122">The Test-CsRegistration cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="cb244-123">Para executar essa verificação usando uma conta de teste, basta especificar o FQDN do pool de registradores do Lync Server que está sendo testado.</span><span class="sxs-lookup"><span data-stu-id="cb244-123">To run this check using a test account, you just have to specify the FQDN of the Lync Server Registrar pool being tested.</span></span> <span data-ttu-id="cb244-124">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="cb244-124">For example:</span></span>

    Test-CsRegistration -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="cb244-125">Para executar essa verificação usando uma conta de usuário real, primeiro você deve criar um objeto de credenciais do Windows PowerShell que contenha o nome da conta e a senha.</span><span class="sxs-lookup"><span data-stu-id="cb244-125">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="cb244-126">Em seguida, você deve incluir esse objeto de credenciais e o endereço SIP atribuído à conta ao chamar Test-CsRegistration:</span><span class="sxs-lookup"><span data-stu-id="cb244-126">You must then include that credentials object and the SIP address assigned to the account when you call Test-CsRegistration:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsRegistration -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="cb244-127">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsRegistration](https://docs.microsoft.com/powershell/module/skype/Test-CsRegistration) .</span><span class="sxs-lookup"><span data-stu-id="cb244-127">For more information, see the Help documentation for the [Test-CsRegistration](https://docs.microsoft.com/powershell/module/skype/Test-CsRegistration) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="cb244-128">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="cb244-128">Determining success or failure</span></span>

<span data-ttu-id="cb244-129">Se o usuário especificado puder fazer logon (e, em seguida, fazer logoff do) Lync Server, você receberá uma saída semelhante a isso com a propriedade Result marcada como **Success:**</span><span class="sxs-lookup"><span data-stu-id="cb244-129">If the specified user can log on to (and then log off from) Lync Server, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="cb244-130">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="cb244-130">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="cb244-131">Resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="cb244-131">Result : Success</span></span>

<span data-ttu-id="cb244-132">Latência: 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="cb244-132">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="cb244-133">Erros</span><span class="sxs-lookup"><span data-stu-id="cb244-133">Error :</span></span>

<span data-ttu-id="cb244-134">Correto</span><span class="sxs-lookup"><span data-stu-id="cb244-134">Diagnosis :</span></span>

<span data-ttu-id="cb244-135">Se o usuário especificado não puder entrar ou fazer logoff, o resultado será mostrado como uma falha, e informações adicionais serão gravadas nas propriedades de erro e diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="cb244-135">If the specified user can't log in or log out, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="cb244-136">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="cb244-136">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="cb244-137">Resultado: falha</span><span class="sxs-lookup"><span data-stu-id="cb244-137">Result : Failure</span></span>

<span data-ttu-id="cb244-138">Latência: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="cb244-138">Latency : 00:00:00</span></span>

<span data-ttu-id="cb244-139">Erro: 404, não encontrado</span><span class="sxs-lookup"><span data-stu-id="cb244-139">Error : 404, Not Found</span></span>

<span data-ttu-id="cb244-140">Diagnóstico: ErrorCode = 1003, Source = ATL-cs-001. litwareinc. com, Reason = o usuário faz</span><span class="sxs-lookup"><span data-stu-id="cb244-140">Diagnosis : ErrorCode=1003,source=atl-cs-001.litwareinc.com,Reason=User does</span></span>

<span data-ttu-id="cb244-141">Não existe</span><span class="sxs-lookup"><span data-stu-id="cb244-141">not exist</span></span>

<span data-ttu-id="cb244-142">Microsoft. RTC. Signaling. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="cb244-142">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="cb244-143">Por exemplo, a saída anterior informa que o teste falhou porque o usuário especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="cb244-143">For example, the previous output states that the test failed because the specified user couldn't be found.</span></span> <span data-ttu-id="cb244-144">Você pode determinar se um endereço SIP é válido (e se o usuário que atribuiu esse endereço SIP está habilitado para o Lync Server) executando este comando:</span><span class="sxs-lookup"><span data-stu-id="cb244-144">You can determine whether or not a SIP address is valid (and whether the user assigned that SIP address is enabled for Lync Server) by running this command:</span></span>

    Get-CsUser "sip:kenmyer@litwareinc.com"

<span data-ttu-id="cb244-145">Se Test-CsRegistration falhar, talvez você queira executar novamente o teste, desta vez, incluindo o parâmetro Verbose:</span><span class="sxs-lookup"><span data-stu-id="cb244-145">If Test-CsRegistration fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsRegistration -UserSipAddress "sip:kenmyer@litwareinc.com" -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="cb244-146">Quando o parâmetro Verbose estiver incluído, Test-CsRegistration retornará uma conta passo a passo de cada ação que tentou verificar quando verificou a capacidade do usuário especificado para fazer logon no Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cb244-146">When the Verbose parameter is included, Test-CsRegistration will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="cb244-147">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="cb244-147">For example:</span></span>

<span data-ttu-id="cb244-148">VERBOse: atividade de ' registro ' iniciada.</span><span class="sxs-lookup"><span data-stu-id="cb244-148">VERBOSE: 'Register' activity started.</span></span>

<span data-ttu-id="cb244-149">Enviando solicitação de registro:</span><span class="sxs-lookup"><span data-stu-id="cb244-149">Sending Registration request:</span></span>

<span data-ttu-id="cb244-150">FQDN de destino = atl-cs-011.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="cb244-150">Target Fqdn = atl-cs-011.litwareinc.com</span></span>

<span data-ttu-id="cb244-151">Endereço SIP do usuário = sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="cb244-151">User Sip Address = sip:kenmyer@litwareinc.com</span></span>

<span data-ttu-id="cb244-152">Porta do registrador = 5061.</span><span class="sxs-lookup"><span data-stu-id="cb244-152">Registrar Port = 5061.</span></span>

<span data-ttu-id="cb244-153">O tipo de autenticação "confiável" está selecionado.</span><span class="sxs-lookup"><span data-stu-id="cb244-153">Auth Type 'Trusted' is selected.</span></span>

<span data-ttu-id="cb244-154">Uma exceção ' o ponto de extremidade não pode se registrar.</span><span class="sxs-lookup"><span data-stu-id="cb244-154">An exception 'The endpoint is unable to register.</span></span> <span data-ttu-id="cb244-155">Veja o código de erro por motivo específico ' durante a execução do fluxo de trabalho Microsoft. RTC. SyntheticTransactions. Workflow. STRegistrerWorkflow.</span><span class="sxs-lookup"><span data-stu-id="cb244-155">See the ErrorCode for specific reason' occurred during Workflow Microsoft.Rtc.SyntheticTransactions.Workflow.STRegistrerWorkflow execution.</span></span>

<span data-ttu-id="cb244-156">Pilha de chamadas de exceção: em Microsoft. RTC. Signaling. SipAsyncResult'1. ThrowIfFailed ()</span><span class="sxs-lookup"><span data-stu-id="cb244-156">Exception Call Stack: at Microsoft.Rtc.Signaling.SipAsyncResult'1.ThrowIfFailed()</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="cb244-157">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="cb244-157">Reasons why the test might have failed</span></span>

<span data-ttu-id="cb244-158">Veja a seguir alguns motivos comuns para que Test-CsRegistration possam falhar:</span><span class="sxs-lookup"><span data-stu-id="cb244-158">Here are some common reasons why Test-CsRegistration might fail:</span></span>

  - <span data-ttu-id="cb244-159">Você especificou uma conta de usuário incorreta.</span><span class="sxs-lookup"><span data-stu-id="cb244-159">You specified an incorrect user account.</span></span> <span data-ttu-id="cb244-160">Você pode verificar se existe uma conta de usuário executando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="cb244-160">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="cb244-161">A conta de usuário é válida, mas a conta não está habilitada no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cb244-161">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="cb244-162">Para verificar se uma conta de usuário está habilitada para o Lync Server, execute um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb244-162">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="cb244-163">Se a propriedade Enabled estiver definida como false, isso significa que o usuário não está habilitado no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cb244-163">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="cb244-164">Você especificou um pool de registradores incorreto.</span><span class="sxs-lookup"><span data-stu-id="cb244-164">You specified an incorrect Registrar pool.</span></span> <span data-ttu-id="cb244-165">Você pode retornar os FQDNs dos seus pools de registradores usando este comando:</span><span class="sxs-lookup"><span data-stu-id="cb244-165">You can return the FQDNs of your Registrar pools by using this command:</span></span>
    
        Get-CsService -Registrar | Select-Object PoolFqdn

  - <span data-ttu-id="cb244-166">No momento, o pool de registradores não está disponível.</span><span class="sxs-lookup"><span data-stu-id="cb244-166">The Registrar pool is currently not available.</span></span> <span data-ttu-id="cb244-167">Tente executar o ping no pool para ver se ele responde:</span><span class="sxs-lookup"><span data-stu-id="cb244-167">Try pinging the pool to see whether it responds:</span></span>
    
        ping atl-cs-001.litwareinc.com

<span data-ttu-id="cb244-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cb244-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

