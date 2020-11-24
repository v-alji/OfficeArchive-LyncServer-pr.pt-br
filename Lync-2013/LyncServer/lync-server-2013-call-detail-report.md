---
title: 'Lync Server 2013: relatório de detalhes da chamada'
description: 'Lync Server 2013: relatório de detalhes da chamada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Detail Report
ms:assetid: 38862e35-3fec-41b9-a035-0b301942d446
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558637(v=OCS.15)
ms:contentKeyID: 48183843
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d72ae6c1c1ec869041eee5b0dc35941c33609710
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390195"
---
# <a name="call-detail-report-in-lync-server-2013"></a><span data-ttu-id="5e764-103">Relatório de detalhes da chamada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5e764-103">Call Detail Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5e764-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5e764-104">

<span> </span></span></span>

<span data-ttu-id="5e764-105">_**Tópico da última modificação:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="5e764-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="5e764-106">O relatório de detalhes da chamada fornece uma visão detalhada de uma chamada individual; o relatório inclui praticamente todas as métricas de experiência de experiência e estatísticas coletadas pelo Lync Server, divididas em seções de relatório, como:</span><span class="sxs-lookup"><span data-stu-id="5e764-106">The Call Detail Report provides a detailed look at an individual call; the report includes nearly all the Quality of Experience metrics and statistics collected by Lync Server, divided into report sections such as:</span></span>

  - <span data-ttu-id="5e764-107">Informações da chamada</span><span class="sxs-lookup"><span data-stu-id="5e764-107">Call Information</span></span>

  - <span data-ttu-id="5e764-108">Medição do dispositivo e do sinal do chamador</span><span class="sxs-lookup"><span data-stu-id="5e764-108">Caller Device and Signal Metrics</span></span>

  - <span data-ttu-id="5e764-109">Medição do dispositivo e do sinal de quem é chamado</span><span class="sxs-lookup"><span data-stu-id="5e764-109">Callee Device and Signal metrics</span></span>

  - <span data-ttu-id="5e764-110">Evento do cliente do chamador</span><span class="sxs-lookup"><span data-stu-id="5e764-110">Caller Client Event</span></span>

  - <span data-ttu-id="5e764-111">Evento do cliente de quem é chamado</span><span class="sxs-lookup"><span data-stu-id="5e764-111">Callee Client Event</span></span>

  - <span data-ttu-id="5e764-112">Fluxo de áudio (do chamador para que é chamado)</span><span class="sxs-lookup"><span data-stu-id="5e764-112">Audio Stream (Caller to Callee)</span></span>

  - <span data-ttu-id="5e764-113">Fluxo de vídeo (do chamador para que é chamado)</span><span class="sxs-lookup"><span data-stu-id="5e764-113">Video Stream (Caller to Callee)</span></span>

  - <span data-ttu-id="5e764-114">Fluxo de áudio (de quem é chamado para o chamador)</span><span class="sxs-lookup"><span data-stu-id="5e764-114">Audio Stream (Callee to Caller)</span></span>

  - <span data-ttu-id="5e764-115">Fluxo de vídeo (de quem é chamado para o chamador)</span><span class="sxs-lookup"><span data-stu-id="5e764-115">Video Stream (Callee to Caller)</span></span>

<span data-ttu-id="5e764-p101">Lembre-se de que as categorias e métricas de um determinado relatório dependem de duas coisas: o tipo de sessão e o tipo de ponto de extremidade usados na sessão. Por exemplo, uma chamada com apenas áudio não reportará métricas de fluxo de vídeo; isso se deve ao fato de a chamada não ter um fluxo de vídeo. Da mesma forma, é possível ter um relatório que liste estatísticas do chamador, mas não de quem é chamado. Normalmente, isso ocorre quando quem foi chamado não usa um dispositivo compatível com SIP. Os pontos de extremidade são responsáveis por reportar estatísticas no final de uma chamada; no entanto, um telefone celular (que desconhece SIP ou as estatísticas de SIP) não pode reportar esse tipo de informação. Se você ligar para alguém e essa pessoa atender em um telefone celular, você não obterá um relatório desse telefone celular quando a chamada terminar.</span><span class="sxs-lookup"><span data-stu-id="5e764-p101">Keep in mind that the categories and the metrics you see on a given report depend on two things: the type of session and the type of endpoints used in the session. For example, an audio-only call will not report metrics for video streams; that's because the call didn't have a video stream. Likewise, you might have a report that lists caller statistics but not callee statistics. That's typically because the callee was not using a SIP-compliant device. Endpoints are responsible for reporting statistics at the end of a call; however, a cell phone (which knows nothing about SIP or SIP statistics) is unable to report that kind of information. If you call someone and they answer you on their cell phone, you will not get a report from that cell phone when the call ends.</span></span>

