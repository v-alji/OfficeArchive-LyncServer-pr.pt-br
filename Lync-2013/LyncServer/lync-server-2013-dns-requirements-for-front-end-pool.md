---
title: 'Lync Server 2013: Requisitos DNS para pool de Front-Ends'
description: 'Lync Server 2013: requisitos de DNS para o pool de front-ends.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pool
ms:assetid: 02d2aa6b-9e01-437b-a2df-00590280150d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398082(v=OCS.15)
ms:contentKeyID: 48183249
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bfce90eccb8c8dff94d4122c96c4ca68ea9150f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437823"
---
# <a name="dns-requirements-for-front-end-pool-in-lync-server-2013"></a><span data-ttu-id="c61fb-103">Requisitos DNS para pool de Front-Ends no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c61fb-103">DNS requirements for Front End pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c61fb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c61fb-104">

<span> </span></span></span>

<span data-ttu-id="c61fb-105">_**Tópico da última modificação:** 2012-11-07_</span><span class="sxs-lookup"><span data-stu-id="c61fb-105">_**Topic Last Modified:** 2012-11-07_</span></span>

<span data-ttu-id="c61fb-106">Para concluir esse procedimento com êxito, você deve estar conectado ao servidor ou domínio minimamente como membro do grupo Domain admins ou um membro do grupo DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="c61fb-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="c61fb-107">Você precisa configurar os registros de sistema de nomes de domínio (DNS) necessários antes de publicar sua topologia no construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="c61fb-107">You need to configure the required Domain Name System (DNS) records prior to publishing your topology in Topology Builder.</span></span> <span data-ttu-id="c61fb-108">Além disso, alguns dos FQDNs (nomes de domínio totalmente qualificados) usados na configuração de uma implantação do Lync Server 2013 são FQDNs lógicos e não físicos do servidor, portanto a configuração DNS adicional é necessária antes da publicação.</span><span class="sxs-lookup"><span data-stu-id="c61fb-108">Additionally, some of the fully qualified domain names (FQDNs) used in the configuration of a Lync Server 2013 deployment are logical and not physical server FQDNs, so additional DNS configuration is required prior to publishing.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="c61fb-109">O Lync Server 2013 não é compatível com domínios com rótulo único.</span><span class="sxs-lookup"><span data-stu-id="c61fb-109">Lync Server 2013 does not support single-labeled domains.</span></span> <span data-ttu-id="c61fb-110">Por exemplo, uma floresta com um domínio raiz chamado <STRONG>contoso. local</STRONG> tem suporte, mas não há suporte para um domínio raiz chamado <STRONG>local</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="c61fb-110">For example, a forest with a root domain named <STRONG>contoso.local</STRONG> is supported, but a root domain named <STRONG>local</STRONG> is not supported.</span></span> <span data-ttu-id="c61fb-111">Para obter detalhes, consulte o artigo 300684 da base de dados de conhecimento Microsoft "informações sobre como configurar o Windows para domínios com nomes DNS de rótulo único" em <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=300684"> https://go.microsoft.com/fwlink/p/?linkid=3052&amp ; kbid = 300684</A>.</span><span class="sxs-lookup"><span data-stu-id="c61fb-111">For details, see Microsoft Knowledge Base article 300684, “Information about configuring Windows for domains with single-label DNS names,” at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=300684">https://go.microsoft.com/fwlink/p/?linkid=3052&amp;kbid=300684</A>.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c61fb-112">O nome que você especificar dever ser idêntico ao nome de computador configurado no servidor.</span><span class="sxs-lookup"><span data-stu-id="c61fb-112">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="c61fb-113">Por padrão, o nome do computador de um computador que não está associado a um domínio é um nome curto, e não um FQDN.</span><span class="sxs-lookup"><span data-stu-id="c61fb-113">By default the computer name of a computer that is not joined to a domain is a short name, not an FQDN.</span></span> <span data-ttu-id="c61fb-114">O Construtor de Topologias usa FQDNs, não nomes curtos.</span><span class="sxs-lookup"><span data-stu-id="c61fb-114">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="c61fb-115"><STRONG>Use somente caracteres padrão</STRONG> (incluindo a – Z, A – z, 0 – 9 e hifens) ao atribuir FQDNs de seus servidores que executam o Lync Server, servidores de borda e pools.</span><span class="sxs-lookup"><span data-stu-id="c61fb-115"><STRONG>Use only standard characters</STRONG> (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your servers running Lync Server, Edge Servers, and pools.</span></span> <span data-ttu-id="c61fb-116">Não use caracteres Unicode ou sublinhados.</span><span class="sxs-lookup"><span data-stu-id="c61fb-116">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="c61fb-117">Os caracteres não padrão em um FQDN geralmente não são compatíveis com o DNS externo e as autoridades de certificação pública (CAs) (quando o FQDN deve ser atribuído ao SN no certificado).</span><span class="sxs-lookup"><span data-stu-id="c61fb-117">Nonstandard characters in an FQDN are often not supported by external DNS and public certification authorities (CAs) (when the FQDN must be assigned to the SN in the certificate).</span></span>



