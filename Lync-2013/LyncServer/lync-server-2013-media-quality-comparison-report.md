---
title: 'Lync Server 2013: relatório de comparação de qualidade de mídia'
description: 'Lync Server 2013: relatório de comparação de qualidade de mídia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Comparison Report
ms:assetid: c1d0b5a8-98ff-455a-b78b-a05a21cf066d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205236(v=OCS.15)
ms:contentKeyID: 48185317
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b2c4c5c948d167ce5210f9814c4e0625ffaa9152
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425679"
---
# <a name="media-quality-comparison-report-in-lync-server-2013"></a><span data-ttu-id="70714-103">Relatório de comparação de qualidade de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="70714-103">Media Quality Comparison Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="70714-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="70714-104">

<span> </span></span></span>

<span data-ttu-id="70714-105">_**Tópico da última modificação:** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="70714-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="70714-106">O Relatório de Comparação de Qualidade da Mídia permite comparar os valores de qualidade da chamada para diferentes tipos de chamadas de áudio (por exemplo, chamadas realizadas por uma rede sem fio contra chamadas realizadas em uma conexão com fio).</span><span class="sxs-lookup"><span data-stu-id="70714-106">The Media Quality Comparison Report enables you to compare call quality values for different types of audio calls (for example, calls made over a wireless network vs. calls made across a wired connection).</span></span>

<div>

## <a name="accessing-the-media-quality-comparison-report"></a><span data-ttu-id="70714-107">Como acessar o Relatório de Comparação de Qualidade de Mídia</span><span class="sxs-lookup"><span data-stu-id="70714-107">Accessing the Media Quality Comparison Report</span></span>

<span data-ttu-id="70714-108">O Relatório de Comparação de Qualidade de Mídia é acessado na página inicial de Relatórios de Monitoramento.</span><span class="sxs-lookup"><span data-stu-id="70714-108">The Media Quality Comparison Report is accessed from the Monitoring Reports home page.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="70714-109">Filtros</span><span class="sxs-lookup"><span data-stu-id="70714-109">Filters</span></span>

<span data-ttu-id="70714-p101">Os filtros oferecem uma forma de retornar um conjunto de dados mais detalhado ou exibir os dados retornados em formas diferentes. A tabela a seguir lista os filtros que você pode usar com o Relatório de Comparação de Qualidade de Mídia.</span><span class="sxs-lookup"><span data-stu-id="70714-p101">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Media Quality Comparison Report.</span></span>

