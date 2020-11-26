---
title: 'Lync Server 2013: Definindo seus requisitos de controle de admissão de chamadas'
description: 'Lync Server 2013: definindo seus requisitos para controle de admissão de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your organization's requirements for call admission control
ms:assetid: 5122171a-a5b0-4059-b033-846caec10d1e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398334(v=OCS.15)
ms:contentKeyID: 48184104
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9f675ac5811e0c0c1c23dc76ebb8b4525857836
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430859"
---
# <a name="defining-your-requirements-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="7b328-103">Definindo seus requisitos de controle de admissão de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7b328-103">Defining your requirements for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7b328-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7b328-104">

<span> </span></span></span>

<span data-ttu-id="7b328-105">_**Tópico da última modificação:** 2013-10-28_</span><span class="sxs-lookup"><span data-stu-id="7b328-105">_**Topic Last Modified:** 2013-10-28_</span></span>

<span data-ttu-id="7b328-106">O planejamento de controle de admissão de chamadas (CAC) requer informações detalhadas sobre a topologia de rede corporativa.</span><span class="sxs-lookup"><span data-stu-id="7b328-106">Planning for call admission control (CAC) requires detailed information about your enterprise network topology.</span></span> <span data-ttu-id="7b328-107">Para ajudar a planejar suas políticas de controle de admissão de chamadas, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="7b328-107">To help plan your call admission control policies, follow these steps.</span></span>

1.  <span data-ttu-id="7b328-108">Identifique os hubs/backbones (chamados de *regiões de rede*) dentro da sua rede corporativa.</span><span class="sxs-lookup"><span data-stu-id="7b328-108">Identify the hubs/backbones (called *network regions*) within your enterprise network.</span></span>

2.  <span data-ttu-id="7b328-109">Identifique os escritórios ou locais (chamados de *sites de rede*) em cada região de rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-109">Identify the offices or locations (called *network sites*) within each network region.</span></span>

3.  <span data-ttu-id="7b328-110">Determine a rota de rede entre todos os pares de regiões de rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-110">Determine the network route between every pair of network regions.</span></span>

4.  <span data-ttu-id="7b328-111">Determine os limites de largura de banda para cada link de WAN.</span><span class="sxs-lookup"><span data-stu-id="7b328-111">Determine the bandwidth limits for each WAN link.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7b328-112">Os limites de largura de banda referem-se à quantidade de largura de banda de um link de WAN atribuída ao tráfego de voz e áudio/vídeo da empresa.</span><span class="sxs-lookup"><span data-stu-id="7b328-112">Bandwidth limits refer to how much of the bandwidth on a WAN link is allocated to Enterprise Voice and audio/video traffic.</span></span> <span data-ttu-id="7b328-113">Quando um link de WAN é descrito como "largura de banda restringida", o link de WAN tem um limite de largura de banda menor do que o tráfego de pico esperado no link.</span><span class="sxs-lookup"><span data-stu-id="7b328-113">When a WAN link is described as “bandwidth-constrained,” the WAN link has a bandwidth limit that is lower than the expected peak traffic over the link.</span></span>

    
    </div>

5.  <span data-ttu-id="7b328-114">Identifique as sub-redes IP atribuídas a cada site de rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-114">Identify the IP subnets that are assigned to each network site.</span></span>

<span data-ttu-id="7b328-115">Para explicar esses conceitos, usaremos a topologia de rede de exemplo mostrada na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="7b328-115">To explain these concepts, we’ll use the example network topology shown in the following figure.</span></span>

<span data-ttu-id="7b328-116">**Exemplo de topologia para controle de admissão de chamadas**</span><span class="sxs-lookup"><span data-stu-id="7b328-116">**Example topology for call admission control**</span></span>

<span data-ttu-id="7b328-117">![Litware Inc. exemplo de topologia de rede](images/Gg398334.477f3b52-2973-4026-9bc0-b1c6bf9f4803(OCS.15).jpg "Litware Inc. exemplo de topologia de rede")</span><span class="sxs-lookup"><span data-stu-id="7b328-117">![Litware Inc. Network Topology Example](images/Gg398334.477f3b52-2973-4026-9bc0-b1c6bf9f4803(OCS.15).jpg "Litware Inc. Network Topology Example")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7b328-118">Todos os sites de rede estão associados a uma região de rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-118">All network sites are associated with a network region.</span></span> <span data-ttu-id="7b328-119">Por exemplo, Portland, Reno e Albuquerque estão incluídos na região da América do Norte.</span><span class="sxs-lookup"><span data-stu-id="7b328-119">For example, Portland, Reno, and Albuquerque are included in the North America region.</span></span> <span data-ttu-id="7b328-120">Nesta figura, somente links WAN que têm políticas de CAC aplicadas são mostrados, com limites de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="7b328-120">In this figure, only WAN links that have CAC policies applied are shown, with bandwidth limits.</span></span> <span data-ttu-id="7b328-121">Os sites de rede de Chicago, Nova York e Detroit são exibidos dentro da elipse da América do Norte, pois eles não são restringidos por largura de banda e, portanto, não exigem políticas do CAC.</span><span class="sxs-lookup"><span data-stu-id="7b328-121">The network sites of Chicago, New York, and Detroit are shown inside the North America region oval because they are not bandwidth-constrained, and therefore do not require CAC policies.</span></span>



