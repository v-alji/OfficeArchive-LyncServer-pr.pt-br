---
title: 'Lync Server 2013: relatório de localização'
description: 'Lync Server 2013: relatório de localização.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location Report
ms:assetid: cb2f1551-1e21-4f13-a39d-91f5f9010ccf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615035(v=OCS.15)
ms:contentKeyID: 48185641
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8b819bcffeee0795cd39d3dde3e38fbd9e4a1b7c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426484"
---
# <a name="location-report-in-lync-server-2013"></a><span data-ttu-id="aa80e-103">Relatório de localização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aa80e-103">Location Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aa80e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aa80e-104">

<span> </span></span></span>

<span data-ttu-id="aa80e-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="aa80e-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="aa80e-p101">O Relatório de Localização oferece informações sobre as métricas de qualidade de chamada agrupadas pelo local de rede (isto é, pela subrede). Se seus usuários enfrentarem problemas com suas chamadas, este relatório pode ajudar você a determinar se estes problemas são amplos ou estão confinados a um determinado segmento da rede.</span><span class="sxs-lookup"><span data-stu-id="aa80e-p101">The Location Report provides information about call quality metrics grouped by network location (that is, by network subnet). If your users are experiencing problems with their calls, this report can help you determine if those problems are widespread or if they are largely confined to a given network segment.</span></span>

<div>

## <a name="accessing-the-location-report"></a><span data-ttu-id="aa80e-108">Acessando o Relatório de Localização</span><span class="sxs-lookup"><span data-stu-id="aa80e-108">Accessing the Location Report</span></span>

<span data-ttu-id="aa80e-p102">O Relatório de Localização é acessado na página inicial de Relatórios de Monitoramento. É possível detalhar o Relatório de Lista de Chamadas clicando em uma das seguintes métricas:</span><span class="sxs-lookup"><span data-stu-id="aa80e-p102">The Location Report is accessed from the Monitoring Reports home page. You can drill down to the Call List Report by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="aa80e-111">Volume da chamada</span><span class="sxs-lookup"><span data-stu-id="aa80e-111">Call volume</span></span>

  - <span data-ttu-id="aa80e-112">Porcentagem de chamadas ruins</span><span class="sxs-lookup"><span data-stu-id="aa80e-112">Poor call percentage</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="aa80e-113">Filtros</span><span class="sxs-lookup"><span data-stu-id="aa80e-113">Filters</span></span>

<span data-ttu-id="aa80e-114">Os filtros oferecem uma forma de retornar um conjunto de dados mais direcionado ou exibir os dados devolvidos em formas diferentes.</span><span class="sxs-lookup"><span data-stu-id="aa80e-114">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways.</span></span> <span data-ttu-id="aa80e-115">Por exemplo, o Relatório de Locais permite que você filtre coisas como o local onde a chamada foi originada ou se a chamada ocorreu em uma conexão com ou sem fio.</span><span class="sxs-lookup"><span data-stu-id="aa80e-115">For example, the Location Report enables you to filter on such things as the location where a call was originated or whether the call took place on a wireless or a wired connection.</span></span> <span data-ttu-id="aa80e-116">Também é possível escolher como os dados devem ser agrupados.</span><span class="sxs-lookup"><span data-stu-id="aa80e-116">You can also choose how data should be grouped.</span></span> <span data-ttu-id="aa80e-117">Nesse caso, as chamadas são agrupadas por hora, dia, semana ou mês.</span><span class="sxs-lookup"><span data-stu-id="aa80e-117">In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="aa80e-118">A tabela a seguir lista os filtros que podem ser usados com o Relatório de Locais.</span><span class="sxs-lookup"><span data-stu-id="aa80e-118">The following table lists the filters that you can use with the Location Report.</span></span>

