---
title: 'Lync Server 2013: relatório de falhas principais'
description: 'Lync Server 2013: relatório de falhas principais.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Top Failures Report
ms:assetid: 438942e2-580a-4b67-9d42-f116111fb26a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558640(v=OCS.15)
ms:contentKeyID: 48184021
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 768c9a99916dece9eb76877b0cd65b057697ff95
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440910"
---
# <a name="top-failures-report-in-lync-server-2013"></a><span data-ttu-id="6901c-103">Relatório de falhas principais no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6901c-103">Top Failures Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6901c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6901c-104">

<span> </span></span></span>

<span data-ttu-id="6901c-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="6901c-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="6901c-p101">O Relatório de Falhas Principais apresenta uma noção das falhas mais frequentemente relatadas e suas tendências ao longo do tempo. As falhas são baseadas em uma combinação das seguintes métricas:</span><span class="sxs-lookup"><span data-stu-id="6901c-p101">The Top Failures Report provides a look at the most-commonly reported failures and their trends over time. Failures are based on a combination of the following two metrics:</span></span>

  - <span data-ttu-id="6901c-p102">**ID de Diagnóstico**. Identificador único (na forma de um cabeçalho ms-diagnostics) que é anexado a uma mensagem SIP. As IDs de Diagnóstico fornecem informações úteis na solução de problemas relacionados a chamadas.</span><span class="sxs-lookup"><span data-stu-id="6901c-p102">**Diagnostic ID**. Unique identifier (in the form of an ms-diagnostics header) that is attached to a SIP message. Diagnostic IDs provide information useful in troubleshooting call-related problems.</span></span>

  - <span data-ttu-id="6901c-111">**Código de resposta**.</span><span class="sxs-lookup"><span data-stu-id="6901c-111">**Response code**.</span></span> <span data-ttu-id="6901c-112">Os códigos de resposta são utilizados nas sessões de comunicação SIP para responder solicitações SIP.</span><span class="sxs-lookup"><span data-stu-id="6901c-112">Response codes are used in SIP communication sessions to respond to SIP requests.</span></span> <span data-ttu-id="6901c-113">Por exemplo, suponha que Ken envie a solicitação INVITE a Pilar Ackerman (isto é, suponha que Ken Myer ligue para Pilar Ackerman).</span><span class="sxs-lookup"><span data-stu-id="6901c-113">For example, suppose Ken sends the INVITE request to Pilar Ackerman (that is, suppose Ken Myer calls Pilar Ackerman).</span></span> <span data-ttu-id="6901c-114">Se Pilar responder, o telefone enviará o código de resposta 200 (OK), permitindo que o telefone de Ken saiba que Pilar atendeu.</span><span class="sxs-lookup"><span data-stu-id="6901c-114">If Pilar answers, her phone will send the response code 200 (OK), letting Ken's phone know that Pilar has answered.</span></span> <span data-ttu-id="6901c-115">O relatório de falhas principais inclui apenas códigos de resposta que foram enviados em resposta a uma falha de chamada; O Lync Server não mantém o controle de todos os códigos de resposta emitidos durante o curso de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="6901c-115">The Top Failures Report only includes response codes that were sent in response to a call failure; Lync Server does not keep track of all the response codes issued during the course of a call.</span></span>

<span data-ttu-id="6901c-116">A informação é relatada não apenas para o número total de sessões quando uma falha ocorre, mas também para o número total de usuários que foram impactados pela falha.</span><span class="sxs-lookup"><span data-stu-id="6901c-116">Information is reported not only for the total number of sessions where a failure occurred but also for the total number of users who were impacted by the failure.</span></span>

<div>

## <a name="accessing-the-top-failures-report"></a><span data-ttu-id="6901c-117">Acessando o Relatório de Falhas Principais</span><span class="sxs-lookup"><span data-stu-id="6901c-117">Accessing the Top Failures Report</span></span>

<span data-ttu-id="6901c-118">O Relatório de Falhas Principais é acessado a partir da home page Relatórios de Monitoramento.</span><span class="sxs-lookup"><span data-stu-id="6901c-118">The Top Failures Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="6901c-119">Clicar na métrica de sessões informadas levará você ao [relatório de distribuição de falha no Lync Server 2013](lync-server-2013-failure-distribution-report.md).</span><span class="sxs-lookup"><span data-stu-id="6901c-119">Clicking the Reported sessions metric will take you to the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md).</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-top-failures-report"></a><span data-ttu-id="6901c-120">Fazendo o melhor uso do Relatório de Falhas Principais</span><span class="sxs-lookup"><span data-stu-id="6901c-120">Making the Best Use of the Top Failures Report</span></span>

