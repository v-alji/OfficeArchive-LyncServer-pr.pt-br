---
title: Pool de diretores em escala - balanceamento de carga de DNS e balanceador de carga de hardware
description: Pool de directors dimensionados-balanceamento de carga de DNS e balanceador de carga de hardware.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scaled Director pool - DNS load balancing and hardware load balancer
ms:assetid: a1f6ffc0-9e6e-4217-a923-025c9679e154
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205142(v=OCS.15)
ms:contentKeyID: 48185023
ms.date: 03/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b30dfcc3515420ffb34343e4653e9518b1b9c3ed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442039"
---
# <a name="scaled-director-pool---dns-load-balancing-and-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="a28f2-103">Pool de diretores em escala - balanceamento de carga de DNS e balanceador de carga de hardware no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a28f2-103">Scaled Director pool - DNS load balancing and hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a28f2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a28f2-104">

<span> </span></span></span>

<span data-ttu-id="a28f2-105">_**Tópico da última modificação:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="a28f2-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="a28f2-106">Um pool de directors em escala, onde há mais de um director implantado para lidar com capacidade adicional e para fornecer alta disponibilidade, requer balanceamento de carga para distribuir a comunicação do cliente e do servidor para todos os membros do pool.</span><span class="sxs-lookup"><span data-stu-id="a28f2-106">A scaled Director pool, where there are more than one Director deployed to handle additional capacity and to provide high availability, requires load balancing to distribute client and server communication to all members of the pool.</span></span> <span data-ttu-id="a28f2-107">Um diretor hospeda serviços Web muito como um pool de front-end.</span><span class="sxs-lookup"><span data-stu-id="a28f2-107">A Director hosts web services much like a Front End pool.</span></span> <span data-ttu-id="a28f2-108">Para fornecer o balanceamento de carga, você pode usar o balanceamento de carga de hardware ou o balanceamento de carga do sistema de nome de domínio (DNS) e o balanceamento de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="a28f2-108">To provide the load balancing, you can use either hardware load balancing or domain name system (DNS) load balancing and hardware load balancing.</span></span> <span data-ttu-id="a28f2-109">O balanceamento de carga de hardware é necessário para os serviços Web, e o balanceamento de carga de DNS sozinha não fornece as funcionalidades necessárias para os serviços Web.</span><span class="sxs-lookup"><span data-stu-id="a28f2-109">Hardware load balancing is required for the web services, and DNS load balancing alone does not provide the capabilities required for the web services.</span></span>

<span data-ttu-id="a28f2-110">Os tópicos a seguir descrevem as considerações de planejamento para a implantação de um pool de directors usando o balanceamento de carga de DNS em conjunto com o balanceamento de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="a28f2-110">The following topics describe the planning considerations for deploying a Director pool using DNS load balancing in conjunction with hardware load balancing.</span></span> <span data-ttu-id="a28f2-111">Se você pretende usar o balanceamento de carga de hardware, mas não o balanceamento de carga de DNS para o pool de diretor, consulte o tópico [pool de diretor de dimensionamento-balanceamento de carga de hardware no Lync Server 2013](lync-server-2013-scaled-director-pool-hardware-load-balancer.md) que descreve os requisitos de planejamento para essa topologia.</span><span class="sxs-lookup"><span data-stu-id="a28f2-111">If you intend to use hardware load balancing, but not DNS load balancing for the Director pool, see the topic [Scaled Director pool - hardware load balancer in Lync Server 2013](lync-server-2013-scaled-director-pool-hardware-load-balancer.md) that describes the planning requirements for that topology.</span></span>

<span data-ttu-id="a28f2-112">![Pool de directors dimensionados](images/JJ205142.35a78a7a-b781-4c8f-951e-168451ba6a65(OCS.15).jpg "Pool de directors dimensionados")</span><span class="sxs-lookup"><span data-stu-id="a28f2-112">![Scaled Director Pool](images/JJ205142.35a78a7a-b781-4c8f-951e-168451ba6a65(OCS.15).jpg "Scaled Director Pool")</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a28f2-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a28f2-113">In This Section</span></span>

  - [<span data-ttu-id="a28f2-114">Resumo de certificado - Cargas de DNS e de HLB balanceadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a28f2-114">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="a28f2-115">Resumo de porta - cargas de DNS e de HLB balanceadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a28f2-115">Port summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-port-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="a28f2-116">Resumo de DNS - Cargas de DNS e de HLB balanceadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a28f2-116">DNS summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-dns-summary-dns-and-hlb-load-balanced.md)

<span data-ttu-id="a28f2-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a28f2-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

