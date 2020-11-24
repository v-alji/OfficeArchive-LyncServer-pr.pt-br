---
title: 'Lync Server 2013: Tabela Locations'
description: 'Lync Server 2013: tabela locais.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Locations table
ms:assetid: 78dc1b14-5394-4f8e-89d3-4ba593272a04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398596(v=OCS.15)
ms:contentKeyID: 48184579
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9d07b6d3d3820f4efb3310adf0734a7e10c53e6d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390333"
---
# <a name="locations-table-in-lync-server-2013"></a><span data-ttu-id="e952a-103">Tabela Locations no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e952a-103">Locations table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e952a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e952a-104">

<span> </span></span></span>

<span data-ttu-id="e952a-105">_**Tópico da última modificação:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="e952a-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="e952a-106">Cada registro representa uma referência de localização em uma chamada de emergência, como uma chamada E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="e952a-106">Each record represents one location reference in an emergency call, like an E9-1-1 call.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e952a-107">Coluna</span><span class="sxs-lookup"><span data-stu-id="e952a-107">Column</span></span></th>
<th><span data-ttu-id="e952a-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e952a-108">Data Type</span></span></th>
<th><span data-ttu-id="e952a-109">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="e952a-109">Key/Index</span></span></th>
<th><span data-ttu-id="e952a-110">Detalhes</span><span class="sxs-lookup"><span data-stu-id="e952a-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e952a-111"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="e952a-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e952a-112">datetime</span><span class="sxs-lookup"><span data-stu-id="e952a-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="e952a-113">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="e952a-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="e952a-114">Tempo de solicitação de sessão.</span><span class="sxs-lookup"><span data-stu-id="e952a-114">Time of session request.</span></span> <span data-ttu-id="e952a-115">Usado em conjunto com o <strong>SessionIdSeq</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="e952a-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="e952a-116">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e952a-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e952a-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e952a-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e952a-118">int</span><span class="sxs-lookup"><span data-stu-id="e952a-118">int</span></span></p></td>
<td><p><span data-ttu-id="e952a-119">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="e952a-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="e952a-120">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="e952a-120">ID number to identify the session.</span></span> <span data-ttu-id="e952a-121">Usado em conjunto com a <strong>identificação_da_sessãotime</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="e952a-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="e952a-122">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e952a-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e952a-123"><strong>Local</strong></span><span class="sxs-lookup"><span data-stu-id="e952a-123"><strong>Location</strong></span></span></p></td>
<td><p><span data-ttu-id="e952a-124">nvarchar (max)</span><span class="sxs-lookup"><span data-stu-id="e952a-124">nvarchar(max)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e952a-125">Local de chamada de emergência.</span><span class="sxs-lookup"><span data-stu-id="e952a-125">Location of emergency call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e952a-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e952a-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

