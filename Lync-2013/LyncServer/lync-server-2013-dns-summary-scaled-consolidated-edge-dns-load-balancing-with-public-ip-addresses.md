---
title: 'Lync Server 2013: Resumo de DNS - Borda consolidada em escala, balanceamento de carga de DNS com endereços IP públicos'
description: 'Lync Server 2013: Resumo de DNS-margem consolidada dimensionada, balanceamento de carga de DNS com endereços IP públicos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled consolidated edge, DNS load balancing with public IP addresses
ms:assetid: dc8f096a-a0a4-4f71-8930-88ff8fc089d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205319(v=OCS.15)
ms:contentKeyID: 48185594
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ca88043b76365508ea00ca840e9a9fdcb0e270be
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429011"
---
# <a name="dns-summary---scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="a102a-103">Resumo de DNS - Borda consolidada em escala, balanceamento de carga de DNS com endereços IP públicos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a102a-103">DNS summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a102a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a102a-104">

<span> </span></span></span>

<span data-ttu-id="a102a-105">_**Tópico da última modificação:** 2017-03-09_</span><span class="sxs-lookup"><span data-stu-id="a102a-105">_**Topic Last Modified:** 2017-03-09_</span></span>

<span data-ttu-id="a102a-106">Os requisitos de registro de DNS para acesso remoto ao Lync Server 2013 são bem simples em comparação com aqueles para certificados e portas.</span><span class="sxs-lookup"><span data-stu-id="a102a-106">DNS record requirements for remote access to Lync Server 2013 are fairly straightforward compared to those for certificates and ports.</span></span> <span data-ttu-id="a102a-107">Além disso, muitos registros são opcionais, dependendo de como você configura os clientes que executam o Lync 2013 e se você habilita a Federação.</span><span class="sxs-lookup"><span data-stu-id="a102a-107">Also, many records are optional, depending on how you configure clients running Lync 2013 and whether you enable federation.</span></span>

