---
title: 'Lync Server 2013: tblNode'
description: 'Lync Server 2013: tblNode.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblNode
ms:assetid: a31d2961-aa83-4286-a12e-15d279c95f19
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615024(v=OCS.15)
ms:contentKeyID: 48184960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0a5d630621c32cbc54501249c7a679bf4023c60
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423516"
---
# <a name="tblnode-in-lync-server-2013"></a><span data-ttu-id="6b2ff-103">tblNode no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6b2ff-103">tblNode in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6b2ff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6b2ff-104">

<span> </span></span></span>

<span data-ttu-id="6b2ff-105">_**Tópico da última modificação:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="6b2ff-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="6b2ff-106">tblNode contém a árvore de objetos (com os nós da categoria ou da sala de chat), conforme gerenciado no painel de controle e cmdlets administrativos do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-106">tblNode contains the object tree (with category or chat room nodes) as managed in the Lync Server 2013 Control Panel and administrative cmdlets.</span></span>

### <a name="columns"></a><span data-ttu-id="6b2ff-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="6b2ff-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b2ff-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="6b2ff-108">Column</span></span></th>
<th><span data-ttu-id="6b2ff-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="6b2ff-109">Type</span></span></th>
<th><span data-ttu-id="6b2ff-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b2ff-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b2ff-111">NodeId</span><span class="sxs-lookup"><span data-stu-id="6b2ff-111">nodeID</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-112">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="6b2ff-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-113">ID do nó (número exclusivo).</span><span class="sxs-lookup"><span data-stu-id="6b2ff-113">Node ID (unique number).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b2ff-114">nodeGuid</span><span class="sxs-lookup"><span data-stu-id="6b2ff-114">nodeGuid</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-115">GUID, não nulo</span><span class="sxs-lookup"><span data-stu-id="6b2ff-115">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-116">GUID do nó.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-116">Node GUID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b2ff-117">parentID</span><span class="sxs-lookup"><span data-stu-id="6b2ff-117">parentID</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-118">int</span><span class="sxs-lookup"><span data-stu-id="6b2ff-118">int</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-119">ID do nó do pai.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-119">Node ID of parent.</span></span> <span data-ttu-id="6b2ff-120">O nó raiz (com ID 1) também inclui o próprio pai.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-120">The root node (with ID 1) includes itself as parent as well.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b2ff-121">nodeType</span><span class="sxs-lookup"><span data-stu-id="6b2ff-121">nodeType</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-122">bit, e não nulo</span><span class="sxs-lookup"><span data-stu-id="6b2ff-122">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-123">Verdadeiro se o nó for uma categoria.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-123">True if the node is a category.</span></span></p>
<p><span data-ttu-id="6b2ff-124">Falso se o nó for uma sala de chat.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-124">False if the node is a chat room.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b2ff-125">Node</span><span class="sxs-lookup"><span data-stu-id="6b2ff-125">nodeName</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-126">nvarchar (256), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="6b2ff-126">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-127">Nome do nó.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-127">Node name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b2ff-128">nodeDesc</span><span class="sxs-lookup"><span data-stu-id="6b2ff-128">nodeDesc</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-129">nvarchar (256), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="6b2ff-129">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-130">Descrição do nó.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-130">Node description.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b2ff-131">Eles</span><span class="sxs-lookup"><span data-stu-id="6b2ff-131">invite</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-132">bit</span><span class="sxs-lookup"><span data-stu-id="6b2ff-132">bit</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-133">Para categorias:</span><span class="sxs-lookup"><span data-stu-id="6b2ff-133">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="6b2ff-134">Verdadeiro se os convites estiverem em.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-134">True if invites are on.</span></span></p></li>
<li><p><span data-ttu-id="6b2ff-135">Falso se os convites estiverem desativados.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-135">False if invites are off.</span></span></p></li>
</ul>
<p><span data-ttu-id="6b2ff-136">Para salas:</span><span class="sxs-lookup"><span data-stu-id="6b2ff-136">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="6b2ff-137">Falso se os convites estiverem desativados (Substitui a categoria pai).</span><span class="sxs-lookup"><span data-stu-id="6b2ff-137">False if invites are off (overrides the parent category).</span></span></p></li>
<li><p><span data-ttu-id="6b2ff-138">Nulo se a configuração convites for herdada da categoria pai.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-138">Null if the invites setting is inherited from the parent category.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b2ff-139">realizou</span><span class="sxs-lookup"><span data-stu-id="6b2ff-139">logged</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-140">bit</span><span class="sxs-lookup"><span data-stu-id="6b2ff-140">bit</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-141">Para categorias:</span><span class="sxs-lookup"><span data-stu-id="6b2ff-141">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="6b2ff-142">Verdadeiro se o histórico de chats estiver ativado.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-142">True if chat history is on.</span></span></p></li>
<li><p><span data-ttu-id="6b2ff-143">Falso se o histórico de chats estiver desativado.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-143">False if chat history is off.</span></span></p></li>
</ul>
<p><span data-ttu-id="6b2ff-144">Para salas:</span><span class="sxs-lookup"><span data-stu-id="6b2ff-144">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="6b2ff-145">Vazio.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-145">Null.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b2ff-146">Postagem de mensagem</span><span class="sxs-lookup"><span data-stu-id="6b2ff-146">filePost</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-147">bit</span><span class="sxs-lookup"><span data-stu-id="6b2ff-147">bit</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-148">Para categorias:</span><span class="sxs-lookup"><span data-stu-id="6b2ff-148">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="6b2ff-149">Verdadeiro se os carregamentos de arquivo forem permitidos.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-149">True if file uploads are allowed.</span></span></p></li>
<li><p><span data-ttu-id="6b2ff-150">Falso se os carregamentos de arquivos não forem permitidos.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-150">False if file uploads are disallowed.</span></span></p></li>
</ul>
<p><span data-ttu-id="6b2ff-151">Para salas:</span><span class="sxs-lookup"><span data-stu-id="6b2ff-151">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="6b2ff-152">Vazio.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-152">Null.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b2ff-153">ativo</span><span class="sxs-lookup"><span data-stu-id="6b2ff-153">disabled</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-154">bit, e não nulo</span><span class="sxs-lookup"><span data-stu-id="6b2ff-154">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-155">Verdadeiro se a sala de chat estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-155">True if the chat room is disabled.</span></span> <span data-ttu-id="6b2ff-156">Aplica-se somente a salas de chat.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-156">Applies only to chat rooms.</span></span> <span data-ttu-id="6b2ff-157">(Falso para categorias.)</span><span class="sxs-lookup"><span data-stu-id="6b2ff-157">(False for categories.)</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b2ff-158">funcionamento</span><span class="sxs-lookup"><span data-stu-id="6b2ff-158">behavior</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-159">smallint, não nulo</span><span class="sxs-lookup"><span data-stu-id="6b2ff-159">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-160">Comportamento (pesquisado na tabela EnumValue):</span><span class="sxs-lookup"><span data-stu-id="6b2ff-160">Behavior (looked up in EnumValue table):</span></span></p>
<ul>
<li><p><span data-ttu-id="6b2ff-161">4: normal (salas de chat normal).</span><span class="sxs-lookup"><span data-stu-id="6b2ff-161">4: Normal (normal chat rooms).</span></span></p></li>
<li><p><span data-ttu-id="6b2ff-162">5: Auditorium (salas de chat Auditorium, somente os apresentadores podem contribuir).</span><span class="sxs-lookup"><span data-stu-id="6b2ff-162">5: Auditorium (auditorium chat rooms, only presenters can contribute).</span></span></p></li>
</ul>
<p><span data-ttu-id="6b2ff-163">Aplica-se somente a salas de chat.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-163">Applies only to chat rooms.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b2ff-164">visibilidade</span><span class="sxs-lookup"><span data-stu-id="6b2ff-164">visibility</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-165">smallint, não nulo</span><span class="sxs-lookup"><span data-stu-id="6b2ff-165">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-166">Visibilidade (pesquisada na tabela de EnumValue):</span><span class="sxs-lookup"><span data-stu-id="6b2ff-166">Visibility (looked up on EnumValue table):</span></span></p>
<ul>
<li><p><span data-ttu-id="6b2ff-167">2: particular</span><span class="sxs-lookup"><span data-stu-id="6b2ff-167">2: Private</span></span></p></li>
<li><p><span data-ttu-id="6b2ff-168">3: com escopo</span><span class="sxs-lookup"><span data-stu-id="6b2ff-168">3: Scoped</span></span></p></li>
<li><p><span data-ttu-id="6b2ff-169">6: abrir</span><span class="sxs-lookup"><span data-stu-id="6b2ff-169">6: Open</span></span></p></li>
</ul>
<p><span data-ttu-id="6b2ff-170">Aplica-se somente a salas de chat.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-170">Applies only to chat rooms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b2ff-171">siopID</span><span class="sxs-lookup"><span data-stu-id="6b2ff-171">siopID</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-172">GUID</span><span class="sxs-lookup"><span data-stu-id="6b2ff-172">GUID</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-173">Add-In GUID se um suplemento estiver associado a esta sala de chat.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-173">Add-In GUID if an add-in is associated with this chat room.</span></span> <span data-ttu-id="6b2ff-174">(As categorias não têm suplementos.)</span><span class="sxs-lookup"><span data-stu-id="6b2ff-174">(Categories do not have add-ins.)</span></span></p>
<p><span data-ttu-id="6b2ff-175">As informações do suplemento são pesquisadas na tabela SiopWhiteList.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-175">The add-in information is looked up in SiopWhiteList table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b2ff-176">nodeAddedBy</span><span class="sxs-lookup"><span data-stu-id="6b2ff-176">nodeAddedBy</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-177">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="6b2ff-177">int, not null</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-178">ID da entidade de segurança que criou esse nó.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-178">ID of the principal that created this node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b2ff-179">nodeAddedOn</span><span class="sxs-lookup"><span data-stu-id="6b2ff-179">nodeAddedOn</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-180">bigint, e não nulo</span><span class="sxs-lookup"><span data-stu-id="6b2ff-180">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-181">Carimbo de data/hora da criação de nós.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-181">Time stamp of the node creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b2ff-182">nodeUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="6b2ff-182">nodeUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-183">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="6b2ff-183">int, not null</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-184">ID da entidade de segurança que fez a atualização mais recente deste nó.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-184">ID of the principal that did the latest update of this node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b2ff-185">nodeUpdatedOn</span><span class="sxs-lookup"><span data-stu-id="6b2ff-185">nodeUpdatedOn</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-186">bigint, e não nulo</span><span class="sxs-lookup"><span data-stu-id="6b2ff-186">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-187">Carimbo de data/hora da atualização mais recente deste nó.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-187">Time stamp of the latest update of this node.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b2ff-188">purgedOn</span><span class="sxs-lookup"><span data-stu-id="6b2ff-188">purgedOn</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-189">datetime</span><span class="sxs-lookup"><span data-stu-id="6b2ff-189">datetime</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-190">Hora da última operação de limpeza (remoção de escopos da tabela tblScopedPrincipal e funções da tabela tblPrincipalRole) que afetou esse nó.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-190">Time of the latest purge operation (removal of scopes from tblScopedPrincipal table and roles from tblPrincipalRole table) that affected this node.</span></span> <span data-ttu-id="6b2ff-191">Isso é usado pelo mecanismo de atualização do cache interno do serviço de chat.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-191">This is used by the Chat service’s internal cache update mechanism.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="6b2ff-192">As</span><span class="sxs-lookup"><span data-stu-id="6b2ff-192">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b2ff-193">Coluna</span><span class="sxs-lookup"><span data-stu-id="6b2ff-193">Column</span></span></th>
<th><span data-ttu-id="6b2ff-194">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b2ff-194">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b2ff-195">NodeId</span><span class="sxs-lookup"><span data-stu-id="6b2ff-195">nodeID</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-196">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-196">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b2ff-197">funcionamento</span><span class="sxs-lookup"><span data-stu-id="6b2ff-197">behavior</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-198">Chave estrangeira com Lookup na tabela tblEnumValue. valueid.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-198">Foreign key with lookup in tblEnumValue.valueID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b2ff-199">visibilidade</span><span class="sxs-lookup"><span data-stu-id="6b2ff-199">visibility</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-200">Chave estrangeira com Lookup na tabela tblEnumValue. valueid.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-200">Foreign key with lookup in tblEnumValue.valueID table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b2ff-201">parentID</span><span class="sxs-lookup"><span data-stu-id="6b2ff-201">parentID</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-202">Chave estrangeira com Lookup na tabela tblNode. NodeId.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-202">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b2ff-203">siopID</span><span class="sxs-lookup"><span data-stu-id="6b2ff-203">siopID</span></span></p></td>
<td><p><span data-ttu-id="6b2ff-204">Chave estrangeira com Lookup na tabela tblSiopWhiteList. siopId.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-204">Foreign key with lookup in tblSiopWhiteList.siopId table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6b2ff-205">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6b2ff-205">


</div>

<span> </span>

</div>

</div>

</span></span></div>

