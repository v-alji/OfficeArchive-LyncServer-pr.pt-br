---
title: 'Lync Server 2013: regras de tradução'
description: 'Lync Server 2013: regras de tradução.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Translation rules
ms:assetid: 6e067bd4-4931-4385-81ac-2acae45a16d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398520(v=OCS.15)
ms:contentKeyID: 48184460
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 65ee21459123ea09f54eb52e65a4d9ecba61c386
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389680"
---
# <a name="translation-rules-in-lync-server-2013"></a><span data-ttu-id="b7d6a-103">Regras de tradução no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7d6a-103">Translation rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7d6a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7d6a-104">

<span> </span></span></span>

<span data-ttu-id="b7d6a-105">_**Tópico da última modificação:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="b7d6a-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="b7d6a-106">O Lync Server 2013 Enterprise Voice requer que todas as cadeias de caracteres de discagem sejam normalizadas para o formato E. 164 para realizar a pesquisa de número reverso (RNL).</span><span class="sxs-lookup"><span data-stu-id="b7d6a-106">Lync Server 2013 Enterprise Voice requires that all dial strings be normalized to E.164 format for the purpose of performing reverse number lookup (RNL).</span></span> <span data-ttu-id="b7d6a-107">No Microsoft Lync Server 2010, há suporte para as regras de tradução somente para números chamados.</span><span class="sxs-lookup"><span data-stu-id="b7d6a-107">In Microsoft Lync Server 2010, translation rules are supported only for called numbers.</span></span> <span data-ttu-id="b7d6a-108">Novo no Microsoft Lync Server 2013, também há suporte para as regras de tradução para números de chamada.</span><span class="sxs-lookup"><span data-stu-id="b7d6a-108">New in Microsoft Lync Server 2013, translation rules are also supported for calling numbers.</span></span> <span data-ttu-id="b7d6a-109">The *trunk peer* (that is, the associated gateway, private branch exchange (PBX), or SIP trunk) may require that numbers be in a local dialing format.</span><span class="sxs-lookup"><span data-stu-id="b7d6a-109">The *trunk peer* (that is, the associated gateway, private branch exchange (PBX), or SIP trunk) may require that numbers be in a local dialing format.</span></span> <span data-ttu-id="b7d6a-110">To translate numbers from E.164 format to a local dialing format, you can define one or more translation rules to manipulate the request URI before you route it to the trunk peer.</span><span class="sxs-lookup"><span data-stu-id="b7d6a-110">To translate numbers from E.164 format to a local dialing format, you can define one or more translation rules to manipulate the request URI before you route it to the trunk peer.</span></span> <span data-ttu-id="b7d6a-111">For example, you could write a translation rule to remove +44 from the beginning of a dial string and replace it with 0144.</span><span class="sxs-lookup"><span data-stu-id="b7d6a-111">For example, you could write a translation rule to remove +44 from the beginning of a dial string and replace it with 0144.</span></span>

<span data-ttu-id="b7d6a-112">Executando a conversão da rota de saída no servidor, você pode reduzir os requisitos de configuração em cada par de tronco individual para converter os números de telefone em um formato de discagem.</span><span class="sxs-lookup"><span data-stu-id="b7d6a-112">By performing outbound route translation on the server, you can reduce the configuration requirements on each individual trunk peer in order to translate phone numbers into a local dialing format.</span></span> <span data-ttu-id="b7d6a-113">Quando você planeja quais gateways e quantos gateways, associar a um cluster de servidor de mediação específico, pode ser útil agrupar pares de tronco com requisitos de discagem locais semelhantes.</span><span class="sxs-lookup"><span data-stu-id="b7d6a-113">When you plan which gateways, and how many gateways, to associate with a specific Mediation Server cluster, it may be useful to group trunk peers with similar local dialing requirements.</span></span> <span data-ttu-id="b7d6a-114">Isso pode reduzir o número de regras de conversão necessárias e o tempo necessário para gravá-las.</span><span class="sxs-lookup"><span data-stu-id="b7d6a-114">This can reduce the number of required translation rules and the time it takes to write them.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b7d6a-115">Associar uma ou mais regras de tradução a uma configuração de tronco do Enterprise Voice deve ser usado como uma alternativa para configurar regras de tradução no par de troncos.</span><span class="sxs-lookup"><span data-stu-id="b7d6a-115">Associating one or more translation rules with an Enterprise Voice trunk configuration should be used as an alternative to configuring translation rules on the trunk peer.</span></span> <span data-ttu-id="b7d6a-116">Não associe as regras de tradução a uma configuração de tronco do Enterprise Voice se você tiver configurado regras de tradução no par de tronco, pois as duas regras podem entrar em conflito.</span><span class="sxs-lookup"><span data-stu-id="b7d6a-116">Do not associate translation rules with an Enterprise Voice trunk configuration if you have configured translation rules on the trunk peer, because the two rules might conflict.</span></span>



</div>

<div>

## <a name="example-translation-rules"></a><span data-ttu-id="b7d6a-117">Exemplo de regras de conversão</span><span class="sxs-lookup"><span data-stu-id="b7d6a-117">Example Translation Rules</span></span>

