---
title: 'Lync Server 2013: testando a capacidade de enviar mensagens instantâneas entre dois usuários'
description: 'Lync Server 2013: testando a capacidade de enviar mensagens instantâneas entre dois usuários.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to IM between two users
ms:assetid: a0f3f5c6-f115-4c3f-90ac-5fdc932b417e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743838(v=OCS.15)
ms:contentKeyID: 63969635
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1409cfb58ed435a66dcf61db56660ca760e16422
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441092"
---
# <a name="testing-ability-to-im-between-two-users-in-lync-server-2013"></a><span data-ttu-id="5509b-103">Testar a capacidade de enviar mensagens instantâneas entre dois usuários no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5509b-103">Testing ability to IM between two users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5509b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5509b-104">

<span> </span></span></span>

<span data-ttu-id="5509b-105">_**Tópico da última modificação:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="5509b-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5509b-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="5509b-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="5509b-107">Diário</span><span class="sxs-lookup"><span data-stu-id="5509b-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5509b-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="5509b-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="5509b-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5509b-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5509b-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="5509b-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="5509b-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="5509b-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="5509b-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsIM.</span><span class="sxs-lookup"><span data-stu-id="5509b-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsIM cmdlet.</span></span> <span data-ttu-id="5509b-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="5509b-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsIM&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="5509b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5509b-114">Description</span></span>

<span data-ttu-id="5509b-115">O cmdlet Test-CsIM verifica se um par de usuários de teste podem trocar mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="5509b-115">The Test-CsIM cmdlet verifies that a pair of test users can exchange instant messages.</span></span> <span data-ttu-id="5509b-116">Quando chamado, o cmdlet Test-CsIM começa a tentar fazer logon em um par de usuários de teste para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5509b-116">When called, the Test-CsIM cmdlet starts off by trying to log on a pair of test users to Lync Server.</span></span> <span data-ttu-id="5509b-117">Pressupondo que os dois logons sejam bem-sucedidos, o cmdlet iniciará uma sessão de mensagem instantânea entre os dois usuários de teste.</span><span class="sxs-lookup"><span data-stu-id="5509b-117">Assuming the two logons are successful, the cmdlet then starts an IM session between the two test users.</span></span> <span data-ttu-id="5509b-118">(O usuário 1 convida o usuário 2 a uma sessão de mensagem instantânea, e o usuário 2 aceita o convite.) Depois de verificar se as mensagens podem ser trocadas entre os dois usuários, Test-CsIM, em seguida, encerra a sessão de mensagem instantânea e registra os dois usuários fora do sistema.</span><span class="sxs-lookup"><span data-stu-id="5509b-118">(User 1 invites User 2 to an IM session, and User 2 accepts the invitation.) After verifying that messages can be exchanged between the two users, Test-CsIM then ends the IM session and logs both users off the system.</span></span>

