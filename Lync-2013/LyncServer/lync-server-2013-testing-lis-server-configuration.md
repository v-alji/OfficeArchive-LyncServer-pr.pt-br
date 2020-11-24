---
title: 'Lync Server 2013: testando a configuração do servidor LIS'
description: 'Lync Server 2013: testando a configuração do servidor LIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing LIS server configuration
ms:assetid: 6b06e7ab-522f-41a2-878b-e89cd4e3c6da
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690129(v=OCS.15)
ms:contentKeyID: 63969614
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba4d16d2ce48e3e5bb89e863f02902d05ce77bd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390043"
---
# <a name="testing-lis-server-configuration-in-lync-server-2013"></a><span data-ttu-id="cf595-103">Testando a configuração do servidor LIS no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf595-103">Testing LIS server configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cf595-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cf595-104">

<span> </span></span></span>

<span data-ttu-id="cf595-105">_**Tópico da última modificação:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="cf595-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf595-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="cf595-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="cf595-107">Diário</span><span class="sxs-lookup"><span data-stu-id="cf595-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf595-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="cf595-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="cf595-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="cf595-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf595-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="cf595-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="cf595-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="cf595-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="cf595-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsLisConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cf595-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsLisConfiguration cmdlet.</span></span> <span data-ttu-id="cf595-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="cf595-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLisConfiguration&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="cf595-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf595-114">Description</span></span>

<span data-ttu-id="cf595-115">O cmdlet Test-CsLisConfiguration verifica sua capacidade de entrar em contato com o serviço Web LIS.</span><span class="sxs-lookup"><span data-stu-id="cf595-115">The Test-CsLisConfiguration cmdlet verifies your ability to contact the LIS web service.</span></span> <span data-ttu-id="cf595-116">Se o serviço Web puder ser contatado, o teste será considerado um sucesso, independentemente de ser possível encontrar locais específicos.</span><span class="sxs-lookup"><span data-stu-id="cf595-116">If the web service can be contacted, then the test will be considered a success, regardless of whether any specific locations can be found.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="cf595-117">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="cf595-117">Running the test</span></span>

