---
title: 'Lync Server 2013: tblServerIdentity'
description: 'Lync Server 2013: tblServerIdentity.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblServerIdentity
ms:assetid: 5411c9bc-b0b3-41fc-8b7e-fa71cccd770b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558648(v=OCS.15)
ms:contentKeyID: 48184125
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e954618cb373f2cf4f1b7ed929c3aaf6d8875e92
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389744"
---
# <a name="tblserveridentity-in-lync-server-2013"></a><span data-ttu-id="90029-103">tblServerIdentity no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="90029-103">tblServerIdentity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="90029-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="90029-104">

<span> </span></span></span>

<span data-ttu-id="90029-105">_**Tópico da última modificação:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="90029-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="90029-106">tblServerIdentity contém os servidores de chat ativos no pool do servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="90029-106">tblServerIdentity contains the active chat servers in the Persistent Chat Server pool.</span></span>

### <a name="columns"></a><span data-ttu-id="90029-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="90029-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90029-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="90029-108">Column</span></span></th>
<th><span data-ttu-id="90029-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="90029-109">Type</span></span></th>
<th><span data-ttu-id="90029-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="90029-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90029-111">serverID</span><span class="sxs-lookup"><span data-stu-id="90029-111">serverID</span></span></p></td>
<td><p><span data-ttu-id="90029-112">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="90029-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="90029-113">ID do servidor.</span><span class="sxs-lookup"><span data-stu-id="90029-113">Server ID.</span></span> <span data-ttu-id="90029-114">Corresponde à ID da instância do repositório de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="90029-114">Corresponds to the instance ID from Central Management store.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90029-115">a</span><span class="sxs-lookup"><span data-stu-id="90029-115">serverAddress</span></span></p></td>
<td><p><span data-ttu-id="90029-116">nvarchar (256), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="90029-116">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="90029-117">Endereço do servidor usando o endereço do Windows Communication Foundation.</span><span class="sxs-lookup"><span data-stu-id="90029-117">Server address using the Windows Communication Foundation address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90029-118">serverLastPingTime</span><span class="sxs-lookup"><span data-stu-id="90029-118">serverLastPingTime</span></span></p></td>
<td><p><span data-ttu-id="90029-119">datetime</span><span class="sxs-lookup"><span data-stu-id="90029-119">datetime</span></span></p></td>
<td><p><span data-ttu-id="90029-120">A última vez em que o servidor de canal atualizou essa linha para dar evidências de que esteja em execução.</span><span class="sxs-lookup"><span data-stu-id="90029-120">The latest time that the Channel Server updated this row to give evidence that it is running.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="90029-121">Chave</span><span class="sxs-lookup"><span data-stu-id="90029-121">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90029-122">Coluna</span><span class="sxs-lookup"><span data-stu-id="90029-122">Column</span></span></th>
<th><span data-ttu-id="90029-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="90029-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90029-124">serverID</span><span class="sxs-lookup"><span data-stu-id="90029-124">serverID</span></span></p></td>
<td><p><span data-ttu-id="90029-125">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="90029-125">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="90029-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="90029-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

