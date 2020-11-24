---
title: 'Lync Server 2013: Determinar requisitios de DNS'
description: 'Lync Server 2013: determinar requisitos de DNS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Determine DNS requirements
ms:assetid: 95777017-6282-44c0-a685-f246af0501b4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398758(v=OCS.15)
ms:contentKeyID: 48184839
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0a4bfe682314fa4f91826f4bf85f8eac36ea91d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390308"
---
# <a name="determine-dns-requirements-for-lync-server-2013"></a><span data-ttu-id="c858e-103">Determinar requisitios de DNS para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c858e-103">Determine DNS requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c858e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c858e-104">

<span> </span></span></span>

<span data-ttu-id="c858e-105">_**Tópico da última modificação:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="c858e-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="c858e-106">Use o fluxograma a seguir para determinar os requisitos do sistema de nomes de domínio (DNS).</span><span class="sxs-lookup"><span data-stu-id="c858e-106">Use the following flow chart to determine Domain Name System (DNS) requirements.</span></span> <span data-ttu-id="c858e-107">Alterações nas atualizações cumulativas do Lync Server 2013:2013 de fevereiro são observadas quando elas se aplicam.</span><span class="sxs-lookup"><span data-stu-id="c858e-107">Changes for the Cumulative Updates for Lync Server 2013: February 2013 are noted where they apply.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c858e-108">O Microsoft Lync Server 2013 oferece suporte ao uso de endereçamento IPv6.</span><span class="sxs-lookup"><span data-stu-id="c858e-108">Microsoft Lync Server 2013 supports the use of IPv6 addressing.</span></span> <span data-ttu-id="c858e-109">Para usar endereços IPv6, você também deve fornecer suporte para o DNS do IPv6 e configurar o host de DNS AAAA (conhecido como registros "quad-A").</span><span class="sxs-lookup"><span data-stu-id="c858e-109">To use IPv6 addresses, you must also provide support for IPv6 DNS and configure DNS host AAAA (known as “quad-A”) records.</span></span> <span data-ttu-id="c858e-110">Em implantações em que o IPv4 e o IPv6 estão sendo usados, é melhor configurar e manter registros de host A para IPv4 e host AAAA para IPv6.</span><span class="sxs-lookup"><span data-stu-id="c858e-110">In deployments where both IPv4 and IPv6 are being used, it is best to configure and maintain both host A records for IPv4 and host AAAA for IPv6.</span></span> <span data-ttu-id="c858e-111">Mesmo que sua implantação tenha sido completada completamente para IPv6, os registros de host DNS IPv4 ainda poderão ser necessários quando usuários externos ainda estiverem usando IPv4.</span><span class="sxs-lookup"><span data-stu-id="c858e-111">Even if your deployment has transitioned fully to IPv6, IPv4 DNS host records may still be required when external users are still using IPv4.</span></span>



</div>

<span data-ttu-id="c858e-112">**Determinando o fluxograma de requisitos de DNS**</span><span class="sxs-lookup"><span data-stu-id="c858e-112">**Determining DNS Requirements Flow Chart**</span></span>

<span data-ttu-id="c858e-113">![175782ac-363e-408a-912f-8991bf152970](images/Gg398758.175782ac-363e-408a-912f-8991bf152970(OCS.15).jpg "175782ac-363e-408a-912f-8991bf152970")</span><span class="sxs-lookup"><span data-stu-id="c858e-113">![175782ac-363e-408a-912f-8991bf152970](images/Gg398758.175782ac-363e-408a-912f-8991bf152970(OCS.15).jpg "175782ac-363e-408a-912f-8991bf152970")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c858e-114">Por padrão, o nome do computador de um computador que não está associado a um domínio é um nome de host, e não um FQDN (nome de domínio totalmente qualificado).</span><span class="sxs-lookup"><span data-stu-id="c858e-114">By default the computer name of a computer that is not joined to a domain is a host name, not a fully qualified domain name (FQDN).</span></span> <span data-ttu-id="c858e-115">O construtor de topologias usa FQDNs, não nomes de host.</span><span class="sxs-lookup"><span data-stu-id="c858e-115">Topology Builder uses FQDNs, not host names.</span></span> <span data-ttu-id="c858e-116">Portanto, você deverá configurar um sufixo DNS no nome do computador a ser implantado no Servidor de Borda que não ingressou no domínio.</span><span class="sxs-lookup"><span data-stu-id="c858e-116">So, you must configure a DNS suffix on the name of the computer to be deployed as an Edge Server that is not joined to a domain.</span></span> <span data-ttu-id="c858e-117"><STRONG>Use apenas caracteres padrão</STRONG> (incluindo A–Z, a–z, 0–9 e hifens) ao atribuir FQDNs de seus Lync Servers, Servidores de Borda e pools.</span><span class="sxs-lookup"><span data-stu-id="c858e-117"><STRONG>Use only standard characters</STRONG> (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="c858e-118">Não use caracteres Unicode ou sublinhados.</span><span class="sxs-lookup"><span data-stu-id="c858e-118">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="c858e-119">Normalmente, caracteres não padrão no FQDN não são suportados por DNS externo e CAs públicas (ou seja, quando o FQDN deve ser atribuído ao SN no certificado).</span><span class="sxs-lookup"><span data-stu-id="c858e-119">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (that is, when the FQDN must be assigned to the SN in the certificate).</span></span> <span data-ttu-id="c858e-120">Para obter detalhes adicionais, consulte <A href="lync-server-2013-configure-dns-host-records.md">Configurar registros de host DNS para o Lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="c858e-120">For additional details, see <A href="lync-server-2013-configure-dns-host-records.md">Configure DNS Host records for Lync Server 2013</A></span></span>



</div>

<div>

## <a name="how-lync-clients-locate-services"></a><span data-ttu-id="c858e-121">Como os clientes do Lync localizam serviços</span><span class="sxs-lookup"><span data-stu-id="c858e-121">How Lync Clients Locate Services</span></span>

<span data-ttu-id="c858e-122">O Microsoft Lync 2010, o Lync 2013 e o Lync Mobile são semelhantes em como o cliente localiza e acessa serviços no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c858e-122">Microsoft Lync 2010, Lync 2013, and Lync Mobile are similar in how the client finds and accesses services in Lync Server 2013.</span></span> <span data-ttu-id="c858e-123">A exceção notável é o aplicativo Lync da Windows Store que usa um processo de localização de serviço diferente.</span><span class="sxs-lookup"><span data-stu-id="c858e-123">The notable exception is the Lync Windows Store app that uses a different service location process.</span></span> <span data-ttu-id="c858e-124">Esta seção detalha dois cenários de como os clientes localizam serviços, primeiro o método tradicional usando uma série de registros SRV e um host, segundo usando somente os registros de serviço descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="c858e-124">This section details two scenarios of how the clients locate services, first the traditional method using a series of SRV and A host records, second using only the Autodiscover service records.</span></span> <span data-ttu-id="c858e-125">As atualizações cumulativas para os clientes da área de trabalho alteram o processo de localização do DNS do Lync Server 2010 para todos os clientes, o processo de consulta DNS continua até que uma consulta bem-sucedida seja retornada, ou a lista de possíveis registros de DNS seja esgotada, e o erro final será retornado ao cliente.</span><span class="sxs-lookup"><span data-stu-id="c858e-125">Cumulative updates to the desktop clients change the DNS location process from Lync Server 2010 For all clients, the DNS query process continues until a successful query is returned, or the list of possible DNS records is exhausted, and the final error is returned to the client.</span></span>

<span data-ttu-id="c858e-126">Para todos os clientes **, exceto** o aplicativo Lync da Windows Store durante a pesquisa de DNS, os registros SRV são consultados e retornados ao cliente na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="c858e-126">For all clients **except** for the Lync Windows Store app During DNS lookup, SRV records are queried and returned to the client in the following order:</span></span>

