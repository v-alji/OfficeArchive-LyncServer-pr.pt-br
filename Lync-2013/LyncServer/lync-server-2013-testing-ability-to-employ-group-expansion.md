---
title: 'Lync Server 2013: testando a capacidade de empregar a expansão do grupo'
description: 'Lync Server 2013: testando a capacidade de empregar a expansão do grupo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to employ group expansion
ms:assetid: 9b0fc954-6f9c-411a-ab32-94ebabc42de2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743836(v=OCS.15)
ms:contentKeyID: 63969634
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6267bc2099fc420c5c57e1ef80f4bf4491334938
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441106"
---
# <a name="testing-ability-to-employ-group-expansion-in-lync-server-2013"></a><span data-ttu-id="36dba-103">Testar a capacidade de empregar a expansão de grupo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36dba-103">Testing ability to employ group expansion in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="36dba-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="36dba-104">

<span> </span></span></span>

<span data-ttu-id="36dba-105">_**Tópico da última modificação:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="36dba-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36dba-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="36dba-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="36dba-107">Diário</span><span class="sxs-lookup"><span data-stu-id="36dba-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36dba-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="36dba-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="36dba-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="36dba-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36dba-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="36dba-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="36dba-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="36dba-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="36dba-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsGroupExpansion.</span><span class="sxs-lookup"><span data-stu-id="36dba-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsGroupExpansion cmdlet.</span></span> <span data-ttu-id="36dba-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="36dba-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsGroupExpansion&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="36dba-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="36dba-114">Description</span></span>

<span data-ttu-id="36dba-115">O cmdlet Test-CsGroupExpansion permite determinar se a expansão de grupo está funcionando em sua organização.</span><span class="sxs-lookup"><span data-stu-id="36dba-115">The Test-CsGroupExpansion cmdlet lets you determine whether group expansion is working within your organization.</span></span> <span data-ttu-id="36dba-116">Quando a expansão de grupo está habilitada, os usuários configuram grupos de distribuição como um contato.</span><span class="sxs-lookup"><span data-stu-id="36dba-116">When group expansion is enabled, users configure distribution groups as a contact.</span></span> <span data-ttu-id="36dba-117">Isso significa que esses usuários podem enviar a mesma mensagem instantânea para todos os membros do grupo, endereçando a mensagem para o grupo em vez de a membros individuais desse grupo.</span><span class="sxs-lookup"><span data-stu-id="36dba-117">That means that those users can then send the same instant message to all the group members by addressing the message to the group instead of to individual members of that group.</span></span> <span data-ttu-id="36dba-118">A expansão de grupo permite exibir rápida e facilmente todos os membros do grupo e seu status atual.</span><span class="sxs-lookup"><span data-stu-id="36dba-118">Group expansion enables you to quickly and easily view all the group members and their current status.</span></span>

<span data-ttu-id="36dba-119">Com o cmdlet Test-CsGroupExpansion, você especifica um grupo de distribuição do Active Directory usando o endereço de email do grupo.</span><span class="sxs-lookup"><span data-stu-id="36dba-119">With the Test-CsGroupExpansion cmdlet, you specify an Active Directory distribution group by using the group’s email address.</span></span> <span data-ttu-id="36dba-120">Test-CsGroupExpansion, em seguida, usa a expansão de grupo para recuperar a associação de grupo e comparar a lista recuperada com a associação do endereço de email do grupo que você forneceu.</span><span class="sxs-lookup"><span data-stu-id="36dba-120">Test-CsGroupExpansion then uses group expansion to retrieve the group membership and compare the retrieved list to the membership of the group email address that you supplied.</span></span> <span data-ttu-id="36dba-121">Se houver correspondência entre as duas listas, a expansão do grupo funcionará corretamente.</span><span class="sxs-lookup"><span data-stu-id="36dba-121">If the two lists match, then group expansion is working correctly.</span></span> <span data-ttu-id="36dba-122">Observe que você pode testar a expansão do grupo de duas maneiras: testando o próprio serviço ou testando o serviço Web associado.</span><span class="sxs-lookup"><span data-stu-id="36dba-122">Note that you can test group expansion in two ways: by testing the service itself or by testing the associated web service.</span></span>