<span data-ttu-id="6901c-p105">O Relatório de Falhas Principais é incomum quanto a uma coisa: ele permite a filtragem de até 5 IDs de diagnóstico de uma vez. (Normalmente, você só pode filtrar um item, como o endereço SIP de usuário, por vez.) Para filtrar várias IDs de diagnóstico, basta inserir cada ID na caixa de ID de Diagnóstico, separando as IDs com vírgula. (Se você quiser, pode deixar um espaço em branco após cada vírgula.) Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6901c-p105">The Top Failures Report is unusual in one regard: it allows you to filter on as many as 5 diagnostic IDs at once. (Typically you can only filter on one item – such as one user SIP address – at a time.) To filter on multiple diagnostic IDs, simply enter each ID in the Diagnostic IDs box, separating the IDs by using commas. (If you want to, you can leave a blank space after each comma.) For example:</span></span>

<span data-ttu-id="6901c-124">1011, 2412, 1033, 52116, 1008</span><span class="sxs-lookup"><span data-stu-id="6901c-124">1011, 2412, 1033, 52116, 1008</span></span>

<span data-ttu-id="6901c-125">Faça isso e apenas chamadas que falharam e foram reportadas pelo menos em uma dessas cinco IDs de diagnóstico serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="6901c-125">Do that, and only failed calls that reported at least one of those five diagnostic IDs will be displayed.</span></span>

<span data-ttu-id="6901c-p106">Ao passar o mouse sobre um Código de Resposta, você verá uma dica que diz o que um Código de Resposta em questão significa. Por exemplo, se você passar o mouse sobre o Código de Resposta 486, verá esta mensagem:</span><span class="sxs-lookup"><span data-stu-id="6901c-p106">If you hold your mouse over a Response code you'll see a tooltip that tells you what the Response code in question means. For example, if you hold the mouse over the Response code 486 you'll see this message:</span></span>

<span data-ttu-id="6901c-128">Ocupado.</span><span class="sxs-lookup"><span data-stu-id="6901c-128">Busy Here.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="6901c-129">Filtros</span><span class="sxs-lookup"><span data-stu-id="6901c-129">Filters</span></span>

<span data-ttu-id="6901c-p107">Os filtros fornecem uma maneira de retornar um conjunto de dados mais direcionado ou exibir os dados retornados de diferentes maneiras. Por exemplo, o Relatório de Falhas Principais permite filtrar os dados retornados com base, por exemplo, no tipo de atividade (sessão ponto a ponto ou sessão de conferência), ou com base no código de resposta SIP que acompanhava a sessão com falha. Você também pode escolher como os dados devem ser agrupados. Nesse caso, os usos são agrupados por hora, dia, semana ou mês.</span><span class="sxs-lookup"><span data-stu-id="6901c-p107">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Top Failures Report enables you to filter the returned data based on such things as the activity type (peer-to-peer session or conferencing session) or by the SIP response code that accompanied the failed session. You can also choose how data should be grouped. In this case, usages are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="6901c-134">A tabela a seguir lista os filtros que você pode usar com o Relatório de Falhas Principais.</span><span class="sxs-lookup"><span data-stu-id="6901c-134">The following table lists the filters that you can use with the Top Failures Report.</span></span>

