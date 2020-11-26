---
title: 'Lync Server 2013: testando a capacidade de fazer mensagens instantâneas em grupo'
description: 'Lync Server 2013: testando a capacidade de fazer mensagens instantâneas em grupo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to do group IM
ms:assetid: ca5545bc-51ac-490f-b96b-917bb742ad04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743839(v=OCS.15)
ms:contentKeyID: 63969652
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f6988a0c1a7ba569f7b4da098ae741beab5e14fa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441099"
---
# <a name="testing-ability-to-do-group-im-in-lync-server-2013"></a><span data-ttu-id="00df8-103">Testar a capacidade de fazer mensagens instantâneas em grupo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="00df8-103">Testing ability to do group IM in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="00df8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="00df8-104">

<span> </span></span></span>

<span data-ttu-id="00df8-105">_**Tópico da última modificação:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="00df8-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00df8-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="00df8-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="00df8-107">Diário</span><span class="sxs-lookup"><span data-stu-id="00df8-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00df8-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="00df8-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="00df8-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="00df8-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00df8-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="00df8-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="00df8-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="00df8-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="00df8-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsGroupIM.</span><span class="sxs-lookup"><span data-stu-id="00df8-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsGroupIM cmdlet.</span></span> <span data-ttu-id="00df8-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="00df8-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsGroupIM&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="00df8-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="00df8-114">Description</span></span>

<span data-ttu-id="00df8-115">O cmdlet Test-CsGroupIM verifica se os usuários em sua organização podem conduzir sessões de mensagens instantâneas em grupo.</span><span class="sxs-lookup"><span data-stu-id="00df8-115">The Test-CsGroupIM cmdlet verifies that users in your organization can conduct group instant messaging sessions.</span></span> <span data-ttu-id="00df8-116">Ao executar Test-CsGroupIM, o cmdlet tenta entrar em um par de usuários de teste para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="00df8-116">When you run Test-CsGroupIM, the cmdlet attempts to sign in a pair of test users to Lync Server.</span></span> <span data-ttu-id="00df8-117">Se for bem-sucedida, Test-CsGroupIM criar uma nova conferência usando o primeiro usuário de teste e convidar o segundo usuário para ingressar na conferência.</span><span class="sxs-lookup"><span data-stu-id="00df8-117">If successful, Test-CsGroupIM creates a new conference using the first test user, then invites the second user to join the conference.</span></span> <span data-ttu-id="00df8-118">Após uma troca de mensagens, os dois usuários são desconectados do sistema.</span><span class="sxs-lookup"><span data-stu-id="00df8-118">After an exchange of messages, both users are then disconnected from the system.</span></span> <span data-ttu-id="00df8-119">Observe que tudo isso acontece sem qualquer interação do usuário e sem afetar os usuários reais.</span><span class="sxs-lookup"><span data-stu-id="00df8-119">Note that all of this happens without any user interaction, and without affecting any actual users.</span></span> <span data-ttu-id="00df8-120">Por exemplo, suponha que o sip:kenmyer@litwareinc.com da conta de teste corresponda a um usuário real que tenha uma conta real do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="00df8-120">For example, suppose that the test account sip:kenmyer@litwareinc.com corresponds to a real user who has a real Lync Server account.</span></span> <span data-ttu-id="00df8-121">Nesse caso, o teste será realizado sem qualquer interrupção no Ken Myer verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="00df8-121">In that case, the test will be conducted without any disruption to the real Ken Myer.</span></span> <span data-ttu-id="00df8-122">Por exemplo, mesmo quando a conta de teste de Ken Myer se desconecta do sistema, Ken Myer a pessoa permanecerá conectada.</span><span class="sxs-lookup"><span data-stu-id="00df8-122">For example, even when the Ken Myer test account logs off from the system, Ken Myer the person will remain logged on.</span></span> <span data-ttu-id="00df8-123">Da mesma forma, o "Ken Myer" realmente não receberá um convite para participar da conferência.</span><span class="sxs-lookup"><span data-stu-id="00df8-123">Likewise, the real Ken Myer won't receive an invitation to join the conference.</span></span> <span data-ttu-id="00df8-124">Este convite será enviado para e aceito pela conta de teste.</span><span class="sxs-lookup"><span data-stu-id="00df8-124">That invitation will be sent to, and accepted by, the test account.</span></span>

