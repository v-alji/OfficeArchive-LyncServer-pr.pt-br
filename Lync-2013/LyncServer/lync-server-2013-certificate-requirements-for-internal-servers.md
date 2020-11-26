---
title: 'Lync Server 2013: Requisitos de certificado para servidores internos'
description: 'Lync Server 2013: requisitos de certificado para servidores internos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate requirements for internal servers
ms:assetid: 0444cdbd-538c-43b1-b9a1-9d7d6cf818d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398094(v=OCS.15)
ms:contentKeyID: 48183270
ms.date: 02/17/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dc1a627dd762c849b848087a96e00e19d320ef01
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435347"
---
# <a name="certificate-requirements-for-internal-servers-in-lync-server-2013"></a><span data-ttu-id="dae91-103">Requisitos de certificado para servidores internos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dae91-103">Certificate requirements for internal servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dae91-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dae91-104">

<span> </span></span></span>

<span data-ttu-id="dae91-105">_**Tópico da última modificação:** 2017-02-17_</span><span class="sxs-lookup"><span data-stu-id="dae91-105">_**Topic Last Modified:** 2017-02-17_</span></span>

<span data-ttu-id="dae91-106">Os servidores internos que executam o Lync Server e que exigem certificados incluem o servidor Standard Edition, o servidor front-end do Enterprise Edition, o servidor de mediação e o diretor.</span><span class="sxs-lookup"><span data-stu-id="dae91-106">Internal servers that are running Lync Server and that require certificates include Standard Edition server, Enterprise Edition Front End Server, Mediation Server, and Director.</span></span> <span data-ttu-id="dae91-107">A tabela a seguir mostra os requisitos de certificado para esses servidores.</span><span class="sxs-lookup"><span data-stu-id="dae91-107">The following table shows the certificate requirements for these servers.</span></span> <span data-ttu-id="dae91-108">Você pode usar o assistente de certificado do Lync Server para solicitar esses certificados.</span><span class="sxs-lookup"><span data-stu-id="dae91-108">You can use the Lync Server certificate wizard to request these certificates.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="dae91-109">Os certificados curinga são compatíveis com os nomes alternativos de assunto associados às URLs simples no pool de front-end, servidor front-end ou diretor.</span><span class="sxs-lookup"><span data-stu-id="dae91-109">Wildcard certificates are supported for the subject alternative names associated with the simple URLs on the Front End pool, Front End Server, or Director.</span></span> <span data-ttu-id="dae91-110">Para obter detalhes sobre o suporte a certificados curinga, consulte <A href="lync-server-2013-wildcard-certificate-support.md">suporte a certificados curinga no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="dae91-110">For details about wildcard certificate support, see <A href="lync-server-2013-wildcard-certificate-support.md">Wildcard certificate support in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="dae91-111">Embora uma CA (autoridade de certificação) corporativa interna seja recomendada para servidores internos, você também pode usar uma CA pública.</span><span class="sxs-lookup"><span data-stu-id="dae91-111">Although an internal enterprise certification authority (CA) is recommended for internal servers, you can also use a public CA.</span></span> <span data-ttu-id="dae91-112">Para obter uma lista de CAs públicas que fornecem certificados compatíveis com requisitos específicos para certificados de comunicação unificada (UC) e que se associaram à Microsoft para garantir que elas funcionem com o assistente de certificado do Lync Server, consulte o artigo Microsoft Knowledge Base 929395, "parceiros de certificado de comunicação unificada para Exchange Server e para comunicações Server" em [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834) .</span><span class="sxs-lookup"><span data-stu-id="dae91-112">For a list of public CAs that provide certificates that comply with specific requirements for unified communications (UC) certificates and have partnered with Microsoft to ensure they work with the Lync Server Certificate Wizard, see article Microsoft Knowledge Base 929395, "Unified Communications Certificate Partners for Exchange Server and for Communications Server," at [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834).</span></span>

