---
title: 'Lync Server 2013: Tabela SessionDetails'
description: 'Lync Server 2013: SessionDetails Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionDetails table
ms:assetid: 783d2508-e31f-4b54-be0c-63aa5ec21c04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398589(v=OCS.15)
ms:contentKeyID: 48184559
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd927f784fb0f2a835c896824105fe8bb112c7a1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444774"
---
# <a name="sessiondetails-table-in-lync-server-2013"></a><span data-ttu-id="9d1c1-103">Tabela SessionDetails no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9d1c1-103">SessionDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9d1c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9d1c1-104">

<span> </span></span></span>

<span data-ttu-id="9d1c1-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="9d1c1-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="9d1c1-106">Cada registro representa uma sessão ponto a ponto, que pode ser uma chamada telefônica VoIP-VoIP, uma sessão de mensagens instantâneas de duas partes ou outro tipo de sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-106">Each record represents one peer-to-peer session, which could be a VoIP-VoIP phone call, two-party IM session, or other type of session.</span></span> <span data-ttu-id="9d1c1-107">Você pode executar uma junção de tabela com a [tabela de mídia no Lync Server 2013](lync-server-2013-media-table.md) para encontrar os detalhes de cada mídia envolvida nesta sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-107">You can perform a table join with the [Media table in Lync Server 2013](lync-server-2013-media-table.md) to find the details of each media involved in this session.</span></span>

