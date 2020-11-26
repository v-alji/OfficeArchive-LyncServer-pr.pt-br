---
title: 'Lync Server 2013: relatório de diagnóstico de conferência'
description: 'Lync Server 2013: relatório de diagnóstico de conferência.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Diagnostic Report
ms:assetid: e9edc23c-8ce8-4ab8-8786-9d22e1e51e14
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615042(v=OCS.15)
ms:contentKeyID: 48185901
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9d3ef3c78bc2145d907d5a40e1aed95a2f4cb4c4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434540"
---
# <a name="conference-diagnostic-report-in-lync-server-2013"></a><span data-ttu-id="d0d52-103">Relatório de diagnóstico de conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0d52-103">Conference Diagnostic Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d0d52-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d0d52-104">

<span> </span></span></span>

<span data-ttu-id="d0d52-105">_**Tópico da última modificação:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="d0d52-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="d0d52-106">O Relatório de Diagnóstico de Conferência oferece informações sobre o êxito e a falha de todas as sessões de conferência.</span><span class="sxs-lookup"><span data-stu-id="d0d52-106">The Conference Diagnostic Report provides information about the success and failure of all conferencing sessions.</span></span> <span data-ttu-id="d0d52-107">Observe que o Microsoft Lync Server distingue entre os diferentes tipos de falha:</span><span class="sxs-lookup"><span data-stu-id="d0d52-107">Note that Microsoft Lync Server distinguishes between different kinds of failure:</span></span>

  - <span data-ttu-id="d0d52-p102">**Falha esperada**. Uma falha esperada normalmente é uma falha apenas no sentido mais técnico. Por exemplo, suponhamos que alguém inicie uma conferência, mas desligue antes que alguém possa ingressar. Tecnicamente, é uma falha: a conferência foi iniciada, mas não foi concluída. No entanto, essa é uma falha que você poderia esperar que acontecesse: se o organizador cancela a conferência antes que alguém possa ingressar, não se poderia esperar que essa conferência fosse concluída.</span><span class="sxs-lookup"><span data-stu-id="d0d52-p102">**Expected failure**. An expected failure is typically a failure only in the most technical sense. For example, suppose someone starts a conference but hangs up before anyone can join. Technically that's a failure: the conference was initiated, but not completed. However, that's a failure that you would expect to happen: if the organizer cancels the conference before anyone can join then you would not expect that conference to be completed.</span></span>

  - <span data-ttu-id="d0d52-p103">**Falha inesperada**. Uma falha inesperada é exatamente o que o nome diz: um erro que, baseado nas circunstâncias, você não esperaria que ocorresse. Por exemplo, suponhamos que uma conferência não tenha acontecido porque a política de reunião do organizador não pôde ser recuperada. Isso é um erro inesperado: afinal, sempre deve ser possível recuperar a política de reunião de um usuário.</span><span class="sxs-lookup"><span data-stu-id="d0d52-p103">**Unexpected failure**. An unexpected error is exactly what the name implies: an error that, based on the circumstances, you would not expect to occur. For example, suppose a conference could not be held because the organizer's meeting policy could not be retrieved. That's an unexpected error: after all, you should always be able to retrieve a user's meeting policy.</span></span>

