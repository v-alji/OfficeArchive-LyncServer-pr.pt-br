---
title: 'Lync Server 2013: relatório de controle de admissão de chamadas'
description: 'Lync Server 2013: relatório de controle de admissão de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Admission Control Report
ms:assetid: ea4b0c9f-7f93-4b8a-b901-01e1636c44fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615043(v=OCS.15)
ms:contentKeyID: 48185933
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8764e51603e7097095894bc1230c2a2bb1126b9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435779"
---
# <a name="call-admission-control-report-in-lync-server-2013"></a><span data-ttu-id="71ef2-103">Relatório de controle de admissão de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="71ef2-103">Call Admission Control Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71ef2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71ef2-104">

<span> </span></span></span>

<span data-ttu-id="71ef2-105">_**Tópico da última modificação:** 2012-06-29_</span><span class="sxs-lookup"><span data-stu-id="71ef2-105">_**Topic Last Modified:** 2012-06-29_</span></span>

<span data-ttu-id="71ef2-106">O Relatório de Controle de Admissão de Chamadas fornece informações sobre sessões de conferência e ponto a ponto que eram conduzidas sob restrições impostas pelo Controle de Admissão de Chamadas.</span><span class="sxs-lookup"><span data-stu-id="71ef2-106">The Call Admission Control Report provides information about peer-to-peer and conferencing sessions that were conducted under restrictions set in place by Call Admission Control.</span></span> <span data-ttu-id="71ef2-107">O controle de admissão de chamadas, introduzido no Microsoft Lync Server 2010, fornece uma maneira para os administradores permitirem (ou não permitirem) sessões de comunicação com base em restrições de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="71ef2-107">Call Admission Control, introduced in Microsoft Lync Server 2010, provides a way for administrators to allow (or not allow) communication sessions based on bandwidth constraints.</span></span> <span data-ttu-id="71ef2-108">Por exemplo, os administradores podem criar políticas que imponham um limite na quantidade de banda disponível para chamadas de voz e vídeo.</span><span class="sxs-lookup"><span data-stu-id="71ef2-108">For example, administrators can create policies that impose a limit on the amount of bandwidth available for voice and video calls.</span></span> <span data-ttu-id="71ef2-109">Caso o limite de banda seja alcançado, novas chamadas de voz ou vídeo não poderão ser feitas até que uma das chamadas atuais termine e libere os recursos de rede necessários.</span><span class="sxs-lookup"><span data-stu-id="71ef2-109">If that bandwidth limit has been reached, then no new voice or video calls can be placed until one of the current calls has ended and freed up the required network resources.</span></span>

<div>

## <a name="accessing-the-call-admission-control-report"></a><span data-ttu-id="71ef2-110">Acessando o Relatório de Controle de Admissão de Chamadas</span><span class="sxs-lookup"><span data-stu-id="71ef2-110">Accessing the Call Admission Control Report</span></span>

<span data-ttu-id="71ef2-p102">O Relatório de Controle de Admissão de Chamadas é acessado através da página de Relatórios de Monitoramento. A partir do Relatório de Controle de Admissão de Chamadas você pode buscar mais detalhes em um dos seguintes relatórios:</span><span class="sxs-lookup"><span data-stu-id="71ef2-p102">The Call Admission Control Report is accessed from the Monitoring Reports home page. From the Call Admission Control Report you can drill down to either of the following reports:</span></span>

  - <span data-ttu-id="71ef2-113">Relatório Detalhado de Conferências – Para acessar esse relatório, clique na métrica Detalhes de uma sessão de conferência.</span><span class="sxs-lookup"><span data-stu-id="71ef2-113">Conference Detail Report – To access this report, click the Details metric from a conference session.</span></span>

  - <span data-ttu-id="71ef2-114">Relatório Detalhado de Sessão Ponto a Ponto – Para acessar esse relatório, clique na métrica Detalhes de uma sessão ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="71ef2-114">Peer-to-Peer Session Detail Report – To access this report, click the Details metric for a peer-to-peer session.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-admission-control-report"></a><span data-ttu-id="71ef2-115">Como usar o Relatório de Controle de Admissão de Chamadas da melhor maneira possível</span><span class="sxs-lookup"><span data-stu-id="71ef2-115">Making the Best Use of the Call Admission Control Report</span></span>

