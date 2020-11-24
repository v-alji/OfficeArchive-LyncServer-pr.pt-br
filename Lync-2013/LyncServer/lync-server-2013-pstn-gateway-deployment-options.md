---
title: 'Lync Server 2013: Opções de implantação do gateway PSTN'
description: 'Lync Server 2013: opções de implantação do gateway PSTN.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN gateway deployment options
ms:assetid: d1ab4f74-18aa-40c7-a8cf-ec806cf6e28a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398899(v=OCS.15)
ms:contentKeyID: 48185445
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 871bc4d573e927f83cdb07d4fb2b5d5b954e6383
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390089"
---
# <a name="pstn-gateway-deployment-options-in-lync-server-2013"></a><span data-ttu-id="cfef7-103">Opções de implantação do gateway PSTN no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cfef7-103">PSTN gateway deployment options in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cfef7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cfef7-104">

<span> </span></span></span>

<span data-ttu-id="cfef7-105">_**Tópico da última modificação:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="cfef7-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<div>

## <a name="pstn-gateways"></a><span data-ttu-id="cfef7-106">Gateways PSTN</span><span class="sxs-lookup"><span data-stu-id="cfef7-106">PSTN Gateways</span></span>

<span data-ttu-id="cfef7-107">Gateways de rede telefônica pública comutada (PSTN) são componentes de hardware de terceiros que traduzem sinais e mídias entre a infraestrutura de voz empresarial e a PSTN, diretamente ou por meio da conexão com troncos SIP.</span><span class="sxs-lookup"><span data-stu-id="cfef7-107">Public switched telephone network (PSTN) gateways are third-party hardware components that translate signaling and media between the Enterprise Voice infrastructure and the PSTN, either directly or through connection to SIP trunks.</span></span> <span data-ttu-id="cfef7-108">Em qualquer topologia, o gateway termina a PSTN.</span><span class="sxs-lookup"><span data-stu-id="cfef7-108">In either topology, the gateway terminates the PSTN.</span></span> <span data-ttu-id="cfef7-109">O gateway está isolado em sua própria sub-rede e está conectado à rede corporativa por meio do servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="cfef7-109">The gateway is isolated in its own subnet and is connected to the enterprise network through the Mediation Server.</span></span>

<span data-ttu-id="cfef7-110">Uma empresa com vários sites normalmente implantou um ou mais gateways em cada site.</span><span class="sxs-lookup"><span data-stu-id="cfef7-110">An enterprise with multiple sites would typically deploy one or more gateways at each site.</span></span> <span data-ttu-id="cfef7-111">Os sites de ramificação podem se conectar à PSTN por meio de um gateway ou por meio de um aparelho de ramificação sobreviventes, que combina o gateway e os servidores em uma única caixa.</span><span class="sxs-lookup"><span data-stu-id="cfef7-111">Branch sites can connect to the PSTN either through a gateway, or through a Survivable Branch Appliance, which combines gateway and servers in a single box.</span></span> <span data-ttu-id="cfef7-112">Se os sites de filiais usarem um gateway, um servidor de registrador e mediação será necessário no site, a menos que o link de WAN seja resiliente.</span><span class="sxs-lookup"><span data-stu-id="cfef7-112">If branch sites use a gateway, both a Registrar and Mediation Server are required on site, unless the WAN link is resilient.</span></span> <span data-ttu-id="cfef7-113">Um ou mais servidores de mediação, que são posicionados em servidores front-end, podem encaminhar chamadas para um ou mais gateways em cada site.</span><span class="sxs-lookup"><span data-stu-id="cfef7-113">One or more Mediation Servers, which are collocated on Front End Servers, can route calls for the one or more gateways at each site.</span></span> <span data-ttu-id="cfef7-114">Recomendamos que o registrador, o servidor de mediação e o gateway necessários no site sejam implantados como um aparelho de ramificação sobreviventes.</span><span class="sxs-lookup"><span data-stu-id="cfef7-114">We recommend that the Registrar, Mediation Server, and gateway required on site are deployed as a Survivable Branch Appliance.</span></span>

