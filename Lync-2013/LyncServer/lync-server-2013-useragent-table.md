---
title: 'Lync Server 2013: Tabela UserAgent'
description: 'Lync Server 2013: tabela UserAgent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgent table
ms:assetid: d6bda1c0-b053-457a-9ffa-2ae859788775
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398939(v=OCS.15)
ms:contentKeyID: 48185582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b701d8384313d0267dd566e0c32242f6cc077472
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439125"
---
# <a name="useragent-table-in-lync-server-2013"></a><span data-ttu-id="cc928-103">Tabela UserAgent no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cc928-103">UserAgent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cc928-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cc928-104">

<span> </span></span></span>

<span data-ttu-id="cc928-105">_**Tópico da última modificação:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="cc928-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="cc928-106">A tabela UserAgent é uma tabela de suporte que armazena uma lista de vários agentes de usuário que participaram de sessões registradas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cc928-106">The UserAgent table is a supporting table that stores a list of the various user agents that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="cc928-107">Cada registro na tabela representa um agente do usuário</span><span class="sxs-lookup"><span data-stu-id="cc928-107">Each record in the table represents one user agent</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cc928-108"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="cc928-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="cc928-109"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="cc928-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="cc928-110"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="cc928-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="cc928-111"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="cc928-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc928-112"><strong>UserAgentKey</strong></span><span class="sxs-lookup"><span data-stu-id="cc928-112"><strong>UserAgentKey</strong></span></span></p></td>
<td><p><span data-ttu-id="cc928-113">int</span><span class="sxs-lookup"><span data-stu-id="cc928-113">int</span></span></p></td>
<td><p><span data-ttu-id="cc928-114">Primária</span><span class="sxs-lookup"><span data-stu-id="cc928-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="cc928-115">Número exclusivo que identifica esse agente de usuário.</span><span class="sxs-lookup"><span data-stu-id="cc928-115">Unique number identifying this user agent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc928-116"><strong>UserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="cc928-116"><strong>UserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="cc928-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cc928-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cc928-118">Exclusividade</span><span class="sxs-lookup"><span data-stu-id="cc928-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="cc928-119">Cadeia de caracteres do agente do usuário.</span><span class="sxs-lookup"><span data-stu-id="cc928-119">User Agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc928-120"><strong>UAType</strong></span><span class="sxs-lookup"><span data-stu-id="cc928-120"><strong>UAType</strong></span></span></p></td>
<td><p><span data-ttu-id="cc928-121">smallint</span><span class="sxs-lookup"><span data-stu-id="cc928-121">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="cc928-122">1 é o servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="cc928-122">1 is Mediation Server.</span></span></p>
<p><span data-ttu-id="cc928-123">2 é um servidor de conferência A/V.</span><span class="sxs-lookup"><span data-stu-id="cc928-123">2 is A/V Conferencing Server.</span></span></p>
<p><span data-ttu-id="cc928-124">4 é o Lync.</span><span class="sxs-lookup"><span data-stu-id="cc928-124">4 is Lync.</span></span></p>
<p><span data-ttu-id="cc928-125">8 é o telefone IP.</span><span class="sxs-lookup"><span data-stu-id="cc928-125">8 is IP Phone.</span></span></p>
<p><span data-ttu-id="cc928-126">16 é o console do Live Meeting.</span><span class="sxs-lookup"><span data-stu-id="cc928-126">16 is Live Meeting Console.</span></span></p>
<p><span data-ttu-id="cc928-127">o 32 é uma ferramenta de validação de implantação (DVT).</span><span class="sxs-lookup"><span data-stu-id="cc928-127">32 is Deployment Validation Tool (DVT).</span></span></p>
<p><span data-ttu-id="cc928-128">o 64 é o Lync em computadores Macintosh.</span><span class="sxs-lookup"><span data-stu-id="cc928-128">64 is Lync on Macintosh computers.</span></span></p>
<p><span data-ttu-id="cc928-129">o 128 é o Office Communications Server 2007 R2 Attendant.</span><span class="sxs-lookup"><span data-stu-id="cc928-129">128 is Office Communications Server 2007 R2 Attendant.</span></span></p>
<p><span data-ttu-id="cc928-130">o 256 é o serviço de anúncio de conferências.</span><span class="sxs-lookup"><span data-stu-id="cc928-130">256 is Conferencing Announcement service.</span></span></p>
<p><span data-ttu-id="cc928-131">o 512 é o atendedor automático da conferência.</span><span class="sxs-lookup"><span data-stu-id="cc928-131">512 is Conferencing Auto Attendant.</span></span></p>
<p><span data-ttu-id="cc928-132">o 1024 é um aplicativo de grupo de resposta.</span><span class="sxs-lookup"><span data-stu-id="cc928-132">1024 is Response Group application.</span></span></p>
<p><span data-ttu-id="cc928-133">2048 está fora do controle de voz.</span><span class="sxs-lookup"><span data-stu-id="cc928-133">2048 is Outside Voice Control.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cc928-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cc928-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

