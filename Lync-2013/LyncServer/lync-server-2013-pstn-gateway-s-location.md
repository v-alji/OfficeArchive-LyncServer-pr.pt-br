---
title: 'Lync Server 2013: Local do gateway PSTN'
description: 'Lync Server 2013: localização do gateway PSTN.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN gateway's location
ms:assetid: 49693a35-fad3-49ee-a71e-c7e4537b79aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994031(v=OCS.15)
ms:contentKeyID: 51803940
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f793249908bd1f064f9038ddd90c7f5b01a61d5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390087"
---
# <a name="pstn-gateways-location-in-lync-server-2013"></a><span data-ttu-id="42ca2-103">Local do gateway PSTN no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42ca2-103">PSTN gateway's location in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42ca2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42ca2-104">

<span> </span></span></span>

<span data-ttu-id="42ca2-105">_**Tópico da última modificação:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="42ca2-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="42ca2-106">Chamadas roteadas por meio de gateways PSTN e PBXs podem exigir restrições de roteamento Location-Based dependendo do local de tais sistemas.</span><span class="sxs-lookup"><span data-stu-id="42ca2-106">Calls routed via PSTN gateways and PBXs might require Location-Based Routing restrictions depending on the location of such systems.</span></span> <span data-ttu-id="42ca2-107">Location-Based roteamento pode ser habilitado na granularidade com base em cada tronco.</span><span class="sxs-lookup"><span data-stu-id="42ca2-107">Location-Based Routing can be enabled at the granularity on a per trunk basis.</span></span>

<span data-ttu-id="42ca2-108">Location-Based roteamento introduz o seguinte conjunto de regras quando habilitado em um tronco:</span><span class="sxs-lookup"><span data-stu-id="42ca2-108">Location-Based Routing introduces the following set of rules when enabled on a trunk:</span></span>

  - <span data-ttu-id="42ca2-109">Quando o roteamento do Location-Based está habilitado em uma base por tronco, as regras definidas nesse tronco serão aplicadas somente a chamadas roteadas por meio desse tronco.</span><span class="sxs-lookup"><span data-stu-id="42ca2-109">When Location-Based Routing is enabled on a per trunk basis, the rules define on that trunk will be applied only to calls routed through that trunk.</span></span>

  - <span data-ttu-id="42ca2-110">Para evitar que as tarifas PSTNs ignorem onde as chamadas são originadas de um site de rede diferente que o site de rede onde o gateway PSTN está localizado, Location-Based roteamento introduz a associação de um site de rede para um determinado tronco.</span><span class="sxs-lookup"><span data-stu-id="42ca2-110">To prevent PSTN tolls bypass where calls originate from a network site different that the network site where the PSTN gateway is located, Location-Based Routing introduces the association of a network site to a given trunk.</span></span> <span data-ttu-id="42ca2-111">Isso definirá o local de rede que permite o encaminhamento de chamadas para um tronco específico.</span><span class="sxs-lookup"><span data-stu-id="42ca2-111">This defines the network site that allows calls to be routed to a given trunk.</span></span>

<span data-ttu-id="42ca2-112">Os troncos podem ser habilitados para roteamento de Location-Based de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="42ca2-112">Trunks can be enabled for Location-Based Routing in two ways:</span></span>

  - <span data-ttu-id="42ca2-p103">O tronco é definido para um gateway PSTN que egressa chamadas para a PSTN. As chamadas de entrada encaminhadas por um tronco desse tipo serão encaminhadas apenas para os pontos de extremidade localizados dentro do mesmo local de rede do tronco.</span><span class="sxs-lookup"><span data-stu-id="42ca2-p103">The trunk is defined for a PSTN gateway that egresses calls to the PSTN. Incoming calls routed by a trunk of this type will be routed only to endpoints located within the same network site as the trunk.</span></span>

  - <span data-ttu-id="42ca2-115">O tronco é definido para um peer do servidor de mediação que não faz chamadas para os usuários de serviços PSTN e PSTN com telefones herdados em locais estáticos (por exemplo, telefones PBX).</span><span class="sxs-lookup"><span data-stu-id="42ca2-115">The trunk is defined for a Mediation Server peer that doesn’t egress calls to the PSTN and services users with legacy phones in a static locations (i.e. PBX phones).</span></span> <span data-ttu-id="42ca2-116">Para essa configuração específica, todas as chamadas de entrada encaminhadas por um tronco desse tipo serão consideradas como originadas do mesmo local de rede do tronco.</span><span class="sxs-lookup"><span data-stu-id="42ca2-116">For this particular configuration, all incoming calls routed by a trunk of this type will be considered to be originating from the same network site as the trunk.</span></span> <span data-ttu-id="42ca2-117">As chamadas de usuários do PBX terão a mesma imposição de roteamento Location-Based como usuários do Lync que estão localizados no mesmo local de rede que o tronco.</span><span class="sxs-lookup"><span data-stu-id="42ca2-117">Calls from PBX users will have the same Location-Based Routing enforcement as Lync users who are located in the same network site as the trunk.</span></span> <span data-ttu-id="42ca2-118">Se dois sistemas PBX localizados em sites de rede separados estiverem conectados pelo Lync Server, Location-Based roteamento permitirá o roteamento de um ponto de extremidade de PBX em um site de rede para outro ponto de extremidade de PBX no outro site de rede.</span><span class="sxs-lookup"><span data-stu-id="42ca2-118">If two PBX systems located in separate network sites are connected through Lync Server, Location-Based Routing will allow routing from one PBX endpoint in one network site to another PBX endpoint in the other network site.</span></span> <span data-ttu-id="42ca2-119">Esse cenário não será bloqueado pelo roteamento Location-Based.</span><span class="sxs-lookup"><span data-stu-id="42ca2-119">This scenario will not be blocked by Location-Based Routing.</span></span> <span data-ttu-id="42ca2-120">Além desse cenário e de maneira semelhante a um usuário do Lync no mesmo local, os pontos de extremidade conectados a um servidor de mediação ponto a ponto com essa configuração poderão fazer ou receber chamadas para e a partir de outros Peers do servidor de mediação que não roteiam chamadas para a PSTN (ou seja, um ponto de extremidade conectado a um PBX diferente) independentemente do site de rede ao qual o peer do servidor de mediação está associado.</span><span class="sxs-lookup"><span data-stu-id="42ca2-120">In addition to this scenario and in a similar way as a Lync user in the same location, endpoints connected to a Mediation Server peer with this configuration will be able to make or receive calls to and from other Mediation Server peer that do not route calls to the PSTN (i.e. an endpoint connected to a different PBX) regardless of the network site to which the Mediation Server peer is associated.</span></span> <span data-ttu-id="42ca2-121">Todas as chamadas recebidas, chamadas de saída, transferências de chamadas e encaminhamentos de chamadas que envolvem pontos de extremidade PSTN estarão sujeitas ao roteamento baseado em localização para usar somente gateways PSTN definidos como locais para o peer do servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="42ca2-121">All inbound calls, outbound calls, call transfers and call forwards involving PSTN endpoints will be subject to Location Based Routing to use only PSTN gateways that are defined as local to such Mediation Server peer.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="42ca2-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="42ca2-122">See Also</span></span>


[<span data-ttu-id="42ca2-123">Orientação para Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42ca2-123">Guidance for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-guidance-for-location-based-routing.md)  
  

<span data-ttu-id="42ca2-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42ca2-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

