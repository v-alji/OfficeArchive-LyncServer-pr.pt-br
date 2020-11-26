---
title: 'Lync Server 2013: relatório de diagnóstico de atividade ponto a ponto'
description: 'Lync Server 2013: relatório de diagnóstico de atividade ponto a ponto.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Peer-to-Peer Activity Diagnostic Report
ms:assetid: 025e8ab4-2e64-4a6b-8f52-caf756a5cac3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558602(v=OCS.15)
ms:contentKeyID: 48183242
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 80172c5e0f8b23bf05fad6ec300f0d1ffefb3327
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424679"
---
# <a name="peer-to-peer-activity-diagnostic-report-in-lync-server-2013"></a><span data-ttu-id="47827-103">Relatório de diagnóstico de atividade ponto a ponto no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47827-103">Peer-to-Peer Activity Diagnostic Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="47827-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="47827-104">

<span> </span></span></span>

<span data-ttu-id="47827-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="47827-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="47827-106">O Relatório de Diagnóstico de Atividades Ponto a Ponto fornece informações sobre o sucesso e falha de suas sessões de comunicação ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="47827-106">The Peer-to-Peer Activity Diagnostic Report provides information about the success and failure of your peer-to-peer communication sessions.</span></span> <span data-ttu-id="47827-107">Observe que o Microsoft Lync Server 2013 distingue entre os diferentes tipos de falha:</span><span class="sxs-lookup"><span data-stu-id="47827-107">Note that Microsoft Lync Server 2013 distinguishes between different kinds of failure:</span></span>

  - <span data-ttu-id="47827-108">**Falha esperada**.</span><span class="sxs-lookup"><span data-stu-id="47827-108">**Expected failure**.</span></span> <span data-ttu-id="47827-109">Uma falha esperada é normalmente uma falha somente no sentido mais técnico.</span><span class="sxs-lookup"><span data-stu-id="47827-109">An expected failure is typically a failure only in the most technical sense.</span></span> <span data-ttu-id="47827-110">Por exemplo, vamos supor que você ligue para alguém, mas ele ou ela esteja fora do escritório e não possa atender ao telefone.</span><span class="sxs-lookup"><span data-stu-id="47827-110">For example, suppose you call someone, but he or she is away from the office and is unable to answer the phone.</span></span> <span data-ttu-id="47827-111">Como a chamada não foi atendida, ela é considerada tecnicamente uma falha.</span><span class="sxs-lookup"><span data-stu-id="47827-111">Because the call was not answered, the call is technically considered a failure.</span></span> <span data-ttu-id="47827-112">Por outro lado, isso era uma falha esperada: o Microsoft Lync Server 2013 não espera que você atenda ao telefone se não estiver disponível para atender ao telefone.</span><span class="sxs-lookup"><span data-stu-id="47827-112">On the other hand, this was an expected failure: Microsoft Lync Server 2013 does not expect you to answer the phone if you're not available to answer the phone.</span></span> <span data-ttu-id="47827-113">Da mesma maneira, uma falha esperada ocorrerá se você tentar enviar uma mensagem instantânea a um usuário que esteja offline, ou conectado apenas a um telefone que não suporta mensagem instantânea.</span><span class="sxs-lookup"><span data-stu-id="47827-113">Likewise, an expected failure will occur if you attempt to send an instant message to a user who is offline, or is logged on only to a phone that does not support instant messaging.</span></span>

  - <span data-ttu-id="47827-114">**Falha inesperada**.</span><span class="sxs-lookup"><span data-stu-id="47827-114">**Unexpected failure**.</span></span> <span data-ttu-id="47827-115">Um erro inesperado é exatamente o que o nome sugere: um erro que, baseado nas circunstâncias, você não espera.</span><span class="sxs-lookup"><span data-stu-id="47827-115">An unexpected error is exactly what the name implies: an error that, based on the circumstances, you would not expect to occur.</span></span> <span data-ttu-id="47827-116">Por exemplo, suponha que você ligue para alguém e essa pessoa está disponível para atender a chamada; no entanto, quando o Lync Server 2013 tenta encaminhar sua chamada para o correio de voz, a chamada falha porque a conectividade com a Unificação de mensagens do Exchange foi perdida.</span><span class="sxs-lookup"><span data-stu-id="47827-116">For example, suppose you call someone and that person is available to answer the call; however, when Lync Server 2013 tries to route your call to voicemail the call fails because connectivity to Exchange Unified Messaging has been lost.</span></span> <span data-ttu-id="47827-117">Isso é um erro inesperado: você espera que as chamadas sejam sempre roteadas para o correio de voz.</span><span class="sxs-lookup"><span data-stu-id="47827-117">That's an unexpected error: you would expect that calls could always be routed to voicemail.</span></span> <span data-ttu-id="47827-118">Como regra geral, falhas inesperadas são verdadeiras falhas: elas são problemas que provavelmente não podem ser corrigidos por meio da educação do usuário ou por medidas parecidas.</span><span class="sxs-lookup"><span data-stu-id="47827-118">As a general rule, unexpected failures are true failures: they are problems that likely cannot be remedied through user education or similar measures.</span></span>