1.  <span data-ttu-id="c858e-127">lyncdiscoverinternal.\<domain\></span><span class="sxs-lookup"><span data-stu-id="c858e-127">lyncdiscoverinternal.\<domain\></span></span>   <span data-ttu-id="c858e-128">Um registro de (host) para o serviço de descoberta automática nos serviços Web internos</span><span class="sxs-lookup"><span data-stu-id="c858e-128">A (host) record for the Autodiscover service on the internal Web services</span></span>

2.  <span data-ttu-id="c858e-129">lyncdiscover.\<domain\></span><span class="sxs-lookup"><span data-stu-id="c858e-129">lyncdiscover.\<domain\></span></span>   <span data-ttu-id="c858e-130">Um registro de (host) para o serviço de descoberta automática nos serviços Web externos</span><span class="sxs-lookup"><span data-stu-id="c858e-130">A (host) record for the Autodiscover service on the external Web services</span></span>

3.  <span data-ttu-id="c858e-131">\_sipinternaltls. \_ Protocol.\<domain\></span><span class="sxs-lookup"><span data-stu-id="c858e-131">\_sipinternaltls.\_tcp.\<domain\></span></span>   <span data-ttu-id="c858e-132">Registro SRV (localizador de serviço) para conexões TLS internas</span><span class="sxs-lookup"><span data-stu-id="c858e-132">SRV (service locator) record for internal TLS connections</span></span>

4.  <span data-ttu-id="c858e-133">\_sipinternal. \_ Protocol.\<domain\></span><span class="sxs-lookup"><span data-stu-id="c858e-133">\_sipinternal.\_tcp.\<domain\></span></span>   <span data-ttu-id="c858e-134">Registro SRV (localizador de serviço) para conexões TCP internas (executadas somente se o TCP for permitido)</span><span class="sxs-lookup"><span data-stu-id="c858e-134">SRV (service locator) record for internal TCP connections (performed only if TCP is allowed)</span></span>

5.  <span data-ttu-id="c858e-135">\_SIP. \_ protocolos.\<domain\></span><span class="sxs-lookup"><span data-stu-id="c858e-135">\_sip.\_tls.\<domain\></span></span>   <span data-ttu-id="c858e-136">Registro SRV (localizador de serviço) para conexões TLS externas</span><span class="sxs-lookup"><span data-stu-id="c858e-136">SRV (service locator) record for external TLS connections</span></span>

6.  <span data-ttu-id="c858e-137">sipinternal.\<domain\></span><span class="sxs-lookup"><span data-stu-id="c858e-137">sipinternal.\<domain\></span></span>   <span data-ttu-id="c858e-138">Um registro (host) para o pool ou o diretor de front-end, que é resolvível somente na rede interna</span><span class="sxs-lookup"><span data-stu-id="c858e-138">A (host) record for the Front End pool or Director, resolvable only on the internal network</span></span>

7.  <span data-ttu-id="c858e-139">sip.\<domain\></span><span class="sxs-lookup"><span data-stu-id="c858e-139">sip.\<domain\></span></span>   <span data-ttu-id="c858e-140">Um registro (host) para o pool ou o diretor de front-end na rede interna ou o serviço de borda de acesso quando o cliente for externo</span><span class="sxs-lookup"><span data-stu-id="c858e-140">A (host) record for the Front End pool or Director on the internal network, or the Access Edge service when the client is external</span></span>

8.  <span data-ttu-id="c858e-141">sipexternal.\<domain\></span><span class="sxs-lookup"><span data-stu-id="c858e-141">sipexternal.\<domain\></span></span>   <span data-ttu-id="c858e-142">Um registro (host) para o serviço de borda de acesso quando o cliente for externo</span><span class="sxs-lookup"><span data-stu-id="c858e-142">A (host) record for the Access Edge service when the client is external</span></span>

<span data-ttu-id="c858e-143">O aplicativo Lync da Windows Store altera o processo completamente porque usa dois registros:</span><span class="sxs-lookup"><span data-stu-id="c858e-143">The Lync Windows Store app changes the process completely because it uses two records:</span></span>

1.  <span data-ttu-id="c858e-144">lyncdiscoverinternal.\<domain\></span><span class="sxs-lookup"><span data-stu-id="c858e-144">lyncdiscoverinternal.\<domain\></span></span>   <span data-ttu-id="c858e-145">Um registro de (host) para o serviço de descoberta automática nos serviços Web internos</span><span class="sxs-lookup"><span data-stu-id="c858e-145">A (host) record for the Autodiscover service on the internal Web services</span></span>

2.  <span data-ttu-id="c858e-146">lyncdiscover.\<domain\></span><span class="sxs-lookup"><span data-stu-id="c858e-146">lyncdiscover.\<domain\></span></span>   <span data-ttu-id="c858e-147">Um registro de (host) para o serviço de descoberta automática nos serviços Web externos</span><span class="sxs-lookup"><span data-stu-id="c858e-147">A (host) record for the Autodiscover service on the external Web services</span></span>

<span data-ttu-id="c858e-148">Não há nenhum fallback para os outros tipos de registro.</span><span class="sxs-lookup"><span data-stu-id="c858e-148">There is no fallback to the other record types.</span></span>

<span data-ttu-id="c858e-149">A diferença entre os métodos usados para clientes mais recentes em comparação com clientes mais antigos é que o serviço de descoberta automática está se tornando o método preferencial para localizar todos os serviços.</span><span class="sxs-lookup"><span data-stu-id="c858e-149">The difference between the methods used for newer clients as compared to older clients is that the Autodiscover service is becoming the preferred method to locate all services.</span></span>

<span data-ttu-id="c858e-150">Quando uma conexão é bem-sucedida, o serviço descoberta automática retorna todas as URLs de serviços Web do pool primário do usuário, incluindo o serviço de mobilidade (conhecido como MCX pelo diretório virtual criado para o serviço no IIS), URLs do Microsoft Lync Web App e do Web Scheduler do Web App.</span><span class="sxs-lookup"><span data-stu-id="c858e-150">When a connection is successful, the Autodiscover Service returns all the Web Services URLs for the user's home pool, including the Mobility Service (known as Mcx by the virtual directory created for the service in IIS), Microsoft Lync Web App and Web scheduler URLs.</span></span> <span data-ttu-id="c858e-151">No entanto, a URL do serviço de mobilidade interna e a URL do serviço de mobilidade externa estão associadas ao FQDN dos serviços Web externos.</span><span class="sxs-lookup"><span data-stu-id="c858e-151">However, both the internal Mobility Service URL and the external Mobility Service URL is associated with the external Web Services FQDN.</span></span> <span data-ttu-id="c858e-152">Portanto, independentemente de um dispositivo móvel ser interno ou externo à rede, o dispositivo sempre se conecta ao serviço de mobilidade externamente por meio do proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="c858e-152">Therefore, regardless of whether a mobile device is internal or external to the network, the device always connects to the Mobility Service externally through the reverse proxy.</span></span>

