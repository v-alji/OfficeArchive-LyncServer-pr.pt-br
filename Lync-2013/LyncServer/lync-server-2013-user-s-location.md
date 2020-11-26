---
title: 'Lync Server 2013: Local do usuário'
description: 'Lync Server 2013: local do usuário.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User's location
ms:assetid: ce57941d-086b-448e-8ada-c7d636a2a1c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994073(v=OCS.15)
ms:contentKeyID: 51803984
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a92ec780809cdb3e1ee582ce6c348c884bbb5890
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439167"
---
# <a name="users-location-in-lync-server-2013"></a><span data-ttu-id="cf3c2-103">Local do usuário no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf3c2-103">User's location in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cf3c2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cf3c2-104">

<span> </span></span></span>

<span data-ttu-id="cf3c2-105">_**Tópico da última modificação:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="cf3c2-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="cf3c2-106">O roteamento de Location-Based aproveita as mesmas regiões de rede, sites e sub-redes, conforme definido no Lync Server usado pelo E9-1-1, CAC e bypass de mídia para aplicar restrições de roteamento de chamadas para impedir o bypass de chamada PSTN.</span><span class="sxs-lookup"><span data-stu-id="cf3c2-106">Location-Based Routing leverages the same network regions, sites and subnets as defined in Lync Server used by E9-1-1, CAC and Media Bypass to apply call routing restrictions to prevent PSTN toll bypass.</span></span> <span data-ttu-id="cf3c2-107">A localização de um usuário é determinada pela sub-rede IP do (s) ponto (s) do Lync do usuário está conectado (s).</span><span class="sxs-lookup"><span data-stu-id="cf3c2-107">A user’s location is determined by the IP subnet of the user’s Lync endpoint(s) are connected from.</span></span> <span data-ttu-id="cf3c2-108">Cada sub-rede IP está associada a um local de rede que, por sua vez, está agregado a regiões de rede definidas pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="cf3c2-108">Each IP subnet is associated to a network site, which are aggregated into network regions defined by the administrator.</span></span> <span data-ttu-id="cf3c2-109">O Roteamento Baseado na Localização é imposto com base no local de rede do usuário.</span><span class="sxs-lookup"><span data-stu-id="cf3c2-109">Location-Based Routing is enforced based on the user’s network site.</span></span>

<span data-ttu-id="cf3c2-110">Location-Based regras de roteamento são aplicadas por site de rede, o que significa que um determinado conjunto de regras será aplicado a todos os pontos de extremidade habilitados para Location-Based roteamento localizado dentro do mesmo local de rede.</span><span class="sxs-lookup"><span data-stu-id="cf3c2-110">Location-Based Routing rules are applied on a per network site basis, meaning that a given set of rules will be applied to all endpoints enabled for Location-Based Routing that are located within the same network site.</span></span> <span data-ttu-id="cf3c2-111">Os administradores podem aplicar o Roteamento Baseado na Localização aos locais de rede que necessitarem dele.</span><span class="sxs-lookup"><span data-stu-id="cf3c2-111">Administrators can apply Location-Based Routing to network sites that require it.</span></span>

<span data-ttu-id="cf3c2-112">As políticas de roteamento de voz podem ser definidas por local de rede a fim de determinar um gateway PSTN específico que deve ser usado por todos os usuários localizados no local de rede para chamar números de telefone PSTN.</span><span class="sxs-lookup"><span data-stu-id="cf3c2-112">Voice routing policies can be defined on a per network site basis to define a particular PSTN gateway that should be used by all users located in the network site to call PSTN phone numbers.</span></span> <span data-ttu-id="cf3c2-113">Essas políticas de roteamento de voz terão precedência sobre o roteamento definido pela política de voz do usuário quando o usuário estiver localizado em um site de rede habilitado para roteamento Location-Based, e ele impedirá o roteamento de chamadas por meio de outros gateways PSTN habilitados para Location-Based roteamento.</span><span class="sxs-lookup"><span data-stu-id="cf3c2-113">Such voice routing policies will take precedence over the routing defined by the user’s voice policy when the user is located in a network site enabled for Location-Based Routing, and it will prevent the routing of calls via other PSTN gateways that are enabled for Location-Based Routing.</span></span> <span data-ttu-id="cf3c2-114">Quando um usuário do Lync coloca uma chamada PSTN, a política de voz do usuário determina se o usuário pode ser autorizado a fazer a chamada.</span><span class="sxs-lookup"><span data-stu-id="cf3c2-114">When a Lync user places a PSTN call, the user’s voice policy determines whether the user can be authorized to place the call.</span></span> <span data-ttu-id="cf3c2-115">Se a política de voz do usuário permitir que o usuário faça a chamada, Location-Based roteamento determinará o gateway PSTN do qual a chamada deve fazer a saída.</span><span class="sxs-lookup"><span data-stu-id="cf3c2-115">If the user’s voice policy allows the user to place the call, Location-Based Routing determines which PSTN gateway the call should egress from.</span></span> <span data-ttu-id="cf3c2-116">Location-Based o roteamento faz essa determinação com base na localização do usuário.</span><span class="sxs-lookup"><span data-stu-id="cf3c2-116">Location-Based Routing makes this determination based on the user’s location.</span></span>