<span data-ttu-id="36dba-123">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) .</span><span class="sxs-lookup"><span data-stu-id="36dba-123">For more information, see the Help documentation for the [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="36dba-124">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="36dba-124">Running the test</span></span>

<span data-ttu-id="36dba-125">O cmdlet Test-CsGroupExpansion pode ser executado usando uma conta de teste pré-configurada (consulte Configurando contas de teste para executar testes do Lync Server) ou a conta de qualquer usuário habilitado para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="36dba-125">The Test-CsGroupExpansion cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who was enabled for Lync Server.</span></span> <span data-ttu-id="36dba-126">Para executar essa verificação usando uma conta de teste, basta especificar o FQDN do pool do servidor do Lync que está sendo testado e o endereço de email de um grupo de distribuição válido.</span><span class="sxs-lookup"><span data-stu-id="36dba-126">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested and the email address for a valid distribution group.</span></span> <span data-ttu-id="36dba-127">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="36dba-127">For example:</span></span>

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com"

<span data-ttu-id="36dba-128">Para executar essa verificação usando uma conta de usuário real, primeiro você deve criar um objeto de credenciais do Lync Server que contenha o nome da conta e a senha.</span><span class="sxs-lookup"><span data-stu-id="36dba-128">To run this check using an actual user account, you must first create a Lync Server credentials object that contains the account name and password.</span></span> <span data-ttu-id="36dba-129">Em seguida, você deve incluir esse objeto de credenciais e o endereço SIP atribuído à conta quando o sistema chamar Test-CsGroupExpansion:</span><span class="sxs-lookup"><span data-stu-id="36dba-129">You must then include that credentials object and the SIP address assigned to the account when the system calls Test-CsGroupExpansion:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="36dba-130">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) .</span><span class="sxs-lookup"><span data-stu-id="36dba-130">For more information, see the Help documentation for the [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="36dba-131">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="36dba-131">Determining success or failure</span></span>

<span data-ttu-id="36dba-132">Se o usuário especificado puder usar a expansão de grupo, você receberá uma saída semelhante a isso com a propriedade Result marcada como **Success:**</span><span class="sxs-lookup"><span data-stu-id="36dba-132">If the specified user can use group expansion, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="36dba-133">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="36dba-133">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="36dba-134">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="36dba-134">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="36dba-135">Resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="36dba-135">Result : Success</span></span>

<span data-ttu-id="36dba-136">Latência: 00:00:01.1234976</span><span class="sxs-lookup"><span data-stu-id="36dba-136">Latency : 00:00:01.1234976</span></span>

<span data-ttu-id="36dba-137">Erros</span><span class="sxs-lookup"><span data-stu-id="36dba-137">Error :</span></span>

<span data-ttu-id="36dba-138">Correto</span><span class="sxs-lookup"><span data-stu-id="36dba-138">Diagnosis :</span></span>

<span data-ttu-id="36dba-139">Se o usuário especificado não puder usar a expansão de grupo, o resultado será mostrado como falha e as informações adicionais serão gravadas nas propriedades de erro e diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="36dba-139">If the specified user can't use group expansion, then the Result will be shown as Failure and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="36dba-140">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="36dba-140">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="36dba-141">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="36dba-141">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="36dba-142">Resultado: falha</span><span class="sxs-lookup"><span data-stu-id="36dba-142">Result : Failure</span></span>

<span data-ttu-id="36dba-143">Latência: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="36dba-143">Latency : 00:00:00</span></span>

<span data-ttu-id="36dba-144">Erros</span><span class="sxs-lookup"><span data-stu-id="36dba-144">Error :</span></span>

<span data-ttu-id="36dba-145">Correto</span><span class="sxs-lookup"><span data-stu-id="36dba-145">Diagnosis :</span></span>

<span data-ttu-id="36dba-146">Test-CsGroupExpansion: o ponto de extremidade não pôde se registrar.</span><span class="sxs-lookup"><span data-stu-id="36dba-146">Test-CsGroupExpansion : The endpoint was unable to register.</span></span> <span data-ttu-id="36dba-147">Consulte ErrorCode por motivo específico.</span><span class="sxs-lookup"><span data-stu-id="36dba-147">See the ErrorCode for specific reason.</span></span>

<span data-ttu-id="36dba-148">A saída anterior informa que o teste falhou porque o usuário especificado não pôde se registrar no Lync Server.</span><span class="sxs-lookup"><span data-stu-id="36dba-148">The previous output states that the test failed because the specified user was unable to register with Lync Server.</span></span> <span data-ttu-id="36dba-149">Isso normalmente ocorrerá se a conta de teste não existir ou não tiver sido habilitada para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="36dba-149">This will typically occur if the test account does not exist or has not enabled for Lync Server.</span></span> <span data-ttu-id="36dba-150">Você pode verificar se a conta existe e determinar se a conta foi habilitada para nm-OCS-14-3ª executando um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="36dba-150">You can verify that the account exists, and determine whether or not the account has been enabled for nm-ocs-14-3rd by running a command similar to the following:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, Enabled

<span data-ttu-id="36dba-151">Se Test-CsGroupExpansion falhar, talvez você queira executar novamente o teste, desta vez, incluindo o parâmetro Verbose:</span><span class="sxs-lookup"><span data-stu-id="36dba-151">If Test-CsGroupExpansion fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -Verbose

<span data-ttu-id="36dba-152">Quando o parâmetro Verbose estiver incluído Test-CsGroupExpansion retornará uma conta passo a passo de cada ação que tentou verificar quando verificou a capacidade do usuário especificado de fazer logon no Lync Server.</span><span class="sxs-lookup"><span data-stu-id="36dba-152">When the Verbose parameter is included Test-CsGroupExpansion will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="36dba-153">Por exemplo, essa saída indica que o grupo de distribuição especificado não foi encontrado:</span><span class="sxs-lookup"><span data-stu-id="36dba-153">For example, this output indicates that the specified distribution group couldn't be found:</span></span>

<span data-ttu-id="36dba-154">Tentando obter a permissão na Web.</span><span class="sxs-lookup"><span data-stu-id="36dba-154">Trying to get web ticket.</span></span>

<span data-ttu-id="36dba-155">URL do serviço Web: https://atl-cs-001.litwareinc.com:443/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="36dba-155">Web Service url : https://atl-cs-001.litwareinc.com:443/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="36dba-156">Usando autenticação NTLM/Kerb.</span><span class="sxs-lookup"><span data-stu-id="36dba-156">Using NTLM/Kerb auth.</span></span>

<span data-ttu-id="36dba-157">GetWebTicketActivity concluído.</span><span class="sxs-lookup"><span data-stu-id="36dba-157">GetWebTicketActivity completed.</span></span>

<span data-ttu-id="36dba-158">Atividade "VerifyDistributionList" iniciada.</span><span class="sxs-lookup"><span data-stu-id="36dba-158">'VerifyDistributionList' activity started.</span></span>

<span data-ttu-id="36dba-159">O status da resposta do serviço Web DLX é: não encontrado.</span><span class="sxs-lookup"><span data-stu-id="36dba-159">DLX Web Service Response Status is: NotFound.</span></span>

<span data-ttu-id="36dba-160">Atividade ' VerifyDistributionList ' concluída em ' 0,2597923 ' segundos.</span><span class="sxs-lookup"><span data-stu-id="36dba-160">'VerifyDistributionList' activity completed in '0.2597923' secs.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="36dba-161">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="36dba-161">Reasons why the test might have failed</span></span>

<span data-ttu-id="36dba-162">Veja a seguir alguns motivos comuns para que Test-CsGroupExpansion possam falhar:</span><span class="sxs-lookup"><span data-stu-id="36dba-162">Here are some common reasons why Test-CsGroupExpansion might fail:</span></span>

  - <span data-ttu-id="36dba-163">Você especificou uma conta de usuário inválida.</span><span class="sxs-lookup"><span data-stu-id="36dba-163">You specified an invalid user account.</span></span> <span data-ttu-id="36dba-164">Você pode verificar se existe uma conta de usuário executando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="36dba-164">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="36dba-165">A conta de usuário é válida, mas a conta não está habilitada no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="36dba-165">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="36dba-166">Para verificar se uma conta de usuário foi habilitada para o Lync Server, execute um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="36dba-166">To verify that a user account was enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="36dba-167">Se a propriedade Enabled estiver definida como false, isso significa que o usuário não está habilitado no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="36dba-167">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="36dba-168">A expansão de grupo pode estar desabilitada.</span><span class="sxs-lookup"><span data-stu-id="36dba-168">Group expansion might be disabled.</span></span> <span data-ttu-id="36dba-169">É possível desativar a expansão do grupo.</span><span class="sxs-lookup"><span data-stu-id="36dba-169">It is possible to turn off group expansion.</span></span> <span data-ttu-id="36dba-170">Se a expansão do grupo tiver sido desabilitada, o cmdlet Test-CsGroupExpansion falhará.</span><span class="sxs-lookup"><span data-stu-id="36dba-170">If group expansion was disabled then the Test-CsGroupExpansion cmdlet will fail.</span></span> <span data-ttu-id="36dba-171">Para determinar se a expansão de grupo está habilitada, use um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="36dba-171">To determine whether group expansion is enabled, use a command similar to this:</span></span>
    
        Get-CsWebServiceConfiguration | Select-Object Identity, EnableGroupExpansion

<span data-ttu-id="36dba-172"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="36dba-172"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

