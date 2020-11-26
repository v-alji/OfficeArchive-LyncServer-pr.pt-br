---
title: 'Lync Server 2013: Planejamento para emparelhamento de pool Front-End'
description: 'Lync Server 2013: planejando o emparelhamento do pool de front-ends.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Front End pool pairing
ms:assetid: cca5773d-57ff-45ce-a7b4-f82ae697c477
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205293(v=OCS.15)
ms:contentKeyID: 48185508
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ac235cf682e286132836e13b34b457adf2bfc233
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424559"
---
# <a name="planning-for-front-end-pool-pairing-in-lync-server-2013"></a><span data-ttu-id="6cd77-103">Planejamento para emparelhamento de pool Front-End no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6cd77-103">Planning for Front End pool pairing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6cd77-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6cd77-104">

<span> </span></span></span>

<span data-ttu-id="6cd77-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="6cd77-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="6cd77-106">Para obter os melhores recursos de recuperação de desastre no Lync Server 2013, implante pares de pools front-end em dois locais geograficamente dispersos.</span><span class="sxs-lookup"><span data-stu-id="6cd77-106">For the best disaster recovery abilities in Lync Server 2013, deploy pairs of Front End pools across two geographically dispersed sites.</span></span> <span data-ttu-id="6cd77-107">Cada site contém um pool de front-ends que está emparelhado com um pool de front-end correspondente no outro site.</span><span class="sxs-lookup"><span data-stu-id="6cd77-107">Each site contains a Front End pool which is paired with a corresponding Front End pool in the other site.</span></span> <span data-ttu-id="6cd77-108">Os dois sites estão ativos e o serviço de backup do Lync Server fornece replicação de dados em tempo real para manter os pools sincronizados.</span><span class="sxs-lookup"><span data-stu-id="6cd77-108">Both sites are active, and the Lync Server Backup Service provides real-time data replication to keep the pools synchronized.</span></span> <span data-ttu-id="6cd77-109">O serviço de backup é um novo recurso do Lync Server 2013, projetado para dar suporte à solução de recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="6cd77-109">The Backup Service is a new feature in Lync Server 2013, designed to support the disaster recovery solution.</span></span> <span data-ttu-id="6cd77-110">Ele é instalado em um pool de front-ends quando você emparelha o pool com outro pool de front-end.</span><span class="sxs-lookup"><span data-stu-id="6cd77-110">It is installed on a Front End pool when you pair the pool with another Front End pool.</span></span>

<span data-ttu-id="6cd77-111">Se o pool em um site falhar, você poderá fazer failover dos usuários desse pool para o pool no outro site, que fornece serviços a todos os usuários em ambos os pools.</span><span class="sxs-lookup"><span data-stu-id="6cd77-111">If the pool in one site fails, you can fail over the users from that pool to the pool in the other site, which then provides services to all the users in both pools.</span></span> <span data-ttu-id="6cd77-112">Para fins de planejamento da capacidade, cada pool deve ser projetado para lidar com as cargas de trabalho de todos os usuários em ambos os pools, no caso de um desastre.</span><span class="sxs-lookup"><span data-stu-id="6cd77-112">For capacity planning purposes, each pool should be designed to handle the workloads of all users in both pools in the event of a disaster.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6cd77-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6cd77-113">In This Section</span></span>

  - [<span data-ttu-id="6cd77-114">Opções de emparelhamento de pool compatível e práticas recomendadas para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6cd77-114">Supported pool pairing options and best practices for Lync Server 2013</span></span>](lync-server-2013-supported-pool-pairing-options-and-best-practices.md)

  - [<span data-ttu-id="6cd77-115">Relacionamentos de Registradores de backup no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6cd77-115">Backup Registrar relationships in Lync Server 2013</span></span>](lync-server-2013-backup-registrar-relationships.md)

  - [<span data-ttu-id="6cd77-116">Tempo de recuperação para failover e failback de pool no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6cd77-116">Recovery time for pool failover and pool failback in Lync Server 2013</span></span>](lync-server-2013-recovery-time-for-pool-failover-and-pool-failback.md)

  - [<span data-ttu-id="6cd77-117">Failover do repositório do Gerenciamento Central no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6cd77-117">Central Management store failover in Lync Server 2013</span></span>](lync-server-2013-central-management-store-failover.md)

  - [<span data-ttu-id="6cd77-118">Segurança de dados de emparelhamento do pool Front End no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6cd77-118">Front End pool pairing data security in Lync Server 2013</span></span>](lync-server-2013-front-end-pool-pairing-data-security.md)

<span data-ttu-id="6cd77-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6cd77-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

