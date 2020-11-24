---
title: 'Lync Server 2013: Habilitando o roteamento Location-Based'
description: 'Lync Server 2013: Habilitando o roteamento de Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling Location-Based Routing
ms:assetid: 029ede7e-0c4e-4ad2-af99-909ae674d6fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994014(v=OCS.15)
ms:contentKeyID: 51803920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7844af5792468cd5645b6b42c857c63b943c2df1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390151"
---
# <a name="enabling-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="34d50-103">Habilitando o roteamento de Location-Based no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="34d50-103">Enabling Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="34d50-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="34d50-104">

<span> </span></span></span>

<span data-ttu-id="34d50-105">_**Tópico da última modificação:** 2013-04-26_</span><span class="sxs-lookup"><span data-stu-id="34d50-105">_**Topic Last Modified:** 2013-04-26_</span></span>

<span data-ttu-id="34d50-106">Depois que o Enterprise Voice é implantado e as regiões de rede, sites e sub-redes são definidas, você pode habilitar o roteamento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="34d50-106">Once Enterprise Voice is deployed and network regions, sites and subnets are defined, you can enable Location-Based Routing.</span></span> <span data-ttu-id="34d50-107">Location-Based roteamento deve ser habilitado para os seguintes elementos da Enterprise Voice:</span><span class="sxs-lookup"><span data-stu-id="34d50-107">Location-Based Routing must be enabled for the following Enterprise Voice elements:</span></span>

  - <span data-ttu-id="34d50-108">Sites de rede</span><span class="sxs-lookup"><span data-stu-id="34d50-108">Network sites</span></span>

  - <span data-ttu-id="34d50-109">Configurações de tronco</span><span class="sxs-lookup"><span data-stu-id="34d50-109">Trunk configurations</span></span>

  - <span data-ttu-id="34d50-110">Políticas de voz</span><span class="sxs-lookup"><span data-stu-id="34d50-110">Voice policies</span></span>

  - <span data-ttu-id="34d50-111">Configuração de roteamento</span><span class="sxs-lookup"><span data-stu-id="34d50-111">Routing configuration</span></span>

<div>

## <a name="enable-location-based-routing-to-network-sites"></a><span data-ttu-id="34d50-112">Habilitar o roteamento Location-Based para sites de rede</span><span class="sxs-lookup"><span data-stu-id="34d50-112">Enable Location-Based Routing to Network Sites</span></span>

<span data-ttu-id="34d50-113">Depois de implantar o Enterprise Voice e configurar os sites de rede, você estará pronto para configurar o roteamento do Location-Based.</span><span class="sxs-lookup"><span data-stu-id="34d50-113">After you have deployed Enterprise Voice, and configured network sites, you are ready to configure Location-Based Routing.</span></span> <span data-ttu-id="34d50-114">Primeiro, crie uma política de roteamento de voz para associar o site de rede com os usos de PSTN apropriados.</span><span class="sxs-lookup"><span data-stu-id="34d50-114">First, you create a voice routing policy to associate the network site with the appropriate PSTN usages.</span></span> <span data-ttu-id="34d50-115">Ao atribuir usos de PSTN a uma política de roteamento de voz, certifique-se de usar somente os usos de PSTN associados a rotas de voz que usam um gateway PSTN local para o site ou um gateway PSTN localizado em uma região onde Location-Based restrições de roteamento não são necessárias. Use o comando do Windows PowerShell do Lync Server, o New-CsVoiceRoutingPolicy ou o painel de controle do Lync Server para criar políticas de roteamento de voz.</span><span class="sxs-lookup"><span data-stu-id="34d50-115">When assigning PSTN usages to a voice routing policy, make sure to only use PSTN usages that are associated to voice routes that use a PSTN gateway local to the site or a PSTN gateway that is located in a region where Location-Based Routing restrictions are not needed.Use the Lync Server Windows PowerShell command, New-CsVoiceRoutingPolicy, or Lync Server Control Panel to create voice routing policies.</span></span>

    New-CsVoiceRoutingPolicy -Identity <voice routing policy ID> -Name <voice routing policy name> -PstnUsages <usages>

<span data-ttu-id="34d50-116">Para obter mais informações, consulte [New-CsVoiceRoutingPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoiceRoutingPolicy).</span><span class="sxs-lookup"><span data-stu-id="34d50-116">For more information, see [New-CsVoiceRoutingPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoiceRoutingPolicy).</span></span>

