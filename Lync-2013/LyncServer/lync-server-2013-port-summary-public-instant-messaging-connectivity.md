---
title: 'Lync Server 2013: Resumo de porta-conectividade de mensagens instantâneas públicas'
description: 'Lync Server 2013: Resumo de portabilidade-conectividade de mensagens instantâneas públicas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Public instant messaging connectivity
ms:assetid: f46756ec-1401-4ca2-a4a4-5cd28bcfdc7f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618376(v=OCS.15)
ms:contentKeyID: 49105663
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4137b5f92e043dc15dc9aa1f0b9593b4d9f7c2ca
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424272"
---
# <a name="port-summary---public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="29107-103">Resumo de portabilidade-conectividade de mensagens instantâneas públicas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="29107-103">Port summary - Public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="29107-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="29107-104">

<span> </span></span></span>

<span data-ttu-id="29107-105">_**Tópico da última modificação:** 2013-02-16_</span><span class="sxs-lookup"><span data-stu-id="29107-105">_**Topic Last Modified:** 2013-02-16_</span></span>

<span data-ttu-id="29107-106">Para configurar o seu firewall para portas e protocolos necessários para dar suporte à conectividade de mensagens instantâneas públicas, primeiro Observe que SIP/MTLS/TCP 5061 é bidirecional para a conta da capacidade dos contatos no provedor de IM públicos entrarem em contato com os clientes do Lync ou para que o Lync entre em contato com contatos públicos de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="29107-106">To configure your firewall for ports and protocols necessary to support public instant messaging connectivity, first note that SIP/MTLS/TCP 5061 is bidirectional to account for the ability of contacts in the public IM provider to contact Lync clients, or for Lync to contact public IM contacts.</span></span>

<span data-ttu-id="29107-107">O Windows Live Messenger pode participar de comunicações de áudio/vídeo com clientes do Lync.</span><span class="sxs-lookup"><span data-stu-id="29107-107">Windows Live Messenger can participate in audio/video communications with Lync clients.</span></span> <span data-ttu-id="29107-108">Isso conta com uma configuração de protocolo e porta de firewall muito parecidas que você normalmente teria no firewall para dar suporte a clientes Lync como usuários externos.</span><span class="sxs-lookup"><span data-stu-id="29107-108">This accounts for the very similar firewall port and protocol configuration that you would typically have on the firewall to support Lync clients as external users.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="29107-109">Mais do que nunca, o Lync é uma ferramenta poderosa para a conexão entre organizações e pessoas ao redor do mundo.</span><span class="sxs-lookup"><span data-stu-id="29107-109">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="29107-110">A Federação com o Windows Live Messenger não requer mais licenças de usuário/dispositivo além da licença de acesso de cliente padrão do Lync (CAL).</span><span class="sxs-lookup"><span data-stu-id="29107-110">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard Client Access License (CAL).</span></span> <span data-ttu-id="29107-111">A Federação do Skype será adicionada a essa lista, permitindo que os usuários do Lync atinjam centenas de milhões de pessoas com mensagens instantâneas e voz.</span><span class="sxs-lookup"><span data-stu-id="29107-111">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span><BR><span data-ttu-id="29107-112">A Federação com contatos de cliente do Messenger será encerrada oficialmente em 15 de março de 2013, exceto para a China continental.</span><span class="sxs-lookup"><span data-stu-id="29107-112">Federation with Messenger client contacts will officially end on March 15, 2013, except for mainland China.</span></span> <span data-ttu-id="29107-113">O Skype se tornará o cliente de Federação para usuários federados que usaram anteriormente o Messenger.</span><span class="sxs-lookup"><span data-stu-id="29107-113">Skype will become the federation client for federated users who previously used Messenger.</span></span>



</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="29107-114">Resumo do Firewall – Conectividade de mensagens instantâneas públicas</span><span class="sxs-lookup"><span data-stu-id="29107-114">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="29107-115">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="29107-115">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="29107-116">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="29107-116">Source IP address</span></span></th>
<th><span data-ttu-id="29107-117">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="29107-117">Destination IP address</span></span></th>
<th><span data-ttu-id="29107-118">Notas</span><span class="sxs-lookup"><span data-stu-id="29107-118">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29107-119">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="29107-119">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="29107-120">Parceiros de conectividade de mensagens de chat públicas</span><span class="sxs-lookup"><span data-stu-id="29107-120">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="29107-121">Interface de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="29107-121">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="29107-122">Para conectividade de mensagem de chat pública e federada que usa SIP.</span><span class="sxs-lookup"><span data-stu-id="29107-122">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29107-123">/TCP/5061 de acesso/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="29107-123">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="29107-124">Interface de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="29107-124">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="29107-125">Parceiros de conectividade de mensagens de chat públicas</span><span class="sxs-lookup"><span data-stu-id="29107-125">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="29107-126">Para conectividade de mensagem de chat pública e federada que usa SIP.</span><span class="sxs-lookup"><span data-stu-id="29107-126">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29107-127">/TCP/443 de acesso/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="29107-127">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="29107-128">Clientes</span><span class="sxs-lookup"><span data-stu-id="29107-128">Clients</span></span></p></td>
<td><p><span data-ttu-id="29107-129">Interface de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="29107-129">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="29107-130">Tráfego SIP do cliente ao servidor para o acesso do usuário externo.</span><span class="sxs-lookup"><span data-stu-id="29107-130">Client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29107-131">A/V/RTP/TCP/50.000 A 59.999</span><span class="sxs-lookup"><span data-stu-id="29107-131">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="29107-132">Interface de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="29107-132">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="29107-133">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="29107-133">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="29107-134">Usado para sessões de A/V com o Windows Live Messenger se a conectividade de mensagem de chat pública estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="29107-134">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29107-135">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="29107-135">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="29107-136">Interface de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="29107-136">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="29107-137">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="29107-137">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="29107-138">Necessário para conectividade de IM pública com o Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="29107-138">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29107-139">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="29107-139">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="29107-140">Clientes do Live Messenger</span><span class="sxs-lookup"><span data-stu-id="29107-140">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="29107-141">Interface de acesso do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="29107-141">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="29107-142">Necessário para conectividade de IM pública com o Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="29107-142">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="29107-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="29107-143">See Also</span></span>


[<span data-ttu-id="29107-144">Cenários de acesso de usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="29107-144">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="29107-145">Determinar firewall A/V externo e requisitos de porta para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="29107-145">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  
  

<span data-ttu-id="29107-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="29107-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

