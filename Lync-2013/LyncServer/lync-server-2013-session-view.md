---
title: 'Lync Server 2013: modo de exibição de sessão'
description: 'Lync Server 2013: modo de exibição de sessão.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Session view
ms:assetid: 49e33f5b-45d0-4146-a5a4-76954d895a98
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688048(v=OCS.15)
ms:contentKeyID: 49733641
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ff4bc4abbd55e073006693d28f092f077698ef75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444788"
---
# <a name="session-view-in-lync-server-2013"></a><span data-ttu-id="82ec7-103">Modo de exibição de sessão no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="82ec7-103">Session view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="82ec7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="82ec7-104">

<span> </span></span></span>

<span data-ttu-id="82ec7-105">_**Tópico da última modificação:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="82ec7-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="82ec7-106">A exibição de sessão armazena informações sobre as sessões que têm registros no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="82ec7-106">The Session View stores information about sessions that have records in the database.</span></span> <span data-ttu-id="82ec7-107">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="82ec7-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="82ec7-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="82ec7-108">Column</span></span></th>
<th><span data-ttu-id="82ec7-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="82ec7-109">Data Type</span></span></th>
<th><span data-ttu-id="82ec7-110">Detalhes</span><span class="sxs-lookup"><span data-stu-id="82ec7-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82ec7-111">ConferenceDateTime</span><span class="sxs-lookup"><span data-stu-id="82ec7-111">ConferenceDateTime</span></span></p></td>
<td><p><span data-ttu-id="82ec7-112">datetime</span><span class="sxs-lookup"><span data-stu-id="82ec7-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="82ec7-113">Referenciado da tabela de mídia.</span><span class="sxs-lookup"><span data-stu-id="82ec7-113">Referenced from the MediaLine Table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82ec7-114">ConferenceURI</span><span class="sxs-lookup"><span data-stu-id="82ec7-114">ConferenceURI</span></span></p></td>
<td><p><span data-ttu-id="82ec7-115">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="82ec7-115">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="82ec7-116">URL da conferência se for uma conferência ou caixa de diálogo se for uma sessão ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="82ec7-116">Conference URI if this is a conference, or DialogID if this is a peer-to-peer session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82ec7-117">Relation</span><span class="sxs-lookup"><span data-stu-id="82ec7-117">Correlation</span></span></p></td>
<td><p><span data-ttu-id="82ec7-118">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="82ec7-118">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="82ec7-119">ID de correlação da sessão.</span><span class="sxs-lookup"><span data-stu-id="82ec7-119">Correlation ID of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82ec7-120">DialogCategory</span><span class="sxs-lookup"><span data-stu-id="82ec7-120">DialogCategory</span></span></p></td>
<td><p><span data-ttu-id="82ec7-121">bit</span><span class="sxs-lookup"><span data-stu-id="82ec7-121">bit</span></span></p></td>
<td><p><span data-ttu-id="82ec7-122">Categoria da caixa de diálogo; 0 é o servidor do Lync para o segmento do servidor de mediação; 1 é o servidor de mediação para a perna do gateway PSTN.</span><span class="sxs-lookup"><span data-stu-id="82ec7-122">Dialog category; 0 is Lync Server to Mediation Server leg; 1 is Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82ec7-123">MediationServerBypassFlag</span><span class="sxs-lookup"><span data-stu-id="82ec7-123">MediationServerBypassFlag</span></span></p></td>
<td><p><span data-ttu-id="82ec7-124">bit</span><span class="sxs-lookup"><span data-stu-id="82ec7-124">bit</span></span></p></td>
<td><p><span data-ttu-id="82ec7-125">Indica se a chamada foi ignorada ou não.</span><span class="sxs-lookup"><span data-stu-id="82ec7-125">Indicates whether or not the call was bypassed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82ec7-126">MediaBypassWarningFlag</span><span class="sxs-lookup"><span data-stu-id="82ec7-126">MediaBypassWarningFlag</span></span></p></td>
<td><p><span data-ttu-id="82ec7-127">int</span><span class="sxs-lookup"><span data-stu-id="82ec7-127">int</span></span></p></td>
<td><p><span data-ttu-id="82ec7-128">Esse campo, se presente, indicará por que uma chamada não foi ignorada mesmo se as IDs de bypass forem atendidas.</span><span class="sxs-lookup"><span data-stu-id="82ec7-128">This field, if present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="82ec7-129">Para o Lync Server, somente um valor é definido:</span><span class="sxs-lookup"><span data-stu-id="82ec7-129">For Lync Server, only one value is defined:</span></span></p>
<p><span data-ttu-id="82ec7-130">0x0001 – ID de bypass desconhecido para o adaptador de rede padrão</span><span class="sxs-lookup"><span data-stu-id="82ec7-130">0x0001 – Unknown bypass ID for Default network adapter</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82ec7-131">StartTime </span><span class="sxs-lookup"><span data-stu-id="82ec7-131">StartTime</span></span></p></td>
<td><p><span data-ttu-id="82ec7-132">datetime</span><span class="sxs-lookup"><span data-stu-id="82ec7-132">datetime</span></span></p></td>
<td><p><span data-ttu-id="82ec7-133">Hora de início da chamada.</span><span class="sxs-lookup"><span data-stu-id="82ec7-133">Call start time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82ec7-134">EndTime</span><span class="sxs-lookup"><span data-stu-id="82ec7-134">EndTime</span></span></p></td>
<td><p><span data-ttu-id="82ec7-135">datetime</span><span class="sxs-lookup"><span data-stu-id="82ec7-135">datetime</span></span></p></td>
<td><p><span data-ttu-id="82ec7-136">Hora de término da chamada.</span><span class="sxs-lookup"><span data-stu-id="82ec7-136">Call end time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82ec7-137">CallerPool</span><span class="sxs-lookup"><span data-stu-id="82ec7-137">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="82ec7-138">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="82ec7-138">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="82ec7-139">FQDN do pool de chamadas.</span><span class="sxs-lookup"><span data-stu-id="82ec7-139">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82ec7-140">CalleePool</span><span class="sxs-lookup"><span data-stu-id="82ec7-140">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="82ec7-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="82ec7-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="82ec7-142">FQDN do pool do chamador.</span><span class="sxs-lookup"><span data-stu-id="82ec7-142">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82ec7-143">CallerPAI</span><span class="sxs-lookup"><span data-stu-id="82ec7-143">CallerPAI</span></span></p></td>
<td><p><span data-ttu-id="82ec7-144">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="82ec7-144">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="82ec7-145">URI de identidade declarado p do chamador.</span><span class="sxs-lookup"><span data-stu-id="82ec7-145">Caller’s p-asserted identity URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82ec7-146">CalleePAI</span><span class="sxs-lookup"><span data-stu-id="82ec7-146">CalleePAI</span></span></p></td>
<td><p><span data-ttu-id="82ec7-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="82ec7-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="82ec7-148">URI de identidade declarada do p do chamador.</span><span class="sxs-lookup"><span data-stu-id="82ec7-148">Callee’s p-asserted identity URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82ec7-149">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="82ec7-149">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="82ec7-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="82ec7-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="82ec7-151">Nome do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="82ec7-151">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82ec7-152">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="82ec7-152">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="82ec7-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="82ec7-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="82ec7-154">Nome do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="82ec7-154">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82ec7-155">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="82ec7-155">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="82ec7-156">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="82ec7-156">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="82ec7-157">Cadeia de caracteres do agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="82ec7-157">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82ec7-158">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="82ec7-158">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="82ec7-159">smallint</span><span class="sxs-lookup"><span data-stu-id="82ec7-159">smallint</span></span></p></td>
<td><p><span data-ttu-id="82ec7-160">Tipo de agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="82ec7-160">Type of caller’s user agent.</span></span> <span data-ttu-id="82ec7-161">Consulte a <a href="lync-server-2013-useragent-table.md">tabela UserAgent no Lync Server 2013</a> para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="82ec7-161">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82ec7-162">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="82ec7-162">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="82ec7-163">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="82ec7-163">nvarchar (64)</span></span></p></td>
<td><p><span data-ttu-id="82ec7-164">Categoria do agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="82ec7-164">Category of caller’s user agent.</span></span> <span data-ttu-id="82ec7-165">Consulte a <a href="lync-server-2013-useragentdef-table-qoe.md">tabela UserAgentDef (QoE) no Lync Server 2013</a> para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="82ec7-165">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82ec7-166">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="82ec7-166">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="82ec7-167">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="82ec7-167">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="82ec7-168">Cadeia de caracteres do agente do usuário do chamador.</span><span class="sxs-lookup"><span data-stu-id="82ec7-168">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82ec7-169">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="82ec7-169">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="82ec7-170">smallint</span><span class="sxs-lookup"><span data-stu-id="82ec7-170">smallint</span></span></p></td>
<td><p><span data-ttu-id="82ec7-171">Tipo de agente do usuário para o chamador.</span><span class="sxs-lookup"><span data-stu-id="82ec7-171">Type of user agent for the callee.</span></span> <span data-ttu-id="82ec7-172">Consulte a <a href="lync-server-2013-useragent-table.md">tabela UserAgent no Lync Server 2013</a> para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="82ec7-172">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82ec7-173">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="82ec7-173">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="82ec7-174">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="82ec7-174">nvarchar (64)</span></span></p></td>
<td><p><span data-ttu-id="82ec7-175">Categoria do agente do usuário para o chamador.</span><span class="sxs-lookup"><span data-stu-id="82ec7-175">User agent category for the callee.</span></span> <span data-ttu-id="82ec7-176">Consulte a <a href="lync-server-2013-useragentdef-table-qoe.md">tabela UserAgentDef (QoE) no Lync Server 2013</a> para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="82ec7-176">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82ec7-177">CallerURI</span><span class="sxs-lookup"><span data-stu-id="82ec7-177">CallerURI</span></span></p></td>
<td><p><span data-ttu-id="82ec7-178">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="82ec7-178">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="82ec7-179">URI do chamador.</span><span class="sxs-lookup"><span data-stu-id="82ec7-179">Caller’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82ec7-180">CalleeURI</span><span class="sxs-lookup"><span data-stu-id="82ec7-180">CalleeURI</span></span></p></td>
<td><p><span data-ttu-id="82ec7-181">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="82ec7-181">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="82ec7-182">URI do chamador.</span><span class="sxs-lookup"><span data-stu-id="82ec7-182">Callee’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82ec7-183">CallPrioirty</span><span class="sxs-lookup"><span data-stu-id="82ec7-183">CallPrioirty</span></span></p></td>
<td><p><span data-ttu-id="82ec7-184">int</span><span class="sxs-lookup"><span data-stu-id="82ec7-184">int</span></span></p></td>
<td><p><span data-ttu-id="82ec7-185">Prioridade da chamada.</span><span class="sxs-lookup"><span data-stu-id="82ec7-185">Priority of the call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="82ec7-186">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="82ec7-186">


</div>

<span> </span>

</div>

</div>

</span></span></div>