</div>

<span data-ttu-id="7b328-122">Os componentes deste exemplo de topologia são explicados nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="7b328-122">The components of this example topology are explained in the following sections.</span></span> <span data-ttu-id="7b328-123">Para obter detalhes sobre como essa topologia era planejada, incluindo os limites de largura de banda, consulte [exemplo: reunir seus requisitos para o controle de admissão de chamadas no Lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md).</span><span class="sxs-lookup"><span data-stu-id="7b328-123">For details about how this topology was planned, including the bandwidth limits, see [Example: Gathering your requirements for call admission control in Lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md).</span></span>

<div>

## <a name="identify-network-regions"></a><span data-ttu-id="7b328-124">Identificar regiões de rede</span><span class="sxs-lookup"><span data-stu-id="7b328-124">Identify Network Regions</span></span>

<span data-ttu-id="7b328-125">Uma região de rede representa um backbone de rede ou um hub de rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-125">A network region represents a network backbone or a network hub.</span></span>

<span data-ttu-id="7b328-126">Um backbone ou Hub de rede é uma parte da infraestrutura de rede de computador que interconecta partes diferentes da rede, fornecendo um caminho para a troca de informações entre diferentes LANs ou sub-redes.</span><span class="sxs-lookup"><span data-stu-id="7b328-126">A network backbone or hub is a part of computer network infrastructure that interconnects different parts of the network, providing a path for the exchange of information between different LANs or subnets.</span></span> <span data-ttu-id="7b328-127">Um backbone pode unir várias redes diferentes de um local pequeno para uma ampla área geográfica.</span><span class="sxs-lookup"><span data-stu-id="7b328-127">A backbone can tie together diverse networks from a small location to a wide geographic area.</span></span> <span data-ttu-id="7b328-128">A capacidade do backbone normalmente é maior do que a das redes conectadas a ele.</span><span class="sxs-lookup"><span data-stu-id="7b328-128">The backbone's capacity is typically greater than that of the networks that connect to it.</span></span>

<span data-ttu-id="7b328-129">Nosso exemplo de topologia têm três regiões de rede: América do Norte, EMEA e APAC.</span><span class="sxs-lookup"><span data-stu-id="7b328-129">Our example topology has three network regions: North America, EMEA, and APAC.</span></span> <span data-ttu-id="7b328-130">Uma região de rede contém um conjunto de sites de rede (consulte a definição de sites de rede mais adiante neste tópico).</span><span class="sxs-lookup"><span data-stu-id="7b328-130">A network region contains a collection of network sites (see the definition of network sites later in this topic).</span></span> <span data-ttu-id="7b328-131">Trabalhe com sua equipe de operações de rede para identificar suas regiões de rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-131">Work with your network operations team to identify your network regions.</span></span>

</div>

<div>

## <a name="associating-a-central-site-with-each-network-region"></a><span data-ttu-id="7b328-132">Associando um site central a cada região de rede</span><span class="sxs-lookup"><span data-stu-id="7b328-132">Associating a Central Site with each Network Region</span></span>

<span data-ttu-id="7b328-133">O CAC requer que um site central do Lync Server seja definido para cada região de rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-133">CAC requires that a Lync Server central site is defined for each network region.</span></span> <span data-ttu-id="7b328-134">O site central é selecionado com a melhor conectividade de rede e largura de banda mais alta para todos os outros sites na região da rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-134">The central site is selected with the best network connectivity and highest bandwidth to all the other sites within that network region.</span></span> <span data-ttu-id="7b328-135">O exemplo anterior da topologia de rede mostra três regiões de rede, cada uma com um site central que gerencia decisões do CAC.</span><span class="sxs-lookup"><span data-stu-id="7b328-135">The preceding example of network topology shows three network regions, each with a central site that manages CAC decisions.</span></span> <span data-ttu-id="7b328-136">No exemplo anterior, a associação apropriada é mostrada na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7b328-136">From the preceding example, the appropriate association is shown in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7b328-137">Os sites centrais não correspondem necessariamente a sites de rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-137">Central sites do not necessarily correspond to network sites.</span></span> <span data-ttu-id="7b328-138">Nos exemplos desta documentação, alguns sites centrais (Chicago, Londres e Pequim) compartilham o mesmo nome dos sites de rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-138">In the examples in this documentation, some central sites—Chicago, London, and Beijing—share the same name as the network sites.</span></span> <span data-ttu-id="7b328-139">No entanto, mesmo se um site central e um site de rede compartilharem o mesmo nome, o site central será um elemento da topologia do Lync Server, enquanto o site de rede faz parte da rede geral na qual a topologia do Lync Server reside.</span><span class="sxs-lookup"><span data-stu-id="7b328-139">However, even if a central site and network site share the same name, the central site is an element of the Lync Server topology, whereas the network site is a part of the overall network in which the Lync Server topology resides.</span></span>



