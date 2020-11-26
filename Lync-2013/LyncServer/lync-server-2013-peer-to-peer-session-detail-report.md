---
title: 'Lync Server 2013: relatório detalhado de sessão ponto a ponto'
description: 'Lync Server 2013: relatório detalhado de sessão ponto a ponto.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Peer-to-Peer Session Detail Report
ms:assetid: 6be1d676-68f7-4a53-a72a-de73296c5571
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558659(v=OCS.15)
ms:contentKeyID: 48184416
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e712225fddabb646cc3b862f59601857a7df8eff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445033"
---
# <a name="peer-to-peer-session-detail-report-in-lync-server-2013"></a><span data-ttu-id="e914c-103">Relatório detalhado de sessão ponto a ponto no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e914c-103">Peer-to-Peer Session Detail Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e914c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e914c-104">

<span> </span></span></span>

<span data-ttu-id="e914c-105">_**Tópico da última modificação:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="e914c-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="e914c-p101">O Relatório Detalhado de Sessão Ponto a Ponto retorna informações detalhadas sobre uma sessão ponto a ponto. Por exemplo, se você selecionar uma sessão de mensagens instantâneas, o relatório informará o número de mensagens enviadas por cada um dos dois usuários na seção.</span><span class="sxs-lookup"><span data-stu-id="e914c-p101">The Peer-to-Peer Session Detail Report returns detailed information about a peer-to-peer session. For example, if you select an instant messaging session, the report will tell you the number of messages sent by each of the two users in the session.</span></span>

<div>

## <a name="accessing-the-peer-to-peer-session-detail-report"></a><span data-ttu-id="e914c-108">Acessando o Relatório Detalhado de Sessão Ponto a Ponto</span><span class="sxs-lookup"><span data-stu-id="e914c-108">Accessing the Peer-to-Peer Session Detail Report</span></span>

<span data-ttu-id="e914c-109">O Relatório Detalhado de Sessão Ponto a Ponto pode ser acessado a partir de qualquer um dos relatórios a seguir (todos os quais podem ser acessados a partir da home page Relatórios de Monitoramento):</span><span class="sxs-lookup"><span data-stu-id="e914c-109">The Peer-to-Peer Session Detail Report can be accessed from any of the following reports (all of which can be accessed from the Monitoring Reports home page):</span></span>

  - <span data-ttu-id="e914c-110">Relatório de Inventário de Telefones IP</span><span class="sxs-lookup"><span data-stu-id="e914c-110">IP Phone Inventory Report</span></span>

  - <span data-ttu-id="e914c-111">Relatório de Atividades do Usuário</span><span class="sxs-lookup"><span data-stu-id="e914c-111">User Activity Report</span></span>

  - <span data-ttu-id="e914c-112">Relatório de Controle de Admissão de Chamadas</span><span class="sxs-lookup"><span data-stu-id="e914c-112">Call Admission Control Report</span></span>

  - <span data-ttu-id="e914c-113">Relatório de lista de falhas</span><span class="sxs-lookup"><span data-stu-id="e914c-113">Failure List Report</span></span>

<span data-ttu-id="e914c-114">No relatório de detalhes da sessão ponto a ponto, você pode acessar o [relatório de diagnóstico no Lync Server 2013](lync-server-2013-diagnostic-report.md) clicando na métrica relatório de diagnóstico (detalhes).</span><span class="sxs-lookup"><span data-stu-id="e914c-114">From within the Peer-to-Peer Session Detail Report you can access the [Diagnostic Report in Lync Server 2013](lync-server-2013-diagnostic-report.md) by clicking the Diagnostic Report (Details) metric.</span></span> <span data-ttu-id="e914c-115">Você também pode acessar o Relatório das Principais Falhas clicando em uma destas duas métricas:</span><span class="sxs-lookup"><span data-stu-id="e914c-115">You can also access the Top Failures Report by clicking either of these two metrics:</span></span>

  - <span data-ttu-id="e914c-116">Resposta</span><span class="sxs-lookup"><span data-stu-id="e914c-116">Response</span></span>

  - <span data-ttu-id="e914c-117">ID do Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="e914c-117">Diagnostic ID</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-peer-to-peer-session-detail-report"></a><span data-ttu-id="e914c-118">Usando o Relatório Detalhado de Sessão Ponto a Ponto da melhor maneira possível</span><span class="sxs-lookup"><span data-stu-id="e914c-118">Making the Best Use of the Peer-to-Peer session Detail Report</span></span>

