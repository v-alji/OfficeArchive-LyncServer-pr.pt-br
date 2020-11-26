---
title: 'Lync Server 2013: Escalabilidade'
description: Redimensionamento do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scalability
ms:assetid: 46fa0cb5-1507-4a12-ad3f-ba64585e2dc4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg417160(v=OCS.15)
ms:contentKeyID: 48183995
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28cd5820755ffd1eb863ed6f2369b5756a7ae3f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442114"
---
# <a name="scalability-with-lync-server-2013"></a><span data-ttu-id="d9432-103">Escalabilidade com Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d9432-103">Scalability with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d9432-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d9432-104">

<span> </span></span></span>

<span data-ttu-id="d9432-105">_**Tópico da última modificação:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="d9432-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="d9432-106">O Lync Server é oferecido em duas edições, Enterprise Edition e Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="d9432-106">Lync Server is offered in two editions, Enterprise Edition and Standard Edition.</span></span> <span data-ttu-id="d9432-107">As diferentes edições são direcionadas principalmente para diferentes tamanhos de organizações.</span><span class="sxs-lookup"><span data-stu-id="d9432-107">The different editions are intended primarily for different sizes of organizations.</span></span> <span data-ttu-id="d9432-108">Conforme mostrado na tabela a seguir, ambas as edições dão suporte a toda a funcionalidade em todas as cargas de trabalho, exceto para alta disponibilidade e recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="d9432-108">As shown in the following table, both editions support all functionality in all workloads, except for high availability and disaster recovery.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9432-109">Recurso</span><span class="sxs-lookup"><span data-stu-id="d9432-109">Feature</span></span></th>
<th><span data-ttu-id="d9432-110">Tem suporte na Enterprise Edition?</span><span class="sxs-lookup"><span data-stu-id="d9432-110">Supported in Enterprise Edition?</span></span></th>
<th><span data-ttu-id="d9432-111">Compatível com a Standard Edition?</span><span class="sxs-lookup"><span data-stu-id="d9432-111">Supported in Standard Edition?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9432-112">Mensagens instantâneas (IM) e presença</span><span class="sxs-lookup"><span data-stu-id="d9432-112">Instant messaging (IM) and presence</span></span></p></td>
<td><p><span data-ttu-id="d9432-113">Sim</span><span class="sxs-lookup"><span data-stu-id="d9432-113">Yes</span></span></p></td>
<td><p><span data-ttu-id="d9432-114">Sim</span><span class="sxs-lookup"><span data-stu-id="d9432-114">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9432-115">Conferência</span><span class="sxs-lookup"><span data-stu-id="d9432-115">Conferencing</span></span></p></td>
<td><p><span data-ttu-id="d9432-116">Sim</span><span class="sxs-lookup"><span data-stu-id="d9432-116">Yes</span></span></p></td>
<td><p><span data-ttu-id="d9432-117">Sim</span><span class="sxs-lookup"><span data-stu-id="d9432-117">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9432-118">Conferências de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="d9432-118">A/V conferencing</span></span></p></td>
<td><p><span data-ttu-id="d9432-119">Sim</span><span class="sxs-lookup"><span data-stu-id="d9432-119">Yes</span></span></p></td>
<td><p><span data-ttu-id="d9432-120">Sim</span><span class="sxs-lookup"><span data-stu-id="d9432-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9432-121">Conferência discada</span><span class="sxs-lookup"><span data-stu-id="d9432-121">Dial-in conferencing</span></span></p></td>
<td><p><span data-ttu-id="d9432-122">Sim</span><span class="sxs-lookup"><span data-stu-id="d9432-122">Yes</span></span></p></td>
<td><p><span data-ttu-id="d9432-123">Sim</span><span class="sxs-lookup"><span data-stu-id="d9432-123">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9432-124">Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="d9432-124">Enterprise Voice</span></span></p></td>
<td><p><span data-ttu-id="d9432-125">Sim</span><span class="sxs-lookup"><span data-stu-id="d9432-125">Yes</span></span></p></td>
<td><p><span data-ttu-id="d9432-126">Sim</span><span class="sxs-lookup"><span data-stu-id="d9432-126">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9432-127">Visualização</span><span class="sxs-lookup"><span data-stu-id="d9432-127">Virtualization</span></span></p></td>
<td><p><span data-ttu-id="d9432-128">Sim</span><span class="sxs-lookup"><span data-stu-id="d9432-128">Yes</span></span></p></td>
<td><p><span data-ttu-id="d9432-129">Sim</span><span class="sxs-lookup"><span data-stu-id="d9432-129">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9432-130">Alta disponibilidade, failover e recuperação de desastres</span><span class="sxs-lookup"><span data-stu-id="d9432-130">High availability, failover, and disaster recovery</span></span></p></td>
<td><p><span data-ttu-id="d9432-131">Sim</span><span class="sxs-lookup"><span data-stu-id="d9432-131">Yes</span></span></p></td>
<td><p><span data-ttu-id="d9432-132">Não</span><span class="sxs-lookup"><span data-stu-id="d9432-132">No</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d9432-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d9432-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

