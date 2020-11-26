---
title: 'Lync Server 2013: relatório de distribuição de falha'
description: 'Lync Server 2013: relatório de distribuição de falha.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failure Distribution Report
ms:assetid: 365c7beb-24d4-40f5-92e7-4978b9688916
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558635(v=OCS.15)
ms:contentKeyID: 48183849
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5a87f779f87d6b7002fa108f1969c33739eed9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428213"
---
# <a name="failure-distribution-report-in-lync-server-2013"></a><span data-ttu-id="f2f11-103">Relatório de distribuição de falha no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2f11-103">Failure Distribution Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f2f11-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f2f11-104">

<span> </span></span></span>

<span data-ttu-id="f2f11-105">_**Tópico da última modificação:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="f2f11-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="f2f11-106">O Relatório de Distribuição de Falhas classifica sessões com falha nas seguintes categorias:</span><span class="sxs-lookup"><span data-stu-id="f2f11-106">The Failure Distribution Report ranks failed sessions in the following categories:</span></span>

  - <span data-ttu-id="f2f11-107">Principais motivos diagnósticos</span><span class="sxs-lookup"><span data-stu-id="f2f11-107">Top diagnostic reasons</span></span>

  - <span data-ttu-id="f2f11-108">Principais modalidades</span><span class="sxs-lookup"><span data-stu-id="f2f11-108">Top modalities</span></span>

  - <span data-ttu-id="f2f11-109">Principais pools</span><span class="sxs-lookup"><span data-stu-id="f2f11-109">Top pools</span></span>

  - <span data-ttu-id="f2f11-110">Principais fontes</span><span class="sxs-lookup"><span data-stu-id="f2f11-110">Top sources</span></span>

  - <span data-ttu-id="f2f11-111">Principais componentes</span><span class="sxs-lookup"><span data-stu-id="f2f11-111">Top components</span></span>

  - <span data-ttu-id="f2f11-112">Principais usuários "De"</span><span class="sxs-lookup"><span data-stu-id="f2f11-112">Top from users</span></span>

  - <span data-ttu-id="f2f11-113">Principais usuários "Para"</span><span class="sxs-lookup"><span data-stu-id="f2f11-113">Top to users</span></span>

  - <span data-ttu-id="f2f11-114">Principais agentes do usuário "De"</span><span class="sxs-lookup"><span data-stu-id="f2f11-114">Top from user agents</span></span>

<span data-ttu-id="f2f11-p101">É possível usar essas categorias para determinar exatamente onde está ocorrendo um problema e, em alguns casos, porque o problema está ocorrendo. Por exemplo, suponha que você tenha registrado 242 sessões de áudio/vídeo com falha durante um determinado dia. Se você observar o Relatório de Distribuição de Falhas, ele poderá mostrar que 237 das sessões com falha ocorreram no pool de Dublin. Isso fornece um ótimo ponto inicial para rastrear e diagnosticar as causas por trás dessas falhas. Se você clicar no pool de Dublin na categoria **Principais pools**, você verá um Relatório de Distribuição de Falhas exclusivo desse pool. Será possível então começar a analisar por que o pool de Dublin enfrentou tantas dificuldades.</span><span class="sxs-lookup"><span data-stu-id="f2f11-p101">You can use these categories to determine exactly where a problem is occurring and, in some cases, why the problem is occurring. For example, suppose you recorded 242 failed audio/video sessions during a given day. If you look at the Failure Distribution Report, it might show that 237 of those failed sessions took place in your Dublin pool. That gives you a good place to start when it comes to tracking down and diagnosing the causes behind those failures. If you click on the Dublin pool under the **Top pools** category, you will see a Failure Distribution Report just for that pool. You can then begin analyzing why the Dublin pool was experiencing so many difficulties.</span></span>

<div>

## <a name="viewing-the-failure-distribution-report"></a><span data-ttu-id="f2f11-121">Exibindo o Relatório de Distribuição de Falhas</span><span class="sxs-lookup"><span data-stu-id="f2f11-121">Viewing the Failure Distribution Report</span></span>

