---
title: 'Lync Server 2013: relatório de atividade de conferência'
description: 'Lync Server 2013: relatório de atividade da conferência.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Activity Report
ms:assetid: 22ddb509-af16-4fc8-9b98-6f58caa6f37e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558627(v=OCS.15)
ms:contentKeyID: 48183618
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b7a2b23a08970defaec62b98d075ad1167527fd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434542"
---
# <a name="conference-activity-report-in-lync-server-2013"></a><span data-ttu-id="3906f-103">Relatório de atividade de conferências no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3906f-103">Conference Activity Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3906f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3906f-104">

<span> </span></span></span>

<span data-ttu-id="3906f-105">_**Tópico da última modificação:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="3906f-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="3906f-106">O Relatório de Atividade de Conferência torna fácil responder perguntas como estas: quantas conferências estão sendo realizadas diariamente e quando estas conferências são realizadas?</span><span class="sxs-lookup"><span data-stu-id="3906f-106">The Conference Activity Report makes it easy for you to answer questions like these: how many conferences are being held each day, and when are those conferences being held?</span></span> <span data-ttu-id="3906f-107">Informações como estas são úteis não apenas em seu próprio direito, mas também como uma ferramenta de resolução de problemas.</span><span class="sxs-lookup"><span data-stu-id="3906f-107">Information like this is useful not only in its own right, but also as a troubleshooting tool.</span></span> <span data-ttu-id="3906f-108">Por exemplo, vamos supor que os usuários estão reclamando que a rede parece particularmente lenta no meio do dia.</span><span class="sxs-lookup"><span data-stu-id="3906f-108">For example, suppose users are complaining that the network seems particularly slow in the middle of the day.</span></span> <span data-ttu-id="3906f-109">Uma rápida descrição dos relatórios de atividade de conferência pode sugerir um possível motivo: muito mais conferências estão sendo agendadas entre as horas de 10:00 AM e 2:00 PM em qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="3906f-109">A quick glance at the Conference Activity reports might suggest one possible reason: far more conferences are being scheduled between the hours of 10:00 AM and 2:00 PM then at any other time.</span></span>

<span data-ttu-id="3906f-110">Se a rede lenta está causando problemas, é possível incentivar os usuários a reprogramar algumas de suas conferências durante horários com menos tráfego durante o dia.</span><span class="sxs-lookup"><span data-stu-id="3906f-110">If the slow network is causing problems, you can encourage users to reschedule some of their conferences during the less-heavily trafficked times of the day.</span></span>

<div>

## <a name="accessing-the-conference-activity-report"></a><span data-ttu-id="3906f-111">Acessando o Relatório de Atividade da Conferência</span><span class="sxs-lookup"><span data-stu-id="3906f-111">Accessing the Conference Activity Report</span></span>

<span data-ttu-id="3906f-112">O relatório atividade de conferência é acessado do [relatório Resumo de conferências no Lync Server 2013](lync-server-2013-conference-summary-report.md) clicando em uma das seguintes métricas:</span><span class="sxs-lookup"><span data-stu-id="3906f-112">The Conference Activity Report is accessed from the [Conference Summary Report in Lync Server 2013](lync-server-2013-conference-summary-report.md) by clicking either one of the following metrics:</span></span>

  - <span data-ttu-id="3906f-113">Total de conferências</span><span class="sxs-lookup"><span data-stu-id="3906f-113">Total conferences</span></span>

  - <span data-ttu-id="3906f-114">Total de participantes</span><span class="sxs-lookup"><span data-stu-id="3906f-114">Total participants</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-conference-activity-report"></a><span data-ttu-id="3906f-115">Fazendo o melhor uso do Relatório de Atividade de Conferência</span><span class="sxs-lookup"><span data-stu-id="3906f-115">Making the Best Use of the Conference Activity Report</span></span>

<span data-ttu-id="3906f-p102">Por padrão, o Relatório de Atividade de Conferência mostra o número total de conferências para um determinado período de tempo (por exemplo, o número total de conferências por dia ou o número total de conferências por hora do dia). No entanto, é possível escolher exibir o número total de participantes neste período de tempo ou o número total de participantes em minutos. Para fazer isso, clique no botão Exibir/Ocultar parâmetros para exibir as opções de filtragem e selecione um dos seguintes na lista suspensa Relatar por:</span><span class="sxs-lookup"><span data-stu-id="3906f-p102">By default the Conference Activity Report shows you the total number of conferences for the specified time period (for example, the total number of conferences per day, or the total number of conferences per hour of the day). However, you can also choose to display the total number of participants for that time period or the total number of participant minutes. To do that, click the Show/Hide Parameters button to display the filtering options, and then select one of the following from the Report by dropdown list:</span></span>

  - <span data-ttu-id="3906f-119">Contagem de participantes</span><span class="sxs-lookup"><span data-stu-id="3906f-119">Participant count</span></span>

  - <span data-ttu-id="3906f-120">Minutos dos participantes</span><span class="sxs-lookup"><span data-stu-id="3906f-120">Participant minutes</span></span>

  - <span data-ttu-id="3906f-121">Contagem de conferência</span><span class="sxs-lookup"><span data-stu-id="3906f-121">Conference count</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="3906f-122">Filtros</span><span class="sxs-lookup"><span data-stu-id="3906f-122">Filters</span></span>

