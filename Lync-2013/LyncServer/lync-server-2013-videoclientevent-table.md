---
title: 'Lync Server 2013: Tabela VideoClientEvent'
description: 'Lync Server 2013: VideoClientEvent Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoClientEvent table
ms:assetid: e8ab963b-fe1d-45b3-b9bd-66a5f44c1629
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399039(v=OCS.15)
ms:contentKeyID: 48185891
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae73ac2548e838241febe60a2d31f80983b01de5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390388"
---
# <a name="videoclientevent-table-in-lync-server-2013"></a><span data-ttu-id="b20b1-103">Tabela VideoClientEvent no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b20b1-103">VideoClientEvent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b20b1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b20b1-104">

<span> </span></span></span>

<span data-ttu-id="b20b1-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="b20b1-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="b20b1-106">Cada registro contém um evento de cliente para um ponto de extremidade em uma chamada com vídeo.</span><span class="sxs-lookup"><span data-stu-id="b20b1-106">Each record contains client event for one endpoint in a video call.</span></span> <span data-ttu-id="b20b1-107">Geralmente, uma chamada tem dois registros, um para o chamador e outro para o receptor.</span><span class="sxs-lookup"><span data-stu-id="b20b1-107">Usually, one call has two records, one for caller and one for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b20b1-108"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="b20b1-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="b20b1-109"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="b20b1-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="b20b1-110"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="b20b1-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="b20b1-111"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="b20b1-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b20b1-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="b20b1-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b20b1-113">datetime</span><span class="sxs-lookup"><span data-stu-id="b20b1-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="b20b1-114">Primária</span><span class="sxs-lookup"><span data-stu-id="b20b1-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="b20b1-115">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="b20b1-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20b1-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="b20b1-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="b20b1-117">int</span><span class="sxs-lookup"><span data-stu-id="b20b1-117">int</span></span></p></td>
<td><p><span data-ttu-id="b20b1-118">Primária</span><span class="sxs-lookup"><span data-stu-id="b20b1-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="b20b1-119">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="b20b1-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20b1-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="b20b1-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="b20b1-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="b20b1-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="b20b1-122">Primária</span><span class="sxs-lookup"><span data-stu-id="b20b1-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="b20b1-123">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="b20b1-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20b1-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="b20b1-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="b20b1-125">bit</span><span class="sxs-lookup"><span data-stu-id="b20b1-125">bit</span></span></p></td>
<td><p><span data-ttu-id="b20b1-126">Primária</span><span class="sxs-lookup"><span data-stu-id="b20b1-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="b20b1-127">0: dados do chamador</span><span class="sxs-lookup"><span data-stu-id="b20b1-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="b20b1-128">1: dados do chamador</span><span class="sxs-lookup"><span data-stu-id="b20b1-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b20b1-129"><strong>NetworkBandwidthLowEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="b20b1-129"><strong>NetworkBandwidthLowEventRatio</strong></span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b20b1-130">Porcentagem da sessão o evento LowBandwidth foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="b20b1-130">Percentage of session the LowBandwidth event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="b20b1-131">A largura de banda disponível é insuficiente para uma experiência de voz aceitável.</span><span class="sxs-lookup"><span data-stu-id="b20b1-131">The available bandwidth is insufficient for an acceptable voice experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b20b1-132"><strong>NetworkReceiveQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="b20b1-132"><strong>NetworkReceiveQualityEventRatio</strong></span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b20b1-133">Porcentagem da sessão o evento ReceiveSendQuality foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="b20b1-133">Percentage of session the ReceiveSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="b20b1-134">A qualidade da rede em termos de tremulação ou perda de pacote é severa e afeta a qualidade do áudio sendo recebido.</span><span class="sxs-lookup"><span data-stu-id="b20b1-134">Network quality in terms of jitter or packet loss is severe and impacts the quality of audio being received.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b20b1-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b20b1-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

