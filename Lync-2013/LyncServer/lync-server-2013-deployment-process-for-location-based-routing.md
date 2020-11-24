---
title: 'Lync Server 2013: Processo de implantação para Roteamento Baseado em Local'
description: 'Lync Server 2013: processo de implantação para roteamento Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for Location-Based Routing
ms:assetid: 9e923e72-83fc-4a4f-8937-28a55739ed3e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994055(v=OCS.15)
ms:contentKeyID: 51803966
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2c321d9b0eada6e9501b2ded69120feae36be171
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390245"
---
# <a name="deployment-process-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="ca5d2-103">Processo de implantação para Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ca5d2-103">Deployment process for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ca5d2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ca5d2-104">

<span> </span></span></span>

<span data-ttu-id="ca5d2-105">_**Tópico da última modificação:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="ca5d2-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="ca5d2-106">Este tópico fornece uma visão geral do processo envolvido na configuração do roteamento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-106">This topic provides an overview of the process involved in configuring Location-Based Routing.</span></span> <span data-ttu-id="ca5d2-107">Você deve implantar o Lync Server Enterprise Edition ou Standard Edition com o Enterprise Voice antes de configurar o roteamento do Location-Based.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-107">You must deploy Lync Server Enterprise Edition or Standard Edition with Enterprise Voice before you configure Location-Based Routing.</span></span> <span data-ttu-id="ca5d2-108">Os componentes exigidos pelo roteamento do Location-Based já estão instalados e habilitados durante a implantação do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-108">The components required by Location-Based Routing are already installed and enabled when you deploy Enterprise Voice.</span></span>

### <a name="location-based-routing-deployment-process"></a><span data-ttu-id="ca5d2-109">Location-Based processo de implantação de roteamento</span><span class="sxs-lookup"><span data-stu-id="ca5d2-109">Location-Based Routing Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca5d2-110">Fase</span><span class="sxs-lookup"><span data-stu-id="ca5d2-110">Phase</span></span></th>
<th><span data-ttu-id="ca5d2-111">Etapas</span><span class="sxs-lookup"><span data-stu-id="ca5d2-111">Steps</span></span></th>
<th><span data-ttu-id="ca5d2-112">Grupos e funções necessários</span><span class="sxs-lookup"><span data-stu-id="ca5d2-112">Required groups and roles</span></span></th>
<th><span data-ttu-id="ca5d2-113">Documentação de Implantação</span><span class="sxs-lookup"><span data-stu-id="ca5d2-113">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca5d2-114">Implantar o Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="ca5d2-114">Deploy Enterprise Voice</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="ca5d2-115">Configurar troncos</span><span class="sxs-lookup"><span data-stu-id="ca5d2-115">Configure Trunks</span></span></p></li>
<li><p><span data-ttu-id="ca5d2-116">Criar políticas de voz</span><span class="sxs-lookup"><span data-stu-id="ca5d2-116">Create Voice Policies</span></span></p></li>
<li><p><span data-ttu-id="ca5d2-117">Definir roteiros de voz</span><span class="sxs-lookup"><span data-stu-id="ca5d2-117">Define Voice Routes</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="ca5d2-118">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="ca5d2-118">CSVoiceAdmins</span></span><br />
<span data-ttu-id="ca5d2-119">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="ca5d2-119">CsAdministrator</span></span><br />
<span data-ttu-id="ca5d2-120">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="ca5d2-120">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-121">Implantação do Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="ca5d2-121">Deploying Enterprise Voice</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca5d2-122">Verificar a implantação do Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="ca5d2-122">Verify your Enterprise Voice deployment</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ca5d2-123">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="ca5d2-123">CSVoiceAdmins</span></span><br />
<span data-ttu-id="ca5d2-124">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="ca5d2-124">CsAdministrator</span></span><br />
<span data-ttu-id="ca5d2-125">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="ca5d2-125">CsServerAdministrator</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca5d2-126">Configurar regiões de rede, sites e sub-redes</span><span class="sxs-lookup"><span data-stu-id="ca5d2-126">Configure network regions, sites, and subnets</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="ca5d2-127">Criar regiões de rede</span><span class="sxs-lookup"><span data-stu-id="ca5d2-127">Create network regions</span></span></p></li>
<li><p><span data-ttu-id="ca5d2-128">Criar sites de rede</span><span class="sxs-lookup"><span data-stu-id="ca5d2-128">Create network sites</span></span></p></li>
<li><p><span data-ttu-id="ca5d2-129">Associa sub-redes a sites de rede</span><span class="sxs-lookup"><span data-stu-id="ca5d2-129">Associates subnets with network sites</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="ca5d2-130">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="ca5d2-130">CSVoiceAdmins</span></span><br />
<span data-ttu-id="ca5d2-131">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="ca5d2-131">CsAdministrator</span></span><br />
<span data-ttu-id="ca5d2-132">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="ca5d2-132">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-133">Sobre regiões de rede, sites e sub-redes</span><span class="sxs-lookup"><span data-stu-id="ca5d2-133">About Network Regions, Sites, and Subnets</span></span><br />
<span data-ttu-id="ca5d2-134">Criar ou modificar uma região de rede</span><span class="sxs-lookup"><span data-stu-id="ca5d2-134">Create or Modify a Network Region</span></span><br />
<span data-ttu-id="ca5d2-135">Criar ou modificar um site de rede</span><span class="sxs-lookup"><span data-stu-id="ca5d2-135">Create or Modify a Network Site</span></span><br />
<span data-ttu-id="ca5d2-136">Associar uma sub-rede a um site de rede</span><span class="sxs-lookup"><span data-stu-id="ca5d2-136">Associate a Subnet with a Network Site</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca5d2-137">Configurar o roteamento Location-Based</span><span class="sxs-lookup"><span data-stu-id="ca5d2-137">Configure Location-Based Routing</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="ca5d2-138">Criar políticas de roteamento de voz</span><span class="sxs-lookup"><span data-stu-id="ca5d2-138">Create voice routing policies</span></span></p></li>
<li><p><span data-ttu-id="ca5d2-139">Definir configuração de tronco separada por tronco</span><span class="sxs-lookup"><span data-stu-id="ca5d2-139">Define separate trunk configuration per trunk</span></span></p></li>
<li><p><span data-ttu-id="ca5d2-140">Modificar políticas de voz</span><span class="sxs-lookup"><span data-stu-id="ca5d2-140">Modify voice policies</span></span></p></li>
<li><p><span data-ttu-id="ca5d2-141">Habilitar a configuração de roteamento Location-Based</span><span class="sxs-lookup"><span data-stu-id="ca5d2-141">Enable Location-Based Routing configuration</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="ca5d2-142">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="ca5d2-142">CSVoiceAdmins</span></span><br />
<span data-ttu-id="ca5d2-143">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="ca5d2-143">CsAdministrator</span></span><br />
<span data-ttu-id="ca5d2-144">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="ca5d2-144">CsServerAdministrator</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="sample-deployment"></a><span data-ttu-id="ca5d2-145">Exemplo de implantação</span><span class="sxs-lookup"><span data-stu-id="ca5d2-145">Sample Deployment</span></span>