<span data-ttu-id="c858e-153">Se as atualizações cumulativas do Lync Server 2013:2013 de fevereiro tiverem sido instaladas, o serviço de descoberta automática também retornará referências para interno/UCWA, External/UCWA e UCWA.</span><span class="sxs-lookup"><span data-stu-id="c858e-153">If the Cumulative Updates for Lync Server 2013: February 2013 has been installed, the Autodiscover Service also returns references to Internal/UCWA, External/UCWA and UCWA.</span></span> <span data-ttu-id="c858e-154">Essas entradas se referem ao componente da Web da API de comunicação unificada (UCWA).</span><span class="sxs-lookup"><span data-stu-id="c858e-154">These entries refer to the Unified Communications Web API (UCWA) web component.</span></span> <span data-ttu-id="c858e-155">Atualmente, somente a entrada UCWA é usada e fornece uma referência a uma URL para o componente da Web.</span><span class="sxs-lookup"><span data-stu-id="c858e-155">Currently, only the entry UCWA is used and provides a reference to a URL for the web component.</span></span> <span data-ttu-id="c858e-156">UCWA é usado pelos clientes móveis do Lync 2013 em vez do serviço de mobilidade do MCX usado pelos clientes móveis do Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="c858e-156">UCWA is used by Lync 2013 Mobile clients instead of the Mcx Mobility Service used by the Lync 2010 Mobile clients.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c858e-157">Ao criar registros SRV, é importante lembrar que eles devem apontar para um registro DNS A e AAAA (se você estiver usando endereçamento IPv6) no mesmo domínio em que o registro SRV DNS for criado.</span><span class="sxs-lookup"><span data-stu-id="c858e-157">When creating SRV records, it is important to remember that they must point to a DNS A and AAAA (if you are using IPv6 addressing) record in the same domain in which the DNS SRV record is created.</span></span> <span data-ttu-id="c858e-158">Por exemplo, se o registro SRV estiver em contoso.com, o registro a e AAAA (se você estiver usando endereçamento IPv6) aponta para não pode estar no fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="c858e-158">For example, if the SRV record is in contoso.com, the A and AAAA (if you are using IPv6 addressing) record it points to cannot be in fabrikam.com.</span></span>



</div>

<div>


> [!TIP]  
> <span data-ttu-id="c858e-159">A configuração padrão é direcionar todo o tráfego de cliente móvel por meio do site externo.</span><span class="sxs-lookup"><span data-stu-id="c858e-159">The default configuration is to direct all mobile client traffic through the external site.</span></span> <span data-ttu-id="c858e-160">Você pode modificar as configurações para retornar apenas a URL interna, se for mais preferível para atender às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="c858e-160">You can modify settings to return only the internal URL, if this is more preferable for your requirements.</span></span> <span data-ttu-id="c858e-161">Com essa configuração, os usuários podem usar os aplicativos móveis do Lync em seus dispositivos móveis somente quando estiverem dentro da rede corporativa.</span><span class="sxs-lookup"><span data-stu-id="c858e-161">With this configuration, users can use Lync mobile applications on their mobile devices only when they are inside the corporate network.</span></span> <span data-ttu-id="c858e-162">Para definir essa configuração, use o cmdlet <STRONG>set-CsMcxConfiguration</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="c858e-162">To define this configuration, you use the <STRONG>Set-CsMcxConfiguration</STRONG> cmdlet.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="c858e-163">Embora os aplicativos móveis também possam se conectar a outros serviços do Lync Server 2013, como serviço de catálogo de endereços, solicitações da Web de aplicativo móvel interno acessam o FQDN da Web externa somente para o serviço de mobilidade.</span><span class="sxs-lookup"><span data-stu-id="c858e-163">Although mobile applications can also connect to other Lync Server 2013 services, such as Address Book Service, internal mobile application web requests go to the external web FQDN only for the Mobility Service.</span></span> <span data-ttu-id="c858e-164">Outras solicitações de serviço, como solicitações de catálogo de endereços, não exigem essa configuração.</span><span class="sxs-lookup"><span data-stu-id="c858e-164">Other service requests, such as Address Book requests, do not require this configuration.</span></span>



</div>

<span data-ttu-id="c858e-165">Os dispositivos móveis dão suporte à descoberta manual de serviços.</span><span class="sxs-lookup"><span data-stu-id="c858e-165">Mobile devices support manual discovery of services.</span></span> <span data-ttu-id="c858e-166">Nesse caso, cada usuário deve configurar as configurações do dispositivo móvel com os URIs de serviço de descoberta automática interna e externa, incluindo o protocolo e o caminho, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c858e-166">In this case, each user must configure the mobile device settings with the full internal and external Autodiscover Service URIs, including the protocol and path, as follows:</span></span>

  - <span data-ttu-id="c858e-167"> https:// \<ExtPoolFQDN\> /autodiscover/autodiscoverservice.svc/root para acesso externo</span><span class="sxs-lookup"><span data-stu-id="c858e-167">https://\<ExtPoolFQDN\>/Autodiscover/autodiscoverservice.svc/Root for external access</span></span>

  - <span data-ttu-id="c858e-168"> https:// \<IntPoolFQDN\> /autodiscover/autodiscover.svc/root para acesso interno</span><span class="sxs-lookup"><span data-stu-id="c858e-168">https://\<IntPoolFQDN\>/AutoDiscover/AutoDiscover.svc/Root for internal access</span></span>

<span data-ttu-id="c858e-169">Recomendamos que você use a descoberta automática, em vez da descoberta manual.</span><span class="sxs-lookup"><span data-stu-id="c858e-169">We recommend that you use automatic discovery, rather than manual discovery.</span></span> <span data-ttu-id="c858e-170">No entanto, as configurações manuais podem ser úteis para solucionar problemas de conectividade de dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="c858e-170">However, manual settings can be useful for troubleshooting mobile device connectivity issues.</span></span>

</div>

<div>

## <a name="configuring-split-brain-dns-with-lync-server"></a><span data-ttu-id="c858e-171">Configurar o Split-Brain DNS com o Lync Server</span><span class="sxs-lookup"><span data-stu-id="c858e-171">Configuring Split-Brain DNS with Lync Server</span></span>

<span data-ttu-id="c858e-172">O DNS Split-Brain é conhecido por vários nomes, por exemplo, Split DNS ou Split-Horizon DNS.</span><span class="sxs-lookup"><span data-stu-id="c858e-172">Split-brain DNS is known by a number of names, for example, split DNS or split-horizon DNS.</span></span> <span data-ttu-id="c858e-173">Simplesmente, ele descreve uma configuração de DNS onde há duas zonas DNS com o mesmo namespace – mas uma única solicitação de serviços de zona DNS e os outros serviços de zona DNS são solicitações somente externas.</span><span class="sxs-lookup"><span data-stu-id="c858e-173">Simply, it describes a DNS configuration where there are two DNS zones with the same namespace – but one DNS zone services internal-only requests, and the other DNS zone services external-only requests.</span></span> <span data-ttu-id="c858e-174">No entanto, muitos dos SRV DNS e registros contidos no DNS interno não serão contidos no DNS externo e o inverso também será verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="c858e-174">However, many of the DNS SRV and A records contained in the internal DNS will not be contained in the external DNS, and the reverse is also true.</span></span> <span data-ttu-id="c858e-175">Nos casos em que o mesmo registro DNS existe no DNS interno e externo (por exemplo, www.contoso.com), o endereço IP retornado será diferente com base em onde (interno ou externo) a consulta foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="c858e-175">In cases where the same DNS record exists in both the internal and external DNS (for example, www.contoso.com), the IP address returned will be different based on where (internal or external) the query was initiated.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c858e-176">Atualmente, não há suporte para o Split-Brain DNS para a mobilidade ou, mais especificamente, os registros DNS LyncDiscover e LyncDiscoverInternal.</span><span class="sxs-lookup"><span data-stu-id="c858e-176">Currently, Split-Brain DNS is not supported for the mobility, or more specifically, the LyncDiscover and LyncDiscoverInternal DNS records.</span></span> <span data-ttu-id="c858e-177">LyncDiscover deve ser definido em um servidor DNS externo e LyncDiscoverInternal deve ser definido em um servidor DNS interno.</span><span class="sxs-lookup"><span data-stu-id="c858e-177">LyncDiscover must be defined on an external DNS server and LyncDiscoverInternal must be defined on an internal DNS server.</span></span>



</div>

<span data-ttu-id="c858e-178">Para os fins desses tópicos, o termo divisão-Brain DNS será usado.</span><span class="sxs-lookup"><span data-stu-id="c858e-178">For the purposes of these topics, the term split-brain DNS will be used.</span></span>