</div>

### <a name="network-regions-central-sites-and-network-sites"></a><span data-ttu-id="7b328-140">Regiões de rede, sites centrais e sites de rede</span><span class="sxs-lookup"><span data-stu-id="7b328-140">Network regions, central sites, and network sites</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b328-141">Região de rede</span><span class="sxs-lookup"><span data-stu-id="7b328-141">Network Region</span></span></th>
<th><span data-ttu-id="7b328-142">Local central</span><span class="sxs-lookup"><span data-stu-id="7b328-142">Central Site</span></span></th>
<th><span data-ttu-id="7b328-143">Sites de rede</span><span class="sxs-lookup"><span data-stu-id="7b328-143">Network Sites</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b328-144">América do Norte</span><span class="sxs-lookup"><span data-stu-id="7b328-144">North America</span></span></p></td>
<td><p><span data-ttu-id="7b328-145">Chicago</span><span class="sxs-lookup"><span data-stu-id="7b328-145">Chicago</span></span></p></td>
<td><p><span data-ttu-id="7b328-146">Chicago</span><span class="sxs-lookup"><span data-stu-id="7b328-146">Chicago</span></span></p>
<p><span data-ttu-id="7b328-147">Nova York</span><span class="sxs-lookup"><span data-stu-id="7b328-147">New York</span></span></p>
<p><span data-ttu-id="7b328-148">Detroit</span><span class="sxs-lookup"><span data-stu-id="7b328-148">Detroit</span></span></p>
<p><span data-ttu-id="7b328-149">Portland</span><span class="sxs-lookup"><span data-stu-id="7b328-149">Portland</span></span></p>
<p><span data-ttu-id="7b328-150">Reno</span><span class="sxs-lookup"><span data-stu-id="7b328-150">Reno</span></span></p>
<p><span data-ttu-id="7b328-151">Albuquerque</span><span class="sxs-lookup"><span data-stu-id="7b328-151">Albuquerque</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b328-152">EMEA</span><span class="sxs-lookup"><span data-stu-id="7b328-152">EMEA</span></span></p></td>
<td><p><span data-ttu-id="7b328-153">Londres</span><span class="sxs-lookup"><span data-stu-id="7b328-153">London</span></span></p></td>
<td><p><span data-ttu-id="7b328-154">Londres</span><span class="sxs-lookup"><span data-stu-id="7b328-154">London</span></span></p>
<p><span data-ttu-id="7b328-155">Cologne</span><span class="sxs-lookup"><span data-stu-id="7b328-155">Cologne</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b328-156">APAC</span><span class="sxs-lookup"><span data-stu-id="7b328-156">APAC</span></span></p></td>
<td><p><span data-ttu-id="7b328-157">Pequim</span><span class="sxs-lookup"><span data-stu-id="7b328-157">Beijing</span></span></p></td>
<td><p><span data-ttu-id="7b328-158">Pequim</span><span class="sxs-lookup"><span data-stu-id="7b328-158">Beijing</span></span></p>
<p><span data-ttu-id="7b328-159">Manila</span><span class="sxs-lookup"><span data-stu-id="7b328-159">Manila</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="identify-network-sites"></a><span data-ttu-id="7b328-160">Identificar sites de rede</span><span class="sxs-lookup"><span data-stu-id="7b328-160">Identify Network Sites</span></span>

<span data-ttu-id="7b328-161">Um site de rede representa um local onde sua organização tem um local físico, por exemplo, escritórios, um conjunto de prédios ou um campus.</span><span class="sxs-lookup"><span data-stu-id="7b328-161">A network site represents a location where your organization has a physical venue—for example, offices, a set of buildings, or a campus.</span></span> <span data-ttu-id="7b328-162">Um local físico com uma LAN e com conectividade de WAN a outros sites é considerado um site de rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-162">A physical venue with a LAN and has WAN connectivity to other sites is considered a network site.</span></span> <span data-ttu-id="7b328-163">Comece inventariando todos os escritórios da sua organização.</span><span class="sxs-lookup"><span data-stu-id="7b328-163">Start by inventorying all of your organization’s offices.</span></span> <span data-ttu-id="7b328-164">Na nossa topologia de exemplo, a região de rede da América do Norte consiste nos seguintes sites de rede: New York, Chicago, Detroit, Portland, Reno e Albuquerque.</span><span class="sxs-lookup"><span data-stu-id="7b328-164">In our example topology, the North America network region consists of the following network sites: New York, Chicago, Detroit, Portland, Reno, and Albuquerque.</span></span>