### <a name="top-failures-report-filters"></a><span data-ttu-id="6901c-135">Filtros de Relatório de Falhas Principais</span><span class="sxs-lookup"><span data-stu-id="6901c-135">Top Failures Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6901c-136">Nome</span><span class="sxs-lookup"><span data-stu-id="6901c-136">Name</span></span></th>
<th><span data-ttu-id="6901c-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="6901c-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6901c-138"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="6901c-138"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="6901c-p108">Data/hora de início para o intervalo de tempo. Para ver os dados por horas, insira a data e hora de início conforme segue:</span><span class="sxs-lookup"><span data-stu-id="6901c-p108">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="6901c-141">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="6901c-141">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="6901c-p109">Se você não inserir a hora de início, o relatório começará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="6901c-p109">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="6901c-144">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="6901c-144">7/7/2012</span></span></p>
<p><span data-ttu-id="6901c-145">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="6901c-145">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="6901c-146">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="6901c-146">7/3/2012</span></span></p>
<p><span data-ttu-id="6901c-147">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="6901c-147">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6901c-148"><strong>Até</strong></span><span class="sxs-lookup"><span data-stu-id="6901c-148"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="6901c-p110">Data/hora final de intervalo de tempo. Para ver os dados por horas, insira a data e hora final conforme segue:</span><span class="sxs-lookup"><span data-stu-id="6901c-p110">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="6901c-151">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="6901c-151">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="6901c-p111">Se você não inserir a hora final, o relatório terminará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="6901c-p111">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="6901c-154">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="6901c-154">7/7/2012</span></span></p>
<p><span data-ttu-id="6901c-155">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="6901c-155">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="6901c-156">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="6901c-156">7/3/2012</span></span></p>
<p><span data-ttu-id="6901c-157">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="6901c-157">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6901c-158"><strong>Tipo de atividade</strong></span><span class="sxs-lookup"><span data-stu-id="6901c-158"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="6901c-p112">Tipo de atividade. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="6901c-p112">Type of activity. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="6901c-161">[Todos]</span><span class="sxs-lookup"><span data-stu-id="6901c-161">[All]</span></span></p></li>
<li><p><span data-ttu-id="6901c-162">Ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="6901c-162">Peer-to-peer</span></span></p></li>
<li><p><span data-ttu-id="6901c-163">Conferência</span><span class="sxs-lookup"><span data-stu-id="6901c-163">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6901c-164"><strong>Modalidade</strong></span><span class="sxs-lookup"><span data-stu-id="6901c-164"><strong>Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="6901c-165">Neste momento, a única opção disponível é <strong>[Todos]</strong>.</span><span class="sxs-lookup"><span data-stu-id="6901c-165">At this time the only option available is <strong>[All]</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6901c-166"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="6901c-166"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="6901c-p113">O FQDN (nome de domínio totalmente qualificado) do pool Registrador Avançado ou Servidor de Borda. Você pode selecionar um pool individual ou clicar em <strong>[Todos]</strong> para ver os dados de todos os pools. Essa lista suspensa é preenchida automaticamente com base nos registros no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6901c-p113">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6901c-170"><strong>Categoria</strong></span><span class="sxs-lookup"><span data-stu-id="6901c-170"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="6901c-p114">Tipo de falha ocorrido. Selecione um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="6901c-p114">Type of failure experienced. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="6901c-173">Falha inesperada e esperada</span><span class="sxs-lookup"><span data-stu-id="6901c-173">Both expected and unexpected failure</span></span></p></li>
<li><p><span data-ttu-id="6901c-174">Falha inesperada</span><span class="sxs-lookup"><span data-stu-id="6901c-174">Unexpected failure</span></span></p></li>
</ul>
<p><span data-ttu-id="6901c-175">Uma &quot; falha esperada &quot; é uma falha que espera acontecer.</span><span class="sxs-lookup"><span data-stu-id="6901c-175">An &quot;expected failure&quot; is a failure that is expected to happen.</span></span> <span data-ttu-id="6901c-176">Por exemplo, se um usuário tiver definido seu status como Não perturbe, é esperado que qualquer chamada para esse usuário falhe.</span><span class="sxs-lookup"><span data-stu-id="6901c-176">For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span> <span data-ttu-id="6901c-177">Uma &quot; falha inesperada &quot; é uma falha que ocorre em que parece ser um sistema de outra forma saudável.</span><span class="sxs-lookup"><span data-stu-id="6901c-177">An &quot;unexpected failure&quot; is a failure that occurs in what would appear to be an otherwise healthy system.</span></span> <span data-ttu-id="6901c-178">Por exemplo, uma chamada não deve ser encerrada se o chamador for colocado em espera.</span><span class="sxs-lookup"><span data-stu-id="6901c-178">For example, a call should not be terminated if the caller is placed on hold.</span></span> <span data-ttu-id="6901c-179">Se isso ocorrer, a situação será sinalizada como falha inesperada.</span><span class="sxs-lookup"><span data-stu-id="6901c-179">If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6901c-180"><strong>Código de resposta</strong></span><span class="sxs-lookup"><span data-stu-id="6901c-180"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="6901c-p116">O código de resposta enviado quando a conferência falhou. Digite o código de resposta inteiro. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6901c-p116">SIP response code sent when the conference failed. Enter the entire response code For example:</span></span></p>
<p><span data-ttu-id="6901c-183">400</span><span class="sxs-lookup"><span data-stu-id="6901c-183">400</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6901c-184"><strong>ID do Diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="6901c-184"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="6901c-p117">Identificador exclusivo (na forma de um cabeçalho ms-diagnostics) anexado a uma mensagem SIP que fornece informações úteis para resolução de erros. Os cabeçalhos de diagnóstico são opcionais (é possível ter sessões SIP que não os incluem), e as IDs de diagnóstico são relatadas somente em sessões com algum tipo de problema.</span><span class="sxs-lookup"><span data-stu-id="6901c-p117">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="6901c-187">Métricas</span><span class="sxs-lookup"><span data-stu-id="6901c-187">Metrics</span></span>

