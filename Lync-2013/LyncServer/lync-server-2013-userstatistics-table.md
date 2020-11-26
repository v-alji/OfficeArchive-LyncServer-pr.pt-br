---
title: 'Lync Server 2013: tabela userstatistics'
description: 'Lync Server 2013: tabela userstatistics.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserStatistics table
ms:assetid: cfaf803b-1679-4169-92d3-533fad3e56ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721893(v=OCS.15)
ms:contentKeyID: 49733827
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 75b34fa3c34af4cc9cf2cacc6ae7feb4d217114c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436094"
---
# <a name="userstatistics-table-in-lync-server-2013"></a><span data-ttu-id="9a000-103">Tabela userstatistics no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a000-103">UserStatistics table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a000-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a000-104">

<span> </span></span></span>

<span data-ttu-id="9a000-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="9a000-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="9a000-106">A tabela userstatistics é uma tabela de suporte.</span><span class="sxs-lookup"><span data-stu-id="9a000-106">The UserStatistics table is a supporting table.</span></span> <span data-ttu-id="9a000-107">Cada registro na tabela armazena informações sobre o uso de um usuário individual do sistema.</span><span class="sxs-lookup"><span data-stu-id="9a000-107">Each record in the table stores information about an individual user’s usage of the system.</span></span> <span data-ttu-id="9a000-108">Esta tabela foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9a000-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a000-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="9a000-109">Column</span></span></th>
<th><span data-ttu-id="9a000-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9a000-110">Data Type</span></span></th>
<th><span data-ttu-id="9a000-111">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="9a000-111">Key/Index</span></span></th>
<th><span data-ttu-id="9a000-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="9a000-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a000-113"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="9a000-113"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="9a000-114">int</span><span class="sxs-lookup"><span data-stu-id="9a000-114">int</span></span></p></td>
<td><p><span data-ttu-id="9a000-115">Primária</span><span class="sxs-lookup"><span data-stu-id="9a000-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="9a000-116">Número exclusivo que identifica esse usuário.</span><span class="sxs-lookup"><span data-stu-id="9a000-116">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a000-117"><strong>LastLogInTime</strong></span><span class="sxs-lookup"><span data-stu-id="9a000-117"><strong>LastLogInTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9a000-118">datetime</span><span class="sxs-lookup"><span data-stu-id="9a000-118">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9a000-119">Última vez em que o usuário se conectou.</span><span class="sxs-lookup"><span data-stu-id="9a000-119">Last time the user logged in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a000-120"><strong>LastConfOrganizedTime</strong></span><span class="sxs-lookup"><span data-stu-id="9a000-120"><strong>LastConfOrganizedTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9a000-121">datetime</span><span class="sxs-lookup"><span data-stu-id="9a000-121">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9a000-122">Última vez em que o usuário organizou uma conferência.</span><span class="sxs-lookup"><span data-stu-id="9a000-122">Last time the user organized a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a000-123"><strong>LastCallOrganizerCallFailureTime</strong></span><span class="sxs-lookup"><span data-stu-id="9a000-123"><strong>LastCallOrganizerCallFailureTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9a000-124">datetime</span><span class="sxs-lookup"><span data-stu-id="9a000-124">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9a000-125">Última vez que o usuário experimentou uma falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="9a000-125">Last time the user experienced a call failure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a000-126"><strong>LastConfOrganizerCallFailureTime</strong></span><span class="sxs-lookup"><span data-stu-id="9a000-126"><strong>LastConfOrganizerCallFailureTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9a000-127">datetime</span><span class="sxs-lookup"><span data-stu-id="9a000-127">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9a000-128">Última vez que o usuário experimentou uma falha na chamada como um organizador de conferências.</span><span class="sxs-lookup"><span data-stu-id="9a000-128">Last time the user experienced a call failure as a conference organizer.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9a000-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a000-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

