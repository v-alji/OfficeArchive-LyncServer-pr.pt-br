---
title: 'Lync Server 2013: Implantando regiões de rede, sites e sub-redes'
description: 'Lync Server 2013: Implantando regiões de rede, sites e sub-redes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying network regions, sites, and subnets
ms:assetid: c4b75601-3538-4d07-8d23-1ad90459ae48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994067(v=OCS.15)
ms:contentKeyID: 51803978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1c4c08cd9b78b1439000cdb4a7bbe3ffc2f99d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429843"
---
# <a name="deploying-network-regions-sites-and-subnets-in-lync-server-2013"></a><span data-ttu-id="01ffd-103">Implantando regiões de rede, sites e sub-redes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="01ffd-103">Deploying network regions, sites, and subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="01ffd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="01ffd-104">

<span> </span></span></span>

<span data-ttu-id="01ffd-105">_**Tópico da última modificação:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="01ffd-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="01ffd-106">Depois que o Enterprise Voice for implantado, você precisará configurar:</span><span class="sxs-lookup"><span data-stu-id="01ffd-106">Once Enterprise Voice is deployed, you need to configure:</span></span>

  - <span data-ttu-id="01ffd-107">Regiões de rede</span><span class="sxs-lookup"><span data-stu-id="01ffd-107">Network regions</span></span>

  - <span data-ttu-id="01ffd-108">Sites de rede</span><span class="sxs-lookup"><span data-stu-id="01ffd-108">Network sites</span></span>

  - <span data-ttu-id="01ffd-109">Sub-redes de rede</span><span class="sxs-lookup"><span data-stu-id="01ffd-109">Network subnets</span></span>

<div>

## <a name="define-network-regions"></a><span data-ttu-id="01ffd-110">Definir regiões de rede</span><span class="sxs-lookup"><span data-stu-id="01ffd-110">Define Network Regions</span></span>

<span data-ttu-id="01ffd-111">Use o comando do Windows PowerShell do Lync Server, novo-CsNetworkRegion ou o painel de controle do Lync Server para definir regiões de rede.</span><span class="sxs-lookup"><span data-stu-id="01ffd-111">Use the Lync Server Windows PowerShell command, New-CsNetworkRegion, or Lync Server Control Panel to define network regions.</span></span>

    New-CsNetworkRegion -NetworkRegionID <region ID> -CentralSite <site ID>

<span data-ttu-id="01ffd-112">Para obter mais informações, consulte [New-CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion).</span><span class="sxs-lookup"><span data-stu-id="01ffd-112">For more information, see [New-CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion).</span></span>

<span data-ttu-id="01ffd-113">Para este exemplo, o seguinte comando do Windows PowerShell ilustra a região de rede, região 1 (Índia), definida nesse cenário.</span><span class="sxs-lookup"><span data-stu-id="01ffd-113">For this example, the following Windows PowerShell command illustrates the network region, region 1 (India), defined in this scenario.</span></span>

    New-CsNetworkRegion -NetworkRegionID "India" -CentralSite "India Central Site"

<div>


</div>

</div>

<div>

## <a name="define-network-sites"></a><span data-ttu-id="01ffd-114">Definir sites de rede</span><span class="sxs-lookup"><span data-stu-id="01ffd-114">Define Network Sites</span></span>

<span data-ttu-id="01ffd-115">Use o comando do Windows PowerShell do Lync Server, novo-CsNetworkSite ou o painel de controle do Lync Server para definir sites de rede.</span><span class="sxs-lookup"><span data-stu-id="01ffd-115">Use the Lync Server Windows PowerShell command, New-CsNetworkSite, or the Lync Server Control Panel to define network sites.</span></span>

    New-CsNetworkSite -NetworkSiteID <site ID> -NetworkRegionID <region ID>

<span data-ttu-id="01ffd-116">Para obter mais informações, consulte [New-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite).</span><span class="sxs-lookup"><span data-stu-id="01ffd-116">For more information, see [New-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite).</span></span>

<span data-ttu-id="01ffd-117">Para este exemplo, a tabela a seguir e o comando do Windows PowerShell do Lync Server ilustram os sites de rede definidos neste cenário.</span><span class="sxs-lookup"><span data-stu-id="01ffd-117">For this example, the following table and Lync Server Windows PowerShell command illustrate the network sites defined in this scenario.</span></span> <span data-ttu-id="01ffd-118">Somente as configurações específicas do roteamento Location-Based são incluídas na tabela para fins de ilustração.</span><span class="sxs-lookup"><span data-stu-id="01ffd-118">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsNetworkSite -NetworkSiteID "Delhi" -NetworkRegionID "India"
    New-CsNetworkSite -NetworkSiteID "Hyderabad" -NetworkRegionID "India"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="01ffd-119">Site 1 (Déli)</span><span class="sxs-lookup"><span data-stu-id="01ffd-119">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="01ffd-120">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="01ffd-120">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01ffd-121">ID do site</span><span class="sxs-lookup"><span data-stu-id="01ffd-121">Site ID</span></span></p></td>
