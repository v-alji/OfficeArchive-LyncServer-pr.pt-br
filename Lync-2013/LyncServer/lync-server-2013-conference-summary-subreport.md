---
title: 'Lync Server 2013: sub relatório Resumo da conferência'
description: 'Lync Server 2013: sub relatório Resumo da conferência.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Summary Subreport
ms:assetid: 2fc1d2bf-34f5-4093-a6e2-250ec1f1b004
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204779(v=OCS.15)
ms:contentKeyID: 48183742
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0612ce1adb8a6b0fdea5e3bf70b88346f7c08044
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434484"
---
# <a name="conference-summary-subreport-in-lync-server-2013"></a><span data-ttu-id="63b99-103">Sub-relatório de Resumo de conferências no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="63b99-103">Conference Summary Subreport in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="63b99-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="63b99-104">

<span> </span></span></span>

<span data-ttu-id="63b99-105">_**Tópico da última modificação:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="63b99-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="63b99-p101">O Sub-relatório de Resumo de Conferências oferece uma visão geral de sessões de conferências com falha. Estas sessões com falha são detalhadas pelo tipo de sessão: sessões de Foco e sessões MCU.</span><span class="sxs-lookup"><span data-stu-id="63b99-p101">The Conference Summary Subreport provides an overall view of failed conference sessions. These failed sessions are further broken down by session type: Focus sessions and MCU sessions.</span></span>

<div>

## <a name="filters"></a><span data-ttu-id="63b99-108">Filtros</span><span class="sxs-lookup"><span data-stu-id="63b99-108">Filters</span></span>

<span data-ttu-id="63b99-p102">Os filtros oferecem uma forma de retornar um conjunto de dados mais detalhado ou para exibir os dados retornados de formas diferentes. A tabela a seguir lista os filtros que você pode usar com o Sub-relatório de Resumo de Conferências.</span><span class="sxs-lookup"><span data-stu-id="63b99-p102">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Conference Summary Subreport.</span></span>

### <a name="conference-summary-subreport-filters"></a><span data-ttu-id="63b99-111">Filtros do Sub-relatório de Resumo de Conferências</span><span class="sxs-lookup"><span data-stu-id="63b99-111">Conference Summary Subreport Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63b99-112">Nome</span><span class="sxs-lookup"><span data-stu-id="63b99-112">Name</span></span></th>
<th><span data-ttu-id="63b99-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="63b99-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63b99-114"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="63b99-114"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="63b99-p103">Data/hora de início para o intervalo de tempo. Para ver os dados por horas, insira a data e hora de início conforme segue:</span><span class="sxs-lookup"><span data-stu-id="63b99-p103">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="63b99-117">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="63b99-117">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="63b99-p104">Se você não inserir a hora de início, o relatório começará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="63b99-p104">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="63b99-120">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="63b99-120">7/7/2012</span></span></p>
<p><span data-ttu-id="63b99-121">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="63b99-121">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="63b99-122">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="63b99-122">7/3/2012</span></span></p>
<p><span data-ttu-id="63b99-123">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="63b99-123">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63b99-124"><strong>Até</strong></span><span class="sxs-lookup"><span data-stu-id="63b99-124"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="63b99-p105">Data/hora final de intervalo de tempo. Para ver os dados por horas, insira a data e hora final conforme segue:</span><span class="sxs-lookup"><span data-stu-id="63b99-p105">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="63b99-127">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="63b99-127">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="63b99-p106">Se você não inserir a hora final, o relatório terminará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="63b99-p106">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="63b99-130">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="63b99-130">7/7/2012</span></span></p>
<p><span data-ttu-id="63b99-131">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="63b99-131">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="63b99-132">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="63b99-132">7/3/2012</span></span></p>
<p><span data-ttu-id="63b99-133">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="63b99-133">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63b99-134"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="63b99-134"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="63b99-p107">O FQDN (nome de domínio totalmente qualificado) do pool Registrador Avançado ou Servidor de Borda. Você pode selecionar um pool individual ou clicar em <strong>[Todos]</strong> para ver os dados de todos os pools. Essa lista suspensa é preenchida automaticamente com base nos registros no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="63b99-p107">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="63b99-138">Métricas</span><span class="sxs-lookup"><span data-stu-id="63b99-138">Metrics</span></span>

<span data-ttu-id="63b99-139">A tabela a seguir lista as informações fornecidas no Sub-relatório de Resumo de Conferências.</span><span class="sxs-lookup"><span data-stu-id="63b99-139">The following table lists the information provided in the Conference Summary Subreport.</span></span>

