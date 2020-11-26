---
title: 'Lync Server 2013: Sites'
description: Sites do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Sites
ms:assetid: 022cb6dd-37e2-4882-a53e-5ddfdbc6f53a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398076(v=OCS.15)
ms:contentKeyID: 48183233
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59739c5a81fca1f1f3ab5c1b83a23f0be0a5ee2d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423796"
---
# <a name="lync-server-sites-for-lync-server-2013"></a><span data-ttu-id="ad33b-103">Sites do Lync Server no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad33b-103">Lync Server sites for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ad33b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ad33b-104">

<span> </span></span></span>

<span data-ttu-id="ad33b-105">_**Tópico da última modificação:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="ad33b-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="ad33b-106">No Lync Server, você define *sites* em sua rede que contenham componentes do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ad33b-106">In Lync Server, you define *sites* on your network that contain Lync Server components.</span></span> <span data-ttu-id="ad33b-107">Um site é um conjunto de computadores conectados por meio de uma rede de alta velocidade e baixa latência, como uma rede local (LAN), ou de duas redes conectadas por uma rede de fibra ótica de alta velocidade.</span><span class="sxs-lookup"><span data-stu-id="ad33b-107">A site is a set of computers that is well-connected by a high-speed, low-latency network, such as a single local area network (LAN) or two networks connected by a high-speed fiber optic network.</span></span> <span data-ttu-id="ad33b-108">Observe que os sites do Lync Server são um conceito separado dos sites dos serviços de domínio Active Directory e dos sites do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ad33b-108">Note that Lync Server sites are a separate concept from Active Directory Domain Services sites and Microsoft Exchange Server sites.</span></span> <span data-ttu-id="ad33b-109">Seus sites do Lync Server não precisam corresponder a seus sites do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ad33b-109">Your Lync Server sites do not need to correspond to your Active Directory sites.</span></span>

<div>

## <a name="site-types"></a><span data-ttu-id="ad33b-110">Tipos de site</span><span class="sxs-lookup"><span data-stu-id="ad33b-110">Site Types</span></span>

<span data-ttu-id="ad33b-111">Cada site é um *site central*, que contém pelo menos um pool de front-end ou um servidor Standard Edition, ou um *site de filial*.</span><span class="sxs-lookup"><span data-stu-id="ad33b-111">Each site is either a *central site*, which contains at least one Front End pool or a Standard Edition server, or a *branch site*.</span></span> <span data-ttu-id="ad33b-112">Cada site de filial está associado a exatamente um site central, e os usuários no site de filial obtêm a maior parte da funcionalidade do Lync Server dos servidores no site central associado.</span><span class="sxs-lookup"><span data-stu-id="ad33b-112">Each branch site is associated with exactly one central site, and the users at the branch site get most of their Lync Server functionality from the servers at the associated central site.</span></span>

