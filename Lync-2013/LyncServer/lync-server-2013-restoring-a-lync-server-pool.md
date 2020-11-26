---
title: 'Lync Server 2013: restaurar um pool do Lync Server'
description: 'Lync Server 2013: restaurando um pool do Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a Lync Server pool
ms:assetid: 6fe80fb3-38ad-4931-a07b-1763b61aa448
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202176(v=OCS.15)
ms:contentKeyID: 51541488
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 02e92b4e7af9cf782d49c265425006e0118b9161
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442597"
---
# <a name="restoring-a-lync-server-pool-in-lync-server-2013"></a><span data-ttu-id="b6764-103">Restaurando um pool do Lync Server no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6764-103">Restoring a Lync Server pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b6764-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b6764-104">

<span> </span></span></span>

<span data-ttu-id="b6764-105">_**Tópico da última modificação:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="b6764-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="b6764-106">A implantação do Lync Server pode incluir qualquer um dos seguintes tipos de pool:</span><span class="sxs-lookup"><span data-stu-id="b6764-106">Your Lync Server deployment may include any of the following types of pools:</span></span>

  - <span data-ttu-id="b6764-107">Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="b6764-107">Front End Server</span></span>

  - <span data-ttu-id="b6764-108">Servidor de Mediação</span><span class="sxs-lookup"><span data-stu-id="b6764-108">Mediation Server</span></span>

  - <span data-ttu-id="b6764-109">Servidor de Chat Persistente</span><span class="sxs-lookup"><span data-stu-id="b6764-109">Persistent Chat Server</span></span>

  - <span data-ttu-id="b6764-110">Servidor de Borda</span><span class="sxs-lookup"><span data-stu-id="b6764-110">Edge Server</span></span>

<span data-ttu-id="b6764-111">Se um pool inteiro apresentar uma falha, siga estes procedimentos para cada servidor membro do pool.</span><span class="sxs-lookup"><span data-stu-id="b6764-111">If an entire pool experiences an outage, follow these procedures for each member server in the pool.</span></span>

  - <span data-ttu-id="b6764-112">Para um pool de front-ends, restaure primeiro o servidor back-end e, em seguida, restaure cada servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="b6764-112">For a Front End pool, restore the Back End Server first, and then restore each Front End Server.</span></span> <span data-ttu-id="b6764-113">Para obter detalhes, consulte [restaurando um servidor back-end do Enterprise Edition no Lync server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md) e [restaurando um servidor membro da Enterprise Edition no Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span><span class="sxs-lookup"><span data-stu-id="b6764-113">For details, see [Restoring an Enterprise Edition Back End Server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md) and [Restoring an Enterprise Edition member server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span></span>

  - <span data-ttu-id="b6764-114">Para todos os outros tipos de pools, restaure cada servidor membro.</span><span class="sxs-lookup"><span data-stu-id="b6764-114">For all other types of pools, restore each member server.</span></span> <span data-ttu-id="b6764-115">Para obter detalhes, consulte [restaurando um servidor membro do Enterprise Edition no Lync server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span><span class="sxs-lookup"><span data-stu-id="b6764-115">For details, see [Restoring an Enterprise Edition member server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span></span>

<span data-ttu-id="b6764-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b6764-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

