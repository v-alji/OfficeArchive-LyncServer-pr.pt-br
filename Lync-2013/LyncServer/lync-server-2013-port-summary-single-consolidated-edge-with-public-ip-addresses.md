---
title: Sumário de porta - única borda consolidada com endereços IP públicos
description: Resumo da porta – borda única consolidada com endereços IP públicos.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single consolidated edge with public IP addresses
ms:assetid: 28407acc-8b92-4f78-875c-fd6b4323b602
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204756(v=OCS.15)
ms:contentKeyID: 48183685
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82ab2d89404fb174994d8e5b798f64bb68768326
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424252"
---
# <a name="port-summary---single-consolidated-edge-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="9faaf-103">Sumário de porta - única borda consolidada com endereços IP públicos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9faaf-103">Port summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9faaf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9faaf-104">

<span> </span></span></span>

<span data-ttu-id="9faaf-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="9faaf-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="9faaf-106">A funcionalidade do servidor de borda do Lync Server 2013 descrita nesta arquitetura de cenário é muito semelhante à implementada no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="9faaf-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="9faaf-107">A adição mais perceptível é a porta **5269 sobre** a entrada TCP para o protocolo de mensagens extensíveis e de presença (XMPP).</span><span class="sxs-lookup"><span data-stu-id="9faaf-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="9faaf-108">O Lync Server 2013, opcionalmente, implanta um proxy XMPP no servidor de borda ou no pool de periféricos e o servidor de Gateway XMPP no servidor front-end ou no pool de front-end.</span><span class="sxs-lookup"><span data-stu-id="9faaf-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span> <span data-ttu-id="9faaf-109">As informações de planejamento para o proxy reverso e a Federação são encontradas em [cenários para inverter proxy no Lync server 2013](lync-server-2013-scenarios-for-reverse-proxy.md) e [planejamento para SIP, Federação do XMPP e mensagens instantâneas públicas nas seções do Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9faaf-109">Planning information for the reverse proxy and federation are found in [Scenarios for reverse proxy in Lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md) and [Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md) sections, respectively.</span></span>

<span data-ttu-id="9faaf-110">Além do IPv4, o servidor de borda agora oferece suporte ao IPv6.</span><span class="sxs-lookup"><span data-stu-id="9faaf-110">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="9faaf-111">Para fins de clareza, somente o IPv4 é usado nos cenários.</span><span class="sxs-lookup"><span data-stu-id="9faaf-111">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="9faaf-112">**Rede de perímetro da empresa para uma única aresta consolidada com endereçamento de IP público**</span><span class="sxs-lookup"><span data-stu-id="9faaf-112">**Enterprise perimeter network for single consolidated edge with public IP addressing**</span></span>

<span data-ttu-id="9faaf-113">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span><span class="sxs-lookup"><span data-stu-id="9faaf-113">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="9faaf-114">Detalhes de protocolo e porta</span><span class="sxs-lookup"><span data-stu-id="9faaf-114">Port and Protocol Details</span></span>