<span data-ttu-id="dae91-113">A comunicação com outros aplicativos e servidores, como o Exchange 2013, requer um certificado que seja compatível com outros aplicativos e produtos.</span><span class="sxs-lookup"><span data-stu-id="dae91-113">Communication with other applications and servers, such as Exchange 2013, requires a certificate that is supported by the other applications and products.</span></span> <span data-ttu-id="dae91-114">Para o lançamento do 2013, Lync Server 2013 e outros produtos do Microsoft Server, incluindo Exchange 2013 e SharePoint Server, suporte ao protocolo de autorização aberta (OAuth) para autenticação e autorização do servidor para servidor.</span><span class="sxs-lookup"><span data-stu-id="dae91-114">For the 2013 release, Lync Server 2013 and other Microsoft server products, including Exchange 2013 and SharePoint Server, support the Open Authorization (OAuth) protocol for server-to-server authentication and authorization.</span></span> <span data-ttu-id="dae91-115">Para obter detalhes, consulte [Gerenciando a autenticação de servidor para servidor (OAuth) e aplicativos de parceiros no Lync server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) na documentação de implantação ou na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="dae91-115">For details, see [Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) in the Deployment documentation or the Operations documentation.</span></span>

<span data-ttu-id="dae91-116">Para conexões de clientes que executam o sistema operacional Windows 7, sistema operacional Windows Server 2008, sistema operacional Windows Server 2008 R2, sistema operacional Windows Vista e Microsoft Lync Phone Edition, Lync Server 2013 inclui suporte para (mas não precisa) de certificados assinados usando a função hash criptográfico SHA-256.</span><span class="sxs-lookup"><span data-stu-id="dae91-116">For connections from clients running Windows 7 operating system, Windows Server 2008 operating system, Windows Server 2008 R2 operating system, Windows Vista operating system, and Microsoft Lync Phone Edition, Lync Server 2013 includes support for (but does not require) certificates signed using the SHA-256 cryptographic hash function.</span></span> <span data-ttu-id="dae91-117">Para dar suporte ao acesso externo usando SHA-256, o certificado externo é emitido por uma autoridade de certificação pública que usa SHA-256.</span><span class="sxs-lookup"><span data-stu-id="dae91-117">To support external access using SHA-256, the external certificate is issued by a public CA using SHA-256.</span></span>

<span data-ttu-id="dae91-118">As tabelas a seguir mostram os requisitos de certificado por função de servidor para os pools front-end e os servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="dae91-118">The following tables show certificate requirements by server role for Front End pools and Standard Edition servers.</span></span> <span data-ttu-id="dae91-119">Todos esses são certificados de servidor Web padrão, chave privada, não-exportável.</span><span class="sxs-lookup"><span data-stu-id="dae91-119">All these are standard web server certificates, private key, non-exportable.</span></span>

<span data-ttu-id="dae91-120">Observe que o uso avançado de chave do servidor (EKU) é automaticamente configurado quando você usa o assistente de certificado para solicitar certificados.</span><span class="sxs-lookup"><span data-stu-id="dae91-120">Note that server enhanced key usage (EKU) is automatically configured when you use the certificate wizard to request certificates.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="dae91-121">Cada nome amigável do certificado deve ser exclusivo na loja do computador.</span><span class="sxs-lookup"><span data-stu-id="dae91-121">Each certificate Friendly Name must be unique in the computer store.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="dae91-122">Se você tiver configurado o sipinternal.contoso.com ou o sipexternal.contoso.com no seu DNS, será necessário adicioná-los ao nome alternativo do requerente do certificado.</span><span class="sxs-lookup"><span data-stu-id="dae91-122">If you have configured sipinternal.contoso.com or sipexternal.contoso.com in your DNS, you will need to add them in the certificate’s Subject Alternative Name.</span></span>



</div>

