---
title: 'Lync Server 2013: Tabela AudioSignal'
description: 'Lync Server 2013: AudioSignal Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioSignal table
ms:assetid: 0013c8c6-cdf9-4d70-bc2a-cddd1560f66b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398064(v=OCS.15)
ms:contentKeyID: 48183217
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82f3b3119eaccfe56c4706cff07469bc3434461f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438201"
---
# <a name="audiosignal-table-in-lync-server-2013"></a><span data-ttu-id="b92a9-103">Tabela AudioSignal no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b92a9-103">AudioSignal table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b92a9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b92a9-104">

<span> </span></span></span>

<span data-ttu-id="b92a9-105">_**Tópico da última modificação:** 2013-11-12_</span><span class="sxs-lookup"><span data-stu-id="b92a9-105">_**Topic Last Modified:** 2013-11-12_</span></span>

<span data-ttu-id="b92a9-106">Cada registro representa as métricas do sinal de áudio para um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="b92a9-106">Each record represents audio signal metrics for one endpoint.</span></span> <span data-ttu-id="b92a9-107">Geralmente, cada chamada tem dois registros, um é para o chamador e um é para o receptor.</span><span class="sxs-lookup"><span data-stu-id="b92a9-107">Usually, each call has two records, one is for caller, and one is for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b92a9-108"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="b92a9-109"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="b92a9-110"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="b92a9-111"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-113">datetime</span><span class="sxs-lookup"><span data-stu-id="b92a9-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="b92a9-114">Primária</span><span class="sxs-lookup"><span data-stu-id="b92a9-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="b92a9-115">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="b92a9-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b92a9-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-117">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-117">int</span></span></p></td>
<td><p><span data-ttu-id="b92a9-118">Primária</span><span class="sxs-lookup"><span data-stu-id="b92a9-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="b92a9-119">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="b92a9-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="b92a9-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="b92a9-122">Primária</span><span class="sxs-lookup"><span data-stu-id="b92a9-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="b92a9-123">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="b92a9-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b92a9-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-125">bit</span><span class="sxs-lookup"><span data-stu-id="b92a9-125">bit</span></span></p></td>
<td><p><span data-ttu-id="b92a9-126">Primária</span><span class="sxs-lookup"><span data-stu-id="b92a9-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="b92a9-127">0: dados do chamador</span><span class="sxs-lookup"><span data-stu-id="b92a9-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="b92a9-128">1: dados do chamador</span><span class="sxs-lookup"><span data-stu-id="b92a9-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-129"><strong>SendSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-129"><strong>SendSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-130">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-130">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-131">Representa o nível de sinal de áudio de controle de ganho de cruz analógico.</span><span class="sxs-lookup"><span data-stu-id="b92a9-131">Represents the Post-Analog Gain Control audio signal level.</span></span> <span data-ttu-id="b92a9-132">A unidade para essa métrica é dBmo.</span><span class="sxs-lookup"><span data-stu-id="b92a9-132">The unit for this metric is dBmo.</span></span> <span data-ttu-id="b92a9-133">Para ter uma qualidade aceitável, ele deve ter pelo menos 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="b92a9-133">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="b92a9-134">Essa métrica não é reportada pelo servidor de conferência A/V ou por telefones IP.</span><span class="sxs-lookup"><span data-stu-id="b92a9-134">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b92a9-135"><strong>RecvSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-135"><strong>RecvSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-136">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-136">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-137">Consulte SendSignalLevel.</span><span class="sxs-lookup"><span data-stu-id="b92a9-137">See SendSignalLevel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-138"><strong>SendNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-138"><strong>SendNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-139">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-139">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-140">Representa o nível de ruído de áudio de controle de ganho analógicos.</span><span class="sxs-lookup"><span data-stu-id="b92a9-140">Represents the Post-Analog Gain Control audio noise level.</span></span> <span data-ttu-id="b92a9-141">A unidade para essa métrica é dBmo.</span><span class="sxs-lookup"><span data-stu-id="b92a9-141">The unit for this metric is dBmo.</span></span> <span data-ttu-id="b92a9-142">Para ter uma qualidade aceitável, deve ser menor do que 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="b92a9-142">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="b92a9-143">Essa métrica não é reportada pelo servidor de conferência A/V ou por telefones IP.</span><span class="sxs-lookup"><span data-stu-id="b92a9-143">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b92a9-144"><strong>RecvNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-144"><strong>RecvNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-145">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-145">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-146">Consulte SendNoiseLevel.</span><span class="sxs-lookup"><span data-stu-id="b92a9-146">See SendNoiseLevel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-147"><strong>EchoReturn</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-147"><strong>EchoReturn</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-148">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-148">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-149">Métrica de aprimoramento de perda de retorno de eco.</span><span class="sxs-lookup"><span data-stu-id="b92a9-149">Echo Return Loss Enhancement metric.</span></span> <span data-ttu-id="b92a9-150">A unidade para essa métrica é dB.</span><span class="sxs-lookup"><span data-stu-id="b92a9-150">The unit for this metric is dB.</span></span> <span data-ttu-id="b92a9-151">Valores inferiores representam menos eco.</span><span class="sxs-lookup"><span data-stu-id="b92a9-151">Lower values represent less echo.</span></span> <span data-ttu-id="b92a9-152">Essa métrica não é reportada pelo servidor de conferência A/V ou por telefones IP.</span><span class="sxs-lookup"><span data-stu-id="b92a9-152">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b92a9-153"><strong>AudioSpeakerGlitchRate</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-153"><strong>AudioSpeakerGlitchRate</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-154">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-154">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-155">Média de falhas por cinco minutos para a renderização de alto-falante.</span><span class="sxs-lookup"><span data-stu-id="b92a9-155">Average glitches per five minutes for the loudspeaker rendering.</span></span> <span data-ttu-id="b92a9-156">Para ter uma boa qualidade, isso deve ser inferior a um por cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="b92a9-156">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="b92a9-157">Não relatado por servidores de conferência A/V, servidores de mediação ou telefones IP.</span><span class="sxs-lookup"><span data-stu-id="b92a9-157">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-158"><strong>AudioMicGlitchRate</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-158"><strong>AudioMicGlitchRate</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-159">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-159">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-160">Média de falhas por cinco minutos para a captura de microfone.</span><span class="sxs-lookup"><span data-stu-id="b92a9-160">Average glitches per five minutes for the microphone capture.</span></span> <span data-ttu-id="b92a9-161">Para ter uma boa qualidade, isso deve ser inferior a um por cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="b92a9-161">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="b92a9-162">Não relatado por servidores de conferência A/V, servidores de mediação ou telefones IP.</span><span class="sxs-lookup"><span data-stu-id="b92a9-162">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b92a9-163"><strong>AudioTimestampDriftRateMic</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-163"><strong>AudioTimestampDriftRateMic</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-164">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="b92a9-164">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-165">Taxa de descompasso do relógio do dispositivo de microfone, relativa ao relógio da CPU.</span><span class="sxs-lookup"><span data-stu-id="b92a9-165">Microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-166"><strong>AudioTimestampDriftRateSpk</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-166"><strong>AudioTimestampDriftRateSpk</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-167">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="b92a9-167">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-168">Taxa de descompasso do relógio do dispositivo de alto-falante, relativa ao relógio da CPU.</span><span class="sxs-lookup"><span data-stu-id="b92a9-168">Speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b92a9-169"><strong>AudioTimestampErrorMicMs</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-169"><strong>AudioTimestampErrorMicMs</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-170">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="b92a9-170">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-171">Taxa de descompasso do relógio do dispositivo de alto-falante, relativa ao relógio da CPU.</span><span class="sxs-lookup"><span data-stu-id="b92a9-171">Speaker device clock drift rate, relative to CPU clock.</span></span></p>
<p><span data-ttu-id="b92a9-172">Erro de carimbo de data/hora médio do fluxo de captura de microfone, em milissegundos, nos últimos 20 segundos da chamada.</span><span class="sxs-lookup"><span data-stu-id="b92a9-172">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-173"><strong>AudioTimestampErrorSpkMs</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-173"><strong>AudioTimestampErrorSpkMs</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-174">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="b92a9-174">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-175">Média de um erro de carimbo de data/hora do fluxo de alto-falante, em milissegundos, nos últimos 20 segundos da chamada.</span><span class="sxs-lookup"><span data-stu-id="b92a9-175">Average speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b92a9-176"><strong>VsEntryCauses</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-176"><strong>VsEntryCauses</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-177">smallint</span><span class="sxs-lookup"><span data-stu-id="b92a9-177">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-178">A opção de voz é um modo Half-duplex com capacidade de interrupção reduzida.</span><span class="sxs-lookup"><span data-stu-id="b92a9-178">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="b92a9-179">Causas da entrada da opção de voz:</span><span class="sxs-lookup"><span data-stu-id="b92a9-179">Causes of voice switch entry:</span></span></p>
<p><span data-ttu-id="b92a9-180">ENTER_VS_BADTS 0x01</span><span class="sxs-lookup"><span data-stu-id="b92a9-180">ENTER_VS_BADTS 0x01</span></span></p>
<p><span data-ttu-id="b92a9-181">ENTER_VS_ECHO 0x02</span><span class="sxs-lookup"><span data-stu-id="b92a9-181">ENTER_VS_ECHO 0x02</span></span></p>
<p><span data-ttu-id="b92a9-182">ENTER_VS_FORCEORCONVERGENCE 0x04</span><span class="sxs-lookup"><span data-stu-id="b92a9-182">ENTER_VS_FORCEORCONVERGENCE 0x04</span></span></p>
<p><span data-ttu-id="b92a9-183">ENTER_VS_DNLP 0x08</span><span class="sxs-lookup"><span data-stu-id="b92a9-183">ENTER_VS_DNLP 0x08</span></span></p>
<p><span data-ttu-id="b92a9-184">A causa pode ser uma combinação dessas causas individuais.</span><span class="sxs-lookup"><span data-stu-id="b92a9-184">The cause can be a combination of those individual causes.</span></span> <span data-ttu-id="b92a9-185">ENTER_VS_FORCEORCONVERGENCE só pode ser habilitado pela RegKey para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="b92a9-185">ENTER_VS_FORCEORCONVERGENCE can only be enabled by regkey for test purpose.</span></span></p>
<p><span data-ttu-id="b92a9-186">O tipo de dados para esta coluna foi alterado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b92a9-186">The data type for this column was changed in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-187"><strong>EchoEventCauses</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-187"><strong>EchoEventCauses</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-188">tinyint</span><span class="sxs-lookup"><span data-stu-id="b92a9-188">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-189">Causas de um evento de eco:</span><span class="sxs-lookup"><span data-stu-id="b92a9-189">Causes of an echo event:</span></span></p>
<p><span data-ttu-id="b92a9-190">ECHO_EVENT_BAD_TIMESTAMP 0x01</span><span class="sxs-lookup"><span data-stu-id="b92a9-190">ECHO_EVENT_BAD_TIMESTAMP 0x01</span></span></p>
<p><span data-ttu-id="b92a9-191">ECHO_EVENT_POSTAEC_ECHO 0x02</span><span class="sxs-lookup"><span data-stu-id="b92a9-191">ECHO_EVENT_POSTAEC_ECHO 0x02</span></span></p>
<p><span data-ttu-id="b92a9-192">ECHO_EVENT_ANLP 0x04</span><span class="sxs-lookup"><span data-stu-id="b92a9-192">ECHO_EVENT_ANLP 0x04</span></span></p>
<p><span data-ttu-id="b92a9-193">ECHO_EVENT_DNLP 0x08</span><span class="sxs-lookup"><span data-stu-id="b92a9-193">ECHO_EVENT_DNLP 0x08</span></span></p>
<p><span data-ttu-id="b92a9-194">ECHO_EVENT_MIC_CLIPPING 0x10</span><span class="sxs-lookup"><span data-stu-id="b92a9-194">ECHO_EVENT_MIC_CLIPPING 0x10</span></span></p>
<p><span data-ttu-id="b92a9-195">ECHO_EVENT_BAD_STATE 0x20</span><span class="sxs-lookup"><span data-stu-id="b92a9-195">ECHO_EVENT_BAD_STATE 0x20</span></span></p>
<p><span data-ttu-id="b92a9-196">A causa pode ser uma combinação dessas causas individuais.</span><span class="sxs-lookup"><span data-stu-id="b92a9-196">The cause can be a combination of those individual causes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b92a9-197"><strong>EchoPercentMicIn</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-197"><strong>EchoPercentMicIn</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-198">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="b92a9-198">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-p109">Porcentagem de tempo em que o eco foi detectado no fluxo de captura do microfone. Normalmente, os valores são baixos para fones de ouvido ou celulares e mais altos para viva voz e auto falante. Para dispositivos que suportam cancelamento de eco acústico na placa, os altos níveis indicam vazamento de eco. Para outros dispositivos, essa métrica não deve ser utilizada para avaliar a qualidade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b92a9-p109">Percentage of time when echo was detected in the microphone capture stream. Typically, values are low for headsets or handsets, and higher for speaker phones or stand-alone speakers. For devices that support on-board acoustic echo cancellation, high values indicate echo leak. For other devices, this metric should not be used to evaluate device quality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-203"><strong>EchoPercentSend</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-203"><strong>EchoPercentSend</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-204">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="b92a9-204">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b92a9-205">Porcentagem de tempo em que o eco é detectado no fluxo de envio.</span><span class="sxs-lookup"><span data-stu-id="b92a9-205">Percentage of time when echo is detected in sent stream.</span></span> <span data-ttu-id="b92a9-206">Alta porcentagem de eco em enviar transmite uma indicação de vazamento de eco.</span><span class="sxs-lookup"><span data-stu-id="b92a9-206">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b92a9-207"><strong>RxAGCSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-207"><strong>RxAGCSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-208">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-208">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-209">Nível de sinal recebido no servidor de mediação do gateway; Isso se aplica apenas ao servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="b92a9-209">Received signal level on the Mediation Server from the Gateway; this applies only to the Mediation Server.</span></span> <span data-ttu-id="b92a9-210">A unidade desta métrica é dBoV.</span><span class="sxs-lookup"><span data-stu-id="b92a9-210">The unit of this metric is dBoV.</span></span> <span data-ttu-id="b92a9-211">Para ter uma boa qualidade, o intervalo aceitável deve ser [-30 a-18] dBoV.</span><span class="sxs-lookup"><span data-stu-id="b92a9-211">For good quality, the acceptable range should be [-30 to -18] dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-212"><strong>RxAGCNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-212"><strong>RxAGCNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-213">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-213">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-214">Nível de sinal recebido no servidor de mediação do gateway.</span><span class="sxs-lookup"><span data-stu-id="b92a9-214">Received signal level on the Mediation Server from the Gateway.</span></span> <span data-ttu-id="b92a9-215">Isso se aplica apenas ao servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="b92a9-215">This applies only to the Mediation Server.</span></span> <span data-ttu-id="b92a9-216">A unidade desta métrica é dBoV.</span><span class="sxs-lookup"><span data-stu-id="b92a9-216">The unit of this metric is dBoV.</span></span> <span data-ttu-id="b92a9-217">Para ter uma boa qualidade, o intervalo aceitável deve ser menor do que-50 dBoV.</span><span class="sxs-lookup"><span data-stu-id="b92a9-217">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b92a9-218"><strong>RxAvgAGCGain</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-218"><strong>RxAvgAGCGain</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-219">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-219">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-220">Controle de ganho automático (AGC) no lado do servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="b92a9-220">Automatic gain control (AGC) on the Mediation Server side.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-221"><strong>InitialSignalLevelRMS</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-221"><strong>InitialSignalLevelRMS</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-222">float</span><span class="sxs-lookup"><span data-stu-id="b92a9-222">float</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b92a9-223">O quadrado de raiz média (RMS) do sinal de entrada de até os primeiros 30 segundos da chamada.</span><span class="sxs-lookup"><span data-stu-id="b92a9-223">The root mean square (RMS) of the incoming signal of up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b92a9-224"><strong>RecvSignalLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-224"><strong>RecvSignalLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-225">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-225">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b92a9-226">Nível de sinal como recebido no canal 1.</span><span class="sxs-lookup"><span data-stu-id="b92a9-226">Signal level as received on channel 1.</span></span></p>
<p><span data-ttu-id="b92a9-227">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b92a9-227">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-228"><strong>RecvSignalLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-228"><strong>RecvSignalLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-229">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-229">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b92a9-230">Nível de sinal como recebido no canal 2.</span><span class="sxs-lookup"><span data-stu-id="b92a9-230">Signal level as received on channel 2.</span></span></p>
<p><span data-ttu-id="b92a9-231">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b92a9-231">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b92a9-232"><strong>RecvNoiseLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-232"><strong>RecvNoiseLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-233">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-233">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b92a9-234">Nível de ruído como recebido no canal 1.</span><span class="sxs-lookup"><span data-stu-id="b92a9-234">Noise level as received on channel 1.</span></span></p>
<p><span data-ttu-id="b92a9-235">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b92a9-235">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-236"><strong>RecvNoiseLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-236"><strong>RecvNoiseLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-237">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-237">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b92a9-238">Nível de ruído como recebido no canal 2.</span><span class="sxs-lookup"><span data-stu-id="b92a9-238">Noise level as received on channel 2.</span></span></p>
<p><span data-ttu-id="b92a9-239">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b92a9-239">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b92a9-240"><strong>SendSignalLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-240"><strong>SendSignalLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-241">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-241">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b92a9-242">Nível de sinal como enviado no canal 1.</span><span class="sxs-lookup"><span data-stu-id="b92a9-242">Signal level as sent on channel 1.</span></span></p>
<p><span data-ttu-id="b92a9-243">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b92a9-243">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-244"><strong>SendSignalLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-244"><strong>SendSignalLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-245">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-245">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b92a9-246">Nível de sinal como enviado no canal 2.</span><span class="sxs-lookup"><span data-stu-id="b92a9-246">Signal level as sent on channel 2.</span></span></p>
<p><span data-ttu-id="b92a9-247">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b92a9-247">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b92a9-248"><strong>SendNoiseLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-248"><strong>SendNoiseLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-249">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-249">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b92a9-250">Nível de ruído enviado no canal 1.</span><span class="sxs-lookup"><span data-stu-id="b92a9-250">Noise level as sent on channel 1.</span></span></p>
<p><span data-ttu-id="b92a9-251">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b92a9-251">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b92a9-252"><strong>SendNoiseLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="b92a9-252"><strong>SendNoiseLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="b92a9-253">int</span><span class="sxs-lookup"><span data-stu-id="b92a9-253">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b92a9-254">Nível de ruído enviado no canal 2.</span><span class="sxs-lookup"><span data-stu-id="b92a9-254">Noise level as sent on channel 2.</span></span></p>
<p><span data-ttu-id="b92a9-255">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b92a9-255">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b92a9-256">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b92a9-256">


</div>

<span> </span>

</div>

</div>

</span></span></div>