<span data-ttu-id="c858e-179">Se você estiver configurando o DNS Split-Brain, a seguinte zona interna e externa contém um resumo dos tipos de registros de DNS necessários em cada zona.</span><span class="sxs-lookup"><span data-stu-id="c858e-179">If you are configuring split-brain DNS, the following internal and external zone contain a summary of the types of DNS records required in each zone.</span></span> <span data-ttu-id="c858e-180">Para obter detalhes, consulte [cenários para acesso de usuários externos no Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="c858e-180">For details, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

<span data-ttu-id="c858e-181">**DNS interno:**</span><span class="sxs-lookup"><span data-stu-id="c858e-181">**Internal DNS:**</span></span>

  - <span data-ttu-id="c858e-182">Contém uma zona DNS chamada contoso.com para a qual é autoritativa</span><span class="sxs-lookup"><span data-stu-id="c858e-182">Contains a DNS zone called contoso.com for which it is authoritative</span></span>

  - <span data-ttu-id="c858e-183">A zona contoso.com interna contém:</span><span class="sxs-lookup"><span data-stu-id="c858e-183">The internal contoso.com zone contains:</span></span>
    
      - <span data-ttu-id="c858e-184">DNS A e AAAA (se você estiver usando endereçamento IPv6) e Registros SRV para configuração automática de cliente do Lync Server 2013 (opcional)</span><span class="sxs-lookup"><span data-stu-id="c858e-184">DNS A and AAAA (if you are using IPv6 addressing) and SRV records for internal Lync Server 2013 client autoconfiguration (optional)</span></span>
    
      - <span data-ttu-id="c858e-185">DNS A e AAAA (se você estiver usando endereçamento IPv6) ou registros CNAME para descoberta automática de serviços Web do Lync Server 2013 (opcional)</span><span class="sxs-lookup"><span data-stu-id="c858e-185">DNS A and AAAA (if you are using IPv6 addressing) or CNAME records for automatic discovery of Lync Server 2013 Web Services (optional)</span></span>
    
      - <span data-ttu-id="c858e-186">Registros A e AAAA do DNS (se você estiver usando endereçamento IPv6) para nome do pool de front-end, diretor ou nome do pool do diretor e todos os servidores internos que executam o Lync Server 2013 na rede da empresa</span><span class="sxs-lookup"><span data-stu-id="c858e-186">DNS A and AAAA (if you are using IPv6 addressing) records for Front End pool name, Director or Director pool name, and all internal servers running Lync Server 2013 in the corporate network</span></span>
    
      - <span data-ttu-id="c858e-187">Registros A e AAAA do DNS (se você estiver usando endereçamento IPv6) para a interface interna de borda de cada servidor do Lync 2013, servidor de borda na rede de perímetro</span><span class="sxs-lookup"><span data-stu-id="c858e-187">DNS A and AAAA (if you are using IPv6 addressing) records for the Edge internal interface of each Lync Server 2013, Edge Server in the perimeter network</span></span>
    
      - <span data-ttu-id="c858e-188">Registros DNS A e AAAA (se você estiver usando endereçamento IPv6) para a interface interna de cada servidor de proxy reverso na rede de perímetro (opcional para o gerenciamento de proxy reverso)</span><span class="sxs-lookup"><span data-stu-id="c858e-188">DNS A and AAAA (if you are using IPv6 addressing) records for the internal interface of each reverse proxy server in the perimeter network (optional for management of reverse proxy)</span></span>
    
      - <span data-ttu-id="c858e-189">Todas as interfaces de borda interna do servidor de borda do Lync Server 2013 na rede de perímetro usam a zona DNS interna para a resolução de consultas para o contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-189">All Lync Server 2013  Edge Server internal edge interfaces in the perimeter network use the internal DNS zone for resolving queries to contoso.com</span></span>
    
      - <span data-ttu-id="c858e-190">Todos os servidores que executam o Lync Server 2013 e os clientes que executam o Lync 2013 na rede corporativa apontam para os servidores DNS internos para a resolução de consultas para o contoso.com ou o uso do arquivo HOSTs em cada servidor de borda e lista de A e AAAA (se você estiver usando endereçamento IPv6) para o próximo servidor de salto, especificamente o diretor ou VIP, VIP ou servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="c858e-190">All servers running Lync Server 2013 and clients running Lync 2013 in the corporate network point to the internal DNS servers for resolving queries to contoso.com, or use of HOSTS file on each Edge server and list A and AAAA (if you are using IPv6 addressing) records for next hop server, specifically the Director or Director VIP, Front End pool VIP, or Standard Edition server</span></span>

<span data-ttu-id="c858e-191">**DNS externo:**</span><span class="sxs-lookup"><span data-stu-id="c858e-191">**External DNS:**</span></span>

  - <span data-ttu-id="c858e-192">Contém uma zona DNS chamada contoso.com para a qual é autoritativa</span><span class="sxs-lookup"><span data-stu-id="c858e-192">Contains a DNS zone called contoso.com for which it is authoritative</span></span>

  - <span data-ttu-id="c858e-193">A zona contoso.com externa contém:</span><span class="sxs-lookup"><span data-stu-id="c858e-193">The external contoso.com zone contains:</span></span>
    
      - <span data-ttu-id="c858e-194">DNS A e AAAA (se você estiver usando endereçamento IPv6) e Registros SRV para configuração automática do cliente do Lync Server 2013 (opcional)</span><span class="sxs-lookup"><span data-stu-id="c858e-194">DNS A and AAAA (if you are using IPv6 addressing) and SRV records for Lync Server 2013 client autoconfiguration (optional)</span></span>
    
      - <span data-ttu-id="c858e-195">DNS A e AAAA (se você estiver usando endereçamento IPv6) ou registros CNAME para descoberta automática de serviços Web do Lync Server 2013 para uso com o Mobility</span><span class="sxs-lookup"><span data-stu-id="c858e-195">DNS A and AAAA (if you are using IPv6 addressing) or CNAME records for automatic discovery of Lync Server 2013 Web Services for use with mobility</span></span>
    
      - <span data-ttu-id="c858e-196">DNS A e AAAA (se você estiver usando endereçamento IPv6) e Registros SRV para a interface externa Edge de cada Lync Server 2013, servidor de borda ou VIP (IP virtual) do balanceador de carga de hardware na rede de perímetro</span><span class="sxs-lookup"><span data-stu-id="c858e-196">DNS A and AAAA (if you are using IPv6 addressing) and SRV records for the Edge external interface of each Lync Server 2013, Edge Server or hardware load balancer virtual IP (VIP) in the perimeter network</span></span>
    
      - <span data-ttu-id="c858e-197">Registros DNS A e AAAA (se você estiver usando endereçamento IPv6) para a interface externa do servidor proxy reverso ou VIP para um pool de servidores proxy reverso na rede de perímetro</span><span class="sxs-lookup"><span data-stu-id="c858e-197">DNS A and AAAA (if you are using IPv6 addressing) records for the external interface of the reverse proxy server or VIP for a pool of reverse proxy servers in the perimeter network</span></span>

</div>

<div>

## <a name="automatic-configuration-without-split-brain-dns"></a><span data-ttu-id="c858e-198">Configuração automática sem Split-Brain DNS</span><span class="sxs-lookup"><span data-stu-id="c858e-198">Automatic Configuration without Split-Brain DNS</span></span>

<span data-ttu-id="c858e-199">Usando o DNS Split-Brain, um usuário do Lync Server 2013 que entra internamente pode aproveitar a configuração automática se a zona DNS interna contiver um \_ sipinternaltls. \_ registro SRV TCP para cada domínio SIP em uso.</span><span class="sxs-lookup"><span data-stu-id="c858e-199">Using split-brain DNS, a Lync Server 2013 user that signs in internally can take advantage of automatic configuration if the internal DNS zone contains a \_sipinternaltls.\_tcp SRV record for each SIP domain in use.</span></span> <span data-ttu-id="c858e-200">No entanto, se você não usar DNS Split-Brain, a configuração interna automática de clientes que executa o Lync não funcionará, a menos que uma das soluções alternativas descritas mais adiante nesta seção seja implementada.</span><span class="sxs-lookup"><span data-stu-id="c858e-200">However, if you do not use split-brain DNS, internal automatic configuration of clients running Lync will not work unless one of the workarounds described in later in this section is implemented.</span></span> <span data-ttu-id="c858e-201">Isso ocorre porque o Lync Server 2013 exige que o URI SIP do usuário corresponda ao domínio do pool de front-ends designado para configuração automática.</span><span class="sxs-lookup"><span data-stu-id="c858e-201">This is because Lync Server 2013 requires the user’s SIP URI to match the domain of the Front End pool designated for automatic configuration.</span></span> <span data-ttu-id="c858e-202">Este também era o caso das versões anteriores do Communicator.</span><span class="sxs-lookup"><span data-stu-id="c858e-202">This was also the case with earlier versions of Communicator.</span></span>

<span data-ttu-id="c858e-203">Por exemplo, se você tiver dois domínios SIP em uso, os seguintes registros de serviço DNS (SRV) seriam necessários:</span><span class="sxs-lookup"><span data-stu-id="c858e-203">For example, if you have two SIP domains in use, the following DNS service (SRV) records would be required:</span></span>

  - <span data-ttu-id="c858e-204">Se um usuário entrar como bob@contoso.com, o seguinte registro SRV funcionará para configuração automática, porque o domínio SIP do usuário (contoso.com) corresponde ao domínio do pool de front-end de configuração automática):</span><span class="sxs-lookup"><span data-stu-id="c858e-204">If a user signs in as bob@contoso.com the following SRV record will work for automatic configuration because the user’s SIP domain (contoso.com) matches the domain of automatic configuration Front End pool):</span></span>
    
     <span data-ttu-id="c858e-205">\_sipinternaltls. \_ tcp.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c858e-205">\_sipinternaltls.\_tcp.contoso.com.</span></span> <span data-ttu-id="c858e-206">86400 IN SRV 0 0 5061 pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-206">86400 IN SRV 0 0 5061 pool01.contoso.com</span></span>

  - <span data-ttu-id="c858e-207">Se um usuário entrar como alice@fabrikam.com, o seguinte registro SRV DNS funcionará para a configuração automática do segundo domínio SIP.</span><span class="sxs-lookup"><span data-stu-id="c858e-207">If a user signs in as alice@fabrikam.com the following DNS SRV record will work for automatic configuration of the second SIP domain.</span></span>
    
     <span data-ttu-id="c858e-208">\_sipinternaltls. \_ tcp.fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="c858e-208">\_sipinternaltls.\_tcp.fabrikam.com.</span></span> <span data-ttu-id="c858e-209">86400 IN SRV 0 0 5061 pool01.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="c858e-209">86400 IN SRV 0 0 5061 pool01.fabrikam.com</span></span>