<span data-ttu-id="b7d6a-118">Os exemplos a seguir de regras de conversão mostram como você pode desenvolver as regras no servidor para converter números do formato E.164 para um formato local para o par de tronco.</span><span class="sxs-lookup"><span data-stu-id="b7d6a-118">The following examples of translation rules show how you can develop rules on the server to translate numbers from E.164 format to a local format for the trunk peer.</span></span>

<span data-ttu-id="b7d6a-119">Para obter detalhes sobre como implementar regras de tradução, consulte [definindo regras de tradução no Lync Server 2013](lync-server-2013-defining-translation-rules.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="b7d6a-119">For details about how to implement translation rules, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>


<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7d6a-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7d6a-120">Description</span></span></th>
<th><span data-ttu-id="b7d6a-121">Dígitos iniciais</span><span class="sxs-lookup"><span data-stu-id="b7d6a-121">Starting Digits</span></span></th>
<th><span data-ttu-id="b7d6a-122">Comprimento</span><span class="sxs-lookup"><span data-stu-id="b7d6a-122">Length</span></span></th>
<th><span data-ttu-id="b7d6a-123">Dígitos a serem removidos</span><span class="sxs-lookup"><span data-stu-id="b7d6a-123">Digits to Remove</span></span></th>
<th><span data-ttu-id="b7d6a-124">Dígitos a serem adicionados</span><span class="sxs-lookup"><span data-stu-id="b7d6a-124">Digits to Add</span></span></th>
<th><span data-ttu-id="b7d6a-125">Padrão de correspondência</span><span class="sxs-lookup"><span data-stu-id="b7d6a-125">Matching Pattern</span></span></th>
<th><span data-ttu-id="b7d6a-126">Tradução</span><span class="sxs-lookup"><span data-stu-id="b7d6a-126">Translation</span></span></th>
<th><span data-ttu-id="b7d6a-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b7d6a-127">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7d6a-128">Discagem convencional de longa distância nos EUA</span><span class="sxs-lookup"><span data-stu-id="b7d6a-128">Conventional long-distance dialing in U.S.</span></span></p>
<p><span data-ttu-id="b7d6a-129">(retirar o '+')</span><span class="sxs-lookup"><span data-stu-id="b7d6a-129">(strip out the ‘+’)</span></span></p></td>
<td><p><span data-ttu-id="b7d6a-130">+1</span><span class="sxs-lookup"><span data-stu-id="b7d6a-130">+1</span></span></p></td>
<td><p><span data-ttu-id="b7d6a-131">Exatamente 12</span><span class="sxs-lookup"><span data-stu-id="b7d6a-131">Exactly 12</span></span></p></td>
<td><p><span data-ttu-id="b7d6a-132">1</span><span class="sxs-lookup"><span data-stu-id="b7d6a-132">1</span></span></p></td>
<td><p><span data-ttu-id="b7d6a-133">0</span><span class="sxs-lookup"><span data-stu-id="b7d6a-133">0</span></span></p></td>
<td><p><span data-ttu-id="b7d6a-134">^\+(1 \ d {10} ) $</span><span class="sxs-lookup"><span data-stu-id="b7d6a-134">^\+(1\d{10})$</span></span></p></td>
<td><p><span data-ttu-id="b7d6a-135">$1</span><span class="sxs-lookup"><span data-stu-id="b7d6a-135">$1</span></span></p></td>
<td><p><span data-ttu-id="b7d6a-136">+14255551010 se torna 14255551010</span><span class="sxs-lookup"><span data-stu-id="b7d6a-136">+14255551010 becomes 14255551010</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7d6a-137">Discagem de longa distância internacional dos EUA</span><span class="sxs-lookup"><span data-stu-id="b7d6a-137">U.S. international long-distance dialing</span></span></p>
<p><span data-ttu-id="b7d6a-138">(retirar '+' e adicionar 011)</span><span class="sxs-lookup"><span data-stu-id="b7d6a-138">(strip out ‘+’ and add 011)</span></span></p></td>
<td><p>+</p></td>
<td><p><span data-ttu-id="b7d6a-139">Pelo menos 11</span><span class="sxs-lookup"><span data-stu-id="b7d6a-139">At least 11</span></span></p></td>
<td><p><span data-ttu-id="b7d6a-140">1</span><span class="sxs-lookup"><span data-stu-id="b7d6a-140">1</span></span></p></td>
<td><p><span data-ttu-id="b7d6a-141">011</span><span class="sxs-lookup"><span data-stu-id="b7d6a-141">011</span></span></p></td>
<td><p><span data-ttu-id="b7d6a-142">^\+(\d {9} \d +) $</span><span class="sxs-lookup"><span data-stu-id="b7d6a-142">^\+(\d{9}\d+)$</span></span></p></td>
<td><p><span data-ttu-id="b7d6a-143">011$1</span><span class="sxs-lookup"><span data-stu-id="b7d6a-143">011$1</span></span></p></td>
<td><p><span data-ttu-id="b7d6a-144">+441235551010 se torna 011441235551010</span><span class="sxs-lookup"><span data-stu-id="b7d6a-144">+441235551010 becomes 011441235551010</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b7d6a-145">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7d6a-145">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