<span data-ttu-id="ca5d2-146">A implantação a seguir é usada para ilustrar mais os mecanismos habilitados pelo roteamento Location-Based.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-146">The following deployment is used to illustrate further the mechanisms enabled by Location-Based Routing.</span></span>

<span data-ttu-id="ca5d2-147">![e1bd2230-44da-4784-B359-24572b6ce02d](images/JJ994055.e1bd2230-44da-4784-b359-24572b6ce02d(OCS.15).png "e1bd2230-44da-4784-B359-24572b6ce02d")</span><span class="sxs-lookup"><span data-stu-id="ca5d2-147">![e1bd2230-44da-4784-b359-24572b6ce02d](images/JJ994055.e1bd2230-44da-4784-b359-24572b6ce02d(OCS.15).png "e1bd2230-44da-4784-b359-24572b6ce02d")</span></span>

<div>

## <a name="incoming-pstn-calls"></a><span data-ttu-id="ca5d2-148">Chamadas PSTN recebidas</span><span class="sxs-lookup"><span data-stu-id="ca5d2-148">Incoming PSTN calls</span></span>

<span data-ttu-id="ca5d2-149">Um administrador pode habilitar o tronco definido para direcionar chamadas para "gateway do site 1" para Location-Based roteamento e associar o "gateway do site 1" ao site 1.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-149">An administrator can enable the trunk defined to route calls to “Site 1 Gateway” for Location-Based Routing and associate the “Site 1 Gateway” to site 1.</span></span> <span data-ttu-id="ca5d2-150">Uma vez habilitada, as chamadas roteadas pelo "gateway do site 1" só serão roteadas para os usuários localizados no site 1.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-150">Once enabled, calls that are routed through “Site 1 Gateway“ will only be routed to users that are located in site 1.</span></span> <span data-ttu-id="ca5d2-151">Todas as chamadas roteadas pelo tronco "gateway do site 1" destinados a usuários em um site diferente, como o site 2 serão bloqueadas para impedir o bypass de chamada PSTN.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-151">All calls routed through the “Site 1 Gateway” trunk destined to users in a different site, such as site 2 will be blocked to prevent PSTN toll bypass.</span></span>

