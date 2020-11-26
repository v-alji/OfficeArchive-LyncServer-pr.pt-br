---
title: 'Lync Server 2013: testando a chamada de áudio/vídeo ponto a ponto'
description: 'Lync Server 2013: testando a chamada de áudio/vídeo ponto a ponto.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing peer to peer audio/video call
ms:assetid: 95eb3693-b866-4652-bc45-9b75fdb40b49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743835(v=OCS.15)
ms:contentKeyID: 63969627
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03bab69d926a99c091a510ce64b78dbf505d4cbc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439811"
---
# <a name="testing-peer-to-peer-audiovideo-call-in-lync-server-2013"></a><span data-ttu-id="9d743-103">Testando a chamada de áudio/vídeo ponto a ponto no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9d743-103">Testing peer to peer audio/video call in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9d743-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9d743-104">

<span> </span></span></span>

<span data-ttu-id="9d743-105">_**Tópico da última modificação:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="9d743-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d743-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="9d743-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="9d743-107">Diário</span><span class="sxs-lookup"><span data-stu-id="9d743-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d743-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="9d743-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="9d743-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d743-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d743-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="9d743-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="9d743-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="9d743-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="9d743-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsP2PAV.</span><span class="sxs-lookup"><span data-stu-id="9d743-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsP2PAV cmdlet.</span></span> <span data-ttu-id="9d743-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9d743-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsP2PAV&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="9d743-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d743-114">Description</span></span>

<span data-ttu-id="9d743-115">Test-CsP2PAV é usado para determinar se um par de usuários de teste podem participar de uma conversa ponto a ponto A/V.</span><span class="sxs-lookup"><span data-stu-id="9d743-115">Test-CsP2PAV is used to determine whether a pair of test users can participate in a peer-to-peer A/V conversation.</span></span> <span data-ttu-id="9d743-116">Para testar esse cenário, o cmdlet começa a fazer logon nos dois usuários do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9d743-116">To test this scenario, the cmdlet starts off by logging on the two users to Lync Server.</span></span> <span data-ttu-id="9d743-117">Pressupondo que os dois logons sejam bem-sucedidos, o primeiro usuário convida o segundo usuário para ingressar em uma chamada A/V.</span><span class="sxs-lookup"><span data-stu-id="9d743-117">Assuming that the two logons succeed, the first user then invites the second user to join an A/V call.</span></span> <span data-ttu-id="9d743-118">O segundo usuário aceita a chamada, a conexão entre os dois usuários é testada e, em seguida, a chamada é encerrada e os usuários de teste são desconectados do sistema.</span><span class="sxs-lookup"><span data-stu-id="9d743-118">The second user accepts the call, the connection between the two users is tested, and then the call is ended and the test users are logged off from the system.</span></span>

<span data-ttu-id="9d743-119">Test-CsP2PAV não realiza uma chamada A/V.</span><span class="sxs-lookup"><span data-stu-id="9d743-119">Test-CsP2PAV does not actually conduct an A/V call.</span></span> <span data-ttu-id="9d743-120">As informações de multimídia não são trocadas entre os usuários do teste.</span><span class="sxs-lookup"><span data-stu-id="9d743-120">Multimedia information is not exchanged between the test users.</span></span> <span data-ttu-id="9d743-121">Em vez disso, o cmdlet verifica apenas se as conexões apropriadas podem ser feitas e se os dois usuários podem conduzir essa chamada.</span><span class="sxs-lookup"><span data-stu-id="9d743-121">Instead, the cmdlet merely verifies that the appropriate connections can be made and that the two users can conduct such a call.</span></span>

