---
title: 'Lync Server 2013: Componentes obrigatórios para acesso de usuário externo'
description: 'Lync Server 2013: componentes necessários para o acesso de usuários externos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components required for external user access
ms:assetid: 2d0f9817-14e7-4109-95dc-62420e3c29e2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425779(v=OCS.15)
ms:contentKeyID: 48183711
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d75ef0c7f2000353a35acefa0b177c90bdcc879b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389899"
---
# <a name="components-required-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="8b75b-103">Componentes obrigatórios para acesso de usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8b75b-103">Components required for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8b75b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8b75b-104">

<span> </span></span></span>

<span data-ttu-id="8b75b-105">_**Tópico da última modificação:** 2014-05-29_</span><span class="sxs-lookup"><span data-stu-id="8b75b-105">_**Topic Last Modified:** 2014-05-29_</span></span>

<span data-ttu-id="8b75b-106">A maioria dos componentes de Borda é implantada em uma rede de perímetro.</span><span class="sxs-lookup"><span data-stu-id="8b75b-106">Most Edge components are deployed in a perimeter network.</span></span> <span data-ttu-id="8b75b-107">Os componentes a seguir compõem a topologia de borda da rede de perímetro.</span><span class="sxs-lookup"><span data-stu-id="8b75b-107">The following components make up the edge topology of the perimeter network.</span></span> <span data-ttu-id="8b75b-108">Exceto onde observado, os componentes fazem parte dos [cenários para o acesso de usuários externos no Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) e na rede de perímetro.</span><span class="sxs-lookup"><span data-stu-id="8b75b-108">Except where noted, the components are part of the [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) and are in the perimeter network.</span></span> <span data-ttu-id="8b75b-109">Os componentes de Borda incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8b75b-109">Edge components include the following:</span></span>

  - <span data-ttu-id="8b75b-110">Edge Servers</span><span class="sxs-lookup"><span data-stu-id="8b75b-110">Edge Servers</span></span>

  - <span data-ttu-id="8b75b-111">Reverse proxies</span><span class="sxs-lookup"><span data-stu-id="8b75b-111">Reverse proxies</span></span>

  - <span data-ttu-id="8b75b-112">Firewalls</span><span class="sxs-lookup"><span data-stu-id="8b75b-112">Firewalls</span></span>

  - <span data-ttu-id="8b75b-113">Diretores (opcional e logicamente localizado na rede interna)</span><span class="sxs-lookup"><span data-stu-id="8b75b-113">Directors (optional, and logically located on the internal network)</span></span>

  - <span data-ttu-id="8b75b-114">Balanceamento de carga para Topologias de Borda Dimensionadas (balanceamento de carga DNS ou um balanceador de carga de hardware)</span><span class="sxs-lookup"><span data-stu-id="8b75b-114">Load balancing for Scaled Edge Topologies (either DNS load balancing or a hardware load balancer)</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="8b75b-p102">O uso do balanceamento de carga de DNS em uma interface e do balanceamento de carga de hardware na outra não é suportado. É preciso usar o balanceamento de carga de hardware ou de DNS nas duas interfaces.</span><span class="sxs-lookup"><span data-stu-id="8b75b-p102">Using DNS load balancing on one interface and hardware load balancing on the other is not supported. You must use hardware load balancing for both interfaces or DNS load balancing for both.</span></span>

    
    </div>

<div>

## <a name="edge-servers"></a><span data-ttu-id="8b75b-117">Servidores de Borda</span><span class="sxs-lookup"><span data-stu-id="8b75b-117">Edge Servers</span></span>

