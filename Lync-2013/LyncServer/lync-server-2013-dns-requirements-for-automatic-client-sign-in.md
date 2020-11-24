---
title: 'Lync Server 2013: requisitos de DNS para entrada automática do cliente'
description: 'Lync Server 2013: requisitos de DNS para a entrada automática do cliente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for automatic client sign-in
ms:assetid: 3bcd4bb3-a022-4ffa-b005-1a95ad2b1796
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425884(v=OCS.15)
ms:contentKeyID: 48183873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2247c955e0a563a22fb5d0ec20735291a836cdfc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390305"
---
# <a name="dns-requirements-for-automatic-client-sign-in-in-lync-server-2013"></a><span data-ttu-id="da03a-103">Requisitos de DNS para entrada automática do cliente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="da03a-103">DNS requirements for automatic client sign-in in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="da03a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="da03a-104">

<span> </span></span></span>

<span data-ttu-id="da03a-105">_**Tópico da última modificação:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="da03a-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="da03a-106">Esta seção explica os registros de sistema de nome de domínio (DNS) necessários para a entrada automática do cliente.</span><span class="sxs-lookup"><span data-stu-id="da03a-106">This section explains the Domain Name System (DNS) records that are required for automatic client sign-in.</span></span> <span data-ttu-id="da03a-107">Ao implantar seus servidores Standard Edition ou pools front-end, você pode configurar seus clientes para usar a descoberta automática para entrar no servidor padrão da edição ou no pool de front-end apropriado.</span><span class="sxs-lookup"><span data-stu-id="da03a-107">When you deploy your Standard Edition servers or Front End pools, you can configure your clients to use automatic discovery to sign in to the appropriate Standard Edition server or Front End pool.</span></span> <span data-ttu-id="da03a-108">Se você planeja exigir que seus clientes se conectem manualmente ao Lync Server 2013, poderá ignorar este tópico.</span><span class="sxs-lookup"><span data-stu-id="da03a-108">If you plan to require your clients to connect manually to Lync Server 2013, you can skip this topic.</span></span>

<span data-ttu-id="da03a-109">Para dar suporte à entrada automática do cliente, você deve:</span><span class="sxs-lookup"><span data-stu-id="da03a-109">To support automatic client sign-in, you must:</span></span>

  - <span data-ttu-id="da03a-110">Designe um único servidor ou pool para distribuir e autenticar solicitações de entrada do cliente.</span><span class="sxs-lookup"><span data-stu-id="da03a-110">Designate a single server or pool to distribute and authenticate client sign-in requests.</span></span> <span data-ttu-id="da03a-111">Pode ser um servidor ou pool existente em sua organização que hospeda usuários ou você pode designar um servidor ou pool dedicado para essa finalidade que não hospede usuários.</span><span class="sxs-lookup"><span data-stu-id="da03a-111">This can be an existing server or pool in your organization that hosts users, or you can designate a dedicated server or pool for this purpose that hosts no users.</span></span> <span data-ttu-id="da03a-112">Para alta disponibilidade, recomendamos que você designe um pool de front-ends para essa função.</span><span class="sxs-lookup"><span data-stu-id="da03a-112">For high availability, we recommend that you designate a Front End pool for this function.</span></span>

  - <span data-ttu-id="da03a-113">Crie um registro SRV DNS interno para dar suporte à entrada automática do cliente para este servidor ou pool.</span><span class="sxs-lookup"><span data-stu-id="da03a-113">Create an internal DNS SRV record to support automatic client sign-in for this server or pool.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="da03a-114">Nos seguintes requisitos de registro, o domínio SIP refere-se à porção host dos URIs SIP atribuídos aos usuários.</span><span class="sxs-lookup"><span data-stu-id="da03a-114">In the following record requirements, SIP domain refers to the host portion of the SIP URIs assigned to users.</span></span> <span data-ttu-id="da03a-115">Por exemplo, se URIs SIP forem do formato \* @contoso. com, contoso.com será o domínio SIP.</span><span class="sxs-lookup"><span data-stu-id="da03a-115">For example, if SIP URIs are of the form \*@contoso.com, contoso.com is the SIP domain.</span></span> <span data-ttu-id="da03a-116">O domínio SIP muitas vezes é diferente do domínio interno do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="da03a-116">The SIP domain is often different from the internal Active Directory domain.</span></span> <span data-ttu-id="da03a-117">Uma organização também pode dar suporte a vários domínios SIP.</span><span class="sxs-lookup"><span data-stu-id="da03a-117">An organization can also support multiple SIP domains.</span></span>

    
    </div>

<span data-ttu-id="da03a-118">Para habilitar a configuração automática para seus clientes, você deve criar um registro SRV DNS interno que mapeie um dos seguintes registros para o nome de domínio totalmente qualificado (FQDN) do pool de front-ends ou o servidor Standard Edition que distribui solicitações de entrada de clientes do Lync:</span><span class="sxs-lookup"><span data-stu-id="da03a-118">To enable automatic configuration for your clients, you must create an internal DNS SRV record that maps one of the following records to the fully qualified domain name (FQDN) of the Front End pool or Standard Edition server that distributes sign-in requests from Lync clients:</span></span>

  - <span data-ttu-id="da03a-119">\_sipinternaltls. \_ Protocol.\<domain\></span><span class="sxs-lookup"><span data-stu-id="da03a-119">\_sipinternaltls.\_tcp.\<domain\></span></span> <span data-ttu-id="da03a-120">-para conexões TLS internas</span><span class="sxs-lookup"><span data-stu-id="da03a-120">- for internal TLS connections</span></span>

