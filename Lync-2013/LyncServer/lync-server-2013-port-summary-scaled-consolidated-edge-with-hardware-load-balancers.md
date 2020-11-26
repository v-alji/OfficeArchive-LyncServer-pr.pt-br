---
title: Resumo de porta - borda consolidada em escala com balanceadores de carga de hardware
description: Resumo da porta – borda consolidada dimensionada com balanceadores de carga de hardware.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge with hardware load balancers
ms:assetid: 91213b1e-f875-464b-83e8-fe3a351595a4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398739(v=OCS.15)
ms:contentKeyID: 48184841
ms.date: 04/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1a03acb3644d83669bcf0065ebb20c526ef5fa32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424305"
---
# <a name="port-summary---scaled-consolidated-edge-with-hardware-load-balancers-in-lync-server-2013"></a><span data-ttu-id="72f2b-103">Resumo de porta - borda consolidada em escala com balanceadores de carga de hardware no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="72f2b-103">Port summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="72f2b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="72f2b-104">

<span> </span></span></span>

<span data-ttu-id="72f2b-105">_**Tópico da última modificação:** 2015-04-27_</span><span class="sxs-lookup"><span data-stu-id="72f2b-105">_**Topic Last Modified:** 2015-04-27_</span></span>

<span data-ttu-id="72f2b-106">A funcionalidade do servidor de borda do Lync Server 2013 descrita nesta arquitetura de cenário é muito semelhante à implementada no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="72f2b-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="72f2b-107">A adição mais perceptível é a porta **5269 sobre** a entrada TCP para o protocolo de mensagens extensíveis e de presença (XMPP).</span><span class="sxs-lookup"><span data-stu-id="72f2b-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="72f2b-108">O Lync Server 2013, opcionalmente, implanta um proxy XMPP no servidor de borda ou no pool de periféricos e o servidor de Gateway XMPP no servidor front-end ou no pool de front-end.</span><span class="sxs-lookup"><span data-stu-id="72f2b-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="72f2b-109">Além do IPv4, o servidor de borda agora oferece suporte ao IPv6.</span><span class="sxs-lookup"><span data-stu-id="72f2b-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="72f2b-110">Para fins de clareza, somente o IPv4 é usado nos cenários.</span><span class="sxs-lookup"><span data-stu-id="72f2b-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="72f2b-111">**Borda consolidada dimensionada usando o balanceamento de carga de hardware**</span><span class="sxs-lookup"><span data-stu-id="72f2b-111">**Scaled Consolidated Edge using Hardware Load Balancing**</span></span>

<span data-ttu-id="72f2b-112">![Portas e protocolos de rede do perímetro do servidor de borda](images/Gg398739.063f7dd1-16db-4cc7-8708-bca9bc41184d(OCS.15).jpg "Portas e protocolos de rede do perímetro do servidor de borda")</span><span class="sxs-lookup"><span data-stu-id="72f2b-112">![Edge Server Perimeter Network ports and protocols](images/Gg398739.063f7dd1-16db-4cc7-8708-bca9bc41184d(OCS.15).jpg "Edge Server Perimeter Network ports and protocols")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="72f2b-113">Detalhes de protocolo e porta</span><span class="sxs-lookup"><span data-stu-id="72f2b-113">Port and Protocol Details</span></span>