<span data-ttu-id="7b328-165">Você deve associar todos os sites de rede a uma região de rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-165">You must associate every network site with a network region.</span></span> <span data-ttu-id="7b328-166">Dependendo se o site de rede tem um link de WAN restrito, uma política de largura de banda é associada ao site de rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-166">Depending on whether the network site has a constrained WAN link, a bandwidth policy is associated with the network site.</span></span> <span data-ttu-id="7b328-167">Para obter detalhes sobre as políticas do CAC e a largura de banda que você atribuir usando-as, consulte "definir políticas de largura de banda" mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="7b328-167">For details about CAC policies and the bandwidth that you allocate by using them, see "Define Bandwidth Policies" later in this topic.</span></span> <span data-ttu-id="7b328-168">Para configurar o CAC, associe sites de rede com regiões de rede e, em seguida, crie políticas de alocação de largura de banda para aplicar às conexões restritas de largura de banda entre um determinado site ou região e as conexões WAN entre os sites e regiões.</span><span class="sxs-lookup"><span data-stu-id="7b328-168">To configure CAC, you associate network sites with network regions, and then you create bandwidth-allocating policies to apply to the bandwidth-constrained connections between a given site or region and the WAN connections between the sites and regions.</span></span>

</div>

<div>

## <a name="identify-network-links"></a><span data-ttu-id="7b328-169">Identificar links de rede</span><span class="sxs-lookup"><span data-stu-id="7b328-169">Identify Network Links</span></span>

<span data-ttu-id="7b328-170">Links de rede representam conexões para a WAN física que vincula diferentes áreas e sites.</span><span class="sxs-lookup"><span data-stu-id="7b328-170">Network links represent connections to the physical WAN that links different regions and sites.</span></span> <span data-ttu-id="7b328-171">Na nossa topologia de exemplo, há dois links de rede regionais, cinco links de rede entre regiões e sites e um link de rede entre dois sites.</span><span class="sxs-lookup"><span data-stu-id="7b328-171">In our example topology, there are two regional network links, five network links between regions and sites, and one network link between two sites.</span></span>

<span data-ttu-id="7b328-172">Os dois links regionais estão entre a América do Norte e a EMEA, representados como NA-EMEA-LINK e entre a Ásia e a EMEA, representados como EMEA-Ásia-LINK.</span><span class="sxs-lookup"><span data-stu-id="7b328-172">The two regional links are between North America and EMEA, represented as NA-EMEA-LINK, and between APAC and EMEA, represented as EMEA-APAC-LINK.</span></span>

<span data-ttu-id="7b328-173">Os links de site são indicados pelas linhas que conectam a Portland, Reno e Albuquerque à região da América do Norte, Manila à região da Ásia e Cologne à região da EMEA.</span><span class="sxs-lookup"><span data-stu-id="7b328-173">The site links are indicated by the lines connecting Portland, Reno, and Albuquerque to the North America region, Manila to the APAC region, and Cologne to the EMEA region.</span></span> <span data-ttu-id="7b328-174">A linha entre Reno e Albuquerque mostra um link de rede direto entre esses dois sites.</span><span class="sxs-lookup"><span data-stu-id="7b328-174">The line between Reno and Albuquerque shows a direct network link between these two sites.</span></span>

</div>

<div>

## <a name="define-bandwidth-policies"></a><span data-ttu-id="7b328-175">Definir políticas de largura de banda</span><span class="sxs-lookup"><span data-stu-id="7b328-175">Define Bandwidth Policies</span></span>

<span data-ttu-id="7b328-176">Trabalhe com sua equipe de operações de rede para determinar Quanta largura de banda de WAN está disponível para tráfego de áudio e vídeo em tempo real nos links WAN de sua organização.</span><span class="sxs-lookup"><span data-stu-id="7b328-176">Work with your network operations team to determine how much WAN bandwidth is available for real-time audio and video traffic across the WAN links in your organization.</span></span> <span data-ttu-id="7b328-177">Geralmente, as políticas de largura de banda são aplicadas ao WAN links se o uso da largura de banda for restrito; ou seja, se ela deveria ser maior que a largura de banda que pode ser alocada para modalidades de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="7b328-177">Bandwidth policies are typically applied to WAN links if the bandwidth usage is constrained; that is, if it expected to be more than the bandwidth that can be allocated for audio and video modalities.</span></span>

<span data-ttu-id="7b328-178">*Políticas de largura de banda* do CAC definem a largura de banda máxima que pode ser reservada para modalidades de áudio e vídeo em tempo real.</span><span class="sxs-lookup"><span data-stu-id="7b328-178">CAC *bandwidth policies* define the maximum bandwidth that can be reserved for real-time audio and video modalities.</span></span> <span data-ttu-id="7b328-179">Como o CAC não limita a largura de banda de outro tráfego, ele não pode evitar outros tráfegos de dados, como uma transferência de arquivo grande, fluxo de música, desde o uso de toda a largura de banda da rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-179">Since CAC does not limit the bandwidth of other traffic, it cannot prevent other data traffic such as a large file transfer, music streaming, from using up all of the network bandwidth.</span></span>