<span data-ttu-id="3906f-p103">Os filtros fornecem uma maneira de retornar um conjunto de dados mais direcionadas ou para exibir os dados retornados de diferentes maneiras. A tabela a seguir lista os filtros que você pode usar com o Relatório de Atividades de Conferência.</span><span class="sxs-lookup"><span data-stu-id="3906f-p103">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Conference Activity Report.</span></span>

### <a name="conference-activity-report-filters"></a><span data-ttu-id="3906f-125">Filtros de relatório de atividade de conferência</span><span class="sxs-lookup"><span data-stu-id="3906f-125">Conference Activity Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3906f-126">Nome</span><span class="sxs-lookup"><span data-stu-id="3906f-126">Name</span></span></th>
<th><span data-ttu-id="3906f-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="3906f-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3906f-128"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="3906f-128"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="3906f-p104">Data/hora de início para o intervalo de tempo. Para ver os dados por horas, insira a data e hora de início conforme segue:</span><span class="sxs-lookup"><span data-stu-id="3906f-p104">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="3906f-131">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="3906f-131">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="3906f-p105">Se você não inserir a hora de início, o relatório começará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="3906f-p105">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="3906f-134">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="3906f-134">7/7/2012</span></span></p>
<p><span data-ttu-id="3906f-135">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="3906f-135">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="3906f-136">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="3906f-136">7/3/2012</span></span></p>
<p><span data-ttu-id="3906f-137">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="3906f-137">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3906f-138"><strong>Até</strong></span><span class="sxs-lookup"><span data-stu-id="3906f-138"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="3906f-p106">Data/hora final de intervalo de tempo. Para ver os dados por horas, insira a data e hora final conforme segue:</span><span class="sxs-lookup"><span data-stu-id="3906f-p106">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="3906f-141">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="3906f-141">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="3906f-p107">Se você não inserir a hora final, o relatório terminará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="3906f-p107">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="3906f-144">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="3906f-144">7/7/2012</span></span></p>
<p><span data-ttu-id="3906f-145">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="3906f-145">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="3906f-146">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="3906f-146">7/3/2012</span></span></p>
<p><span data-ttu-id="3906f-147">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="3906f-147">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3906f-148"><strong>Intervalo</strong></span><span class="sxs-lookup"><span data-stu-id="3906f-148"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="3906f-p108">Intervalo de tempo. Selecione qualquer um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="3906f-p108">Time interval. Select any of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="3906f-151">Por hora (é possível exibir no máximo 25 horas)</span><span class="sxs-lookup"><span data-stu-id="3906f-151">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="3906f-152">Diariamente (é possível exibir no máximo 31 dias)</span><span class="sxs-lookup"><span data-stu-id="3906f-152">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="3906f-153">Semanalmente (é possível exibir no máximo 12 semanas)</span><span class="sxs-lookup"><span data-stu-id="3906f-153">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="3906f-154">Mensalmente (é possível exibir no máximo 12 meses)</span><span class="sxs-lookup"><span data-stu-id="3906f-154">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="3906f-155">Se as datas de início e término excederem o número máximo de valores permitidos para o intervalo selecionado, somente o número máximo de valores (a partir da data de início) será exibido.</span><span class="sxs-lookup"><span data-stu-id="3906f-155">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="3906f-156">Por exemplo, se você selecionar o intervalo diário com uma data de início de 7/7/2012 e uma data de término de 2/28/2012, os dados serão exibidos para os dias 8/7/2012 12:00 AM a 9/7/2012 12:00 AM (ou seja, um total de 31 dias da importância dos dados).</span><span class="sxs-lookup"><span data-stu-id="3906f-156">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3906f-157"><strong>Relatar por</strong></span><span class="sxs-lookup"><span data-stu-id="3906f-157"><strong>Report by</strong></span></span></p></td>
<td><p><span data-ttu-id="3906f-p110">Indica os valores a serem usados no relatório. Você pode selecionar um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="3906f-p110">Indicates the values to be used in the report. You can select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="3906f-160">Contagem de participantes</span><span class="sxs-lookup"><span data-stu-id="3906f-160">Participant Count</span></span></p></li>
<li><p><span data-ttu-id="3906f-161">Minutos dos participantes</span><span class="sxs-lookup"><span data-stu-id="3906f-161">Participant Minutes</span></span></p></li>
<li><p><span data-ttu-id="3906f-162">Contagem de conferência</span><span class="sxs-lookup"><span data-stu-id="3906f-162">Conference Count</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferences-by-pool"></a><span data-ttu-id="3906f-163">Métricas para conferências por pool</span><span class="sxs-lookup"><span data-stu-id="3906f-163">Metrics for Conferences by Pool</span></span>

<span data-ttu-id="3906f-164">A tabela a seguir lista as informações no Relatório de Atividade de Conferência para cada pool.</span><span class="sxs-lookup"><span data-stu-id="3906f-164">The following table lists the information in the Conference Activity Report for each pool.</span></span>