<span data-ttu-id="5e764-122">O Relatório Detalhado de Chamadas é especialmente útil quando você está tentando determinar exatamente porque determinada chamada enfrentou problemas de qualidade de mídia.</span><span class="sxs-lookup"><span data-stu-id="5e764-122">The Call Detail Report is most useful when you are trying to determine exactly why a given call experienced media quality problems.</span></span>

<div>

## <a name="accessing-the-call-detail-report"></a><span data-ttu-id="5e764-123">Acessando o Relatório Detalhado de Chamadas</span><span class="sxs-lookup"><span data-stu-id="5e764-123">Accessing the Call Detail Report</span></span>

<span data-ttu-id="5e764-124">O Relatório Detalhado de Chamadas pode ser acessado a partir de qualquer um dos seguintes relatórios:</span><span class="sxs-lookup"><span data-stu-id="5e764-124">The Call Detail Report can be accessed from any of the following reports:</span></span>

  - <span data-ttu-id="5e764-125">O [relatório de localização no Lync Server 2013](lync-server-2013-location-report.md) (clicando no volume da chamada ou na métrica de porcentagem baixa de chamada)</span><span class="sxs-lookup"><span data-stu-id="5e764-125">The [Location Report in Lync Server 2013](lync-server-2013-location-report.md) (by clicking either the Call volume or the Poor call percentage metric)</span></span>

  - <span data-ttu-id="5e764-126">O [relatório de Resumo de qualidade de mídia no Lync Server 2013](lync-server-2013-media-quality-summary-report.md) (clicando no volume da chamada ou na métrica de porcentagem baixa de chamada)</span><span class="sxs-lookup"><span data-stu-id="5e764-126">The [Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md) (by clicking either the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="5e764-127">O [relatório de comparação de qualidade de mídia no Lync server 2013](lync-server-2013-media-quality-comparison-report.md) (clicando no [relatório lista de chamadas no Lync Server 2013](lync-server-2013-call-list-report.md) e, em seguida, clicando na métrica de detalhes).</span><span class="sxs-lookup"><span data-stu-id="5e764-127">The [Media Quality Comparison Report in Lync Server 2013](lync-server-2013-media-quality-comparison-report.md) (by clicking the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) and then clicking the Detail metric).</span></span>

  - <span data-ttu-id="5e764-128">O [relatório de desempenho do servidor no Lync Server 2013](lync-server-2013-server-performance-report.md) (clicando no volume da chamada ou na métrica de porcentagem baixa de chamada)</span><span class="sxs-lookup"><span data-stu-id="5e764-128">The [Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md) (by clicking either the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="5e764-129">O [relatório lista de chamadas no Lync Server 2013](lync-server-2013-call-list-report.md) (clicando na métrica detalhe)</span><span class="sxs-lookup"><span data-stu-id="5e764-129">The [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) (by clicking the Detail metric)</span></span>

<span data-ttu-id="5e764-130">No relatório de detalhes da chamada, você pode acessar o [relatório de dispositivo no Lync Server 2013](lync-server-2013-device-report.md) clicando em uma das seguintes métricas:</span><span class="sxs-lookup"><span data-stu-id="5e764-130">From within the Call Detail Report you can access the [Device Report in Lync Server 2013](lync-server-2013-device-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="5e764-131">Dispositivo de captura</span><span class="sxs-lookup"><span data-stu-id="5e764-131">Capture device</span></span>

  - <span data-ttu-id="5e764-132">Dispositivos de renderização</span><span class="sxs-lookup"><span data-stu-id="5e764-132">Render device</span></span>

<span data-ttu-id="5e764-133">Também é possível acessar o Relatório de Tendências de Qualidade de Mídia clicando na métrica Servidor de borda de áudio/vídeo.</span><span class="sxs-lookup"><span data-stu-id="5e764-133">You can also access the Server Media Quality Trend Report by clicking the A/V edge server metric.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-detail-report"></a><span data-ttu-id="5e764-134">Fazendo o melhor uso do Relatório Detalhado de Chamadas</span><span class="sxs-lookup"><span data-stu-id="5e764-134">Making the Best Use of the Call Detail Report</span></span>

<span data-ttu-id="5e764-p102">O Relatório Detalhado de Chamadas normalmente contém 250 métricas diferentes, inclusive itens como Descompasso do carimbo de data/hora do microfone, Tempo de SNR baixo e Extremidade próxima ao tempo de eco. Se não conseguir se lembrar o que exatamente todas essas métricas avaliam, tente pousar o mouse sobre o rótulo da métrica; na maioria das vezes, uma dica de ferramenta será exibida descrevendo a métrica.</span><span class="sxs-lookup"><span data-stu-id="5e764-p102">The Call Detail Report typically includes over 250 different metrics, including such items as Microphone timestamp drift, Low SNR time, and Near end to echo time. If you can't remember what all of these metrics actually measure, try holding your mouse over the metric label; often-times, a tooltip will appear describing that metric.</span></span>

<span data-ttu-id="5e764-137">Se você tiver problemas para localizar uma métrica, digite parte do rótulo métrica na caixa de pesquisa e clique em localizar.</span><span class="sxs-lookup"><span data-stu-id="5e764-137">If you have problems locating a metric, type part of the metric label in the search box and then click Find.</span></span> <span data-ttu-id="5e764-138">Por exemplo, se você não conseguir encontrar a métrica de tempo SNR baixa, digite SNR na caixa de pesquisa e clique em localizar.</span><span class="sxs-lookup"><span data-stu-id="5e764-138">For example, if you can't find the Low SNR time metric, type SNR in the search box and then click Find.</span></span>

<span data-ttu-id="5e764-p104">Observe que o relatório rastreia apenas as informações sobre uma chamada. A chamada em si não é gravada.</span><span class="sxs-lookup"><span data-stu-id="5e764-p104">Note that the report only tracks information about a call. The call itself is not recorded.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="5e764-141">Filtros</span><span class="sxs-lookup"><span data-stu-id="5e764-141">Filters</span></span>

<span data-ttu-id="5e764-p105">Nenhum. Você não pode filtrar o Relatório Detalhado de Chamadas.</span><span class="sxs-lookup"><span data-stu-id="5e764-p105">None. You cannot filter the Call Detail Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="5e764-144">Métricas</span><span class="sxs-lookup"><span data-stu-id="5e764-144">Metrics</span></span>

<span data-ttu-id="5e764-145">A tabela a seguir lista as informações fornecidas no Relatório Detalhado de Chamadas para cada chamada.</span><span class="sxs-lookup"><span data-stu-id="5e764-145">The following table lists the information provided in the Call Detail Report for each call.</span></span>

### <a name="call-detail-report-metrics"></a><span data-ttu-id="5e764-146">Métricas do Relatório Detalhado de Chamadas</span><span class="sxs-lookup"><span data-stu-id="5e764-146">Call Detail Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5e764-147">Nome</span><span class="sxs-lookup"><span data-stu-id="5e764-147">Name</span></span></th>
<th><span data-ttu-id="5e764-148">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="5e764-148">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="5e764-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e764-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e764-150"><strong>PAI do chamador</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-150"><strong>Caller PAI</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-151">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-151">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-p106">O P-Asserted-Identity do usuário que iniciou a chamada. Essa identidade é usada para transportar a identidade comprovada de um usuário dentro de uma rede confiável.</span><span class="sxs-lookup"><span data-stu-id="5e764-p106">P-Asserted-Identity of the user who initiated the call. The P-Asserted-Identity is used to convey the proven identity of a user within a trusted network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e764-154"><strong>URI do chamador</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-154"><strong>Caller URI</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-155">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-155">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-156">Endereço SIP do usuário que iniciou a chamada.</span><span class="sxs-lookup"><span data-stu-id="5e764-156">SIP address of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e764-157"><strong>Ponto de extremidade do chamador</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-157"><strong>Caller endpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-158">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-158">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-159">Dispositivo usado para efetuar a chamada.</span><span class="sxs-lookup"><span data-stu-id="5e764-159">Device used to make the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e764-160"><strong>Agente do usuário do chamador</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-160"><strong>Caller user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-161">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-161">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-162">Software usado no dispositivo que fez a chamada.</span><span class="sxs-lookup"><span data-stu-id="5e764-162">Software used on the device that made the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e764-163"><strong>Início da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-163"><strong>Call start</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-164">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-164">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-165">Data e hora em que a chamada foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="5e764-165">Date and time that the call was initially placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e764-166"><strong>Chamada de desvio do Servidor de Mediação</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-166"><strong>Mediation Server bypass call</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-167">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-167">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-168">Indica se a chamada conectou a um gateway de voz PSTN ou IP-PBX qualificado sem passar pelo Servidor de Mediação.</span><span class="sxs-lookup"><span data-stu-id="5e764-168">Indicates whether the call connected to a PSTN voice gateway or qualified IP-PBX without passing through the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e764-169"><strong>OS do chamador</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-169"><strong>Caller OS</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-170">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-170">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-171">Sistema operacional do computador do chamador.</span><span class="sxs-lookup"><span data-stu-id="5e764-171">Operating system of the caller's computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e764-172"><strong>CPU do chamador</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-172"><strong>Caller CPU</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-173">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-173">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-174">CPU instalado no computador do usuário que iniciou a chamada.</span><span class="sxs-lookup"><span data-stu-id="5e764-174">CPU installed in the computer of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e764-175"><strong>Número de core do CPU do chamador</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-175"><strong>Caller CPU core number</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-176">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-176">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-177">Número do processador no computador usado pela pessoa que iniciou a chamada.</span><span class="sxs-lookup"><span data-stu-id="5e764-177">Processor number in the computer used by the person who initiated the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e764-178"><strong>Velocidade de CPU do chamador</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-178"><strong>Caller CPU speed</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-179">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-179">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-180">Velocidade de relógio do CPU do computador usado pela pessoa que iniciou a chamada.</span><span class="sxs-lookup"><span data-stu-id="5e764-180">Clock speed of the CPU of the computer used by the person who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e764-181"><strong>Virtualização de CPU do chamador</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-181"><strong>Caller CPU virtualization</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-182">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-182">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-183">Virtualização (se houver) no computador usado pela pessoa que iniciou a chamada.</span><span class="sxs-lookup"><span data-stu-id="5e764-183">Virtualization (if any) used on the computer used by the person who initiated the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e764-184"><strong>PAI do receptor da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-184"><strong>Callee PAI</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-185">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-185">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-p107">O P-Asserted-Identity do usuário convidado a entrar na chamada. Essa identidade é usada para transportar a identidade comprovada de um usuário dentro de uma rede confiável.</span><span class="sxs-lookup"><span data-stu-id="5e764-p107">P-Asserted-Identity of the user who was invited to join the call. The P-Asserted-Identity is used to convey the proven identity of a user within a trusted network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e764-188"><strong>URI do receptor da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-188"><strong>Callee URI</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-189">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-189">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-190">Endereço SIP do usuário que foi chamado.</span><span class="sxs-lookup"><span data-stu-id="5e764-190">SIP address of the user who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e764-191"><strong>Ponto de extremidade do receptor da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-191"><strong>Callee endpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-192">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-192">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-193">Dispositivo usado para receber a chamada.</span><span class="sxs-lookup"><span data-stu-id="5e764-193">Device used to receive the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e764-194"><strong>Agente do usuário do receptor</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-194"><strong>Callee user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-195">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-195">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-196">Software usado no dispositivo que recebeu a chamada.</span><span class="sxs-lookup"><span data-stu-id="5e764-196">Software used on the device that received the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e764-197"><strong>Duração</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-197"><strong>Duration</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-198">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-198">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-199">Tempo da chamada.</span><span class="sxs-lookup"><span data-stu-id="5e764-199">Length of time for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e764-200"><strong>Sinalizador de aviso do desvio de mídia</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-200"><strong>Media bypass warning flag</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-201">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-201">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-202">Aviso emitido quando o Servidor de Mediação foi desviado.</span><span class="sxs-lookup"><span data-stu-id="5e764-202">Warning issued when the Mediation Server was bypassed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e764-203"><strong>OS do receptor da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-203"><strong>Callee OS</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-204">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-204">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-205">Sistema operacional do computador do usuário que foi chamado.</span><span class="sxs-lookup"><span data-stu-id="5e764-205">Operating system of the computer for the user who was called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e764-206"><strong>CPU do receptor da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-206"><strong>Callee CPU</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-207">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-207">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-208">CPU instalado no computador do usuário que foi chamado.</span><span class="sxs-lookup"><span data-stu-id="5e764-208">CPU installed in the computer of the user who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e764-209"><strong>Número de core do receptor da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-209"><strong>Callee core number</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-210">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-210">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-211">Número do processador no computador usado pela pessoa que foi chamada.</span><span class="sxs-lookup"><span data-stu-id="5e764-211">Processor number in the computer used by the person who was called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e764-212"><strong>Velocidade de CPU do receptor da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-212"><strong>Callee CPU speed</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-213">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-213">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-214">Velocidade de relógio do CPU do computador usado pela pessoa que foi chamada.</span><span class="sxs-lookup"><span data-stu-id="5e764-214">Clock speed of the CPU of the computer used by the person who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e764-215"><strong>Virtualização de CPU do receptor da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="5e764-215"><strong>Callee CPU virtualization</strong></span></span></p></td>
<td><p><span data-ttu-id="5e764-216">Não</span><span class="sxs-lookup"><span data-stu-id="5e764-216">No</span></span></p></td>
<td><p><span data-ttu-id="5e764-217">Virtualização (se houver) no computador usado pela pessoa que foi chamada.</span><span class="sxs-lookup"><span data-stu-id="5e764-217">Virtualization (if any) used on the computer used by the person who was called.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5e764-218">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5e764-218">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