<span data-ttu-id="47827-p104">Observe que talvez as métricas Sucesso, Falha esperada e Falha inesperada não acrescentem à métrica Total de sessões. Por exemplo, na ilustração anterior, temos os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="47827-p104">Note that the Success, Expected failure, and Unexpected failure metrics might not add up to the Total sessions metric. For example, in the preceding illustration, we have the following values:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="47827-121">Êxitos</span><span class="sxs-lookup"><span data-stu-id="47827-121">Successes</span></span></th>
<th><span data-ttu-id="47827-122">Falhas esperadas</span><span class="sxs-lookup"><span data-stu-id="47827-122">Expected failures</span></span></th>
<th><span data-ttu-id="47827-123">Falhas inesperadas</span><span class="sxs-lookup"><span data-stu-id="47827-123">Unexpected failures</span></span></th>
<th><span data-ttu-id="47827-124">Total de sessões</span><span class="sxs-lookup"><span data-stu-id="47827-124">Total sessions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47827-125">2024</span><span class="sxs-lookup"><span data-stu-id="47827-125">2024</span></span></p></td>
<td><p><span data-ttu-id="47827-126">469</span><span class="sxs-lookup"><span data-stu-id="47827-126">469</span></span></p></td>
<td><p><span data-ttu-id="47827-127">16</span><span class="sxs-lookup"><span data-stu-id="47827-127">16</span></span></p></td>
<td><p><span data-ttu-id="47827-128">2521</span><span class="sxs-lookup"><span data-stu-id="47827-128">2521</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="47827-129">Se você adicionar 2024 + 469 + 16 terá um total de 2.509 sessões, ainda assim a coluna Total de sessões mostrará um total de 2.521 sessões.</span><span class="sxs-lookup"><span data-stu-id="47827-129">If you add 2024 + 469 + 16 you get a total of 2,509 sessions, yet the Total sessions column shows a total of 2,521 sessions.</span></span> <span data-ttu-id="47827-130">As 12 sessões que "faltam" são sessões que o sistema não pode categorizar como bem-sucedida ou sem sucesso.</span><span class="sxs-lookup"><span data-stu-id="47827-130">The "missing" 12 sessions are sessions that the system was unable to categorize as successful or unsuccessful.</span></span> <span data-ttu-id="47827-131">Isso, às vezes, é o caso quando um produto de terceiros introduz um novo código de diagnóstico que não é familiar ao Lync Server.</span><span class="sxs-lookup"><span data-stu-id="47827-131">That will sometimes be the case when a third-party product introduces a new diagnostic code that is unfamiliar to Lync Server.</span></span> <span data-ttu-id="47827-132">Quando isso acontece, as chamadas feitas usando esse produto, e o relatório desse código de diagnóstico, não podem sempre ser categorizados como Sucesso, Falha esperada ou Falha inesperada.</span><span class="sxs-lookup"><span data-stu-id="47827-132">When that happens, calls made using that product, and reporting that diagnostic code, cannot always be categorized as being a Success, an Expected failure, or an Unexpected failure.</span></span>

<div>

## <a name="accessing-the-peer-to-peer-activity-diagnostic-report"></a><span data-ttu-id="47827-133">Acessando o Relatório de Diagnóstico de Atividades Ponto a Ponto</span><span class="sxs-lookup"><span data-stu-id="47827-133">Accessing the Peer-to-Peer Activity Diagnostic Report</span></span>

