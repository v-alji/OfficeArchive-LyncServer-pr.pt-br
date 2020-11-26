---
title: 'Lync Server 2013: verificar regras de normalização de voz'
description: 'Lync Server 2013: verificar regras de normalização de voz.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Check voice normalization rules
ms:assetid: bf71a218-71cd-4b64-b8e8-b3a98b6e87a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725212(v=OCS.15)
ms:contentKeyID: 63969649
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f68bbde24a3dc7d8e8214dcfe506d4b8112fbbb3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435002"
---
# <a name="check-voice-normalization-rules-in-lync-server-2013"></a><span data-ttu-id="c5de8-103">Verificar regras de normalização de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c5de8-103">Check voice normalization rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c5de8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c5de8-104">

<span> </span></span></span>

<span data-ttu-id="c5de8-105">_**Tópico da última modificação:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="c5de8-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5de8-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="c5de8-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="c5de8-107">Mensal</span><span class="sxs-lookup"><span data-stu-id="c5de8-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5de8-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="c5de8-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="c5de8-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c5de8-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5de8-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="c5de8-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="c5de8-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="c5de8-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="c5de8-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsVoiceNormalizationRule.</span><span class="sxs-lookup"><span data-stu-id="c5de8-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsVoiceNormalizationRule cmdlet.</span></span> <span data-ttu-id="c5de8-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="c5de8-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoiceNormalizationRule&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="c5de8-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5de8-114">Description</span></span>

<span data-ttu-id="c5de8-115">As regras de normalização de voz são usadas para converter um número de telefone discado por um usuário (por exemplo, 2065551219) para o formato E. 164 usado pelo Lync Server (+ 12065551219).</span><span class="sxs-lookup"><span data-stu-id="c5de8-115">Voice normalization rules are used to convert a phone number dialed by a user (for example, 2065551219) to the E.164 format that is used by Lync Server (+12065551219).</span></span> <span data-ttu-id="c5de8-116">Por exemplo, se os usuários estiverem no hábito de discar um número de telefone sem incluir o código de país ou o código de área (por exemplo, 5551219), você deve ter uma regra de normalização de voz que pode converter esse número no formato E. 164: + 12065551219.</span><span class="sxs-lookup"><span data-stu-id="c5de8-116">For example, if users are in the habit of dialing a phone number without including the country code or the area code (e.g., 5551219) then you must have a voice normalization rule that can convert that number to the E.164 format: +12065551219.</span></span> <span data-ttu-id="c5de8-117">Sem essa regra, o usuário não poderá ligar para 555-1219.</span><span class="sxs-lookup"><span data-stu-id="c5de8-117">Without such a rule, the user won't be able to call 555-1219.</span></span>

<span data-ttu-id="c5de8-118">O cmdlet Test-CsVoiceNormalizationRule verifica se uma regra de normalização de voz especificada pode converter com êxito um número de telefone especificado.</span><span class="sxs-lookup"><span data-stu-id="c5de8-118">The Test-CsVoiceNormalizationRule cmdlet verifies that a specified voice normalization rule can successfully convert a specified phone number.</span></span> <span data-ttu-id="c5de8-119">Por exemplo, esse comando verifica se a regra de normalização global NoAreaCode pode normalizar e converter a cadeia de caracteres de discagem 5551219.</span><span class="sxs-lookup"><span data-stu-id="c5de8-119">For example, this command checks whether the global normalization rule NoAreaCode can normalize and convert the dial string 5551219.</span></span>

`Get-CsVoiceNormalizationRule -Identity "global/NoAreaCode" | Test-CsVoiceNormalizationRule -DialedNumber "5551219"`

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="c5de8-120">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="c5de8-120">Running the test</span></span>

