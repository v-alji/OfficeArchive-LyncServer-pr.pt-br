---
title: 'Lync Server 2013: tblPrincipalAffiliations'
description: 'Lync Server 2013: tblPrincipalAffiliations.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalAffiliations
ms:assetid: 45fd8484-5837-44d2-85bb-45c83546607c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558642(v=OCS.15)
ms:contentKeyID: 48183993
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01c373147a58300e64f22e60e989a777c59b2653
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441365"
---
# <a name="tblprincipalaffiliations-in-lync-server-2013"></a><span data-ttu-id="7fe8b-103">tblPrincipalAffiliations no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7fe8b-103">tblPrincipalAffiliations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7fe8b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7fe8b-104">

<span> </span></span></span>

<span data-ttu-id="7fe8b-105">_**Tópico da última modificação:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="7fe8b-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="7fe8b-106">tblPrincipalAffiliations contém as afiliações principais que descrevem associações em locais, incluindo grupos de segurança dos serviços de domínio Active Directory, em contêineres do Active Directory, em domínios.</span><span class="sxs-lookup"><span data-stu-id="7fe8b-106">tblPrincipalAffiliations contains the principal affiliations that describe memberships in locations, including Active Directory Domain Services security groups, in Active Directory containers, in domains.</span></span>

### <a name="columns"></a><span data-ttu-id="7fe8b-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="7fe8b-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7fe8b-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="7fe8b-108">Column</span></span></th>
<th><span data-ttu-id="7fe8b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7fe8b-109">Type</span></span></th>
<th><span data-ttu-id="7fe8b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7fe8b-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7fe8b-111">entidade de segurança</span><span class="sxs-lookup"><span data-stu-id="7fe8b-111">principalID</span></span></p></td>
<td><p><span data-ttu-id="7fe8b-112">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="7fe8b-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="7fe8b-113">ID do objeto associado.</span><span class="sxs-lookup"><span data-stu-id="7fe8b-113">ID of the affiliated principal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fe8b-114">afiliaid</span><span class="sxs-lookup"><span data-stu-id="7fe8b-114">affiliationID</span></span></p></td>
<td><p><span data-ttu-id="7fe8b-115">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="7fe8b-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="7fe8b-116">ID da entidade de segurança que representa a afiliada.</span><span class="sxs-lookup"><span data-stu-id="7fe8b-116">ID of the principal representing the affiliation.</span></span> <span data-ttu-id="7fe8b-117">Cada entidade de segurança (exceto tipos de usuário do sistema) também tem uma afiliada.</span><span class="sxs-lookup"><span data-stu-id="7fe8b-117">Each principal (except system-user-types) has a self-affiliation as well.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7fe8b-118">dedo</span><span class="sxs-lookup"><span data-stu-id="7fe8b-118">index</span></span></p></td>
<td><p><span data-ttu-id="7fe8b-119">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="7fe8b-119">int, not null</span></span></p></td>
<td><p><span data-ttu-id="7fe8b-120">Dedo.</span><span class="sxs-lookup"><span data-stu-id="7fe8b-120">Index.</span></span> <span data-ttu-id="7fe8b-121">O valor para autoafiliações é-1 e para as outras afiliações que ele aumenta sequencialmente de 1 dentro de cada &lt; objeto de entidade de segurança, o &gt; BucketID.</span><span class="sxs-lookup"><span data-stu-id="7fe8b-121">The value for self-affiliations is -1, and for the other affiliations it increases sequentially from 1 within each &lt;principalID, affiliationId&gt; bucket.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fe8b-122">updatedBy</span><span class="sxs-lookup"><span data-stu-id="7fe8b-122">updatedBy</span></span></p></td>
<td><p><span data-ttu-id="7fe8b-123">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="7fe8b-123">int, not null</span></span></p></td>
<td><p><span data-ttu-id="7fe8b-124">Entidade de segurança que fez a atualização mais recente.</span><span class="sxs-lookup"><span data-stu-id="7fe8b-124">Principal that did the latest update.</span></span> <span data-ttu-id="7fe8b-125">Geralmente, isso é 1, o que significa sincronização do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7fe8b-125">This is usually 1, which means Active Directory Sync.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="7fe8b-126">As</span><span class="sxs-lookup"><span data-stu-id="7fe8b-126">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7fe8b-127">Colunas</span><span class="sxs-lookup"><span data-stu-id="7fe8b-127">Columns</span></span></th>
<th><span data-ttu-id="7fe8b-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="7fe8b-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7fe8b-129">&lt;entidade de segurança, índice, afiliaid&gt;</span><span class="sxs-lookup"><span data-stu-id="7fe8b-129">&lt;principalID, index, affiliationID&gt;</span></span></p></td>
<td><p><span data-ttu-id="7fe8b-130">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="7fe8b-130">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fe8b-131">entidade de segurança</span><span class="sxs-lookup"><span data-stu-id="7fe8b-131">principalID</span></span></p></td>
<td><p><span data-ttu-id="7fe8b-132">Chave estrangeira com Lookup na tabela tblPrincipal. retoid.</span><span class="sxs-lookup"><span data-stu-id="7fe8b-132">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7fe8b-133">afiliaid</span><span class="sxs-lookup"><span data-stu-id="7fe8b-133">affiliationID</span></span></p></td>
<td><p><span data-ttu-id="7fe8b-134">Chave estrangeira com Lookup na tabela tblPrincipal. retoid.</span><span class="sxs-lookup"><span data-stu-id="7fe8b-134">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7fe8b-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7fe8b-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