<span data-ttu-id="e914c-p103">O Relatório Detalhado de Sessão Ponto a Ponto inclui um grande número de métricas, muitas das quais os administradores de sistemas podem desconhecer. Muitas vezes, porém, você pode exibir uma dica de ferramenta que oferece uma breve descrição da métrica. Para isso, basta manter o cursor do mouse sobre o rótulo da métrica.</span><span class="sxs-lookup"><span data-stu-id="e914c-p103">The Peer-to-Peer Session Detail Report includes a large number of metrics, many of which might not be familiar to system administrators. Often-times, however, you can view a tooltip that offers a brief description of that metric simply by holding your mouse over the metric label.</span></span>

<span data-ttu-id="e914c-p104">Observe que as métricas mostradas em determinado relatório dependerão do tipo de sessão ponto a ponto selecionada. Uma sessão de áudio/vídeo mostrará um conjunto de métricas diferente de uma sessão de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="e914c-p104">Note that the actual metrics shown on a given report will depend on the type of peer-to-peer session you selected. An audio/video session will report a different set of metrics than an instant messaging session.</span></span>

<span data-ttu-id="e914c-123">Você também pode manter o cursor do mouse sobre as métricas Código de resposta e ID de diagnóstico para obter uma descrição desses valores:</span><span class="sxs-lookup"><span data-stu-id="e914c-123">You can also hold your mouse over the Response code and Diagnostic ID metrics in order to obtain a description of those values:</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="e914c-124">Filtros</span><span class="sxs-lookup"><span data-stu-id="e914c-124">Filters</span></span>

<span data-ttu-id="e914c-p105">Nenhum. Não é possível filtrar o relatório de Detalhes de Sessão Ponto a Ponto.</span><span class="sxs-lookup"><span data-stu-id="e914c-p105">None. You cannot filter the Peer-to-Peer Session Detail Report.</span></span>

</div>

<div>

## <a name="session-information-metrics"></a><span data-ttu-id="e914c-127">Métricas de informações da sessão</span><span class="sxs-lookup"><span data-stu-id="e914c-127">Session Information Metrics</span></span>

<span data-ttu-id="e914c-128">A tabela a seguir lista as informações fornecidas no relatório de Detalhes de Sessão Ponto a Ponto para cada sessão.</span><span class="sxs-lookup"><span data-stu-id="e914c-128">The following table lists the information provided in the Peer-to-Peer Session Detail Report for each session.</span></span>

