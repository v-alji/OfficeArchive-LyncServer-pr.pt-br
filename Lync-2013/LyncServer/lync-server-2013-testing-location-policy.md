---
title: 'Lync Server 2013: testando a política de localização'
description: 'Lync Server 2013: testando a política de localização.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing location policy
ms:assetid: 23d06fd3-31ee-4480-ba1e-d179a55b8b14
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690127(v=OCS.15)
ms:contentKeyID: 63969591
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4efc7ac6f3beef875ce1496b19b875ff252b145b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390041"
---
# <a name="testing-location-policy-in-lync-server-2013"></a><span data-ttu-id="69049-103">Testando a política de localização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="69049-103">Testing location policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="69049-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="69049-104">

<span> </span></span></span>

<span data-ttu-id="69049-105">_**Tópico da última modificação:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="69049-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69049-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="69049-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="69049-107">Diário</span><span class="sxs-lookup"><span data-stu-id="69049-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69049-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="69049-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="69049-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="69049-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69049-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="69049-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="69049-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="69049-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="69049-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsLocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="69049-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsLocationPolicy cmdlet.</span></span> <span data-ttu-id="69049-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="69049-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLocationPolicy&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="69049-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="69049-114">Description</span></span>

<span data-ttu-id="69049-115">O cmdlet Test-CsLocationPolicy verifica se uma política de localização está atribuída a um usuário.</span><span class="sxs-lookup"><span data-stu-id="69049-115">The Test-CsLocationPolicy cmdlet verifies that a location policy is assigned to a user.</span></span> <span data-ttu-id="69049-116">A política de localização é usada para aplicar configurações relacionadas à funcionalidade do E9-1-1 e ao local do cliente.</span><span class="sxs-lookup"><span data-stu-id="69049-116">The location policy is used to apply settings that relate to E9-1-1 functionality and client location.</span></span> <span data-ttu-id="69049-117">A política de localização determina se um usuário está habilitado para E9-1-1 e, se a resposta for "Sim", qual é o comportamento de uma chamada de emergência.</span><span class="sxs-lookup"><span data-stu-id="69049-117">The location policy determines whether a user is enabled for E9-1-1, and, if the answer is "yes,", what the behavior is of an emergency call.</span></span> <span data-ttu-id="69049-118">Por exemplo, você pode usar a política de localização para definir qual número constitui uma chamada de emergência (911 nos Estados Unidos), se a segurança corporativa deve ser notificada automaticamente e como a chamada deve ser roteada.</span><span class="sxs-lookup"><span data-stu-id="69049-118">For example, you can use the location policy to define what number makes up an emergency call (911 in the United States), whether corporate security should be automatically notified, and how the call should be routed.</span></span>

<span data-ttu-id="69049-119">Você pode testar políticas de localização em usuários ou em sub-redes de rede.</span><span class="sxs-lookup"><span data-stu-id="69049-119">You can test location policies on users or on network subnets.</span></span> <span data-ttu-id="69049-120">Se você executar o teste em uma sub-rede (especificando um valor para o parâmetro de sub-rede), o cmdlet tentará resolver a política de localização dessa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="69049-120">If you run the test against a subnet (by specifying a value for the Subnet parameter), the cmdlet will attempt to resolve the location policy for that subnet.</span></span> <span data-ttu-id="69049-121">Se nenhuma política de localização for atribuída à sub-rede, a política de localização para o usuário configurado será recuperada.</span><span class="sxs-lookup"><span data-stu-id="69049-121">If no location policy is assigned to the subnet, the location policy for the configured user will be retrieved.</span></span> <span data-ttu-id="69049-122">Se a política de sub-rede for recuperada com êxito, a saída incluirá um valor LocationPolicyTagID que começa com subnet-TagId.</span><span class="sxs-lookup"><span data-stu-id="69049-122">If the subnet policy is retrieved successfully, the output will include a LocationPolicyTagID value that begins with subnet-tagid.</span></span> <span data-ttu-id="69049-123">Se uma política de localização para a sub-rede não for encontrada, o LocationPolicyTagID começará com o User-TagId.</span><span class="sxs-lookup"><span data-stu-id="69049-123">If a location policy for the subnet was not found, the LocationPolicyTagID will begin with user-tagid.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="69049-124">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="69049-124">Running the test</span></span>

