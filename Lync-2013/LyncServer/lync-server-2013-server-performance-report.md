---
title: 'Lync Server 2013: relatório de desempenho do servidor'
description: 'Lync Server 2013: relatório de desempenho do servidor.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server Performance Report
ms:assetid: 942bb39a-1790-498e-9d99-8f6ce2d155c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615018(v=OCS.15)
ms:contentKeyID: 48184879
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aed9b3b9eeec4487dce4d401df0d70ffba89677b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441876"
---
# <a name="server-performance-report-in-lync-server-2013"></a><span data-ttu-id="bb017-103">Relatório de desempenho do servidor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb017-103">Server Performance Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bb017-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bb017-104">

<span> </span></span></span>

<span data-ttu-id="bb017-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="bb017-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="bb017-106">O relatório de desempenho do servidor fornece uma lista de servidores do Microsoft Lync Server 2013 que tiveram o maior percentual de chamadas ruins.</span><span class="sxs-lookup"><span data-stu-id="bb017-106">The Server Performance Report provides a list of Microsoft Lync Server 2013 servers that have experienced the highest-percentage of poor calls.</span></span> <span data-ttu-id="bb017-107">O relatório divide os servidores por tipo, relatando estatísticas separadas para os seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="bb017-107">The report breaks down servers by server type, reporting separate statistics for the following types:</span></span>

  - <span data-ttu-id="bb017-108">Servidor de Mediação</span><span class="sxs-lookup"><span data-stu-id="bb017-108">Mediation Server</span></span>

  - <span data-ttu-id="bb017-109">Servidor de Conferência A/V</span><span class="sxs-lookup"><span data-stu-id="bb017-109">A/V Conferencing Server</span></span>

  - <span data-ttu-id="bb017-110">Servidor de Borda A/V</span><span class="sxs-lookup"><span data-stu-id="bb017-110">A/V Edge Server</span></span>

  - <span data-ttu-id="bb017-111">Gateway (Servidor de Mediação)</span><span class="sxs-lookup"><span data-stu-id="bb017-111">Gateway (Mediation Server)</span></span>

  - <span data-ttu-id="bb017-112">Gateway (desvio de Servidor de Mediação)</span><span class="sxs-lookup"><span data-stu-id="bb017-112">Gateway (Mediation Server bypass)</span></span>

  - <span data-ttu-id="bb017-113">Vídeo (incluindo métricas de vídeo para Servidores de Conferência A/V e Servidores de Borda A/V)</span><span class="sxs-lookup"><span data-stu-id="bb017-113">Video (including video metrics for A/V Conferencing servers and A/V Edge servers)</span></span>

  - <span data-ttu-id="bb017-114">Compartilhamento de aplicativos (incluindo métricas de compartilhamento de aplicativos para Servidores de Conferência A/V e Servidores de Borda A/V)</span><span class="sxs-lookup"><span data-stu-id="bb017-114">Application Sharing (including application sharing metrics for A/V Conferencing servers and A/V Edge servers)</span></span>

<span data-ttu-id="bb017-p102">É importante observar a classificação mostrada neste relatório como classificação relativa. Por exemplo, suponha que seu servidor com pior desempenho tenha uma chamada ruim entre suas 1.000 chamadas efetuadas. Isso é uma porcentagem de 0,1% que é mais que aceitável. No entanto, se esse for seu servidor com pior desempenho (isto é, se todos os seus outros servidores tiverem uma porcentagem de chamada ruim mais baixa que 0,1%), então esse servidor aparecerá mesmo assim no Relatório de desempenho do servidor.</span><span class="sxs-lookup"><span data-stu-id="bb017-p102">It’s important to note that the ranking shown in this report as relative rankings. For example, suppose your worst-performing server had one poor call among its 1,000 placed calls. That's a more-than-acceptable percentage of .1%. However, if that's the worst-performing server you have (that is, if all your other servers have a poor call percentage even lower than .1%), then that server will still appear on the Server Performance Report.</span></span>

<div>

