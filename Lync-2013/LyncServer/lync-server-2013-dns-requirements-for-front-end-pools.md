---
title: 'Lync Server 2013: requisitos DNS para pools de Front-End'
description: 'Lync Server 2013: requisitos DNS para pools de Front-End.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pools
ms:assetid: ba28919c-fbbe-4c54-8bf9-2b0cd3fa39c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412910(v=OCS.15)
ms:contentKeyID: 48185228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c0369e82bd8ed2ea63e2156728b41f9942b0148
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429067"
---
# <a name="dns-requirements-for-front-end-pools-in-lync-server-2013"></a><span data-ttu-id="ae81c-103">Requisitos dns para pools de front-end no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae81c-103">DNS requirements for Front End pools in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae81c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae81c-104">

<span> </span></span></span>

<span data-ttu-id="ae81c-105">_**Tópico Última Modificação:** 2012-11-07_</span><span class="sxs-lookup"><span data-stu-id="ae81c-105">_**Topic Last Modified:** 2012-11-07_</span></span>

<span data-ttu-id="ae81c-106">Esta seção descreve os registros DNS (Sistema de Nomes de Domínio) necessários para a implantação de pools de Front-End.</span><span class="sxs-lookup"><span data-stu-id="ae81c-106">This section describes the Domain Name System (DNS) records that are required for deployment of Front End pools.</span></span>

<div>

## <a name="dns-records-for-front-end-pools"></a><span data-ttu-id="ae81c-107">Registros DNS para pools de front-end</span><span class="sxs-lookup"><span data-stu-id="ae81c-107">DNS Records for Front End Pools</span></span>

<span data-ttu-id="ae81c-108">A tabela a seguir especifica os requisitos DNS para uma implantação de pool de Front-End do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ae81c-108">The following table specifies DNS requirements for a Lync Server 2013 Front End pool deployment.</span></span>

### <a name="dns-requirements-for-a-front-end-pool"></a><span data-ttu-id="ae81c-109">Requisitos DNS para um pool de front-end</span><span class="sxs-lookup"><span data-stu-id="ae81c-109">DNS Requirements for a Front End Pool</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae81c-110">Cenário da implantação</span><span class="sxs-lookup"><span data-stu-id="ae81c-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="ae81c-111">Requisitos de DNS</span><span class="sxs-lookup"><span data-stu-id="ae81c-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae81c-112">Pool de front-end com vários Servidores Front-End e um balanceador de carga de hardware (se o balanceamento de carga DNS também é implantado nesse pool)</span><span class="sxs-lookup"><span data-stu-id="ae81c-112">Front End pool with multiple Front End Servers and a hardware load balancer (whether or not DNS load balancing is also deployed on that pool)</span></span></p></td>
<td><p><span data-ttu-id="ae81c-113">Ao usar o balanceamento de carga DNS e um balanceador de carga de hardware, você precisa hospedar registros (A).</span><span class="sxs-lookup"><span data-stu-id="ae81c-113">When using both DNS load balancing and a hardware load balancer, you need to Host (A) records.</span></span> <span data-ttu-id="ae81c-114">Crie um registro A interno que resolva o FQDN (nome de domínio totalmente qualificado) do pool de Front-End para balanceamento de carga DNS.</span><span class="sxs-lookup"><span data-stu-id="ae81c-114">Create an internal A record that resolves the fully qualified domain name (FQDN) of the Front End pool for DNS load balancing.</span></span> <span data-ttu-id="ae81c-115">Crie um registro de host interno (A) para os serviços Web internos para o endereço IP virtual (VIP) do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ae81c-115">Create an internal host (A) record for the internal Web services to the virtual IP (VIP) address of the load balancer.</span></span> <span data-ttu-id="ae81c-116">Você deve usar o nome dos serviços Web internos conforme definido no Construtor de Topologias.</span><span class="sxs-lookup"><span data-stu-id="ae81c-116">You must use the internal Web services name as defined in Topology Builder.</span></span></p>
<p><span data-ttu-id="ae81c-117">Por exemplo, se você usar balanceamento de carga DNS e balanceamento de carga de hardware, terá um registro A para cada Servidor Front-End em um pool para balanceamento de carga DNS e um registro A para os serviços Web internos apontando para o IP virtual do balanceador de carga de hardware:</span><span class="sxs-lookup"><span data-stu-id="ae81c-117">For example, if you use both DNS load balancing and hardware load balancing, you would have an A record for each Front End Server in a pool for DNS load balancing, and an A record for the internal Web services pointing to the virtual IP of the hardware load balancer:</span></span></p>
<ul>
<li><p><span data-ttu-id="ae81c-118">Balanceamento de carga DNS: Pool01.contoso.net IP do pool 10.10.10.5</span><span class="sxs-lookup"><span data-stu-id="ae81c-118">DNS load balancing:   Pool01.contoso.net   IP Address of pool   10.10.10.5</span></span></p>
<div>