<span data-ttu-id="6901c-188">A tabela a seguir lista as informações fornecidas no Relatório de Falhas Principais.</span><span class="sxs-lookup"><span data-stu-id="6901c-188">The following table lists the information provided in the Top Failures Report.</span></span>

### <a name="top-failures-report-metrics"></a><span data-ttu-id="6901c-189">Métricas do Relatório de Falhas Principais</span><span class="sxs-lookup"><span data-stu-id="6901c-189">Top Failures Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6901c-190">Nome</span><span class="sxs-lookup"><span data-stu-id="6901c-190">Name</span></span></th>
<th><span data-ttu-id="6901c-191">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="6901c-191">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="6901c-192">Descrição</span><span class="sxs-lookup"><span data-stu-id="6901c-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6901c-193"><strong>Classificação</strong></span><span class="sxs-lookup"><span data-stu-id="6901c-193"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="6901c-194">Sim</span><span class="sxs-lookup"><span data-stu-id="6901c-194">Yes</span></span></p></td>
<td><p><span data-ttu-id="6901c-195">Classificação relativa com base no número de sessões relatadas.</span><span class="sxs-lookup"><span data-stu-id="6901c-195">Relative rank based on the number of reported sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6901c-196"><strong>Sessões relatadas</strong></span><span class="sxs-lookup"><span data-stu-id="6901c-196"><strong>Reported sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="6901c-197">Sim</span><span class="sxs-lookup"><span data-stu-id="6901c-197">Yes</span></span></p></td>
<td><p><span data-ttu-id="6901c-198">Número total de sessões com falha com base na ID de diagnóstico e no código de resposta SIP.</span><span class="sxs-lookup"><span data-stu-id="6901c-198">Total number of failed sessions based on diagnostic ID and SIP response code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6901c-199"><strong>Usuários afetados</strong></span><span class="sxs-lookup"><span data-stu-id="6901c-199"><strong>Users impacted</strong></span></span></p></td>
<td><p><span data-ttu-id="6901c-200">Sim</span><span class="sxs-lookup"><span data-stu-id="6901c-200">Yes</span></span></p></td>
<td><p><span data-ttu-id="6901c-201">Número total de usuários afetados pela sessão com falha.</span><span class="sxs-lookup"><span data-stu-id="6901c-201">Total number of users affected by the failed session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6901c-202"><strong>Informações da falha</strong></span><span class="sxs-lookup"><span data-stu-id="6901c-202"><strong>Failure information</strong></span></span></p></td>
<td><p><span data-ttu-id="6901c-203">Não</span><span class="sxs-lookup"><span data-stu-id="6901c-203">No</span></span></p></td>
<td><p><span data-ttu-id="6901c-204">Informações detalhadas sobre a falha, incluindo a ID de diagnóstico, o código de resposta SIP e a descrição do motivo da falha na sessão.</span><span class="sxs-lookup"><span data-stu-id="6901c-204">Detailed information about the failure, including diagnostic ID, SIP response code, and description of why the session failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6901c-205"><strong>Tendência no passado</strong></span><span class="sxs-lookup"><span data-stu-id="6901c-205"><strong>Trend in the past</strong></span></span></p></td>
<td><p><span data-ttu-id="6901c-206">Não</span><span class="sxs-lookup"><span data-stu-id="6901c-206">No</span></span></p></td>
<td><p><span data-ttu-id="6901c-207">Representa graficamente as sessões com falha ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="6901c-207">Graphs failed sessions over time.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6901c-208">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6901c-208">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

