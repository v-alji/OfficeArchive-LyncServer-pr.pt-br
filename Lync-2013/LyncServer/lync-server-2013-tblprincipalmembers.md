---
title: 'Lync Server 2013: tblPrincipalMembers'
description: 'Lync Server 2013: tblPrincipalMembers.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalMembers
ms:assetid: 9a3e24cf-6ef7-4b82-99fc-50ba41800b6f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615022(v=OCS.15)
ms:contentKeyID: 48184965
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8bbb8be0b83d09b1bd54ea98655558581e6df834
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389759"
---
# <a name="tblprincipalmembers-in-lync-server-2013"></a><span data-ttu-id="38748-103">tblPrincipalMembers no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="38748-103">tblPrincipalMembers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="38748-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="38748-104">

<span> </span></span></span>

<span data-ttu-id="38748-105">_**Tópico da última modificação:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="38748-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="38748-106">tblPrincipalMembers contém associações de entidades de segurança.</span><span class="sxs-lookup"><span data-stu-id="38748-106">tblPrincipalMembers contains principal memberships.</span></span>

### <a name="columns"></a><span data-ttu-id="38748-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="38748-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="38748-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="38748-108">Column</span></span></th>
<th><span data-ttu-id="38748-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="38748-109">Type</span></span></th>
<th><span data-ttu-id="38748-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="38748-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38748-111">multiimprimir</span><span class="sxs-lookup"><span data-stu-id="38748-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="38748-112">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="38748-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="38748-113">ID da entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="38748-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38748-114">memberADPath</span><span class="sxs-lookup"><span data-stu-id="38748-114">memberADPath</span></span></p></td>
<td><p><span data-ttu-id="38748-115">nvarchar (384), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="38748-115">nvarchar (384), not null</span></span></p></td>
<td><p><span data-ttu-id="38748-116">Nome diferenciado de um membro.</span><span class="sxs-lookup"><span data-stu-id="38748-116">Distinguished name of a member.</span></span> <span data-ttu-id="38748-117">Um membro não precisa ser um principal (na tabela tblPrincipal).</span><span class="sxs-lookup"><span data-stu-id="38748-117">A member does not have to be a principal (in tblPrincipal table).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="38748-118">As</span><span class="sxs-lookup"><span data-stu-id="38748-118">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="38748-119">Coluna</span><span class="sxs-lookup"><span data-stu-id="38748-119">Column</span></span></th>
<th><span data-ttu-id="38748-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="38748-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38748-121">&lt;memberADPath&gt;</span><span class="sxs-lookup"><span data-stu-id="38748-121">&lt;prinID, memberADPath&gt;</span></span></p></td>
<td><p><span data-ttu-id="38748-122">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="38748-122">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38748-123">multiimprimir</span><span class="sxs-lookup"><span data-stu-id="38748-123">prinID</span></span></p></td>
<td><p><span data-ttu-id="38748-124">Chave estrangeira com Lookup em tblPrincipal. importaid.</span><span class="sxs-lookup"><span data-stu-id="38748-124">Foreign key with lookup in tblPrincipal.prinID.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="38748-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="38748-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