<span data-ttu-id="5509b-119">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsIM](https://docs.microsoft.com/powershell/module/skype/Test-CsIM) .</span><span class="sxs-lookup"><span data-stu-id="5509b-119">For more information, see the Help documentation for the [Test-CsIM](https://docs.microsoft.com/powershell/module/skype/Test-CsIM) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="5509b-120">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="5509b-120">Running the Test</span></span>

<span data-ttu-id="5509b-121">O cmdlet Test-CsIM pode ser executado usando um par de contas de teste pré-configuradas (consulte Configurando contas de teste para executar testes do Lync Server) ou as contas de dois usuários que estão habilitados para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5509b-121">The Test-CsIM cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="5509b-122">Para executar essa verificação usando contas de teste, basta especificar o FQDN do pool do servidor do Lync que está sendo testado.</span><span class="sxs-lookup"><span data-stu-id="5509b-122">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="5509b-123">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5509b-123">For example:</span></span>

    Test-CsIM -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="5509b-124">Para executar essa verificação usando contas de usuário reais, você deve criar dois objetos de credenciais do Windows PowerShell (objetos que contêm o nome da conta e a senha) para cada conta.</span><span class="sxs-lookup"><span data-stu-id="5509b-124">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="5509b-125">Em seguida, você deve incluir esses objetos de credenciais e os endereços SIP das duas contas ao chamar Test-CsIM:</span><span class="sxs-lookup"><span data-stu-id="5509b-125">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsIM:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsIm -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="5509b-126">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsIM](https://docs.microsoft.com/powershell/module/skype/Test-CsIM) .</span><span class="sxs-lookup"><span data-stu-id="5509b-126">For more information, see the Help documentation for the [Test-CsIM](https://docs.microsoft.com/powershell/module/skype/Test-CsIM) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="5509b-127">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="5509b-127">Determining Success or Failure</span></span>

<span data-ttu-id="5509b-128">Se os dois usuários puderem concluir uma sessão de mensagens instantâneas, você receberá uma saída semelhante a isso, com a propriedade Result marcada como **Success:**</span><span class="sxs-lookup"><span data-stu-id="5509b-128">If the two users can complete an instant messaging session, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="5509b-129">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="5509b-129">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="5509b-130">Resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="5509b-130">Result : Success</span></span>

<span data-ttu-id="5509b-131">Latência: 00:00:06.6630911</span><span class="sxs-lookup"><span data-stu-id="5509b-131">Latency : 00:00:06.6630911</span></span>

<span data-ttu-id="5509b-132">Erros</span><span class="sxs-lookup"><span data-stu-id="5509b-132">Error :</span></span>

<span data-ttu-id="5509b-133">Correto</span><span class="sxs-lookup"><span data-stu-id="5509b-133">Diagnosis :</span></span>

<span data-ttu-id="5509b-134">Se os usuários do teste não puderem concluir a sessão, o resultado será mostrado como uma falha, e informações adicionais serão gravadas nas propriedades de erro e diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="5509b-134">If the test users can't complete the session, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="5509b-135">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="5509b-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="5509b-136">Resultado: falha</span><span class="sxs-lookup"><span data-stu-id="5509b-136">Result : Failure</span></span>

<span data-ttu-id="5509b-137">Latência: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5509b-137">Latency : 00:00:00</span></span>

<span data-ttu-id="5509b-138">Erro: 504, tempo limite do servidor</span><span class="sxs-lookup"><span data-stu-id="5509b-138">Error : 504, Server time-out</span></span>

<span data-ttu-id="5509b-139">Diagnóstico: ErrorCode = 2, origem = ATL-cs-001. litwareinc. com, motivo = Veja</span><span class="sxs-lookup"><span data-stu-id="5509b-139">Diagnosis : ErrorCode=2, Source=atl-cs-001.litwareinc.com,Reason=See</span></span>

<span data-ttu-id="5509b-140">código de resposta e frase de motivo.</span><span class="sxs-lookup"><span data-stu-id="5509b-140">response code and reason phrase.</span></span>

<span data-ttu-id="5509b-141">Microsoft. RTC. Signaling. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="5509b-141">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="5509b-142">Por exemplo, a saída anterior informa que o teste falhou porque o usuário especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="5509b-142">For example, the previous output states that the test failed because the specified user couldn't be found.</span></span> <span data-ttu-id="5509b-143">Você pode determinar se um endereço SIP é válido (e se o usuário que atribuiu o endereço SIP foi habilitado para o Lync Server) executando este comando:</span><span class="sxs-lookup"><span data-stu-id="5509b-143">You can determine whether a SIP address is valid (and whether the user assigned that SIP address was enabled for Lync Server) by running this command:</span></span>

    Get-CsUser "Ken Myer" | Select-Object SipAddress, Enabled

<span data-ttu-id="5509b-144">Se Test-CsIM falhar, talvez você queira executar novamente o teste, desta vez, incluindo o parâmetro Verbose:</span><span class="sxs-lookup"><span data-stu-id="5509b-144">If Test-CsIM fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsIM -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="5509b-145">Quando o parâmetro Verbose estiver incluído, Test-CsIM retornará uma conta passo a passo de cada ação que tentou quando verificou a capacidade dos dois usuários de teste participarem de uma sessão de mensagem instantânea.</span><span class="sxs-lookup"><span data-stu-id="5509b-145">When the Verbose parameter is included, Test-CsIM will return a step-by-step account of each action it tried when it checked the ability of the two test users to take part in an IM session.</span></span> <span data-ttu-id="5509b-146">Por exemplo, veja a seguir uma saída de exemplo que ocorre quando um conjunto incorreto de credenciais de usuário (nesse caso, uma senha incorreta) é fornecido para Test-CsIM:</span><span class="sxs-lookup"><span data-stu-id="5509b-146">For example, here’s sample output that occurs when an incorrect set of user credentials (in this case, an incorrect password) is supplied to Test-CsIM:</span></span>

<span data-ttu-id="5509b-147">Enviando solicitação de registro:</span><span class="sxs-lookup"><span data-stu-id="5509b-147">Sending Registration request :</span></span>

<span data-ttu-id="5509b-148">FQDN de destino = atl-cs-011.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="5509b-148">Target Fqdn = atl-cs-011.litwareinc.com</span></span>

<span data-ttu-id="5509b-149">Endereço SIP do usuário = sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="5509b-149">User Sip Address = sip:kenmyer@litwareinc.com</span></span>

<span data-ttu-id="5509b-150">Porta do registrador = 5061</span><span class="sxs-lookup"><span data-stu-id="5509b-150">Registrar Port = 5061</span></span>

<span data-ttu-id="5509b-151">O tipo de autenticação ' IWA ' é selecionado.</span><span class="sxs-lookup"><span data-stu-id="5509b-151">Auth Type 'IWA' is selected.</span></span>

<span data-ttu-id="5509b-152">Acesso à inscrição em SIP/ATL-cs-001. litwareinc. com</span><span class="sxs-lookup"><span data-stu-id="5509b-152">Registration hit against sip/atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="5509b-153">Atividade ' Register ' concluída em ' 0, 601795 ' segundos.</span><span class="sxs-lookup"><span data-stu-id="5509b-153">'Register' activity completed in '0.0601795' secs.</span></span>

<span data-ttu-id="5509b-154">Uma exceção ' o logon foi negado.</span><span class="sxs-lookup"><span data-stu-id="5509b-154">An exception 'The log on was denied.</span></span> <span data-ttu-id="5509b-155">Verifique se as credenciais corretas estão sendo usadas e se a conta está ativa.</span><span class="sxs-lookup"><span data-stu-id="5509b-155">Check that the correct credentials are being used and the account is active.'</span></span> <span data-ttu-id="5509b-156">ocorridas durante o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5509b-156">occurred during the Workflow.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="5509b-157">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="5509b-157">Reasons Why the Test Might Have Failed</span></span>

<span data-ttu-id="5509b-158">Veja a seguir alguns motivos comuns para que Test-CsIM possam falhar:</span><span class="sxs-lookup"><span data-stu-id="5509b-158">Here are some common reasons why Test-CsIM might fail:</span></span>

  - <span data-ttu-id="5509b-159">Você especificou uma conta de usuário que não é válida.</span><span class="sxs-lookup"><span data-stu-id="5509b-159">You specified a user account that is not valid.</span></span> <span data-ttu-id="5509b-160">Você pode verificar se existe uma conta de usuário executando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="5509b-160">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="5509b-161">A conta de usuário é válida, mas a conta não está habilitada no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5509b-161">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="5509b-162">Para verificar se uma conta de usuário está habilitada para o Lync Server, execute um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="5509b-162">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="5509b-163">Se a propriedade Enabled estiver definida como false, isso significa que o usuário não está habilitado no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5509b-163">If the Enabled property is set to False that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="5509b-164">O serviço de mensagem instantânea pode não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="5509b-164">The instant messaging service might not be available.</span></span> <span data-ttu-id="5509b-165">Com o Lync Server, você pode configurar o sistema para que o sistema de mensagens instantâneas não esteja disponível se o banco de dados de arquivamento não puder ser acessado.</span><span class="sxs-lookup"><span data-stu-id="5509b-165">With Lync Server, you can configure the system so that IM is not available if the archiving database cannot be accessed.</span></span> <span data-ttu-id="5509b-166">Você pode verificar se está executando um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="5509b-166">You can verify that by running a command similar to the following:</span></span>
    
        Get-CsArchivingConfiguration -Identity "atl-cs-001.litwareinc.com" | Select-Object BlockOnArchiveFailure
    
    <span data-ttu-id="5509b-167">Se BlockOnArchiveFailure for definido como true, você deve determinar se o banco de dados de arquivamento está disponível.</span><span class="sxs-lookup"><span data-stu-id="5509b-167">If BlockOnArchiveFailure is set to True, then you should determine whether or not the archiving database is available.</span></span> <span data-ttu-id="5509b-168">Você pode retornar os locais dos bancos de dados de arquivamento usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="5509b-168">You can return the locations of your archiving databases by using the following command:</span></span>
    
        Get-CsService -ArchivingDatabase

  - <span data-ttu-id="5509b-169">O servidor de arquivamento pode não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="5509b-169">The Archiving server might not be available.</span></span> <span data-ttu-id="5509b-170">Você pode recuperar o FQDN dos seus servidores de arquivamento usando este comando:</span><span class="sxs-lookup"><span data-stu-id="5509b-170">You can retrieve the FQDN of your Archiving servers by using this command:</span></span>
    
        Get-CsService -ArchivingServer
    
    <span data-ttu-id="5509b-171">Em seguida, você pode executar ping no servidor apropriado para verificar se ele está disponível.</span><span class="sxs-lookup"><span data-stu-id="5509b-171">You can then ping the appropriate server to verify that it is available.</span></span> <span data-ttu-id="5509b-172">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5509b-172">For example:</span></span>
    
        ping atl-archiving-001.litwareinc.com

<span data-ttu-id="5509b-173"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5509b-173"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

