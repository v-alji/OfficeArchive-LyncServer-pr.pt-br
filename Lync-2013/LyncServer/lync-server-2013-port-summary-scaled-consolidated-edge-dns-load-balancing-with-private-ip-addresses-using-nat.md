---
title: 'Lync Server 2013: Resumo de porta - borda consolidada em escala, balanceamento de carga de DNS com endereços IP privados usando NAT'
description: 'Lync Server 2013: Resumo da porta – borda consolidada dimensionada, balanceamento de carga de DNS com endereços IP privados usando NAT.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT
ms:assetid: a296c2af-54d4-4b4f-9795-9191baf688cb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412756(v=OCS.15)
ms:contentKeyID: 48184955
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e0402b6682e86e5edf263fca78dfbe0f8fa070b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424280"
---
# <a name="port-summary---scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="2e19e-103">Resumo de porta - borda consolidada em escala, balanceamento de carga de DNS com endereços IP privados usando NAT no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2e19e-103">Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2e19e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2e19e-104">

<span> </span></span></span>

<span data-ttu-id="2e19e-105">_**Tópico da última modificação:** 2012-12-04_</span><span class="sxs-lookup"><span data-stu-id="2e19e-105">_**Topic Last Modified:** 2012-12-04_</span></span>

<span data-ttu-id="2e19e-106">A funcionalidade do servidor de borda do Lync Server 2013 descrita nesta arquitetura de cenário é muito semelhante à implementada no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="2e19e-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="2e19e-107">A adição mais perceptível é a porta **5269 sobre** a entrada TCP para o protocolo de mensagens extensíveis e de presença (XMPP).</span><span class="sxs-lookup"><span data-stu-id="2e19e-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="2e19e-108">O Lync Server 2013, opcionalmente, implanta um proxy XMPP no servidor de borda ou no pool de periféricos e o servidor de Gateway XMPP no servidor front-end ou no pool de front-end.</span><span class="sxs-lookup"><span data-stu-id="2e19e-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="2e19e-109">Além do IPv4, o servidor de borda agora oferece suporte ao IPv6.</span><span class="sxs-lookup"><span data-stu-id="2e19e-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="2e19e-110">Para fins de clareza, somente o IPv4 é usado nos cenários.</span><span class="sxs-lookup"><span data-stu-id="2e19e-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="2e19e-111">**Rede de perímetro da empresa para borda consolidada dimensionada com endereços IP privados usando NAT**</span><span class="sxs-lookup"><span data-stu-id="2e19e-111">**Enterprise perimeter network for scaled consolidated edge with private IP addresses using NAT**</span></span>

<span data-ttu-id="2e19e-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span><span class="sxs-lookup"><span data-stu-id="2e19e-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="2e19e-113">Detalhes de protocolo e porta</span><span class="sxs-lookup"><span data-stu-id="2e19e-113">Port and Protocol Details</span></span>

