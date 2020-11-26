---
title: 'Lync Server 2013: componente do servidor de mediação'
description: 'Lync Server 2013: componente do servidor de mediação.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mediation Server component
ms:assetid: 5b19edef-4a54-43c9-aa12-5643b8108355
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398399(v=OCS.15)
ms:contentKeyID: 48184239
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 08c11bff3ee7077d991204cda5a9885787c50ec2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445967"
---
# <a name="mediation-server-component-in-lync-server-2013"></a><span data-ttu-id="96b62-103">Componente servidor de mediação no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96b62-103">Mediation Server component in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="96b62-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="96b62-104">

<span> </span></span></span>

<span data-ttu-id="96b62-105">_**Tópico da última modificação:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="96b62-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="96b62-106">Você deve implantar o Lync Server 2013, o servidor de mediação se implantar a carga de trabalho do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="96b62-106">You must deploy Lync Server 2013, Mediation Server if you deploy the Enterprise Voice workload.</span></span> <span data-ttu-id="96b62-107">Esta seção descreve funcionalidade básica, dependências, topologias básicas e diretrizes de planejamento.</span><span class="sxs-lookup"><span data-stu-id="96b62-107">This section describes basic functionality, dependencies, basic topologies, and planning guidelines.</span></span>

<span data-ttu-id="96b62-108">O servidor de mediação traduz a sinalização e, em algumas configurações, mídia entre a sua rede do Lync Server 2013, a infraestrutura do Enterprise Voice e um gateway de rede telefônica pública comutada (PSTN) ou um tronco de protocolo de iniciação de sessão (SIP).</span><span class="sxs-lookup"><span data-stu-id="96b62-108">The Mediation Server translates signaling and, in some configurations, media between your internal Lync Server 2013, Enterprise Voice infrastructure and a public switched telephone network (PSTN) gateway or a Session Initiation Protocol (SIP) trunk.</span></span> <span data-ttu-id="96b62-109">Na 2013 do Lync Server, o servidor de mediação escuta em um único endereço de transporte de protocolo NNTP (MTLS) mútuo.</span><span class="sxs-lookup"><span data-stu-id="96b62-109">On the Lync Server 2013 side, Mediation Server listens on a single mutual TLS (MTLS) transport address.</span></span> <span data-ttu-id="96b62-110">No lado do gateway, o servidor de mediação escuta todas as portas de escuta associadas a troncos definidas no documento de topologia.</span><span class="sxs-lookup"><span data-stu-id="96b62-110">On the gateway side, Mediation Server listens on all associated listening ports associated with trunks defined in the Topology document.</span></span> <span data-ttu-id="96b62-111">Todos os gateways qualificados devem dar suporte a TLS, mas também podem habilitar o TCP.</span><span class="sxs-lookup"><span data-stu-id="96b62-111">All qualified gateways must support TLS, but can enable TCP as well.</span></span> <span data-ttu-id="96b62-112">O TCP é aceito para gateways que não dão suporte a TLS.</span><span class="sxs-lookup"><span data-stu-id="96b62-112">TCP is supported for gateways that do not support TLS.</span></span>

<span data-ttu-id="96b62-113">Se você também tiver um PBX (Exchange Branch Exchange) existente em seu ambiente, o servidor de mediação manipulará chamadas entre usuários do Enterprise Voice e o PBX.</span><span class="sxs-lookup"><span data-stu-id="96b62-113">If you also have an existing Public Branch Exchange (PBX) in your environment, Mediation Server handles calls between Enterprise Voice users and the PBX.</span></span> <span data-ttu-id="96b62-114">Se o seu PBX for um PBX IP, você poderá criar uma conexão SIP direta entre o PBX e o servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="96b62-114">If your PBX is an IP-PBX, you can create a direct SIP connection between the PBX and Mediation Server.</span></span> <span data-ttu-id="96b62-115">Se o seu PBX for um PBX TDM (Time Division multiplex), você também deve implantar um gateway PSTN entre o servidor de mediação e o PBX.</span><span class="sxs-lookup"><span data-stu-id="96b62-115">If your PBX is a Time Division Multiplex (TDM) PBX, you must also deploy a PSTN gateway between Mediation Server and the PBX.</span></span>