<span data-ttu-id="9d1c1-108">Observe que os campos IsUser1IntegratedWithDeskPhone e IsUser2IntegratedWithDeskPhone foram descartados da tabela SessionDetails usada no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-108">Note that the IsUser1IntegratedWithDeskPhone and the IsUser2IntegratedWithDeskPhone fields have been dropped from the SessionDetails table used in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d1c1-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="9d1c1-109">Column</span></span></th>
<th><span data-ttu-id="9d1c1-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9d1c1-110">Data Type</span></span></th>
<th><span data-ttu-id="9d1c1-111">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="9d1c1-111">Key/Index</span></span></th>
<th><span data-ttu-id="9d1c1-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="9d1c1-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-113"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-113"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-114">datetime</span><span class="sxs-lookup"><span data-stu-id="9d1c1-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-115">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="9d1c1-115">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-116">Tempo de solicitação de sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-116">Time of session request.</span></span> <span data-ttu-id="9d1c1-117">Usado em conjunto com o <strong>SessionIdSeq</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-117">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="9d1c1-118">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-118">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-119"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-119"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-120">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-120">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-121">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="9d1c1-121">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-122">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-122">ID number to identify the session.</span></span> <span data-ttu-id="9d1c1-123">Usado em conjunto com a <strong>identificação_da_sessãotime</strong> para identificar exclusivamente uma sessão. \* consulte a <a href="lync-server-2013-dialogs-table.md">tabela de caixas de diálogo no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-123">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.\* See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-124"><strong>CorrelationId</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-124"><strong>CorrelationId</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-125">identificador</span><span class="sxs-lookup"><span data-stu-id="9d1c1-125">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-126">Um GUID para correlacionar várias sessões.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-126">A GUID to correlate multiple sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-127"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-127"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-128">datetime</span><span class="sxs-lookup"><span data-stu-id="9d1c1-128">datetime</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-129">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-130">Número de identificação para identificar a caixa de diálogo que foi substituída pela sessão atual.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-130">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="9d1c1-131">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-131">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-132"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-132"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-133">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-133">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-134">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-134">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-135">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-135">ID number to identify the session.</span></span> <span data-ttu-id="9d1c1-136">Usado em conjunto com <strong>ReplacesDialogIdTime</strong> para identificar exclusivamente uma sessão substituída por esta sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-136">Used in conjunction with <strong>ReplacesDialogIdTime</strong> to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="9d1c1-137">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-137">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-138"><strong>Usuário1id</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-138"><strong>User1Id</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-139">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-139">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-140">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-140">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-141">ID de um usuário na sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-141">ID of one user in the session.</span></span> <span data-ttu-id="9d1c1-142">Consulte a <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-142">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-143"><strong>User2Id</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-143"><strong>User2Id</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-144">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-144">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-145">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-145">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-146">ID do outro usuário na sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-146">ID of the other user in the session.</span></span> <span data-ttu-id="9d1c1-147">Consulte a <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-147">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-148"><strong>User1EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-148"><strong>User1EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-149">Identificador</span><span class="sxs-lookup"><span data-stu-id="9d1c1-149">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-150">GUID que identifica o ponto de extremidade usado pelo primeiro usuário na sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-150">GUID that identifies the endpoint used by the first user in the session.</span></span></p>
<p><span data-ttu-id="9d1c1-151">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-151">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-152"><strong>User2EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-152"><strong>User2EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-153">Identificador</span><span class="sxs-lookup"><span data-stu-id="9d1c1-153">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-154">GUID que identifica o ponto de extremidade usado pelo segundo usuário na sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-154">GUID that identifies the endpoint used by the second user in the session.</span></span></p>
<p><span data-ttu-id="9d1c1-155">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-156"><strong>TargetUserId</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-156"><strong>TargetUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-157">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-157">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-158">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-158">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-159">O URI do usuário original na solicitação SIP.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-159">The original To user URI in the SIP request.</span></span> <span data-ttu-id="9d1c1-160">consulte a <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-160">see the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-161"><strong>SessionStartedById</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-161"><strong>SessionStartedById</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-162">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-162">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-163">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-163">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-164">ID do usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-164">ID of the user who started the session.</span></span> <span data-ttu-id="9d1c1-165">Consulte a <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-165">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-166"><strong>OnBehalfOfId</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-166"><strong>OnBehalfOfId</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-167">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-167">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-168">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-168">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-169">Indica a ID do usuário de quem o chamador está em nome.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-169">Indicates the ID of the user of who the caller is on behalf.</span></span> <span data-ttu-id="9d1c1-170">Consulte a <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-170">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-171"><strong>ReferredById</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-171"><strong>ReferredById</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-172">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-172">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-173">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-173">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-174">ID do usuário por quem a chamada é referida.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-174">ID of the user by who the call is referred.</span></span> <span data-ttu-id="9d1c1-175">Consulte a <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-175">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-176"><strong>ServerID</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-176"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-177">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-177">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-178">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-178">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-179">ID do servidor front-end usado para esta sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-179">ID of the front-end server used for this session.</span></span> <span data-ttu-id="9d1c1-180">Consulte a <a href="lync-server-2013-servers-table.md">tabela servidores no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-180">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-181"><strong>Poolid</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-181"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-182">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-182">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-183">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-183">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-184">ID do pool no qual a sessão foi capturada.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-184">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="9d1c1-185">Consulte a <a href="lync-server-2013-pools-table.md">tabela de grupos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-185">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-186"><strong>ContentTypeid</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-186"><strong>ContentTypeID</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-187">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-187">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-188">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-188">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-189">Tipo de conteúdo usado na sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-189">Content type used in the session.</span></span> <span data-ttu-id="9d1c1-190">Consulte a <a href="lync-server-2013-contenttypes-table.md">tabela ContentTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-190">See the <a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-191"><strong>User1ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-191"><strong>User1ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-192">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-192">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-193">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-194">Versão do cliente usada pelo Usuário1.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-194">Client version used by User1.</span></span> <span data-ttu-id="9d1c1-195">Consulte a <a href="lync-server-2013-clientversions-table.md">tabela ClientVersions no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-195">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-196"><strong>User2ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-196"><strong>User2ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-197">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-197">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-198">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-198">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-199">Versão do cliente usada pelo user2.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-199">Client version used by User2.</span></span> <span data-ttu-id="9d1c1-200">Consulte a <a href="lync-server-2013-clientversions-table.md">tabela ClientVersions no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-200">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-201"><strong>User1EdgeServerid</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-201"><strong>User1EdgeServerid</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-202">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-202">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-203">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-203">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-204">Servidor de borda usado pelo Usuário1.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-204">Edge Server used by User1.</span></span> <span data-ttu-id="9d1c1-205">Consulte a <a href="lync-server-2013-edgeservers-table.md">tabela EdgeServers no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-205">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-206"><strong>User2EdgeServerid</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-206"><strong>User2EdgeServerid</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-207">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-207">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-208">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-208">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-209">Servidor de borda usado pelo user2.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-209">Edge Server used by User2.</span></span> <span data-ttu-id="9d1c1-210">Consulte a <a href="lync-server-2013-edgeservers-table.md">tabela EdgeServers no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-210">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-211"><strong>IsUser1Internal</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-211"><strong>IsUser1Internal</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-212">bit</span><span class="sxs-lookup"><span data-stu-id="9d1c1-212">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-213">Se user1 está conectado de Internal ou not.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-213">Whether User1 is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-214"><strong>IsUser2Internal</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-214"><strong>IsUser2Internal</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-215">bit</span><span class="sxs-lookup"><span data-stu-id="9d1c1-215">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-216">Se o User2 está conectado do Internal ou não.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-216">Whether User2 is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-217"><strong>Invitetime</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-217"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-218">datetime</span><span class="sxs-lookup"><span data-stu-id="9d1c1-218">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-219">A hora da primeira solicitação INVITE.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-219">The time of the first INVITE request.</span></span> <span data-ttu-id="9d1c1-220">Geralmente, esse campo é preenchido por dados gerados da mensagem de convite inicial na sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-220">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="9d1c1-221">Se não houver nenhuma mensagem de convite, o campo será preenchido com a data e a hora da primeira mensagem SIP relevante (até mais, cancelamento, mensagem ou informações).</span><span class="sxs-lookup"><span data-stu-id="9d1c1-221">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span> <span data-ttu-id="9d1c1-222">Geralmente, esse campo é preenchido por dados gerados da mensagem de convite inicial na sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-222">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="9d1c1-223">Se não houver nenhuma mensagem de convite, o campo será preenchido com a data e a hora da primeira mensagem SIP relevante (até mais, cancelamento, mensagem ou informações).</span><span class="sxs-lookup"><span data-stu-id="9d1c1-223">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-224"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-224"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-225">datetime</span><span class="sxs-lookup"><span data-stu-id="9d1c1-225">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-226">A hora da resposta para a primeira mensagem de convite.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-226">The time of the response to the first INVITE message.</span></span> <span data-ttu-id="9d1c1-227">Geralmente, esse campo é preenchido por dados gerados da mensagem de convite inicial na sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-227">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="9d1c1-228">Se não houver nenhuma mensagem de convite, o campo será preenchido com a data e a hora da primeira mensagem SIP relevante (até mais, cancelamento, mensagem ou informações).</span><span class="sxs-lookup"><span data-stu-id="9d1c1-228">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-229"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-229"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-230">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-230">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-231">Código de resposta SIP para o convite da sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-231">SIP response code to the session invitation.</span></span> <span data-ttu-id="9d1c1-232">Geralmente, esse campo é preenchido por dados gerados da mensagem de convite inicial na sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-232">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="9d1c1-233">Se não houver nenhuma mensagem de convite, o campo será preenchido com a data e a hora da primeira mensagem SIP relevante (até mais, cancelamento, mensagem ou informações).</span><span class="sxs-lookup"><span data-stu-id="9d1c1-233">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-234"><strong>Diagnosticid</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-234"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-235">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-235">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-236">ID de diagnóstico capturada do cabeçalho SIP.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-236">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-237"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-237"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-238">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-238">int</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-239">Exterior</span><span class="sxs-lookup"><span data-stu-id="9d1c1-239">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-240">Prioridade da chamada.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-240">Call priority.</span></span> <span data-ttu-id="9d1c1-241">Consulte a <a href="lync-server-2013-callpriorities-table.md">tabela CallPriorities no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-241">See the <a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-242"><strong>User1MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-242"><strong>User1MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-243">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-243">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-244">Número de mensagens enviadas pelo Usuário1 durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-244">Number of messages sent by User1 during the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-245"><strong>User2MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-245"><strong>User2MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-246">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-246">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-247">Número de mensagens enviadas pelo user2 durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-247">Number of messages sent by User2 during the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-248"><strong>SessionEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-248"><strong>SessionEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-249">datetime</span><span class="sxs-lookup"><span data-stu-id="9d1c1-249">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-250">Hora no final da sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-250">Time at the end of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-251"><strong>MediaTypes</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-251"><strong>MediaTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-252">int</span><span class="sxs-lookup"><span data-stu-id="9d1c1-252">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-253">Um conjunto de bits que indica o tipo de mídia desta sessão.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-253">A bit set that indicates the media type of this session.</span></span> <span data-ttu-id="9d1c1-254">Listadas são as definições dos tipos:</span><span class="sxs-lookup"><span data-stu-id="9d1c1-254">Listed are the definitions of the types:</span></span></p>
<h3 id="section-1"> </h3>
<div>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-255">Mensagem instantânea</span><span class="sxs-lookup"><span data-stu-id="9d1c1-255">IM</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-256">1</span><span class="sxs-lookup"><span data-stu-id="9d1c1-256">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-257">FILE_TRANSFER</span><span class="sxs-lookup"><span data-stu-id="9d1c1-257">FILE_TRANSFER</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-258">2</span><span class="sxs-lookup"><span data-stu-id="9d1c1-258">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-259">REMOTE_ASSISTANCE</span><span class="sxs-lookup"><span data-stu-id="9d1c1-259">REMOTE_ASSISTANCE</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-260">4</span><span class="sxs-lookup"><span data-stu-id="9d1c1-260">4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-261">APP_SHARING</span><span class="sxs-lookup"><span data-stu-id="9d1c1-261">APP_SHARING</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-262">8</span><span class="sxs-lookup"><span data-stu-id="9d1c1-262">8</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-263">ÁUDIO</span><span class="sxs-lookup"><span data-stu-id="9d1c1-263">AUDIO</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-264">16</span><span class="sxs-lookup"><span data-stu-id="9d1c1-264">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-265">VIDEO</span><span class="sxs-lookup"><span data-stu-id="9d1c1-265">VIDEO</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-266">32</span><span class="sxs-lookup"><span data-stu-id="9d1c1-266">32</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-267">APP_INVITE</span><span class="sxs-lookup"><span data-stu-id="9d1c1-267">APP_INVITE</span></span></p></td>
<td><p><span data-ttu-id="9d1c1-268">64</span><span class="sxs-lookup"><span data-stu-id="9d1c1-268">64</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-269"><strong>User1Flag</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-269"><strong>User1Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-270">smallint</span><span class="sxs-lookup"><span data-stu-id="9d1c1-270">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-271">Um conjunto de bits que indica os atributos Usuário1.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-271">A bit set that indicates the User1 attributes.</span></span> <span data-ttu-id="9d1c1-272">As definições de atributo a seguir estão listadas:</span><span class="sxs-lookup"><span data-stu-id="9d1c1-272">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d1c1-273">0x01-integrado ao telefone desktop</span><span class="sxs-lookup"><span data-stu-id="9d1c1-273">0x01 - Integrated with desktop phone</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-274"><strong>User2Flag</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-274"><strong>User2Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-275">smallint</span><span class="sxs-lookup"><span data-stu-id="9d1c1-275">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-276">Um conjunto de bits que indica os atributos do user2.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-276">A bit set that indicates the User2 attributes.</span></span> <span data-ttu-id="9d1c1-277">As definições de atributo a seguir estão listadas:</span><span class="sxs-lookup"><span data-stu-id="9d1c1-277">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d1c1-278">0x01-integrado ao telefone desktop</span><span class="sxs-lookup"><span data-stu-id="9d1c1-278">0x01 - Integrated with desktop phone</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d1c1-279"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-279"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-280">smallint</span><span class="sxs-lookup"><span data-stu-id="9d1c1-280">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-281">Um conjunto de bits que indica os atributos da chamada.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-281">A bit set that indicates the call attributes.</span></span> <span data-ttu-id="9d1c1-282">As definições de atributo a seguir estão listadas:</span><span class="sxs-lookup"><span data-stu-id="9d1c1-282">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="9d1c1-283">0x01-sessão repetida</span><span class="sxs-lookup"><span data-stu-id="9d1c1-283">0x01 - Retried Session</span></span></p></li>
<li><p><span data-ttu-id="9d1c1-284">0x02-uma chamada feita pelo agente em nome de um grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="9d1c1-284">0x02 - A call made by agent on behalf of a response group</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d1c1-285"><strong>Processe</strong></span><span class="sxs-lookup"><span data-stu-id="9d1c1-285"><strong>Processed</strong></span></span></p></td>
<td><p><span data-ttu-id="9d1c1-286">bit</span><span class="sxs-lookup"><span data-stu-id="9d1c1-286">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d1c1-287">Para uso interno pelo serviço de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-287">For internal use by the Monitoring service.</span></span></p>
<p><span data-ttu-id="9d1c1-288">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-288">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9d1c1-289">\* Para a maioria das sessões, o SessionIdSeq terá o valor de 1.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-289">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="9d1c1-290">Se várias sessões começarem exatamente ao mesmo tempo, o SessionIdSeq de uma será 1, por outro será 2, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9d1c1-290">If multiple sessions start at exactly the same time, the SessionIdSeq for one will be 1, for another will be 2, and so on.</span></span>

<span data-ttu-id="9d1c1-291"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9d1c1-291"></div>

<span> </span>

</div>

</div>

</span></span></div>

