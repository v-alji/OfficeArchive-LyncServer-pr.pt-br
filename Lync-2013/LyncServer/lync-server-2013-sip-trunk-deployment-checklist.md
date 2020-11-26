---
title: 'Lync Server 2013: Lista de verificação de tronco SIP'
description: 'Lync Server 2013: lista de verificação de implantação de tronco SIP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SIP trunk deployment checklist
ms:assetid: 94f4f03e-19d5-4198-92be-e4076dbb959a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398755(v=OCS.15)
ms:contentKeyID: 48184891
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbab9647a7146b2478317ab6c020969506f9c0ef
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423810"
---
# <a name="sip-trunk-deployment-checklist-for-lync-server-2013"></a><span data-ttu-id="9f673-103">Lista de verificação de tronco SIP para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f673-103">SIP trunk deployment checklist for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9f673-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9f673-104">

<span> </span></span></span>

<span data-ttu-id="9f673-105">_**Tópico da última modificação:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="9f673-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="9f673-106">Antes de poder implantar um tronco SIP, você e seu provedor de serviços devem trocar informações básicas de conexão sobre seus respectivos pontos de extremidade de tronco SIP.</span><span class="sxs-lookup"><span data-stu-id="9f673-106">Before you can deploy a SIP trunk, you and your service provider must exchange some basic connection information about your respective SIP trunk endpoints.</span></span>

<span data-ttu-id="9f673-107">Obtenha as seguintes informações para cada gateway do ITSP ao qual você irá se conectar:</span><span class="sxs-lookup"><span data-stu-id="9f673-107">Get the following information for each ITSP gateway that you will connect to:</span></span>

  - <span data-ttu-id="9f673-108">Endereço IP</span><span class="sxs-lookup"><span data-stu-id="9f673-108">IP address</span></span>

  - <span data-ttu-id="9f673-109">FQDN (nome de domínio totalmente qualificado)</span><span class="sxs-lookup"><span data-stu-id="9f673-109">Fully qualified domain name (FQDN)</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9f673-110">O provedor de serviço pode solicitar que você se conecte a mais de um gateway do ITSP.</span><span class="sxs-lookup"><span data-stu-id="9f673-110">The service provider may ask you to connect to more than one ITSP gateway.</span></span> <span data-ttu-id="9f673-111">Nesse caso, você deve configurar uma conexão entre cada gateway do ITSP e cada servidor de mediação em seu pool.</span><span class="sxs-lookup"><span data-stu-id="9f673-111">In that case, you must configure a connection between each ITSP gateway and each Mediation Server in your pool.</span></span>



</div>

<span data-ttu-id="9f673-112">As informações que você fornece ao seu provedor de serviço dependem do seu tipo de conexão de tronco SIP:</span><span class="sxs-lookup"><span data-stu-id="9f673-112">The information you give to your service provider depends on your SIP trunk connection type:</span></span>

  - <span data-ttu-id="9f673-113">Para conexões de rótulo de multiprotocolo (MPLS) ou de rede privada, forneça ao ITSP o endereço IP publicamente roteável do roteador em sua rede de perímetro (também conhecido como DMZ, zona desmilitarizada e sub-rede filtrada).</span><span class="sxs-lookup"><span data-stu-id="9f673-113">For Multiprotocol Label Switching (MPLS) or private network connections, give the ITSP the publicly routable IP Address of the router in your perimeter network (also known as DMZ, demilitarized zone, and screened subnet).</span></span> <span data-ttu-id="9f673-114">Verifique se o gateway ou o controle de borda de sessão (SBC) no ITSP pode chegar a este endereço.</span><span class="sxs-lookup"><span data-stu-id="9f673-114">Verify that the gateway or Session Border Controller (SBC) at the ITSP can reach this address.</span></span> <span data-ttu-id="9f673-115">Além disso, dê ao ITSP o FQDN do servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="9f673-115">Also give the ITSP the FQDN of your Mediation Server.</span></span>

  - <span data-ttu-id="9f673-116">Para conexões VPN (rede virtual privada), dê ao ITSP o endereço IP do seu servidor VPN.</span><span class="sxs-lookup"><span data-stu-id="9f673-116">For virtual private network (VPN) connections, give the ITSP the IP address of your VPN server.</span></span>

