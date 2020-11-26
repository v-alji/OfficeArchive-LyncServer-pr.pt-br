---
title: Resumo de porta - única borda consolidada com endereços IP privados usando NAT
description: Resumo da porta – borda única consolidada com endereços IP privados usando NAT.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single consolidated edge with private IP addresses using NAT
ms:assetid: 3c1a389f-5f42-4719-a05b-e0b84aa3eb9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425891(v=OCS.15)
ms:contentKeyID: 48183877
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3fc182b9fbbd24d589feb7f73e3c0086fa23152
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424293"
---
# <a name="port-summary---single-consolidated-edge-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="26597-103">Resumo de porta - única borda consolidada com endereços IP privados usando NAT no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26597-103">Port summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="26597-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="26597-104">

<span> </span></span></span>

<span data-ttu-id="26597-105">_**Tópico da última modificação:** 2013-04-03_</span><span class="sxs-lookup"><span data-stu-id="26597-105">_**Topic Last Modified:** 2013-04-03_</span></span>

<span data-ttu-id="26597-106">A funcionalidade do servidor de borda do Lync Server 2013 descrita nesta arquitetura de cenário é muito semelhante à implementada no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="26597-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="26597-107">A adição mais perceptível é a porta **5269 sobre** a entrada TCP para o protocolo de mensagens extensíveis e de presença (XMPP).</span><span class="sxs-lookup"><span data-stu-id="26597-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="26597-108">O Lync Server 2013, opcionalmente, implanta um proxy XMPP no servidor de borda ou no pool de periféricos e o servidor de Gateway XMPP no servidor front-end ou no pool de front-end.</span><span class="sxs-lookup"><span data-stu-id="26597-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="26597-109">Além do IPv4, o servidor de borda agora oferece suporte ao IPv6.</span><span class="sxs-lookup"><span data-stu-id="26597-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="26597-110">Para fins de clareza, somente o IPv4 é usado nos cenários.</span><span class="sxs-lookup"><span data-stu-id="26597-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="26597-111">**Perímetro de rede para um único servidor de borda consolidado com endereçamento IP privado usando NAT**</span><span class="sxs-lookup"><span data-stu-id="26597-111">**Network Perimeter for a Single Consolidated Edge Server with Private IP Addressing Using NAT**</span></span>

<span data-ttu-id="26597-112">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span><span class="sxs-lookup"><span data-stu-id="26597-112">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="26597-113">Detalhes de protocolo e porta</span><span class="sxs-lookup"><span data-stu-id="26597-113">Port and Protocol Details</span></span>

<span data-ttu-id="26597-114">Recomendamos que você abra apenas as portas necessárias para dar suporte à funcionalidade para a qual você está fornecendo acesso externo.</span><span class="sxs-lookup"><span data-stu-id="26597-114">We recommend that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="26597-115">Para que o acesso remoto funcione para qualquer serviço de borda, é obrigatório que o tráfego SIP tenha permissão de fluxo bidirecional, conforme mostrado na figura de tráfego de borda de entrada/saída.</span><span class="sxs-lookup"><span data-stu-id="26597-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="26597-116">Declarado de outra maneira, o recurso de mensagens SIP para e do serviço de borda de acesso está envolvido em mensagens instantâneas (IM), presença, conferência via Web, áudio/vídeo (A/V) e Federação.</span><span class="sxs-lookup"><span data-stu-id="26597-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V), and federation.</span></span>