<span data-ttu-id="34d50-117">Para este exemplo, a tabela a seguir e os comandos do Windows PowerShell ilustram duas políticas de roteamento de voz e seus usos de PSTN associados definidos nesse cenário.</span><span class="sxs-lookup"><span data-stu-id="34d50-117">For this example, the following table and Windows PowerShell commands illustrate two voice routing policies and their associated PSTN usages defined in this scenario.</span></span> <span data-ttu-id="34d50-118">Somente as configurações específicas do roteamento Location-Based são incluídas na tabela para fins de ilustração.</span><span class="sxs-lookup"><span data-stu-id="34d50-118">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsVoiceRoutingPolicy -Identity "DelhiVoiceRoutingPolicy" -Name "Delhi voice routing policy" -PstnUsages @{add="Delhi usage", "PBX Del usage", "PBX Hyd usage"}
    New-CsVoiceRoutingPolicy -Identity "HyderabadVoiceRoutingPolicy" -Name " Hyderabad voice routing policy" -PstnUsages @{add="Hyderabad usage", "PBX Del usage", "PBX Hyd usage"}


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="34d50-119">Política de roteamento de voz 1</span><span class="sxs-lookup"><span data-stu-id="34d50-119">Voice routing policy 1</span></span></th>
<th><span data-ttu-id="34d50-120">Política de roteamento de voz 2</span><span class="sxs-lookup"><span data-stu-id="34d50-120">Voice routing policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34d50-121">ID da política de voz</span><span class="sxs-lookup"><span data-stu-id="34d50-121">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="34d50-122">Política de roteamento de voz Delhi</span><span class="sxs-lookup"><span data-stu-id="34d50-122">Delhi voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="34d50-123">Política de roteamento de voz Hyderabad</span><span class="sxs-lookup"><span data-stu-id="34d50-123">Hyderabad voice routing policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34d50-124">Usos de PSTN</span><span class="sxs-lookup"><span data-stu-id="34d50-124">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="34d50-125">Uso de Delhi, uso do PBX, uso do PBX Hyd</span><span class="sxs-lookup"><span data-stu-id="34d50-125">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="34d50-126">Uso do Hyderabad, Hyd do PBX, uso do PBX</span><span class="sxs-lookup"><span data-stu-id="34d50-126">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="34d50-127">Em seguida, configure o roteamento Location-Based para os sites de rede aplicáveis e associe suas políticas de roteamento de voz a eles.</span><span class="sxs-lookup"><span data-stu-id="34d50-127">Next, configure Location-Based Routing for the applicable network sites and associate your voice routing policies to them.</span></span> <span data-ttu-id="34d50-128">Use o comando do Windows PowerShell do Lync Server, New-CsNetworkSite, para habilitar Location-Based roteamento e associar políticas de roteamento de voz a seus sites de rede que devem impor restrições de roteamento.</span><span class="sxs-lookup"><span data-stu-id="34d50-128">Use the Lync Server Windows PowerShell command, New-CsNetworkSite, to enable Location-Based Routing and associate voice routing policies to your network sites that must enforce routing restrictions.</span></span>

    Set-CsNetworkSite -Identity <site ID> -EnableLocationBasedRouting <$true|$false> -VoiceRoutingPolicy <voice routing policy ID>

<span data-ttu-id="34d50-129">Neste exemplo, a tabela a seguir ilustra Location-Based roteamento para dois locais de rede diferentes, Delhi e Hyderabad, definido neste cenário usando o Windows PowerShell do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="34d50-129">In this example, the following table illustrates Location-Based Routing for two different network sites, Delhi and Hyderabad, defined in this scenario using the Lync Server Windows PowerShell.</span></span> <span data-ttu-id="34d50-130">Somente as configurações específicas do roteamento Location-Based são incluídas na tabela para fins de ilustração.</span><span class="sxs-lookup"><span data-stu-id="34d50-130">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    Set-CsNetworkSite -Identity "Delhi" -EnableLocationBasedRouting $true -VoiceRoutingPolicy "DelhiVoiceRoutingPolicy"
    Set-CsNetworkSite -Identity "Hyderabad" -EnableLocationBasedRouting $true -VoiceRoutingPolicy "HyderabadVoiceRoutingPolicy"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="34d50-131">Site 1 (Déli)</span><span class="sxs-lookup"><span data-stu-id="34d50-131">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="34d50-132">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="34d50-132">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34d50-133">Nome do site</span><span class="sxs-lookup"><span data-stu-id="34d50-133">Site Name</span></span></p></td>