## <a name="accessing-the-server-performance-report"></a><span data-ttu-id="bb017-119">Como avaliar o Relatório de desempenho do servidor</span><span class="sxs-lookup"><span data-stu-id="bb017-119">Accessing the Server Performance Report</span></span>

<span data-ttu-id="bb017-120">O Relatório de desempenho do servidor é acessado na página inicial dos Relatórios de Monitoramento.</span><span class="sxs-lookup"><span data-stu-id="bb017-120">The Server Performance Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="bb017-121">Você pode fazer uma busca detalhada no [relatório de lista de chamadas no Lync Server 2013](lync-server-2013-call-list-report.md) clicando em uma das seguintes métricas:</span><span class="sxs-lookup"><span data-stu-id="bb017-121">You can drill down to the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="bb017-122">Volume da chamada</span><span class="sxs-lookup"><span data-stu-id="bb017-122">Call volume</span></span>

  - <span data-ttu-id="bb017-123">Porcentagem de chamada inválida</span><span class="sxs-lookup"><span data-stu-id="bb017-123">Poor call percentage</span></span>

<span data-ttu-id="bb017-124">Além disso, você ver os detalhes do Relatório de Tendência de Qualidade de Mídia do Servidor clicando na seguinte métrica:</span><span class="sxs-lookup"><span data-stu-id="bb017-124">In addition, you can drill down to the Server Media Quality Trend Report by clicking the following metric:</span></span>

  - <span data-ttu-id="bb017-125">Tendência</span><span class="sxs-lookup"><span data-stu-id="bb017-125">Trend</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-server-performance-report"></a><span data-ttu-id="bb017-126">Como aproveitar ao máximo o relatório de desempenho do servidor</span><span class="sxs-lookup"><span data-stu-id="bb017-126">Making the Best Use of the Server Performance Report</span></span>

<span data-ttu-id="bb017-p104">O Relatório de desempenho do servidor fornece várias maneiras de filtrar dados; por exemplo, você pode filtrar por tipo de rede (chamadas feitas de uma chamada cabeada x chamadas de uma conexão sem fio) e tipo de acesso (chamadas feitas de dentro do firewall x chamadas feitas de fora do firewall). Ao exibir o relatório de desempenho do servidor, é uma boa ideia usar esses filtros. Por exemplo, suponha que você tem um Servidor de Mediação que tenha uma porcentagem de chamadas ruins igual a 3,24%. Se você observar apenas as chamadas sem fio, o mesmo servidor teria uma porcentagem de chamadas ruins próxima de 20%. Isso significa que o servidor tem dificuldades com chamadas sem fio, um problema que é obscurecido parcialmente porque o servidor não tem problemas em lidar com chamadas com fio.</span><span class="sxs-lookup"><span data-stu-id="bb017-p104">The Server Performance Report provides a number of ways to filter data; for example, you can filter on network type (calls made from a wired connection vs. calls made from a wireless connection) and access type (calls made from inside the firewall vs. calls made from outside the firewall). It's a good idea when viewing the server performance report to make use of these filters. For example, suppose you have a Mediation Server that has a poor call percentage of 3.24%. If you look solely at wireless calls, that same server might have a poor call percentage approaching 20%. That means that the server was having difficulty with wireless calls, a problem that is partially obscured because the server was not having problems with wired calls.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="bb017-132">Filtros</span><span class="sxs-lookup"><span data-stu-id="bb017-132">Filters</span></span>

<span data-ttu-id="bb017-p105">Filtros fornecem uma forma de retornar um conjunto de dados mais focado ou exibir os dados retornados de diferentes formas. Por exemplo o Relatório de Desempenho do Servidor permite fazer coisas como filtrar os dados retornados por tipo de servidor ou por tipo de rede (ou seja, com ou sem fio). Você também pode escolher como os dados serão agrupados. Neste caso, os dados são agrupados por hora, dia, semana ou mês.</span><span class="sxs-lookup"><span data-stu-id="bb017-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Server Performance Report enables you to do such things as filter the returned data by server type or by network type (that is, wired or wireless). You can also choose how data should be grouped. In this case, data is grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="bb017-137">A tabela a seguir lista os filtros que podem ser usados com o Relatório de Desempenho do Servidor.</span><span class="sxs-lookup"><span data-stu-id="bb017-137">The following table lists the filters that you can use with the Server Performance Report.</span></span>

