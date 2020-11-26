---
title: 'Lync Server 2013: relatório de resumo da conferência'
description: 'Lync Server 2013: relatório de resumo da conferência.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Summary Report
ms:assetid: 62f54812-5700-45a3-8526-8f58b0f77fbc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558656(v=OCS.15)
ms:contentKeyID: 48184299
ms.date: 09/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2d9c0b8ad7280d2c7336282c14f46e6b5d6a1aec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434491"
---
# <a name="conference-summary-report-in-lync-server-2013"></a><span data-ttu-id="39c32-103">Relatório de Resumo de conferências no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39c32-103">Conference Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39c32-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39c32-104">

<span> </span></span></span>

<span data-ttu-id="39c32-105">_**Tópico da última modificação:** 2014-09-03_</span><span class="sxs-lookup"><span data-stu-id="39c32-105">_**Topic Last Modified:** 2014-09-03_</span></span>

<span data-ttu-id="39c32-106">O Relatório de Resumo de Conferências traz uma visão geral de suas sessões de conferência online.</span><span class="sxs-lookup"><span data-stu-id="39c32-106">The Conference Summary Report provides an overall view of your online conferencing sessions.</span></span> <span data-ttu-id="39c32-107">Geralmente, uma conferência envolve mais de 2 usuários e requer o uso de serviços de conferência do Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="39c32-107">A conference typically involves more than 2 users and requires the use of Microsoft Lync Server 2013 conferencing services.</span></span> <span data-ttu-id="39c32-108">Por comparação, uma sessão ponto a ponto geralmente envolve apenas 2 usuários e não requer o uso de serviços de conferência do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="39c32-108">By comparison, a peer-to-peer session typically involves just 2 users and does not require the use of Lync Server's conferencing services.</span></span> <span data-ttu-id="39c32-109">As atividades ponto a ponto são relatadas no [relatório de Resumo de atividades ponto a ponto no Lync Server 2013](lync-server-2013-peer-to-peer-activity-summary-report.md).</span><span class="sxs-lookup"><span data-stu-id="39c32-109">Peer-to-peer activities are reported on the [Peer-to-Peer Activity Summary Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-summary-report.md).</span></span>

<span data-ttu-id="39c32-110">O relatório de Resumo de conferências não só informa quantas conferências foram mantidas durante um determinado período (por hora, diária, semanal, mensal), mas também informa o número total de pessoas que participaram dessas conferências e o número total de organizadores de conferência exclusivos.</span><span class="sxs-lookup"><span data-stu-id="39c32-110">The Conference Summary Report not only tells you how many conferences were held during a given time period (hourly, daily, weekly, monthly) but also tells you the total number of people who took part in those conferences, and the total number of unique conference organizers.</span></span>

