---
title: 'Lync Server 2013: Suporte à alta disponibilidade e recuperação de desastre'
description: 'Lync Server 2013: alta disponibilidade e suporte à recuperação de desastres.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: High availability and disaster recovery support
ms:assetid: 47e77e85-c7c3-4ade-8db7-a34c71aeafd7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204866(v=OCS.15)
ms:contentKeyID: 48184053
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8113c6b54cbb55e8149f8d6dd1b53ccbdc9436d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427625"
---
# <a name="high-availability-and-disaster-recovery-support-in-lync-server-2013"></a><span data-ttu-id="c8c4a-103">Suporte à alta disponibilidade e recuperação de desastre no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8c4a-103">High availability and disaster recovery support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c8c4a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c8c4a-104">

<span> </span></span></span>

<span data-ttu-id="c8c4a-105">_**Tópico da última modificação:** 2012-09-25_</span><span class="sxs-lookup"><span data-stu-id="c8c4a-105">_**Topic Last Modified:** 2012-09-25_</span></span>

<span data-ttu-id="c8c4a-106">O Lync Server 2013 fornece alta disponibilidade por redundância de servidor via pool.</span><span class="sxs-lookup"><span data-stu-id="c8c4a-106">Lync Server 2013 provides high availability by server redundancy via pooling.</span></span> <span data-ttu-id="c8c4a-107">Se um servidor que executa determinada função falhar, os demais servidores do pool que executam a mesma função assumirão a carga desse servidor.</span><span class="sxs-lookup"><span data-stu-id="c8c4a-107">If a server running a certain server role fails, the other servers in the pool running the same role take the load of that server.</span></span> <span data-ttu-id="c8c4a-108">Isso se aplica a Servidores Front-End, Servidores de Borda, Servidores de Mediação e Diretores.</span><span class="sxs-lookup"><span data-stu-id="c8c4a-108">This applies to Front End Servers, Edge Servers, Mediation Servers, and Directors.</span></span> <span data-ttu-id="c8c4a-109">Para obter detalhes sobre as funções de servidor, consulte [funções de servidor no Lync server 2013](lync-server-2013-server-roles.md).</span><span class="sxs-lookup"><span data-stu-id="c8c4a-109">For details about server roles, see [Server roles in Lync Server 2013](lync-server-2013-server-roles.md).</span></span>

<span data-ttu-id="c8c4a-110">O Lync Server 2013 também fornece medidas de recuperação de desastres habilitando o emparelhamento de pool.</span><span class="sxs-lookup"><span data-stu-id="c8c4a-110">Lync Server 2013 also provides disaster recovery measures by enabling pool pairing.</span></span> <span data-ttu-id="c8c4a-111">Se implantar essa topologia, você designará pares de pools de Front-Ends, com cada pool de um par localizado em um datacenter e em uma área geográfica distinta.</span><span class="sxs-lookup"><span data-stu-id="c8c4a-111">If you deploy this topology, you will designate pairs of Front End pools, with each pool in a pair located in a separate data center, and in a separate geographical area.</span></span> <span data-ttu-id="c8c4a-112">Se um pool ou site ficar inativo, você poderá redirecionar os usuários desse pool para outro pool do par, com o mínimo de interrupção de serviço.</span><span class="sxs-lookup"><span data-stu-id="c8c4a-112">If one pool or site goes down, you can redirect the users of that pool to use the other pool in the pair, with minimal interruption of service.</span></span>

<span data-ttu-id="c8c4a-113">O Lync Server 2013 também oferece suporte à alta disponibilidade do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="c8c4a-113">Lync Server 2013 also supports Back End Server high availability.</span></span> <span data-ttu-id="c8c4a-114">Esta é uma topologia opcional na qual você implanta dois servidores back-end para um pool de front-end e configura o espelhamento do SQL Server síncrono para todos os bancos de dados do Lync em execução nos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="c8c4a-114">This is an optional topology in which you deploy two Back End Servers for a Front End pool, and set up synchronous SQL Server mirroring for all the Lync databases running on the Back End Servers.</span></span>

<span data-ttu-id="c8c4a-115">Para obter detalhes sobre o emparelhamento de pool e o espelhamento do servidor back-end, consulte [planejando alta disponibilidade e recuperação de desastres no Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="c8c4a-115">For details about pool pairing and Back End Server mirroring, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="c8c4a-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8c4a-116">See Also</span></span>


[<span data-ttu-id="c8c4a-117">Funções do servidor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8c4a-117">Server roles in Lync Server 2013</span></span>](lync-server-2013-server-roles.md)  
[<span data-ttu-id="c8c4a-118">Planejamento para alta disponibilidade e recuperação de desastre no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8c4a-118">Planning for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)  
  

<span data-ttu-id="c8c4a-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c8c4a-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

