---
title: 'Lync Server 2013: Alterações de topologia'
description: A topologia do Lync Server 2013 muda.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Topology changes
ms:assetid: 9e40ef93-9ab0-498c-9bbf-f94584353e53
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688153(v=OCS.15)
ms:contentKeyID: 49733756
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 562766eae939e4510a0d3af20e40b4731c361040
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436227"
---
# <a name="topology-changes-in-lync-server-2013"></a><span data-ttu-id="5358d-103">Alterações de topologia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5358d-103">Topology changes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5358d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5358d-104">

<span> </span></span></span>

<span data-ttu-id="5358d-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="5358d-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="5358d-106">Os requisitos de topologia e as considerações para o Lync Server 2013 são diferentes dos requisitos para versões anteriores, conforme descrito nesta seção.</span><span class="sxs-lookup"><span data-stu-id="5358d-106">Topology requirements and considerations for Lync Server 2013 are different from those for earlier releases, as described in this section.</span></span>

<div>

## <a name="new-front-end-pools-architecture"></a><span data-ttu-id="5358d-107">Nova arquitetura de grupos de front-end</span><span class="sxs-lookup"><span data-stu-id="5358d-107">New Front End Pools Architecture</span></span>

<span data-ttu-id="5358d-108">No Lync Server 2013, a arquitetura dos pools de front-end do Enterprise Edition foi alterada para uma arquitetura de sistema distribuído.</span><span class="sxs-lookup"><span data-stu-id="5358d-108">In Lync Server 2013, the architecture of Enterprise Edition Front End pools has changed to a distributed systems architecture.</span></span>

<span data-ttu-id="5358d-109">Com essa nova arquitetura, o banco de dados back-end não é mais o repositório de dados em tempo real em um pool.</span><span class="sxs-lookup"><span data-stu-id="5358d-109">With this new architecture, the Back End database is no longer the real-time data store in a pool.</span></span> <span data-ttu-id="5358d-110">As informações sobre um determinado usuário são mantidas em três servidores front-end no pool.</span><span class="sxs-lookup"><span data-stu-id="5358d-110">Information about a particular user is kept on three Front End Servers in the pool.</span></span> <span data-ttu-id="5358d-111">Para cada usuário, um servidor front-end atua como mestre para as informações do usuário e outros dois servidores front-end servem como réplicas.</span><span class="sxs-lookup"><span data-stu-id="5358d-111">For each user, one Front End Server acts as the master for that user’s information, and two other Front End Servers serve as replicas.</span></span> <span data-ttu-id="5358d-112">Se um servidor front-end for desligado, outro servidor front-end que seja servido como réplica será automaticamente promovido para Master.</span><span class="sxs-lookup"><span data-stu-id="5358d-112">If a Front End Server goes down, another Front End Server which served as a replica is automatically promoted to master.</span></span>

<span data-ttu-id="5358d-113">Isso acontece nos bastidores, e os administradores não precisam saber quais servidores de front-end são os mestres para os quais os usuários.</span><span class="sxs-lookup"><span data-stu-id="5358d-113">This happens behind the scenes, and administrators do not need to know which Front End Servers are the masters for which users.</span></span> <span data-ttu-id="5358d-114">Essa distribuição de armazenamento de dados melhora o desempenho e a escalabilidade dentro do pool e elimina o único ponto de falha de um único servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="5358d-114">This distribution of data storage improves performance and scalability within the pool, and eliminates the single point of failure of a single Back End Server.</span></span>

<span data-ttu-id="5358d-115">O servidor back-end funciona como armazenamento de backup para dados de usuários e de conferências e também é o armazenamento principal para outros bancos de dados, como o banco de dados do grupo de resposta.</span><span class="sxs-lookup"><span data-stu-id="5358d-115">The Back End Server serves as backup storage for user and conference data, and is also the primary storage for other databases such as the Response Group database.</span></span>

