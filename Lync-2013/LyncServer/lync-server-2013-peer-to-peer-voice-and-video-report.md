---
title: 'Lync Server 2013: relatório de voz e vídeo ponto a ponto'
description: 'Lync Server 2013: relatório de voz e vídeo ponto a ponto.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Peer-to-Peer Voice and Video Report
ms:assetid: e17c36b5-5a2f-4673-9696-3b2d31c2bb2f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615040(v=OCS.15)
ms:contentKeyID: 48185535
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 43041926b3d6b57508b6ee4c53ca9cb055bcb348
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424681"
---
# <a name="peer-to-peer-voice-and-video-report-in-lync-server-2013"></a><span data-ttu-id="c26a3-103">Relatório de voz e vídeo ponto a ponto no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c26a3-103">Peer-to-Peer Voice and Video Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c26a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c26a3-104">

<span> </span></span></span>

<span data-ttu-id="c26a3-105">_**Tópico da última modificação:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="c26a3-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="c26a3-p101">O Relatório de Vídeo e Voz Ponto a Ponto oferece uma visão detalhada da distribuição de chamadas de voz e vídeo por um período específico (por exemplo, chamadas por hora ou chamadas por dia). O relatório também oferece a opção de exibir todas as chamadas de voz e vídeo realizadas ou de exibir apenas as chamadas bem-sucedidas ou com falha. Os relatórios mostram as informações das chamadas divididas nos seguintes agrupamentos:</span><span class="sxs-lookup"><span data-stu-id="c26a3-p101">The Peer-to-Peer Voice and Video Report provides a detailed look at the distribution of voice and video calls over a specified period of time (for example, calls per hour or calls per day). The report also gives you the option of viewing all the voice and video calls that were made, or of viewing only the successful or failed calls. The reports shows call information broken down into the following groupings:</span></span>

  - <span data-ttu-id="c26a3-109">Chamadas por pool</span><span class="sxs-lookup"><span data-stu-id="c26a3-109">Calls per pool</span></span>

  - <span data-ttu-id="c26a3-110">Chamadas por tipo de chamada (por exemplo, uma chamada de Lync para Lync versus uma chamada do Lync para uma pessoa na rede PSTN)</span><span class="sxs-lookup"><span data-stu-id="c26a3-110">Calls per call type (for example, a Lync to Lync call vs. a Lync call to a person on the PSTN network)</span></span>

  - <span data-ttu-id="c26a3-111">Chamadas por tipo de acesso (os usuários conectados na rede interna versus usuários conectados na rede externa)</span><span class="sxs-lookup"><span data-stu-id="c26a3-111">Calls per access type (users logged on to the internal network vs. users logged on to the external network)</span></span>

  - <span data-ttu-id="c26a3-112">Chamadas por servidor de mediação</span><span class="sxs-lookup"><span data-stu-id="c26a3-112">Calls per Mediation Server</span></span>

<div>

## <a name="to-access-the-peer-to-peer-voice-and-video-report"></a><span data-ttu-id="c26a3-113">Para acessar o relatório de vídeo e voz ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="c26a3-113">To access the peer-to-peer voice and video report</span></span>

<span data-ttu-id="c26a3-114">É possível acessar o Relatório de Vídeo e Voz Ponto a Ponto apenas abrindo o Relatório de Resumo de Atividades Ponto a Ponto e clicando em qualquer uma das seguintes métricas:</span><span class="sxs-lookup"><span data-stu-id="c26a3-114">You can access the Peer-to-Peer Voice and Video Report only by opening the Peer-to-Peer Activity Summary Report and then clicking any of the following metrics:</span></span>

  - <span data-ttu-id="c26a3-115">Total de sessões de áudio ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="c26a3-115">Total peer-to-peer audio sessions</span></span>

  - <span data-ttu-id="c26a3-116">Total de minutos de áudio ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="c26a3-116">Total peer-to-peer audio minutes</span></span>

  - <span data-ttu-id="c26a3-117">Total de sessões de vídeo ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="c26a3-117">Total peer-to-peer video sessions</span></span>

  - <span data-ttu-id="c26a3-118">Total de minutos de vídeo ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="c26a3-118">Total peer-to-peer video minutes</span></span>

