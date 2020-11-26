---
title: 'Lync Server 2013: modo de exibição VoIPDetails'
description: 'Lync Server 2013: modo de exibição VoIPDetails.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VoIPDetails view
ms:assetid: 14c44736-71ba-4fc5-82c7-1df65bf6261c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687973(v=OCS.15)
ms:contentKeyID: 49733561
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ecd34be0c8568eef29d773f088e8503a8065743
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446181"
---
# <a name="voipdetails-view-in-lync-server-2013"></a><span data-ttu-id="09c0d-103">Exibição VoIPDetails no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09c0d-103">VoIPDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09c0d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09c0d-104">

<span> </span></span></span>

<span data-ttu-id="09c0d-105">_**Tópico da última modificação:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="09c0d-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="09c0d-106">A exibição VoIPDetails armazena informações sobre sessões ponto a ponto, onde pelo menos um usuário é um usuário de VoIP.</span><span class="sxs-lookup"><span data-stu-id="09c0d-106">The VoIPDetails view stores information about peer-to-peer sessions, where at least one user is a VoIP user.</span></span> <span data-ttu-id="09c0d-107">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="09c0d-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="09c0d-108">A exibição VoIPDetails contém todas as colunas na <A href="lync-server-2013-sessiondetails-view.md">exibição SessionDetails do Lync Server 2013</A> , além das colunas listadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="09c0d-108">The VoIPDetails view contains all of the columns in the <A href="lync-server-2013-sessiondetails-view.md">SessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09c0d-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="09c0d-109">Column</span></span></th>
<th><span data-ttu-id="09c0d-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="09c0d-110">Data Type</span></span></th>
<th><span data-ttu-id="09c0d-111">Detalhes</span><span class="sxs-lookup"><span data-stu-id="09c0d-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09c0d-112"><strong>FromPhone</strong></span><span class="sxs-lookup"><span data-stu-id="09c0d-112"><strong>FromPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="09c0d-113">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="09c0d-113">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="09c0d-114">URI do telefone do usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="09c0d-114">Phone URI of the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09c0d-115"><strong>Por telefone</strong></span><span class="sxs-lookup"><span data-stu-id="09c0d-115"><strong>ToPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="09c0d-116">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="09c0d-116">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="09c0d-117">URI do telefone do usuário que ingressou na sessão.</span><span class="sxs-lookup"><span data-stu-id="09c0d-117">Phone URI of the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09c0d-118"><strong>DisconnectedByUri</strong></span><span class="sxs-lookup"><span data-stu-id="09c0d-118"><strong>DisconnectedByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="09c0d-119">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="09c0d-119">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="09c0d-120">URL do usuário que desconectou a sessão.</span><span class="sxs-lookup"><span data-stu-id="09c0d-120">URI of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09c0d-121"><strong>DisconnectedByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="09c0d-121"><strong>DisconnectedByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="09c0d-122">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="09c0d-122">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="09c0d-123">Tipo de URI do usuário que desconectou a sessão.</span><span class="sxs-lookup"><span data-stu-id="09c0d-123">Type of URI of the user who disconnected the session.</span></span> <span data-ttu-id="09c0d-124">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="09c0d-124">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09c0d-125"><strong>DisconnectedByTenant</strong></span><span class="sxs-lookup"><span data-stu-id="09c0d-125"><strong>DisconnectedByTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="09c0d-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="09c0d-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="09c0d-127">Locatário do usuário que desconectou a sessão.</span><span class="sxs-lookup"><span data-stu-id="09c0d-127">Tenant of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09c0d-128"><strong>DisconnectedByPhone</strong></span><span class="sxs-lookup"><span data-stu-id="09c0d-128"><strong>DisconnectedByPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="09c0d-129">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="09c0d-129">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="09c0d-130">URI do telefone do usuário que desconectou a sessão.</span><span class="sxs-lookup"><span data-stu-id="09c0d-130">Phone URI of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09c0d-131"><strong>FromMediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="09c0d-131"><strong>FromMediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="09c0d-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="09c0d-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="09c0d-133">Servidor de mediação usado pelo usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="09c0d-133">Mediation Server used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09c0d-134"><strong>ToMediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="09c0d-134"><strong>ToMediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="09c0d-135">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="09c0d-135">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="09c0d-136">Servidor de mediação usado pelo usuário que ingressou na sessão.</span><span class="sxs-lookup"><span data-stu-id="09c0d-136">Mediation Server used by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09c0d-137"><strong>FromGateway</strong></span><span class="sxs-lookup"><span data-stu-id="09c0d-137"><strong>FromGateway</strong></span></span></p></td>
<td><p><span data-ttu-id="09c0d-138">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="09c0d-138">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="09c0d-139">O gateway usado pelo usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="09c0d-139">Gateway used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09c0d-140"><strong>Togateway</strong></span><span class="sxs-lookup"><span data-stu-id="09c0d-140"><strong>ToGateway</strong></span></span></p></td>
<td><p><span data-ttu-id="09c0d-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="09c0d-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="09c0d-142">O gateway usado pelo usuário que ingressou na sessão.</span><span class="sxs-lookup"><span data-stu-id="09c0d-142">Gateway used by the user who joined the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="09c0d-143">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09c0d-143">


</div>

<span> </span>

</div>

</div>

</span></span></div>

