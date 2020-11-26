---
title: 'Lync Server 2013: Tabela Session'
description: 'Lync Server 2013: tabela de sessão.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Session table
ms:assetid: 7f05529c-794d-41ed-bca4-2e85b87b2dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398635(v=OCS.15)
ms:contentKeyID: 48184626
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1a52813dfea808253cc934f71a9d4c846c2dbbd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441813"
---
# <a name="session-table-in-lync-server-2013"></a><span data-ttu-id="470bc-103">Tabela Session no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="470bc-103">Session table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="470bc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="470bc-104">

<span> </span></span></span>

<span data-ttu-id="470bc-105">_**Tópico da última modificação:** 2013-09-09_</span><span class="sxs-lookup"><span data-stu-id="470bc-105">_**Topic Last Modified:** 2013-09-09_</span></span>

<span data-ttu-id="470bc-106">Cada registro representa uma sessão que envolve áudio ou áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="470bc-106">Each record represents one session which involves audio or audio and video.</span></span> <span data-ttu-id="470bc-107">Ele contém informações gerais sobre a sessão.</span><span class="sxs-lookup"><span data-stu-id="470bc-107">It contains overall information about the session.</span></span> <span data-ttu-id="470bc-108">Uma sessão é definida como uma caixa de diálogo de protocolo de iniciação de sessão de áudio ou de vídeo (SIP) entre dois pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="470bc-108">A session is defined as an audio or video Session Initiation Protocol (SIP) dialog between two endpoints.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="470bc-109"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="470bc-110"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="470bc-111"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="470bc-112"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="470bc-113"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-113"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-114">datetime</span><span class="sxs-lookup"><span data-stu-id="470bc-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="470bc-115">Primária</span><span class="sxs-lookup"><span data-stu-id="470bc-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="470bc-116">Referenciado pela <a href="lync-server-2013-dialog-table.md">tabela de caixa de diálogo no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="470bc-116">Referenced from the <a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="470bc-117"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-117"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-118">int</span><span class="sxs-lookup"><span data-stu-id="470bc-118">int</span></span></p></td>
<td><p><span data-ttu-id="470bc-119">Primária</span><span class="sxs-lookup"><span data-stu-id="470bc-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="470bc-120">Referenciado pela <a href="lync-server-2013-dialog-table.md">tabela de caixa de diálogo no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="470bc-120">Referenced from the <a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="470bc-121"><strong>ConferenceKey</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-121"><strong>ConferenceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-122">int</span><span class="sxs-lookup"><span data-stu-id="470bc-122">int</span></span></p></td>
<td><p><span data-ttu-id="470bc-123">Exterior</span><span class="sxs-lookup"><span data-stu-id="470bc-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="470bc-124">Chave de conferência.</span><span class="sxs-lookup"><span data-stu-id="470bc-124">Conference key.</span></span> <span data-ttu-id="470bc-125">Referenciado na <a href="lync-server-2013-conference-table.md">tabela de conferências no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="470bc-125">Referenced from the <a href="lync-server-2013-conference-table.md">Conference table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="470bc-126"><strong>CorrelationKey</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-126"><strong>CorrelationKey</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-127">int</span><span class="sxs-lookup"><span data-stu-id="470bc-127">int</span></span></p></td>
<td><p><span data-ttu-id="470bc-128">Exterior</span><span class="sxs-lookup"><span data-stu-id="470bc-128">Foreign</span></span></p></td>
<td><p><span data-ttu-id="470bc-129">Chave de correlação.</span><span class="sxs-lookup"><span data-stu-id="470bc-129">Correlation key.</span></span> <span data-ttu-id="470bc-130">Referenciado pela <a href="lync-server-2013-sessioncorrelation-table.md">tabela SessionCorrelation no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="470bc-130">Referenced from the <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="470bc-131"><strong>DialogCategory</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-131"><strong>DialogCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-132">bit</span><span class="sxs-lookup"><span data-stu-id="470bc-132">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="470bc-133">Categoria da caixa de diálogo; 0 é o servidor do Lync para o segmento do servidor de mediação; 1 é o servidor de mediação para a perna do gateway PSTN.</span><span class="sxs-lookup"><span data-stu-id="470bc-133">Dialog category; 0 is Lync Server to Mediation Server leg; 1 is Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="470bc-134"><strong>MediationServerBypassFlag</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-134"><strong>MediationServerBypassFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-135">bit</span><span class="sxs-lookup"><span data-stu-id="470bc-135">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="470bc-136">Sinalizador que indica se a chamada foi ignorada ou não.</span><span class="sxs-lookup"><span data-stu-id="470bc-136">Flag indicating if the call was bypassed or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="470bc-137"><strong>MediaBypassWarningFlag</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-137"><strong>MediaBypassWarningFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-138">int</span><span class="sxs-lookup"><span data-stu-id="470bc-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="470bc-139">Esse campo, se presente, indicará por que uma chamada não foi ignorada mesmo se as IDs de bypass forem atendidas.</span><span class="sxs-lookup"><span data-stu-id="470bc-139">This field, if present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="470bc-140">Para o Lync Server, somente um valor é definido.</span><span class="sxs-lookup"><span data-stu-id="470bc-140">For Lync Server, only one value is defined.</span></span></p>
<p><span data-ttu-id="470bc-141">0x0001 – ID de bypass desconhecido para o adaptador de rede padrão.</span><span class="sxs-lookup"><span data-stu-id="470bc-141">0x0001 – Unknown bypass ID for Default network adapter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="470bc-142"><strong>StartTime </strong></span><span class="sxs-lookup"><span data-stu-id="470bc-142"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-143">datetime</span><span class="sxs-lookup"><span data-stu-id="470bc-143">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="470bc-144">Hora de início da chamada.</span><span class="sxs-lookup"><span data-stu-id="470bc-144">Call start time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="470bc-145"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-145"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-146">datetime</span><span class="sxs-lookup"><span data-stu-id="470bc-146">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="470bc-147">Hora de término da chamada.</span><span class="sxs-lookup"><span data-stu-id="470bc-147">Call end time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="470bc-148"><strong>CallerPool</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-148"><strong>CallerPool</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-149">int</span><span class="sxs-lookup"><span data-stu-id="470bc-149">int</span></span></p></td>
<td><p><span data-ttu-id="470bc-150">Exterior</span><span class="sxs-lookup"><span data-stu-id="470bc-150">Foreign</span></span></p></td>
<td><p><span data-ttu-id="470bc-151">O pool do chamador.</span><span class="sxs-lookup"><span data-stu-id="470bc-151">The pool of the caller.</span></span> <span data-ttu-id="470bc-152">Referenciado na <a href="lync-server-2013-pool-table.md">tabela pool no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="470bc-152">Referenced from the <a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="470bc-153"><strong>CalleePool</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-153"><strong>CalleePool</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-154">int</span><span class="sxs-lookup"><span data-stu-id="470bc-154">int</span></span></p></td>
<td><p><span data-ttu-id="470bc-155">Exterior</span><span class="sxs-lookup"><span data-stu-id="470bc-155">Foreign</span></span></p></td>
<td><p><span data-ttu-id="470bc-156">O pool do receptor da chamada.</span><span class="sxs-lookup"><span data-stu-id="470bc-156">The pool of the call receiver.</span></span> <span data-ttu-id="470bc-157">Referenciado na <a href="lync-server-2013-pool-table.md">tabela pool no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="470bc-157">Referenced from the <a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="470bc-158"><strong>CalleePAI</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-158"><strong>CalleePAI</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-159">int</span><span class="sxs-lookup"><span data-stu-id="470bc-159">int</span></span></p></td>
<td><p><span data-ttu-id="470bc-160">Exterior</span><span class="sxs-lookup"><span data-stu-id="470bc-160">Foreign</span></span></p></td>
<td><p><span data-ttu-id="470bc-161">O URI de SIP na identidade SIP p-declarated (PAI) do ponto de extremidade de recebimento.</span><span class="sxs-lookup"><span data-stu-id="470bc-161">SIP URI in the SIP p-asserted identity (PAI) of the receiving endpoint.</span></span> <span data-ttu-id="470bc-162">Referenciado da <a href="lync-server-2013-user-table.md">tabela de usuário no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="470bc-162">Referenced from the <a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="470bc-163"><strong>CallerURI</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-163"><strong>CallerURI</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-164">int</span><span class="sxs-lookup"><span data-stu-id="470bc-164">int</span></span></p></td>
<td><p><span data-ttu-id="470bc-165">Exterior</span><span class="sxs-lookup"><span data-stu-id="470bc-165">Foreign</span></span></p></td>
<td><p><span data-ttu-id="470bc-166">URI do chamador.</span><span class="sxs-lookup"><span data-stu-id="470bc-166">Caller’s URI.</span></span> <span data-ttu-id="470bc-167">Referenciado da <a href="lync-server-2013-user-table.md">tabela de usuário no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="470bc-167">Referenced from the <a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="470bc-168"><strong>CallerEndpoint</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-168"><strong>CallerEndpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-169">int</span><span class="sxs-lookup"><span data-stu-id="470bc-169">int</span></span></p></td>
<td><p><span data-ttu-id="470bc-170">Exterior</span><span class="sxs-lookup"><span data-stu-id="470bc-170">Foreign</span></span></p></td>
<td><p><span data-ttu-id="470bc-171">Ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="470bc-171">Caller’s endpoint.</span></span> <span data-ttu-id="470bc-172">Referenciado na <a href="lync-server-2013-endpoint-table.md">tabela de pontos de extremidade no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="470bc-172">Referenced from the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="470bc-173"><strong>CallerUserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-173"><strong>CallerUserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-174">bit</span><span class="sxs-lookup"><span data-stu-id="470bc-174">bit</span></span></p></td>
<td><p><span data-ttu-id="470bc-175">Exterior</span><span class="sxs-lookup"><span data-stu-id="470bc-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="470bc-176">Agente de usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="470bc-176">Caller’s user agent.</span></span> <span data-ttu-id="470bc-177">Referenciado na <a href="lync-server-2013-useragent-table.md">tabela UserAgent no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="470bc-177">Referenced from the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="470bc-178"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-178"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-179">smallint</span><span class="sxs-lookup"><span data-stu-id="470bc-179">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="470bc-180">A prioridade desta chamada.</span><span class="sxs-lookup"><span data-stu-id="470bc-180">The priority of this call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="470bc-181"><strong>ClassifiedPoorCall</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-181"><strong>ClassifiedPoorCall</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-182">bit</span><span class="sxs-lookup"><span data-stu-id="470bc-182">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="470bc-183">Esta coluna foi preterida e não é usada no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="470bc-183">This column has been deprecated and is not used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="470bc-184">Em vez disso, essas informações são relatadas em bases de linhas por mídia.</span><span class="sxs-lookup"><span data-stu-id="470bc-184">Instead, this information is reported on a per-media line bases.</span></span> <span data-ttu-id="470bc-185">Consulte a <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="470bc-185">Refer to the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="470bc-186"><strong>CallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-186"><strong>CallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-187">int</span><span class="sxs-lookup"><span data-stu-id="470bc-187">int</span></span></p></td>
<td><p><span data-ttu-id="470bc-188">Exterior</span><span class="sxs-lookup"><span data-stu-id="470bc-188">Foreign</span></span></p></td>
<td><p><span data-ttu-id="470bc-189">P-declarado-identidade do usuário que fez a chamada.</span><span class="sxs-lookup"><span data-stu-id="470bc-189">P-Asserted-Identity of the user who placed the call.</span></span> <span data-ttu-id="470bc-190">A identidade de P-declarada (PAI) é usada para transmitir a verdadeira identidade do usuário que fez a chamada.</span><span class="sxs-lookup"><span data-stu-id="470bc-190">The P-Asserted-Identity (PAI) is used to convey the true identity of the user who placed the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="470bc-191"><strong>CalleeEndpoint</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-191"><strong>CalleeEndpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-192">int</span><span class="sxs-lookup"><span data-stu-id="470bc-192">int</span></span></p></td>
<td><p><span data-ttu-id="470bc-193">Exterior</span><span class="sxs-lookup"><span data-stu-id="470bc-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="470bc-194">Ponto de extremidade que recebeu a chamada.</span><span class="sxs-lookup"><span data-stu-id="470bc-194">Endpoint that received the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="470bc-195"><strong>CalleeUserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-195"><strong>CalleeUserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-196">int</span><span class="sxs-lookup"><span data-stu-id="470bc-196">int</span></span></p></td>
<td><p><span data-ttu-id="470bc-197">Exterior</span><span class="sxs-lookup"><span data-stu-id="470bc-197">Foreign</span></span></p></td>
<td><p><span data-ttu-id="470bc-198">Agente de usuário empregado pelo usuário que recebeu a chamada.</span><span class="sxs-lookup"><span data-stu-id="470bc-198">User agent employed by the user who received the call.</span></span> <span data-ttu-id="470bc-199">Os agentes de usuário representam o dispositivo de ponto de extremidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="470bc-199">User agents represent the client endpoint device.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="470bc-200"><strong>CalleeUri</strong></span><span class="sxs-lookup"><span data-stu-id="470bc-200"><strong>CalleeUri</strong></span></span></p></td>
<td><p><span data-ttu-id="470bc-201">int</span><span class="sxs-lookup"><span data-stu-id="470bc-201">int</span></span></p></td>
<td><p><span data-ttu-id="470bc-202">Exterior</span><span class="sxs-lookup"><span data-stu-id="470bc-202">Foreign</span></span></p></td>
<td><p><span data-ttu-id="470bc-203">O URI SIP do usuário que recebeu a chamada.</span><span class="sxs-lookup"><span data-stu-id="470bc-203">SIP URI of the user who received the call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="470bc-204">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="470bc-204">


</div>

<span> </span>

</div>

</div>

</span></span></div>

