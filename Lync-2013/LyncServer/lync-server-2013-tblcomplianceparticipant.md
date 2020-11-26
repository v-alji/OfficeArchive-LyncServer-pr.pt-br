---
title: 'Lync Server 2013: tblComplianceParticipant'
description: 'Lync Server 2013: tblComplianceParticipant.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceParticipant
ms:assetid: 5d7e0dea-74f7-46d1-badf-b94abc8f066d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558655(v=OCS.15)
ms:contentKeyID: 48184262
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1385b0a635f003a72de93f10f72642314ad7ebd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444452"
---
# <a name="tblcomplianceparticipant-in-lync-server-2013"></a><span data-ttu-id="fc094-103">tblComplianceParticipant no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc094-103">tblComplianceParticipant in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fc094-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fc094-104">

<span> </span></span></span>

<span data-ttu-id="fc094-105">_**Tópico da última modificação:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="fc094-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="fc094-106">tblComplianceParticipant contém os participantes atuais por canal e por servidor.</span><span class="sxs-lookup"><span data-stu-id="fc094-106">tblComplianceParticipant contains the current participants per channel and per server.</span></span>

### <a name="columns"></a><span data-ttu-id="fc094-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="fc094-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc094-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="fc094-108">Column</span></span></th>
<th><span data-ttu-id="fc094-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc094-109">Type</span></span></th>
<th><span data-ttu-id="fc094-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc094-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc094-111">channelUri</span><span class="sxs-lookup"><span data-stu-id="fc094-111">channelUri</span></span></p></td>
<td><p><span data-ttu-id="fc094-112">nvarchar (255), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="fc094-112">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="fc094-113">URI (Uniform Resource Identifier) do canal.</span><span class="sxs-lookup"><span data-stu-id="fc094-113">Channel Uniform Resource Identifier (URI).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc094-114">ID</span><span class="sxs-lookup"><span data-stu-id="fc094-114">userId</span></span></p></td>
<td><p><span data-ttu-id="fc094-115">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="fc094-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="fc094-116">ID da entidade de segurança do participante (correspondente à tabela tblPrincipal. retoid).</span><span class="sxs-lookup"><span data-stu-id="fc094-116">Principal ID of the participant (corresponding to tblPrincipal.prinID table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc094-117">joinedAt</span><span class="sxs-lookup"><span data-stu-id="fc094-117">joinedAt</span></span></p></td>
<td><p><span data-ttu-id="fc094-118">bigint, e não nulo</span><span class="sxs-lookup"><span data-stu-id="fc094-118">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="fc094-119">Carimbo de data/hora do evento de associação.</span><span class="sxs-lookup"><span data-stu-id="fc094-119">Time stamp of the joining event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc094-120">partedAt</span><span class="sxs-lookup"><span data-stu-id="fc094-120">partedAt</span></span></p></td>
<td><p><span data-ttu-id="fc094-121">bigint</span><span class="sxs-lookup"><span data-stu-id="fc094-121">bigint</span></span></p></td>
<td><p><span data-ttu-id="fc094-122">NULL se o participante ainda estiver associado.</span><span class="sxs-lookup"><span data-stu-id="fc094-122">Null if participant is still joined.</span></span> <span data-ttu-id="fc094-123">O carimbo de data/hora do evento de persaiar de canal, se não for nulo.</span><span class="sxs-lookup"><span data-stu-id="fc094-123">The time stamp of the channel leaving event if not null.</span></span></p>
<p><span data-ttu-id="fc094-124">Essas entradas são eventualmente removidas quando todos os tradutores processam o evento.</span><span class="sxs-lookup"><span data-stu-id="fc094-124">These entries are eventually removed when all translators process the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc094-125">userUri</span><span class="sxs-lookup"><span data-stu-id="fc094-125">userUri</span></span></p></td>
<td><p><span data-ttu-id="fc094-126">nvarchar (255), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="fc094-126">nvarchar(255), not null</span></span></p></td>
<td><p><span data-ttu-id="fc094-127">URI de usuário.</span><span class="sxs-lookup"><span data-stu-id="fc094-127">User URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc094-128">serverID</span><span class="sxs-lookup"><span data-stu-id="fc094-128">serverID</span></span></p></td>
<td><p><span data-ttu-id="fc094-129">int</span><span class="sxs-lookup"><span data-stu-id="fc094-129">int</span></span></p></td>
<td><p><span data-ttu-id="fc094-130">Identidade do servidor (como na tabela tblServerIdentity. ServerId).</span><span class="sxs-lookup"><span data-stu-id="fc094-130">Server identity (as in tblServerIdentity.serverID table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc094-131">Identificação</span><span class="sxs-lookup"><span data-stu-id="fc094-131">sessionId</span></span></p></td>
<td><p><span data-ttu-id="fc094-132">bigint</span><span class="sxs-lookup"><span data-stu-id="fc094-132">bigint</span></span></p></td>
<td><p><span data-ttu-id="fc094-133">Sessão do servidor.</span><span class="sxs-lookup"><span data-stu-id="fc094-133">Server session.</span></span> <span data-ttu-id="fc094-134">Esse é um número aleatório gerado cada vez que um serviço de chat é iniciado.</span><span class="sxs-lookup"><span data-stu-id="fc094-134">This is a random number generated each time a Chat service starts.</span></span> <span data-ttu-id="fc094-135">Ele é usado para diferenciar sessões para fins de identificação de participantes órfãos.</span><span class="sxs-lookup"><span data-stu-id="fc094-135">It is used to differentiate sessions for the purpose of identifying orphaned participants.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="fc094-136">Chave</span><span class="sxs-lookup"><span data-stu-id="fc094-136">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc094-137">Coluna</span><span class="sxs-lookup"><span data-stu-id="fc094-137">Column</span></span></th>
<th><span data-ttu-id="fc094-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc094-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc094-139">&lt;channelUri, userId, joinedAt&gt;</span><span class="sxs-lookup"><span data-stu-id="fc094-139">&lt;channelUri, userId, joinedAt&gt;</span></span></p></td>
<td><p><span data-ttu-id="fc094-140">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="fc094-140">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fc094-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fc094-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

