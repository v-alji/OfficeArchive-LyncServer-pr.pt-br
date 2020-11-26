---
title: 'Lync Server 2013: visão geral do controle de admissão de chamadas'
description: 'Lync Server 2013: visão geral do controle de admissão de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of call admission control
ms:assetid: 6fda0195-4c89-4dea-82e8-624f03e3d062
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398529(v=OCS.15)
ms:contentKeyID: 48184474
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b0fe2fc75ea9bc887709b7dbe1c2128513fcff6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424763"
---
# <a name="overview-of-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="630fd-103">Visão geral do controle de admissão de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="630fd-103">Overview of call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="630fd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="630fd-104">

<span> </span></span></span>

<span data-ttu-id="630fd-105">_**Tópico da última modificação:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="630fd-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="630fd-106">As comunicações em tempo real são sensíveis à latência e perda de pacotes que podem ocorrer em redes congestionadas.</span><span class="sxs-lookup"><span data-stu-id="630fd-106">Real-time communications are sensitive to the latency and packet loss that can occur on congested networks.</span></span> <span data-ttu-id="630fd-107">O CAC (serviço de controle de admissão de chamadas) determina, com base na largura de banda da rede disponível, se será permitido estabelecer sessões de comunicação em tempo real, como chamadas de voz ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="630fd-107">Call admission control (CAC) determines, based on available network bandwidth, whether to allow real-time communications sessions such as voice or video calls to be established.</span></span> <span data-ttu-id="630fd-108">O design do CAC no Lync Server 2013 oferece quatro atributos principais:</span><span class="sxs-lookup"><span data-stu-id="630fd-108">The CAC design in Lync Server 2013 offers four main attributes:</span></span>

  - <span data-ttu-id="630fd-109">É simples implantar e gerenciar sem exigir equipamento adicional, como roteadores especialmente configurados.</span><span class="sxs-lookup"><span data-stu-id="630fd-109">It is simple to deploy and manage without requiring additional equipment, such as specially configured routers.</span></span>

  - <span data-ttu-id="630fd-110">Ele aborda casos críticos de uso de comunicações unificadas, como usuários móveis e vários pontos de presença.</span><span class="sxs-lookup"><span data-stu-id="630fd-110">It addresses critical unified communications use cases, such as roaming users and multiple points of presence.</span></span> <span data-ttu-id="630fd-111">Políticas do CAC são impostas de acordo com o local em que o ponto de extremidade está localizado, não onde o usuário está hospedado.</span><span class="sxs-lookup"><span data-stu-id="630fd-111">CAC policies are enforced according to where the endpoint is located, not where the user is homed.</span></span>

  - <span data-ttu-id="630fd-112">Além de chamadas de voz, ela pode ser aplicada a outro tráfego, como chamadas com vídeo e sessões de videoconferência/videoconferência.</span><span class="sxs-lookup"><span data-stu-id="630fd-112">In addition to voice calls, it can be applied to other traffic, such as video calls and audio/video conferencing sessions.</span></span>

  - <span data-ttu-id="630fd-113">Fornece a flexibilidade para habilitar a representação de vários tipos de topologias de rede.</span><span class="sxs-lookup"><span data-stu-id="630fd-113">Provides the flexibility to enable representation of various kinds of network topologies.</span></span> <span data-ttu-id="630fd-114">Para obter exemplos, consulte [componentes e topologias do CAC no Lync Server 2013](lync-server-2013-components-and-topologies-for-cac.md).</span><span class="sxs-lookup"><span data-stu-id="630fd-114">For examples, see [Components and topologies for CAC in Lync Server 2013](lync-server-2013-components-and-topologies-for-cac.md).</span></span>

<span data-ttu-id="630fd-115">Se uma nova sessão de voz ou de vídeo exceder os limites de largura de banda definidos em um link de rede de longa distância, a sessão será bloqueada ou (apenas para chamadas telefônicas) redirecionada para a PSTN.</span><span class="sxs-lookup"><span data-stu-id="630fd-115">If a new voice or video session exceeds the bandwidth limits that you have set on a WAN link, the session is either blocked or (for phone calls only) rerouted to the PSTN.</span></span>

<span data-ttu-id="630fd-116">O CAC controla o tráfego em tempo real para voz e vídeo somente.</span><span class="sxs-lookup"><span data-stu-id="630fd-116">CAC controls real-time traffic for voice and video only.</span></span> <span data-ttu-id="630fd-117">Ele não controla o tráfego de dados.</span><span class="sxs-lookup"><span data-stu-id="630fd-117">It does not control data traffic.</span></span>