<span data-ttu-id="ca5d2-152">Todas as chamadas PSTN de entrada por meio do "gateway do site 1" só poderão ser roteadas para pontos de extremidade localizados no site 1.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-152">All incoming PSTN calls through “Site 1 Gateway” will only be allowed to route to endpoints located in site 1.</span></span> <span data-ttu-id="ca5d2-153">Por exemplo, quando "usuário do Lync 1" viaja para o site 2, todas as chamadas PSTN de entrada por meio do "gateway do site 1" não serão roteadas para os pontos de extremidade "usuário do Lync 1" localizado no site 2.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-153">For example, when “Lync user 1” travels to site 2, all incoming PSTN calls through “Site 1 Gateway” will not be routed to “Lync user 1” endpoints located in site 2.</span></span> <span data-ttu-id="ca5d2-154">A mesma regra de roteamento se aplica se "usuário do Lync 1" viajar para um site de rede desconhecido onde a localização do usuário não pode ser determinada.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-154">The same routing rule applies if “Lync user 1” travels to an unknown network site where the user’s location can’t be determined.</span></span>

<span data-ttu-id="ca5d2-155">A tabela a seguir descreve a experiência do usuário do "usuário do Lync 1" nesse contexto.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-155">The following table outlines the user experience of “Lync user 1” in this context.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ca5d2-156">Pontos de extremidade de usuário 1 do Lync localizados no site de rede 1</span><span class="sxs-lookup"><span data-stu-id="ca5d2-156">Lync user 1 endpoints located in network site 1</span></span></th>
<th><span data-ttu-id="ca5d2-157">Pontos de extremidade de usuário 1 do Lync localizados no site de rede 2</span><span class="sxs-lookup"><span data-stu-id="ca5d2-157">Lync user 1 endpoints located in network site 2</span></span></th>
<th><span data-ttu-id="ca5d2-158">Pontos de extremidade de usuário 1 do Lync localizados em um site de rede desconhecido</span><span class="sxs-lookup"><span data-stu-id="ca5d2-158">Lync user 1 endpoints located in unknown network site</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca5d2-159">Chamadas PSTN de entrada para o usuário 1 do Lync</span><span class="sxs-lookup"><span data-stu-id="ca5d2-159">Inbound PSTN calls to Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-160">As chamadas são roteadas para pontos de extremidade neste local</span><span class="sxs-lookup"><span data-stu-id="ca5d2-160">Calls are routed to endpoints in this location</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-161">As chamadas não são roteadas para pontos de extremidade neste local</span><span class="sxs-lookup"><span data-stu-id="ca5d2-161">Calls are not routed to endpoints in this location</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-162">As chamadas não são roteadas para pontos de extremidade neste local</span><span class="sxs-lookup"><span data-stu-id="ca5d2-162">Calls are not routed to endpoints in this location</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="outgoing-pstn-calls"></a><span data-ttu-id="ca5d2-163">Chamadas PSTN de saída</span><span class="sxs-lookup"><span data-stu-id="ca5d2-163">Outgoing PSTN calls</span></span>

<span data-ttu-id="ca5d2-164">As rotas de voz são referenciadas em políticas de voz atribuídas diretamente a usuários e políticas de roteamento de voz atribuídas a sites de rede.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-164">Voice routes are referenced in both Voice Policies assigned directly to users, and Voice Routing Policies assigned to network sites.</span></span> <span data-ttu-id="ca5d2-165">Ambas as políticas contêm referências a rotas, que podem ser usadas para direcionar uma chamada de maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-165">Both policies contain references to routes, which can be used to route a call differently.</span></span> <span data-ttu-id="ca5d2-166">Por exemplo, um administrador pode definir uma política de roteamento de voz para todos os usuários localizados no site 1 de rede para direcionar todas as chamadas feitas por meio do "gateway do site 1" enquanto a política de voz de alguns usuários define uma rota para todas as chamadas feitas por meio do "gateway 2 do site".</span><span class="sxs-lookup"><span data-stu-id="ca5d2-166">For example, an administrator can define a Voice Routing Policy for all users located in network site 1 to route all outbound calls through the “Site 1 Gateway” while the Voice Policy of some users define a route for all outbound calls through the “Site 2 Gateway”.</span></span> <span data-ttu-id="ca5d2-167">Enquanto esses usuários estão localizados no site da rede 1, suas chamadas de saída serão roteadas pelo "gateway do site 1".</span><span class="sxs-lookup"><span data-stu-id="ca5d2-167">While these users are located in network site 1, their outbound calls will be routed through the “Site 1 Gateway”.</span></span>

