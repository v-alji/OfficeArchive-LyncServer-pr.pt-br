---
title: 'Lync Server 2013: modo de exibição AudioStreamDetail'
description: 'Lync Server 2013: modo de exibição AudioStreamDetail.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStreamDetail view
ms:assetid: b6a435b3-103c-41c4-96ed-33c3784534c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721859(v=OCS.15)
ms:contentKeyID: 49733792
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92c4c9bbb4f126e242e28d835222f6ba2af89d8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438159"
---
# <a name="audiostreamdetail-view-in-lync-server-2013"></a><span data-ttu-id="9f9b0-103">Exibição AudioStreamDetail no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f9b0-103">AudioStreamDetail view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9f9b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9f9b0-104">

<span> </span></span></span>

<span data-ttu-id="9f9b0-105">_**Tópico da última modificação:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="9f9b0-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="9f9b0-106">A exibição AudioStreamDetail armazena informações sobre cada fluxo de áudio no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-106">The AudioStreamDetail View stores information about each audio stream in the database.</span></span> <span data-ttu-id="9f9b0-107">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f9b0-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="9f9b0-108">Column</span></span></th>
<th><span data-ttu-id="9f9b0-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9f9b0-109">Data Type</span></span></th>
<th><span data-ttu-id="9f9b0-110">Detalhes</span><span class="sxs-lookup"><span data-stu-id="9f9b0-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-111">Sessiontime</span><span class="sxs-lookup"><span data-stu-id="9f9b0-111">SessionTime</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-112">datetime</span><span class="sxs-lookup"><span data-stu-id="9f9b0-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-113">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-113">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-114">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="9f9b0-114">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-115">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-115">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-116">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-116">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-117">Streamid</span><span class="sxs-lookup"><span data-stu-id="9f9b0-117">StreamId</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-118">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-118">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-119">ID exclusiva dentro de uma linha de mídia.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-119">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-120">StartTime </span><span class="sxs-lookup"><span data-stu-id="9f9b0-120">StartTime</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-121">datetime</span><span class="sxs-lookup"><span data-stu-id="9f9b0-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-122">Hora de início da sessão.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-122">Start time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-123">EndTime</span><span class="sxs-lookup"><span data-stu-id="9f9b0-123">EndTime</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-124">datetime</span><span class="sxs-lookup"><span data-stu-id="9f9b0-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-125">Hora de término da sessão.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-125">End time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-126">DialogCategory</span><span class="sxs-lookup"><span data-stu-id="9f9b0-126">DialogCategory</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-127">bit</span><span class="sxs-lookup"><span data-stu-id="9f9b0-127">bit</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-128">Categoria do diálogo: 0 é o servidor do Lync para o trecho do servidor de mediação; 1 é o servidor de mediação para a perna do gateway PSTN.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-128">Dialog category: 0 is the Lync Server to Mediation Server leg; 1 is the Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-129">MediationServerBypassFlag</span><span class="sxs-lookup"><span data-stu-id="9f9b0-129">MediationServerBypassFlag</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-130">bit</span><span class="sxs-lookup"><span data-stu-id="9f9b0-130">bit</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-131">Sinalizador que indica se a chamada foi ignorada ou não.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-131">Flag indicating if the call was bypassed or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-132">MediaBypassWarningFlag</span><span class="sxs-lookup"><span data-stu-id="9f9b0-132">MediaBypassWarningFlag</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-133">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-133">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-134">Se presente, indica por que uma chamada não foi ignorada mesmo se as IDs de bypass forem atendidas.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-134">If present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="9f9b0-135">Somente um valor é definido:</span><span class="sxs-lookup"><span data-stu-id="9f9b0-135">Only one value is defined:</span></span></p>
<p><span data-ttu-id="9f9b0-136">0x0001 – ID de bypass desconhecido para o adaptador de rede padrão.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-136">0x0001 – Unknown bypass ID for Default network adapter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-137">CallPriority</span><span class="sxs-lookup"><span data-stu-id="9f9b0-137">CallPriority</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-138">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-138">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-139">Prioridade da chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-139">Priority of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-140">CallerPool</span><span class="sxs-lookup"><span data-stu-id="9f9b0-140">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-142">FQDN do pool de chamadas.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-142">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-143">CalleePool</span><span class="sxs-lookup"><span data-stu-id="9f9b0-143">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-144">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-144">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-145">FQDN do pool do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-145">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-146">Chamador</span><span class="sxs-lookup"><span data-stu-id="9f9b0-146">Caller</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-148">URI do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-148">Caller’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-149">Receptor</span><span class="sxs-lookup"><span data-stu-id="9f9b0-149">Callee</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-150">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-150">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-151">URI do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-151">Callee’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-152">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="9f9b0-152">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-154">Cadeia de caracteres do agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-154">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-155">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="9f9b0-155">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-156">smallint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-156">smallint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-157">Tipo de agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-157">Type of the caller’s user agent.</span></span> <span data-ttu-id="9f9b0-158">Consulte a <a href="lync-server-2013-useragent-table.md">tabela UserAgent no Lync Server 2013</a> para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-158">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-159">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="9f9b0-159">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-160">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-160">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-161">Categoria do agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-161">Category of the caller’s user agent.</span></span> <span data-ttu-id="9f9b0-162">Consulte a <a href="lync-server-2013-useragentdef-table-qoe.md">tabela UserAgentDef (QoE) no Lync Server 2013</a> para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-162">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-163">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="9f9b0-163">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-164">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-164">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-165">Cadeia de caracteres do agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-165">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-166">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="9f9b0-166">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-167">smallint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-167">smallint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-168">Tipo de agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-168">Type of callee’s user agent.</span></span> <span data-ttu-id="9f9b0-169">Consulte a <a href="lync-server-2013-useragent-table.md">tabela UserAgent no Lync Server 2013</a> para obter informações.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-169">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-170">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="9f9b0-170">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-171">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-171">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-172">Categoria do agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-172">Category of callee’s user agent.</span></span> <span data-ttu-id="9f9b0-173">Consulte a <a href="lync-server-2013-useragentdef-table-qoe.md">tabela UserAgentDef (QoE) no Lync Server 2013</a> para obter informações.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-173">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-174">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-174">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-175">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-175">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-176">Nome do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-176">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-177">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-177">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-178">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-178">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-179">Nome do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-179">Callee’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-180">CallerOS</span><span class="sxs-lookup"><span data-stu-id="9f9b0-180">CallerOS</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-181">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="9f9b0-181">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-182">Sistema operacional (SO) do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-182">Operating system (OS) of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-183">CalleeOS</span><span class="sxs-lookup"><span data-stu-id="9f9b0-183">CalleeOS</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-184">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="9f9b0-184">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-185">Sistema operacional (SO) do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-185">Operating system (OS) of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-186">CallerCPUName</span><span class="sxs-lookup"><span data-stu-id="9f9b0-186">CallerCPUName</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-187">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="9f9b0-187">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-188">Nome da CPU do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-188">CPU name of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-189">CalleeCPUName</span><span class="sxs-lookup"><span data-stu-id="9f9b0-189">CalleeCPUName</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-190">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="9f9b0-190">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-191">Nome da CPU do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-191">CPU name of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-192">CallerCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="9f9b0-192">CallerCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-193">smallint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-193">smallint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-194">Número de núcleos da CPU no ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-194">Number of CPU cores in the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-195">CalleeCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="9f9b0-195">CalleeCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-196">smallint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-196">smallint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-197">Número de núcleos da CPU no ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-197">Number of CPU cores in the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-198">CallerCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="9f9b0-198">CallerCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-199">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-199">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-200">Velocidade do processador da CPU do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-200">CPU processor speed of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-201">CalleeCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="9f9b0-201">CalleeCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-202">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-202">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-203">Velocidade do processador da CPU do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-203">CPU processor speed of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-204">CallerVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="9f9b0-204">CallerVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-205">tinyint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-205">tinyint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-206">Indica se o sistema do chamador está em execução em um ambiente virtualizado.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-206">Indicates whether the caller’s system is running in a virtualized environment.</span></span> <span data-ttu-id="9f9b0-207">Consulte a <a href="lync-server-2013-endpoint-table.md">tabela de pontos de extremidade no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-207">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-208">CalleeVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="9f9b0-208">CalleeVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-209">tinyint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-209">tinyint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-210">Indica se o sistema do chamador está em execução em um ambiente virtualizado.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-210">Indicates whether the callee’s system is running in a virtualized environment.</span></span> <span data-ttu-id="9f9b0-211">Consulte a <a href="lync-server-2013-endpoint-table.md">tabela de pontos de extremidade no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-211">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-212">CorrelationKey</span><span class="sxs-lookup"><span data-stu-id="9f9b0-212">CorrelationKey</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9f9b0-213">Chave de correlação.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-213">Correlation key.</span></span> <span data-ttu-id="9f9b0-214">Referenciado pela <a href="lync-server-2013-sessioncorrelation-table.md">tabela SessionCorrelation no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-214">Referenced from the <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-215">ConnectivityIce</span><span class="sxs-lookup"><span data-stu-id="9f9b0-215">ConnectivityIce</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-216">tinyint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-216">tinyint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-217">Informações sobre o caminho de mídia, como direta ou retransmitida.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-217">Information about the media path, such as direct or relayed.</span></span> <span data-ttu-id="9f9b0-218">Consulte a <a href="lync-server-2013-medialine-table.md">tabela de mídia no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-218">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-219">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="9f9b0-219">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-220">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-220">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-221">Informações sobre o processo de estabelecimento de conectividade interativa (ICE) descrito em sinalizadores de bits para o chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-221">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="9f9b0-222">Para obter detalhes, consulte a especificação de protocolo de servidor de monitoração de experiência de qualidade.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-222">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-223">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="9f9b0-223">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-224">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-224">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-225">Informações sobre o processo de estabelecimento de conectividade interativa (ICE) descrito em sinalizadores de bits para o chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-225">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="9f9b0-226">Para obter detalhes, consulte a especificação de protocolo de servidor de monitoração de experiência de qualidade.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-226">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-227">SMTP</span><span class="sxs-lookup"><span data-stu-id="9f9b0-227">Transport</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-228">tinyint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-228">tinyint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-229">Tipo de transporte: 0 é UDP; 1 é o TCP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-229">Transport type: 0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-230">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="9f9b0-230">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-231">var (50)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-231">var(50)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-232">Endereço IP do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-232">IP address of the caller.</span></span> <span data-ttu-id="9f9b0-233">Pode ser um endereço IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-233">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-234">CallerPort</span><span class="sxs-lookup"><span data-stu-id="9f9b0-234">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-235">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-235">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-236">Porta usada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-236">Port used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-237">CallerInside</span><span class="sxs-lookup"><span data-stu-id="9f9b0-237">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-238">bit</span><span class="sxs-lookup"><span data-stu-id="9f9b0-238">bit</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-239">Indica se o chamador está dentro da rede de intervalo: 1 significa que a chamada está dentro da rede corporativa, 0 significa que o chamador está fora da rede.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-239">Indicates whether the caller is inside the interval network: 1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-240">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="9f9b0-240">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-241">var (50)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-241">var(50)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-242">Endereço IP do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-242">IP address of the callee.</span></span> <span data-ttu-id="9f9b0-243">Pode ser um endereço IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-243">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-244">CalleePort</span><span class="sxs-lookup"><span data-stu-id="9f9b0-244">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-245">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-245">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-246">Porta usada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-246">Port used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-247">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="9f9b0-247">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-248">bit</span><span class="sxs-lookup"><span data-stu-id="9f9b0-248">bit</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-249">Indica se a chamada está dentro do intervalo de rede: 1 significa que a chamada está dentro da rede corporativa, 0 significa que o chamador está fora da rede.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-249">Indicates whether the callee is inside the interval network: 1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-250">CallerUserSite</span><span class="sxs-lookup"><span data-stu-id="9f9b0-250">CallerUserSite</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-251">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="9f9b0-251">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-252">Nome do site do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-252">Name of the caller’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-253">CallerRegion</span><span class="sxs-lookup"><span data-stu-id="9f9b0-253">CallerRegion</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-254">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="9f9b0-254">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-255">Nome do país/região do site do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-255">Name of the country/region of the caller’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-256">CalleeUserSite</span><span class="sxs-lookup"><span data-stu-id="9f9b0-256">CalleeUserSite</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-257">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="9f9b0-257">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-258">Nome do site do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-258">Name of the callee’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-259">CalleeRegion</span><span class="sxs-lookup"><span data-stu-id="9f9b0-259">CalleeRegion</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-260">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="9f9b0-260">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-261">Nome do país/região do site do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-261">Name of the country/region of the callee’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-262">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="9f9b0-262">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-263">var (50)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-263">var(50)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-264">Endereço IP do serviço de borda A/V usado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-264">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="9f9b0-265">Consulte a <a href="lync-server-2013-ipaddress-table.md">tabela IPAddress no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-265">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-266">CallerRelayPort</span><span class="sxs-lookup"><span data-stu-id="9f9b0-266">CallerRelayPort</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-267">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-267">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-268">Porta usada no serviço de borda A/V usado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-268">Port used on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-269">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="9f9b0-269">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-270">var (50)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-270">var(50)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-271">Chave de endereço IP do serviço de borda A/V usado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-271">IP Address key of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="9f9b0-272">Consulte a <a href="lync-server-2013-ipaddress-table.md">tabela IPAddress no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-272">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-273">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="9f9b0-273">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-274">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-274">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-275">Porta usada no serviço de borda A/V usado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-275">Port used on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-276">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="9f9b0-276">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-277">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-277">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-278">Nome do dispositivo de captura do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-278">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-279">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="9f9b0-279">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-280">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-280">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-281">Nome do dispositivo de renderização do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-281">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-282">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="9f9b0-282">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-283">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-283">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-284">Nome do driver do dispositivo de captura do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-284">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-285">CallerRenderDriver</span><span class="sxs-lookup"><span data-stu-id="9f9b0-285">CallerRenderDriver</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-286">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-286">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-287">O nome do driver de dispositivo de renderização do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-287">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-288">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="9f9b0-288">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-289">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-289">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-290">Nome do dispositivo de captura do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-290">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-291">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="9f9b0-291">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-292">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-292">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-293">Nome do dispositivo de renderização do Calle.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-293">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-294">CalleeCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="9f9b0-294">CalleeCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-295">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-295">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-296">Nome do driver do dispositivo de captura do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-296">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-297">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="9f9b0-297">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-298">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-298">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-299">Chame o nome do driver do dispositivo de processamento do recurso.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-299">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-300">CallerNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="9f9b0-300">CallerNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-301">tinyint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-301">tinyint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-302">Tipo de conexão de rede do chamador: 0 é cabeado, 1 é sem fio.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-302">Caller’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-303">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="9f9b0-303">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-304">bit</span><span class="sxs-lookup"><span data-stu-id="9f9b0-304">bit</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-305">Indica se o chamador está conectado por meio de uma rede privada virtual: 1 é uma rede virtual privada (VPN), 0 não é VPN.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-305">Indicates whether the caller connected over a virtual private network: 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-306">CallerLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="9f9b0-306">CallerLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-307">decimal (18, 0)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-307">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-308">Velocidade do link de rede para o ponto de extremidade do chamador em bps.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-308">Network link speed for the caller's endpoint in bps.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-309">CalleeNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="9f9b0-309">CalleeNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-310">tinyint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-310">tinyint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-311">Tipo de conexão de rede do chamador: 0 é cabeado, 1 é sem fio.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-311">Callee’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-312">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="9f9b0-312">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-313">bit</span><span class="sxs-lookup"><span data-stu-id="9f9b0-313">bit</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-314">Indica se o chamador está conectado por meio de uma rede privada virtual: 1 é uma rede virtual privada (VPN), 0 não é VPN.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-314">Indicates whether the caller connected over a virtual private network: 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-315">CalleeLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="9f9b0-315">CalleeLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-316">decimal (18, 0)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-316">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-317">Velocidade do link de rede para o ponto de extremidade do chamador em bps.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-317">Network link speed for the callee's endpoint in bps.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-318">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="9f9b0-318">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-319">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-319">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-320">O MOS de conversa de banda estreita das sessões de áudio (com base nos dois fluxos de áudio).</span><span class="sxs-lookup"><span data-stu-id="9f9b0-320">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-321">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="9f9b0-321">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-322">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-322">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-323">A largura de banda real aplicada ao fluxo de envio do lado fornecido tem várias configurações de política (ativar, API, SDP, servidor de política e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="9f9b0-323">Actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="9f9b0-324">Isso não deve ser confundido com a largura de banda efetiva porque pode haver uma largura de banda mais econômica com base na estimativa de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-324">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="9f9b0-325">Isso é basicamente a largura de banda máxima que o fluxo de envio pode ter limites de bloqueio impostos pela estimativa da largura de banda</span><span class="sxs-lookup"><span data-stu-id="9f9b0-325">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-326">JitterInterArrival</span><span class="sxs-lookup"><span data-stu-id="9f9b0-326">JitterInterArrival</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-327">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-327">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-328">Tremulação média de rede de estatísticas de protocolo de controle de tempo real (RTCP).</span><span class="sxs-lookup"><span data-stu-id="9f9b0-328">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-329">JitterInterArrivalMax</span><span class="sxs-lookup"><span data-stu-id="9f9b0-329">JitterInterArrivalMax</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-330">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-330">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-331">Maior tremulação de rede durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-331">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-332">PacketLossRate</span><span class="sxs-lookup"><span data-stu-id="9f9b0-332">PacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-333">decimal (5, 4)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-333">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-334">Taxa média de perda de pacotes durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-334">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-335">PacketLossRateMax</span><span class="sxs-lookup"><span data-stu-id="9f9b0-335">PacketLossRateMax</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-336">decimal (5, 4)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-336">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-337">Perda máxima de pacote observado durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-337">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-338">BurstDensity</span><span class="sxs-lookup"><span data-stu-id="9f9b0-338">BurstDensity</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-339">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-339">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-340">Densidade média de perda de pacote durante intermitências de perdas durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-340">Average density of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-341">BurstDuration</span><span class="sxs-lookup"><span data-stu-id="9f9b0-341">BurstDuration</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-342">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-342">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-343">Duração média da perda de pacote durante intermitências de perdas durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-343">Average duration of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-344">BurstGapDensity</span><span class="sxs-lookup"><span data-stu-id="9f9b0-344">BurstGapDensity</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-345">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-345">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-346">Densidade média de perda de pacote durante intervalos entre intermitências de perda de pacote.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-346">Average density of packet loss during gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-347">BurstGapDuration</span><span class="sxs-lookup"><span data-stu-id="9f9b0-347">BurstGapDuration</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-348">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-348">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-349">Duração média de lacunas entre intermitências de perda de pacote.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-349">Average duration of gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-350">PacketUtilization</span><span class="sxs-lookup"><span data-stu-id="9f9b0-350">PacketUtilization</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-351">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-351">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-352">Contagem de pacotes para o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-352">Packet count for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-353">Largura de banda</span><span class="sxs-lookup"><span data-stu-id="9f9b0-353">BandwidthEst</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-354">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-354">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-355">Estimativas de largura de banda para o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-355">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-356">DegradationAvg</span><span class="sxs-lookup"><span data-stu-id="9f9b0-356">DegradationAvg</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-357">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-357">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-358">Degradação do MOS de rede para toda a chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-358">Network MOS Degradation for the whole call.</span></span> <span data-ttu-id="9f9b0-359">O intervalo é de 0,0 a 5,0.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-359">Range is 0.0 to 5.0.</span></span> <span data-ttu-id="9f9b0-360">Essa métrica mostra o valor que o MOS de rede foi reduzido devido à instabilidade e à perda de pacote.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-360">This metric shows the amount the Network MOS was reduced because of jitter and packet loss.</span></span> <span data-ttu-id="9f9b0-361">Para ter uma qualidade aceitável, ele deve ser menor do que 0,5.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-361">For acceptable quality it should less than 0.5.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-362">DegradationMax</span><span class="sxs-lookup"><span data-stu-id="9f9b0-362">DegradationMax</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-363">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-363">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-364">Degradação do MOS de rede máxima durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-364">Maximum Network MOS degradation during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-365">DegradationJitterAvg</span><span class="sxs-lookup"><span data-stu-id="9f9b0-365">DegradationJitterAvg</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-366">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-366">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-367">Degradação de MOS de rede causada pela tremulação.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-367">Network MOS degradation caused by jitter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-368">DegradationPacketLossAvg</span><span class="sxs-lookup"><span data-stu-id="9f9b0-368">DegradationPacketLossAvg</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-369">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-369">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-370">Degradação de MOS de rede causada por perda de pacote.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-370">Network MOS degradation caused by packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-371">PayloadDescription</span><span class="sxs-lookup"><span data-stu-id="9f9b0-371">PayloadDescription</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-372">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-372">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-373">O codec de áudio usado para a chamada, referenciado pela <a href="lync-server-2013-payloaddescription-table.md">tabela PayloadDescription no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-373">The audio codec used for the call, referenced from the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-374">AudioSampleRate</span><span class="sxs-lookup"><span data-stu-id="9f9b0-374">AudioSampleRate</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-375">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-375">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-376">Taxa de amostragem do fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-376">Sampling rate for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-377">CallerSendSignalLevel</span><span class="sxs-lookup"><span data-stu-id="9f9b0-377">CallerSendSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-378">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-378">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-379">O nível de sinal de áudio pós-analógico de controle de ganho para o áudio enviado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-379">Post-Analog Gain Control audio signal level for the audio the caller sent.</span></span> <span data-ttu-id="9f9b0-380">A unidade para essa métrica é dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-380">The unit for this metric is dBmo.</span></span> <span data-ttu-id="9f9b0-381">Para ter uma qualidade aceitável, ele deve ter pelo menos 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-381">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="9f9b0-382">Essa métrica não é reportada pelo servidor de conferência A/V ou por telefones IP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-382">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-383">CallerRecvSignalLevel</span><span class="sxs-lookup"><span data-stu-id="9f9b0-383">CallerRecvSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-384">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-384">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-385">Nível de sinal de áudio para o áudio recebido pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-385">Audio signal level for the audio the caller received.</span></span> <span data-ttu-id="9f9b0-386">A unidade para essa métrica é dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-386">The unit for this metric is dBmo.</span></span> <span data-ttu-id="9f9b0-387">Para ter uma qualidade aceitável, ele deve ter pelo menos 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-387">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="9f9b0-388">Essa métrica não é reportada pelo servidor de conferência A/V ou por telefones IP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-388">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-389">CallerSendNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="9f9b0-389">CallerSendNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-390">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-390">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-391">Nível de ruído de áudio de controle de ganho analógico-analógico para o áudio enviado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-391">Post-Analog Gain Control audio noise level for the audio the caller sent.</span></span> <span data-ttu-id="9f9b0-392">A unidade para essa métrica é dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-392">The unit for this metric is dBmo.</span></span> <span data-ttu-id="9f9b0-393">Para ter uma qualidade aceitável, deve ser menor do que 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-393">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="9f9b0-394">Essa métrica não é reportada pelo servidor de conferência A/V ou por telefones IP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-394">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-395">CallerRecvNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="9f9b0-395">CallerRecvNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-396">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-396">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-397">Nível de ruído de áudio de controle de ganho analógico-analógico para o áudio recebido pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-397">Post-Analog Gain Control audio noise level for the audio the caller received.</span></span> <span data-ttu-id="9f9b0-398">A unidade para essa métrica é dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-398">The unit for this metric is dBmo.</span></span> <span data-ttu-id="9f9b0-399">Para ter uma qualidade aceitável, deve ser menor do que 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-399">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="9f9b0-400">Essa métrica não é reportada pelo servidor de conferência A/V ou por telefones IP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-400">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-401">CallerEchoReturn</span><span class="sxs-lookup"><span data-stu-id="9f9b0-401">CallerEchoReturn</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-402">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-402">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-403">Aprimoramento da perda de retorno de eco para o chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-403">Echo Return Loss Enhancement for the caller.</span></span> <span data-ttu-id="9f9b0-404">A unidade para essa métrica é dB.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-404">The unit for this metric is dB.</span></span> <span data-ttu-id="9f9b0-405">Valores inferiores representam menos eco.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-405">Lower values represent less echo.</span></span> <span data-ttu-id="9f9b0-406">Essa métrica não é reportada pelo servidor de conferência A/V ou por telefones IP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-406">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-407">CallerSpeakerGlitchRate</span><span class="sxs-lookup"><span data-stu-id="9f9b0-407">CallerSpeakerGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-408">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-408">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-409">Média de falhas por cinco minutos para a renderização de alto-falante do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-409">Average glitches per five minutes for the caller’s loudspeaker rendering.</span></span> <span data-ttu-id="9f9b0-410">Para ter uma boa qualidade, isso deve ser inferior a um por cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-410">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="9f9b0-411">Não relatado por servidores de conferência A/V, servidores de mediação ou telefones IP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-411">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-412">CallerMicGlitchRate</span><span class="sxs-lookup"><span data-stu-id="9f9b0-412">CallerMicGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-413">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-413">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-414">Média de falhas por cinco minutos para a captura de microfone do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-414">Average glitches per five minutes for the caller’s microphone capture.</span></span> <span data-ttu-id="9f9b0-415">Para ter uma boa qualidade, isso deve ser inferior a um por cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-415">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="9f9b0-416">Não relatado por servidores de conferência A/V, servidores de mediação ou telefones IP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-416">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-417">CallerTimestampDriftRateMic</span><span class="sxs-lookup"><span data-stu-id="9f9b0-417">CallerTimestampDriftRateMic</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-418">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-418">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-419">Taxa de descompasso do relógio do dispositivo de microfone do chamador, relativa ao relógio da CPU.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-419">Caller’s microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-420">CallerTimestampDriftRateSpk</span><span class="sxs-lookup"><span data-stu-id="9f9b0-420">CallerTimestampDriftRateSpk</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-421">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-421">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-422">Taxa de descompasso do relógio do dispositivo de alto-falante do chamador em relação ao relógio da CPU.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-422">Caller’s speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-423">CallerTimestampErrorMicMs</span><span class="sxs-lookup"><span data-stu-id="9f9b0-423">CallerTimestampErrorMicMs</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-424">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-424">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-425">Erro de carimbo de data/hora médio do fluxo de captura de microfone, em milissegundos, nos últimos 20 segundos da chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-425">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-426">CallerTimestampErrorSpkMs</span><span class="sxs-lookup"><span data-stu-id="9f9b0-426">CallerTimestampErrorSpkMs</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-427">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-427">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-428">Média do alto-falante do chamador processar carimbo de data/hora do fluxo, em milissegundos, nos últimos 20 segundos da chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-428">Average of the caller’s speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-429">CallerVsEntryCauses</span><span class="sxs-lookup"><span data-stu-id="9f9b0-429">CallerVsEntryCauses</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-430">smallint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-430">smallint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-431">A opção de voz é um modo Half-duplex com capacidade de interrupção reduzida.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-431">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="9f9b0-432">Consulte a <a href="lync-server-2013-medialine-table.md">tabela de mídia no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-432">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-433">CallerEchoEventCauses</span><span class="sxs-lookup"><span data-stu-id="9f9b0-433">CallerEchoEventCauses</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-434">tinyint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-434">tinyint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-435">Causa de um evento de eco para o chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-435">Causes of an echo event for the caller.</span></span> <span data-ttu-id="9f9b0-436">Consulte a <a href="lync-server-2013-medialine-table.md">tabela de mídia no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-436">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-437">CallerEchoPercentMicIn</span><span class="sxs-lookup"><span data-stu-id="9f9b0-437">CallerEchoPercentMicIn</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-438">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-438">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-439">Porcentagem de tempo em que o eco é detectado no fluxo de captura de microfone do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-439">Percentage of time when echo is detected in the caller’s microphone capture stream.</span></span> <span data-ttu-id="9f9b0-440">Se o fone de ouvido estiver sendo usado, o valor deve ser baixo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-440">If headset is used, the value should be low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-441">CallerEchoPercentSend</span><span class="sxs-lookup"><span data-stu-id="9f9b0-441">CallerEchoPercentSend</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-442">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-442">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-443">Porcentagem de tempo em que o eco é detectado no fluxo de envio do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-443">Percentage of time when echo is detected in the caller’s sent stream.</span></span> <span data-ttu-id="9f9b0-444">Alta porcentagem de eco em enviar transmite uma indicação de vazamento de eco.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-444">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-445">CallerRxAGCSignalLevel</span><span class="sxs-lookup"><span data-stu-id="9f9b0-445">CallerRxAGCSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-446">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-446">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-447">Nível de sinal recebido no servidor de mediação do gateway para o áudio do chamador; Isso se aplica apenas ao servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-447">Received signal level on the Mediation Server from the Gateway for the caller’s audio; this applies only to the Mediation Server.</span></span> <span data-ttu-id="9f9b0-448">A unidade desta métrica é dBoV.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-448">The unit of this metric is dBoV.</span></span> <span data-ttu-id="9f9b0-449">Para ter uma boa qualidade, o intervalo aceitável deve ser de-30 a-18 dBoV.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-449">For good quality, the acceptable range should be -30 to -18 dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-450">CallerRxAGCNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="9f9b0-450">CallerRxAGCNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-451">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-451">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-452">Nível de sinal recebido no servidor de mediação do gateway para o áudio do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-452">Received signal level on the Mediation Server from the Gateway for the caller’s audio.</span></span> <span data-ttu-id="9f9b0-453">Isso se aplica apenas ao servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-453">This applies only to the Mediation Server.</span></span> <span data-ttu-id="9f9b0-454">A unidade desta métrica é dBoV.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-454">The unit of this metric is dBoV.</span></span> <span data-ttu-id="9f9b0-455">Para ter uma boa qualidade, o intervalo aceitável deve ser menor do que-50 dBoV.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-455">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-456">CallerRxAGCGain</span><span class="sxs-lookup"><span data-stu-id="9f9b0-456">CallerRxAGCGain</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-457">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-457">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-458">Controle de ganho automático (AGC) no lado do servidor de mediação aplicado ao áudio do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-458">Automatic gain control (AGC) on the Mediation Server side applied to the caller’s audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-459">CallerInitialSignalLevelRMS</span><span class="sxs-lookup"><span data-stu-id="9f9b0-459">CallerInitialSignalLevelRMS</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-460">float</span><span class="sxs-lookup"><span data-stu-id="9f9b0-460">float</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-461">A base média (RMS) do sinal de entrada para o chamador para até os primeiros 30 segundos da chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-461">Root mean square (RMS) of the incoming signal to the caller for up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-462">CalleeSendSignalLevel</span><span class="sxs-lookup"><span data-stu-id="9f9b0-462">CalleeSendSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-463">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-463">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-464">Representa o nível de sinal de áudio de controle de ganho de cruz analógico para o áudio enviado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-464">Represents the Post-Analog Gain Control audio signal level for the audio the callee sent.</span></span> <span data-ttu-id="9f9b0-465">A unidade para essa métrica é dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-465">The unit for this metric is dBmo.</span></span> <span data-ttu-id="9f9b0-466">Para ter uma qualidade aceitável, ele deve ter pelo menos 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-466">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="9f9b0-467">Essa métrica não é reportada pelo servidor de conferência A/V ou por telefones IP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-467">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-468">CalleeRecvSignalLevel</span><span class="sxs-lookup"><span data-stu-id="9f9b0-468">CalleeRecvSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-469">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-469">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-470">Nível de sinal de áudio para o áudio que o chama recebido.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-470">Audio signal level for the audio the callee received.</span></span> <span data-ttu-id="9f9b0-471">A unidade para essa métrica é dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-471">The unit for this metric is dBmo.</span></span> <span data-ttu-id="9f9b0-472">Para ter uma qualidade aceitável, ele deve ter pelo menos 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-472">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="9f9b0-473">Essa métrica não é reportada pelo servidor de conferência A/V ou por telefones IP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-473">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-474">CalleeSendNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="9f9b0-474">CalleeSendNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-475">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-475">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-476">Nível de ruído de áudio de controle de ganho analógico-analógico para o áudio enviado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-476">Post-Analog Gain Control audio noise level for the audio the callee sent.</span></span> <span data-ttu-id="9f9b0-477">A unidade para essa métrica é dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-477">The unit for this metric is dBmo.</span></span> <span data-ttu-id="9f9b0-478">Para ter uma qualidade aceitável, deve ser menor do que 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-478">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="9f9b0-479">Essa métrica não é reportada pelo servidor de conferência A/V ou por telefones IP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-479">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-480">CalleeRecvNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="9f9b0-480">CalleeRecvNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-481">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-481">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-482">Nível de ruído de áudio de controle de ganho analógico-analógico para o áudio que o chamador recebeu.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-482">Post-Analog Gain Control audio noise level for the audio the callee received.</span></span> <span data-ttu-id="9f9b0-483">A unidade para essa métrica é dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-483">The unit for this metric is dBmo.</span></span> <span data-ttu-id="9f9b0-484">Para ter uma qualidade aceitável, deve ser menor do que 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-484">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="9f9b0-485">Essa métrica não é reportada pelo servidor de conferência A/V ou por telefones IP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-485">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-486">CalleeEchoReturn</span><span class="sxs-lookup"><span data-stu-id="9f9b0-486">CalleeEchoReturn</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-487">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-487">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-488">Aprimoramento da perda de retorno de eco para o chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-488">Echo Return Loss Enhancement for the callee.</span></span> <span data-ttu-id="9f9b0-489">A unidade para essa métrica é dB.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-489">The unit for this metric is dB.</span></span> <span data-ttu-id="9f9b0-490">Valores inferiores representam menos eco.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-490">Lower values represent less echo.</span></span> <span data-ttu-id="9f9b0-491">Essa métrica não é reportada pelo servidor de conferência A/V ou por telefones IP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-491">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-492">CalleeSpeakerGlitchRate</span><span class="sxs-lookup"><span data-stu-id="9f9b0-492">CalleeSpeakerGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-493">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-493">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-494">Média de falhas por cinco minutos para a renderização do alto-falante do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-494">Average glitches per five minutes for the callee’s loudspeaker rendering.</span></span> <span data-ttu-id="9f9b0-495">Para ter uma boa qualidade, isso deve ser inferior a um por cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-495">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="9f9b0-496">Não relatado por servidores de conferência A/V, servidores de mediação ou telefones IP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-496">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-497">CalleeMicGlitchRate</span><span class="sxs-lookup"><span data-stu-id="9f9b0-497">CalleeMicGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-498">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-498">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-499">Média de falhas por cinco minutos para a captura de microfone do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-499">Average glitches per five minutes for the callee’s microphone capture.</span></span> <span data-ttu-id="9f9b0-500">Para ter uma boa qualidade, isso deve ser inferior a um por cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-500">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="9f9b0-501">Não relatado por servidores de conferência A/V, servidores de mediação ou telefones IP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-501">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-502">CalleeTimestampDriftRateMic</span><span class="sxs-lookup"><span data-stu-id="9f9b0-502">CalleeTimestampDriftRateMic</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-503">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-503">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-504">Taxa de descompasso do relógio do dispositivo de microfone do chamador, em relação ao relógio da CPU.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-504">Callee’s microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-505">CalleeTimestampDriftRateSpk</span><span class="sxs-lookup"><span data-stu-id="9f9b0-505">CalleeTimestampDriftRateSpk</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-506">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-506">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-507">Taxa de descompasso do relógio do dispositivo de alto-falante do chamador, em relação ao relógio da CPU.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-507">Callee’s speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-508">CalleeTimestampErrorMicMs</span><span class="sxs-lookup"><span data-stu-id="9f9b0-508">CalleeTimestampErrorMicMs</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-509">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-509">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-510">Erro de carimbo de data/hora médio do fluxo de captura de microfone, em milissegundos, nos últimos 20 segundos da chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-510">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-511">CalleeTimestampErrorSpkMs</span><span class="sxs-lookup"><span data-stu-id="9f9b0-511">CalleeTimestampErrorSpkMs</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-512">decimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-512">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-513">Média do erro de carimbo de data/hora do fluxo de processamento do palestrante em milissegundos, nos últimos 20 segundos da chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-513">Average of the callee’s speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-514">CalleeVsEntryCauses</span><span class="sxs-lookup"><span data-stu-id="9f9b0-514">CalleeVsEntryCauses</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-515">smallint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-515">smallint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-516">A opção de voz é um modo Half-duplex com capacidade de interrupção reduzida.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-516">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="9f9b0-517">Consulte a <a href="lync-server-2013-medialine-table.md">tabela de mídia no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-517">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-518">CalleeEchoEventCauses</span><span class="sxs-lookup"><span data-stu-id="9f9b0-518">CalleeEchoEventCauses</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-519">tinyint</span><span class="sxs-lookup"><span data-stu-id="9f9b0-519">tinyint</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-520">Causas de um evento de eco para o chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-520">Causes of an echo event for the callee.</span></span> <span data-ttu-id="9f9b0-521">Consulte a <a href="lync-server-2013-medialine-table.md">tabela de mídia no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-521">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-522">CalleeEchoPercentMicIn</span><span class="sxs-lookup"><span data-stu-id="9f9b0-522">CalleeEchoPercentMicIn</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-523">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-523">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-524">Porcentagem de tempo em que o eco é detectado no fluxo de captura do microfone do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-524">Percentage of time when echo is detected in the callee’s microphone capture stream.</span></span> <span data-ttu-id="9f9b0-525">Se o fone de ouvido estiver sendo usado, o valor deve ser baixo.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-525">If headset is used, the value should be low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-526">CalleeEchoPercentSend</span><span class="sxs-lookup"><span data-stu-id="9f9b0-526">CalleeEchoPercentSend</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-527">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-527">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-528">Porcentagem de tempo em que o eco é detectado no fluxo enviado do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-528">Percentage of time when echo is detected in the callee’s sent stream.</span></span> <span data-ttu-id="9f9b0-529">Alta porcentagem de eco em enviar transmite uma indicação de vazamento de eco.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-529">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-530">CalleeRxAGCSignalLevel</span><span class="sxs-lookup"><span data-stu-id="9f9b0-530">CalleeRxAGCSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-531">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-531">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-532">Nível de sinal recebido no servidor de mediação do gateway para o áudio do chamador; Isso se aplica apenas ao servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-532">Received signal level on the Mediation Server from the Gateway for the callee’s audio; this applies only to the Mediation Server.</span></span> <span data-ttu-id="9f9b0-533">A unidade desta métrica é dBoV.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-533">The unit of this metric is dBoV.</span></span> <span data-ttu-id="9f9b0-534">Para ter uma boa qualidade, o intervalo aceitável deve ser [-30 a-18] dBoV.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-534">For good quality, the acceptable range should be [-30 to -18] dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-535">CalleeRxAGCNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="9f9b0-535">CalleeRxAGCNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-536">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-536">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-537">Nível de sinal recebido no servidor de mediação do gateway para o áudio do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-537">Received signal level on the Mediation Server from the Gateway for the callee’s audio.</span></span> <span data-ttu-id="9f9b0-538">Isso se aplica apenas ao servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-538">This applies only to the Mediation Server.</span></span> <span data-ttu-id="9f9b0-539">A unidade desta métrica é dBoV.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-539">The unit of this metric is dBoV.</span></span> <span data-ttu-id="9f9b0-540">Para ter uma boa qualidade, o intervalo aceitável deve ser menor do que-50 dBoV.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-540">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-541">CalleeRxAGCGain</span><span class="sxs-lookup"><span data-stu-id="9f9b0-541">CalleeRxAGCGain</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-542">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-542">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-543">Controle de ganho automático (AGC) no lado do servidor de mediação aplicado ao áudio do chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-543">Automatic gain control (AGC) on the Mediation Server side applied to the callee’s audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-544">CalleeInitialSignalLevelRMS</span><span class="sxs-lookup"><span data-stu-id="9f9b0-544">CalleeInitialSignalLevelRMS</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-545">float</span><span class="sxs-lookup"><span data-stu-id="9f9b0-545">float</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-546">A base média (RMS) do sinal de entrada para o receptor para até os primeiros 30 segundos da chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-546">Root mean square (RMS) of the incoming signal to the callee for up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-547">RatioConcealedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="9f9b0-547">RatioConcealedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-548">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-548">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-549">Índice médio de amostras ocultas geradas pelo reparo de áudio para amostras típicas.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-549">Average ratio of concealed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-550">RatioStretchedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="9f9b0-550">RatioStretchedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-551">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-551">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-552">Índice médio de amostras ampliadas geradas pelo reparo de áudio para amostras típicas.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-552">Average ratio of stretched samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-553">RatioCompressedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="9f9b0-553">RatioCompressedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-554">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-554">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-555">Índice médio de amostras compactadas geradas pelo reparo de áudio para amostras típicas.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-555">Average ratio of compressed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-556">RoundTrip</span><span class="sxs-lookup"><span data-stu-id="9f9b0-556">RoundTrip</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-557">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-557">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-558">Tempo de ida e volta das estatísticas do RTCP.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-558">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-559">RoundTripMax</span><span class="sxs-lookup"><span data-stu-id="9f9b0-559">RoundTripMax</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-560">int</span><span class="sxs-lookup"><span data-stu-id="9f9b0-560">int</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-561">Tempo máximo de ida e volta do fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-561">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-562">OverallAvgNetworkMOS</span><span class="sxs-lookup"><span data-stu-id="9f9b0-562">OverallAvgNetworkMOS</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-563">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-563">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-564">Banda larga médio de um MOS de rede para a chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-564">Average wideband Network MOS for the call.</span></span> <span data-ttu-id="9f9b0-565">Essa métrica depende da perda de pacotes, da tremulação e do codec usados.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-565">This metric depends on the packet loss, jitter, and codec used.</span></span> <span data-ttu-id="9f9b0-566">O intervalo é de 1,0 a 5,0.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-566">Range is 1.0 to 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-567">OverallMinNetworkMOS</span><span class="sxs-lookup"><span data-stu-id="9f9b0-567">OverallMinNetworkMOS</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-568">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-568">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-569">Banda larga de rede mínima para a chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-569">Minimum wideband Network MOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-570">SendListenMOS</span><span class="sxs-lookup"><span data-stu-id="9f9b0-570">SendListenMOS</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-571">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-571">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-572">Pontuação estimada banda larga de escuta da MOS para áudio enviado, incluindo o nível de fala, o nível de ruído e as características do dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-572">Average predicted wideband Listening MOS score for audio sent, including speech level, noise level and capture device characteristics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-573">SendListenMOSMin</span><span class="sxs-lookup"><span data-stu-id="9f9b0-573">SendListenMOSMin</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-574">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-574">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-575">SendListenMOS mínima para a chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-575">Minimum SendListenMOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-576">RecvListenMOS</span><span class="sxs-lookup"><span data-stu-id="9f9b0-576">RecvListenMOS</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-577">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-577">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-578">Média prevista banda larga ouvindo a Pontuação do MOS para áudio recebido da rede, incluindo o nível de fala, o nível de ruído, o codec, as condições da rede e as características do dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-578">Average predicted wideband Listening MOS score for audio received from the network including speech level, noise level, codec, network conditions and capture device characteristics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-579">RecvListenMOSMin</span><span class="sxs-lookup"><span data-stu-id="9f9b0-579">RecvListenMOSMin</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-580">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="9f9b0-580">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-581">RecvListenMOS mínima para a chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-581">Minimum RecvListenMOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f9b0-582">AudioFECUsed</span><span class="sxs-lookup"><span data-stu-id="9f9b0-582">AudioFECUsed</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-583">bit</span><span class="sxs-lookup"><span data-stu-id="9f9b0-583">bit</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-584">Indica se o FEC de áudio foi usado para a chamada.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-584">Indicates whether audio FEC was used for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f9b0-585">SenderIsCallerPAI</span><span class="sxs-lookup"><span data-stu-id="9f9b0-585">SenderIsCallerPAI</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-586">bit</span><span class="sxs-lookup"><span data-stu-id="9f9b0-586">bit</span></span></p></td>
<td><p><span data-ttu-id="9f9b0-587">Indica a direção das informações de identificação p-declaradas; 1 significa que a direção do fluxo é do chamador para o receptor; 0 significa que a direção do fluxo é do receptor para o chamador.</span><span class="sxs-lookup"><span data-stu-id="9f9b0-587">Indicates direction of the p-asserted identify information; 1 means the stream direction is from the caller to the callee; 0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9f9b0-588">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9f9b0-588">


</div>

<span> </span>

</div>

</div>

</span></span></div>