<span data-ttu-id="630fd-118">Os administradores definem políticas do CAC, que são impostas pelo serviço de política de largura de banda que é instalado com cada pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="630fd-118">Administrators define CAC policies, which are enforced by the Bandwidth Policy Service that is installed with every Front End pool.</span></span> <span data-ttu-id="630fd-119">As configurações de CAC são automaticamente propagadas para todos os servidores de front-end do Lync Server na sua rede.</span><span class="sxs-lookup"><span data-stu-id="630fd-119">CAC settings are automatically propagated to all Lync Server Front End Servers in your network.</span></span>

<span data-ttu-id="630fd-120">Para chamadas que falham devido às políticas do CAC, a ordem de precedência para redirecionar a chamada é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="630fd-120">For calls that fail because of CAC policies, the order of precedence for rerouting the call is as follows:</span></span>

1.  <span data-ttu-id="630fd-121">Internet</span><span class="sxs-lookup"><span data-stu-id="630fd-121">Internet</span></span>

2.  <span data-ttu-id="630fd-122">PSTN</span><span class="sxs-lookup"><span data-stu-id="630fd-122">PSTN</span></span>

3.  <span data-ttu-id="630fd-123">Caixa postal</span><span class="sxs-lookup"><span data-stu-id="630fd-123">Voice mail</span></span>

<span data-ttu-id="630fd-124">A gravação de detalhes de chamadas (CDR) captura informações sobre chamadas redirecionadas para a PSTN ou para a caixa postal.</span><span class="sxs-lookup"><span data-stu-id="630fd-124">Call detail recording (CDR) captures information about calls that are rerouted to the PSTN or to voice mail.</span></span> <span data-ttu-id="630fd-125">A CDR não captura informações sobre chamadas redirecionadas para a Internet, porque a Internet é tratada como um caminho alternativo, em vez de uma opção secundária.</span><span class="sxs-lookup"><span data-stu-id="630fd-125">CDR does not capture information about calls that are rerouted to the Internet, because the Internet is treated as an alternate path rather than a secondary option.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="630fd-126">Os depósitos da caixa postal não serão negados devido a restrições de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="630fd-126">Voice mail deposits will not be denied because of bandwidth constraints.</span></span>



</div>

<span data-ttu-id="630fd-127">O serviço de política de largura de banda gera dois tipos de arquivos de log no formato CSV (valores separados por vírgula).</span><span class="sxs-lookup"><span data-stu-id="630fd-127">The Bandwidth Policy Service generates two types of log files in comma separated values (CSV) format.</span></span> <span data-ttu-id="630fd-128">O arquivo de log de **falhas de verificação** captura informações quando as solicitações de largura de banda são negadas.</span><span class="sxs-lookup"><span data-stu-id="630fd-128">The **check failures** log file captures information when bandwidth requests are denied.</span></span> <span data-ttu-id="630fd-129">O arquivo de log de **utilização do link** captura um instantâneo da topologia de rede e a utilização da largura de banda do link WAN.</span><span class="sxs-lookup"><span data-stu-id="630fd-129">The **link utilization** log file captures a snapshot of the network topology and the WAN link bandwidth utilization.</span></span> <span data-ttu-id="630fd-130">Esses dois arquivos de registro podem ajudá-lo a ajustar suas políticas do CAC com base na utilização.</span><span class="sxs-lookup"><span data-stu-id="630fd-130">Both of these log files can assist you in fine-tuning your CAC policies based on utilization.</span></span>

<div>

## <a name="call-admission-control-considerations"></a><span data-ttu-id="630fd-131">Considerações sobre o controle de admissão de chamadas</span><span class="sxs-lookup"><span data-stu-id="630fd-131">Call Admission Control Considerations</span></span>