### <a name="location-report-filters"></a><span data-ttu-id="aa80e-119">Filtros do Relatório de Locais</span><span class="sxs-lookup"><span data-stu-id="aa80e-119">Location Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa80e-120">Nome</span><span class="sxs-lookup"><span data-stu-id="aa80e-120">Name</span></span></th>
<th><span data-ttu-id="aa80e-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa80e-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa80e-122"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-122"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-p104">Data/hora de início para o intervalo de tempo. Para ver os dados por horas, insira a data e hora de início conforme segue:</span><span class="sxs-lookup"><span data-stu-id="aa80e-p104">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="aa80e-125">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="aa80e-125">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="aa80e-p105">Se você não inserir a hora de início, o relatório começará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="aa80e-p105">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="aa80e-128">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="aa80e-128">7/7/2012</span></span></p>
<p><span data-ttu-id="aa80e-129">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="aa80e-129">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="aa80e-130">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="aa80e-130">7/3/2012</span></span></p>
<p><span data-ttu-id="aa80e-131">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="aa80e-131">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa80e-132"><strong>Até</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-132"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-p106">Data/hora final de intervalo de tempo. Para ver os dados por horas, insira a data e hora final conforme segue:</span><span class="sxs-lookup"><span data-stu-id="aa80e-p106">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="aa80e-135">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="aa80e-135">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="aa80e-p107">Se você não inserir a hora final, o relatório terminará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="aa80e-p107">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="aa80e-138">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="aa80e-138">7/7/2012</span></span></p>
<p><span data-ttu-id="aa80e-139">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="aa80e-139">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="aa80e-140">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="aa80e-140">7/3/2012</span></span></p>
<p><span data-ttu-id="aa80e-141">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="aa80e-141">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa80e-142"><strong>Local do chamador</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-142"><strong>Caller location</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-p108">Sub-rede IP do usuário que fez a chamada. É possível selecionar somente <strong>[Tudo]</strong> para indicar todas as sub-redes.</span><span class="sxs-lookup"><span data-stu-id="aa80e-p108">IP subnet of the user who placed the call. You can only select <strong>[All]</strong> to indicate all subnets.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa80e-145"><strong>Local do computador chamado</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-145"><strong>Callee location</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-p109">Sub-rede IP do usuário que recebeu a chamada. É possível selecionar somente <strong>[Tudo]</strong> para indicar todas as sub-redes.</span><span class="sxs-lookup"><span data-stu-id="aa80e-p109">IP subnet of the user who received the call. You can only select <strong>[All]</strong> to indicate all subnets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa80e-148"><strong>Tipo de rede</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-148"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-p110">Indica o tipo de rede que o cliente estava conectado quando a chamada foi realizada. Selecione um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="aa80e-p110">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="aa80e-151">[Todos]</span><span class="sxs-lookup"><span data-stu-id="aa80e-151">[All]</span></span></p></li>
<li><p><span data-ttu-id="aa80e-152">Com fio</span><span class="sxs-lookup"><span data-stu-id="aa80e-152">Wired</span></span></p></li>
<li><p><span data-ttu-id="aa80e-153">Sem fio</span><span class="sxs-lookup"><span data-stu-id="aa80e-153">Wireless</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa80e-154"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-154"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-p111">Indica se um cliente externo estava usando uma conexão de rede privada virtual (VPN) quando a chamada foi realizada. Selecione um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="aa80e-p111">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="aa80e-157">[Todos]</span><span class="sxs-lookup"><span data-stu-id="aa80e-157">[All]</span></span></p></li>
<li><p><span data-ttu-id="aa80e-158">VPN</span><span class="sxs-lookup"><span data-stu-id="aa80e-158">VPN</span></span></p></li>
<li><p><span data-ttu-id="aa80e-159">Não-VPN</span><span class="sxs-lookup"><span data-stu-id="aa80e-159">Non-VPN</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="aa80e-160">Métricas</span><span class="sxs-lookup"><span data-stu-id="aa80e-160">Metrics</span></span>

<span data-ttu-id="aa80e-161">A tabela a seguir lista as informações fornecidas no Relatório de Locais.</span><span class="sxs-lookup"><span data-stu-id="aa80e-161">The following table lists the information provided in the Location Report.</span></span>