<span data-ttu-id="c858e-210">Para comparação, se um usuário entrar como tim@litwareinc.com, o seguinte registro SRV DNS não funcionará para configuração automática, porque o domínio SIP do cliente (litwareinc.com) não corresponde ao domínio no qual o pool está (fabrikam.com):</span><span class="sxs-lookup"><span data-stu-id="c858e-210">For comparison, if a user signs in as tim@litwareinc.com the following DNS SRV record will not work for automatic configuration, because the client’s SIP domain (litwareinc.com) does not match the domain that the pool is in (fabrikam.com):</span></span>

 <span data-ttu-id="c858e-211">\_sipinternaltls. \_ tcp.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="c858e-211">\_sipinternaltls.\_tcp.litwareinc.com.</span></span> <span data-ttu-id="c858e-212">86400 IN SRV 0 0 5061 pool01.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="c858e-212">86400 IN SRV 0 0 5061 pool01.fabrikam.com</span></span>

<span data-ttu-id="c858e-213">Se a configuração automática for necessária para os clientes que executam o Lync, selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="c858e-213">If automatic configuration is required for clients running Lync, select one of the following options:</span></span>

  - <span data-ttu-id="c858e-214">**Objetos de política de grupo**   Use objetos de política de grupo (GPOs) para preencher os valores de servidor corretos.</span><span class="sxs-lookup"><span data-stu-id="c858e-214">**Group Policy Objects**   Use Group Policy objects (GPOs) to populate the correct server values.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c858e-215">Essa opção não habilita a configuração automática, mas automatiza o processo de configuração manual, portanto, se essa abordagem for usada, os registros SRV associados à configuração automática não serão necessários.</span><span class="sxs-lookup"><span data-stu-id="c858e-215">This option does not enable automatic configuration, but it does automate the process of manual configuration, so if this approach is used, the SRV records associated with automatic configuration are not required.</span></span>

    
    </div>

  - <span data-ttu-id="c858e-216">**Zona interna correspondente**   Crie uma zona no DNS interno que corresponda à zona DNS externa (por exemplo, contoso.com) e crie registros DNS A e AAAA (se você estiver usando endereçamento IPv6) correspondentes ao pool do Lync Server 2013 usado para configuração automática.</span><span class="sxs-lookup"><span data-stu-id="c858e-216">**Matching internal zone**   Create a zone in the internal DNS that matches the external DNS zone (for example, contoso.com) and create DNS A and AAAA (if you are using IPv6 addressing) records corresponding to the Lync Server 2013 pool used for automatic configuration.</span></span> <span data-ttu-id="c858e-217">Por exemplo, se um usuário estiver hospedado no pool01.contoso.net, mas entrar no Lync como bob@contoso.com, crie uma zona DNS interna chamada contoso.com e dentro dela, crie um registro DNS A e AAAA (se o endereçamento IPv6 for usado) para pool01.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c858e-217">For example, if a user is homed on pool01.contoso.net but signs into Lync as bob@contoso.com, create an internal DNS zone called contoso.com and inside it, create a DNS A and AAAA (if IPv6 addressing is used) record for pool01.contoso.com.</span></span>

  - <span data-ttu-id="c858e-218">**Zona interna de ponto de fixação**   Se você estiver criando uma zona inteira no DNS interno não for uma opção, poderá criar zonas de ponto PIN (ou seja, dedicada) que correspondam aos Registros SRV necessários para a configuração automática e preencher essas zonas usando dnscmd.exe.</span><span class="sxs-lookup"><span data-stu-id="c858e-218">**Pin-point internal zone**   If you are creating an entire zone in the internal DNS is not an option, you can create pin-point (that is, dedicated) zones that correspond to the SRV records that are required for automatic configuration, and populate those zones using dnscmd.exe.</span></span> <span data-ttu-id="c858e-219">Dnscmd.exe é necessária porque a interface do usuário DNS não dá suporte à criação de zonas de ponto PIN.</span><span class="sxs-lookup"><span data-stu-id="c858e-219">Dnscmd.exe is required because the DNS user interface does not support creation of pin-point zones.</span></span> <span data-ttu-id="c858e-220">Por exemplo, se o domínio SIP for contoso.com e você tiver um pool de front-end chamado pool01 que contém dois servidores front-end, você precisará das seguintes zonas de ponto de fixação e registros no seu DNS interno:</span><span class="sxs-lookup"><span data-stu-id="c858e-220">For example, if the SIP domain is contoso.com and you have a Front End pool called pool01 that contains two Front End Servers, you need the following pin-point zones and A records in your internal DNS:</span></span>
    
        dnscmd . /zoneadd _sipinternaltls._tcp.contoso.com. /dsprimary
        dnscmd . /recordadd _sipinternaltls._tcp.contoso.com. @ SRV 0 0 5061 pool01.contoso.com.
        dnscmd . /zoneadd pool01.contoso.com. /dsprimary
        dnscmd . /recordadd pool01.contoso.com. @ A 192.168.10.90
        dnscmd . /recordadd pool01.contoso.com. @ AAAA <IPv6 address>
        dnscmd . /recordadd pool01.contoso.com. @ A 192.168.10.91 
        dnscmd . /recordadd pool01.contoso.com. @ AAAA <IPv6 address>
    
    <span data-ttu-id="c858e-221">Se o ambiente contiver um segundo domínio SIP (por exemplo, fabrikam.com), você precisará das seguintes zonas de ponto PIN e registros no seu DNS interno:</span><span class="sxs-lookup"><span data-stu-id="c858e-221">If your environment contains a second SIP domain (for example, fabrikam.com), you need the following pin-point zones and A records in your internal DNS:</span></span>
    
        dnscmd . /zoneadd _sipinternaltls._tcp.fabrikam.com. /dsprimary
        dnscmd . /recordadd _sipinternaltls._tcp.fabrikam.com. @ SRV 0 0 5061 pool01.fabrikam.com.
        dnscmd . /zoneadd pool01.fabrikam.com. /dsprimary
        dnscmd . /recordadd pool01.fabrikam.com. @ A 192.168.10.90
        dnscmd . /recordadd pool01.contoso.com. @ AAAA <IPv6 address>
        dnscmd . /recordadd pool01.fabrikam.com. @ A 192.168.10.91
        dnscmd . /recordadd pool01.contoso.com. @ AAAA <IPv6 address>

