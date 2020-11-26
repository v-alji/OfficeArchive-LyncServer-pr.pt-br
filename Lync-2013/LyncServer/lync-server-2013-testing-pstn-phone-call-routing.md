---
title: 'Lync Server 2013: testando o encaminhamento de chamadas telefônicas PSTN'
description: 'Lync Server 2013: testando o roteamento de chamadas telefônicas PSTN.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing PSTN phone call routing
ms:assetid: 301dd44d-03e9-41cd-9722-54e00365aa45
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727302(v=OCS.15)
ms:contentKeyID: 63969598
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da931b43176932a9b6781fa27318e83e6994548c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440987"
---
# <a name="testing-pstn-phone-call-routing-in-lync-server-2013"></a><span data-ttu-id="d6b49-103">Testando o roteamento de chamadas telefônicas PSTN no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6b49-103">Testing PSTN phone call routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d6b49-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d6b49-104">

<span> </span></span></span>

<span data-ttu-id="d6b49-105">_**Tópico da última modificação:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="d6b49-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6b49-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="d6b49-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="d6b49-107">Diário</span><span class="sxs-lookup"><span data-stu-id="d6b49-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6b49-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="d6b49-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="d6b49-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6b49-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6b49-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="d6b49-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="d6b49-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="d6b49-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="d6b49-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet <strong>Test-CsInterTrunkRouting</strong> .</span><span class="sxs-lookup"><span data-stu-id="d6b49-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsInterTrunkRouting</strong> cmdlet.</span></span> <span data-ttu-id="d6b49-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="d6b49-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsInterTrunkRouting&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="d6b49-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6b49-114">Description</span></span>

<span data-ttu-id="d6b49-115">O cmdlet **Test-CsInterTrunkRouting** verifica se as chamadas podem ser roteadas de um SIP para outro.</span><span class="sxs-lookup"><span data-stu-id="d6b49-115">The **Test-CsInterTrunkRouting** cmdlet verifies that calls can be routed from one SIP to another.</span></span> <span data-ttu-id="d6b49-116">Para fazer isso, o cmdlet recebe um número de telefone e uma configuração de tronco.</span><span class="sxs-lookup"><span data-stu-id="d6b49-116">To do this, the cmdlet is given a phone number and a trunk configuration.</span></span> <span data-ttu-id="d6b49-117">**Test-CsInterTrunkRouting** reportará os roteiros correspondentes e os usos de PSTN correspondentes para o número especificado.</span><span class="sxs-lookup"><span data-stu-id="d6b49-117">**Test-CsInterTrunkRouting** will then report back matching routes and matching PSTN usages for the specified number.</span></span> <span data-ttu-id="d6b49-118">Observe que as chamadas podem ser roteadas entre troncos apenas se os troncos possuem um padrão de número que corresponde ao número de telefone especificado e apenas se os troncos compartilham pelo menos um uso PSTN.</span><span class="sxs-lookup"><span data-stu-id="d6b49-118">Note that calls can be routed between trunks only if the trunks have a number pattern that matches the specified phone number and only if the trunks share at least one PSTN usage.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="d6b49-119">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="d6b49-119">Running the test</span></span>

<span data-ttu-id="d6b49-120">Os comandos exibidos abaixo retornam as rotas correspondentes e os usos de telefone correspondentes que permitem que os usuários chamem o número de telefone 1-206-555-1219 usando as configurações de tronco de configuração para o site de Redmond.</span><span class="sxs-lookup"><span data-stu-id="d6b49-120">The commands shown below return the matching routes and matching phone usages that enable users to call the phone number 1-206-555-1219 using the trunk configuration settings for the Redmond site.</span></span>

    $trunk = Get-CsTrunkConfiguration -Identity "site:Redmond"
    
    Test-CsInterTrunkRouting -TargetNumber "tel:+12065551219" -TrunkConfiguration $trunk

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="d6b49-121">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="d6b49-121">Determining success or failure</span></span>

<span data-ttu-id="d6b49-122">Se as chamadas puderem ser roteadas de um SIP para outro, você receberá uma saída semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="d6b49-122">If calls can be routed from one SIP to another, you'll receive output similar to this:</span></span>

<span data-ttu-id="d6b49-123">FirstMatchingRoute MatchingUsage MatchingRoutes</span><span class="sxs-lookup"><span data-stu-id="d6b49-123">FirstMatchingRoute MatchingUsage MatchingRoutes</span></span>

<span data-ttu-id="d6b49-124">\------------------ ------------- --------------</span><span class="sxs-lookup"><span data-stu-id="d6b49-124">\------------------ ------------- --------------</span></span>