<span data-ttu-id="47827-134">O Relatório de Diagnóstico de Atividades Ponto a Ponto é acessado a partir da home page dos Relatórios de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="47827-134">The Peer-to-Peer Diagnostic Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="47827-135">Você pode acessar o [relatório de distribuição de falha no Lync Server 2013](lync-server-2013-failure-distribution-report.md) clicando em uma das seguintes métricas:</span><span class="sxs-lookup"><span data-stu-id="47827-135">You can access the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="47827-136">Volume de falhas inesperadas</span><span class="sxs-lookup"><span data-stu-id="47827-136">Unexpected failure volume</span></span>

  - <span data-ttu-id="47827-137">Volume de falhas esperadas</span><span class="sxs-lookup"><span data-stu-id="47827-137">Expected failure volume</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-peer-to-peer-activity-diagnostic-report"></a><span data-ttu-id="47827-138">Fazendo o melhor uso do Relatório de Diagnóstico de Atividades Ponto a Ponto</span><span class="sxs-lookup"><span data-stu-id="47827-138">Making the Best Use of the Peer-to-Peer Activity Diagnostic Report</span></span>

<span data-ttu-id="47827-p107">Há diversas maneiras de usar filtrar o Relatório de Diagnóstico de Atividades Ponto a Ponto, mas, por padrão, essas opções de filtragem ficam ocultas. Para exibir as opções de filtragem disponíveis, clique no botão Mostrar/Ocultar Parâmetros no canto superior direito da janela de relatório. Depois de fazer isso, as opções de filtragem ficarão disponíveis para uso.</span><span class="sxs-lookup"><span data-stu-id="47827-p107">There are a number of ways you can filter the Peer-to-Peer Activity Diagnostic Report but, by default, those filtering options are hidden from view. To view the filtering options available to you, click the Show/Hide Parameters button in the upper right-hand corner of the report window. Once you do that the filtering options will be available for use.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="47827-142">Filtros</span><span class="sxs-lookup"><span data-stu-id="47827-142">Filters</span></span>

<span data-ttu-id="47827-p108">Filtros oferecem uma maneira de você retornar um conjunto de dados mais preciso ou visualizar os dados retornados de maneiras diferentes. Por exemplo, o Relatório de Diagnóstico de Atividade Ponto-a-Ponto permite que você filtre tais coisas como a modalidade de sessão (por exemplo, mensagens instantâneas, transferência de arquivos ou compartilhamento de arquivos). Você pode escolher também como os dados devem ser agrupados. Neste caso, as chamadas são agrupadas por hora, dia, semana ou mês.</span><span class="sxs-lookup"><span data-stu-id="47827-p108">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Peer-to-Peer Activity Diagnostic Report enables you to filter on such things as the session modality (for example, instant messaging, file transfer, or application sharing). You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="47827-147">A tabela a seguir lista os filtros que você pode utilizar com o Relatório de Diagnóstico de Atividade Ponto-a-Ponto.</span><span class="sxs-lookup"><span data-stu-id="47827-147">The following table lists the filters that you can use with the Peer-to-Peer Activity Diagnostic Report.</span></span>