<span data-ttu-id="da03a-121">Você só precisa criar um único registro SRV para o pool de front-end ou o servidor Standard Edition, ou isso distribuirá solicitações de entrada.</span><span class="sxs-lookup"><span data-stu-id="da03a-121">You only need to create a single SRV record for the Front End pool or Standard Edition server or that will distribute sign-in requests.</span></span>

<span data-ttu-id="da03a-122">A tabela a seguir mostra alguns exemplos de registros necessários para a contoso da empresa fictícia, que oferece suporte a domínios SIP do contoso.com e do retail.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="da03a-122">The following table shows some example records required for the fictitious company Contoso, which supports SIP domains of contoso.com and retail.contoso.com.</span></span>

### <a name="example-of-dns-records-required-for-automatic-client-sign-in-with-multiple-sip-domains"></a><span data-ttu-id="da03a-123">Exemplo de registros DNS necessários para a entrada automática do cliente com vários domínios SIP</span><span class="sxs-lookup"><span data-stu-id="da03a-123">Example of DNS Records Required for Automatic Client Sign-in with Multiple SIP Domains</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="da03a-124">FQDN do pool de front-end usado para distribuir solicitações de entrada</span><span class="sxs-lookup"><span data-stu-id="da03a-124">FQDN of Front End pool used to distribute sign-in requests</span></span></th>
<th><span data-ttu-id="da03a-125">Domínio SIP</span><span class="sxs-lookup"><span data-stu-id="da03a-125">SIP domain</span></span></th>
<th><span data-ttu-id="da03a-126">Registro SRV de DNS</span><span class="sxs-lookup"><span data-stu-id="da03a-126">DNS SRV record</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da03a-127">pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="da03a-127">pool01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="da03a-128">contoso.com</span><span class="sxs-lookup"><span data-stu-id="da03a-128">contoso.com</span></span></p></td>
<td><p><span data-ttu-id="da03a-129">Um registro SRV para o domínio _sipinternaltls. _ TCP. contoso. com na porta 5061 mapeada para pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="da03a-129">An SRV record for _sipinternaltls._tcp.contoso.com domain over port 5061 that maps to pool01.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da03a-130">pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="da03a-130">pool01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="da03a-131">retail.contoso.com</span><span class="sxs-lookup"><span data-stu-id="da03a-131">retail.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="da03a-132">Um registro SRV para o domínio _sipinternaltls. _ TCP. Retail. contoso. com na porta 5061 mapeada para pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="da03a-132">An SRV record for _sipinternaltls._tcp.retail.contoso.com domain over port 5061 that maps to pool01.contoso.com</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="da03a-133">Por padrão, as consultas de registros DNS aderem à correspondência de nome de domínio estrito entre o domínio no nome de usuário e o registro SRV.</span><span class="sxs-lookup"><span data-stu-id="da03a-133">By default, queries for DNS records adhere to strict domain name matching between the domain in the user name and the SRV record.</span></span> <span data-ttu-id="da03a-134">Se você preferir que as consultas DNS do cliente usem a correspondência de sufixo em vez disso, você pode configurar a política de grupo DisableStrictDNSNaming.</span><span class="sxs-lookup"><span data-stu-id="da03a-134">If you prefer that client DNS queries use suffix matching instead, you can configure the DisableStrictDNSNaming Group Policy.</span></span> <span data-ttu-id="da03a-135">Para obter detalhes, consulte <A href="lync-server-2013-planning-for-clients-and-devices.md">planejando para clientes e dispositivos no Lync Server 2013</A> na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="da03a-135">For details, see <A href="lync-server-2013-planning-for-clients-and-devices.md">Planning for clients and devices in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="example-of-the-certificates-and-dns-records-required-for-automatic-client-sign-in"></a><span data-ttu-id="da03a-136">Exemplo dos certificados e dos registros DNS necessários para o cliente Sign-In automático</span><span class="sxs-lookup"><span data-stu-id="da03a-136">Example of the Certificates and DNS Records Required for Automatic Client Sign-In</span></span>

<span data-ttu-id="da03a-137">Este exemplo usa os mesmos nomes de exemplo na tabela anterior.</span><span class="sxs-lookup"><span data-stu-id="da03a-137">This example uses the same example names in the preceding table.</span></span> <span data-ttu-id="da03a-138">A organização Contoso suporta os domínios SIP do contoso.com e do retail.contoso.com, e todos os seus usuários têm um URI SIP em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="da03a-138">The Contoso organization supports the SIP domains of contoso.com and retail.contoso.com, and all of its users have a SIP URI in one of the following forms:</span></span>

  - <span data-ttu-id="da03a-139">\<user\>@retail. contoso.com</span><span class="sxs-lookup"><span data-stu-id="da03a-139">\<user\>@retail.contoso.com</span></span>

  - <span data-ttu-id="da03a-140">\<user\>@contoso. com</span><span class="sxs-lookup"><span data-stu-id="da03a-140">\<user\>@contoso.com</span></span>

<span data-ttu-id="da03a-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="da03a-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

