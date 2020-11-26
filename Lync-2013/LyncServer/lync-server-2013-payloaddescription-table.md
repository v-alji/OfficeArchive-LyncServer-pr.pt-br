---
title: 'Lync Server 2013: Tabela PayloadDescription'
description: 'Lync Server 2013: PayloadDescription Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PayloadDescription table
ms:assetid: c49d61c0-305a-4770-a5d2-5d9f05decc6d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412971(v=OCS.15)
ms:contentKeyID: 48185353
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 90ba6b3b85060601487b5b6d0d8747c5fbfa2a9a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445047"
---
# <a name="payloaddescription-table-in-lync-server-2013"></a><span data-ttu-id="818f8-103">Tabela PayloadDescription no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="818f8-103">PayloadDescription table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="818f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="818f8-104">

<span> </span></span></span>

<span data-ttu-id="818f8-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="818f8-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="818f8-106">A tabela PayloadDescription é uma tabela de suporte.</span><span class="sxs-lookup"><span data-stu-id="818f8-106">The PayloadDescription table is a supporting table.</span></span> <span data-ttu-id="818f8-107">Cada registro representa um codec, que é usado em uma sessão de áudio ou de vídeo.</span><span class="sxs-lookup"><span data-stu-id="818f8-107">Each record represents one Codec, which is used in an audio or video session.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="818f8-108"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="818f8-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="818f8-109"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="818f8-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="818f8-110"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="818f8-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="818f8-111"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="818f8-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="818f8-112"><strong>PayloadDescriptionKey</strong></span><span class="sxs-lookup"><span data-stu-id="818f8-112"><strong>PayloadDescriptionKey</strong></span></span></p></td>
<td><p><span data-ttu-id="818f8-113">int</span><span class="sxs-lookup"><span data-stu-id="818f8-113">int</span></span></p></td>
<td><p><span data-ttu-id="818f8-114">Primária</span><span class="sxs-lookup"><span data-stu-id="818f8-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="818f8-115">Número exclusivo que identifica o codec.</span><span class="sxs-lookup"><span data-stu-id="818f8-115">Unique number identifying the Codec.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="818f8-116"><strong>PayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="818f8-116"><strong>PayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="818f8-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="818f8-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="818f8-118">Exclusividade</span><span class="sxs-lookup"><span data-stu-id="818f8-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="818f8-119">Nome do codec.</span><span class="sxs-lookup"><span data-stu-id="818f8-119">Codec name.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="818f8-120">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="818f8-120">


</div>

<span> </span>

</div>

</div>

</span></span></div>

