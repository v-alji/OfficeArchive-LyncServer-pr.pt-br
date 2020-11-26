---
title: 'Lync Server 2013: verificar a configuração de tronco em relação a um número de telefone'
description: 'Lync Server 2013: Verifique a configuração de tronco em relação a um número de telefone.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Check trunk configuration against a phone number
ms:assetid: 0800d7a3-fc35-482b-a9a4-203d890bfa45
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725206(v=OCS.15)
ms:contentKeyID: 63969574
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7cdfe1a2a9c5c87310ad561464960c5a01fea7b5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434981"
---
# <a name="check-trunk-configuration-against-a-phone-number-in-lync-server-2013"></a><span data-ttu-id="e96f8-103">Verificar a configuração de tronco em relação a um número de telefone no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e96f8-103">Check trunk configuration against a phone number in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e96f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e96f8-104">

<span> </span></span></span>

<span data-ttu-id="e96f8-105">_**Tópico da última modificação:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="e96f8-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e96f8-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="e96f8-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="e96f8-107">Mensal</span><span class="sxs-lookup"><span data-stu-id="e96f8-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e96f8-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="e96f8-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="e96f8-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e96f8-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e96f8-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="e96f8-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="e96f8-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="e96f8-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="e96f8-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsTrunkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e96f8-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsTrunkConfiguration cmdlet.</span></span> <span data-ttu-id="e96f8-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e96f8-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsTrunkConfiguration&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="e96f8-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e96f8-114">Description</span></span>

<span data-ttu-id="e96f8-115">Os troncos SIP conectam a rede do Lync Server Internal Enterprise Voice a qualquer um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="e96f8-115">SIP trunks connect the Lync Server internal Enterprise Voice network to any of the following:</span></span>

  - <span data-ttu-id="e96f8-116">A rede telefônica pública comutada (PSTN).</span><span class="sxs-lookup"><span data-stu-id="e96f8-116">The Public Switched Telephone network (PSTN).</span></span>

  - <span data-ttu-id="e96f8-117">Um PBX IP-Public Branch Exchange (PBX).</span><span class="sxs-lookup"><span data-stu-id="e96f8-117">An IP-public branch exchange (PBX).</span></span>

  - <span data-ttu-id="e96f8-118">Um controlador de borda de sessão (SBC).</span><span class="sxs-lookup"><span data-stu-id="e96f8-118">A Session Border Controller (SBC).</span></span>

<span data-ttu-id="e96f8-119">O cmdlet Test-CsTrunkConfiguration verifica se um número de telefone (como discado por um usuário) pode ser convertido na rede E. 164 e roteado em um tronco SIP especificado.</span><span class="sxs-lookup"><span data-stu-id="e96f8-119">The Test-CsTrunkConfiguration cmdlet verifies that a phone number (as dialed by a user) can be converted to the E.164 network and routed over a specified SIP trunk.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="e96f8-120">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="e96f8-120">Running the test</span></span>

<span data-ttu-id="e96f8-121">Para executar o cmdlet Test-CsTrunkConfiguration, primeiro você deve usar o cmdlet Get-CsTrunkConfiguration para recuperar uma instância de suas configurações de tronco SIP; essa instância é então canalizada para Test-CsTrunkConfiguration:</span><span class="sxs-lookup"><span data-stu-id="e96f8-121">To run the Test-CsTrunkConfiguration cmdlet you must first use the Get-CsTrunkConfiguration cmdlet to retrieve an instance of your SIP trunk configuration settings; that instance is then piped to Test-CsTrunkConfiguration:</span></span>

`Get-CsTrunkConfiguration -Identity "Global" | Test-CsTrunkConfiguration -DialedNumber "12065551219"`

<span data-ttu-id="e96f8-122">Executar o Test-CsTrunkConfiguration sem a primeira execução do Get-CsTrunkConfiguration não funcionará.</span><span class="sxs-lookup"><span data-stu-id="e96f8-122">Running Test-CsTrunkConfiguration without first running Get-CsTrunkConfiguration won't work.</span></span> <span data-ttu-id="e96f8-123">Por exemplo, esse comando falhará sem retornar nenhum dado:</span><span class="sxs-lookup"><span data-stu-id="e96f8-123">For example, this command will fail without returning any data:</span></span>

`Test-CsTrunkConfiguration -DialedNumber "12065551219" -TrunkConfiguration "Global"`

<span data-ttu-id="e96f8-124">Se você tiver várias coleções de configurações de configuração de tronco SIP, poderá usar um comando semelhante ao seguinte para, ao mesmo tempo, testar cada coleção com o mesmo número de telefone:</span><span class="sxs-lookup"><span data-stu-id="e96f8-124">If you have multiple collections of SIP trunk configuration settings, you can use a command similar to the following to at the same time test each collection against the same phone number:</span></span>

`Get-CsTrunkConfiguration | Test-CsTrunkConfiguration -DialedNumber "12065551219"`

<span data-ttu-id="e96f8-125">Para obter mais informações, consulte a documentação da ajuda para o cmdlet Test-CsTrunkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e96f8-125">For more information, see the Help documentation for the Test-CsTrunkConfiguration cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="e96f8-126">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="e96f8-126">Determining success or failure</span></span>