<span data-ttu-id="cfef7-115">Determinar o número, o tamanho e a localização dos gateways PSTN talvez seja a decisão mais importante e cara que você deve fazer ao planejar sua infraestrutura empresarial.</span><span class="sxs-lookup"><span data-stu-id="cfef7-115">Determining the number, size, and location of PSTN gateways is perhaps the most important and expensive decision you must make when planning your Enterprise Voice infrastructure.</span></span>

<span data-ttu-id="cfef7-116">Aqui estão as principais perguntas a serem consideradas.</span><span class="sxs-lookup"><span data-stu-id="cfef7-116">Here are the main questions to consider.</span></span> <span data-ttu-id="cfef7-117">Tenha em mente que as respostas para essas perguntas são todas interdependentes</span><span class="sxs-lookup"><span data-stu-id="cfef7-117">Keep in mind that the answers to these questions are all interdependent</span></span>

  - <span data-ttu-id="cfef7-118">Quantos gateways PSTN são necessários?</span><span class="sxs-lookup"><span data-stu-id="cfef7-118">How many PSTN gateways are needed?</span></span> <span data-ttu-id="cfef7-119">A resposta depende do número de usuários, do número previsto de chamadas simultâneas (carga de tráfego) e do número de sites (cada site precisa de um).</span><span class="sxs-lookup"><span data-stu-id="cfef7-119">The answer depends on the number of users, the anticipated number of simultaneous calls (traffic load), and the number of sites (each site needs one).</span></span>

  - <span data-ttu-id="cfef7-120">Qual é o tamanho dos gateways?</span><span class="sxs-lookup"><span data-stu-id="cfef7-120">What size should the gateways be?</span></span> <span data-ttu-id="cfef7-121">A resposta depende do número de usuários no site e na carga do tráfego.</span><span class="sxs-lookup"><span data-stu-id="cfef7-121">The answer depends on the number of users at the site and on the traffic load.</span></span>

  - <span data-ttu-id="cfef7-122">Onde os gateways devem estar localizados?</span><span class="sxs-lookup"><span data-stu-id="cfef7-122">Where should the gateways be located?</span></span> <span data-ttu-id="cfef7-123">A resposta depende em parte da topologia e em parte da distribuição geográfica da sua organização.</span><span class="sxs-lookup"><span data-stu-id="cfef7-123">The answer depends in part on the topology and in part on the geographic distribution of your organization.</span></span>

<span data-ttu-id="cfef7-124">Você também deve considerar as opções de topologia do gateway (para obter detalhes, consulte Topologias de gateway mais adiante neste tópico).</span><span class="sxs-lookup"><span data-stu-id="cfef7-124">You should also consider your gateway topology options (for details, see Gateway Topologies later in this topic).</span></span>

<div>

## <a name="mn-trunk-support"></a><span data-ttu-id="cfef7-125">Suporte de Tronco M:N</span><span class="sxs-lookup"><span data-stu-id="cfef7-125">M:N Trunk Support</span></span>

<span data-ttu-id="cfef7-126">Os servidores de mediação podem rotear chamadas por meio de vários gateways, Session Borderting (SBCs) fornecido pelos provedores de serviços de telefonia pela Internet ou uma combinação dos dois.</span><span class="sxs-lookup"><span data-stu-id="cfef7-126">The Mediation Servers can route calls through multiple gateways, Session Border Controllers (SBCs) provided by Internet telephony service providers, or a combination of the two.</span></span> <span data-ttu-id="cfef7-127">Além disso, vários servidores de mediação no pool podem interagir com vários gateways.</span><span class="sxs-lookup"><span data-stu-id="cfef7-127">Additionally, multiple Mediation Servers in the pool can interact with multiple gateways.</span></span> <span data-ttu-id="cfef7-128">A rota lógica definida entre um servidor de mediação e um gateway é chamada de *tronco*.</span><span class="sxs-lookup"><span data-stu-id="cfef7-128">The logical route defined between a Mediation Server and gateway is called a *trunk*.</span></span> <span data-ttu-id="cfef7-129">Quando um usuário interno coloca uma chamada PSTN, a lógica de roteamento de saída no pool de front-ends escolhe qual tronco deve ser roteado por todas as combinações possíveis que podem estar disponíveis para roteamento com essa chamada específica.</span><span class="sxs-lookup"><span data-stu-id="cfef7-129">When an internal user places a PSTN call, outbound routing logic on the Front End pool chooses which trunk to route over out of all possible combinations that may be available for routing that particular call.</span></span> <span data-ttu-id="cfef7-130">Com o balanceamento de carga de DNS, se uma chamada não entrar em contato com um gateway devido a um problema com um servidor de mediação específico no pool, a chamada será repetida em um servidor de mediação alternativo no pool.</span><span class="sxs-lookup"><span data-stu-id="cfef7-130">With DNS load balancing, if a call fails to reach a gateway due to an issue with a particular Mediation Server in the pool, the call will be retried to an alternate Mediation Server in the pool.</span></span>

