---
title: 'Lync Server 2013: tblPrincipalInvites'
description: 'Lync Server 2013: tblPrincipalInvites.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalInvites
ms:assetid: 548ec156-4d1a-469d-a804-62cff226e5c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558650(v=OCS.15)
ms:contentKeyID: 48184141
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d30d741864ed2a3cfbec8329215be33c21b3b262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423502"
---
# <a name="tblprincipalinvites-in-lync-server-2013"></a><span data-ttu-id="ae9d6-103">tblPrincipalInvites no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae9d6-103">tblPrincipalInvites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae9d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae9d6-104">

<span> </span></span></span>

<span data-ttu-id="ae9d6-105">_**Tópico da última modificação:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="ae9d6-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="ae9d6-106">tblPrincipalInvites contém convites para todos os usuários provisionados para todos os nós com convite automático ativado.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-106">tblPrincipalInvites contains invitations for all provisioned users for all nodes with auto-invite on.</span></span>

### <a name="columns"></a><span data-ttu-id="ae9d6-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="ae9d6-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae9d6-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="ae9d6-108">Column</span></span></th>
<th><span data-ttu-id="ae9d6-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae9d6-109">Type</span></span></th>
<th><span data-ttu-id="ae9d6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae9d6-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae9d6-111">multiimprimir</span><span class="sxs-lookup"><span data-stu-id="ae9d6-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="ae9d6-112">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="ae9d6-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="ae9d6-113">ID da entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae9d6-114">invID</span><span class="sxs-lookup"><span data-stu-id="ae9d6-114">invID</span></span></p></td>
<td><p><span data-ttu-id="ae9d6-115">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="ae9d6-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="ae9d6-116">Número seqüencial exclusivo (por ID da entidade) gerado pela tabela tblLastInviteId.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-116">Unique sequential number (per principal ID) generated from tblLastInviteId table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae9d6-117">NodeId</span><span class="sxs-lookup"><span data-stu-id="ae9d6-117">nodeID</span></span></p></td>
<td><p><span data-ttu-id="ae9d6-118">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="ae9d6-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="ae9d6-119">ID do nó (somente sala de chat).</span><span class="sxs-lookup"><span data-stu-id="ae9d6-119">Node ID (chat room only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae9d6-120">criar</span><span class="sxs-lookup"><span data-stu-id="ae9d6-120">createdOn</span></span></p></td>
<td><p><span data-ttu-id="ae9d6-121">DateTime, não nulo</span><span class="sxs-lookup"><span data-stu-id="ae9d6-121">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="ae9d6-122">Hora da criação.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-122">Time of creation.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="ae9d6-123">As</span><span class="sxs-lookup"><span data-stu-id="ae9d6-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae9d6-124">Coluna</span><span class="sxs-lookup"><span data-stu-id="ae9d6-124">Column</span></span></th>
<th><span data-ttu-id="ae9d6-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae9d6-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae9d6-126">&lt;, NodeId&gt;</span><span class="sxs-lookup"><span data-stu-id="ae9d6-126">&lt;prinID, nodeID&gt;</span></span></p></td>
<td><p><span data-ttu-id="ae9d6-127">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae9d6-128">multiimprimir</span><span class="sxs-lookup"><span data-stu-id="ae9d6-128">prinID</span></span></p></td>
<td><p><span data-ttu-id="ae9d6-129">Chave estrangeira com Lookup na tabela tblPrincipal. retoid.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-129">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae9d6-130">NodeId</span><span class="sxs-lookup"><span data-stu-id="ae9d6-130">nodeID</span></span></p></td>
<td><p><span data-ttu-id="ae9d6-131">Chave estrangeira com Lookup na tabela tblNode. NodeId.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-131">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ae9d6-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae9d6-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

