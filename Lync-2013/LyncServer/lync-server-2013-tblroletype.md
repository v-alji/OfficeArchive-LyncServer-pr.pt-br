---
title: 'Lync Server 2013: tblRoleType'
description: 'Lync Server 2013: tblRoleType.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblRoleType
ms:assetid: 1eac3a54-656a-40ac-b771-edfc64d6e34b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558623(v=OCS.15)
ms:contentKeyID: 48183577
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f458259acaee7821d5f6a7339b993c70fe65f595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389748"
---
# <a name="tblroletype-in-lync-server-2013"></a><span data-ttu-id="7d502-103">tblRoleType no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d502-103">tblRoleType in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7d502-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7d502-104">

<span> </span></span></span>

<span data-ttu-id="7d502-105">_**Tópico da última modificação:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="7d502-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="7d502-106">tblRoleType é uma tabela de pesquisa estática com tipos de função e seus conjuntos de permissões associados.</span><span class="sxs-lookup"><span data-stu-id="7d502-106">tblRoleType is a static lookup table with role types and their associated permission sets.</span></span>

### <a name="columns"></a><span data-ttu-id="7d502-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="7d502-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7d502-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="7d502-108">Column</span></span></th>
<th><span data-ttu-id="7d502-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d502-109">Type</span></span></th>
<th><span data-ttu-id="7d502-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d502-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d502-111">rtypeID</span><span class="sxs-lookup"><span data-stu-id="7d502-111">rtypeID</span></span></p></td>
<td><p><span data-ttu-id="7d502-112">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="7d502-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="7d502-113">ID do tipo de função.</span><span class="sxs-lookup"><span data-stu-id="7d502-113">Role type ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d502-114">rtypeDesc</span><span class="sxs-lookup"><span data-stu-id="7d502-114">rtypeDesc</span></span></p></td>
<td><p><span data-ttu-id="7d502-115">nvarchar (256), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="7d502-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="7d502-116">Descrição do tipo de função.</span><span class="sxs-lookup"><span data-stu-id="7d502-116">Role type description.</span></span> <span data-ttu-id="7d502-117">Há quatro funções disponíveis:</span><span class="sxs-lookup"><span data-stu-id="7d502-117">There are four available roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="7d502-118">Membro: membro da sala de chat</span><span class="sxs-lookup"><span data-stu-id="7d502-118">Member: Chat room member</span></span></p></li>
<li><p><span data-ttu-id="7d502-119">Manager: gerente da sala de chat</span><span class="sxs-lookup"><span data-stu-id="7d502-119">Manager: Chat room manager</span></span></p></li>
<li><p><span data-ttu-id="7d502-120">Encaixado: apresentador para uma sala de chat do Auditorium</span><span class="sxs-lookup"><span data-stu-id="7d502-120">Voiced: Presenter for an auditorium chat room</span></span></p></li>
<li><p><span data-ttu-id="7d502-121">Creator: pode criar salas de chat</span><span class="sxs-lookup"><span data-stu-id="7d502-121">Creator: Can create chat rooms</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d502-122">rtypeAllowedPermSet</span><span class="sxs-lookup"><span data-stu-id="7d502-122">rtypeAllowedPermSet</span></span></p></td>
<td><p><span data-ttu-id="7d502-123">bigint, e não nulo</span><span class="sxs-lookup"><span data-stu-id="7d502-123">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="7d502-124">Conjunto de permissões para a função.</span><span class="sxs-lookup"><span data-stu-id="7d502-124">Permission set for the role.</span></span> <span data-ttu-id="7d502-125">Os bits usados são:</span><span class="sxs-lookup"><span data-stu-id="7d502-125">The used bits are:</span></span></p>
<ul>
<li><p><span data-ttu-id="7d502-126">2: verdadeiro se a função puder gerenciar nós.</span><span class="sxs-lookup"><span data-stu-id="7d502-126">2: True if the role can manage nodes.</span></span></p></li>
<li><p><span data-ttu-id="7d502-127">4: verdadeiro se a função puder criar nós filhos.</span><span class="sxs-lookup"><span data-stu-id="7d502-127">4: True if the role can create children nodes.</span></span></p></li>
<li><p><span data-ttu-id="7d502-128">7: verdadeiro se a função puder ingressar em uma sala de chat (ou salas de chat dos filhos de uma categoria).</span><span class="sxs-lookup"><span data-stu-id="7d502-128">7: True if the role can join a chat room (or children chat rooms of a category).</span></span></p></li>
<li><p><span data-ttu-id="7d502-129">8: verdadeiro se a função puder conversar em uma sala de chat (ou nas salas de chat dos filhos de uma categoria).</span><span class="sxs-lookup"><span data-stu-id="7d502-129">8: True if the role can chat in a chat room (or in children chat rooms of a category).</span></span></p></li>
<li><p><span data-ttu-id="7d502-130">10: verdadeiro se a função puder ler o histórico de chats mesmo quando não estiver associado a uma sala de chat.</span><span class="sxs-lookup"><span data-stu-id="7d502-130">10: True if the role can read chat history even when not joined to a chat room.</span></span></p></li>
<li><p><span data-ttu-id="7d502-131">11: verdadeiro se a função puder ver a sala de chat.</span><span class="sxs-lookup"><span data-stu-id="7d502-131">11: True if the role can see the chat room.</span></span> <span data-ttu-id="7d502-132">(Isso é ainda mais refinado por fatores como escopo e visibilidade.)</span><span class="sxs-lookup"><span data-stu-id="7d502-132">(This is further refined by factors such as scope and visibility.)</span></span></p></li>
<li><p><span data-ttu-id="7d502-133">12: verdadeiro se a função puder conversar em uma sala de chat do Auditorium.</span><span class="sxs-lookup"><span data-stu-id="7d502-133">12: True if the role can chat in an auditorium chat room.</span></span></p></li>
<li><p><span data-ttu-id="7d502-134">13: verdadeiro se a função puder ignorar as regras de visibilidade ao exibir nós.</span><span class="sxs-lookup"><span data-stu-id="7d502-134">13: True if the role can bypass visibility rules when viewing nodes.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="7d502-135">Chave</span><span class="sxs-lookup"><span data-stu-id="7d502-135">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7d502-136">Coluna</span><span class="sxs-lookup"><span data-stu-id="7d502-136">Column</span></span></th>
<th><span data-ttu-id="7d502-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d502-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d502-138">rtypeID</span><span class="sxs-lookup"><span data-stu-id="7d502-138">rtypeID</span></span></p></td>
<td><p><span data-ttu-id="7d502-139">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="7d502-139">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7d502-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7d502-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

