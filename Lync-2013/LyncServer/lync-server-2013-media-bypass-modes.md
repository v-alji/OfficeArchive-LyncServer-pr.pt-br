---
title: 'Lync Server 2013: Modos de bypass de mídia'
description: 'Lync Server 2013: modos de bypass de mídia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media bypass modes
ms:assetid: 38c06c81-7e45-4423-9e00-7fbfa4befe46
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425862(v=OCS.15)
ms:contentKeyID: 48183898
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a7f1a71930df7ef92a29087f42bdb9382b3904c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425686"
---
# <a name="media-bypass-modes-in-lync-server-2013"></a><span data-ttu-id="fd7c4-103">Modos de bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd7c4-103">Media bypass modes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fd7c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fd7c4-104">

<span> </span></span></span>

<span data-ttu-id="fd7c4-105">_**Tópico da última modificação:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="fd7c4-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="fd7c4-p101">Configure o bypass de mídia globalmente e para cada tronco PSTN individual. Ao habilitar o bypass de mídia globalmente, você tem duas opções: **Sempre ignorar** e **Use Site and Region Information** (Usar informações do site e da região).</span><span class="sxs-lookup"><span data-stu-id="fd7c4-p101">You must configure media bypass both globally and for each individual PSTN trunk. When enabling media bypass globally, you have two choices: **Always Bypass** and **Use Site and Region Information**.</span></span>

<span data-ttu-id="fd7c4-p102">Como o nome sugere, **Sempre ignorar** significa que o bypass será tentado para todas as chamadas de PSTN. **Sempre ignorar** é usado para as implantações em que não há necessidade de ativar o controle de admissão da chamada, e nem de especificar informações detalhadas da configuração de quando tentar o bypass de mídia. Além disso, **Sempre ignorar** é usado quando existe uma conectividade total entre os clientes e os gateways de PSTN. Nesta configuração, todas as sub-redes são mapeadas apenas para um ID de bypass, que é calculado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="fd7c4-p102">As the name suggests, **Always Bypass** means that bypass will be attempted for all PSTN calls. **Always Bypass** is used for deployments where there is no need to enable call admission control, nor is there a need to specify detailed configuration information regarding when to attempt media bypass. Furthermore, **Always Bypass** is used when there is full connectivity between clients and PSTN gateways. In this configuration, all subnets are mapped to one and only one bypass ID, which is computed by the system.</span></span>

<span data-ttu-id="fd7c4-p103">Com **Use Site and Region Information** (Usar informações do site e da região), a ID de bypass é associada à configuração do site e de região usada para tomar a decisão do bypass. Essa configuração fornece a flexibilidade de configurar o bypass para as topologias mais comuns, porque permite um controle refinado de quando o bypass acontece, além de oferecer suporte às interações com o serviço de controle de admissão de chamadas (CAC). O sistema tentar facilitar sua tarefa, atribuindo automaticamente IDs de bypass conforme indicado a seguir.</span><span class="sxs-lookup"><span data-stu-id="fd7c4-p103">With **Use Site and Region Information**, the bypass ID associated with site and region configuration is used to make the bypass decision. This configuration provides the flexibility to configure bypass for most common topologies, as it gives you fine-grained control over when bypass happens, in addition to supporting interactions with call admission control (CAC). The system tries to ease your task by automatically assigning bypass IDs as follows.</span></span>

  - <span data-ttu-id="fd7c4-115">O sistema atribui automaticamente uma única ID de bypass exclusiva para cada região.</span><span class="sxs-lookup"><span data-stu-id="fd7c4-115">The system automatically assigns a single unique bypass ID to each region.</span></span>

  - <span data-ttu-id="fd7c4-116">Qualquer site conectado a uma região via link WAN, sem restrições de largura de banda, herda a mesma ID de bypass que a região.</span><span class="sxs-lookup"><span data-stu-id="fd7c4-116">Any site connected to a region over a WAN link without bandwidth constraints inherits the same bypass ID as the region.</span></span>

  - <span data-ttu-id="fd7c4-117">Um site associado à região via link WAN com largura de banda restrita é atribuído a uma ID de bypass diferente do da região.</span><span class="sxs-lookup"><span data-stu-id="fd7c4-117">A site associated with the region over a WAN link with constrained bandwidth is assigned a different bypass ID from that of the region.</span></span>

  - <span data-ttu-id="fd7c4-118">As sub-redes associadas a cada site herdam a ID de bypass do site.</span><span class="sxs-lookup"><span data-stu-id="fd7c4-118">Subnets associated with each site inherit the bypass ID for that site.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="fd7c4-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd7c4-119">See Also</span></span>


[<span data-ttu-id="fd7c4-120">Visão geral do bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd7c4-120">Overview of media bypass in Lync Server 2013</span></span>](lync-server-2013-overview-of-media-bypass.md)  
[<span data-ttu-id="fd7c4-121">Bypass de mídia e controle de admissão de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd7c4-121">Media bypass and call admission control in Lync Server 2013</span></span>](lync-server-2013-media-bypass-and-call-admission-control.md)  
[<span data-ttu-id="fd7c4-122">Requisitos técnicos para bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd7c4-122">Technical requirements for media bypass in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-media-bypass.md)  
  

<span data-ttu-id="fd7c4-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fd7c4-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

