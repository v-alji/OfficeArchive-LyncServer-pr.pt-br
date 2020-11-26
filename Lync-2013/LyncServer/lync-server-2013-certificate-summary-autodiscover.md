---
title: 'Lync Server 2013: Resumo do certificado-descoberta automática'
description: 'Lync Server 2013: Resumo do certificado-descoberta automática.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Autodiscover
ms:assetid: 16ac96bb-882a-4141-b75c-9530637548d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945616(v=OCS.15)
ms:contentKeyID: 51541451
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae421401421434a4c4069c1d90ee287dfb016997
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435345"
---
# <a name="certificate-summary---autodiscover-in-lync-server-2013"></a><span data-ttu-id="f21ad-103">Resumo do certificado-descoberta automática no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f21ad-103">Certificate summary - Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f21ad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f21ad-104">

<span> </span></span></span>

<span data-ttu-id="f21ad-105">_**Tópico da última modificação:** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="f21ad-105">_**Topic Last Modified:** 2013-02-14_</span></span>

<span data-ttu-id="f21ad-106">O serviço de descoberta automática do Lync Server 2013 é executado nos servidores do diretor e do pool de front-end e, quando publicados no DNS, pode ser usado pelos clientes do Lync para localizar serviços de servidor e usuário.</span><span class="sxs-lookup"><span data-stu-id="f21ad-106">The Lync Server 2013 Autodiscover Service runs on the Director and Front End pool servers, and when published in DNS, can be used by Lync clients to locate server and user services.</span></span> <span data-ttu-id="f21ad-107">Se você estiver atualizando do Lync Server 2010 e não implantou a mobilidade, antes que os clientes possam usar a descoberta automática, você deve modificar listas de nomes alternativos de entidades de certificado em qualquer director e servidor front-end executando o serviço descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="f21ad-107">If you are upgrading from Lync Server 2010 and did not deploy Mobility, before clients can use automatic discovery, you must modify certificate subject alternative name lists on any Director and Front End Server running the Autodiscover Service.</span></span> <span data-ttu-id="f21ad-108">Além disso, pode ser necessário modificar as listas de nomes alternativos de entidades nos certificados usados para regras de publicação de serviço Web externo em proxies reverso.</span><span class="sxs-lookup"><span data-stu-id="f21ad-108">In addition, it may be necessary to modify the subject alternative name lists on certificates used for external web service publishing rules on reverse proxies.</span></span>

