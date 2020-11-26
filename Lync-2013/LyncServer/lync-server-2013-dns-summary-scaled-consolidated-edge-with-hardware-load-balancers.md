---
title: Resumo de DNS - borda consolidada em escala com balanceadores de carga de hardware
description: Resumo DNS – borda consolidada dimensionada com balanceadores de carga de hardware.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled consolidated edge with hardware load balancers
ms:assetid: 8453297c-da1d-4b9e-a37e-6721458c6feb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398670(v=OCS.15)
ms:contentKeyID: 48184700
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59581f435267a7db607e03a8cbf52d21f70897f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437697"
---
# <a name="dns-summary---scaled-consolidated-edge-with-hardware-load-balancers-in-lync-server-2013"></a><span data-ttu-id="2aead-103">Resumo de DNS - borda consolidada em escala com balanceadores de carga de hardware no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2aead-103">DNS summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2aead-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2aead-104">

<span> </span></span></span>

<span data-ttu-id="2aead-105">_**Tópico da última modificação:** 2013-01-27_</span><span class="sxs-lookup"><span data-stu-id="2aead-105">_**Topic Last Modified:** 2013-01-27_</span></span>

<span data-ttu-id="2aead-106">Os requisitos de registro de DNS para acesso remoto ao Lync Server 2013 são bem simples em comparação com aqueles para certificados e portas.</span><span class="sxs-lookup"><span data-stu-id="2aead-106">DNS record requirements for remote access to Lync Server 2013 are fairly straightforward compared to those for certificates and ports.</span></span> <span data-ttu-id="2aead-107">Além disso, muitos registros são opcionais, dependendo de como você configura os clientes que executam o Lync 2013 e se você habilita a Federação.</span><span class="sxs-lookup"><span data-stu-id="2aead-107">Also, many records are optional, depending on how you configure clients running Lync 2013 and whether you enable federation.</span></span>