<span data-ttu-id="cfef7-131">Para obter detalhes sobre o planejamento de vários gateways, consulte [M:N trunk in Lync Server 2013](lync-server-2013-m-n-trunk.md).</span><span class="sxs-lookup"><span data-stu-id="cfef7-131">For details about planning for multiple gateways, see [M:N trunk in Lync Server 2013](lync-server-2013-m-n-trunk.md).</span></span>

<span data-ttu-id="cfef7-132">Para obter detalhes sobre outros aprimoramentos de roteamento de saída, consulte [rotas de voz no Lync Server 2013](lync-server-2013-voice-routes.md).</span><span class="sxs-lookup"><span data-stu-id="cfef7-132">For details about other outbound routing enhancements, see [Voice routes in Lync Server 2013](lync-server-2013-voice-routes.md).</span></span>

</div>

<div>

## <a name="gateway-topologies"></a><span data-ttu-id="cfef7-133">Topologias de gateway</span><span class="sxs-lookup"><span data-stu-id="cfef7-133">Gateway Topologies</span></span>

<span data-ttu-id="cfef7-134">Ao considerar as questões fundamentais de implantação de gateway, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="cfef7-134">When you consider the fundamental questions of gateway deployment, follow these steps:</span></span>

1.  <span data-ttu-id="cfef7-135">Conte os sites nos quais você deseja fornecer conectividade PSTN usando o Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="cfef7-135">Count the sites at which you want to provide PSTN connectivity by using Enterprise Voice.</span></span>

2.  <span data-ttu-id="cfef7-136">Estimar o tráfego em cada site (número de usuários e número médio de chamadas por hora por hora por usuário).</span><span class="sxs-lookup"><span data-stu-id="cfef7-136">Estimate the traffic at each site (number of users and average number of calls per hour per user).</span></span>

3.  <span data-ttu-id="cfef7-137">Implante um ou mais gateways em cada site para manipular o tráfego previsto.</span><span class="sxs-lookup"><span data-stu-id="cfef7-137">Deploy one or more gateways at each site to handle the anticipated traffic.</span></span>

<span data-ttu-id="cfef7-138">A topologia de gateway distribuído resultante é mostrada na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="cfef7-138">The resulting distributed gateway topology is shown in the following figure.</span></span>

<span data-ttu-id="cfef7-139">**Topologia de gateway distribuído**</span><span class="sxs-lookup"><span data-stu-id="cfef7-139">**Distributed gateway topology**</span></span>

<span data-ttu-id="cfef7-140">![Diagrama de topologia de gateway distribuído](images/Gg398899.f0f65a0b-a462-491a-878b-4d4bf0a96f6d(OCS.15).jpg "Diagrama de topologia de gateway distribuído")</span><span class="sxs-lookup"><span data-stu-id="cfef7-140">![Distributed Gateway Topology diagram](images/Gg398899.f0f65a0b-a462-491a-878b-4d4bf0a96f6d(OCS.15).jpg "Distributed Gateway Topology diagram")</span></span>

<span data-ttu-id="cfef7-141">Com essa topologia, chamadas entre trabalhadores em cada site e entre sites são roteadas pela intranet.</span><span class="sxs-lookup"><span data-stu-id="cfef7-141">With this topology, calls among workers at each site and between sites are all routed over your intranet.</span></span> <span data-ttu-id="cfef7-142">As chamadas para a PSTN são roteadas na rede de IP da empresa para os gateways mais próximos ao local dos números de destino. Mas e se a sua organização oferecer suporte a dezenas ou centenas de sites ou até a milhares de sites distribuídos em um ou mais continentes, pois muitas instituições financeiras e outras grandes empresas fazem?</span><span class="sxs-lookup"><span data-stu-id="cfef7-142">Calls to the PSTN are routed over the enterprise IP network to the gateways that are closest to the location of the destination numbers.But what if your organization supports dozens or hundreds or even thousands of sites spread across one or more continents, as many financial institutions and other large enterprises do?</span></span> <span data-ttu-id="cfef7-143">Nesses casos, a implantação de um gateway separado em cada site não é prática.</span><span class="sxs-lookup"><span data-stu-id="cfef7-143">In such cases, deploying a separate gateway at each site is not practical.</span></span>