<span data-ttu-id="d6b49-125">RedmondRoute LocalUsage {RedmondRoute}</span><span class="sxs-lookup"><span data-stu-id="d6b49-125">RedmondRoute LocalUsage {RedmondRoute}</span></span>

<span data-ttu-id="d6b49-126">Se o teste não for bem-sucedido, você receberá uma saída semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="d6b49-126">If the test did not succeed, you'll receive output similar to this:</span></span>

<span data-ttu-id="d6b49-127">Test-CsInterTrunkRouting: não é possível processar a transformação do argumento no parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6b49-127">Test-CsInterTrunkRouting : Cannot process argument transformation on parameter</span></span>

<span data-ttu-id="d6b49-128">'TrunkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="d6b49-128">'TrunkConfiguration'.</span></span> <span data-ttu-id="d6b49-129">TrunkConfigurationsetting (parâmetro) inválido.</span><span class="sxs-lookup"><span data-stu-id="d6b49-129">Invalid TrunkConfigurationsetting (parameter).</span></span> <span data-ttu-id="d6b49-130">Especificar um</span><span class="sxs-lookup"><span data-stu-id="d6b49-130">Specify a</span></span>

<span data-ttu-id="d6b49-131">configuração válida (parâmetro) e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="d6b49-131">valid setting (parameter) and then try again.</span></span>

<span data-ttu-id="d6b49-132">Na linha: 1 caractere: 79</span><span class="sxs-lookup"><span data-stu-id="d6b49-132">At line:1 char:79</span></span>

<span data-ttu-id="d6b49-133">\+ Test-CsInterTrunkRouting-TargetNumber "Tel: + 12065551219"</span><span class="sxs-lookup"><span data-stu-id="d6b49-133">\+ Test-CsInterTrunkRouting -TargetNumber "tel:+12065551219"</span></span>

<span data-ttu-id="d6b49-134">\-TrunkConfiguration $t...</span><span class="sxs-lookup"><span data-stu-id="d6b49-134">\-TrunkConfiguration $t ...</span></span>

\+

~~

<span data-ttu-id="d6b49-135">\+ CategoryInfo: InvalidData: (:) \[ Test-CsInterTrunkRouting \] , par</span><span class="sxs-lookup"><span data-stu-id="d6b49-135">\+ CategoryInfo : InvalidData: (:) \[Test-CsInterTrunkRouting\], Par</span></span>

<span data-ttu-id="d6b49-136">ameterBindingArgumentTransformationException</span><span class="sxs-lookup"><span data-stu-id="d6b49-136">ameterBindingArgumentTransformationException</span></span>

<span data-ttu-id="d6b49-137">\+ FullyQualifiedErrorId: ParameterArgumentTransformationError, Microsoft. R</span><span class="sxs-lookup"><span data-stu-id="d6b49-137">\+ FullyQualifiedErrorId : ParameterArgumentTransformationError,Microsoft.R</span></span>

<span data-ttu-id="d6b49-138">TC. Management. Voice. cmdlets. TestOcsInterTrunkRoutingCmdlet</span><span class="sxs-lookup"><span data-stu-id="d6b49-138">tc.Management.Voice.Cmdlets.TestOcsInterTrunkRoutingCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="d6b49-139">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="d6b49-139">Reasons why the test might have failed</span></span>

<span data-ttu-id="d6b49-140">Aqui estão alguns motivos comuns pelos quais **Test-CsInterTrunkRouting** pode falhar:</span><span class="sxs-lookup"><span data-stu-id="d6b49-140">Here are some common reasons why **Test-CsInterTrunkRouting** might fail:</span></span>

  - <span data-ttu-id="d6b49-141">Você especificou parâmetros inválidos.</span><span class="sxs-lookup"><span data-stu-id="d6b49-141">You specified invalid parameters.</span></span> <span data-ttu-id="d6b49-142">O tronco pode não estar corretamente configurado e o número de destino especificado pode estar incorreto ou inválido.</span><span class="sxs-lookup"><span data-stu-id="d6b49-142">The trunk might not yet be correctly configured and the specified target number might be incorrect or invalid.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d6b49-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6b49-143">See Also</span></span>


[<span data-ttu-id="d6b49-144">Get-CsTrunk</span><span class="sxs-lookup"><span data-stu-id="d6b49-144">Get-CsTrunk</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunk)  
[<span data-ttu-id="d6b49-145">Get-CsTrunkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6b49-145">Get-CsTrunkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunkConfiguration)  
  

<span data-ttu-id="d6b49-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d6b49-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

