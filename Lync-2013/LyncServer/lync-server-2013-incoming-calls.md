---
title: 'Lync Server 2013: Chamadas de entrada'
description: 'Lync Server 2013: chamadas recebidas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Incoming calls
ms:assetid: 65b9c1b4-6af7-4527-8c33-22c4442bd209
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994038(v=OCS.15)
ms:contentKeyID: 51803948
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a72c7fc378240f9751eae8e6c24e9cc601b08d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427296"
---
# <a name="incoming-calls-in-lync-server-2013"></a><span data-ttu-id="ac38f-103">Chamadas de entrada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ac38f-103">Incoming calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ac38f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ac38f-104">

<span> </span></span></span>

<span data-ttu-id="ac38f-105">_**Tópico da última modificação:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="ac38f-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="ac38f-106">O roteamento de chamadas de entrada para usuários habilitados para roteamento Location-Based depende do local do ponto de extremidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="ac38f-106">The routing of incoming calls to users enabled for Location-Based Routing depends on the location of the user’s endpoint.</span></span> <span data-ttu-id="ac38f-107">Veja a seguir como o roteamento das chamadas de entrada é afetado.</span><span class="sxs-lookup"><span data-stu-id="ac38f-107">The routing of incoming calls is affected in the following way.</span></span> <span data-ttu-id="ac38f-108">Se um usuário tiver uma chamada de entrada para um ponto de extremidade localizado em um site de rede de roteamento Location-Based habilitado e o ponto de extremidade estiver localizado no mesmo site de rede que o gateway PSTN, a chamada será roteada.</span><span class="sxs-lookup"><span data-stu-id="ac38f-108">If a user has an incoming call to an endpoint located in a Location-Based Routing enabled network site, and the endpoint is located in the same network site as the PSTN gateway, the call will be routed.</span></span> <span data-ttu-id="ac38f-109">Se um usuário tiver uma chamada de entrada para um ponto de extremidade localizado em um site de rede de roteamento Location-Based habilitado e o ponto de extremidade estiver localizado em um site de rede diferente do gateway PSTN, a chamada não será roteada.</span><span class="sxs-lookup"><span data-stu-id="ac38f-109">If a user has an incoming call to an endpoint located in a Location-Based Routing enabled network site, and the endpoint is located in a different network site than the PSTN gateway, the call will not be routed.</span></span> <span data-ttu-id="ac38f-110">Quando um usuário não tiver pontos de extremidade localizados no mesmo local de rede do gateway PSTN do qual a chamada de entrada é originada, a chamada de entrada será encaminhada diretamente para o correio de voz do usuário e uma notificação de chamada perdida será enviada para a parte chamada.</span><span class="sxs-lookup"><span data-stu-id="ac38f-110">When a user has no endpoints located in the same network site as the PSTN gateway where the incoming call is originating from, the incoming call will be routed directly to the user’s voicemail and a missed call notification will be sent to the called party.</span></span>

<span data-ttu-id="ac38f-111">As configurações de encaminhamento de chamadas de um usuário habilitado para Location-Based roteamento continuarão a ser impostas, entretanto, as chamadas encaminhadas estarão sujeitas a Location-Based restrições de roteamento do usuário.</span><span class="sxs-lookup"><span data-stu-id="ac38f-111">The call forwarding settings of a user that is enabled for Location-Based Routing will continue to be enforced, however, calls forwarded will be subject to Location-Based Routing restrictions of the user.</span></span>

<span data-ttu-id="ac38f-112">A tabela a seguir ilustra como Location-Based o roteamento afeta o roteamento de chamadas recebidas dependendo da localização do ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="ac38f-112">The following table illustrates how Location-Based Routing affects the routing of inbound calls depending on the location of the callee’s endpoint.</span></span> <span data-ttu-id="ac38f-113">O site de rede do gateway PSTN está habilitado para roteamento Location-Based e Location-Based o roteamento somente permite o roteamento de chamadas PSTN para pontos de extremidade dentro do mesmo site de rede.</span><span class="sxs-lookup"><span data-stu-id="ac38f-113">The network site of the PSTN gateway is enabled for Location-Based Routing, and Location-Based Routing only permits routing of PSTN calls to endpoints within the same network site.</span></span>

### <a name="callee-receiving-an-inbound-call-from-the-pstn"></a><span data-ttu-id="ac38f-114">O destinatário da chamada recebe uma chamada de entrada da PSTN</span><span class="sxs-lookup"><span data-stu-id="ac38f-114">Callee receiving an inbound call from the PSTN</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ac38f-115">O ponto de extremidade do destinatário da chamada está localizado no mesmo local de rede do gateway PSTN</span><span class="sxs-lookup"><span data-stu-id="ac38f-115">Callee’s endpoint located in the same network site as PSTN gateway</span></span></th>
<th><span data-ttu-id="ac38f-116">O ponto de extremidade do destinatário da chamada não fica no mesmo local de rede que o gateway PSTN</span><span class="sxs-lookup"><span data-stu-id="ac38f-116">Callee’s endpoint not located in the same network site as PSTN gateway</span></span></th>
<th><span data-ttu-id="ac38f-117">O ponto de extremidade do destinatário da chamada está localizado em um local de rede desconhecido ou não habilitado para Roteamento Baseado na Localização</span><span class="sxs-lookup"><span data-stu-id="ac38f-117">Callee’s endpoint located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac38f-118">Roteamento da chamada PSTN recebida</span><span class="sxs-lookup"><span data-stu-id="ac38f-118">Routing of inbound PSTN call</span></span></p></td>
<td><p><span data-ttu-id="ac38f-119">A chamada de entrada é encaminhada para os pontos de extremidade do destinatário da chamada</span><span class="sxs-lookup"><span data-stu-id="ac38f-119">Incoming call is routed to callee’s endpoints</span></span></p></td>
<td><p><span data-ttu-id="ac38f-120">A chamada de entrada não é encaminhada para os pontos de extremidade do destinatário da chamada</span><span class="sxs-lookup"><span data-stu-id="ac38f-120">Incoming call is not routed to callee’s endpoints</span></span></p></td>
<td><p><span data-ttu-id="ac38f-121">A chamada de entrada não é encaminhada para os pontos de extremidade do destinatário da chamada</span><span class="sxs-lookup"><span data-stu-id="ac38f-121">Incoming call is not routed to callee’s endpoints</span></span></p></td>
</tr>
</tbody>
</table>

  

<div>

## <a name="see-also"></a><span data-ttu-id="ac38f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac38f-122">See Also</span></span>


[<span data-ttu-id="ac38f-123">Cenários para Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ac38f-123">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="ac38f-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ac38f-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