<span data-ttu-id="d0d52-p104">Observe que a soma das métricas de Êxitos, Falhas esperadas e Falhas inesperadas podem não resultar na métrica de Total de sessões. Por exemplo, você pode ver os seguintes valores no Relatório:</span><span class="sxs-lookup"><span data-stu-id="d0d52-p104">Note that the Success, Expected failure, and Unexpected failure metrics might not add up to the Total sessions metric. For example, you might see the following values in the Report:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d0d52-119">Êxitos</span><span class="sxs-lookup"><span data-stu-id="d0d52-119">Successes</span></span></th>
<th><span data-ttu-id="d0d52-120">Falhas esperadas</span><span class="sxs-lookup"><span data-stu-id="d0d52-120">Expected failures</span></span></th>
<th><span data-ttu-id="d0d52-121">Falhas inesperadas</span><span class="sxs-lookup"><span data-stu-id="d0d52-121">Unexpected failures</span></span></th>
<th><span data-ttu-id="d0d52-122">Total de sessões</span><span class="sxs-lookup"><span data-stu-id="d0d52-122">Total sessions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0d52-123">2024</span><span class="sxs-lookup"><span data-stu-id="d0d52-123">2024</span></span></p></td>
<td><p><span data-ttu-id="d0d52-124">469</span><span class="sxs-lookup"><span data-stu-id="d0d52-124">469</span></span></p></td>
<td><p><span data-ttu-id="d0d52-125">16</span><span class="sxs-lookup"><span data-stu-id="d0d52-125">16</span></span></p></td>
<td><p><span data-ttu-id="d0d52-126">2521</span><span class="sxs-lookup"><span data-stu-id="d0d52-126">2521</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d0d52-127">Somando 2024 + 469 + 16, você obtém um total de 2.509 sessões e, no entanto, a coluna de Total de sessões mostra um total de 2.521 sessões.</span><span class="sxs-lookup"><span data-stu-id="d0d52-127">If you add 2024 + 469 + 16 you get a total of 2,509 sessions and yet, the Total sessions column shows a total of 2,521 sessions.</span></span> <span data-ttu-id="d0d52-128">As 12 sessões que estão "faltando" são sessões que o sistema não conseguiu categorizar como êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="d0d52-128">The "missing" 12 sessions for are sessions that the system was unable to categorize as successful or unsuccessful.</span></span> <span data-ttu-id="d0d52-129">Isso, às vezes, é o caso quando um produto de terceiros introduz um novo código de diagnóstico desconhecido para monitorar o servidor.</span><span class="sxs-lookup"><span data-stu-id="d0d52-129">That will sometimes be the case when a third-party product introduces a new diagnostic code that is unfamiliar to Monitoring Server.</span></span> <span data-ttu-id="d0d52-130">Quando isso acontece, as chamadas efetuadas com o produto e o relatório desse código de diagnóstico nem sempre podem ser categorizados como Êxito, Falha esperada ou Falha inesperada.</span><span class="sxs-lookup"><span data-stu-id="d0d52-130">When that happens, calls made using that product, and reporting that diagnostic code, cannot always be categorized as being a Success, an Expected failure, or an Unexpected failure.</span></span>

<div>

## <a name="accessing-the-conference-diagnostic-report"></a><span data-ttu-id="d0d52-131">Acessando o Relatório de Diagnóstico de Conferência</span><span class="sxs-lookup"><span data-stu-id="d0d52-131">Accessing the Conference Diagnostic Report</span></span>

<span data-ttu-id="d0d52-132">O Relatório de Diagnóstico de Conferência é acessado na página inicial de Relatórios de Monitoramento.</span><span class="sxs-lookup"><span data-stu-id="d0d52-132">The Conference Diagnostic Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="d0d52-133">Você pode acessar o [relatório de distribuição de falha no Lync Server 2013](lync-server-2013-failure-distribution-report.md) clicando em uma das seguintes métricas:</span><span class="sxs-lookup"><span data-stu-id="d0d52-133">You can access the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="d0d52-134">Volume de falhas inesperadas</span><span class="sxs-lookup"><span data-stu-id="d0d52-134">Unexpected failure volume</span></span>

  - <span data-ttu-id="d0d52-135">Volume de falha esperado</span><span class="sxs-lookup"><span data-stu-id="d0d52-135">Expected failure volume</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-conference-diagnostic-report"></a><span data-ttu-id="d0d52-136">Como usar o Relatório de Diagnóstico de Conferência da melhor maneira possível</span><span class="sxs-lookup"><span data-stu-id="d0d52-136">Making the Best Use of the Conference Diagnostic Report</span></span>

<span data-ttu-id="d0d52-137">O Relatório de Diagnóstico de Conferência inclui uma série de gráficos.</span><span class="sxs-lookup"><span data-stu-id="d0d52-137">The Conference Diagnostic Report includes a series of graphs.</span></span> <span data-ttu-id="d0d52-138">Cada uma das colunas exibidas no gráfico é, na verdade, um hiperlink.</span><span class="sxs-lookup"><span data-stu-id="d0d52-138">Each of the columns shown in the graph is actually a hyperlink.</span></span> <span data-ttu-id="d0d52-139">Se você clicar em uma coluna, fará uma busca detalhada no [relatório de distribuição de falha no Lync Server 2013](lync-server-2013-failure-distribution-report.md) para esse período de tempo e esse tipo de conferência.</span><span class="sxs-lookup"><span data-stu-id="d0d52-139">If you click a column, you'll drill down to the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md) for that time period and that conference type.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="d0d52-140">Filtros</span><span class="sxs-lookup"><span data-stu-id="d0d52-140">Filters</span></span>