<span data-ttu-id="e96f8-127">Se Test-CsTrunkConfiguration pode fazer uma chamada para o número discado, o número de telefone traduzido (no formato E. 164) e a regra usada para traduzir esse número de telefone serão exibidos na tela:</span><span class="sxs-lookup"><span data-stu-id="e96f8-127">If Test-CsTrunkConfiguration can place a call to the dialed number then the translated phone number (in the E.164 format) and the rule used to translate that phone number will both be displayed on screen:</span></span>

<span data-ttu-id="e96f8-128">TranslatedNumber MatchingRule</span><span class="sxs-lookup"><span data-stu-id="e96f8-128">TranslatedNumber MatchingRule</span></span>

<span data-ttu-id="e96f8-129">\---------------- ------------</span><span class="sxs-lookup"><span data-stu-id="e96f8-129">\---------------- ------------</span></span>

<span data-ttu-id="e96f8-130">\+12065551219 global/Redmond</span><span class="sxs-lookup"><span data-stu-id="e96f8-130">\+12065551219 Global/Redmond</span></span>

<span data-ttu-id="e96f8-131">Se o teste falhar, Test-CsTrunkConfiguration retornará valores de propriedade vazios:</span><span class="sxs-lookup"><span data-stu-id="e96f8-131">If the test fails, Test-CsTrunkConfiguration will return empty property values:</span></span>

<span data-ttu-id="e96f8-132">TranslatedNumber MatchingRule</span><span class="sxs-lookup"><span data-stu-id="e96f8-132">TranslatedNumber MatchingRule</span></span>

<span data-ttu-id="e96f8-133">\---------------- ------------</span><span class="sxs-lookup"><span data-stu-id="e96f8-133">\---------------- ------------</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="e96f8-134">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="e96f8-134">Reasons why the test might have failed</span></span>

<span data-ttu-id="e96f8-135">Se Test-CsTrunkConfiguration não retornar uma coincidência que normalmente significa que as configurações de configuração de tronco que estão sendo testadas não têm uma regra de tradução de número de chamadas de saída capaz de converter o número discado para o formato E. 164.</span><span class="sxs-lookup"><span data-stu-id="e96f8-135">If Test-CsTrunkConfiguration does not return a match that typically means that the trunk configuration settings being test do not have an outgoing calling number translation rule capable to converting the dialed number to the E.164 format.</span></span> <span data-ttu-id="e96f8-136">Para recuperar as regras de tradução atribuídas a uma coleção de definições de configuração de tronco, você pode usar uma sintaxe semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="e96f8-136">To retrieve the translation rules assigned to a collection of trunk configuration settings, you can use syntax similar to this:</span></span>

`Get-CsTrunkConfiguration -Identity "global" | Select-Object -ExpandProperty OutboundTranslationRulesList`

<span data-ttu-id="e96f8-137">Que retorna informações semelhantes para cada regra de Tradução:</span><span class="sxs-lookup"><span data-stu-id="e96f8-137">That returns information similar to this for each translation rule:</span></span>

<span data-ttu-id="e96f8-138">Descrição: números de telefone sem um código de país ou código de área.</span><span class="sxs-lookup"><span data-stu-id="e96f8-138">Description : Phone numbers without a country code or area code.</span></span>

<span data-ttu-id="e96f8-139">Padrão: ^ \\ + ( \\ d \* ) $</span><span class="sxs-lookup"><span data-stu-id="e96f8-139">Pattern : ^\\+(\\d\*)$</span></span>

`Translation : $1`

<span data-ttu-id="e96f8-140">Nome: NoAreaCode</span><span class="sxs-lookup"><span data-stu-id="e96f8-140">Name : NoAreaCode</span></span>

<span data-ttu-id="e96f8-141">Nesse ponto, você verifica o valor da propriedade Pattern (que é uma cadeia de caracteres de [expressão regular](https://go.microsoft.com/fwlink/?linkid=400464) ) para ver se alguma das regras de tradução está configurada para manipular o número discado.</span><span class="sxs-lookup"><span data-stu-id="e96f8-141">At that point, you check the value of the Pattern property (which is a [regular expression](https://go.microsoft.com/fwlink/?linkid=400464) string) to see whether any of the translation rules are configured to handle the dialed number.</span></span> <span data-ttu-id="e96f8-142">Caso contrário, você precisará alterar uma das regras existentes (Set-CsOutboundTranslationRule) ou usar o cmdlet New-CsOutboundTranslationRule para adicionar uma nova regra à coleção.</span><span class="sxs-lookup"><span data-stu-id="e96f8-142">If not, you'll either have to change one of the existing rules (Set-CsOutboundTranslationRule) or use the New-CsOutboundTranslationRule cmdlet to add a new rule to the collection.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e96f8-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="e96f8-143">See Also</span></span>


[<span data-ttu-id="e96f8-144">Test-CsTrunkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e96f8-144">Test-CsTrunkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsTrunkConfiguration)  
  

<span data-ttu-id="e96f8-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e96f8-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