<span data-ttu-id="c5de8-121">Para executar o cmdlet Test-CsVoiceNormalizationRule, você deve primeiro usar o cmdlet Get-CsVoiceNormalizationRule para recuperar uma instância da regra que está sendo testada e, em seguida, canalizar essa instância para Test-CsVoiceNormalizationRule.</span><span class="sxs-lookup"><span data-stu-id="c5de8-121">To run the Test-CsVoiceNormalizationRule cmdlet, you must first use the Get-CsVoiceNormalizationRule cmdlet to retrieve an instance of the rule being tested, and then pipe that instance to Test-CsVoiceNormalizationRule.</span></span> <span data-ttu-id="c5de8-122">A sintaxe semelhante a esta não funcionará:</span><span class="sxs-lookup"><span data-stu-id="c5de8-122">Syntax similar to this won't work:</span></span>

<span data-ttu-id="c5de8-123">Test-CsVoiceNormalizationRule-DialedNumber "12065551219" – NormalizationRule "global/prefix All"</span><span class="sxs-lookup"><span data-stu-id="c5de8-123">Test-CsVoiceNormalizationRule -DialedNumber "12065551219" –NormalizationRule "global/Prefix All"</span></span>

<span data-ttu-id="c5de8-124">Em vez disso, use a sintaxe como a seguir, que combina os cmdlets Get-CsVoiceNormalizationRule e Test-CsVoiceNormalizationRule:</span><span class="sxs-lookup"><span data-stu-id="c5de8-124">Instead, use syntax such as the following, which combines both the Get-CsVoiceNormalizationRule and the Test-CsVoiceNormalizationRule cmdlets:</span></span>

<span data-ttu-id="c5de8-125">Get-CsVoiceNormalizationRule-identidade "global/prefixo tudo" | Test-CsVoiceNormalizationRule-DialedNumber "12065551219"</span><span class="sxs-lookup"><span data-stu-id="c5de8-125">Get-CsVoiceNormalizationRule -Identity "global/Prefix All" | Test-CsVoiceNormalizationRule -DialedNumber "12065551219"</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c5de8-126">.</span><span class="sxs-lookup"><span data-stu-id="c5de8-126">.</span></span> <span data-ttu-id="c5de8-127">Ou, você também pode usar essa abordagem para recuperar uma instância de uma regra e, em seguida, testar essa regra em relação a um número de telefone especificado:</span><span class="sxs-lookup"><span data-stu-id="c5de8-127">Or, you can also use this approach to retrieve an instance of a rule and then test that rule against a specified phone number:</span></span>



</div>

`$x = Get-CsVoiceNormalizationRule -Identity "global/Prefix All"`

`Test-CsVoiceNormalizationRule -DialedNumber "12065551219" -NormalizationRule $x`

<span data-ttu-id="c5de8-128">Digite o valor do parâmetro DialedNumber exatamente como você espera que o número seja discado.</span><span class="sxs-lookup"><span data-stu-id="c5de8-128">Enter the value for the DialedNumber parameter exactly as you expect that number to be dialed.</span></span> <span data-ttu-id="c5de8-129">Por exemplo, se a regra de normalização de voz especificada deve adicionar automaticamente o código de país (o 1 inicial no valor 12065551219), você deve deixar de fora o código de país:</span><span class="sxs-lookup"><span data-stu-id="c5de8-129">For example, if the specified voice normalization rule is supposed to automatically add the country code (the initial 1 in the value 12065551219) then you should leave off the country code:</span></span>

`-DialedNumber "2065551219"`

<span data-ttu-id="c5de8-130">Se a regra estiver configurada corretamente, ela adicionará automaticamente o código do país ao traduzir o número para o formato E. 164 que é usado pelo Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c5de8-130">If the rule is configured correctly, it will automatically add the country code when translating the number to the E.164 format that is used by Lync Server.</span></span>

<span data-ttu-id="c5de8-131">Para obter mais informações, consulte a documentação da ajuda para o cmdlet Test-CsVoiceNormalizationRule.</span><span class="sxs-lookup"><span data-stu-id="c5de8-131">For more information, see the Help documentation for the Test-CsVoiceNormalizationRule cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="c5de8-132">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="c5de8-132">Determining success or failure</span></span>