<span data-ttu-id="96b62-116">O servidor de mediação é posicionado com o servidor front-end por padrão.</span><span class="sxs-lookup"><span data-stu-id="96b62-116">The Mediation Server is collocated with the Front End Server by default.</span></span> <span data-ttu-id="96b62-117">O servidor de mediação também pode ser implantado em um pool autônomo por motivos de desempenho, ou se você implantar o entroncamento SIP, caso em que o pool autônomo seja altamente recomendado.</span><span class="sxs-lookup"><span data-stu-id="96b62-117">The Mediation Server can also be deployed in a stand-alone pool for performance reasons, or if you deploy SIP trunking, in which case the stand-alone pool is strongly recommended.</span></span>

<span data-ttu-id="96b62-118">Se você implantar conexões SIP diretas em um gateway PSTN qualificado que ofereça suporte ao bypass de mídia e ao balanceamento de carga de DNS, um pool autônomo do servidor de mediação não será necessário.</span><span class="sxs-lookup"><span data-stu-id="96b62-118">If you deploy Direct SIP connections to a qualified PSTN gateway that supports media bypass and DNS load balancing, a stand-alone Mediation Server pool is not necessary.</span></span> <span data-ttu-id="96b62-119">Um pool autônomo do servidor de mediação não é necessário porque gateways qualificados são capazes de balanceamento de carga de DNS para um pool de servidores de mediação e podem receber tráfego de qualquer servidor de mediação em um pool.</span><span class="sxs-lookup"><span data-stu-id="96b62-119">A stand-alone Mediation Server pool is not necessary because qualified gateways are capable of DNS load balancing to a pool of Mediation Servers and they can receive traffic from any Mediation Server in a pool.</span></span>

<span data-ttu-id="96b62-120">Também recomendamos que você colocar o servidor de mediação em um pool de front-end quando tiver implantado IP-PBXs ou se conectar a um controlador de borda de sessão (SBC) do provedor de servidor de telefonia pela Internet, contanto que qualquer uma das seguintes condições seja atendida:</span><span class="sxs-lookup"><span data-stu-id="96b62-120">We also recommend that you collocate the Mediation Server on a Front End pool when you have deployed IP-PBXs or connect to an Internet Telephony Server Provider’s Session Border Controller (SBC), as long as any of the following conditions are met:</span></span>

  - <span data-ttu-id="96b62-121">O IP-PBX ou o SBC está configurado para receber tráfego de qualquer servidor de mediação no pool e pode rotear o tráfego uniformemente para todos os servidores de mediação no pool.</span><span class="sxs-lookup"><span data-stu-id="96b62-121">The IP-PBX or SBC is configured to receive traffic from any Mediation Server in the pool and can route traffic uniformly to all Mediation Servers in the pool.</span></span>

  - <span data-ttu-id="96b62-122">O IP-PBX não é compatível com o bypass de mídia, mas o pool de front-end que hospeda o servidor de mediação pode manipular a transcodificação de voz para chamadas para as quais o bypass de mídia não se aplica.</span><span class="sxs-lookup"><span data-stu-id="96b62-122">The IP-PBX does not support media bypass, but the Front End pool that is hosting the Mediation Server can handle voice transcoding for calls to which media bypass does not apply.</span></span>

<span data-ttu-id="96b62-123">Você pode usar o Microsoft Lync Server 2013, ferramenta de planejamento para avaliar se o pool de front-ends em que você deseja colocar o servidor de mediação pode manipular a carga.</span><span class="sxs-lookup"><span data-stu-id="96b62-123">You can use the Microsoft Lync Server 2013, Planning Tool to evaluate whether the Front End pool where you want to collocate the Mediation Server can handle the load.</span></span> <span data-ttu-id="96b62-124">Se o seu ambiente não puder atender a esses requisitos, você deve implantar um pool autônomo do servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="96b62-124">If your environment cannot meet these requirements, then you must deploy a stand-alone Mediation Server pool.</span></span>