### <a name="firewall-summary-for-single-consolidated-edge-with-private-ip-addresses-using-nat-external-interface"></a><span data-ttu-id="26597-117">Resumo de firewall para uma única aresta consolidada com endereços IP privados usando NAT: interface externa</span><span class="sxs-lookup"><span data-stu-id="26597-117">Firewall Summary for Single Consolidated Edge with Private IP Addresses using NAT: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26597-118">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="26597-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="26597-119">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="26597-119">Source IP address</span></span></th>
<th><span data-ttu-id="26597-120">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="26597-120">Destination IP address</span></span></th>
<th><span data-ttu-id="26597-121">Notas</span><span class="sxs-lookup"><span data-stu-id="26597-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26597-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="26597-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="26597-123">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-123">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-124">Serviço de proxy XMPP (compartilha o endereço IP com o serviço de borda de acesso)</span><span class="sxs-lookup"><span data-stu-id="26597-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="26597-125">O serviço de proxy XMPP aceita o tráfego de contatos do XMPP em agrupamentos XMPP definidos</span><span class="sxs-lookup"><span data-stu-id="26597-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-126">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="26597-126">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="26597-127">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-127">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-128">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-128">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-129">Revogação e verificação de revogação/revogação de certificados e recuperação</span><span class="sxs-lookup"><span data-stu-id="26597-129">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26597-130">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="26597-130">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="26597-131">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-131">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-132">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-132">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-133">Consulta DNS via TCP</span><span class="sxs-lookup"><span data-stu-id="26597-133">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-134">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="26597-134">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="26597-135">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-135">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-136">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-136">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-137">Consulta DNS via UDP</span><span class="sxs-lookup"><span data-stu-id="26597-137">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26597-138">/TCP/443 de acesso/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="26597-138">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="26597-139">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-139">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-140">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-140">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-141">Tráfego SIP de cliente para servidor para acesso de usuário externo</span><span class="sxs-lookup"><span data-stu-id="26597-141">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-142">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="26597-142">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="26597-143">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-143">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-144">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-144">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-145">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="26597-145">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26597-146">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="26597-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="26597-147">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-147">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-148">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-148">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-149">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="26597-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-150">Web Conferencing/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="26597-150">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="26597-151">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-151">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-152">Serviço de borda de Webconferência Web Edge Server</span><span class="sxs-lookup"><span data-stu-id="26597-152">Edge Server Web Conferencing Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-153">Mídia de Webconferência</span><span class="sxs-lookup"><span data-stu-id="26597-153">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26597-154">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="26597-154">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="26597-155">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="26597-155">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-156">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-156">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-157">Obrigatório para federação com parceiros que executam o Office Communications Server 2007, o Office Communications Server 2007 R2, o Lync Server 2010 e o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="26597-157">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-158">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="26597-158">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="26597-159">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="26597-159">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-160">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-160">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-161">Obrigatório somente para federação com parceiros que executam o Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="26597-161">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26597-162">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="26597-162">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="26597-163">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-163">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-164">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="26597-164">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-165">Obrigatório somente para federação com parceiros que executam o Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="26597-165">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-166">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="26597-166">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="26597-167">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-167">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-168">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="26597-168">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-169">Obrigatório somente para federação com parceiros que executam o Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="26597-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26597-170">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="26597-170">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="26597-171">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="26597-171">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-172">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-172">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-173">3478 a saída é usada para determinar a versão do servidor de borda com a qual o Lync Server está se comunicando e também para o tráfego de mídia do servidor edge edge-to-edge.</span><span class="sxs-lookup"><span data-stu-id="26597-173">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="26597-174">Obrigatório para federação com o Lync Server 2010, o Windows Live Messenger e o Office Communications Server 2007 R2 e também se vários pools de bordas forem implantados em uma empresa.</span><span class="sxs-lookup"><span data-stu-id="26597-174">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-175">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="26597-175">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="26597-176">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-176">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-177">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="26597-177">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-178">STUN/desliga a negociação de candidatos via UDP/3478</span><span class="sxs-lookup"><span data-stu-id="26597-178">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26597-179">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="26597-179">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="26597-180">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-180">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-181">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="26597-181">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-182">STUN/TRANSFORMe a negociação de candidatos via TCP/443</span><span class="sxs-lookup"><span data-stu-id="26597-182">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-183">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="26597-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="26597-184">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="26597-184">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-185">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-185">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-186">STUN/TRANSFORMe a negociação de candidatos via TCP/443</span><span class="sxs-lookup"><span data-stu-id="26597-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-single-consolidated-edge-with-private-ip-addresses-using-nat-internal-interface"></a><span data-ttu-id="26597-187">Resumo de firewall para uma única aresta consolidada com endereços IP privados usando NAT: interface interna</span><span class="sxs-lookup"><span data-stu-id="26597-187">Firewall Summary for Single Consolidated Edge with Private IP Addresses Using NAT: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26597-188">Protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="26597-188">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="26597-189">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="26597-189">Source IP address</span></span></th>
<th><span data-ttu-id="26597-190">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="26597-190">Destination IP address</span></span></th>
<th><span data-ttu-id="26597-191">Comentários</span><span class="sxs-lookup"><span data-stu-id="26597-191">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26597-192">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="26597-192">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="26597-193">Any (pode ser definido como padrão de servidor Standard Edition, endereço IP do servidor Standard Edition ou endereço IP do pool executando o serviço de gateway do XMPP)</span><span class="sxs-lookup"><span data-stu-id="26597-193">Any (can be defined as Standard Edition server IP, Standard Edition server IP address, or pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="26597-194">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="26597-195">Tráfego de XMPP de saída do serviço de gateway do XMPP em execução em servidor front-end ou pool de front-end</span><span class="sxs-lookup"><span data-stu-id="26597-195">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-196">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="26597-196">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="26597-197">Any (pode ser definido como director, endereço IP do pool do diretor, servidor front-end ou endereço IP do pool de front-end)</span><span class="sxs-lookup"><span data-stu-id="26597-197">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="26597-198">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="26597-199">Tráfego SIP de saída (do director, endereço IP do pool do diretor, servidor front-end ou endereço IP do pool de front-end) para a interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-199">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26597-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="26597-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="26597-201">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-201">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="26597-202">Any (pode ser definido como director, endereço IP do pool do diretor, servidor front-end ou endereço IP do pool de front-end)</span><span class="sxs-lookup"><span data-stu-id="26597-202">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="26597-203">Tráfego SIP de entrada (para o director, endereço IP do pool do diretor, servidor front-end ou endereço IP do pool de front-end) da interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-203">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-204">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="26597-204">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="26597-205">Any (pode ser definido como o endereço IP do servidor front-end ou cada endereço IP do servidor front-end em um pool Front-end)</span><span class="sxs-lookup"><span data-stu-id="26597-205">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="26597-206">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-206">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="26597-207">Tráfego de Webconferência do servidor front-end ou de cada servidor front-end se estiver em um pool, para a interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-207">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26597-208">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="26597-208">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="26597-209">Any (pode ser definido como endereço IP do servidor front-end ou endereço IP do pool de front-end ou qualquer aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes que use este servidor de borda)</span><span class="sxs-lookup"><span data-stu-id="26597-209">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="26597-210">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="26597-211">Autenticação de usuários de A/V (serviço de autenticação A/V) do servidor front-end ou do endereço IP do pool de front-end ou qualquer aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes que use este servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-211">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-212">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="26597-212">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="26597-213">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-213">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-214">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="26597-215">Caminho preferencial para transferência de mídia A/V entre usuários internos e externos, aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes</span><span class="sxs-lookup"><span data-stu-id="26597-215">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26597-216">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="26597-216">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="26597-217">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-217">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-218">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="26597-219">Caminho de fallback para transferência de mídia A/V entre usuários internos e externos, aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes se não for possível estabelecer comunicação UDP, o TCP será usado para transferência de arquivos e compartilhamento de área de trabalho</span><span class="sxs-lookup"><span data-stu-id="26597-219">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-220">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="26597-220">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="26597-221">Any (pode ser definido como o endereço IP do servidor front-end ou o pool que mantém o repositório de gerenciamento central)</span><span class="sxs-lookup"><span data-stu-id="26597-221">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="26597-222">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="26597-223">Replicação de alterações do repositório de gerenciamento central para o servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-223">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26597-224">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="26597-224">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="26597-225">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-225">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-226">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="26597-227">Controlador de serviço de log centralizado usando cmdlets do Shell de gerenciamento do Lync Server e do serviço de log centralizado, comandos de linha de comando do ClsController (ClsController.exe) ou de agente (ClsAgent.exe) e coleção de logs</span><span class="sxs-lookup"><span data-stu-id="26597-227">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-228">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="26597-228">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="26597-229">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-229">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-230">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="26597-231">Controlador de serviço de log centralizado usando cmdlets do Shell de gerenciamento do Lync Server e do serviço de log centralizado, comandos de linha de comando do ClsController (ClsController.exe) ou de agente (ClsAgent.exe) e coleção de logs</span><span class="sxs-lookup"><span data-stu-id="26597-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26597-232">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="26597-232">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="26597-233">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-233">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-234">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="26597-235">Controlador de serviço de log centralizado usando cmdlets do Shell de gerenciamento do Lync Server e do serviço de log centralizado, comandos de linha de comando do ClsController (ClsController.exe) ou de agente (ClsAgent.exe) e coleção de logs</span><span class="sxs-lookup"><span data-stu-id="26597-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="26597-236">Resumo do firewall para Federação</span><span class="sxs-lookup"><span data-stu-id="26597-236">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26597-237">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="26597-237">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="26597-238">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="26597-238">Source IP address</span></span></th>
<th><span data-ttu-id="26597-239">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="26597-239">Destination IP address</span></span></th>
<th><span data-ttu-id="26597-240">Notas</span><span class="sxs-lookup"><span data-stu-id="26597-240">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26597-241">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="26597-241">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="26597-242">Endereço IP público do serviço de borda do Access</span><span class="sxs-lookup"><span data-stu-id="26597-242">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="26597-243">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-243">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-244">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="26597-244">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="26597-245">Resumo do Firewall – Conectividade de mensagens instantâneas públicas</span><span class="sxs-lookup"><span data-stu-id="26597-245">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26597-246">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="26597-246">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="26597-247">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="26597-247">Source IP address</span></span></th>
<th><span data-ttu-id="26597-248">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="26597-248">Destination IP address</span></span></th>
<th><span data-ttu-id="26597-249">Notas</span><span class="sxs-lookup"><span data-stu-id="26597-249">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26597-250">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="26597-250">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="26597-251">Parceiros de conectividade de mensagens de chat públicas</span><span class="sxs-lookup"><span data-stu-id="26597-251">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="26597-252">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-252">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-253">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="26597-253">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-254">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="26597-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="26597-255">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-255">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-256">Parceiros de conectividade de mensagens de chat públicas</span><span class="sxs-lookup"><span data-stu-id="26597-256">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="26597-257">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="26597-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26597-258">/TCP/443 de acesso/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="26597-258">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="26597-259">Clientes</span><span class="sxs-lookup"><span data-stu-id="26597-259">Clients</span></span></p></td>
<td><p><span data-ttu-id="26597-260">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-260">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-261">Tráfego SIP de cliente para servidor para acesso de usuário externo</span><span class="sxs-lookup"><span data-stu-id="26597-261">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-262">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="26597-262">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="26597-263">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="26597-263">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-264">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="26597-264">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="26597-265">Usado para sessões de A/V com o Windows Live Messenger se a conectividade de mensagem de chat pública estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="26597-265">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26597-266">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="26597-266">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="26597-267">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="26597-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-268">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="26597-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="26597-269">Necessário para conectividade de IM pública com o Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="26597-269">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-270">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="26597-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="26597-271">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="26597-271">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="26597-272">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="26597-272">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="26597-273">Necessário para conectividade de IM pública com o Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="26597-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="26597-274">Resumo de firewall para mensagens extensíveis e protocolo de presença</span><span class="sxs-lookup"><span data-stu-id="26597-274">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26597-275">Protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="26597-275">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="26597-276">Fonte (endereço IP)</span><span class="sxs-lookup"><span data-stu-id="26597-276">Source (IP address)</span></span></th>
<th><span data-ttu-id="26597-277">Destino (endereço IP)</span><span class="sxs-lookup"><span data-stu-id="26597-277">Destination (IP address)</span></span></th>
<th><span data-ttu-id="26597-278">Comentários</span><span class="sxs-lookup"><span data-stu-id="26597-278">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26597-279">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="26597-279">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="26597-280">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-280">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-281">Endereço IP da interface do serviço de borda do acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-281">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="26597-282">Porta de comunicação de servidor para servidor padrão para XMPP.</span><span class="sxs-lookup"><span data-stu-id="26597-282">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="26597-283">Permite a comunicação com o servidor de borda XMPP o proxy de parceiros de XMPP federado</span><span class="sxs-lookup"><span data-stu-id="26597-283">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26597-284">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="26597-284">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="26597-285">Endereço IP da interface do serviço de borda do acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="26597-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="26597-286">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-286">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-287">Porta de comunicação de servidor para servidor padrão para XMPP.</span><span class="sxs-lookup"><span data-stu-id="26597-287">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="26597-288">Permite a comunicação do proxy do servidor de borda XMPP com parceiros do XMPP federado</span><span class="sxs-lookup"><span data-stu-id="26597-288">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26597-289">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="26597-289">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="26597-290">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="26597-290">Any</span></span></p></td>
<td><p><span data-ttu-id="26597-291">Cada IP de interface do servidor de borda interna</span><span class="sxs-lookup"><span data-stu-id="26597-291">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="26597-292">Tráfego de XMPP interno do Gateway XMPP no servidor front-end ou do pool de front-end para o endereço IP interno do servidor de borda ou o endereço IP interno de cada membro do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="26597-292">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="26597-293">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="26597-293">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

