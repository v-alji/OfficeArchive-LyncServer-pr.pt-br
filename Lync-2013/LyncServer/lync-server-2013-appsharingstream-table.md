---
title: 'Lync Server 2013: tabela AppSharingStream'
description: 'Lync Server 2013: AppSharingStream Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingStream table
ms:assetid: 391490cb-d7b8-44ca-b4d1-429600da909c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204808(v=OCS.15)
ms:contentKeyID: 48183852
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b530af5b489e090e5d0d00fbb01b2b950bafbe5a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440553"
---
# <a name="appsharingstream-table-in-lync-server-2013"></a><span data-ttu-id="ae04c-103">Tabela AppSharingStream no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae04c-103">AppSharingStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae04c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae04c-104">

<span> </span></span></span>

<span data-ttu-id="ae04c-105">_**Tópico da última modificação:** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="ae04c-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="ae04c-106">A tabela AppSharingStream contém métricas de qualidade de experiência para os fluxos de rede usados para compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ae04c-106">The AppSharingStream table contains Quality of Experience metrics for the network streams used for application sharing.</span></span> <span data-ttu-id="ae04c-107">Esta tabela foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ae04c-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae04c-108"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="ae04c-109"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="ae04c-110"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="ae04c-111"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-113">dateTime</span><span class="sxs-lookup"><span data-stu-id="ae04c-113">dateTime</span></span></p></td>
<td><p><span data-ttu-id="ae04c-114">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="ae04c-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="ae04c-115">Data e hora em que a sessão foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="ae04c-115">Date and time that the session started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-117">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-117">int</span></span></p></td>
<td><p><span data-ttu-id="ae04c-118">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="ae04c-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="ae04c-119">Identificador sequencial usado para distinguir entre as sessões iniciadas na mesma data e ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="ae04c-119">Sequential identifier used to distinguish between sessions that started on the same date and at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="ae04c-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ae04c-122">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="ae04c-122">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="ae04c-123">Representa o tipo de linha de vídeo usado na chamada.</span><span class="sxs-lookup"><span data-stu-id="ae04c-123">Represents the type of video line used in the call.</span></span> <span data-ttu-id="ae04c-124">Os valores permitidos são:</span><span class="sxs-lookup"><span data-stu-id="ae04c-124">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="ae04c-125">0 – áudio</span><span class="sxs-lookup"><span data-stu-id="ae04c-125">0 – Audio</span></span></p></li>
<li><p><span data-ttu-id="ae04c-126">1 – vídeo</span><span class="sxs-lookup"><span data-stu-id="ae04c-126">1 – Video</span></span></p></li>
<li><p><span data-ttu-id="ae04c-127">2 – vídeo panorâmico</span><span class="sxs-lookup"><span data-stu-id="ae04c-127">2 – Panoramic video</span></span></p></li>
<li><p><span data-ttu-id="ae04c-128">3 – compartilhamento de aplicativos/área de trabalho</span><span class="sxs-lookup"><span data-stu-id="ae04c-128">3 –Application/Desktop Sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-129"><strong>Streamid</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-129"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-130">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-130">int</span></span></p></td>
<td><p><span data-ttu-id="ae04c-131">Primária</span><span class="sxs-lookup"><span data-stu-id="ae04c-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="ae04c-132">Identificador exclusivo do fluxo de compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ae04c-132">Unique identifier of the application sharing stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-133"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-133"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-134">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-134">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-135">Tremulação média detectada entre chegadas de pacote RTP.</span><span class="sxs-lookup"><span data-stu-id="ae04c-135">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="ae04c-136">(Tremulação é uma medida do &quot; shakiness &quot; de uma chamada.) Os valores de variação alta geralmente são causados por congestionamento ou um servidor de mídia sobrecarregado, resultando em áudio distorcido ou perdido.</span><span class="sxs-lookup"><span data-stu-id="ae04c-136">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-137"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-137"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-138">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-139">Variação máxima detectada entre as entradas do pacote RTP.</span><span class="sxs-lookup"><span data-stu-id="ae04c-139">Maximum jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="ae04c-140">(Tremulação é uma medida do &quot; shakiness &quot; de uma chamada.) Os valores de variação alta geralmente são causados por congestionamento ou um servidor de mídia sobrecarregado, resultando em áudio distorcido ou perdido.</span><span class="sxs-lookup"><span data-stu-id="ae04c-140">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-141"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-141"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-142">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-142">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-p105">Quantidade média (em milissegundos) exigida para que um pacote de protocolo RTP viaje até outro ponto de extremidade e retorne. Tempos de viagem de ida e volta de 200 milissegundos ou menos são considerados de qualidade aceitável.</span><span class="sxs-lookup"><span data-stu-id="ae04c-p105">Average amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back. Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="ae04c-p106">Os valores altos de tempo de resposta podem ser causados por roteamento de chamadas internacionais, configuração incorreta de um roteamento ou um servidor de mídia sobrecarregado. Tempos de resposta altos resultam em dificuldades para conversas de áudio bidirecionais e em tempo real.</span><span class="sxs-lookup"><span data-stu-id="ae04c-p106">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-147"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-147"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-148">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-148">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-149">A quantidade máxima de (em milissegundos) necessária para que um pacote de protocolo de transporte Real-Time vá para outro ponto de extremidade e, em seguida, retorne.</span><span class="sxs-lookup"><span data-stu-id="ae04c-149">Maximum amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back.</span></span> <span data-ttu-id="ae04c-150">Tempos de ida e volta de 200 milissegundos ou menos são considerados de qualidade aceitável.</span><span class="sxs-lookup"><span data-stu-id="ae04c-150">Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="ae04c-p108">Altos valores de tempo de resposta podem ser causados por roteamento de chamadas internacionais, configuração incorreta de um roteamento ou um servidor de mídia sobrecarregado. Tempos de resposta altos resultam em dificuldades para conversas de áudio bidirecionais e em tempo real.</span><span class="sxs-lookup"><span data-stu-id="ae04c-p108">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-153"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-153"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-154">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-154">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-p109">Taxa média de perda de pacotes de RTP (protocolo de transporte em tempo real). (A perda de pacotes ocorre quando pacotes de RTP, um protocolo usado para transmitir áudio e vídeo pela Internet, falha ao tentar alcançar seu destino). Altas taxas de perda geralmente são causadas por congestionamento, insuficiência da largura de banda, congestionamento ou interferência na rede sem fio ou um servidor de mídia sobrecarregado. A perda de pacotes normalmente resulta em distorção ou perda de áudio.</span><span class="sxs-lookup"><span data-stu-id="ae04c-p109">Average rate of Real-Time Transport Protocol (RTP) packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-158"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-158"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-159">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-159">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-160">Taxa máxima de perda de pacotes RTP (protocolo de transporte de Real-Time).</span><span class="sxs-lookup"><span data-stu-id="ae04c-160">Maximum rate of Real-Time Transport Protocol (RTP) packet loss.</span></span> <span data-ttu-id="ae04c-161">(A perda de pacote ocorre quando pacotes RTP, um protocolo usado para a transmissão de áudio e vídeo pela Internet, não atinge seu destino.) Tarifas de alta perda são geralmente causadas por congestionamento; falta de largura de banda; congestionamento ou interferência sem fio; ou um servidor de mídia sobrecarregado.</span><span class="sxs-lookup"><span data-stu-id="ae04c-161">(Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server.</span></span> <span data-ttu-id="ae04c-162">A perda de pacote normalmente resulta em perda ou distorção de áudio.</span><span class="sxs-lookup"><span data-stu-id="ae04c-162">Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-163"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-163"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-164">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-164">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-165">Número de pacotes enviados.</span><span class="sxs-lookup"><span data-stu-id="ae04c-165">Number of packets sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-166"><strong>Largura de banda</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-166"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-167">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-167">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-168">Largura de banda unidirecional estimada disponível no final da sessão.</span><span class="sxs-lookup"><span data-stu-id="ae04c-168">Estimated one-way bandwidth available at the end of the session.</span></span> <span data-ttu-id="ae04c-169">Relatado em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ae04c-169">Reported in bits per second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-170"><strong>AppSharingPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-170"><strong>AppSharingPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-171">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-171">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-172">Descrição da carga de compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ae04c-172">Description of the application sharing payload.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-173"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-173"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-174">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-174">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-175">Valor total de latência unidirecional.</span><span class="sxs-lookup"><span data-stu-id="ae04c-175">Total amount of one-way latency.</span></span> <span data-ttu-id="ae04c-176">A latência unidirecional relativa mede o atraso entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="ae04c-176">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-177"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-177"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-178">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-178">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-179">Valor médio de uma latência unidirecional.</span><span class="sxs-lookup"><span data-stu-id="ae04c-179">Average amount of one-way latency.</span></span> <span data-ttu-id="ae04c-180">A latência unidirecional relativa mede o atraso entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="ae04c-180">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-181"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-181"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-182">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-182">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-183">Valor máximo de latência unidirecional.</span><span class="sxs-lookup"><span data-stu-id="ae04c-183">Maximum amount of one-way latency.</span></span> <span data-ttu-id="ae04c-184">A latência unidirecional relativa mede o atraso entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="ae04c-184">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-185"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-185"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-186">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-186">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-187">Total de ocorrências intermitentes unidirecionais.</span><span class="sxs-lookup"><span data-stu-id="ae04c-187">Total one-way burst occurrences.</span></span> <span data-ttu-id="ae04c-188">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante.</span><span class="sxs-lookup"><span data-stu-id="ae04c-188">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="ae04c-189">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="ae04c-189">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-190"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-190"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-191">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-191">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-192">Densidade total de intermitência unidirecional.</span><span class="sxs-lookup"><span data-stu-id="ae04c-192">Total one-way burst density.</span></span> <span data-ttu-id="ae04c-193">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante.</span><span class="sxs-lookup"><span data-stu-id="ae04c-193">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="ae04c-194">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="ae04c-194">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-195"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-195"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-196">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-196">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-197">Duração total de intermitência unidirecional.</span><span class="sxs-lookup"><span data-stu-id="ae04c-197">Total one-way burst duration.</span></span> <span data-ttu-id="ae04c-198">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante.</span><span class="sxs-lookup"><span data-stu-id="ae04c-198">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="ae04c-199">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="ae04c-199">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-200"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-200"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-201">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-201">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-202">Total de ocorrências de espaçamento unidirecionais.</span><span class="sxs-lookup"><span data-stu-id="ae04c-202">Total one-way gap occurrences.</span></span> <span data-ttu-id="ae04c-203">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante; as lacunas indicam atrasos entre essas intermitências.</span><span class="sxs-lookup"><span data-stu-id="ae04c-203">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="ae04c-204">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="ae04c-204">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-205"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-205"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-206">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-206">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-207">Densidade total do espaço unidirecional.</span><span class="sxs-lookup"><span data-stu-id="ae04c-207">Total one-way gap density.</span></span> <span data-ttu-id="ae04c-208">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante; as lacunas indicam atrasos entre essas intermitências.</span><span class="sxs-lookup"><span data-stu-id="ae04c-208">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="ae04c-209">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="ae04c-209">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-210"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-210"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-211">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-211">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-212">Duração total unidirecional do espaço.</span><span class="sxs-lookup"><span data-stu-id="ae04c-212">Total one-way gap duration.</span></span> <span data-ttu-id="ae04c-213">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante; as lacunas indicam atrasos entre essas intermitências.</span><span class="sxs-lookup"><span data-stu-id="ae04c-213">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="ae04c-214">Essa métrica mede o fluxo de dados entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="ae04c-214">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-215"><strong>ApplicationSharingType</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-215"><strong>ApplicationSharingType</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-216">varChar (256)</span><span class="sxs-lookup"><span data-stu-id="ae04c-216">varChar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-217">Função do aplicativo (compartilhamento ou visualizador) e tipo de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ae04c-217">Application role (Sharer or Viewer) and content type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-218"><strong>RDPTileProcessingLatencyTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-218"><strong>RDPTileProcessingLatencyTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-219">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-219">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-220">Tempo total de processamento para blocos RDP (protocolo de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="ae04c-220">Total processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ae04c-221">Um total maior equivale a um atraso mais longo na experiência de visualização.</span><span class="sxs-lookup"><span data-stu-id="ae04c-221">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-222"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-222"><strong>RDPTileProcessingLatencyAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-223">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-223">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-224">Tempo médio de processamento de blocos RDP (protocolo de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="ae04c-224">Average processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ae04c-225">Um total maior equivale a um atraso mais longo na experiência de visualização.</span><span class="sxs-lookup"><span data-stu-id="ae04c-225">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-226"><strong>RDPTileProcessingLatencyMax</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-226"><strong>RDPTileProcessingLatencyMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-227">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-227">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-228">Tempo máximo de processamento de blocos RDP (protocolo de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="ae04c-228">Maximum processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ae04c-229">Um total maior equivale a um atraso mais longo na experiência de visualização.</span><span class="sxs-lookup"><span data-stu-id="ae04c-229">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-230"><strong>RDPTileProcessingLatencyBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-230"><strong>RDPTileProcessingLatencyBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-231">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-231">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-232">Ocorrências intermitentes no tempo de processamento dos blocos RDP (protocolo de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="ae04c-232">Burst occurrences in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ae04c-233">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante.</span><span class="sxs-lookup"><span data-stu-id="ae04c-233">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-234"><strong>RDPTileProcessingLatencyBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-234"><strong>RDPTileProcessingLatencyBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-235">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-235">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-236">Densidade de intermitência no tempo de processamento dos blocos RDP (protocolo de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="ae04c-236">Burst density in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ae04c-237">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante.</span><span class="sxs-lookup"><span data-stu-id="ae04c-237">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-238"><strong>RDPTileProcessingLatencyBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-238"><strong>RDPTileProcessingLatencyBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-239">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-239">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-240">Duração da intermitência no tempo de processamento dos blocos RDP (protocolo de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="ae04c-240">Burst duration in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ae04c-241">Uma transmissão "intermitente" é uma transmissão na qual os dados fluem em picos imprevisíveis em oposição a um fluxo constante.</span><span class="sxs-lookup"><span data-stu-id="ae04c-241">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-242"><strong>RDPTileProcessingLatencyGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-242"><strong>RDPTileProcessingLatencyGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-243">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-243">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-244">Ocorrências de lacunas no tempo de processamento dos blocos RDP (protocolo de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="ae04c-244">Gap occurrences in the processing time for remote desktop protocol (RDP) tiles.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-245"><strong>RDPTileProcessingLatencyGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-245"><strong>RDPTileProcessingLatencyGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-246">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-246">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-247">Densidade de espaço no bloco tempo de processamento de blocos RDP (protocolo de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="ae04c-247">Gap density in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ae04c-248">A densidade de lacunas baixas equivale a uma melhor experiência de exibição.</span><span class="sxs-lookup"><span data-stu-id="ae04c-248">Low gap density equates to a better viewing experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-249"><strong>RDPTileProcessingLatencyGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-249"><strong>RDPTileProcessingLatencyGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-250">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-250">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-251">Duração do espaço no bloco de tempo de processamento para blocos RDP (protocolo de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="ae04c-251">Gap duration in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="ae04c-252">Durações de espaço curto equivalem a uma melhor experiência de exibição.</span><span class="sxs-lookup"><span data-stu-id="ae04c-252">Short gap durations equate to a better viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-253"><strong>CaptureTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-253"><strong>CaptureTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-254">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-255">Taxa total de blocos capturados (em blocos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ae04c-255">Total rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-256"><strong>CaptureTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-256"><strong>CaptureTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-257">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-257">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-258">Taxa média de blocos capturados (em blocos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ae04c-258">Average rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-259"><strong>CaptureTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-259"><strong>CaptureTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-260">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-260">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-261">Taxa máxima de blocos capturados (em blocos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ae04c-261">Maximum rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-262"><strong>CaptureTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-262"><strong>CaptureTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-263">em t</span><span class="sxs-lookup"><span data-stu-id="ae04c-263">in t</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-264">Ocorrências intermitentes na taxa de blocos capturados (em blocos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ae04c-264">Burst occurrences in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-265"><strong>CaptureTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-265"><strong>CaptureTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-266">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-266">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-267">Densidade de intermitência na taxa de blocos capturados (em blocos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ae04c-267">Burst density in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-268"><strong>CaptureTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-268"><strong>CaptureTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-269">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-269">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-270">Duração da intermitência na taxa de blocos capturados (em blocos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ae04c-270">Burst duration in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-271"><strong>CaptureTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-271"><strong>CaptureTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-272">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-272">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-273">Ocorrências de lacunas na taxa de blocos capturados (em blocos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ae04c-273">Gap occurrences in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-274"><strong>CaptureTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-274"><strong>CaptureTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-275">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-275">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-276">Densidade da lacuna na taxa de blocos capturados (em blocos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ae04c-276">Gap density in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-277"><strong>CaptureTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-277"><strong>CaptureTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-278">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-278">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-279">Duração do espaçamento na taxa de blocos capturados (em blocos por segundo).</span><span class="sxs-lookup"><span data-stu-id="ae04c-279">Gap duration in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-280"><strong>À</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-280"><strong>SpoiledTilePercentTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-281">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-281">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-282">A porcentagem total do conteúdo que não chegou ao visualizador, em vez disso, foi descartado e sobrescrito pelo novo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ae04c-282">Total percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-283"><strong>SpoiledTilePercentAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-283"><strong>SpoiledTilePercentAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-284">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-284">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-285">A porcentagem média do conteúdo que não tinha chegado ao visualizador, em vez disso, foi descartado e sobrescrito pelo novo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ae04c-285">Average percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-286"><strong>SpoiledTilePercentMax</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-286"><strong>SpoiledTilePercentMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-287">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-287">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-288">A porcentagem máxima do conteúdo que não tinha chegado ao visualizador, em vez disso, foi descartada e sobrescrita pelo conteúdo novo.</span><span class="sxs-lookup"><span data-stu-id="ae04c-288">Maximum percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-289"><strong>SpoiledTilePercentBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-289"><strong>SpoiledTilePercentBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-290">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-290">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-291">As ocorrências de intermitência do conteúdo que não chegavam ao visualizador foram descartadas e sobrescritas pelo conteúdo novo.</span><span class="sxs-lookup"><span data-stu-id="ae04c-291">Burst occurrences for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-292"><strong>SpoiledTilePercentBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-292"><strong>SpoiledTilePercentBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-293">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-293">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-294">Densidade de intermitência para o conteúdo que não tinha chegado ao visualizador, em vez disso, foi descartado e sobrescrito pelo novo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ae04c-294">Burst density for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-295"><strong>SpoiledTilePercentBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-295"><strong>SpoiledTilePercentBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-296">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-296">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-297">A duração da intermitência para o conteúdo que não tinha chegado ao visualizador, em vez disso, foi descartado e sobrescrito pelo novo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ae04c-297">Burst duration for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-298"><strong>SpoiledTilePercentGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-298"><strong>SpoiledTilePercentGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-299">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-299">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-300">As ocorrências de lacunas do conteúdo que não chegavam ao visualizador foram descartadas e sobrescritas pelo conteúdo novo.</span><span class="sxs-lookup"><span data-stu-id="ae04c-300">Gap occurrences for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-301"><strong>SpoiledTilePercentGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-301"><strong>SpoiledTilePercentGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-302">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-302">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-303">Densidade de espaço para o conteúdo que não tinha chegado ao visualizador, em vez disso, foi descartado e sobrescrito pelo novo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ae04c-303">Gap density for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-304"><strong>SpoiledTilePercentGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-304"><strong>SpoiledTilePercentGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-305">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-305">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-306">Duração do espaço para o conteúdo que não tinha chegado ao visualizador, em vez disso, foi descartado e sobrescrito pelo novo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ae04c-306">Gap duration for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-307"><strong>ScrapingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-307"><strong>ScrapingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-308">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-308">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-309">Número total de quadros recortedos da fonte de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="ae04c-309">Total number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-310"><strong>ScrapingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-310"><strong>ScrapingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-311">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-311">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-312">Número médio de quadros recortes da fonte de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="ae04c-312">Average number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-313"><strong>ScrapingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-313"><strong>ScrapingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-314">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-314">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-315">Número máximo de quadros recortes da fonte de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="ae04c-315">Maximum number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-316"><strong>ScrapingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-316"><strong>ScrapingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-317">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-317">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-318">Ocorrências intermitentes nos quadros recortes da fonte gráfica.</span><span class="sxs-lookup"><span data-stu-id="ae04c-318">Burst occurrences in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-319"><strong>ScrapingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-319"><strong>ScrapingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-320">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-320">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-321">Densidade de intermitência nos quadros recapturada da fonte de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="ae04c-321">Burst density in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-322"><strong>ScrapingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-322"><strong>ScrapingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-323">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-323">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-324">A duração da intermitência nos quadros é recapturada da fonte de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="ae04c-324">Burst duration in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-325"><strong>ScrapingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-325"><strong>ScrapingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-326">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-326">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-327">Ocorrências de lacunas nos quadros recortes da fonte gráfica.</span><span class="sxs-lookup"><span data-stu-id="ae04c-327">Gap occurrences in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-328"><strong>ScrapingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-328"><strong>ScrapingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-329">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-329">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-330">Densidade de lacunas nos quadros recortes da fonte gráfica.</span><span class="sxs-lookup"><span data-stu-id="ae04c-330">Gap density in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-331"><strong>ScrapingFrameRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-331"><strong>ScrapingFrameRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-332">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-332">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-333">Intervalo de tempo nos quadros recortes da fonte de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="ae04c-333">Gap duration in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-334"><strong>IncomingTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-334"><strong>IncomingTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-335">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-335">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-336">Taxa de quadro de entrada total conforme recebido pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-336">Total incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-337"><strong>IncomingTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-337"><strong>IncomingTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-338">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-338">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-339">Taxa média de quadros recebidos, conforme recebido pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-339">Average incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-340"><strong>IncomingTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-340"><strong>IncomingTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-341">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-341">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-342">Taxa máxima de bloco de entrada recebido pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-342">Maximum incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-343"><strong>IncomingTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-343"><strong>IncomingTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-344">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-344">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-345">Ocorrências de intermitência na taxa de peça de entrada recebidas pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-345">Burst occurrences in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-346"><strong>IncomingTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-346"><strong>IncomingTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-347">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-347">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-348">Densidade de intermitência na taxa de peça de entrada como recebida pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-348">Burst density in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-349"><strong>IncomingTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-349"><strong>IncomingTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-350">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-350">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-351">Duração da intermitência na taxa de peça de entrada como recebida pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-351">Burst duration in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-352"><strong>IncomingTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-352"><strong>IncomingTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-353">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-353">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-354">Ocorrências de lacunas na taxa de peça de entrada recebidas pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-354">Gap occurrences in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-355"><strong>IncomingTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-355"><strong>IncomingTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-356">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-356">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-357">Densidade de espaço na taxa de peça de entrada como recebida pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-357">Gap density in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-358"><strong>IncomingTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-358"><strong>IncomingTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-359">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-359">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-360">Duração do espaçamento na taxa de peça de entrada como recebida pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-360">Gap duration in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-361"><strong>IncomingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-361"><strong>IncomingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-362">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-362">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-363">Taxa de quadro de entrada total conforme recebido pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-363">Total incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-364"><strong>IncomingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-364"><strong>IncomingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-365">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-365">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-366">Taxa média de quadros recebidos, conforme recebido pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-366">Average incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-367"><strong>IncomingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-367"><strong>IncomingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-368">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-368">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-369">Taxa máxima de quadros de entrada, conforme recebido pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-369">Maximum incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-370"><strong>IncomingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-370"><strong>IncomingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-371">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-371">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-372">Ocorrências de intermitência na taxa de quadros de entrada conforme recebidas pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-372">Burst occurrences in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-373"><strong>IncomingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-373"><strong>IncomingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-374">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-374">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-375">Densidade de intermitência na taxa de quadros de entrada como recebida pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-375">Burst density in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-376"><strong>IncomingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-376"><strong>IncomingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-377">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-377">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-378">Duração da intermitência na taxa de quadros de entrada como recebida pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-378">Burst duration in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-379"><strong>IncomingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-379"><strong>IncomingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-380">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-380">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-381">Ocorrências de lacunas na taxa de quadros de entrada recebidas pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-381">Gap occurrences in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-382"><strong>IncomingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-382"><strong>IncomingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-383">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-383">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-384">Densidade de espaço na taxa de quadros de entrada como recebida pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-384">Gap density in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-385"><strong>IncomingFrameRateDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-385"><strong>IncomingFrameRateDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-386">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-386">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-387">Duração do espaçamento na taxa de quadro de entrada como recebida pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-387">Gap duration in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-388"><strong>OutgoingTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-388"><strong>OutgoingTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-389">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-389">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-390">Taxa total de blocos de saída para o remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-390">Total outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-391"><strong>OutgoingTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-391"><strong>OutgoingTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-392">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-392">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-393">Taxa média de peça de saída para o remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-393">Average outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-394"><strong>OutgoingTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-394"><strong>OutgoingTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-395">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-395">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-396">Taxa máxima de bloco de saída para o remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-396">Maximum outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-397"><strong>OutgoingTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-397"><strong>OutgoingTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-398">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-398">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-399">Ocorrências de intermitência na taxa de bloco de saída para o remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-399">Burst occurrences in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-400"><strong>OutgoingTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-400"><strong>OutgoingTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-401">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-401">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-402">Densidade de intermitência na taxa de peça de saída do remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-402">Burst density in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-403"><strong>OutgoingTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-403"><strong>OutgoingTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-404">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-404">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-405">Duração da intermitência na taxa de peça de saída do remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-405">Burst duration in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-406"><strong>OutgoingTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-406"><strong>OutgoingTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-407">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-407">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-408">Ocorrências de lacunas na taxa de bloco de saída para o remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-408">Gap occurrences in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-409"><strong>OutgoingTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-409"><strong>OutgoingTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-410">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-410">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-411">Densidade de espaço na taxa de bloco de saída para o remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-411">Gap density in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-412"><strong>OutgoingTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-412"><strong>OutgoingTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-413">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-413">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-414">Duração do espaçamento na taxa de peça de saída para o remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-414">Gap duration in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-415"><strong>OutgoingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-415"><strong>OutgoingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-416">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-416">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-417">Taxa de quadros de saída total para o remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-417">Total outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-418"><strong>OutgoingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-418"><strong>OutgoingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-419">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-419">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-420">taxa média de quadros de saída para o remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-420">average outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-421"><strong>OutgoingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-421"><strong>OutgoingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-422">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-422">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-423">Taxa máxima de quadros de saída para o remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-423">Maximum outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-424"><strong>OutgoingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-424"><strong>OutgoingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-425">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-425">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-426">Ocorrências intermitentes na taxa de quadros de saída do remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-426">Burst occurrences in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-427"><strong>OutgoingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-427"><strong>OutgoingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-428">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-428">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-429">Densidade de intermitência na taxa de quadros de saída do remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-429">Burst density in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-430"><strong>OutgoingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-430"><strong>OutgoingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-431">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-431">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-432">Duração da intermitência na taxa de quadros de saída do remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-432">Burst duration in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-433"><strong>OutgoingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-433"><strong>OutgoingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-434">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-434">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-435">Ocorrências de lacunas na taxa de quadros de saída do remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-435">Gap occurrences in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-436"><strong>OutgoingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-436"><strong>OutgoingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-437">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-437">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-438">Densidade da lacuna na taxa de quadros de saída do remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-438">Gap density in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-439"><strong>OutgoingFrameRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-439"><strong>OutgoingFrameRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-440">float</span><span class="sxs-lookup"><span data-stu-id="ae04c-440">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-441">Duração do espaçamento na taxa de quadros de saída do remetente.</span><span class="sxs-lookup"><span data-stu-id="ae04c-441">Gap duration in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-442"><strong>AverageRectangleHeight</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-442"><strong>AverageRectangleHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-443">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-443">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-444">Altura média da resolução de vídeo em pixels.</span><span class="sxs-lookup"><span data-stu-id="ae04c-444">Average video resolution height, in pixels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-445"><strong>AverageRectangleWidth</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-445"><strong>AverageRectangleWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-446">int</span><span class="sxs-lookup"><span data-stu-id="ae04c-446">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-447">Largura média da resolução de vídeo em pixels.</span><span class="sxs-lookup"><span data-stu-id="ae04c-447">Average video resolution width, in pixels.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-448"><strong>Entrada</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-448"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-449">bit</span><span class="sxs-lookup"><span data-stu-id="ae04c-449">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-450">Taxa média de quadros (em quadros por segundo) para transmissões de entrada.</span><span class="sxs-lookup"><span data-stu-id="ae04c-450">Average frame rate (in frames per second) for inbound transmissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae04c-451"><strong>Saída</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-451"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-452">bit</span><span class="sxs-lookup"><span data-stu-id="ae04c-452">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-453">Taxa média de quadros (em quadros por segundo) para transmissões de saída.</span><span class="sxs-lookup"><span data-stu-id="ae04c-453">Average frame rate (in frames per second) for outbound transmissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae04c-454"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="ae04c-454"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="ae04c-455">bit</span><span class="sxs-lookup"><span data-stu-id="ae04c-455">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ae04c-456">1 significa que a direção do fluxo é do chamador para o chamado.</span><span class="sxs-lookup"><span data-stu-id="ae04c-456">1 means the stream direction is from the caller to callee.</span></span></p>
<p><span data-ttu-id="ae04c-457">0 significa que a direção do fluxo é do receptor para o chamador.</span><span class="sxs-lookup"><span data-stu-id="ae04c-457">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ae04c-458">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae04c-458">


</div>

<span> </span>

</div>

</div>

</span></span></div>

