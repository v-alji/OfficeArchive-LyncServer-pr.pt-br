---
title: 'Lync Server 2013: Resumo de porta - Borda consolidada em escala, balanceamento de carga de DNS com endereços IP públicos'
description: 'Lync Server 2013: Resumo da porta – borda consolidada dimensionada, balanceamento de carga de DNS com endereços IP públicos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses
ms:assetid: f7cbd0f1-841d-4116-8d17-e9d991daa4a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205394(v=OCS.15)
ms:contentKeyID: 48185865
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8090435485b4b6a183702a608b139cec91ae26a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446336"
---
# <a name="port-summary---scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="7aa5e-103">Resumo de porta - Borda consolidada em escala, balanceamento de carga de DNS com endereços IP públicos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7aa5e-103">Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7aa5e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7aa5e-104">

<span> </span></span></span>

<span data-ttu-id="7aa5e-105">_**Tópico da última modificação:** 2013-04-03_</span><span class="sxs-lookup"><span data-stu-id="7aa5e-105">_**Topic Last Modified:** 2013-04-03_</span></span>

<span data-ttu-id="7aa5e-106">A funcionalidade do servidor de borda do Lync Server 2013 descrita nesta arquitetura de cenário é muito semelhante à implementada no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="7aa5e-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="7aa5e-107">A adição mais perceptível é a porta **5269 sobre** a entrada TCP para o protocolo de mensagens extensíveis e de presença (XMPP).</span><span class="sxs-lookup"><span data-stu-id="7aa5e-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="7aa5e-108">O Lync Server 2013, opcionalmente, implanta um proxy XMPP no servidor de borda ou no pool de periféricos e o servidor de Gateway XMPP no servidor front-end ou no pool de front-end.</span><span class="sxs-lookup"><span data-stu-id="7aa5e-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="7aa5e-109">Além do IPv4, o servidor de borda agora oferece suporte ao IPv6.</span><span class="sxs-lookup"><span data-stu-id="7aa5e-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="7aa5e-110">Para fins de clareza, somente o IPv4 é usado nos cenários.</span><span class="sxs-lookup"><span data-stu-id="7aa5e-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="7aa5e-111">**Rede de perímetro da empresa para borda consolidada dimensionada, balanceamento de carga de DNS com endereços IP públicos**</span><span class="sxs-lookup"><span data-stu-id="7aa5e-111">**Enterprise perimeter network for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses**</span></span>

<span data-ttu-id="7aa5e-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span><span class="sxs-lookup"><span data-stu-id="7aa5e-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="7aa5e-113">Detalhes de protocolo e porta</span><span class="sxs-lookup"><span data-stu-id="7aa5e-113">Port and Protocol Details</span></span>

