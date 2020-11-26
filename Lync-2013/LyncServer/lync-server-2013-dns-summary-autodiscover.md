---
title: 'Lync Server 2013: Resumo de DNS-descoberta automática'
description: 'Lync Server 2013: Resumo de DNS-descoberta automática.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Autodiscover
ms:assetid: b336a2ae-0e58-4b74-b606-aedbbd411587
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945644(v=OCS.15)
ms:contentKeyID: 51541504
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eef9bd6a2489561145718c7bbf2f710ab0b1f248
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429039"
---
# <a name="dns-summary---autodiscover-in-lync-server-2013"></a><span data-ttu-id="04a05-103">Resumo de DNS-descoberta automática no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="04a05-103">DNS summary - Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="04a05-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="04a05-104">

<span> </span></span></span>

<span data-ttu-id="04a05-105">_**Tópico da última modificação:** 2013-02-13_</span><span class="sxs-lookup"><span data-stu-id="04a05-105">_**Topic Last Modified:** 2013-02-13_</span></span>

<span data-ttu-id="04a05-106">A descoberta automática é um serviço flexível, pois ele aceitará comunicação via HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="04a05-106">Autodiscover is a flexible service in that it will accept communication over HTTP or HTTPS.</span></span> <span data-ttu-id="04a05-107">Para fazer isso, o sistema de nomes de domínio (DNS) e os certificados usados por servidores que hospedam o serviço de descoberta automática devem ser configurados corretamente.</span><span class="sxs-lookup"><span data-stu-id="04a05-107">To accomplish this, the domain name system (DNS) and the certificates used by servers that host the Autodiscover service must be configured correctly.</span></span> <span data-ttu-id="04a05-108">Os requisitos de certificado são abordados no [Resumo do certificado-descoberta automática no Lync Server 2013](lync-server-2013-certificate-summary-autodiscover.md).</span><span class="sxs-lookup"><span data-stu-id="04a05-108">Certificate requirements are covered in [Certificate summary - Autodiscover in Lync Server 2013](lync-server-2013-certificate-summary-autodiscover.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="04a05-109">A lógica de pesquisa de DNS para os clientes do Lync Server usa uma ordem específica de resolução.</span><span class="sxs-lookup"><span data-stu-id="04a05-109">DNS lookup logic for the Lync Server clients uses a specific order of resolution.</span></span> <span data-ttu-id="04a05-110">Você deve sempre incluir o lyncdiscoverinternal. &lt; domínio &gt; e lyncdiscover. &lt; domínio &gt; no seu DNS.</span><span class="sxs-lookup"><span data-stu-id="04a05-110">You should always include both the lyncdiscoverinternal.&lt;domain&gt; and the lyncdiscover.&lt;domain&gt; in your DNS.</span></span> <span data-ttu-id="04a05-111">Excluindo o lyncdiscoverinternal. &lt; o registro de domínio causará &gt; falha nos clientes internos para se conectar aos serviços pretendidos ou receber a resposta de descoberta automática incorreta.</span><span class="sxs-lookup"><span data-stu-id="04a05-111">Excluding the lyncdiscoverinternal.&lt;domain&gt; record will cause internal clients to fail to connect to the intended services or receive the incorrect Autodiscover response.</span></span>



</div>

### <a name="internal-dns-records"></a><span data-ttu-id="04a05-112">Registros DNS internos</span><span class="sxs-lookup"><span data-stu-id="04a05-112">Internal DNS Records</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04a05-113">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="04a05-113">Record type</span></span></th>
<th><span data-ttu-id="04a05-114">Nome do host</span><span class="sxs-lookup"><span data-stu-id="04a05-114">Host name</span></span></th>
<th><span data-ttu-id="04a05-115">Resolve para</span><span class="sxs-lookup"><span data-stu-id="04a05-115">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04a05-116">CNAME</span><span class="sxs-lookup"><span data-stu-id="04a05-116">CNAME</span></span></p></td>
<td><p><span data-ttu-id="04a05-117">Lyncdiscoverinternal. &lt; nome de domínio interno&gt;</span><span class="sxs-lookup"><span data-stu-id="04a05-117">Lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
<td><p><span data-ttu-id="04a05-118">FQDN de serviços Web internos para seu pool de directors, se você tiver um ou para o seu pool de front-ends se não tiver um director.</span><span class="sxs-lookup"><span data-stu-id="04a05-118">Internal Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04a05-119">A (host, se IPv6, AAAA)</span><span class="sxs-lookup"><span data-stu-id="04a05-119">A (host, if IPv6, AAAA)</span></span></p></td>
<td><p><span data-ttu-id="04a05-120">lyncdiscoverinternal. &lt; nome de domínio interno&gt;</span><span class="sxs-lookup"><span data-stu-id="04a05-120">lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
<td><p><span data-ttu-id="04a05-121">Endereço IP interno dos serviços Web (VIP) se você usar um balanceador de carga de seu pool de directors, se você tiver um ou do seu pool Front-End se não tiver um director.</span><span class="sxs-lookup"><span data-stu-id="04a05-121">Internal Web Services IP address (virtual IP (VIP) address if you use a load balancer) of your Director pool, if you have one, or of your Front End pool if you do not have a Director.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="04a05-122">Você precisa criar um dos seguintes registros de DNS externo:</span><span class="sxs-lookup"><span data-stu-id="04a05-122">You need to create one of the following external DNS records:</span></span>

### <a name="external-dns-records"></a><span data-ttu-id="04a05-123">Registros DNS externos</span><span class="sxs-lookup"><span data-stu-id="04a05-123">External DNS Records</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04a05-124">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="04a05-124">Record type</span></span></th>
<th><span data-ttu-id="04a05-125">Nome do host</span><span class="sxs-lookup"><span data-stu-id="04a05-125">Host name</span></span></th>
<th><span data-ttu-id="04a05-126">Resolve para</span><span class="sxs-lookup"><span data-stu-id="04a05-126">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04a05-127">CNAME</span><span class="sxs-lookup"><span data-stu-id="04a05-127">CNAME</span></span></p></td>
<td><p><span data-ttu-id="04a05-128">lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="04a05-128">lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="04a05-129">FQDN de serviços Web externos para o seu pool de directors, se você tiver um ou para o seu pool de front-end se não tiver um director.</span><span class="sxs-lookup"><span data-stu-id="04a05-129">External Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04a05-130">A (host, se IPv6, AAAA)</span><span class="sxs-lookup"><span data-stu-id="04a05-130">A (host, if IPv6, AAAA)</span></span></p></td>
<td><p><span data-ttu-id="04a05-131">lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="04a05-131">lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="04a05-132">Endereço IP externo ou público do proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="04a05-132">External or public IP address of the reverse proxy.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="04a05-133">O tráfego externo passa pelo proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="04a05-133">External traffic goes through the reverse proxy.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="04a05-134">Os clientes de dispositivos móveis não dão suporte a vários certificados SSL (Secure Sockets Layer) de domínios diferentes.</span><span class="sxs-lookup"><span data-stu-id="04a05-134">Mobile device clients do not support multiple Secure Sockets Layer (SSL) certificates from different domains.</span></span> <span data-ttu-id="04a05-135">Portanto, não há suporte para o redirecionamento CNAME para domínios diferentes em HTTPS.</span><span class="sxs-lookup"><span data-stu-id="04a05-135">Therefore, CNAME redirection to different domains is not supported over HTTPS.</span></span> <span data-ttu-id="04a05-136">Por exemplo, um registro CNAME de DNS para lyncdiscover.contoso.com que redireciona para um endereço de director.contoso.net não é compatível com HTTPS.</span><span class="sxs-lookup"><span data-stu-id="04a05-136">For example, a DNS CNAME record for lyncdiscover.contoso.com that redirects to an address of director.contoso.net is not supported over HTTPS.</span></span> <span data-ttu-id="04a05-137">Em uma topologia como essa, um cliente de dispositivo móvel precisa usar HTTP para a primeira solicitação, para que o redirecionamento CNAME seja resolvido por HTTP.</span><span class="sxs-lookup"><span data-stu-id="04a05-137">In such a topology, a mobile device client needs to use HTTP for the first request, so that the CNAME redirection is resolved over HTTP.</span></span> <span data-ttu-id="04a05-138">Solicitações subsequentes e, em seguida, use HTTPS.</span><span class="sxs-lookup"><span data-stu-id="04a05-138">Subsequent requests then use HTTPS.</span></span> <span data-ttu-id="04a05-139">Para dar suporte a esse cenário, você precisa configurar seu proxy reverso com uma regra de publicação na Web para a porta 80 (HTTP).</span><span class="sxs-lookup"><span data-stu-id="04a05-139">To support this scenario, you need to configure your reverse proxy with a web publishing rule for port 80 (HTTP).</span></span> <span data-ttu-id="04a05-140">Para obter detalhes, consulte "criar uma regra de publicação na Web para a porta 80" em <A href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Configurando o proxy reverso para a mobilidade no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="04a05-140">For details, see "To create a web publishing rule for port 80" in <A href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Configuring the reverse proxy for mobility in Lync Server 2013</A>.</span></span> <span data-ttu-id="04a05-141">O redirecionamento CNAME para o mesmo domínio é compatível com HTTPS.</span><span class="sxs-lookup"><span data-stu-id="04a05-141">CNAME redirection to the same domain is supported over HTTPS.</span></span> <span data-ttu-id="04a05-142">Nesse caso, o certificado do domínio de destino abrange o domínio de origem.</span><span class="sxs-lookup"><span data-stu-id="04a05-142">In this case, the destination domain's certificate covers the originating domain.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="04a05-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="04a05-143">See Also</span></span>


[<span data-ttu-id="04a05-144">Configurando o proxy reverso para mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="04a05-144">Configuring the reverse proxy for mobility in Lync Server 2013</span></span>](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md)  


[<span data-ttu-id="04a05-145">Resumo do certificado-descoberta automática no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="04a05-145">Certificate summary - Autodiscover in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-autodiscover.md)  
  

<span data-ttu-id="04a05-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="04a05-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