<div>


> [!NOTE]  
> <span data-ttu-id="c858e-222">O FQDN do pool de front-end aparece duas vezes, mas com dois endereços IP diferentes.</span><span class="sxs-lookup"><span data-stu-id="c858e-222">The Front End pool FQDN appears twice, but with two different IP addresses.</span></span> <span data-ttu-id="c858e-223">Isso ocorre porque o balanceamento de carga de DNS é usado, mas se o balanceamento de carga de hardware for usado, haveria apenas uma única entrada de pool de front-end.</span><span class="sxs-lookup"><span data-stu-id="c858e-223">This is because DNS load balancing is used, but if hardware load balancing is used, there would be only a single Front End pool entry.</span></span> <span data-ttu-id="c858e-224">Além disso, os valores de FQDN do pool de front-end são alterados entre o exemplo contoso.com e o fabrikam.com exemplo, mas os endereços IP permanecem os mesmos.</span><span class="sxs-lookup"><span data-stu-id="c858e-224">Also, the Front End pool FQDN values change between the contoso.com example and the fabrikam.com example, but the IP addresses remain the same.</span></span> <span data-ttu-id="c858e-225">Isso ocorre porque os usuários se conectam de um domínio SIP, usam o mesmo pool de front-end para configuração automática.</span><span class="sxs-lookup"><span data-stu-id="c858e-225">This is because users signing in from either SIP domain, use the same Front End pool for automatic configuration.</span></span>



</div>