<span data-ttu-id="f2f11-122">É possível acessar o Relatório de Distribuição de Falhas a partir de qualquer um dos seguintes relatórios clicando nas medidas **Volume de falhas esperado** ou **Volume de falhas não esperado**:</span><span class="sxs-lookup"><span data-stu-id="f2f11-122">You can access the Failure Distribution Report from any of the following reports by clicking either the **Expected failure volume** or the **Unexpected failure volume** metric:</span></span>

  - [<span data-ttu-id="f2f11-123">Relatório de falhas principais no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2f11-123">Top Failures Report in Lync Server 2013</span></span>](lync-server-2013-top-failures-report.md)

  - [<span data-ttu-id="f2f11-124">Relatório de diagnóstico de conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2f11-124">Conference Diagnostic Report in Lync Server 2013</span></span>](lync-server-2013-conference-diagnostic-report.md)

  - [<span data-ttu-id="f2f11-125">Relatório de diagnóstico de atividade ponto a ponto no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2f11-125">Peer-to-Peer Activity Diagnostic Report in Lync Server 2013</span></span>](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)

<span data-ttu-id="f2f11-126">No relatório de distribuição de falha, você pode clicar em qualquer uma das seguintes métricas para exibir o [relatório de lista de falhas no Lync Server 2013](lync-server-2013-failure-list-report.md):</span><span class="sxs-lookup"><span data-stu-id="f2f11-126">From the Failure Distribution Report, you can click any of the following metrics to view the [Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md):</span></span>

  - <span data-ttu-id="f2f11-127">Principais motivos diagnósticos (sessões)</span><span class="sxs-lookup"><span data-stu-id="f2f11-127">Top diagnostic reasons (sessions)</span></span>

  - <span data-ttu-id="f2f11-128">Principais modalidades (sessões)</span><span class="sxs-lookup"><span data-stu-id="f2f11-128">Top modalities (sessions)</span></span>

  - <span data-ttu-id="f2f11-129">Principais pools (sessões)</span><span class="sxs-lookup"><span data-stu-id="f2f11-129">Top pools (sessions)</span></span>

  - <span data-ttu-id="f2f11-130">Principais fontes (sessões)</span><span class="sxs-lookup"><span data-stu-id="f2f11-130">Top sources (sessions)</span></span>

  - <span data-ttu-id="f2f11-131">Principais componentes (sessões)</span><span class="sxs-lookup"><span data-stu-id="f2f11-131">Top components (sessions)</span></span>

  - <span data-ttu-id="f2f11-132">Principais usuários "De" (sessões)</span><span class="sxs-lookup"><span data-stu-id="f2f11-132">Top from users (sessions)</span></span>

  - <span data-ttu-id="f2f11-133">Principais usuários "Para" (sessões)</span><span class="sxs-lookup"><span data-stu-id="f2f11-133">Top to users (sessions)</span></span>

  - <span data-ttu-id="f2f11-134">Principais agentes do usuários "De" (sessões)</span><span class="sxs-lookup"><span data-stu-id="f2f11-134">Top from user agents (sessions)</span></span>

</div>

<div>

## <a name="using-the-failure-distribution-report"></a><span data-ttu-id="f2f11-135">Usando o Relatório de Distribuição de Falhas</span><span class="sxs-lookup"><span data-stu-id="f2f11-135">Using the Failure Distribution Report</span></span>

<span data-ttu-id="f2f11-p102">Dependendo do tamanho de seu monitor e da resolução da tela, é possível que alguns dos dados apresentados no Relatório de Distribuição de Falhas sejam truncados que exibidos na tela. Por exemplo, um agente de usuário com o nome "UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Lync 2013)" poderá aparecer apenas parcialmente na tela:</span><span class="sxs-lookup"><span data-stu-id="f2f11-p102">Depending on your monitor size and screen resolution, it's possible that some of the data shown in the Failure Distribution Report might be truncated when you view it onscreen. This is especially true for metrics such as user agents, which can have very long labels. For example, a user agent with a name like "UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Lync 2013)" might only partially appear onscreen:</span></span>

<span data-ttu-id="f2f11-139">UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Ly...</span><span class="sxs-lookup"><span data-stu-id="f2f11-139">UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Ly...</span></span>

<span data-ttu-id="f2f11-140">Felizmente, é possível ver o nome completo mantendo o mouse sobre o valor truncado.</span><span class="sxs-lookup"><span data-stu-id="f2f11-140">Fortunately, you can see the entire label simply by holding your mouse over the truncated value.</span></span>

<span data-ttu-id="f2f11-p103">Um medida interessante que pode ser filtrada usando o Relatório de Distribuição de Falhas é o ID do diagnóstico. Se vir o mesmo ID do diagnóstico surgir em outros relatórios, será possível filtrar esse ID no Relatório de Distribuição de Falhas e obter uma visão bastante detalhada de exatamente onde e com que frequência esse ID foi reportado durante uma sessão com falha.</span><span class="sxs-lookup"><span data-stu-id="f2f11-p103">One interesting metric that you can filter on by using the Failure Distribution Report is Diagnostic ID. If you see the same Diagnostic ID cropping up in other reports you can filter on that ID in the Failure Distribution Report and get a very detailed look at exactly where, and how often, that ID has been reported during a failed session.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="f2f11-143">Filtros</span><span class="sxs-lookup"><span data-stu-id="f2f11-143">Filters</span></span>

<span data-ttu-id="f2f11-p104">O filtro é uma maneira de retornar um conjunto de dados mais refinado e direcionado, ou ver os dados retornados de maneiras diferentes. Por exemplo, o Relatório de Falha na Distribuição permite filtrar itens como tipo de atividade (sessão ponto a ponto ou de conferência) ou pelo ID diagnóstico que acompanha cada sessão com falha.</span><span class="sxs-lookup"><span data-stu-id="f2f11-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Failed Distribution Report enables you to filter on such things as the activity type (peer-to-peer session or conferencing session) or by the diagnostic ID that accompanied each failed session.</span></span>

<span data-ttu-id="f2f11-146">A tabela a seguir lista os filtros que você pode usar com o Relatório de Falha na Distribuição.</span><span class="sxs-lookup"><span data-stu-id="f2f11-146">The following table lists the filters that you can use with the Failure Distribution Report.</span></span>

### <a name="failure-distribution-report-filters"></a><span data-ttu-id="f2f11-147">Filtros do Relatório de Falha na Distribuição</span><span class="sxs-lookup"><span data-stu-id="f2f11-147">Failure Distribution Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2f11-148">Nome</span><span class="sxs-lookup"><span data-stu-id="f2f11-148">Name</span></span></th>
<th><span data-ttu-id="f2f11-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2f11-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-150"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-150"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-p105">Data/hora de início para o intervalo de tempo. Para ver os dados por horas, insira a data e hora de início conforme segue:</span><span class="sxs-lookup"><span data-stu-id="f2f11-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="f2f11-153">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="f2f11-153">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="f2f11-p106">Se você não inserir a hora de início, o relatório começará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="f2f11-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="f2f11-156">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="f2f11-156">7/7/2012</span></span></p>
<p><span data-ttu-id="f2f11-157">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="f2f11-157">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="f2f11-158">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="f2f11-158">7/3/2012</span></span></p>
<p><span data-ttu-id="f2f11-159">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="f2f11-159">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f11-160"><strong>Até</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-160"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-p107">Data/hora final de intervalo de tempo. Para ver os dados por horas, insira a data e hora final conforme segue:</span><span class="sxs-lookup"><span data-stu-id="f2f11-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="f2f11-163">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="f2f11-163">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="f2f11-p108">Se você não inserir a hora final, o relatório terminará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="f2f11-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="f2f11-166">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="f2f11-166">7/7/2012</span></span></p>
<p><span data-ttu-id="f2f11-167">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="f2f11-167">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="f2f11-168">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="f2f11-168">7/3/2012</span></span></p>
<p><span data-ttu-id="f2f11-169">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="f2f11-169">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-170"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-170"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-p109">FQDN (Nome de domínio totalmente qualificado) do Pool de registradores ou Servidor de Borda. Você pode selecionar um pool individual ou clicar em <strong>[Todos]</strong> para ver os dados de todos os pools. Essa lista suspensa é automaticamente preenchida para você com base nos registros no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f2f11-p109">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f11-174"><strong>Tipo de atividade</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-174"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-p110">Tipo de atividade para filtrar. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="f2f11-p110">Type of activity to filter on. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="f2f11-177">[Todos]</span><span class="sxs-lookup"><span data-stu-id="f2f11-177">[All]</span></span></p></li>
<li><p><span data-ttu-id="f2f11-178">Ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="f2f11-178">Peer-to-peer</span></span></p></li>
<li><p><span data-ttu-id="f2f11-179">Conferência</span><span class="sxs-lookup"><span data-stu-id="f2f11-179">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-180"><strong>Categoria da sessão</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-180"><strong>Session category</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-p111">Indica se a atividade em questão teve sucesso ou falhou. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="f2f11-p111">Indicates whether the activity in question succeeded or failed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="f2f11-183">[Todos]</span><span class="sxs-lookup"><span data-stu-id="f2f11-183">[All]</span></span></p></li>
<li><p><span data-ttu-id="f2f11-184">Sucesso</span><span class="sxs-lookup"><span data-stu-id="f2f11-184">Success</span></span></p></li>
<li><p><span data-ttu-id="f2f11-185">Falha esperada</span><span class="sxs-lookup"><span data-stu-id="f2f11-185">Expected failure</span></span></p></li>
<li><p><span data-ttu-id="f2f11-186">Falha inesperada</span><span class="sxs-lookup"><span data-stu-id="f2f11-186">Unexpected failure</span></span></p></li>
</ul>
<p><span data-ttu-id="f2f11-187">Uma &quot; falha esperada &quot; é uma falha que espera acontecer.</span><span class="sxs-lookup"><span data-stu-id="f2f11-187">An &quot;expected failure&quot; is a failure that is expected to happen.</span></span> <span data-ttu-id="f2f11-188">Por exemplo, se um usuário tiver definido seu status como Não perturbe, é esperado que qualquer chamada para esse usuário falhe.</span><span class="sxs-lookup"><span data-stu-id="f2f11-188">For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span> <span data-ttu-id="f2f11-189">Uma &quot; falha inesperada &quot; é uma falha que ocorre em que parece ser um sistema de outra forma saudável.</span><span class="sxs-lookup"><span data-stu-id="f2f11-189">An &quot;unexpected failure&quot; is a failure that occurs in what would appear to be an otherwise healthy system.</span></span> <span data-ttu-id="f2f11-190">Por exemplo, uma chamada não deve ser encerrada se o chamador for colocado em espera.</span><span class="sxs-lookup"><span data-stu-id="f2f11-190">For example, a call should not be terminated if the caller is placed on hold.</span></span> <span data-ttu-id="f2f11-191">Se isso ocorrer, isso seria sinalizado como uma falha inesperada.</span><span class="sxs-lookup"><span data-stu-id="f2f11-191">If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f11-192"><strong>ID do Diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-192"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-p113">Identificador exclusivo (na forma de um cabeçalho de diagnóstico-ms) anexado a uma mensagem SIP que fornece informações úteis sobre os erros de solução de problemas. Os cabeçalhos diagnósticos são opcionais (é possível ter sessões SIP que não os incluem), e os IDs diagnósticos são relatados somente para as sessões com algum tipo de problema.</span><span class="sxs-lookup"><span data-stu-id="f2f11-p113">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-diagnostic-reasons"></a><span data-ttu-id="f2f11-195">Métricas para os principais motivos diagnósticos</span><span class="sxs-lookup"><span data-stu-id="f2f11-195">Metrics for Top Diagnostic Reasons</span></span>

<span data-ttu-id="f2f11-196">A tabela a seguir lista as informações fornecidas no Relatório de Falha de Distribuição, com base no ID diagnóstico relatado com mais frequência.</span><span class="sxs-lookup"><span data-stu-id="f2f11-196">The following table lists the information provided in the Failure Distribution Report based on the most frequently reported diagnostic ID.</span></span>

### <a name="metrics-for-top-diagnostic-reasons"></a><span data-ttu-id="f2f11-197">Métricas para os principais motivos diagnósticos</span><span class="sxs-lookup"><span data-stu-id="f2f11-197">Metrics for Top Diagnostic Reasons</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2f11-198">Nome</span><span class="sxs-lookup"><span data-stu-id="f2f11-198">Name</span></span></th>
<th><span data-ttu-id="f2f11-199">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="f2f11-199">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f2f11-200">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2f11-200">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-201"><strong>Classificação</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-201"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-202">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-202">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-p114">Classificação relativa das sessões com falha, com base no ID diagnóstico, que é um identificador exclusivo (na forma de um cabeçalho de diagnóstico-ms) anexado a uma mensagem SIP que fornece informações úteis sobre os erros de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="f2f11-p114">Relative ranking of failed sessions based on diagnostic IDs. The diagnostic ID is a unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f11-205"><strong>Principais motivos diagnósticos</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-205"><strong>Top diagnostic reasons</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-206">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-206">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-207">ID diagnóstico gerado em uma sessão.</span><span class="sxs-lookup"><span data-stu-id="f2f11-207">Diagnostic ID generated in a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-208"><strong>Sessões</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-208"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-209">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-209">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-210">Número total de sessões com falha em que ID diagnóstico especificado foi gerado.</span><span class="sxs-lookup"><span data-stu-id="f2f11-210">Total number of failed sessions where the specified diagnostic ID was generated.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-modalities"></a><span data-ttu-id="f2f11-211">Métricas para as principais modalidades</span><span class="sxs-lookup"><span data-stu-id="f2f11-211">Metrics for Top Modalities</span></span>

<span data-ttu-id="f2f11-212">A tabela a seguir lista as informações fornecidas no Relatório de Falha de Distribuição, com base nas modalidades de sessão que apresentaram mais falhas.</span><span class="sxs-lookup"><span data-stu-id="f2f11-212">The following table lists the information provided in the Failure Distribution Report based on the session modalities that experienced the most failures.</span></span>

### <a name="metrics-for-top-modalities"></a><span data-ttu-id="f2f11-213">Métricas para as principais modalidades</span><span class="sxs-lookup"><span data-stu-id="f2f11-213">Metrics for Top Modalities</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2f11-214">Nome</span><span class="sxs-lookup"><span data-stu-id="f2f11-214">Name</span></span></th>
<th><span data-ttu-id="f2f11-215">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="f2f11-215">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f2f11-216">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2f11-216">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-217"><strong>Classificação</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-217"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-218">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-218">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-219">Classificação relativa com base na sessão com falha baseada no tipo de sessão (por exemplo, conferência de áudio/vídeo ou sessão de transferência de arquivo ponto a ponto).</span><span class="sxs-lookup"><span data-stu-id="f2f11-219">Relative ranking based of failed session based on session type (for example, an audio/video conference or a peer-to-peer file transfer session).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f11-220"><strong>Principais modalidades</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-220"><strong>Top modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-221">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-221">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-222">Tipo de sessão.</span><span class="sxs-lookup"><span data-stu-id="f2f11-222">Session type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-223"><strong>Sessões</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-223"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-224">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-224">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-225">Número total de sessões com falha envolvendo a modalidade especificada.</span><span class="sxs-lookup"><span data-stu-id="f2f11-225">Total number of failed sessions involving the specified modality.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-pools"></a><span data-ttu-id="f2f11-226">Métricas para os principais pools</span><span class="sxs-lookup"><span data-stu-id="f2f11-226">Metrics for Top Pools</span></span>

<span data-ttu-id="f2f11-227">A tabela a seguir lista as informações fornecidas no Relatório de Falha de Distribuição, com base nos pools que apresentaram mais falhas.</span><span class="sxs-lookup"><span data-stu-id="f2f11-227">The following table lists the information provided in the Failure Distribution Report based on the pools that experienced the most failures.</span></span>

### <a name="metrics-for-top-pools"></a><span data-ttu-id="f2f11-228">Métricas para os principais pools</span><span class="sxs-lookup"><span data-stu-id="f2f11-228">Metrics for Top Pools</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2f11-229">Nome</span><span class="sxs-lookup"><span data-stu-id="f2f11-229">Name</span></span></th>
<th><span data-ttu-id="f2f11-230">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="f2f11-230">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f2f11-231">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2f11-231">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-232"><strong>Classificação</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-232"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-233">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-233">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-234">Classificação relativa de sessões com falha com base no pool de registradores ou no servidor de borda em que a sessão foi conduzida.</span><span class="sxs-lookup"><span data-stu-id="f2f11-234">Relative ranking of failed sessions based on the Registrar pool or Edge Server where the session was conducted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f11-235"><strong>Principais pools</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-235"><strong>Top pools</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-236">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-236">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-237">Nome do pool de registradores ou servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="f2f11-237">Name of the Registrar pool or Edge Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-238"><strong>Sessões</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-238"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-239">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-239">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-240">Número total de sessões com falha por pool de registradores ou servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="f2f11-240">Total number of failed sessions per Registrar pool or Edge Server.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-sources"></a><span data-ttu-id="f2f11-241">Métricas para as principais fontes</span><span class="sxs-lookup"><span data-stu-id="f2f11-241">Metrics for Top Sources</span></span>

<span data-ttu-id="f2f11-242">A tabela a seguir lista as informações fornecidas no Relatório de Falha de Distribuição, com base nos computadores que apresentaram mais falhas.</span><span class="sxs-lookup"><span data-stu-id="f2f11-242">The following table lists the information provided in the Failure Distribution Report based on the computers that experienced the most failures.</span></span>

### <a name="metrics-for-top-sources"></a><span data-ttu-id="f2f11-243">Métricas para as principais fontes</span><span class="sxs-lookup"><span data-stu-id="f2f11-243">Metrics for Top Sources</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2f11-244">Nome</span><span class="sxs-lookup"><span data-stu-id="f2f11-244">Name</span></span></th>
<th><span data-ttu-id="f2f11-245">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="f2f11-245">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f2f11-246">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2f11-246">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-247"><strong>Classificação</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-247"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-248">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-248">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-249">Classificação relativa das sessões com falha por computador.</span><span class="sxs-lookup"><span data-stu-id="f2f11-249">Relative ranking failed sessions per computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f11-250"><strong>Principais fontes</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-250"><strong>Top sources</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-251">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-251">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-252">Nome do computador envolvido na sessão com falha.</span><span class="sxs-lookup"><span data-stu-id="f2f11-252">Name of the computer involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-253"><strong>Sessões</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-253"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-254">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-254">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-255">Número total de sessões com falha por computador.</span><span class="sxs-lookup"><span data-stu-id="f2f11-255">Total number of failed sessions per computer.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-components"></a><span data-ttu-id="f2f11-256">Métricas para os principais componentes</span><span class="sxs-lookup"><span data-stu-id="f2f11-256">Metrics for Top Components</span></span>

<span data-ttu-id="f2f11-257">A tabela a seguir lista as informações fornecidas no relatório de distribuição de falha com base nos componentes do Microsoft Lync Server 2010 que tiveram mais falhas.</span><span class="sxs-lookup"><span data-stu-id="f2f11-257">The following table lists the information provided in the Failure Distribution Report based on the Microsoft Lync Server 2010 components that experienced the most failures.</span></span>

### <a name="metrics-for-top-components"></a><span data-ttu-id="f2f11-258">Métricas para os principais componentes</span><span class="sxs-lookup"><span data-stu-id="f2f11-258">Metrics for Top Components</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2f11-259">Nome</span><span class="sxs-lookup"><span data-stu-id="f2f11-259">Name</span></span></th>
<th><span data-ttu-id="f2f11-260">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="f2f11-260">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f2f11-261">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2f11-261">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-262"><strong>Classificação</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-262"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-263">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-263">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-264">Classificação relativa de sessões com falha com base no componente do Lync Server 2010 (por exemplo, ExumRouting, GroupChat ou MediationServer).</span><span class="sxs-lookup"><span data-stu-id="f2f11-264">Relative ranking of failed sessions based on Lync Server 2010 component (for example, ExumRouting, GroupChat, or MediationServer).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f11-265"><strong>Principais componentes</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-265"><strong>Top components</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-266">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-266">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-267">Nome do componente envolvido na sessão com falha.</span><span class="sxs-lookup"><span data-stu-id="f2f11-267">Name of the component involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-268"><strong>Sessões</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-268"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-269">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-269">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-270">Número total de sessões com falha por componente.</span><span class="sxs-lookup"><span data-stu-id="f2f11-270">Total number of failed sessions per component.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-from-users"></a><span data-ttu-id="f2f11-271">Métricas para os principais usuários "Para"</span><span class="sxs-lookup"><span data-stu-id="f2f11-271">Metrics for Top From Users</span></span>

<span data-ttu-id="f2f11-272">A tabela a seguir lista as informações fornecidas no Relatório de Falha de Distribuição, com base nos usuários que apresentaram mais falhas quando tentaram chamar alguém (conhecidos como usuários "De").</span><span class="sxs-lookup"><span data-stu-id="f2f11-272">The following table lists the information provided in the Failure Distribution Report based on users who experienced the most failures when they tried to call someone else (known as "From" users).</span></span>

### <a name="metrics-for-top-from-users"></a><span data-ttu-id="f2f11-273">Métricas para os principais usuários "Para"</span><span class="sxs-lookup"><span data-stu-id="f2f11-273">Metrics for Top From Users</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2f11-274">Nome</span><span class="sxs-lookup"><span data-stu-id="f2f11-274">Name</span></span></th>
<th><span data-ttu-id="f2f11-275">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="f2f11-275">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f2f11-276">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2f11-276">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-277"><strong>Classificação</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-277"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-278">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-278">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-279">Classificação relativa das sessões com falha, com base no usuário convidado a entrar na sessão.</span><span class="sxs-lookup"><span data-stu-id="f2f11-279">Relative ranking of failed sessions based on the user who was invited to join the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f11-280"><strong>Principais usuários "De"</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-280"><strong>Top from users</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-281">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-281">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-282">Endereço SIP do usuário convidado para entrar na sessão.</span><span class="sxs-lookup"><span data-stu-id="f2f11-282">SIP address of the user invited to join the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-283"><strong>Sessões</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-283"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-284">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-284">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-285">Número total de sessões com falha por usuário.</span><span class="sxs-lookup"><span data-stu-id="f2f11-285">Total number of failed sessions per user.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-to-users"></a><span data-ttu-id="f2f11-286">Métricas para os principais usuários</span><span class="sxs-lookup"><span data-stu-id="f2f11-286">Metrics for Top To Users</span></span>

<span data-ttu-id="f2f11-287">A tabela a seguir lista as informações fornecidas no Relatório de Falha de Distribuição, com base nos usuários que apresentaram mais falhas quando o outro usuário tentou chamá-los (conhecidos como usuários "Para").</span><span class="sxs-lookup"><span data-stu-id="f2f11-287">The following table lists the information provided in the Failure Distribution Report based on the users who experienced the most failures when another user tried to call them (known as "To" users).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2f11-288">Nome</span><span class="sxs-lookup"><span data-stu-id="f2f11-288">Name</span></span></th>
<th><span data-ttu-id="f2f11-289">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="f2f11-289">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f2f11-290">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2f11-290">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-291"><strong>Classificação</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-291"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-292">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-292">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-293">Classificação relativa das sessões com falha, com base no usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="f2f11-293">Relative ranking of failed sessions based on the user who initiated the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f11-294"><strong>Principais usuários "Para"</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-294"><strong>Top to users</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-295">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-295">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-296">Endereço SIP do usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="f2f11-296">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-297"><strong>Sessões</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-297"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-298">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-298">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-299">Número total de sessões com falha por usuário.</span><span class="sxs-lookup"><span data-stu-id="f2f11-299">Total number of failed sessions per user.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-user-agents"></a><span data-ttu-id="f2f11-300">Métricas para os principais agentes do usuário</span><span class="sxs-lookup"><span data-stu-id="f2f11-300">Metrics for Top User Agents</span></span>

<span data-ttu-id="f2f11-301">A tabela a seguir lista as informações fornecidas no Relatório de Falha de Distribuição, com base no software de ponto de extremidade que apresentou mais falhas.</span><span class="sxs-lookup"><span data-stu-id="f2f11-301">The following table lists the information provided in the Failure Distribution Report based on the endpoint software that experienced the most failures.</span></span>

### <a name="metrics-for-top-user-agents"></a><span data-ttu-id="f2f11-302">Métricas para os principais agentes do usuário</span><span class="sxs-lookup"><span data-stu-id="f2f11-302">Metrics for Top User Agents</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2f11-303">Nome</span><span class="sxs-lookup"><span data-stu-id="f2f11-303">Name</span></span></th>
<th><span data-ttu-id="f2f11-304">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="f2f11-304">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f2f11-305">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2f11-305">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-306"><strong>Classificação</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-306"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-307">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-307">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-p115">Classificação relativa de sessões com falha, com base no agente do usuário (software) envolvido na sessão. Por exemplo: RTCC/4.0.0.0 Inbound Routing/4.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="f2f11-p115">Relative ranking of failed sessions based on the user agent (software) involved in the session. For example: RTCC/4.0.0.0 Inbound Routing/4.0.0.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f11-310"><strong>Principais agentes do usuário</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-310"><strong>Top user agents</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-311">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-311">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-312">Nome do agente do usuário envolvido na sessão com falha.</span><span class="sxs-lookup"><span data-stu-id="f2f11-312">Name of the user agent involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f11-313"><strong>Sessões</strong></span><span class="sxs-lookup"><span data-stu-id="f2f11-313"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f11-314">Não</span><span class="sxs-lookup"><span data-stu-id="f2f11-314">No</span></span></p></td>
<td><p><span data-ttu-id="f2f11-315">Número total de sessões com falha por agente do usuário.</span><span class="sxs-lookup"><span data-stu-id="f2f11-315">Total number of failed sessions per user agent.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f2f11-316">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f2f11-316">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