<span data-ttu-id="c5de8-133">Se a regra de normalização de voz especificada puder traduzir o número fornecido, o número traduzido será exibido na tela:</span><span class="sxs-lookup"><span data-stu-id="c5de8-133">If the specified voice normalization rule can translate the supplied number then the translated number will be displayed on-screen:</span></span>

<span data-ttu-id="c5de8-134">TranslatedNumber</span><span class="sxs-lookup"><span data-stu-id="c5de8-134">TranslatedNumber</span></span>

\----------------

<span data-ttu-id="c5de8-135">\+12065551219</span><span class="sxs-lookup"><span data-stu-id="c5de8-135">\+12065551219</span></span>

<span data-ttu-id="c5de8-136">Se o teste falhar, um número traduzido em branco será retornado:</span><span class="sxs-lookup"><span data-stu-id="c5de8-136">If the test fails then a blank translated number will be returned:</span></span>

<span data-ttu-id="c5de8-137">TranslatedNumber</span><span class="sxs-lookup"><span data-stu-id="c5de8-137">TranslatedNumber</span></span>

\----------------

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="c5de8-138">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="c5de8-138">Reasons why the test might have failed</span></span>

<span data-ttu-id="c5de8-139">Se o Test-CsVoiceNormalizationRule retornar um número traduzido que significa que a regra de normalização de voz especificada não pôde traduzir o número de telefone fornecido para o formato E. 164 que é usado pelo Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c5de8-139">If the Test-CsVoiceNormalizationRule does return a translated number that means that the specified voice normalization rule was unable to translate the supplied telephone number into the E.164 format that is used by Lync Server.</span></span> <span data-ttu-id="c5de8-140">Para verificar isso, primeiro certifique-se de que digitou o número de telefone corretamente.</span><span class="sxs-lookup"><span data-stu-id="c5de8-140">To verify that, first make sure that you typed the telephone number in correctly.</span></span> <span data-ttu-id="c5de8-141">Por exemplo, você espera que sua regra de normalização de voz tenha problemas para traduzir um número semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="c5de8-141">For example, you would expect your voice normalization rule to have problems translating a number similar to this:</span></span>

`-DialedNumber "1"`

<span data-ttu-id="c5de8-142">Pressupondo que o número foi digitado corretamente, a próxima etapa deve ser verificar se a regra de normalização especificada foi projetada para manipular esse número de telefone.</span><span class="sxs-lookup"><span data-stu-id="c5de8-142">Assuming the number was entered correctly, your next step should be to verify that the specified normalization rule is designed to handle that phone number.</span></span> <span data-ttu-id="c5de8-143">Por exemplo, uma regra de normalização pode ser projetada para manipular o formato 12065551219, mas uma segunda regra pode ser projetada para manipular o número 2065551219.</span><span class="sxs-lookup"><span data-stu-id="c5de8-143">For example, one normalization rule might be designed to handle the format 12065551219, but a second rule might be designed to handle the number 2065551219.</span></span> <span data-ttu-id="c5de8-144">(Esse é o mesmo número de telefone, menos o código de país 1 no início.) Para retornar informações detalhadas sobre uma regra de normalização de voz, execute um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="c5de8-144">(That’s the same phone number, minus the country code 1 at the very beginning.) To return detailed information about a voice normalization rule, run a command similar to this:</span></span>

`Get-CsVoiceNormalizationRule -Identity "global/Prefix All" | Format-List`

<span data-ttu-id="c5de8-145">Para retornar informações detalhadas sobre todas as regras de normalização de voz, execute este comando em vez disso:</span><span class="sxs-lookup"><span data-stu-id="c5de8-145">To return detailed information about all the voice normalization rules, run this command instead:</span></span>

`Get-CsVoiceNormalizationRule | Format-List`

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c5de8-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5de8-146">See Also</span></span>


[<span data-ttu-id="c5de8-147">Test-CsVoiceNormalizationRule</span><span class="sxs-lookup"><span data-stu-id="c5de8-147">Test-CsVoiceNormalizationRule</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsVoiceNormalizationRule)  
  

<span data-ttu-id="c5de8-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c5de8-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