<span data-ttu-id="72f2b-114">É recomendável que você abra apenas as portas necessárias para dar suporte à funcionalidade para a qual você está fornecendo acesso externo.</span><span class="sxs-lookup"><span data-stu-id="72f2b-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="72f2b-115">Para que o acesso remoto funcione para qualquer serviço de borda, é obrigatório que o tráfego SIP tenha permissão de fluxo bidirecional, conforme mostrado na figura de tráfego de borda de entrada/saída.</span><span class="sxs-lookup"><span data-stu-id="72f2b-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="72f2b-116">Declarado de outra maneira, o recurso de mensagens SIP para e do serviço de borda de acesso está envolvido em mensagens instantâneas (IM), presença, Web conferência, áudio/vídeo (A/V) e Federação.</span><span class="sxs-lookup"><span data-stu-id="72f2b-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="72f2b-117">Resumo de firewall para borda consolidada dimensionada, carga de hardware balanceada: interface externa – nó 1 e nó 2 (exemplo)</span><span class="sxs-lookup"><span data-stu-id="72f2b-117">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72f2b-118">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="72f2b-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="72f2b-119">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="72f2b-119">Source IP address</span></span></th>
<th><span data-ttu-id="72f2b-120">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="72f2b-120">Destination IP address</span></span></th>
<th><span data-ttu-id="72f2b-121">Notas</span><span class="sxs-lookup"><span data-stu-id="72f2b-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-122">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="72f2b-122">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="72f2b-123">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-123">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-124">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-124">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-125">Revogação e verificação de revogação/revogação de certificados e recuperação</span><span class="sxs-lookup"><span data-stu-id="72f2b-125">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-126">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="72f2b-126">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="72f2b-127">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-127">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-128">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-128">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-129">Consulta DNS via TCP</span><span class="sxs-lookup"><span data-stu-id="72f2b-129">DNS query over TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-130">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="72f2b-130">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="72f2b-131">Endereço IP público do serviço de borda do acesso ao servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-131">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-132">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-132">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-133">Consulta DNS via UDP</span><span class="sxs-lookup"><span data-stu-id="72f2b-133">DNS query over UDP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-134">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="72f2b-134">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="72f2b-135">Endereço IP do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="72f2b-135">Edge Server A/V Edge service IP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-136">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-136">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-137">Obrigatório para federação com parceiros que executam o Office Communications Server 2007, o Office Communications Server 2007 R2, o Lync Server 2010 e o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="72f2b-137">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-138">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="72f2b-138">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="72f2b-139">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="72f2b-139">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-140">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-140">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-141">Obrigatório somente para federação com parceiros que executam o Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="72f2b-141">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-142">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="72f2b-142">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="72f2b-143">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-143">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-144">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="72f2b-144">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-145">Obrigatório somente para federação com parceiros que executam o Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="72f2b-145">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-146">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="72f2b-146">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="72f2b-147">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-147">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-148">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="72f2b-148">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-149">Obrigatório somente para federação com parceiros que executam o Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="72f2b-149">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-150">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="72f2b-150">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="72f2b-151">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="72f2b-151">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-152">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-152">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-153">3478 a saída é usada para determinar a versão do servidor de borda com a qual o Lync Server está se comunicando e também para o tráfego de mídia do servidor edge edge-to-edge.</span><span class="sxs-lookup"><span data-stu-id="72f2b-153">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="72f2b-154">Obrigatório para federação com o Lync Server 2010, o Windows Live Messenger e o Office Communications Server 2007 R2 e também se vários pools de bordas forem implantados em uma empresa.</span><span class="sxs-lookup"><span data-stu-id="72f2b-154">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-155">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="72f2b-155">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="72f2b-156">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-156">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-157">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="72f2b-157">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-158">STUN/desliga a negociação de candidatos via UDP/3478</span><span class="sxs-lookup"><span data-stu-id="72f2b-158">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-159">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="72f2b-159">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="72f2b-160">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-160">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-161">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="72f2b-161">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-162">STUN/TRANSFORMe a negociação de candidatos via TCP/443</span><span class="sxs-lookup"><span data-stu-id="72f2b-162">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-163">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="72f2b-163">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="72f2b-164">Endereço IP público do serviço de borda do servidor de borda A/V</span><span class="sxs-lookup"><span data-stu-id="72f2b-164">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-165">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-165">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-166">STUN/TRANSFORMe a negociação de candidatos via TCP/443</span><span class="sxs-lookup"><span data-stu-id="72f2b-166">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-internal-interface-node-1-and-node-2"></a><span data-ttu-id="72f2b-167">Resumo de firewall para borda consolidada dimensionada, balanceamento de carga de hardware: nó de interface interna 1 e nó 2</span><span class="sxs-lookup"><span data-stu-id="72f2b-167">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: Internal Interface Node 1 and Node 2</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72f2b-168">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="72f2b-168">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="72f2b-169">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="72f2b-169">Source IP address</span></span></th>
<th><span data-ttu-id="72f2b-170">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="72f2b-170">Destination IP address</span></span></th>
<th><span data-ttu-id="72f2b-171">Notas</span><span class="sxs-lookup"><span data-stu-id="72f2b-171">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-172">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="72f2b-172">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="72f2b-173">Any (pode ser definido como endereço do servidor front-end ou endereço IP virtual do pool de front-end executando o serviço de gateway do XMPP)</span><span class="sxs-lookup"><span data-stu-id="72f2b-173">Any (can be defined as Front End Server address, or Front End pool virtual IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="72f2b-174">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-174">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="72f2b-175">Tráfego de XMPP de saída do serviço de gateway do XMPP em execução em servidor front-end ou pool de front-end</span><span class="sxs-lookup"><span data-stu-id="72f2b-175">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-176">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="72f2b-176">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="72f2b-177">Any (pode ser definido como o IP ou pool do servidor de front-end que mantém o repositório de gerenciamento central)</span><span class="sxs-lookup"><span data-stu-id="72f2b-177">Any (can be defined as the Front End Server server IP or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="72f2b-178">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-178">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="72f2b-179">Replicação de alterações do repositório de gerenciamento central para o servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-179">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-180">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="72f2b-180">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="72f2b-181">Any (pode ser definido como IP do diretor, IP do servidor front-end ou IP virtual do pool)</span><span class="sxs-lookup"><span data-stu-id="72f2b-181">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="72f2b-182">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-182">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="72f2b-183">Tráfego de Webconferência da implantação interna para a interface de servidor de borda interna</span><span class="sxs-lookup"><span data-stu-id="72f2b-183">Web conferencing traffic from Internal deployment to Internal Edge Server interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-184">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="72f2b-184">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="72f2b-185">Any (pode ser definido como IP do diretor, IP do servidor front-end ou IP virtual do pool)</span><span class="sxs-lookup"><span data-stu-id="72f2b-185">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="72f2b-186">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-186">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="72f2b-187">Caminho preferencial para transferência de mídia A/V entre usuários internos e externos, aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes</span><span class="sxs-lookup"><span data-stu-id="72f2b-187">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-188">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="72f2b-188">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="72f2b-189">Any (pode ser definido como IP do diretor, IP do servidor front-end ou IP virtual do pool)</span><span class="sxs-lookup"><span data-stu-id="72f2b-189">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="72f2b-190">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-190">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="72f2b-191">Caminho de fallback para transferência de mídia A/V entre usuários internos e externos, aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes se não for possível estabelecer comunicação UDP, o TCP será usado para transferência de arquivos e compartilhamento de área de trabalho</span><span class="sxs-lookup"><span data-stu-id="72f2b-191">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-192">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="72f2b-192">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="72f2b-193">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-193">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-194">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="72f2b-195">Controlador de serviço de log centralizado usando cmdlets do Shell de gerenciamento do Lync Server e do serviço de log centralizado, comandos de linha de comando do ClsController (ClsController.exe) ou de agente (ClsAgent.exe) e coleção de logs</span><span class="sxs-lookup"><span data-stu-id="72f2b-195">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-196">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="72f2b-196">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="72f2b-197">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-197">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-198">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="72f2b-199">Controlador de serviço de log centralizado usando cmdlets do Shell de gerenciamento do Lync Server e do serviço de log centralizado, comandos de linha de comando do ClsController (ClsController.exe) ou de agente (ClsAgent.exe) e coleção de logs</span><span class="sxs-lookup"><span data-stu-id="72f2b-199">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-200">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="72f2b-200">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="72f2b-201">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-201">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-202">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="72f2b-203">Controlador de serviço de log centralizado usando cmdlets do Shell de gerenciamento do Lync Server e do serviço de log centralizado, comandos de linha de comando do ClsController (ClsController.exe) ou de agente (ClsAgent.exe) e coleção de logs</span><span class="sxs-lookup"><span data-stu-id="72f2b-203">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="72f2b-204">Os balanceadores de carga de hardware têm requisitos específicos quando implantados para fornecer disponibilidade e balanceamento de carga do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="72f2b-204">Hardware load balancers have specific requirements when deployed to provide availability and load balancing for Lync Server.</span></span> <span data-ttu-id="72f2b-205">Os requisitos são definidos na figura e nas tabelas a seguir.</span><span class="sxs-lookup"><span data-stu-id="72f2b-205">The requirements are defined in the following figure and tables.</span></span> <span data-ttu-id="72f2b-206">Fornecedores de terceiros podem usar terminologia diferente para os requisitos definidos aqui.</span><span class="sxs-lookup"><span data-stu-id="72f2b-206">Third party vendors may use different terminology for the requirements defined here.</span></span> <span data-ttu-id="72f2b-207">Será necessário mapear os requisitos do Lync Server para os recursos e as opções de configuração fornecidas pelo fornecedor do balanceador de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="72f2b-207">It will be necessary to map the requirements of Lync Server to the features and configuration options provided by your hardware load balancer vendor.</span></span>

