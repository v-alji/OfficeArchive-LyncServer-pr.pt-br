---
title: 'Lync Server 2013: relatório de detalhes da conferência'
description: 'Lync Server 2013: relatório de detalhes da conferência.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Detail Report
ms:assetid: 1d61cd81-dcfe-40b4-9a41-a73b038bc216
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204728(v=OCS.15)
ms:contentKeyID: 48183565
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07c50b545f4a9ee3308a840fc2aa5a15e617a5bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389895"
---
# <a name="conference-detail-report-in-lync-server-2013"></a><span data-ttu-id="db634-103">Relatório de detalhes da conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db634-103">Conference Detail Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="db634-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="db634-104">

<span> </span></span></span>

<span data-ttu-id="db634-105">_**Tópico da última modificação:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="db634-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="db634-p101">O Relatório de Detalhe da Conferência fornece informações detalhadas sobre todos os usuários que participaram de uma conferência. Por exemplo, você pode ver tal informação como a data e hora que um usuário participou da conferência, a data e hora que o usuário saiu da conferência e o agente do usuário do ponto de extremidade que foi usado para conectar o usuário à conferência. Também é possível ver informações da função do usuário em cada conferência (por exemplo, Apresentador ou Participante). Talvez, o mais importante, você pode ver rapidamente quais usuários participaram com sucesso e concluíram a conferência e quais usuários não puderam participar e concluir a conferência.</span><span class="sxs-lookup"><span data-stu-id="db634-p101">The Conference Detail Report provides detailed information about all the users who participated in a conference. For example, you can see such information as the date and time that a user joined the conference, the date and time that the user left the conference, and the user agent of the endpoint that was used to connect that user to the conference. You can also see information the user's role in each conference (for example, Presenter or Attendee). Perhaps most important, you get quickly see which users successfully join and complete the conference, and which users were not able to successfully join and complete the conference.</span></span>

<div>

## <a name="accessing-the-conference-detail-report"></a><span data-ttu-id="db634-110">Acessar o Relatório de Detalhe da Conferência</span><span class="sxs-lookup"><span data-stu-id="db634-110">Accessing the Conference Detail Report</span></span>

<span data-ttu-id="db634-111">O Relatório de Detalhe da Conferência pode ser acessado pelos seguintes relatórios:</span><span class="sxs-lookup"><span data-stu-id="db634-111">The Conference Detail Report can be accessed from the following reports:</span></span>

  - <span data-ttu-id="db634-112">O [relatório de controle de admissão de chamadas no Lync Server 2013](lync-server-2013-call-admission-control-report.md) (clicando na métrica de detalhes de uma conferência)</span><span class="sxs-lookup"><span data-stu-id="db634-112">The [Call Admission Control Report in Lync Server 2013](lync-server-2013-call-admission-control-report.md) (by clicking the Detail metric for a conference)</span></span>

  - <span data-ttu-id="db634-113">O [relatório lista de falhas no Lync Server 2013](lync-server-2013-failure-list-report.md) (clicando na métrica da conferência)</span><span class="sxs-lookup"><span data-stu-id="db634-113">The [Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md) (by clicking the Conference metric)</span></span>

  - <span data-ttu-id="db634-114">O [relatório de atividade do usuário no Lync Server 2013](lync-server-2013-user-activity-report.md) (clicando na métrica de URI de conferência)</span><span class="sxs-lookup"><span data-stu-id="db634-114">The [User Activity Report in Lync Server 2013](lync-server-2013-user-activity-report.md) (by clicking the Conference URI metric)</span></span>

<span data-ttu-id="db634-115">No relatório de detalhes da conferência, você pode acessar o [relatório de diagnóstico no Lync Server 2013](lync-server-2013-diagnostic-report.md) clicando no relatório de diagnóstico (detalhe) métrica.</span><span class="sxs-lookup"><span data-stu-id="db634-115">From the Conference Detail Report you can access the [Diagnostic Report in Lync Server 2013](lync-server-2013-diagnostic-report.md) by clicking the Diagnostic Report (Detail) metric.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="db634-116">Filtros</span><span class="sxs-lookup"><span data-stu-id="db634-116">Filters</span></span>

