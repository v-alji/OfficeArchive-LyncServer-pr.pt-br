---
title: Requisitos de porta do Lync Server 2013
description: Requisitos de porta do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port requirements
ms:assetid: 9a6c1300-ef88-4181-a8f1-43cd3093962b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398798(v=OCS.15)
ms:contentKeyID: 48184886
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba7ae9a1ee098f55c61ae476f12c3b856c69f90e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424391"
---
# <a name="port-requirements-for-lync-server-2013"></a><span data-ttu-id="6375d-103">Requisitos de porta para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6375d-103">Port requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6375d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6375d-104">

<span> </span></span></span>

<span data-ttu-id="6375d-105">_**Tópico da última modificação:** 2013-03-27_</span><span class="sxs-lookup"><span data-stu-id="6375d-105">_**Topic Last Modified:** 2013-03-27_</span></span>

<span data-ttu-id="6375d-106">O Lync Server requer a abertura de portas específicas no firewall.</span><span class="sxs-lookup"><span data-stu-id="6375d-106">Lync Server requires that specific ports on the firewall be open.</span></span> <span data-ttu-id="6375d-107">Adicionalmente, se o protocolo IPsec (Internet Protocol security) tiver sido implantado em sua organização, ele deverá estar desabilitado no intervalo de portas usadas para a distribuição de áudio, vídeo e vídeo panorama.</span><span class="sxs-lookup"><span data-stu-id="6375d-107">Additionally, if Internet Protocol security (IPsec) is deployed in your organization, IPsec must be disabled over the range of ports used for the delivery of audio, video, and panorama video.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6375d-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6375d-108">In This Section</span></span>

<span data-ttu-id="6375d-109">Esta seção inclui os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="6375d-109">This section includes the following topics:</span></span>

  - [<span data-ttu-id="6375d-110">Portas e protocolos para servidores internos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6375d-110">Ports and protocols for internal servers in Lync Server 2013</span></span>](lync-server-2013-ports-and-protocols-for-internal-servers.md)

  - [<span data-ttu-id="6375d-111">Exceções de IPsec no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6375d-111">IPsec exceptions in Lync Server 2013</span></span>](lync-server-2013-ipsec-exceptions.md)

  - [<span data-ttu-id="6375d-112">Resumo de porta - única borda consolidada com endereços IP privados usando NAT no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6375d-112">Port summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-port-summary-single-consolidated-edge-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="6375d-113">Sumário de porta - única borda consolidada com endereços IP públicos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6375d-113">Port summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-port-summary-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="6375d-114">Resumo de porta - borda consolidada em escala, balanceamento de carga de DNS com endereços IP privados usando NAT no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6375d-114">Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-port-summary-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="6375d-115">Resumo de porta - Borda consolidada em escala, balanceamento de carga de DNS com endereços IP públicos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6375d-115">Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-port-summary-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

  - [<span data-ttu-id="6375d-116">Resumo de porta - borda consolidada em escala com balanceadores de carga de hardware no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6375d-116">Port summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md)

  - [<span data-ttu-id="6375d-117">Resumo de porta - Proxy reverso no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6375d-117">Port summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-port-summary-reverse-proxy.md)

  - [<span data-ttu-id="6375d-118">Resumo da porta-SIP, Federação do XMPP e mensagens instantâneas públicas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6375d-118">Port summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-port-summary-sip-xmpp-federation-and-public-instant-messaging.md)

<span data-ttu-id="6375d-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6375d-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