</div>

<span data-ttu-id="c61fb-118">Antes de operar a topologia após a implantação, certifique-se de que os seguintes registros de DNS e do Active Directory sejam criados (conforme suas necessidades para recursos específicos exigirem):</span><span class="sxs-lookup"><span data-stu-id="c61fb-118">Prior to operating the topology after it has been deployed, ensure that the following Active Directory and DNS records are created (as your needs for specific features dictate):</span></span>

  - <span data-ttu-id="c61fb-119">Cada função de servidor que existirá na topologia será publicada como um objeto do Active Directory (o ingresso no computador para o domínio vai conseguir isso).</span><span class="sxs-lookup"><span data-stu-id="c61fb-119">Each server role that will exist in the topology is published as an Active Directory object (joining the computer to the domain will accomplish this).</span></span>

  - <span data-ttu-id="c61fb-120">Existe um registro DNS A para cada servidor.</span><span class="sxs-lookup"><span data-stu-id="c61fb-120">A DNS A Record exists for each server.</span></span>

  - <span data-ttu-id="c61fb-121">Um registro SRV DNS existe para cada domínio SIP se você planeja usar o logon automático para clientes na forma de \_ sipinternaltls \_ TCP. \<SIP domain\> .</span><span class="sxs-lookup"><span data-stu-id="c61fb-121">A DNS SRV Record exists for each SIP domain if you plan to use automatic logon for clients in the form of \_sipinternaltls\_tcp.\<SIP domain\>.</span></span> <span data-ttu-id="c61fb-122">Se você usar a configuração manual para clientes, esse registro não será necessário.</span><span class="sxs-lookup"><span data-stu-id="c61fb-122">If you will use manual configuration for clients, this record is not necessary.</span></span>

  - <span data-ttu-id="c61fb-123">Um registro de DNS A para cada URL simples configurada, do qual há geralmente quatro: atender, dial-in, LWA e scheduler.</span><span class="sxs-lookup"><span data-stu-id="c61fb-123">A DNS A Record for each configured simple URL, of which there are typically four: meet, dialin, lwa, and scheduler.</span></span> <span data-ttu-id="c61fb-124">Além disso, há a URL simples do administrador, que é uma URL especial para acessar o painel de controle do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c61fb-124">Additionally, there is the admin simple URL which is a special URL for access to the Lync Server 2013 Control Panel.</span></span>

  - <span data-ttu-id="c61fb-125">O servidor que executa o SQL Server deve estar associado ao domínio e alcançável pelo computador do qual o construtor de topologias está publicando.</span><span class="sxs-lookup"><span data-stu-id="c61fb-125">The server running SQL Server must be joined to the domain, and reachable by the computer that Topology Builder is publishing from.</span></span>

<span data-ttu-id="c61fb-126">A tabela segue as arquiteturas de referência apresentadas na seção planejamento.</span><span class="sxs-lookup"><span data-stu-id="c61fb-126">The table follows the reference architectures presented in the Planning section.</span></span> <span data-ttu-id="c61fb-127">Para obter detalhes, consulte [cenários para acesso de usuários externos no Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="c61fb-127">For details, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) in the Planning documentation.</span></span>

<div id="sectionSection0" class="section">

