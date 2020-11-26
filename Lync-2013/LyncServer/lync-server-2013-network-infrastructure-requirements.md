---
title: Requisitos de infraestrutura de rede do Lync Server 2013
description: Requisitos de infraestrutura de rede do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Network infrastructure requirements
ms:assetid: 35c7bb3f-8e0f-48b7-8a2c-857d4b42a4c4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425841(v=OCS.15)
ms:contentKeyID: 48183804
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6f7ff21c2f936ef8e048f6831d55408994055400
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425189"
---
# <a name="network-infrastructure-requirements-for-lync-server-2013"></a><span data-ttu-id="289cb-103">Requisitos da infraestrutura de rede para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="289cb-103">Network infrastructure requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="289cb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="289cb-104">

<span> </span></span></span>

<span data-ttu-id="289cb-105">_**Tópico da última modificação:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="289cb-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="289cb-106">A placa adaptadora de rede de cada servidor na topologia do Lync Server 2013 deve dar suporte a pelo menos 1 gigabit por segundo (Gbps).</span><span class="sxs-lookup"><span data-stu-id="289cb-106">The network adapter card of each server in the Lync Server 2013 topology must support at least 1 gigabit per second (Gbps).</span></span> <span data-ttu-id="289cb-107">Em geral, você deve conectar todas as funções de servidor na topologia do Lync Server usando uma rede local de baixa latência e alta largura de banda (LAN).</span><span class="sxs-lookup"><span data-stu-id="289cb-107">In general, you should connect all server roles within the Lync Server topology using a low latency and high bandwidth local area network (LAN).</span></span> <span data-ttu-id="289cb-108">O tamanho da LAN depende do tamanho da topologia:</span><span class="sxs-lookup"><span data-stu-id="289cb-108">The size of the LAN is dependent on the size of the topology:</span></span>

  - <span data-ttu-id="289cb-109">Em topologias de edição padrão, os servidores devem estar em uma rede que suporte Ethernet de 1 Gbps ou equivalente.</span><span class="sxs-lookup"><span data-stu-id="289cb-109">In Standard Edition topologies, servers should be in a network that supports 1 Gbps Ethernet or equivalent.</span></span>

  - <span data-ttu-id="289cb-110">Em topologias de pool Front-end, a maioria dos servidores deve estar em uma rede com suporte para mais de 1 Gbps, especialmente quando oferecer suporte à conferência de áudio/vídeo (A/V) e compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="289cb-110">In Front End pool topologies, most servers should be in a network that supports more than 1 Gbps, especially when supporting audio/video (A/V) conferencing and application sharing.</span></span>

<span data-ttu-id="289cb-111">Para a integração com Rede Telefônica Pública Comutada (PSTN), você pode usar linhas T1/E1 ou tronco SIP.</span><span class="sxs-lookup"><span data-stu-id="289cb-111">For public switched telephone network (PSTN) integration, you can integrate by using either T1/E1 lines or SIP trunking.</span></span>

<div>

## <a name="audiovideo-network-requirements"></a><span data-ttu-id="289cb-112">Requisitos de rede de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="289cb-112">Audio/Video Network Requirements</span></span>