### <a name="server-performance-report-filters"></a><span data-ttu-id="bb017-138">Filtros do Relatório de Desempenho do Servidor</span><span class="sxs-lookup"><span data-stu-id="bb017-138">Server Performance Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb017-139">Nome</span><span class="sxs-lookup"><span data-stu-id="bb017-139">Name</span></span></th>
<th><span data-ttu-id="bb017-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb017-140">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb017-141"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-141"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-p106">Data/hora de início para o intervalo de tempo. Para ver os dados por horas, insira a data e hora de início conforme segue:</span><span class="sxs-lookup"><span data-stu-id="bb017-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="bb017-144">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="bb017-144">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="bb017-p107">Se você não inserir a hora de início, o relatório começará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="bb017-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="bb017-147">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="bb017-147">7/7/2012</span></span></p>
<p><span data-ttu-id="bb017-148">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="bb017-148">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="bb017-149">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="bb017-149">7/3/2012</span></span></p>
<p><span data-ttu-id="bb017-150">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="bb017-150">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-151"><strong>Até</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-151"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-p108">Data/hora final de intervalo de tempo. Para ver os dados por horas, insira a data e hora final conforme segue:</span><span class="sxs-lookup"><span data-stu-id="bb017-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="bb017-154">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="bb017-154">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="bb017-p109">Se você não inserir a hora final, o relatório terminará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="bb017-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="bb017-157">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="bb017-157">7/7/2012</span></span></p>
<p><span data-ttu-id="bb017-158">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="bb017-158">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="bb017-159">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="bb017-159">7/3/2012</span></span></p>
<p><span data-ttu-id="bb017-160">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="bb017-160">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-161"><strong>Tipo de servidor</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-161"><strong>Server type</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-p110">Indica o tipo de servidor cujo desempenho deve ser reportado. Selecione um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="bb017-p110">Indicates the type of server whose performance should be reported. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="bb017-164">[Todos]</span><span class="sxs-lookup"><span data-stu-id="bb017-164">[All]</span></span></p></li>
<li><p><span data-ttu-id="bb017-165">Servidor de Mediação</span><span class="sxs-lookup"><span data-stu-id="bb017-165">Mediation Server</span></span></p></li>
<li><p><span data-ttu-id="bb017-166">Servidor de Conferência A/V</span><span class="sxs-lookup"><span data-stu-id="bb017-166">A/V Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="bb017-167">Servidor de Borda A/V</span><span class="sxs-lookup"><span data-stu-id="bb017-167">A/V Edge Server</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-168"><strong>N Primeiros</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-168"><strong>Top N</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-p111">Indica o número de servidores (com base no percentual de chamadas ruins) a serem exibidos em cada categoria. Por exemplo, se você selecionar <strong>5</strong>, os cinco servidores com pior desempenho são exibidos. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="bb017-p111">Indicates the number of servers (based on their poor call percentage) to be displayed in each category. For example, if you select <strong>5</strong> then the five poorest-performing servers are displayed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="bb017-172">[Todos]</span><span class="sxs-lookup"><span data-stu-id="bb017-172">[All]</span></span></p></li>
<li><p><span data-ttu-id="bb017-173">5</span><span class="sxs-lookup"><span data-stu-id="bb017-173">5</span></span></p></li>
<li><p><span data-ttu-id="bb017-174">254</span><span class="sxs-lookup"><span data-stu-id="bb017-174">10</span></span></p></li>
</ol></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-175"><strong>Tipo de acesso</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-175"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-p112">Indica se um cliente estava conectado na rede interna ou na rede externa quando a chamada foi realizada. Selecione um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="bb017-p112">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="bb017-178">[Todos]</span><span class="sxs-lookup"><span data-stu-id="bb017-178">[All]</span></span></p></li>
<li><p><span data-ttu-id="bb017-179">Interno</span><span class="sxs-lookup"><span data-stu-id="bb017-179">Internal</span></span></p></li>
<li><p><span data-ttu-id="bb017-180">Externo</span><span class="sxs-lookup"><span data-stu-id="bb017-180">External</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-181"><strong>Tipo de rede</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-181"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-p113">Indica o tipo de rede que o cliente estava conectado quando a chamada foi realizada. Selecione um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="bb017-p113">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="bb017-184">[Todos]</span><span class="sxs-lookup"><span data-stu-id="bb017-184">[All]</span></span></p></li>
<li><p><span data-ttu-id="bb017-185">Com fio</span><span class="sxs-lookup"><span data-stu-id="bb017-185">Wired</span></span></p></li>
<li><p><span data-ttu-id="bb017-186">Sem fio</span><span class="sxs-lookup"><span data-stu-id="bb017-186">Wireless</span></span></p></li>
</ol></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-187"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-187"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-p114">Indica se um cliente externo estava usando uma conexão de rede privada virtual (VPN) quando a chamada foi realizada. Selecione um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="bb017-p114">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="bb017-190">[Todos]</span><span class="sxs-lookup"><span data-stu-id="bb017-190">[All]</span></span></p></li>
<li><p><span data-ttu-id="bb017-191">VPN</span><span class="sxs-lookup"><span data-stu-id="bb017-191">VPN</span></span></p></li>
<li><p><span data-ttu-id="bb017-192">Não-VPN</span><span class="sxs-lookup"><span data-stu-id="bb017-192">Non-VPN</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="bb017-193">Métricas</span><span class="sxs-lookup"><span data-stu-id="bb017-193">Metrics</span></span>