<span data-ttu-id="630fd-132">O administrador seleciona a instalação do serviço de política de largura de banda no primeiro pool configurado no site central.</span><span class="sxs-lookup"><span data-stu-id="630fd-132">The administrator selects to install the Bandwidth Policy Service on the first pool configured in the central site.</span></span> <span data-ttu-id="630fd-133">Como há um único site central por região de rede, há apenas um serviço de política de largura de banda por região de rede, que gerencia a política de largura de banda para essa região, seus sites associados e os links para esses sites.</span><span class="sxs-lookup"><span data-stu-id="630fd-133">Since there is a single central site per network region, there is only one Bandwidth Policy Service per network region, which manages bandwidth policy for that region, its associated sites and the links to those sites.</span></span> <span data-ttu-id="630fd-134">O serviço de política de largura de banda é executado como parte dos servidores front-end e, portanto, a alta disponibilidade é interna dentro desse pool.</span><span class="sxs-lookup"><span data-stu-id="630fd-134">The Bandwidth Policy Service runs as part of the Front End Servers, and therefore high availability is built-in within that pool.</span></span> <span data-ttu-id="630fd-135">O serviço de política de largura de banda executado em cada servidor front-end sincroniza a cada 15 segundos.</span><span class="sxs-lookup"><span data-stu-id="630fd-135">The Bandwidth Policy Service running on each Front End Server synchronizes every 15 seconds.</span></span> <span data-ttu-id="630fd-136">Se o pool de front-ends falhar, as políticas do CAC não serão mais impostas para esse site até o pool de front-ends e, consequentemente, o serviço de política de largura de banda ficará operacional novamente.</span><span class="sxs-lookup"><span data-stu-id="630fd-136">If the Front End pool fails, CAC policies are no longer enforced for that site until the Front End pool and consequently the Bandwidth Policy Service becomes operational again.</span></span> <span data-ttu-id="630fd-137">Isso indica que todas as chamadas passarão durante a duração em que o serviço de política de largura de banda está fora do serviço.</span><span class="sxs-lookup"><span data-stu-id="630fd-137">This implies that all calls will go through for the duration the Bandwidth Policy Service is out of service.</span></span> <span data-ttu-id="630fd-138">Portanto, há a possibilidade de largura de banda superassinatura de seus links durante este período</span><span class="sxs-lookup"><span data-stu-id="630fd-138">Therefore there is the possibility of bandwidth oversubscription of your links during this period</span></span>

<span data-ttu-id="630fd-139">O serviço de política de largura de banda fornece alta disponibilidade em um pool de front-end; no entanto, ele não fornece redundância entre pools de front-end.</span><span class="sxs-lookup"><span data-stu-id="630fd-139">The Bandwidth Policy Service provides high availability within a Front End pool; however, it does not provide redundancy across Front End pools.</span></span> <span data-ttu-id="630fd-140">O serviço de política de largura de banda não pode fazer failover de um pool de front-end para outro.</span><span class="sxs-lookup"><span data-stu-id="630fd-140">The Bandwidth Policy Service cannot failover from one Front End pool to another.</span></span> <span data-ttu-id="630fd-141">Uma vez que o serviço para o pool de front-end seja restaurado, o serviço de política de largura de banda é retomado e pode impor verificações de política de largura</span><span class="sxs-lookup"><span data-stu-id="630fd-141">Once service to the Front End pool is restored, the Bandwidth Policy Service is resumed and can enforce bandwidth policy checks again.</span></span>

<div>

## <a name="network-considerations"></a><span data-ttu-id="630fd-142">Considerações de rede</span><span class="sxs-lookup"><span data-stu-id="630fd-142">Network Considerations</span></span>

<span data-ttu-id="630fd-143">Embora a restrição de largura de banda para áudio e vídeo seja imposta pelo serviço de política de largura de banda no Lync Server 2013, essa restrição não é imposta no roteador de rede (camada 2 e 3).</span><span class="sxs-lookup"><span data-stu-id="630fd-143">Although bandwidth restriction for audio and video is enforced by the Bandwidth Policy Service in Lync Server 2013, this restriction is not enforced at the network router (layer 2 and 3).</span></span> <span data-ttu-id="630fd-144">Lync Server 2010 o CAC não pode impedir que um aplicativo de dados, por exemplo, consuma toda a largura de banda de rede em um link de WAN, incluindo a largura de banda que é reservada para áudio e vídeo pela sua política do CAC.</span><span class="sxs-lookup"><span data-stu-id="630fd-144">Lync Server 2010 CAC cannot prevent a data application, for example, from consuming the entire network bandwidth on a WAN link, including the bandwidth that is reserved for audio and video by your CAC policy.</span></span> <span data-ttu-id="630fd-145">Para proteger a largura de banda necessária na sua rede, você pode implantar um protocolo de QoS (qualidade de serviço), como serviços diferenciados (DiffServ).</span><span class="sxs-lookup"><span data-stu-id="630fd-145">To protect the necessary bandwidth on your network, you can deploy a Quality of Service (QoS) protocol such as Differentiated Services (DiffServ).</span></span> <span data-ttu-id="630fd-146">Portanto, uma prática recomendada é coordenar as políticas de largura de banda do CAC que você define com qualquer configuração de QoS que possa ser implantada.</span><span class="sxs-lookup"><span data-stu-id="630fd-146">Therefore, a best practice is to coordinate the CAC bandwidth policies you define with any QoS settings that you might deploy.</span></span>

