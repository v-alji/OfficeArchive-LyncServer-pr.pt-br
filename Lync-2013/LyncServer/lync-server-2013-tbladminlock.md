---
title: 'Lync Server 2013: tblAdminLock'
description: 'Lync Server 2013: tblAdminLock.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblAdminLock
ms:assetid: 785a43c0-6892-474c-821c-fa9cdbeb99d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558665(v=OCS.15)
ms:contentKeyID: 48184560
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c3313826b2c0d578c515fb25f83e713b8978ae63
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389963"
---
# <a name="tbladminlock-in-lync-server-2013"></a><span data-ttu-id="f98da-103">tblAdminLock no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f98da-103">tblAdminLock in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f98da-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f98da-104">

<span> </span></span></span>

<span data-ttu-id="f98da-105">_**Tópico da última modificação:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="f98da-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="f98da-106">tblAdminLock contém o bloqueio do administrador necessário para executar alguns comandos de administrador.</span><span class="sxs-lookup"><span data-stu-id="f98da-106">tblAdminLock contains the administrator lock that is needed to run some administrator commands.</span></span>

### <a name="columns"></a><span data-ttu-id="f98da-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="f98da-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f98da-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="f98da-108">Column</span></span></th>
<th><span data-ttu-id="f98da-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f98da-109">Type</span></span></th>
<th><span data-ttu-id="f98da-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f98da-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f98da-111">lockExpiresTime</span><span class="sxs-lookup"><span data-stu-id="f98da-111">lockExpiresTime</span></span></p></td>
<td><p><span data-ttu-id="f98da-112">DateTime, não nulo</span><span class="sxs-lookup"><span data-stu-id="f98da-112">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="f98da-113">Bloquear data e hora de expiração.</span><span class="sxs-lookup"><span data-stu-id="f98da-113">Lock expiration date and time.</span></span> <span data-ttu-id="f98da-114">O proprietário pode estender esse valor periodicamente.</span><span class="sxs-lookup"><span data-stu-id="f98da-114">The owner can extend this value periodically.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f98da-115">lockServerID</span><span class="sxs-lookup"><span data-stu-id="f98da-115">lockServerID</span></span></p></td>
<td><p><span data-ttu-id="f98da-116">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="f98da-116">int, not null</span></span></p></td>
<td><p><span data-ttu-id="f98da-117">ID do servidor que é proprietário do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="f98da-117">ID of the server that owns the lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f98da-118">lockActorID</span><span class="sxs-lookup"><span data-stu-id="f98da-118">lockActorID</span></span></p></td>
<td><p><span data-ttu-id="f98da-119">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="f98da-119">int, not null</span></span></p></td>
<td><p><span data-ttu-id="f98da-120">ID da entidade de segurança que é proprietária do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="f98da-120">ID of the principal that owns the lock.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f98da-121">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f98da-121">


</div>

<span> </span>

</div>

</div>

</span></span></div>

