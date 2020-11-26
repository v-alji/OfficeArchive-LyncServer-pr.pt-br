---
title: 'Lync Server 2013: tblEnumValue'
description: 'Lync Server 2013: tblEnumValue.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblEnumValue
ms:assetid: a33df20c-d19d-4f5c-b012-29dab8fb9200
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615025(v=OCS.15)
ms:contentKeyID: 48185040
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 159f90bb96c367fcb3e11725a582a9993080d3fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444445"
---
# <a name="tblenumvalue-in-lync-server-2013"></a><span data-ttu-id="32afa-103">tblEnumValue no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32afa-103">tblEnumValue in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="32afa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="32afa-104">

<span> </span></span></span>

<span data-ttu-id="32afa-105">_**Tópico da última modificação:** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="32afa-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="32afa-106">tblEnumValue é uma tabela codificada que contém os valores de visibilidade e comportamento dos atributos usados na tabela de nós.</span><span class="sxs-lookup"><span data-stu-id="32afa-106">tblEnumValue is a hardcoded table that contains the Visibility and Behavior values of the attributes that are used in the Node table.</span></span>

### <a name="columns"></a><span data-ttu-id="32afa-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="32afa-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32afa-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="32afa-108">Column</span></span></th>
<th><span data-ttu-id="32afa-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="32afa-109">Type</span></span></th>
<th><span data-ttu-id="32afa-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="32afa-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32afa-111">valueid</span><span class="sxs-lookup"><span data-stu-id="32afa-111">valueID</span></span></p></td>
<td><p><span data-ttu-id="32afa-112">smallint, não nulo</span><span class="sxs-lookup"><span data-stu-id="32afa-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="32afa-113">ID do valor.</span><span class="sxs-lookup"><span data-stu-id="32afa-113">ID of the value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32afa-114">attributeID</span><span class="sxs-lookup"><span data-stu-id="32afa-114">attributeID</span></span></p></td>
<td><p><span data-ttu-id="32afa-115">smallint, não nulo</span><span class="sxs-lookup"><span data-stu-id="32afa-115">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="32afa-116">ID do atributo.</span><span class="sxs-lookup"><span data-stu-id="32afa-116">ID of the attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32afa-117">atributovalue</span><span class="sxs-lookup"><span data-stu-id="32afa-117">attributeValue</span></span></p></td>
<td><p><span data-ttu-id="32afa-118">nvarchar (256), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="32afa-118">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="32afa-119">Nome do valor.</span><span class="sxs-lookup"><span data-stu-id="32afa-119">Name of the value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="32afa-120">As</span><span class="sxs-lookup"><span data-stu-id="32afa-120">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32afa-121">Coluna</span><span class="sxs-lookup"><span data-stu-id="32afa-121">Column</span></span></th>
<th><span data-ttu-id="32afa-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="32afa-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32afa-123">valueid</span><span class="sxs-lookup"><span data-stu-id="32afa-123">valueID</span></span></p></td>
<td><p><span data-ttu-id="32afa-124">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="32afa-124">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32afa-125">attributeID</span><span class="sxs-lookup"><span data-stu-id="32afa-125">attributeID</span></span></p></td>
<td><p><span data-ttu-id="32afa-126">Chave estrangeira com pesquisa na tabela tblEnumAttribute. attributeID.</span><span class="sxs-lookup"><span data-stu-id="32afa-126">Foreign key with lookup in tblEnumAttribute.attributeID table.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-values"></a><span data-ttu-id="32afa-127">Valores da tabela</span><span class="sxs-lookup"><span data-stu-id="32afa-127">Table Values</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32afa-128">valueid</span><span class="sxs-lookup"><span data-stu-id="32afa-128">valueID</span></span></th>
<th><span data-ttu-id="32afa-129">attributeID</span><span class="sxs-lookup"><span data-stu-id="32afa-129">attributeID</span></span></th>
<th><span data-ttu-id="32afa-130">atributovalue</span><span class="sxs-lookup"><span data-stu-id="32afa-130">attributeValue</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32afa-131">2</span><span class="sxs-lookup"><span data-stu-id="32afa-131">2</span></span></p></td>
<td><p><span data-ttu-id="32afa-132">1</span><span class="sxs-lookup"><span data-stu-id="32afa-132">1</span></span></p></td>
<td><p><span data-ttu-id="32afa-133">private</span><span class="sxs-lookup"><span data-stu-id="32afa-133">private</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32afa-134">3</span><span class="sxs-lookup"><span data-stu-id="32afa-134">3</span></span></p></td>
<td><p><span data-ttu-id="32afa-135">1</span><span class="sxs-lookup"><span data-stu-id="32afa-135">1</span></span></p></td>
<td><p><span data-ttu-id="32afa-136">com</span><span class="sxs-lookup"><span data-stu-id="32afa-136">scope</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32afa-137">4</span><span class="sxs-lookup"><span data-stu-id="32afa-137">4</span></span></p></td>
<td><p><span data-ttu-id="32afa-138">2</span><span class="sxs-lookup"><span data-stu-id="32afa-138">2</span></span></p></td>
<td><p><span data-ttu-id="32afa-139">Normalmente</span><span class="sxs-lookup"><span data-stu-id="32afa-139">normal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32afa-140">5</span><span class="sxs-lookup"><span data-stu-id="32afa-140">5</span></span></p></td>
<td><p><span data-ttu-id="32afa-141">2</span><span class="sxs-lookup"><span data-stu-id="32afa-141">2</span></span></p></td>
<td><p><span data-ttu-id="32afa-142">auditorium</span><span class="sxs-lookup"><span data-stu-id="32afa-142">auditorium</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32afa-143">6</span><span class="sxs-lookup"><span data-stu-id="32afa-143">6</span></span></p></td>
<td><p><span data-ttu-id="32afa-144">1</span><span class="sxs-lookup"><span data-stu-id="32afa-144">1</span></span></p></td>
<td><p><span data-ttu-id="32afa-145">abriu</span><span class="sxs-lookup"><span data-stu-id="32afa-145">open</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="32afa-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="32afa-146">See Also</span></span>


[<span data-ttu-id="32afa-147">tblNode no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32afa-147">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)  
  

<span data-ttu-id="32afa-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="32afa-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