</div>

<div>

## <a name="media-and-signaling-paths-over-vpn"></a><span data-ttu-id="630fd-147">Caminhos de mídia e sinalização via VPN</span><span class="sxs-lookup"><span data-stu-id="630fd-147">Media and Signaling Paths over VPN</span></span>

<span data-ttu-id="630fd-148">Se a sua empresa for compatível com mídia via VPN, certifique-se de que tanto o fluxo de mídia quanto o fluxo de sinalização passem pela VPN ou ambos sejam roteados pela Internet.</span><span class="sxs-lookup"><span data-stu-id="630fd-148">If your enterprise supports media through VPN, ensure that either both the media stream and the signaling stream go through the VPN or both are routed through the internet.</span></span> <span data-ttu-id="630fd-149">Por padrão, a mídia e os fluxos de sinalização passam pelo túnel VPN.</span><span class="sxs-lookup"><span data-stu-id="630fd-149">By default, the media and signaling streams go through the VPN tunnel.</span></span>

</div>

<div>

## <a name="call-admission-control-of-outside-users"></a><span data-ttu-id="630fd-150">Controle de admissão de chamadas de usuários externos</span><span class="sxs-lookup"><span data-stu-id="630fd-150">Call Admission Control of Outside Users</span></span>

<span data-ttu-id="630fd-151">O controle de admissão de chamadas não é imposto para usuários remotos nos quais o tráfego de rede flui pela Internet.</span><span class="sxs-lookup"><span data-stu-id="630fd-151">Call admission control is not enforced for remote users where the network traffic flows through the Internet.</span></span> <span data-ttu-id="630fd-152">Como o tráfego de mídia está atravessando a Internet, o que não é gerenciado pelo Lync Server, o CAC não pode ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="630fd-152">Because the media traffic is traversing the Internet, which is not managed by Lync Server, CAC cannot be applied.</span></span> <span data-ttu-id="630fd-153">Cheques do CAC serão executados, no entanto, na parte da chamada que flui pela rede da empresa.</span><span class="sxs-lookup"><span data-stu-id="630fd-153">CAC checks will be performed, however, on the portion of the call that flows through the enterprise network.</span></span>

</div>

<div>

## <a name="call-admission-control-of-pstn-connections"></a><span data-ttu-id="630fd-154">Controle de admissão de chamadas de conexões PSTN</span><span class="sxs-lookup"><span data-stu-id="630fd-154">Call Admission Control of PSTN Connections</span></span>

<span data-ttu-id="630fd-155">O controle de admissão de chamadas é aplicável no servidor de mediação independentemente de estar conectado a um IP/PBX, a um gateway PSTN ou a um tronco SIP.</span><span class="sxs-lookup"><span data-stu-id="630fd-155">Call admission control is enforceable on the Mediation Server regardless of whether it is connected to an IP/PBX, a PSTN gateway, or a SIP trunk.</span></span> <span data-ttu-id="630fd-156">Como o servidor de mediação é um agente de usuário back-to-back (B2BUA), ele termina a mídia.</span><span class="sxs-lookup"><span data-stu-id="630fd-156">Because the Mediation Server is a back-to-back user agent (B2BUA), it terminates media.</span></span> <span data-ttu-id="630fd-157">Ele tem dois lados de conexão: um lado conectado ao Lync Server e um lado do gateway, que é conectado a gateways PSTN, IP/PBXs ou troncos SIP.</span><span class="sxs-lookup"><span data-stu-id="630fd-157">It has two connection sides: a side that is connected to Lync Server and a gateway side, which is connected to PSTN gateways, IP/PBXs, or SIP trunks.</span></span> <span data-ttu-id="630fd-158">Para obter detalhes sobre conexões PSTN, consulte [planejando a conectividade PSTN no Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md).</span><span class="sxs-lookup"><span data-stu-id="630fd-158">For details about PSTN connections, see [Planning for PSTN connectivity in Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md).</span></span>