### <a name="location-report-metrics"></a><span data-ttu-id="aa80e-162">Métricas do Relatório de Locais</span><span class="sxs-lookup"><span data-stu-id="aa80e-162">Location Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa80e-163">Nome</span><span class="sxs-lookup"><span data-stu-id="aa80e-163">Name</span></span></th>
<th><span data-ttu-id="aa80e-164">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="aa80e-164">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="aa80e-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa80e-165">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa80e-166"><strong>Sub-rede do chamador</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-166"><strong>Caller subnet</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-167">Não</span><span class="sxs-lookup"><span data-stu-id="aa80e-167">No</span></span></p></td>
<td><p><span data-ttu-id="aa80e-168">Sub-rede IP do usuário que fez a chamada.</span><span class="sxs-lookup"><span data-stu-id="aa80e-168">IP subnet of the user who placed the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa80e-169"><strong>Sub-rede do computador chamado</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-169"><strong>Callee subnet</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-170">Não</span><span class="sxs-lookup"><span data-stu-id="aa80e-170">No</span></span></p></td>
<td><p><span data-ttu-id="aa80e-171">Sub-rede IP do usuário que recebeu a chamada.</span><span class="sxs-lookup"><span data-stu-id="aa80e-171">IP subnet of the user who received the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa80e-172"><strong>Volume da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-172"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-173">Sim</span><span class="sxs-lookup"><span data-stu-id="aa80e-173">Yes</span></span></p></td>
<td><p><span data-ttu-id="aa80e-174">Número total de chamadas realizadas.</span><span class="sxs-lookup"><span data-stu-id="aa80e-174">Total number of calls placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa80e-175"><strong>Porcentagem de chamadas ruins</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-175"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-176">Sim</span><span class="sxs-lookup"><span data-stu-id="aa80e-176">Yes</span></span></p></td>
<td><p><span data-ttu-id="aa80e-p112">Percentual de chamadas classificadas como ruins. Uma chamada ruim é qualquer chamada da qual pelo menos uma das métricas medidas excedeu o valor permitido (por exemplo, uma chamada que experimentou tremulação excessiva).</span><span class="sxs-lookup"><span data-stu-id="aa80e-p112">Percentage of calls classified as poor calls. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa80e-179"><strong>Viagem de ida e volta (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-179"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-180">Sim</span><span class="sxs-lookup"><span data-stu-id="aa80e-180">Yes</span></span></p></td>
<td><p><span data-ttu-id="aa80e-p113">Quantidade média de (em milissegundos) exigida para que um pacote RTP (protocolo de transporte em tempo real) viaje até outra extremidade e retorne. Tempos de viagem de ida e volta de 100 milissegundos ou menos são considerados de qualidade aceitável.</span><span class="sxs-lookup"><span data-stu-id="aa80e-p113">Average amount of (in milliseconds) required for a real-time transport protocol (RTP) packet to travel to another endpoint and then back. Round-trip times of 100 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="aa80e-p114">Os valores altos de ida e volta pode ser causados por roteamento de chamada internacional, um erro de configuração de roteamento ou um servidor de mídia sobrecarregado. Tempos de ida e volta altos resultam em dificuldades com conversas de áudio em tempo real e bidirecionais.</span><span class="sxs-lookup"><span data-stu-id="aa80e-p114">High round-trip values can be caused by international call routing, a routing misconfiguration, or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa80e-185"><strong>Degradação (MOS)</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-185"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-186">Sim</span><span class="sxs-lookup"><span data-stu-id="aa80e-186">Yes</span></span></p></td>
<td><p><span data-ttu-id="aa80e-187">Quantidade média da degradação MOS (pontuação média de opinião) enfrentada durante uma chamada.</span><span class="sxs-lookup"><span data-stu-id="aa80e-187">Average amount of mean opinion score (MOS) degradation experienced during a call.</span></span> <span data-ttu-id="aa80e-188">Os valores de degradação variam de um baixo de 0,0 a um alto de 5,0.</span><span class="sxs-lookup"><span data-stu-id="aa80e-188">Degradation values can range from a low of 0.0 to a high of 5.0.</span></span> <span data-ttu-id="aa80e-189">Um valor de 0,5 ou menos representa degradação aceitável.</span><span class="sxs-lookup"><span data-stu-id="aa80e-189">A value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="aa80e-190">As pontuações médias de opinião costumava ser calculadas a partir da classificação da qualidade de uma chamada em uma escala de 1 a 5, feita pelos dos usuários.</span><span class="sxs-lookup"><span data-stu-id="aa80e-190">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="aa80e-191">No Lync Server, o Lync Server usa um conjunto de algoritmos para prever como os usuários teriam classificado uma chamada.</span><span class="sxs-lookup"><span data-stu-id="aa80e-191">In Lync Server, Lync Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="aa80e-p116">Os valores de degradação altos podem ser causados por congestão, falta de largura de banda, congestionamento ou interferência sem fio ou um servidor de mídia ou ponto de extremidade sobrecarregado. A alta degradação resulta em perda ou distorção de áudio.</span><span class="sxs-lookup"><span data-stu-id="aa80e-p116">High degradation values can be caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa80e-194"><strong>Perda de pacote</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-194"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-195">Sim</span><span class="sxs-lookup"><span data-stu-id="aa80e-195">Yes</span></span></p></td>
<td><p><span data-ttu-id="aa80e-p117">Taxa média de perda de pacote RTP. (A perda de pacote ocorre quando os pacotes RTP, um protocolo usado para transmissão de áudio e vídeo pela Internet, não conseguem chegar aos seus destinos.) Taxas de perda altas normalmente são causadas por congestionamento, falta de largura de banda, congestionamento ou interferência sem fio ou um servidor de mídia sobrecarregado. A perda de pacote normalmente resulta em perda ou distorção de áudio.</span><span class="sxs-lookup"><span data-stu-id="aa80e-p117">Average rate of RTP packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa80e-199"><strong>Tremulação</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-199"><strong>Jitter</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-200">Sim</span><span class="sxs-lookup"><span data-stu-id="aa80e-200">Yes</span></span></p></td>
<td><p><span data-ttu-id="aa80e-201">Tremulação média detectada entre chegadas de pacote RTP.</span><span class="sxs-lookup"><span data-stu-id="aa80e-201">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="aa80e-202">(Tremulação é uma medida do &quot; shakiness &quot; de uma chamada.) Os valores de variação alta geralmente são causados por congestionamento ou um servidor de mídia sobrecarregado, resultando em áudio distorcido ou perdido.</span><span class="sxs-lookup"><span data-stu-id="aa80e-202">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa80e-203"><strong>Taxa de correção oculta</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-203"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-204">Sim</span><span class="sxs-lookup"><span data-stu-id="aa80e-204">Yes</span></span></p></td>
<td><p><span data-ttu-id="aa80e-p119">Taxa média de amostras de áudio ocultas para o número total de amostras. (Uma amostra de áudio oculta é uma técnica usada para suavizar a transição abrupta que normalmente seria causada por pacotes de rede descartados.) Valores altos indicam níveis consideráveis de perda de ocultação aplicada causada por perda de pacote ou tremulação e resulta na perda ou distorção de áudio.</span><span class="sxs-lookup"><span data-stu-id="aa80e-p119">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa80e-207"><strong>Taxa de correção estendida</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-207"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-208">Sim</span><span class="sxs-lookup"><span data-stu-id="aa80e-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="aa80e-p120">Taxa média de amostras de áudio estendidas para o número total de amostras. (Áudio estendido é o áudio que foi expandido a fim de ajudar a manter a qualidade da chamada quando um pacote de rede descartado é detectado.) Valores altos indicam níveis significativos de extensão de amostra causada por tremulação e resultam em um som robótico ou distorcido.</span><span class="sxs-lookup"><span data-stu-id="aa80e-p120">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa80e-211"><strong>Taxa de correção compactada</strong></span><span class="sxs-lookup"><span data-stu-id="aa80e-211"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="aa80e-212">Sim</span><span class="sxs-lookup"><span data-stu-id="aa80e-212">Yes</span></span></p></td>
<td><p><span data-ttu-id="aa80e-p121">Taxa média de amostras de áudio compactadas para o número total de amostras. (Áudio compactado é o áudio que foi compactado para ajudar a manter a qualidade da chamada quando um pacote de rede descartado é detectado.) Valores altos podem indicar níveis consideráveis de compactação de amostra causada por tremulação e resultam em um som acelerado ou distorcido.</span><span class="sxs-lookup"><span data-stu-id="aa80e-p121">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="aa80e-215">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aa80e-215">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