<span data-ttu-id="7b328-180">As políticas de largura de banda do CAC podem definir qualquer um dos seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="7b328-180">CAC bandwidth policies can define any or all of the following:</span></span>

  - <span data-ttu-id="7b328-181">Largura de banda total máxima atribuída para áudio.</span><span class="sxs-lookup"><span data-stu-id="7b328-181">Maximum total bandwidth allocated for audio.</span></span>

  - <span data-ttu-id="7b328-182">Largura de banda total máxima alocada para vídeo.</span><span class="sxs-lookup"><span data-stu-id="7b328-182">Maximum total bandwidth allocated for video.</span></span>

  - <span data-ttu-id="7b328-183">Largura de banda máxima alocada para uma única chamada de áudio (sessão).</span><span class="sxs-lookup"><span data-stu-id="7b328-183">Maximum bandwidth allocated for a single audio call (session).</span></span>

  - <span data-ttu-id="7b328-184">Largura de banda máxima alocada para uma única chamada de vídeo (sessão).</span><span class="sxs-lookup"><span data-stu-id="7b328-184">Maximum bandwidth allocated for a single video call (session).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7b328-185">Todos os valores de largura de banda do CAC representam os limites de largura de banda <EM>unidirecionais</EM></span><span class="sxs-lookup"><span data-stu-id="7b328-185">All CAC bandwidth values represent the maximum <EM>unidirectional</EM> bandwidth limits.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="7b328-186">Os recursos da política de voz do Lync Server 2013 fornecem a capacidade de substituir verificações de política de largura de banda para chamadas recebidas para o usuário (não para chamadas feitas pelo usuário).</span><span class="sxs-lookup"><span data-stu-id="7b328-186">The Lync Server 2013 Voice Policy features provide the ability to override bandwidth policy checks for incoming calls to the user (not for outgoing calls that are placed by the user).</span></span> <span data-ttu-id="7b328-187">Depois que a sessão for estabelecida, o consumo de largura de banda será considerado com precisão.</span><span class="sxs-lookup"><span data-stu-id="7b328-187">After the session is established, the bandwidth consumption will be accurately accounted for.</span></span> <span data-ttu-id="7b328-188">Esta configuração deve ser usada com moderação.</span><span class="sxs-lookup"><span data-stu-id="7b328-188">This setting should be used sparingly.</span></span> <span data-ttu-id="7b328-189">Para obter detalhes, consulte <A href="lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md">criar uma política de voz e configurar registros de uso de PSTN no Lync server 2013</A> ou <A href="lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md">modificar uma política de voz e configurar registros de uso PSTN no Lync Server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="7b328-189">For details, see <A href="lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md">Create a voice policy and configure PSTN usage records in Lync Server 2013</A> or <A href="lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md">Modify a voice policy and configure PSTN usage records in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<span data-ttu-id="7b328-190">Para otimizar a utilização da largura de banda com base em cada sessão, considere o tipo de codecs de áudio e vídeo que será usado.</span><span class="sxs-lookup"><span data-stu-id="7b328-190">To optimize bandwidth utilization on a per-session basis, consider the type of audio and video codecs that will be used.</span></span> <span data-ttu-id="7b328-191">Em particular, evite alocar largura de banda insuficiente para um codec que você espera que seja usado com frequência.</span><span class="sxs-lookup"><span data-stu-id="7b328-191">In particular, avoid allocating insufficient bandwidth for a codec that you expect to be used frequently.</span></span> <span data-ttu-id="7b328-192">Por outro lado, se você quiser impedir que a mídia use um codec que exija mais largura de banda, deve definir a largura de banda máxima por sessão, o suficiente para desencorajar tal uso.</span><span class="sxs-lookup"><span data-stu-id="7b328-192">Conversely, if you want to prevent media from using a codec that requires more bandwidth, you should set the maximum bandwidth per session low enough to discourage such use.</span></span> <span data-ttu-id="7b328-193">Para áudio, nem todos os codecs estão disponíveis para todos os cenários.</span><span class="sxs-lookup"><span data-stu-id="7b328-193">For audio, not every codec is available for every scenario.</span></span> <span data-ttu-id="7b328-194">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="7b328-194">For example:</span></span>

  - <span data-ttu-id="7b328-195">As chamadas de áudio ponto a ponto entre os pontos de extremidade do Lync usarão RTAudio (8kHz) ou RTAudio (16kHz) quando você fatorar a largura de banda e a priorização de codecs.</span><span class="sxs-lookup"><span data-stu-id="7b328-195">Peer-to-peer audio calls between Lync endpoints will use either RTAudio (8kHz) or RTAudio (16kHz) when you factor in the bandwidth and prioritization of codecs.</span></span>

  - <span data-ttu-id="7b328-196">As chamadas em conferência entre os pontos de extremidade do Lync e o serviço de conferência A/V usarão G. 722 ou sirene.</span><span class="sxs-lookup"><span data-stu-id="7b328-196">Conference calls between Lync endpoints and the A/V Conferencing service will use either G.722 or Siren.</span></span>

  - <span data-ttu-id="7b328-197">As chamadas para a rede telefônica pública comutada (PSTN) para ou a partir de pontos de extremidade do Lync usarão G. 711 ou RTAudio (8kHz).</span><span class="sxs-lookup"><span data-stu-id="7b328-197">Calls to the public switched telephone network (PSTN) either to or from Lync endpoints will use either G.711 or RTAudio (8kHz).</span></span>