<span data-ttu-id="39c32-111">Um organizador "exclusivo" é qualquer pessoa que agenda pelo menos uma conferência.</span><span class="sxs-lookup"><span data-stu-id="39c32-111">A "unique” organizer is anyone who schedules at least one conference.</span></span> <span data-ttu-id="39c32-112">Por exemplo, se Pilar Ackerman agendar uma conferência, ela será contabilizada como um organizador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="39c32-112">For example, if Pilar Ackerman schedules one conference she counts as one unique organizer.</span></span> <span data-ttu-id="39c32-113">Se Ken Myer agendar 148 conferências, ele também será contabilizado como um único organizador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="39c32-113">If Ken Myer schedules 148 conferences he, too counts as one unique organizer.</span></span> <span data-ttu-id="39c32-114">Por exemplo, a tabela a seguir mostra 8 conferências agendadas, mas apenas três organizadores exclusivos (Ken Myer, pilar Alverca e David ahs).</span><span class="sxs-lookup"><span data-stu-id="39c32-114">For example, the table below shows 8 conferences scheduled, but just three unique organizers (Ken Myer, Pilar Ackerman, and David Ahs).</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39c32-115">Organizador da conferência</span><span class="sxs-lookup"><span data-stu-id="39c32-115">Conference Organizer</span></span></th>
<th><span data-ttu-id="39c32-116">Data da conferência</span><span class="sxs-lookup"><span data-stu-id="39c32-116">Conference Date</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39c32-117">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="39c32-117">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="39c32-118">7/7/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="39c32-118">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c32-119">David Ahs</span><span class="sxs-lookup"><span data-stu-id="39c32-119">David Ahs</span></span></p></td>
<td><p><span data-ttu-id="39c32-120">7/7/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="39c32-120">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c32-121">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="39c32-121">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="39c32-122">7/7/2012 11:00 AM</span><span class="sxs-lookup"><span data-stu-id="39c32-122">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c32-123">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="39c32-123">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="39c32-124">7/7/2012 11:00 AM</span><span class="sxs-lookup"><span data-stu-id="39c32-124">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c32-125">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="39c32-125">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="39c32-126">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="39c32-126">7/7/2012 1:00 PM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c32-127">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="39c32-127">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="39c32-128">7/7/2012 2:00 PM</span><span class="sxs-lookup"><span data-stu-id="39c32-128">7/7/2012 2:00 PM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c32-129">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="39c32-129">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="39c32-130">7/2/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="39c32-130">7/2/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c32-131">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="39c32-131">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="39c32-132">7/2/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="39c32-132">7/2/2012 10:00 AM</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="39c32-133">O Relatório de Resumo de Conferências também indica quantas conferências incluíram áudio e/ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="39c32-133">The Conference Summary Report also indicates how many conferences included audio and/or video.</span></span>

<div>

## <a name="accessing-the-conference-summary-report"></a><span data-ttu-id="39c32-134">Acessando o Relatório de Resumo de Conferências</span><span class="sxs-lookup"><span data-stu-id="39c32-134">Accessing the Conference Summary Report</span></span>

<span data-ttu-id="39c32-p103">O Relatório de Resumo de Conferências pode ser acessado na home page Relatórios de Monitoramento. Você pode filtrar pelo Relatório de Atividade de Conferência clicando em uma das métricas a seguir:</span><span class="sxs-lookup"><span data-stu-id="39c32-p103">The Conference Summary Report is accessed from the Monitoring Reports home page. You can drill down to the Conference Activity report by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="39c32-137">Total de conferências</span><span class="sxs-lookup"><span data-stu-id="39c32-137">Total conferences</span></span>

  - <span data-ttu-id="39c32-138">Total de participantes</span><span class="sxs-lookup"><span data-stu-id="39c32-138">Total participants</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-conference-summary-report"></a><span data-ttu-id="39c32-139">Usando o Relatório de Resumo de Conferências da melhor maneira possível</span><span class="sxs-lookup"><span data-stu-id="39c32-139">Making the Best Use of the Conference Summary Report</span></span>