<span data-ttu-id="ca5d2-168">Quando um usuário está localizado em um site de rede configurado para roteamento Location-Based, a rota da política de roteamento de voz do site da rede substitui a rota de política de voz do usuário.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-168">When a user is located in a network site configured for Location-Based Routing, the network site’s Voice Routing Policy route overrides the user’s Voice Policy route.</span></span> <span data-ttu-id="ca5d2-169">Essa regra é particularmente útil para os usuários que se movem temporariamente para um site diferente.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-169">This rule is particularly useful for users that temporarily move to a different site.</span></span> <span data-ttu-id="ca5d2-170">Nesse caso específico, um usuário sempre usará um gateway local para o seu local; Se o "usuário do Lync 3" estiver localizado em "site 2", todas as suas chamadas serão roteadas pelo "gateway do site 2", mas se ele viajar para o site 1, todas as suas chamadas feitas durante o site 1 serão roteadas pelo "gateway do site 1".</span><span class="sxs-lookup"><span data-stu-id="ca5d2-170">In this particular case a user will always use a gateway that is local to his location; if “Lync user 3” is located at “Site 2”, all his outbound calls will be routed via “Site 2 Gateway”, but if he travels to site 1, all his outbound calls placed while he’s at site 1 will be routed through “Site 1 Gateway”.</span></span>

<span data-ttu-id="ca5d2-171">A tabela a seguir ilustra a experiência do usuário do Lync usuário 1 fazendo uma chamada de saída dos seguintes sites de rede.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-171">The following table illustrates the user experience of Lync user 1 placing an outbound call from the following network sites.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ca5d2-172">Site de rede 1</span><span class="sxs-lookup"><span data-stu-id="ca5d2-172">Network site 1</span></span></th>
<th><span data-ttu-id="ca5d2-173">Site de rede 2</span><span class="sxs-lookup"><span data-stu-id="ca5d2-173">Network site 2</span></span></th>
<th><span data-ttu-id="ca5d2-174">Site de rede desconhecido ou não habilitado para roteamento Location-Based</span><span class="sxs-lookup"><span data-stu-id="ca5d2-174">Unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca5d2-175">Autorização de chamadas de saída</span><span class="sxs-lookup"><span data-stu-id="ca5d2-175">Authorization of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-176">Política de voz do usuário 1 do Lync</span><span class="sxs-lookup"><span data-stu-id="ca5d2-176">Lync user 1 voice policy</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-177">Política de voz do usuário 1 do Lync</span><span class="sxs-lookup"><span data-stu-id="ca5d2-177">Lync user 1 voice policy</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-178">Política de voz do usuário 1 do Lync</span><span class="sxs-lookup"><span data-stu-id="ca5d2-178">Lync user 1 voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca5d2-179">Roteamento de chamadas de saída</span><span class="sxs-lookup"><span data-stu-id="ca5d2-179">Routing of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-180">Política de roteamento de voz do site 1</span><span class="sxs-lookup"><span data-stu-id="ca5d2-180">Site 1 voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-181">Política de roteamento de voz do site 2</span><span class="sxs-lookup"><span data-stu-id="ca5d2-181">Site 2 voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-182">Política de voz do usuário e somente para sistemas não habilitados para roteamento Location-Based</span><span class="sxs-lookup"><span data-stu-id="ca5d2-182">User’s voice policy and only to systems not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="call-transfers-and-forwards"></a><span data-ttu-id="ca5d2-183">Transferências de chamadas e encaminhamentos</span><span class="sxs-lookup"><span data-stu-id="ca5d2-183">Call transfers and forwards</span></span>

<span data-ttu-id="ca5d2-184">Quando as chamadas são transferidas ou encaminhadas, o roteamento de chamadas é afetado pelo roteamento Location-Based.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-184">When calls are transferred or forwarded, the routing of calls is affected by Location-Based Routing.</span></span>

