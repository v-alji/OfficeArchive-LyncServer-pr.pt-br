---
title: 'Lync Server 2013: Planejamento de bypass de mídia'
description: 'Lync Server 2013: planejando a bypass de mídia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for media bypass
ms:assetid: 8ac732b6-8538-4d7b-b1a9-2035e419dac2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398703(v=OCS.15)
ms:contentKeyID: 48184768
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d92a50d9d838b0f13fd6837cbfadee1c48712f0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424476"
---
# <a name="planning-for-media-bypass-in-lync-server-2013"></a><span data-ttu-id="eec31-103">Planejamento de bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eec31-103">Planning for media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eec31-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eec31-104">

<span> </span></span></span>

<span data-ttu-id="eec31-105">_**Tópico da última modificação:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="eec31-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="eec31-106">O bypass de mídia se refere a remover o servidor de mediação do caminho de mídia sempre que possível para chamadas cujo sinal percorre o servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="eec31-106">Media bypass refers to removing the Mediation Server from the media path whenever possible for calls whose signaling traverses the Mediation Server.</span></span>

<span data-ttu-id="eec31-107">O bypass de mídia pode aprimorar a qualidade da voz reduzindo a latência, conversões desnecessárias, possibilidade de perda de pacotes e o número de pontos de falha possíveis.</span><span class="sxs-lookup"><span data-stu-id="eec31-107">Media bypass can improve voice quality by reducing latency, needless translation, possibility of packet loss, and the number of points of potential failure.</span></span> <span data-ttu-id="eec31-108">A escalabilidade pode ser aprimorada, pois a eliminação do processamento de mídia para chamadas ignoradas reduz a carga no servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="eec31-108">Scalability can be improved, because elimination of media processing for bypassed calls reduces the load on the Mediation Server.</span></span> <span data-ttu-id="eec31-109">Essa redução na carga complementa a capacidade do servidor de mediação para controlar vários gateways.</span><span class="sxs-lookup"><span data-stu-id="eec31-109">This reduction in load complements the ability of the Mediation Server to control multiple gateways.</span></span>

<span data-ttu-id="eec31-110">Onde um site de filiais sem um servidor de mediação está conectado a um site central por um ou mais links de WAN com largura de banda restrita, o bypass de mídia reduz a necessidade de largura de banda ao permitir que a mídia de um cliente em um site de mediação flua diretamente para seu gateway local, sem antes ter que fluir pelo link de WAN para um servidor de mediação no</span><span class="sxs-lookup"><span data-stu-id="eec31-110">Where a branch site without a Mediation Server is connected to a central site by one or more WAN links with constrained bandwidth, media bypass lowers the bandwidth requirement by allowing media from a client at a branch site to flow directly to its local gateway without first having to flow across the WAN link to a Mediation Server at the central site and back.</span></span>

<span data-ttu-id="eec31-111">Ao enliberar o servidor de mediação do processamento de mídia, o bypass da mídia também pode reduzir o número de servidores de mediação que uma infraestrutura Enterprise Voice requer.</span><span class="sxs-lookup"><span data-stu-id="eec31-111">By relieving the Mediation Server from media processing, media bypass may also reduce the number of Mediation Servers that an Enterprise Voice infrastructure requires.</span></span>

<span data-ttu-id="eec31-112">A figura a seguir exibe caminhos de mídia e sinalização básicos em topologias com e sem bypass de mídia.</span><span class="sxs-lookup"><span data-stu-id="eec31-112">The following figure shows basic media and signaling pathways in topologies with and without media bypass.</span></span>

<span data-ttu-id="eec31-113">**Caminhos de mídia e sinalização com e sem desvio de mídia**</span><span class="sxs-lookup"><span data-stu-id="eec31-113">**Media and signaling pathways with and without media bypass**</span></span>

<span data-ttu-id="eec31-114">![Aplicação de voz do CAC ignorando a imposição de conexão](images/Gg398703.4d66d529-0912-4de1-abec-266f54272eb3(OCS.15).jpg "Aplicação de voz do CAC ignorando a imposição de conexão")</span><span class="sxs-lookup"><span data-stu-id="eec31-114">![Voice CAC Media Bypass Connection Enforcement](images/Gg398703.4d66d529-0912-4de1-abec-266f54272eb3(OCS.15).jpg "Voice CAC Media Bypass Connection Enforcement")</span></span>

<span data-ttu-id="eec31-115">Como regra geral, habilite o bypass de mídia sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="eec31-115">As a general rule, enable media bypass wherever possible.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="eec31-116">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="eec31-116">In This Section</span></span>

  - [<span data-ttu-id="eec31-117">Visão geral do bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eec31-117">Overview of media bypass in Lync Server 2013</span></span>](lync-server-2013-overview-of-media-bypass.md)

  - [<span data-ttu-id="eec31-118">Modos de bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eec31-118">Media bypass modes in Lync Server 2013</span></span>](lync-server-2013-media-bypass-modes.md)

  - [<span data-ttu-id="eec31-119">Bypass de mídia e controle de admissão de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eec31-119">Media bypass and call admission control in Lync Server 2013</span></span>](lync-server-2013-media-bypass-and-call-admission-control.md)

  - [<span data-ttu-id="eec31-120">Requisitos técnicos para bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eec31-120">Technical requirements for media bypass in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-media-bypass.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="eec31-121">Seções Relacionadas</span><span class="sxs-lookup"><span data-stu-id="eec31-121">Related Sections</span></span>

[<span data-ttu-id="eec31-122">Implantação de recursos avançados do Enterprise Voice no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eec31-122">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="eec31-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="eec31-123">See Also</span></span>


[<span data-ttu-id="eec31-124">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eec31-124">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)  


[<span data-ttu-id="eec31-125">Opções de bypass de mídia global no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eec31-125">Global media bypass options in Lync Server 2013</span></span>](lync-server-2013-global-media-bypass-options.md)  
  

<span data-ttu-id="eec31-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eec31-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