### <a name="session-information-metrics"></a><span data-ttu-id="e914c-129">Métricas de informações da sessão</span><span class="sxs-lookup"><span data-stu-id="e914c-129">Session Information Metrics</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e914c-130">Nome</span><span class="sxs-lookup"><span data-stu-id="e914c-130">Name</span></span></th>
<th><span data-ttu-id="e914c-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="e914c-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e914c-132"><strong>FQDN do pool</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-132"><strong>Pool FQDN</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-133">Nome de domínio totalmente qualificado (FQDN) do pool de Registradores ou Servidor de Borda envolvido na sessão.</span><span class="sxs-lookup"><span data-stu-id="e914c-133">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server involved in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e914c-134"><strong>Hora do convite</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-134"><strong>Invite time</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-135">Data e hora em que o convite de sessão foi originalmente enviado.</span><span class="sxs-lookup"><span data-stu-id="e914c-135">Date and time the session invitation was originally sent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e914c-136"><strong>Hora da resposta</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-136"><strong>Response time</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-137">Data e hora de recebimento da aceitação do convite.</span><span class="sxs-lookup"><span data-stu-id="e914c-137">Date and time that the invitation acceptance was received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e914c-138"><strong>Usuário "De"</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-138"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-139">Endereço SIP do usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="e914c-139">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e914c-140"><strong>Agente do usuário "De"</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-140"><strong>From user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-141">Software usado pelo ponto de extremidade do usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="e914c-141">Software used by the endpoint of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e914c-142"><strong>É usuário "De" interno</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-142"><strong>Is From user internal</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-143">Indica se o usuário que iniciou a sessão estava conectado à rede interna.</span><span class="sxs-lookup"><span data-stu-id="e914c-143">Indicates whether the user who initiated the session was logged on to the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e914c-144"><strong>É usuário "De" integrado com telefone de mesa</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-144"><strong>Is From user integrated with desk phone</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-145">Indica se o ponto de extremidade usado pelo usuário que iniciou a sessão está integrado ao seu telefone de mesa.</span><span class="sxs-lookup"><span data-stu-id="e914c-145">Indicates whether the endpoint used by the user who initiated the session is integrated with his or her desktop phone.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e914c-146"><strong>Prioridade da Sessão</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-146"><strong>Session Priority</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-p106">Prioridade atribuída à sessão. As prioridades válidas são: Desconhecida; Não Urgente; Normal; Urgente; e Emergência.</span><span class="sxs-lookup"><span data-stu-id="e914c-p106">Priority assigned to the session. Valid priorities are: Unknown; Non-Urgent; Normal; Urgent; and Emergency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e914c-149"><strong>Código da resposta</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-149"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-150">Código da resposta SIP enviado quando a sessão falhou.</span><span class="sxs-lookup"><span data-stu-id="e914c-150">SIP response code sent when the session failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e914c-151"><strong>Front-End</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-151"><strong>Front end</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-152">Nome do Servidor Front-End usado na conferência.</span><span class="sxs-lookup"><span data-stu-id="e914c-152">Name of the Front End Server used in the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e914c-153"><strong>Hora da captura</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-153"><strong>Capture time</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-154">Data e hora em que a sessão de informações foi gravada.</span><span class="sxs-lookup"><span data-stu-id="e914c-154">Date and time that the session information was recorded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e914c-155"><strong>Hora final</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-155"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-156">Data e hora em que a sessão foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="e914c-156">Date and time the session ended.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e914c-157"><strong>Usuário "Para"</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-157"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-158">Endereço SIP do usuário convidado para a sessão.</span><span class="sxs-lookup"><span data-stu-id="e914c-158">SIP address of the user who was invited to the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e914c-159"><strong>Agente do usuário "Para"</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-159"><strong>To user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-160">Software usado pelo ponto de extremidade do usuário que foi convidado para a sessão.</span><span class="sxs-lookup"><span data-stu-id="e914c-160">Software used by the endpoint of the user who was invited to the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e914c-161"><strong>É usuário "Para" interno</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-161"><strong>Is To user internal</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-162">Indica se o usuário que foi convidado para a sessão estava conectado à rede interna.</span><span class="sxs-lookup"><span data-stu-id="e914c-162">Indicates whether the user who was invited to the session was logged on to the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e914c-163"><strong>É usuário "Para" integrado com telefone de mesa</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-163"><strong>Is To user integrated with desk phone</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-164">Indica se o ponto de extremidade usado pelo usuário que foi convidado para a sessão está integrado ao seu telefone de mesa.</span><span class="sxs-lookup"><span data-stu-id="e914c-164">Indicates whether the endpoint used by the user who was invited to the session is integrated with his or her desktop phone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e914c-165"><strong>É sessão repetida</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-165"><strong>Is retried session</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-166">Indica se a sessão é uma tentativa para repetir uma sessão que falhou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e914c-166">Indicates whether the session is an attempt to retry a session that previously failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e914c-167"><strong>ID do Diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-167"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-p107">Identificador exclusivo (no formato de um cabeçalho ms-diagnostics) anexado a uma mensagem SIP que frequentemente oferece informações úteis para resolução de erros. Mantenha o mouse sobre o número de identificação para exibir informações adicionais sobre essa identificação.</span><span class="sxs-lookup"><span data-stu-id="e914c-p107">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Hold the mouse over the ID number to view additional information about that ID.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-modalities"></a><span data-ttu-id="e914c-170">Métricas para modalidades</span><span class="sxs-lookup"><span data-stu-id="e914c-170">Metrics for Modalities</span></span>

<span data-ttu-id="e914c-171">A tabela a seguir lista as informações fornecidas no relatório de Detalhes de Sessão Ponto a Ponto para cada sessão de modalidade.</span><span class="sxs-lookup"><span data-stu-id="e914c-171">The following table lists the information provided in the Peer-to-Peer Session Detail Report for each session modality.</span></span>

### <a name="metrics-for-modalities"></a><span data-ttu-id="e914c-172">Métricas para modalidades</span><span class="sxs-lookup"><span data-stu-id="e914c-172">Metrics for Modalities</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e914c-173">Nome</span><span class="sxs-lookup"><span data-stu-id="e914c-173">Name</span></span></th>
<th><span data-ttu-id="e914c-174">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="e914c-174">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e914c-175">Descrição</span><span class="sxs-lookup"><span data-stu-id="e914c-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e914c-176"><strong>Modalidades</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-176"><strong>Modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-177">Não</span><span class="sxs-lookup"><span data-stu-id="e914c-177">No</span></span></p></td>
<td><p><span data-ttu-id="e914c-p108">Modalidades usadas na sessão. Por exemplo, mensagens instantâneas ou transferência de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e914c-p108">Modalities used in the session. For example, instant messaging (IM) or file transfer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e914c-180"><strong>Mensagens do usuário "De"</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-180"><strong>From user messages</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-181">Não</span><span class="sxs-lookup"><span data-stu-id="e914c-181">No</span></span></p></td>
<td><p><span data-ttu-id="e914c-182">Número de mensagens enviadas pelo usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="e914c-182">Number of messages sent by the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e914c-183"><strong>Mensagens do usuário "Para"</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-183"><strong>To user messages</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-184">Não</span><span class="sxs-lookup"><span data-stu-id="e914c-184">No</span></span></p></td>
<td><p><span data-ttu-id="e914c-185">Número de mensagens enviadas pelo usuário que foi convidado para a sessão.</span><span class="sxs-lookup"><span data-stu-id="e914c-185">Number of messages sent by the user who was invited to join the session.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-diagnostic-reports"></a><span data-ttu-id="e914c-186">Métricas para relatórios de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="e914c-186">Metrics for Diagnostic Reports</span></span>