<span data-ttu-id="2aead-108">Para obter detalhes sobre os requisitos de DNS do Lync 2013, consulte [determinar requisitos de DNS para o Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2aead-108">For details about Lync 2013 DNS requirements, see [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="2aead-109">Para obter detalhes sobre como configurar a configuração automática de clientes do Lync 2013 se a divisão do DNS não estiver configurada, consulte a seção "configuração automática sem DNS de Brain" em [determinar requisitos de DNS para o Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2aead-109">For details about configuring automatic configuration of Lync 2013 clients if split-brain DNS is not configured, see the "Automatic Configuration without Split Brain DNS" section in [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="2aead-110">A tabela a seguir contém um resumo dos registros DNS necessários para dar suporte à topologia de borda consolidada redimensionada (balanceamento de carga de hardware) da figura.</span><span class="sxs-lookup"><span data-stu-id="2aead-110">The following table contains a summary of the DNS records that are required to support the Scaled Consolidated Edge Topology (Hardware Load Balanced) figure.</span></span> <span data-ttu-id="2aead-111">Observe que determinados registros DNS são necessários somente para a configuração automática de clientes do Lync.</span><span class="sxs-lookup"><span data-stu-id="2aead-111">Note that certain DNS records are required only for automatic configuration for Lync clients.</span></span> <span data-ttu-id="2aead-112">Se você pretende usar objetos de política de grupo (GPOs) para configurar os clientes do Lync, os registros associados não são necessários.</span><span class="sxs-lookup"><span data-stu-id="2aead-112">If you plan to use group policy objects (GPOs) to configure Lync clients, the associated records are not necessary.</span></span>

<div>

## <a name="important-edge-server-network-adapter-requirements"></a><span data-ttu-id="2aead-113">IMPORTANTE: requisitos do adaptador de rede do Edge Server</span><span class="sxs-lookup"><span data-stu-id="2aead-113">IMPORTANT: Edge Server Network Adapter Requirements</span></span>

<span data-ttu-id="2aead-114">Para evitar problemas de roteamento, verifique se há pelo menos dois adaptadores de rede em seus servidores de borda e se o gateway padrão está definido somente no adaptador de rede associado à interface externa.</span><span class="sxs-lookup"><span data-stu-id="2aead-114">To avoid routing issues, verify that there are at least two network adapters in your Edge Servers and that the default gateway is set only on the network adapter associated with the external interface.</span></span> <span data-ttu-id="2aead-115">Por exemplo, conforme mostrado na figura de cenário de borda consolidada dimensionada na [borda consolidada dimensionada com balanceadores de carga de hardware no Lync Server 2013](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md), o gateway padrão apontaria para o firewall externo.</span><span class="sxs-lookup"><span data-stu-id="2aead-115">For example, as shown in the Scaled Consolidated Edge Scenario figure in [Scaled consolidated edge with hardware load balancers in Lync Server 2013](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md), the default gateway would point to the external firewall.</span></span>

<span data-ttu-id="2aead-116">Você pode configurar dois adaptadores de rede em cada um dos seus servidores de borda da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2aead-116">You can configure two network adapters in each of your Edge Servers as follows:</span></span>

  - <span data-ttu-id="2aead-117">**Adaptador de rede 1 (interface interna)**</span><span class="sxs-lookup"><span data-stu-id="2aead-117">**Network adapter 1 (Internal Interface)**</span></span>
    
    <span data-ttu-id="2aead-118">Interface interna com 172.25.33.10 atribuído.</span><span class="sxs-lookup"><span data-stu-id="2aead-118">Internal interface with 172.25.33.10 assigned.</span></span>
    
    <span data-ttu-id="2aead-119">Nenhum gateway padrão.</span><span class="sxs-lookup"><span data-stu-id="2aead-119">No default gateway.</span></span>
    
    <span data-ttu-id="2aead-120">Verifique se há uma rota da rede que contém a interface interna do servidor de borda para qualquer rede que contenha clientes ou servidores do Lync Server que executam o Lync Server (por exemplo, de 172.25.33.0 para 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="2aead-120">Ensure there is a route from the network containing the Edge Server internal interface to any networks that contain Lync Server clients or servers running Lync Server (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="2aead-121">**Adaptador de rede 2 (interface externa)**</span><span class="sxs-lookup"><span data-stu-id="2aead-121">**Network adapter 2 (External Interface)**</span></span>
    
    <span data-ttu-id="2aead-122">Três endereços IP públicos são atribuídos a esse adaptador de rede, por exemplo, 131.107.155.10 para serviço de borda do Access, 131.107.155.20 para serviço de borda de webconferência, 131.107.155.30 para o serviço de borda A/V.</span><span class="sxs-lookup"><span data-stu-id="2aead-122">Three public IP addresses are assigned to this network adapter, for example 131.107.155.10 for Access Edge service, 131.107.155.20 for Web Conferencing Edge service, 131.107.155.30 for A/V Edge service.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="2aead-123">Os endereços IP atribuídos às interfaces de rede externa reais do servidor de borda podem depender do balanceamento de carga de hardware que você escolher.</span><span class="sxs-lookup"><span data-stu-id="2aead-123">The IP addresses that are assigned to the actual external network interfaces of the Edge Server may depend on which hardware load balancer you choose.</span></span> <span data-ttu-id="2aead-124">Consulte a documentação do balanceador de carga de hardware para compreender os requisitos de endereço IP real.</span><span class="sxs-lookup"><span data-stu-id="2aead-124">Refer to the documentation for your hardware load balancer to understand the actual IP address requirements.</span></span><BR><span data-ttu-id="2aead-125">É possível, mas não recomendado, usar um único endereço IP para todas as três interfaces de serviço de borda.</span><span class="sxs-lookup"><span data-stu-id="2aead-125">It is possible, though not recommended, to use a single IP address for all three Edge service interfaces.</span></span> <span data-ttu-id="2aead-126">Embora isso salve endereços IP, ele exige números de porta diferentes para cada serviço.</span><span class="sxs-lookup"><span data-stu-id="2aead-126">Though this does save IP addresses, it requires different port numbers for each service.</span></span> <span data-ttu-id="2aead-127">O número da porta padrão é 443/TCP, o que garante que os firewalls remotos permitam que o tráfego seja permitido.</span><span class="sxs-lookup"><span data-stu-id="2aead-127">The default port number is 443/TCP, which ensures that most remote firewalls will allow the traffic.</span></span> <span data-ttu-id="2aead-128">Alterar os valores de porta para (por exemplo) 5061/TCP para o serviço de borda de acesso, 444/TCP para o serviço de borda de Webconferência e 443/TCP para o serviço de borda A/V pode causar problemas para usuários remotos nos quais um firewall para os quais estão sendo atrasados não permite o tráfego sobre 5061/TCP e 444/TCP.</span><span class="sxs-lookup"><span data-stu-id="2aead-128">Changing the port values to (for example) 5061/TCP for the Access Edge service, 444/TCP for the Web Conferencing Edge service and 443/TCP for the A/V Edge service might cause problems for remote users where a firewall that they are behind does not allow the traffic over 5061/TCP and 444/TCP.</span></span> <span data-ttu-id="2aead-129">Além disso, três endereços IP distintos facilitam a solução de problemas devido à capacidade de filtrar por endereço IP.</span><span class="sxs-lookup"><span data-stu-id="2aead-129">Additionally, three distinct IP addresses makes troubleshooting easier due to being able to filter on IP address.</span></span>

    
    </div>
    
    <span data-ttu-id="2aead-130">O endereço IP do serviço de borda do Access é primário com o gateway padrão definido como roteador voltado para a Internet (131.107.155.1).</span><span class="sxs-lookup"><span data-stu-id="2aead-130">Access Edge service IP address is primary with default gateway set to Internet-facing router (131.107.155.1).</span></span>
    
    <span data-ttu-id="2aead-131">Serviço de borda de Webconferência e os endereços IP dos serviços de borda A/V secundário.</span><span class="sxs-lookup"><span data-stu-id="2aead-131">Web Conferencing Edge service and A/V Edge service IP addresses secondary.</span></span>

<div>


> [!TIP]
> <span data-ttu-id="2aead-132">A configuração do servidor de borda com dois adaptadores de rede é uma das duas opções.</span><span class="sxs-lookup"><span data-stu-id="2aead-132">Configuring the Edge Server with two network adapters is one of two options.</span></span> <span data-ttu-id="2aead-133">A outra opção é usar um adaptador de rede para o lado interno e três adaptadores de rede para o lado externo do servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="2aead-133">The other option is to use one network adapter for the internal side and three network adapters for the external side of the Edge Server.</span></span> <span data-ttu-id="2aead-134">O principal benefício dessa opção é um adaptador de rede distinto por serviço de servidor de borda e uma coleta de dados possivelmente mais concisa quando a solução de problemas é necessária</span><span class="sxs-lookup"><span data-stu-id="2aead-134">The main benefit of this option is a distinct network adapter per Edge Server service, and potentially more concise data collection when troubleshooting is necessary</span></span>



</div>

### <a name="dns-records-required-for-scaled-consolidated-edge-hardware-load-balanced-example"></a><span data-ttu-id="2aead-135">Registros DNS necessários para borda consolidada dimensionada, balanceamento de carga de hardware (exemplo)</span><span class="sxs-lookup"><span data-stu-id="2aead-135">DNS Records Required for Scaled Consolidated Edge, Hardware Load Balanced (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2aead-136">Local/tipo/porta</span><span class="sxs-lookup"><span data-stu-id="2aead-136">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="2aead-137">Registro FQDN/DNS</span><span class="sxs-lookup"><span data-stu-id="2aead-137">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="2aead-138">Endereço IP/FQDN</span><span class="sxs-lookup"><span data-stu-id="2aead-138">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="2aead-139">Mapas para/comentários</span><span class="sxs-lookup"><span data-stu-id="2aead-139">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2aead-140">DNS/A externo</span><span class="sxs-lookup"><span data-stu-id="2aead-140">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="2aead-141">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="2aead-141">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="2aead-142">131.107.155.10</span><span class="sxs-lookup"><span data-stu-id="2aead-142">131.107.155.10</span></span></p></td>
<td><p><span data-ttu-id="2aead-143">Interface externa do serviço de borda do Access (contoso).</span><span class="sxs-lookup"><span data-stu-id="2aead-143">Access Edge service external interface (Contoso).</span></span> <span data-ttu-id="2aead-144">Repita conforme necessário para todos os domínios SIP com usuários habilitados para Lync</span><span class="sxs-lookup"><span data-stu-id="2aead-144">Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aead-145">DNS/A externo</span><span class="sxs-lookup"><span data-stu-id="2aead-145">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="2aead-146">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="2aead-146">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="2aead-147">131.107.155.20</span><span class="sxs-lookup"><span data-stu-id="2aead-147">131.107.155.20</span></span></p></td>
<td><p><span data-ttu-id="2aead-148">Interface externa do serviço de borda de Webconferência</span><span class="sxs-lookup"><span data-stu-id="2aead-148">Web Conferencing Edge service external interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aead-149">DNS/A externo</span><span class="sxs-lookup"><span data-stu-id="2aead-149">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="2aead-150">av.contoso.com</span><span class="sxs-lookup"><span data-stu-id="2aead-150">av.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="2aead-151">131.107.155.30</span><span class="sxs-lookup"><span data-stu-id="2aead-151">131.107.155.30</span></span></p></td>
<td><p><span data-ttu-id="2aead-152">Interface externa de serviço de borda A/V</span><span class="sxs-lookup"><span data-stu-id="2aead-152">A/V Edge service external interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aead-153">DNS/SRV/443 externos</span><span class="sxs-lookup"><span data-stu-id="2aead-153">External DNS/SRV/443</span></span></p></td>
<td><p><span data-ttu-id="2aead-154">_sip._tls.contoso.com</span><span class="sxs-lookup"><span data-stu-id="2aead-154">_sip._tls.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="2aead-155">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="2aead-155">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="2aead-156">Interface externa do serviço de borda do Access.</span><span class="sxs-lookup"><span data-stu-id="2aead-156">Access Edge service external interface.</span></span> <span data-ttu-id="2aead-157">Obrigatório para configurar automaticamente o Lync 2013 e os clientes do Lync 2010 para trabalhar externamente.</span><span class="sxs-lookup"><span data-stu-id="2aead-157">Required for automatic configuration of Lync 2013 and Lync 2010 clients to work externally.</span></span> <span data-ttu-id="2aead-158">Repita conforme necessário para todos os domínios SIP com usuários habilitados para o Lync.</span><span class="sxs-lookup"><span data-stu-id="2aead-158">Repeat as necessary for all SIP domains with Lync enabled users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2aead-159">DNS/SRV/5061 externo</span><span class="sxs-lookup"><span data-stu-id="2aead-159">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="2aead-160">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="2aead-160">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="2aead-161">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="2aead-161">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="2aead-162">Interface externa do serviço de borda do acesso SIP necessária para descoberta automática de DNS de parceiros federados conhecidos como "domínio SIP permitido" (chamado de Federação aprimorada nas versões anteriores).</span><span class="sxs-lookup"><span data-stu-id="2aead-162">SIP Access Edge service external interface Required for automatic DNS discovery of federated partners known as “Allowed SIP Domain” (called enhanced federation in previous releases).</span></span> <span data-ttu-id="2aead-163">Repita conforme necessário para todos os domínios SIP com usuários habilitados para o Lync e clientes móveis do Microsoft Lync que usam o serviço de notificação por Push ou o serviço de notificação por push da Apple</span><span class="sxs-lookup"><span data-stu-id="2aead-163">Repeat as necessary for all SIP domains with Lync enabled users and Microsoft Lync Mobile clients that use either the Push Notification Service or the Apple Push Notification service</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2aead-164">DNS interno/A</span><span class="sxs-lookup"><span data-stu-id="2aead-164">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="2aead-165">lsedge.contoso.net</span><span class="sxs-lookup"><span data-stu-id="2aead-165">lsedge.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="2aead-166">172.25.33.10</span><span class="sxs-lookup"><span data-stu-id="2aead-166">172.25.33.10</span></span></p></td>
<td><p><span data-ttu-id="2aead-167">Interface interna de borda consolidada</span><span class="sxs-lookup"><span data-stu-id="2aead-167">Consolidated Edge internal interface</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2aead-168">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2aead-168">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

