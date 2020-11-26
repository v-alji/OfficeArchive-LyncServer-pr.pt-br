---
title: 'Lync Server 2013: tabela VideoMetricsThreshold'
description: 'Lync Server 2013: VideoMetricsThreshold Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoMetricsThreshold table
ms:assetid: 2e2f4711-35ba-48c6-b15b-5aba61c4eb75
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204778(v=OCS.15)
ms:contentKeyID: 48183736
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 93cdd6fb4c3c54ac1470499490f36fee87ba283d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438866"
---
# <a name="videometricsthreshold-table-in-lync-server-2013"></a><span data-ttu-id="b40bb-103">Tabela VideoMetricsThreshold no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b40bb-103">VideoMetricsThreshold table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b40bb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b40bb-104">

<span> </span></span></span>

<span data-ttu-id="b40bb-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="b40bb-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="b40bb-106">A tabela VideoMetricsThreshold contém os valores ideais e aceitáveis para as métricas de qualidade da experiência usadas com chamadas com vídeo.</span><span class="sxs-lookup"><span data-stu-id="b40bb-106">The VideoMetricsThreshold table contains optimal and acceptable values for the Quality of Experience metrics used with video calls.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b40bb-107"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-107"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="b40bb-108"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-108"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="b40bb-109"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-109"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="b40bb-110"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-110"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b40bb-111"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-111"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-112">int</span><span class="sxs-lookup"><span data-stu-id="b40bb-112">int</span></span></p></td>
<td><p><span data-ttu-id="b40bb-113">Primária</span><span class="sxs-lookup"><span data-stu-id="b40bb-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="b40bb-114">Tipo de chamada que foi feita.</span><span class="sxs-lookup"><span data-stu-id="b40bb-114">Type of call that was placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b40bb-115"><strong>VideoPostFECPLROptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-115"><strong>VideoPostFECPLROptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-116">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="b40bb-116">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-117">O valor padrão é 0, 5.</span><span class="sxs-lookup"><span data-stu-id="b40bb-117">The default value is 0.05.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b40bb-118"><strong>VideoPostFECPLRAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-118"><strong>VideoPostFECPLRAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-119">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="b40bb-119">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-120">O valor padrão é 0,10.</span><span class="sxs-lookup"><span data-stu-id="b40bb-120">The default value is 0.10.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b40bb-121"><strong>VideoLocalFrameLostPercentageAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-121"><strong>VideoLocalFrameLostPercentageAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-122">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="b40bb-122">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-123">O valor padrão é 5,0.</span><span class="sxs-lookup"><span data-stu-id="b40bb-123">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b40bb-124"><strong>VideoLocalFrameLostPercentageAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-124"><strong>VideoLocalFrameLostPercentageAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-125">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="b40bb-125">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-126">O valor padrão é 10,0.</span><span class="sxs-lookup"><span data-stu-id="b40bb-126">The default value is 10.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b40bb-127"><strong>RecvFrameRateAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-127"><strong>RecvFrameRateAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-128">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="b40bb-128">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-129">O valor padrão é 12, 0.</span><span class="sxs-lookup"><span data-stu-id="b40bb-129">The default value is 12.0000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b40bb-130"><strong>RecvFramerateAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-130"><strong>RecvFramerateAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-131">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="b40bb-131">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-132">O valor padrão é 7, 0.</span><span class="sxs-lookup"><span data-stu-id="b40bb-132">The default value is 7.0000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b40bb-133"><strong>LowFrameRateCallPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-133"><strong>LowFrameRateCallPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-134">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="b40bb-134">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-135">O valor padrão é 5,0.</span><span class="sxs-lookup"><span data-stu-id="b40bb-135">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b40bb-136"><strong>LowFrameRateCallPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-136"><strong>LowFrameRateCallPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-137">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="b40bb-137">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-138">O valor padrão é 10.0/</span><span class="sxs-lookup"><span data-stu-id="b40bb-138">The default value is 10.0/</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b40bb-139"><strong>LowResolutionCallPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-139"><strong>LowResolutionCallPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-140">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="b40bb-140">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-141">O valor padrão é 5,0.</span><span class="sxs-lookup"><span data-stu-id="b40bb-141">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b40bb-142"><strong>LowResolutionCallPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-142"><strong>LowResolutionCallPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-143">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="b40bb-143">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-144">O valor padrão é 10,0.</span><span class="sxs-lookup"><span data-stu-id="b40bb-144">The default value is 10.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b40bb-145"><strong>VideoPacketLossRateOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-145"><strong>VideoPacketLossRateOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-146">foat</span><span class="sxs-lookup"><span data-stu-id="b40bb-146">foat</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-147">O valor padrão é 0, 5.</span><span class="sxs-lookup"><span data-stu-id="b40bb-147">The default value is 0.05.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b40bb-148"><strong>VideoPacketLossRateAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-148"><strong>VideoPacketLossRateAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-149">float</span><span class="sxs-lookup"><span data-stu-id="b40bb-149">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-150">O valor padrão é 0,10.</span><span class="sxs-lookup"><span data-stu-id="b40bb-150">The default value is 0.10.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b40bb-151"><strong>VideoFrameRateAvgOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-151"><strong>VideoFrameRateAvgOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-152">float</span><span class="sxs-lookup"><span data-stu-id="b40bb-152">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-153">O valor padrão é 12.</span><span class="sxs-lookup"><span data-stu-id="b40bb-153">The default value is 12.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b40bb-154"><strong>VideoFrameRateAvgAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-154"><strong>VideoFrameRateAvgAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-155">float</span><span class="sxs-lookup"><span data-stu-id="b40bb-155">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-156">O valor padrão é 7.</span><span class="sxs-lookup"><span data-stu-id="b40bb-156">The default value is 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b40bb-157"><strong>DynamicCapabilityPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-157"><strong>DynamicCapabilityPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-158">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="b40bb-158">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-159">O valor padrão é 5, 0.</span><span class="sxs-lookup"><span data-stu-id="b40bb-159">The default value is 5.00.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b40bb-160"><strong>DynamicCapabilityPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="b40bb-160"><strong>DynamicCapabilityPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="b40bb-161">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="b40bb-161">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b40bb-162">O valor padrão é 10, 0.</span><span class="sxs-lookup"><span data-stu-id="b40bb-162">The default value is 10.00.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b40bb-163">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b40bb-163">


</div>

<span> </span>

</div>

</div>

</span></span></div>

