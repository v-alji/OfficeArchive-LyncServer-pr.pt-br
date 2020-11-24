---
title: 'Lync Server 2013: testando o plano de discagem'
description: 'Lync Server 2013: testando o plano de discagem.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the dial plan
ms:assetid: 70eec03c-aca3-4106-86a7-77ae96b53779
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690130(v=OCS.15)
ms:contentKeyID: 63969616
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a0ef2e3fce9d1fbbb0186b1b7aef608834145d3e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390446"
---
# <a name="testing-the-dial-plan-in-lync-server-2013"></a><span data-ttu-id="581c0-103">Testando o plano de discagem no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="581c0-103">Testing the dial plan in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="581c0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="581c0-104">

<span> </span></span></span>

<span data-ttu-id="581c0-105">_**Tópico da última modificação:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="581c0-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="581c0-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="581c0-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="581c0-107">Diário</span><span class="sxs-lookup"><span data-stu-id="581c0-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="581c0-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="581c0-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="581c0-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="581c0-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="581c0-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="581c0-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="581c0-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="581c0-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="581c0-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsDialPlan.</span><span class="sxs-lookup"><span data-stu-id="581c0-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsDialPlan cmdlet.</span></span> <span data-ttu-id="581c0-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="581c0-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDialPlan&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="581c0-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="581c0-114">Description</span></span>

<span data-ttu-id="581c0-115">O cmdlet Test-CsDialPlan permite que você veja os resultados da aplicação de um plano de discagem para um determinado número de telefone.</span><span class="sxs-lookup"><span data-stu-id="581c0-115">The Test-CsDialPlan cmdlet enables you to see the results of applying a dial plan to a given telephone number.</span></span> <span data-ttu-id="581c0-116">Os planos de discagem fornecem informações, como as regras de normalização são aplicadas, necessárias para permitir que usuários do Enterprise Voice façam chamadas telefônicas.</span><span class="sxs-lookup"><span data-stu-id="581c0-116">Dial plans provide information, such as how normalization rules are applied, required to enable Enterprise Voice users to make telephone calls.</span></span> <span data-ttu-id="581c0-117">Devido a um número discado e um plano de discagem, esse cmdlet verificará qual regra de normalização dentro do plano de discagem será aplicada e qual será o número traduzido.</span><span class="sxs-lookup"><span data-stu-id="581c0-117">Given a dialed number and a dial plan, this cmdlet will verify which normalization rule within the dial plan will be applied and what the translated number will be.</span></span>

<span data-ttu-id="581c0-118">Você pode usar esse cmdlet para solucionar problemas com traduções numéricas ou para verificar como aplicar regras em determinados números.</span><span class="sxs-lookup"><span data-stu-id="581c0-118">You can use this cmdlet for troubleshooting issues with number translations, or for verifying how to apply rules against certain numbers.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="581c0-119">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="581c0-119">Running the test</span></span>

<span data-ttu-id="581c0-120">O cmdlet Test-CsDialPlan requer que você faça duas coisas.</span><span class="sxs-lookup"><span data-stu-id="581c0-120">The Test-CsDialPlan cmdlet requires you to do two things.</span></span> <span data-ttu-id="581c0-121">Primeiro, você deve obter uma instância do plano de discagem que está sendo testado; Isso pode ser feito usando o cmdlet Get-CsDialPlan.</span><span class="sxs-lookup"><span data-stu-id="581c0-121">First, you must obtain an instance of the dial plan being tested; that can be done by using the Get-CsDialPlan cmdlet.</span></span> <span data-ttu-id="581c0-122">Em seguida, você deve especificar o número de telefone que deve ser normalizado.</span><span class="sxs-lookup"><span data-stu-id="581c0-122">Second, you must specify the phone number that has to be normalized.</span></span> <span data-ttu-id="581c0-123">O formato usado para o número de telefone deve corresponder ao número como discado/inserido por um usuário.</span><span class="sxs-lookup"><span data-stu-id="581c0-123">The format that is used for the phone number should match the number as dialed/entered by a user.</span></span> <span data-ttu-id="581c0-124">Por exemplo, esse comando recupera uma instância do plano de discagem, RedmondDialPlan e verifica se o número de telefone 12065551219 pode ser normalizado:</span><span class="sxs-lookup"><span data-stu-id="581c0-124">For example, this command retrieves an instance of the dial plan, RedmondDialPlan, and checks whether the phone number 12065551219 can be normalized:</span></span>

    Get-CsDialPlan -Identity "RedmondDialPlan" | Test-CsDialPlan -DialedNumber "12065551219" | Format-List

<span data-ttu-id="581c0-125">Se você tiver uma regra de normalização que adiciona automaticamente o código de país (neste exemplo, 1) e o código de área (206), talvez você queira verificar o número de telefone 5551219, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="581c0-125">If you have a normalization rule that automatically adds the country code (in this example, 1) and the area code (206), then you might want to check the phone number 5551219, as follows:</span></span>

    Get-CsDialPlan -Identity "RedmondDialPlan" | Test-CsDialPlan -DialedNumber "5551219" | Format-List