<span data-ttu-id="a102a-108">Para obter detalhes sobre os requisitos de DNS do Lync 2013, consulte [determinar requisitos de DNS para o Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a102a-108">For details about Lync 2013 DNS requirements, see [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="a102a-109">Para obter detalhes sobre como configurar a configuração automática de clientes do Lync 2013 se a divisão do DNS não estiver configurada, consulte a seção "configuração automática sem DNS de Brain" em [determinar requisitos de DNS para o Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a102a-109">For details about configuring automatic configuration of Lync 2013 clients if split-brain DNS is not configured, see the "Automatic Configuration without Split Brain DNS" section in [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="a102a-110">A tabela a seguir contém um resumo dos registros DNS necessários para dar suporte à topologia de borda consolidada única mostrada na figura única de topologia de borda consolidada.</span><span class="sxs-lookup"><span data-stu-id="a102a-110">The following table contains a summary of the DNS records that are required to support the single consolidated edge topology shown in the Single Consolidated Edge Topology figure.</span></span> <span data-ttu-id="a102a-111">Observe que determinados registros DNS são necessários somente para a configuração automática de clientes do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="a102a-111">Note that certain DNS records are required only for automatic configuration of Lync 2013 clients.</span></span> <span data-ttu-id="a102a-112">Se você pretende usar objetos de política de grupo (GPOs) para configurar os clientes do Lync, os registros associados não são necessários.</span><span class="sxs-lookup"><span data-stu-id="a102a-112">If you plan to use group policy objects (GPOs) to configure Lync clients, the associated records are not necessary.</span></span>

<div>

## <a name="important-edge-server-network-adapter-requirements"></a><span data-ttu-id="a102a-113">IMPORTANTE: requisitos do adaptador de rede do Edge Server</span><span class="sxs-lookup"><span data-stu-id="a102a-113">IMPORTANT: Edge Server Network Adapter Requirements</span></span>

<span data-ttu-id="a102a-114">Para evitar problemas de roteamento, verifique se há pelo menos dois adaptadores de rede em seus servidores de borda e se o gateway padrão está definido somente no adaptador de rede associado à interface externa.</span><span class="sxs-lookup"><span data-stu-id="a102a-114">To avoid routing issues, verify that there are at least two network adapters in your Edge Servers and that the default gateway is set only on the network adapter associated with the external interface.</span></span> <span data-ttu-id="a102a-115">Por exemplo, conforme mostrado na figura de cenário de borda consolidada dimensionada na [borda consolidada dimensionada, o balanceamento de carga de DNS com endereços IP públicos no Lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md) , o gateway padrão apontaria para o firewall externo.</span><span class="sxs-lookup"><span data-stu-id="a102a-115">For example, as shown in the Scaled Consolidated Edge Scenario figure in [Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md) , the default gateway would point to the external firewall.</span></span>

<span data-ttu-id="a102a-116">Você pode configurar dois adaptadores de rede em cada um dos seus servidores de borda da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a102a-116">You can configure two network adapters in each of your Edge Server as follows:</span></span>

  - <span data-ttu-id="a102a-117">**Adaptador de rede 1-nó 1 (interface interna)**</span><span class="sxs-lookup"><span data-stu-id="a102a-117">**Network adapter 1 - Node 1 (Internal Interface)**</span></span>
    
    <span data-ttu-id="a102a-118">Interface interna com 172.25.33.10 atribuído.</span><span class="sxs-lookup"><span data-stu-id="a102a-118">Internal interface with 172.25.33.10 assigned.</span></span>
    
    <span data-ttu-id="a102a-119">Não há nenhum gateway padrão definido.</span><span class="sxs-lookup"><span data-stu-id="a102a-119">No default gateway is defined.</span></span>
    
    <span data-ttu-id="a102a-120">Verifique se há uma rota da rede que contém a interface interna de borda para qualquer rede que contenha servidores que estejam executando o Lync Server 2013 ou o Lync Server 2013 clientes (por exemplo, de 172.25.33.0 para 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="a102a-120">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="a102a-121">**Adaptador de rede 1-nó 2 (interface interna)**</span><span class="sxs-lookup"><span data-stu-id="a102a-121">**Network adapter 1 - Node 2 (Internal Interface)**</span></span>
    
    <span data-ttu-id="a102a-122">Interface interna com 172.25.33.11 atribuído.</span><span class="sxs-lookup"><span data-stu-id="a102a-122">Internal interface with 172.25.33.11 assigned.</span></span>
    
    <span data-ttu-id="a102a-123">Não há nenhum gateway padrão definido.</span><span class="sxs-lookup"><span data-stu-id="a102a-123">No default gateway is defined.</span></span>
    
    <span data-ttu-id="a102a-124">Verifique se há uma rota da rede que contém a interface interna de borda para qualquer rede que contenha servidores que estejam executando o Lync Server 2013 ou o Lync Server 2013 clientes (por exemplo, de 172.25.33.0 para 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="a102a-124">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="a102a-125">**Adaptador de rede 2 nó 1 (interface externa)**</span><span class="sxs-lookup"><span data-stu-id="a102a-125">**Network adapter 2 Node 1 (External Interface)**</span></span>
    
    <span data-ttu-id="a102a-126">Três endereços IP privados são atribuídos a esse adaptador de rede, por exemplo, 131.107.155.10 para serviço de borda de acesso, 131.107.155.20 para serviço de borda de webconferência, 131.107.155.30 para o serviço de borda A/V.</span><span class="sxs-lookup"><span data-stu-id="a102a-126">Three private IP addresses are assigned to this network adapter, for example 131.107.155.10 for Access Edge service, 131.107.155.20 for Web Conferencing Edge service, 131.107.155.30 for A/V Edge service.</span></span>
    
    <span data-ttu-id="a102a-127">O endereço IP público do serviço de borda do Access é primário com o gateway padrão definido para o roteador público (131.107.155.1).</span><span class="sxs-lookup"><span data-stu-id="a102a-127">The Access Edge service public IP address is primary with default gateway set to the public router (131.107.155.1).</span></span>
    
    <span data-ttu-id="a102a-128">O serviço de borda de Webconferência e os endereços IP privados do serviço de borda a/V são endereços IP adicionais na seção **avançado** das propriedades de **protocolo de Internet versão 4 (TCP/IPv4)** e **protocolo IP versão 6 (TCP/IPv6)** das **Propriedades de conexão de área local** no Windows Server.</span><span class="sxs-lookup"><span data-stu-id="a102a-128">Web Conferencing Edge service and A/V Edge service private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a102a-129">É possível, mas não recomendado, usar um único endereço IP para todas as três interfaces de serviço de borda.</span><span class="sxs-lookup"><span data-stu-id="a102a-129">It is possible, though not recommended, to use a single IP address for all three Edge service interfaces.</span></span> <span data-ttu-id="a102a-130">Embora isso salve endereços IP, ele exige números de porta diferentes para cada serviço.</span><span class="sxs-lookup"><span data-stu-id="a102a-130">Though this does save IP addresses, it requires different port numbers for each service.</span></span> <span data-ttu-id="a102a-131">O número da porta padrão é 443/TCP, o que garante que os firewalls remotos permitam que o tráfego seja permitido.</span><span class="sxs-lookup"><span data-stu-id="a102a-131">The default port number is 443/TCP, which ensures that most remote firewalls will allow the traffic.</span></span> <span data-ttu-id="a102a-132">Alterar os valores de porta para (por exemplo) 5061/TCP para o serviço de borda de acesso, 444/TCP para o serviço de borda de Webconferência e 443/TCP para o serviço de borda A/V pode causar problemas para usuários remotos nos quais um firewall para os quais estão sendo atrasados não permite o tráfego sobre 5061/TCP e 444/TCP.</span><span class="sxs-lookup"><span data-stu-id="a102a-132">Changing the port values to (for example) 5061/TCP for the Access Edge service, 444/TCP for the Web Conferencing Edge service and 443/TCP for the A/V Edge service might cause problems for remote users where a firewall that they are behind does not allow the traffic over 5061/TCP and 444/TCP.</span></span> <span data-ttu-id="a102a-133">Além disso, três endereços IP distintos facilitam a solução de problemas devido à capacidade de filtrar por endereço IP.</span><span class="sxs-lookup"><span data-stu-id="a102a-133">Additionally, three distinct IP addresses makes troubleshooting easier due to being able to filter on IP address.</span></span>

    
    </div>

  - <span data-ttu-id="a102a-134">**Adaptador de rede 2 nó 2 (interface externa)**</span><span class="sxs-lookup"><span data-stu-id="a102a-134">**Network adapter 2 Node 2 (External Interface)**</span></span>
    
    <span data-ttu-id="a102a-135">Três endereços IP privados são atribuídos a esse adaptador de rede, por exemplo, 131.107.155.11 para serviço de borda de acesso, 131.107.155.21 para serviço de borda de webconferência, 131.107.155.31 para o serviço de borda A/V.</span><span class="sxs-lookup"><span data-stu-id="a102a-135">Three private IP addresses are assigned to this network adapter, for example 131.107.155.11 for Access Edge service, 131.107.155.21 for Web Conferencing Edge service, 131.107.155.31 for A/V Edge service.</span></span>
    
    <span data-ttu-id="a102a-136">O endereço IP público do serviço de borda do Access é primário com o gateway padrão definido para o roteador público (131.107.155.1).</span><span class="sxs-lookup"><span data-stu-id="a102a-136">The Access Edge service public IP address is primary with default gateway set to the public router (131.107.155.1).</span></span>
    
    <span data-ttu-id="a102a-137">O serviço de borda de Webconferência e os endereços IP privados do serviço de borda a/V são endereços IP adicionais na seção **avançado** das propriedades de **protocolo de Internet versão 4 (TCP/IPv4)** e **protocolo IP versão 6 (TCP/IPv6)** das **Propriedades de conexão de área local** no Windows Server.</span><span class="sxs-lookup"><span data-stu-id="a102a-137">Web Conferencing Edge service and A/V Edge service private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="a102a-138">A configuração do servidor de borda com dois adaptadores de rede é uma das duas opções.</span><span class="sxs-lookup"><span data-stu-id="a102a-138">Configuring the Edge Server with two network adapters is one of two options.</span></span> <span data-ttu-id="a102a-139">A outra opção é usar um adaptador de rede para o lado interno e três adaptadores de rede para o lado externo do servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="a102a-139">The other option is to use one network adapter for the internal side and three network adapters for the external side of the Edge Server.</span></span> <span data-ttu-id="a102a-140">O principal benefício dessa opção é um adaptador de rede distinto por serviço de servidor de borda e uma coleta de dados possivelmente mais concisa quando a solução de problemas é necessária</span><span class="sxs-lookup"><span data-stu-id="a102a-140">The main benefit of this option is a distinct network adapter per Edge Server service, and potentially more concise data collection when troubleshooting is necessary</span></span>



</div>

### <a name="dns-records-required-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-example"></a><span data-ttu-id="a102a-141">Registros DNS necessários para borda consolidada dimensionada, balanceamento de carga de DNS com endereços IP públicos (exemplo)</span><span class="sxs-lookup"><span data-stu-id="a102a-141">DNS Records Required for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a102a-142">Local/tipo/porta</span><span class="sxs-lookup"><span data-stu-id="a102a-142">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="a102a-143">Registro FQDN/DNS</span><span class="sxs-lookup"><span data-stu-id="a102a-143">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="a102a-144">Endereço IP/FQDN</span><span class="sxs-lookup"><span data-stu-id="a102a-144">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="a102a-145">Mapas para/comentários</span><span class="sxs-lookup"><span data-stu-id="a102a-145">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a102a-146">DNS/A externo</span><span class="sxs-lookup"><span data-stu-id="a102a-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="a102a-147">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a102a-147">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a102a-148">131.107.155.10 e 131.107.155.11</span><span class="sxs-lookup"><span data-stu-id="a102a-148">131.107.155.10 and 131.107.155.11</span></span></p></td>
<td><p><span data-ttu-id="a102a-149">Interface externa do Access Edge Service (contoso) Repita conforme necessário para todos os domínios SIP com usuários habilitados para Lync</span><span class="sxs-lookup"><span data-stu-id="a102a-149">Access Edge service external interface (Contoso) Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a102a-150">DNS/A externo</span><span class="sxs-lookup"><span data-stu-id="a102a-150">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="a102a-151">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a102a-151">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a102a-152">131.107.155.20 e 131.107.155.21</span><span class="sxs-lookup"><span data-stu-id="a102a-152">131.107.155.20 and 131.107.155.21</span></span></p></td>
<td><p><span data-ttu-id="a102a-153">Interface externa do serviço de borda de Webconferência</span><span class="sxs-lookup"><span data-stu-id="a102a-153">Web Conferencing Edge service external interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a102a-154">DNS/A externo</span><span class="sxs-lookup"><span data-stu-id="a102a-154">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="a102a-155">av.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a102a-155">av.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a102a-156">131.107.155.30 e 131.107.155.31</span><span class="sxs-lookup"><span data-stu-id="a102a-156">131.107.155.30 and 131.107.155.31</span></span></p></td>
<td><p><span data-ttu-id="a102a-157">Interface externa de serviço de borda A/V</span><span class="sxs-lookup"><span data-stu-id="a102a-157">A/V Edge service external interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a102a-158">DNS/SRV/443 externos</span><span class="sxs-lookup"><span data-stu-id="a102a-158">External DNS/SRV/443</span></span></p></td>
<td><p><span data-ttu-id="a102a-159">_sip._tls.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a102a-159">_sip._tls.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a102a-160">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a102a-160">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a102a-161">Interface externa do serviço de borda do Access.</span><span class="sxs-lookup"><span data-stu-id="a102a-161">Access Edge service external interface.</span></span> <span data-ttu-id="a102a-162">Obrigatório para configurar automaticamente o Lync 2013 e os clientes do Lync 2010 para trabalhar externamente.</span><span class="sxs-lookup"><span data-stu-id="a102a-162">Required for automatic configuration of Lync 2013 and Lync 2010 clients to work externally.</span></span> <span data-ttu-id="a102a-163">Repita conforme necessário para todos os domínios SIP com usuários habilitados para o Lync.</span><span class="sxs-lookup"><span data-stu-id="a102a-163">Repeat as necessary for all SIP domains with Lync enabled users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a102a-164">DNS/SRV/5061 externo</span><span class="sxs-lookup"><span data-stu-id="a102a-164">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="a102a-165">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a102a-165">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a102a-166">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a102a-166">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a102a-167">Interface externa do serviço de borda do Access necessária para descoberta automática de DNS de parceiros federados conhecidos como "domínio SIP permitido" (chamado de Federação aprimorada nas versões anteriores).</span><span class="sxs-lookup"><span data-stu-id="a102a-167">Access Edge service external interface Required for automatic DNS discovery of federated partners known as “Allowed SIP Domain” (called enhanced federation in previous releases).</span></span> <span data-ttu-id="a102a-168">Repita conforme necessário para todos os domínios SIP com usuários habilitados para Lync</span><span class="sxs-lookup"><span data-stu-id="a102a-168">Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a102a-169">DNS interno/A</span><span class="sxs-lookup"><span data-stu-id="a102a-169">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="a102a-170">lsedge.contoso.net</span><span class="sxs-lookup"><span data-stu-id="a102a-170">lsedge.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="a102a-171">172.25.33.10 e 172.25.33.11</span><span class="sxs-lookup"><span data-stu-id="a102a-171">172.25.33.10 and 172.25.33.11</span></span></p></td>
<td><p><span data-ttu-id="a102a-172">Interface interna de borda consolidada</span><span class="sxs-lookup"><span data-stu-id="a102a-172">Consolidated Edge internal interface</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="records-required-for-federation"></a><span data-ttu-id="a102a-173">Registros necessários para Federação</span><span class="sxs-lookup"><span data-stu-id="a102a-173">Records Required for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a102a-174">Local/tipo/porta</span><span class="sxs-lookup"><span data-stu-id="a102a-174">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="a102a-175">FQDN</span><span class="sxs-lookup"><span data-stu-id="a102a-175">FQDN</span></span></th>
<th><span data-ttu-id="a102a-176">Endereço IP/registro de host FQDN</span><span class="sxs-lookup"><span data-stu-id="a102a-176">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="a102a-177">Mapas para/comentários</span><span class="sxs-lookup"><span data-stu-id="a102a-177">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a102a-178">DNS/SRV/5061 externo</span><span class="sxs-lookup"><span data-stu-id="a102a-178">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="a102a-179">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a102a-179">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a102a-180">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a102a-180">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a102a-181">Interface externa do serviço de borda do acesso SIP necessária para a descoberta automática de DNS da sua Federação para outros parceiros de Federação potenciais e é conhecida como "domínios SIP permitidos" (chamado de Federação aprimorada nas versões anteriores).</span><span class="sxs-lookup"><span data-stu-id="a102a-181">SIP Access Edge service external interface Required for automatic DNS discovery of your federation to other potential federation partners, and is known as “Allowed SIP Domains” (called enhanced federation in previous releases).</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="a102a-182">Repita conforme necessário para todos os domínios SIP com usuários habilitados para o Lync e clientes móveis do Microsoft Lync que usam o serviço de notificação por Push ou o serviço de notificação por push da Apple</span><span class="sxs-lookup"><span data-stu-id="a102a-182">Repeat as necessary for all SIP domains with Lync enabled users and Microsoft Lync Mobile clients that use either the Push Notification Service or the Apple Push Notification service</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="a102a-183">Resumo de DNS para o protocolo de mensagens extensíveis e de presença</span><span class="sxs-lookup"><span data-stu-id="a102a-183">DNS Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a102a-184">Local/tipo/porta</span><span class="sxs-lookup"><span data-stu-id="a102a-184">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="a102a-185">FQDN</span><span class="sxs-lookup"><span data-stu-id="a102a-185">FQDN</span></span></th>
<th><span data-ttu-id="a102a-186">Endereço IP/registro de host FQDN</span><span class="sxs-lookup"><span data-stu-id="a102a-186">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="a102a-187">Mapas para/comentários</span><span class="sxs-lookup"><span data-stu-id="a102a-187">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a102a-188">DNS/SRV/5269 externo</span><span class="sxs-lookup"><span data-stu-id="a102a-188">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="a102a-189">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a102a-189">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a102a-190">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a102a-190">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a102a-191">Interface externa de proxy XMPP no serviço de borda do Access ou no pool de bordas. Repita conforme necessário para todos os domínios SIP internos com usuários habilitados para Lync nos quais o contato com contatos do XMPP é permitido pela configuração da política de acesso externo por meio de uma política global, política de site onde o usuário está localizado ou política de usuário aplicada ao usuário habilitado para Lync.</span><span class="sxs-lookup"><span data-stu-id="a102a-191">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="a102a-192">Um domínio XMPP permitido também deve ser configurado na política de parceiros federados do XMPP.</span><span class="sxs-lookup"><span data-stu-id="a102a-192">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="a102a-193">Consulte os tópicos em <strong>Consulte também</strong> para obter detalhes adicionais</span><span class="sxs-lookup"><span data-stu-id="a102a-193">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a102a-194">DNS/A externo</span><span class="sxs-lookup"><span data-stu-id="a102a-194">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="a102a-195">xmpp.contoso.com (por exemplo)</span><span class="sxs-lookup"><span data-stu-id="a102a-195">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="a102a-196">Endereço IP do serviço de borda de acesso em seu servidor de borda ou em um pool de bordas que hospeda o proxy XMPP</span><span class="sxs-lookup"><span data-stu-id="a102a-196">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="a102a-197">Aponta para o serviço de borda de acesso ou o pool de bordas que hospeda o serviço de proxy XMPP.</span><span class="sxs-lookup"><span data-stu-id="a102a-197">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="a102a-198">Geralmente, o registro SRV que você cria aponta para esse registro de host (A ou AAAA)</span><span class="sxs-lookup"><span data-stu-id="a102a-198">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a102a-199">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a102a-199">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

