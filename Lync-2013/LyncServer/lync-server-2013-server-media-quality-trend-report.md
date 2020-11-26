---
title: 'Lync Server 2013: relatório de tendências de qualidade de mídia do servidor'
description: 'Lync Server 2013: relatório de tendências de qualidade de mídia do servidor.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server Media Quality Trend Report
ms:assetid: 8a51fd13-1487-4632-b5ec-f7ae2abe8ed4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205071(v=OCS.15)
ms:contentKeyID: 48184760
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7ac2482b967aab230c5522c2b6a76e10ced28e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444895"
---
# <a name="server-media-quality-trend-report-in-lync-server-2013"></a><span data-ttu-id="0a8bf-103">Relatório de tendências de qualidade de mídia do servidor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0a8bf-103">Server Media Quality Trend Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0a8bf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0a8bf-104">

<span> </span></span></span>

<span data-ttu-id="0a8bf-105">_**Tópico da última modificação:** 2012-11-12_</span><span class="sxs-lookup"><span data-stu-id="0a8bf-105">_**Topic Last Modified:** 2012-11-12_</span></span>

<span data-ttu-id="0a8bf-106">O relatório de tendências de qualidade de mídia do servidor fornece uma maneira de comparar graficamente até cinco servidores com métricas de qualidade de experiência, como volume de chamadas, porcentagem de chamadas deficientes, perda de pacotes e Tremulação.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-106">The Server Media Quality Trend Report provides a way for you to graphically compare up to 5 servers on Quality of Experience metrics such as call volume, poor call percentage, packet loss, and jitter.</span></span> <span data-ttu-id="0a8bf-107">Ele facilita determinadas tarefas como identificar servidores com desempenho ruim, subutilizados e superutilizados.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-107">This makes it easier to do such things as identify servers that are performing poorly, identify servers that are underutilized, or identify servers that are being overused.</span></span>

<div>

## <a name="accessing-the-server-media-quality-trend-report"></a><span data-ttu-id="0a8bf-108">Acessando o Relatório de Tendências de Qualidade de Mídia do Servidor</span><span class="sxs-lookup"><span data-stu-id="0a8bf-108">Accessing the Server Media Quality Trend Report</span></span>