<span data-ttu-id="39c32-140">Os valores totais para a maioria das métricas usadas no relatório de Resumo de conferências podem ser encontrados na parte inferior do relatório; Role para baixo para ver valores como o número total de conferências mantidas durante o período de tempo especificado e o número total de pessoas que participaram dessas conferências.</span><span class="sxs-lookup"><span data-stu-id="39c32-140">Total values for most of the metrics used on the Conference Summary Report can be found at the bottom of the report; scroll down to see values such as the total number of conferences held during the specified time period, and the total number of people who participated in those conferences.</span></span> <span data-ttu-id="39c32-141">Uma métrica que não está totalizada na parte inferior do relatório é o total de organizadores de conferências exclusivos.</span><span class="sxs-lookup"><span data-stu-id="39c32-141">One metric that is not totaled at the bottom of the report is Total unique conference organizers.</span></span> <span data-ttu-id="39c32-142">Por que não?</span><span class="sxs-lookup"><span data-stu-id="39c32-142">Why not?</span></span> <span data-ttu-id="39c32-143">Aqui está um motivo.</span><span class="sxs-lookup"><span data-stu-id="39c32-143">Here’s one reason.</span></span> <span data-ttu-id="39c32-144">Suponha que você esteja olhando para o valor de dados de um mês.</span><span class="sxs-lookup"><span data-stu-id="39c32-144">Suppose you are looking at a month's worth of data.</span></span> <span data-ttu-id="39c32-145">No dia 1, você tinha 34 organizadores de conferência exclusivos; no dia 2, você tinha 27 organizadores de conferências exclusivos.</span><span class="sxs-lookup"><span data-stu-id="39c32-145">On day 1 you had 34 unique conference organizers; on day 2 you had 27 unique conference organizers.</span></span> <span data-ttu-id="39c32-146">Isso significa que você tinha 61 organizadores de conferência exclusivos para estes dois dias?</span><span class="sxs-lookup"><span data-stu-id="39c32-146">Does that mean you had 61 unique conference organizers for those two days?</span></span> <span data-ttu-id="39c32-147">Não necessariamente.</span><span class="sxs-lookup"><span data-stu-id="39c32-147">Not necessarily.</span></span> <span data-ttu-id="39c32-148">Afinal, todas as 27 pessoas que organizaram conferências no dia 2 podem estar entre as pessoas do 34 que organizaram conferências no dia 1.</span><span class="sxs-lookup"><span data-stu-id="39c32-148">After all, all 27 people who organized conferences on day 2 might be among the 34 people who organized conferences on day 1.</span></span> <span data-ttu-id="39c32-149">Por exemplo, neste relatório simples, observe que Ken Myer e pilar Alverca conferências agendadas no 7/7/2012 e no 7/2/2012:</span><span class="sxs-lookup"><span data-stu-id="39c32-149">For example, in this simple report, note that Ken Myer and Pilar Ackerman scheduled conferences both on 7/7/2012 and on 7/2/2012:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39c32-150">Organizador da conferência</span><span class="sxs-lookup"><span data-stu-id="39c32-150">Conference Organizer</span></span></th>
<th><span data-ttu-id="39c32-151">Data da conferência</span><span class="sxs-lookup"><span data-stu-id="39c32-151">Conference Date</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39c32-152">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="39c32-152">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="39c32-153">7/7/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="39c32-153">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c32-154">David Ahs</span><span class="sxs-lookup"><span data-stu-id="39c32-154">David Ahs</span></span></p></td>
<td><p><span data-ttu-id="39c32-155">7/7/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="39c32-155">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c32-156">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="39c32-156">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="39c32-157">7/7/2012 11:00 AM</span><span class="sxs-lookup"><span data-stu-id="39c32-157">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c32-158">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="39c32-158">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="39c32-159">7/7/2012 11:00 AM</span><span class="sxs-lookup"><span data-stu-id="39c32-159">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c32-160">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="39c32-160">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="39c32-161">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="39c32-161">7/7/2012 1:00 PM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c32-162">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="39c32-162">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="39c32-163">7/7/2012 2:00 PM</span><span class="sxs-lookup"><span data-stu-id="39c32-163">7/7/2012 2:00 PM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c32-164">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="39c32-164">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="39c32-165">7/2/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="39c32-165">7/2/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c32-166">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="39c32-166">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="39c32-167">7/2/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="39c32-167">7/2/2012 10:00 AM</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="39c32-168">Para ter uma ideia melhor do número total de usuários exclusivos que organizaram conferências, altere o intervalo de tempo. Por exemplo, exiba os dados por mês e não por dia.</span><span class="sxs-lookup"><span data-stu-id="39c32-168">To get a better idea of the total number of unique users who organized conferences, change your time interval; for example, look at the data by month instead of by day.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="39c32-169">Filtros</span><span class="sxs-lookup"><span data-stu-id="39c32-169">Filters</span></span>

