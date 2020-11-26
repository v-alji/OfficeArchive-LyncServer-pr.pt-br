---
title: Fases de migração
description: Fases de migração.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migration phases
ms:assetid: cb7747ba-b872-42ca-ab41-76e3c4e77d06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205336(v=OCS.15)
ms:contentKeyID: 48185642
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 72ef47cb9b6c9eba75c395eb9bd94c887ca5a433
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443332"
---
# <a name="migration-phases"></a><span data-ttu-id="30285-103">Fases de migração</span><span class="sxs-lookup"><span data-stu-id="30285-103">Migration phases</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30285-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30285-104">

<span> </span></span></span>

<span data-ttu-id="30285-105">_**Tópico da última modificação:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="30285-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="30285-106">No Lync Server 2013, você define sites em sua rede que contenham componentes do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="30285-106">In Lync Server 2013, you define sites on your network that contain Lync Server 2013 components.</span></span> <span data-ttu-id="30285-107">Um site é um conjunto de computadores que são bem conectados por uma rede de alta velocidade e baixa latência, como uma única rede local (LAN) ou duas redes conectadas por uma rede de fibra ótica de alta velocidade.</span><span class="sxs-lookup"><span data-stu-id="30285-107">A site is a set of computers that are well-connected by a high-speed, low-latency network, such as a single local area network (LAN) or two networks connected by a high-speed fiber optic network.</span></span>

<span data-ttu-id="30285-108">Um *pool de front-ends* é um conjunto de servidores front-end que são configurados de maneira idêntica e trabalham juntos para fornecer serviços para um grupo comum de usuários.</span><span class="sxs-lookup"><span data-stu-id="30285-108">A *Front End pool* is a set of Front End Servers that are configured identically and work together to provide services for a common group of users.</span></span> <span data-ttu-id="30285-109">Um pool fornece recursos de escalabilidade e failover para seus usuários.</span><span class="sxs-lookup"><span data-stu-id="30285-109">A pool provides scalability and failover capability to your users.</span></span> <span data-ttu-id="30285-110">Cada servidor de um pool deve executar funções idênticas de servidor.</span><span class="sxs-lookup"><span data-stu-id="30285-110">Each server in a pool must run an identical server role or roles.</span></span> <span data-ttu-id="30285-111">Um servidor Standard Edition, projetado para pequenas organizações, também define um pool e é executado em um único servidor.</span><span class="sxs-lookup"><span data-stu-id="30285-111">A Standard Edition server, designed for small organizations, also defines a pool and runs on a single server.</span></span> <span data-ttu-id="30285-112">Isso permite que você tenha a funcionalidade do Lync Server 2013 para um custo menor, mas não oferece uma solução real de alta disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="30285-112">This enables you to have Lync Server 2013 functionality for a lesser cost, but does not provide a true high-availability solution.</span></span>

<span data-ttu-id="30285-113">As fases a seguir descrevem o processo de uma migração de pool do Lync Server 2010 para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="30285-113">The following phases describe the process of a pool migration from Lync Server 2010 to Lync Server 2013.</span></span> <span data-ttu-id="30285-114">Para vários sites que contêm vários pools, cada pool individual deve seguir essa abordagem em fases.</span><span class="sxs-lookup"><span data-stu-id="30285-114">For multiple sites containing multiple pools, each individual pool should follow this phased approach.</span></span>

1.  [<span data-ttu-id="30285-115">Fase 1: planejar a migração do Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="30285-115">Phase 1: Plan your migration from Lync Server 2010</span></span>](phase-1-plan-your-migration-from-lync-server-2010.md)

2.  [<span data-ttu-id="30285-116">Fase 2: Preparar para migração</span><span class="sxs-lookup"><span data-stu-id="30285-116">Phase 2: Prepare for migration</span></span>](phase-2-prepare-for-migration.md)

3.  [<span data-ttu-id="30285-117">Fase 3: implantar o pool piloto do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30285-117">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>](phase-3-deploy-lync-server-2013-pilot-pool.md)

4.  [<span data-ttu-id="30285-118">Fase 4: mover os usuários de teste para o pool piloto</span><span class="sxs-lookup"><span data-stu-id="30285-118">Phase 4: Move test users to the pilot pool</span></span>](phase-4-move-test-users-to-the-pilot-pool.md)

5.  [<span data-ttu-id="30285-119">Fase 5: Adicionar o servidor de borda do Lync Server 2013 ao pool piloto</span><span class="sxs-lookup"><span data-stu-id="30285-119">Phase 5: Add Lync Server 2013 Edge Server to pilot pool</span></span>](phase-5-add-lync-server-2013-edge-server-to-pilot-pool.md)

6.  [<span data-ttu-id="30285-120">Fase 6: Mover da implantação piloto para produção</span><span class="sxs-lookup"><span data-stu-id="30285-120">Phase 6: Move from pilot deployment into production</span></span>](phase-6-move-from-pilot-deployment-into-production.md)

7.  [<span data-ttu-id="30285-121">Fase 7: Concluir tarefas pós-migração</span><span class="sxs-lookup"><span data-stu-id="30285-121">Phase 7: Complete post-migration tasks</span></span>](phase-7-complete-post-migration-tasks.md)

8.  [<span data-ttu-id="30285-122">Fase 8: Encerrar os pools herdados</span><span class="sxs-lookup"><span data-stu-id="30285-122">Phase 8: Decommission legacy pools</span></span>](phase-8-decommission-legacy-pools.md)

<span data-ttu-id="30285-123"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30285-123"></div>

<span> </span>

</div>

</div>

</span></span></div>