<span data-ttu-id="db634-p102">Nenhum. Você não pode filtrar o Relatório de Detalhe da Conferência.</span><span class="sxs-lookup"><span data-stu-id="db634-p102">None. You cannot filter on the Conference Detail Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="db634-119">Métricas</span><span class="sxs-lookup"><span data-stu-id="db634-119">Metrics</span></span>

<span data-ttu-id="db634-120">A tabela a seguir lista as informações fornecidas na seção Informação da Conferência do Relatório de Detalhe da Conferência.</span><span class="sxs-lookup"><span data-stu-id="db634-120">The following table lists the information provided in the Conference Information section of the Conference Detail Report.</span></span>

### <a name="conference-information-metrics"></a><span data-ttu-id="db634-121">Métricas de Informação da Conferência</span><span class="sxs-lookup"><span data-stu-id="db634-121">Conference Information Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db634-122">Nome</span><span class="sxs-lookup"><span data-stu-id="db634-122">Name</span></span></th>
<th><span data-ttu-id="db634-123">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="db634-123">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="db634-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="db634-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db634-125"><strong>URI de conferência</strong></span><span class="sxs-lookup"><span data-stu-id="db634-125"><strong>Conference URI</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-p103">URI atribuído à conferência. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="db634-p103">URI assigned to the conference. For example:</span></span></p>
<p><span data-ttu-id="db634-128">sip:kmyer@litwareinc.com;gruu;opaque=app:conf:focus:id:drg2y8v4</span><span class="sxs-lookup"><span data-stu-id="db634-128">sip:kmyer@litwareinc.com;gruu;opaque=app:conf:focus:id:drg2y8v4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db634-129"><strong>FQDN do pool</strong></span><span class="sxs-lookup"><span data-stu-id="db634-129"><strong>Pool FQDN</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-130">Nome de domínio totalmente qualificado do pool do Registrador ou Servidor de Borda envolvido em uma sessão.</span><span class="sxs-lookup"><span data-stu-id="db634-130">Fully-qualified domain name of the Registrar pool or Edge Server involved in a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db634-131"><strong>Hora inicial</strong></span><span class="sxs-lookup"><span data-stu-id="db634-131"><strong>Start time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-132">Data e hora de início da sessão.</span><span class="sxs-lookup"><span data-stu-id="db634-132">Date and time that the conference started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db634-133"><strong>Organizador</strong></span><span class="sxs-lookup"><span data-stu-id="db634-133"><strong>Organizer</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-134">Endereço SIP do usuário que organizou a conferência.</span><span class="sxs-lookup"><span data-stu-id="db634-134">SIP address of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db634-135"><strong>Hora final</strong></span><span class="sxs-lookup"><span data-stu-id="db634-135"><strong>End time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-136">Data e hora em que a conferência terminou.</span><span class="sxs-lookup"><span data-stu-id="db634-136">Date and time that the conference ended.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="db634-137">A tabela a seguir lista as informações oferecidas na Seção de Participação da Conferência do Relatório de Detalhe da Conferência.</span><span class="sxs-lookup"><span data-stu-id="db634-137">The following table lists the information provided in the Conference Participation Section of the Conference Detail Report.</span></span>