<span data-ttu-id="2e19e-114">É recomendável que você abra apenas as portas necessárias para dar suporte à funcionalidade para a qual você está fornecendo acesso externo.</span><span class="sxs-lookup"><span data-stu-id="2e19e-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="2e19e-115">Para que o acesso remoto funcione para qualquer serviço de borda, é obrigatório que o tráfego SIP tenha permissão de fluxo bidirecional, conforme mostrado na figura de tráfego de borda de entrada/saída.</span><span class="sxs-lookup"><span data-stu-id="2e19e-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="2e19e-116">Declarado de outra maneira, o recurso de mensagens SIP para e do serviço de borda de acesso está envolvido em mensagens instantâneas (IM), presença, Web conferência, áudio/vídeo (A/V) e Federação.</span><span class="sxs-lookup"><span data-stu-id="2e19e-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="2e19e-117">Resumo de firewall para borda consolidada dimensionada, balanceamento de carga de DNS com endereços IP privados usando NAT: interface externa – nó 1 e nó 2 (exemplo)</span><span class="sxs-lookup"><span data-stu-id="2e19e-117">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2e19e-118">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="2e19e-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="2e19e-119">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="2e19e-119">Source IP address</span></span></th>
<th><span data-ttu-id="2e19e-120">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="2e19e-120">Destination IP address</span></span></th>
<th><span data-ttu-id="2e19e-121">Notas</span><span class="sxs-lookup"><span data-stu-id="2e19e-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="2e19e-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="2e19e-123">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-123">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-124">Serviço de proxy XMPP (compartilha o endereço IP com o serviço de borda de acesso)</span><span class="sxs-lookup"><span data-stu-id="2e19e-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="2e19e-125">O serviço de proxy XMPP aceita o tráfego de contatos do XMPP em agrupamentos XMPP definidos</span><span class="sxs-lookup"><span data-stu-id="2e19e-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-126">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="2e19e-126">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="2e19e-127">Serviço de proxy XMPP (compartilha o endereço IP com o serviço de borda de acesso)</span><span class="sxs-lookup"><span data-stu-id="2e19e-127">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="2e19e-128">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-128">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-129">O serviço de proxy XMPP envia o tráfego para os contatos do XMPP em federações XMPP definidas</span><span class="sxs-lookup"><span data-stu-id="2e19e-129">XMPP Proxy service sends traffic to XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-130">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="2e19e-130">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="2e19e-131">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-131">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-132">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-132">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-133">Revogação e verificação de revogação/revogação de certificados e recuperação</span><span class="sxs-lookup"><span data-stu-id="2e19e-133">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-134">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="2e19e-134">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="2e19e-135">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-135">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-136">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-136">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-137">Consulta DNS via TCP</span><span class="sxs-lookup"><span data-stu-id="2e19e-137">DNS query over TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-138">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="2e19e-138">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="2e19e-139">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-139">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-140">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-140">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-141">Consulta DNS via UDP</span><span class="sxs-lookup"><span data-stu-id="2e19e-141">DNS query over UDP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-142">/TCP/443 de acesso/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="2e19e-142">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="2e19e-143">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-143">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-144">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-144">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-145">Tráfego SIP de cliente para servidor para acesso de usuário externo</span><span class="sxs-lookup"><span data-stu-id="2e19e-145">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-146">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="2e19e-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="2e19e-147">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-147">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-148">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-148">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-149">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="2e19e-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-150">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="2e19e-150">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="2e19e-151">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-151">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-152">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-152">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-153">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="2e19e-153">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-154">Web Conferencing/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="2e19e-154">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="2e19e-155">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-155">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-156">Serviço de borda de Webconferência Web Edge Server</span><span class="sxs-lookup"><span data-stu-id="2e19e-156">Edge Server Web Conferencing Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-157">Mídia de Webconferência</span><span class="sxs-lookup"><span data-stu-id="2e19e-157">Web Conferencing media</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-158">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="2e19e-158">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="2e19e-159">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="2e19e-159">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-160">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-160">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-161">Obrigatório para federação com parceiros que executam o Office Communications Server 2007, o Office Communications Server 2007 R2, o Lync Server 2010 e o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2e19e-161">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-162">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="2e19e-162">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="2e19e-163">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="2e19e-163">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-164">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-164">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-165">Obrigatório somente para federação com parceiros que executam o Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="2e19e-165">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-166">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="2e19e-166">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="2e19e-167">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-167">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-168">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="2e19e-168">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-169">Obrigatório somente para federação com parceiros que executam o Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="2e19e-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-170">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="2e19e-170">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="2e19e-171">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-171">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-172">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="2e19e-172">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-173">Obrigatório somente para federação com parceiros que executam o Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="2e19e-173">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-174">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="2e19e-174">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="2e19e-175">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="2e19e-175">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-176">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-176">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-177">3478 a saída é usada para determinar a versão do servidor de borda com a qual o Lync Server está se comunicando e também para o tráfego de mídia do servidor edge edge-to-edge.</span><span class="sxs-lookup"><span data-stu-id="2e19e-177">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="2e19e-178">Obrigatório para federação com o Lync Server 2010, o Windows Live Messenger e o Office Communications Server 2007 R2 e também se vários pools de bordas forem implantados em uma empresa.</span><span class="sxs-lookup"><span data-stu-id="2e19e-178">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-179">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="2e19e-179">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="2e19e-180">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-180">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-181">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="2e19e-181">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-182">STUN/desliga a negociação de candidatos via UDP/3478</span><span class="sxs-lookup"><span data-stu-id="2e19e-182">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-183">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="2e19e-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="2e19e-184">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-184">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-185">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="2e19e-185">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-186">STUN/TRANSFORMe a negociação de candidatos via TCP/443</span><span class="sxs-lookup"><span data-stu-id="2e19e-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-187">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="2e19e-187">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="2e19e-188">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="2e19e-188">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-189">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-189">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-190">STUN/TRANSFORMe a negociação de candidatos via TCP/443</span><span class="sxs-lookup"><span data-stu-id="2e19e-190">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-internal-interface--node-1-and-node-2-example"></a><span data-ttu-id="2e19e-191">Resumo de firewall para borda consolidada dimensionada, balanceamento de carga de DNS com endereços IP privados usando NAT: interface interna – nó 1 e nó 2 (exemplo)</span><span class="sxs-lookup"><span data-stu-id="2e19e-191">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT: Internal Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2e19e-192">Protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="2e19e-192">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="2e19e-193">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="2e19e-193">Source IP address</span></span></th>
<th><span data-ttu-id="2e19e-194">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="2e19e-194">Destination IP address</span></span></th>
<th><span data-ttu-id="2e19e-195">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e19e-195">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-196">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="2e19e-196">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="2e19e-197">Any (pode ser definido como endereço do servidor front-end ou endereço IP do pool de front-end executando o serviço de gateway do XMPP)</span><span class="sxs-lookup"><span data-stu-id="2e19e-197">Any (can be defined as Front End Server address, or Front End pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="2e19e-198">Endereço IP da interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-198">Edge Server internal interface IP address</span></span></p></td>
<td><p><span data-ttu-id="2e19e-199">Tráfego de XMPP de saída do serviço de gateway do XMPP em execução em servidor front-end ou pool de front-end</span><span class="sxs-lookup"><span data-stu-id="2e19e-199">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="2e19e-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="2e19e-201">Any (pode ser definido como director, endereço IP do pool do diretor, servidor front-end ou endereço IP do pool de front-end)</span><span class="sxs-lookup"><span data-stu-id="2e19e-201">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="2e19e-202">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="2e19e-203">Tráfego SIP de saída (do director, endereço IP do pool do diretor, servidor front-end ou endereço IP do pool de front-end) para a interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-203">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-204">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="2e19e-204">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="2e19e-205">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-205">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="2e19e-206">Any (pode ser definido como director, endereço IP do pool do diretor, servidor front-end ou endereço IP do pool de front-end)</span><span class="sxs-lookup"><span data-stu-id="2e19e-206">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="2e19e-207">Tráfego SIP de entrada (para o director, endereço IP do pool do diretor, servidor front-end ou endereço IP do pool de front-end) da interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-207">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-208">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="2e19e-208">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="2e19e-209">Any (pode ser definido como o endereço IP do servidor front-end ou cada endereço IP do servidor front-end em um pool Front-end)</span><span class="sxs-lookup"><span data-stu-id="2e19e-209">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="2e19e-210">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="2e19e-211">Tráfego de Webconferência do servidor front-end ou de cada servidor front-end se estiver em um pool, para a interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-211">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-212">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="2e19e-212">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="2e19e-213">Any (pode ser definido como endereço IP do servidor front-end ou endereço IP do pool de front-end ou qualquer aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes que use este servidor de borda)</span><span class="sxs-lookup"><span data-stu-id="2e19e-213">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="2e19e-214">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="2e19e-215">Autenticação de usuários de A/V (serviço de autenticação A/V) do servidor front-end ou do endereço IP do pool de front-end ou qualquer aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes que use este servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-215">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-216">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="2e19e-216">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="2e19e-217">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-217">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-218">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="2e19e-219">Caminho preferencial para transferência de mídia A/V entre usuários internos e externos, aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes</span><span class="sxs-lookup"><span data-stu-id="2e19e-219">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-220">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="2e19e-220">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="2e19e-221">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-221">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-222">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="2e19e-223">Caminho de fallback para transferência de mídia A/V entre usuários internos e externos, aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes se não for possível estabelecer comunicação UDP, o TCP será usado para transferência de arquivos e compartilhamento de área de trabalho</span><span class="sxs-lookup"><span data-stu-id="2e19e-223">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-224">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="2e19e-224">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="2e19e-225">Any (pode ser definido como o endereço IP do servidor front-end ou o pool que mantém o repositório de gerenciamento central)</span><span class="sxs-lookup"><span data-stu-id="2e19e-225">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="2e19e-226">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="2e19e-227">Replicação de alterações do repositório de gerenciamento central para o servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-227">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-228">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="2e19e-228">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="2e19e-229">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-229">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-230">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="2e19e-231">Controlador de serviço de log centralizado usando cmdlets do Shell de gerenciamento do Lync Server e do serviço de log centralizado, comandos de linha de comando do ClsController (ClsController.exe) ou de agente (ClsAgent.exe) e coleção de logs</span><span class="sxs-lookup"><span data-stu-id="2e19e-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-232">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="2e19e-232">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="2e19e-233">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-233">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-234">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="2e19e-235">Controlador de serviço de log centralizado usando cmdlets do Shell de gerenciamento do Lync Server e do serviço de log centralizado, comandos de linha de comando do ClsController (ClsController.exe) ou de agente (ClsAgent.exe) e coleção de logs</span><span class="sxs-lookup"><span data-stu-id="2e19e-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-236">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="2e19e-236">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="2e19e-237">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-237">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-238">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-238">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="2e19e-239">Controlador de serviço de log centralizado usando cmdlets do Shell de gerenciamento do Lync Server e do serviço de log centralizado, comandos de linha de comando do ClsController (ClsController.exe) ou de agente (ClsAgent.exe) e coleção de logs</span><span class="sxs-lookup"><span data-stu-id="2e19e-239">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="2e19e-240">Resumo do firewall para Federação</span><span class="sxs-lookup"><span data-stu-id="2e19e-240">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2e19e-241">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="2e19e-241">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="2e19e-242">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="2e19e-242">Source IP address</span></span></th>
<th><span data-ttu-id="2e19e-243">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="2e19e-243">Destination IP address</span></span></th>
<th><span data-ttu-id="2e19e-244">Notas</span><span class="sxs-lookup"><span data-stu-id="2e19e-244">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-245">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="2e19e-245">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="2e19e-246">Endereço IP público do serviço de borda do Access</span><span class="sxs-lookup"><span data-stu-id="2e19e-246">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="2e19e-247">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-247">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-248">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="2e19e-248">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="2e19e-249">Resumo do Firewall – Conectividade de mensagens instantâneas públicas</span><span class="sxs-lookup"><span data-stu-id="2e19e-249">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2e19e-250">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="2e19e-250">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="2e19e-251">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="2e19e-251">Source IP address</span></span></th>
<th><span data-ttu-id="2e19e-252">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="2e19e-252">Destination IP address</span></span></th>
<th><span data-ttu-id="2e19e-253">Notas</span><span class="sxs-lookup"><span data-stu-id="2e19e-253">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-254">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="2e19e-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="2e19e-255">Parceiros de conectividade de mensagens de chat públicas</span><span class="sxs-lookup"><span data-stu-id="2e19e-255">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="2e19e-256">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-256">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-257">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="2e19e-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-258">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="2e19e-258">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="2e19e-259">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-259">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-260">Parceiros de conectividade de mensagens de chat públicas</span><span class="sxs-lookup"><span data-stu-id="2e19e-260">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="2e19e-261">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="2e19e-261">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-262">/TCP/443 de acesso/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="2e19e-262">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="2e19e-263">Clientes</span><span class="sxs-lookup"><span data-stu-id="2e19e-263">Clients</span></span></p></td>
<td><p><span data-ttu-id="2e19e-264">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-264">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-265">Tráfego SIP de cliente para servidor para acesso de usuário externo</span><span class="sxs-lookup"><span data-stu-id="2e19e-265">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-266">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="2e19e-266">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="2e19e-267">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="2e19e-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-268">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="2e19e-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="2e19e-269">Usado para sessões de A/V com o Windows Live Messenger se a conectividade de mensagem de chat pública estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="2e19e-269">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-270">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="2e19e-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="2e19e-271">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="2e19e-271">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-272">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="2e19e-272">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="2e19e-273">Necessário para conectividade de IM pública com o Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="2e19e-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-274">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="2e19e-274">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="2e19e-275">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="2e19e-275">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="2e19e-276">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="2e19e-276">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="2e19e-277">Necessário para conectividade de IM pública com o Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="2e19e-277">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="2e19e-278">Resumo de firewall para mensagens extensíveis e protocolo de presença</span><span class="sxs-lookup"><span data-stu-id="2e19e-278">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2e19e-279">Protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="2e19e-279">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="2e19e-280">Fonte (endereço IP)</span><span class="sxs-lookup"><span data-stu-id="2e19e-280">Source (IP address)</span></span></th>
<th><span data-ttu-id="2e19e-281">Destino (endereço IP)</span><span class="sxs-lookup"><span data-stu-id="2e19e-281">Destination (IP address)</span></span></th>
<th><span data-ttu-id="2e19e-282">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e19e-282">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-283">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="2e19e-283">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="2e19e-284">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-284">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-285">Endereço IP da interface do serviço de borda do acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="2e19e-286">Porta de comunicação de servidor para servidor padrão para XMPP.</span><span class="sxs-lookup"><span data-stu-id="2e19e-286">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="2e19e-287">Permite a comunicação com o servidor de borda XMPP o proxy de parceiros de XMPP federado</span><span class="sxs-lookup"><span data-stu-id="2e19e-287">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e19e-288">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="2e19e-288">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="2e19e-289">Endereço IP da interface do serviço de borda do acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="2e19e-289">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="2e19e-290">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-290">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-291">Porta de comunicação de servidor para servidor padrão para XMPP.</span><span class="sxs-lookup"><span data-stu-id="2e19e-291">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="2e19e-292">Permite a comunicação do proxy do servidor de borda XMPP com parceiros do XMPP federado</span><span class="sxs-lookup"><span data-stu-id="2e19e-292">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e19e-293">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="2e19e-293">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="2e19e-294">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="2e19e-294">Any</span></span></p></td>
<td><p><span data-ttu-id="2e19e-295">Cada IP de interface do servidor de borda interna</span><span class="sxs-lookup"><span data-stu-id="2e19e-295">Each internal Edge Server interface IP</span></span></p></td>
<td><p><span data-ttu-id="2e19e-296">Tráfego de XMPP interno do Gateway XMPP no servidor front-end ou do pool de front-end para o endereço IP interno do servidor de borda ou o endereço IP interno de cada membro do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="2e19e-296">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2e19e-297">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2e19e-297">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

