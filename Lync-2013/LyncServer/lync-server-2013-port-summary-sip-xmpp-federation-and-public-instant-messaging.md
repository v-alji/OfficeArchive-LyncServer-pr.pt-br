---
title: Resumo da porta-SIP, Federação do XMPP e mensagens instantâneas públicas
description: Resumo da porta-SIP, Federação do XMPP e mensagens instantâneas públicas.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - SIP, XMPP federation, and public instant messaging
ms:assetid: ab05bdd6-e9b0-4b1b-9dd9-29ab88e8befe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618373(v=OCS.15)
ms:contentKeyID: 49105660
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7c58dbf7bdd56b4678d56f96a11332219bb40c17
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389780"
---
# <a name="port-summary---sip-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="cd3df-103">Resumo da porta-SIP, Federação do XMPP e mensagens instantâneas públicas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd3df-103">Port summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cd3df-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cd3df-104">

<span> </span></span></span>

<span data-ttu-id="cd3df-105">_**Tópico da última modificação:** 2013-03-15_</span><span class="sxs-lookup"><span data-stu-id="cd3df-105">_**Topic Last Modified:** 2013-03-15_</span></span>

<span data-ttu-id="cd3df-106">Os requisitos de portabilidade, protocolo e firewall para federação com o Microsoft Lync Server 2013, o Lync Server 2010 e o Office Communications Server são semelhantes aos do servidor de borda implantado.</span><span class="sxs-lookup"><span data-stu-id="cd3df-106">Port, protocol and firewall requirements for federation with Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server are similar to those for the deployed Edge Server.</span></span> <span data-ttu-id="cd3df-107">Os clientes iniciam a comunicação com o serviço de borda de acesso por TLS/SIP/TCP 443.</span><span class="sxs-lookup"><span data-stu-id="cd3df-107">Clients initiate communication with the Access Edge service over TLS/SIP/TCP 443.</span></span> <span data-ttu-id="cd3df-108">No entanto, os parceiros federados iniciarão as comunicações com o serviço de borda de acesso sobre MTLS/SIP/TCP 5061.</span><span class="sxs-lookup"><span data-stu-id="cd3df-108">Federated partners however, will initiate communications to the Access Edge service over MTLS/SIP/TCP 5061.</span></span>

<span data-ttu-id="cd3df-109">Para configurar o seu firewall para portas e protocolos necessários para dar suporte à conectividade de mensagens instantâneas públicas, primeiro Observe que SIP/MTLS/TCP 5061 é bidirecional para a conta da capacidade dos contatos no provedor de IM públicos entrarem em contato com os clientes do Lync ou para que o Lync entre em contato com contatos públicos de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="cd3df-109">To configure your firewall for ports and protocols necessary to support public instant messaging connectivity, first note that SIP/MTLS/TCP 5061 is bidirectional to account for the ability of contacts in the public IM provider to contact Lync clients, or for Lync to contact public IM contacts.</span></span>

<span data-ttu-id="cd3df-110">O Windows Live Messenger pode participar de comunicações de áudio/vídeo com clientes do Lync.</span><span class="sxs-lookup"><span data-stu-id="cd3df-110">Windows Live Messenger can participate in audio/video communications with Lync clients.</span></span> <span data-ttu-id="cd3df-111">Isso conta com uma configuração de protocolo e porta de firewall muito parecidas que você normalmente teria no firewall para dar suporte a clientes Lync como usuários externos.</span><span class="sxs-lookup"><span data-stu-id="cd3df-111">This accounts for the very similar firewall port and protocol configuration that you would typically have on the firewall to support Lync clients as external users.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="cd3df-112">Mais do que nunca, o Lync é uma ferramenta poderosa para a conexão entre organizações e pessoas ao redor do mundo.</span><span class="sxs-lookup"><span data-stu-id="cd3df-112">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="cd3df-113">A Federação com o Windows Live Messenger não requer mais licenças de usuário/dispositivo além da licença de acesso de cliente padrão do Lync (CAL).</span><span class="sxs-lookup"><span data-stu-id="cd3df-113">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard Client Access License (CAL).</span></span> <span data-ttu-id="cd3df-114">A Federação do Skype será adicionada a essa lista, permitindo que os usuários do Lync atinjam centenas de milhões de pessoas com mensagens instantâneas e voz.</span><span class="sxs-lookup"><span data-stu-id="cd3df-114">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span><BR><span data-ttu-id="cd3df-115">A Federação com contatos de cliente do Messenger será encerrada oficialmente em 15 de março de 2013, exceto para a China continental.</span><span class="sxs-lookup"><span data-stu-id="cd3df-115">Federation with Messenger client contacts will officially end on March 15, 2013, except for mainland China.</span></span> <span data-ttu-id="cd3df-116">O Skype se tornará o cliente de Federação para usuários federados que usaram anteriormente o Messenger.</span><span class="sxs-lookup"><span data-stu-id="cd3df-116">Skype will become the federation client for federated users who previously used Messenger.</span></span>