<span data-ttu-id="69049-125">O cmdlet Test-CsLocationPolicy pode ser executado usando uma conta de teste pré-configurada (consulte Configurando contas de teste para executar testes do Lync Server) ou a conta de qualquer usuário habilitado para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69049-125">The Test-CsLocationPolicy cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="69049-126">Para executar essa verificação usando uma conta de teste, basta especificar o FQDN do pool do servidor do Lync que está sendo testado.</span><span class="sxs-lookup"><span data-stu-id="69049-126">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="69049-127">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="69049-127">For example:</span></span>

    Test-CsLocationPolicy -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="69049-128">Para executar essa verificação usando uma conta de usuário real, primeiro você deve criar um objeto de credenciais do Windows PowerShell que contenha o nome da conta e a senha.</span><span class="sxs-lookup"><span data-stu-id="69049-128">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="69049-129">Em seguida, você deve incluir esse objeto de credenciais e o endereço SIP atribuído à conta ao chamar Test-CsLocationPolicy:</span><span class="sxs-lookup"><span data-stu-id="69049-129">You must then include that credentials object and the SIP address assigned to the account when you call Test-CsLocationPolicy:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsLocationPolicy -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="69049-130">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/Test-CsLocationPolicy) .</span><span class="sxs-lookup"><span data-stu-id="69049-130">For more information, see the Help documentation for the [Test-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/Test-CsLocationPolicy) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="69049-131">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="69049-131">Determining success or failure</span></span>

<span data-ttu-id="69049-132">Se o usuário especificado tiver uma política de local válida, você receberá uma saída semelhante a essa, com a propriedade Result marcada como **Success:**</span><span class="sxs-lookup"><span data-stu-id="69049-132">If the specified user has a valid location policy, then you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="69049-133">EnhancedEmergencyServicesEnabled: true</span><span class="sxs-lookup"><span data-stu-id="69049-133">EnhancedEmergencyServicesEnabled : true</span></span>

<span data-ttu-id="69049-134">LocationPolicyTagID: user-TagId</span><span class="sxs-lookup"><span data-stu-id="69049-134">LocationPolicyTagID : user-tagid</span></span>

<span data-ttu-id="69049-135">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="69049-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="69049-136">Resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="69049-136">Result : Success</span></span>

<span data-ttu-id="69049-137">Latência: 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="69049-137">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="69049-138">Erros</span><span class="sxs-lookup"><span data-stu-id="69049-138">Error :</span></span>

<span data-ttu-id="69049-139">Correto</span><span class="sxs-lookup"><span data-stu-id="69049-139">Diagnosis :</span></span>

<span data-ttu-id="69049-140">Se não for possível encontrar uma política de local válida para o usuário especificado, o resultado será mostrado como uma falha, e as informações adicionais serão gravadas nas propriedades erro e diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="69049-140">If a valid location policy cannot be found for the specified user, then Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="69049-141">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="69049-141">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="69049-142">Resultado: falha</span><span class="sxs-lookup"><span data-stu-id="69049-142">Result : Failure</span></span>

<span data-ttu-id="69049-143">Latência: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="69049-143">Latency : 00:00:00</span></span>

<span data-ttu-id="69049-144">Erro: 404, não encontrado</span><span class="sxs-lookup"><span data-stu-id="69049-144">Error : 404, Not Found</span></span>

<span data-ttu-id="69049-145">Diagnóstico: ErrorCode = 4005, Source = ATL-cs-001.litwareinc.com,</span><span class="sxs-lookup"><span data-stu-id="69049-145">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="69049-146">Motivo = o URI de destino não está habilitado para SIP ou não</span><span class="sxs-lookup"><span data-stu-id="69049-146">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="69049-147">Existem.</span><span class="sxs-lookup"><span data-stu-id="69049-147">exist.</span></span>

<span data-ttu-id="69049-148">Microsoft. RTC. Signaling. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="69049-148">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="69049-149">A saída anterior informa que o teste falhou porque o usuário especificado não é válido: ou a conta não existe ou o usuário não foi habilitado para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69049-149">The previous output states that the test failed because the specified user is not valid: either the account does not exist or the user has not been enabled for Lync Server.</span></span> <span data-ttu-id="69049-150">Você pode verificar a validade de uma conta e determinar se essa conta foi habilitada para nm-OCS-14-3º, executando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="69049-150">You can verify the validity of an account, and determine whether or not that account has been enabled for nm-ocs-14-3rd, by running a command similar to this:</span></span>

    Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, Enabled

