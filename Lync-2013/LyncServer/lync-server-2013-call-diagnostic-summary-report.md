---
title: 'Lync Server 2013: relatório de Resumo de diagnóstico de chamadas'
description: 'Lync Server 2013: relatório de Resumo de diagnóstico de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Diagnostic Summary Report
ms:assetid: 9091de56-13e6-440e-9353-f57c10c906fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615016(v=OCS.15)
ms:contentKeyID: 48184789
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b444a176c06974a9eb9827006e078c17b54047a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389721"
---
# <a name="call-diagnostic-summary-report-in-lync-server-2013"></a><span data-ttu-id="adf4d-103">Relatório de resumo do diagnóstico de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="adf4d-103">Call Diagnostic Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="adf4d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="adf4d-104">

<span> </span></span></span>

<span data-ttu-id="adf4d-105">_**Tópico da última modificação:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="adf4d-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="adf4d-p101">O Relatório de Resumo de Diagnóstico de Chamadas fornece uma visão geral de sessões peer-to-peer e de conferências que falharam. O relatório mostra a taxa de falha geral para os dois tipos de sessão, e detalha as informações de falha por tipo de modalidade de sessão:</span><span class="sxs-lookup"><span data-stu-id="adf4d-p101">The Call Diagnostic Summary Report provides an overall look at failed peer-to-peer and conferencing sessions. The report shows the overall failure rate for both types of sessions, and further breaks the failure information down by session modality type:</span></span>

  - <span data-ttu-id="adf4d-108">Mensagens instantâneas</span><span class="sxs-lookup"><span data-stu-id="adf4d-108">Instant messaging</span></span>

  - <span data-ttu-id="adf4d-109">Compartilhamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="adf4d-109">Application sharing</span></span>

  - <span data-ttu-id="adf4d-110">Transferência de arquivos</span><span class="sxs-lookup"><span data-stu-id="adf4d-110">File transfer</span></span>

  - <span data-ttu-id="adf4d-111">Áudio</span><span class="sxs-lookup"><span data-stu-id="adf4d-111">Audio</span></span>

  - <span data-ttu-id="adf4d-112">Vídeo</span><span class="sxs-lookup"><span data-stu-id="adf4d-112">Video</span></span>

<div>

## <a name="accessing-the-call-diagnostic-summary-report"></a><span data-ttu-id="adf4d-113">Como acessar o Relatório de resumo de diagnóstico de chamadas</span><span class="sxs-lookup"><span data-stu-id="adf4d-113">Accessing the Call Diagnostic Summary Report</span></span>

<span data-ttu-id="adf4d-114">O Relatório de resumo de diagnóstico de chamadas é acessado na página inicial dos Relatórios de Monitoramento.</span><span class="sxs-lookup"><span data-stu-id="adf4d-114">The Call Diagnostic Summary Report is accessed from the Monitoring Reports Home page.</span></span> <span data-ttu-id="adf4d-115">No relatório de resumo do diagnóstico de chamadas, você pode acessar o [relatório de diagnóstico de atividades ponto a ponto no Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md) clicando na métrica de taxa de falha na seção Resumo de sessão ponto a ponto do relatório.</span><span class="sxs-lookup"><span data-stu-id="adf4d-115">From the Call Diagnostic Summary Report you can access the [Peer-to-Peer Activity Diagnostic Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md) by clicking the Failure rate metric under the Peer-to-Peer Session Summary section of the report.</span></span> <span data-ttu-id="adf4d-116">Você também pode acessar o [relatório de diagnóstico de conferência no Lync Server 2013](lync-server-2013-conference-diagnostic-report.md) clicando em qualquer uma das seguintes métricas de conferência:</span><span class="sxs-lookup"><span data-stu-id="adf4d-116">You can also access the [Conference Diagnostic Report in Lync Server 2013](lync-server-2013-conference-diagnostic-report.md) by clicking any of the following conference metrics:</span></span>

  - <span data-ttu-id="adf4d-117">Taxa de falha de sessão geral</span><span class="sxs-lookup"><span data-stu-id="adf4d-117">Overall session failure rate</span></span>

  - <span data-ttu-id="adf4d-118">Taxa de falha de foco</span><span class="sxs-lookup"><span data-stu-id="adf4d-118">Focus failure rate</span></span>

  - <span data-ttu-id="adf4d-119">Taxa de falha de MCU</span><span class="sxs-lookup"><span data-stu-id="adf4d-119">MCU failure rate</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-diagnostic-summary-report"></a><span data-ttu-id="adf4d-120">Como usar melhor o Relatório de resumo de diagnóstico de chamadas</span><span class="sxs-lookup"><span data-stu-id="adf4d-120">Making the Best Use of the Call Diagnostic Summary Report</span></span>

