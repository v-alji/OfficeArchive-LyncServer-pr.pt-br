---
title: 'Lync Server 2013: Suporte a certificado curinga'
description: Suporte a certificado de curinga do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Wildcard certificate support
ms:assetid: 0bae2aa8-b6dc-46f5-a3be-3fe7581809d4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202161(v=OCS.15)
ms:contentKeyID: 48183382
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 46cc362eb925a86b5e90d51569db6d425ba88fa6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390027"
---
# <a name="wildcard-certificate-support-in-lync-server-2013"></a><span data-ttu-id="363ca-103">Suporte a certificado curinga no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="363ca-103">Wildcard certificate support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="363ca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="363ca-104">

<span> </span></span></span>

<span data-ttu-id="363ca-105">_**Tópico da última modificação:** 2013-03-21_</span><span class="sxs-lookup"><span data-stu-id="363ca-105">_**Topic Last Modified:** 2013-03-21_</span></span>

<span data-ttu-id="363ca-106">O Lync Server 2013 usa certificados para fornecer criptografia de comunicação e autenticação de identidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="363ca-106">Lync Server 2013 uses certificates to provide communications encryption and server identity authentication.</span></span> <span data-ttu-id="363ca-107">Em alguns casos, como a publicação na Web por meio do proxy inverso, a entrada de nome alternativo de assunto (SAN) forte para o nome de domínio totalmente qualificado (FQDN) do servidor que está apresentando o serviço não é necessária.</span><span class="sxs-lookup"><span data-stu-id="363ca-107">In some cases, such as web publishing through the reverse proxy, strong subject alternative name (SAN) entry matching to the fully qualified domain name (FQDN) of the server presenting the service is not required.</span></span> <span data-ttu-id="363ca-108">Nesses casos, você pode usar certificados com entradas de SAN curinga (geralmente conhecidas como "certificados curinga") para reduzir o custo de um certificado solicitado de uma autoridade de certificação pública e para reduzir a complexidade do processo de planejamento para certificados.</span><span class="sxs-lookup"><span data-stu-id="363ca-108">In these cases, you can use certificates with wildcard SAN entries (commonly known as “wildcard certificates”) to reduce the cost of a certificate requested from a public certification authority and to reduce the complexity of the planning process for certificates.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="363ca-109">Para manter a funcionalidade dos dispositivos de comunicação unificada (UC) (por exemplo, telefones de mesa), você deve testar cuidadosamente o certificado implantado para garantir que os dispositivos funcionarão corretamente após a implementação de um certificado curinga.</span><span class="sxs-lookup"><span data-stu-id="363ca-109">To retain the functionality of unified communications (UC) devices (for example, desk phones), you should test the deployed certificate carefully to ensure that devices function properly after you implement a wildcard certificate.</span></span>



</div>

<span data-ttu-id="363ca-110">Não há suporte para uma entrada de curinga como o nome do requerente (também conhecido como o nome comum ou CN) para qualquer função.</span><span class="sxs-lookup"><span data-stu-id="363ca-110">There is no support for a wildcard entry as the subject name (also referred to as the common name or CN) for any role.</span></span> <span data-ttu-id="363ca-111">As seguintes funções de servidor são suportadas ao usar entradas de curinga na SAN:</span><span class="sxs-lookup"><span data-stu-id="363ca-111">The following server roles are supported when using wildcard entries in the SAN:</span></span>

  - <span></span>  
    <span data-ttu-id="363ca-112">**Proxy reverso.**</span><span class="sxs-lookup"><span data-stu-id="363ca-112">**Reverse proxy.**</span></span>   <span data-ttu-id="363ca-113">Há suporte para a entrada de SAN curinga para o certificado de publicação URL simples (reunião e discagem).</span><span class="sxs-lookup"><span data-stu-id="363ca-113">Wildcard SAN entry is supported for Simple URL (meet and dialin) publishing certificate.</span></span>

  - <span></span>  
    <span data-ttu-id="363ca-114">**Proxy reverso.**</span><span class="sxs-lookup"><span data-stu-id="363ca-114">**Reverse proxy.**</span></span>   <span data-ttu-id="363ca-115">Há suporte para a entrada de SAN curinga nas entradas de SAN para LyncDiscover no certificado de publicação.</span><span class="sxs-lookup"><span data-stu-id="363ca-115">Wildcard SAN entry is supported for the SAN entries for LyncDiscover on the publishing certificate.</span></span>

  - <span></span>  
    <span data-ttu-id="363ca-116">**Diretor.**</span><span class="sxs-lookup"><span data-stu-id="363ca-116">**Director.**</span></span>   <span data-ttu-id="363ca-117">Há suporte para a entrada de SAN curinga para URLs simples (atender e fazer chamadas) e para entradas de SAN para LyncDiscover e LyncDiscoverInternal em Web Components do director.</span><span class="sxs-lookup"><span data-stu-id="363ca-117">Wildcard SAN entry is supported for Simple URLs (meet and dialin) and for SAN entries for LyncDiscover and LyncDiscoverInternal in Director web components.</span></span>

  - <span></span>  
    <span data-ttu-id="363ca-118">**Servidor front-end (Standard Edition) e pool de front-end (Enterprise Edition).**</span><span class="sxs-lookup"><span data-stu-id="363ca-118">**Front End Server (Standard Edition) and Front End pool (Enterprise Edition).**</span></span> <span data-ttu-id="363ca-119">Há suporte para a entrada de SAN curinga para URLs simples (atender e discagem) e para entradas de SAN para LyncDiscover e LyncDiscoverInternal em componentes de front-end Web.</span><span class="sxs-lookup"><span data-stu-id="363ca-119">Wildcard SAN entry is supported for Simple URLs (meet and dialin) and for SAN entries for LyncDiscover and LyncDiscoverInternal in Front End web components.</span></span>

  - <span></span>  
    <span data-ttu-id="363ca-120">**Exchange Unified Messaging (UM).**</span><span class="sxs-lookup"><span data-stu-id="363ca-120">**Exchange Unified Messaging (UM).**</span></span>   <span data-ttu-id="363ca-121">O servidor não usa entradas de SAN quando implantado como um servidor autônomo.</span><span class="sxs-lookup"><span data-stu-id="363ca-121">The server does not use SAN entries when deployed as a stand-alone server.</span></span>

  - <span></span>  
    <span data-ttu-id="363ca-122">**Servidor de acesso para cliente do Microsoft Exchange Server.**</span><span class="sxs-lookup"><span data-stu-id="363ca-122">**Microsoft Exchange Server Client Access server.**</span></span>   <span data-ttu-id="363ca-123">As entradas curinga na SAN têm suporte para clientes internos e externos.</span><span class="sxs-lookup"><span data-stu-id="363ca-123">Wildcard entries in the SAN are supported for internal and external clients.</span></span>

  - <span></span>  
    <span data-ttu-id="363ca-124">**Exchange Unified Messaging (UM) e servidor de acesso para cliente do Microsoft Exchange Server no mesmo servidor.**</span><span class="sxs-lookup"><span data-stu-id="363ca-124">**Exchange Unified Messaging (UM) and Microsoft Exchange Server Client Access server on same server.**</span></span>   <span data-ttu-id="363ca-125">Há suporte para entradas de SAN curinga.</span><span class="sxs-lookup"><span data-stu-id="363ca-125">Wildcard SAN entries are supported.</span></span>

