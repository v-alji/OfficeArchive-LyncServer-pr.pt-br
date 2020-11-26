---
title: 'Lync Server 2013: Tabela Users'
description: 'Lync Server 2013: tabela usuários.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Users table
ms:assetid: a8d71373-4b57-4245-9f02-f7fc0d9fcd3c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412791(v=OCS.15)
ms:contentKeyID: 48185032
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b1418e162a04e46ee0dfeca082aa66b0665fc77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436178"
---
# <a name="users-table-in-lync-server-2013"></a><span data-ttu-id="4cab8-103">Tabela Users no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4cab8-103">Users table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4cab8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4cab8-104">

<span> </span></span></span>

<span data-ttu-id="4cab8-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="4cab8-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="4cab8-106">A tabela usuários é uma tabela de suporte.</span><span class="sxs-lookup"><span data-stu-id="4cab8-106">The Users table is a supporting table.</span></span> <span data-ttu-id="4cab8-107">Cada registro na tabela armazena informações sobre um usuário envolvido em chamadas ou sessões que têm registros no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4cab8-107">Each record in the table stores information about one user involved in calls or sessions that have records in the database.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4cab8-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="4cab8-108">Column</span></span></th>
<th><span data-ttu-id="4cab8-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4cab8-109">Data Type</span></span></th>
<th><span data-ttu-id="4cab8-110">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="4cab8-110">Key/Index</span></span></th>
<th><span data-ttu-id="4cab8-111">Detalhes</span><span class="sxs-lookup"><span data-stu-id="4cab8-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cab8-112"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="4cab8-112"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="4cab8-113">datetime</span><span class="sxs-lookup"><span data-stu-id="4cab8-113">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4cab8-114">Carimbo de data/hora para uso interno.</span><span class="sxs-lookup"><span data-stu-id="4cab8-114">Time stamp for internal use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cab8-115"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="4cab8-115"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="4cab8-116">int</span><span class="sxs-lookup"><span data-stu-id="4cab8-116">int</span></span></p></td>
<td><p><span data-ttu-id="4cab8-117">Primária</span><span class="sxs-lookup"><span data-stu-id="4cab8-117">Primary</span></span></p></td>
<td><p><span data-ttu-id="4cab8-118">Número exclusivo que identifica esse usuário.</span><span class="sxs-lookup"><span data-stu-id="4cab8-118">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cab8-119"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="4cab8-119"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="4cab8-120">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="4cab8-120">nvarchar(450)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="4cab8-121">URI de usuário.</span><span class="sxs-lookup"><span data-stu-id="4cab8-121">User URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cab8-122"><strong>Tenantid</strong></span><span class="sxs-lookup"><span data-stu-id="4cab8-122"><strong>TenantId</strong></span></span></p></td>
<td><p><span data-ttu-id="4cab8-123">int</span><span class="sxs-lookup"><span data-stu-id="4cab8-123">int</span></span></p></td>
<td><p><span data-ttu-id="4cab8-124">Exterior</span><span class="sxs-lookup"><span data-stu-id="4cab8-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="4cab8-125">A ID de locatário deste usuário.</span><span class="sxs-lookup"><span data-stu-id="4cab8-125">This user’s Tenant ID.</span></span> <span data-ttu-id="4cab8-126">Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="4cab8-126">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cab8-127"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="4cab8-127"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="4cab8-128">int</span><span class="sxs-lookup"><span data-stu-id="4cab8-128">int</span></span></p></td>
<td><p><span data-ttu-id="4cab8-129">Exterior</span><span class="sxs-lookup"><span data-stu-id="4cab8-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="4cab8-130">O tipo de URI deste usuário.</span><span class="sxs-lookup"><span data-stu-id="4cab8-130">This user’s URI type.</span></span> <span data-ttu-id="4cab8-131">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="4cab8-131">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4cab8-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4cab8-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

