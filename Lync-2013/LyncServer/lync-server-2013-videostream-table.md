---
title: 'Lync Server 2013: Tabela VideoStream'
description: 'Lync Server 2013: VideoStream Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStream table
ms:assetid: 4275ede7-5467-4a97-b8c8-a4b00917bf32
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425928(v=OCS.15)
ms:contentKeyID: 48184014
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d741478e1f6290685181bff471f143e41ce9ca1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444123"
---
# <a name="videostream-table-in-lync-server-2013"></a><span data-ttu-id="062d6-103">Tabela VideoStream no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="062d6-103">VideoStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="062d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="062d6-104">

<span> </span></span></span>

<span data-ttu-id="062d6-105">_**Tópico da última modificação:** 2013-12-13_</span><span class="sxs-lookup"><span data-stu-id="062d6-105">_**Topic Last Modified:** 2013-12-13_</span></span>

<span data-ttu-id="062d6-106">Cada registro representa um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="062d6-106">Each record represents one video stream.</span></span> <span data-ttu-id="062d6-107">Uma linha de mídia de vídeo geralmente contém dois fluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="062d6-107">One video media line usually contains two video streams.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="062d6-108"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="062d6-109"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="062d6-110"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="062d6-111"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="062d6-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-113">datetime</span><span class="sxs-lookup"><span data-stu-id="062d6-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="062d6-114">Primária</span><span class="sxs-lookup"><span data-stu-id="062d6-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="062d6-115">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="062d6-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-117">int</span><span class="sxs-lookup"><span data-stu-id="062d6-117">int</span></span></p></td>
<td><p><span data-ttu-id="062d6-118">Primária</span><span class="sxs-lookup"><span data-stu-id="062d6-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="062d6-119">R referenciada na <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="062d6-119">R Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="062d6-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="062d6-122">Primária</span><span class="sxs-lookup"><span data-stu-id="062d6-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="062d6-123">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="062d6-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-124"><strong>Streamid</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-124"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-125">int</span><span class="sxs-lookup"><span data-stu-id="062d6-125">int</span></span></p></td>
<td><p><span data-ttu-id="062d6-126">Primária</span><span class="sxs-lookup"><span data-stu-id="062d6-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="062d6-127">ID exclusiva dentro de uma linha de mídia.</span><span class="sxs-lookup"><span data-stu-id="062d6-127">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-128"><strong>VideoPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-128"><strong>VideoPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-129">smallint</span><span class="sxs-lookup"><span data-stu-id="062d6-129">smallint</span></span></p></td>
<td><p><span data-ttu-id="062d6-130">Estrangeiro, primário</span><span class="sxs-lookup"><span data-stu-id="062d6-130">Foreign, Primary</span></span></p></td>
<td><p><span data-ttu-id="062d6-131">Descrição da carga.</span><span class="sxs-lookup"><span data-stu-id="062d6-131">Payload description.</span></span> <span data-ttu-id="062d6-132">Consulte a <a href="lync-server-2013-payloaddescription-table.md">tabela PayloadDescription no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="062d6-132">See the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-133"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-133"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-134">int</span><span class="sxs-lookup"><span data-stu-id="062d6-134">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-135">Tremulação média de rede de estatísticas de protocolo de controle de tempo real (RTCP).</span><span class="sxs-lookup"><span data-stu-id="062d6-135">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-136"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-136"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-137">int</span><span class="sxs-lookup"><span data-stu-id="062d6-137">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-138">Maior tremulação de rede durante a sessão de vídeo.</span><span class="sxs-lookup"><span data-stu-id="062d6-138">Maximum network jitter during the video session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-139"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-139"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-140">int</span><span class="sxs-lookup"><span data-stu-id="062d6-140">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-141">Tempo de ida e volta das estatísticas do RTCP.</span><span class="sxs-lookup"><span data-stu-id="062d6-141">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-142"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-142"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-143">int</span><span class="sxs-lookup"><span data-stu-id="062d6-143">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-144">Tempo máximo de ida e volta do fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="062d6-144">Maximum round trip time for the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-145"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-145"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-146">decimal (5, 4)</span><span class="sxs-lookup"><span data-stu-id="062d6-146">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-147">Taxa média de perda de pacotes durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="062d6-147">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-148"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-148"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-149">decimal (5, 4)</span><span class="sxs-lookup"><span data-stu-id="062d6-149">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-150">Perda máxima de pacote observado durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="062d6-150">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-151"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-151"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-152">int</span><span class="sxs-lookup"><span data-stu-id="062d6-152">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-153">Contagem de pacotes para o fluxo de vídeo (protocolo de transporte em tempo real, RTP).</span><span class="sxs-lookup"><span data-stu-id="062d6-153">Packet count for the video stream (Real Time Transport Protocol, RTP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-154"><strong>Largura de banda</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-154"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-155">int</span><span class="sxs-lookup"><span data-stu-id="062d6-155">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-156">Estimativas de largura de banda para o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="062d6-156">Bandwidth estimates for the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-157"><strong>VideoResolution</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-157"><strong>VideoResolution</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-158">caractere (9)</span><span class="sxs-lookup"><span data-stu-id="062d6-158">char(9)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-159">Resolução do vídeo em largura de pixels multiplicada pela altura de pixels.</span><span class="sxs-lookup"><span data-stu-id="062d6-159">Resolution of the video in pixels width multiplied by pixels height.</span></span> <span data-ttu-id="062d6-160">Relatado como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="062d6-160">Reported as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-161"><strong>VideoBitRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-161"><strong>VideoBitRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-162">int</span><span class="sxs-lookup"><span data-stu-id="062d6-162">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-163">Taxa média de bits do fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="062d6-163">Average bit rate of the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-164"><strong>InboundVideoFrameRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-164"><strong>InboundVideoFrameRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-165">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="062d6-165">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-166">A taxa de quadros de vídeo recebida.</span><span class="sxs-lookup"><span data-stu-id="062d6-166">The video frame rate received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-167"><strong>OutboundVideoFrameRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-167"><strong>OutboundVideoFrameRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-168">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="062d6-168">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-169">A taxa de quadros de vídeo enviada.</span><span class="sxs-lookup"><span data-stu-id="062d6-169">The video frame rate sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-170"><strong>VideoBitRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-170"><strong>VideoBitRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-171">int</span><span class="sxs-lookup"><span data-stu-id="062d6-171">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-172">A taxa máxima de bits de vídeo durante a sessão de vídeo.</span><span class="sxs-lookup"><span data-stu-id="062d6-172">The maximum video bit rate during the video session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-173"><strong>VideoFrameLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-173"><strong>VideoFrameLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-174">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="062d6-174">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-175">A porcentagem total de quadros de vídeo perdidos.</span><span class="sxs-lookup"><span data-stu-id="062d6-175">The percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-176"><strong>VideoFEC</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-176"><strong>VideoFEC</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-177">bit</span><span class="sxs-lookup"><span data-stu-id="062d6-177">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-178">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="062d6-178">Not available.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-179"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-179"><strong>VideoLocalFrameLossPercentageAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-180">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="062d6-180">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-181">A porcentagem total de quadros de vídeo perdidos.</span><span class="sxs-lookup"><span data-stu-id="062d6-181">The percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-182"><strong>CIFQualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-182"><strong>CIFQualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-183">tinyint</span><span class="sxs-lookup"><span data-stu-id="062d6-183">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-184">A porcentagem da chamada que estava na resolução de formato de intercâmbio (CIF) comum.</span><span class="sxs-lookup"><span data-stu-id="062d6-184">The percentage of the call that was at the Common Interchange Format (CIF) resolution.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-185"><strong>VGAQualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-185"><strong>VGAQualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-186">tinyint</span><span class="sxs-lookup"><span data-stu-id="062d6-186">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-187">A porcentagem da chamada que estava na resolução VGA.</span><span class="sxs-lookup"><span data-stu-id="062d6-187">The percentage of the call that was at VGA resolution.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-188"><strong>HD720QualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-188"><strong>HD720QualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-189">tinyint</span><span class="sxs-lookup"><span data-stu-id="062d6-189">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-190">A porcentagem da chamada que estava a HD720 resolução.</span><span class="sxs-lookup"><span data-stu-id="062d6-190">The percentage of the call that was at HD720 resolution.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-191"><strong>NoneDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-191"><strong>NoneDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-192">tinyint</span><span class="sxs-lookup"><span data-stu-id="062d6-192">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-193">Porcentagem de duração da chamada sem depósito de quadro.</span><span class="sxs-lookup"><span data-stu-id="062d6-193">Percentage of call duration with no frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-194"><strong>BDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-194"><strong>BDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-195">tinyint</span><span class="sxs-lookup"><span data-stu-id="062d6-195">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-196">Porcentagem de duração da chamada com B frame drop.</span><span class="sxs-lookup"><span data-stu-id="062d6-196">Percentage of call duration with B frame drop.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-197"><strong>BPDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-197"><strong>BPDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-198">tinyint</span><span class="sxs-lookup"><span data-stu-id="062d6-198">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-199">Porcentagem da duração da chamada com o depósito de quadros BP.</span><span class="sxs-lookup"><span data-stu-id="062d6-199">Percentage of call duration with BP frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-200"><strong>BPSPDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-200"><strong>BPSPDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-201">tinyint</span><span class="sxs-lookup"><span data-stu-id="062d6-201">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-202">Porcentagem da duração da chamada com o BPSP frame drop.</span><span class="sxs-lookup"><span data-stu-id="062d6-202">Percentage of call duration with BPSP frame drop.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-203"><strong>BPSPIDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-203"><strong>BPSPIDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-204">tinyint</span><span class="sxs-lookup"><span data-stu-id="062d6-204">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-205">Porcentagem da duração da chamada com o BPSPI frame drop.</span><span class="sxs-lookup"><span data-stu-id="062d6-205">Percentage of call duration with BPSPI frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-206"><strong>Entrada</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-206"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-207">bit</span><span class="sxs-lookup"><span data-stu-id="062d6-207">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-208">Os dados de fluxo no lado do receptor são recebidos.</span><span class="sxs-lookup"><span data-stu-id="062d6-208">Stream data on receiver side is received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-209"><strong>Saída</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-209"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-210">bit</span><span class="sxs-lookup"><span data-stu-id="062d6-210">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-211">Dados de fluxo no lado do remetente são recebidos.</span><span class="sxs-lookup"><span data-stu-id="062d6-211">Stream data on sender side is received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-212"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-212"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-213">bit</span><span class="sxs-lookup"><span data-stu-id="062d6-213">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="062d6-214">1 significa que a direção do fluxo é do chamador para o chamado.</span><span class="sxs-lookup"><span data-stu-id="062d6-214">1 means the stream direction is from the caller to callee.</span></span></p>
<p><span data-ttu-id="062d6-215">0 significa que a direção do fluxo é do receptor para o chamador.</span><span class="sxs-lookup"><span data-stu-id="062d6-215">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-216"><strong>LossCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-216"><strong>LossCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-217">float</span><span class="sxs-lookup"><span data-stu-id="062d6-217">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-218">Indica a porcentagem do tempo em que a chamada estava em um estado de congestionamento de perda.</span><span class="sxs-lookup"><span data-stu-id="062d6-218">Indicates the percentage of the time when the call was in a loss congestion state.</span></span></p>
<p><span data-ttu-id="062d6-219">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-219">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-220"><strong>DelayCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-220"><strong>DelayCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-221">float</span><span class="sxs-lookup"><span data-stu-id="062d6-221">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-222">Indica a porcentagem da chamada durante a qual o congestionamento foi causado pela chegada atrasada dos pacotes de rede.</span><span class="sxs-lookup"><span data-stu-id="062d6-222">Indicates the percentage of the call during which congestion was caused by the delayed arrival of network packets.</span></span></p>
<p><span data-ttu-id="062d6-223">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-223">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-224"><strong>ContentionDetectedPercent</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-224"><strong>ContentionDetectedPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-225">float</span><span class="sxs-lookup"><span data-stu-id="062d6-225">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-226">Indica a porcentagem do tempo quando a chamada estava competindo pelos recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="062d6-226">Indicates the percentage of the time when the call was competing for network resources.</span></span></p>
<p><span data-ttu-id="062d6-227">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-227">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-228"><strong>BandwidthEstMin</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-228"><strong>BandwidthEstMin</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-229">int</span><span class="sxs-lookup"><span data-stu-id="062d6-229">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-230">Valor mínimo de estimativa de largura de banda medida durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="062d6-230">Minimum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="062d6-231">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-231">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-232"><strong>BandwidthEstMax</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-232"><strong>BandwidthEstMax</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-233">int</span><span class="sxs-lookup"><span data-stu-id="062d6-233">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-234">Valor máximo de estimativa de largura de banda medida durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="062d6-234">Maximum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="062d6-235">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-235">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-236"><strong>BandwidthEstStdDev</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-236"><strong>BandwidthEstStdDev</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-237">int</span><span class="sxs-lookup"><span data-stu-id="062d6-237">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-238">O desvio padrão da estimativa de largura de banda medida durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="062d6-238">Standard deviation of the bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="062d6-239">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-239">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-240"><strong>BandwidthEstAvge</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-240"><strong>BandwidthEstAvge</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-241">int</span><span class="sxs-lookup"><span data-stu-id="062d6-241">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-242">Valor médio da estimativa de largura de banda medida durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="062d6-242">Average amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="062d6-243">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-243">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-244"><strong>LowBandwidthForMultiview</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-244"><strong>LowBandwidthForMultiview</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-245">float</span><span class="sxs-lookup"><span data-stu-id="062d6-245">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-246">Porcentagem da chamada na qual o ponto de extremidade determinou que a conexão de rede não pôde dar suporte a vídeo MultiView.</span><span class="sxs-lookup"><span data-stu-id="062d6-246">Percentage of the call where the endpoint determined that the network connection could not support multiview video.</span></span></p>
<p><span data-ttu-id="062d6-247">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-247">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-248"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-248"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-249">float</span><span class="sxs-lookup"><span data-stu-id="062d6-249">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-250">Valor total de latência unidirecional.</span><span class="sxs-lookup"><span data-stu-id="062d6-250">Total amount of one-way latency.</span></span> <span data-ttu-id="062d6-251">A latência unidirecional relativa mede o atraso entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="062d6-251">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="062d6-252">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-252">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-253"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-253"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-254">float</span><span class="sxs-lookup"><span data-stu-id="062d6-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-255">Valor médio de uma latência unidirecional.</span><span class="sxs-lookup"><span data-stu-id="062d6-255">Average amount of one-way latency.</span></span> <span data-ttu-id="062d6-256">A latência unidirecional relativa mede o atraso entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="062d6-256">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="062d6-257">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-257">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-258"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-258"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-259">float</span><span class="sxs-lookup"><span data-stu-id="062d6-259">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-260">Valor máximo de latência unidirecional.</span><span class="sxs-lookup"><span data-stu-id="062d6-260">Maximum amount of one-way latency.</span></span> <span data-ttu-id="062d6-261">A latência unidirecional relativa mede o atraso entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="062d6-261">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="062d6-262">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-262">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-263"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-263"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-264">int</span><span class="sxs-lookup"><span data-stu-id="062d6-264">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-265">Total de ocorrências intermitentes unidirecionais.</span><span class="sxs-lookup"><span data-stu-id="062d6-265">Total one-way burst occurrences.</span></span> <span data-ttu-id="062d6-266">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante.</span><span class="sxs-lookup"><span data-stu-id="062d6-266">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="062d6-267">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="062d6-267">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="062d6-268">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-268">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-269"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-269"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-270">int</span><span class="sxs-lookup"><span data-stu-id="062d6-270">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-271">Densidade total de intermitência unidirecional.</span><span class="sxs-lookup"><span data-stu-id="062d6-271">Total one-way burst density.</span></span> <span data-ttu-id="062d6-272">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante.</span><span class="sxs-lookup"><span data-stu-id="062d6-272">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="062d6-273">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="062d6-273">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="062d6-274">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-274">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-275"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-275"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-276">float</span><span class="sxs-lookup"><span data-stu-id="062d6-276">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-277">Duração total de intermitência unidirecional.</span><span class="sxs-lookup"><span data-stu-id="062d6-277">Total one-way burst duration.</span></span> <span data-ttu-id="062d6-278">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante.</span><span class="sxs-lookup"><span data-stu-id="062d6-278">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="062d6-279">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="062d6-279">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="062d6-280">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-280">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-281"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-281"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-282">int</span><span class="sxs-lookup"><span data-stu-id="062d6-282">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-283">Total de ocorrências de espaçamento unidirecionais.</span><span class="sxs-lookup"><span data-stu-id="062d6-283">Total one-way gap occurrences.</span></span> <span data-ttu-id="062d6-284">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante; as lacunas indicam atrasos entre essas intermitências.</span><span class="sxs-lookup"><span data-stu-id="062d6-284">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="062d6-285">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="062d6-285">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="062d6-286">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-286">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-287"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-287"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-288">float</span><span class="sxs-lookup"><span data-stu-id="062d6-288">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-289">Densidade total do espaço unidirecional.</span><span class="sxs-lookup"><span data-stu-id="062d6-289">Total one-way gap density.</span></span> <span data-ttu-id="062d6-290">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante; as lacunas indicam atrasos entre essas intermitências.</span><span class="sxs-lookup"><span data-stu-id="062d6-290">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="062d6-291">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="062d6-291">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="062d6-292">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-292">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-293"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-293"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-294">float</span><span class="sxs-lookup"><span data-stu-id="062d6-294">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-295">Duração total unidirecional do espaço.</span><span class="sxs-lookup"><span data-stu-id="062d6-295">Total one-way gap duration.</span></span> <span data-ttu-id="062d6-296">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante; as lacunas indicam atrasos entre essas intermitências.</span><span class="sxs-lookup"><span data-stu-id="062d6-296">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="062d6-297">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="062d6-297">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="062d6-298">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-298">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-299"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-299"><strong>VideoPacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-300">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="062d6-300">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-301">Taxa de perda de pacotes de vídeo.</span><span class="sxs-lookup"><span data-stu-id="062d6-301">Rate at which video packets were lost.</span></span></p>
<p><span data-ttu-id="062d6-302">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-302">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-303"><strong>VideoAllocateBWAvg</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-303"><strong>VideoAllocateBWAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-304">int</span><span class="sxs-lookup"><span data-stu-id="062d6-304">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-305">Quantidade média de largura de banda alocada para vídeo.</span><span class="sxs-lookup"><span data-stu-id="062d6-305">Average amount of bandwidth allocated for video.</span></span></p>
<p><span data-ttu-id="062d6-306">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-306">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-307"><strong>SendCodecTypes</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-307"><strong>SendCodecTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-308">smallint</span><span class="sxs-lookup"><span data-stu-id="062d6-308">smallint</span></span></p></td>
<td><p><span data-ttu-id="062d6-309">Exterior</span><span class="sxs-lookup"><span data-stu-id="062d6-309">Foreign</span></span></p></td>
<td><p><span data-ttu-id="062d6-310">Tipo de codecs de vídeo usados pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="062d6-310">Type of video codecs used by the sender.</span></span> <span data-ttu-id="062d6-311">Consulte a <a href="lync-server-2013-codecdescription-table.md">tabela CodecDescription no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="062d6-311">See the <a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="062d6-312">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-312">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-313"><strong>SendResolutionWidth</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-313"><strong>SendResolutionWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-314">int</span><span class="sxs-lookup"><span data-stu-id="062d6-314">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-315">Largura da resolução usada pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="062d6-315">Resolution width used by the sender.</span></span></p>
<p><span data-ttu-id="062d6-316">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-316">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-317"><strong>SendResolutionHeight</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-317"><strong>SendResolutionHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-318">int</span><span class="sxs-lookup"><span data-stu-id="062d6-318">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-319">Altura da resolução usada pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="062d6-319">Resolution height used by the sender.</span></span></p>
<p><span data-ttu-id="062d6-320">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-320">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-321"><strong>SendFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-321"><strong>SendFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-322">float</span><span class="sxs-lookup"><span data-stu-id="062d6-322">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-323">Transmissão média de taxa de quadros de vídeo usada pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="062d6-323">Average video frame rate transmission used by the sender.</span></span></p>
<p><span data-ttu-id="062d6-324">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-324">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-325"><strong>SendBitRateMaximum</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-325"><strong>SendBitRateMaximum</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-326">int</span><span class="sxs-lookup"><span data-stu-id="062d6-326">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-327">Taxa máxima de bits do remetente.</span><span class="sxs-lookup"><span data-stu-id="062d6-327">Maximum bit rate for the sender.</span></span></p>
<p><span data-ttu-id="062d6-328">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-328">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-329"><strong>SendBitRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-329"><strong>SendBitRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-330">int</span><span class="sxs-lookup"><span data-stu-id="062d6-330">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-331">Taxa média de bits para o remetente.</span><span class="sxs-lookup"><span data-stu-id="062d6-331">Average bit rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-332"><strong>SendVideoStreamsMax</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-332"><strong>SendVideoStreamsMax</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-333">int</span><span class="sxs-lookup"><span data-stu-id="062d6-333">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-334">Número máximo de fluxos de vídeo usados pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="062d6-334">Maximum number of video streams used by the sender.</span></span></p>
<p><span data-ttu-id="062d6-335">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-335">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-336"><strong>RecvCodecTypes</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-336"><strong>RecvCodecTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-337">smallint</span><span class="sxs-lookup"><span data-stu-id="062d6-337">smallint</span></span></p></td>
<td><p><span data-ttu-id="062d6-338">Exterior</span><span class="sxs-lookup"><span data-stu-id="062d6-338">Foreign</span></span></p></td>
<td><p><span data-ttu-id="062d6-339">Códigos de vídeo usados pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="062d6-339">Video codes used by the receiver.</span></span> <span data-ttu-id="062d6-340">Consulte a <a href="lync-server-2013-codecdescription-table.md">tabela CodecDescription no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="062d6-340">See the <a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="062d6-341">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-341">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-342"><strong>RecvResolutionWidth</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-342"><strong>RecvResolutionWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-343">int</span><span class="sxs-lookup"><span data-stu-id="062d6-343">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-344">Largura da resolução usada pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="062d6-344">Resolution width used by the receiver.</span></span></p>
<p><span data-ttu-id="062d6-345">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-345">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-346"><strong>RecvResolutionHeight</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-346"><strong>RecvResolutionHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-347">int</span><span class="sxs-lookup"><span data-stu-id="062d6-347">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-348">Altura da resolução usada pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="062d6-348">Resolution height used by the receiver.</span></span></p>
<p><span data-ttu-id="062d6-349">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-349">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-350"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-350"><strong>RecvFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-351">float</span><span class="sxs-lookup"><span data-stu-id="062d6-351">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-352">Taxa média de quadros de vídeo usada pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="062d6-352">Average video frame rate used by the receiver.</span></span></p>
<p><span data-ttu-id="062d6-353">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-353">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-354"><strong>RecvBitRateMaximum</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-354"><strong>RecvBitRateMaximum</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-355">int</span><span class="sxs-lookup"><span data-stu-id="062d6-355">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-356">Taxa máxima de bits do destinatário.</span><span class="sxs-lookup"><span data-stu-id="062d6-356">Maximum bit rate for the receiver.</span></span></p>
<p><span data-ttu-id="062d6-357">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-357">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-358"><strong>RecvBitRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-358"><strong>RecvBitRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-359">int</span><span class="sxs-lookup"><span data-stu-id="062d6-359">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-360">Taxa média de bits para o destinatário.</span><span class="sxs-lookup"><span data-stu-id="062d6-360">Average bit rate for the receiver.</span></span></p>
<p><span data-ttu-id="062d6-361">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-361">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-362"><strong>RecvVideoStreamsMax</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-362"><strong>RecvVideoStreamsMax</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-363">int</span><span class="sxs-lookup"><span data-stu-id="062d6-363">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-364">Máximo de fluxos de vídeo para o receptor.</span><span class="sxs-lookup"><span data-stu-id="062d6-364">Maximum video streams for the receiver.</span></span></p>
<p><span data-ttu-id="062d6-365">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-365">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-366"><strong>RecvVideoStreamsMin</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-366"><strong>RecvVideoStreamsMin</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-367">int</span><span class="sxs-lookup"><span data-stu-id="062d6-367">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-368">Fluxos de vídeo mínimos para o receptor.</span><span class="sxs-lookup"><span data-stu-id="062d6-368">Minimum video streams for the receiver.</span></span></p>
<p><span data-ttu-id="062d6-369">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-369">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-370"><strong>RecvVideoStreamsMode</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-370"><strong>RecvVideoStreamsMode</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-371">int</span><span class="sxs-lookup"><span data-stu-id="062d6-371">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-372">Modo de vídeo (por exemplo, galeria ou único fluxo) para o destinatário.</span><span class="sxs-lookup"><span data-stu-id="062d6-372">Video mode (for example, gallery or single stream) for the receiver.</span></span></p>
<p><span data-ttu-id="062d6-373">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-373">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-374"><strong>À FEC PLR</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-374"><strong>VideoPostFECPLR</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-375">float</span><span class="sxs-lookup"><span data-stu-id="062d6-375">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-376">Taxa de perda de pacote após a aplicação da correção de erro de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="062d6-376">Packet loss rate after forward error correction has been applied.</span></span></p>
<p><span data-ttu-id="062d6-377">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-377">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-378"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-378"><strong>DynamicCapabilityPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-379">float</span><span class="sxs-lookup"><span data-stu-id="062d6-379">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-380">Porcentagem de tempo que o sinalizador de recurso dinâmico estava ativo.</span><span class="sxs-lookup"><span data-stu-id="062d6-380">Percentage of time that the dynamic capability flag was active.</span></span></p>
<p><span data-ttu-id="062d6-381">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-381">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-382"><strong>ResolutionMin</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-382"><strong>ResolutionMin</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-383">caractere (9)</span><span class="sxs-lookup"><span data-stu-id="062d6-383">char(9)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-384">Resolução mínima medida durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="062d6-384">Minimum resolution measured during the call.</span></span></p>
<p><span data-ttu-id="062d6-385">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-385">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-386"><strong>LowBitRateCallPercent</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-386"><strong>LowBitRateCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-387">float</span><span class="sxs-lookup"><span data-stu-id="062d6-387">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-388">Porcentagem da chamada abaixo do limite de baixa taxa de bits (70 quilobits por segundo).</span><span class="sxs-lookup"><span data-stu-id="062d6-388">Percentage of the call below the low bit rate threshold (70 kilobits per second).</span></span></p>
<p><span data-ttu-id="062d6-389">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-389">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-390"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-390"><strong>LowFrameRateCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-391">float</span><span class="sxs-lookup"><span data-stu-id="062d6-391">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-392">Porcentagem da chamada abaixo do limite de baixa taxa de quadros (7,5 quadros por segundo, entrada).</span><span class="sxs-lookup"><span data-stu-id="062d6-392">Percentage of the call below the low frame rate threshold (7.5 frames per second, inbound).</span></span></p>
<p><span data-ttu-id="062d6-393">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-393">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-394"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-394"><strong>LowResolutionCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-395">float</span><span class="sxs-lookup"><span data-stu-id="062d6-395">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-396">Porcentagem da chamada ocorrida na resolução mais baixa.</span><span class="sxs-lookup"><span data-stu-id="062d6-396">Percentage of the call that occurred at the lowest resolution.</span></span></p>
<p><span data-ttu-id="062d6-397">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-397">This column was introduced in Microsoft Lync Server 2013.</span></span></p>
<p><span data-ttu-id="062d6-398">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-398">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062d6-399"><strong>DurationSeconds</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-399"><strong>DurationSeconds</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-400">float</span><span class="sxs-lookup"><span data-stu-id="062d6-400">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-401">Duração da chamada em segundos.</span><span class="sxs-lookup"><span data-stu-id="062d6-401">Length of the call in seconds.</span></span></p>
<p><span data-ttu-id="062d6-402">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-402">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062d6-403"><strong>IsAggregatedData</strong></span><span class="sxs-lookup"><span data-stu-id="062d6-403"><strong>IsAggregatedData</strong></span></span></p></td>
<td><p><span data-ttu-id="062d6-404">bit</span><span class="sxs-lookup"><span data-stu-id="062d6-404">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="062d6-405">Indica se os dados foram agregados de várias chamadas.</span><span class="sxs-lookup"><span data-stu-id="062d6-405">Indicates whether the data has been aggregated from multiple calls.</span></span></p>
<p><span data-ttu-id="062d6-406">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="062d6-406">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="062d6-407">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="062d6-407">


</div>

<span> </span>

</div>

</div>

</span></span></div>