<span data-ttu-id="f21ad-109">A decisão sobre se deve usar listas de nomes alternativos de entidades em proxies invertidos se baseia se você publica o serviço de descoberta automática na porta 80 ou na porta 443:</span><span class="sxs-lookup"><span data-stu-id="f21ad-109">The decision about whether to use subject alternative name lists on reverse proxies is based on whether you publish the Autodiscover Service on port 80 or on port 443:</span></span>

  - <span data-ttu-id="f21ad-110">**Publicado na porta 80**   Nenhuma alteração de certificado será necessária se a consulta inicial para o serviço descoberta automática ocorrer na porta 80.</span><span class="sxs-lookup"><span data-stu-id="f21ad-110">**Published on port 80**   No certificate changes are required if the initial query to the Autodiscover Service occurs over port 80.</span></span> <span data-ttu-id="f21ad-111">Isso ocorre porque os dispositivos móveis que executam o Lync acessam o proxy reverso na porta 80 externamente e, em seguida, ligados a um diretor ou servidor front-end na porta 8080 internamente.</span><span class="sxs-lookup"><span data-stu-id="f21ad-111">This is because mobile devices running Lync will access the reverse proxy on port 80 externally and then be bridged to a Director or Front End Server on port 8080 internally.</span></span> <span data-ttu-id="f21ad-112">Para obter detalhes, consulte a seção requisitos técnicos da seção "processo de descoberta automática inicial usando a porta 80" [para mobilidade no Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="f21ad-112">For details, see the "Initial Autodiscover Process Using Port 80" section [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span>

  - <span data-ttu-id="f21ad-113">**Publicado na porta 443**   A lista de nomes alternativos de entidades nos certificados usados pela regra de publicação de serviços Web externos deve conter um *lyncdiscover. \<sipdomain\>*</span><span class="sxs-lookup"><span data-stu-id="f21ad-113">**Published on port 443**   The subject alternative name list on certificates used by the external web services publishing rule must contain a *lyncdiscover.\<sipdomain\>*</span></span> <span data-ttu-id="f21ad-114">entrada para cada domínio SIP em sua organização.</span><span class="sxs-lookup"><span data-stu-id="f21ad-114">entry for each SIP domain within your organization.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f21ad-115">É altamente recomendável usar HTTPS sobre HTTP.</span><span class="sxs-lookup"><span data-stu-id="f21ad-115">We highly recommend using HTTPS over HTTP.</span></span> <span data-ttu-id="f21ad-116">HTTPS usa certificados para criptografar o tráfego.</span><span class="sxs-lookup"><span data-stu-id="f21ad-116">HTTPS uses certificates to encrypt traffic.</span></span> <span data-ttu-id="f21ad-117">O HTTP não fornece criptografia, e todos os dados enviados serão texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="f21ad-117">HTTP does not provide for encryption, and any data sent will be plain text.</span></span>

    
    </div>

<span data-ttu-id="f21ad-118">A emissão de certificados por meio de uma autoridade de certificação interna geralmente é um processo simples.</span><span class="sxs-lookup"><span data-stu-id="f21ad-118">Reissuing certificates by using an internal certificate authority is typically a simple process.</span></span> <span data-ttu-id="f21ad-119">Mas para certificados públicos usados na regra de publicação do serviço Web, adicionar várias entradas de nomes alternativos de entidades pode ficar caro.</span><span class="sxs-lookup"><span data-stu-id="f21ad-119">But for public certificates used on the web service publishing rule, adding multiple subject alternative name entries can become expensive.</span></span> <span data-ttu-id="f21ad-120">Para contornar esse problema, oferecemos suporte para a conexão de descoberta automática inicial na porta 80, que é redirecionada para a porta 8080 do diretor ou servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="f21ad-120">To work around this issue, we support the initial automatic discovery connection over port 80, which is then redirected to port 8080 on the Director or Front End Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f21ad-121">Se a sua infraestrutura do Lync Server 2013 usa certificados internos que são emitidos de uma CA (autoridade de certificação) interna e você planeja dar suporte a dispositivos móveis que se conectam sem fio, a cadeia de certificados raiz da autoridade de certificação interna deve ser instalada em dispositivos móveis ou você deve mudar para um certificado público na sua infraestrutura do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f21ad-121">If your Lync Server 2013 infrastructure uses internal certificates that are issued from an internal certification authority (CA) and you plan to support mobile devices connecting wirelessly, either the root certificate chain from the internal CA must be installed on the mobile devices or you must change to a public certificate on your Lync Server 2013 infrastructure.</span></span>



</div>

<span data-ttu-id="f21ad-122">Este tópico descreve os nomes alternativos de entidades adicionados necessários para o diretor, servidor front-end e proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="f21ad-122">This topic describes the added subject alternative names required for the Director, Front End Server and reverse proxy.</span></span> <span data-ttu-id="f21ad-123">Somente os nomes alternativos de entidades (SAN) adicionados são referenciados.</span><span class="sxs-lookup"><span data-stu-id="f21ad-123">Only the added subject alternative names (SAN) are referenced.</span></span> <span data-ttu-id="f21ad-124">Consulte as seções de planejamento para obter diretrizes sobre as outras entradas em certificados.</span><span class="sxs-lookup"><span data-stu-id="f21ad-124">Refer to the planning sections for guidance on the other entries on certificates.</span></span> <span data-ttu-id="f21ad-125">Para obter detalhes, consulte [cenários do diretor do Lync server 2013](lync-server-2013-scenarios-for-the-director.md), [cenários para acesso de usuários externos no Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md)e [cenários para o proxy inverso no Lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md).</span><span class="sxs-lookup"><span data-stu-id="f21ad-125">For details, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md), [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md), and [Scenarios for reverse proxy in Lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md).</span></span>

<span data-ttu-id="f21ad-126">As tabelas a seguir definem as entradas de SAN de descoberta automática para o pool de diretor, o pool de front-ends e o proxy reverso:</span><span class="sxs-lookup"><span data-stu-id="f21ad-126">The following tables define the Autodiscover SAN entries for the Director pool, the Front End pool, and the reverse proxy:</span></span>

### <a name="director-pool-certificate-requirements"></a><span data-ttu-id="f21ad-127">Requisitos de certificado do pool do director</span><span class="sxs-lookup"><span data-stu-id="f21ad-127">Director Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f21ad-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="f21ad-128">Description</span></span></th>
<th><span data-ttu-id="f21ad-129">Entrada de nome alternativo do assunto</span><span class="sxs-lookup"><span data-stu-id="f21ad-129">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f21ad-130">URL interna do serviço de descoberta automática</span><span class="sxs-lookup"><span data-stu-id="f21ad-130">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="f21ad-131">SAN = lyncdiscoverinternal. &lt; nome de domínio interno&gt;</span><span class="sxs-lookup"><span data-stu-id="f21ad-131">SAN=lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f21ad-132">URL do serviço de descoberta automática externo</span><span class="sxs-lookup"><span data-stu-id="f21ad-132">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="f21ad-133">SAN = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="f21ad-133">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="f21ad-134">Você atribui o certificado recém atualizado com a nova entrada de SAN ao certificado padrão.</span><span class="sxs-lookup"><span data-stu-id="f21ad-134">You assign the newly updated certificate with the new SAN entry to the Default certificate.</span></span> <span data-ttu-id="f21ad-135">Você também pode usar SAN = \*. &lt; sipdomain &gt; .</span><span class="sxs-lookup"><span data-stu-id="f21ad-135">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;.</span></span>



</div>

### <a name="front-end-pool-certificate-requirements"></a><span data-ttu-id="f21ad-136">Requisitos de certificado de pool de front-end</span><span class="sxs-lookup"><span data-stu-id="f21ad-136">Front End Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f21ad-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="f21ad-137">Description</span></span></th>
<th><span data-ttu-id="f21ad-138">Entrada de nome alternativo do assunto</span><span class="sxs-lookup"><span data-stu-id="f21ad-138">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f21ad-139">URL interna do serviço de descoberta automática</span><span class="sxs-lookup"><span data-stu-id="f21ad-139">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="f21ad-140">SAN = lyncdiscoverinternal. &lt; nome de domínio interno&gt;</span><span class="sxs-lookup"><span data-stu-id="f21ad-140">SAN=lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f21ad-141">URL do serviço de descoberta automática externo</span><span class="sxs-lookup"><span data-stu-id="f21ad-141">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="f21ad-142">SAN = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="f21ad-142">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="f21ad-143">Você atribui o certificado recém atualizado com a nova entrada de SAN ao certificado padrão.</span><span class="sxs-lookup"><span data-stu-id="f21ad-143">You assign the newly updated certificate with the new SAN entry to the Default certificate.</span></span> <span data-ttu-id="f21ad-144">Você também pode usar SAN = \*. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="f21ad-144">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="reverse-proxy-public-ca-certificate-requirements"></a><span data-ttu-id="f21ad-145">Requisitos de certificado de proxy reverso (CA pública)</span><span class="sxs-lookup"><span data-stu-id="f21ad-145">Reverse Proxy (Public CA) Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f21ad-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="f21ad-146">Description</span></span></th>
<th><span data-ttu-id="f21ad-147">Entrada de nome alternativo do assunto</span><span class="sxs-lookup"><span data-stu-id="f21ad-147">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f21ad-148">URL do serviço de descoberta automática externo</span><span class="sxs-lookup"><span data-stu-id="f21ad-148">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="f21ad-149">SAN = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="f21ad-149">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="f21ad-150">Você atribui o certificado recém atualizado à nova entrada de SAN ao ouvinte SSL no proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="f21ad-150">You assign the newly updated certificate with the new SAN entry to the SSL Listener on the reverse proxy.</span></span>



<span data-ttu-id="f21ad-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f21ad-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