### <a name="media-quality-comparison-report-filters"></a><span data-ttu-id="70714-112">Filtros do Relatório de Comparação de Qualidade de Mídia</span><span class="sxs-lookup"><span data-stu-id="70714-112">Media Quality Comparison Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70714-113">Nome</span><span class="sxs-lookup"><span data-stu-id="70714-113">Name</span></span></th>
<th><span data-ttu-id="70714-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="70714-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70714-115"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="70714-115"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="70714-p102">Data/hora de início para o intervalo de tempo. Para ver os dados por horas, insira a data e hora de início conforme segue:</span><span class="sxs-lookup"><span data-stu-id="70714-p102">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="70714-118">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="70714-118">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="70714-p103">Se você não inserir a hora de início, o relatório começará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="70714-p103">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="70714-121">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="70714-121">7/7/2012</span></span></p>
<p><span data-ttu-id="70714-122">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="70714-122">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="70714-123">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="70714-123">7/3/2012</span></span></p>
<p><span data-ttu-id="70714-124">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="70714-124">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70714-125"><strong>Até</strong></span><span class="sxs-lookup"><span data-stu-id="70714-125"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="70714-p104">Data/hora final de intervalo de tempo. Para ver os dados por horas, insira a data e hora final conforme segue:</span><span class="sxs-lookup"><span data-stu-id="70714-p104">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="70714-128">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="70714-128">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="70714-p105">Se você não inserir a hora final, o relatório terminará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="70714-p105">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="70714-131">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="70714-131">7/7/2012</span></span></p>
<p><span data-ttu-id="70714-132">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="70714-132">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="70714-133">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="70714-133">7/3/2012</span></span></p>
<p><span data-ttu-id="70714-134">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="70714-134">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70714-135"><strong>Chamadas</strong></span><span class="sxs-lookup"><span data-stu-id="70714-135"><strong>Calls</strong></span></span></p></td>
<td><p><span data-ttu-id="70714-p106">Tipo de chamada a ser usado como o item de comparação principal. Os valores permitidos são:</span><span class="sxs-lookup"><span data-stu-id="70714-p106">Type of call to be used as the main comparison item. Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="70714-138">[Todos]</span><span class="sxs-lookup"><span data-stu-id="70714-138">[All]</span></span></p></li>
<li><p><span data-ttu-id="70714-139">Externo</span><span class="sxs-lookup"><span data-stu-id="70714-139">External</span></span></p></li>
<li><p><span data-ttu-id="70714-140">Interno</span><span class="sxs-lookup"><span data-stu-id="70714-140">Internal</span></span></p></li>
<li><p><span data-ttu-id="70714-141">VPN</span><span class="sxs-lookup"><span data-stu-id="70714-141">VPN</span></span></p></li>
<li><p><span data-ttu-id="70714-142">Não VPN</span><span class="sxs-lookup"><span data-stu-id="70714-142">Non-VPN</span></span></p></li>
<li><p><span data-ttu-id="70714-143">Com fio</span><span class="sxs-lookup"><span data-stu-id="70714-143">Wired</span></span></p></li>
<li><p><span data-ttu-id="70714-144">Sem fio</span><span class="sxs-lookup"><span data-stu-id="70714-144">Wireless</span></span></p></li>
<li><p><span data-ttu-id="70714-145">Externo e com fio</span><span class="sxs-lookup"><span data-stu-id="70714-145">External and wired</span></span></p></li>
<li><p><span data-ttu-id="70714-146">Externo e sem fio</span><span class="sxs-lookup"><span data-stu-id="70714-146">External and wireless</span></span></p></li>
<li><p><span data-ttu-id="70714-147">Externo e VPN</span><span class="sxs-lookup"><span data-stu-id="70714-147">External and VPN</span></span></p></li>
<li><p><span data-ttu-id="70714-148">Externo e não VPN</span><span class="sxs-lookup"><span data-stu-id="70714-148">External and non-VPN</span></span></p></li>
<li><p><span data-ttu-id="70714-149">Interno e com fio</span><span class="sxs-lookup"><span data-stu-id="70714-149">Internal and wired</span></span></p></li>
<li><p><span data-ttu-id="70714-150">Interno e sem fio</span><span class="sxs-lookup"><span data-stu-id="70714-150">Internal and wireless</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70714-151"><strong>Comparar com chamadas</strong></span><span class="sxs-lookup"><span data-stu-id="70714-151"><strong>Compare with calls</strong></span></span></p></td>
<td><p><span data-ttu-id="70714-p107">Tipo de chamada a ser usado como o item de comparação secundário. Os valores permitidos são:</span><span class="sxs-lookup"><span data-stu-id="70714-p107">Type of call to be used as the secondary comparison item. Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="70714-154">[Todos]</span><span class="sxs-lookup"><span data-stu-id="70714-154">[All]</span></span></p></li>
<li><p><span data-ttu-id="70714-155">Externo</span><span class="sxs-lookup"><span data-stu-id="70714-155">External</span></span></p></li>
<li><p><span data-ttu-id="70714-156">Interno</span><span class="sxs-lookup"><span data-stu-id="70714-156">Internal</span></span></p></li>
<li><p><span data-ttu-id="70714-157">VPN</span><span class="sxs-lookup"><span data-stu-id="70714-157">VPN</span></span></p></li>
<li><p><span data-ttu-id="70714-158">Não VPN</span><span class="sxs-lookup"><span data-stu-id="70714-158">Non-VPN</span></span></p></li>
<li><p><span data-ttu-id="70714-159">Com fio</span><span class="sxs-lookup"><span data-stu-id="70714-159">Wired</span></span></p></li>
<li><p><span data-ttu-id="70714-160">Sem fio</span><span class="sxs-lookup"><span data-stu-id="70714-160">Wireless</span></span></p></li>
<li><p><span data-ttu-id="70714-161">Externo e com fio</span><span class="sxs-lookup"><span data-stu-id="70714-161">External and wired</span></span></p></li>
<li><p><span data-ttu-id="70714-162">Externo e sem fio</span><span class="sxs-lookup"><span data-stu-id="70714-162">External and wireless</span></span></p></li>
<li><p><span data-ttu-id="70714-163">Externo e VPN</span><span class="sxs-lookup"><span data-stu-id="70714-163">External and VPN</span></span></p></li>
<li><p><span data-ttu-id="70714-164">Externo e não VPN</span><span class="sxs-lookup"><span data-stu-id="70714-164">External and non-VPN</span></span></p></li>
<li><p><span data-ttu-id="70714-165">Interno e com fio</span><span class="sxs-lookup"><span data-stu-id="70714-165">Internal and wired</span></span></p></li>
<li><p><span data-ttu-id="70714-166">Interno e sem fio</span><span class="sxs-lookup"><span data-stu-id="70714-166">Internal and wireless</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70714-167"><strong>Intervalo</strong></span><span class="sxs-lookup"><span data-stu-id="70714-167"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="70714-p108">Intervalo de tempo. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="70714-p108">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="70714-170">Por hora (é possível exibir no máximo 25 horas)</span><span class="sxs-lookup"><span data-stu-id="70714-170">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="70714-171">Diariamente (é possível exibir no máximo 31 dias)</span><span class="sxs-lookup"><span data-stu-id="70714-171">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="70714-172">Semanalmente (é possível exibir no máximo 12 semanas)</span><span class="sxs-lookup"><span data-stu-id="70714-172">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="70714-173">Se as datas de início e término excederem o número máximo de valores permitidos para o intervalo selecionado, somente o número máximo de valores (a partir da data de início) será exibido.</span><span class="sxs-lookup"><span data-stu-id="70714-173">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="70714-174">Por exemplo, se você selecionar o intervalo diário com uma data de início de 7/7/2012 e uma data de término de 2/28/2012, os dados serão exibidos para os dias 8/7/2012 12:00 AM a 9/7/2012 12:00 AM (ou seja, um total de 31 dias da importância dos dados).</span><span class="sxs-lookup"><span data-stu-id="70714-174">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="70714-175">Métricas</span><span class="sxs-lookup"><span data-stu-id="70714-175">Metrics</span></span>