<span data-ttu-id="9faaf-115">Recomendamos que você abra apenas as portas necessárias para dar suporte à funcionalidade para a qual você está fornecendo acesso externo.</span><span class="sxs-lookup"><span data-stu-id="9faaf-115">We recommend that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="9faaf-116">Para que o acesso remoto funcione para qualquer serviço de borda, é obrigatório que o tráfego SIP tenha permissão de fluxo bidirecionalmente, como mostrado na figura de tráfego de borda de entrada/saída.</span><span class="sxs-lookup"><span data-stu-id="9faaf-116">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bidirectionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="9faaf-117">Declarado de outra maneira, o recurso de mensagens SIP para e do serviço de borda de acesso está envolvido em mensagens instantâneas (IM), presença, Web conferência, áudio/vídeo (A/V) e Federação.</span><span class="sxs-lookup"><span data-stu-id="9faaf-117">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-single-consolidated-edge-with-public-ip-addresses-external-interface"></a><span data-ttu-id="9faaf-118">Resumo de firewall para uma única aresta consolidada com endereços IP públicos: interface externa</span><span class="sxs-lookup"><span data-stu-id="9faaf-118">Firewall Summary for Single Consolidated Edge with Public IP Addresses: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9faaf-119">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="9faaf-119">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="9faaf-120">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="9faaf-120">Source IP address</span></span></th>
<th><span data-ttu-id="9faaf-121">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="9faaf-121">Destination IP address</span></span></th>
<th><span data-ttu-id="9faaf-122">Notas</span><span class="sxs-lookup"><span data-stu-id="9faaf-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-123">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="9faaf-123">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="9faaf-124">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-124">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-125">Serviço de proxy XMPP (compartilha o endereço IP com o serviço de borda de acesso)</span><span class="sxs-lookup"><span data-stu-id="9faaf-125">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="9faaf-126">O serviço de proxy XMPP aceita o tráfego de contatos do XMPP em agrupamentos XMPP definidos</span><span class="sxs-lookup"><span data-stu-id="9faaf-126">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-127">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="9faaf-127">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="9faaf-128">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-128">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-129">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-129">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-130">Revogação e verificação de revogação/revogação de certificados e recuperação</span><span class="sxs-lookup"><span data-stu-id="9faaf-130">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-131">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="9faaf-131">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="9faaf-132">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-132">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-133">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-133">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-134">Consulta DNS via TCP</span><span class="sxs-lookup"><span data-stu-id="9faaf-134">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-135">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="9faaf-135">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="9faaf-136">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-136">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-137">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-137">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-138">Consulta DNS via UDP</span><span class="sxs-lookup"><span data-stu-id="9faaf-138">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-139">/TCP/443 de acesso/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="9faaf-139">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9faaf-140">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-140">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-141">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-141">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-142">Tráfego SIP de cliente para servidor para acesso de usuário externo</span><span class="sxs-lookup"><span data-stu-id="9faaf-142">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-143">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="9faaf-143">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="9faaf-144">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-144">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-145">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-145">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-146">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="9faaf-146">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-147">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="9faaf-147">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="9faaf-148">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-148">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-149">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-149">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-150">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="9faaf-150">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-151">Web Conferencing/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9faaf-151">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9faaf-152">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-152">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-153">Endereço IP público do serviço de borda de Webconferência do Edge Server Web</span><span class="sxs-lookup"><span data-stu-id="9faaf-153">Edge Server Web Conferencing Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-154">Mídia de Webconferência</span><span class="sxs-lookup"><span data-stu-id="9faaf-154">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-155">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="9faaf-155">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="9faaf-156">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-156">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-157">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-157">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-158">Obrigatório para federação com parceiros que executam o Office Communications Server 2007, o Office Communications Server 2007 R2, o Lync Server 2010 e o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9faaf-158">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-159">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="9faaf-159">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="9faaf-160">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="9faaf-160">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-161">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-161">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-162">Obrigatório somente para federação com parceiros que executam o Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="9faaf-162">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-163">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="9faaf-163">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="9faaf-164">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-164">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-165">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="9faaf-165">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-166">Obrigatório somente para federação com parceiros que executam o Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="9faaf-166">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-167">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="9faaf-167">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="9faaf-168">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-168">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-169">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="9faaf-169">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-170">Obrigatório somente para federação com parceiros que executam o Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="9faaf-170">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-171">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9faaf-171">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="9faaf-172">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="9faaf-172">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-173">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-173">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-174">3478 a saída é usada para determinar a versão do servidor de borda com a qual o Lync Server está se comunicando e também para o tráfego de mídia do servidor edge edge-to-edge.</span><span class="sxs-lookup"><span data-stu-id="9faaf-174">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="9faaf-175">Obrigatório para federação com o Lync Server 2010, o Windows Live Messenger e o Office Communications Server 2007 R2 e também se vários pools de bordas forem implantados em uma empresa.</span><span class="sxs-lookup"><span data-stu-id="9faaf-175">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-176">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9faaf-176">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="9faaf-177">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-177">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-178">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="9faaf-178">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-179">STUN/desliga a negociação de candidatos via UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9faaf-179">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-180">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9faaf-180">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9faaf-181">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-181">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-182">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="9faaf-182">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-183">STUN/TRANSFORMe a negociação de candidatos via TCP/443</span><span class="sxs-lookup"><span data-stu-id="9faaf-183">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-184">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9faaf-184">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9faaf-185">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="9faaf-185">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-186">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-186">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-187">STUN/TRANSFORMe a negociação de candidatos via TCP/443</span><span class="sxs-lookup"><span data-stu-id="9faaf-187">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-single-consolidated-edge-with-public-ip-addresses-internal-interface"></a><span data-ttu-id="9faaf-188">Resumo de firewall para uma única aresta consolidada com endereços IP públicos: interface interna</span><span class="sxs-lookup"><span data-stu-id="9faaf-188">Firewall Summary for Single Consolidated Edge with Public IP Addresses: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9faaf-189">Protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="9faaf-189">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="9faaf-190">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="9faaf-190">Source IP address</span></span></th>
<th><span data-ttu-id="9faaf-191">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="9faaf-191">Destination IP address</span></span></th>
<th><span data-ttu-id="9faaf-192">Comentários</span><span class="sxs-lookup"><span data-stu-id="9faaf-192">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-193">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="9faaf-193">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="9faaf-194">Any (pode ser definido como padrão de servidor Standard Edition, endereço IP do servidor Standard Edition ou endereço IP do pool executando o serviço de gateway do XMPP)</span><span class="sxs-lookup"><span data-stu-id="9faaf-194">Any (can be defined as Standard Edition server IP, Standard Edition server IP address, or pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="9faaf-195">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-195">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9faaf-196">Tráfego de XMPP de saída do serviço de gateway do XMPP em execução em servidor front-end ou pool de front-end</span><span class="sxs-lookup"><span data-stu-id="9faaf-196">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-197">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="9faaf-197">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="9faaf-198">Any (pode ser definido como director, endereço IP do pool do diretor, servidor front-end ou endereço IP do pool de front-end)</span><span class="sxs-lookup"><span data-stu-id="9faaf-198">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="9faaf-199">IP do servidor de borda ou pool que mantém a interface interna</span><span class="sxs-lookup"><span data-stu-id="9faaf-199">Edge Server IP, or pool that holds the internal interface</span></span></p></td>
<td><p><span data-ttu-id="9faaf-200">Tráfego SIP de saída (do director, endereço IP do pool do diretor, servidor front-end ou endereço IP do pool de front-end) para a interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-200">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-201">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="9faaf-201">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="9faaf-202">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9faaf-203">Any (pode ser definido como director, endereço IP do pool do diretor, servidor front-end ou endereço do pool de front-end)</span><span class="sxs-lookup"><span data-stu-id="9faaf-203">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool address)</span></span></p></td>
<td><p><span data-ttu-id="9faaf-204">Tráfego SIP de entrada (para o director, endereço IP do pool do diretor, servidor front-end ou endereço IP do pool de front-end) da interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-204">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-205">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="9faaf-205">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="9faaf-206">Any (pode ser definido como o endereço IP do servidor front-end ou cada endereço IP do servidor front-end em um pool Front-end)</span><span class="sxs-lookup"><span data-stu-id="9faaf-206">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="9faaf-207">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-207">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9faaf-208">Tráfego de Webconferência do servidor front-end ou de cada servidor front-end se estiver em um pool, para a interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-208">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-209">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="9faaf-209">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="9faaf-210">Any (pode ser definido como endereço IP do servidor front-end ou endereço IP do pool de front-end ou qualquer aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes que use este servidor de borda)</span><span class="sxs-lookup"><span data-stu-id="9faaf-210">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="9faaf-211">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-211">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9faaf-212">Autenticação de usuários de A/V (serviço de autenticação A/V) do servidor front-end ou do endereço IP do pool de front-end ou qualquer aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes que use este servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-212">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-213">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9faaf-213">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="9faaf-214">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-214">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-215">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-215">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9faaf-216">Caminho preferencial para transferência de mídia A/V entre usuários internos e externos, aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes</span><span class="sxs-lookup"><span data-stu-id="9faaf-216">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-217">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9faaf-217">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9faaf-218">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-218">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-219">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-219">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9faaf-220">Caminho de fallback para transferência de mídia A/V entre usuários internos e externos, aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes se não for possível estabelecer comunicação UDP, o TCP será usado para transferência de arquivos e compartilhamento de área de trabalho</span><span class="sxs-lookup"><span data-stu-id="9faaf-220">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-221">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="9faaf-221">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="9faaf-222">Any (pode ser definido como o endereço IP do servidor front-end ou o pool que mantém o repositório de gerenciamento central)</span><span class="sxs-lookup"><span data-stu-id="9faaf-222">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="9faaf-223">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-223">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9faaf-224">Replicação de alterações do repositório de gerenciamento central para o servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-224">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-225">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="9faaf-225">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="9faaf-226">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-226">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-227">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-227">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9faaf-228">Controlador de serviço de log centralizado usando cmdlets do Shell de gerenciamento do Lync Server e do serviço de log centralizado, comandos de linha de comando do ClsController (ClsController.exe) ou de agente (ClsAgent.exe) e coleção de logs</span><span class="sxs-lookup"><span data-stu-id="9faaf-228">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-229">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="9faaf-229">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="9faaf-230">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-230">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-231">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-231">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9faaf-232">Controlador de serviço de log centralizado usando cmdlets do Shell de gerenciamento do Lync Server e do serviço de log centralizado, comandos de linha de comando do ClsController (ClsController.exe) ou de agente (ClsAgent.exe) e coleção de logs</span><span class="sxs-lookup"><span data-stu-id="9faaf-232">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-233">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="9faaf-233">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="9faaf-234">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-234">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-235">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-235">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9faaf-236">Controlador de serviço de log centralizado usando cmdlets do Shell de gerenciamento do Lync Server e do serviço de log centralizado, comandos de linha de comando do ClsController (ClsController.exe) ou de agente (ClsAgent.exe) e coleção de logs</span><span class="sxs-lookup"><span data-stu-id="9faaf-236">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="9faaf-237">Resumo do firewall para Federação</span><span class="sxs-lookup"><span data-stu-id="9faaf-237">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9faaf-238">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="9faaf-238">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="9faaf-239">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="9faaf-239">Source IP address</span></span></th>
<th><span data-ttu-id="9faaf-240">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="9faaf-240">Destination IP address</span></span></th>
<th><span data-ttu-id="9faaf-241">Notas</span><span class="sxs-lookup"><span data-stu-id="9faaf-241">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-242">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="9faaf-242">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="9faaf-243">Endereço IP público do serviço de borda do Access</span><span class="sxs-lookup"><span data-stu-id="9faaf-243">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-244">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-244">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-245">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="9faaf-245">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="9faaf-246">Resumo do Firewall – Conectividade de mensagens instantâneas públicas</span><span class="sxs-lookup"><span data-stu-id="9faaf-246">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9faaf-247">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="9faaf-247">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="9faaf-248">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="9faaf-248">Source IP address</span></span></th>
<th><span data-ttu-id="9faaf-249">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="9faaf-249">Destination IP address</span></span></th>
<th><span data-ttu-id="9faaf-250">Notas</span><span class="sxs-lookup"><span data-stu-id="9faaf-250">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-251">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="9faaf-251">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="9faaf-252">Parceiros de conectividade de mensagens de chat públicas</span><span class="sxs-lookup"><span data-stu-id="9faaf-252">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="9faaf-253">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-253">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="9faaf-254">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="9faaf-254">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-255">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="9faaf-255">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="9faaf-256">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-256">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="9faaf-257">Parceiros de conectividade de mensagens de chat públicas</span><span class="sxs-lookup"><span data-stu-id="9faaf-257">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="9faaf-258">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="9faaf-258">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-259">/TCP/443 de acesso/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="9faaf-259">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9faaf-260">Clientes</span><span class="sxs-lookup"><span data-stu-id="9faaf-260">Clients</span></span></p></td>
<td><p><span data-ttu-id="9faaf-261">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-261">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="9faaf-262">Tráfego SIP de cliente para servidor para acesso de usuário externo</span><span class="sxs-lookup"><span data-stu-id="9faaf-262">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-263">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="9faaf-263">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="9faaf-264">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="9faaf-264">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="9faaf-265">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="9faaf-265">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="9faaf-266">Usado para sessões de A/V com o Windows Live Messenger se a conectividade de mensagem de chat pública estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="9faaf-266">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-267">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9faaf-267">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="9faaf-268">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="9faaf-268">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="9faaf-269">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="9faaf-269">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="9faaf-270">Necessário para conectividade de IM pública com o Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="9faaf-270">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-271">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9faaf-271">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="9faaf-272">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="9faaf-272">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="9faaf-273">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="9faaf-273">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="9faaf-274">Necessário para conectividade de IM pública com o Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="9faaf-274">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="9faaf-275">Resumo de firewall para mensagens extensíveis e protocolo de presença</span><span class="sxs-lookup"><span data-stu-id="9faaf-275">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9faaf-276">Protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="9faaf-276">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="9faaf-277">Fonte (endereço IP)</span><span class="sxs-lookup"><span data-stu-id="9faaf-277">Source (IP address)</span></span></th>
<th><span data-ttu-id="9faaf-278">Destino (endereço IP)</span><span class="sxs-lookup"><span data-stu-id="9faaf-278">Destination (IP address)</span></span></th>
<th><span data-ttu-id="9faaf-279">Comentários</span><span class="sxs-lookup"><span data-stu-id="9faaf-279">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-280">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="9faaf-280">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="9faaf-281">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-281">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-282">Endereço IP da interface do serviço de borda do acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-282">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-283">Porta de comunicação de servidor para servidor padrão para XMPP.</span><span class="sxs-lookup"><span data-stu-id="9faaf-283">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="9faaf-284">Permite a comunicação com o servidor de borda XMPP o proxy de parceiros de XMPP federado</span><span class="sxs-lookup"><span data-stu-id="9faaf-284">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9faaf-285">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="9faaf-285">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="9faaf-286">Endereço IP da interface do serviço de borda do acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="9faaf-286">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="9faaf-287">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-287">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-288">Porta de comunicação de servidor para servidor padrão para XMPP.</span><span class="sxs-lookup"><span data-stu-id="9faaf-288">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="9faaf-289">Permite a comunicação do proxy do servidor de borda XMPP com parceiros do XMPP federado</span><span class="sxs-lookup"><span data-stu-id="9faaf-289">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9faaf-290">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="9faaf-290">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="9faaf-291">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="9faaf-291">Any</span></span></p></td>
<td><p><span data-ttu-id="9faaf-292">Cada IP de interface do servidor de borda interna</span><span class="sxs-lookup"><span data-stu-id="9faaf-292">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="9faaf-293">Tráfego de XMPP interno do Gateway XMPP no servidor front-end ou do pool de front-end para o endereço IP interno do servidor de borda ou o endereço IP interno de cada membro do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="9faaf-293">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9faaf-294">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9faaf-294">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