<span data-ttu-id="adf4d-121">O relatório de resumo do diagnóstico de chamadas inclui gráficos que comparam as tarifas de falha para as diversas modalidades usadas no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="adf4d-121">The Call Diagnostic Summary Report includes graphs that compare failure rates for the various modalities used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="adf4d-122">As colunas nestes gráficos são na verdade hotlinks; por exemplo, se você clicar na coluna mensagens instantâneas para sessões ponto a ponto, fará Drill down até uma instância do [relatório de diagnóstico de atividade ponto a ponto no Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md), um relatório que fornece mais detalhes sobre todas as sessões de mensagens instantâneas incluídas no relatório de resumo do diagnóstico de chamadas.</span><span class="sxs-lookup"><span data-stu-id="adf4d-122">The columns in these graphs are actually hotlinks; for example, if you click the Instant messaging column for peer-to-peer sessions, you'll drill down to an instance of the [Peer-to-Peer Activity Diagnostic Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md), a report that provides additional details about all the instant messaging sessions included in the Call Diagnostic Summary Report.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="adf4d-123">Filtros</span><span class="sxs-lookup"><span data-stu-id="adf4d-123">Filters</span></span>

<span data-ttu-id="adf4d-p104">Filtros fornecem uma forma de retornar um conjunto de dados mais focado ou exibir os dados retornados de diferentes formas. Por exemplo, o Relatório de Resumo de Diagnóstico de Chamadas permite filtrar por informações como pool do Registrador Avançado ou Servidor de Borda usado na sessão. Você também pode escolher como os dados serão agrupados. Neste caso, as chamadas são agrupadas por hora, dia, semana ou mês.</span><span class="sxs-lookup"><span data-stu-id="adf4d-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Call Diagnostic Summary Report enables you to filter on such things as the Registrar pool or Edge Server used in the session. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="adf4d-128">A tabela a seguir lista os filtros que podem ser usados com o Relatório de Resumo de Diagnóstico de Chamadas.</span><span class="sxs-lookup"><span data-stu-id="adf4d-128">The following table lists the filters that you can use with the Call Diagnostic Summary Report.</span></span>

### <a name="call-diagnostic-summary-report-filters"></a><span data-ttu-id="adf4d-129">Filtros do Relatório de Resumo de Diagnóstico de Chamadas</span><span class="sxs-lookup"><span data-stu-id="adf4d-129">Call Diagnostic Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="adf4d-130">Nome</span><span class="sxs-lookup"><span data-stu-id="adf4d-130">Name</span></span></th>
<th><span data-ttu-id="adf4d-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="adf4d-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adf4d-132"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="adf4d-132"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="adf4d-p105">Data/hora de início para o intervalo de tempo. Para ver os dados por horas, insira a data e hora de início conforme segue:</span><span class="sxs-lookup"><span data-stu-id="adf4d-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="adf4d-135">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="adf4d-135">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="adf4d-p106">Se você não inserir a hora de início, o relatório começará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="adf4d-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="adf4d-138">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="adf4d-138">7/7/2012</span></span></p>
<p><span data-ttu-id="adf4d-139">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="adf4d-139">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="adf4d-140">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="adf4d-140">7/3/2012</span></span></p>
<p><span data-ttu-id="adf4d-141">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="adf4d-141">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adf4d-142"><strong>Até</strong></span><span class="sxs-lookup"><span data-stu-id="adf4d-142"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="adf4d-p107">Data/hora final de intervalo de tempo. Para ver os dados por horas, insira a data e hora final conforme segue:</span><span class="sxs-lookup"><span data-stu-id="adf4d-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="adf4d-145">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="adf4d-145">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="adf4d-p108">Se você não inserir a hora final, o relatório terminará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="adf4d-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="adf4d-148">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="adf4d-148">7/7/2012</span></span></p>
<p><span data-ttu-id="adf4d-149">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="adf4d-149">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="adf4d-150">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="adf4d-150">7/3/2012</span></span></p>
<p><span data-ttu-id="adf4d-151">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="adf4d-151">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adf4d-152"><strong>Intervalo</strong></span><span class="sxs-lookup"><span data-stu-id="adf4d-152"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="adf4d-p109">Intervalo de tempo. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="adf4d-p109">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="adf4d-155">Por hora (é possível exibir no máximo 25 horas)</span><span class="sxs-lookup"><span data-stu-id="adf4d-155">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="adf4d-156">Diariamente (é possível exibir no máximo 31 dias)</span><span class="sxs-lookup"><span data-stu-id="adf4d-156">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="adf4d-157">Semanalmente (é possível exibir no máximo 12 semanas)</span><span class="sxs-lookup"><span data-stu-id="adf4d-157">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="adf4d-158">Mensalmente (é possível exibir no máximo 12 meses)</span><span class="sxs-lookup"><span data-stu-id="adf4d-158">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="adf4d-159">Se as datas de início e término excederem o número máximo de valores permitidos para o intervalo selecionado, somente o número máximo de valores (a partir da data de início) será exibido.</span><span class="sxs-lookup"><span data-stu-id="adf4d-159">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="adf4d-160">Por exemplo, se você selecionar o intervalo diário com uma data de início de 7/7/2012 e uma data de término de 2/28/2012, os dados serão exibidos para os dias 8/7/2012 12:00 AM a 9/7/2012 12:00 AM (ou seja, um total de 31 dias da importância dos dados).</span><span class="sxs-lookup"><span data-stu-id="adf4d-160">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adf4d-161"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="adf4d-161"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="adf4d-p111">FQDN (Nome de domínio totalmente qualificado) do pool de Registradores ou Servidor de Borda. Você pode selecionar um pool individual ou clicar em <strong>[Tudo]</strong> para ver os dados de todos os pools. Essa lista suspensa é automaticamente preenchida para você com base nos registros no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="adf4d-p111">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="adf4d-165">Métricas para sessões ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="adf4d-165">Metrics for Peer-to-Peer Sessions</span></span>