> [!WARNING]  
> <span data-ttu-id="ae81c-119">Cada Servidor Front-End também terá um registro A distinto:</span><span class="sxs-lookup"><span data-stu-id="ae81c-119">Each Front End Server will also have a distinct A record:</span></span>


</div>
<ol>
<li><p><span data-ttu-id="ae81c-120">FE01.contoso.net 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="ae81c-120">FE01.contoso.net    10.10.10.1</span></span></p></li>
<li><p><span data-ttu-id="ae81c-121">FE02.contoso.net 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="ae81c-121">FE02.contoso.net    10.10.10.2</span></span></p></li>
<li><p><span data-ttu-id="ae81c-122">FE03.contoso.net 10.10.10.3</span><span class="sxs-lookup"><span data-stu-id="ae81c-122">FE03.contoso.net    10.10.10.3</span></span></p></li>
<li><p><span data-ttu-id="ae81c-123">FE04.contoso.net 10.10.10.4</span><span class="sxs-lookup"><span data-stu-id="ae81c-123">FE04.contoso.net    10.10.10.4</span></span></p></li>
</ol></li>
<li><p><span data-ttu-id="ae81c-124">Balanceamento de carga de hardware: WebInternal.contoso.net IP do HLB VIP 192.168.10.5</span><span class="sxs-lookup"><span data-stu-id="ae81c-124">Hardware load balancing:   WebInternal.contoso.net   IP Address of HLB VIP   192.168.10.5</span></span></p></li>
</ul>
<p><span data-ttu-id="ae81c-125">Todo o tráfego, exceto o tráfego HTTP/HTTPS, usará o Pool01.contoso.net registro.</span><span class="sxs-lookup"><span data-stu-id="ae81c-125">All traffic except for HTTP/HTTPS traffic will use the Pool01.contoso.net record.</span></span> <span data-ttu-id="ae81c-126">O tráfego HTTP/HTTPS usará o endereço de serviços Web interno definido de 192.168.10.5</span><span class="sxs-lookup"><span data-stu-id="ae81c-126">HTTP/HTTPS traffic will use the defined internal Web services address of 192.168.10.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae81c-127">Pool de front-end com balanceamento de carga DNS implantado</span><span class="sxs-lookup"><span data-stu-id="ae81c-127">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="ae81c-128">Um conjunto de registros A internos que resolvem o FQDN do pool para o endereço IP de cada servidor no pool.</span><span class="sxs-lookup"><span data-stu-id="ae81c-128">A set of internal A records that resolve the FQDN of the pool to the IP address of each server in the pool.</span></span> <span data-ttu-id="ae81c-129">Deve haver um registro A para cada servidor no pool.</span><span class="sxs-lookup"><span data-stu-id="ae81c-129">There must one A record for each server in the pool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae81c-130">Pool de front-end com balanceamento de carga DNS implantado</span><span class="sxs-lookup"><span data-stu-id="ae81c-130">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="ae81c-131">Um conjunto de registros A internos que resolvem o FQDN de cada servidor no pool para o endereço IP desse servidor.</span><span class="sxs-lookup"><span data-stu-id="ae81c-131">A set of internal A records that resolve the FQDN of each server in the pool to the IP address of that server.</span></span> <span data-ttu-id="ae81c-132">Para obter detalhes, <a href="lync-server-2013-dns-load-balancing.md">consulte Balanceamento de carga DNS no Lync Server 2013</a> na documentação planejamento.</span><span class="sxs-lookup"><span data-stu-id="ae81c-132">For details, see <a href="lync-server-2013-dns-load-balancing.md">DNS load balancing in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae81c-133">Pool de Front-End com um único Servidor Front-End e um banco de dados back-end dedicado, mas nenhum balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="ae81c-133">Front End pool with a single Front End Server and a dedicated back-end database but no load balancer</span></span></p></td>
<td><p><span data-ttu-id="ae81c-134">Um registro A interno que resolve o FQDN do pool de Front-End para o endereço IP do único Servidor Front-End enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="ae81c-134">An internal A record that resolves the FQDN of the Front End pool to the IP address of the single Enterprise Edition Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae81c-135">Entrada automática do cliente</span><span class="sxs-lookup"><span data-stu-id="ae81c-135">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="ae81c-136">Para cada domínio SIP com suporte, um registro SRV para _sipinternaltls._tcp. &lt; domínio sobre a porta 5061 que mapeia para o &gt; FQDN do pool de Front-End que autentica e redireciona solicitações de cliente para entrada.</span><span class="sxs-lookup"><span data-stu-id="ae81c-136">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Front End pool that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="ae81c-137">Para obter detalhes, consulte REQUISITOS DNS para entrada automática do <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">cliente no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="ae81c-137">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae81c-138">Descoberta do serviço Web de Atualização de Dispositivo por dispositivos UC (Comunicações Unificadas)</span><span class="sxs-lookup"><span data-stu-id="ae81c-138">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="ae81c-139">Um registro A interno com o nome ucupdates-r2. &lt; Domínio SIP &gt; que resolve para o endereço IP do pool de Front-End que hospeda o serviço Web de Atualização de Dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae81c-139">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Front End pool that hosts the Device Update Web service.</span></span> <span data-ttu-id="ae81c-140">Na situação em que um dispositivo UC está ligado, mas um usuário nunca fez logons no dispositivo, o registro A permite que o dispositivo descubra o pool de Front-End que hospeda o serviço Web de Atualização de Dispositivo e obtenha atualizações.</span><span class="sxs-lookup"><span data-stu-id="ae81c-140">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the Front End pool hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="ae81c-141">Caso contrário, os dispositivos obterão essas informações, embora o provisionamento em banda na primeira vez em que um usuário faz logona.</span><span class="sxs-lookup"><span data-stu-id="ae81c-141">Otherwise, devices obtain this information though in-band provisioning the first time a user logs in.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="ae81c-142">Se você tiver uma implantação existente do serviço Web de Atualização de Dispositivo no Lync Server 2010, já criou um registro A interno com o nome ucupdates. &lt; Domínio SIP &gt; .</span><span class="sxs-lookup"><span data-stu-id="ae81c-142">If you have an existing deployment of Device Update Web service in Lync Server 2010, you have already created an internal A record with the name ucupdates.&lt;SIP domain&gt;.</span></span> <span data-ttu-id="ae81c-143">Para Microsoft Office Communications Server 2007 R2, você deve criar um registro DNS A adicional com o nome ucupdates-r2. &lt; Domínio SIP &gt; .</span><span class="sxs-lookup"><span data-stu-id="ae81c-143">For Microsoft Office Communications Server 2007 R2, you must create an additional DNS A record with the name ucupdates-r2.&lt;SIP domain&gt;.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae81c-144">Um proxy reverso para dar suporte ao tráfego HTTP</span><span class="sxs-lookup"><span data-stu-id="ae81c-144">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="ae81c-145">Um registro A externo que resolve o FQDN do farm web externo para o endereço IP externo do proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="ae81c-145">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="ae81c-146">Os clientes e dispositivos UC usam esse registro para se conectar ao proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="ae81c-146">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="ae81c-147">Para obter detalhes, <a href="lync-server-2013-determine-dns-requirements.md">consulte Determine DNS requirements for Lync Server 2013</a> na documentação planejamento.</span><span class="sxs-lookup"><span data-stu-id="ae81c-147">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ae81c-148">A tabela a seguir mostra um exemplo dos registros DNS necessários para o FQDN do farm web interno.</span><span class="sxs-lookup"><span data-stu-id="ae81c-148">The following table shows an example of the DNS records required for the internal web farm FQDN.</span></span>