</div>

<div>

## <a name="to-make-the-best-use-of-the-peer-to-peer-voice-and-video-report"></a><span data-ttu-id="c26a3-119">Para aproveitar melhor o relatório de vídeo e voz ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="c26a3-119">To make the best use of the peer-to-peer voice and video report</span></span>

<span data-ttu-id="c26a3-p102">Existem várias formas de filtrar o Relatório de Vídeo e Voz Ponto a Ponto. No entanto, essas opções de filtragem são ocultas da exibição por padrão. Para exibir as opções de filtragem disponíveis, clique no botão **Exibir/Ocultar Parâmetros** no canto superior direito da janela Relatório.</span><span class="sxs-lookup"><span data-stu-id="c26a3-p102">There are a number of ways you can filter the Peer-to-Peer Voice and Video Report. However, those filtering options are hidden from view by default. To view the filtering options available to you, click **Show/Hide Parameters** button in the upper-right corner of the Report window.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="c26a3-123">Filtros</span><span class="sxs-lookup"><span data-stu-id="c26a3-123">Filters</span></span>

<span data-ttu-id="c26a3-p103">Os filtros fornecem uma maneira de retornar um conjunto de dados mais direcionado ou de exibir dados de maneiras diferentes. A tabela a seguir lista os filtros que podem ser usados com o Relatório de Vídeo e Voz Ponto a Ponto.</span><span class="sxs-lookup"><span data-stu-id="c26a3-p103">Filters provide a way for you to return a more finely targeted set of data or to view the data in different ways. The following table lists the filters that you can use with the Peer-to-Peer Voice and Video Report.</span></span>

