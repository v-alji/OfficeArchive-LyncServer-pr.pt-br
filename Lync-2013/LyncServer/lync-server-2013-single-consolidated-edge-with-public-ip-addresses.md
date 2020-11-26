---
title: 'Lync Server 2013: Única borda consolidada com endereços IP públicos'
description: 'Lync Server 2013: borda única consolidada com endereços IP públicos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Single consolidated edge with public IP addresses
ms:assetid: a92d1179-6a1f-4efe-908a-f8dfc5024f30
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205148(v=OCS.15)
ms:contentKeyID: 48185035
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ac829cd15a592a86d2ba5fdfe174703d0c933037
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423846"
---
# <a name="single-consolidated-edge-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="5c7f9-103">Única borda consolidada com endereços IP públicos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c7f9-103">Single consolidated edge with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c7f9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c7f9-104">

<span> </span></span></span>

<span data-ttu-id="5c7f9-105">_**Tópico da última modificação:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="5c7f9-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="5c7f9-106">Se a sua organização precisar de suporte para menos de 15.000 conexões de cliente de serviço de borda de acesso, 1.000 conexões de cliente de serviço de Webconferência do Lync Server Web 500 e as sessões de borda de A/V simultâneas e alta disponibilidade do servidor de borda não for importante, essa topologia oferece as vantagens de reduzir o custo de hardware e a implantação mais simples.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-106">If your organization needs support for fewer than 15,000 Access Edge service client connections, 1,000 active Lync Server Web Conferencing service client connections, and 500 concurrent A/V Edge sessions, and high availability of the Edge Server is not important, this topology offers the advantages of lower hardware cost and simpler deployment.</span></span> <span data-ttu-id="5c7f9-107">Se você precisa de maior capacidade ou requer alta disponibilidade, implante uma topologia de servidor de borda consolidada dimensionada.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-107">If you need greater capacity or you require high availability, you should deploy a scaled consolidated Edge Server topology.</span></span>

  - <span></span>  
    [<span data-ttu-id="5c7f9-108">Borda consolidada em escala, balanceamento de carga de DNS com endereços IP privados usando NAT no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c7f9-108">Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)

  - <span></span>  
    [<span data-ttu-id="5c7f9-109">Borda consolidada em escala, balanceamento de carga de DNS com endereços IP públicos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c7f9-109">Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

  - <span></span>  
    [<span data-ttu-id="5c7f9-110">Borda consolidada em escala com balanceadores de carga de hardware no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c7f9-110">Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md)

<div>


> [!IMPORTANT]  
> <span data-ttu-id="5c7f9-111">Ao usar o endereço IP público no servidor de borda, o gateway padrão no servidor de borda não é mais o firewall ou o roteador, mas o roteador ou o firewall na sua borda pública do perímetro – que será um endereço público.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-111">When using public IP address on the Edge Server, the default gateway on the Edge Server is no longer your firewall or router, but the router or firewall at your public perimeter edge – which will be a public address.</span></span> <span data-ttu-id="5c7f9-112">O proxy reverso continua a usar o roteador ou o firewall associado à rede de perímetro mais externa.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-112">The reverse proxy continues to use the router or firewall associated with the outermost perimeter network.</span></span> <span data-ttu-id="5c7f9-113">A diferença entre o proxy reverso e o servidor de borda com endereços IP públicos é que o proxy reverso ainda está usando NAT, e o servidor de borda está usando uma relação de rota.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-113">The difference between the reverse proxy and the Edge Server with public IP addresses is that the reverse proxy is still using NAT and the Edge Server is using a route relationship.</span></span>



</div>

<span data-ttu-id="5c7f9-114">A figura não mostra diretores, uma função de servidor opcional implantada na rede interna entre os servidores de borda e seus pools ou servidores de front-end.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-114">The figure does not show Directors, an optional server role deployed in the internal network between the Edge Servers and your Front End pools or server.</span></span> <span data-ttu-id="5c7f9-115">Para obter detalhes sobre a topologia para diretores, consulte [os componentes necessários para o diretor no Lync Server 2013](lync-server-2013-components-required-for-the-director.md).</span><span class="sxs-lookup"><span data-stu-id="5c7f9-115">For details about the topology for Directors, see [Components required for the Director in Lync Server 2013](lync-server-2013-components-required-for-the-director.md).</span></span> <span data-ttu-id="5c7f9-116">A figura representa um único proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-116">The figure represents a single reverse proxy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5c7f9-117">A imagem mostrada é para orientação e exemplo de endereçamento IP, mas não pretende representar os fluxos de comunicação reais com o tráfego de entrada e saída correto.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-117">The figure shown is for orientation and example IP addressing, but does not intend to represent actual communication flows with the correct incoming and outgoing traffic.</span></span> <span data-ttu-id="5c7f9-118">A figura representa uma exibição de alto nível do possível tráfego.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-118">The figure represents a high level view of possible traffic.</span></span> <span data-ttu-id="5c7f9-119">Os detalhes do fluxo de tráfego que pertencem à entrada (em portas de escuta) e saída (para clientes ou servidores de destino) são representados no diagrama de Resumo de porta em cada cenário.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-119">Details for traffic flow as they pertain to incoming (to listening ports) and outgoing (to destination servers or clients) is represented in the Port Summary diagram in each scenario.</span></span> <span data-ttu-id="5c7f9-120">Por exemplo, o TCP 443 é realmente de entrada (apenas para a borda ou proxy reverso) e só é um fluxo bidirecional de uma perspectiva de protocolo (TCP).</span><span class="sxs-lookup"><span data-stu-id="5c7f9-120">For example, TCP 443 is actually inbound (to the Edge or reverse proxy) only, and is only a two-way flow from a protocol (TCP) perspective.</span></span> <span data-ttu-id="5c7f9-121">Além disso, a figura mostra a natureza do tráfego à medida que ele muda quando o NAT (conversão de endereço de rede) ocorre (o endereço de destino é alterado em entrada, o endereço de origem é alterado na saída).</span><span class="sxs-lookup"><span data-stu-id="5c7f9-121">Additionally, the figure shows the nature of traffic as it changes when NAT (network address translation) occurs (destination address is changed on inbound, source address is changed on outbound).</span></span> <span data-ttu-id="5c7f9-122">Exemplo de firewall externo e interno e interfaces do servidor são mostradas somente para fins de referência.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-122">Example external and internal firewall, and server interfaces are shown for reference purposes only.</span></span> <span data-ttu-id="5c7f9-123">Por fim, o gateway padrão e as relações de rota são exibidos, quando aplicável.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-123">Finally, example default gateway and route relationships are shown, where applicable.</span></span> <span data-ttu-id="5c7f9-124">Observe também que o diagrama usa a zona DNS <EM>. com</EM> para representar a zona DNS externa para servidores de proxy reverso e Edge e a zona DNS do <EM>.net</EM> refere-se à zona DNS interna.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-124">Note also that the diagram uses the <EM>.com</EM> DNS zone to represent the external DNS zone for both reverse proxy and Edge Servers, and the <EM>.net</EM> DNS zone refers to the internal DNS zone.</span></span>



</div>

<span data-ttu-id="5c7f9-125">O novo para o Microsoft Lync Server 2013 é compatível com endereçamento IPv6.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-125">New to Microsoft Lync Server 2013 is support for IPv6 addressing.</span></span> <span data-ttu-id="5c7f9-126">Como endereçamento IPv4, os endereços IPv6 devem ser atribuídos de forma que os endereços sejam parte do espaço de endereço IPv6 atribuído.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-126">Much like IPv4 addressing, IPv6 addresses must be assigned in such a way that the addresses are part of your assigned IPv6 address space.</span></span> <span data-ttu-id="5c7f9-127">Os endereços neste tópico são somente por exemplo.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-127">The addresses in this topic are for example only.</span></span> <span data-ttu-id="5c7f9-128">Você deve adquirir endereços IPv6 que funcionarão na sua implantação, fornecer o escopo correto e interoperar com o endereçamento interno e externo.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-128">You must acquire IPv6 addresses that will function in your deployment, provide the correct scope and will interoperate with internal and external addressing.</span></span> <span data-ttu-id="5c7f9-129">O Windows Server fornece um recurso que é importante para a operação IPv6 de transição e comunicação IPv4 para IPv6 chamada de *pilha dupla*.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-129">Windows Server provides a feature that is important to transitional IPv6 operation and IPv4 to IPv6 communication called the *dual stack*.</span></span> <span data-ttu-id="5c7f9-130">A pilha dupla é uma pilha de rede separada e distinta para IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-130">The dual stack is a separate and distinct network stack for IPv4 and for IPv6.</span></span> <span data-ttu-id="5c7f9-131">A pilha dupla é o que permite atribuir endereçamento para IPv4 e IPv6 simultaneamente e permite que o servidor se comunique com outros hosts e clientes de acordo com suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-131">The dual stack is what allows you to assign addressing for IPv4 and IPv6 concurrently, and allows the server to communicate with other hosts and clients based on what their requirements are.</span></span>

<span data-ttu-id="5c7f9-132">Os tipos de endereços típicos que você usará para endereçamento IPv6 serão os endereços globais IPv6 (semelhantes aos endereços IPv4 públicos), os endereços locais exclusivos do IPv6 (semelhantes aos intervalos de endereços IPv4 privados) e os endereços locais de link IPv6 (semelhante a endereços IP privados automáticos no Windows Server para IPv4)</span><span class="sxs-lookup"><span data-stu-id="5c7f9-132">Typical address types that you will use for IPv6 addressing will be the IPv6 global addresses (similar to public IPv4 addresses), IPv6 unique local addresses (similar to the private IPv4 address ranges) and IPv6 link-local addresses (similar to automatic private IP addresses in Windows Server for IPv4)</span></span>

<span data-ttu-id="5c7f9-133">Há tecnologias de conversão de endereços de rede (NAT) para IPv6 que permitirão o NAT IPv6 para IPv4 (comumente chamado de NAT64) e para IPv6 NAT para IPv6 (geralmente chamado de NAT66).</span><span class="sxs-lookup"><span data-stu-id="5c7f9-133">Network address translation technologies (NAT) for IPv6 exist that will allow for NAT IPv6 to IPv4 (commonly referred to as NAT64) and for NAT IPv6 to IPv6 (commonly referred to as NAT66).</span></span> <span data-ttu-id="5c7f9-134">A existência de tecnologias NAT significa que os cinco cenários apresentados para servidores do Lync Server Edge ainda são válidos.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-134">The existence of NAT technologies means that the five scenarios presented for Lync Server Edge Servers are still valid.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="5c7f9-135">O IPv6 é um tópico complexo e requer planejamento cuidadoso com sua equipe de rede e seu provedor de Internet para garantir que os endereços que você atribuir no nível do Windows Server e no nível do Lync Server 2013 funcionarão conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-135">IPv6 is a complex topic and requires careful planning with your networking team and your Internet provider to ensure that the addresses you assign at the Windows server level and at the Lync Server 2013 level will work as expected.</span></span> <span data-ttu-id="5c7f9-136">Consulte os links no final deste tópico para obter recursos adicionais sobre o endereço IPv6 e planejamento.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-136">See the links at the end of this topic for additional resources on IPv6 addressing and planning.</span></span>



</div>

<span data-ttu-id="5c7f9-137">**Uma única aresta consolidada com topologia de endereços IP públicos**</span><span class="sxs-lookup"><span data-stu-id="5c7f9-137">**Single Consolidated Edge with Public IP Addresses topology**</span></span>

<span data-ttu-id="5c7f9-138">![2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d](images/JJ205148.2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d(OCS.15).jpg "2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d")</span><span class="sxs-lookup"><span data-stu-id="5c7f9-138">![2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d](images/JJ205148.2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d(OCS.15).jpg "2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="5c7f9-139">Se você estiver usando o controle de admissão de chamadas (CAC), ainda deverá atribuir endereços IPv4 à interface interna do servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-139">If you are using Call Admission Control (CAC), you still must assign IPv4 addresses to the Edge Server internal interface.</span></span> <span data-ttu-id="5c7f9-140">O CAC usa endereços IPv4 e deve tê-los disponíveis para operação.</span><span class="sxs-lookup"><span data-stu-id="5c7f9-140">CAC uses IPv4 addresses and must have them available to operate.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5c7f9-141">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5c7f9-141">In This Section</span></span>

  - [<span data-ttu-id="5c7f9-142">Resumo de certificado - Única borda consolidada com endereços IP públicos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c7f9-142">Certificate summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="5c7f9-143">Sumário de porta - única borda consolidada com endereços IP públicos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c7f9-143">Port summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-port-summary-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="5c7f9-144">Resumo de DNS - Única borda consolidada com endereços IP públicos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c7f9-144">DNS summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-dns-summary-single-consolidated-edge-with-public-ip-addresses.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5c7f9-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c7f9-145">See Also</span></span>


[<span data-ttu-id="5c7f9-146">Arquitetura de endereçamento de IP versão 6</span><span class="sxs-lookup"><span data-stu-id="5c7f9-146">IP Version 6 Addressing Architecture</span></span>](https://tools.ietf.org/html/rfc4291)  
[<span data-ttu-id="5c7f9-147">Formato de endereço de difusão ponto a ponto global IPv6</span><span class="sxs-lookup"><span data-stu-id="5c7f9-147">IPv6 Global Unicast Address Format</span></span>](https://tools.ietf.org/html/rfc3587)  
[<span data-ttu-id="5c7f9-148">Endereços exclusivos de unicast IPv6 locais</span><span class="sxs-lookup"><span data-stu-id="5c7f9-148">Unique Local IPv6 Unicast Addresses</span></span>](https://tools.ietf.org/html/rfc4193)  
  

<span data-ttu-id="5c7f9-149"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c7f9-149"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