<span data-ttu-id="39c32-p105">Os filtros fornecem uma maneira de retornar um conjunto de dados mais direcionado ou de exibir os dados retornados de diferentes maneiras. Por exemplo, o Relatório de Resumo de Conferências permite que você escolha como os dados devem ser agrupados. Nesse caso, conferências agrupadas por hora, dia, semana ou mês.</span><span class="sxs-lookup"><span data-stu-id="39c32-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Conference Summary Report enables you to choose how data should be grouped. In this case, conferences grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="39c32-173">A tabela a seguir lista os filtros que você pode usar com o Relatório de Resumo de Conferências.</span><span class="sxs-lookup"><span data-stu-id="39c32-173">The following table lists the filters that you can use with the Conference Summary Report.</span></span>

### <a name="conference-summary-report-filters"></a><span data-ttu-id="39c32-174">Filtros do Relatório de Resumo de Conferências</span><span class="sxs-lookup"><span data-stu-id="39c32-174">Conference Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39c32-175">Nome</span><span class="sxs-lookup"><span data-stu-id="39c32-175">Name</span></span></th>
<th><span data-ttu-id="39c32-176">Descrição</span><span class="sxs-lookup"><span data-stu-id="39c32-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39c32-177"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-177"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="39c32-p106">Data/hora de início para o intervalo de tempo. Para ver os dados por horas, insira a data e hora de início conforme segue:</span><span class="sxs-lookup"><span data-stu-id="39c32-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="39c32-180">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="39c32-180">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="39c32-p107">Se você não inserir a hora de início, o relatório começará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="39c32-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="39c32-183">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="39c32-183">7/7/2012</span></span></p>
<p><span data-ttu-id="39c32-184">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="39c32-184">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="39c32-185">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="39c32-185">7/3/2012</span></span></p>
<p><span data-ttu-id="39c32-186">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="39c32-186">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c32-187"><strong>Até</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-187"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="39c32-p108">Data/hora final de intervalo de tempo. Para ver os dados por horas, insira a data e hora final conforme segue:</span><span class="sxs-lookup"><span data-stu-id="39c32-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="39c32-190">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="39c32-190">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="39c32-p109">Se você não inserir a hora final, o relatório terminará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="39c32-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="39c32-193">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="39c32-193">7/7/2012</span></span></p>
<p><span data-ttu-id="39c32-194">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="39c32-194">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="39c32-195">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="39c32-195">7/3/2012</span></span></p>
<p><span data-ttu-id="39c32-196">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="39c32-196">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c32-197"><strong>Intervalo</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-197"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="39c32-p110">Intervalo de tempo. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="39c32-p110">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="39c32-200">Por hora (é possível exibir no máximo 25 horas)</span><span class="sxs-lookup"><span data-stu-id="39c32-200">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="39c32-201">Diariamente (é possível exibir no máximo 31 dias)</span><span class="sxs-lookup"><span data-stu-id="39c32-201">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="39c32-202">Semanalmente (é possível exibir no máximo 12 semanas)</span><span class="sxs-lookup"><span data-stu-id="39c32-202">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="39c32-203">Mensalmente (é possível exibir no máximo 12 meses)</span><span class="sxs-lookup"><span data-stu-id="39c32-203">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="39c32-204">Se as datas de início e término excederem o número máximo de valores permitidos para o intervalo selecionado, apenas o número máximo de valores (começando pela data de início) será exibido.</span><span class="sxs-lookup"><span data-stu-id="39c32-204">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) are displayed.</span></span> <span data-ttu-id="39c32-205">Por exemplo, se você selecionar o intervalo diário com uma data de início de 7/7/2012 e uma data de término de 2/28/2012, os dados serão exibidos para os dias 8/7/2012 12:00 AM a 9/7/2012 12:00 AM (ou seja, um total de 31 dias da importância dos dados).</span><span class="sxs-lookup"><span data-stu-id="39c32-205">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="39c32-206">Métricas</span><span class="sxs-lookup"><span data-stu-id="39c32-206">Metrics</span></span>

<span data-ttu-id="39c32-207">A tabela a seguir as informações fornecidas pelo Relatório de Resumo de Conferências.</span><span class="sxs-lookup"><span data-stu-id="39c32-207">The following table the information provided by the Conferences Summary Report.</span></span>