### <a name="example-dns-records-for-internal-web-farm-fqdn"></a><span data-ttu-id="ae81c-149">Exemplo de registros DNS para FQDN do Farm Web Interno</span><span class="sxs-lookup"><span data-stu-id="ae81c-149">Example DNS Records for Internal Web Farm FQDN</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae81c-150">FQDN do farm web interno</span><span class="sxs-lookup"><span data-stu-id="ae81c-150">Internal web farm FQDN</span></span></th>
<th><span data-ttu-id="ae81c-151">FQDN do pool</span><span class="sxs-lookup"><span data-stu-id="ae81c-151">Pool FQDN</span></span></th>
<th><span data-ttu-id="ae81c-152">Registros DNS A( s)</span><span class="sxs-lookup"><span data-stu-id="ae81c-152">DNS A record(s)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae81c-153">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ae81c-153">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ae81c-154">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ae81c-154">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ae81c-155">Registro DNS A para o ee-pool.contoso.com que resolve para o endereço VIP do balanceador de carga usado pelos Servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="ae81c-155">DNS A record for the ee-pool.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p>
<p><span data-ttu-id="ae81c-156">Registro DNS A para webcon.contoso.com que é resolvido para o endereço VIP do balanceador de carga usado pelos Servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="ae81c-156">DNS A record for webcon.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae81c-157">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ae81c-157">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ae81c-158">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ae81c-158">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ae81c-159">Registro DNS A para ee-pool.contoso.com que resolve para o endereço IP virtual (VIP) do balanceador de carga usado pelos Servidores Front-End Enterprise Edition no pool de Front-End.</span><span class="sxs-lookup"><span data-stu-id="ae81c-159">DNS A record for ee-pool.contoso.com that resolves to the virtual IP (VIP) address of the load balancer used by the Enterprise Edition Front End Servers in the Front End pool.</span></span></p>
<p><span data-ttu-id="ae81c-160">Observe que, se você estiver usando o balanceamento de carga DNS neste pool, o pool de Front-End e o farm web interno não poderão ter o mesmo FQDN.</span><span class="sxs-lookup"><span data-stu-id="ae81c-160">Note that if you are using DNS load balancing on this pool, your Front End pool and internal web farm cannot have the same FQDN.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ae81c-161">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae81c-161">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