<span data-ttu-id="bb017-194">A tabela a seguir lista as informações fornecidas no Relatório de Desempenho do Servidor.</span><span class="sxs-lookup"><span data-stu-id="bb017-194">The following table lists the information provided in the Server Performance Report.</span></span>

### <a name="server-performance-report-metrics-audio-call-summary"></a><span data-ttu-id="bb017-195">Métricas do Relatório de Desempenho do Servidor: Resumo da chamada de áudio</span><span class="sxs-lookup"><span data-stu-id="bb017-195">Server Performance Report Metrics: Audio Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb017-196">Nome</span><span class="sxs-lookup"><span data-stu-id="bb017-196">Name</span></span></th>
<th><span data-ttu-id="bb017-197">É possível classificar por</span><span class="sxs-lookup"><span data-stu-id="bb017-197">Can Sort On</span></span></th>
<th><span data-ttu-id="bb017-198">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb017-198">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb017-199"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-200">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-200">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-201">Nome/endereço IP do servidor.</span><span class="sxs-lookup"><span data-stu-id="bb017-201">Name/IP address of the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-202"><strong>Volume da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-202"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-203">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-203">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-204">Número total de chamadas realizadas.</span><span class="sxs-lookup"><span data-stu-id="bb017-204">Total number of calls made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-205"><strong>Porcentagem de chamada inválida</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-205"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-206">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-206">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-p115">Número total de chamadas classificadas como ruins. Uma chamada ruim é qualquer chamada em que no mínimo uma das métricas medidas excedeu o valor permitido (por exemplo, uma chamada com tremulação excessiva).</span><span class="sxs-lookup"><span data-stu-id="bb017-p115">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-209"><strong>Viagem de ida e volta (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-209"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-210">Sim</span><span class="sxs-lookup"><span data-stu-id="bb017-210">Yes</span></span></p></td>
<td><p><span data-ttu-id="bb017-p116">Quantidade média de (em milissegundos) exigida para que um pacote RTP (protocolo de transporte em tempo real) viaje até outra extremidade e retorne. Tempos de viagem de ida e volta de 100 milissegundos ou menos são considerados de qualidade aceitável.</span><span class="sxs-lookup"><span data-stu-id="bb017-p116">Average amount of (in milliseconds) required for a real-time transport protocol (RTP) packet to travel to another endpoint and then back. Round-trip times of 100 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="bb017-p117">Altos valores de tempo de resposta podem ser causados por roteamento de chamadas internacionais, configuração incorreta de um roteamento ou um servidor de mídia sobrecarregado. Tempos de resposta altos resultam em dificuldades para conversas de áudio bidirecionais e em tempo real.</span><span class="sxs-lookup"><span data-stu-id="bb017-p117">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-215"><strong>Degradação (MOS)</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-215"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-216">Sim</span><span class="sxs-lookup"><span data-stu-id="bb017-216">Yes</span></span></p></td>
<td><p><span data-ttu-id="bb017-217">Quantidade média da degradação MOS (pontuação média de opinião) enfrentada durante uma chamada.</span><span class="sxs-lookup"><span data-stu-id="bb017-217">Average amount of mean opinion score (MOS) degradation experienced during a call.</span></span> <span data-ttu-id="bb017-218">Os valores de degradação variam de um baixo de 0,0 a um alto de 5,0.</span><span class="sxs-lookup"><span data-stu-id="bb017-218">Degradation values can range from a low of 0.0 to a high of 5.0.</span></span> <span data-ttu-id="bb017-219">Um valor de 0,5 ou menos representa degradação aceitável.</span><span class="sxs-lookup"><span data-stu-id="bb017-219">A value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="bb017-220">As pontuações médias de opinião costumava ser calculadas a partir da classificação da qualidade de uma chamada em uma escala de 1 a 5, feita pelos dos usuários.</span><span class="sxs-lookup"><span data-stu-id="bb017-220">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="bb017-221">No Lync Server, o Monitoring Server usa um conjunto de algoritmos para prever como os usuários teriam classificado uma chamada.</span><span class="sxs-lookup"><span data-stu-id="bb017-221">In Lync Server, the Monitoring Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="bb017-p119">Os valores de degradação altos podem ser causados por congestão, falta de largura de banda, congestionamento ou interferência sem fio ou um servidor de mídia ou ponto de extremidade sobrecarregado. A alta degradação resulta em perda ou distorção de áudio.</span><span class="sxs-lookup"><span data-stu-id="bb017-p119">High degradation values can be caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-224"><strong>Perda de pacote</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-224"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-225">Sim</span><span class="sxs-lookup"><span data-stu-id="bb017-225">Yes</span></span></p></td>
<td><p><span data-ttu-id="bb017-p120">Taxa média de perda de pacotes de protocolo de transporte em tempo real (RTP) (a perda de pacotes ocorre quando pacotes RTP, um protocolo usado para transmitir áudio e vídeo pela internet, falha ao tentar alcançar seu destino). Altas taxas de perda geralmente são causadas por congestionamento, insuficiência da largura de banda, congestionamento ou interferência na rede sem fio ou um servidor de mídia sobrecarregado. A perda de pacotes normalmente resulta em distorção ou perda de áudio.</span><span class="sxs-lookup"><span data-stu-id="bb017-p120">Average rate of real-time transport protocol (RTP) packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-229"><strong>Tremulação (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-229"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-230">Sim</span><span class="sxs-lookup"><span data-stu-id="bb017-230">Yes</span></span></p></td>
<td><p><span data-ttu-id="bb017-231">Tremulação média detectada entre chegadas de pacote RTP.</span><span class="sxs-lookup"><span data-stu-id="bb017-231">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="bb017-232">(Tremulação é uma medida do &quot; shakiness &quot; de uma chamada.) Os valores de variação alta geralmente são causados por congestionamento ou um servidor de mídia sobrecarregado, resultando em áudio distorcido ou perdido.</span><span class="sxs-lookup"><span data-stu-id="bb017-232">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-233"><strong>Taxa de correção oculta</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-233"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-234">Sim</span><span class="sxs-lookup"><span data-stu-id="bb017-234">Yes</span></span></p></td>
<td><p><span data-ttu-id="bb017-p122">Taxa média de amostras de áudio ocultas para o número total de amostras. (Uma amostra de áudio oculta é uma técnica usada para suavizar a transição abrupta que normalmente seria causada por pacotes de rede descartados.) Valores altos indicam níveis consideráveis de perda de ocultação aplicada causada por perda de pacote ou tremulação e resulta na perda ou distorção de áudio.</span><span class="sxs-lookup"><span data-stu-id="bb017-p122">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-237"><strong>Taxa de correção estendida</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-237"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-238">Sim</span><span class="sxs-lookup"><span data-stu-id="bb017-238">Yes</span></span></p></td>
<td><p><span data-ttu-id="bb017-p123">Taxa média de amostras de áudio estendidas para o número total de amostras. (Áudio estendido é o áudio que foi expandido a fim de ajudar a manter a qualidade da chamada quando um pacote de rede descartado é detectado.) Valores altos indicam níveis significativos de extensão de amostra causada por tremulação e resultam em um som robótico ou distorcido.</span><span class="sxs-lookup"><span data-stu-id="bb017-p123">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-241"><strong>Taxa de correção compactada</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-241"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-242">Sim</span><span class="sxs-lookup"><span data-stu-id="bb017-242">Yes</span></span></p></td>
<td><p><span data-ttu-id="bb017-p124">Taxa média de amostras de áudio compactadas para o número total de amostras. (Áudio compactado é o áudio que foi compactado para ajudar a manter a qualidade da chamada quando um pacote de rede descartado é detectado.) Valores altos podem indicar níveis consideráveis de compactação de amostra causada por tremulação e resultam em um som acelerado ou distorcido.</span><span class="sxs-lookup"><span data-stu-id="bb017-p124">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="server-performance-report-metrics-video-call-summary"></a><span data-ttu-id="bb017-245">Métricas do Relatório de Desempenho do Servidor: Resumo da chamada de vídeo</span><span class="sxs-lookup"><span data-stu-id="bb017-245">Server Performance Report Metrics: Video Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb017-246">Nome</span><span class="sxs-lookup"><span data-stu-id="bb017-246">Name</span></span></th>
<th><span data-ttu-id="bb017-247">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="bb017-247">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="bb017-248">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb017-248">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb017-249"><strong>Tipo de chamada/Tipo de ponto de extremidade</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-249"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-250">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-250">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-p125">Ao clicar neste item, o relatório mostra informações detalhadas sobre chamadas baseadas no tipo escolhido. Tipos de chamada incluem:</span><span class="sxs-lookup"><span data-stu-id="bb017-p125">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="bb017-253">Chamadas Ponto a Ponto de UC</span><span class="sxs-lookup"><span data-stu-id="bb017-253">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="bb017-254">Sessões de Conferência de UC</span><span class="sxs-lookup"><span data-stu-id="bb017-254">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="bb017-255">Sessões de Conferência PSTN</span><span class="sxs-lookup"><span data-stu-id="bb017-255">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="bb017-256">Chamadas PSTN: Desvio de Mídia</span><span class="sxs-lookup"><span data-stu-id="bb017-256">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="bb017-257">Chamadas PSTN (Não Ignorar): Trecho de UC</span><span class="sxs-lookup"><span data-stu-id="bb017-257">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="bb017-258">Chamadas PSTN (Não Ignorar): Trecho de Gateway</span><span class="sxs-lookup"><span data-stu-id="bb017-258">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="bb017-259">Outros Tipos de Chamada</span><span class="sxs-lookup"><span data-stu-id="bb017-259">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-260"><strong>Volume da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-260"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-261">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-261">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-262">Número total de chamadas por tipo de chamada.</span><span class="sxs-lookup"><span data-stu-id="bb017-262">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-263"><strong>Porcentagem de chamada inválida</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-263"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-264">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-264">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-p126">Número total de chamadas classificadas como ruins. Uma chamada ruim é qualquer chamada em que no mínimo uma das métricas medidas excedeu o valor permitido (por exemplo, uma chamada com tremulação excessiva).</span><span class="sxs-lookup"><span data-stu-id="bb017-p126">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-267"><strong>Volume de chamadas (chamadas sem fio)</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-267"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-268">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-268">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-269">Número total de chamadas que usaram uma conexão sem fio.</span><span class="sxs-lookup"><span data-stu-id="bb017-269">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-270"><strong>Volume de chamadas (chamadas VPN)</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-270"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-271">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-271">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-272">Número total de chamadas que usaram uma conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="bb017-272">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-273"><strong>Volume de chamadas (chamadas externas)</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-273"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-274">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-274">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-275">Número de chamadas que usaram uma conexão externa (ou seja, uma conexão fora da rede interna).</span><span class="sxs-lookup"><span data-stu-id="bb017-275">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-276"><strong>Taxa de bits média (Kbits/s)</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-276"><strong>Avg bit-rate (Kbits/s)</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-277">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-277">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-278">Taxa de bits média (em quilobytes por segundo).</span><span class="sxs-lookup"><span data-stu-id="bb017-278">Average video bit rate (in kilobits per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-279"><strong>Taxa de bits baixa %</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-279"><strong>Low bit-rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-280">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-280">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-281">Porcentagem da chamada onde a taxa de bits foi baixa.</span><span class="sxs-lookup"><span data-stu-id="bb017-281">Percentage of the call where the bit rate was low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-282"><strong>Perda de pacote de saída</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-282"><strong>Outbound packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-283">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-283">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-p127">Perda de pacotes do Protocolo de transporte em tempo real (RTP) para pacotes enviados. (A perda de pacotes ocorre quando pacotes RTP, um protocolo usado para transmitir áudio e vídeo pela internet, falha ao tentar alcançar seu destino). Altas taxas de perda geralmente são causadas por congestionamento, insuficiência da largura de banda, congestionamento ou interferência na rede sem fio ou um servidor de mídia sobrecarregado. A perda de pacotes normalmente resulta em distorção ou perda de áudio.</span><span class="sxs-lookup"><span data-stu-id="bb017-p127">Real-Time Transport Protocol (RTP) packet loss for outbound packets. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-287"><strong>% de quadros congelados</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-287"><strong>Frozen frame %</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-288">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-288">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-p128">Porcentagem de quadros "congelados". Em um quadro congelado, o vídeo não avança enquanto a parte de áudio da chamada prossegue.</span><span class="sxs-lookup"><span data-stu-id="bb017-p128">Percentage of “frozen” frames. In a frozen frame, the video stops advancing while the audio portion of the call continues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-291"><strong>Taxa de quadros média de saída</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-291"><strong>Outbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-292">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-292">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-293">Taxa de quadros média para transmissões de saída durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="bb017-293">Average frame rate for outbound transmissions during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-294"><strong>Taxa de quadros média de entrada</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-294"><strong>Inbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-295">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-295">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-296">Taxa de quadros média para transmissões de entrada durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="bb017-296">Average frame rate for incoming transmissions during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-297"><strong>% de taxa de quadros baixa de entrada</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-297"><strong>Inbound low frame rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-298">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-298">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-299">Porcentagem da chamada onde a taxa de bits foi baixa para vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="bb017-299">Percentage of the call where the bit rate for incoming video was low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-300"><strong>% de integridade do cliente</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-300"><strong>Client health %</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="bb017-301">Indica o estado relativo do dispositivo do cliente durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="bb017-301">Indicates the relative health of the client device during the call.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="server-performance-report-metrics-application-sharing-call-summary"></a><span data-ttu-id="bb017-302">Métricas do Relatório de Desempenho do Servidor: Resumo da chamada de compartilhamento de aplicativo</span><span class="sxs-lookup"><span data-stu-id="bb017-302">Server Performance Report Metrics: Application Sharing Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb017-303">Nome</span><span class="sxs-lookup"><span data-stu-id="bb017-303">Name</span></span></th>
<th><span data-ttu-id="bb017-304">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="bb017-304">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="bb017-305">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb017-305">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb017-306"><strong>Tipo de chamada/Tipo de ponto de extremidade</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-306"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-307">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-307">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-p129">Ao clicar neste item, o relatório mostra informações detalhadas sobre chamadas baseadas no tipo escolhido. Tipos de chamada incluem:</span><span class="sxs-lookup"><span data-stu-id="bb017-p129">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="bb017-310">Chamadas Ponto a Ponto de UC</span><span class="sxs-lookup"><span data-stu-id="bb017-310">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="bb017-311">Sessões de Conferência de UC</span><span class="sxs-lookup"><span data-stu-id="bb017-311">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="bb017-312">Sessões de Conferência PSTN</span><span class="sxs-lookup"><span data-stu-id="bb017-312">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="bb017-313">Chamadas PSTN: Desvio de Mídia</span><span class="sxs-lookup"><span data-stu-id="bb017-313">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="bb017-314">Chamadas PSTN (Não Ignorar): Trecho de UC</span><span class="sxs-lookup"><span data-stu-id="bb017-314">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="bb017-315">Chamadas PSTN (Não Ignorar): Trecho de Gateway</span><span class="sxs-lookup"><span data-stu-id="bb017-315">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="bb017-316">Outros Tipos de Chamada</span><span class="sxs-lookup"><span data-stu-id="bb017-316">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-317"><strong>Volume da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-317"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-318">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-318">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-319">Número total de chamadas por tipo de chamada.</span><span class="sxs-lookup"><span data-stu-id="bb017-319">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-320"><strong>Porcentagem de chamada inválida</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-320"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-321">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-321">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-p130">Número total de chamadas classificadas como ruins. Uma chamada ruim é qualquer chamada em que no mínimo uma das métricas medidas excedeu o valor permitido (por exemplo, uma chamada com tremulação excessiva).</span><span class="sxs-lookup"><span data-stu-id="bb017-p130">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-324"><strong>Volume de chamadas (chamadas sem fio)</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-324"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-325">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-325">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-326">Número total de chamadas que usaram uma conexão sem fio.</span><span class="sxs-lookup"><span data-stu-id="bb017-326">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-327"><strong>Volume de chamadas (chamadas VPN)</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-327"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-328">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-328">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-329">Número total de chamadas que usaram uma conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="bb017-329">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-330"><strong>Volume de chamadas (chamadas externas)</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-330"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-331">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-331">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-332">Número de chamadas que usaram uma conexão externa (ou seja, uma conexão fora da rede interna).</span><span class="sxs-lookup"><span data-stu-id="bb017-332">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-333"><strong>Tremulação (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-333"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-334">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-334">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-335">Tremulação média detectada entre chegadas de pacote RTP.</span><span class="sxs-lookup"><span data-stu-id="bb017-335">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="bb017-336">(Tremulação é uma medida do &quot; shakiness &quot; de uma chamada.) Os valores de variação alta geralmente são causados por congestionamento ou um servidor de mídia sobrecarregado, resultando em áudio distorcido ou perdido.</span><span class="sxs-lookup"><span data-stu-id="bb017-336">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-337"><strong>Unidirecional relativo médio</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-337"><strong>Avg. relative one way</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-338">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-338">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-p132">Atraso unidirecional relativo médio entre dois pontos de extremidade de mídia. Esta é uma medida de latência de salto único.</span><span class="sxs-lookup"><span data-stu-id="bb017-p132">Average relative one-way delay between two media endpoints. This is a single-hop latency measure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb017-341"><strong>Latência média de processamento lado a lado RDP</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-341"><strong>Avg. RDP tile processing latency</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-342">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-342">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-p133">A latência média de processamento lado a lado RDP no Servidor de Conferência AS durante a sessão de visualização. Essa métrica não cobre a latência de rede. Uma média alta reflete um atraso maior na experiência de visualização. Um servidor de conferência sobrecarregado pode enfrentar atrasos médios maiores.</span><span class="sxs-lookup"><span data-stu-id="bb017-p133">The average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session. This metric does not cover network latency. A high average reflects a longer delay in the viewing experience. An overloaded conferencing server may experience higher average delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb017-347"><strong>% total de lado a lado estragado</strong></span><span class="sxs-lookup"><span data-stu-id="bb017-347"><strong>Total spoiled tile %</strong></span></span></p></td>
<td><p><span data-ttu-id="bb017-348">Não</span><span class="sxs-lookup"><span data-stu-id="bb017-348">No</span></span></p></td>
<td><p><span data-ttu-id="bb017-349">A porcentagem total de lado a lado estragados.</span><span class="sxs-lookup"><span data-stu-id="bb017-349">Total percentage of spoiled RDP tiles.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bb017-350">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bb017-350">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