### <a name="peer-to-peer-voice-and-video-report-filters"></a><span data-ttu-id="c26a3-126">Filtros do relatório de vídeo e voz ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="c26a3-126">Peer-to-peer voice and video report filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c26a3-127">Nome</span><span class="sxs-lookup"><span data-stu-id="c26a3-127">Name</span></span></th>
<th><span data-ttu-id="c26a3-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="c26a3-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c26a3-129"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-129"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-p104">Data e hora de início do intervalo de tempo. Para ver os dados por hora, insira a data e hora de início desta forma:</span><span class="sxs-lookup"><span data-stu-id="c26a3-p104">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="c26a3-132">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="c26a3-132">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="c26a3-p105">Se você não inserir a hora de início, o relatório começará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="c26a3-p105">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="c26a3-135">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="c26a3-135">7/7/2012</span></span></p>
<p><span data-ttu-id="c26a3-136">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="c26a3-136">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="c26a3-137">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="c26a3-137">7/3/2012</span></span></p>
<p><span data-ttu-id="c26a3-138">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="c26a3-138">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c26a3-139"><strong>Até</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-139"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-p106">Data/hora final de intervalo de tempo. Para ver os dados por horas, insira a data e hora final conforme segue:</span><span class="sxs-lookup"><span data-stu-id="c26a3-p106">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="c26a3-142">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="c26a3-142">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="c26a3-p107">Se você não inserir a hora final, o relatório terminará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="c26a3-p107">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="c26a3-145">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="c26a3-145">7/7/2012</span></span></p>
<p><span data-ttu-id="c26a3-146">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="c26a3-146">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="c26a3-147">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="c26a3-147">7/3/2012</span></span></p>
<p><span data-ttu-id="c26a3-148">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="c26a3-148">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c26a3-149"><strong>Intervalo</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-149"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-p108">Intervalo de tempo. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="c26a3-p108">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c26a3-152">Por hora (é possível exibir no máximo 25 horas)</span><span class="sxs-lookup"><span data-stu-id="c26a3-152">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="c26a3-153">Diariamente (é possível exibir no máximo 31 dias)</span><span class="sxs-lookup"><span data-stu-id="c26a3-153">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="c26a3-154">Semanalmente (é possível exibir no máximo 12 semanas)</span><span class="sxs-lookup"><span data-stu-id="c26a3-154">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="c26a3-155">Mensalmente (é possível exibir no máximo 12 meses)</span><span class="sxs-lookup"><span data-stu-id="c26a3-155">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="c26a3-156">Se as datas de início e término excederem o número máximo de valores permitidos para o intervalo selecionado, somente o número máximo de valores (a partir da data de início) será exibido.</span><span class="sxs-lookup"><span data-stu-id="c26a3-156">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="c26a3-157">Por exemplo, se você selecionar o intervalo diário com uma data de início de 7/7/2012 e uma data de término de 2/28/2012, os dados serão exibidos para os dias 8/7/2012 12:00 AM a 9/7/2012 12:00 AM (ou seja, um total de 31 dias da importância dos dados).</span><span class="sxs-lookup"><span data-stu-id="c26a3-157">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c26a3-158"><strong>Tipo de mídia</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-158"><strong>Media type</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-p110">Indica o tipo de mídia usado na sessão. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="c26a3-p110">Indicates the type of media used in the session. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c26a3-161">Ambos</span><span class="sxs-lookup"><span data-stu-id="c26a3-161">Both</span></span></p></li>
<li><p><span data-ttu-id="c26a3-162">Áudio</span><span class="sxs-lookup"><span data-stu-id="c26a3-162">Audio</span></span></p></li>
<li><p><span data-ttu-id="c26a3-163">Vídeo</span><span class="sxs-lookup"><span data-stu-id="c26a3-163">Video</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c26a3-164"><strong>Disposição da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-164"><strong>Call disposition</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-p111">Indica o sucesso ou fracasso da sessão. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="c26a3-p111">Indicates the success or failure of the session. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c26a3-167">[Todos]</span><span class="sxs-lookup"><span data-stu-id="c26a3-167">[All]</span></span></p></li>
<li><p><span data-ttu-id="c26a3-168">Chamadas com Êxito</span><span class="sxs-lookup"><span data-stu-id="c26a3-168">Success Calls</span></span></p></li>
<li><p><span data-ttu-id="c26a3-169">Chamadas com Falha</span><span class="sxs-lookup"><span data-stu-id="c26a3-169">Failed Calls</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c26a3-170"><strong>Relatório por</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-170"><strong>Report by</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-p112">Indica os valores a serem usados no relatório. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="c26a3-p112">Indicates the values to be used in the report. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c26a3-173">Contagem de sessões</span><span class="sxs-lookup"><span data-stu-id="c26a3-173">Session count</span></span></p></li>
<li><p><span data-ttu-id="c26a3-174">Minutos de chamadas</span><span class="sxs-lookup"><span data-stu-id="c26a3-174">Call minutes</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-pool"></a><span data-ttu-id="c26a3-175">Métricas para atividade de vídeo e voz ponto a ponto por pool</span><span class="sxs-lookup"><span data-stu-id="c26a3-175">Metrics for peer-to-peer voice and video activity by Pool</span></span>

<span data-ttu-id="c26a3-176">A tabela a seguir lista as informações fornecidas no Relatório de Vídeo e Voz Ponto a Ponto para cada pool.</span><span class="sxs-lookup"><span data-stu-id="c26a3-176">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each pool.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-pool"></a><span data-ttu-id="c26a3-177">Métricas para atividade de vídeo e voz ponto a ponto por pool</span><span class="sxs-lookup"><span data-stu-id="c26a3-177">Metrics for peer-to-peer voice and video activity by pool</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c26a3-178">Nome</span><span class="sxs-lookup"><span data-stu-id="c26a3-178">Name</span></span></th>
<th><span data-ttu-id="c26a3-179">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="c26a3-179">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="c26a3-180">Descrição</span><span class="sxs-lookup"><span data-stu-id="c26a3-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c26a3-181"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-181"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-182">Não</span><span class="sxs-lookup"><span data-stu-id="c26a3-182">No</span></span></p></td>
<td><p><span data-ttu-id="c26a3-183">Nome do pool de registradores ou servidor de borda usado para a chamada.</span><span class="sxs-lookup"><span data-stu-id="c26a3-183">Name of the Registrar pool or Edge Server used for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c26a3-184"><strong>Data/Hora</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-184"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-185">Não</span><span class="sxs-lookup"><span data-stu-id="c26a3-185">No</span></span></p></td>
<td><p><span data-ttu-id="c26a3-186">Período de data e hora durante o qual a chamada foi realizada.</span><span class="sxs-lookup"><span data-stu-id="c26a3-186">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c26a3-187"><strong>Total</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-187"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-188">Não</span><span class="sxs-lookup"><span data-stu-id="c26a3-188">No</span></span></p></td>
<td><p><span data-ttu-id="c26a3-189">Número total de sessões ou contagem total de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c26a3-189">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-call-type"></a><span data-ttu-id="c26a3-190">Métricas da atividade de vídeo e voz ponto a ponto por tipo de chamada</span><span class="sxs-lookup"><span data-stu-id="c26a3-190">Metrics for peer-to-peer voice and video activity by call type</span></span>