<span data-ttu-id="96b62-125">As principais funções do servidor de mediação são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="96b62-125">The main functions of the Mediation Server are as follows:</span></span>

  - <span data-ttu-id="96b62-126">Criptografar e descriptografar SRTP no lado do Lync Server</span><span class="sxs-lookup"><span data-stu-id="96b62-126">Encrypting and decrypting SRTP on the Lync Server side</span></span>

  - <span data-ttu-id="96b62-127">Convertendo SIP via TCP (para gateways que não são compatíveis com TLS) para SIP em TLS mútuo</span><span class="sxs-lookup"><span data-stu-id="96b62-127">Translating SIP over TCP (for gateways that do not support TLS) to SIP over mutual TLS</span></span>

  - <span data-ttu-id="96b62-128">Traduzir fluxos de mídia entre o Lync Server e o peer do gateway do servidor de mediação</span><span class="sxs-lookup"><span data-stu-id="96b62-128">Translating media streams between Lync Server and the gateway peer of the Mediation Server</span></span>

  - <span data-ttu-id="96b62-129">Conectando clientes que estão fora da rede para componentes ICE internos, que permitem a passagem de mídia de NAT e firewalls</span><span class="sxs-lookup"><span data-stu-id="96b62-129">Connecting clients that are outside the network to internal ICE components, which enable media traversal of NAT and firewalls</span></span>

  - <span data-ttu-id="96b62-130">Atuar como intermediário para fluxos de chamadas aos quais um gateway não oferece suporte, como chamadas de trabalhadores remotos em um cliente Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="96b62-130">Acting as an intermediary for call flows that a gateway does not support, such as calls from remote workers on an Enterprise Voice client</span></span>

  - <span data-ttu-id="96b62-131">Em implantações que incluem entroncamento SIP, trabalhando com o provedor de serviço de entroncamento SIP para fornecer suporte a PSTN, o que elimina a necessidade de um gateway PSTN</span><span class="sxs-lookup"><span data-stu-id="96b62-131">In deployments that include SIP trunking, working with the SIP trunking service provider to provide PSTN support, which eliminates the need for a PSTN gateway</span></span>

<span data-ttu-id="96b62-132">A figura a seguir mostra os protocolos de sinalização e mídia usados pelo servidor de mediação durante a comunicação com um gateway PSTN básico e com a infraestrutura Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="96b62-132">The following figure shows the signaling and media protocols that are used by the Mediation Server when communicating with a basic PSTN gateway and the Enterprise Voice infrastructure.</span></span>

<span data-ttu-id="96b62-133">**Protocolos de sinalização e a mídia usados pelo Servidor de Mediação**</span><span class="sxs-lookup"><span data-stu-id="96b62-133">**Signaling and media protocols used by the Mediation Server**</span></span>

<span data-ttu-id="96b62-134">![Diagrama de protocolos do servidor de mediação](images/Gg398399.c3d39ba0-e323-4a58-8f07-4e80d3278af2(OCS.15).jpg "Diagrama de protocolos do servidor de mediação")</span><span class="sxs-lookup"><span data-stu-id="96b62-134">![Mediation Server Protocols diagram](images/Gg398399.c3d39ba0-e323-4a58-8f07-4e80d3278af2(OCS.15).jpg "Mediation Server Protocols diagram")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="96b62-135">Se você estiver usando TCP ou RTP/RTCP (em vez do SRTP ou SRTCP) na rede entre o gateway PSTN e o servidor de mediação, recomendamos que você tome medidas para ajudar a garantir a segurança e a privacidade da rede.</span><span class="sxs-lookup"><span data-stu-id="96b62-135">If you are using TCP or RTP/RTCP (instead of SRTP or SRTCP) on the network between the PSTN gateway and the Mediation Server, we recommend that you take measures to help ensure the security and privacy of the network.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="96b62-136">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="96b62-136">In This Section</span></span>

  - [<span data-ttu-id="96b62-137">Tronco M:N no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96b62-137">M:N trunk in Lync Server 2013</span></span>](lync-server-2013-m-n-trunk.md)

  - [<span data-ttu-id="96b62-138">Controle de admissão de chamada e Servidor de Mediação no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96b62-138">Call admission control and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-call-admission-control-and-mediation-server.md)

  - [<span data-ttu-id="96b62-139">9-1-1 Avançado (E9-1-1) e Servidor de Mediação no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96b62-139">Enhanced 9-1-1 (E9-1-1) and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-enhanced-9-1-1-e9-1-1-and-mediation-server.md)

  - [<span data-ttu-id="96b62-140">Bypass de mídia e Servidor de Mediação no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96b62-140">Media bypass and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-media-bypass-and-mediation-server.md)

  - [<span data-ttu-id="96b62-141">Componentes e topologias para o Servidor de Mediação no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96b62-141">Components and topologies for Mediation Server in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-mediation-server.md)

  - [<span data-ttu-id="96b62-142">Diretrizes de implantação para o servidor de mediação no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96b62-142">Deployment guidelines for Mediation Server in Lync Server 2013</span></span>](lync-server-2013-deployment-guidelines-for-mediation-server.md)

<span data-ttu-id="96b62-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="96b62-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

