---
title: 'Lync Server 2013: Planejamento de Roteamento Baseado em Local'
description: 'Lync Server 2013: planejando para Location-Based roteamento.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Location-Based Routing
ms:assetid: bb035924-6b52-4f0f-8e05-b76864fb9ef3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994068(v=OCS.15)
ms:contentKeyID: 51803979
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 894a596e998fe07b97ad7911441eced670ba85b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442947"
---
# <a name="planning-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="46042-103">Planejamento de Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46042-103">Planning for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="46042-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="46042-104">

<span> </span></span></span>

<span data-ttu-id="46042-105">_**Tópico da última modificação:** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="46042-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="46042-106">A informação neste tópico está relacionada às Atualizações Cumulativas para Lync Server 2013: Fevereiro de 2013.</span><span class="sxs-lookup"><span data-stu-id="46042-106">The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.</span></span>

<span data-ttu-id="46042-107">Location-Based o roteamento torna possível restringir o roteamento de chamadas entre pontos de extremidade VoIP e pontos de extremidade PSTN com base no local das partes na chamada.</span><span class="sxs-lookup"><span data-stu-id="46042-107">Location-Based Routing makes it possible to restrict the routing of calls between VoIP endpoints and PSTN endpoints based on the location of the parties in the call.</span></span> <span data-ttu-id="46042-108">Location-Based roteamento faz parte da infraestrutura do Lync Server 2013 Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="46042-108">Location-Based Routing is part of the Lync Server 2013 Enterprise Voice infrastructure.</span></span> <span data-ttu-id="46042-109">Location-Based o roteamento é um recurso de gerenciamento de chamadas que controla como as chamadas são roteadas pelo Lync Server 2013 CU1.</span><span class="sxs-lookup"><span data-stu-id="46042-109">Location-Based Routing is a call management feature that controls how calls are routed by Lync Server 2013 CU1.</span></span> <span data-ttu-id="46042-110">Ele impõe regras de autorização de chamadas se as chamadas podem ser roteadas para os pontos de extremidade PBX ou PSTN com base na localização geográfica do chamador do Lync.</span><span class="sxs-lookup"><span data-stu-id="46042-110">It enforces call authorization rules on whether calls can be routed to PBX or PSTN endpoints based on the Lync caller’s geographic location.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="46042-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="46042-111">In This Section</span></span>

  - [<span data-ttu-id="46042-112">Visão geral do roteamento de Location-Based no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46042-112">Overview of Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-overview-of-location-based-routing.md)

  - [<span data-ttu-id="46042-113">Orientação para Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46042-113">Guidance for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-guidance-for-location-based-routing.md)

  - [<span data-ttu-id="46042-114">Cenários para Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46042-114">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)

  - [<span data-ttu-id="46042-115">Considerações técnicas para Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46042-115">Technical considerations for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-technical-considerations-for-location-based-routing.md)

  - [<span data-ttu-id="46042-116">Suporte a cliente e servidor para Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46042-116">Client and server support for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-client-and-server-support-for-location-based-routing.md)

  - [<span data-ttu-id="46042-117">Recursos não suportados pelo Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46042-117">Capabilities not supported by Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-capabilities-not-supported-by-location-based-routing.md)

  - [<span data-ttu-id="46042-118">Processo de implantação para Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46042-118">Deployment process for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-location-based-routing.md)

  - [<span data-ttu-id="46042-119">Roteamento baseado em local para conferências no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46042-119">Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-location-based-routing-for-conferencing.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="46042-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="46042-120">See Also</span></span>


[<span data-ttu-id="46042-121">Planejando para Enterprise Voice no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46042-121">Planning for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice.md)  
  

<span data-ttu-id="46042-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="46042-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