<span data-ttu-id="69049-151">Se Test-CsLocationPolicy falhar, talvez você queira executar novamente o teste, desta vez, incluindo o parâmetro Verbose:</span><span class="sxs-lookup"><span data-stu-id="69049-151">If Test-CsLocationPolicy fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsLocationPolicy -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="69049-152">Quando o parâmetro Verbose estiver incluído, Test-CsLocationPolicy retornará uma conta passo a passo de cada ação que tentou ao verificar a política de localização.</span><span class="sxs-lookup"><span data-stu-id="69049-152">When the Verbose parameter is included, Test-CsLocationPolicy will return a step-by-step account of each action it tried when verifying the location policy.</span></span> <span data-ttu-id="69049-153">Por exemplo, essa saída indica que o Lync Server não pôde fazer logon no usuário de teste, provavelmente porque foi fornecida uma senha inválida:</span><span class="sxs-lookup"><span data-stu-id="69049-153">For example, this output indicates that Lync Server couldn't log on the test user, probably because an invalid password was supplied:</span></span>

<span data-ttu-id="69049-154">Enviando solicitação de registro:</span><span class="sxs-lookup"><span data-stu-id="69049-154">Sending Registration request :</span></span>

<span data-ttu-id="69049-155">FQDN de destino = atl-cs-011.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="69049-155">Target Fqdn = atl-cs-011.litwareinc.com</span></span>

<span data-ttu-id="69049-156">Endereço SIP do usuário = sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="69049-156">User Sip Address = sip:kenmyer@litwareinc.com</span></span>

<span data-ttu-id="69049-157">Porta do registrador = 5061</span><span class="sxs-lookup"><span data-stu-id="69049-157">Registrar Port = 5061</span></span>

<span data-ttu-id="69049-158">O tipo de autenticação ' IWA ' é selecionado.</span><span class="sxs-lookup"><span data-stu-id="69049-158">Auth Type 'IWA' is selected.</span></span>

<span data-ttu-id="69049-159">Acesso à inscrição em SIP/ATL-cs-001. litwareinc. com</span><span class="sxs-lookup"><span data-stu-id="69049-159">Registration hit against sip/atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="69049-160">Atividade ' Register ' concluída em ' 0, 601795 ' segundos.</span><span class="sxs-lookup"><span data-stu-id="69049-160">'Register' activity completed in '0.0601795' secs.</span></span>

<span data-ttu-id="69049-161">Uma exceção ' o logon foi negado.</span><span class="sxs-lookup"><span data-stu-id="69049-161">An exception 'The log on was denied.</span></span> <span data-ttu-id="69049-162">Verifique se as credenciais corretas estão sendo usadas e se a conta está ativa.</span><span class="sxs-lookup"><span data-stu-id="69049-162">Check that the correct credentials are being used and the account is active.'</span></span> <span data-ttu-id="69049-163">ocorridas durante o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="69049-163">occurred during the Workflow.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="69049-164">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="69049-164">Reasons why the test might have failed</span></span>

<span data-ttu-id="69049-165">Veja a seguir alguns motivos comuns para que Test-CsLocationPolicy possam falhar:</span><span class="sxs-lookup"><span data-stu-id="69049-165">Here are some common reasons why Test-CsLocationPolicy might fail:</span></span>

  - <span data-ttu-id="69049-166">Você especificou uma conta de usuário que não é válida.</span><span class="sxs-lookup"><span data-stu-id="69049-166">You specified a user account that is not valid.</span></span> <span data-ttu-id="69049-167">Você pode verificar se existe uma conta de usuário executando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="69049-167">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="69049-168">A conta de usuário é válida, mas a conta não está habilitada no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69049-168">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="69049-169">Para verificar se uma conta de usuário está habilitada para o Lync Server, execute um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="69049-169">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="69049-170">Se a propriedade Enabled estiver definida como false, isso significa que o usuário não está habilitado no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69049-170">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

<span data-ttu-id="69049-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="69049-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

