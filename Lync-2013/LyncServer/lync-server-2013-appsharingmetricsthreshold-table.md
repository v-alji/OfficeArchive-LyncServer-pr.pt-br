---
title: 'Lync Server 2013: tabela AppSharingMetricsThreshold'
description: 'Lync Server 2013: AppSharingMetricsThreshold Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingMetricsThreshold table
ms:assetid: 782cfab9-01a6-4843-aea1-28f47b0b51f7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205018(v=OCS.15)
ms:contentKeyID: 48184556
ms.date: 12/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 092c7d08026e6b736b81043a71b4ecaabc4d5f1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439862"
---
# <a name="appsharingmetricsthreshold-table-in-lync-server-2013"></a><span data-ttu-id="d14e2-103">Tabela AppSharingMetricsThreshold no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d14e2-103">AppSharingMetricsThreshold table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d14e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d14e2-104">

<span> </span></span></span>

<span data-ttu-id="d14e2-105">_**Tópico da última modificação:** 2015-12-08_</span><span class="sxs-lookup"><span data-stu-id="d14e2-105">_**Topic Last Modified:** 2015-12-08_</span></span>

<span data-ttu-id="d14e2-106">A tabela AppSharingMetricsThreshold contém os valores ideais e aceitáveis para as métricas de qualidade da experiência usadas com o compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d14e2-106">The AppSharingMetricsThreshold table contains optimal and acceptable values for the Quality of Experience metrics used with application sharing.</span></span> <span data-ttu-id="d14e2-107">Esses limiares são usados para determinar se a experiência de compartilhamento de aplicativos deve ser classificada como ruim.</span><span class="sxs-lookup"><span data-stu-id="d14e2-107">These thresholds are used to determine if the application sharing experience should be classified as poor.</span></span>