<span data-ttu-id="cfef7-144">Para solucionar esse problema, muitas grandes empresas preferem implantar um ou alguns sites centrais de telefonia grandes, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="cfef7-144">To address this issue, many large companies prefer to deploy one or a few large telephony central sites, as shown in the following figure.</span></span>

<span data-ttu-id="cfef7-145">**Topologia de site central de telefonia**</span><span class="sxs-lookup"><span data-stu-id="cfef7-145">**Telephony central site topology**</span></span>

<span data-ttu-id="cfef7-146">![Topologia de gateway do Data Center](images/Gg398899.927f4808-bf74-405a-be20-2cd9cd87af6d(OCS.15).jpg "Topologia de gateway do Data Center")</span><span class="sxs-lookup"><span data-stu-id="cfef7-146">![Data center gateway topology](images/Gg398899.927f4808-bf74-405a-be20-2cd9cd87af6d(OCS.15).jpg "Data center gateway topology")</span></span>

<span data-ttu-id="cfef7-147">Nessa topologia, vários gateways grandes suficientes para acomodar a carga de usuário prevista são implantados em cada site central.</span><span class="sxs-lookup"><span data-stu-id="cfef7-147">In this topology, several large gateways sufficient to accommodate the anticipated user load are deployed at each central site.</span></span> <span data-ttu-id="cfef7-148">Todas as chamadas para os usuários na empresa são encaminhadas pelo provedor de serviços telefônicos da empresa para um site central.</span><span class="sxs-lookup"><span data-stu-id="cfef7-148">All calls to users in the enterprise are forwarded by the company's telephone service provider to a central site.</span></span> <span data-ttu-id="cfef7-149">A lógica de roteamento no site central determina se a chamada deve ser roteada pela intranet ou pela PSTN.</span><span class="sxs-lookup"><span data-stu-id="cfef7-149">Routing logic at the central site determines whether the call should be routed over the intranet or to the PSTN.</span></span>

</div>

<div>

## <a name="gateway-location"></a><span data-ttu-id="cfef7-150">Localização do gateway</span><span class="sxs-lookup"><span data-stu-id="cfef7-150">Gateway Location</span></span>

<span data-ttu-id="cfef7-151">O local do gateway também pode determinar os tipos de gateway que você escolher e como eles são configurados.</span><span class="sxs-lookup"><span data-stu-id="cfef7-151">Gateway location may also determine the types of gateways that you choose and how they are configured.</span></span> <span data-ttu-id="cfef7-152">Há dezenas de protocolos PSTN, nenhum dos quais é um padrão mundial.</span><span class="sxs-lookup"><span data-stu-id="cfef7-152">There are dozens of PSTN protocols, none of which is a worldwide standard.</span></span> <span data-ttu-id="cfef7-153">Se todos os seus gateways estiverem localizados em um único país/região, isso não é um problema, mas se você localizar gateways em vários países/regiões, cada um deve ser configurado de acordo com os padrões PSTN desse país/região.</span><span class="sxs-lookup"><span data-stu-id="cfef7-153">If all your gateways are located in a single country/region, this is not an issue, but if you locate gateways in several countries/regions, each must be configured according to the PSTN standards of that country/region.</span></span> <span data-ttu-id="cfef7-154">Além disso, os gateways certificados para a operação, por exemplo, no Canadá, podem não ser certificados na Índia, Brasil ou na União Européia.</span><span class="sxs-lookup"><span data-stu-id="cfef7-154">Moreover, gateways that are certified for operation in, for example, Canada, may not be certified in India, Brazil, or the European Union.</span></span>

</div>

<div>

## <a name="gateway-size-and-number"></a><span data-ttu-id="cfef7-155">Tamanho e número do gateway</span><span class="sxs-lookup"><span data-stu-id="cfef7-155">Gateway Size and Number</span></span>