<span data-ttu-id="ca5d2-185">A tabela a seguir descreve o usuário do Lync 1 transferindo ou encaminhando uma chamada PSTN para outro usuário do Lync.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-185">The following table depicts Lync user 1 transferring or forwarding a PSTN call to another Lync user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca5d2-186">Usuário Iniciando transferência ou encaminhamento de chamadas</span><span class="sxs-lookup"><span data-stu-id="ca5d2-186">User initiating call transfer or forward</span></span></th>
<th><span data-ttu-id="ca5d2-187">Usuário do Lync 2</span><span class="sxs-lookup"><span data-stu-id="ca5d2-187">Lync user 2</span></span></th>
<th><span data-ttu-id="ca5d2-188">Usuário do Lync 4</span><span class="sxs-lookup"><span data-stu-id="ca5d2-188">Lync user 4</span></span></th>
<th><span data-ttu-id="ca5d2-189">Usuário do Lync no site de rede não habilitado para roteamento Location-Based</span><span class="sxs-lookup"><span data-stu-id="ca5d2-189">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca5d2-190">Usuário 1 do Lync</span><span class="sxs-lookup"><span data-stu-id="ca5d2-190">Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-191">Encaminhamento ou transferência de chamada permitido</span><span class="sxs-lookup"><span data-stu-id="ca5d2-191">Call forward or transfer is allowed</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-192">Encaminhamento ou transferência de chamada não permitido</span><span class="sxs-lookup"><span data-stu-id="ca5d2-192">Call forward or transfer is not allowed</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-193">Encaminhamento ou transferência de chamada não permitido</span><span class="sxs-lookup"><span data-stu-id="ca5d2-193">Call forward or transfer is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="ca5d2-194">A tabela a seguir ilustra como Location-Based o roteamento afeta a forma como a chamada é roteada com base na localização do usuário do Lync que está sendo transferido (usuário do Lync 2, usuário do Lync 4 etc) para um ponto de extremidade PSTN</span><span class="sxs-lookup"><span data-stu-id="ca5d2-194">The following table illustrates how Location-Based Routing affects how the call is routed based on the location of the Lync user being transferred (Lync user 2, Lync user 4, etc) to a PSTN endpoint</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca5d2-195">Ponto de extremidade onde a chamada é transferida ou encaminhada para</span><span class="sxs-lookup"><span data-stu-id="ca5d2-195">Endpoint where call is transferred or forwarded to</span></span></th>
<th><span data-ttu-id="ca5d2-196">Usuário do Lync 2</span><span class="sxs-lookup"><span data-stu-id="ca5d2-196">Lync user 2</span></span></th>
<th><span data-ttu-id="ca5d2-197">Usuário do Lync 4</span><span class="sxs-lookup"><span data-stu-id="ca5d2-197">Lync user 4</span></span></th>
<th><span data-ttu-id="ca5d2-198">Usuário do Lync no site de rede não habilitado para roteamento Location-Based</span><span class="sxs-lookup"><span data-stu-id="ca5d2-198">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca5d2-199">Ponto de extremidade PSTN</span><span class="sxs-lookup"><span data-stu-id="ca5d2-199">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-200">Encaminhamento de chamadas ou transferência é roteada pela política de roteamento de voz do site 1 e egresso pelo gateway do site 1</span><span class="sxs-lookup"><span data-stu-id="ca5d2-200">Call forward or transfer is routed through site 1 voice routing policy and egress via Site 1 Gateway</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-201">Encaminhamento de chamadas ou transferência é roteada pela política de roteamento de voz do site 2 e egresso via gateway do site 2</span><span class="sxs-lookup"><span data-stu-id="ca5d2-201">Call forward or transfer is routed through site 2 voice routing policy and egress via Site 2 Gateway</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-202">Encaminhamento de chamadas ou transferência é roteada pela política de voz do usuário do Lync e egresso por meio de um gateway não habilitado para roteamento baseado em local (se disponível)</span><span class="sxs-lookup"><span data-stu-id="ca5d2-202">Call forward or transfer is routed through the Lync user voice policy and egress via a gateway not enabled for location-based routing (if available)</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="simultaneous-ringing"></a><span data-ttu-id="ca5d2-203">Toque simultâneo</span><span class="sxs-lookup"><span data-stu-id="ca5d2-203">Simultaneous ringing</span></span>