<span data-ttu-id="8b75b-118">Os servidores de borda enviam e recebem tráfego de rede para os serviços oferecidos pela implantação interna por usuários externos.</span><span class="sxs-lookup"><span data-stu-id="8b75b-118">The Edge Servers send and receive network traffic for the services offered by internal deployment by external users.</span></span> <span data-ttu-id="8b75b-119">O servidor de borda executa os seguintes serviços:</span><span class="sxs-lookup"><span data-stu-id="8b75b-119">The Edge Server runs the following services:</span></span>

  - <span data-ttu-id="8b75b-120">**Serviço de borda de acesso**   O serviço de borda de acesso fornece um ponto de conexão confiável e único para tráfego de protocolo de iniciação de sessão de entrada e saída (SIP).</span><span class="sxs-lookup"><span data-stu-id="8b75b-120">**Access Edge service**   The Access Edge service provides a single, trusted connection point for both outbound and inbound Session Initiation Protocol (SIP) traffic.</span></span>

  - <span data-ttu-id="8b75b-121">**Serviço de borda de Webconferência**   O serviço de borda de Webconferência permite que usuários externos ingressem em reuniões hospedadas em sua implantação interna do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8b75b-121">**Web Conferencing Edge service**   The Web Conferencing Edge service enables external users to join meetings that are hosted on your internal Lync Server 2013 deployment.</span></span>

  - <span data-ttu-id="8b75b-122">**Serviço de borda A/V**   O serviço de borda a/V torna o compartilhamento de áudio, vídeo, compartilhamento de aplicativos e transferência de arquivos disponível para usuários externos.</span><span class="sxs-lookup"><span data-stu-id="8b75b-122">**A/V Edge service**   The A/V Edge service makes audio, video, application sharing, and file transfer available to external users.</span></span> <span data-ttu-id="8b75b-123">Seus usuários podem adicionar áudio e vídeo a reuniões que incluam participantes externos, e eles podem se comunicar usando áudio e/ou vídeo diretamente com um usuário externo em sessões ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="8b75b-123">Your users can add audio and video to meetings that include external participants, and they can communicate using audio and/or video directly with an external user in point-to-point sessions.</span></span> <span data-ttu-id="8b75b-124">O serviço de borda a/V também oferece suporte para compartilhamento de área de trabalho e transferência de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8b75b-124">The A/V Edge service also provides support for desktop sharing and file transfer.</span></span>

  - <span data-ttu-id="8b75b-125">**Serviço de proxy XMPP**   O serviço de proxy do XMPP aceita e envia mensagens de protocolo de presença e de mensagens extensíveis (XMPP) para e de parceiros federados XMPP configurados.</span><span class="sxs-lookup"><span data-stu-id="8b75b-125">**XMPP Proxy service**   The XMPP Proxy service accepts and sends extensible messaging and presence protocol (XMPP) messages to and from configured XMPP Federated partners.</span></span>

<span data-ttu-id="8b75b-126">Usuários externos autorizados podem acessar os servidores de borda para se conectar à implantação interna do Lync Server 2013, mas os servidores de borda não fornecem meios para qualquer outro acesso à rede interna.</span><span class="sxs-lookup"><span data-stu-id="8b75b-126">Authorized external users can access the Edge Servers in order to connect to your internal Lync Server 2013 deployment, but the Edge Servers do not provide a means for any other access to the internal network.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8b75b-127">Os servidores de borda são implantados para fornecer conexões para clientes Lync habilitados e outros servidores Microsoft Edge (como em cenários de Federação).</span><span class="sxs-lookup"><span data-stu-id="8b75b-127">Edge servers are deployed to provide connections for enabled Lync clients and other Microsoft Edge servers (as in federation scenarios).</span></span> <span data-ttu-id="8b75b-128">Elas não são projetadas para permitir conexões de outros tipos de cliente ou servidor de ponto final.</span><span class="sxs-lookup"><span data-stu-id="8b75b-128">They are not designed to allow connections from other end point client or server types.</span></span> <span data-ttu-id="8b75b-129">O servidor de Gateway XMPP pode ser implantado para permitir conexões com os parceiros do XMPP configurados.</span><span class="sxs-lookup"><span data-stu-id="8b75b-129">The XMPP Gateway server can be deployed to allow connections with configured XMPP partners.</span></span> <span data-ttu-id="8b75b-130">O servidor de borda e o Gateway XMPP só podem dar suporte a conexões de ponto de extremidade desses tipos de cliente e de Federação.</span><span class="sxs-lookup"><span data-stu-id="8b75b-130">The Edge server and XMPP Gateway can only support end point connections from these client and federation types.</span></span>



</div>

</div>

<div>

## <a name="reverse-proxy"></a><span data-ttu-id="8b75b-131">Proxy reverso</span><span class="sxs-lookup"><span data-stu-id="8b75b-131">Reverse Proxy</span></span>