<span data-ttu-id="adf4d-166">A tabela a seguir lista as informações fornecidas no Relatório de Resumo de Diagnóstico de Chamadas para sessões ponto a ponto (ou seja, sessões envolvendo somente dois participantes).</span><span class="sxs-lookup"><span data-stu-id="adf4d-166">The following table lists the information provided in the Call Diagnostic Summary Report for peer-to-peer sessions (that is, sessions involving just two participants).</span></span>

### <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="adf4d-167">Métricas para sessões ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="adf4d-167">Metrics for Peer-to-Peer Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="adf4d-168">Nome</span><span class="sxs-lookup"><span data-stu-id="adf4d-168">Name</span></span></th>
<th><span data-ttu-id="adf4d-169">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="adf4d-169">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="adf4d-170">Descrição</span><span class="sxs-lookup"><span data-stu-id="adf4d-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adf4d-171"><strong>Total de sessões</strong></span><span class="sxs-lookup"><span data-stu-id="adf4d-171"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="adf4d-172">Não</span><span class="sxs-lookup"><span data-stu-id="adf4d-172">No</span></span></p></td>
<td><p><span data-ttu-id="adf4d-173">Número total de sessões ponto a ponto conduzidas.</span><span class="sxs-lookup"><span data-stu-id="adf4d-173">Total number of peer-to-peer sessions conducted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adf4d-174"><strong>Taxa de falha</strong></span><span class="sxs-lookup"><span data-stu-id="adf4d-174"><strong>Failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="adf4d-175">Não</span><span class="sxs-lookup"><span data-stu-id="adf4d-175">No</span></span></p></td>
<td><p><span data-ttu-id="adf4d-p112">Percentual de sessões ponto a ponto que falharam. Ao clicar neste item, o relatório exibe o relatório de Diagnóstico de Atividades Ponto a Ponto, que mostra informações mais detalhadas sobre as sessões ponto a ponto com falha.</span><span class="sxs-lookup"><span data-stu-id="adf4d-p112">Percentage of peer-to-peer sessions that failed. When you click this item, the report shows the Peer-to-Peer Activity Diagnostic report, which displays more detailed information about the failed peer-to-peer sessions.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="adf4d-178">Métricas para sessões de conferência</span><span class="sxs-lookup"><span data-stu-id="adf4d-178">Metrics for Conferencing Sessions</span></span>

<span data-ttu-id="adf4d-179">A tabela a seguir lista as informações fornecidas pelo Relatório de Diagnóstico de Chamadas para sessões de conferência (ou seja, sessões envolvendo três ou mais participantes).</span><span class="sxs-lookup"><span data-stu-id="adf4d-179">The following table lists the information provided in the Call Diagnostic Report for conferencing sessions (that is, sessions involving three or more participants).</span></span>