<td><p><span data-ttu-id="34d50-134">Site 1 (Déli)</span><span class="sxs-lookup"><span data-stu-id="34d50-134">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="34d50-135">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="34d50-135">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34d50-136">EnableLocationBasedRouting</span><span class="sxs-lookup"><span data-stu-id="34d50-136">EnableLocationBasedRouting</span></span></p></td>
<td><p><span data-ttu-id="34d50-137">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="34d50-137">True</span></span></p></td>
<td><p><span data-ttu-id="34d50-138">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="34d50-138">True</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34d50-139">Política de roteamento de voz</span><span class="sxs-lookup"><span data-stu-id="34d50-139">Voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="34d50-140">Política de roteamento de voz Delhi</span><span class="sxs-lookup"><span data-stu-id="34d50-140">Delhi voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="34d50-141">Política de roteamento de voz Hyderabad</span><span class="sxs-lookup"><span data-stu-id="34d50-141">Hyderabad voice routing policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34d50-142">Sub-redes</span><span class="sxs-lookup"><span data-stu-id="34d50-142">Subnets</span></span></p></td>
<td><p><span data-ttu-id="34d50-143">Sub-rede 1 (Déli)</span><span class="sxs-lookup"><span data-stu-id="34d50-143">Subnet 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="34d50-144">Sub-rede 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="34d50-144">Subnet 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-to-trunks"></a><span data-ttu-id="34d50-145">Habilitar roteamento Location-Based para troncos</span><span class="sxs-lookup"><span data-stu-id="34d50-145">Enable Location-Based Routing to Trunks</span></span>

<span data-ttu-id="34d50-146">Antes que uma configuração de tronco possa ser habilitada para roteamento Location-Based, você precisará criar uma configuração de tronco para cada tronco ou site de rede.</span><span class="sxs-lookup"><span data-stu-id="34d50-146">Before a trunk configuration can be enabled for Location-Based Routing, you need to create a trunk configuration for each trunk or each network site.</span></span> <span data-ttu-id="34d50-147">Use o comando do Windows PowerShell do Lync Server, New-CsTrunkConfiguration, para criar uma configuração de tronco.</span><span class="sxs-lookup"><span data-stu-id="34d50-147">Use the Lync Server Windows PowerShell command, New-CsTrunkConfiguration, to create a trunk configuration.</span></span> <span data-ttu-id="34d50-148">Se vários troncos estiverem associados a um determinado sistema (ou seja, gateway ou PBX), cada configuração de tronco deve ser modificada para habilitar restrições de roteamento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="34d50-148">If multiple trunks are associated with a given system (i.e. Gateway or PBX), each trunk configuration must be modified to enable Location-Based Routing restrictions.</span></span>

    New-CsTrunkConfiguration -Identity < trunk configuration ID>