<span data-ttu-id="7aa5e-114">É recomendável que você abra apenas as portas necessárias para dar suporte à funcionalidade para a qual você está fornecendo acesso externo.</span><span class="sxs-lookup"><span data-stu-id="7aa5e-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="7aa5e-115">Para que o acesso remoto funcione para qualquer serviço de borda, é obrigatório que o tráfego SIP tenha permissão de fluxo bidirecional, conforme mostrado na figura de tráfego de borda de entrada/saída.</span><span class="sxs-lookup"><span data-stu-id="7aa5e-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="7aa5e-116">Declarado de outra maneira, o recurso de mensagens SIP para e do serviço de borda de acesso está envolvido em mensagens instantâneas (IM), presença, Web conferência, áudio/vídeo (A/V) e Federação.</span><span class="sxs-lookup"><span data-stu-id="7aa5e-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="7aa5e-117">Resumo de firewall para borda consolidada dimensionada, balanceamento de carga de DNS com endereços IP públicos: interface externa – nó 1 e nó 2 (exemplo)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-117">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7aa5e-118">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="7aa5e-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="7aa5e-119">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="7aa5e-119">Source IP address</span></span></th>
<th><span data-ttu-id="7aa5e-120">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="7aa5e-120">Destination IP address</span></span></th>
<th><span data-ttu-id="7aa5e-121">Notas</span><span class="sxs-lookup"><span data-stu-id="7aa5e-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="7aa5e-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-123">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-123">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-124">Serviço de proxy XMPP (compartilha o endereço IP com o serviço de borda de acesso)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-125">O serviço de proxy XMPP aceita o tráfego de contatos do XMPP em agrupamentos XMPP definidos</span><span class="sxs-lookup"><span data-stu-id="7aa5e-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-126">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="7aa5e-126">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-127">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-127">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-128">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-128">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-129">Revogação e verificação de revogação/revogação de certificados e recuperação</span><span class="sxs-lookup"><span data-stu-id="7aa5e-129">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-130">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="7aa5e-130">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-131">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-131">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-132">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-132">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-133">Consulta DNS via TCP</span><span class="sxs-lookup"><span data-stu-id="7aa5e-133">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-134">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="7aa5e-134">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-135">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-135">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-136">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-136">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-137">Consulta DNS via UDP</span><span class="sxs-lookup"><span data-stu-id="7aa5e-137">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-138">/TCP/443 de acesso/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-138">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-139">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-139">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-140">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-140">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-141">Tráfego SIP de cliente para servidor para acesso de usuário externo</span><span class="sxs-lookup"><span data-stu-id="7aa5e-141">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-142">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-142">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-143">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-143">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-144">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-144">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-145">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="7aa5e-145">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-146">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-147">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-147">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-148">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-148">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-149">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="7aa5e-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-150">Web Conferencing/PSOM (TLS) TCP/443</span><span class="sxs-lookup"><span data-stu-id="7aa5e-150">Web Conferencing/PSOM(TLS)TCP/443</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-151">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-151">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-152">Endereço IP público do serviço de borda de Webconferência do Edge Server Web</span><span class="sxs-lookup"><span data-stu-id="7aa5e-152">Edge Server Web Conferencing Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-153">Mídia de Webconferência</span><span class="sxs-lookup"><span data-stu-id="7aa5e-153">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-154">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="7aa5e-154">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-155">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="7aa5e-155">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-156">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-156">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-157">Obrigatório para federação com parceiros que executam o Office Communications Server 2007, o Office Communications Server 2007 R2, o Lync Server 2010 e o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7aa5e-157">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-158">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="7aa5e-158">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-159">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="7aa5e-159">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-160">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-160">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-161">Obrigatório somente para federação com parceiros que executam o Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="7aa5e-161">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-162">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="7aa5e-162">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-163">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-163">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-164">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="7aa5e-164">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-165">Obrigatório somente para federação com parceiros que executam o Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="7aa5e-165">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-166">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="7aa5e-166">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-167">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-167">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-168">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="7aa5e-168">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-169">Obrigatório somente para federação com parceiros que executam o Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="7aa5e-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-170">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="7aa5e-170">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-171">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="7aa5e-171">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-172">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-172">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-173">3478 a saída é usada para determinar a versão do servidor de borda com a qual o Lync Server está se comunicando e também para o tráfego de mídia do servidor edge edge-to-edge.</span><span class="sxs-lookup"><span data-stu-id="7aa5e-173">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="7aa5e-174">Obrigatório para federação com o Lync Server 2010, o Windows Live Messenger e o Office Communications Server 2007 R2 e também se vários pools de bordas forem implantados em uma empresa.</span><span class="sxs-lookup"><span data-stu-id="7aa5e-174">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-175">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="7aa5e-175">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-176">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-176">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-177">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="7aa5e-177">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-178">STUN/desliga a negociação de candidatos via UDP/3478</span><span class="sxs-lookup"><span data-stu-id="7aa5e-178">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-179">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="7aa5e-179">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-180">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-180">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-181">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="7aa5e-181">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-182">STUN/TRANSFORMe a negociação de candidatos via TCP/443</span><span class="sxs-lookup"><span data-stu-id="7aa5e-182">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-183">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="7aa5e-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-184">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="7aa5e-184">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-185">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-185">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-186">STUN/TRANSFORMe a negociação de candidatos via TCP/443</span><span class="sxs-lookup"><span data-stu-id="7aa5e-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-internal-interface--node-1-and-node-2-example"></a><span data-ttu-id="7aa5e-187">Resumo de firewall para borda consolidada dimensionada, balanceamento de carga de DNS com endereços IP públicos: interface interna – nó 1 e nó 2 (exemplo)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-187">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses: Internal Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7aa5e-188">Protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="7aa5e-188">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="7aa5e-189">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="7aa5e-189">Source IP address</span></span></th>
<th><span data-ttu-id="7aa5e-190">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="7aa5e-190">Destination IP address</span></span></th>
<th><span data-ttu-id="7aa5e-191">Comentários</span><span class="sxs-lookup"><span data-stu-id="7aa5e-191">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-192">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="7aa5e-192">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-193">Any (pode ser definido como endereço do servidor front-end ou endereço IP do pool de front-end executando o serviço de gateway do XMPP)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-193">Any (can be defined as Front End Server address, or Front End pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-194">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-195">Tráfego de XMPP de saída do serviço de gateway do XMPP em execução em servidor front-end ou pool de front-end</span><span class="sxs-lookup"><span data-stu-id="7aa5e-195">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-196">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="7aa5e-196">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-197">Any (pode ser definido como director, endereço IP do pool do diretor, servidor front-end ou endereço IP do pool de front-end)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-197">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-198">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-199">Tráfego SIP de saída (do director, endereço IP do pool do diretor, servidor front-end ou endereço IP do pool de front-end) para a interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-199">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="7aa5e-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-201">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-201">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-202">Any (pode ser definido como director, endereço IP do pool do diretor, servidor front-end ou endereço IP do pool de front-end)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-202">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-203">Tráfego SIP de entrada (para o director, endereço IP do pool do diretor, servidor front-end ou endereço IP do pool de front-end) da interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-203">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-204">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="7aa5e-204">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-205">Any (pode ser definido como o endereço IP do servidor front-end ou cada endereço IP do servidor front-end em um pool Front-end)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-205">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-206">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-206">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-207">Tráfego de Webconferência do servidor front-end ou de cada servidor front-end se estiver em um pool, para a interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-207">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-208">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="7aa5e-208">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-209">Any (pode ser definido como endereço IP do servidor front-end ou endereço IP do pool de front-end ou qualquer aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes que use este servidor de borda)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-209">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-210">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-211">Autenticação de usuários de A/V (serviço de autenticação A/V) do servidor front-end ou do endereço IP do pool de front-end ou qualquer aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes que use este servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-211">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-212">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="7aa5e-212">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-213">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-213">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-214">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-215">Caminho preferencial para transferência de mídia A/V entre usuários internos e externos, aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes</span><span class="sxs-lookup"><span data-stu-id="7aa5e-215">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-216">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="7aa5e-216">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-217">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-217">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-218">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-219">Caminho de fallback para transferência de mídia A/V entre usuários internos e externos, aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes se não for possível estabelecer comunicação UDP, o TCP será usado para transferência de arquivos e compartilhamento de área de trabalho</span><span class="sxs-lookup"><span data-stu-id="7aa5e-219">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-220">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="7aa5e-220">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-221">Any (pode ser definido como o endereço IP do servidor front-end ou o pool que mantém o repositório de gerenciamento central)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-221">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-222">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-223">Replicação de alterações do repositório de gerenciamento central para o servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-223">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-224">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="7aa5e-224">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-225">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-225">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-226">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-227">Controlador de serviço de log centralizado usando cmdlets do Shell de gerenciamento do Lync Server e do serviço de log centralizado, comandos de linha de comando do ClsController (ClsController.exe) ou de agente (ClsAgent.exe) e coleção de logs</span><span class="sxs-lookup"><span data-stu-id="7aa5e-227">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-228">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="7aa5e-228">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-229">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-229">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-230">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-231">Controlador de serviço de log centralizado usando cmdlets do Shell de gerenciamento do Lync Server e do serviço de log centralizado, comandos de linha de comando do ClsController (ClsController.exe) ou de agente (ClsAgent.exe) e coleção de logs</span><span class="sxs-lookup"><span data-stu-id="7aa5e-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-232">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="7aa5e-232">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-233">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-233">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-234">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-235">Controlador de serviço de log centralizado usando cmdlets do Shell de gerenciamento do Lync Server e do serviço de log centralizado, comandos de linha de comando do ClsController (ClsController.exe) ou de agente (ClsAgent.exe) e coleção de logs</span><span class="sxs-lookup"><span data-stu-id="7aa5e-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="7aa5e-236">Resumo do firewall para Federação</span><span class="sxs-lookup"><span data-stu-id="7aa5e-236">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7aa5e-237">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="7aa5e-237">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="7aa5e-238">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="7aa5e-238">Source IP address</span></span></th>
<th><span data-ttu-id="7aa5e-239">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="7aa5e-239">Destination IP address</span></span></th>
<th><span data-ttu-id="7aa5e-240">Notas</span><span class="sxs-lookup"><span data-stu-id="7aa5e-240">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-241">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-241">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-242">Endereço IP público do serviço de borda do Access</span><span class="sxs-lookup"><span data-stu-id="7aa5e-242">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-243">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-243">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-244">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="7aa5e-244">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="7aa5e-245">Resumo do Firewall – Conectividade de mensagens instantâneas públicas</span><span class="sxs-lookup"><span data-stu-id="7aa5e-245">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7aa5e-246">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="7aa5e-246">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="7aa5e-247">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="7aa5e-247">Source IP address</span></span></th>
<th><span data-ttu-id="7aa5e-248">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="7aa5e-248">Destination IP address</span></span></th>
<th><span data-ttu-id="7aa5e-249">Notas</span><span class="sxs-lookup"><span data-stu-id="7aa5e-249">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-250">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-250">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-251">Parceiros de conectividade de mensagens de chat públicas</span><span class="sxs-lookup"><span data-stu-id="7aa5e-251">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-252">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-252">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-253">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="7aa5e-253">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-254">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-255">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-255">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-256">Parceiros de conectividade de mensagens de chat públicas</span><span class="sxs-lookup"><span data-stu-id="7aa5e-256">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-257">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="7aa5e-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-258">/TCP/443 de acesso/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-258">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-259">Clientes</span><span class="sxs-lookup"><span data-stu-id="7aa5e-259">Clients</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-260">Serviço de borda de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-260">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-261">Tráfego SIP de cliente para servidor para acesso de usuário externo</span><span class="sxs-lookup"><span data-stu-id="7aa5e-261">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-262">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="7aa5e-262">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-263">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="7aa5e-263">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-264">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="7aa5e-264">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-265">Usado para sessões de A/V com o Windows Live Messenger se a conectividade de mensagem de chat pública estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="7aa5e-265">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-266">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="7aa5e-266">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-267">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="7aa5e-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-268">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="7aa5e-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-269">Necessário para conectividade de IM pública com o Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="7aa5e-269">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-270">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="7aa5e-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-271">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="7aa5e-271">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-272">Serviço Edge Server A/V Edge</span><span class="sxs-lookup"><span data-stu-id="7aa5e-272">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-273">Necessário para conectividade de IM pública com o Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="7aa5e-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="7aa5e-274">Resumo de firewall para mensagens extensíveis e protocolo de presença</span><span class="sxs-lookup"><span data-stu-id="7aa5e-274">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7aa5e-275">Protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="7aa5e-275">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="7aa5e-276">Fonte (endereço IP)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-276">Source (IP address)</span></span></th>
<th><span data-ttu-id="7aa5e-277">Destino (endereço IP)</span><span class="sxs-lookup"><span data-stu-id="7aa5e-277">Destination (IP address)</span></span></th>
<th><span data-ttu-id="7aa5e-278">Comentários</span><span class="sxs-lookup"><span data-stu-id="7aa5e-278">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-279">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="7aa5e-279">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-280">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-280">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-281">Endereço IP da interface do serviço de borda do acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-281">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-282">Porta de comunicação de servidor para servidor padrão para XMPP.</span><span class="sxs-lookup"><span data-stu-id="7aa5e-282">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="7aa5e-283">Permite a comunicação com o servidor de borda XMPP o proxy de parceiros de XMPP federado</span><span class="sxs-lookup"><span data-stu-id="7aa5e-283">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa5e-284">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="7aa5e-284">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-285">Endereço IP da interface do serviço de borda do acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="7aa5e-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-286">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-286">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-287">Porta de comunicação de servidor para servidor padrão para XMPP.</span><span class="sxs-lookup"><span data-stu-id="7aa5e-287">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="7aa5e-288">Permite a comunicação do proxy do servidor de borda XMPP com parceiros do XMPP federado</span><span class="sxs-lookup"><span data-stu-id="7aa5e-288">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa5e-289">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="7aa5e-289">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-290">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="7aa5e-290">Any</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-291">Cada IP de interface do servidor de borda interna</span><span class="sxs-lookup"><span data-stu-id="7aa5e-291">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="7aa5e-292">Tráfego de XMPP interno do Gateway XMPP no servidor front-end ou do pool de front-end para o endereço IP interno do servidor de borda ou o endereço IP interno de cada membro do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="7aa5e-292">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7aa5e-293">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7aa5e-293">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