### <a name="certificates-for-standard-edition-server"></a><span data-ttu-id="dae91-123">Certificados para o servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="dae91-123">Certificates for Standard Edition Server</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dae91-124">Certificado</span><span class="sxs-lookup"><span data-stu-id="dae91-124">Certificate</span></span></th>
<th><span data-ttu-id="dae91-125">Nome do assunto/nome comum</span><span class="sxs-lookup"><span data-stu-id="dae91-125">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="dae91-126">Nome alternativo de entidade</span><span class="sxs-lookup"><span data-stu-id="dae91-126">Subject alternative name</span></span></th>
<th><span data-ttu-id="dae91-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dae91-127">Example</span></span></th>
<th><span data-ttu-id="dae91-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="dae91-128">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dae91-129">Padrão</span><span class="sxs-lookup"><span data-stu-id="dae91-129">Default</span></span></p></td>
<td><p><span data-ttu-id="dae91-130">FQDN (nome de domínio totalmente qualificado) do pool</span><span class="sxs-lookup"><span data-stu-id="dae91-130">Fully qualified domain name (FQDN) of the pool</span></span></p></td>
<td><p><span data-ttu-id="dae91-131">FQDN do pool e do FQDN do servidor</span><span class="sxs-lookup"><span data-stu-id="dae91-131">FQDN of the pool and the FQDN of the server</span></span></p>
<p><span data-ttu-id="dae91-132">Se você tiver vários domínios SIP e tiver habilitado a configuração automática do cliente, o assistente de certificados detectará e adicionará os FQDNs de cada domínio SIP aceito.</span><span class="sxs-lookup"><span data-stu-id="dae91-132">If you have multiple SIP domains and have enabled automatic client configuration, the certificate wizard detects and adds each supported SIP domain FQDNs.</span></span></p>
<p><span data-ttu-id="dae91-133">Se esse pool for o servidor de logon automático para clientes, e a combinação estrita do Sistema de Nome de Domínio (DNS) for exigida na política do grupo, também serão necessárias entradas para o sip.sipdomain (para cada domínio de SIP que você tiver).</span><span class="sxs-lookup"><span data-stu-id="dae91-133">If this pool is the auto-logon server for clients and strict Domain Name System (DNS) matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="dae91-134">SN=se01.contoso.com; SAN=se01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="dae91-134">SN=se01.contoso.com; SAN=se01.contoso.com</span></span></p>
<p><span data-ttu-id="dae91-135">Se esse pool for o servidor de logon automático para clientes, e se a combinação estrita de DNS for exigida na política do grupo, também serão necessários: SAN=sip.contoso.com; SAN=sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="dae91-135">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="dae91-136">No servidor Standard Edition, o FQDN do servidor é o mesmo que o FQDN do pool.</span><span class="sxs-lookup"><span data-stu-id="dae91-136">On Standard Edition server, the server FQDN is the same as the pool FQDN.</span></span></p>
<p><span data-ttu-id="dae91-137">O assistente detecta quaisquer domínios SIP especificados durante a instalação e os adiciona automaticamente ao nome alternativo para a entidade.</span><span class="sxs-lookup"><span data-stu-id="dae91-137">The wizard detects any SIP domains you specified during setup and automatically adds them to the subject alternative name.</span></span></p>
<p><span data-ttu-id="dae91-138">Você também utiliza este certificado para Autenticação de Servidor para Servidor.</span><span class="sxs-lookup"><span data-stu-id="dae91-138">You can also use this certificate for Server-to-Server Authentication.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dae91-139">Web interna</span><span class="sxs-lookup"><span data-stu-id="dae91-139">Web internal</span></span></p></td>
<td><p><span data-ttu-id="dae91-140">FQDN do servidor</span><span class="sxs-lookup"><span data-stu-id="dae91-140">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="dae91-141">Cada um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="dae91-141">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="dae91-142">FQDN de web interna (que é o mesmo que o FQDN do servidor)</span><span class="sxs-lookup"><span data-stu-id="dae91-142">Internal web FQDN (which is the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="dae91-143">Atender a URLs simples</span><span class="sxs-lookup"><span data-stu-id="dae91-143">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="dae91-144">URL simples de discagem</span><span class="sxs-lookup"><span data-stu-id="dae91-144">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="dae91-145">Administrar URL simples</span><span class="sxs-lookup"><span data-stu-id="dae91-145">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="dae91-146">Ou uma entrada curinga para as URLs simples</span><span class="sxs-lookup"><span data-stu-id="dae91-146">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="dae91-147">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="dae91-147">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="dae91-148">Como usar um certificado curinga:</span><span class="sxs-lookup"><span data-stu-id="dae91-148">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="dae91-149">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="dae91-149">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="dae91-150">Não é possível substituir o FQDN da Web interna no construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="dae91-150">You cannot override the Internal web FQDN in Topology Builder.</span></span></p>
<p><span data-ttu-id="dae91-151">Se você tiver várias URLs que atendem a URLs simples, você deve incluir todas elas como nomes alternativos de assunto.</span><span class="sxs-lookup"><span data-stu-id="dae91-151">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="dae91-152">As entradas curinga são suportadas pelas entradas de URL simples.</span><span class="sxs-lookup"><span data-stu-id="dae91-152">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dae91-153">Web externa</span><span class="sxs-lookup"><span data-stu-id="dae91-153">Web external</span></span></p></td>
<td><p><span data-ttu-id="dae91-154">FQDN do servidor</span><span class="sxs-lookup"><span data-stu-id="dae91-154">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="dae91-155">Cada um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="dae91-155">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="dae91-156">FQDN da web externa</span><span class="sxs-lookup"><span data-stu-id="dae91-156">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="dae91-157">URL simples de discagem</span><span class="sxs-lookup"><span data-stu-id="dae91-157">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="dae91-158">Encontre URLs simples por domínio SIP</span><span class="sxs-lookup"><span data-stu-id="dae91-158">Meet simple URLs per SIP domain</span></span></p></li>
<li><p><span data-ttu-id="dae91-159">Ou uma entrada curinga para as URLs simples</span><span class="sxs-lookup"><span data-stu-id="dae91-159">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="dae91-160">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="dae91-160">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="dae91-161">Como usar um certificado curinga:</span><span class="sxs-lookup"><span data-stu-id="dae91-161">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="dae91-162">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="dae91-162">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="dae91-163">Se você tiver várias URLs que atendem a URLs simples, você deve incluir todas elas como nomes alternativos de assunto.</span><span class="sxs-lookup"><span data-stu-id="dae91-163">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="dae91-164">As entradas curinga são suportadas pelas entradas de URL simples.</span><span class="sxs-lookup"><span data-stu-id="dae91-164">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-front-end-server-in-a-front-end-pool"></a><span data-ttu-id="dae91-165">Certificados do servidor front-end em um pool de front-ends</span><span class="sxs-lookup"><span data-stu-id="dae91-165">Certificates for Front End Server in a Front End Pool</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dae91-166">Certificado</span><span class="sxs-lookup"><span data-stu-id="dae91-166">Certificate</span></span></th>
<th><span data-ttu-id="dae91-167">Nome do assunto/nome comum</span><span class="sxs-lookup"><span data-stu-id="dae91-167">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="dae91-168">Nome alternativo de entidade</span><span class="sxs-lookup"><span data-stu-id="dae91-168">Subject alternative name</span></span></th>
<th><span data-ttu-id="dae91-169">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dae91-169">Example</span></span></th>
<th><span data-ttu-id="dae91-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="dae91-170">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dae91-171">Padrão</span><span class="sxs-lookup"><span data-stu-id="dae91-171">Default</span></span></p></td>
<td><p><span data-ttu-id="dae91-172">FQDN do pool</span><span class="sxs-lookup"><span data-stu-id="dae91-172">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="dae91-173">FQDN do pool e FQDN do servidor.</span><span class="sxs-lookup"><span data-stu-id="dae91-173">FQDN of the pool and FQDN of the server.</span></span></p>
<p><span data-ttu-id="dae91-174">Se você tiver vários domínios SIP e tiver habilitado a configuração automática do cliente, o assistente de certificados detectará e adicionará os FQDNs de cada domínio SIP aceito.</span><span class="sxs-lookup"><span data-stu-id="dae91-174">If you have multiple SIP domains and have enabled automatic client configuration, the certificate wizard detects and adds each supported SIP domain FQDNs.</span></span></p>
<p><span data-ttu-id="dae91-175">Se esse pool for o servidor de logon automático para clientes e a correspondência de DNS estrito for necessária na política de grupo, você também precisará de entradas para SIP. sipdomain (para cada domínio SIP que você tiver).</span><span class="sxs-lookup"><span data-stu-id="dae91-175">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="dae91-176">SN=eepool.contoso.com; SAN=eepool.contoso.com; SAN=ee01.contoso.com </span><span class="sxs-lookup"><span data-stu-id="dae91-176">SN=eepool.contoso.com; SAN=eepool.contoso.com; SAN=ee01.contoso.com</span></span></p>
<p><span data-ttu-id="dae91-177">Se esse pool for o servidor de logon automático para clientes, e se a combinação estrita de DNS for exigida na política do grupo, também serão necessários: SAN=sip.contoso.com; SAN=sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="dae91-177">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="dae91-178">O assistente detecta quaisquer domínios SIP especificados durante a instalação e os adiciona automaticamente ao nome alternativo para a entidade.</span><span class="sxs-lookup"><span data-stu-id="dae91-178">The wizard detects any SIP domains you specified during setup and automatically adds them to the subject alternative name.</span></span></p>
<p><span data-ttu-id="dae91-179">Você também utiliza este certificado para Autenticação de Servidor para Servidor.</span><span class="sxs-lookup"><span data-stu-id="dae91-179">You can also use this certificate for Server-to-Server Authentication.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dae91-180">Web Internal</span><span class="sxs-lookup"><span data-stu-id="dae91-180">Web Internal</span></span></p></td>
<td><p><span data-ttu-id="dae91-181">FQDN do pool</span><span class="sxs-lookup"><span data-stu-id="dae91-181">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="dae91-182">Cada um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="dae91-182">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="dae91-183">FQDN da Web interna (que NÃO é igual ao FQDN do servidor)</span><span class="sxs-lookup"><span data-stu-id="dae91-183">Internal web FQDN (which is NOT the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="dae91-184">FQDN do servidor</span><span class="sxs-lookup"><span data-stu-id="dae91-184">Server FQDN</span></span></p></li>
<li><p><span data-ttu-id="dae91-185">FQDN do pool do Lync</span><span class="sxs-lookup"><span data-stu-id="dae91-185">Lync pool FQDN</span></span></p></li>
<li><p><span data-ttu-id="dae91-186">Atender a URLs simples</span><span class="sxs-lookup"><span data-stu-id="dae91-186">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="dae91-187">URL simples de discagem</span><span class="sxs-lookup"><span data-stu-id="dae91-187">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="dae91-188">Administrar URL simples</span><span class="sxs-lookup"><span data-stu-id="dae91-188">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="dae91-189">Ou uma entrada curinga para as URLs simples</span><span class="sxs-lookup"><span data-stu-id="dae91-189">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="dae91-190">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="dae91-190">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="dae91-191">Como usar um certificado curinga:</span><span class="sxs-lookup"><span data-stu-id="dae91-191">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="dae91-192">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="dae91-192">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="dae91-193">Se você tiver várias URLs que atendem a URLs simples, você deve incluir todas elas como nomes alternativos de assunto.</span><span class="sxs-lookup"><span data-stu-id="dae91-193">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="dae91-194">As entradas curinga são suportadas pelas entradas de URL simples.</span><span class="sxs-lookup"><span data-stu-id="dae91-194">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dae91-195">Web externa</span><span class="sxs-lookup"><span data-stu-id="dae91-195">Web external</span></span></p></td>
<td><p><span data-ttu-id="dae91-196">FQDN do pool</span><span class="sxs-lookup"><span data-stu-id="dae91-196">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="dae91-197">Cada um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="dae91-197">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="dae91-198">FQDN da web externa</span><span class="sxs-lookup"><span data-stu-id="dae91-198">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="dae91-199">URL simples de discagem</span><span class="sxs-lookup"><span data-stu-id="dae91-199">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="dae91-200">Administrar URL simples</span><span class="sxs-lookup"><span data-stu-id="dae91-200">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="dae91-201">Ou uma entrada curinga para as URLs simples</span><span class="sxs-lookup"><span data-stu-id="dae91-201">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="dae91-202">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="dae91-202">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="dae91-203">Como usar um certificado curinga:</span><span class="sxs-lookup"><span data-stu-id="dae91-203">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="dae91-204">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="dae91-204">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="dae91-205">Se você tiver várias URLs que atendem a URLs simples, você deve incluir todas elas como nomes alternativos de assunto.</span><span class="sxs-lookup"><span data-stu-id="dae91-205">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="dae91-206">As entradas curinga são suportadas pelas entradas de URL simples.</span><span class="sxs-lookup"><span data-stu-id="dae91-206">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-director"></a><span data-ttu-id="dae91-207">Certificados para o diretor</span><span class="sxs-lookup"><span data-stu-id="dae91-207">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dae91-208">Certificado</span><span class="sxs-lookup"><span data-stu-id="dae91-208">Certificate</span></span></th>
<th><span data-ttu-id="dae91-209">Nome do assunto/nome comum</span><span class="sxs-lookup"><span data-stu-id="dae91-209">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="dae91-210">Nome alternativo de entidade</span><span class="sxs-lookup"><span data-stu-id="dae91-210">Subject alternative name</span></span></th>
<th><span data-ttu-id="dae91-211">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dae91-211">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dae91-212">Padrão</span><span class="sxs-lookup"><span data-stu-id="dae91-212">Default</span></span></p></td>
<td><p><span data-ttu-id="dae91-213">FQDN do pool de diretor</span><span class="sxs-lookup"><span data-stu-id="dae91-213">FQDN of the Director pool</span></span></p></td>
<td><p><span data-ttu-id="dae91-214">FQDN do diretor, FQDN do pool de diretor</span><span class="sxs-lookup"><span data-stu-id="dae91-214">FQDN of the Director, FQDN of the Director pool</span></span></p>
<p><span data-ttu-id="dae91-215">Se esse pool for o servidor de logon automático para clientes e a correspondência de DNS estrito for necessária na política de grupo, você também precisará de entradas para SIP. sipdomain (para cada domínio SIP que você tiver).</span><span class="sxs-lookup"><span data-stu-id="dae91-215">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="dae91-216">SN = dir-pool.contoso.com; SAN = dir-pool.contoso.com; SAN = dir01. contoso. com</span><span class="sxs-lookup"><span data-stu-id="dae91-216">SN=dir-pool.contoso.com; SAN=dir-pool.contoso.com; SAN=dir01.contoso.com</span></span></p>
<p><span data-ttu-id="dae91-217">Se esse pool de diretor for o servidor de logon automático para clientes e a correspondência de DNS estrito for necessária na política de grupo, você também precisará de SAN = SIP. contoso. com; SAN = SIP. fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="dae91-217">If this Director pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dae91-218">Web Internal</span><span class="sxs-lookup"><span data-stu-id="dae91-218">Web Internal</span></span></p></td>
<td><p><span data-ttu-id="dae91-219">FQDN do servidor</span><span class="sxs-lookup"><span data-stu-id="dae91-219">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="dae91-220">Cada um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="dae91-220">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="dae91-221">FQDN de web interna (que é o mesmo que o FQDN do servidor)</span><span class="sxs-lookup"><span data-stu-id="dae91-221">Internal web FQDN (which is the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="dae91-222">FQDN do servidor</span><span class="sxs-lookup"><span data-stu-id="dae91-222">Server FQDN</span></span></p></li>
<li><p><span data-ttu-id="dae91-223">FQDN do pool do Lync</span><span class="sxs-lookup"><span data-stu-id="dae91-223">Lync pool FQDN</span></span></p></li>
<li><p><span data-ttu-id="dae91-224">Atender a URLs simples</span><span class="sxs-lookup"><span data-stu-id="dae91-224">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="dae91-225">URL simples de discagem</span><span class="sxs-lookup"><span data-stu-id="dae91-225">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="dae91-226">Administrar URL simples</span><span class="sxs-lookup"><span data-stu-id="dae91-226">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="dae91-227">Ou uma entrada curinga para as URLs simples</span><span class="sxs-lookup"><span data-stu-id="dae91-227">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="dae91-228">SN=dir01.contoso.com; SAN=dir01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="dae91-228">SN=dir01.contoso.com; SAN=dir01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="dae91-229">SN=dir01.contoso.com; SAN=dir01.contoso.com SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="dae91-229">SN=dir01.contoso.com; SAN=dir01.contoso.com SAN=\*.contoso.com</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dae91-230">Web externa</span><span class="sxs-lookup"><span data-stu-id="dae91-230">Web external</span></span></p></td>
<td><p><span data-ttu-id="dae91-231">FQDN do servidor</span><span class="sxs-lookup"><span data-stu-id="dae91-231">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="dae91-232">Cada um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="dae91-232">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="dae91-233">FQDN da web externa</span><span class="sxs-lookup"><span data-stu-id="dae91-233">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="dae91-234">URL simples de discagem</span><span class="sxs-lookup"><span data-stu-id="dae91-234">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="dae91-235">Administrar URL simples</span><span class="sxs-lookup"><span data-stu-id="dae91-235">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="dae91-236">Ou uma entrada curinga para as URLs simples</span><span class="sxs-lookup"><span data-stu-id="dae91-236">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="dae91-237">O FQDN da Web externa do diretor deve ser diferente do pool de front-end ou do servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="dae91-237">The Director external web FQDN must be different from the Front End pool or Front End Server.</span></span></p>
<p><span data-ttu-id="dae91-238">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="dae91-238">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="dae91-239">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="dae91-239">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=\*.contoso.com</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dae91-240">Se você tiver um pool autônomo do servidor de mediação, os servidores de mediação em cada um precisam dos certificados listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dae91-240">If you have a stand-alone Mediation Server pool, the Mediation Servers in it each need the certificates listed in the following table.</span></span> <span data-ttu-id="dae91-241">Se você colocar o servidor de mediação com os servidores front end, os certificados listados na tabela "certificados para servidor front-end no pool Front-End", anteriormente neste tópico, serão suficientes.</span><span class="sxs-lookup"><span data-stu-id="dae91-241">If you collocate Mediation Server with the Front End Servers, the certificates listed in the “Certificates for Front End Server in Front End Pool” table earlier in this topic are sufficient.</span></span>

### <a name="certificates-for-stand-alone-mediation-server"></a><span data-ttu-id="dae91-242">Certificados para servidor de mediação autônomo</span><span class="sxs-lookup"><span data-stu-id="dae91-242">Certificates for Stand-alone Mediation Server</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dae91-243">Certificado</span><span class="sxs-lookup"><span data-stu-id="dae91-243">Certificate</span></span></th>
<th><span data-ttu-id="dae91-244">Nome do assunto/nome comum</span><span class="sxs-lookup"><span data-stu-id="dae91-244">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="dae91-245">Nome alternativo de entidade</span><span class="sxs-lookup"><span data-stu-id="dae91-245">Subject alternative name</span></span></th>
<th><span data-ttu-id="dae91-246">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dae91-246">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dae91-247">Padrão</span><span class="sxs-lookup"><span data-stu-id="dae91-247">Default</span></span></p></td>
<td><p><span data-ttu-id="dae91-248">FQDN do pool</span><span class="sxs-lookup"><span data-stu-id="dae91-248">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="dae91-249">FQDN do pool</span><span class="sxs-lookup"><span data-stu-id="dae91-249">FQDN of the pool</span></span></p>
<p><span data-ttu-id="dae91-250">FQDN do servidor membro do pool</span><span class="sxs-lookup"><span data-stu-id="dae91-250">FQDN of pool member server</span></span></p></td>
<td><p><span data-ttu-id="dae91-251">SN=medsvr-pool.contoso.net; SAN=medsvr-pool.contoso.net; SAN=medsvr01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="dae91-251">SN=medsvr-pool.contoso.net; SAN=medsvr-pool.contoso.net; SAN=medsvr01.contoso.net</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-survivable-branch-appliance"></a><span data-ttu-id="dae91-252">Certificados para aparelho de ramificação sobreviventes</span><span class="sxs-lookup"><span data-stu-id="dae91-252">Certificates for Survivable Branch Appliance</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dae91-253">Certificado</span><span class="sxs-lookup"><span data-stu-id="dae91-253">Certificate</span></span></th>
<th><span data-ttu-id="dae91-254">Nome do assunto/nome comum</span><span class="sxs-lookup"><span data-stu-id="dae91-254">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="dae91-255">Nome alternativo de entidade</span><span class="sxs-lookup"><span data-stu-id="dae91-255">Subject alternative name</span></span></th>
<th><span data-ttu-id="dae91-256">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dae91-256">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dae91-257">Padrão</span><span class="sxs-lookup"><span data-stu-id="dae91-257">Default</span></span></p></td>
<td><p><span data-ttu-id="dae91-258">FQDN do aplicativo</span><span class="sxs-lookup"><span data-stu-id="dae91-258">FQDN of the appliance</span></span></p></td>
<td><p><span data-ttu-id="dae91-259">SIP. &lt; sipdomain &gt; (precisa de uma entrada por domínio SIP)</span><span class="sxs-lookup"><span data-stu-id="dae91-259">SIP.&lt;sipdomain&gt; (need one entry per SIP domain)</span></span></p></td>
<td><p><span data-ttu-id="dae91-260">SN=sba01.contoso.net; SAN=sip.contoso.com; SAN=sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="dae91-260">SN=sba01.contoso.net; SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="dae91-261">Confira também</span><span class="sxs-lookup"><span data-stu-id="dae91-261">See Also</span></span>


[<span data-ttu-id="dae91-262">Suporte a certificado curinga no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dae91-262">Wildcard certificate support in Lync Server 2013</span></span>](lync-server-2013-wildcard-certificate-support.md)  
  

<span data-ttu-id="dae91-263"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dae91-263"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