<span data-ttu-id="7b328-198">Use a tabela a seguir para ajudar a otimizar as configurações de largura de banda máxima por sessão.</span><span class="sxs-lookup"><span data-stu-id="7b328-198">Use the following table to help optimize the maximum per-session bandwidth settings.</span></span>

### <a name="bandwidth-utilization-by-codecs"></a><span data-ttu-id="7b328-199">Utilização de largura de banda por codecs</span><span class="sxs-lookup"><span data-stu-id="7b328-199">Bandwidth utilization by codecs</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b328-200">Codec</span><span class="sxs-lookup"><span data-stu-id="7b328-200">Codec</span></span></th>
<th><span data-ttu-id="7b328-201">Requisitos de largura de banda sem correção de erro antecipado (FEC)</span><span class="sxs-lookup"><span data-stu-id="7b328-201">Bandwidth requirement with no forward error correction (FEC)</span></span></th>
<th><span data-ttu-id="7b328-202">Requisitos de largura de banda com a correção de erro antecipada (FEC)</span><span class="sxs-lookup"><span data-stu-id="7b328-202">Bandwidth requirement with forward error correction (FEC)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b328-203">RTAudio (8kHz)</span><span class="sxs-lookup"><span data-stu-id="7b328-203">RTAudio (8kHz)</span></span></p></td>
<td><p><span data-ttu-id="7b328-204">49,8 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-204">49.8 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-205">61,6 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-205">61.6 kbps</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b328-206">RTAudio (16kHz)</span><span class="sxs-lookup"><span data-stu-id="7b328-206">RTAudio (16kHz)</span></span></p></td>
<td><p><span data-ttu-id="7b328-207">67 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-207">67 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-208">96 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-208">96 kbps</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b328-209">Siren</span><span class="sxs-lookup"><span data-stu-id="7b328-209">Siren</span></span></p></td>
<td><p><span data-ttu-id="7b328-210">57,6 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-210">57.6 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-211">73,6 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-211">73.6 kbps</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b328-212">G.711</span><span class="sxs-lookup"><span data-stu-id="7b328-212">G.711</span></span></p></td>
<td><p><span data-ttu-id="7b328-213">102 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-213">102 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-214">166 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-214">166 kbps</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b328-215">G.722</span><span class="sxs-lookup"><span data-stu-id="7b328-215">G.722</span></span></p></td>
<td><p><span data-ttu-id="7b328-216">105,6 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-216">105.6 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-217">169,6 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-217">169.6 kbps</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b328-218">RTVideo (CIF 15 fps)</span><span class="sxs-lookup"><span data-stu-id="7b328-218">RTVideo (CIF 15 fps)</span></span></p></td>
<td><p><span data-ttu-id="7b328-219">260 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-219">260 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-220">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="7b328-220">Not applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b328-221">RTVideo (VGA de 30 fps)</span><span class="sxs-lookup"><span data-stu-id="7b328-221">RTVideo (VGA 30 fps)</span></span></p></td>
<td><p><span data-ttu-id="7b328-222">610 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-222">610 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-223">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="7b328-223">Not applicable</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="7b328-224">Os requisitos de largura de banda levam em conta a sobrecarga para o seguinte: Ethernet II, IP, protocolo de datagrama de usuário (UDP), RTP (protocolo de transporte em tempo real) e SRTP (Secure real-time Transport Protocol).</span><span class="sxs-lookup"><span data-stu-id="7b328-224">Bandwidth requirements take into account overhead for the following: Ethernet II, IP, User Datagram Protocol (UDP), RTP (real-time transport protocol), and SRTP (secure real-time transport protocol).</span></span> <span data-ttu-id="7b328-225">Eles também incluem 10 kbps para a sobrecarga RTCP.</span><span class="sxs-lookup"><span data-stu-id="7b328-225">They also include 10 kbps for RTCP overhead.</span></span>



</div>

<span data-ttu-id="7b328-226">Os codecs G. 722.1 e sirene são semelhantes, mas oferecem tarifas de bit diferentes.</span><span class="sxs-lookup"><span data-stu-id="7b328-226">The G.722.1 and Siren codecs are similar, but they offer different bit rates.</span></span>

<span data-ttu-id="7b328-227">O G. 722, o codec padrão para a conferência do Lync Server, é completamente diferente dos codecs G. 722.1 e sirene.</span><span class="sxs-lookup"><span data-stu-id="7b328-227">G.722, the default codec for Lync Server conferencing, is completely different from the G.722.1 and Siren codecs.</span></span>