<span data-ttu-id="71ef2-p103">Para obter uma lista de chamadas que falharam por causa de largura de banda insuficiente, selecione Chamadas rejeitadas devido ao controle de admissão de chamadas, na lista suspensa Categoria da chamada. A maioria das chamadas retornadas provavelmente terá a ID de diagnóstico 5:</span><span class="sxs-lookup"><span data-stu-id="71ef2-p103">To get a list of calls that failed because of insufficient bandwidth, select Calls rejected because of call admission control from the Call category dropdown list. Most of the returned calls will likely have a diagnostic ID of 5:</span></span>

<span data-ttu-id="71ef2-p104">Largura de banda insuficiente para estabelecer sessão. Tente reencaminhamento por PSTN.</span><span class="sxs-lookup"><span data-stu-id="71ef2-p104">Insufficient bandwidth to establish session. Attempt PSTN re-route.</span></span>

<span data-ttu-id="71ef2-120">Isso indica que as limitações do Controle de Admissão de Chamadas estavam impedindo a chamada de ser efetuada na rede VoIP.</span><span class="sxs-lookup"><span data-stu-id="71ef2-120">That indicates that Call Admission Control limitations were preventing the call from being made on the VoIP network.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="71ef2-121">Filtros</span><span class="sxs-lookup"><span data-stu-id="71ef2-121">Filters</span></span>

<span data-ttu-id="71ef2-p105">Os filtros fornecem uma maneira de retornar um conjunto de dados mais direcionado ou de exibir os dados retornados de maneiras diferentes. Por exemplo, o Relatório de Controle de Admissão de Chamadas permite que você filtre as chamadas de acordo com o usuário que iniciou a chamada ou com o usuário que está sendo chamado. Também é possível escolher como os dados devem ser agrupados. Nesse caso, as chamadas são agrupadas por hora, dia, semana ou mês.</span><span class="sxs-lookup"><span data-stu-id="71ef2-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Call Admission Control Report enables you to filter calls by the user who initiated the call or by the user who was being called. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="71ef2-126">A tabela a seguir lista os filtros que podem ser usados com o Relatório de Controle de Admissão de Chamadas.</span><span class="sxs-lookup"><span data-stu-id="71ef2-126">The following table lists the filters that you can use with the Call Admission Control Report.</span></span>

### <a name="call-admission-control-report-filters"></a><span data-ttu-id="71ef2-127">Filtros do Relatório de Controle de Admissão de Chamadas</span><span class="sxs-lookup"><span data-stu-id="71ef2-127">Call Admission Control Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71ef2-128">Nome</span><span class="sxs-lookup"><span data-stu-id="71ef2-128">Name</span></span></th>
<th><span data-ttu-id="71ef2-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="71ef2-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71ef2-130"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-130"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-p106">Data/hora de início para o intervalo de tempo. Para ver os dados por horas, insira a data e hora de início conforme segue:</span><span class="sxs-lookup"><span data-stu-id="71ef2-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="71ef2-133">7/17/12012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="71ef2-133">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="71ef2-p107">Se você não inserir a hora de início, o relatório começará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="71ef2-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="71ef2-136">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="71ef2-136">7/17/12012</span></span></p>
<p><span data-ttu-id="71ef2-137">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="71ef2-137">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="71ef2-138">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="71ef2-138">7/13/2012</span></span></p>
<p><span data-ttu-id="71ef2-139">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="71ef2-139">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71ef2-140"><strong>Até</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-140"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-p108">Data/hora final de intervalo de tempo. Para ver os dados por horas, insira a data e hora final conforme segue:</span><span class="sxs-lookup"><span data-stu-id="71ef2-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="71ef2-143">7/17/12012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="71ef2-143">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="71ef2-p109">Se você não inserir a hora final, o relatório terminará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="71ef2-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="71ef2-146">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="71ef2-146">7/17/12012</span></span></p>
<p><span data-ttu-id="71ef2-147">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="71ef2-147">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="71ef2-148">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="71ef2-148">7/13/2012</span></span></p>
<p><span data-ttu-id="71ef2-149">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="71ef2-149">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71ef2-150"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-150"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-p110">FQDN (Nome de domínio totalmente qualificado) do Pool de registradores ou Servidor de Borda. Você pode selecionar um pool individual ou clicar em <strong>[Todos]</strong> para ver os dados de todos os pools. Essa lista suspensa é automaticamente preenchida para você com base nos registros no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71ef2-p110">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71ef2-154"><strong>Tipo de atividade</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-154"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-p111">Tipo de atividade. Selecione uma das seguintes atividades:</span><span class="sxs-lookup"><span data-stu-id="71ef2-p111">Type of activity. Select one of the following activities:</span></span></p>
<ul>
<li><p><span data-ttu-id="71ef2-157">[Todos]</span><span class="sxs-lookup"><span data-stu-id="71ef2-157">[All]</span></span></p></li>
<li><p><span data-ttu-id="71ef2-158">Ponto a Ponto</span><span class="sxs-lookup"><span data-stu-id="71ef2-158">Peer-to-Peer</span></span></p></li>
<li><p><span data-ttu-id="71ef2-159">Conferência</span><span class="sxs-lookup"><span data-stu-id="71ef2-159">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71ef2-160"><strong>Categoria da chamada</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-160"><strong>Call category</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-p112">Indica o motivo de o CAC ter sido usado para a chamada. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="71ef2-p112">Indicates the reason that CAC was used for the call. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="71ef2-163">[Todos]</span><span class="sxs-lookup"><span data-stu-id="71ef2-163">[All]</span></span></p></li>
<li><p><span data-ttu-id="71ef2-164">Chamada rejeitada devido ao controle de admissão de chamadas</span><span class="sxs-lookup"><span data-stu-id="71ef2-164">Call rejected because of call admission control</span></span></p></li>
<li><p><span data-ttu-id="71ef2-165">Chamadas roteadas novamente por PSTN devido ao controle de admissão de chamadas</span><span class="sxs-lookup"><span data-stu-id="71ef2-165">Calls rerouted through PSTN because of call admission control</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="71ef2-166">Métricas para sessões ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="71ef2-166">Metrics for Peer-to-Peer Sessions</span></span>