<span data-ttu-id="d14e2-108">Esta tabela foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d14e2-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d14e2-109"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="d14e2-110"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="d14e2-111"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="d14e2-112"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d14e2-113"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-113"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="d14e2-114">int</span><span class="sxs-lookup"><span data-stu-id="d14e2-114">int</span></span></p></td>
<td><p><span data-ttu-id="d14e2-115">Primária</span><span class="sxs-lookup"><span data-stu-id="d14e2-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="d14e2-116">Tipo de chamada que foi feita.</span><span class="sxs-lookup"><span data-stu-id="d14e2-116">Type of call that was placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d14e2-117"><strong>AppliedBandwidthLimitOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-117"><strong>AppliedBandwidthLimitOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d14e2-118">int</span><span class="sxs-lookup"><span data-stu-id="d14e2-118">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d14e2-119">Limitação de largura de banda ideal para compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d14e2-119">Optimal bandwidth limitation for application sharing.</span></span> <span data-ttu-id="d14e2-120">O valor padrão é 1 milhão.</span><span class="sxs-lookup"><span data-stu-id="d14e2-120">The default value is 1000000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d14e2-121"><strong>AppliedBandwidthLimitAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-121"><strong>AppliedBandwidthLimitAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="d14e2-122">int</span><span class="sxs-lookup"><span data-stu-id="d14e2-122">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d14e2-123">Limitação de largura de banda aceitável para compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d14e2-123">Acceptable bandwidth limitation for application sharing.</span></span> <span data-ttu-id="d14e2-124">O valor padrão é 500000.</span><span class="sxs-lookup"><span data-stu-id="d14e2-124">The default value is 500000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d14e2-125"><strong>SpoiledTilePercentTotalOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-125"><strong>SpoiledTilePercentTotalOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d14e2-126">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d14e2-126">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d14e2-127">A taxa de porcentagem ideal para blocos "danificados" para classificar uma qualidade de compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d14e2-127">Optimal percentage rate for “spoiled” tiles for classifying an Application Sharing quality.</span></span> <span data-ttu-id="d14e2-128">Esse valor é a porcentagem do conteúdo do participante do compartilhamento que não tinha chegado ao visualizador.</span><span class="sxs-lookup"><span data-stu-id="d14e2-128">This value is the percentage of the content from the sharer that did not reach the viewer.</span></span> <span data-ttu-id="d14e2-129">O conteúdo pode ser descartado (ou danificados) quando o participante do compartilhamento descarta blocos da fonte gráfica ou os blocos do ASMCU descartam os blocos do participante do compartilhamento, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d14e2-129">Content may be discarded (or spoiled) when the sharer discards tiles from the graphics source or the ASMCU tiles discards tiles from Sharer respectively.</span></span> <span data-ttu-id="d14e2-130">O valor padrão é 11%.</span><span class="sxs-lookup"><span data-stu-id="d14e2-130">The default value is 11 percent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d14e2-131"><strong>SpoiledTilePercentTotalAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-131"><strong>SpoiledTilePercentTotalAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="d14e2-132">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="d14e2-132">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d14e2-133">cceptable a taxa de porcentagem para blocos "danificados" para classificar uma qualidade de compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d14e2-133">cceptable percentage rate for “spoiled” tiles for classifying an Application Sharing quality.</span></span> <span data-ttu-id="d14e2-134">Esse valor é a porcentagem do conteúdo do participante do compartilhamento que não tinha chegado ao visualizador.</span><span class="sxs-lookup"><span data-stu-id="d14e2-134">This value is the percentage of the content from the sharer that did not reach the viewer.</span></span> <span data-ttu-id="d14e2-135">O conteúdo pode ser descartado (ou danificados) quando o participante do compartilhamento descarta blocos da fonte gráfica ou os blocos do ASMCU descartam os blocos do participante do compartilhamento, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d14e2-135">Content may be discarded (or spoiled) when the sharer discards tiles from the graphics source or the ASMCU tiles discards tiles from Sharer respectively.</span></span> <span data-ttu-id="d14e2-136">O valor padrão é 36%.</span><span class="sxs-lookup"><span data-stu-id="d14e2-136">The default value is 36 percent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d14e2-137"><strong>JitterInterArrivalOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-137"><strong>JitterInterArrivalOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d14e2-138">int</span><span class="sxs-lookup"><span data-stu-id="d14e2-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d14e2-139">Esta coluna não é usada no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d14e2-139">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d14e2-140"><strong>JitterInterArrivalAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-140"><strong>JitterInterArrivalAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="d14e2-141">int</span><span class="sxs-lookup"><span data-stu-id="d14e2-141">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d14e2-142">Esta coluna não é usada no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d14e2-142">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d14e2-143"><strong>RelativeOneWayBurstDensityOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-143"><strong>RelativeOneWayBurstDensityOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d14e2-144">float</span><span class="sxs-lookup"><span data-stu-id="d14e2-144">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d14e2-145">Esta coluna não é usada no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d14e2-145">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d14e2-146"><strong>RelativeOneWayBurstDensityAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-146"><strong>RelativeOneWayBurstDensityAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="d14e2-147">float</span><span class="sxs-lookup"><span data-stu-id="d14e2-147">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d14e2-148">Esta coluna não é usada no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d14e2-148">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d14e2-149"><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-149"><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d14e2-150">float</span><span class="sxs-lookup"><span data-stu-id="d14e2-150">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d14e2-151">Esta coluna não é usada no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d14e2-151">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d14e2-152"><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-152"><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="d14e2-153">float</span><span class="sxs-lookup"><span data-stu-id="d14e2-153">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d14e2-154">Esta coluna não é usada no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d14e2-154">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d14e2-155"><strong>RelativeOneWayAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-155"><strong>RelativeOneWayAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d14e2-156">float</span><span class="sxs-lookup"><span data-stu-id="d14e2-156">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d14e2-157">Valor ideal para o atraso unidirecional relativo entre os dois pontos de extremidade de mídia envolvidos no compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d14e2-157">Optimal value for the relative one-way delay between the two media endpoints involved in the application sharing.</span></span> <span data-ttu-id="d14e2-158">Esta é uma medida de latência de salto único.</span><span class="sxs-lookup"><span data-stu-id="d14e2-158">This is a single-hop latency measure.</span></span> <span data-ttu-id="d14e2-159">O valor padrão é 1,0 segundos.</span><span class="sxs-lookup"><span data-stu-id="d14e2-159">The default value is 1.0 seconds.</span></span></p>
<p><span data-ttu-id="d14e2-160">A coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d14e2-160">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d14e2-161"><strong>RelativeOneWayAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-161"><strong>RelativeOneWayAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="d14e2-162">float</span><span class="sxs-lookup"><span data-stu-id="d14e2-162">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d14e2-163">Valor ideal para o atraso unidirecional relativo entre os dois pontos de extremidade de mídia envolvidos no compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d14e2-163">Optimal value for the relative one-way delay between the two media endpoints involved in the application sharing.</span></span> <span data-ttu-id="d14e2-164">Esta é uma medida de latência de salto único.</span><span class="sxs-lookup"><span data-stu-id="d14e2-164">This is a single-hop latency measure.</span></span> <span data-ttu-id="d14e2-165">O valor padrão é 1,75 segundos.</span><span class="sxs-lookup"><span data-stu-id="d14e2-165">The default value is 1.75 seconds.</span></span></p>
<p><span data-ttu-id="d14e2-166">A coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d14e2-166">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d14e2-167"><strong>RDPTileProcessingLatencyAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-167"><strong>RDPTileProcessingLatencyAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d14e2-168">float</span><span class="sxs-lookup"><span data-stu-id="d14e2-168">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d14e2-169">O valor ideal da latência média de processamento de bloco RDP no servidor de conferência as na duração da sessão de exibição.</span><span class="sxs-lookup"><span data-stu-id="d14e2-169">Optimal value of the average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session.</span></span> <span data-ttu-id="d14e2-170">Latência é a diferença de tempo entre o momento em que o quadro inicial é codificado no servidor (participante do compartilhamento ou MCU, dependendo do cenário) e o mesmo quadro inicial é decodificado no visualizador.</span><span class="sxs-lookup"><span data-stu-id="d14e2-170">Latency is the time difference between when the Start Frame is encoded on the server (sharer or MCU depending on the scenario) and the same Start Frame is decoded on the viewer.</span></span></p>
<p><span data-ttu-id="d14e2-171">Uma média alta reflete um atraso maior na experiência de visualização.</span><span class="sxs-lookup"><span data-stu-id="d14e2-171">A high average reflects a longer delay in the viewing experience.</span></span> <span data-ttu-id="d14e2-172">Um servidor de conferência sobrecarregado pode enfrentar atrasos médios maiores.</span><span class="sxs-lookup"><span data-stu-id="d14e2-172">An overloaded conferencing server may experience higher average delays.</span></span> <span data-ttu-id="d14e2-173">O valor padrão é 200ms.</span><span class="sxs-lookup"><span data-stu-id="d14e2-173">The default value is 200ms.</span></span></p>
<p><span data-ttu-id="d14e2-174">A coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d14e2-174">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d14e2-175"><strong>RDPTileProcessingLatencyAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="d14e2-175"><strong>RDPTileProcessingLatencyAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="d14e2-176">float</span><span class="sxs-lookup"><span data-stu-id="d14e2-176">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d14e2-177">Valor aceitável da latência média de processamento de bloco RDP no servidor de conferência as na duração da sessão de exibição.</span><span class="sxs-lookup"><span data-stu-id="d14e2-177">Acceptable value of the average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session.</span></span> <span data-ttu-id="d14e2-178">Latência é a diferença de tempo entre o momento em que o quadro inicial é codificado no servidor (participante do compartilhamento ou MCU, dependendo do cenário) e o mesmo quadro inicial é decodificado no visualizador.</span><span class="sxs-lookup"><span data-stu-id="d14e2-178">Latency is the time difference between when the Start Frame is encoded on the server (sharer or MCU depending on the scenario) and the same Start Frame is decoded on the viewer.</span></span></p>
<p><span data-ttu-id="d14e2-179">Uma média alta reflete um atraso maior na experiência de visualização.</span><span class="sxs-lookup"><span data-stu-id="d14e2-179">A high average reflects a longer delay in the viewing experience.</span></span> <span data-ttu-id="d14e2-180">Um servidor de conferência sobrecarregado pode enfrentar atrasos médios maiores.</span><span class="sxs-lookup"><span data-stu-id="d14e2-180">An overloaded conferencing server may experience higher average delays.</span></span> <span data-ttu-id="d14e2-181">O valor padrão é 200ms.</span><span class="sxs-lookup"><span data-stu-id="d14e2-181">The default value is 200ms.</span></span></p>
<p><span data-ttu-id="d14e2-182">A coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d14e2-182">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d14e2-183">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d14e2-183">


</div>

<span> </span>

</div>

</div>

</span></span></div>