<span data-ttu-id="cf3c2-117">O local de um usuário pode ser categorizado das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="cf3c2-117">A user location can be categorized in the following ways:</span></span>

  - <span data-ttu-id="cf3c2-118">O usuário está localizado em um site de rede conhecido habilitado para roteamento de Location-Based e seu número DID (Direct Inward Dial) termina em um gateway PSTN colocado no mesmo local de rede (por exemplo, Office).</span><span class="sxs-lookup"><span data-stu-id="cf3c2-118">The user is located in a known network site enabled for Location-Based Routing and his DID (Direct Inward Dial) number terminates on a PSTN gateway placed in the same network site (i.e. office).</span></span> <span data-ttu-id="cf3c2-119">O roteamento das chamadas de saída será feito pela política de roteamento de voz do local de rede em que o usuário está localizado.</span><span class="sxs-lookup"><span data-stu-id="cf3c2-119">The routing of outbound calls will be through the voice routing policy of the network site in which the user is located.</span></span> <span data-ttu-id="cf3c2-120">As chamadas PSTN de entrada para o usuário serão encaminhadas para pontos de extremidade localizados no mesmo local de rede do gateway PSTN.</span><span class="sxs-lookup"><span data-stu-id="cf3c2-120">Incoming PSTN calls to the user are routed to endpoints that are located in the same network site as the PSTN gateway.</span></span>

  - <span data-ttu-id="cf3c2-p105">O usuário está em um local de rede conhecido que fica em um local de rede diferente do gateway PSTN (isto é, o usuário viajou para outro escritório da empresa). O roteamento das chamadas de saída será feito pela política de roteamento de voz do local de rede em que o usuário está localizado. As chamadas PSTN de entrada para o usuário não serão encaminhadas para pontos de extremidade localizados em locais diferentes do gateway PSTN a fim de impedir bypass das chamadas tarifadas PSTN.</span><span class="sxs-lookup"><span data-stu-id="cf3c2-p105">The user is located in a known network site that is in different from the network site where the PSTN gateway is located. (i.e. the user traveled to another corporate office). The routing of outbound calls will be using the voice routing policy of the network site in which the user is located. Incoming PSTN calls to the user will not be routed to endpoints that are located in different sites than the PSTN gateway to prevent PSTN toll bypassing.</span></span>

  - <span data-ttu-id="cf3c2-125">Quando um usuário está localizado em um site de rede desconhecido para a implantação do Lync Server, o roteamento de chamadas de saída será baseado na política de voz atribuída ao usuário a gateways PSTN não associados a Location-Based restrições de roteamento.</span><span class="sxs-lookup"><span data-stu-id="cf3c2-125">When a user is located in a network site that is unknown to the Lync Server deployment, the routing of outbound calls will be based on the voice policy assigned to the user to PSTN gateways not bound to Location-Based Routing restrictions.</span></span> <span data-ttu-id="cf3c2-126">As chamadas PSTN de entrada não serão encaminhadas para os pontos de extremidade localizados em locais de rede desconhecidos a fim de impedir bypass de chamadas tarifadas PSTN.</span><span class="sxs-lookup"><span data-stu-id="cf3c2-126">Incoming PSTN calls will not be routed to endpoints that are located in unknown network sites to prevent PSTN toll bypassing.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="cf3c2-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf3c2-127">See Also</span></span>


[<span data-ttu-id="cf3c2-128">Orientação para Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf3c2-128">Guidance for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-guidance-for-location-based-routing.md)  
  

<span data-ttu-id="cf3c2-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cf3c2-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