<span data-ttu-id="c26a3-191">A tabela a seguir lista as informações fornecidas no Relatório de Vídeo e Voz Ponto a Ponto para cada tipo de chamada realizada.</span><span class="sxs-lookup"><span data-stu-id="c26a3-191">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each type of call that was made.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-call-type"></a><span data-ttu-id="c26a3-192">Métricas da atividade de vídeo e voz ponto a ponto por tipo de chamada</span><span class="sxs-lookup"><span data-stu-id="c26a3-192">Metrics for peer-to-peer voice and video activity by call type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c26a3-193">Nome</span><span class="sxs-lookup"><span data-stu-id="c26a3-193">Name</span></span></th>
<th><span data-ttu-id="c26a3-194">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="c26a3-194">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="c26a3-195">Descrição</span><span class="sxs-lookup"><span data-stu-id="c26a3-195">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c26a3-196"><strong>Tipo de chamada</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-196"><strong>Call type</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-197">Não</span><span class="sxs-lookup"><span data-stu-id="c26a3-197">No</span></span></p></td>
<td><p><span data-ttu-id="c26a3-p113">Indica o tipo de chamada realizada. Os valores são um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="c26a3-p113">Indicates the type of call that was made. Values are one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c26a3-200">UC-para-UC</span><span class="sxs-lookup"><span data-stu-id="c26a3-200">UC-to-UC</span></span></p></li>
<li><p><span data-ttu-id="c26a3-201">UC-para-PSTN</span><span class="sxs-lookup"><span data-stu-id="c26a3-201">UC-to-PSTN</span></span></p></li>
<li><p><span data-ttu-id="c26a3-202">PSTN-para-UC</span><span class="sxs-lookup"><span data-stu-id="c26a3-202">PSTN-to-UC</span></span></p></li>
<li><p><span data-ttu-id="c26a3-203">PSTN-para-PSTN</span><span class="sxs-lookup"><span data-stu-id="c26a3-203">PSTN-to-PSTN</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c26a3-204"><strong>Data/Hora</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-204"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-205">Não</span><span class="sxs-lookup"><span data-stu-id="c26a3-205">No</span></span></p></td>
<td><p><span data-ttu-id="c26a3-206">Período de data e hora durante o qual a chamada foi realizada.</span><span class="sxs-lookup"><span data-stu-id="c26a3-206">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c26a3-207"><strong>Total</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-207"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-208">Não</span><span class="sxs-lookup"><span data-stu-id="c26a3-208">No</span></span></p></td>
<td><p><span data-ttu-id="c26a3-209">Número total de sessões ou contagem total de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c26a3-209">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-access-type"></a><span data-ttu-id="c26a3-210">Métricas da atividade de vídeo e voz ponto a ponto por tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="c26a3-210">Metrics for peer-to-peer voice and video activity by access type</span></span>