<span data-ttu-id="71ef2-167">A tabela a seguir lista as informações fornecidas no Relatório de Controle de Admissão de Chamadas para sessões ponto a ponto (ou seja, sessões que envolvem apenas dois participantes).</span><span class="sxs-lookup"><span data-stu-id="71ef2-167">The following table lists the information provided in the Call Admission Control Report for peer-to-peer sessions (that is, sessions involving just two participants).</span></span>

### <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="71ef2-168">Métricas para sessões ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="71ef2-168">Metrics for Peer-to-Peer Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71ef2-169">Nome</span><span class="sxs-lookup"><span data-stu-id="71ef2-169">Name</span></span></th>
<th><span data-ttu-id="71ef2-170">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="71ef2-170">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="71ef2-171">Descrição</span><span class="sxs-lookup"><span data-stu-id="71ef2-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71ef2-172"><strong>Detalhe</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-172"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-173">Não</span><span class="sxs-lookup"><span data-stu-id="71ef2-173">No</span></span></p></td>
<td><p><span data-ttu-id="71ef2-174">Quando você clica nesse item, o relatório mostra o Relatório Detalhado de Sessão Ponto a Ponto para a sessão especificada.</span><span class="sxs-lookup"><span data-stu-id="71ef2-174">When you click this item, the report shows you a Peer-to-Peer Session Detail Report for the specified session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71ef2-175"><strong>De usuário</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-175"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-176">Sim</span><span class="sxs-lookup"><span data-stu-id="71ef2-176">Yes</span></span></p></td>
<td><p><span data-ttu-id="71ef2-177">Endereço SIP do usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="71ef2-177">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71ef2-178"><strong>Para usuário</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-178"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-179">Sim</span><span class="sxs-lookup"><span data-stu-id="71ef2-179">Yes</span></span></p></td>
<td><p><span data-ttu-id="71ef2-180">Endereço SIP do usuário convidado para ingressar na sessão.</span><span class="sxs-lookup"><span data-stu-id="71ef2-180">SIP address of the user who was invited to join the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71ef2-181"><strong>Modalidades</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-181"><strong>Modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-182">Sim</span><span class="sxs-lookup"><span data-stu-id="71ef2-182">Yes</span></span></p></td>
<td><p><span data-ttu-id="71ef2-183">Modalidades de comunicação (como áudio e vídeo) usadas durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="71ef2-183">Communication modalities (such as audio and video) that were used during the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71ef2-184"><strong>Hora do convite</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-184"><strong>Invite time</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-185">Sim</span><span class="sxs-lookup"><span data-stu-id="71ef2-185">Yes</span></span></p></td>
<td><p><span data-ttu-id="71ef2-186">Data e hora de envio do convite inicial da sessão para o usuário remetente.</span><span class="sxs-lookup"><span data-stu-id="71ef2-186">Date and time the initial session invitation was sent to the From user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71ef2-187"><strong>Hora da resposta</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-187"><strong>Response time</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-188">Sim</span><span class="sxs-lookup"><span data-stu-id="71ef2-188">Yes</span></span></p></td>
<td><p><span data-ttu-id="71ef2-189">Data e hora de recebimento da aceitação do convite.</span><span class="sxs-lookup"><span data-stu-id="71ef2-189">Date and time that the invitation acceptance was received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71ef2-190"><strong>Hora de término</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-190"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-191">Sim</span><span class="sxs-lookup"><span data-stu-id="71ef2-191">Yes</span></span></p></td>
<td><p><span data-ttu-id="71ef2-192">Data e hora de encerramento da sessão.</span><span class="sxs-lookup"><span data-stu-id="71ef2-192">Date and time that the session ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71ef2-193"><strong>ID do Diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-193"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-194">Sim</span><span class="sxs-lookup"><span data-stu-id="71ef2-194">Yes</span></span></p></td>
<td><p><span data-ttu-id="71ef2-p113">Identificador exclusivo (na forma de cabeçalho ms-diagnostics) anexado a uma mensagem SIP que fornece informações úteis para solucionar erros. Os cabeçalhos Diagnóstico são opcionais (é possível ter sessões SIP que não os incluem), e as IDs de diagnóstico são relatadas somente para as sessões com algum tipo de problema.</span><span class="sxs-lookup"><span data-stu-id="71ef2-p113">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="71ef2-197">Métricas para sessões de conferência</span><span class="sxs-lookup"><span data-stu-id="71ef2-197">Metrics for Conferencing Sessions</span></span>

