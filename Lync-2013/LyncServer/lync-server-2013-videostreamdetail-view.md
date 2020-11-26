---
title: 'Lync Server 2013: modo de exibição VideoStreamDetail'
description: 'Lync Server 2013: modo de exibição VideoStreamDetail.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStreamDetail view
ms:assetid: ec8c45e1-307d-40ec-a75e-6083306105f2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721928(v=OCS.15)
ms:contentKeyID: 49733863
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3f420c292627d15fd0d54f2eba01c565a49a72d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443423"
---
# <a name="videostreamdetail-view-in-lync-server-2013"></a><span data-ttu-id="1bfdf-103">Exibição VideoStreamDetail no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1bfdf-103">VideoStreamDetail view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1bfdf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1bfdf-104">

<span> </span></span></span>

<span data-ttu-id="1bfdf-105">_**Tópico da última modificação:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="1bfdf-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="1bfdf-106">A exibição VideoStreamDetail armazena informações sobre cada fluxo de vídeo no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-106">The VideoStreamDetail View stores information about each video stream in the database.</span></span> <span data-ttu-id="1bfdf-107">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1bfdf-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="1bfdf-108">Column</span></span></th>
<th><span data-ttu-id="1bfdf-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1bfdf-109">Data Type</span></span></th>
<th><span data-ttu-id="1bfdf-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1bfdf-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-111">Sessiontime</span><span class="sxs-lookup"><span data-stu-id="1bfdf-111">SessionTime</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-112">datetime</span><span class="sxs-lookup"><span data-stu-id="1bfdf-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-113">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-113">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-114">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="1bfdf-114">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-115">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-115">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-116">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-116">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-117">MediaLineLabel</span><span class="sxs-lookup"><span data-stu-id="1bfdf-117">MediaLineLabel</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-118">tinyint</span><span class="sxs-lookup"><span data-stu-id="1bfdf-118">tinyint</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-119">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-120">Streamid</span><span class="sxs-lookup"><span data-stu-id="1bfdf-120">StreamId</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-121">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-121">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-122">ID exclusiva dentro de uma linha de mídia.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-122">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-123">StartTime </span><span class="sxs-lookup"><span data-stu-id="1bfdf-123">StartTime</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-124">datetime</span><span class="sxs-lookup"><span data-stu-id="1bfdf-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-125">Hora de início da sessão.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-125">Start time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-126">EndTime</span><span class="sxs-lookup"><span data-stu-id="1bfdf-126">EndTime</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-127">datetime</span><span class="sxs-lookup"><span data-stu-id="1bfdf-127">datetime</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-128">Hora de término da sessão.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-128">End time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-129">CallPriority</span><span class="sxs-lookup"><span data-stu-id="1bfdf-129">CallPriority</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-130">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-130">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-131">Prioridade da chamada.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-131">Priority of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-132">CallerPool</span><span class="sxs-lookup"><span data-stu-id="1bfdf-132">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-133">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-133">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-134">FQDN do pool de chamadas.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-134">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-135">CalleePool</span><span class="sxs-lookup"><span data-stu-id="1bfdf-135">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-136">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-136">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-137">FQDN do pool do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-137">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-138">Chamador</span><span class="sxs-lookup"><span data-stu-id="1bfdf-138">Caller</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-140">URI do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-140">Caller’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-141">Receptor</span><span class="sxs-lookup"><span data-stu-id="1bfdf-141">Callee</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-142">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-142">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-143">URI do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-143">Callee’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-144">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="1bfdf-144">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-145">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-145">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-146">Cadeia de caracteres do agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-146">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-147">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="1bfdf-147">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-148">smallint</span><span class="sxs-lookup"><span data-stu-id="1bfdf-148">smallint</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-149">Tipo de agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-149">Type of caller’s user agent.</span></span> <span data-ttu-id="1bfdf-150">Consulte a <a href="lync-server-2013-useragent-table.md">tabela UserAgent no Lync Server 2013</a> para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-150">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-151">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="1bfdf-151">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-152">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-152">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-153">Categoria do agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-153">Category of caller’s user agent.</span></span> <span data-ttu-id="1bfdf-154">Consulte a <a href="lync-server-2013-useragentdef-table-qoe.md">tabela UserAgentDef (QoE) no Lync Server 2013</a> para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-154">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-155">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="1bfdf-155">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-156">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-156">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-157">Cadeia de caracteres do agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-157">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-158">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="1bfdf-158">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-159">smallint</span><span class="sxs-lookup"><span data-stu-id="1bfdf-159">smallint</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-160">Tipo de agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-160">Type of callee’s user agent.</span></span> <span data-ttu-id="1bfdf-161">Consulte a <a href="lync-server-2013-useragent-table.md">tabela UserAgent no Lync Server 2013</a> para obter informações.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-161">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-162">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="1bfdf-162">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-163">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-163">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-164">Categoria do agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-164">Category of callee’s user agent.</span></span> <span data-ttu-id="1bfdf-165">Consulte a <a href="lync-server-2013-useragentdef-table-qoe.md">tabela UserAgentDef (QoE) no Lync Server 2013</a> para obter informações.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-165">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-166">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1bfdf-166">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-167">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-167">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-168">Nome do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-168">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-169">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="1bfdf-169">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-170">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-170">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-171">Nome do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-171">Callee’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-172">CallerOS</span><span class="sxs-lookup"><span data-stu-id="1bfdf-172">CallerOS</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-173">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="1bfdf-173">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-174">Sistema operacional (SO) do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-174">Operating system (OS) of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-175">CalleeOS</span><span class="sxs-lookup"><span data-stu-id="1bfdf-175">CalleeOS</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-176">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="1bfdf-176">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-177">Sistema operacional (SO) do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-177">Operating system (OS) of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-178">CallerCPUName</span><span class="sxs-lookup"><span data-stu-id="1bfdf-178">CallerCPUName</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-179">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="1bfdf-179">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-180">Nome da CPU do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-180">CPU name of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-181">CalleeCPUName</span><span class="sxs-lookup"><span data-stu-id="1bfdf-181">CalleeCPUName</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-182">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="1bfdf-182">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-183">Nome da CPU do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-183">CPU name of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-184">CallerCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="1bfdf-184">CallerCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-185">smallint</span><span class="sxs-lookup"><span data-stu-id="1bfdf-185">smallint</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-186">Número de núcleos da CPU do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-186">Number of CPU cores of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-187">CalleeCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="1bfdf-187">CalleeCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-188">smallint</span><span class="sxs-lookup"><span data-stu-id="1bfdf-188">smallint</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-189">Número de núcleos da CPU do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-189">Number of CPU cores of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-190">CallerCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="1bfdf-190">CallerCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-191">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-191">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-192">Velocidade do processador da CPU do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-192">CPU processor speed of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-193">CalleeCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="1bfdf-193">CalleeCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-194">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-194">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-195">Velocidade do processador da CPU do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-195">CPU processor speed of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-196">CallerVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="1bfdf-196">CallerVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-197">tinyint</span><span class="sxs-lookup"><span data-stu-id="1bfdf-197">tinyint</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-198">Indica se o sistema do chamador está em execução em um ambiente virtualizado.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-198">Indicates whether the caller’s system is running in a virtualized environment.</span></span> <span data-ttu-id="1bfdf-199">Consulte a <a href="lync-server-2013-endpoint-table.md">tabela de pontos de extremidade no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-199">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-200">CalleeVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="1bfdf-200">CalleeVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-201">tinyint</span><span class="sxs-lookup"><span data-stu-id="1bfdf-201">tinyint</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-202">Indica se o sistema do chamador está em execução em um ambiente virtualizado.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-202">Indicates whether the callee’s system is running in a virtualized environment.</span></span> <span data-ttu-id="1bfdf-203">Consulte a <a href="lync-server-2013-endpoint-table.md">tabela de pontos de extremidade no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-203">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-204">ConnectivityIce</span><span class="sxs-lookup"><span data-stu-id="1bfdf-204">ConnectivityIce</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-205">tinyint</span><span class="sxs-lookup"><span data-stu-id="1bfdf-205">tinyint</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-206">Informações sobre o caminho de mídia, como direta ou retransmitida.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-206">Information about media path, such as direct or relayed.</span></span> <span data-ttu-id="1bfdf-207">Consulte a <a href="lync-server-2013-medialine-table.md">tabela de mídia no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-207">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-208">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="1bfdf-208">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-209">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-209">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-210">Informações sobre o processo de estabelecimento de conectividade interativa (ICE) descrito em sinalizadores de bits para o chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-210">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="1bfdf-211">Para obter detalhes, consulte a especificação de protocolo de servidor de monitoração de experiência de qualidade.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-211">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-212">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="1bfdf-212">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-213">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-213">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-214">Informações sobre o processo de estabelecimento de conectividade interativa (ICE) descrito em sinalizadores de bits para o chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-214">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="1bfdf-215">Para obter detalhes, consulte a especificação de protocolo de servidor de monitoração de experiência de qualidade.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-215">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-216">SMTP</span><span class="sxs-lookup"><span data-stu-id="1bfdf-216">Transport</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-217">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-217">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-218">Tipo de transporte: 0 é UDP; 1 é o TCP.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-218">Transport type: 0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-219">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="1bfdf-219">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-220">var (50)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-220">var(50)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-221">Endereço IP do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-221">IP address of the caller.</span></span> <span data-ttu-id="1bfdf-222">Pode ser um endereço IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-222">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-223">CallerPort</span><span class="sxs-lookup"><span data-stu-id="1bfdf-223">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-224">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-224">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-225">Porta usada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-225">Port used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-226">CallerInside</span><span class="sxs-lookup"><span data-stu-id="1bfdf-226">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-227">bit</span><span class="sxs-lookup"><span data-stu-id="1bfdf-227">bit</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-228">Indica se o chamador está dentro da rede da organização.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-228">Indicates whether the caller is inside the organization network.</span></span> <span data-ttu-id="1bfdf-229">1 significa que a chamada está dentro da rede corporativa, 0 significa que o chamador está fora da rede.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-229">1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-230">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="1bfdf-230">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-231">var (50)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-231">var(50)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-232">Endereço IP do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-232">IP address of the callee.</span></span> <span data-ttu-id="1bfdf-233">Pode ser um endereço IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-233">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-234">CalleePort</span><span class="sxs-lookup"><span data-stu-id="1bfdf-234">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-235">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-235">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-236">Porta usada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-236">Port used by the callee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-237">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="1bfdf-237">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-238">bit</span><span class="sxs-lookup"><span data-stu-id="1bfdf-238">bit</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-239">Indica se o chamador está dentro da rede da organização. 1 significa que a chamada está dentro da rede corporativa, 0 significa que o chamador está fora da rede.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-239">Indicates whether the caller is inside the organization network.1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-240">CallerUserSite</span><span class="sxs-lookup"><span data-stu-id="1bfdf-240">CallerUserSite</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-241">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="1bfdf-241">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-242">Nome do site do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-242">Name of the caller’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-243">CallerRegion</span><span class="sxs-lookup"><span data-stu-id="1bfdf-243">CallerRegion</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-244">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="1bfdf-244">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-245">Nome do país/região do site do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-245">Name of the country/region of the caller’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-246">CalleeUserSite</span><span class="sxs-lookup"><span data-stu-id="1bfdf-246">CalleeUserSite</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-247">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="1bfdf-247">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-248">Nome do site do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-248">Name of the callee’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-249">CalleeRegion</span><span class="sxs-lookup"><span data-stu-id="1bfdf-249">CalleeRegion</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-250">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="1bfdf-250">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-251">Nome do país/região do site do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-251">Name of the country/region of the callee’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-252">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="1bfdf-252">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-253">var (50)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-253">var(50)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-254">Endereço IP do serviço de borda A/V usado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-254">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="1bfdf-255">Consulte a <a href="lync-server-2013-ipaddress-table.md">tabela IPAddress no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-255">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-256">CallerRelayPort</span><span class="sxs-lookup"><span data-stu-id="1bfdf-256">CallerRelayPort</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-257">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-257">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-258">Porta no serviço de borda A/V usado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-258">Port on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-259">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="1bfdf-259">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-260">var (50)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-260">var(50)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-261">Chave de endereço IP do serviço de borda A/V usado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-261">IP Address key of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="1bfdf-262">Consulte a <a href="lync-server-2013-ipaddress-table.md">tabela IPAddress no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-262">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-263">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="1bfdf-263">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-264">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-264">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-265">Porta no serviço de borda A/V usado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-265">Port on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-266">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="1bfdf-266">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-267">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-267">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-268">Nome do dispositivo de captura do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-268">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-269">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="1bfdf-269">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-270">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-270">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-271">Nome do dispositivo de renderização do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-271">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-272">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="1bfdf-272">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-273">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-273">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-274">Nome do driver do dispositivo de captura do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-274">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-275">CallerRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="1bfdf-275">CallerRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-276">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-276">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-277">O nome do driver de dispositivo de renderização do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-277">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-278">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="1bfdf-278">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-279">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-279">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-280">Nome do dispositivo de captura do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-280">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-281">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="1bfdf-281">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-282">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-282">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-283">Nome do dispositivo de renderização do Calle.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-283">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-284">CalleCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="1bfdf-284">CalleCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-285">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-285">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-286">Nome do driver do dispositivo de captura do chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-286">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-287">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="1bfdf-287">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-288">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-288">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-289">Chame o nome do driver do dispositivo de processamento do recurso.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-289">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-290">CallerNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="1bfdf-290">CallerNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-291">tinyint</span><span class="sxs-lookup"><span data-stu-id="1bfdf-291">tinyint</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-292">Tipo de conexão de rede do chamador: 0 é cabeado, 1 é sem fio.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-292">Caller’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-293">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="1bfdf-293">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-294">bit</span><span class="sxs-lookup"><span data-stu-id="1bfdf-294">bit</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-295">Indica se o chamador se conecta ou não a uma rede virtual privada.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-295">Indicates whether or not the caller connected over a virtual private network.</span></span> <span data-ttu-id="1bfdf-296">1 é uma rede virtual privada (VPN), 0 não é VPN.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-296">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-297">CallerLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="1bfdf-297">CallerLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-298">decimal (18)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-298">decimal(18,)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-299">Velocidade do link de rede para o ponto de extremidade do chamador em bps.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-299">Network link speed for the caller's endpoint in bps.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-300">CalleeNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="1bfdf-300">CalleeNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-301">tinyint</span><span class="sxs-lookup"><span data-stu-id="1bfdf-301">tinyint</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-302">Tipo de conexão de rede do chamador: 0 é cabeado, 1 é sem fio.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-302">Callee’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-303">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="1bfdf-303">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-304">bit</span><span class="sxs-lookup"><span data-stu-id="1bfdf-304">bit</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-305">Indica se o chamador se conecta em uma rede virtual privada.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-305">Indicates whether or not the callee connected over a virtual private network.</span></span> <span data-ttu-id="1bfdf-306">1 é uma rede virtual privada (VPN), 0 não é VPN.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-306">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-307">CalleeLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="1bfdf-307">CalleeLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-308">decimal (18, 0)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-308">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-309">Velocidade do link de rede para o ponto de extremidade do chamador (em bps).</span><span class="sxs-lookup"><span data-stu-id="1bfdf-309">Network link speed for the callee’s endpoint (in bps).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-310">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="1bfdf-310">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-311">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-311">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-312">O MOS de conversa de banda estreita das sessões de áudio (com base nos dois fluxos de áudio).</span><span class="sxs-lookup"><span data-stu-id="1bfdf-312">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-313">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="1bfdf-313">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-314">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-314">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-315">A largura de banda real aplicada ao fluxo de envio do lado fornecido tem várias configurações de política (ativar, API, SDP, servidor de política e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="1bfdf-315">Actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="1bfdf-316">Isso não deve ser confundido com a largura de banda efetiva porque pode haver uma largura de banda mais econômica com base na estimativa de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-316">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="1bfdf-317">Isso é basicamente a largura de banda máxima que o fluxo de envio pode ter limites de bloqueio impostos pela estimativa da largura de banda.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-317">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-318">JitterInterArrival</span><span class="sxs-lookup"><span data-stu-id="1bfdf-318">JitterInterArrival</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-319">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-319">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-320">Tremulação média de rede de estatísticas de protocolo de controle de tempo real (RTCP).</span><span class="sxs-lookup"><span data-stu-id="1bfdf-320">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-321">JitterInterArrivalMax</span><span class="sxs-lookup"><span data-stu-id="1bfdf-321">JitterInterArrivalMax</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-322">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-322">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-323">Maior tremulação de rede durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-323">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-324">RoundTrip</span><span class="sxs-lookup"><span data-stu-id="1bfdf-324">RoundTrip</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-325">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-325">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-326">Tempo de ida e volta das estatísticas do RTCP.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-326">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-327">RoundTripMax</span><span class="sxs-lookup"><span data-stu-id="1bfdf-327">RoundTripMax</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-328">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-328">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-329">Tempo máximo de ida e volta do fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-329">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-330">PacketLossRate</span><span class="sxs-lookup"><span data-stu-id="1bfdf-330">PacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-331">decimal (5, 4)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-331">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-332">Taxa média de perda de pacotes durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-332">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-333">PacketLossRateMax</span><span class="sxs-lookup"><span data-stu-id="1bfdf-333">PacketLossRateMax</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-334">decimal (5, 4)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-334">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-335">Perda máxima de pacote observado durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-335">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-336">PacketUtilization</span><span class="sxs-lookup"><span data-stu-id="1bfdf-336">PacketUtilization</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-337">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-337">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-338">Contagem de pacotes para o fluxo de vídeo (protocolo de transporte em tempo real, RTP).</span><span class="sxs-lookup"><span data-stu-id="1bfdf-338">Packet count for the video stream (Real Time Transport Protocol, RTP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-339">Largura de banda</span><span class="sxs-lookup"><span data-stu-id="1bfdf-339">BandwidthEst</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-340">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-340">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-341">Estimativas de largura de banda para o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-341">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-342">PayloadDescription</span><span class="sxs-lookup"><span data-stu-id="1bfdf-342">PayloadDescription</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-343">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-343">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-344">Codec de áudio usado para a chamada, referenciado pela <a href="lync-server-2013-payloaddescription-table.md">tabela PayloadDescription no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-344">Audio codec used for the call, referenced from the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-345">VideoResolution</span><span class="sxs-lookup"><span data-stu-id="1bfdf-345">VideoResolution</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-346">caractere (9)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-346">char(9)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-347">Resolução do vídeo em largura de pixels multiplicada pela altura de pixels.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-347">Resolution of the video in pixels width multiplied by pixels height.</span></span> <span data-ttu-id="1bfdf-348">Relatado como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-348">Reported as a string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-349">VideoBitRateAvg</span><span class="sxs-lookup"><span data-stu-id="1bfdf-349">VideoBitRateAvg</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-350">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-350">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-351">Taxa média de bits do fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-351">Average bit rate of the video stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-352">InboundVideoFrameRateAvg</span><span class="sxs-lookup"><span data-stu-id="1bfdf-352">InboundVideoFrameRateAvg</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-353">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-353">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-354">Taxa de quadro de vídeo recebida.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-354">Frame rate of video received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-355">OutboundVideoFrameRateAvg</span><span class="sxs-lookup"><span data-stu-id="1bfdf-355">OutboundVideoFrameRateAvg</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-356">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-356">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-357">Taxa de quadro de vídeo enviada.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-357">Frame rate of video sent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-358">ViideoBitRateMax</span><span class="sxs-lookup"><span data-stu-id="1bfdf-358">ViideoBitRateMax</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-359">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-359">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-360">Taxa máxima de bits de vídeo durante a sessão de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-360">Maximum video bit rate during the video session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-361">À</span><span class="sxs-lookup"><span data-stu-id="1bfdf-361">VideoPacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-362">decimal (9, 4)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-362">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-363">Taxa de perda de pacotes de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-363">Rate at which video packets were lost.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-364">VideoFrameLossRate</span><span class="sxs-lookup"><span data-stu-id="1bfdf-364">VideoFrameLossRate</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-365">decimal (9.4)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-365">decimal(9.4)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-366">Porcentagem total de quadros de vídeo perdidos.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-366">Percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-367">VideoFEC</span><span class="sxs-lookup"><span data-stu-id="1bfdf-367">VideoFEC</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-368">bit</span><span class="sxs-lookup"><span data-stu-id="1bfdf-368">bit</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-369">Não usado.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-369">Not used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-370">VideoAllocateBWAvg</span><span class="sxs-lookup"><span data-stu-id="1bfdf-370">VideoAllocateBWAvg</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-371">int</span><span class="sxs-lookup"><span data-stu-id="1bfdf-371">int</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-372">Quantidade média de largura de banda alocada para vídeo.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-372">Average amount of bandwidth allocated for video.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bfdf-373">À</span><span class="sxs-lookup"><span data-stu-id="1bfdf-373">VideoLocalFrameLossPercentageAvg</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-374">decimal (9.4)</span><span class="sxs-lookup"><span data-stu-id="1bfdf-374">decimal(9.4)</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-375">Porcentagem total de quadros de vídeo perdidos.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-375">Percentage of total video frames that were lost.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bfdf-376">SenderIsCallerPAI</span><span class="sxs-lookup"><span data-stu-id="1bfdf-376">SenderIsCallerPAI</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-377">bit</span><span class="sxs-lookup"><span data-stu-id="1bfdf-377">bit</span></span></p></td>
<td><p><span data-ttu-id="1bfdf-378">Direção de fluxo para informações de identidades p-declaradas.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-378">Stream direction for p-asserted identity information.</span></span> <span data-ttu-id="1bfdf-379">1 significa que a direção do fluxo é do chamador para o receptor; 0 significa que a direção do fluxo é do receptor para o chamador.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-379">1 means the stream direction is from the caller to the callee; 0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1bfdf-380">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1bfdf-380">


</div>

<span> </span>

</div>

</div>

</span></span></div>