<span data-ttu-id="cf595-118">O cmdlet Test-CsLisConfguration pode ser executado usando uma conta de teste pré-configurada (consulte Configurando contas de teste para executar testes do Lync Server) ou a conta de qualquer usuário habilitado para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cf595-118">The Test-CsLisConfguration cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="cf595-119">Para executar essa verificação usando uma conta de teste, basta especificar o FQDN do pool do servidor do Lync que está sendo testado.</span><span class="sxs-lookup"><span data-stu-id="cf595-119">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="cf595-120">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="cf595-120">For example:</span></span>

    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="cf595-121">Para executar essa verificação usando uma conta de usuário real, primeiro você deve criar um objeto de credenciais do Windows PowerShell que contenha o nome da conta e a senha.</span><span class="sxs-lookup"><span data-stu-id="cf595-121">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="cf595-122">Em seguida, você deve incluir esse objeto de credenciais e o endereço SIP atribuído à conta ao chamar Test-CsLisConfiguration:</span><span class="sxs-lookup"><span data-stu-id="cf595-122">You must then include that credentials object and the SIP address assigned to the account when you call Test-CsLisConfiguration:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="cf595-123">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsLisConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsLisConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="cf595-123">For more information, see the Help documentation for the [Test-CsLisConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsLisConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="cf595-124">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="cf595-124">Determining success or failure</span></span>

<span data-ttu-id="cf595-125">Se o LIS estiver configurado corretamente, você receberá uma saída semelhante a isso, com a propriedade Result marcada como **Success:**</span><span class="sxs-lookup"><span data-stu-id="cf595-125">If the LIS is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="cf595-126">TargetUri : https://atl-cs-001.litwareinc.com:443/locationinformation/</span><span class="sxs-lookup"><span data-stu-id="cf595-126">TargetUri : https://atl-cs-001.litwareinc.com:443/locationinformation/</span></span>

<span data-ttu-id="cf595-127">liservice. svc</span><span class="sxs-lookup"><span data-stu-id="cf595-127">liservice.svc</span></span>

<span data-ttu-id="cf595-128">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="cf595-128">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="cf595-129">Resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="cf595-129">Result : Success</span></span>

<span data-ttu-id="cf595-130">Latência: 00:00:06.1616913</span><span class="sxs-lookup"><span data-stu-id="cf595-130">Latency : 00:00:06.1616913</span></span>

<span data-ttu-id="cf595-131">Erros</span><span class="sxs-lookup"><span data-stu-id="cf595-131">Error :</span></span>

<span data-ttu-id="cf595-132">Correto</span><span class="sxs-lookup"><span data-stu-id="cf595-132">Diagnosis :</span></span>

<span data-ttu-id="cf595-133">Se o usuário especificado não puder fazer logon ou logoff, o resultado será mostrado como uma falha, e informações adicionais serão gravadas nas propriedades de erro e diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="cf595-133">If the specified user can't log on or log off, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="cf595-134">TargetUri :</span><span class="sxs-lookup"><span data-stu-id="cf595-134">TargetUri :</span></span>

<span data-ttu-id="cf595-135">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="cf595-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="cf595-136">Resultado: falha</span><span class="sxs-lookup"><span data-stu-id="cf595-136">Result : Failure</span></span>

<span data-ttu-id="cf595-137">Latência: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="cf595-137">Latency : 00:00:00</span></span>

<span data-ttu-id="cf595-138">Erro: 11004, o nome solicitado é válido, mas não tem dados do pedido</span><span class="sxs-lookup"><span data-stu-id="cf595-138">Error : 11004, The requested name is valid but no data of the requested</span></span>

<span data-ttu-id="cf595-139">tipo encontrado</span><span class="sxs-lookup"><span data-stu-id="cf595-139">type was found</span></span>

<span data-ttu-id="cf595-140">Correto</span><span class="sxs-lookup"><span data-stu-id="cf595-140">Diagnosis :</span></span>

<span data-ttu-id="cf595-141">Test-CsLisConfiguration: nenhum cluster de correspondência localizado na topologia.</span><span class="sxs-lookup"><span data-stu-id="cf595-141">Test-CsLisConfiguration : No matching cluster found in topology.</span></span>

<span data-ttu-id="cf595-142">Por exemplo, a saída anterior inclui a observação "nenhum cluster correspondente encontrado na topologia".</span><span class="sxs-lookup"><span data-stu-id="cf595-142">For example, the previous output includes the note “No matching cluster found in topology.”</span></span> <span data-ttu-id="cf595-143">Isso geralmente indica um problema com o servidor de borda: o LIS usando o servidor de borda para se conectar ao provedor de serviços e validar os endereços.</span><span class="sxs-lookup"><span data-stu-id="cf595-143">That typically indicates a problem with the Edge Server: the LIS using the Edge Server to connect to the service provider and validate addresses.</span></span>

<span data-ttu-id="cf595-144">Se Test-CsLisConfiguration falhar, talvez você queira executar novamente o teste, desta vez, incluindo o parâmetro Verbose:</span><span class="sxs-lookup"><span data-stu-id="cf595-144">If Test-CsLisConfiguration fails then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="cf595-145">Quando o parâmetro Verbose estiver incluído, Test-CsLisConfiguration retornará uma conta passo a passo de cada ação que tentou verificar quando verificou a capacidade do usuário especificado para fazer logon no Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cf595-145">When the Verbose parameter is included, Test-CsLisConfiguration will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="cf595-146">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="cf595-146">For example:</span></span>

<span data-ttu-id="cf595-147">Serviço de informações de localização de chamadas.</span><span class="sxs-lookup"><span data-stu-id="cf595-147">Calling Location Information Service.</span></span>

<span data-ttu-id="cf595-148">Caminho do serviço = https://atl-cs-001.litwareinc.com:443/locationinformation/liservice.svc</span><span class="sxs-lookup"><span data-stu-id="cf595-148">Service Path = https://atl-cs-001.litwareinc.com:443/locationinformation/liservice.svc</span></span>

<span data-ttu-id="cf595-149">Subnet =</span><span class="sxs-lookup"><span data-stu-id="cf595-149">Subnet =</span></span>

<span data-ttu-id="cf595-150">BssId = 5</span><span class="sxs-lookup"><span data-stu-id="cf595-150">BssId = 5</span></span>

<span data-ttu-id="cf595-151">ChassisId =</span><span class="sxs-lookup"><span data-stu-id="cf595-151">ChassisId =</span></span>

<span data-ttu-id="cf595-152">Portid =</span><span class="sxs-lookup"><span data-stu-id="cf595-152">PortId =</span></span>

<span data-ttu-id="cf595-153">PortIdSubType = tipo indefinido</span><span class="sxs-lookup"><span data-stu-id="cf595-153">PortIdSubType = Undefined Type</span></span>

<span data-ttu-id="cf595-154">Mac</span><span class="sxs-lookup"><span data-stu-id="cf595-154">Mac</span></span>

<span data-ttu-id="cf595-155">Falha na solicitação de serviço Web de informações de localização de uma exceção com um código de resposta Item400. '</span><span class="sxs-lookup"><span data-stu-id="cf595-155">An exception 'Location Information Web Service request has failed with a response code Item400.'</span></span> <span data-ttu-id="cf595-156">ocorrido durante a execução do fluxo de trabalho Microsoft. RTC. SyntheticTrsnactions. workflows. STLisConfigurationWorkflow.</span><span class="sxs-lookup"><span data-stu-id="cf595-156">occurred during Workflow Microsoft.Rtc.SyntheticTrsnactions.Workflows.STLisConfigurationWorkflow execution.</span></span>

<span data-ttu-id="cf595-157">Se você examinar a saída anterior atentamente, verá que o cmdlet falhou após a tentativa de chamar o serviço de informações de localização.</span><span class="sxs-lookup"><span data-stu-id="cf595-157">If you examine the previous output closely, you’ll see that the cmdlet failed after it tried to call the Location Information Service.</span></span> <span data-ttu-id="cf595-158">Um dos parâmetros que foram usados nesta chamada foi o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cf595-158">One of the parameters that were used in that call was this:</span></span>

<span data-ttu-id="cf595-159">BssId = 5</span><span class="sxs-lookup"><span data-stu-id="cf595-159">BssId = 5</span></span>

<span data-ttu-id="cf595-160">Esse não é um valor válido para o BssID (Basic Service Set Identifier).</span><span class="sxs-lookup"><span data-stu-id="cf595-160">That’s not a valid value for the Basic Service Set Identifier (BssID).</span></span> <span data-ttu-id="cf595-161">Em vez disso, um BssID deve ser semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="cf595-161">Instead, a BssID should resemble this:</span></span>

<span data-ttu-id="cf595-162">12-34-56-78-90-AB</span><span class="sxs-lookup"><span data-stu-id="cf595-162">12-34-56-78-90-ab</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="cf595-163">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="cf595-163">Reasons why the test might have failed</span></span>

<span data-ttu-id="cf595-164">Veja a seguir alguns motivos comuns para que Test-CsLisConfiguration possam falhar:</span><span class="sxs-lookup"><span data-stu-id="cf595-164">Here are some common reasons why Test-CsLisConfiguration might fail:</span></span>

  - <span data-ttu-id="cf595-165">Um valor de parâmetro incorreto foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="cf595-165">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="cf595-166">Conforme mostrado no exemplo anterior, os parâmetros opcionais devem ser configurados corretamente ou o teste falhará.</span><span class="sxs-lookup"><span data-stu-id="cf595-166">As shown in the previous example, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="cf595-167">Execute o comando novamente sem os parâmetros opcionais e veja se isso é bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cf595-167">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

<span data-ttu-id="cf595-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cf595-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