<span data-ttu-id="5358d-116">Esses aprimoramentos também significam que há alterações na maneira como você planeja e mantém seus pools.</span><span class="sxs-lookup"><span data-stu-id="5358d-116">These improvements also mean there are changes in how you plan and maintain your pools.</span></span> <span data-ttu-id="5358d-117">Recomendamos que todos os seus pools do front-end do Enterprise Edition incluam pelo menos três servidores front end para fornecer o número total de réplicas para as quais a arquitetura do pool de front-end foi desenvolvida.</span><span class="sxs-lookup"><span data-stu-id="5358d-117">We recommend that all your Enterprise Edition Front End pools include at least three Front End Servers, to provide the full number of replicas that the Front End pool architecture is designed for.</span></span> <span data-ttu-id="5358d-118">Além disso, você deve seguir determinados procedimentos ao adicionar servidores a um pool de front-end, remover servidores dele ou atualizar servidores.</span><span class="sxs-lookup"><span data-stu-id="5358d-118">Additionally, you must follow certain procedures when adding servers to a Front End pool, removing servers from it, or upgrading servers.</span></span> <span data-ttu-id="5358d-119">Para obter mais informações, consulte [topologias e componentes para servidores front-end, mensagens instantâneas e presença no Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span><span class="sxs-lookup"><span data-stu-id="5358d-119">For more information, see [Topologies and components for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span></span>

<div>

## <a name="server-role-topology-changes"></a><span data-ttu-id="5358d-120">Alterações de topologia de função de servidor</span><span class="sxs-lookup"><span data-stu-id="5358d-120">Server Role Topology Changes</span></span>

<span data-ttu-id="5358d-121">Algumas funções de servidor executadas anteriormente em servidores separados agora são consolidadas na função de servidor front-end, permitindo que você economize em custos de hardware</span><span class="sxs-lookup"><span data-stu-id="5358d-121">Some server roles that previously ran on separate servers are now consolidated into the Front End Server role, enabling you to save on hardware costs</span></span>

  - <span data-ttu-id="5358d-122">No Lync Server 2013, o servidor de conferência A/V sempre é posicionado com o servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="5358d-122">In Lync Server 2013, A/V Conferencing Server is always collocated with Front End Server.</span></span>

  - <span data-ttu-id="5358d-123">Os front-ends para monitoramento e arquivamento agora são sempre posicionados com o servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="5358d-123">The front ends for both Monitoring and Archiving are now always collocated with Front End Server.</span></span> <span data-ttu-id="5358d-124">Monitorar e arquivar cada um ainda exige um banco de dados Back-End separado, que pode ser posicionado no mesmo servidor que o banco de dados back-end do pool de front-end, ou pode ser hospedado em servidores Back-End separados.</span><span class="sxs-lookup"><span data-stu-id="5358d-124">Monitoring and Archiving each still require a separate Back-End Database, which can be collocated on the same server as the Front End Pool’s back-end database, or can be hosted on separate Back-End Servers.</span></span>

  - <span data-ttu-id="5358d-125">O servidor de chat persistente agora é uma função de servidor.</span><span class="sxs-lookup"><span data-stu-id="5358d-125">Persistent Chat Server is now a server role.</span></span> <span data-ttu-id="5358d-126">No Microsoft Lync Server 2010, o servidor de chat de grupo era um aplicativo confiável de terceiros para o Microsoft Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="5358d-126">In Microsoft Lync Server 2010, Group Chat Server was a third-party trusted application for Microsoft Lync Server 2010.</span></span> <span data-ttu-id="5358d-127">No Lync Server 2013, a funcionalidade do servidor de chat persistente é implementada usando três novas funções de servidor:</span><span class="sxs-lookup"><span data-stu-id="5358d-127">In Lync Server 2013, Persistent Chat Server functionality is implemented using three new server roles:</span></span>
    
      - <span data-ttu-id="5358d-128">**PersistentChatService:** Principais serviços de servidor de chat persistentes implementados como uma função de front-end</span><span class="sxs-lookup"><span data-stu-id="5358d-128">**PersistentChatService:** Main Persistent Chat Server services implemented as a front end role</span></span>
    
      - <span data-ttu-id="5358d-129">**PersistentChatStore:** Função de servidor back-end</span><span class="sxs-lookup"><span data-stu-id="5358d-129">**PersistentChatStore:** Back End Server role</span></span>
    
      - <span data-ttu-id="5358d-130">**PersistentChatComplianceStore:** Função de servidor back-end para conformidade com o chat persistente</span><span class="sxs-lookup"><span data-stu-id="5358d-130">**PersistentChatComplianceStore:** Back End Server role for Persistent Chat Compliance</span></span>

<span data-ttu-id="5358d-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5358d-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