### <a name="metrics-for-conferences-by-pool"></a><span data-ttu-id="3906f-165">Métricas para conferências por pool</span><span class="sxs-lookup"><span data-stu-id="3906f-165">Metrics for Conferences by Pool</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3906f-166">Nome</span><span class="sxs-lookup"><span data-stu-id="3906f-166">Name</span></span></th>
<th><span data-ttu-id="3906f-167">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="3906f-167">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="3906f-168">Descrição</span><span class="sxs-lookup"><span data-stu-id="3906f-168">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3906f-169"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="3906f-169"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="3906f-170">Não</span><span class="sxs-lookup"><span data-stu-id="3906f-170">No</span></span></p></td>
<td><p><span data-ttu-id="3906f-171">Nome do pool do Registrador ou Servidor de Borda usado na conferência.</span><span class="sxs-lookup"><span data-stu-id="3906f-171">Name of the Registrar pool or Edge Server used in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3906f-172"><strong>Data/Hora</strong></span><span class="sxs-lookup"><span data-stu-id="3906f-172"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="3906f-173">Não</span><span class="sxs-lookup"><span data-stu-id="3906f-173">No</span></span></p></td>
<td><p><span data-ttu-id="3906f-174">Data e hora de quando a conferência foi realizada.</span><span class="sxs-lookup"><span data-stu-id="3906f-174">Date and time when the conference was held.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3906f-175"><strong>Total</strong></span><span class="sxs-lookup"><span data-stu-id="3906f-175"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="3906f-176">Não</span><span class="sxs-lookup"><span data-stu-id="3906f-176">No</span></span></p></td>
<td><p><span data-ttu-id="3906f-177">Contagem total de participantes, minutos totais de participantes ou contagem total da conferência.</span><span class="sxs-lookup"><span data-stu-id="3906f-177">Total participant count, total participant minutes, or total conference count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferences-by-server-type"></a><span data-ttu-id="3906f-178">Métricas para conferência por tipo de servidor</span><span class="sxs-lookup"><span data-stu-id="3906f-178">Metrics for Conferences by Server Type</span></span>

<span data-ttu-id="3906f-179">A tabela a seguir lista as informações no relatório de atividade de conferência para cada tipo de servidor.</span><span class="sxs-lookup"><span data-stu-id="3906f-179">The following table lists the information in the Conference Activity Report for each type of server.</span></span>

### <a name="metrics-for-conferences-by-server-type"></a><span data-ttu-id="3906f-180">Métricas para conferência por tipo de servidor</span><span class="sxs-lookup"><span data-stu-id="3906f-180">Metrics for Conferences by Server Type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3906f-181">Nome</span><span class="sxs-lookup"><span data-stu-id="3906f-181">Name</span></span></th>
<th><span data-ttu-id="3906f-182">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="3906f-182">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="3906f-183">Descrição</span><span class="sxs-lookup"><span data-stu-id="3906f-183">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3906f-184"><strong>Tipo de servidor de conferência</strong></span><span class="sxs-lookup"><span data-stu-id="3906f-184"><strong>Conferencing server type</strong></span></span></p></td>
<td><p><span data-ttu-id="3906f-185">Não</span><span class="sxs-lookup"><span data-stu-id="3906f-185">No</span></span></p></td>
<td><p><span data-ttu-id="3906f-186">Tipo de servidor usado na conferência, geralmente um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="3906f-186">Type of server used in the conference, typically one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="3906f-187">Servidor de conferência da Web</span><span class="sxs-lookup"><span data-stu-id="3906f-187">Web Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="3906f-188">Servidor de conferência de IM</span><span class="sxs-lookup"><span data-stu-id="3906f-188">IM Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="3906f-189">Servidor de conferência com telefonia</span><span class="sxs-lookup"><span data-stu-id="3906f-189">Telephony Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="3906f-190">Servidor de conferência de AV</span><span class="sxs-lookup"><span data-stu-id="3906f-190">AV Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="3906f-191">Compartilhamento de Aplicativos</span><span class="sxs-lookup"><span data-stu-id="3906f-191">Application Sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3906f-192"><strong>Data/Hora</strong></span><span class="sxs-lookup"><span data-stu-id="3906f-192"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="3906f-193">Não</span><span class="sxs-lookup"><span data-stu-id="3906f-193">No</span></span></p></td>
<td><p><span data-ttu-id="3906f-194">Data e hora de quando a conferência foi realizada.</span><span class="sxs-lookup"><span data-stu-id="3906f-194">Date and time when the conference was held.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3906f-195"><strong>Total</strong></span><span class="sxs-lookup"><span data-stu-id="3906f-195"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="3906f-196">Não</span><span class="sxs-lookup"><span data-stu-id="3906f-196">No</span></span></p></td>
<td><p><span data-ttu-id="3906f-197">Contagem total de participantes, minutos totais de participantes ou contagem total da conferência.</span><span class="sxs-lookup"><span data-stu-id="3906f-197">Total participant count, total participant minutes, or total conference count.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3906f-198">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3906f-198">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