### <a name="peer-to-peer-activity-diagnostic-report-filters"></a><span data-ttu-id="47827-148">Filtros de Relatório de Diagnóstico de Atividade Ponto-a-Ponto</span><span class="sxs-lookup"><span data-stu-id="47827-148">Peer-to-Peer Activity Diagnostic Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="47827-149">Nome</span><span class="sxs-lookup"><span data-stu-id="47827-149">Name</span></span></th>
<th><span data-ttu-id="47827-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="47827-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47827-151"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="47827-151"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="47827-p109">Data/hora de início para o intervalo de tempo. Para ver os dados por horas, insira a data e hora de início conforme segue:</span><span class="sxs-lookup"><span data-stu-id="47827-p109">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="47827-154">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="47827-154">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="47827-p110">Se você não inserir a hora de início, o relatório começará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="47827-p110">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="47827-157">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="47827-157">7/7/2012</span></span></p>
<p><span data-ttu-id="47827-158">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="47827-158">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="47827-159">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="47827-159">7/3/2012</span></span></p>
<p><span data-ttu-id="47827-160">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="47827-160">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47827-161"><strong>Até</strong></span><span class="sxs-lookup"><span data-stu-id="47827-161"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="47827-p111">Data/hora final de intervalo de tempo. Para ver os dados por horas, insira a data e hora final conforme segue:</span><span class="sxs-lookup"><span data-stu-id="47827-p111">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="47827-164">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="47827-164">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="47827-p112">Se você não inserir a hora final, o relatório terminará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="47827-p112">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="47827-167">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="47827-167">7/7/2012</span></span></p>
<p><span data-ttu-id="47827-168">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="47827-168">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="47827-169">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="47827-169">7/3/2012</span></span></p>
<p><span data-ttu-id="47827-170">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="47827-170">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47827-171"><strong>Intervalo</strong></span><span class="sxs-lookup"><span data-stu-id="47827-171"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="47827-p113">Intervalo de tempo. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="47827-p113">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="47827-174">Por hora (é possível exibir no máximo 25 horas)</span><span class="sxs-lookup"><span data-stu-id="47827-174">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="47827-175">Diariamente (é possível exibir no máximo 31 dias)</span><span class="sxs-lookup"><span data-stu-id="47827-175">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="47827-176">Semanalmente (é possível exibir no máximo 12 semanas)</span><span class="sxs-lookup"><span data-stu-id="47827-176">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="47827-177">Mensalmente (é possível exibir no máximo 12 meses)</span><span class="sxs-lookup"><span data-stu-id="47827-177">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="47827-178">Se as datas de início e término excederem o número máximo de valores permitidos para o intervalo selecionado, somente o número máximo de valores (a partir da data de início) será exibido.</span><span class="sxs-lookup"><span data-stu-id="47827-178">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="47827-179">Por exemplo, se você selecionar o intervalo diário com uma data de início de 7/7/2012 e uma data de término de 2/28/2012, os dados serão exibidos para os dias 8/7/2012 12:00 AM a 9/7/2012 12:00 AM (ou seja, um total de 31 dias da importância dos dados).</span><span class="sxs-lookup"><span data-stu-id="47827-179">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47827-180"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="47827-180"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="47827-p115">FQDN (Nome de domínio totalmente qualificado) do pool de Registradores ou Servidor de Borda. Você pode selecionar um pool individual ou clicar em <strong>[Tudo]</strong> para ver os dados de todos os pools. Essa lista suspensa é automaticamente preenchida para você com base nos registros no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="47827-p115">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47827-184"><strong>Modalidade</strong></span><span class="sxs-lookup"><span data-stu-id="47827-184"><strong>Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="47827-p116">Indica o tipo de atividade de comunicação que ocorreu. Selecione um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="47827-p116">Indicates the type of communication activity that took place. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="47827-187">[Todos]</span><span class="sxs-lookup"><span data-stu-id="47827-187">[All]</span></span></p></li>
<li><p><span data-ttu-id="47827-188">Mensagens instantâneas</span><span class="sxs-lookup"><span data-stu-id="47827-188">Instant messaging</span></span></p></li>
<li><p><span data-ttu-id="47827-189">Transferência de arquivos</span><span class="sxs-lookup"><span data-stu-id="47827-189">File transfer</span></span></p></li>
<li><p><span data-ttu-id="47827-190">Compartilhamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="47827-190">Application sharing</span></span></p></li>
<li><p><span data-ttu-id="47827-191">Áudio</span><span class="sxs-lookup"><span data-stu-id="47827-191">Audio</span></span></p></li>
<li><p><span data-ttu-id="47827-192">Vídeo</span><span class="sxs-lookup"><span data-stu-id="47827-192">Video</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-per-modality"></a><span data-ttu-id="47827-193">Medidas (por modalidade)</span><span class="sxs-lookup"><span data-stu-id="47827-193">Metrics (per modality)</span></span>

<span data-ttu-id="47827-194">A tabela a seguir lista as informações oferecidas no Relatório de Diagnóstico de Atividades Ponto-a-Ponto para cada modalidade.</span><span class="sxs-lookup"><span data-stu-id="47827-194">The following table lists the information provided in the Peer-to-Peer Activity Diagnostic Report for each modality.</span></span>