<span data-ttu-id="d0d52-p108">Os filtros fornecem uma maneira de retornar um conjunto de dados mais direcionado ou de exibir os dados retornados de maneiras diferentes. Por exemplo, o Relatório de Diagnóstico de Conferência permite que você filtre coisas como o tipo de conferência que está sendo conduzida (por exemplo, uma conferência baseada em Foco) ou pelo Servidor de Borda usado na conferência. Também é possível escolher como os dados devem ser agrupados. Nesse caso, as conferências são agrupadas por hora, dia, semana ou mês.</span><span class="sxs-lookup"><span data-stu-id="d0d52-p108">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Conference Diagnostic Report enables you to filter on such things as the type of conference being conducted (for example, a Focus-based conference) or by the Edge Server used in the conference. You can also choose how data should be grouped. In this case, conferences are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="d0d52-145">A tabela a seguir lista os filtros que podem ser usados com o Relatório de Diagnóstico de Conferência.</span><span class="sxs-lookup"><span data-stu-id="d0d52-145">The following table lists the filters that you can use with the Conference Diagnostic Report.</span></span>

### <a name="conference-diagnostic-report-filters"></a><span data-ttu-id="d0d52-146">Filtros do Relatório de Diagnóstico de Conferência</span><span class="sxs-lookup"><span data-stu-id="d0d52-146">Conference Diagnostic Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d0d52-147">Nome</span><span class="sxs-lookup"><span data-stu-id="d0d52-147">Name</span></span></th>
<th><span data-ttu-id="d0d52-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0d52-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0d52-149"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="d0d52-149"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="d0d52-p109">Data/hora de início para o intervalo de tempo. Para ver os dados por horas, insira a data e hora de início conforme segue:</span><span class="sxs-lookup"><span data-stu-id="d0d52-p109">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="d0d52-152">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="d0d52-152">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="d0d52-p110">Se você não inserir a hora de início, o relatório começará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="d0d52-p110">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="d0d52-155">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="d0d52-155">7/7/2012</span></span></p>
<p><span data-ttu-id="d0d52-156">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="d0d52-156">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="d0d52-157">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="d0d52-157">7/3/2012</span></span></p>
<p><span data-ttu-id="d0d52-158">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="d0d52-158">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0d52-159"><strong>Até</strong></span><span class="sxs-lookup"><span data-stu-id="d0d52-159"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="d0d52-p111">Data/hora final de intervalo de tempo. Para ver os dados por horas, insira a data e hora final conforme segue:</span><span class="sxs-lookup"><span data-stu-id="d0d52-p111">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="d0d52-162">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="d0d52-162">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="d0d52-p112">Se você não inserir a hora final, o relatório terminará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="d0d52-p112">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="d0d52-165">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="d0d52-165">7/7/2012</span></span></p>
<p><span data-ttu-id="d0d52-166">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="d0d52-166">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="d0d52-167">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="d0d52-167">7/3/2012</span></span></p>
<p><span data-ttu-id="d0d52-168">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="d0d52-168">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0d52-169"><strong>Intervalo</strong></span><span class="sxs-lookup"><span data-stu-id="d0d52-169"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="d0d52-p113">Intervalo de tempo. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="d0d52-p113">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d0d52-172">Por hora (é possível exibir no máximo 25 horas)</span><span class="sxs-lookup"><span data-stu-id="d0d52-172">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="d0d52-173">Diariamente (é possível exibir no máximo 31 dias)</span><span class="sxs-lookup"><span data-stu-id="d0d52-173">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="d0d52-174">Semanalmente (é possível exibir no máximo 12 semanas)</span><span class="sxs-lookup"><span data-stu-id="d0d52-174">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="d0d52-175">Mensalmente (é possível exibir no máximo 12 meses)</span><span class="sxs-lookup"><span data-stu-id="d0d52-175">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="d0d52-176">Se as datas de início e término excederem o número máximo de valores permitidos para o intervalo selecionado, somente o número máximo de valores (a partir da data de início) será exibido.</span><span class="sxs-lookup"><span data-stu-id="d0d52-176">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="d0d52-177">Por exemplo, se você selecionar o intervalo diário com uma data de início de 7/7/2012 e uma data de término de 2/28/2012, os dados serão exibidos para os dias 8/7/2012 12:00 AM a 9/7/2012 12:00 AM (ou seja, um total de 31 dias da importância dos dados).</span><span class="sxs-lookup"><span data-stu-id="d0d52-177">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0d52-178"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="d0d52-178"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="d0d52-p115">FQDN (Nome de domínio totalmente qualificado) do pool de Registradores Avançados ou Servidores de Borda. Você pode selecionar um pool individual ou clicar em <strong>[Tudo]</strong> para ver os dados de todos os pools. Essa lista suspensa é automaticamente preenchida para você com base nos registros no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d0d52-p115">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0d52-182"><strong>Sessões de conferência</strong></span><span class="sxs-lookup"><span data-stu-id="d0d52-182"><strong>Conference sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="d0d52-p116">Indica o tipo de sessão de conferência. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="d0d52-p116">Indicates the type of conferencing session. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d0d52-185">[Todos]</span><span class="sxs-lookup"><span data-stu-id="d0d52-185">[All]</span></span></p></li>
<li><p><span data-ttu-id="d0d52-186">Sessões de foco</span><span class="sxs-lookup"><span data-stu-id="d0d52-186">Focus sessions</span></span></p></li>
<li><p><span data-ttu-id="d0d52-187">Todas as sessões MCU</span><span class="sxs-lookup"><span data-stu-id="d0d52-187">All MCU sessions</span></span></p></li>
<li><p><span data-ttu-id="d0d52-188">Conferência de IM</span><span class="sxs-lookup"><span data-stu-id="d0d52-188">IM conferencing</span></span></p></li>
<li><p><span data-ttu-id="d0d52-189">Compartilhamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="d0d52-189">Application sharing</span></span></p></li>
<li><p><span data-ttu-id="d0d52-190">Conferência de A/V</span><span class="sxs-lookup"><span data-stu-id="d0d52-190">A/V conferencing</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="d0d52-191">Métricas</span><span class="sxs-lookup"><span data-stu-id="d0d52-191">Metrics</span></span>

