---
title: 'Lync Server 2013: Configurando o DNS para descoberta automática'
description: 'Lync Server 2013: Configurando o DNS para descoberta automática.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring DNS for Autodiscover
ms:assetid: f07a634c-3cf3-4958-8556-84596319ef54
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945656(v=OCS.15)
ms:contentKeyID: 51541528
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98a56cf3aa260bcbec9099e65958a9b17c3eaf26
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433182"
---
# <a name="configuring-dns-for-autodiscover-in-lync-server-2013"></a><span data-ttu-id="7186f-103">Configurando o DNS para descoberta automática no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7186f-103">Configuring DNS for Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7186f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7186f-104">

<span> </span></span></span>

<span data-ttu-id="7186f-105">_**Tópico da última modificação:** 2012-12-12_</span><span class="sxs-lookup"><span data-stu-id="7186f-105">_**Topic Last Modified:** 2012-12-12_</span></span>

<span data-ttu-id="7186f-106">Para dar suporte à descoberta automática de clientes do Lync, você precisa criar os seguintes registros de sistema de nome de domínio (DNS):</span><span class="sxs-lookup"><span data-stu-id="7186f-106">To support autodiscovery for Lync clients, you need to create the following Domain Name System (DNS) records:</span></span>

  - <span data-ttu-id="7186f-107">Um registro DNS interno para dar suporte a clientes do Lync que se conectam dentro da rede da sua organização</span><span class="sxs-lookup"><span data-stu-id="7186f-107">An internal DNS record to support Lync clients who connect from within your organization's network</span></span>

  - <span data-ttu-id="7186f-108">Um registro DNS externo ou público para dar suporte a clientes do Lync que se conectam pela Internet</span><span class="sxs-lookup"><span data-stu-id="7186f-108">An external, or public, DNS record to support Lync clients who connect from the Internet</span></span>

<span data-ttu-id="7186f-109">Você deve criar um registro DNS interno e um registro DNS externo para cada domínio SIP.</span><span class="sxs-lookup"><span data-stu-id="7186f-109">You must create an internal DNS record and an external DNS record for each SIP domain.</span></span>

<span data-ttu-id="7186f-110">Os registros DNS podem ser registros (host) ou registros CNAME, com base na sua capacidade de criar novos certificados com o nome alternativo de requerente (SAN) adicional.</span><span class="sxs-lookup"><span data-stu-id="7186f-110">The DNS records can be either A (host) records or CNAME records, based on your ability to create new certificates with the additional subject alternate name (SAN).</span></span> <span data-ttu-id="7186f-111">Se não for possível solicitar e implantar um novo certificado externo (público) com o lyncdiscover.\<domain name\></span><span class="sxs-lookup"><span data-stu-id="7186f-111">If you are not able to request and deploy a new external (public) certificate with the lyncdiscover.\<domain name\></span></span> <span data-ttu-id="7186f-112">SAN, use o procedimento para usar a porta HTTP/TCP 80.</span><span class="sxs-lookup"><span data-stu-id="7186f-112">SAN, use the procedure for using HTTP/TCP port 80.</span></span> <span data-ttu-id="7186f-113">Os procedimentos a seguir descrevem como criar registros DNS internos e externos.</span><span class="sxs-lookup"><span data-stu-id="7186f-113">The following procedures describe how to create internal and external DNS records.</span></span>

<div>

## <a name="to-create-dns-cname-records"></a><span data-ttu-id="7186f-114">Para criar registros CNAME DNS</span><span class="sxs-lookup"><span data-stu-id="7186f-114">To create DNS CNAME records</span></span>

1.  <span data-ttu-id="7186f-115">Faça logon em um servidor DNS da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="7186f-115">Log on to a DNS server as follows:</span></span>
    
      - <span data-ttu-id="7186f-116">Para criar um registro DNS interno, faça logon em um servidor DNS na sua rede como membro do grupo Domain admins ou um membro do grupo DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="7186f-116">To create an internal DNS record, log on to a DNS server in your network as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>
    
      - <span data-ttu-id="7186f-117">Para criar um registro DNS externo, conecte-se ao seu provedor de DNS público.</span><span class="sxs-lookup"><span data-stu-id="7186f-117">To create an external DNS record, connect to your public DNS provider.</span></span>