<span data-ttu-id="289cb-113">Os requisitos de rede para áudio/vídeo (A/V) em uma implantação do Lync Server incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="289cb-113">Network requirements for audio/video (A/V) in a Lync Server deployment include the following:</span></span>

  - <span data-ttu-id="289cb-114">Se você estiver implantando um servidor de borda único ou um pool de bordas usando o balanceamento de carga de DNS, poderá configurar o firewall externo como um NAT.</span><span class="sxs-lookup"><span data-stu-id="289cb-114">If you are deploying a single Edge Server or an Edge pool using DNS load balancing, you can configure the external firewall as a NAT.</span></span> <span data-ttu-id="289cb-115">Você não pode configurar o firewall interno como um NAT.</span><span class="sxs-lookup"><span data-stu-id="289cb-115">You cannot configure the internal firewall as a NAT.</span></span> <span data-ttu-id="289cb-116">Para obter detalhes sobre esses requisitos, consulte [determinar requisitos de firewall e porta externo A/V para o Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="289cb-116">For details about these requirements, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md) in the Planning documentation.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="289cb-117">Se você tiver um pool de bordas e estiver usando um balanceador de carga de hardware, será necessário usar endereços IP públicos em cada um dos servidores de borda e não poderá usar o NAT para os servidores ou o pool em seu dispositivo NAT (por exemplo, o firewall ou outro dispositivo de infraestrutura que faria o tráfego de entrada ou saída do NAT).</span><span class="sxs-lookup"><span data-stu-id="289cb-117">If you have an Edge pool and are using a hardware load balancer, you must use public IP addresses on each of the Edge Servers and you cannot use NAT for the servers or the pool at your NAT device (for example, the firewall, or other infrastructure device that would NAT inbound or outbound traffic).</span></span> <span data-ttu-id="289cb-118">Para obter detalhes, consulte <A href="lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md">Resumo de portabilidade-dimensionamento consolidado com balanceadores de carga de hardware no Lync Server 2013</A> na documentação planejando para acesso de usuário externo.</span><span class="sxs-lookup"><span data-stu-id="289cb-118">For details, see <A href="lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md">Port summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</A> in the Planning for External User Access documentation.</span></span>

    
    </div>

  - <span data-ttu-id="289cb-119">Se a sua organização usa uma infraestrutura de QoS (Qualidade de Serviço), o subsistema de mídia é projetado para funcionar com essa infraestrutura existente.</span><span class="sxs-lookup"><span data-stu-id="289cb-119">If your organization uses a Quality of Service (QoS) infrastructure, the media subsystem is designed to work within this existing infrastructure.</span></span>

  - <span data-ttu-id="289cb-120">Caso você utilize o protocolo IPsec, é recomendável desabilitá-lo nos intervalos de portas usados para o tráfego de A/V.</span><span class="sxs-lookup"><span data-stu-id="289cb-120">If you use Internet Protocol security (IPsec), we recommend disabling IPsec over the port ranges used for A/V traffic.</span></span> <span data-ttu-id="289cb-121">Para obter detalhes, consulte [exceções de IPsec no Lync Server 2013](lync-server-2013-ipsec-exceptions.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="289cb-121">For details, see [IPsec exceptions in Lync Server 2013](lync-server-2013-ipsec-exceptions.md) in the Planning documentation.</span></span>

<span data-ttu-id="289cb-122">Para garantir a qualidade de mídia ideal, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="289cb-122">To ensure optimal media quality, do the following:</span></span>

  - <span data-ttu-id="289cb-123">Provisione seus links de rede para dar suporte a throughput de 65 kilobits por segundo (Kbps) por fluxo de áudio e 500 kbps por fluxo de vídeo, se habilitados, durante períodos de pico de uso.</span><span class="sxs-lookup"><span data-stu-id="289cb-123">Provision your network links to support throughput of 65 kilobits per second (Kbps) per audio stream and 500 Kbps per video stream, if enabled, during peak usage periods.</span></span> <span data-ttu-id="289cb-124">Uma sessão de áudio ou de vídeo bidirecional consiste em dois fluxos.</span><span class="sxs-lookup"><span data-stu-id="289cb-124">A bidirectional audio or video session consists of two streams.</span></span>

  - <span data-ttu-id="289cb-125">Para lidar com picos inesperados no tráfego acima desse nível e maior utilização ao longo do tempo, os pontos de extremidade de mídia do Lync Server podem se adaptar às diferentes condições de rede e às cargas de suporte de três vezes a taxa de transferência (consulte o parágrafo anterior) para áudio e vídeo enquanto ainda mantém a qualidade aceitável.</span><span class="sxs-lookup"><span data-stu-id="289cb-125">To cope with unexpected spikes in traffic above this level and increased usage over time, Lync Server media endpoints can adapt to varying network conditions and support loads of three times the throughput (see previous paragraph) for audio and video while still retaining acceptable quality.</span></span> <span data-ttu-id="289cb-126">No entanto, não presuma que essa capacidade de adaptação dará suporte a uma rede subvisionada.</span><span class="sxs-lookup"><span data-stu-id="289cb-126">However, do not assume that this adaptability will support an under-provisioned network.</span></span> <span data-ttu-id="289cb-127">Em uma rede subprovisionada, a capacidade dos pontos de extremidade de mídia do Lync Server de lidar dinamicamente com condições de rede variáveis (por exemplo, perda de pacotes de alta capacidade temporária) é reduzida.</span><span class="sxs-lookup"><span data-stu-id="289cb-127">In an under-provisioned network, the ability of the Lync Server media endpoints to dynamically deal with varying network conditions (for example, temporary high packet loss) is reduced.</span></span>

  - <span data-ttu-id="289cb-128">Para links de rede em que o provisionamento é extremamente dispendioso e difícil, talvez seja necessário considerar o provisionamento para um volume menor de tráfego.</span><span class="sxs-lookup"><span data-stu-id="289cb-128">For network links where provisioning is extremely costly and difficult, you may need to consider provisioning for a lower volume of traffic.</span></span> <span data-ttu-id="289cb-129">Nesse cenário, permita que a elasticidade dos pontos de extremidade de mídia do Lync Server absorvesse a diferença entre o volume de tráfego e o nível de tráfego de pico, ao custo de uma redução na qualidade de voz.</span><span class="sxs-lookup"><span data-stu-id="289cb-129">In this scenario, let the elasticity of the Lync Server media endpoints absorb the difference between the traffic volume and the peak traffic level, at the cost of some reduction in the voice quality.</span></span> <span data-ttu-id="289cb-130">Além disso, há uma redução no espaço de qualquer outra forma disponível para absorver picos repentinos de tráfego.</span><span class="sxs-lookup"><span data-stu-id="289cb-130">Also, there is a decrease in the headroom otherwise available to absorb sudden peaks in traffic.</span></span>

  - <span data-ttu-id="289cb-131">Para links que não podem ser provisionados corretamente em curto prazo (por exemplo, um site com links WAN muito ruins), considere a possibilidade de desabilitar o vídeo para determinados usuários.</span><span class="sxs-lookup"><span data-stu-id="289cb-131">For links that cannot be correctly provisioned in the short term (for example, a site with very poor WAN links), consider disabling video for certain users.</span></span>

  - <span data-ttu-id="289cb-132">Provisione sua rede para garantir um atraso máximo de ponto a ponto (latência) de 150 milissegundos (MS) em carga máxima.</span><span class="sxs-lookup"><span data-stu-id="289cb-132">Provision your network to ensure a maximum end-to-end delay (latency) of 150 milliseconds (ms) under peak load.</span></span> <span data-ttu-id="289cb-133">A latência é a única deficiência da rede que os componentes de mídia do Lync Server não podem reduzir e é importante localizar e eliminar os pontos fracos.</span><span class="sxs-lookup"><span data-stu-id="289cb-133">Latency is the one network impairment that Lync Server media components cannot reduce, and it is important to find and eliminate the weak points.</span></span>

  - <span data-ttu-id="289cb-134">Para servidores que executam o software antivírus, inclua todos os servidores que executam o Lync Server na lista de exceções para fornecer desempenho e qualidade de áudio ideais.</span><span class="sxs-lookup"><span data-stu-id="289cb-134">For servers running antivirus software, include all servers running Lync Server in the exception list in order to provide optimal performance and audio quality.</span></span>

</div>

<div>

## <a name="conferencing-network-requirements"></a><span data-ttu-id="289cb-135">Requisitos de rede de conferência</span><span class="sxs-lookup"><span data-stu-id="289cb-135">Conferencing Network Requirements</span></span>

<span data-ttu-id="289cb-136">A largura de banda usada para baixar o conteúdo da conferência do servidor dos serviços de informações da Internet (IIS) depende do tamanho do conteúdo que foi carregado.</span><span class="sxs-lookup"><span data-stu-id="289cb-136">The bandwidth that is used to download conference content from the Internet Information Services (IIS) server depends on the size of the content that is uploaded.</span></span>

<span data-ttu-id="289cb-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="289cb-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