### <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="adf4d-180">Métricas para sessões de conferência</span><span class="sxs-lookup"><span data-stu-id="adf4d-180">Metrics for Conferencing Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="adf4d-181">Nome</span><span class="sxs-lookup"><span data-stu-id="adf4d-181">Name</span></span></th>
<th><span data-ttu-id="adf4d-182">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="adf4d-182">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="adf4d-183">Descrição</span><span class="sxs-lookup"><span data-stu-id="adf4d-183">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adf4d-184"><strong>Conferências totais</strong></span><span class="sxs-lookup"><span data-stu-id="adf4d-184"><strong>Total conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="adf4d-185">Não</span><span class="sxs-lookup"><span data-stu-id="adf4d-185">No</span></span></p></td>
<td><p><span data-ttu-id="adf4d-186">Número total de conferências conduzidas.</span><span class="sxs-lookup"><span data-stu-id="adf4d-186">Total number of conferences conducted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adf4d-187"><strong>Sessões de conferência totais</strong></span><span class="sxs-lookup"><span data-stu-id="adf4d-187"><strong>Total conference sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="adf4d-188">Não</span><span class="sxs-lookup"><span data-stu-id="adf4d-188">No</span></span></p></td>
<td><p><span data-ttu-id="adf4d-189">Número total de sessões de conferência conduzidas.</span><span class="sxs-lookup"><span data-stu-id="adf4d-189">Total number of conferencing sessions conducted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adf4d-190"><strong>Taxa de falha de sessão geral</strong></span><span class="sxs-lookup"><span data-stu-id="adf4d-190"><strong>Overall session failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="adf4d-191">Não</span><span class="sxs-lookup"><span data-stu-id="adf4d-191">No</span></span></p></td>
<td><p><span data-ttu-id="adf4d-192">Percentual de sessões de conferência totais que falharam.</span><span class="sxs-lookup"><span data-stu-id="adf4d-192">Percentage of the total conferencing sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adf4d-193"><strong>Sessões de foco</strong></span><span class="sxs-lookup"><span data-stu-id="adf4d-193"><strong>Focus sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="adf4d-194">Não</span><span class="sxs-lookup"><span data-stu-id="adf4d-194">No</span></span></p></td>
<td><p><span data-ttu-id="adf4d-195">Número total de sessões de conferência baseadas em Foco que falharam.</span><span class="sxs-lookup"><span data-stu-id="adf4d-195">Total number of Focus-based conferencing sessions that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adf4d-196"><strong>Taxa de falha de foco</strong></span><span class="sxs-lookup"><span data-stu-id="adf4d-196"><strong>Focus failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="adf4d-197">Não</span><span class="sxs-lookup"><span data-stu-id="adf4d-197">No</span></span></p></td>
<td><p><span data-ttu-id="adf4d-198">Percentual de sessões de conferência baseadas em Foco que falharam.</span><span class="sxs-lookup"><span data-stu-id="adf4d-198">Percentage of the Focus-based conferencing sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adf4d-199"><strong>Sessões MCU</strong></span><span class="sxs-lookup"><span data-stu-id="adf4d-199"><strong>MCU sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="adf4d-200">Não</span><span class="sxs-lookup"><span data-stu-id="adf4d-200">No</span></span></p></td>
<td><p><span data-ttu-id="adf4d-201">Número total de conferências baseadas em servidor (anteriormente conhecidas como Unidade de Controle de Multipontos ou MCU) que falharam.</span><span class="sxs-lookup"><span data-stu-id="adf4d-201">Total number of conferencing server-based (formerly known as Multipoint Control Unit or MCU) conferences that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adf4d-202"><strong>Taxa de falha de MCU</strong></span><span class="sxs-lookup"><span data-stu-id="adf4d-202"><strong>MCU failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="adf4d-203">Não</span><span class="sxs-lookup"><span data-stu-id="adf4d-203">No</span></span></p></td>
<td><p><span data-ttu-id="adf4d-204">Percentual de conferências baseadas em servidor (anteriormente conhecidas como Unidade de Controle de Multipontos ou MCU) que falharam.</span><span class="sxs-lookup"><span data-stu-id="adf4d-204">Percentage of the conferencing server-based (formerly known as Multipoint Control Unit or MCU) conferences that failed.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="adf4d-205">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="adf4d-205">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

