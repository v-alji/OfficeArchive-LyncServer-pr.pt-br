---
title: 'Lync Server 2013: tabela TraceRoute'
description: 'Lync Server 2013: tabela TraceRoute.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: TraceRoute table
ms:assetid: b9493cef-6ece-4f13-bf68-dbf132aab4f4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205205(v=OCS.15)
ms:contentKeyID: 48185242
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af33e572065fbab1eaaaef684997e7f95edaed9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440833"
---
# <a name="traceroute-table-in-lync-server-2013"></a><span data-ttu-id="532ea-103">Tabela TraceRoute no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="532ea-103">TraceRoute table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="532ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="532ea-104">

<span> </span></span></span>

<span data-ttu-id="532ea-105">_**Tópico da última modificação:** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="532ea-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="532ea-106">A tabela TraceRoute contém informações de roteamento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="532ea-106">The TraceRoute table contains routing information from calls.</span></span> <span data-ttu-id="532ea-107">Esta tabela foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="532ea-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="532ea-108"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="532ea-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="532ea-109"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="532ea-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="532ea-110"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="532ea-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="532ea-111"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="532ea-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="532ea-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="532ea-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="532ea-113">datetime</span><span class="sxs-lookup"><span data-stu-id="532ea-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="532ea-114">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="532ea-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="532ea-115">Data e hora em que a chamada começou.</span><span class="sxs-lookup"><span data-stu-id="532ea-115">Date and time that the call began.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="532ea-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="532ea-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="532ea-117">int</span><span class="sxs-lookup"><span data-stu-id="532ea-117">int</span></span></p></td>
<td><p><span data-ttu-id="532ea-118">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="532ea-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="532ea-119">Identificador exclusivo usado para distinguir entre várias chamadas que podem ter começado na mesma data e ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="532ea-119">Unique identifier used to distinguish between multiple calls that might have begun on the same date and at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="532ea-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="532ea-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="532ea-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="532ea-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="532ea-122">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="532ea-122">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="532ea-123">Representa o tipo de linha de vídeo usado na chamada.</span><span class="sxs-lookup"><span data-stu-id="532ea-123">Represents the type of video line used in the call.</span></span> <span data-ttu-id="532ea-124">Os valores permitidos são:</span><span class="sxs-lookup"><span data-stu-id="532ea-124">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="532ea-125">0 – áudio</span><span class="sxs-lookup"><span data-stu-id="532ea-125">0 – Audio</span></span></p></li>
<li><p><span data-ttu-id="532ea-126">1 – vídeo</span><span class="sxs-lookup"><span data-stu-id="532ea-126">1 – Video</span></span></p></li>
<li><p><span data-ttu-id="532ea-127">2 – vídeo panorâmico</span><span class="sxs-lookup"><span data-stu-id="532ea-127">2 – Panoramic video</span></span></p></li>
<li><p><span data-ttu-id="532ea-128">3 – compartilhamento de aplicativos/área de trabalho</span><span class="sxs-lookup"><span data-stu-id="532ea-128">3 – Application/Desktop sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="532ea-129"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="532ea-129"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="532ea-130">bit</span><span class="sxs-lookup"><span data-stu-id="532ea-130">bit</span></span></p></td>
<td><p><span data-ttu-id="532ea-131">Primária</span><span class="sxs-lookup"><span data-stu-id="532ea-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="532ea-132">Ponto de extremidade que fez a chamada.</span><span class="sxs-lookup"><span data-stu-id="532ea-132">Endpoint that placed the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="532ea-133"><strong>Hop</strong></span><span class="sxs-lookup"><span data-stu-id="532ea-133"><strong>Hop</strong></span></span></p></td>
<td><p><span data-ttu-id="532ea-134">int</span><span class="sxs-lookup"><span data-stu-id="532ea-134">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="532ea-135">Salto de rede/</span><span class="sxs-lookup"><span data-stu-id="532ea-135">Network hop/</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="532ea-136"><strong>IPAddressKey</strong></span><span class="sxs-lookup"><span data-stu-id="532ea-136"><strong>IPAddressKey</strong></span></span></p></td>
<td><p><span data-ttu-id="532ea-137">int</span><span class="sxs-lookup"><span data-stu-id="532ea-137">int</span></span></p></td>
<td><p><span data-ttu-id="532ea-138">Exterior</span><span class="sxs-lookup"><span data-stu-id="532ea-138">Foreign</span></span></p></td>
<td><p><span data-ttu-id="532ea-139">Identificador exclusivo do endereço IP.</span><span class="sxs-lookup"><span data-stu-id="532ea-139">Unique identifier for the IP address.</span></span> <span data-ttu-id="532ea-140">As informações de endereço IP são armazenadas na <a href="lync-server-2013-ipaddress-table.md">tabela IPAddress no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="532ea-140">IP address information is stored in the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="532ea-141"><strong>RESPOSTA</strong></span><span class="sxs-lookup"><span data-stu-id="532ea-141"><strong>RTT</strong></span></span></p></td>
<td><p><span data-ttu-id="532ea-142">int</span><span class="sxs-lookup"><span data-stu-id="532ea-142">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="532ea-143">Tempo de resposta.</span><span class="sxs-lookup"><span data-stu-id="532ea-143">Roundtrip time.</span></span> <span data-ttu-id="532ea-144">O tempo de resposta mede a quantidade de tempo que leva para um pacote de voz alcançar seu destino e enviar notificações de volta para que ele seja recebido.</span><span class="sxs-lookup"><span data-stu-id="532ea-144">The roundtrip time measures the amount of time it takes for a voice packet to reach its destination and then send back notification that it was received.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="532ea-145">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="532ea-145">


</div>

<span> </span>

</div>

</div>

</span></span></div>