<span data-ttu-id="00df8-125">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) .</span><span class="sxs-lookup"><span data-stu-id="00df8-125">For more information, see the Help documentation for the [Test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="00df8-126">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="00df8-126">Running the test</span></span>

<span data-ttu-id="00df8-127">O cmdlet Test-CsGroupIM pode ser executado usando um par de contas de teste pré-configuradas (consulte Configurando contas de teste para executar testes do Lync Server) ou as contas de dois usuários que estão habilitados para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="00df8-127">The Test-CsGroupIM cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="00df8-128">Para executar essa verificação usando contas de teste, basta especificar o FQDN do pool do servidor do Lync que está sendo testado.</span><span class="sxs-lookup"><span data-stu-id="00df8-128">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="00df8-129">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="00df8-129">For example:</span></span>

    Test-CsGroupIM -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="00df8-130">Para executar essa verificação usando contas de usuário reais, você deve criar dois objetos de credenciais do Shell de gerenciamento do Lync Server (objetos que contêm o nome e a senha da conta) para cada conta.</span><span class="sxs-lookup"><span data-stu-id="00df8-130">To run this check using actual user accounts, you must create two Lync Server Management Shell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="00df8-131">Em seguida, você deve incluir esses objetos de credenciais e os endereços SIP das duas contas ao chamar Test-CsGroupIM:</span><span class="sxs-lookup"><span data-stu-id="00df8-131">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsGroupIM:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsGroupIm -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="00df8-132">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) .</span><span class="sxs-lookup"><span data-stu-id="00df8-132">For more information, see the Help documentation for the [Test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="00df8-133">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="00df8-133">Determining Success or Failure</span></span>

<span data-ttu-id="00df8-134">Se os dois usuários puderem concluir uma sessão de mensagens instantâneas em grupo, você receberá uma saída semelhante a isso com a propriedade Result marcada como **Success:**</span><span class="sxs-lookup"><span data-stu-id="00df8-134">If the two users can complete a group instant messaging session, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="00df8-135">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="00df8-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="00df8-136">Resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="00df8-136">Result : Success</span></span>

<span data-ttu-id="00df8-137">Latência: 00:00:06.3812203</span><span class="sxs-lookup"><span data-stu-id="00df8-137">Latency : 00:00:06.3812203</span></span>

<span data-ttu-id="00df8-138">Erros</span><span class="sxs-lookup"><span data-stu-id="00df8-138">Error :</span></span>

<span data-ttu-id="00df8-139">Correto</span><span class="sxs-lookup"><span data-stu-id="00df8-139">Diagnosis :</span></span>

<span data-ttu-id="00df8-140">Se os dois usuários não puderem concluir a sessão de mensagens instantâneas, o resultado será mostrado como uma falha, e informações adicionais serão gravadas nas propriedades de erro e diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="00df8-140">If the two users can't able to complete the instant messaging session, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="00df8-141">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="00df8-141">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="00df8-142">Resultado: falha</span><span class="sxs-lookup"><span data-stu-id="00df8-142">Result : Failure</span></span>

<span data-ttu-id="00df8-143">Latência: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="00df8-143">Latency : 00:00:00</span></span>

<span data-ttu-id="00df8-144">Erro: 404, não encontrado</span><span class="sxs-lookup"><span data-stu-id="00df8-144">Error : 404, Not Found</span></span>

<span data-ttu-id="00df8-145">Diagnóstico: ErrorCode = 4005, Source = ATL-cs-001.litwareinc.com,</span><span class="sxs-lookup"><span data-stu-id="00df8-145">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="00df8-146">Motivo = o URI de destino não está habilitado para SIP ou não</span><span class="sxs-lookup"><span data-stu-id="00df8-146">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="00df8-147">Existem.</span><span class="sxs-lookup"><span data-stu-id="00df8-147">exist.</span></span>

<span data-ttu-id="00df8-148">Microsoft. RTC. Signaling. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="00df8-148">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="00df8-149">A saída anterior informa que o teste falhou porque, pelo menos uma das contas de teste não era válida, porque a conta não existe ou porque o usuário não foi habilitado para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="00df8-149">The previous output states that the test failed because at least one of the test accounts was not valid, either because the account does not exist or because the user has not been enabled for Lync Server.</span></span> <span data-ttu-id="00df8-150">Você pode verificar se a conta existe e se a conta foi habilitada para nm-OCS-14-3ª executando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="00df8-150">You can verify the account exists, and whether or not the account has been enabled for nm-ocs-14-3rd by running a command similar to this:</span></span>

    "Ken Myer", "David Longmire" | Get-CsUser | Select-Object SipAddress, Enabled

<span data-ttu-id="00df8-151">Se Test-CsGroupIM falhar, talvez você queira executar novamente o teste, desta vez, incluindo o parâmetro Verbose:</span><span class="sxs-lookup"><span data-stu-id="00df8-151">If Test-CsGroupIM fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsGroupIM -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="00df8-152">Quando o parâmetro Verbose estiver incluído, Test-CsGroupIM retornará uma conta passo a passo de cada ação que tentou verificar quando verificou a capacidade dos usuários especificados para participar de sessões de mensagens instantâneas em grupo.</span><span class="sxs-lookup"><span data-stu-id="00df8-152">When the Verbose parameter is included, Test-CsGroupIM will return a step-by-step account of each action it tried when it checked the ability of the specified users to participate in a group instant messaging sessions.</span></span> <span data-ttu-id="00df8-153">Por exemplo, se o teste falhar e você for informado de que uma ou mais contas de usuário não são válidas, você pode executar novamente o teste usando o parâmetro Verbose e determinar qual conta de usuário não é válida:</span><span class="sxs-lookup"><span data-stu-id="00df8-153">For example, if your test fails and you are told that one or more of the user accounts is not valid, you can rerun the test using the Verbose parameter and determine which user account is not valid:</span></span>

<span data-ttu-id="00df8-154">Enviando solicitação de registro:</span><span class="sxs-lookup"><span data-stu-id="00df8-154">Sending Registration request:</span></span>

 <span data-ttu-id="00df8-155">FQDN de destino = atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="00df8-155">Target Fqdn      = atl-cs-001.litwareinc.com</span></span>

 <span data-ttu-id="00df8-156">Endereço SIP do usuário = sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="00df8-156">User SIP Address = sip:kenmyer@litwareinc.com</span></span>

 <span data-ttu-id="00df8-157">Porta do registro = 5061</span><span class="sxs-lookup"><span data-stu-id="00df8-157">Register Port    = 5061</span></span>

<span data-ttu-id="00df8-158">O tipo de autenticação ' IWA ' é selecionado.</span><span class="sxs-lookup"><span data-stu-id="00df8-158">Auth type 'IWA' is selected.</span></span>

<span data-ttu-id="00df8-159">Uma exceção ' o logon foi negado.</span><span class="sxs-lookup"><span data-stu-id="00df8-159">An exception 'The log on was denied.</span></span> <span data-ttu-id="00df8-160">Verifique se as credenciais corretas estão sendo usadas e se a conta está ativa</span><span class="sxs-lookup"><span data-stu-id="00df8-160">Check that the correct credentials are being used and the account is active'</span></span>

<span data-ttu-id="00df8-161">Como você pode ver, neste exemplo, o usuário que tem o endereço SIP sip:kenmyer@litwareinc.com não pôde fazer logon.</span><span class="sxs-lookup"><span data-stu-id="00df8-161">As you can see, in this example the user who has the SIP address sip:kenmyer@litwareinc.com was not able to log on.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="00df8-162">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="00df8-162">Reasons why the test might have failed</span></span>

<span data-ttu-id="00df8-163">Veja a seguir alguns motivos comuns para que Test-CsGroupIM possam falhar:</span><span class="sxs-lookup"><span data-stu-id="00df8-163">Here are some common reasons why Test-CsGroupIM might fail:</span></span>

  - <span data-ttu-id="00df8-164">Você especificou uma conta de usuário incorreta.</span><span class="sxs-lookup"><span data-stu-id="00df8-164">You specified an incorrect user account.</span></span> <span data-ttu-id="00df8-165">Você pode verificar se existe uma conta de usuário executando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="00df8-165">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="00df8-166">A conta de usuário é válida, mas a conta não está habilitada no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="00df8-166">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="00df8-167">Para verificar se uma conta de usuário foi habilitada para o Lync Server, execute um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="00df8-167">To verify that a user account was enabled for Lync Server, run a command similar to the following:</span></span>
    
    <span data-ttu-id="00df8-168">Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object habilitado</span><span class="sxs-lookup"><span data-stu-id="00df8-168">Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled</span></span>
    
    <span data-ttu-id="00df8-169">Se a propriedade Enabled estiver definida como false, isso significa que o usuário não está habilitado no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="00df8-169">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="00df8-170">O serviço de mensagem instantânea pode não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="00df8-170">The instant messaging service might not be available.</span></span> <span data-ttu-id="00df8-171">Com o Lync Server, você pode configurar o sistema para que o sistema de mensagens instantâneas não esteja disponível se o banco de dados de arquivamento não puder ser acessado.</span><span class="sxs-lookup"><span data-stu-id="00df8-171">With Lync Server, you can configure the system so that instant messaging is not available if the archiving database cannot be accessed.</span></span> <span data-ttu-id="00df8-172">Você pode verificar se está executando um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="00df8-172">You can verify that by running a command similar to the following:</span></span>
    
        Get-CsArchivingConfiguration -Identity "atl-cs-001.litwareinc.com" | Select-Object BlockOnArchiveFailure
    
    <span data-ttu-id="00df8-173">Se BlockOnArchiveFailure for definido como true, você deve determinar se o banco de dados de arquivamento está disponível.</span><span class="sxs-lookup"><span data-stu-id="00df8-173">If BlockOnArchiveFailure is set to True, then you should determine whether or not the archiving database is available.</span></span> <span data-ttu-id="00df8-174">Você pode retornar os locais dos bancos de dados de arquivamento usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="00df8-174">You can return the locations of your archiving databases by using the following command:</span></span>
    
        Get-CsService -ArchivingDatabase

  - <span data-ttu-id="00df8-175">O servidor de arquivamento pode não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="00df8-175">The Archiving Server might not be available.</span></span> <span data-ttu-id="00df8-176">Você pode recuperar o FQDN dos seus servidores de arquivamento usando este comando:</span><span class="sxs-lookup"><span data-stu-id="00df8-176">You can retrieve the FQDN of your Archiving Servers by using this command:</span></span>
    
        Get-CsService -ArchivingServer
    
    <span data-ttu-id="00df8-177">Em seguida, você pode executar ping no servidor apropriado para verificar se ele está disponível.</span><span class="sxs-lookup"><span data-stu-id="00df8-177">You can then ping the appropriate server to verify that it is available.</span></span> <span data-ttu-id="00df8-178">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="00df8-178">For example:</span></span>
    
        ping atl-archiving-001.litwareinc.com

<span data-ttu-id="00df8-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="00df8-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

