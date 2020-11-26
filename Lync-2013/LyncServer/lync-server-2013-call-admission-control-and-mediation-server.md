---
title: 'Lync Server 2013: Controle de admissão de chamada e Servidor de Mediação'
description: 'Lync Server 2013: controle de admissão de chamadas e servidor de mediação.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call admission control and Mediation Server
ms:assetid: 76faccdc-67d0-4c8b-8e47-1e23c93b02c6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398585(v=OCS.15)
ms:contentKeyID: 48184546
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 77e4b12a11f941923d50f3ffcab7a8f9b6a9edc5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435926"
---
# <a name="call-admission-control-and-mediation-server-in-lync-server-2013"></a><span data-ttu-id="2b4ca-103">Controle de admissão de chamada e Servidor de Mediação no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b4ca-103">Call admission control and Mediation Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b4ca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b4ca-104">

<span> </span></span></span>

<span data-ttu-id="2b4ca-105">_**Tópico da última modificação:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="2b4ca-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="2b4ca-106">O controle de admissão de chamadas (CAC), apresentado primeiro no Lync Server 2010, gerencia a determinação da sessão em tempo real, com base na largura de banda disponível, para ajudar a evitar má qualidade da experiência (QoE) para usuários em redes congestionadas.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-106">Call admission control (CAC), first introduced in Lync Server 2010, manages real-time session establishment, based on available bandwidth, to help prevent poor Quality of Experience (QoE) for users on congested networks.</span></span> <span data-ttu-id="2b4ca-107">Para dar suporte a esse recurso, o servidor de mediação, que fornece sinalização e conversão de mídia entre a infraestrutura Enterprise Voice e um provedor de entroncamento SIP ou gateway, é responsável pelo gerenciamento de largura de banda para suas duas interações no lado do Lync Server e no lado do gateway.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-107">To support this capability, the Mediation Server, which provides signaling and media translation between the Enterprise Voice infrastructure and a gateway or SIP trunking provider, is responsible for bandwidth management for its two interactions on the Lync Server side and on the gateway side.</span></span> <span data-ttu-id="2b4ca-108">No controle de admissão de chamadas, a entidade de terminação de uma chamada lida com a reserva de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-108">In call admission control, the terminating entity for a call handles the bandwidth reservation.</span></span> <span data-ttu-id="2b4ca-109">Os pares de gateway (gateway PSTN, IP-PBX, SBC) com o qual o servidor de mediação interage no lado do gateway não dão suporte ao controle de admissão de chamadas do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-109">The gateway peers (PSTN gateway, IP-PBX, SBC) that the Mediation Server interacts with on the gateway side do not support Lync Server 2013 call admission control.</span></span> <span data-ttu-id="2b4ca-110">Portanto, o servidor de mediação precisa manipular interações de largura de banda em nome de seu peer de gateway.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-110">Thus, the Mediation Server has to handle bandwidth interactions on behalf of its gateway peer.</span></span> <span data-ttu-id="2b4ca-111">Sempre que possível, o servidor de mediação reservará largura de banda antecipadamente.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-111">Whenever possible, the Mediation Server will reserve bandwidth in advance.</span></span> <span data-ttu-id="2b4ca-112">Se isso não for possível (por exemplo, se a localidade do ponto de extremidade de mídia final no lado do gateway for desconhecido de uma chamada de saída para o par de gateway), a largura de banda será reservada quando a chamada for feita.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-112">If that is not possible (for example, if the locality of the ultimate media endpoint on the gateway side is unknown for an outgoing call to the gateway peer), bandwidth is reserved when the call is placed.</span></span> <span data-ttu-id="2b4ca-113">Esse comportamento poderá resultar em uma inscrição em excesso de assinatura da largura de banda, mas é a única maneira de impedir anéis falsos.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-113">This behavior can result in oversubscription of bandwidth, but it is the only way to prevent false rings.</span></span>

<span data-ttu-id="2b4ca-114">O bypass de mídia e a reserva de largura de banda são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-114">Media bypass and bandwidth reservation are mutually exclusive.</span></span> <span data-ttu-id="2b4ca-115">Se um bypass de mídia for empregado para uma chamada, o controle de admissão de chamadas não será executado para essa chamada.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-115">If a media bypass is employed for a call, call admission control is not performed for that call.</span></span> <span data-ttu-id="2b4ca-116">Presume-se que não haja links envolvidos na chamada com a largura de banda restrita.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-116">The assumption here is that there are no links with constrained bandwidth involved in the call.</span></span> <span data-ttu-id="2b4ca-117">Se o controle de admissão de chamadas for usado para uma chamada específica que envolva o servidor de mediação, essa chamada não poderá empregar o bypass de mídia.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-117">If call admission control is used for a particular call that involves the Mediation Server, that call cannot employ media bypass.</span></span>

<span data-ttu-id="2b4ca-118">Para obter detalhes sobre o bypass de mídia ou o controle de admissão de chamadas, consulte [planejando a bypass de mídia no Lync server 2013](lync-server-2013-planning-for-media-bypass.md) ou [planejando o controle de admissão de chamadas no Lync Server 2013](lync-server-2013-planning-for-call-admission-control.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-118">For details about media bypass or call admission control, see [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) or [Planning for call admission control in Lync Server 2013](lync-server-2013-planning-for-call-admission-control.md) in the Planning documentation.</span></span>

<span data-ttu-id="2b4ca-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b4ca-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

