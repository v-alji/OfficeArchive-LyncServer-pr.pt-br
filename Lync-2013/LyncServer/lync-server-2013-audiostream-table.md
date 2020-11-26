---
title: 'Lync Server 2013: Tabela AudioStream'
description: 'Lync Server 2013: AudioStream Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStream table
ms:assetid: 49ccbbc3-2f73-45fc-80a6-e612535cbc10
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425961(v=OCS.15)
ms:contentKeyID: 48184077
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af2e622e14c54fa4f9a6313e1b0dae8f2483132
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438173"
---
# <a name="audiostream-table-in-lync-server-2013"></a><span data-ttu-id="e4420-103">Tabela AudioStream no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e4420-103">AudioStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e4420-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e4420-104">

<span> </span></span></span>

<span data-ttu-id="e4420-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="e4420-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="e4420-106">Cada registro representa um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="e4420-106">Each record represents one audio stream.</span></span> <span data-ttu-id="e4420-107">Uma linha de mídia de áudio geralmente contém dois fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="e4420-107">One audio media line usually contains two audio streams.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e4420-108"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="e4420-109"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="e4420-110"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="e4420-111"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4420-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-113">datetime</span><span class="sxs-lookup"><span data-stu-id="e4420-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="e4420-114">Primária</span><span class="sxs-lookup"><span data-stu-id="e4420-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="e4420-115">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e4420-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-117">int</span><span class="sxs-lookup"><span data-stu-id="e4420-117">int</span></span></p></td>
<td><p><span data-ttu-id="e4420-118">Primária</span><span class="sxs-lookup"><span data-stu-id="e4420-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="e4420-119">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e4420-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="e4420-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e4420-122">Primária</span><span class="sxs-lookup"><span data-stu-id="e4420-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="e4420-123">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e4420-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-124"><strong>Streamid</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-124"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-125">int</span><span class="sxs-lookup"><span data-stu-id="e4420-125">int</span></span></p></td>
<td><p><span data-ttu-id="e4420-126">Primária</span><span class="sxs-lookup"><span data-stu-id="e4420-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="e4420-127">ID exclusiva dentro de uma linha de mídia.</span><span class="sxs-lookup"><span data-stu-id="e4420-127">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-128"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-128"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-129">int</span><span class="sxs-lookup"><span data-stu-id="e4420-129">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-130">Tremulação média de rede de estatísticas de protocolo de controle de tempo real (RTCP).</span><span class="sxs-lookup"><span data-stu-id="e4420-130">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-131"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-131"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-132">int</span><span class="sxs-lookup"><span data-stu-id="e4420-132">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-133">Maior tremulação de rede durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-133">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-134"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-134"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-135">decimal (5, 4)</span><span class="sxs-lookup"><span data-stu-id="e4420-135">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-136">Taxa média de perda de pacotes durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-136">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-137"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-137"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-138">decimal (5, 4)</span><span class="sxs-lookup"><span data-stu-id="e4420-138">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-139">Perda máxima de pacote observado durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-139">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-140"><strong>BurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-140"><strong>BurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-141">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="e4420-141">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-142">Densidade média de perda de pacote durante intermitências de perdas durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-142">Average density of packet Loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-143"><strong>BurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-143"><strong>BurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-144">int</span><span class="sxs-lookup"><span data-stu-id="e4420-144">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-145">Duração média da perda de pacote durante intermitências de perdas durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-145">Average duration of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-146"><strong>BurstGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-146"><strong>BurstGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-147">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="e4420-147">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-148">Densidade média de perda de pacote durante intervalos entre intermitências de perda de pacote.</span><span class="sxs-lookup"><span data-stu-id="e4420-148">Average density of packet loss during gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-149"><strong>BurstGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-149"><strong>BurstGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-150">int</span><span class="sxs-lookup"><span data-stu-id="e4420-150">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-151">Duração média de lacunas entre intermitências de perda de pacote.</span><span class="sxs-lookup"><span data-stu-id="e4420-151">Average duration of gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-152"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-152"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-153">Núm</span><span class="sxs-lookup"><span data-stu-id="e4420-153">Int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-154">Contagem de pacotes para o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="e4420-154">Packet count for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-155"><strong>Largura de banda</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-155"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-156">Núm</span><span class="sxs-lookup"><span data-stu-id="e4420-156">Int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-157">Estimativas de largura de banda para o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="e4420-157">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-158"><strong>DegradationAvg</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-158"><strong>DegradationAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-159">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="e4420-159">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-160">Degradação do MOS de rede para toda a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-160">Network MOS Degradation for the whole call.</span></span> <span data-ttu-id="e4420-161">O intervalo é de 0,0 a 5,0.</span><span class="sxs-lookup"><span data-stu-id="e4420-161">Range is 0.0 to 5.0.</span></span> <span data-ttu-id="e4420-162">Essa métrica mostra o valor que o MOS de rede foi reduzido devido à instabilidade e à perda de pacote.</span><span class="sxs-lookup"><span data-stu-id="e4420-162">This metric shows the amount the Network MOS was reduced because of jitter and packet loss.</span></span> <span data-ttu-id="e4420-163">Para ter uma qualidade aceitável, ele deve ser menor do que 0,5.</span><span class="sxs-lookup"><span data-stu-id="e4420-163">For acceptable quality it should less than 0.5.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-164"><strong>DegradationMax</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-164"><strong>DegradationMax</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-165">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="e4420-165">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-166">Degradação do MOS de rede máxima durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-166">Maximum Network MOS degradation during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-167"><strong>DegradationJitterAvg</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-167"><strong>DegradationJitterAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-168">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="e4420-168">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-169">Degradação de MOS de rede causada pela tremulação.</span><span class="sxs-lookup"><span data-stu-id="e4420-169">Network MOS degradation caused by jitter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-170"><strong>DegradationPacketLossAvg</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-170"><strong>DegradationPacketLossAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-171">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="e4420-171">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-172">Degradação de MOS de rede causada por perda de pacote.</span><span class="sxs-lookup"><span data-stu-id="e4420-172">Network MOS degradation caused by packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-173"><strong>AudioPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-173"><strong>AudioPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-174">int</span><span class="sxs-lookup"><span data-stu-id="e4420-174">int</span></span></p></td>
<td><p><span data-ttu-id="e4420-175">Exterior</span><span class="sxs-lookup"><span data-stu-id="e4420-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4420-176">O codec de áudio usado para a chamada, referenciado pela tabela PayloadDescription.</span><span class="sxs-lookup"><span data-stu-id="e4420-176">The audio Codec used for the call, referenced from PayloadDescription Table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-177"><strong>AudioSampleRate</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-177"><strong>AudioSampleRate</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-178">int</span><span class="sxs-lookup"><span data-stu-id="e4420-178">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-179">Taxa de amostragem do fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="e4420-179">Sampling rate for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-180"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-180"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-181">int</span><span class="sxs-lookup"><span data-stu-id="e4420-181">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-182">Tempo de ida e volta das estatísticas do RTCP.</span><span class="sxs-lookup"><span data-stu-id="e4420-182">Round trip time from RTCP statistics.</span></span> <span data-ttu-id="e4420-183">Para ter uma qualidade aceitável, isso deve ser menor que 100 milhões.</span><span class="sxs-lookup"><span data-stu-id="e4420-183">For acceptable quality this should be less than 100ms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-184"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-184"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-185">int</span><span class="sxs-lookup"><span data-stu-id="e4420-185">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-186">Tempo máximo de ida e volta do fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="e4420-186">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-187"><strong>OverallAvgNetworkMOS</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-187"><strong>OverallAvgNetworkMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-188">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="e4420-188">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-189">Banda larga médio de um MOS de rede para a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-189">Average wideband Network MOS for the call.</span></span> <span data-ttu-id="e4420-190">Essa métrica depende da perda de pacotes, da tremulação e do codec usados.</span><span class="sxs-lookup"><span data-stu-id="e4420-190">This metric depends on the packet loss, jitter, and codec used.</span></span> <span data-ttu-id="e4420-191">O intervalo é de [1,0 a 5,0].</span><span class="sxs-lookup"><span data-stu-id="e4420-191">Range is [1.0 to 5.0].</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-192"><strong>OverallMinNetworkMOS</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-192"><strong>OverallMinNetworkMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-193">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="e4420-193">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-194">A banda larga de rede mínima para a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-194">The minimum wideband Network MOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-195"><strong>SendListenMOS</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-195"><strong>SendListenMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-196">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="e4420-196">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-197">A média de Pontuação estimada banda larga de escuta do MOS para áudio enviado, incluindo o nível de fala, o nível de ruído e as características do dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="e4420-197">The average predicted wideband Listening MOS score for audio sent, including speech level, noise level and capture device characteristics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-198"><strong>SendListenMOSMin</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-198"><strong>SendListenMOSMin</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-199">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="e4420-199">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-200">A SendListenMOS mínima para a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-200">The minimum SendListenMOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-201"><strong>RecvListenMOS</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-201"><strong>RecvListenMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-202">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="e4420-202">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-203">A média de Pontuação estimada banda larga de escuta do MOS para áudio recebido da rede, incluindo o nível de fala, o nível de ruído, o codec, as condições de rede e as características do dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="e4420-203">The average predicted wideband Listening MOS score for audio received from the network including speech level, noise level, codec, network conditions and capture device characteristics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-204"><strong>RecvListenMOSMin</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-204"><strong>RecvListenMOSMin</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-205">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="e4420-205">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-206">A RecvListenMOS mínima para a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-206">The minimum RecvListenMOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-207"><strong>AudioFECUsed</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-207"><strong>AudioFECUsed</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-208">bit</span><span class="sxs-lookup"><span data-stu-id="e4420-208">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-209">Sinalizador que indica se o FEC de áudio foi usado para a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-209">Flag indicating if audio FEC was used for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-210"><strong>RatioConcealedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-210"><strong>RatioConcealedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-211">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="e4420-211">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-212">Índice médio de amostras ocultas geradas pelo reparo de áudio para amostras típicas.</span><span class="sxs-lookup"><span data-stu-id="e4420-212">Average ratio of concealed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-213"><strong>RatioStretchedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-213"><strong>RatioStretchedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-214">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="e4420-214">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-215">Índice médio de amostras ampliadas geradas pelo reparo de áudio para amostras típicas.</span><span class="sxs-lookup"><span data-stu-id="e4420-215">Average ratio of stretched samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-216"><strong>RatioCompressedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-216"><strong>RatioCompressedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-217">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="e4420-217">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-218">Índice médio de amostras compactadas geradas pelo reparo de áudio para amostras típicas.</span><span class="sxs-lookup"><span data-stu-id="e4420-218">Average ratio of compressed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-219"><strong>Entrada</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-219"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-220">bit</span><span class="sxs-lookup"><span data-stu-id="e4420-220">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-221">Os dados de fluxo no lado do receptor são recebidos.</span><span class="sxs-lookup"><span data-stu-id="e4420-221">Stream data on receiver side is received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-222"><strong>Saída</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-222"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-223">bit</span><span class="sxs-lookup"><span data-stu-id="e4420-223">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-224">Dados de fluxo no lado do remetente são recebidos.</span><span class="sxs-lookup"><span data-stu-id="e4420-224">Stream data on sender side is received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-225"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-225"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-226">bit</span><span class="sxs-lookup"><span data-stu-id="e4420-226">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4420-227">1 significa que a direção do fluxo é do chamador para o receptor.</span><span class="sxs-lookup"><span data-stu-id="e4420-227">1 means the stream direction is from the caller to the callee.</span></span></p>
<p><span data-ttu-id="e4420-228">0 significa que a direção do fluxo é do receptor para o chamador.</span><span class="sxs-lookup"><span data-stu-id="e4420-228">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-229"><strong>JitterInterArrivalSD</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-229"><strong>JitterInterArrivalSD</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-230">float</span><span class="sxs-lookup"><span data-stu-id="e4420-230">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-231">Desvio padrão de tempos de chegada de tremulação.</span><span class="sxs-lookup"><span data-stu-id="e4420-231">Standard deviation for jitter arrival times.</span></span></p>
<p><span data-ttu-id="e4420-232">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-232">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-233"><strong>ConcealRatioMax</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-233"><strong>ConcealRatioMax</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-234">float</span><span class="sxs-lookup"><span data-stu-id="e4420-234">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-235">Índice máximo de pacotes ocultados pelo REO reparo.</span><span class="sxs-lookup"><span data-stu-id="e4420-235">Maximum ratio of packets concealed by the healer.</span></span></p>
<p><span data-ttu-id="e4420-236">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-236">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-237"><strong>ConcealRatioSD</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-237"><strong>ConcealRatioSD</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-238">float</span><span class="sxs-lookup"><span data-stu-id="e4420-238">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-239">Desvio padrão da taxa de pacotes ocultados pelo REO reparo.</span><span class="sxs-lookup"><span data-stu-id="e4420-239">Standard deviation for the ratio of packets concealed by the healer.</span></span></p>
<p><span data-ttu-id="e4420-240">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-240">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-241"><strong>HealerPacketDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-241"><strong>HealerPacketDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-242">float</span><span class="sxs-lookup"><span data-stu-id="e4420-242">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-243">Taxa de pacotes removidos pelo REO reparo em comparação ao número total de pacotes recebidos.</span><span class="sxs-lookup"><span data-stu-id="e4420-243">Ratio of packets dropped by the healer compared to the total number of packets received.</span></span></p>
<p><span data-ttu-id="e4420-244">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-244">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-245"><strong>HealerFECPacketUsedRatio</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-245"><strong>HealerFECPacketUsedRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-246">float</span><span class="sxs-lookup"><span data-stu-id="e4420-246">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-247">Taxa de pacotes de correção de erro usados encaminhar em comparação com o número total de pacotes recebidos.</span><span class="sxs-lookup"><span data-stu-id="e4420-247">Ratio of used forward error correction packets compared to the total number of packets received.</span></span></p>
<p><span data-ttu-id="e4420-248">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-248">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-249"><strong>MaxCompressedSamples</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-249"><strong>MaxCompressedSamples</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-250">float</span><span class="sxs-lookup"><span data-stu-id="e4420-250">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-251">Número máximo de pacotes de áudio que foram compactados pelo REO reparo.</span><span class="sxs-lookup"><span data-stu-id="e4420-251">Maximum number of audio packets that were compressed by the healer.</span></span></p>
<p><span data-ttu-id="e4420-252">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-252">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-253"><strong>LossCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-253"><strong>LossCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-254">float</span><span class="sxs-lookup"><span data-stu-id="e4420-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-255">Indica a porcentagem do tempo em que a chamada estava em um estado de congestionamento de perda.</span><span class="sxs-lookup"><span data-stu-id="e4420-255">Indicates the percentage of the time when the call was in a loss congestion state.</span></span></p>
<p><span data-ttu-id="e4420-256">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-256">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-257"><strong>DelayCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-257"><strong>DelayCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-258">float</span><span class="sxs-lookup"><span data-stu-id="e4420-258">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-259">Indica a porcentagem da chamada durante a qual o congestionamento foi causado pela chegada atrasada dos pacotes de rede.</span><span class="sxs-lookup"><span data-stu-id="e4420-259">Indicates the percentage of the call during which congestion was caused by the delayed arrival of network packets.</span></span></p>
<p><span data-ttu-id="e4420-260">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-260">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-261"><strong>ContentionDetectedPercent</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-261"><strong>ContentionDetectedPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-262">float</span><span class="sxs-lookup"><span data-stu-id="e4420-262">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-263">Indica a porcentagem do tempo quando a chamada estava competindo pelos recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="e4420-263">Indicates the percentage of the time when the call was competing for network resources.</span></span></p>
<p><span data-ttu-id="e4420-264">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-264">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-265"><strong>BandwidthEstMin</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-265"><strong>BandwidthEstMin</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-266">int</span><span class="sxs-lookup"><span data-stu-id="e4420-266">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-267">Valor mínimo de estimativa de largura de banda medida durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-267">Minimum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="e4420-268">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-268">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-269"><strong>BandwidthEstMax</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-269"><strong>BandwidthEstMax</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-270">int</span><span class="sxs-lookup"><span data-stu-id="e4420-270">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-271">Valor máximo de estimativa de largura de banda medida durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-271">Maximum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="e4420-272">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-272">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-273"><strong>BandwidthEstStdDev</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-273"><strong>BandwidthEstStdDev</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-274">int</span><span class="sxs-lookup"><span data-stu-id="e4420-274">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-275">O desvio padrão da estimativa de largura de banda medida durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-275">Standard deviation of the bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="e4420-276">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-276">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-277"><strong>BandwidthEstAvge</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-277"><strong>BandwidthEstAvge</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-278">int</span><span class="sxs-lookup"><span data-stu-id="e4420-278">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-279">Valor médio da estimativa de largura de banda medida durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="e4420-279">Average amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="e4420-280">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-280">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-281"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-281"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-282">float</span><span class="sxs-lookup"><span data-stu-id="e4420-282">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-283">Valor total de latência unidirecional.</span><span class="sxs-lookup"><span data-stu-id="e4420-283">Total amount of one-way latency.</span></span> <span data-ttu-id="e4420-284">A latência unidirecional relativa mede o atraso entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="e4420-284">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="e4420-285">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-285">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-286"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-286"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-287">float</span><span class="sxs-lookup"><span data-stu-id="e4420-287">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-288">Valor médio de uma latência unidirecional.</span><span class="sxs-lookup"><span data-stu-id="e4420-288">Average amount of one-way latency.</span></span> <span data-ttu-id="e4420-289">A latência unidirecional relativa mede o atraso entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="e4420-289">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="e4420-290">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-290">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-291"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-291"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-292">float</span><span class="sxs-lookup"><span data-stu-id="e4420-292">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-293">Valor máximo de latência unidirecional.</span><span class="sxs-lookup"><span data-stu-id="e4420-293">Maximum amount of one-way latency.</span></span> <span data-ttu-id="e4420-294">A latência unidirecional relativa mede o atraso entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="e4420-294">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="e4420-295">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-295">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-296"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-296"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-297">int</span><span class="sxs-lookup"><span data-stu-id="e4420-297">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-298">Total de ocorrências intermitentes unidirecionais.</span><span class="sxs-lookup"><span data-stu-id="e4420-298">Total one-way burst occurrences.</span></span> <span data-ttu-id="e4420-299">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante.</span><span class="sxs-lookup"><span data-stu-id="e4420-299">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="e4420-300">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="e4420-300">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="e4420-301">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-301">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-302"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-302"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-303">float</span><span class="sxs-lookup"><span data-stu-id="e4420-303">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-304">Densidade total de intermitência unidirecional.</span><span class="sxs-lookup"><span data-stu-id="e4420-304">Total one-way burst density.</span></span> <span data-ttu-id="e4420-305">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante.</span><span class="sxs-lookup"><span data-stu-id="e4420-305">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="e4420-306">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="e4420-306">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="e4420-307">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-307">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-308"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-308"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-309">float</span><span class="sxs-lookup"><span data-stu-id="e4420-309">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-310">Duração total de intermitência unidirecional.</span><span class="sxs-lookup"><span data-stu-id="e4420-310">Total one-way burst duration.</span></span> <span data-ttu-id="e4420-311">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante.</span><span class="sxs-lookup"><span data-stu-id="e4420-311">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="e4420-312">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="e4420-312">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="e4420-313">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-313">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-314"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-314"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-315">int</span><span class="sxs-lookup"><span data-stu-id="e4420-315">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-316">Total de ocorrências de espaçamento unidirecionais.</span><span class="sxs-lookup"><span data-stu-id="e4420-316">Total one-way gap occurrences.</span></span> <span data-ttu-id="e4420-317">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante; as lacunas indicam atrasos entre essas intermitências.</span><span class="sxs-lookup"><span data-stu-id="e4420-317">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="e4420-318">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="e4420-318">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="e4420-319">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-319">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-320"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-320"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-321">float</span><span class="sxs-lookup"><span data-stu-id="e4420-321">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-322">Densidade total do espaço unidirecional.</span><span class="sxs-lookup"><span data-stu-id="e4420-322">Total one-way gap density.</span></span> <span data-ttu-id="e4420-323">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante; as lacunas indicam atrasos entre essas intermitências.</span><span class="sxs-lookup"><span data-stu-id="e4420-323">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="e4420-324">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="e4420-324">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="e4420-325">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-325">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-326"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-326"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-327">float</span><span class="sxs-lookup"><span data-stu-id="e4420-327">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-328">Duração total unidirecional do espaço.</span><span class="sxs-lookup"><span data-stu-id="e4420-328">Total one-way gap duration.</span></span> <span data-ttu-id="e4420-329">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante; as lacunas indicam atrasos entre essas intermitências.</span><span class="sxs-lookup"><span data-stu-id="e4420-329">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="e4420-330">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="e4420-330">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="e4420-331">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-331">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-332"><strong>DecodeStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-332"><strong>DecodeStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-333">float</span><span class="sxs-lookup"><span data-stu-id="e4420-333">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-334">Porcentagem da chamada decodificada como estéreo.</span><span class="sxs-lookup"><span data-stu-id="e4420-334">Percentage of the call decoded as stereo.</span></span></p>
<p><span data-ttu-id="e4420-335">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-335">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-336"><strong>AecRenderStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-336"><strong>AecRenderStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-337">float</span><span class="sxs-lookup"><span data-stu-id="e4420-337">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-338">Porcentagem da chamada renderizada como estéreo pelo cancelador de eco acústico.</span><span class="sxs-lookup"><span data-stu-id="e4420-338">Percentage of the call rendered as stereo by the acoustic echo canceller.</span></span></p>
<p><span data-ttu-id="e4420-339">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-339">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-340"><strong>AudioPostFECPLR</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-340"><strong>AudioPostFECPLR</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-341">float</span><span class="sxs-lookup"><span data-stu-id="e4420-341">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-342">Taxa de perda de pacote após a aplicação da correção de erro de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="e4420-342">Packet loss rate after forward error correction has been applied.</span></span></p>
<p><span data-ttu-id="e4420-343">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-343">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4420-344"><strong>EncodeStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-344"><strong>EncodeStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-345">float</span><span class="sxs-lookup"><span data-stu-id="e4420-345">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-346">Porcentagem da chamada codificada como estéreo.</span><span class="sxs-lookup"><span data-stu-id="e4420-346">Percentage of the call encoded as stereo.</span></span></p>
<p><span data-ttu-id="e4420-347">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-347">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4420-348"><strong>AecCaptureStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="e4420-348"><strong>AecCaptureStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="e4420-349">float</span><span class="sxs-lookup"><span data-stu-id="e4420-349">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4420-350">Porcentagem da chamada capturada como estéreo pelo cancelador de eco acústico.</span><span class="sxs-lookup"><span data-stu-id="e4420-350">Percentage of the call captured as stereo by the acoustic echo canceller.</span></span></p>
<p><span data-ttu-id="e4420-351">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e4420-351">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e4420-352">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e4420-352">


</div>

<span> </span>

</div>

</div>

</span></span></div>