### <a name="dns-records-required-for-the-front-end-pool"></a><span data-ttu-id="c61fb-128">Registros DNS necessários para o pool de front-ends</span><span class="sxs-lookup"><span data-stu-id="c61fb-128">DNS Records Required for the Front End pool</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c61fb-129">Local</span><span class="sxs-lookup"><span data-stu-id="c61fb-129">Location</span></span></th>
<th><span data-ttu-id="c61fb-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="c61fb-130">Type</span></span></th>
<th><span data-ttu-id="c61fb-131">FQDN</span><span class="sxs-lookup"><span data-stu-id="c61fb-131">FQDN</span></span></th>
<th><span data-ttu-id="c61fb-132">Mapas para/comentários</span><span class="sxs-lookup"><span data-stu-id="c61fb-132">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c61fb-133">DNS Interno</span><span class="sxs-lookup"><span data-stu-id="c61fb-133">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="c61fb-134">A</span><span class="sxs-lookup"><span data-stu-id="c61fb-134">A</span></span></p></td>
<td><p><span data-ttu-id="c61fb-135">pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="c61fb-135">pool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="c61fb-136">Pool01 (balanceamento de carga de DNS).</span><span class="sxs-lookup"><span data-stu-id="c61fb-136">Pool01 (DNS load balancing).</span></span> <span data-ttu-id="c61fb-137">Requer um registro DNS A para o endereço IP de cada servidor front-end dentro do pool, mapeando para o pool FQDN.</span><span class="sxs-lookup"><span data-stu-id="c61fb-137">Requires a DNS A record for the IP address of each Front End Server within the pool, mapping to the pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c61fb-138">DNS Interno</span><span class="sxs-lookup"><span data-stu-id="c61fb-138">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="c61fb-139">A</span><span class="sxs-lookup"><span data-stu-id="c61fb-139">A</span></span></p></td>
<td><p><span data-ttu-id="c61fb-140">pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="c61fb-140">pool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="c61fb-141">Pool01 (VIP (IP virtual) do balanceador de carga de hardware).</span><span class="sxs-lookup"><span data-stu-id="c61fb-141">Pool01 (virtual IP (VIP) of hardware load balancer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c61fb-142">DNS Interno</span><span class="sxs-lookup"><span data-stu-id="c61fb-142">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="c61fb-143">A</span><span class="sxs-lookup"><span data-stu-id="c61fb-143">A</span></span></p></td>
<td><p><span data-ttu-id="c61fb-144">fe01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="c61fb-144">fe01.contoso.net</span></span></p>
<p><span data-ttu-id="c61fb-145">fe02.contoso.net</span><span class="sxs-lookup"><span data-stu-id="c61fb-145">fe02.contoso.net</span></span></p>
<p><span data-ttu-id="c61fb-146">fe03.contoso.net</span><span class="sxs-lookup"><span data-stu-id="c61fb-146">fe03.contoso.net</span></span></p>
<p><span data-ttu-id="c61fb-147">…</span><span class="sxs-lookup"><span data-stu-id="c61fb-147">…</span></span></p></td>
<td><p><span data-ttu-id="c61fb-148">Servidor front-end Pool01 (nó 1).</span><span class="sxs-lookup"><span data-stu-id="c61fb-148">Pool01 Front End Server (NODE 1).</span></span></p>
<p><span data-ttu-id="c61fb-149">Servidor front-end Pool01 (nó 2).</span><span class="sxs-lookup"><span data-stu-id="c61fb-149">Pool01 Front End Server (NODE 2).</span></span></p>
<p><span data-ttu-id="c61fb-150">Servidor front-end Pool01 (nó 3).</span><span class="sxs-lookup"><span data-stu-id="c61fb-150">Pool01 Front End Server (NODE 3).</span></span></p>
<p><span data-ttu-id="c61fb-151">…</span><span class="sxs-lookup"><span data-stu-id="c61fb-151">…</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c61fb-152">DNS Interno</span><span class="sxs-lookup"><span data-stu-id="c61fb-152">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="c61fb-153">A</span><span class="sxs-lookup"><span data-stu-id="c61fb-153">A</span></span></p></td>
<td><p><span data-ttu-id="c61fb-154">fe02.contoso.net</span><span class="sxs-lookup"><span data-stu-id="c61fb-154">fe02.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="c61fb-155">Servidor front-end Pool01 (nó 2).</span><span class="sxs-lookup"><span data-stu-id="c61fb-155">Pool01 Front End Server (NODE 2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c61fb-156">DNS Interno</span><span class="sxs-lookup"><span data-stu-id="c61fb-156">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="c61fb-157">A</span><span class="sxs-lookup"><span data-stu-id="c61fb-157">A</span></span></p></td>
<td><p><span data-ttu-id="c61fb-158">lsweb.contoso.net</span><span class="sxs-lookup"><span data-stu-id="c61fb-158">lsweb.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="c61fb-159">Pool01 (VIP) para tráfego da Web de cliente para servidor.</span><span class="sxs-lookup"><span data-stu-id="c61fb-159">Pool01 (VIP) for client-to-server web traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c61fb-160">DNS Interno</span><span class="sxs-lookup"><span data-stu-id="c61fb-160">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="c61fb-161">A</span><span class="sxs-lookup"><span data-stu-id="c61fb-161">A</span></span></p></td>
<td><p><span data-ttu-id="c61fb-162">sqlbe.contoso.net</span><span class="sxs-lookup"><span data-stu-id="c61fb-162">sqlbe.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="c61fb-163">Pool01 back-end Server executando o SQL Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c61fb-163">Pool01 Back End Server running SQL Server 2008 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c61fb-164">DNS Interno</span><span class="sxs-lookup"><span data-stu-id="c61fb-164">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="c61fb-165">A</span><span class="sxs-lookup"><span data-stu-id="c61fb-165">A</span></span></p></td>
<td><p><span data-ttu-id="c61fb-166">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c61fb-166">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c61fb-167">Necessário para o Lync Phone Edition ou o logon automático de clientes sem registros SRV DNS e para correspondência de domínio estrito.</span><span class="sxs-lookup"><span data-stu-id="c61fb-167">Required for Lync Phone Edition, or automatic logon of clients without DNS SRV records, and for strict domain matching.</span></span> <span data-ttu-id="c61fb-168">Não é necessário em todos os casos.</span><span class="sxs-lookup"><span data-stu-id="c61fb-168">Not required in all cases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c61fb-169">DNS Interno</span><span class="sxs-lookup"><span data-stu-id="c61fb-169">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="c61fb-170">A</span><span class="sxs-lookup"><span data-stu-id="c61fb-170">A</span></span></p></td>
<td><p><span data-ttu-id="c61fb-171">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="c61fb-171">sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="c61fb-172">Assume um segundo domínio SIP.</span><span class="sxs-lookup"><span data-stu-id="c61fb-172">Assumes a second SIP domain.</span></span> <span data-ttu-id="c61fb-173">Obrigatório para o Lync Phone Edition, o logon automático de clientes sem registros SRV DNS e para correspondência de domínio estrito.</span><span class="sxs-lookup"><span data-stu-id="c61fb-173">Required for Lync Phone Edition, automatic logon of clients without DNS SRV records, and for strict domain matching.</span></span> <span data-ttu-id="c61fb-174">Não é necessário em todos os casos.</span><span class="sxs-lookup"><span data-stu-id="c61fb-174">Not required in all cases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c61fb-175">DNS Interno</span><span class="sxs-lookup"><span data-stu-id="c61fb-175">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="c61fb-176">A</span><span class="sxs-lookup"><span data-stu-id="c61fb-176">A</span></span></p></td>
<td><p><span data-ttu-id="c61fb-177">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c61fb-177">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c61fb-178">URL simples para conferência discada publicada internamente – o servidor front-end (ou diretor, se instalado) responderá a consultas de URL simples.</span><span class="sxs-lookup"><span data-stu-id="c61fb-178">Simple URL for dial-in conferencing published internally – Front End Server (or Director, if installed) responds to simple URL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c61fb-179">DNS Interno</span><span class="sxs-lookup"><span data-stu-id="c61fb-179">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="c61fb-180">A</span><span class="sxs-lookup"><span data-stu-id="c61fb-180">A</span></span></p></td>
<td><p><span data-ttu-id="c61fb-181">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c61fb-181">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c61fb-182">URL simples para conferências publicadas internamente – front-end Server (ou director, se instalado) responde a consultas de URL simples.</span><span class="sxs-lookup"><span data-stu-id="c61fb-182">Simple URL for conferences published internally – Front End Server (or Director, if installed) responds to simple URL queries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c61fb-183">DNS Interno</span><span class="sxs-lookup"><span data-stu-id="c61fb-183">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="c61fb-184">A</span><span class="sxs-lookup"><span data-stu-id="c61fb-184">A</span></span></p></td>
<td><p><span data-ttu-id="c61fb-185">admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c61fb-185">admin.contoso.com</span></span></p>
<p><span data-ttu-id="c61fb-186">locatário</span><span class="sxs-lookup"><span data-stu-id="c61fb-186">admin</span></span></p></td>
<td><p><span data-ttu-id="c61fb-187">Registro opcional, URL simples para o painel de controle do Lync Server 2013 publicada internamente – o servidor front-end (ou director, se instalado) responde às consultas de URL simples.</span><span class="sxs-lookup"><span data-stu-id="c61fb-187">Optional record, simple URL for Lync Server 2013 Control Panel published internally - Front End Server (or Director, if installed) responds to simple URL queries.</span></span> <span data-ttu-id="c61fb-188">Somente nome do host (nenhum nome de domínio) é recomendado.</span><span class="sxs-lookup"><span data-stu-id="c61fb-188">Host name only (no domain name) is recommended.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="c61fb-189">VIP = endereço IP virtual para balanceador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="c61fb-189">VIP = Virtual IP address for hardware load balancer</span></span>



</div>

</div>

<div>

## <a name="dns-srv-records-for-the-front-end-pool"></a><span data-ttu-id="c61fb-190">Registros SRV DNS para o pool de front-ends</span><span class="sxs-lookup"><span data-stu-id="c61fb-190">DNS SRV Records for the Front End pool</span></span>


<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c61fb-191">Local</span><span class="sxs-lookup"><span data-stu-id="c61fb-191">Location</span></span></th>
<th><span data-ttu-id="c61fb-192">Tipo</span><span class="sxs-lookup"><span data-stu-id="c61fb-192">Type</span></span></th>
<th><span data-ttu-id="c61fb-193">FQDN</span><span class="sxs-lookup"><span data-stu-id="c61fb-193">FQDN</span></span></th>
<th><span data-ttu-id="c61fb-194">FQDN de destino</span><span class="sxs-lookup"><span data-stu-id="c61fb-194">Target FQDN</span></span></th>
<th><span data-ttu-id="c61fb-195">Porta</span><span class="sxs-lookup"><span data-stu-id="c61fb-195">Port</span></span></th>
<th><span data-ttu-id="c61fb-196">Mapas para/comentários</span><span class="sxs-lookup"><span data-stu-id="c61fb-196">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c61fb-197">DNS Interno</span><span class="sxs-lookup"><span data-stu-id="c61fb-197">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="c61fb-198">SRV</span><span class="sxs-lookup"><span data-stu-id="c61fb-198">SRV</span></span></p></td>
<td><p><span data-ttu-id="c61fb-199">_sipinternaltls _sipinternaltls._tcp. contoso. com</span><span class="sxs-lookup"><span data-stu-id="c61fb-199">_sipinternaltls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c61fb-200">pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c61fb-200">pool01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c61fb-201">5061</span><span class="sxs-lookup"><span data-stu-id="c61fb-201">5061</span></span></p></td>
<td><p><span data-ttu-id="c61fb-202">Obrigatório para a configuração automática de clientes do Lync 2013 trabalhar internamente.</span><span class="sxs-lookup"><span data-stu-id="c61fb-202">Required for automatic configuration of Lync 2013 clients to work internally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c61fb-203">DNS Interno</span><span class="sxs-lookup"><span data-stu-id="c61fb-203">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="c61fb-204">SRV</span><span class="sxs-lookup"><span data-stu-id="c61fb-204">SRV</span></span></p></td>
<td><p><span data-ttu-id="c61fb-205">_sipinternaltls _sipinternaltls._tcp. fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="c61fb-205">_sipinternaltls._tcp.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="c61fb-206">pool01.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="c61fb-206">pool01.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="c61fb-207">5061</span><span class="sxs-lookup"><span data-stu-id="c61fb-207">5061</span></span></p></td>
<td><p><span data-ttu-id="c61fb-208">Obrigatório para a configuração automática de clientes do Lync 2013 trabalhar internamente.</span><span class="sxs-lookup"><span data-stu-id="c61fb-208">Required for automatic configuration of Lync 2013 clients to work internally.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c61fb-209">DNS Interno</span><span class="sxs-lookup"><span data-stu-id="c61fb-209">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="c61fb-210">SRV</span><span class="sxs-lookup"><span data-stu-id="c61fb-210">SRV</span></span></p></td>
<td><p><span data-ttu-id="c61fb-211">_ntp._udp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c61fb-211">_ntp._udp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c61fb-212">dc01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c61fb-212">dc01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="c61fb-213">123</span><span class="sxs-lookup"><span data-stu-id="c61fb-213">123</span></span></p></td>
<td><p><span data-ttu-id="c61fb-214">Fonte de protocolo de tempo de rede (NTP) necessária para dispositivos que executam o Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="c61fb-214">Network Time Protocol (NTP) source required for devices running Lync Phone Edition.</span></span> <span data-ttu-id="c61fb-215">Internamente, isso deve apontar para o controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="c61fb-215">Internally, this should point to the domain controller.</span></span> <span data-ttu-id="c61fb-216">Se o controlador de domínio não estiver definido, ele tentará usar o servidor NTP time.windows.com.</span><span class="sxs-lookup"><span data-stu-id="c61fb-216">If the domain controller is not defined, it will try to use the NTP server time.windows.com.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c61fb-217">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c61fb-217">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