<span data-ttu-id="d0d52-192">A tabela a seguir lista as informações fornecidas no Relatório de Diagnóstico de Conferência para cada tipo de sessão de conferência.</span><span class="sxs-lookup"><span data-stu-id="d0d52-192">The following table lists the information provided in the Conference Diagnostic Report for each type of conferencing session.</span></span>

### <a name="conference-diagnostic-report-metrics"></a><span data-ttu-id="d0d52-193">Métricas do Relatório de Diagnóstico de Conferência</span><span class="sxs-lookup"><span data-stu-id="d0d52-193">Conference Diagnostic Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d0d52-194">Nome</span><span class="sxs-lookup"><span data-stu-id="d0d52-194">Name</span></span></th>
<th><span data-ttu-id="d0d52-195">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="d0d52-195">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="d0d52-196">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0d52-196">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0d52-197"><strong>Volume de sucesso</strong></span><span class="sxs-lookup"><span data-stu-id="d0d52-197"><strong>Success volume</strong></span></span></p></td>
<td><p><span data-ttu-id="d0d52-198">Não</span><span class="sxs-lookup"><span data-stu-id="d0d52-198">No</span></span></p></td>
<td><p><span data-ttu-id="d0d52-199">Número total de conferências bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="d0d52-199">Total number of successful conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0d52-200"><strong>Porcentagem de sucesso</strong></span><span class="sxs-lookup"><span data-stu-id="d0d52-200"><strong>Success percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="d0d52-201">Não</span><span class="sxs-lookup"><span data-stu-id="d0d52-201">No</span></span></p></td>
<td><p><span data-ttu-id="d0d52-p117">Percentual de conferências concluídas com problemas consideráveis. Calculado dividindo o Volume de sucesso pelo Total de sessões.</span><span class="sxs-lookup"><span data-stu-id="d0d52-p117">Percentage of conferences that completed with significant problems. Calculated by dividing the Success volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0d52-204"><strong>Volume de falha esperado</strong></span><span class="sxs-lookup"><span data-stu-id="d0d52-204"><strong>Expected failure volume</strong></span></span></p></td>
<td><p><span data-ttu-id="d0d52-205">Não</span><span class="sxs-lookup"><span data-stu-id="d0d52-205">No</span></span></p></td>
<td><p><span data-ttu-id="d0d52-206">Número total de conferências em que &quot; ocorreu uma falha esperada &quot; .</span><span class="sxs-lookup"><span data-stu-id="d0d52-206">Total number of conferences where an &quot;expected failure&quot; occurred.</span></span></p>
<p><span data-ttu-id="d0d52-p118">Uma falha esperada é quando se sabe que a falha ocorrerá. Por exemplo, se um usuário tiver definido seu status como Não perturbe, é esperado que qualquer chamada para esse usuário falhe.</span><span class="sxs-lookup"><span data-stu-id="d0d52-p118">An expected failure is a failure that is expected to happen. For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0d52-209"><strong>Percentual de falhas esperadas</strong></span><span class="sxs-lookup"><span data-stu-id="d0d52-209"><strong>Expected failure percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="d0d52-210">Não</span><span class="sxs-lookup"><span data-stu-id="d0d52-210">No</span></span></p></td>
<td><p><span data-ttu-id="d0d52-p119">Percentual de conferências que enfrentaram um erro esperado. Calculado pela divisão do Volume de falha esperado pelo Total de sessões.</span><span class="sxs-lookup"><span data-stu-id="d0d52-p119">Percentage of conferences that experienced an expected error. Calculated by dividing the Expected failure volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0d52-213"><strong>Volume de falha inesperado</strong></span><span class="sxs-lookup"><span data-stu-id="d0d52-213"><strong>Unexpected failure volume</strong></span></span></p></td>
<td><p><span data-ttu-id="d0d52-214">Não</span><span class="sxs-lookup"><span data-stu-id="d0d52-214">No</span></span></p></td>
<td><p><span data-ttu-id="d0d52-215">Número total de conferências em que &quot; ocorreu uma falha inesperada &quot; .</span><span class="sxs-lookup"><span data-stu-id="d0d52-215">Total number of conferences where an &quot;unexpected failure&quot; occurred.</span></span></p>
<p><span data-ttu-id="d0d52-p120">Uma falha inesperada é uma falha que ocorre no que aparenta ser um sistema íntegro. Por exemplo, uma chamada não deve ser encerrada se o chamador for colocado em espera. Se isso ocorrer, isso seria sinalizado como uma falha inesperada.</span><span class="sxs-lookup"><span data-stu-id="d0d52-p120">An unexpected failure is a failure that occurs in what would appear to be an otherwise healthy system. For example, a call should not be terminated if the caller is placed on hold. If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0d52-219"><strong>Percentual de falhas inesperadas</strong></span><span class="sxs-lookup"><span data-stu-id="d0d52-219"><strong>Unexpected failure percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="d0d52-220">Não</span><span class="sxs-lookup"><span data-stu-id="d0d52-220">No</span></span></p></td>
<td><p><span data-ttu-id="d0d52-p121">Percentual de conferências que enfrentaram um erro esperado. Calculado pela divisão do Volume de falha inesperado pelo Total de sessões.</span><span class="sxs-lookup"><span data-stu-id="d0d52-p121">Percentage of conferences that experienced an unexpected error. Calculated by dividing the Unexpected failure volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0d52-223"><strong>Total de sessões</strong></span><span class="sxs-lookup"><span data-stu-id="d0d52-223"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="d0d52-224">Não</span><span class="sxs-lookup"><span data-stu-id="d0d52-224">No</span></span></p></td>
<td><p><span data-ttu-id="d0d52-225">Número total de conferências, incluindo conferências bem-sucedidas, conferências com falha (falhas esperadas e inesperadas) e conferências não categorizadas.</span><span class="sxs-lookup"><span data-stu-id="d0d52-225">Total number of conferences, including successful conferences, failed conferences (both expected failures and unexpected failures), and uncategorized conferences.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d0d52-226">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d0d52-226">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

