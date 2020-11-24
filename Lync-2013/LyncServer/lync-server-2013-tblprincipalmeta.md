---
title: 'Lync Server 2013: tblPrincipalMeta'
description: 'Lync Server 2013: tblPrincipalMeta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalMeta
ms:assetid: 808490d4-7d6d-47a2-b8af-b5940d47073b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615009(v=OCS.15)
ms:contentKeyID: 48184648
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 899fd1e450dac52afa56c1ee1de86da82b2db309
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389758"
---
# <a name="tblprincipalmeta-in-lync-server-2013"></a><span data-ttu-id="5b320-103">tblPrincipalMeta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5b320-103">tblPrincipalMeta in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b320-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b320-104">

<span> </span></span></span>

<span data-ttu-id="5b320-105">_**Tópico da última modificação:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="5b320-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="5b320-106">tblPrincipalMeta contém as entidades de segurança que devem ser atualizadas a partir dos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5b320-106">tblPrincipalMeta contains the principals that have to be refreshed from Active Directory Domain Services.</span></span>

### <a name="columns"></a><span data-ttu-id="5b320-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="5b320-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b320-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="5b320-108">Column</span></span></th>
<th><span data-ttu-id="5b320-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5b320-109">Type</span></span></th>
<th><span data-ttu-id="5b320-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b320-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b320-111">multiimprimir</span><span class="sxs-lookup"><span data-stu-id="5b320-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="5b320-112">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="5b320-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="5b320-113">ID da entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="5b320-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b320-114">prinAffiliationsDirty</span><span class="sxs-lookup"><span data-stu-id="5b320-114">prinAffiliationsDirty</span></span></p></td>
<td><p><span data-ttu-id="5b320-115">bit, e não nulo</span><span class="sxs-lookup"><span data-stu-id="5b320-115">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="5b320-116">Verdadeiro se as afiliações principais precisarem ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="5b320-116">True if principal affiliations have to be refreshed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b320-117">prinAttributesDirty</span><span class="sxs-lookup"><span data-stu-id="5b320-117">prinAttributesDirty</span></span></p></td>
<td><p><span data-ttu-id="5b320-118">bit, e não nulo</span><span class="sxs-lookup"><span data-stu-id="5b320-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="5b320-119">Verdadeiro se os atributos principais precisarem ser atualizados.</span><span class="sxs-lookup"><span data-stu-id="5b320-119">True if principal attributes have to be refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b320-120">prinDeleted</span><span class="sxs-lookup"><span data-stu-id="5b320-120">prinDeleted</span></span></p></td>
<td><p><span data-ttu-id="5b320-121">bit, e não nulo</span><span class="sxs-lookup"><span data-stu-id="5b320-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="5b320-122">Verdadeiro se o capital foi excluído.</span><span class="sxs-lookup"><span data-stu-id="5b320-122">True if the principal has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b320-123">tryCount</span><span class="sxs-lookup"><span data-stu-id="5b320-123">tryCount</span></span></p></td>
<td><p><span data-ttu-id="5b320-124">int</span><span class="sxs-lookup"><span data-stu-id="5b320-124">int</span></span></p></td>
<td><p><span data-ttu-id="5b320-125">Número de tentativas de atualizar a entidade de segurança do AD DS que aconteceram até agora.</span><span class="sxs-lookup"><span data-stu-id="5b320-125">Number of attempts to refresh the principal from AD DS that have happened so far.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b320-126">lastTry</span><span class="sxs-lookup"><span data-stu-id="5b320-126">lastTry</span></span></p></td>
<td><p><span data-ttu-id="5b320-127">datetime</span><span class="sxs-lookup"><span data-stu-id="5b320-127">datetime</span></span></p></td>
<td><p><span data-ttu-id="5b320-128">Carimbo de data/hora da tentativa mais recente de atualizar a entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="5b320-128">Time stamp from the latest attempt to refresh the principal.</span></span> <span data-ttu-id="5b320-129">Pode ser NULL se ainda não houver uma tentativa de atualização.</span><span class="sxs-lookup"><span data-stu-id="5b320-129">Can be null if no refresh has been attempted yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b320-130">nextTry</span><span class="sxs-lookup"><span data-stu-id="5b320-130">nextTry</span></span></p></td>
<td><p><span data-ttu-id="5b320-131">datetime</span><span class="sxs-lookup"><span data-stu-id="5b320-131">datetime</span></span></p></td>
<td><p><span data-ttu-id="5b320-132">Carimbo de data/hora para a próxima atualização agendada.</span><span class="sxs-lookup"><span data-stu-id="5b320-132">Time stamp for the next scheduled refresh.</span></span> <span data-ttu-id="5b320-133">Pode ser NULL se não houver mais nenhuma atualização agendada.</span><span class="sxs-lookup"><span data-stu-id="5b320-133">Can be null if no further refresh has been scheduled.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="5b320-134">As</span><span class="sxs-lookup"><span data-stu-id="5b320-134">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b320-135">Coluna</span><span class="sxs-lookup"><span data-stu-id="5b320-135">Column</span></span></th>
<th><span data-ttu-id="5b320-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b320-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b320-137">multiimprimir</span><span class="sxs-lookup"><span data-stu-id="5b320-137">prinID</span></span></p></td>
<td><p><span data-ttu-id="5b320-138">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="5b320-138">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b320-139">multiimprimir</span><span class="sxs-lookup"><span data-stu-id="5b320-139">prinID</span></span></p></td>
<td><p><span data-ttu-id="5b320-140">Chave estrangeira com Lookup na tabela tblPrincipal. retoid.</span><span class="sxs-lookup"><span data-stu-id="5b320-140">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5b320-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b320-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