</div>

<span data-ttu-id="cd3df-117">As portas e protocolos definidos para o proxy de protocolo de presença e mensagens extensível (XMPP) implantadas no servidor de borda permitem comunicações do parceiro federado do XMPP com o servidor de borda e também permite a comunicação do servidor de borda com o parceiro federado do XMPP.</span><span class="sxs-lookup"><span data-stu-id="cd3df-117">The ports and protocols defined for the extensible messaging and presence protocol (XMPP) proxy deployed on the Edge Server allow communications from the XMPP federated partner to the Edge Server, and also allows communication from your Edge Server to the XMPP federated partner.</span></span> <span data-ttu-id="cd3df-118">Uma regra também é definida no firewall de face interna do servidor front-end ou do pool de front-ends para o servidor de borda ou o pool de bordas.</span><span class="sxs-lookup"><span data-stu-id="cd3df-118">A rule is also defined on the internal-facing firewall from the Front End Server or Front End pool to the Edge Server or Edge pool.</span></span>

<div>

## <a name="firewall-summary---sip-federation"></a><span data-ttu-id="cd3df-119">Resumo do firewall-Federação SIP</span><span class="sxs-lookup"><span data-stu-id="cd3df-119">Firewall Summary - SIP Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd3df-120">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="cd3df-120">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="cd3df-121">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="cd3df-121">Source IP address</span></span></th>
<th><span data-ttu-id="cd3df-122">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="cd3df-122">Destination IP address</span></span></th>
<th><span data-ttu-id="cd3df-123">Notas</span><span class="sxs-lookup"><span data-stu-id="cd3df-123">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd3df-124">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="cd3df-124">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="cd3df-125">Endereço IP público do serviço de borda do Access</span><span class="sxs-lookup"><span data-stu-id="cd3df-125">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="cd3df-126">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="cd3df-126">Any</span></span></p></td>
<td><p><span data-ttu-id="cd3df-127">Para conectividade de mensagens de chat públicas e federadas usando SIP</span><span class="sxs-lookup"><span data-stu-id="cd3df-127">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="cd3df-128">Resumo do Firewall – Conectividade de mensagens instantâneas públicas</span><span class="sxs-lookup"><span data-stu-id="cd3df-128">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd3df-129">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="cd3df-129">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="cd3df-130">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="cd3df-130">Source IP address</span></span></th>
<th><span data-ttu-id="cd3df-131">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="cd3df-131">Destination IP address</span></span></th>
<th><span data-ttu-id="cd3df-132">Notas</span><span class="sxs-lookup"><span data-stu-id="cd3df-132">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd3df-133">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="cd3df-133">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="cd3df-134">Parceiros de conectividade de mensagens de chat públicas</span><span class="sxs-lookup"><span data-stu-id="cd3df-134">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="cd3df-135">Interface de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="cd3df-135">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="cd3df-136">Para conectividade de mensagem de chat pública e federada que usa SIP.</span><span class="sxs-lookup"><span data-stu-id="cd3df-136">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd3df-137">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="cd3df-137">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="cd3df-138">Interface de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="cd3df-138">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="cd3df-139">Parceiros de conectividade de mensagens de chat públicas</span><span class="sxs-lookup"><span data-stu-id="cd3df-139">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="cd3df-140">Para conectividade de mensagem de chat pública e federada que usa SIP.</span><span class="sxs-lookup"><span data-stu-id="cd3df-140">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd3df-141">/TCP/443 de acesso/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="cd3df-141">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="cd3df-142">Clientes</span><span class="sxs-lookup"><span data-stu-id="cd3df-142">Clients</span></span></p></td>
<td><p><span data-ttu-id="cd3df-143">Interface de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="cd3df-143">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="cd3df-144">Tráfego SIP do cliente ao servidor para o acesso do usuário externo.</span><span class="sxs-lookup"><span data-stu-id="cd3df-144">Client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd3df-145">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="cd3df-145">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="cd3df-146">Interface de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="cd3df-146">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="cd3df-147">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="cd3df-147">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="cd3df-148">Usado para sessões de A/V com o Windows Live Messenger se a conectividade de mensagem de chat pública estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="cd3df-148">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd3df-149">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="cd3df-149">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="cd3df-150">Interface de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="cd3df-150">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="cd3df-151">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="cd3df-151">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="cd3df-152">Necessário para conectividade de IM pública com o Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="cd3df-152">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd3df-153">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="cd3df-153">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="cd3df-154">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="cd3df-154">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="cd3df-155">Interface de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="cd3df-155">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="cd3df-156">Necessário para conectividade de IM pública com o Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="cd3df-156">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary---extensible-messaging-and-presence-protocol-xmpp"></a><span data-ttu-id="cd3df-157">Resumo de firewall-mensagens extensíveis e protocolo de presença (XMPP)</span><span class="sxs-lookup"><span data-stu-id="cd3df-157">Firewall Summary - Extensible Messaging and Presence Protocol (XMPP)</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd3df-158">Protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="cd3df-158">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="cd3df-159">Fonte (endereço IP)</span><span class="sxs-lookup"><span data-stu-id="cd3df-159">Source (IP address)</span></span></th>
<th><span data-ttu-id="cd3df-160">Destino (endereço IP)</span><span class="sxs-lookup"><span data-stu-id="cd3df-160">Destination (IP address)</span></span></th>
<th><span data-ttu-id="cd3df-161">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd3df-161">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd3df-162">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="cd3df-162">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="cd3df-163">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="cd3df-163">Any</span></span></p></td>
<td><p><span data-ttu-id="cd3df-164">Endereço IP da interface do serviço de borda do Access</span><span class="sxs-lookup"><span data-stu-id="cd3df-164">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="cd3df-165">Porta de comunicação de servidor para servidor padrão para XMPP.</span><span class="sxs-lookup"><span data-stu-id="cd3df-165">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="cd3df-166">Permite a comunicação com o servidor de borda XMPP o proxy de parceiros de XMPP federado</span><span class="sxs-lookup"><span data-stu-id="cd3df-166">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd3df-167">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="cd3df-167">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="cd3df-168">Endereço IP da interface do serviço de borda do Access</span><span class="sxs-lookup"><span data-stu-id="cd3df-168">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="cd3df-169">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="cd3df-169">Any</span></span></p></td>
<td><p><span data-ttu-id="cd3df-170">Porta de comunicação de servidor para servidor padrão para XMPP.</span><span class="sxs-lookup"><span data-stu-id="cd3df-170">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="cd3df-171">Permite a comunicação do proxy do servidor de borda XMPP com parceiros do XMPP federado</span><span class="sxs-lookup"><span data-stu-id="cd3df-171">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd3df-172">XMPP/MTLS/23456</span><span class="sxs-lookup"><span data-stu-id="cd3df-172">XMPP/MTLS/23456</span></span></p></td>
<td><p><span data-ttu-id="cd3df-173">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="cd3df-173">Any</span></span></p></td>
<td><p><span data-ttu-id="cd3df-174">IP de interface do servidor de borda interna</span><span class="sxs-lookup"><span data-stu-id="cd3df-174">Internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="cd3df-175">Tráfego de XMPP interno do Gateway XMPP no servidor front-end ou do pool de front-end para o servidor de borda</span><span class="sxs-lookup"><span data-stu-id="cd3df-175">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="cd3df-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd3df-176">See Also</span></span>


[<span data-ttu-id="cd3df-177">Cenários de acesso de usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd3df-177">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="cd3df-178">Determinar firewall A/V externo e requisitos de porta para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd3df-178">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  


[<span data-ttu-id="cd3df-179">Gerenciar parceiros XMPP federados no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd3df-179">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
  

<span data-ttu-id="cd3df-180"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cd3df-180"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

