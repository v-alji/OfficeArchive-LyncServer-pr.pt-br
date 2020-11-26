---
title: 'Lync Server 2013: Tabela Endpoint'
description: 'Lync Server 2013: tabela de pontos de extremidade.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Endpoint table
ms:assetid: 500f330d-4d7d-4e88-b1cc-fef9a9de6b5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398327(v=OCS.15)
ms:contentKeyID: 48184098
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 614872eee41b5d8e56da4b96cf5bbe3a4a1cf4d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428675"
---
# <a name="endpoint-table-in-lync-server-2013"></a><span data-ttu-id="f9c77-103">Tabela Endpoint no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9c77-103">Endpoint table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f9c77-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f9c77-104">

<span> </span></span></span>

<span data-ttu-id="f9c77-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="f9c77-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="f9c77-106">A tabela de pontos de extremidade é uma tabela de suporte que armazena informações sobre os pontos de extremidade que participaram em sessões registradas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9c77-106">The Endpoint table is a supporting table that stores information about the endpoints that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="f9c77-107">Cada registro na tabela representa um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f9c77-107">Each record in the table represents one endpoint.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9c77-108"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="f9c77-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="f9c77-109"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="f9c77-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="f9c77-110"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="f9c77-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="f9c77-111"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="f9c77-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9c77-112"><strong>EndpointKey</strong></span><span class="sxs-lookup"><span data-stu-id="f9c77-112"><strong>EndpointKey</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c77-113">int</span><span class="sxs-lookup"><span data-stu-id="f9c77-113">int</span></span></p></td>
<td><p><span data-ttu-id="f9c77-114">Primária</span><span class="sxs-lookup"><span data-stu-id="f9c77-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="f9c77-115">Número exclusivo que identifica esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f9c77-115">Unique number identifying this endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c77-116"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="f9c77-116"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c77-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="f9c77-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f9c77-118">Exclusividade</span><span class="sxs-lookup"><span data-stu-id="f9c77-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="f9c77-119">Nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f9c77-119">Endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c77-120"><strong>Sistema operacional</strong></span><span class="sxs-lookup"><span data-stu-id="f9c77-120"><strong>OS</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c77-121">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="f9c77-121">nvarchar(128)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f9c77-122">Sistema operacional (SO) da empresa.</span><span class="sxs-lookup"><span data-stu-id="f9c77-122">Operating system (OS) of the endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c77-123"><strong>CPUName</strong></span><span class="sxs-lookup"><span data-stu-id="f9c77-123"><strong>CPUName</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c77-124">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="f9c77-124">nvarchar(128)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f9c77-125">Nome da CPU do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f9c77-125">CPU name of the endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c77-126"><strong>CPUNumberOfCores</strong></span><span class="sxs-lookup"><span data-stu-id="f9c77-126"><strong>CPUNumberOfCores</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c77-127">smallint</span><span class="sxs-lookup"><span data-stu-id="f9c77-127">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f9c77-128">Número de núcleos da CPU da empresa.</span><span class="sxs-lookup"><span data-stu-id="f9c77-128">Number of CPU cores of the endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c77-129"><strong>CPUProcessorSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="f9c77-129"><strong>CPUProcessorSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c77-130">int</span><span class="sxs-lookup"><span data-stu-id="f9c77-130">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f9c77-131">Velocidade do processador da CPU do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f9c77-131">CPU processor speed of the endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c77-132"><strong>VirtualizationFlag</strong></span><span class="sxs-lookup"><span data-stu-id="f9c77-132"><strong>VirtualizationFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c77-133">tinyint</span><span class="sxs-lookup"><span data-stu-id="f9c77-133">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f9c77-134">Sinalizador de bit que indica se o sistema está em execução em um ambiente virtualizado:</span><span class="sxs-lookup"><span data-stu-id="f9c77-134">Bit flag that indicates if the system is running in a virtualized environment:</span></span></p>
<ul>
<li><p><span data-ttu-id="f9c77-135">0x0000 – nenhum</span><span class="sxs-lookup"><span data-stu-id="f9c77-135">0x0000 – None</span></span></p></li>
<li><p><span data-ttu-id="f9c77-136">0x0001 – HyperV</span><span class="sxs-lookup"><span data-stu-id="f9c77-136">0x0001 – HyperV</span></span></p></li>
<li><p><span data-ttu-id="f9c77-137">0x0002 – VMWare</span><span class="sxs-lookup"><span data-stu-id="f9c77-137">0x0002 – VMWare</span></span></p></li>
<li><p><span data-ttu-id="f9c77-138">0x0004 – Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f9c77-138">0x0004 – Virtual PC</span></span></p></li>
<li><p><span data-ttu-id="f9c77-139">0x0008 – computador Xen</span><span class="sxs-lookup"><span data-stu-id="f9c77-139">0x0008 – Xen PC</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="f9c77-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f9c77-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