<span data-ttu-id="0a8bf-109">O Relatório de Tendências de Qualidade de Mídia do Servidor pode ser acessado por um destes relatórios:</span><span class="sxs-lookup"><span data-stu-id="0a8bf-109">The Server Media Quality Trend Report can be accessed from either one of the following report:</span></span>

  - <span data-ttu-id="0a8bf-110">[Relatório de desempenho do servidor no Lync Server 2013](lync-server-2013-server-performance-report.md) (clicando na métrica de tendência)</span><span class="sxs-lookup"><span data-stu-id="0a8bf-110">[Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md) (by clicking the Trend metric)</span></span>

  - <span data-ttu-id="0a8bf-111">[Relatório de detalhes de chamadas no Lync Server 2013](lync-server-2013-call-detail-report.md) (clicando na métrica de servidor de borda a/V.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-111">[Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md) (by clicking the A/V edge server metric.</span></span> <span data-ttu-id="0a8bf-112">Se o chamador ou o receptor for um servidor, você também poderá acessar o relatório de tendências de mídia de qualidade do servidor clicando no nome do ponto de extremidade.)</span><span class="sxs-lookup"><span data-stu-id="0a8bf-112">If the caller or callee is a server, you can also reach the Server Quality Media Trend Report by clicking the endpoint name.)</span></span>

</div>

<div>

## <a name="making-the-best-use-of-server-media-quality-trend-report"></a><span data-ttu-id="0a8bf-113">Aproveitando ao máximo o Relatório de Tendências de Qualidade de Mídia do Servidor</span><span class="sxs-lookup"><span data-stu-id="0a8bf-113">Making the Best Use of Server Media Quality Trend Report</span></span>

<span data-ttu-id="0a8bf-114">Quando você clica na métrica de tendência no [relatório de desempenho do servidor no Lync Server 2013](lync-server-2013-server-performance-report.md) para um servidor específico, o relatório de tendências de qualidade de mídia do servidor será aberto.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-114">When you click the Trend metric on the [Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md) for a specific server, the Server Media Quality Trend Report will open.</span></span> <span data-ttu-id="0a8bf-115">No entanto, você verá uma instância em branco do relatório; o servidor selecionado no Relatório de Desempenho do Servidor não será exibido na tela.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-115">However, you will see only a blank instance of that report; the server you selected on the Server Performance Report will not be displayed onscreen.</span></span> <span data-ttu-id="0a8bf-116">Será necessário selecionar o servidor em questão no menu suspenso "Servidores".</span><span class="sxs-lookup"><span data-stu-id="0a8bf-116">Instead, you will need to select that server from the Servers dropdown.</span></span> <span data-ttu-id="0a8bf-117">O menu suspenso "Servidores" apresenta também a opção "Selecionar tudo".</span><span class="sxs-lookup"><span data-stu-id="0a8bf-117">Note, too that the Servers dropdown includes a Select All option.</span></span> <span data-ttu-id="0a8bf-118">Essa opção não funcionará caso haja mais de cinco servidores; o relatório de tendências de qualidade de mídia do servidor só pode exibir dados para, no máximo, cinco servidores por vez.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-118">This option will not work if you have more than 5 servers; the Server Media Quality Trend Report can only display data for a maximum of 5 servers at a time.</span></span>

<span data-ttu-id="0a8bf-119">Nos gráficos exibidos pelo relatório de tendências de qualidade de mídia do servidor, os pontos com o rótulo de chamadas e a porcentagem de chamada baixa são hotlinks; clicar em um ponto no gráfico abrirá uma instância do [relatório de lista de chamadas no Lync Server 2013](lync-server-2013-call-list-report.md) mostrando o total de chamadas (ou chamadas ruins) pelo período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-119">On the graphs displayed by the Server Media Quality Trend Report, the points labeled Call Volume and Poor Call Percentage are hotlinks; clicking a point on the graph will open an instance of the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) showing the total calls (or poor calls) for the specified time period.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="0a8bf-120">Filtros</span><span class="sxs-lookup"><span data-stu-id="0a8bf-120">Filters</span></span>

<span data-ttu-id="0a8bf-p104">Os filtros são uma forma de obter dados mais direcionados ou visualizar os dados obtidos de diferentes maneiras. A tabela a seguir relaciona os filtros que podem ser usados no relatório de tendências de qualidade de mídia do servidor.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Server Media Quality Trend Report.</span></span>

### <a name="server-media-quality-trend-report-filters"></a><span data-ttu-id="0a8bf-123">Filtros do Relatório de Tendências de Qualidade de Mídia do Servidor</span><span class="sxs-lookup"><span data-stu-id="0a8bf-123">Server Media Quality Trend Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a8bf-124">Nome</span><span class="sxs-lookup"><span data-stu-id="0a8bf-124">Name</span></span></th>
<th><span data-ttu-id="0a8bf-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a8bf-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a8bf-126"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-126"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-p105">Data/hora de início para o intervalo de tempo. Para ver os dados por horas, insira a data e hora de início conforme segue:</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="0a8bf-129">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="0a8bf-129">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="0a8bf-p106">Se você não inserir a hora de início, o relatório começará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="0a8bf-132">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="0a8bf-132">7/7/2012</span></span></p>
<p><span data-ttu-id="0a8bf-133">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="0a8bf-133">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="0a8bf-134">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="0a8bf-134">7/3/2012</span></span></p>
<p><span data-ttu-id="0a8bf-135">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-135">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8bf-136"><strong>Até</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-136"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-p107">Data/hora final de intervalo de tempo. Para ver os dados por horas, insira a data e hora final conforme segue:</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="0a8bf-139">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="0a8bf-139">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="0a8bf-p108">Se você não inserir a hora final, o relatório terminará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="0a8bf-142">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="0a8bf-142">7/7/2012</span></span></p>
<p><span data-ttu-id="0a8bf-143">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="0a8bf-143">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="0a8bf-144">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="0a8bf-144">7/3/2012</span></span></p>
<p><span data-ttu-id="0a8bf-145">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-145">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a8bf-146"><strong>Intervalo</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-146"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-p109">Intervalo de tempo. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p109">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="0a8bf-149">Por hora (é possível exibir no máximo 25 horas)</span><span class="sxs-lookup"><span data-stu-id="0a8bf-149">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="0a8bf-150">Diariamente (é possível exibir no máximo 31 dias)</span><span class="sxs-lookup"><span data-stu-id="0a8bf-150">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="0a8bf-151">Semanalmente (é possível exibir no máximo 12 semanas)</span><span class="sxs-lookup"><span data-stu-id="0a8bf-151">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="0a8bf-152">Se as datas de início e término excederem o número máximo de valores permitidos para o intervalo selecionado, somente o número máximo de valores (a partir da data de início) será exibido.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-152">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="0a8bf-153">Por exemplo, se você selecionar o intervalo diário com uma data de início de 8/7/2012 e uma data de término de 9/28/2012, os dados serão exibidos para os dias 8/7/2012 12:00 AM a 9/7/2012 12:00 AM (ou seja, um total de 31 dias da importância dos dados).</span><span class="sxs-lookup"><span data-stu-id="0a8bf-153">For example, if you select the Daily interval with a start date of 8/7/2012 and an end date of 9/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8bf-154"><strong>Tipo de Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-154"><strong>Server type</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-p111">Tipo de servidor envolvido na chamada. Os valores permitidos são</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p111">Type of server involved in the call. Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="0a8bf-157">Servidor de Mediação</span><span class="sxs-lookup"><span data-stu-id="0a8bf-157">Mediation Server</span></span></p></li>
<li><p><span data-ttu-id="0a8bf-158">Servidor de Conferência A/V</span><span class="sxs-lookup"><span data-stu-id="0a8bf-158">A/V Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="0a8bf-159">Servidor de Borda A/V</span><span class="sxs-lookup"><span data-stu-id="0a8bf-159">A/V Edge Server</span></span></p></li>
<li><p><span data-ttu-id="0a8bf-160">Gateway (Servidor de Mediação)</span><span class="sxs-lookup"><span data-stu-id="0a8bf-160">Gateway (Mediation Server)</span></span></p></li>
<li><p><span data-ttu-id="0a8bf-161">Gateway (Bypass do servidor de mediação)</span><span class="sxs-lookup"><span data-stu-id="0a8bf-161">Gateway (Mediation Server Bypass)</span></span></p></li>
<li><p><span data-ttu-id="0a8bf-162">Servidor de conferência AS</span><span class="sxs-lookup"><span data-stu-id="0a8bf-162">AS Conferencing Server</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a8bf-163"><strong>Servidores</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-163"><strong>Servers</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-p112">Nome do servidor envolvido na sessão; essa lista suspensa é preenchida automaticamente com base no valor do filtro de tipo de arquivo. É possível selecionar até cinco servidores diferentes ao compilar o relatório.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p112">Name of the server involved in the session; this dropdown list is automatically populated for you based on the value of the Server type filter. You can select up to 5 different servers when compiling a report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8bf-166"><strong>Tipo de acesso</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-166"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-p113">Indica se o participante fez logon a partir da rede interna ou de uma rede externa. Os valores permitidos são:</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p113">Indicates whether the participant was logged on to the internal network or from the external network. Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="0a8bf-169">[Todos]</span><span class="sxs-lookup"><span data-stu-id="0a8bf-169">[All]</span></span></p></li>
<li><p><span data-ttu-id="0a8bf-170">Interno</span><span class="sxs-lookup"><span data-stu-id="0a8bf-170">Internal</span></span></p></li>
<li><p><span data-ttu-id="0a8bf-171">Externo</span><span class="sxs-lookup"><span data-stu-id="0a8bf-171">External</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a8bf-172"><strong>Tipo de rede</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-172"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-p114">Indica o tipo de rede ao qual o participante estava conectado. Os valores permitidos são:</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p114">Indicates the type of network the participant was connected to. Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="0a8bf-175">[Todos]</span><span class="sxs-lookup"><span data-stu-id="0a8bf-175">[All]</span></span></p></li>
<li><p><span data-ttu-id="0a8bf-176">Com fio</span><span class="sxs-lookup"><span data-stu-id="0a8bf-176">Wired</span></span></p></li>
<li><p><span data-ttu-id="0a8bf-177">Sem fio</span><span class="sxs-lookup"><span data-stu-id="0a8bf-177">Wireless</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8bf-178"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-178"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-p115">Indica se o participante externos estava usando conexão VPN durante a sessão. Os valores permitidos são:</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p115">Indicates whether an external participant was using a virtual private network (VPN) connection during the session. Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="0a8bf-181">[Todos]</span><span class="sxs-lookup"><span data-stu-id="0a8bf-181">[All]</span></span></p></li>
<li><p><span data-ttu-id="0a8bf-182">VPN</span><span class="sxs-lookup"><span data-stu-id="0a8bf-182">VPN</span></span></p></li>
<li><p><span data-ttu-id="0a8bf-183">Não-VPN</span><span class="sxs-lookup"><span data-stu-id="0a8bf-183">Non-VPN</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="0a8bf-184">Métricas</span><span class="sxs-lookup"><span data-stu-id="0a8bf-184">Metrics</span></span>

<span data-ttu-id="0a8bf-185">A tabela a seguir lista as informações fornecidas no relatório de tendências de qualidade de mídia do servidor.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-185">The following table lists the information provided in the Server Media Quality Trend Report.</span></span>

### <a name="server-media-quality-trend-report-metrics"></a><span data-ttu-id="0a8bf-186">Métricas do relatório de tendências de qualidade de mídia do servidor</span><span class="sxs-lookup"><span data-stu-id="0a8bf-186">Server Media Quality Trend Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a8bf-187">Nome</span><span class="sxs-lookup"><span data-stu-id="0a8bf-187">Name</span></span></th>
<th><span data-ttu-id="0a8bf-188">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="0a8bf-188">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="0a8bf-189">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a8bf-189">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a8bf-190"><strong>Volume da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-190"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-191">Não</span><span class="sxs-lookup"><span data-stu-id="0a8bf-191">No</span></span></p></td>
<td><p><span data-ttu-id="0a8bf-192">Número total de chamadas.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-192">Total number of calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8bf-193"><strong>Degradação (MOS)</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-193"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-194">Não</span><span class="sxs-lookup"><span data-stu-id="0a8bf-194">No</span></span></p></td>
<td><p><span data-ttu-id="0a8bf-195">Valor médio de uma redução da opção MOS (média da opção) durante uma chamada.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-195">Average amount of MOS (mean option score) degradation experienced during a call.</span></span> <span data-ttu-id="0a8bf-196">Os valores de degradação podem variar de um baixo de 0,0 a um alto de 5,0; um valor de 0,5 ou menos representa uma degradação aceitável.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-196">Degradation values can range from a low of 0.0 to a high of 5.0; a value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="0a8bf-197">As pontuações médias de opinião costumava ser calculadas a partir da classificação da qualidade de uma chamada em uma escala de 1 a 5, feita pelos dos usuários.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-197">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="0a8bf-198">O Lync Server usa um conjunto de algoritmos para prever como os usuários teriam classificado uma chamada.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-198">Lync Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="0a8bf-p117">Valores altos de degradação podem ser causados por congestionamento, falta de largura de banda, congestionamento ou interferência na rede sem fio ou um servidor de mídia ou ponto de extremidade sobrecarregado. A alta degradação resulta em perda ou distorção de áudio.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p117">High degradation values can be caused by congestion; lack of bandwidth; wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a8bf-201"><strong>Porcentagem de chamadas ruins</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-201"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-202">Não</span><span class="sxs-lookup"><span data-stu-id="0a8bf-202">No</span></span></p></td>
<td><p><span data-ttu-id="0a8bf-p118">O número total de chamadas classificadas como ruins. Uma chamada ruim é qualquer chamada em que no mínimo uma das métricas excedeu o valor permitido (por exemplo, uma chamada com tremulação excessiva).</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p118">The total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8bf-205"><strong>Ida e volta (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-205"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-206">Não</span><span class="sxs-lookup"><span data-stu-id="0a8bf-206">No</span></span></p></td>
<td><p><span data-ttu-id="0a8bf-p119">Quantidade média de tempo (em milissegundos) exigida para que um pacote de protocolo RTP vá até um ponto de extremidade e retorne. Tempos de ida e volta de 200 milissegundos ou menos são considerados de qualidade aceitável.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p119">Average amount of time (in milliseconds) required for a Real-Time Transport Protocol packet to travel to one endpoint and then back. Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="0a8bf-p120">Altos valores de tempo de resposta podem ser causados por roteamento de chamadas internacionais, configuração incorreta de um roteamento ou um servidor de mídia sobrecarregado. Tempos de resposta altos resultam em dificuldades para conversas de áudio bidirecionais e em tempo real.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p120">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a8bf-211"><strong>Perda de pacote</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-211"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-212">Não</span><span class="sxs-lookup"><span data-stu-id="0a8bf-212">No</span></span></p></td>
<td><p><span data-ttu-id="0a8bf-p121">Taxa média de perda de pacotes de RTP (protocolo de transporte em tempo real). (A perda de pacotes ocorre quando pacotes de RTP, um protocolo usado para transmitir áudio e vídeo pela Internet, falha ao tentar alcançar seu destino). Altas taxas de perda geralmente são causadas por congestionamento, insuficiência da largura de banda, congestionamento ou interferência na rede sem fio ou um servidor de mídia sobrecarregado. A perda de pacotes normalmente resulta em distorção ou perda de áudio.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p121">Average rate of Real-Time Transport Protocol (RTP) packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8bf-216"><strong>Tremulação (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-216"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-217">Não</span><span class="sxs-lookup"><span data-stu-id="0a8bf-217">No</span></span></p></td>
<td><p><span data-ttu-id="0a8bf-218">Tremulação média detectada entre chegadas de pacote RTP.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-218">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="0a8bf-219">(Tremulação é uma medida do &quot; shakiness &quot; de uma chamada.) Os valores de variação alta geralmente são causados por congestionamento ou um servidor de mídia sobrecarregado, resultando em áudio distorcido ou perdido.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-219">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a8bf-220"><strong>Taxa de correção oculta</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-220"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-221">Não</span><span class="sxs-lookup"><span data-stu-id="0a8bf-221">No</span></span></p></td>
<td><p><span data-ttu-id="0a8bf-p123">Taxa média de amostras de áudio ocultas para o número total de amostras. (Uma amostra de áudio oculta é uma técnica usada para suavizar a transição abrupta que normalmente seria causada por pacotes de rede descartados.) Valores altos indicam níveis consideráveis de perda de ocultação aplicada causada por perda de pacote ou tremulação e resulta na perda ou distorção de áudio.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p123">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8bf-224"><strong>Taxa de correção estendida</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-224"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-225">Não</span><span class="sxs-lookup"><span data-stu-id="0a8bf-225">No</span></span></p></td>
<td><p><span data-ttu-id="0a8bf-p124">Taxa média de amostras de áudio estendidas para o número total de amostras. (Áudio estendido é o áudio que foi expandido a fim de ajudar a manter a qualidade da chamada quando um pacote de rede descartado é detectado.) Valores altos indicam níveis significativos de extensão de amostra causada por tremulação e resultam em um som robótico ou distorcido.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p124">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a8bf-228"><strong>Taxa de correção compactada</strong></span><span class="sxs-lookup"><span data-stu-id="0a8bf-228"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="0a8bf-229">Não</span><span class="sxs-lookup"><span data-stu-id="0a8bf-229">No</span></span></p></td>
<td><p><span data-ttu-id="0a8bf-p125">Taxa média de amostras de áudio compactadas para o número total de amostras. (Áudio compactado é o áudio que foi compactado para ajudar a manter a qualidade da chamada quando um pacote de rede descartado é detectado.) Valores altos podem indicar níveis consideráveis de compactação de amostra causada por tremulação e resultam em um som acelerado ou distorcido.</span><span class="sxs-lookup"><span data-stu-id="0a8bf-p125">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0a8bf-232">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0a8bf-232">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