<span data-ttu-id="7b328-228">O codec sirene é usado no Lync Server nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="7b328-228">The Siren codec is used in Lync Server in the following situations:</span></span>

  - <span data-ttu-id="7b328-229">Se a política de largura de banda estiver definida como muito baixa para G. 722 a ser usada.</span><span class="sxs-lookup"><span data-stu-id="7b328-229">If the bandwidth policy is set too low for G.722 to be used.</span></span>

  - <span data-ttu-id="7b328-230">Se um cliente do Communications Server 2007 ou Communications Server 2007 R2 se conectar a um serviço de conferência do Lync Server (pois esses clientes não dão suporte para o codec G. 722).</span><span class="sxs-lookup"><span data-stu-id="7b328-230">If a Communications Server 2007 or Communications Server 2007 R2 client connects to a Lync Server conferencing service (because those clients do not support the G.722 codec).</span></span>

### <a name="bandwidth-utilization-by-scenario"></a><span data-ttu-id="7b328-231">Utilização da largura de banda por cenário</span><span class="sxs-lookup"><span data-stu-id="7b328-231">Bandwidth utilization by scenario</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b328-232">Cenário</span><span class="sxs-lookup"><span data-stu-id="7b328-232">Scenario</span></span></th>
<th><span data-ttu-id="7b328-233">Requisitos de largura de banda otimizados para quantidade (Kbps)</span><span class="sxs-lookup"><span data-stu-id="7b328-233">Bandwidth requirement optimized for quantity (kbps)</span></span></th>
<th><span data-ttu-id="7b328-234">Requisitos de largura de banda para o modo balanceado (Kbps)</span><span class="sxs-lookup"><span data-stu-id="7b328-234">Bandwidth requirement for Balanced mode (kbps)</span></span></th>
<th><span data-ttu-id="7b328-235">Requisitos de largura de banda otimizados para qualidade (Kbps)</span><span class="sxs-lookup"><span data-stu-id="7b328-235">Bandwidth requirement optimized for quality (kbps)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b328-236">Chamadas de áudio ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="7b328-236">Peer-to-peer audio calls</span></span></p></td>
<td><p><span data-ttu-id="7b328-237">45 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-237">45 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-238">62 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-238">62 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-239">91 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-239">91 kbps</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b328-240">Chamadas em conferência</span><span class="sxs-lookup"><span data-stu-id="7b328-240">Conference calls</span></span></p></td>
<td><p><span data-ttu-id="7b328-241">53 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-241">53 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-242">101 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-242">101 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-243">165 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-243">165 kbps</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b328-244">Chamadas PSTN (entre o Lync 2013 e o gateway PSTN com bypass de mídia)</span><span class="sxs-lookup"><span data-stu-id="7b328-244">PSTN calls (between Lync 2013 and PSTN gateway, with media bypass)</span></span></p></td>
<td><p><span data-ttu-id="7b328-245">97 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-245">97 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-246">97 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-246">97 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-247">161 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-247">161 kbps</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b328-248">Chamadas PSTN (entre o Lync 2013 e o servidor de mediação, sem bypass de mídia)</span><span class="sxs-lookup"><span data-stu-id="7b328-248">PSTN calls (between Lync 2013 and Mediation Server, without media bypass)</span></span></p></td>
<td><p><span data-ttu-id="7b328-249">45 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-249">45 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-250">97 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-250">97 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-251">161 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-251">161 kbps</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b328-252">Chamadas PSTN (entre o servidor de mediação e o gateway PSTN sem bypass de mídia)</span><span class="sxs-lookup"><span data-stu-id="7b328-252">PSTN calls (between Mediation Server and PSTN gateway, without media bypass)</span></span></p></td>
<td><p><span data-ttu-id="7b328-253">97 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-253">97 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-254">97 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-254">97 kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-255">161 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-255">161 kbps</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b328-256">Chamadas do Lync Polycom</span><span class="sxs-lookup"><span data-stu-id="7b328-256">Lync - Polycom calls</span></span></p></td>
<td><p><span data-ttu-id="7b328-257">101 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-257">101 Kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-258">101 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-258">101 Kbps</span></span></p></td>
<td><p><span data-ttu-id="7b328-259">101 kbps</span><span class="sxs-lookup"><span data-stu-id="7b328-259">101 Kbps</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="identify-ip-subnets"></a><span data-ttu-id="7b328-260">Identifique as subredes IP</span><span class="sxs-lookup"><span data-stu-id="7b328-260">Identify IP Subnets</span></span>

<span data-ttu-id="7b328-261">Para cada site de rede, você precisará trabalhar com o administrador da rede para determinar quais sub-redes IP serão atribuídas a cada site de rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-261">For each network site, you will need to work with your network administrator to determine what IP subnets are assigned to each network site.</span></span> <span data-ttu-id="7b328-262">Se seu administrador de rede já organizou as subredes IP em regiões de rede e sites de rede, seu trabalho fica muito mais simples.</span><span class="sxs-lookup"><span data-stu-id="7b328-262">If your network administrator has already organized the IP subnets into network regions and network sites, then your work is significantly simplified.</span></span>

