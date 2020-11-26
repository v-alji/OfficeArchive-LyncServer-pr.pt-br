---
title: 'Lync Server 2013: Tabela MediaList'
description: 'Lync Server 2013: tabela Medialist.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaList table
ms:assetid: 1f440590-c1bc-483e-b7bc-6cc763847768
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398279(v=OCS.15)
ms:contentKeyID: 48183579
ms.date: 07/12/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e54535cd4a081657e7dcd59446cf65aaa3af7cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445922"
---
# <a name="medialist-table-in-lync-server-2013"></a><span data-ttu-id="ed804-103">Tabela MediaList no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ed804-103">MediaList table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ed804-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ed804-104">

<span> </span></span></span>

<span data-ttu-id="ed804-105">_**Tópico da última modificação:** 2016-07-12_</span><span class="sxs-lookup"><span data-stu-id="ed804-105">_**Topic Last Modified:** 2016-07-12_</span></span>

<span data-ttu-id="ed804-106">MediaList é uma tabela estática que armazena a lista de vários tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="ed804-106">The MediaList table is a static table that stores the list of various media types.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed804-107">Coluna</span><span class="sxs-lookup"><span data-stu-id="ed804-107">Column</span></span></th>
<th><span data-ttu-id="ed804-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ed804-108">Data Type</span></span></th>
<th><span data-ttu-id="ed804-109">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="ed804-109">Key/Index</span></span></th>
<th><span data-ttu-id="ed804-110">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ed804-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed804-111"><strong>MediaId</strong></span><span class="sxs-lookup"><span data-stu-id="ed804-111"><strong>MediaId</strong></span></span></p></td>
<td><p><span data-ttu-id="ed804-112">tinyint</span><span class="sxs-lookup"><span data-stu-id="ed804-112">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ed804-113">Primária</span><span class="sxs-lookup"><span data-stu-id="ed804-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="ed804-114">Valores: 1-7</span><span class="sxs-lookup"><span data-stu-id="ed804-114">Values: 1-7</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed804-115"><strong>Media</strong></span><span class="sxs-lookup"><span data-stu-id="ed804-115"><strong>Media</strong></span></span></p></td>
<td><p><span data-ttu-id="ed804-116">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ed804-116">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ed804-117">Mapeamento estático dos valores de MediaID e Media:</span><span class="sxs-lookup"><span data-stu-id="ed804-117">Static mapping of MediaID and Media values:</span></span></p>
<ul>
<li><p><span data-ttu-id="ed804-118">1 – MENSAGEM INSTANTÂNEA</span><span class="sxs-lookup"><span data-stu-id="ed804-118">1 – IM</span></span></p></li>
<li><p><span data-ttu-id="ed804-119">2 – Transferência de arquivo</span><span class="sxs-lookup"><span data-stu-id="ed804-119">2 – File Transfer</span></span></p></li>
<li><p><span data-ttu-id="ed804-120">3 – Assistência remota</span><span class="sxs-lookup"><span data-stu-id="ed804-120">3 – Remote Assistance</span></span></p></li>
<li><p><span data-ttu-id="ed804-121">4 – Compartilhamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="ed804-121">4 – Application Sharing</span></span></p></li>
<li><p><span data-ttu-id="ed804-122">5 – áudio</span><span class="sxs-lookup"><span data-stu-id="ed804-122">5 – Audio</span></span></p></li>
<li><p><span data-ttu-id="ed804-123">6 – vídeo</span><span class="sxs-lookup"><span data-stu-id="ed804-123">6 – Video</span></span></p></li>
<li><p><span data-ttu-id="ed804-124">7 – Convite do aplicativo</span><span class="sxs-lookup"><span data-stu-id="ed804-124">7 – App Invite</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ed804-125">Se você está tentando determinar o tipo de modalidade dos valores em LcsCDR.SessionDetailsView.MediaTypes, use o seguinte snippet Join: </span><span class="sxs-lookup"><span data-stu-id="ed804-125">If you are trying to determine the modality type for the values in LcsCDR.SessionDetailsView.MediaTypes, then you need to use the following Join snippet:</span></span>

    LEFT JOIN on Media.MediaId = MediaList.MediaId

<span data-ttu-id="ed804-126"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ed804-126"></div>

<span> </span>

</div>

</div>

</span></span></div>

