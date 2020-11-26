---
title: 'Lync Server 2013: Resumo de DNS - Proxy reverso'
description: 'Lync Server 2013: Resumo DNS-proxy reverso.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Reverse proxy
ms:assetid: 3073affa-4d92-4453-9974-3a82ca0c6445
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204781(v=OCS.15)
ms:contentKeyID: 48183755
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dc2d806893786a11317be1eff9bfdc08c9230bf3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437718"
---
# <a name="dns-summary---reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="7ab88-103">Resumo de DNS - Proxy reverso no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7ab88-103">DNS summary - Reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7ab88-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7ab88-104">

<span> </span></span></span>

<span data-ttu-id="7ab88-105">_**Tópico da última modificação:** 2013-03-22_</span><span class="sxs-lookup"><span data-stu-id="7ab88-105">_**Topic Last Modified:** 2013-03-22_</span></span>

<span data-ttu-id="7ab88-106">Você configura dois adaptadores de rede no seu proxy reverso da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7ab88-106">You configure two network adapters in your reverse proxy as follows:</span></span>

<div>

## <a name="reverse-proxy-network-adapter-requirements"></a><span data-ttu-id="7ab88-107">Requisitos do adaptador de rede proxy reverso</span><span class="sxs-lookup"><span data-stu-id="7ab88-107">Reverse Proxy Network Adapter Requirements</span></span>

  - <span data-ttu-id="7ab88-108">Exemplo **de adaptador de rede 1 (interface interna)**</span><span class="sxs-lookup"><span data-stu-id="7ab88-108">**Network adapter 1 (Internal Interface)** example</span></span>
    
    <span data-ttu-id="7ab88-109">Interface interna com 172.25.33.40 atribuído.</span><span class="sxs-lookup"><span data-stu-id="7ab88-109">Internal interface with 172.25.33.40 assigned.</span></span>
    
    <span data-ttu-id="7ab88-110">Não há nenhum gateway padrão definido.</span><span class="sxs-lookup"><span data-stu-id="7ab88-110">No default gateway is defined.</span></span>
    
    <span data-ttu-id="7ab88-111">Verifique se há uma rota da rede que contém a interface interna de proxy inverso para qualquer rede que contenha servidores de pool de front-end do Lync Server (por exemplo, de 172.25.33.0 para 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="7ab88-111">Ensure there is a route from the network containing the reverse proxy internal interface to any networks that contain Lync Server Front End pool servers (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="7ab88-112">Exemplo **de adaptador de rede 2 (interface externa)**</span><span class="sxs-lookup"><span data-stu-id="7ab88-112">**Network adapter 2 (External Interface)** example</span></span>
    
    <span data-ttu-id="7ab88-113">Um mínimo de um endereço IP público é atribuído a esse adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="7ab88-113">A minimum of one public IP address is assigned to this network adapter.</span></span>
    
    <span data-ttu-id="7ab88-114">O gateway é definido para apontar para o roteador ou o firewall integrado em seu perímetro externo.</span><span class="sxs-lookup"><span data-stu-id="7ab88-114">Gateway is defined to point to the router or integrated firewall in your outer perimeter.</span></span> <span data-ttu-id="7ab88-115">(10.45.16.1 nos exemplos de cenário)</span><span class="sxs-lookup"><span data-stu-id="7ab88-115">(10.45.16.1 in the scenario examples)</span></span>

### <a name="dns-records-required-for-reverse-proxy"></a><span data-ttu-id="7ab88-116">Registros DNS necessários para proxy reverso</span><span class="sxs-lookup"><span data-stu-id="7ab88-116">DNS Records Required for Reverse Proxy</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ab88-117">Local/tipo/porta</span><span class="sxs-lookup"><span data-stu-id="7ab88-117">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="7ab88-118">FQDN</span><span class="sxs-lookup"><span data-stu-id="7ab88-118">FQDN</span></span></th>
<th><span data-ttu-id="7ab88-119">Endereço IP</span><span class="sxs-lookup"><span data-stu-id="7ab88-119">IP address</span></span></th>
<th><span data-ttu-id="7ab88-120">Mapas para/comentários</span><span class="sxs-lookup"><span data-stu-id="7ab88-120">Maps to/comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ab88-121">DNS/A externo</span><span class="sxs-lookup"><span data-stu-id="7ab88-121">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="7ab88-122">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7ab88-122">webext.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7ab88-123">Ouvinte atribuído para recursos publicados externamente</span><span class="sxs-lookup"><span data-stu-id="7ab88-123">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="7ab88-124">Serviços Web externos da implantação interna.</span><span class="sxs-lookup"><span data-stu-id="7ab88-124">External web services from the internal deployment.</span></span> <span data-ttu-id="7ab88-125">Registros adicionais podem ser definidos e criados para todos os pools e servidores individuais para qualquer domínio SIP que usará esse proxy reverso e definido serviços Web externos.</span><span class="sxs-lookup"><span data-stu-id="7ab88-125">Additional records can be defined and created for all pools and single servers for any SIP domain that will use this reverse proxy, and has defined external web services.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ab88-126">DNS/A externo</span><span class="sxs-lookup"><span data-stu-id="7ab88-126">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="7ab88-127">webdirext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7ab88-127">webdirext.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7ab88-128">Ouvinte atribuído para recursos publicados externamente</span><span class="sxs-lookup"><span data-stu-id="7ab88-128">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="7ab88-129">Serviços Web externos para os directors ou pools de directors na sua implantação.</span><span class="sxs-lookup"><span data-stu-id="7ab88-129">External web services for the Directors or Director pools in your deployment.</span></span> <span data-ttu-id="7ab88-130">Você pode definir tantos diretores quantos são diferentes diretores, que podem estar associados a outros domínios SIP.</span><span class="sxs-lookup"><span data-stu-id="7ab88-130">You can define as many Directors as there are distinct Directors, of which may be associated with other SIP domains.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="7ab88-131">A definição dos registros de DNS para e a publicação dos directors não é o pool de front-end ou a decisão do diretor.</span><span class="sxs-lookup"><span data-stu-id="7ab88-131">Defining the DNS records for and publishing the Directors is not an either the Front End pool or the Director decision.</span></span> <span data-ttu-id="7ab88-132">Você deve definir e publicar os serviços Web externos do diretor e do pool de front-end se estiver usando directors.</span><span class="sxs-lookup"><span data-stu-id="7ab88-132">You must define and publish both the Director and the Front End pool external web services if you are using Directors.</span></span> <span data-ttu-id="7ab88-133">Tipos de tráfego específicos (para autenticação e outros usos) serão enviados ao diretor primeiro, se ele for definido na topologia.</span><span class="sxs-lookup"><span data-stu-id="7ab88-133">Specific traffic types (for authentication and other uses) will be sent to the Director first, if it is defined in the topology.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ab88-134">DNS/A externo</span><span class="sxs-lookup"><span data-stu-id="7ab88-134">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="7ab88-135">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7ab88-135">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7ab88-136">Ouvinte atribuído para recursos publicados externamente</span><span class="sxs-lookup"><span data-stu-id="7ab88-136">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="7ab88-137">Conferência discada publicada externamente</span><span class="sxs-lookup"><span data-stu-id="7ab88-137">Dial-in conferencing published externally</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ab88-138">DNS/A externo</span><span class="sxs-lookup"><span data-stu-id="7ab88-138">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="7ab88-139">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7ab88-139">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7ab88-140">Ouvinte atribuído para recursos publicados externamente</span><span class="sxs-lookup"><span data-stu-id="7ab88-140">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="7ab88-141">Conferências publicadas externamente</span><span class="sxs-lookup"><span data-stu-id="7ab88-141">Conferences published externally</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ab88-142">DNS/A externo</span><span class="sxs-lookup"><span data-stu-id="7ab88-142">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="7ab88-143">officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7ab88-143">officewebapps01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7ab88-144">Escuta atribuído para o servidor do Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="7ab88-144">Assigned listener for Office Web Apps Server</span></span></p></td>
<td><p><span data-ttu-id="7ab88-145">Office Web Apps Server implantado internamente ou no perímetro e publicado para acesso de cliente externo</span><span class="sxs-lookup"><span data-stu-id="7ab88-145">Office Web Apps Server deployed internally or in the perimeter, and published for external client access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ab88-146">DNS/A externo</span><span class="sxs-lookup"><span data-stu-id="7ab88-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="7ab88-147">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7ab88-147">lyncdiscover.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7ab88-148">Ouvinte atribuído para recursos publicados externamente</span><span class="sxs-lookup"><span data-stu-id="7ab88-148">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="7ab88-149">O Lync descobriu registro externo para descoberta automática publicada externamente e inclui mobilidade, Microsoft Lync Web App e Agendador Web App</span><span class="sxs-lookup"><span data-stu-id="7ab88-149">Lync Discover External record for externally published AutoDiscover, and includes Mobility, Microsoft Lync Web App, and scheduler Web app</span></span></p></td>
</tr><span data-ttu-id="7ab88-150">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7ab88-150">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

