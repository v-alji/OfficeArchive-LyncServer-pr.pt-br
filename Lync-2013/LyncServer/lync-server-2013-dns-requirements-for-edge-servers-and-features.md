---
title: 'Lync Server 2013: requisitos de DNS para servidores e recursos de Edge'
description: 'Lync Server 2013: requisitos de DNS para servidores e recursos de Edge.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Edge Servers and features
ms:assetid: e3bf05c8-96fb-4dd2-acb1-f0d141c9e2ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721912(v=OCS.15)
ms:contentKeyID: 49733846
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9bcfd00080e765924eecc3138bc3d552ce331b63
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390304"
---
# <a name="dns-requirements-for-edge-servers-and-features-in-lync-server-2013"></a><span data-ttu-id="3a25b-103">Requisitos de DNS para servidores de borda e recursos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3a25b-103">DNS requirements for Edge Servers and features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3a25b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3a25b-104">

<span> </span></span></span>

<span data-ttu-id="3a25b-105">_**Tópico da última modificação:** 2014-04-08_</span><span class="sxs-lookup"><span data-stu-id="3a25b-105">_**Topic Last Modified:** 2014-04-08_</span></span>

<span data-ttu-id="3a25b-106">Servidores de borda do Lync Server 2013, pools de bordas e proxies invertidos têm requisitos específicos para registros DNS (sistema de nomes de domínio).</span><span class="sxs-lookup"><span data-stu-id="3a25b-106">Lync Server 2013 Edge Servers, Edge pools, and reverse proxies have specific requirements for Domain Name System (DNS) records.</span></span> <span data-ttu-id="3a25b-107">No Lync Server 2013 quando IPv4 e IPv6 estiverem em uso, você deverá planejar os registros do host A e do AAAA.</span><span class="sxs-lookup"><span data-stu-id="3a25b-107">In Lync Server 2013 when IPv4 and IPv6 are in use, you must plan for both host A and AAAA records.</span></span>

<span data-ttu-id="3a25b-108">Os tópicos listados abaixo definem o uso de registros de DNS para o planejamento de implantação:</span><span class="sxs-lookup"><span data-stu-id="3a25b-108">The topics listed below define the use of DNS records for your deployment planning:</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3a25b-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="3a25b-109">In This Section</span></span>

  - [<span data-ttu-id="3a25b-110">Resumo de DNS - única borda consolidada com endereços IP privados usando NAT no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3a25b-110">DNS summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-dns-summary-single-consolidated-edge-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="3a25b-111">Resumo de DNS - Única borda consolidada com endereços IP públicos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3a25b-111">DNS summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-dns-summary-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="3a25b-112">Resumo de DNS - borda consolidada dimensionada, balanceamento de carga DNS com endereços IP privados usando NAT no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3a25b-112">DNS summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-dns-summary-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="3a25b-113">Resumo de DNS - Borda consolidada em escala, balanceamento de carga de DNS com endereços IP públicos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3a25b-113">DNS summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-dns-summary-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

  - [<span data-ttu-id="3a25b-114">Resumo de DNS - borda consolidada em escala com balanceadores de carga de hardware no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3a25b-114">DNS summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-dns-summary-scaled-consolidated-edge-with-hardware-load-balancers.md)

  - [<span data-ttu-id="3a25b-115">Resumo de DNS - Proxy reverso no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3a25b-115">DNS summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-dns-summary-reverse-proxy.md)

  - [<span data-ttu-id="3a25b-116">Resumo de DNS-SIP, Federação de XMPP e mensagens instantâneas públicas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3a25b-116">DNS summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-dns-summary-sip-xmpp-federation-and-public-instant-messaging.md)

<span data-ttu-id="3a25b-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3a25b-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

