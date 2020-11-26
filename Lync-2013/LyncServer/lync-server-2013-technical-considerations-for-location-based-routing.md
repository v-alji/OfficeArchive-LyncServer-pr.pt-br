---
title: 'Lync Server 2013: Considerações técnicas para Roteamento Baseado em Local'
description: 'Lync Server 2013: considerações técnicas para roteamento de Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical considerations for Location-Based Routing
ms:assetid: 2e2a9199-7c6f-48d3-9adb-3873fc4f8c4e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994027(v=OCS.15)
ms:contentKeyID: 51803936
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54a025af81ab148ad41f95d0a8cf4f900beb7e00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423425"
---
# <a name="technical-considerations-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="c4a4b-103">Considerações técnicas para Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4a4b-103">Technical considerations for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c4a4b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c4a4b-104">

<span> </span></span></span>

<span data-ttu-id="c4a4b-105">_**Tópico da última modificação:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="c4a4b-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="c4a4b-106">Ao planejar Location-Based roteamento, considere o impacto para os cenários a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-106">When planning Location-Based Routing, you should consider the impact to the following scenarios.</span></span>

<div>

## <a name="disaster-recovery"></a><span data-ttu-id="c4a4b-107">Recuperação de desastres</span><span class="sxs-lookup"><span data-stu-id="c4a4b-107">Disaster Recovery</span></span>

<span data-ttu-id="c4a4b-108">Durante um failover do pool primário para um pool de backup e também durante a restauração de operações normais para o pool primário, Location-Based roteamento permanece em vigor a qualquer momento durante um desastre e procedimento de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-108">During a failover from the primary pool to a backup pool as well as when restoring normal operations to the primary pool, Location-Based Routing remains enforced at all times during a disaster and recovery procedure.</span></span>

</div>

<div>

## <a name="survivable-branch-appliance"></a><span data-ttu-id="c4a4b-109">Aparelho de Filial Persistente</span><span class="sxs-lookup"><span data-stu-id="c4a4b-109">Survivable Branch Appliance</span></span>

<span data-ttu-id="c4a4b-110">A configuração do roteamento de Location-Based afeta o planejamento de onde você implanta os gateways associados a seus aparelhos de ramificação sobreviventes.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-110">Configuring Location-Based Routing impacts the planning of where you deploy the gateways associated to your Survivable Branch Appliances.</span></span> <span data-ttu-id="c4a4b-111">O gateway associado a seu SBA deve estar localizado no mesmo site de rede que o seu aparelho de ramificação sobreviventes; caso contrário, os usuários hospedados em seu aparelho de ramificação sobreviventes não terão permissão para fazer chamadas de saída se Location-Based roteamento estiver configurado.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-111">The gateway associated to your SBA must be located in the same network site as your Survivable Branch Appliance; otherwise, users homed on your Survivable Branch Appliance will not be permitted to place outbound calls if Location-Based Routing is configured.</span></span> <span data-ttu-id="c4a4b-112">Quando a conexão de WAN entre seu aparelho de ramificação sobreviventes e o site central está inoperante, Location-Based restrições de roteamento permanecem impostas.</span><span class="sxs-lookup"><span data-stu-id="c4a4b-112">When the WAN connection between your Survivable Branch Appliance and the central site is down, Location-Based Routing restrictions remains enforced.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c4a4b-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4a4b-113">See Also</span></span>


[<span data-ttu-id="c4a4b-114">Planejamento de Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4a4b-114">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="c4a4b-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c4a4b-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