<span data-ttu-id="72f2b-208">Ao configurar balanceadores de carga de hardware, considere os seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="72f2b-208">When configuring hardware load balancers, consider the following requirements:</span></span>

  - <span data-ttu-id="72f2b-209">A conversão de endereços de rede de origem (SNAT) pode ser configurada no balanceamento de carga de hardware (HLB) para serviço de borda de acesso e serviço de borda de conferência Web</span><span class="sxs-lookup"><span data-stu-id="72f2b-209">Source Network Address Translation (SNAT) can be configured on the hardware load balancer (HLB) for Access Edge service and Web Conferencing Edge service</span></span>

  - <span data-ttu-id="72f2b-210">O SNAT não pode ser configurado no serviço de borda A/V – o serviço de borda A/V deve responder com o endereço do servidor real, e não com o IP virtual (VIP) do HLB, para fazer uma simples passagem do UDP sobre NAT (STUN)/Traversal usando o NAT de retransmissão (ativar)/Federation TURN (FTURN) para funcionar corretamente</span><span class="sxs-lookup"><span data-stu-id="72f2b-210">SNAT cannot be configured on the A/V Edge service– the A/V Edge service must respond with the real server address, not the HLB virtual IP (VIP), for simple traversal of UDP over NAT (STUN)/traversal using relay NAT (TURN)/federation TURN (FTURN) to work properly</span></span>
    
      - <span data-ttu-id="72f2b-211">Se o cliente envia uma solicitação para o HLB, a resposta deve retornar do VIP HLB</span><span class="sxs-lookup"><span data-stu-id="72f2b-211">If the client sends a request to the HLB, the response must come back from the HLB VIP</span></span>
    
      - <span data-ttu-id="72f2b-212">Se o cliente envia uma solicitação para a borda, a resposta deve retornar do IP de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-212">If the client sends a request to the Edge, the response must come back from the Edge IP</span></span>

  - <span data-ttu-id="72f2b-213">Os endereços IP públicos são usados em cada interface do servidor e nos VIPs do HLB, e as suas necessidades de endereço IP público são N + 1, onde há um endereço IP público para cada interface do servidor real e outra para cada VIP HLB.</span><span class="sxs-lookup"><span data-stu-id="72f2b-213">Public IP addresses are used on each server interface and on the VIPs of the HLB, and your public IP address requirements are N+1, where there is a public IP address for each real server interface and one for each HLB VIP.</span></span> <span data-ttu-id="72f2b-214">Onde você tem dois servidores de borda no pool, isso resulta em 9 endereços IP públicos, em que 3 são usados para VIPs HLB e um para cada interface do servidor de borda (um total de seis para os servidores)</span><span class="sxs-lookup"><span data-stu-id="72f2b-214">Where you have 2 Edge servers in the pool, this results in 9 public IP addresses, where 3 are used for the HLB VIPs, and one for each Edge server interface (a total of six for the servers)</span></span>

  - <span data-ttu-id="72f2b-215">Para o serviço de borda de acesso e o serviço de borda de Webconferência (e usar NAT no HLB) o cliente entra em contato com o VIP, o VIP altera o endereço IP de origem do cliente para seu próprio endereço IP.</span><span class="sxs-lookup"><span data-stu-id="72f2b-215">For the Access Edge service and Web Conferencing Edge service, (and using NAT on the HLB) the client contacts the VIP, the VIP changes the source IP address from the client to its own IP address.</span></span> <span data-ttu-id="72f2b-216">A interface do servidor endereça o endereço do remetente ao VIP, o VIP altera o endereço de origem do endereço IP da interface do servidor e envia o pacote para o cliente</span><span class="sxs-lookup"><span data-stu-id="72f2b-216">The server interface addresses the return address to the VIP, the VIP changes the source address from the server interface IP address and sends the packet to the client</span></span>

  - <span data-ttu-id="72f2b-217">Para o serviço de borda a/V, o VIP não deve alterar o endereço IP de origem e o endereço do servidor real é retornado ao cliente diretamente – você não pode configurar o NAT no HLB para tráfego de AV</span><span class="sxs-lookup"><span data-stu-id="72f2b-217">For the A/V Edge service, the VIP must NOT change the source IP address, and the real server address is returned to the client directly – you cannot configure NAT on the HLB for AV traffic</span></span>
    
      - <span data-ttu-id="72f2b-218">Se o cliente envia uma solicitação para o VIP HLB, a resposta deve retornar do VIP HLB</span><span class="sxs-lookup"><span data-stu-id="72f2b-218">If the client sends a request to the HLB VIP, the response must come back from the HLB VIP</span></span>
    
      - <span data-ttu-id="72f2b-219">Se o cliente envia uma solicitação ao IP de borda, a resposta deve retornar do IP de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-219">If the client sends a request to the Edge IP, the response must come back from the Edge IP</span></span>

  - <span data-ttu-id="72f2b-220">Para o AV, o firewall externo manterá o endereço IP público do real Server para todos os pacotes</span><span class="sxs-lookup"><span data-stu-id="72f2b-220">For AV, the external firewall will retain the real server public IP address for all packets</span></span>

  - <span data-ttu-id="72f2b-221">Depois de estabelecida, o cliente para a comunicação do serviço de borda a/V se destina ao real Server, não ao HLB</span><span class="sxs-lookup"><span data-stu-id="72f2b-221">Once established, client to A/V Edge service communication is to the real server, not the HLB</span></span>

  - <span data-ttu-id="72f2b-222">A borda interna para servidores internos e clientes devem ser roteadas, e as rotas persistentes são definidas para todas as redes internas que hospedam servidores ou clientes</span><span class="sxs-lookup"><span data-stu-id="72f2b-222">Internal edge to internal servers and clients must be routed, and persistent routes are set for all internal networks that host servers or clients</span></span>

  - <span data-ttu-id="72f2b-223">O serviço de borda de acesso do HLB funcionará como o gateway padrão para cada interface do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-223">The HLB Access Edge service VIP will act as the default gateway for each Edge server interface</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="72f2b-224">Para obter mais informações sobre o planejamento e a funcionalidade do NAT, consulte <A href="lync-server-2013-hardware-load-balancer-requirements.md">requisitos do balanceador de carga de hardware para o Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="72f2b-224">For further information on NAT planning and functionality, please refer to <A href="lync-server-2013-hardware-load-balancer-requirements.md">Hardware load balancer requirements for Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="72f2b-225">![Detalhes de portas e protocolos do servidor de borda](images/Gg398739.1c193b80-98ab-4d59-a854-dbfdb5e209e2(OCS.15).jpg "Detalhes de portas e protocolos do servidor de borda")</span><span class="sxs-lookup"><span data-stu-id="72f2b-225">![Edge Server ports and protocols details](images/Gg398739.1c193b80-98ab-4d59-a854-dbfdb5e209e2(OCS.15).jpg "Edge Server ports and protocols details")</span></span>