<span data-ttu-id="630fd-159">O CAC pode ser imposto em ambos os lados do servidor de mediação, a menos que a opção ignorar mídia esteja habilitada.</span><span class="sxs-lookup"><span data-stu-id="630fd-159">CAC can be enforced on both sides of the Mediation Server unless media bypass is enabled.</span></span> <span data-ttu-id="630fd-160">Se a bypass de mídia estiver habilitada, o tráfego de mídia não percorrerá o servidor de mediação, mas fluirá diretamente entre o cliente do Lync e o gateway.</span><span class="sxs-lookup"><span data-stu-id="630fd-160">If media bypass is enabled, the media traffic doesn’t traverse the Mediation Server but instead flows directly between the Lync client and the gateway.</span></span> <span data-ttu-id="630fd-161">Nesse caso, o CAC não é necessário.</span><span class="sxs-lookup"><span data-stu-id="630fd-161">In this case, CAC is not needed.</span></span> <span data-ttu-id="630fd-162">Para obter detalhes, consulte [planejando o bypass de mídia no Lync Server 2013](lync-server-2013-planning-for-media-bypass.md).</span><span class="sxs-lookup"><span data-stu-id="630fd-162">For details, see [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md).</span></span>

<span data-ttu-id="630fd-163">A figura a seguir ilustra como o CAC é imposto sobre conexões PSTN com e sem o bypass de mídia habilitado.</span><span class="sxs-lookup"><span data-stu-id="630fd-163">The following figure illustrates how CAC is enforced on PSTN connections with and without media bypass enabled.</span></span>

<span data-ttu-id="630fd-164">**Aplicação de controle de admissão de chamadas em conexões com PSTN**</span><span class="sxs-lookup"><span data-stu-id="630fd-164">**Call admission control enforcement on connections to the PSTN**</span></span>

<span data-ttu-id="630fd-165">![Aplicação de voz do CAC ignorando a imposição de conexão](images/Gg398703.4d66d529-0912-4de1-abec-266f54272eb3(OCS.15).jpg "Aplicação de voz do CAC ignorando a imposição de conexão")</span><span class="sxs-lookup"><span data-stu-id="630fd-165">![Voice CAC Media Bypass Connection Enforcement](images/Gg398703.4d66d529-0912-4de1-abec-266f54272eb3(OCS.15).jpg "Voice CAC Media Bypass Connection Enforcement")</span></span>

</div>

<div>

## <a name="compatibility-of-call-admission-control-with-earlier-versions-of-office-communications-server"></a><span data-ttu-id="630fd-166">Compatibilidade do controle de admissão de chamadas com versões anteriores do Office Communications Server</span><span class="sxs-lookup"><span data-stu-id="630fd-166">Compatibility of Call Admission Control with Earlier Versions of Office Communications Server</span></span>

<span data-ttu-id="630fd-167">O controle de admissão de chamadas pode ser habilitado somente em pontos de extremidade habilitados para o Lync Server 2010 e posteriores.</span><span class="sxs-lookup"><span data-stu-id="630fd-167">Call admission control can be enabled only on endpoints that are enabled for Lync Server 2010 and later.</span></span>

<span data-ttu-id="630fd-168">O controle de admissão de chamadas não pode ser habilitado em pontos de extremidade que executam o Office Communicator 2007 R2 ou anterior.</span><span class="sxs-lookup"><span data-stu-id="630fd-168">Call admission control cannot be enabled on endpoints running Office Communicator 2007 R2 or earlier.</span></span>

<span data-ttu-id="630fd-169">**Aplicativo do CAC em diferentes versões do Lync Server**</span><span class="sxs-lookup"><span data-stu-id="630fd-169">**Application of CAC on different Lync Server versions**</span></span>

<span data-ttu-id="630fd-170">![Diagrama de comparação da versão do CAC do CAC](images/Gg398529.fdbfee7e-15fc-445b-949d-8d61e61ac350(OCS.15).jpg "Diagrama de comparação da versão do CAC do CAC")</span><span class="sxs-lookup"><span data-stu-id="630fd-170">![Voice CAC Version Comparison diagram](images/Gg398529.fdbfee7e-15fc-445b-949d-8d61e61ac350(OCS.15).jpg "Voice CAC Version Comparison diagram")</span></span>

<span data-ttu-id="630fd-171"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="630fd-171"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