<span data-ttu-id="34d50-149">Para obter mais informações, consulte [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span><span class="sxs-lookup"><span data-stu-id="34d50-149">For more information, see [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span></span>

<span data-ttu-id="34d50-150">Para este exemplo, os comandos do Windows PowerShell a seguir ilustram a criação de uma configuração de tronco para cada tronco na implantação definido neste cenário.</span><span class="sxs-lookup"><span data-stu-id="34d50-150">For this example, the following Windows PowerShell commands illustrate creating one trunk configuration for each trunk in the deployment defined in this scenario.</span></span>

    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 1 DEL-GW>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 2 HYD-GW>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 3 DEL-PBX>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 4 HYD-PBX>"

<span data-ttu-id="34d50-151">Depois que uma configuração de tronco é configurada por tronco, você pode usar o comando do Windows PowerShell do Lync Server, Set-CsTrunkConfiguration, para habilitar Location-Based roteamento para seus troncos que devem impor restrições de roteamento.</span><span class="sxs-lookup"><span data-stu-id="34d50-151">Once a trunk configuration is configured per trunk, you can use the Lync Server Windows PowerShell command, Set-CsTrunkConfiguration, to enable Location-Based Routing to your trunks that must enforce routing restrictions.</span></span> <span data-ttu-id="34d50-152">Habilite o roteamento Location-Based para troncos que roteiam chamadas para gateways PSTN que roteiam chamadas para a PSTN e associe o site de rede onde o gateway está localizado.</span><span class="sxs-lookup"><span data-stu-id="34d50-152">Enable Location-Based Routing to trunks that route calls to PSTN gateways that route calls to the PSTN, and associate the network site where the gateway is located.</span></span>

    Set-CsTrunkConfiguration -Identity <trunk configuration ID> -EnableLocationRestriction $true -NetworkSiteID <site ID>

<span data-ttu-id="34d50-153">Para obter mais informações, consulte [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span><span class="sxs-lookup"><span data-stu-id="34d50-153">For more information, see [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span></span>

<span data-ttu-id="34d50-154">Neste exemplo, Location-Based roteamento está habilitado para cada tronco associado a gateways PSTN em Delhi e Hyderabad:</span><span class="sxs-lookup"><span data-stu-id="34d50-154">In this example, Location-Based Routing is enabled for each trunk that is associated to PSTN gateways in Delhi and Hyderabad:</span></span>

    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 1 DEL-GW -EnableLocationRestriction $true -NetworkSiteID "Delhi"
    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 2 HYD-GW -EnableLocationRestriction $true -NetworkSiteID "Hyderabad"

  

<span data-ttu-id="34d50-155">Não habilite o roteamento de Location-Based para troncos que não roteiam chamadas para a PSTN; no entanto, você ainda deve associar o tronco ao site de rede onde o sistema está localizado como as restrições de roteamento Location-Based precisam ser impostas para que chamadas PSTN atinjam pontos de extremidade conectados por meio deste tronco.</span><span class="sxs-lookup"><span data-stu-id="34d50-155">Do not enable Location-Based Routing for trunks that do not route calls to the PSTN; however, you must still associate the trunk to the network site where the system is located as Location-Based Routing restrictions need to be enforced for PSTN calls reaching endpoints connected via this trunk.</span></span> <span data-ttu-id="34d50-156">Para este exemplo, Location-Based roteamento não está habilitado para cada tronco associado a sistemas PBX em Delhi e Hyderabad:</span><span class="sxs-lookup"><span data-stu-id="34d50-156">For this example, Location-Based Routing is not enabled for each trunk that is associated to PBX systems in Delhi and Hyderabad:</span></span>

    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 3 DEL-PBX -EnableLocationRestriction $false -NetworkSiteID "Delhi"
    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 4 HYD-PBX -EnableLocationRestriction $false -NetworkSiteID "Hyderabad"

  
<span data-ttu-id="34d50-157">Os pontos de extremidade conectados a sistemas que não roteiam chamadas para o PSTN (ou seja, um PBX) terão restrições semelhantes aos pontos de extremidade do Lync dos usuários habilitados para roteamento Location-Based.</span><span class="sxs-lookup"><span data-stu-id="34d50-157">Endpoints that are connected to systems that do not route calls to the PSTN (i.e. a PBX) will have similar restrictions as Lync endpoints of users enabled for Location-Based Routing.</span></span> <span data-ttu-id="34d50-158">Isso significa que esses usuários poderão fazer e receber chamadas de e para o usuário do Lync, independentemente da localização do usuário.</span><span class="sxs-lookup"><span data-stu-id="34d50-158">This means that these users will be able to place and receive calls to and from Lync user regardless of the user’s location.</span></span> <span data-ttu-id="34d50-159">Eles também poderão fazer um recebimento de chamadas para e de outros sistemas que não roteiam chamadas para a rede PSTN (ou seja, um ponto de extremidade conectado a um PBX diferente), independentemente do site de rede ao qual o sistema está associado.</span><span class="sxs-lookup"><span data-stu-id="34d50-159">They will also be able to place an receive calls to and from other systems that do not route calls to the PSTN network (i.e. an endpoint connected to a different PBX) regardless of the network site to which the system is associated.</span></span> <span data-ttu-id="34d50-160">Todas as chamadas recebidas, chamadas de saída, transferências de chamadas e encaminhamento de chamadas que envolvem pontos de extremidade PSTN estarão sujeitas a Location-Based imposição de roteamento.</span><span class="sxs-lookup"><span data-stu-id="34d50-160">All inbound calls, outbound calls, call transfers and call forwarding involving PSTN endpoints will be subject to Location-Based Routing enforcements.</span></span> <span data-ttu-id="34d50-161">Essas chamadas devem usar somente gateways PSTN definidos como locais para tais sistemas.</span><span class="sxs-lookup"><span data-stu-id="34d50-161">Such calls must use only PSTN gateways that are defined as local to such systems.</span></span>

<span data-ttu-id="34d50-162">A tabela a seguir ilustra a configuração de troncos de quatro troncos em dois locais de rede diferentes: dois conectados a gateways PSTN e dois conectados a sistemas PBX.</span><span class="sxs-lookup"><span data-stu-id="34d50-162">The following table illustrates the trunk configuration of four trunks in two different network sites: two connected to PSTN gateways and two connected to PBX systems.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34d50-163">Nome</span><span class="sxs-lookup"><span data-stu-id="34d50-163">Name</span></span></th>
<th><span data-ttu-id="34d50-164">EnableLocationRestriction</span><span class="sxs-lookup"><span data-stu-id="34d50-164">EnableLocationRestriction</span></span></th>
<th><span data-ttu-id="34d50-165">NetworkSiteID</span><span class="sxs-lookup"><span data-stu-id="34d50-165">NetworkSiteID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34d50-166">PstnGateway: tronco 1 DEL-GW</span><span class="sxs-lookup"><span data-stu-id="34d50-166">PstnGateway:Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="34d50-167">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="34d50-167">True</span></span></p></td>
<td><p><span data-ttu-id="34d50-168">Site 1 (Déli)</span><span class="sxs-lookup"><span data-stu-id="34d50-168">Site 1 (Delhi)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34d50-169">PstnGateway: tronco 2 HYD-GW</span><span class="sxs-lookup"><span data-stu-id="34d50-169">PstnGateway:Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="34d50-170">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="34d50-170">True</span></span></p></td>
<td><p><span data-ttu-id="34d50-171">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="34d50-171">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34d50-172">PstnGateway: tronco 3 DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="34d50-172">PstnGateway:Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="34d50-173">Falso</span><span class="sxs-lookup"><span data-stu-id="34d50-173">False</span></span></p></td>
<td><p><span data-ttu-id="34d50-174">Site 1 (Déli)</span><span class="sxs-lookup"><span data-stu-id="34d50-174">Site 1 (Delhi)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34d50-175">PstnGateway: trunk 4 HYD-PBX</span><span class="sxs-lookup"><span data-stu-id="34d50-175">PstnGateway:Trunk 4 HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="34d50-176">Falso</span><span class="sxs-lookup"><span data-stu-id="34d50-176">False</span></span></p></td>
<td><p><span data-ttu-id="34d50-177">Site 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="34d50-177">Site 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-to-voice-policies"></a><span data-ttu-id="34d50-178">Habilitar o roteamento Location-Based para políticas de voz</span><span class="sxs-lookup"><span data-stu-id="34d50-178">Enable Location-Based Routing to Voice Policies</span></span>

<span data-ttu-id="34d50-179">Para impor Location-Based roteamento a usuários específicos, configure a política de voz dos usuários para impedir que a chamada em PSTN seja ignorada.</span><span class="sxs-lookup"><span data-stu-id="34d50-179">To enforce Location-Based Routing to specific users, configure those users’ voice policy to prevent PSTN toll bypass.</span></span> <span data-ttu-id="34d50-180">Use o comando do Windows PowerShell do Lync Server, New-CsVoicePolicy, para criar uma nova política de voz ou Set-CsVoicePolicy, se estiver usando uma política existente, para habilitar Location-Based roteamento impedindo o desvio de chamada PSTN.</span><span class="sxs-lookup"><span data-stu-id="34d50-180">Use the Lync Server Windows PowerShell command, New-CsVoicePolicy, to create a new voice policy or Set-CsVoicePolicy, if using an existing policy, to enable Location-Based Routing by preventing PSTN toll bypass.</span></span>

    Set-CsVoicePolicy -Identity <voice policy ID> -PreventPSTNTollBypass <$true|$false>

<span data-ttu-id="34d50-181">Para obter mais informações, consulte [New-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoicePolicy).</span><span class="sxs-lookup"><span data-stu-id="34d50-181">For more information, see [New-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoicePolicy).</span></span>

<span data-ttu-id="34d50-182">Para este exemplo, a tabela a seguir e os comandos do Windows PowerShell ilustram a prevenção de bypass de chamada PSTN para as políticas de voz Delhi e Hyderabad definidas nesse cenário.</span><span class="sxs-lookup"><span data-stu-id="34d50-182">For this example, the following table and Windows PowerShell commands illustrate enabling the prevention of PSTN toll bypass to the Delhi and Hyderabad voice policies defined in this scenario.</span></span> <span data-ttu-id="34d50-183">Somente as configurações específicas do roteamento Location-Based são incluídas na tabela para fins de ilustração.</span><span class="sxs-lookup"><span data-stu-id="34d50-183">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    Set-CsVoicePolicy -Identity "Delhi voice policy" -PreventPSTNTollBypass $true
    Set-CsVoicePolicy -Identity "Hyderabad voice policy" -PreventPSTNTollBypass $true


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="34d50-184">Política de voz 1</span><span class="sxs-lookup"><span data-stu-id="34d50-184">Voice policy 1</span></span></th>
<th><span data-ttu-id="34d50-185">Política de voz 2</span><span class="sxs-lookup"><span data-stu-id="34d50-185">Voice policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34d50-186">ID da política de voz</span><span class="sxs-lookup"><span data-stu-id="34d50-186">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="34d50-187">Política de voz de Délhi</span><span class="sxs-lookup"><span data-stu-id="34d50-187">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="34d50-188">Política de voz Hyderabad</span><span class="sxs-lookup"><span data-stu-id="34d50-188">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34d50-189">Usos de PSTN</span><span class="sxs-lookup"><span data-stu-id="34d50-189">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="34d50-190">Uso de Delhi, uso do PBX, uso do PBX Hyd</span><span class="sxs-lookup"><span data-stu-id="34d50-190">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="34d50-191">Uso do Hyderabad, Hyd do PBX, uso do PBX</span><span class="sxs-lookup"><span data-stu-id="34d50-191">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34d50-192">PreventPSTNTollBypass</span><span class="sxs-lookup"><span data-stu-id="34d50-192">PreventPSTNTollBypass</span></span></p></td>
<td><p><span data-ttu-id="34d50-193">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="34d50-193">True</span></span></p></td>
<td><p><span data-ttu-id="34d50-194">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="34d50-194">True</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-in-the-routing-configuration"></a><span data-ttu-id="34d50-195">Habilitar o roteamento de Location-Based na configuração de roteamento</span><span class="sxs-lookup"><span data-stu-id="34d50-195">Enable Location-Based Routing in the routing configuration</span></span>

<span data-ttu-id="34d50-196">Por fim, habilite globalmente o roteamento de Location-Based para sua configuração de roteamento.</span><span class="sxs-lookup"><span data-stu-id="34d50-196">Finally, globally enable Location-Based Routing to your routing configuration.</span></span> <span data-ttu-id="34d50-197">Use o comando do Windows PowerShell do Lync Server, New-CsRoutingConfiguration, para habilitar o roteamento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="34d50-197">Use the Lync Server Windows PowerShell command, New-CsRoutingConfiguration, to enable Location-Based Routing.</span></span>

    Set-CsRoutingConfiguration -EnableLocationBasedRouting $true

<span data-ttu-id="34d50-198">Para obter mais informações, consulte [set-CsRoutingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsRoutingConfiguration).</span><span class="sxs-lookup"><span data-stu-id="34d50-198">For more information, see [Set-CsRoutingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsRoutingConfiguration).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="34d50-199">Embora Location-Based roteamento deva ser habilitado por meio de uma configuração global, o conjunto de regras a ser aplicado só será imposto para os sites, os usuários e os troncos para os quais foram configurados conforme especificado nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="34d50-199">while Location-Based Routing must be enabled via a global configuration, the set of rules to be applied will only be enforced for the sites, users and trunks for which it has been configured as specified in this documentation.</span></span>



</div>

<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="34d50-200">Confira também</span><span class="sxs-lookup"><span data-stu-id="34d50-200">See Also</span></span>


[<span data-ttu-id="34d50-201">Configurando o Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="34d50-201">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="34d50-202"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="34d50-202"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

