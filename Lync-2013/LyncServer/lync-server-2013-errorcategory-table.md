---
title: 'Lync Server 2013: tabela ErrorCategory'
description: 'Lync Server 2013: ErrorCategory Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorCategory table
ms:assetid: 0fde3b73-9a2f-44dd-b8dc-6df512303ff1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204675(v=OCS.15)
ms:contentKeyID: 48183425
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8154c73f33b5dad62a338335a960553cfc06ec13
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428563"
---
# <a name="errorcategory-table-in-lync-server-2013"></a><span data-ttu-id="9fc4f-103">Tabela ErrorCategory no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9fc4f-103">ErrorCategory table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9fc4f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9fc4f-104">

<span> </span></span></span>

<span data-ttu-id="9fc4f-105">_**Tópico da última modificação:** 2012-08-20_</span><span class="sxs-lookup"><span data-stu-id="9fc4f-105">_**Topic Last Modified:** 2012-08-20_</span></span>

<span data-ttu-id="9fc4f-106">A tabela ErrorCategory contém o nome amigável para cada classificação de diagnóstico do Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9fc4f-106">The ErrorCategory table contains the friendly name for each Microsoft Lync Server 2013 diagnostic classification.</span></span> <span data-ttu-id="9fc4f-107">Por padrão, o Lync Server 2013 usa as seguintes classificações:</span><span class="sxs-lookup"><span data-stu-id="9fc4f-107">By default, Lync Server 2013 uses the following classifications:</span></span>

  - <span data-ttu-id="9fc4f-108">0--sucesso</span><span class="sxs-lookup"><span data-stu-id="9fc4f-108">0 -- Success</span></span>

  - <span data-ttu-id="9fc4f-109">1--falha prevista</span><span class="sxs-lookup"><span data-stu-id="9fc4f-109">1 -- Expected failure</span></span>

  - <span data-ttu-id="9fc4f-110">2 – falha inesperada</span><span class="sxs-lookup"><span data-stu-id="9fc4f-110">2 – Unexpected failure</span></span>

<span data-ttu-id="9fc4f-111">Esta tabela foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9fc4f-111">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9fc4f-112">Coluna</span><span class="sxs-lookup"><span data-stu-id="9fc4f-112">Column</span></span></th>
<th><span data-ttu-id="9fc4f-113">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9fc4f-113">Data Type</span></span></th>
<th><span data-ttu-id="9fc4f-114">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="9fc4f-114">Key/Index</span></span></th>
<th><span data-ttu-id="9fc4f-115">Detalhes</span><span class="sxs-lookup"><span data-stu-id="9fc4f-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9fc4f-116"><strong>CódigoDaCategoria</strong></span><span class="sxs-lookup"><span data-stu-id="9fc4f-116"><strong>CategoryId</strong></span></span></p></td>
<td><p><span data-ttu-id="9fc4f-117">tinyint</span><span class="sxs-lookup"><span data-stu-id="9fc4f-117">tinyint</span></span></p></td>
<td><p><span data-ttu-id="9fc4f-118">Primária</span><span class="sxs-lookup"><span data-stu-id="9fc4f-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="9fc4f-119">Identificador exclusivo da classificação.</span><span class="sxs-lookup"><span data-stu-id="9fc4f-119">Unique identifier for the classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fc4f-120"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="9fc4f-120"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="9fc4f-121">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9fc4f-121">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9fc4f-122">Valor e nome amigável atribuídos à classificação.</span><span class="sxs-lookup"><span data-stu-id="9fc4f-122">Value and friendly name assigned to the classification.</span></span> <span data-ttu-id="9fc4f-123">Os valores permitidos são:</span><span class="sxs-lookup"><span data-stu-id="9fc4f-123">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="9fc4f-124">0--sucesso</span><span class="sxs-lookup"><span data-stu-id="9fc4f-124">0 -- Success</span></span></p></li>
<li><p><span data-ttu-id="9fc4f-125">1--falha prevista</span><span class="sxs-lookup"><span data-stu-id="9fc4f-125">1 -- Expected failure</span></span></p></li>
<li><p><span data-ttu-id="9fc4f-126">2 – falha inesperada</span><span class="sxs-lookup"><span data-stu-id="9fc4f-126">2 – Unexpected failure</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="9fc4f-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9fc4f-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