<span data-ttu-id="ad33b-113">Cada site de filial contém um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="ad33b-113">Each branch site contains one of the following:</span></span>

  - <span data-ttu-id="ad33b-114">Um *aparelho de ramificação sobreviventes (SBA)*, que é um servidor blade padrão do setor com um registrador do Lync Server e um servidor de mediação em execução no Windows Server.</span><span class="sxs-lookup"><span data-stu-id="ad33b-114">A *Survivable Branch Appliance (SBA)*, which is an industry-standard blade server with a Lync Server Registrar and a Mediation Server running on Windows Server.</span></span> <span data-ttu-id="ad33b-115">O aparelho de ramificação sobreviventes também contém um gateway PSTN (rede telefônica pública comutada).</span><span class="sxs-lookup"><span data-stu-id="ad33b-115">The Survivable Branch Appliance also contains a public switched telephone network (PSTN) gateway.</span></span> <span data-ttu-id="ad33b-116">O aparelho de ramificação sobreviventes foi projetado para sites de filiais com entre 25 e 1000 usuários.</span><span class="sxs-lookup"><span data-stu-id="ad33b-116">The Survivable Branch Appliance is designed for branch sites with between 25 and 1000 users.</span></span>

  - <span data-ttu-id="ad33b-117">Um *servidor de ramificação sobreviventes (SBS)*, que é um servidor que executa o Windows Server e atende aos requisitos de hardware especificado e que tem o software do Lync Server registrador e do servidor de mediação instalado nele.</span><span class="sxs-lookup"><span data-stu-id="ad33b-117">A *Survivable Branch Server (SBS)*, which is a server running Windows Server that meets specified hardware requirements, and that has Lync Server Registrar and Mediation Server software installed on it.</span></span> <span data-ttu-id="ad33b-118">Ele deve estar conectado a um provedor de serviços telefônicos por meio de um gateway PSTN ou de um tronco SIP.</span><span class="sxs-lookup"><span data-stu-id="ad33b-118">It must connect to either a PSTN gateway or a SIP trunk to a telephone service provider.</span></span> <span data-ttu-id="ad33b-119">O servidor de ramificação sobreviventes foi projetado para sites de filiais com os usuários do 1000 e do 5000.</span><span class="sxs-lookup"><span data-stu-id="ad33b-119">The Survivable Branch Server is designed for branch sites with between 1000 and 5000 users.</span></span>

  - <span data-ttu-id="ad33b-120">Um gateway PSTN e, opcionalmente, um *servidor de mediação*.</span><span class="sxs-lookup"><span data-stu-id="ad33b-120">A PSTN gateway, and, optionally, a *Mediation Server*.</span></span> <span data-ttu-id="ad33b-121">Para obter detalhes sobre essa e outras funções de servidor, consulte [funções de servidor no Lync server 2013](lync-server-2013-server-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ad33b-121">For details on this and other server roles, see [Server roles in Lync Server 2013](lync-server-2013-server-roles.md).</span></span>

<span data-ttu-id="ad33b-122">Uma filial com um link de rede de longa distância (WAN) resistente para um site central pode usar a terceira opção, um gateway PSTN e, opcionalmente, um servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="ad33b-122">A branch office with a resilient wide area network (WAN) link to a central site can use the third option—a PSTN gateway, and, optionally, a Mediation Server.</span></span> <span data-ttu-id="ad33b-123">Os sites de filiais com links menos resistentes devem usar um aparelho de ramificação sobreviventes ou um servidor de ramificação sobreviventes, que fornecem resiliência em casos de falha de rede de longa distância.</span><span class="sxs-lookup"><span data-stu-id="ad33b-123">Branch office sites with less-resilient links should use a Survivable Branch Appliance or Survivable Branch Server, which provide resiliency in times of wide-area network failures.</span></span> <span data-ttu-id="ad33b-124">Por exemplo, em um site com um aparelho de ramificação sobreviventes ou um servidor de ramificação sobreviventes implantado, os usuários ainda poderão fazer e receber chamadas de voz corporativa se a WAN que estiver conectando o site de filial ao site central estiver inativa.</span><span class="sxs-lookup"><span data-stu-id="ad33b-124">For example, in a site with a Survivable Branch Appliance or Survivable Branch Server deployed, users can still make and receive Enterprise Voice calls if the WAN connecting the branch site to the central site is down.</span></span> <span data-ttu-id="ad33b-125">Para obter detalhes sobre o dispositivo de ramificação sobreviventes, servidor de ramificação sobreviventes e resiliência, consulte [planejando a resiliência do Enterprise Voice no Lync Server 2013](lync-server-2013-planning-for-enterprise-voice-resiliency.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="ad33b-125">For details about the Survivable Branch Appliance, Survivable Branch Server, and resiliency, see [Planning for Enterprise Voice resiliency in Lync Server 2013](lync-server-2013-planning-for-enterprise-voice-resiliency.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="site-topologies"></a><span data-ttu-id="ad33b-126">Topologias de site</span><span class="sxs-lookup"><span data-stu-id="ad33b-126">Site Topologies</span></span>

<span data-ttu-id="ad33b-127">Sua implantação deve incluir pelo menos um site central e pode incluir zero em muitos sites de filiais.</span><span class="sxs-lookup"><span data-stu-id="ad33b-127">Your deployment must include at least one central site, and can include zero to many branch sites.</span></span> <span data-ttu-id="ad33b-128">Cada site de filial está associado a um site central.</span><span class="sxs-lookup"><span data-stu-id="ad33b-128">Each branch site is affiliated with one central site.</span></span> <span data-ttu-id="ad33b-129">O site central fornece os serviços do Lync Server para o site de ramificação que não são hospedados localmente no site da filial, como presença e conferência.</span><span class="sxs-lookup"><span data-stu-id="ad33b-129">The central site provides the Lync Server services to the branch site that are not hosted locally at the branch site, such as presence and conferencing.</span></span>

<span data-ttu-id="ad33b-130">Se você tiver vários sites, poderá emparelhar os pools de front-ends em sites diferentes para permitir recursos de recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="ad33b-130">If you have multiple sites, you can pair together the Front End pools at different sites to enable disaster recovery abilities.</span></span> <span data-ttu-id="ad33b-131">Para obter detalhes, consulte [suporte de alta disponibilidade e recuperação de desastre no Lync Server 2013](lync-server-2013-high-availability-and-disaster-recovery-support.md).</span><span class="sxs-lookup"><span data-stu-id="ad33b-131">For details, see [High availability and disaster recovery support in Lync Server 2013](lync-server-2013-high-availability-and-disaster-recovery-support.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ad33b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad33b-132">See Also</span></span>


[<span data-ttu-id="ad33b-133">Funções do servidor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad33b-133">Server roles in Lync Server 2013</span></span>](lync-server-2013-server-roles.md)  
[<span data-ttu-id="ad33b-134">Suporte à alta disponibilidade e recuperação de desastre no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad33b-134">High availability and disaster recovery support in Lync Server 2013</span></span>](lync-server-2013-high-availability-and-disaster-recovery-support.md)  


[<span data-ttu-id="ad33b-135">Planejamento para resiliência do Enterprise Voice no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad33b-135">Planning for Enterprise Voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice-resiliency.md)  
  

<span data-ttu-id="ad33b-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ad33b-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