### <a name="conference-participation-metrics"></a><span data-ttu-id="db634-138">Métricas de Participação da Conferência</span><span class="sxs-lookup"><span data-stu-id="db634-138">Conference Participation Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db634-139">Nome</span><span class="sxs-lookup"><span data-stu-id="db634-139">Name</span></span></th>
<th><span data-ttu-id="db634-140">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="db634-140">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="db634-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="db634-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db634-142"><strong>Usuário</strong></span><span class="sxs-lookup"><span data-stu-id="db634-142"><strong>User</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-143">Endereço SIP do usuário que participou da conferência.</span><span class="sxs-lookup"><span data-stu-id="db634-143">SIP address of the user who participated in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db634-144"><strong>Função</strong></span><span class="sxs-lookup"><span data-stu-id="db634-144"><strong>Role</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-145">Função (por exemplo, Apresentador) desempenhada pelo participante da conferência.</span><span class="sxs-lookup"><span data-stu-id="db634-145">Role (for example, Presenter) played by the conference participant.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db634-146"><strong>Conectividade</strong></span><span class="sxs-lookup"><span data-stu-id="db634-146"><strong>Connectivity</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-147">Conectividade de rede (normalmente Interna ou Externa) para o participante.</span><span class="sxs-lookup"><span data-stu-id="db634-147">Network connectivity (typically From Internal or From External) for the participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db634-148">Hora da ingresso</span><span class="sxs-lookup"><span data-stu-id="db634-148">Join time</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-149">Data e hora de ingresso do participante na conferência.</span><span class="sxs-lookup"><span data-stu-id="db634-149">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db634-150"><strong>Hora da saída</strong></span><span class="sxs-lookup"><span data-stu-id="db634-150"><strong>Leave time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-151">Data e hora de saída do participante da conferência.</span><span class="sxs-lookup"><span data-stu-id="db634-151">Date and time that the participant left the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db634-152"><strong>Agente do usuário</strong></span><span class="sxs-lookup"><span data-stu-id="db634-152"><strong>User agent</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-153">Identificador do software usado pelo ponto de extremidade do participante.</span><span class="sxs-lookup"><span data-stu-id="db634-153">Identifier for the software used by the participant’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db634-154"><strong>Relatórios de diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="db634-154"><strong>Diagnostic reports</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-p104">Fornece informações de resolução de problemas e diagnóstico. Incluindo códigos de resposta SIP, cabeçalhos de diagnóstico, hora de ingresso na conferência e IDs de diagnósticos para sessões com falha.</span><span class="sxs-lookup"><span data-stu-id="db634-p104">Provides diagnostic and troubleshooting information. Including SIP response codes, diagnostic headers, conference join times, and diagnostic IDs for failed sessions.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="db634-157">A tabela a seguir lista as informações fornecidas na seção de modalidades de conferência do relatório de detalhes da conferência.</span><span class="sxs-lookup"><span data-stu-id="db634-157">The following table lists the information provided in the Conference Modalities section of the Conference Detail Report.</span></span>

### <a name="conference-modalities-metrics"></a><span data-ttu-id="db634-158">Métricas das Modalidades da Conferência</span><span class="sxs-lookup"><span data-stu-id="db634-158">Conference Modalities Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db634-159">Nome</span><span class="sxs-lookup"><span data-stu-id="db634-159">Name</span></span></th>
<th><span data-ttu-id="db634-160">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="db634-160">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="db634-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="db634-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db634-162"><strong>Usuário</strong></span><span class="sxs-lookup"><span data-stu-id="db634-162"><strong>User</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-163">Endereço SIP do usuário que participou da conferência.</span><span class="sxs-lookup"><span data-stu-id="db634-163">SIP address of the user who participated in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db634-164"><strong>Hora da ingresso</strong></span><span class="sxs-lookup"><span data-stu-id="db634-164"><strong>Join time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-165">Data e hora de ingresso do participante na conferência.</span><span class="sxs-lookup"><span data-stu-id="db634-165">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db634-166"><strong>Hora da saída</strong></span><span class="sxs-lookup"><span data-stu-id="db634-166"><strong>Leave time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-167">Data e hora que um participante deixou a conferência.</span><span class="sxs-lookup"><span data-stu-id="db634-167">Date and time that a participant left the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db634-168"><strong>URI do servidor de conferência</strong></span><span class="sxs-lookup"><span data-stu-id="db634-168"><strong>Conferencing server URI</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-169">URI para o servidor de Conferência usado na conferência.</span><span class="sxs-lookup"><span data-stu-id="db634-169">URI for the Conferencing server used in the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db634-170"><strong>Relatórios de diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="db634-170"><strong>Diagnostic reports</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="db634-p105">Fornece informações de resolução de problemas e diagnóstico. Incluindo códigos de resposta SIP, cabeçalhos de diagnóstico, hora de ingresso na conferência e IDs de diagnósticos para sessões com falha.</span><span class="sxs-lookup"><span data-stu-id="db634-p105">Provides diagnostic and troubleshooting information. Including SIP response codes, diagnostic headers, conference join times, and diagnostic IDs for failed sessions.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="db634-173">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="db634-173">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