### <a name="conference-summary-subreport-metrics"></a><span data-ttu-id="63b99-140">Métricas do Sub-relatório de Resumo de Conferências</span><span class="sxs-lookup"><span data-stu-id="63b99-140">Conference Summary Subreport Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63b99-141">Nome</span><span class="sxs-lookup"><span data-stu-id="63b99-141">Name</span></span></th>
<th><span data-ttu-id="63b99-142">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="63b99-142">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="63b99-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="63b99-143">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63b99-144"><strong>Conferências totais</strong></span><span class="sxs-lookup"><span data-stu-id="63b99-144"><strong>Total conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="63b99-145">Não</span><span class="sxs-lookup"><span data-stu-id="63b99-145">No</span></span></p></td>
<td><p><span data-ttu-id="63b99-146">Número total de conferências realizadas.</span><span class="sxs-lookup"><span data-stu-id="63b99-146">Total number of conferences held.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63b99-147"><strong>Total de sessões de conferência</strong></span><span class="sxs-lookup"><span data-stu-id="63b99-147"><strong>Total conference sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="63b99-148">Não</span><span class="sxs-lookup"><span data-stu-id="63b99-148">No</span></span></p></td>
<td><p><span data-ttu-id="63b99-p108">Número total de sessões de conferência. Uma única conferência pode ter várias sessões; por exemplo, uma conferência pode incluir uma sessão Foco e uma sessão MCU.</span><span class="sxs-lookup"><span data-stu-id="63b99-p108">Total number of conference sessions. A single conference can have multiple sessions; for example, a conference might include both a Focus session and an MCU session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63b99-151"><strong>Taxa geral de falha de sessão</strong></span><span class="sxs-lookup"><span data-stu-id="63b99-151"><strong>Overall session failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="63b99-152">Não</span><span class="sxs-lookup"><span data-stu-id="63b99-152">No</span></span></p></td>
<td><p><span data-ttu-id="63b99-153">Porcentagem de todas as conferências que falharam.</span><span class="sxs-lookup"><span data-stu-id="63b99-153">Percentage of all conferences that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63b99-154"><strong>Sessões de Foco</strong></span><span class="sxs-lookup"><span data-stu-id="63b99-154"><strong>Focus sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="63b99-155">Não</span><span class="sxs-lookup"><span data-stu-id="63b99-155">No</span></span></p></td>
<td><p><span data-ttu-id="63b99-156">Número total de sessões de Foco.</span><span class="sxs-lookup"><span data-stu-id="63b99-156">Total number of Focus sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63b99-157"><strong>Taxa de falha de Foco</strong></span><span class="sxs-lookup"><span data-stu-id="63b99-157"><strong>Focus failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="63b99-158">Não</span><span class="sxs-lookup"><span data-stu-id="63b99-158">No</span></span></p></td>
<td><p><span data-ttu-id="63b99-159">Porcentagem das sessões de Foco que falharam.</span><span class="sxs-lookup"><span data-stu-id="63b99-159">Percentage of Focus sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63b99-160">Sessões MCU</span><span class="sxs-lookup"><span data-stu-id="63b99-160">MCU sessions</span></span></p></td>
<td><p><span data-ttu-id="63b99-161">Não</span><span class="sxs-lookup"><span data-stu-id="63b99-161">No</span></span></p></td>
<td><p><span data-ttu-id="63b99-162">Número total de sessões MCU.</span><span class="sxs-lookup"><span data-stu-id="63b99-162">Total number of MCU sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63b99-163"><strong>Taxa de falha de MCU</strong></span><span class="sxs-lookup"><span data-stu-id="63b99-163"><strong>MCU failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="63b99-164">Não</span><span class="sxs-lookup"><span data-stu-id="63b99-164">No</span></span></p></td>
<td><p><span data-ttu-id="63b99-165">Porcentagem de sessões MCU que falharam.</span><span class="sxs-lookup"><span data-stu-id="63b99-165">Percentage of MCU sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63b99-166"><strong>Sessões MCU por modalidade</strong></span><span class="sxs-lookup"><span data-stu-id="63b99-166"><strong>MCU sessions by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="63b99-167">Não</span><span class="sxs-lookup"><span data-stu-id="63b99-167">No</span></span></p></td>
<td><p><span data-ttu-id="63b99-168">Número total de sessões MCU, agrupado por modalidade (por exemplo, conferência de IM).</span><span class="sxs-lookup"><span data-stu-id="63b99-168">Total number of MCU sessions, grouped by modality (for example, IM conferencing).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63b99-169"><strong>Taxa de falha por modalidade</strong></span><span class="sxs-lookup"><span data-stu-id="63b99-169"><strong>Failure rate by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="63b99-170">Não</span><span class="sxs-lookup"><span data-stu-id="63b99-170">No</span></span></p></td>
<td><p><span data-ttu-id="63b99-171">Porcentagem de sessões MCU que falharam, agrupadas por modalidade (por exemplo, conferência de IM).</span><span class="sxs-lookup"><span data-stu-id="63b99-171">Percentage of MCU sessions that failed, grouped by modality (for example, IM conferencing).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="63b99-172">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="63b99-172">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

