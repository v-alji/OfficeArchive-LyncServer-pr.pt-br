---
title: 'Lync Server 2013: Tabela User'
description: 'Lync Server 2013: tabela do usuário.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User table
ms:assetid: 6b52047e-286d-47ab-b7bc-a9b266f62d82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398505(v=OCS.15)
ms:contentKeyID: 48184437
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 15d1ac08a229f4afea35a2727ef1105a5f24b826
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444165"
---
# <a name="user-table-in-lync-server-2013"></a><span data-ttu-id="88d51-103">Tabela User no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88d51-103">User table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="88d51-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="88d51-104">

<span> </span></span></span>

<span data-ttu-id="88d51-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="88d51-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="88d51-106">A tabela do usuário é uma tabela de suporte que armazena uma lista de vários usuários que participaram de sessões registradas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="88d51-106">The User table is a supporting table that stores a list of the various users who have participated in sessions recorded in the database.</span></span> <span data-ttu-id="88d51-107">Cada registro na tabela representa um usuário.</span><span class="sxs-lookup"><span data-stu-id="88d51-107">Each record in the table represents one user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88d51-108"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="88d51-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="88d51-109"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="88d51-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="88d51-110"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="88d51-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="88d51-111"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="88d51-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88d51-112"><strong>UserKey</strong></span><span class="sxs-lookup"><span data-stu-id="88d51-112"><strong>UserKey</strong></span></span></p></td>
<td><p><span data-ttu-id="88d51-113">int</span><span class="sxs-lookup"><span data-stu-id="88d51-113">int</span></span></p></td>
<td><p><span data-ttu-id="88d51-114">Primária</span><span class="sxs-lookup"><span data-stu-id="88d51-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="88d51-115">Número exclusivo que identifica esse usuário.</span><span class="sxs-lookup"><span data-stu-id="88d51-115">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88d51-116"><strong>SOLICITAÇÃO</strong></span><span class="sxs-lookup"><span data-stu-id="88d51-116"><strong>URI</strong></span></span></p></td>
<td><p><span data-ttu-id="88d51-117">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="88d51-117">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="88d51-118">Exclusividade</span><span class="sxs-lookup"><span data-stu-id="88d51-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="88d51-119">Cadeia de caracteres de URI.</span><span class="sxs-lookup"><span data-stu-id="88d51-119">URI string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88d51-120"><strong>URIType</strong></span><span class="sxs-lookup"><span data-stu-id="88d51-120"><strong>URIType</strong></span></span></p></td>
<td><p><span data-ttu-id="88d51-121">int</span><span class="sxs-lookup"><span data-stu-id="88d51-121">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="88d51-122">1 é um tipo de URI desconhecido.</span><span class="sxs-lookup"><span data-stu-id="88d51-122">1 is unknown URI type.</span></span></p>
<p><span data-ttu-id="88d51-123">2 é o URI do usuário.</span><span class="sxs-lookup"><span data-stu-id="88d51-123">2 is user URI.</span></span></p>
<p><span data-ttu-id="88d51-124">4 é o URI da conferência.</span><span class="sxs-lookup"><span data-stu-id="88d51-124">4 is conference URI.</span></span></p>
<p><span data-ttu-id="88d51-125">8 é o URI do telefone.</span><span class="sxs-lookup"><span data-stu-id="88d51-125">8 is phone URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88d51-126"><strong>TenantKey</strong></span><span class="sxs-lookup"><span data-stu-id="88d51-126"><strong>TenantKey</strong></span></span></p></td>
<td><p><span data-ttu-id="88d51-127">int</span><span class="sxs-lookup"><span data-stu-id="88d51-127">int</span></span></p></td>
<td><p><span data-ttu-id="88d51-128">Exterior</span><span class="sxs-lookup"><span data-stu-id="88d51-128">Foreign</span></span></p></td>
<td><p><span data-ttu-id="88d51-129">Locatário do usuário, referenciado da tabela de locatários.</span><span class="sxs-lookup"><span data-stu-id="88d51-129">Tenant of the user, referenced from tenant table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88d51-130"><strong>LastPoorCallTime</strong></span><span class="sxs-lookup"><span data-stu-id="88d51-130"><strong>LastPoorCallTime</strong></span></span></p></td>
<td><p><span data-ttu-id="88d51-131">datetime</span><span class="sxs-lookup"><span data-stu-id="88d51-131">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="88d51-132">Carimbo de data/hora mais recente quando o usuário tiver uma chamada de áudio ruim.</span><span class="sxs-lookup"><span data-stu-id="88d51-132">Latest time stamp when the user had a poor audio call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88d51-133"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="88d51-133"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="88d51-134">datetime</span><span class="sxs-lookup"><span data-stu-id="88d51-134">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="88d51-135">Somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="88d51-135">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="88d51-136">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="88d51-136">


</div>

<span> </span>

</div>

</div>

</span></span></div>