<span data-ttu-id="581c0-126">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsDialPlan](https://docs.microsoft.com/powershell/module/skype/Test-CsDialPlan) .</span><span class="sxs-lookup"><span data-stu-id="581c0-126">For more information, see the Help documentation for the [Test-CsDialPlan](https://docs.microsoft.com/powershell/module/skype/Test-CsDialPlan) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="581c0-127">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="581c0-127">Determining success or failure</span></span>

<span data-ttu-id="581c0-128">Test-CsDialPlan é diferente de muitos dos cmdlets de teste do Lync Server porque apenas indiretamente indica se um teste foi bem-sucedido ou falhou.</span><span class="sxs-lookup"><span data-stu-id="581c0-128">Test-CsDialPlan differs from many of the Lync Server test cmdlets because it only indirectly indicates whether a test succeeded or failed.</span></span> <span data-ttu-id="581c0-129">Ao usar Test-CsDialPlan você não recebe uma saída semelhante a isso com o rótulo claramente identificado:</span><span class="sxs-lookup"><span data-stu-id="581c0-129">When using Test-CsDialPlan you do not receive back output similar to this with the Result clearly labeled:</span></span>

<span data-ttu-id="581c0-130">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="581c0-130">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="581c0-131">Resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="581c0-131">Result : Success</span></span>

<span data-ttu-id="581c0-132">Latência: 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="581c0-132">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="581c0-133">Erros</span><span class="sxs-lookup"><span data-stu-id="581c0-133">Error :</span></span>

<span data-ttu-id="581c0-134">Correto</span><span class="sxs-lookup"><span data-stu-id="581c0-134">Diagnosis :</span></span>

<span data-ttu-id="581c0-135">Em vez disso, se Test-CsDialPlan for bem-sucedida, você receberá informações sobre a regra de normalização que foi capaz de traduzir e usar o número de telefone especificado:</span><span class="sxs-lookup"><span data-stu-id="581c0-135">Instead, if Test-CsDialPlan succeeds, then you'll receive information about the normalization rule that was able to successfully translate and use the specified phone number:</span></span>

<span data-ttu-id="581c0-136">TranslatedNumber: + 12065551219</span><span class="sxs-lookup"><span data-stu-id="581c0-136">TranslatedNumber : +12065551219</span></span>

<span data-ttu-id="581c0-137">MatchingRule: Descrição =; Padrão = ^ ( \\ d (11)) $; Tradução = + $1;</span><span class="sxs-lookup"><span data-stu-id="581c0-137">MatchingRule : Description=;Pattern=^(\\d(11))$;Translation=+$1;</span></span>

<span data-ttu-id="581c0-138">Name = prefix All; IsInternalExtension = false</span><span class="sxs-lookup"><span data-stu-id="581c0-138">Name=Prefix All; IsInternalExtension=False</span></span>

<span data-ttu-id="581c0-139">Se Test-CsDialPlan falhar (ou seja, se o plano de discagem não tiver uma regra de normalização que pode traduzir o número de telefone especificado), você receberá a seguinte saída "Empty" da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="581c0-139">If Test-CsDialPlan fails (that is, if the dial plan does not have a normalization rule that can translate the specified phone number), you'll just receive “empty” output as follows:</span></span>

<span data-ttu-id="581c0-140">TranslatedNumber :</span><span class="sxs-lookup"><span data-stu-id="581c0-140">TranslatedNumber :</span></span>

<span data-ttu-id="581c0-141">MatchingRule :</span><span class="sxs-lookup"><span data-stu-id="581c0-141">MatchingRule :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="581c0-142">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="581c0-142">Reasons why the test might have failed</span></span>

<span data-ttu-id="581c0-143">Veja a seguir alguns motivos comuns para que Test-CsDialPlan possam falhar:</span><span class="sxs-lookup"><span data-stu-id="581c0-143">Here are some common reasons why Test-CsDialPlan might fail:</span></span>

  - <span data-ttu-id="581c0-144">Você pode ter usado um formato incorreto ao especificar o número de telefone.</span><span class="sxs-lookup"><span data-stu-id="581c0-144">You might have used an incorrect format when specifying the phone number.</span></span> <span data-ttu-id="581c0-145">Os planos de discagem incluem regras de normalização que permitem ao Lync Server converter os números de telefone discados ou inseridos por um usuário.</span><span class="sxs-lookup"><span data-stu-id="581c0-145">Dial plans include normalization rules that enable Lync Server to translate the phone numbers dialed or entered by a user.</span></span> <span data-ttu-id="581c0-146">Portanto, seu plano de discagem deve ter regras de normalização que correspondam aos números que os usuários podem discar.</span><span class="sxs-lookup"><span data-stu-id="581c0-146">Therefore, your dial plan should have normalization rules that match the numbers users are likely to dial.</span></span> <span data-ttu-id="581c0-147">Por exemplo, se os usuários podem discar o código de país, o código de área e o número de telefone em si, isso significa que seu plano de discagem deve ter uma regra de normalização para lidar com números de telefone, como este:</span><span class="sxs-lookup"><span data-stu-id="581c0-147">For example, if users might dial the country code, area code, and then the phone number itself, that means that your dial plan should have a normalization rule to handle phone numbers such as this:</span></span>
    
    <span data-ttu-id="581c0-148">12065551219</span><span class="sxs-lookup"><span data-stu-id="581c0-148">12065551219</span></span>
    
    <span data-ttu-id="581c0-149">No entanto, se você digitar um número de telefone incorreto (por exemplo, deixando o último dígito), Test-CsDialPlan irá falhar.</span><span class="sxs-lookup"><span data-stu-id="581c0-149">However, if you enter an incorrect phone number (for example, leaving off the final digit), then Test-CsDialPlan will fail.</span></span> <span data-ttu-id="581c0-150">Isso não é porque o plano de discagem está defeituoso, mas porque você digitou um número de telefone que não pode ser interpretado.</span><span class="sxs-lookup"><span data-stu-id="581c0-150">That’s not because the dial plan is faulty but because you have entered a phone number than can’t be interpreted.</span></span>

<span data-ttu-id="581c0-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="581c0-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