<span data-ttu-id="c858e-226">Para obter detalhes, consulte o artigo do blog da DMTF, "configuração automática do Communicator e Split-Brain DNS", em [https://go.microsoft.com/fwlink/p/?linkId=200707](https://go.microsoft.com/fwlink/p/?linkid=200707) .</span><span class="sxs-lookup"><span data-stu-id="c858e-226">For details, see the DMTF blog article, "Communicator Automatic Configuration and Split-Brain DNS," at [https://go.microsoft.com/fwlink/p/?linkId=200707](https://go.microsoft.com/fwlink/p/?linkid=200707).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c858e-227">O conteúdo de cada blog e sua URL estão sujeitos a alterações sem aviso prévio.</span><span class="sxs-lookup"><span data-stu-id="c858e-227">The content of each blog and its URL are subject to change without notice.</span></span>



</div>

</div>

<div>

## <a name="configuring-the-domain-name-system-dns-for-disaster-recovery"></a><span data-ttu-id="c858e-228">Configurando o sistema de nomes de domínio (DNS) para recuperação de desastres</span><span class="sxs-lookup"><span data-stu-id="c858e-228">Configuring the domain name system (DNS) for Disaster Recovery</span></span>

<span data-ttu-id="c858e-229">Para configurar o DNS para redirecionar o tráfego da Web do Lync Server 2013 para seus sites de failover e recuperação de desastres, você deve estar usando um provedor de DNS compatível com GeoDNS.</span><span class="sxs-lookup"><span data-stu-id="c858e-229">To configure DNS to redirect Lync Server 2013 Web traffic to your disaster recovery and failover sites, you must be using a DNS provider that supports GeoDNS.</span></span> <span data-ttu-id="c858e-230">Você pode configurar seus registros DNS para a Web para dar suporte à recuperação de desastres, de modo que os recursos que usam serviços Web continuem mesmo se um pool de front-end inteiro ficar inativo.</span><span class="sxs-lookup"><span data-stu-id="c858e-230">You can set up your DNS records for Web to support disaster recovery, so that features that use Web services continue even if one entire Front End pool goes down.</span></span> <span data-ttu-id="c858e-231">Este recurso de recuperação de desastres dá suporte à descoberta automática (URL Lyncdiscover), a chamadas e a URLs simples de discagem.</span><span class="sxs-lookup"><span data-stu-id="c858e-231">This disaster recovery feature supports the Autodiscover (Lyncdiscover URL), Meet and Dial-In simple URLs.</span></span>

<span data-ttu-id="c858e-232">Você define e configura registros de host DNS adicionais (A e AAAA se estiver usando IPv6) para resolução interna e externa de serviços Web em seu provedor de GeoDNS.</span><span class="sxs-lookup"><span data-stu-id="c858e-232">You define and configure additional DNS host (A and AAAA if using IPv6) records for internal and external resolution of Web services at your GeoDNS provider.</span></span> <span data-ttu-id="c858e-233">Os detalhes a seguir pressupõem pools emparelhados, geograficamente dispersos e GeoDNS compatíveis com o seu provedor com o DNS de rodízio, ou configurado para usar o Pool1 como principal, e para fazer failover para Pool2 no caso de perda de comunicações ou falha de hardware.</span><span class="sxs-lookup"><span data-stu-id="c858e-233">The following details assume paired pools, geographically dispersed, and GeoDNS supported by your provider with either round-robin DNS, or configured to use Pool1 as primary, and fail over to Pool2 in the event of communications loss or hardware failure.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c858e-234">Registro GeoDNS (exemplo)</span><span class="sxs-lookup"><span data-stu-id="c858e-234">GeoDNS record (example)</span></span></th>
<th><span data-ttu-id="c858e-235">Registros de pool (exemplo)</span><span class="sxs-lookup"><span data-stu-id="c858e-235">Pool records (example)</span></span></th>
<th><span data-ttu-id="c858e-236">Registros CNAME (exemplo)</span><span class="sxs-lookup"><span data-stu-id="c858e-236">CNAME records (example)</span></span></th>
<th><span data-ttu-id="c858e-237">Registros DNS (selecione uma opção)</span><span class="sxs-lookup"><span data-stu-id="c858e-237">DNS settings (select one option)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c858e-238">Meet-int.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-238">Meet-int.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-239">Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-239">Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-240">Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-240">Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-241">Alias Meet.contoso.com para Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-241">Meet.contoso.com alias to Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-242">Alias Meet.contoso.com para Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-242">Meet.contoso.com alias to Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-243">Round Robin entre pools</span><span class="sxs-lookup"><span data-stu-id="c858e-243">Round Robin between pools</span></span></p>
<p><span data-ttu-id="c858e-244">Usar primário, conectar ao secundário se houver falha</span><span class="sxs-lookup"><span data-stu-id="c858e-244">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c858e-245">Meet-ext.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-245">Meet-ext.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-246">Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-246">Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-247">Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-247">Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-248">Alias Meet.contoso.com para Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-248">Meet.contoso.com alias to Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-249">Alias Meet.contoso.com para Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-249">Meet.contoso.com alias to Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-250">Round Robin entre pools</span><span class="sxs-lookup"><span data-stu-id="c858e-250">Round Robin between pools</span></span></p>
<p><span data-ttu-id="c858e-251">Usar primário, conectar ao secundário se houver falha</span><span class="sxs-lookup"><span data-stu-id="c858e-251">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c858e-252">Dialin-int.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-252">Dialin-int.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-253">Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-253">Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-254">Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-254">Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-255">Alias Dialin.contoso.com para Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-255">Dialin.contoso.com alias to Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-256">Alias Dialin.contoso.com para Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-256">Dialin.contoso.com alias to Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-257">Round Robin entre pools</span><span class="sxs-lookup"><span data-stu-id="c858e-257">Round Robin between pools</span></span></p>
<p><span data-ttu-id="c858e-258">Usar primário, conectar ao secundário se houver falha</span><span class="sxs-lookup"><span data-stu-id="c858e-258">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c858e-259">Dialin-ext.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-259">Dialin-ext.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-260">Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-260">Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-261">Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-261">Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-262">Alias Dialin.contoso.com para Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-262">Dialin.contoso.com alias to Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-263">Alias Dialin.contoso.com para Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-263">Dialin.contoso.com alias to Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-264">Round Robin entre pools</span><span class="sxs-lookup"><span data-stu-id="c858e-264">Round Robin between pools</span></span></p>
<p><span data-ttu-id="c858e-265">Usar primário, conectar ao secundário se houver falha</span><span class="sxs-lookup"><span data-stu-id="c858e-265">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c858e-266">Lyncdiscoverint-int.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-266">Lyncdiscoverint-int.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-267">Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-267">Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-268">Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-268">Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-269">Alias Lyncdiscoverinternal.contoso.com para Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-269">Lyncdiscoverinternal.contoso.com alias to Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-270">Alias Lyncdiscoverinternal.contoso.com para Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-270">Lyncdiscoverinternal.contoso.com alias to Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-271">Round Robin entre pools</span><span class="sxs-lookup"><span data-stu-id="c858e-271">Round Robin between pools</span></span></p>
<p><span data-ttu-id="c858e-272">Usar primário, conectar ao secundário se houver falha</span><span class="sxs-lookup"><span data-stu-id="c858e-272">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c858e-273">Lyncdiscover-ext.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-273">Lyncdiscover-ext.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-274">Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-274">Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-275">Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-275">Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-276">Alias Lyncdiscover.contoso.com para Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-276">Lyncdiscover.contoso.com alias to Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-277">Alias Lyncdiscover.contoso.com para Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-277">Lyncdiscover.contoso.com alias to Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-278">Round Robin entre pools</span><span class="sxs-lookup"><span data-stu-id="c858e-278">Round Robin between pools</span></span></p>
<p><span data-ttu-id="c858e-279">Usar primário, conectar ao secundário se houver falha</span><span class="sxs-lookup"><span data-stu-id="c858e-279">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c858e-280">Scheduler-int.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-280">Scheduler-int.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-281">Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-281">Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-282">Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-282">Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-283">Alias Scheduler.contoso.com para Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-283">Scheduler.contoso.com alias to Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-284">Alias Scheduler.contoso.com para Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-284">Scheduler.contoso.com alias to Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-285">Round Robin entre pools</span><span class="sxs-lookup"><span data-stu-id="c858e-285">Round Robin between pools</span></span></p>
<p><span data-ttu-id="c858e-286">Usar primário, conectar ao secundário se houver falha</span><span class="sxs-lookup"><span data-stu-id="c858e-286">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c858e-287">Scheduler-ext.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-287">Scheduler-ext.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-288">Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-288">Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-289">Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-289">Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-290">Alias Scheduler.contoso.com para Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-290">Scheduler.contoso.com alias to Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="c858e-291">Alias Scheduler.contoso.com para Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c858e-291">Scheduler.contoso.com alias to Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c858e-292">Round Robin entre pools</span><span class="sxs-lookup"><span data-stu-id="c858e-292">Round Robin between pools</span></span></p>
<p><span data-ttu-id="c858e-293">Usar primário, conectar ao secundário se houver falha</span><span class="sxs-lookup"><span data-stu-id="c858e-293">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-load-balancing"></a><span data-ttu-id="c858e-294">DNS Load Balancing</span><span class="sxs-lookup"><span data-stu-id="c858e-294">DNS Load Balancing</span></span>

<span data-ttu-id="c858e-295">O balanceamento de carga de DNS geralmente é implementado no nível do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c858e-295">DNS load balancing is typically implemented at the application level.</span></span> <span data-ttu-id="c858e-296">O aplicativo (por exemplo, um cliente executando o Lync), tenta se conectar a um servidor em um pool conectando-se a um dos endereços IP retornados pela consulta de registro DNS A e AAAA (se o endereçamento IPv6 for usado) para o pool FQDN (nome de domínio totalmente qualificado).</span><span class="sxs-lookup"><span data-stu-id="c858e-296">The application (for example, a client running Lync), tries to connect to a server in a pool by connecting to one of the IP addresses returned from the DNS A and AAAA (if IPv6 addressing is used) record query for the pool fully qualified domain name (FQDN).</span></span>

<span data-ttu-id="c858e-297">Por exemplo, se houver três servidores front-end em um pool chamado pool01.contoso.com, ocorrerá o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c858e-297">For example, if there are three front end servers in a pool named pool01.contoso.com, the following will happen:</span></span>

  - <span data-ttu-id="c858e-298">Clientes que executam o DNS de consulta do Lync para pool01.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c858e-298">Clients running Lync query DNS for pool01.contoso.com.</span></span> <span data-ttu-id="c858e-299">A consulta retorna três endereços IP e os armazena em cache da seguinte maneira (não necessariamente nesta ordem):</span><span class="sxs-lookup"><span data-stu-id="c858e-299">The query returns three IP addresses and caches them as follows (not necessarily in this order):</span></span>
    
    <span data-ttu-id="c858e-300">pool01.contoso.com 192.168.10.90</span><span class="sxs-lookup"><span data-stu-id="c858e-300">pool01.contoso.com      192.168.10.90</span></span>
    
    <span data-ttu-id="c858e-301">pool01.contoso.com 192.168.10.91</span><span class="sxs-lookup"><span data-stu-id="c858e-301">pool01.contoso.com      192.168.10.91</span></span>
    
    <span data-ttu-id="c858e-302">pool01.contoso.com 192.168.10.92</span><span class="sxs-lookup"><span data-stu-id="c858e-302">pool01.contoso.com      192.168.10.92</span></span>

  - <span data-ttu-id="c858e-303">O cliente tenta estabelecer uma conexão TCP (Transmission Control Protocol) a um dos endereços IP.</span><span class="sxs-lookup"><span data-stu-id="c858e-303">The client attempts to establish a Transmission Control Protocol (TCP) connection to one of the IP addresses.</span></span> <span data-ttu-id="c858e-304">Se isso falhar, o cliente tentará o próximo endereço IP no cache.</span><span class="sxs-lookup"><span data-stu-id="c858e-304">If that fails, the client tries the next IP address in the cache.</span></span>

  - <span data-ttu-id="c858e-305">Se a conexão TCP for bem -sucedida, o cliente negocia o TLS para se conectar ao Registrador Avançado primário em pool01.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c858e-305">If the TCP connection succeeds, the client negotiates TLS to connect to the primary registrar on pool01.contoso.com.</span></span>

  - <span data-ttu-id="c858e-306">Se o cliente tentar todas as entradas armazenadas em cache sem uma conexão bem-sucedida, o usuário será notificado de que nenhum servidor executando o Lync Server 2013 está disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="c858e-306">If the client tries all cached entries without a successful connection, the user is notified that no servers running Lync Server 2013 are available at the moment.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c858e-307">O balanceamento de carga baseado em DNS é diferente do rodízio de DNS (DNS RR) que geralmente se refere ao balanceamento de carga ao confiar no DNS para fornecer uma ordem diferente de endereços IP correspondentes aos servidores em um pool.</span><span class="sxs-lookup"><span data-stu-id="c858e-307">DNS-based load balancing is different from DNS round robin (DNS RR) which typically refers to load balancing by relying on DNS to provide a different order of IP addresses corresponding to the servers in a pool.</span></span> <span data-ttu-id="c858e-308">Normalmente, o RR DNS habilita somente a distribuição de carga, mas não habilita o failover.</span><span class="sxs-lookup"><span data-stu-id="c858e-308">Typically DNS RR only enables load distribution, but does not enable failover.</span></span> <span data-ttu-id="c858e-309">Por exemplo, se a conexão com um endereço IP retornado pela consulta DNS A e AAAA (se você estiver usando endereçamento IPv6) falhar, a conexão falhará.</span><span class="sxs-lookup"><span data-stu-id="c858e-309">For example, if the connection to the one IP address returned by the DNS A and AAAA (if you are using IPv6 addressing) query fails, the connection fails.</span></span> <span data-ttu-id="c858e-310">Portanto, o rodízio de DNS por si só é menos confiável do que o balanceamento de carga baseado em DNS.</span><span class="sxs-lookup"><span data-stu-id="c858e-310">Therefore, DNS round robin by itself is less reliable than DNS-based load balancing.</span></span> <span data-ttu-id="c858e-311">Você pode usar a repetição alternada de DNS em conjunto com o balanceamento de carga de DNS.</span><span class="sxs-lookup"><span data-stu-id="c858e-311">You can use DNS round robin in conjunction with DNS load balancing.</span></span>



</div>

<span data-ttu-id="c858e-312">O balanceamento de carga de DNS é usado para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c858e-312">DNS load balancing is used for the following:</span></span>

  - <span data-ttu-id="c858e-313">Balanceamento de carga do servidor para o servidor SIP para os servidores de borda</span><span class="sxs-lookup"><span data-stu-id="c858e-313">Load balancing server-to-server SIP to the Edge Servers</span></span>

  - <span data-ttu-id="c858e-314">Aplicativos UCAS (serviços de aplicativo de comunicação unificada) de balanceamento de carga, como atendedor automático de conferência, grupo de resposta e estacionamento de chamada</span><span class="sxs-lookup"><span data-stu-id="c858e-314">Load balancing Unified Communications Application Services (UCAS) applications such as Conferencing Auto Attendant, Response Group, and Call Park</span></span>

  - <span data-ttu-id="c858e-315">Evitando novas conexões para aplicativos do UCAS (também conhecido como "descarga")</span><span class="sxs-lookup"><span data-stu-id="c858e-315">Preventing new connections to UCAS applications (also known as "draining")</span></span>

  - <span data-ttu-id="c858e-316">Balanceamento de carga de todo o tráfego de cliente para servidor entre clientes e servidores de borda</span><span class="sxs-lookup"><span data-stu-id="c858e-316">Load balancing all client-to-server traffic between clients and Edge Servers</span></span>

<span data-ttu-id="c858e-317">O balanceamento de carga de DNS não pode ser usado para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c858e-317">DNS load balancing cannot be used for the following:</span></span>

  - <span data-ttu-id="c858e-318">Tráfego da Web de cliente para servidor para director ou servidores front-end</span><span class="sxs-lookup"><span data-stu-id="c858e-318">Client-to-server web traffic to Director or Front End Servers</span></span>

<span data-ttu-id="c858e-319">Balanceamento de carga de DNS e tráfego federado:</span><span class="sxs-lookup"><span data-stu-id="c858e-319">DNS load balancing and federated traffic:</span></span>

<span data-ttu-id="c858e-320">Se vários registros DNS forem retornados por uma consulta de servidor DNS, o serviço de borda de acesso sempre escolhe o registro SRV DNS com a prioridade numérica mais baixa e a espessura numérica mais alta.</span><span class="sxs-lookup"><span data-stu-id="c858e-320">If multiple DNS records are returned by a DNS SRV query, the Access Edge service always picks the DNS SRV record with the lowest numeric priority and highest numeric weight.</span></span> <span data-ttu-id="c858e-321">O documento da Internet Engineering Task Force "um RR DNS para especificar o local dos serviços (DNS SRV)" <http://www.ietf.org/rfc/rfc2782.txt> especifica que, se houver vários registros SRV DNS definidos, a prioridade será usada primeiro e, em seguida, peso.</span><span class="sxs-lookup"><span data-stu-id="c858e-321">The Internet Engineering Task Force document “A DNS RR for specifying the location of services (DNS SRV)” <http://www.ietf.org/rfc/rfc2782.txt> specifies that if there are multiple DNS SRV records defined, priority is first used, then weight.</span></span> <span data-ttu-id="c858e-322">Por exemplo, o registro SRV DNS A tem uma ponderação de 20 e uma prioridade de 40 e o registro SRV DNS B tem uma ponderação de 10 e prioridade de 50.</span><span class="sxs-lookup"><span data-stu-id="c858e-322">For example DNS SRV record A has a weight of 20 and a priority of 40 and DNS SRV record B has a weight of 10 and priority of 50.</span></span> <span data-ttu-id="c858e-323">Registro SRV DNS A with Priority 40 será selecionada.</span><span class="sxs-lookup"><span data-stu-id="c858e-323">DNS SRV record A with priority 40 will be selected.</span></span> <span data-ttu-id="c858e-324">As regras a seguir se aplicam à seleção de registro SRV DNS:</span><span class="sxs-lookup"><span data-stu-id="c858e-324">The following rules apply to DNS SRV record selection:</span></span>

  - <span data-ttu-id="c858e-325">A prioridade é considerada primeiro.</span><span class="sxs-lookup"><span data-stu-id="c858e-325">Priority is considered first.</span></span> <span data-ttu-id="c858e-326">Um cliente deve tentar contatar o host de destino definido pelo registro SRV DNS com o menor prioridade numerada que ele pode alcançar.</span><span class="sxs-lookup"><span data-stu-id="c858e-326">A client MUST attempt to contact the target host defined by the DNS SRV record with the lowest numbered priority it can reach.</span></span> <span data-ttu-id="c858e-327">Os destinos com a mesma prioridade devem ser testados em uma ordem definida pelo campo peso.</span><span class="sxs-lookup"><span data-stu-id="c858e-327">Targets with the same priority SHOULD be tried in an order defined by the weight field.</span></span>

  - <span data-ttu-id="c858e-328">O campo peso especifica um peso relativo para entradas com a mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="c858e-328">The weight field specifies a relative weight for entries with the same priority.</span></span> <span data-ttu-id="c858e-329">Atribuições maiores devem ter uma probabilidade mais alta proporcional mais alta de ser selecionada.</span><span class="sxs-lookup"><span data-stu-id="c858e-329">Larger weights SHOULD be given a proportionately higher probability of being selected.</span></span> <span data-ttu-id="c858e-330">Os administradores de DNS devem usar o peso 0 quando não houver nenhuma seleção de servidor para fazer.</span><span class="sxs-lookup"><span data-stu-id="c858e-330">DNS administrators SHOULD use Weight 0 when there isn’t any server selection to do.</span></span> <span data-ttu-id="c858e-331">Na presença de registros que contêm pesos maiores do que 0, os registros com peso 0 devem ter uma chance muito menor de serem selecionados.</span><span class="sxs-lookup"><span data-stu-id="c858e-331">In the presence of records containing weights greater than 0, records with weight 0 should have a very small chance of being selected.</span></span>

<span data-ttu-id="c858e-332">Se vários registros SRV DNS com prioridade e peso iguais forem retornados, o serviço de borda de acesso selecionará o registro SRV que foi recebido primeiro do servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="c858e-332">If multiple DNS SRV records with equal priority and weight are returned, the Access Edge service will select the SRV record that was received first from the DNS server.</span></span>

<span data-ttu-id="c858e-333"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c858e-333"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