<span data-ttu-id="8b75b-132">O proxy reverso é necessário para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8b75b-132">The reverse proxy is required for the following:</span></span>

  - <span data-ttu-id="8b75b-133">Para permitir que os usuários se conectem a reuniões ou conferências discadas usando URLs simples</span><span class="sxs-lookup"><span data-stu-id="8b75b-133">To allow users to connect to meetings or dial-in conferences using simple URLs</span></span>

  - <span data-ttu-id="8b75b-134">Para habilitar usuários externos para baixar o conteúdo da reunião</span><span class="sxs-lookup"><span data-stu-id="8b75b-134">To enable external users to download meeting content</span></span>

  - <span data-ttu-id="8b75b-135">Para permitir que usuários externos expandam grupos de distribuição</span><span class="sxs-lookup"><span data-stu-id="8b75b-135">To enable external users to expand distribution groups</span></span>

  - <span data-ttu-id="8b75b-136">Para permitir que o usuário obtenha um certificado baseado em usuário para autenticação baseada em certificado de cliente</span><span class="sxs-lookup"><span data-stu-id="8b75b-136">To allow the user to obtain a user-based certificate for client certificate based authentication</span></span>

  - <span data-ttu-id="8b75b-137">Para habilitar usuários remotos a baixar arquivos do servidor de catálogo de endereços ou enviar consultas para o serviço de consulta à Web do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="8b75b-137">To enable remote users to download files from the Address Book Server or to submit queries to the Address Book Web Query service</span></span>

  - <span data-ttu-id="8b75b-138">Para permitir que os usuários remotos obtenham atualizações para software cliente e dispositivo</span><span class="sxs-lookup"><span data-stu-id="8b75b-138">To enable remote users to obtain updates to client and device software</span></span>

  - <span data-ttu-id="8b75b-139">Para habilitar dispositivos móveis para detectar automaticamente servidores front-end que oferecem serviços de mobilidade</span><span class="sxs-lookup"><span data-stu-id="8b75b-139">To enable mobile devices to automatically discover Front End Servers offering mobility services</span></span>

  - <span data-ttu-id="8b75b-140">Para habilitar as notificações por push para dispositivos móveis dos serviços de notificação por push do Microsoft 365, do Office 365 ou da Apple push</span><span class="sxs-lookup"><span data-stu-id="8b75b-140">To enable push notifications to mobile devices from the Microsoft 365, Office 365, or Apple push notification services</span></span>