<span data-ttu-id="ca5d2-204">Quando o roteamento baseado em local está configurado na topologia de exemplo, as seguintes interações são impostas.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-204">Once location-based routing is configured in the sample topology, the following interactions are enforced.</span></span>

<span data-ttu-id="ca5d2-205">A tabela a seguir ilustra se Location-Based roteamento permite o toque simultâneo para diferentes usuários do Lync (ou seja, usuário do Lync 2, usuário do Lync 4 etc.).</span><span class="sxs-lookup"><span data-stu-id="ca5d2-205">The following table illustrates whether Location-Based Routing allows simultaneous ringing for different Lync users (i.e. Lync user 2, Lync user 4, etc).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca5d2-206">Destino da chamada PSTN de entrada</span><span class="sxs-lookup"><span data-stu-id="ca5d2-206">Incoming PSTN call target</span></span></th>
<th><span data-ttu-id="ca5d2-207">Usuário do Lync 2</span><span class="sxs-lookup"><span data-stu-id="ca5d2-207">Lync user 2</span></span></th>
<th><span data-ttu-id="ca5d2-208">Usuário do Lync 4</span><span class="sxs-lookup"><span data-stu-id="ca5d2-208">Lync user 4</span></span></th>
<th><span data-ttu-id="ca5d2-209">Usuário do Lync no site de rede não habilitado para roteamento Location-Based</span><span class="sxs-lookup"><span data-stu-id="ca5d2-209">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca5d2-210">Usuário 1 do Lync</span><span class="sxs-lookup"><span data-stu-id="ca5d2-210">Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-211">O toque simultâneo é permitido</span><span class="sxs-lookup"><span data-stu-id="ca5d2-211">Simultaneous ring is allowed</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-212">O toque simultâneo não é permitido</span><span class="sxs-lookup"><span data-stu-id="ca5d2-212">Simultaneous ring is not allowed</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-213">O toque simultâneo não é permitido</span><span class="sxs-lookup"><span data-stu-id="ca5d2-213">Simultaneous ring is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="ca5d2-214">A tabela a seguir ilustra se Location-Based roteamento permite o toque simultâneo de um ponto de extremidade PSTN de diferentes usuários do Lync (ou seja, usuário do Lync 2, usuário do Lync 4, etc).</span><span class="sxs-lookup"><span data-stu-id="ca5d2-214">The following table illustrates whether Location-Based Routing allows simultaneous ringing to a PSTN endpoint from different Lync users (i.e. Lync user 2, Lync user 4, etc).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca5d2-215">Destino de toque simultâneo</span><span class="sxs-lookup"><span data-stu-id="ca5d2-215">Simultaneous ring target</span></span></th>
<th><span data-ttu-id="ca5d2-216">Usuário do Lync 2</span><span class="sxs-lookup"><span data-stu-id="ca5d2-216">Lync user 2</span></span></th>
<th><span data-ttu-id="ca5d2-217">Usuário do Lync 4</span><span class="sxs-lookup"><span data-stu-id="ca5d2-217">Lync user 4</span></span></th>
<th><span data-ttu-id="ca5d2-218">Usuário do Lync no site de rede não habilitado para roteamento Location-Based</span><span class="sxs-lookup"><span data-stu-id="ca5d2-218">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca5d2-219">Telefone celular usuário 1 do Lync (ponto de extremidade PSTN)</span><span class="sxs-lookup"><span data-stu-id="ca5d2-219">Lync user 1 mobile phone (PSTN endpoint)</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-220">Chamada roteada pela política de roteamento de voz do site 1 e egresso por meio do gateway do site 1</span><span class="sxs-lookup"><span data-stu-id="ca5d2-220">Call routed through network site 1’s voice routing policy and egress via site 1 gateway</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-221">Chamada roteada pela política de roteamento de voz do site 2 da rede e egresso via gateway do site 2</span><span class="sxs-lookup"><span data-stu-id="ca5d2-221">Call routed through network site 2’s voice routing policy and egress via site 2 gateway</span></span></p></td>
<td><p><span data-ttu-id="ca5d2-222">Chamada roteada pela política de voz do chamador e será egresso por meio de um gateway PSTN não habilitado para roteamento Location-Based</span><span class="sxs-lookup"><span data-stu-id="ca5d2-222">Call routed through the caller voice policy and will egress via a PSTN gateway not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ca5d2-223">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca5d2-223">See Also</span></span>


[<span data-ttu-id="ca5d2-224">Planejamento de Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ca5d2-224">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="ca5d2-225"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ca5d2-225"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