<span data-ttu-id="c26a3-211">A tabela a seguir lista as informações fornecidas no Relatório de Vídeo e Voz Ponto a Ponto para cada tipo de acesso à rede.</span><span class="sxs-lookup"><span data-stu-id="c26a3-211">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each network access type.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-access-type"></a><span data-ttu-id="c26a3-212">Métricas da atividade de vídeo e voz ponto a ponto por tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="c26a3-212">Metrics for peer-to-peer voice and video activity by access type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c26a3-213">Nome</span><span class="sxs-lookup"><span data-stu-id="c26a3-213">Name</span></span></th>
<th><span data-ttu-id="c26a3-214">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="c26a3-214">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="c26a3-215">Descrição</span><span class="sxs-lookup"><span data-stu-id="c26a3-215">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c26a3-216"><strong>Tipo de atividade</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-216"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-217">Não</span><span class="sxs-lookup"><span data-stu-id="c26a3-217">No</span></span></p></td>
<td><p><span data-ttu-id="c26a3-p114">Indica se os clientes estavam conectados na rede interna ou rede externa quando a chamada foi realizada. Os valores são normalmente um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="c26a3-p114">Indicates whether the clients were logged on to the internal network or the external network when the call was placed. Values are typically one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c26a3-220">Interno</span><span class="sxs-lookup"><span data-stu-id="c26a3-220">Internal</span></span></p></li>
<li><p><span data-ttu-id="c26a3-221">Externo</span><span class="sxs-lookup"><span data-stu-id="c26a3-221">External</span></span></p></li>
<li><p><span data-ttu-id="c26a3-222">Misto</span><span class="sxs-lookup"><span data-stu-id="c26a3-222">Mixed</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c26a3-223"><strong>Data/Hora</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-223"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-224">Não</span><span class="sxs-lookup"><span data-stu-id="c26a3-224">No</span></span></p></td>
<td><p><span data-ttu-id="c26a3-225">Período de data e hora durante o qual a chamada foi realizada.</span><span class="sxs-lookup"><span data-stu-id="c26a3-225">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c26a3-226"><strong>Total</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-226"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-227">Não</span><span class="sxs-lookup"><span data-stu-id="c26a3-227">No</span></span></p></td>
<td><p><span data-ttu-id="c26a3-228">Número total de sessões ou contagem total de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c26a3-228">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-mediation-server"></a><span data-ttu-id="c26a3-229">Métricas para atividade de vídeo e voz ponto a ponto por servidor de mediação</span><span class="sxs-lookup"><span data-stu-id="c26a3-229">Metrics for peer-to-peer voice and video activity by mediation server</span></span>

<span data-ttu-id="c26a3-230">A tabela a seguir lista as informações fornecidas no relatório de voz e vídeo ponto a ponto para cada servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="c26a3-230">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each Mediation Server.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-mediation-server"></a><span data-ttu-id="c26a3-231">Métricas para atividade de vídeo e voz ponto a ponto por servidor de mediação</span><span class="sxs-lookup"><span data-stu-id="c26a3-231">Metrics for peer-to-peer voice and video activity by mediation server</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c26a3-232">Nome</span><span class="sxs-lookup"><span data-stu-id="c26a3-232">Name</span></span></th>
<th><span data-ttu-id="c26a3-233">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="c26a3-233">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="c26a3-234">Descrição</span><span class="sxs-lookup"><span data-stu-id="c26a3-234">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c26a3-235"><strong>Servidor de Mediação</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-235"><strong>Mediation Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-236">Não</span><span class="sxs-lookup"><span data-stu-id="c26a3-236">No</span></span></p></td>
<td><p><span data-ttu-id="c26a3-237">Nome do servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="c26a3-237">Name of the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c26a3-238"><strong>Data/Hora</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-238"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-239">Não</span><span class="sxs-lookup"><span data-stu-id="c26a3-239">No</span></span></p></td>
<td><p><span data-ttu-id="c26a3-240">Período de data e hora durante o qual a chamada foi realizada.</span><span class="sxs-lookup"><span data-stu-id="c26a3-240">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c26a3-241"><strong>Total</strong></span><span class="sxs-lookup"><span data-stu-id="c26a3-241"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="c26a3-242">Não</span><span class="sxs-lookup"><span data-stu-id="c26a3-242">No</span></span></p></td>
<td><p><span data-ttu-id="c26a3-243">Número total de sessões ou contagem total de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c26a3-243">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c26a3-244">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c26a3-244">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