<div>

## <a name="certificate-considerations"></a><span data-ttu-id="9f673-117">Considerações sobre certificado</span><span class="sxs-lookup"><span data-stu-id="9f673-117">Certificate Considerations</span></span>

<span data-ttu-id="9f673-118">Para determinar se você precisa de um certificado para o entroncamento SIP, consulte o ITSP sobre o suporte ao protocolo:</span><span class="sxs-lookup"><span data-stu-id="9f673-118">To determine whether you need a certificate for SIP trunking, check with your ITSP about protocol support:</span></span>

1.  <span data-ttu-id="9f673-119">Se o seu ITSP der suporte somente para TCP (Transmission Control Protocol), você não precisará de um certificado.</span><span class="sxs-lookup"><span data-stu-id="9f673-119">If your ITSP supports Transmission Control Protocol (TCP) only, you do not need a certificate.</span></span>

2.  <span data-ttu-id="9f673-120">Se o seu ITSP suporta TLS (Transport Layer Security), o ITSP deve fornecer um certificado.</span><span class="sxs-lookup"><span data-stu-id="9f673-120">If your ITSP supports Transport Layer Security (TLS), the ITSP must provide you with a certificate.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9f673-121">O SIP funciona em conjunto com o protocolo de transporte em tempo real (RTP) ou SSTP (protocolo de transporte em tempo real seguro), os protocolos que gerenciam os dados de voz reais nas chamadas de protocolo de voz pela Internet (VoIP).</span><span class="sxs-lookup"><span data-stu-id="9f673-121">SIP works in conjunction with real-time transport protocol (RTP) or secure real-time transport protocol (SRTP), the protocols that manage the actual voice data in Voice over Internet Protocol (VoIP) calls.</span></span>



</div>

</div>

<div>

## <a name="deployment-process"></a><span data-ttu-id="9f673-122">Processo de implantação</span><span class="sxs-lookup"><span data-stu-id="9f673-122">Deployment Process</span></span>

<span data-ttu-id="9f673-123">Para implementar o lado do Lync Server da conexão do tronco SIP, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="9f673-123">To implement the Lync Server side of the SIP trunk connection, follow these steps:</span></span>

1.  <span data-ttu-id="9f673-124">Usando o construtor de topologias do Lync Server, crie e configure a topologia de domínio SIP.</span><span class="sxs-lookup"><span data-stu-id="9f673-124">Using the Lync Server Topology Builder, create and configure the SIP domain topology.</span></span> <span data-ttu-id="9f673-125">Para obter detalhes, consulte [definir e configurar uma topologia no construtor de topologias para o Lync Server 2013](lync-server-2013-define-and-configure-a-topology-in-topology-builder.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="9f673-125">For details, see [Define and configure a topology in Topology Builder for Lync Server 2013](lync-server-2013-define-and-configure-a-topology-in-topology-builder.md) in the Deployment documentation.</span></span>

2.  <span data-ttu-id="9f673-126">Usando o painel de controle do Lync Server, configure o roteamento de voz para o novo domínio SIP.</span><span class="sxs-lookup"><span data-stu-id="9f673-126">Using the Lync Server Control Panel, configure voice routing for the new SIP domain.</span></span> <span data-ttu-id="9f673-127">Para obter detalhes, consulte [Configurando troncos no Lync Server 2013](lync-server-2013-configuring-trunks.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="9f673-127">For details, see [Configuring trunks in Lync Server 2013](lync-server-2013-configuring-trunks.md) in the Deployment documentation.</span></span>

3.  <span data-ttu-id="9f673-128">Testar a conectividade usando o cmdlet **Test-CsPstnOutboundCall** .</span><span class="sxs-lookup"><span data-stu-id="9f673-128">Test connectivity by using the **Test-CsPstnOutboundCall** cmdlet.</span></span> <span data-ttu-id="9f673-129">Para obter detalhes, consulte a documentação do Shell de gerenciamento do Lync Server ou a ajuda do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9f673-129">For details, see the Lync Server Management Shell documentation or Help for Lync Server Management Shell.</span></span>

<span data-ttu-id="9f673-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9f673-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