### <a name="external-port-settings-required-for-scaled-consolidated-edge-hardware-load-balanced-external-interface-virtual-ips"></a><span data-ttu-id="72f2b-226">Configurações de porta externa necessárias para borda consolidada dimensionada, carga de hardware balanceada: IPs virtuais de interface externa</span><span class="sxs-lookup"><span data-stu-id="72f2b-226">External Port Settings Required for Scaled Consolidated Edge, Hardware Load Balanced: External Interface Virtual IPs</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72f2b-227">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="72f2b-227">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="72f2b-228">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="72f2b-228">Source IP address</span></span></th>
<th><span data-ttu-id="72f2b-229">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="72f2b-229">Destination IP address</span></span></th>
<th><span data-ttu-id="72f2b-230">Notas</span><span class="sxs-lookup"><span data-stu-id="72f2b-230">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-231">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="72f2b-231">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="72f2b-232">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-232">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-233">Serviço de proxy XMPP (compartilha o endereço IP com o serviço de borda de acesso)</span><span class="sxs-lookup"><span data-stu-id="72f2b-233">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="72f2b-234">O serviço de proxy XMPP aceita o tráfego de contatos do XMPP em agrupamentos XMPP definidos</span><span class="sxs-lookup"><span data-stu-id="72f2b-234">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-235">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="72f2b-235">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="72f2b-236">Serviço de proxy XMPP (compartilha o endereço IP com o serviço de borda de acesso)</span><span class="sxs-lookup"><span data-stu-id="72f2b-236">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="72f2b-237">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-237">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-238">O serviço de proxy XMPP envia o tráfego para os contatos do XMPP em federações XMPP definidas</span><span class="sxs-lookup"><span data-stu-id="72f2b-238">XMPP Proxy service sends traffic to XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-239">/TCP/443 de acesso/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="72f2b-239">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="72f2b-240">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-240">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-241">Endereço VIP público do serviço de borda do Access</span><span class="sxs-lookup"><span data-stu-id="72f2b-241">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-242">Tráfego SIP de cliente para servidor para acesso de usuário externo</span><span class="sxs-lookup"><span data-stu-id="72f2b-242">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-243">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="72f2b-243">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="72f2b-244">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-244">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-245">Endereço VIP público do serviço de borda do Access</span><span class="sxs-lookup"><span data-stu-id="72f2b-245">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-246">Sinalização SIP, conectividade de mensagens de chat públicas e federadas usando o SIP</span><span class="sxs-lookup"><span data-stu-id="72f2b-246">SIP signaling, federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-247">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="72f2b-247">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="72f2b-248">Endereço VIP público do serviço de borda do Access</span><span class="sxs-lookup"><span data-stu-id="72f2b-248">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-249">Parceiro federado</span><span class="sxs-lookup"><span data-stu-id="72f2b-249">Federated partner</span></span></p></td>
<td><p><span data-ttu-id="72f2b-250">Sinalização SIP, conectividade de mensagens de chat públicas e federadas usando o SIP</span><span class="sxs-lookup"><span data-stu-id="72f2b-250">SIP signaling, federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-251">Web Conferencing/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="72f2b-251">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="72f2b-252">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-252">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-253">Endereço VIP público do serviço de borda de Webconferência da Web Edge</span><span class="sxs-lookup"><span data-stu-id="72f2b-253">Edge Server Web Conferencing Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-254">Mídia de Webconferência</span><span class="sxs-lookup"><span data-stu-id="72f2b-254">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-255">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="72f2b-255">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="72f2b-256">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-256">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-257">Endereço VIP público do serviço Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="72f2b-257">Edge Server A/V Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-258">STUN/desliga a negociação de candidatos via UDP/3478</span><span class="sxs-lookup"><span data-stu-id="72f2b-258">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-259">A/V/STUN, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="72f2b-259">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="72f2b-260">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-260">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-261">Endereço VIP público do serviço Edge Server A/V</span><span class="sxs-lookup"><span data-stu-id="72f2b-261">Edge Server A/V Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="72f2b-262">STUN/TRANSFORMe a negociação de candidatos via TCP/443</span><span class="sxs-lookup"><span data-stu-id="72f2b-262">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-internal-interface-virtual-ips"></a><span data-ttu-id="72f2b-263">Resumo de firewall para borda consolidada em escala, balanceamento de carga de hardware: interface interna IPs virtual</span><span class="sxs-lookup"><span data-stu-id="72f2b-263">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: Internal Interface Virtual IPs</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72f2b-264">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="72f2b-264">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="72f2b-265">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="72f2b-265">Source IP address</span></span></th>
<th><span data-ttu-id="72f2b-266">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="72f2b-266">Destination IP address</span></span></th>
<th><span data-ttu-id="72f2b-267">Notas</span><span class="sxs-lookup"><span data-stu-id="72f2b-267">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-268">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="72f2b-268">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="72f2b-269">Any (pode ser definido como director, endereço IP virtual do pool do diretor, servidor front-end ou endereço IP virtual do pool de front-end)</span><span class="sxs-lookup"><span data-stu-id="72f2b-269">Any (can be defined as Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)</span></span></p></td>
<td><p><span data-ttu-id="72f2b-270">Interface VIP interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-270">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="72f2b-271">Tráfego SIP de saída (do diretor, endereço IP virtual do pool diretor, servidor front-end ou endereço IP virtual do pool de front-end) para VIP de borda interna</span><span class="sxs-lookup"><span data-stu-id="72f2b-271">Outbound SIP traffic (from Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)to Internal Edge VIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-272">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="72f2b-272">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="72f2b-273">Interface VIP interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-273">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="72f2b-274">Any (pode ser definido como director, endereço IP virtual do pool do diretor, servidor front-end ou endereço IP virtual do pool de front-end)</span><span class="sxs-lookup"><span data-stu-id="72f2b-274">Any (can be defined as Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)</span></span></p></td>
<td><p><span data-ttu-id="72f2b-275">Tráfego SIP de entrada (para o director, endereço IP virtual do pool diretor, servidor front-end ou endereço IP virtual do pool de front-end) da interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-275">Inbound SIP traffic (to Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-276">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="72f2b-276">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="72f2b-277">Any (pode ser definido como endereço IP do servidor front-end ou endereço IP do pool de front-end ou qualquer aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes que use este servidor de borda)</span><span class="sxs-lookup"><span data-stu-id="72f2b-277">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="72f2b-278">Interface VIP interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-278">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="72f2b-279">Autenticação de usuários de A/V (serviço de autenticação A/V) do servidor front-end ou do endereço IP do pool de front-end ou qualquer aparelho de ramificação sobreviventes ou servidor de ramificação sobreviventes que use este servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-279">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-280">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="72f2b-280">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="72f2b-281">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-281">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-282">Interface VIP interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-282">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="72f2b-283">Caminho preferencial para transferência de mídia A/V entre usuários internos e externos</span><span class="sxs-lookup"><span data-stu-id="72f2b-283">Preferred path for A/V media transfer between internal and external users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72f2b-284">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="72f2b-284">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="72f2b-285">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-285">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-286">Interface VIP interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-286">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="72f2b-287">Caminho de fallback para transferência de mídia A/V entre usuários internos e externos se não for possível estabelecer a comunicação UDP, o TCP será usado para transferência de arquivos e compartilhamento de área de trabalho</span><span class="sxs-lookup"><span data-stu-id="72f2b-287">Fallback path for A/V media transfer between internal and external users if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72f2b-288">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="72f2b-288">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="72f2b-289">Interface VIP interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="72f2b-289">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="72f2b-290">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="72f2b-290">Any</span></span></p></td>
<td><p><span data-ttu-id="72f2b-291">Caminho de fallback para transferência de mídia A/V entre usuários internos e externos se não for possível estabelecer a comunicação UDP, o TCP será usado para transferência de arquivos e compartilhamento de área de trabalho</span><span class="sxs-lookup"><span data-stu-id="72f2b-291">Fallback path for A/V media transfer between internal and external users if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="72f2b-292">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="72f2b-292">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