<span data-ttu-id="8b75b-141">Para obter informações adicionais relacionadas a proxies invertidos e os requisitos que os proxies inversos devem atender, consulte os detalhes em [requisitos de configuração para o proxy inverso no Lync Server 2013](lync-server-2013-configuration-requirements-for-reverse-proxy.md).</span><span class="sxs-lookup"><span data-stu-id="8b75b-141">For additional information related to reverse proxies and the requirements that reverse proxies must meet, see the details in [Configuration requirements for reverse proxy in Lync Server 2013](lync-server-2013-configuration-requirements-for-reverse-proxy.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8b75b-142">Os usuários externos não precisam de uma conexão de rede virtual privada (VPN) à sua organização para participar de comunicações usando o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8b75b-142">External users do not need a virtual private network (VPN) connection to your organization in order to participate in communications using Lync Server 2013.</span></span> <span data-ttu-id="8b75b-143">Se você implementou a tecnologia VPN em sua organização e seus usuários usam a VPN para o Lync, o tráfego de mídia (como videoconferência) pode ser afetado negativamente.</span><span class="sxs-lookup"><span data-stu-id="8b75b-143">If you have implemented VPN technology in your organization and your users use the VPN for Lync, media traffic (such as video conferencing) can be adversely affected.</span></span> <span data-ttu-id="8b75b-144">Você deve considerar o fornecimento de um meio para tráfego de mídia para se conectar ao serviço de borda de AV diretamente e ignorar a VPN.</span><span class="sxs-lookup"><span data-stu-id="8b75b-144">You should consider providing a means for media traffic to connect to the AV Edge service directly and bypass the VPN.</span></span> <span data-ttu-id="8b75b-145">Para obter detalhes, consulte o artigo sobre o blog NextHop, "Ativando o Lync Media para ignorar um túnel VPN" <A href="https://go.microsoft.com/fwlink/p/?linkid=256532">https://go.microsoft.com/fwlink/p/?LinkId=256532</A> .</span><span class="sxs-lookup"><span data-stu-id="8b75b-145">For details, see the NextHop Blog article, “Enabling Lync Media to Bypass a VPN Tunnel,” at <A href="https://go.microsoft.com/fwlink/p/?linkid=256532">https://go.microsoft.com/fwlink/p/?LinkId=256532</A>.</span></span>



</div>

</div>

<div>

## <a name="firewall"></a><span data-ttu-id="8b75b-146">Firewall</span><span class="sxs-lookup"><span data-stu-id="8b75b-146">Firewall</span></span>

<span data-ttu-id="8b75b-147">Você pode implantar a topologia de borda com apenas um firewall externo ou firewalls internos e externos.</span><span class="sxs-lookup"><span data-stu-id="8b75b-147">You can deploy your edge topology with only an external firewall or both external and internal firewalls.</span></span> <span data-ttu-id="8b75b-148">As arquiteturas de cenário incluem dois firewalls.</span><span class="sxs-lookup"><span data-stu-id="8b75b-148">The scenario architectures include two firewalls.</span></span> <span data-ttu-id="8b75b-149">Usar dois firewalls é a abordagem recomendada porque garante um roteamento estrito de uma borda de rede para a outra e protege sua implantação interna atrás de dois níveis de firewall.</span><span class="sxs-lookup"><span data-stu-id="8b75b-149">Using two firewalls is the recommended approach because it ensures strict routing from one network edge to the other, and it protects your internal deployment behind two levels of firewall.</span></span>

</div>

<div>

## <a name="director"></a><span data-ttu-id="8b75b-150">Diretor</span><span class="sxs-lookup"><span data-stu-id="8b75b-150">Director</span></span>

<span data-ttu-id="8b75b-151">Um diretor é uma função de servidor opcional separada no Lync Server 2013 que não hospeda contas de usuário nem fornece serviços de presença ou conferência.</span><span class="sxs-lookup"><span data-stu-id="8b75b-151">A Director is a separate, optional server role in Lync Server 2013 that does not home user accounts, or provide presence or conferencing services.</span></span> <span data-ttu-id="8b75b-152">Ele funciona como um servidor de um próximo salto interno ao qual um servidor de Borda roteia o tráfego SIP de entrada destinado para servidores internos.</span><span class="sxs-lookup"><span data-stu-id="8b75b-152">It serves as an internal next hop server to which an Edge Server routes inbound SIP traffic destined for internal servers.</span></span> <span data-ttu-id="8b75b-153">O diretor autentica solicitações de entrada e as redireciona para o pool ou servidor primário do usuário.</span><span class="sxs-lookup"><span data-stu-id="8b75b-153">The Director preauthenticates inbound requests and redirects them to the user’s home pool or server.</span></span> <span data-ttu-id="8b75b-154">Ao autenticar no director, você pode descartar solicitações de contas de usuários desconhecidas para a implantação.</span><span class="sxs-lookup"><span data-stu-id="8b75b-154">By preauthenticating at the Director, you can drop requests from user accounts that are unknown to the deployment.</span></span>

<span data-ttu-id="8b75b-155">Um diretor ajuda a isolar servidores de front-end do Enterprise Edition em pools front-end do Enterprise Edition contra tráfego mal-intencionado, como ataques de negação de serviço (DoS).</span><span class="sxs-lookup"><span data-stu-id="8b75b-155">A Director helps insulate Standard Edition servers and Front End Servers in Enterprise Edition Front End pools from malicious traffic such as denial-of-service (DoS) attacks.</span></span> <span data-ttu-id="8b75b-156">Se a rede estiver inundada com tráfego externo inválido nesse tipo de ataque, o tráfego terminará no diretor.</span><span class="sxs-lookup"><span data-stu-id="8b75b-156">If the network is flooded with invalid external traffic in such an attack, the traffic ends at the Director.</span></span> <span data-ttu-id="8b75b-157">Para obter detalhes sobre o uso de directors, consulte [cenários do diretor do Lync Server 2013](lync-server-2013-scenarios-for-the-director.md).</span><span class="sxs-lookup"><span data-stu-id="8b75b-157">For details about the use of Directors, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8b75b-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b75b-158">See Also</span></span>


[<span data-ttu-id="8b75b-159">Requisitos do balanceador de carga do hardware para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8b75b-159">Hardware load balancer requirements for Lync Server 2013</span></span>](lync-server-2013-hardware-load-balancer-requirements.md)  
  

<span data-ttu-id="8b75b-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8b75b-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

