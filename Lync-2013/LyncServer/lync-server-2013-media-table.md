---
title: 'Lync Server 2013: Tabela Media'
description: 'Lync Server 2013: tabela de mídia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media table
ms:assetid: 1e1b427f-59b5-4564-bde5-1002a80439ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398268(v=OCS.15)
ms:contentKeyID: 48183568
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31e30d1f91c59b8e3aa7915fc0d513618d0f709f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425672"
---
# <a name="media-table-in-lync-server-2013"></a><span data-ttu-id="6e6bd-103">Tabela Media no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6e6bd-103">Media table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6e6bd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6e6bd-104">

<span> </span></span></span>

<span data-ttu-id="6e6bd-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="6e6bd-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="6e6bd-106">Cada registro representa um tipo de mídia usado em uma sessão ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-106">Each record represents one media type used in a peer-to-peer session.</span></span> <span data-ttu-id="6e6bd-107">Uma sessão seria representada por vários registros na tabela, se mais de um tipo de mídia for usado.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-107">One session would be represented by multiple records in the table, if more than one media type is used.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6e6bd-108">A tabela de mídia não deve ser usada para calcular a duração da mídia de uma sessão.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-108">The Media table should not be used to calculate the media duration for a session.</span></span> <span data-ttu-id="6e6bd-109">Esta tabela contém os detalhes de sinalização da troca de mídia em uma sessão.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-109">This table contains the signaling details of media exchange in a session.</span></span> <span data-ttu-id="6e6bd-110">A troca de mídia é feita pela solicitação de convite e StartTime indica a hora em que o convite foi enviado. O tempo de convite não necessariamente significa a hora de início da mídia porque a mídia só inicia depois que a sessão aceita a sessão.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-110">Media exchange is done by the INVITE request, and StartTime indicates the time that the INVITE was sent out. The invite time does not necessarily mean the media start time, because media starts only after the sessionee accepts the session.</span></span> <span data-ttu-id="6e6bd-111">A EndTime geralmente significa a hora de término desta sessão.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-111">The EndTime usually means the end time of this session.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6e6bd-112">Coluna</span><span class="sxs-lookup"><span data-stu-id="6e6bd-112">Column</span></span></th>
<th><span data-ttu-id="6e6bd-113">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6e6bd-113">Data Type</span></span></th>
<th><span data-ttu-id="6e6bd-114">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="6e6bd-114">Key/Index</span></span></th>
<th><span data-ttu-id="6e6bd-115">Detalhes</span><span class="sxs-lookup"><span data-stu-id="6e6bd-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e6bd-116"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="6e6bd-116"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6e6bd-117">datetime</span><span class="sxs-lookup"><span data-stu-id="6e6bd-117">datetime</span></span></p></td>
<td><p><span data-ttu-id="6e6bd-118">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="6e6bd-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="6e6bd-119">Tempo de solicitação de sessão.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-119">Time of session request.</span></span> <span data-ttu-id="6e6bd-120">Usado em conjunto com o <strong>SessionIdSeq</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-120">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="6e6bd-121">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e6bd-122"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="6e6bd-122"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="6e6bd-123">int</span><span class="sxs-lookup"><span data-stu-id="6e6bd-123">int</span></span></p></td>
<td><p><span data-ttu-id="6e6bd-124">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="6e6bd-124">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="6e6bd-125">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-125">ID number to identify the session.</span></span> <span data-ttu-id="6e6bd-126">Usado em conjunto com a <strong>identificação_da_sessãotime</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-126">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="6e6bd-127">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-127">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e6bd-128"><strong>MediaId</strong></span><span class="sxs-lookup"><span data-stu-id="6e6bd-128"><strong>MediaId</strong></span></span></p></td>
<td><p><span data-ttu-id="6e6bd-129">tinyint</span><span class="sxs-lookup"><span data-stu-id="6e6bd-129">tinyint</span></span></p></td>
<td><p><span data-ttu-id="6e6bd-130">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="6e6bd-130">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="6e6bd-131">Número exclusivo que identifica esse tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-131">Unique number identifying this media type.</span></span> <span data-ttu-id="6e6bd-132">Consulte a <a href="lync-server-2013-medialist-table.md">tabela medialist no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-132">See the <a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e6bd-133"><strong>StartTime </strong></span><span class="sxs-lookup"><span data-stu-id="6e6bd-133"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6e6bd-134">datetime</span><span class="sxs-lookup"><span data-stu-id="6e6bd-134">datetime</span></span></p></td>
<td><p><span data-ttu-id="6e6bd-135">Primária</span><span class="sxs-lookup"><span data-stu-id="6e6bd-135">Primary</span></span></p></td>
<td><p><span data-ttu-id="6e6bd-136">Esta é a hora em que uma solicitação de mídia foi enviada, e não a hora de início da mídia real.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-136">This is the time that a media request was sent out, not the real media start time.</span></span> <span data-ttu-id="6e6bd-137"><strong>StartTime</strong> inclui o tempo de configuração da sessão.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-137"><strong>StartTime</strong> includes the session setup time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e6bd-138"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="6e6bd-138"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6e6bd-139">datetime</span><span class="sxs-lookup"><span data-stu-id="6e6bd-139">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6e6bd-140">Esta é a hora de término da sessão.</span><span class="sxs-lookup"><span data-stu-id="6e6bd-140">This is the end time of the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6e6bd-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6e6bd-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

