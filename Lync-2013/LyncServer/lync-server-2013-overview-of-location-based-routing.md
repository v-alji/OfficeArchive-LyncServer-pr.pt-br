---
title: 'Lync Server 2013: visão geral do roteamento Location-Based'
description: 'Lync Server 2013: visão geral do roteamento do Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing
ms:assetid: 4aa494bd-0d66-4335-b9e8-f758d44a7202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994032(v=OCS.15)
ms:contentKeyID: 51803941
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b1e026791a8562629231b91b58d7e7eff569ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390282"
---
# <a name="overview-of-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="ef1a1-103">Visão geral do roteamento de Location-Based no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ef1a1-103">Overview of Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ef1a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ef1a1-104">

<span> </span></span></span>

<span data-ttu-id="ef1a1-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="ef1a1-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="ef1a1-p101">O roteamento baseado na localização introduz um novo conjunto de regras que modifica o roteamento de chamadas PSTN nacionais e internacionais para evitar desvio de tarifas. O roteamento baseado na localização oferece a flexibilidade para abranger essas regras em regiões específicas, gateways específicos ou somente conjunto de usuários específico.</span><span class="sxs-lookup"><span data-stu-id="ef1a1-p101">Location-Based Routing introduces a new set of rules that modifies the routing of national and international PSTN calls to prevent toll bypass. Location-Based Routing provides the flexibility to scope these rules to specific regions, specific gateways or to specific set of users only.</span></span>

<span data-ttu-id="ef1a1-108">Os cenários a seguir ilustram os principais tipos de restrições Location-Based o roteamento pode impor:</span><span class="sxs-lookup"><span data-stu-id="ef1a1-108">The following scenarios illustrate the main types of restrictions Location-Based Routing can enforce:</span></span>

  - <span data-ttu-id="ef1a1-109">Chamadas de egresso – o roteamento Location-Based pode impor chamadas feitas para egresso a partir de um gateway PSTN localizado na mesma região onde o chamador é para impedir a interchamada PSTN PSTN, o que impede chamadas de saída de um gateway PSTN localizado em uma região diferente como o chamador.</span><span class="sxs-lookup"><span data-stu-id="ef1a1-109">Egress calls – Location-Based Routing can enforce outgoing calls to egress from a PSTN gateway that is located in the same region as where the caller is to prevent PSTN toll bypass, which prevents calls to egress from a PSTN gateway located in a different region as the caller.</span></span>

  - <span data-ttu-id="ef1a1-110">Chamadas de ingresso – o roteamento Location-Based pode evitar chamadas PSTN de entrada para ligar pontos de extremidade do Lync se o gateway PSTN que faz a chamada de entrada não estiver localizado na mesma região que o usuário chamado do Lync.</span><span class="sxs-lookup"><span data-stu-id="ef1a1-110">Ingress calls – Location-Based Routing can prevent incoming PSTN calls to ring Lync endpoints if the PSTN gateway routing the incoming call is not located in the same region as the called Lync user.</span></span>

  - <span data-ttu-id="ef1a1-111">Regiões desconhecidas – o roteamento de Location-Based restringe as chamadas PSTN de entrada e saída para e de usuários localizados em locais indeterminados (ou seja, usuários remotos que se conectam a partir da Internet ou localizados em regiões desconhecidas).</span><span class="sxs-lookup"><span data-stu-id="ef1a1-111">Unknown regions – Location-Based Routing restricts incoming and outgoing PSTN calls to and from users that are located in undetermined locations (i.e. remote users connecting from the Internet or located in unknown regions).</span></span>

  - <span data-ttu-id="ef1a1-112">Regiões internacionais – o roteamento Location-Based reforça o roteamento de chamadas feitas por meio de gateways PSTN internacionais se um gateway local para o local do usuário não puder ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="ef1a1-112">International regions – Location-Based Routing enforces routing of outgoing calls through international PSTN gateways if a gateway local to the user’s location cannot be found.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="ef1a1-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef1a1-113">See Also</span></span>


[<span data-ttu-id="ef1a1-114">Planejamento de Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ef1a1-114">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="ef1a1-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ef1a1-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

