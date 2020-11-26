---
title: 'Lync Server 2013: Tabela ConferenceMessageCount'
description: 'Lync Server 2013: ConferenceMessageCount Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceMessageCount table
ms:assetid: 78569dbf-5217-42fa-ba1a-4380f56e2a3d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398590(v=OCS.15)
ms:contentKeyID: 48184570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 271b654c09ab1aef194eb613e660de208aea1534
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434449"
---
# <a name="conferencemessagecount-table-in-lync-server-2013"></a><span data-ttu-id="7a28e-103">Tabela ConferenceMessageCount no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a28e-103">ConferenceMessageCount table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7a28e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7a28e-104">

<span> </span></span></span>

<span data-ttu-id="7a28e-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="7a28e-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="7a28e-106">Cada registro nessa tabela representa um usuário em uma conferência de mensagem instantânea e inclui o número de mensagens enviadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="7a28e-106">Each record in this table represents one user in one IM conference and includes the number of messages sent by that user.</span></span> <span data-ttu-id="7a28e-107">Cada conferência é representada por vários registros nesta tabela; um registro para cada usuário.</span><span class="sxs-lookup"><span data-stu-id="7a28e-107">Each conference is represented by multiple records in this table; one record for each user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a28e-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="7a28e-108">Column</span></span></th>
<th><span data-ttu-id="7a28e-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7a28e-109">Data Type</span></span></th>
<th><span data-ttu-id="7a28e-110">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="7a28e-110">Key/Index</span></span></th>
<th><span data-ttu-id="7a28e-111">Detalhes</span><span class="sxs-lookup"><span data-stu-id="7a28e-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a28e-112"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="7a28e-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="7a28e-113">datetime</span><span class="sxs-lookup"><span data-stu-id="7a28e-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="7a28e-114">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="7a28e-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="7a28e-115">Hora da ocorrência da conferência.</span><span class="sxs-lookup"><span data-stu-id="7a28e-115">Time of conference instance.</span></span> <span data-ttu-id="7a28e-116">Usado em conjunto com <strong>SessionIdSeq</strong> para identificar uma instância de conferência de maneira exclusiva.</span><span class="sxs-lookup"><span data-stu-id="7a28e-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="7a28e-117">Consulte a <a href="lync-server-2013-conferences-table.md">tabela conferências no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="7a28e-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a28e-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="7a28e-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="7a28e-119">int</span><span class="sxs-lookup"><span data-stu-id="7a28e-119">int</span></span></p></td>
<td><p><span data-ttu-id="7a28e-120">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="7a28e-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="7a28e-121">Número de identificação para identificar a instância de conferência.</span><span class="sxs-lookup"><span data-stu-id="7a28e-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="7a28e-122">Usado em conjunto com a <strong>identificação_da_sessãotime</strong> para identificar exclusivamente uma instância de conferência.</span><span class="sxs-lookup"><span data-stu-id="7a28e-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="7a28e-123">Consulte a <a href="lync-server-2013-conferences-table.md">tabela conferências no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="7a28e-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a28e-124"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="7a28e-124"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="7a28e-125">int</span><span class="sxs-lookup"><span data-stu-id="7a28e-125">int</span></span></p></td>
<td><p><span data-ttu-id="7a28e-126">Exterior</span><span class="sxs-lookup"><span data-stu-id="7a28e-126">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7a28e-127">Número exclusivo que identifica esse usuário, referenciado pela <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="7a28e-127">Unique number identifying this user, referenced from the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a28e-128"><strong>MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="7a28e-128"><strong>MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="7a28e-129">smallint</span><span class="sxs-lookup"><span data-stu-id="7a28e-129">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7a28e-130">O número de mensagens enviadas por este usuário durante esta conferência.</span><span class="sxs-lookup"><span data-stu-id="7a28e-130">The number of messages sent by this user during this conference.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7a28e-131">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7a28e-131">


</div>

<span> </span>

</div>

</div>

</span></span></div>