<span data-ttu-id="71ef2-198">A tabela a seguir lista as informações fornecidas no Relatório de Controle de Admissão de Chamadas para sessões de conferência (ou seja, sessões que envolvem três ou mais participantes).</span><span class="sxs-lookup"><span data-stu-id="71ef2-198">The following table lists the information provided in the Call Admission Control Report for conferencing sessions (that is, sessions involving three or more participants).</span></span>

### <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="71ef2-199">Métricas para sessões de conferência</span><span class="sxs-lookup"><span data-stu-id="71ef2-199">Metrics for Conferencing Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71ef2-200">Nome</span><span class="sxs-lookup"><span data-stu-id="71ef2-200">Name</span></span></th>
<th><span data-ttu-id="71ef2-201">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="71ef2-201">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="71ef2-202">Descrição</span><span class="sxs-lookup"><span data-stu-id="71ef2-202">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71ef2-203"><strong>URI de conferência</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-203"><strong>Conference URI</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-204">Sim</span><span class="sxs-lookup"><span data-stu-id="71ef2-204">Yes</span></span></p></td>
<td><p><span data-ttu-id="71ef2-p114">Identificador exclusivo para a conferência. Quando você clica nesse item, o relatório mostra os participantes individuais da conferência.</span><span class="sxs-lookup"><span data-stu-id="71ef2-p114">Unique identifier for the conference. When you click this item, the report shows the individual conference participants.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71ef2-207"><strong>Organizador</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-207"><strong>Organizer</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-208">Sim</span><span class="sxs-lookup"><span data-stu-id="71ef2-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="71ef2-209">Endereço SIP do usuário que organizou a conferência.</span><span class="sxs-lookup"><span data-stu-id="71ef2-209">SIP address of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71ef2-210"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-210"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-211">Sim</span><span class="sxs-lookup"><span data-stu-id="71ef2-211">Yes</span></span></p></td>
<td><p><span data-ttu-id="71ef2-212">Servidor de Borda usado na conferência.</span><span class="sxs-lookup"><span data-stu-id="71ef2-212">Edge Server used in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71ef2-213"><strong>Hora de início</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-213"><strong>Start time</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-214">Sim</span><span class="sxs-lookup"><span data-stu-id="71ef2-214">Yes</span></span></p></td>
<td><p><span data-ttu-id="71ef2-215">Data e hora de início da sessão.</span><span class="sxs-lookup"><span data-stu-id="71ef2-215">Date and time that the conference started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71ef2-216"><strong>Hora de término</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-216"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-217">Sim</span><span class="sxs-lookup"><span data-stu-id="71ef2-217">Yes</span></span></p></td>
<td><p><span data-ttu-id="71ef2-218">Data e hora em que a conferência terminou.</span><span class="sxs-lookup"><span data-stu-id="71ef2-218">Date and time that the conference ended.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-individual-conference-participants"></a><span data-ttu-id="71ef2-219">Métricas para participantes individuais da conferência</span><span class="sxs-lookup"><span data-stu-id="71ef2-219">Metrics for Individual Conference Participants</span></span>

