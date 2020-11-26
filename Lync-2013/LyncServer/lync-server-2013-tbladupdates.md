---
title: 'Lync Server 2013: tblADUpdates'
description: 'Lync Server 2013: tblADUpdates.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblADUpdates
ms:assetid: ba19fa16-4d2d-4635-ac32-f93e09469546
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615033(v=OCS.15)
ms:contentKeyID: 48185227
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ab4418a10eac283d0f39d09b1c1fe15a32b2e68
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444480"
---
# <a name="tbladupdates-in-lync-server-2013"></a><span data-ttu-id="5157f-103">tblADUpdates no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5157f-103">tblADUpdates in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5157f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5157f-104">

<span> </span></span></span>

<span data-ttu-id="5157f-105">_**Tópico da última modificação:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="5157f-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="5157f-106">o tblADUpdates contém alterações dos serviços de domínio Active Directory que ainda não foram processadas pelas etapas de sincronização posteriores do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5157f-106">tblADUpdates contains Active Directory Domain Services changes that have not yet been processed by the later Active Directory Sync steps.</span></span>

### <a name="columns"></a><span data-ttu-id="5157f-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="5157f-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5157f-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="5157f-108">Column</span></span></th>
<th><span data-ttu-id="5157f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5157f-109">Type</span></span></th>
<th><span data-ttu-id="5157f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5157f-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5157f-111">prinGuid</span><span class="sxs-lookup"><span data-stu-id="5157f-111">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="5157f-112">GUID, não nulo</span><span class="sxs-lookup"><span data-stu-id="5157f-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="5157f-113">O principal GUID do objeto que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="5157f-113">Principal GUID of the object that changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5157f-114">prinADPath</span><span class="sxs-lookup"><span data-stu-id="5157f-114">prinADPath</span></span></p></td>
<td><p><span data-ttu-id="5157f-115">nvarchar (384), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="5157f-115">nvarchar (384), not null</span></span></p></td>
<td><p><span data-ttu-id="5157f-116">Nome diferenciado do objeto.</span><span class="sxs-lookup"><span data-stu-id="5157f-116">Distinguished name of the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5157f-117">prinAttributesChanged</span><span class="sxs-lookup"><span data-stu-id="5157f-117">prinAttributesChanged</span></span></p></td>
<td><p><span data-ttu-id="5157f-118">bit, e não nulo</span><span class="sxs-lookup"><span data-stu-id="5157f-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="5157f-119">True se pelo menos um atributo do objeto foi alterado.</span><span class="sxs-lookup"><span data-stu-id="5157f-119">True if at least one attribute of the object changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5157f-120">prinMembersChanged</span><span class="sxs-lookup"><span data-stu-id="5157f-120">prinMembersChanged</span></span></p></td>
<td><p><span data-ttu-id="5157f-121">bit, e não nulo</span><span class="sxs-lookup"><span data-stu-id="5157f-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="5157f-122">Verdadeiro se a associação for alterada.</span><span class="sxs-lookup"><span data-stu-id="5157f-122">True if the membership changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5157f-123">prinAffiliationsChanged</span><span class="sxs-lookup"><span data-stu-id="5157f-123">prinAffiliationsChanged</span></span></p></td>
<td><p><span data-ttu-id="5157f-124">bit, e não nulo</span><span class="sxs-lookup"><span data-stu-id="5157f-124">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="5157f-125">Não usado.</span><span class="sxs-lookup"><span data-stu-id="5157f-125">Not used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5157f-126">prinDeleted</span><span class="sxs-lookup"><span data-stu-id="5157f-126">prinDeleted</span></span></p></td>
<td><p><span data-ttu-id="5157f-127">bit, e não nulo</span><span class="sxs-lookup"><span data-stu-id="5157f-127">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="5157f-128">Verdadeiro se o objeto foi excluído.</span><span class="sxs-lookup"><span data-stu-id="5157f-128">True if the object was deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5157f-129">lastUpdated</span><span class="sxs-lookup"><span data-stu-id="5157f-129">lastUpdated</span></span></p></td>
<td><p><span data-ttu-id="5157f-130">DateTime, não nulo</span><span class="sxs-lookup"><span data-stu-id="5157f-130">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="5157f-131">Carimbo de data/hora de quando a linha foi inserida.</span><span class="sxs-lookup"><span data-stu-id="5157f-131">Time stamp of when the row was inserted.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5157f-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5157f-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