### <a name="conference-summary-report-metrics"></a><span data-ttu-id="39c32-208">Métricas do Relatório de Resumo de Conferências</span><span class="sxs-lookup"><span data-stu-id="39c32-208">Conference Summary Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39c32-209">Nome</span><span class="sxs-lookup"><span data-stu-id="39c32-209">Name</span></span></th>
<th><span data-ttu-id="39c32-210">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="39c32-210">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="39c32-211">Descrição</span><span class="sxs-lookup"><span data-stu-id="39c32-211">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39c32-212"><strong>Por hora</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-212"><strong>Hourly</strong></span></span></p>
<p><span data-ttu-id="39c32-213"><strong>Diário</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-213"><strong>Daily</strong></span></span></p>
<p><span data-ttu-id="39c32-214"><strong>Semanal</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-214"><strong>Weekly</strong></span></span></p>
<p><span data-ttu-id="39c32-215"><strong>Mensal</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-215"><strong>Monthly</strong></span></span></p></td>
<td><p><span data-ttu-id="39c32-216">Não</span><span class="sxs-lookup"><span data-stu-id="39c32-216">No</span></span></p></td>
<td><p><span data-ttu-id="39c32-217">Indica o intervalo de tempo selecionado na barra de ferramentas de filtro.</span><span class="sxs-lookup"><span data-stu-id="39c32-217">Indicates the time interval that you selected on the filter toolbar.</span></span> <span data-ttu-id="39c32-218">Quando aplicável, é possível clicar em determinado intervalo de tempo para exibir informações detalhadas sobre ele.</span><span class="sxs-lookup"><span data-stu-id="39c32-218">Where applicable, you can click a given time interval to view detailed information for that interval.</span></span> <span data-ttu-id="39c32-219">Por exemplo, se você estiver usando o intervalo diário e clicar em 7/7/2012, verá um detalhamento por hora da atividade de registro do usuário para essa data.</span><span class="sxs-lookup"><span data-stu-id="39c32-219">For example, if you are using the Daily interval and you click 7/7/2012, you see an hourly breakdown of user registration activity for that date.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c32-220"><strong>Conferências totais</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-220"><strong>Total conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="39c32-221">Não</span><span class="sxs-lookup"><span data-stu-id="39c32-221">No</span></span></p></td>
<td><p><span data-ttu-id="39c32-p113">Número total de conferências (independentemente do tipo de conferência) que foram mantidas. Quando você clica nesse item, o relatório mostra o Relatório de Resumo de Conferências para o período de tempo selecionado.</span><span class="sxs-lookup"><span data-stu-id="39c32-p113">Total number of conferences (regardless of conference type) that were held. When you click this item, the report shows you the Conference Activity Report for the selected time period.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c32-224"><strong>Total de participantes</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-224"><strong>Total participants</strong></span></span></p></td>
<td><p><span data-ttu-id="39c32-225">Não</span><span class="sxs-lookup"><span data-stu-id="39c32-225">No</span></span></p></td>
<td><p><span data-ttu-id="39c32-p114">Número total de pessoas que participaram nas conferências. Quando você clica nesse item, o relatório mostra o Relatório de Resumo de Conferências para o período de tempo selecionado.</span><span class="sxs-lookup"><span data-stu-id="39c32-p114">Total number of people who took part in the conferences. When you click this item, the report shows you the Conference Activity Report for the selected time period.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c32-228"><strong>Média de participantes por conferência</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-228"><strong>Average participants per conference</strong></span></span></p></td>
<td><p><span data-ttu-id="39c32-229">Não</span><span class="sxs-lookup"><span data-stu-id="39c32-229">No</span></span></p></td>
<td><p><span data-ttu-id="39c32-p115">Número médio de pessoas que participaram de uma determinada conferência. É determinado dividindo o total de conferências pelo total de participantes.</span><span class="sxs-lookup"><span data-stu-id="39c32-p115">Average number of people who took part in a given conference. Determined by dividing the total conferences by the total participants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c32-232"><strong>Total de conferências A/V</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-232"><strong>Total A/V conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="39c32-233">Não</span><span class="sxs-lookup"><span data-stu-id="39c32-233">No</span></span></p></td>
<td><p><span data-ttu-id="39c32-234">Número total de conferências com áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="39c32-234">Total number of conferences that included audio or video.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c32-235"><strong>Total de minutos de conferências de A/V</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-235"><strong>Total A/V conference minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="39c32-236">Não</span><span class="sxs-lookup"><span data-stu-id="39c32-236">No</span></span></p></td>
<td><p><span data-ttu-id="39c32-237">Número total de minutos para a conferência de áudio/vídeo.</span><span class="sxs-lookup"><span data-stu-id="39c32-237">Total number of minutes devoted to audio/video conferencing.</span></span></p>
<p><span data-ttu-id="39c32-238">A métrica de minutos total de conferência a/V resume todos os tipos de áudio/conferência Visual, incluindo: conferências A/V; Conferências de mensagens instantâneas; conferências de compartilhamento de aplicativos; conferências de dados; e conferências PSTN.</span><span class="sxs-lookup"><span data-stu-id="39c32-238">The Total A/V conference minutes metric summarizes all the audio/visual conference types, including: A/V conferences; IM conferences; app sharing conferences; data conferences; and PSTN conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c32-239"><strong>Total de minutos de participantes de conferências de A/V</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-239"><strong>Total A/V conference participant minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="39c32-240">Não</span><span class="sxs-lookup"><span data-stu-id="39c32-240">No</span></span></p></td>
<td><p><span data-ttu-id="39c32-p116">Número total de minutos do participante na conferência de áudio/vídeo. Por exemplo, suponha que um usuário gaste cinco minutos em uma conferência de áudio/vídeo e um segundo usuário gaste três minutos nessa mesma conferência. O que soma um total de oito minutos de participantes: cinco minutos mais três minutos.</span><span class="sxs-lookup"><span data-stu-id="39c32-p116">Total number of participant minutes devoted to audio/video conferencing. For example, suppose one user spends 5 minutes in an audio/video conference and a second user spends 3 minutes in that same conference. That makes a total of 8 participant minutes: 5 minutes plus 3 minutes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c32-244"><strong>Média de minutos da conferência A/V</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-244"><strong>Average A/V conference minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="39c32-245">Não</span><span class="sxs-lookup"><span data-stu-id="39c32-245">No</span></span></p></td>
<td><p><span data-ttu-id="39c32-246">Número médio de minutos por conferência de áudio/vídeo.</span><span class="sxs-lookup"><span data-stu-id="39c32-246">Average number of minutes per audio/video conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c32-247"><strong>Número total de organizadores exclusivos de conferências</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-247"><strong>Total number of unique organizers of conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="39c32-248">Não</span><span class="sxs-lookup"><span data-stu-id="39c32-248">No</span></span></p></td>
<td><p><span data-ttu-id="39c32-p117">Número total de usuários que organizaram pelo menos uma conferência. Os usuários que organizaram mais de uma conferência são contados como um organizador exclusivo, assim como os usuários que só organizaram uma única conferência.</span><span class="sxs-lookup"><span data-stu-id="39c32-p117">Total number of users who organized at least one conference. Users who organized more than one conference are counted as one unique organizer, just like users who only organized a single conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c32-251"><strong>Total de mensagens de conferência</strong></span><span class="sxs-lookup"><span data-stu-id="39c32-251"><strong>Total conference messages</strong></span></span></p></td>
<td><p><span data-ttu-id="39c32-252">Não</span><span class="sxs-lookup"><span data-stu-id="39c32-252">No</span></span></p></td>
<td><p><span data-ttu-id="39c32-253">Número total de mensagens instantâneas enviadas durante as conferências.</span><span class="sxs-lookup"><span data-stu-id="39c32-253">Total number of instant messages sent during the conferences.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="39c32-254">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39c32-254">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