<span data-ttu-id="70714-176">A tabela a seguir lista as informações fornecidas no Relatório de Comparação de Qualidade da Mídia.</span><span class="sxs-lookup"><span data-stu-id="70714-176">The following table lists the information provided in the Media Quality Comparison Report.</span></span>

### <a name="media-quality-comparison-report-metrics"></a><span data-ttu-id="70714-177">Métricas do Relatório de Comparação de Qualidade da Mídia</span><span class="sxs-lookup"><span data-stu-id="70714-177">Media Quality Comparison Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70714-178">Nome</span><span class="sxs-lookup"><span data-stu-id="70714-178">Name</span></span></th>
<th><span data-ttu-id="70714-179">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="70714-179">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="70714-180">Descrição</span><span class="sxs-lookup"><span data-stu-id="70714-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70714-181"><strong>Volume da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="70714-181"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="70714-182">Não</span><span class="sxs-lookup"><span data-stu-id="70714-182">No</span></span></p></td>
<td><p><span data-ttu-id="70714-183">Número total de chamadas.</span><span class="sxs-lookup"><span data-stu-id="70714-183">Total number of calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70714-184"><strong>Degradação (MOS)</strong></span><span class="sxs-lookup"><span data-stu-id="70714-184"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="70714-185">Não</span><span class="sxs-lookup"><span data-stu-id="70714-185">No</span></span></p></td>
<td><p><span data-ttu-id="70714-186">Valor médio da degradação da MOS (Pontuação de opinião média) durante uma chamada.</span><span class="sxs-lookup"><span data-stu-id="70714-186">Average amount of MOS (mean opinion score) degradation experienced during a call.</span></span> <span data-ttu-id="70714-187">Os valores de degradação podem variar de um baixo de 0,0 a um alto de 5,0; um valor de 0,5 ou menos representa uma degradação aceitável.</span><span class="sxs-lookup"><span data-stu-id="70714-187">Degradation values can range from a low of 0.0 to a high of 5.0; a value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="70714-188">Historicamente, a média das pontuações de opinião foi calculada pela necessidade de os usuários classificarem a qualidade de uma chamada em uma escala de 1 a 5.</span><span class="sxs-lookup"><span data-stu-id="70714-188">Historically, mean opinion scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="70714-189">O Lync Server usa um conjunto de algoritmos para prever como os usuários teriam classificado uma chamada.</span><span class="sxs-lookup"><span data-stu-id="70714-189">Lync Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="70714-p111">Valores altos de degradação podem ser causados por congestionamento, falta de largura de banda, congestionamento ou interferência na rede sem fio ou um servidor de mídia ou ponto de extremidade sobrecarregado. A alta degradação resulta em perda ou distorção de áudio.</span><span class="sxs-lookup"><span data-stu-id="70714-p111">High degradation values can be caused by congestion; lack of bandwidth; wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70714-192"><strong>Porcentagem de chamadas ruins</strong></span><span class="sxs-lookup"><span data-stu-id="70714-192"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="70714-193">Não</span><span class="sxs-lookup"><span data-stu-id="70714-193">No</span></span></p></td>
<td><p><span data-ttu-id="70714-p112">O número total de chamadas classificadas como ruins. Uma chamada ruim é qualquer chamada em que no mínimo uma das métricas excedeu o valor permitido (por exemplo, uma chamada com tremulação excessiva).</span><span class="sxs-lookup"><span data-stu-id="70714-p112">The total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70714-196"><strong>Ida e volta (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="70714-196"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="70714-197">Não</span><span class="sxs-lookup"><span data-stu-id="70714-197">No</span></span></p></td>
<td><p><span data-ttu-id="70714-p113">Quantidade média (em milissegundos) exigida para que um pacote de protocolo RTP viaje até outro ponto de extremidade e retorne. Tempos de viagem de ida e volta de 200 milissegundos ou menos são considerados de qualidade aceitável.</span><span class="sxs-lookup"><span data-stu-id="70714-p113">Average amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back. Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="70714-p114">Os valores altos de tempo de resposta podem ser causados por roteamento de chamadas internacionais, configuração incorreta de um roteamento ou um servidor de mídia sobrecarregado. Tempos de resposta altos resultam em dificuldades para conversas de áudio bidirecionais e em tempo real.</span><span class="sxs-lookup"><span data-stu-id="70714-p114">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70714-202"><strong>Perda de pacote</strong></span><span class="sxs-lookup"><span data-stu-id="70714-202"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="70714-203">Não</span><span class="sxs-lookup"><span data-stu-id="70714-203">No</span></span></p></td>
<td><p><span data-ttu-id="70714-p115">Taxa média de perda de pacotes de RTP (protocolo de transporte em tempo real). (A perda de pacotes ocorre quando pacotes de RTP, um protocolo usado para transmitir áudio e vídeo pela Internet, falha ao tentar alcançar seu destino). Altas taxas de perda geralmente são causadas por congestionamento, insuficiência da largura de banda, congestionamento ou interferência na rede sem fio ou um servidor de mídia sobrecarregado. A perda de pacotes normalmente resulta em distorção ou perda de áudio.</span><span class="sxs-lookup"><span data-stu-id="70714-p115">Average rate of Real-Time Transport Protocol (RTP) packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70714-207"><strong>Tremulação (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="70714-207"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="70714-208">Não</span><span class="sxs-lookup"><span data-stu-id="70714-208">No</span></span></p></td>
<td><p><span data-ttu-id="70714-209">Tremulação média detectada entre chegadas de pacote RTP.</span><span class="sxs-lookup"><span data-stu-id="70714-209">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="70714-210">(Tremulação é uma medida do &quot; shakiness &quot; de uma chamada.) Os valores de variação alta geralmente são causados por congestionamento ou um servidor de mídia sobrecarregado, resultando em áudio distorcido ou perdido.</span><span class="sxs-lookup"><span data-stu-id="70714-210">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70714-211"><strong>Taxa de correção oculta</strong></span><span class="sxs-lookup"><span data-stu-id="70714-211"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="70714-212">Não</span><span class="sxs-lookup"><span data-stu-id="70714-212">No</span></span></p></td>
<td><p><span data-ttu-id="70714-p117">Taxa média de amostras de áudio ocultas para o número total de amostras. (Uma amostra de áudio oculta é uma técnica usada para suavizar a transição abrupta que normalmente seria causada por pacotes de rede descartados.) Valores altos indicam níveis consideráveis de perda de ocultação aplicada causada por perda de pacote ou tremulação e resulta na perda ou distorção de áudio.</span><span class="sxs-lookup"><span data-stu-id="70714-p117">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70714-215"><strong>Taxa de correção estendida</strong></span><span class="sxs-lookup"><span data-stu-id="70714-215"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="70714-216">Não</span><span class="sxs-lookup"><span data-stu-id="70714-216">No</span></span></p></td>
<td><p><span data-ttu-id="70714-p118">Taxa média de amostras de áudio estendidas para o número total de amostras. (Áudio estendido é o áudio que foi expandido a fim de ajudar a manter a qualidade da chamada quando um pacote de rede descartado é detectado.) Valores altos indicam níveis significativos de extensão de amostra causada por tremulação e resultam em um som robótico ou distorcido.</span><span class="sxs-lookup"><span data-stu-id="70714-p118">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70714-219"><strong>Taxa de correção compactada</strong></span><span class="sxs-lookup"><span data-stu-id="70714-219"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="70714-220">Não</span><span class="sxs-lookup"><span data-stu-id="70714-220">No</span></span></p></td>
<td><p><span data-ttu-id="70714-p119">Taxa média de amostras de áudio compactadas para o número total de amostras. (Áudio compactado é o áudio que foi compactado para ajudar a manter a qualidade da chamada quando um pacote de rede descartado é detectado.) Valores altos podem indicar níveis consideráveis de compactação de amostra causada por tremulação e resultam em um som acelerado ou distorcido.</span><span class="sxs-lookup"><span data-stu-id="70714-p119">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="70714-223">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="70714-223">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