<span data-ttu-id="9d743-122">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsP2PAV](https://docs.microsoft.com/powershell/module/skype/Test-CsP2PAV) .</span><span class="sxs-lookup"><span data-stu-id="9d743-122">For more information, see the Help documentation for the [Test-CsP2PAV](https://docs.microsoft.com/powershell/module/skype/Test-CsP2PAV) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="9d743-123">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="9d743-123">Running the test</span></span>

<span data-ttu-id="9d743-124">O cmdlet Test-CsP2PAV pode ser executado usando um par de contas de teste pré-configuradas (consulte Configurando contas de teste para executar testes do Lync Server) ou as contas de dois usuários que estão habilitados para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9d743-124">The Test-CsP2PAV cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="9d743-125">Para executar essa verificação usando contas de teste, basta especificar o FQDN do pool do servidor do Lync que está sendo testado.</span><span class="sxs-lookup"><span data-stu-id="9d743-125">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="9d743-126">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="9d743-126">For example:</span></span>

    Test-CsP2PAV -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="9d743-127">Para executar essa verificação usando contas de usuário reais, você deve criar dois objetos de credenciais do Lync Server (objetos que contêm o nome da conta e a senha) para cada conta.</span><span class="sxs-lookup"><span data-stu-id="9d743-127">To run this check using actual user accounts, you must create two Lync Server credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="9d743-128">Em seguida, você deve incluir esses objetos de credenciais e os endereços SIP das duas contas ao chamar Test-CsP2PAV:</span><span class="sxs-lookup"><span data-stu-id="9d743-128">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsP2PAV:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsP2PAV -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="9d743-129">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="9d743-129">Determining success or failure</span></span>

<span data-ttu-id="9d743-130">Se os dois usuários do teste puderem concluir uma chamada de A/V ponto a ponto, você receberá uma saída semelhante a isso com a propriedade Result marcada como **Success:**</span><span class="sxs-lookup"><span data-stu-id="9d743-130">If the two test users can complete a peer-to-peer A/V call, then you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="9d743-131">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="9d743-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="9d743-132">Resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="9d743-132">Result : Success</span></span>

<span data-ttu-id="9d743-133">Latência: 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="9d743-133">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="9d743-134">Erros</span><span class="sxs-lookup"><span data-stu-id="9d743-134">Error :</span></span>

<span data-ttu-id="9d743-135">Correto</span><span class="sxs-lookup"><span data-stu-id="9d743-135">Diagnosis :</span></span>

<span data-ttu-id="9d743-136">Se os usuários do teste não puderem concluir a chamada, o resultado será mostrado como uma falha, e informações adicionais serão gravadas nas propriedades de erro e diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="9d743-136">If the test users can't complete the call, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="9d743-137">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="9d743-137">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="9d743-138">Resultado: falha</span><span class="sxs-lookup"><span data-stu-id="9d743-138">Result : Failure</span></span>

<span data-ttu-id="9d743-139">Latência: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9d743-139">Latency : 00:00:00</span></span>

<span data-ttu-id="9d743-140">Erro: 480, temporariamente indisponível</span><span class="sxs-lookup"><span data-stu-id="9d743-140">Error : 480, Temporarily Unavailable</span></span>

<span data-ttu-id="9d743-141">Diagnóstico: ErrorCode = 15030, Source = ATL-cs-001. litwareinc. com, Reason = Failed</span><span class="sxs-lookup"><span data-stu-id="9d743-141">Diagnosis : ErrorCode=15030,Source=atl-cs-001.litwareinc.com,Reason=Failed</span></span>

<span data-ttu-id="9d743-142">para circular para o Exchange Server</span><span class="sxs-lookup"><span data-stu-id="9d743-142">to route to Exchange Server</span></span>

<span data-ttu-id="9d743-143">Microsoft. RTC. Signaling. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="9d743-143">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="9d743-144">Por exemplo, a saída anterior informa que o teste falhou porque não foi possível entrar em contato com o Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9d743-144">For example, the previous output states that the test failed because the Microsoft Exchange Server couldn't be contacted.</span></span> <span data-ttu-id="9d743-145">Geralmente, essa mensagem de erro indica um problema com a configuração da Unificação de mensagens do Exchange.</span><span class="sxs-lookup"><span data-stu-id="9d743-145">This error message typically indicates a problem the configuration of Exchange Unified Messaging.</span></span>

<span data-ttu-id="9d743-146">Se Test-CsP2PAV falhar, talvez você queira executar novamente o teste, desta vez, incluindo o parâmetro Verbose:</span><span class="sxs-lookup"><span data-stu-id="9d743-146">If Test-CsP2PAV fails then you might want to rerun the test, this time including the Verbose parameter:</span></span>

<span data-ttu-id="9d743-147">Test-CsP2PAV-TargetFqdn "atl-cs-001.litwareinc.com"-detalhado</span><span class="sxs-lookup"><span data-stu-id="9d743-147">Test-CsP2PAV -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose</span></span>

<span data-ttu-id="9d743-148">Quando o parâmetro Verbose estiver incluído, Test-CsP2PAV retornará uma conta passo a passo de cada ação que tentou verificar se verificou a capacidade do usuário especificado de fazer logon no Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9d743-148">When the Verbose parameter is included, Test-CsP2PAV will return a step-by-step account of each action it tried as it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="9d743-149">Por exemplo, suponha que o teste falhou com o seguinte diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="9d743-149">For example, suppose that your test failed with the following Diagnosis:</span></span>

<span data-ttu-id="9d743-150">ErrorCode = 6003, Source = ATL-cs-001. litwareinc. com, Reason = incompatível solicitação de caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="9d743-150">ErrorCode=6003,Source=atl-cs-001.litwareinc.com,Reason=Unsupported out of dialog request</span></span>

<span data-ttu-id="9d743-151">Se você executar novamente Test-CsP2PAV e incluir o parâmetro Verbose, você receberá uma saída semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="9d743-151">If you rerun Test-CsP2PAV and include the Verbose parameter, you'll get output similar to this:</span></span>

<span data-ttu-id="9d743-152">VERBOse: atividade de ' registro ' iniciada.</span><span class="sxs-lookup"><span data-stu-id="9d743-152">VERBOSE: 'Register' activity started.</span></span>

<span data-ttu-id="9d743-153">Enviando solicitação de registro:</span><span class="sxs-lookup"><span data-stu-id="9d743-153">Sending Registration request:</span></span>

<span data-ttu-id="9d743-154">FQDN de destino = atl-cs-011.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="9d743-154">Target Fqdn = atl-cs-011.litwareinc.com</span></span>

<span data-ttu-id="9d743-155">Endereço SIP do usuário = sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="9d743-155">User Sip Address = sip:kenmyer@litwareinc.com</span></span>

<span data-ttu-id="9d743-156">Porta do registrador = 5062.</span><span class="sxs-lookup"><span data-stu-id="9d743-156">Registrar Port = 5062.</span></span>

<span data-ttu-id="9d743-157">O tipo de autenticação ' IWA ' é selecionado.</span><span class="sxs-lookup"><span data-stu-id="9d743-157">Auth Type 'IWA' is selected.</span></span>

<span data-ttu-id="9d743-158">Uma exceção ' o ponto de extremidade não pôde se registrar.</span><span class="sxs-lookup"><span data-stu-id="9d743-158">An exception 'The endpoint was unable to register.</span></span> <span data-ttu-id="9d743-159">Veja ErrorCode por motivo específico. '</span><span class="sxs-lookup"><span data-stu-id="9d743-159">See the ErrorCode for specific reason.'</span></span> <span data-ttu-id="9d743-160">ocorrido durante a execução do fluxo de trabalho Microsoft. RTC. SyntheticTransactions. workflows. STP2PAVWorkflow.</span><span class="sxs-lookup"><span data-stu-id="9d743-160">occurred during workflow Microsoft.Rtc.SyntheticTransactions.Workflows.STP2PAVWorkflow execution.</span></span>

<span data-ttu-id="9d743-161">Embora talvez não seja imediatamente óbvio, se você examinar a saída cuidadosamente, verá que uma porta de registrador incorreta (porta 5062) foi especificada.</span><span class="sxs-lookup"><span data-stu-id="9d743-161">Although it might not be immediately obvious, if you examine the output carefully you’ll see that an incorrect Registrar port (port 5062) was specified.</span></span> <span data-ttu-id="9d743-162">Por sua vez, isso fez com que o teste falhasse.</span><span class="sxs-lookup"><span data-stu-id="9d743-162">In turn, that caused the test to fail.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="9d743-163">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="9d743-163">Reasons why the test might have failed</span></span>

<span data-ttu-id="9d743-164">Veja a seguir alguns motivos comuns para que Test-CsP2PAV possam falhar:</span><span class="sxs-lookup"><span data-stu-id="9d743-164">Here are some common reasons why Test-CsP2PAV might fail:</span></span>

  - <span data-ttu-id="9d743-165">Você especificou uma conta de usuário que não é válida.</span><span class="sxs-lookup"><span data-stu-id="9d743-165">You specified a user account that is not valid.</span></span> <span data-ttu-id="9d743-166">Você pode verificar se existe uma conta de usuário executando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="9d743-166">You can verify that a user account exists by running a command similar to this:</span></span>
    
    <span data-ttu-id="9d743-167">Get-CsUser "sip:kenmyer@litwareinc.com"</span><span class="sxs-lookup"><span data-stu-id="9d743-167">Get-CsUser "sip:kenmyer@litwareinc.com"</span></span>

  - <span data-ttu-id="9d743-168">A conta de usuário é válida, mas a conta não está habilitada no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9d743-168">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="9d743-169">Para verificar se uma conta de usuário está habilitada para o Lync Server, execute um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="9d743-169">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="9d743-170">Se a propriedade Enabled estiver definida como false, isso significa que o usuário não está habilitado no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9d743-170">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

<span data-ttu-id="9d743-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9d743-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

