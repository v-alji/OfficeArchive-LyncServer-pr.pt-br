---
title: 'Lync Server 2013: tblActivePeers'
description: 'Lync Server 2013: tblActivePeers.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblActivePeers
ms:assetid: b50c3f4a-bab6-4cb9-b40e-016cf1a9c607
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615030(v=OCS.15)
ms:contentKeyID: 48185176
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f274f82a280883e38e8e02409305982b64c18e4a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389964"
---
# <a name="tblactivepeers-in-lync-server-2013"></a><span data-ttu-id="11535-103">tblActivePeers no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="11535-103">tblActivePeers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="11535-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="11535-104">

<span> </span></span></span>

<span data-ttu-id="11535-105">_**Tópico da última modificação:** 2012-06-29_</span><span class="sxs-lookup"><span data-stu-id="11535-105">_**Topic Last Modified:** 2012-06-29_</span></span>

<span data-ttu-id="11535-106">o tblActivePeers contém as conexões ponto-a-ponto atuais entre os serviços de chat.</span><span class="sxs-lookup"><span data-stu-id="11535-106">tblActivePeers contains the current peer-to-peer connections between chat services.</span></span>

### <a name="columns"></a><span data-ttu-id="11535-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="11535-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11535-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="11535-108">Column</span></span></th>
<th><span data-ttu-id="11535-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="11535-109">Type</span></span></th>
<th><span data-ttu-id="11535-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="11535-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11535-111">aplServerID</span><span class="sxs-lookup"><span data-stu-id="11535-111">aplServerID</span></span></p></td>
<td><p><span data-ttu-id="11535-112">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="11535-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="11535-113">ID do servidor que postou a entrada.</span><span class="sxs-lookup"><span data-stu-id="11535-113">ID of the server that posted the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11535-114">aplPeerID</span><span class="sxs-lookup"><span data-stu-id="11535-114">aplPeerID</span></span></p></td>
<td><p><span data-ttu-id="11535-115">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="11535-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="11535-116">ID do par ao qual o servidor de postagem está conectado.</span><span class="sxs-lookup"><span data-stu-id="11535-116">ID of the peer that the posting server is connected to.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="11535-117">As</span><span class="sxs-lookup"><span data-stu-id="11535-117">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11535-118">Coluna</span><span class="sxs-lookup"><span data-stu-id="11535-118">Column</span></span></th>
<th><span data-ttu-id="11535-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="11535-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11535-120">&lt;aplServerID, aplPeerID&gt;</span><span class="sxs-lookup"><span data-stu-id="11535-120">&lt;aplServerID, aplPeerID&gt;</span></span></p></td>
<td><p><span data-ttu-id="11535-121">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="11535-121">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11535-122">aplServerID</span><span class="sxs-lookup"><span data-stu-id="11535-122">aplServerID</span></span></p></td>
<td><p><span data-ttu-id="11535-123">Chave estrangeira com Lookup na tabela tblServerIdentity. serverID.</span><span class="sxs-lookup"><span data-stu-id="11535-123">Foreign key with lookup in tblServerIdentity.serverID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11535-124">aplPeerID</span><span class="sxs-lookup"><span data-stu-id="11535-124">aplPeerID</span></span></p></td>
<td><p><span data-ttu-id="11535-125">Chave estrangeira com Lookup na tabela tblServerIdentity. serverID.</span><span class="sxs-lookup"><span data-stu-id="11535-125">Foreign key with lookup in tblServerIdentity.serverID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="11535-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="11535-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