<span data-ttu-id="e914c-187">A tabela a seguir lista as informações fornecidas no relatório de Detalhes de Sessão Ponto a Ponto para cada relatório de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="e914c-187">The following table lists the information provided in the Peer-to-Peer Session Detail Report for each diagnostic report.</span></span>

### <a name="metrics-for-diagnostic-reports"></a><span data-ttu-id="e914c-188">Métricas para Relatórios de Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="e914c-188">Metrics for Diagnostic Reports</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e914c-189">Nome</span><span class="sxs-lookup"><span data-stu-id="e914c-189">Name</span></span></th>
<th><span data-ttu-id="e914c-190">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="e914c-190">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e914c-191">Descrição</span><span class="sxs-lookup"><span data-stu-id="e914c-191">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e914c-192"><strong>Detalhe</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-192"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-193">Não</span><span class="sxs-lookup"><span data-stu-id="e914c-193">No</span></span></p></td>
<td><p><span data-ttu-id="e914c-194">Quando você clica nesse item, o relatório mostra o Relatório de Diagnóstico da sessão.</span><span class="sxs-lookup"><span data-stu-id="e914c-194">When you click this item, the report shows the Diagnostic Report for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e914c-195"><strong>Hora do relatório</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-195"><strong>Report time</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-196">Não</span><span class="sxs-lookup"><span data-stu-id="e914c-196">No</span></span></p></td>
<td><p><span data-ttu-id="e914c-197">Data e hora do registro do relatório.</span><span class="sxs-lookup"><span data-stu-id="e914c-197">Date and time the report was recorded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e914c-198"><strong>Solicitação</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-198"><strong>Request</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-199">Não</span><span class="sxs-lookup"><span data-stu-id="e914c-199">No</span></span></p></td>
<td><p><span data-ttu-id="e914c-p109">Tipo de solicitação SIP. Por exemplo, INVITE ou BYE.</span><span class="sxs-lookup"><span data-stu-id="e914c-p109">SIP request type. For example, INVITE or BYE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e914c-202"><strong>ID do Diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-202"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-203">Não</span><span class="sxs-lookup"><span data-stu-id="e914c-203">No</span></span></p></td>
<td><p><span data-ttu-id="e914c-204">Identificador exclusivo (na forma de um cabeçalho de diagnóstico-ms) anexado a uma mensagem SIP que fornece informações úteis sobre os erros de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="e914c-204">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e914c-205"><strong>Tipo de conteúdo</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-205"><strong>Content type</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-206">Não</span><span class="sxs-lookup"><span data-stu-id="e914c-206">No</span></span></p></td>
<td><p><span data-ttu-id="e914c-p110">Tipo de conteúdo de mídia usado na conferência. Por exemplo, um tipo de conteúdo comum é Application/sdp. O protocolo SDP é um protocolo padrão de Internet usado para comunicados de sessão, convites de sessão e outras formas de início de sessão multimídia.</span><span class="sxs-lookup"><span data-stu-id="e914c-p110">Type of media content used in the conference. For example, a common content type is Application/sdp. Session Description Protocol (SDP) is a standard Internet protocol used for session announcements, session invitations, and other forms of multimedia session initiation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e914c-210"><strong>Relatado por</strong></span><span class="sxs-lookup"><span data-stu-id="e914c-210"><strong>Reported by</strong></span></span></p></td>
<td><p><span data-ttu-id="e914c-211">Não</span><span class="sxs-lookup"><span data-stu-id="e914c-211">No</span></span></p></td>
<td><p><span data-ttu-id="e914c-212">Computador (isso é, o cliente ou servidor) que relatou o problema.</span><span class="sxs-lookup"><span data-stu-id="e914c-212">Computer (that is, client or server) that reported the problem.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e914c-213">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e914c-213">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