2.  <span data-ttu-id="7186f-118">Abra o snap-in administrativo do DNS: clique em **Iniciar**, em **Ferramentas administrativas** e em **DNS**.</span><span class="sxs-lookup"><span data-stu-id="7186f-118">Open the DNS administrative snap-in: Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="7186f-119">Siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="7186f-119">Do one of the following:</span></span>
    
      - <span data-ttu-id="7186f-120">Para um registro DNS interno, na árvore de console do servidor DNS, expanda **zonas de pesquisa direta** para seu domínio do Active Directory (por exemplo, contoso. local).</span><span class="sxs-lookup"><span data-stu-id="7186f-120">For an internal DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your Active Directory domain (for example, contoso.local).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="7186f-121">Este domínio é o domínio do Active Directory onde o pool de &nbsp; directors e o pool de front-ends do Lync Server 2013 estão instalados.</span><span class="sxs-lookup"><span data-stu-id="7186f-121">This domain is the Active Directory domain where your Lync Server 2013&nbsp;Director pool and Front End pool are installed.</span></span>

        
        </div>
    
      - <span data-ttu-id="7186f-122">Para um registro DNS externo, na árvore de console do servidor DNS, expanda **zonas de pesquisa direta** para seu domínio SIP (por exemplo, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="7186f-122">For an external DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>

4.  <span data-ttu-id="7186f-123">Verifique se existe um registro de host para o pool de diretor da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7186f-123">Verify that a host A record exists for your Director pool as follows:</span></span>
    
      - <span data-ttu-id="7186f-124">Para um registro DNS interno, deve haver um registro de host a para o nome de domínio totalmente qualificado dos serviços Web (FQDN) do seu pool de directors (por exemplo, lyncwebdir01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="7186f-124">For an internal DNS record, a host A record should exist for the internal Web Services fully qualified domain name (FQDN) for your Director pool (for example, lyncwebdir01.contoso.local).</span></span>
    
      - <span data-ttu-id="7186f-125">Para um registro DNS externo, deve haver um registro de host a para o FQDN de serviços Web externos para o seu pool de diretor (por exemplo, lyncwebextdir.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="7186f-125">For an external DNS record, a host A record should exist for the external web services FQDN for your Director pool (for example, lyncwebextdir.contoso.com).</span></span>

5.  <span data-ttu-id="7186f-126">Verifique se existe um registro de host para o seu pool Front-end da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7186f-126">Verify that a host A record exists for your Front End pool as follows:</span></span>
    
      - <span data-ttu-id="7186f-127">Para um registro DNS interno, deve haver um registro de host a para o FQDN de serviços Web internos do seu pool de front-end (por exemplo, lyncwebpool01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="7186f-127">For an internal DNS record, a host A record should exist for the internal Web Services FQDN for your Front End pool (for example, lyncwebpool01.contoso.local).</span></span>
    
      - <span data-ttu-id="7186f-128">Para um registro DNS externo, deve haver um registro de host a para o FQDN de serviços Web externos para o seu pool de front-ends (por exemplo, lyncwebextpool01.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="7186f-128">For an external DNS record, a host A record should exist for the external Web Services FQDN for your Front End pool (for example, lyncwebextpool01.contoso.com).</span></span>

6.  <span data-ttu-id="7186f-129">Para um registro DNS interno, na árvore de console do servidor DNS, expanda **zonas de pesquisa direta** para seu domínio SIP (por exemplo, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="7186f-129">For an internal DNS record, in the console tree of your DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7186f-130">Se você estiver criando um registro DNS externo, as <STRONG>zonas de pesquisa direta</STRONG> já estão expandidas para seu domínio SIP da etapa 3.</span><span class="sxs-lookup"><span data-stu-id="7186f-130">If you are creating an external DNS record, <STRONG>Forward Lookup Zones</STRONG> is already expanded for your SIP domain from step 3.</span></span>

    
    </div>

7.  <span data-ttu-id="7186f-131">Clique com o botão direito do mouse no nome do domínio SIP e, em seguida, clique em **novo alias (CNAME)**.</span><span class="sxs-lookup"><span data-stu-id="7186f-131">Right-click the SIP domain name, and then click **New Alias (CNAME)**.</span></span>

8.  <span data-ttu-id="7186f-132">Em **nome do alias**, digite um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="7186f-132">In **Alias name**, type one of the following:</span></span>
    
      - <span data-ttu-id="7186f-133">Para um registro DNS interno, digite lyncdiscoverinternal como o nome de host para a URL do serviço de descoberta automática interna.</span><span class="sxs-lookup"><span data-stu-id="7186f-133">For an internal DNS record, type lyncdiscoverinternal as the host name for the internal Autodiscover Service URL.</span></span>
    
      - <span data-ttu-id="7186f-134">Para um registro DNS externo, digite lyncdiscover como o nome de host para a URL do serviço de descoberta automática externa.</span><span class="sxs-lookup"><span data-stu-id="7186f-134">For an external DNS record, type lyncdiscover as the host name for the external Autodiscover Service URL.</span></span>

9.  <span data-ttu-id="7186f-135">Em **nome de domínio totalmente qualificado (FQDN) do host de destino**, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="7186f-135">In **Fully qualified domain name (FQDN) for target host**, do one of the following:</span></span>
    
      - <span data-ttu-id="7186f-136">Para um registro DNS interno, digite ou navegue até o FQDN de serviços Web internos do seu pool de diretor (por exemplo, lyncwebdir01. contoso. local) e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7186f-136">For an internal DNS record, type or browse to the internal Web Services FQDN for your Director pool (for example, lyncwebdir01.contoso.local), and then click **OK**.</span></span>
    
      - <span data-ttu-id="7186f-137">Para um registro DNS externo, digite ou navegue até o FQDN de serviços Web externos para o seu pool de diretor (por exemplo, lyncwebextdir.contoso.com) e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7186f-137">For an external DNS record, type or browse to the external Web Services FQDN for your Director pool (for example, lyncwebextdir.contoso.com), and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7186f-138">Se você não usar um director, use o FQDN de serviços Web internos e externos para o pool de front-ends ou, para um único servidor, o FQDN para o servidor front-end ou o servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="7186f-138">If you do not use a Director, use the internal and external Web Services FQDN for the Front End pool, or, for a single server, the FQDN for the Front End Server or Standard Edition server.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="7186f-139">Você deve criar um novo registro CNAME de descoberta automática na zona de pesquisa direta de cada domínio SIP ao qual você dá suporte no ambiente do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7186f-139">You must create a new Autodiscover CNAME record in the forward lookup zone of each SIP domain that you support in your Lync Server 2013 environment.</span></span>

    
    </div>

</div>

<div>

## <a name="to-create-dns-a-records"></a><span data-ttu-id="7186f-140">Para criar registros DNS A</span><span class="sxs-lookup"><span data-stu-id="7186f-140">To create DNS A records</span></span>

1.  <span data-ttu-id="7186f-141">Faça logon em um servidor DNS da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="7186f-141">Log on to a DNS server as follows:</span></span>
    
      - <span data-ttu-id="7186f-142">Para criar um registro DNS interno, faça logon em um servidor DNS na sua rede como membro do grupo Domain admins ou um membro do grupo DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="7186f-142">To create an internal DNS record, log on to a DNS server in your network as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>
    
      - <span data-ttu-id="7186f-143">Para criar um registro DNS externo, conecte-se ao seu provedor DNS público ou servidor DNS externo.</span><span class="sxs-lookup"><span data-stu-id="7186f-143">To create an external DNS record, connect to your public DNS provider or external DNS server.</span></span>

2.  <span data-ttu-id="7186f-144">Abra o snap-in administrativo do DNS: clique em **Iniciar**, em **Ferramentas administrativas** e em **DNS**.</span><span class="sxs-lookup"><span data-stu-id="7186f-144">Open the DNS administrative snap-in: Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="7186f-145">Siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="7186f-145">Do one of the following:</span></span>
    
      - <span data-ttu-id="7186f-146">Para um registro DNS interno, na árvore de console do servidor DNS, expanda **zonas de pesquisa direta** para seu domínio do Active Directory (por exemplo, contoso. local).</span><span class="sxs-lookup"><span data-stu-id="7186f-146">For an internal DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your Active Directory domain (for example, contoso.local).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="7186f-147">Este domínio é o domínio do Active Directory onde o pool de &nbsp; directors e o pool de front-ends do Lync Server 2013 estão instalados.</span><span class="sxs-lookup"><span data-stu-id="7186f-147">This domain is the Active Directory domain where your Lync Server 2013&nbsp;Director pool and Front End pool are installed.</span></span>

        
        </div>
    
      - <span data-ttu-id="7186f-148">Para um registro DNS externo, na árvore de console do servidor DNS, expanda **zonas de pesquisa direta** para seu domínio SIP (por exemplo, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="7186f-148">For an external DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>

4.  <span data-ttu-id="7186f-149">Verifique se há um registro do host A (para IPv6, AAAA) para o seu pool de directors da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7186f-149">Verify that a host A (for IPv6, AAAA) record exists for your Director pool as follows:</span></span>
    
      - <span data-ttu-id="7186f-150">Para um registro DNS interno, deve haver um registro de host A (para IPv6, AAAA) para o FQDN de serviços Web internos do seu pool de diretor (por exemplo, lyncwebdir01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="7186f-150">For an internal DNS record, a host A (for IPv6, AAAA) record should exist for the internal Web Services FQDN for your Director pool (for example, lyncwebdir01.contoso.local).</span></span>
    
      - <span data-ttu-id="7186f-151">Para um registro DNS externo, deve haver um registro de host A (para IPv6, AAAA) para o FQDN de serviços Web externos para o seu pool de diretor (por exemplo, lyncwebextdir.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="7186f-151">For an external DNS record, a host A (for IPv6, AAAA) record should exist for the external Web Services FQDN for your Director pool (for example, lyncwebextdir.contoso.com).</span></span>

5.  <span data-ttu-id="7186f-152">Verifique se há um registro do host A (para IPv6, AAAA) para o seu pool Front-end da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7186f-152">Verify that a host A (for IPv6, AAAA) record exists for your Front End pool as follows:</span></span>
    
      - <span data-ttu-id="7186f-153">Para um registro DNS interno, deve haver um registro de host A (para IPv6, AAAA) para o FQDN de serviços Web internos para o seu pool de front-end (por exemplo, lyncwebpool01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="7186f-153">For an internal DNS record, a host A (for IPv6, AAAA) record should exist for the internal Web Services FQDN for your Front End pool (for example, lyncwebpool01.contoso.local).</span></span>
    
      - <span data-ttu-id="7186f-154">Para um registro DNS externo, deve haver um registro de host A (para IPv6, AAAA) para o FQDN de serviços Web externos para o seu pool de front-end (por exemplo, lyncwebextpool01.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="7186f-154">For an external DNS record, a host A (for IPv6, AAAA) record should exist for the external Web Services FQDN for your Front End pool (for example, lyncwebextpool01.contoso.com).</span></span>

6.  <span data-ttu-id="7186f-155">Para um registro DNS interno, na árvore de console do servidor DNS, expanda **zonas de pesquisa direta** para seu domínio SIP (por exemplo, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="7186f-155">For an internal DNS record, in the console tree of your DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7186f-156">Se você estiver criando um registro DNS externo, as <STRONG>zonas de pesquisa direta</STRONG> já estão expandidas para seu domínio SIP da etapa 3.</span><span class="sxs-lookup"><span data-stu-id="7186f-156">If you are creating an external DNS record, <STRONG>Forward Lookup Zones</STRONG> is already expanded for your SIP domain from step 3.</span></span>

    
    </div>

7.  <span data-ttu-id="7186f-157">Clique com o botão direito do mouse no nome do domínio SIP e clique em **novo host (A ou aaaa)**.</span><span class="sxs-lookup"><span data-stu-id="7186f-157">Right-click the SIP domain name, and then click **New Host (A or AAAA)**.</span></span>

8.  <span data-ttu-id="7186f-158">Em **nome**, digite o nome do host da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7186f-158">In **Name**, type the host name as follows:</span></span>
    
      - <span data-ttu-id="7186f-159">Para um registro DNS interno, digite lyncdiscoverinternal como o nome de host para a URL do serviço de descoberta automática interna.</span><span class="sxs-lookup"><span data-stu-id="7186f-159">For an internal DNS record, type lyncdiscoverinternal as the host name for the internal Autodiscover Service URL.</span></span>
    
      - <span data-ttu-id="7186f-160">Para um registro DNS externo, digite lyncdiscover como o nome de host para a URL do serviço de descoberta automática externa.</span><span class="sxs-lookup"><span data-stu-id="7186f-160">For an external DNS record, type lyncdiscover as the host name for the external Autodiscover Service URL.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7186f-161">O nome do domínio é presumido na zona na qual o registro é definido e, portanto, não precisa ser inserido como parte do registro A.</span><span class="sxs-lookup"><span data-stu-id="7186f-161">The domain name is assumed from the zone in which the record is defined and, therefore, does not need to be entered as part of the A record.</span></span>

    
    </div>

9.  <span data-ttu-id="7186f-162">Em **endereço IP**, digite o endereço IP da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7186f-162">In **IP Address**, type the IP address as follows:</span></span>
    
      - <span data-ttu-id="7186f-163">Para um registro DNS interno, digite o endereço IP dos serviços Web internos do diretor (ou, se você usar um balanceador de carga, digite o IP virtual (VIP) do balanceador de carga do diretor).</span><span class="sxs-lookup"><span data-stu-id="7186f-163">For an internal DNS record, type the internal Web Services IP address of the Director (or, if you use a load balancer, type the virtual IP (VIP) of the Director load balancer).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="7186f-164">Se você não usar um director, digite o endereço IP do servidor front-end ou do servidor Standard Edition, ou, se usar um balanceador de carga, digite o VIP do balanceador de carga do pool de front-end.</span><span class="sxs-lookup"><span data-stu-id="7186f-164">If you do not use a Director, type the IP address of the Front End Server or Standard Edition server, or, if you use a load balancer, type the VIP of the Front End pool load balancer.</span></span>

        
        </div>
    
      - <span data-ttu-id="7186f-165">Para um registro DNS externo, digite o endereço IP externo ou público do proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="7186f-165">For an external DNS record, type the external or public IP address of the reverse proxy.</span></span>

10. <span data-ttu-id="7186f-166">Clique em **Adicionar host** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7186f-166">Click **Add Host**, and then click **OK**.</span></span>

11. <span data-ttu-id="7186f-167">Para criar um registro adicional adicional, repita as etapas 8 a 10.</span><span class="sxs-lookup"><span data-stu-id="7186f-167">To create an additional A record, repeat steps 8 through 10.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="7186f-168">Você deve criar um novo lyncdiscover e lyncdiscoverinternal registros na zona de pesquisa direta de cada domínio SIP para o qual você dá suporte no ambiente do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7186f-168">You must create a new lyncdiscover and lyncdiscoverinternal A records in the forward lookup zone of each SIP domain that you support in your Lync Server 2013 environment.</span></span>

    
    </div>

12. <span data-ttu-id="7186f-169">Quando terminar de criar os registros (para IPv6, AAAA), clique em **concluído**.</span><span class="sxs-lookup"><span data-stu-id="7186f-169">When you are finished creating A (for IPv6, AAAA) records, click **Done**.</span></span>

<span data-ttu-id="7186f-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7186f-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