### <a name="metrics-per-modality"></a><span data-ttu-id="47827-195">Medidas (por modalidade)</span><span class="sxs-lookup"><span data-stu-id="47827-195">Metrics (per modality)</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="47827-196">Nome</span><span class="sxs-lookup"><span data-stu-id="47827-196">Name</span></span></th>
<th><span data-ttu-id="47827-197">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="47827-197">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="47827-198">Descrição</span><span class="sxs-lookup"><span data-stu-id="47827-198">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47827-199"><strong>Volume de sucesso</strong></span><span class="sxs-lookup"><span data-stu-id="47827-199"><strong>Success volume</strong></span></span></p></td>
<td><p><span data-ttu-id="47827-200">Não</span><span class="sxs-lookup"><span data-stu-id="47827-200">No</span></span></p></td>
<td><p><span data-ttu-id="47827-201">Número total de sessões ponto-a-ponto com êxito.</span><span class="sxs-lookup"><span data-stu-id="47827-201">Total number of successful peer-to-peer sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47827-202"><strong>Porcentagem de sucesso</strong></span><span class="sxs-lookup"><span data-stu-id="47827-202"><strong>Success percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="47827-203">Não</span><span class="sxs-lookup"><span data-stu-id="47827-203">No</span></span></p></td>
<td><p><span data-ttu-id="47827-p117">Porcentagem de sessões ponto-a-ponto completas com problemas significativos. Calculado dividindo o Volume de sucesso pelo Total de sessões.</span><span class="sxs-lookup"><span data-stu-id="47827-p117">Percentage of peer-to-peer sessions that completed with significant problems. Calculated by dividing the Success volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47827-206"><strong>Volume de falhas esperadas</strong></span><span class="sxs-lookup"><span data-stu-id="47827-206"><strong>Expected failure volume</strong></span></span></p></td>
<td><p><span data-ttu-id="47827-207">Não</span><span class="sxs-lookup"><span data-stu-id="47827-207">No</span></span></p></td>
<td><p><span data-ttu-id="47827-208">Número total de sessões em que &quot; ocorreu uma falha esperada &quot; .</span><span class="sxs-lookup"><span data-stu-id="47827-208">Total number of sessions where an &quot;expected failure&quot; occurred.</span></span></p>
<p><span data-ttu-id="47827-p118">Uma falha esperada é quando se sabe que a falha ocorrerá. Por exemplo, se um usuário tiver definido seu status como Não perturbe, é esperado que qualquer chamada para esse usuário falhe.</span><span class="sxs-lookup"><span data-stu-id="47827-p118">An expected failure is a failure that is expected to happen. For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47827-211"><strong>Percentual de falhas esperadas</strong></span><span class="sxs-lookup"><span data-stu-id="47827-211"><strong>Expected failure percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="47827-212">Não</span><span class="sxs-lookup"><span data-stu-id="47827-212">No</span></span></p></td>
<td><p><span data-ttu-id="47827-p119">Porcentagem de sessões ponto-a-ponto que tiveram um erro esperado. Calculado dividindo o Volume de falhas esperadas pelo Total de sessões.</span><span class="sxs-lookup"><span data-stu-id="47827-p119">Percentage of peer-to-peer sessions that experienced an expected error. Calculated by dividing the Expected failure volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47827-215"><strong>Volume de falhas inesperadas</strong></span><span class="sxs-lookup"><span data-stu-id="47827-215"><strong>Unexpected failure volume</strong></span></span></p></td>
<td><p><span data-ttu-id="47827-216">Não</span><span class="sxs-lookup"><span data-stu-id="47827-216">No</span></span></p></td>
<td><p><span data-ttu-id="47827-217">Número total de sessões em que &quot; ocorreu uma falha inesperada &quot; .</span><span class="sxs-lookup"><span data-stu-id="47827-217">Total number of sessions where an &quot;unexpected failure&quot; occurred.</span></span></p>
<p><span data-ttu-id="47827-p120">Uma falha inesperada é uma falha que ocorre no que aparenta ser um sistema íntegro. Por exemplo, uma chamada não deve ser encerrada se o chamador for colocado em espera. Se isso ocorrer, isso seria sinalizado como uma falha inesperada.</span><span class="sxs-lookup"><span data-stu-id="47827-p120">An unexpected failure is a failure that occurs in what would appear to be an otherwise healthy system. For example, a call should not be terminated if the caller is placed on hold. If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47827-221"><strong>Percentual de falhas inesperadas</strong></span><span class="sxs-lookup"><span data-stu-id="47827-221"><strong>Unexpected failure percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="47827-222">Não</span><span class="sxs-lookup"><span data-stu-id="47827-222">No</span></span></p></td>
<td><p><span data-ttu-id="47827-p121">Porcentagem de sessões ponto-a-ponto nas quais um erro inesperado ocorreu. Calculado dividindo o Volume de falhas inesperadas pelo Total de sessões.</span><span class="sxs-lookup"><span data-stu-id="47827-p121">Percentage of peer-to-peer sessions that experienced an unexpected error. Calculated by dividing the Unexpected failure volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47827-225"><strong>Total de sessões</strong></span><span class="sxs-lookup"><span data-stu-id="47827-225"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="47827-226">Não</span><span class="sxs-lookup"><span data-stu-id="47827-226">No</span></span></p></td>
<td><p><span data-ttu-id="47827-227">Número total de sessões, incluindo sessões bem-sucedidas, com falha (tanto falhas esperadas quanto inesperadas) e sessões não categorizadas.</span><span class="sxs-lookup"><span data-stu-id="47827-227">Total number of sessions, including successful sessions, failed sessions (both expected failures and unexpected failures), and uncategorized sessions.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="47827-228">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="47827-228">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