<span data-ttu-id="cfef7-156">Os gateways PSTN que a maioria das organizações considerará a implantação de intervalo em tamanho de 2 a até 960 portas.</span><span class="sxs-lookup"><span data-stu-id="cfef7-156">The PSTN gateways that most organizations will consider deploying range in size from 2 to as many as 960 ports.</span></span> <span data-ttu-id="cfef7-157">(Ainda há gateways maiores, mas eles são usados principalmente por provedores de serviço de telefonia.) Ao estimar o número de portas necessárias para sua organização, use as seguintes diretrizes:</span><span class="sxs-lookup"><span data-stu-id="cfef7-157">(There are even larger gateways, but these are used mainly by telephone service providers.) When estimating the number of ports your organization requires, use the following guidelines:</span></span>

  - <span data-ttu-id="cfef7-158">Organizações com uso leve de telefonia (uma chamada PSTN por usuário por hora) devem atribuir uma porta para cada 15 usuários.</span><span class="sxs-lookup"><span data-stu-id="cfef7-158">Organizations with light telephony usage (one PSTN call per user per hour) should allocate one port for every 15 users.</span></span> <span data-ttu-id="cfef7-159">Por exemplo, se você tiver 20 usuários, será necessário um gateway com duas portas.</span><span class="sxs-lookup"><span data-stu-id="cfef7-159">For example, if you have 20 users, you will require a gateway with two ports.</span></span>

  - <span data-ttu-id="cfef7-160">Organizações com uso moderado de telefonia (duas chamadas PSTN por usuário por hora) devem atribuir uma porta para cada 10 usuários.</span><span class="sxs-lookup"><span data-stu-id="cfef7-160">Organizations with moderate telephony usage (two PSTN calls per user per hour) should allocate one port for every 10 users.</span></span> <span data-ttu-id="cfef7-161">Por exemplo, se você tiver usuários do 100, precisará de um total de 10 portas alocadas entre um ou mais gateways.</span><span class="sxs-lookup"><span data-stu-id="cfef7-161">For example, if you have 100 users, you will require a total of 10 ports allocated among one or more gateways.</span></span>

  - <span data-ttu-id="cfef7-162">Organizações com uso intenso de telefonia (três ou mais chamadas PSTN por usuário por hora) devem atribuir uma porta para cada cinco usuários.</span><span class="sxs-lookup"><span data-stu-id="cfef7-162">Organizations with heavy telephony usage (three or more PSTN calls per user per hour) should allocate one port for every five users.</span></span> <span data-ttu-id="cfef7-163">Por exemplo, se você tiver usuários do 47.000, precisará de um total de 9.400 portas alocadas entre pelo menos 10 gateways maiores.</span><span class="sxs-lookup"><span data-stu-id="cfef7-163">For example, if you have 47,000 users, you will require a total of 9,400 ports allocated among at least 10 large gateways.</span></span>

  - <span data-ttu-id="cfef7-164">Portas adicionais podem ser adquiridas à medida que aumenta o número de usuários ou o volume de tráfego da sua organização.</span><span class="sxs-lookup"><span data-stu-id="cfef7-164">Additional ports can be acquired as the number of users or amount of traffic in your organization increases.</span></span>

<span data-ttu-id="cfef7-165">Para qualquer número específico de usuários que você precisa dar suporte, você tem a opção de implantar mais gateways ou menos, ou menores.</span><span class="sxs-lookup"><span data-stu-id="cfef7-165">For any given number of users you must support, you have the choice of deploying fewer, larger gateways, or smaller ones.</span></span> <span data-ttu-id="cfef7-166">Como regra, um mínimo de dois gateways para uma organização é recomendado para manter a disponibilidade se um gateway falha.</span><span class="sxs-lookup"><span data-stu-id="cfef7-166">As a rule, a minimum of two gateways for an organization is recommended to maintain availability if one gateway fails.</span></span>

<span data-ttu-id="cfef7-167">Cada gateway PSTN que você implantar deve ter pelo menos um servidor de mediação correspondente.</span><span class="sxs-lookup"><span data-stu-id="cfef7-167">Each PSTN gateway that you deploy must have at least one corresponding Mediation Server.</span></span>

<span data-ttu-id="cfef7-168"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cfef7-168"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