<span data-ttu-id="363ca-126">Funções de servidor que não são abordadas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="363ca-126">Server roles that are not addressed in this topic:</span></span>

  - <span data-ttu-id="363ca-127">Funções de servidor interno (incluindo, entre outros, o servidor de mediação, o servidor de monitoramento e o servidor de mediação, o aparelho de ramificação sobreviventes ou o servidor de ramificação sobreviventes)</span><span class="sxs-lookup"><span data-stu-id="363ca-127">Internal server roles (including, but not limited to the Mediation Server, Archiving and Monitoring Server, Survivable Branch Appliance, or Survivable Branch Server)</span></span>

  - <span data-ttu-id="363ca-128">Interfaces do servidor de borda externa</span><span class="sxs-lookup"><span data-stu-id="363ca-128">External Edge Server interfaces</span></span>

  - <span data-ttu-id="363ca-129">Servidor de borda interna</span><span class="sxs-lookup"><span data-stu-id="363ca-129">Internal Edge Server</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="363ca-130">Para a interface do servidor de borda interna, uma entrada de curinga pode ser atribuída à SAN e é compatível.</span><span class="sxs-lookup"><span data-stu-id="363ca-130">For the internal Edge Server interface, a wildcard entry can be assigned to the SAN, and is supported.</span></span> <span data-ttu-id="363ca-131">A SAN no servidor de borda interno não é consultada e uma entrada de SAN por curinga tem um valor limitado.</span><span class="sxs-lookup"><span data-stu-id="363ca-131">The SAN on the internal Edge Server is not queried, and a wildcard SAN entry is of limited value.</span></span>

    
    </div>

<span data-ttu-id="363ca-132">Para obter detalhes sobre configurações de certificado, incluindo o uso de caracteres curinga em certificados, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="363ca-132">For details about certificate configurations, including the use of wildcards in certificates, see the following topics:</span></span>

  - [<span data-ttu-id="363ca-133">Requisitos de certificado para servidores internos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="363ca-133">Certificate requirements for internal servers in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-internal-servers.md)

  - [<span data-ttu-id="363ca-134">Requisitos de certificado para acesso do usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="363ca-134">Certificate requirements for external user access in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-external-user-access.md)

  - [<span data-ttu-id="363ca-135">Resumo de certificado - Cargas de DNS e de HLB balanceadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="363ca-135">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="363ca-136">Resumo do certificado - Diretor único no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="363ca-136">Certificate summary - Single Director in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-director.md)

  - [<span data-ttu-id="363ca-137">Resumo de certificado - pool Certificate summary - pool de diretores em escala, balanceador de carga de hardware no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="363ca-137">Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-director-pool-hardware-load-balancer.md)

  - [<span data-ttu-id="363ca-138">Resumo de certificado - Proxy reverso no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="363ca-138">Certificate summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-reverse-proxy.md)

  - [<span data-ttu-id="363ca-139">Orientações para integração de Unificação de Mensagens local e Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="363ca-139">Guidelines for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-guidelines-for-integrating-on-premises-unified-messaging.md)

<span data-ttu-id="363ca-140">Para obter detalhes sobre como configurar certificados para Exchange, incluindo o uso de caracteres curinga, consulte a documentação do produto Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="363ca-140">For details about configuring certificates for Exchange, including the use of wildcards, see the Exchange 2013 product documentation.</span></span>

<span data-ttu-id="363ca-141"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="363ca-141"></div>

<span> </span>

</div>

</div>

</span></span></div>