<span data-ttu-id="7b328-263">Em nosso exemplo, o site de Nova York na região da América do Norte recebe as seguintes sub-redes de IP: 172.29.80.0/23, 157.57.216.0/25, 172.29.91.0/23, 172.29.81.0/24.</span><span class="sxs-lookup"><span data-stu-id="7b328-263">In our example, the New York site in the North America region is assigned the following IP subnets: 172.29.80.0/23, 157.57.216.0/25, 172.29.91.0/23, 172.29.81.0/24.</span></span> <span data-ttu-id="7b328-264">Suponha que o Bob geralmente funcione no Detroit, vá para o escritório de Nova York para treinamento.</span><span class="sxs-lookup"><span data-stu-id="7b328-264">Suppose Bob, who typically works in Detroit, travels to the New York office for training.</span></span> <span data-ttu-id="7b328-265">Quando ele ligar o computador e se conectar à rede, o computador receberá um endereço IP em um dos quatro intervalos reservados para Nova York, por exemplo, 172.29.80.103.</span><span class="sxs-lookup"><span data-stu-id="7b328-265">When he turns on his computer and connects to the network, his computer will get an IP address in one of the four ranges reserved for New York, for example 172.29.80.103.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="7b328-266">As sub-redes IP especificadas durante a configuração de rede no servidor devem corresponder ao formato fornecido pelos computadores cliente para serem usadas corretamente para o bypass de mídia.</span><span class="sxs-lookup"><span data-stu-id="7b328-266">The IP subnets specified during network configuration on the server must match the format provided by client computers in order to be properly used for media bypass.</span></span> <span data-ttu-id="7b328-267">Um cliente do Lync assume seu endereço IP local e mascara o endereço IP com a máscara de sub-rede associada.</span><span class="sxs-lookup"><span data-stu-id="7b328-267">A Lync client takes its local IP address and masks the IP address with the associated subnet mask.</span></span> <span data-ttu-id="7b328-268">Ao determinar a ID de bypass associada a cada cliente, o registrador irá comparar a lista de sub-redes IP associadas a cada site de rede em relação à sub-rede fornecida pelo cliente para uma correspondência exata.</span><span class="sxs-lookup"><span data-stu-id="7b328-268">When determining the bypass ID associated with each client, the Registrar will compare the list of IP subnets associated with each network site against the subnet provided by the client for an exact match.</span></span> <span data-ttu-id="7b328-269">Por este motivo, é importante que as subredes inseridas durante a configuração de rede no servidor sejam subredes reais ao invés de subredes virtuais.</span><span class="sxs-lookup"><span data-stu-id="7b328-269">For this reason, it is important that subnets entered during network configuration on the server are actual subnets instead of virtual subnets.</span></span> <span data-ttu-id="7b328-270">(Se você implantar o controle de admissão de chamada, mas não o bypass de mídia, o controle de admissão de chamada funcionará mesmo se você configurar as subredes virtuais.)</span><span class="sxs-lookup"><span data-stu-id="7b328-270">(If you deploy call admission control, but not media bypass, call admission control will function properly even if you configure virtual subnets.)</span></span><BR><span data-ttu-id="7b328-271">Por exemplo, se um cliente entrar em um computador com um endereço IP de 172.29.81.57 com uma máscara de sub-rede IP de 255.255.255.0, o Lync 2013 solicitará a ID de bypass associada à 172.29.81.0 de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="7b328-271">For example, if a client signs in on a computer with an IP address of 172.29.81.57 with an IP subnet mask of 255.255.255.0, Lync 2013 will request the bypass ID associated with subnet 172.29.81.0.</span></span> <span data-ttu-id="7b328-272">Se a subrede for definida como 172.29.0.0/16, embora o cliente pertença à subrede virtual, o Registrador não irá considerar uma correspondência porque ele está procurando especificamente pela subrede 172.29.81.0.</span><span class="sxs-lookup"><span data-stu-id="7b328-272">If the subnet is defined as 172.29.0.0/16, although the client belongs to the virtual subnet, the Registrar will not consider this a match because the Registrar is specifically looking for subnet 172.29.81.0.</span></span> <span data-ttu-id="7b328-273">Portanto, é importante que o administrador insira sub-redes exatamente conforme fornecido pelos clientes do Lync (que são provisionados com sub-redes durante a configuração de rede, de forma estática ou por DHCP.)</span><span class="sxs-lookup"><span data-stu-id="7b328-273">Therefore, it is important that the administrator enters subnets exactly as provided by Lync clients (which are provisioned with subnets during network configuration either statically or by DHCP.)</span></span>



<span data-ttu-id="7b328-274"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7b328-274"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