<td><p><span data-ttu-id="01ffd-122">Site 1 (Déli)</span><span class="sxs-lookup"><span data-stu-id="01ffd-122">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="01ffd-123">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="01ffd-123">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01ffd-124">ID da região</span><span class="sxs-lookup"><span data-stu-id="01ffd-124">Region ID</span></span></p></td>
<td><p><span data-ttu-id="01ffd-125">Região 1 (Índia)</span><span class="sxs-lookup"><span data-stu-id="01ffd-125">Region 1 (India)</span></span></p></td>
<td><p><span data-ttu-id="01ffd-126">Região 1 (Índia)</span><span class="sxs-lookup"><span data-stu-id="01ffd-126">Region 1 (India)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-network-subnets"></a><span data-ttu-id="01ffd-127">Definir sub-redes de rede</span><span class="sxs-lookup"><span data-stu-id="01ffd-127">Define Network Subnets</span></span>

<span data-ttu-id="01ffd-128">Use o comando do Windows PowerShell do Lync Server, novo-CsNetworkSubnet ou o painel de controle do Lync Server para definir sub-redes de rede e atribuí-las a sites de rede.</span><span class="sxs-lookup"><span data-stu-id="01ffd-128">Use the Lync Server Windows PowerShell command, New-CsNetworkSubnet, or the Lync Server Control Panel to define network subnets and assign them to network sites.</span></span>

    New-CsNetworkSubnet -SubnetID <Subnet IP address> -MaskBits <Subnet bitmask> -NetworkSiteID <site ID>

<span data-ttu-id="01ffd-129">Para obter mais informações, consulte [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span><span class="sxs-lookup"><span data-stu-id="01ffd-129">For more information, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<span data-ttu-id="01ffd-130">Para este exemplo, a tabela a seguir e os comandos do Windows PowerShell ilustram a atribuição de sub-redes de rede para os sites de rede, Delhi e Hyderabad, definidas nesse cenário.</span><span class="sxs-lookup"><span data-stu-id="01ffd-130">For this example, the following table and Windows PowerShell commands illustrate the assignment of network subnets to the network sites, Delhi and Hyderabad, defined in this scenario.</span></span> <span data-ttu-id="01ffd-131">Somente as configurações específicas do roteamento Location-Based são incluídas na tabela para fins de ilustração.</span><span class="sxs-lookup"><span data-stu-id="01ffd-131">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsNetworkSubnet -SubnetID "192.168.0.0" -MaskBits "24" -NetworkSiteID "Delhi"
    New-CsNetworkSubnet -SubnetID "192.168.1.0" -MaskBits "24" -NetworkSiteID "Hyderabad"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="01ffd-132">Site 1 (Déli)</span><span class="sxs-lookup"><span data-stu-id="01ffd-132">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="01ffd-133">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="01ffd-133">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01ffd-134">ID de sub-rede</span><span class="sxs-lookup"><span data-stu-id="01ffd-134">Subnet ID</span></span></p></td>
<td><p><span data-ttu-id="01ffd-135">192.168.0.0</span><span class="sxs-lookup"><span data-stu-id="01ffd-135">192.168.0.0</span></span></p></td>
<td><p><span data-ttu-id="01ffd-136">192.168.1.0</span><span class="sxs-lookup"><span data-stu-id="01ffd-136">192.168.1.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01ffd-137">Remoção</span><span class="sxs-lookup"><span data-stu-id="01ffd-137">Mask</span></span></p></td>
<td><p><span data-ttu-id="01ffd-138">24</span><span class="sxs-lookup"><span data-stu-id="01ffd-138">24</span></span></p></td>
<td><p><span data-ttu-id="01ffd-139">24</span><span class="sxs-lookup"><span data-stu-id="01ffd-139">24</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01ffd-140">ID do site</span><span class="sxs-lookup"><span data-stu-id="01ffd-140">Site ID</span></span></p></td>
<td><p><span data-ttu-id="01ffd-141">Site 1 (Déli)</span><span class="sxs-lookup"><span data-stu-id="01ffd-141">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="01ffd-142">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="01ffd-142">Site 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="01ffd-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="01ffd-143">See Also</span></span>


[<span data-ttu-id="01ffd-144">Configurando o Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="01ffd-144">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="01ffd-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="01ffd-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