<span data-ttu-id="71ef2-220">A tabela a seguir lista as informações fornecidas no Relatório de Controle de Admissão de Chamadas para participantes individuais da conferência.</span><span class="sxs-lookup"><span data-stu-id="71ef2-220">The following table lists the information provided in the Call Admission Control Report for individual conference participants.</span></span>

### <a name="metrics-for-individual-conference-participants"></a><span data-ttu-id="71ef2-221">Métricas para participantes individuais da conferência</span><span class="sxs-lookup"><span data-stu-id="71ef2-221">Metrics for Individual Conference Participants</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71ef2-222">Nome</span><span class="sxs-lookup"><span data-stu-id="71ef2-222">Name</span></span></th>
<th><span data-ttu-id="71ef2-223">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="71ef2-223">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="71ef2-224">Descrição</span><span class="sxs-lookup"><span data-stu-id="71ef2-224">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71ef2-225"><strong>Função</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-225"><strong>Role</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-226">Não</span><span class="sxs-lookup"><span data-stu-id="71ef2-226">No</span></span></p></td>
<td><p><span data-ttu-id="71ef2-227">Função (por exemplo, Apresentador) desempenhada pelo participante da conferência.</span><span class="sxs-lookup"><span data-stu-id="71ef2-227">Role (for example, Presenter) played by the conference participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71ef2-228"><strong>Participante</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-228"><strong>Participant</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-229">Não</span><span class="sxs-lookup"><span data-stu-id="71ef2-229">No</span></span></p></td>
<td><p><span data-ttu-id="71ef2-230">Endereço SIP do participante de conferência.</span><span class="sxs-lookup"><span data-stu-id="71ef2-230">SIP address of the conference participant.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71ef2-231"><strong>Conectividade</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-231"><strong>Connectivity</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-232">Não</span><span class="sxs-lookup"><span data-stu-id="71ef2-232">No</span></span></p></td>
<td><p><span data-ttu-id="71ef2-233">Conectividade de rede (normalmente Interna ou Externa) para o participante.</span><span class="sxs-lookup"><span data-stu-id="71ef2-233">Network connectivity (typically From Internal or From External) for the participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71ef2-234"><strong>Modalidade</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-234"><strong>Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-235">Não</span><span class="sxs-lookup"><span data-stu-id="71ef2-235">No</span></span></p></td>
<td><p><span data-ttu-id="71ef2-236">Tipo de conferência (por exemplo, conferência de A/V).</span><span class="sxs-lookup"><span data-stu-id="71ef2-236">Conference type (for example, A/V conferencing).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71ef2-237"><strong>Hora de ingresso</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-237"><strong>Join time</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-238">Não</span><span class="sxs-lookup"><span data-stu-id="71ef2-238">No</span></span></p></td>
<td><p><span data-ttu-id="71ef2-239">Data e hora de ingresso do participante na conferência.</span><span class="sxs-lookup"><span data-stu-id="71ef2-239">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71ef2-240"><strong>Hora da saída</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-240"><strong>Leave time</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-241">Não</span><span class="sxs-lookup"><span data-stu-id="71ef2-241">No</span></span></p></td>
<td><p><span data-ttu-id="71ef2-242">Data e hora de saída do participante da conferência.</span><span class="sxs-lookup"><span data-stu-id="71ef2-242">Date and time that the participant left the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71ef2-243"><strong>ID do Diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="71ef2-243"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="71ef2-244">Não</span><span class="sxs-lookup"><span data-stu-id="71ef2-244">No</span></span></p></td>
<td><p><span data-ttu-id="71ef2-p115">Identificador exclusivo (na forma de um cabeçalho de diagnóstico-ms) anexado a uma mensagem SIP que fornece informações úteis sobre os erros de solução de problemas. Os cabeçalhos diagnósticos são opcionais (é possível ter sessões SIP que não os incluem), e os IDs diagnósticos são relatados somente para as sessões com algum tipo de problema.</span><span class="sxs-lookup"><span data-stu-id="71ef2-p115">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="71ef2-247">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71ef2-247">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

