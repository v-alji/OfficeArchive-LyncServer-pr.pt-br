---
title: 'Lync Server 2013: requisitos para o roteamento Location-Based para conferência'
description: 'Lync Server 2013: requisitos para o roteamento Location-Based para conferência.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Requirements for Location-Based Routing for conferencing
ms:assetid: 766d9286-2c34-4faf-bb3e-f0ca478a70cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362806(v=OCS.15)
ms:contentKeyID: 56335085
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbaa1af2690c3148d2ecfb173b13be288a21d80f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442660"
---
# <a name="requirements-for-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="6d8b8-103">Requisitos para o Location-Based roteamento de conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6d8b8-103">Requirements for Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6d8b8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6d8b8-104">

<span> </span></span></span>

<span data-ttu-id="6d8b8-105">_**Tópico da última modificação:** 2013-07-19_</span><span class="sxs-lookup"><span data-stu-id="6d8b8-105">_**Topic Last Modified:** 2013-07-19_</span></span>

<span data-ttu-id="6d8b8-106">Veja a seguir os requisitos necessários para a instalação e a configuração do aplicativo de Location-Based de conferência de roteamento:</span><span class="sxs-lookup"><span data-stu-id="6d8b8-106">The following are the requirements needed for the installation and configuration of the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="6d8b8-107">A atualização cumulativa 2 do Lync Server 2013 deve ser implantada em todos os servidores ou pools na sua topologia.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-107">Lync Server 2013 Cumulative Update 2 must be deployed on all servers or pools in your topology.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6d8b8-108">Se um servidor ou pool do Lync na sua topologia não tiver a atualização cumulativa 2 do Lync Server 2013 ou posterior instalada, a aplicação de Location-Based roteamento de reuniões do Lync não poderá ser garantida.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-108">If a Lync server or pool in your topology does not have Lync Server 2013 Cumulative Update 2 or higher installed, then enforcement of Location-Based Routing of Lync meetings cannot be guaranteed.</span></span>



</div>

  - <span data-ttu-id="6d8b8-109">Lync Server 2013 Location-Based o roteamento é um pré-requisito para Location-Based aplicativo de conferência de roteamento.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-109">Lync Server 2013 Location-Based Routing is a pre-requisite for Location-Based Routing Conferencing application.</span></span> <span data-ttu-id="6d8b8-110">Para obter mais informações sobre como configurar o roteamento Location-Based do Lync Server 2013, consulte [Configurando Location-Based roteamento](lync-server-2013-configuring-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="6d8b8-110">For further information on configuring Lync Server 2013 Location-Based Routing, please refer to [Configuring Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).</span></span>

  - <span data-ttu-id="6d8b8-111">Os requisitos do aplicativo Location-Based de conferência de roteamento são iguais aos requisitos do Lync Server 2013 Location-Based o roteamento.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-111">Requirements of Location-Based Routing Conferencing application are the same as the requirements for Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="6d8b8-112">Para obter mais informações, consulte [planejando o roteamento Location-Based](lync-server-2013-planning-for-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="6d8b8-112">For more information, please refer to [Planning for Location-Based Routing](lync-server-2013-planning-for-location-based-routing.md).</span></span>

<div>

## <a name="supported-servers"></a><span data-ttu-id="6d8b8-113">Servidores com suporte</span><span class="sxs-lookup"><span data-stu-id="6d8b8-113">Supported Servers</span></span>

<span data-ttu-id="6d8b8-114">O aplicativo de conferência de roteamento Location-Based requer que a atualização cumulativa 2 do Lync Server 2013 seja implantada em todos os pools de Front-End e servidores Standard Edition na sua topologia.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-114">The Location-Based Routing Conferencing application requires that Lync Server 2013 Cumulative Update 2 is deployed on all Front-End pools and Standard Edition Servers in your topology.</span></span> <span data-ttu-id="6d8b8-115">Se a atualização cumulativa 2 do Lync Server 2013 não estiver instalada em alguns servidores do Lync na sua topologia, Location-Based restrições de roteamento não poderão ser totalmente impostas em reuniões do Lync e transferências de chamadas consultivas.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-115">If Lync Server 2013 Cumulative Update 2 is not installed on some Lync Servers in your topology, Location-Based Routing restrictions cannot be fully enforced on Lync meetings and consultative call transfers.</span></span>

<span data-ttu-id="6d8b8-116">A tabela a seguir identifica a combinação de funções de servidor e versões que dão suporte ao roteamento Location-Based.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-116">The following table identifies the combination of server roles and versions that support Location-Based Routing.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d8b8-117">Versão do Pool de Front-End</span><span class="sxs-lookup"><span data-stu-id="6d8b8-117">Front-End Pool version</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-118">Versão do Servidor de Mediação</span><span class="sxs-lookup"><span data-stu-id="6d8b8-118">Mediation Server version</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6d8b8-119">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d8b8-120">Atualização Cumulativa 2 do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6d8b8-120">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-121">Atualização Cumulativa 2 do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6d8b8-121">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-122">Sim</span><span class="sxs-lookup"><span data-stu-id="6d8b8-122">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d8b8-123">Atualização Cumulativa 2 do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6d8b8-123">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-124">Atualização Cumulativa 1 do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6d8b8-124">Lync Server 2013 Cumulative Update 1</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-125">Não</span><span class="sxs-lookup"><span data-stu-id="6d8b8-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d8b8-126">Atualização Cumulativa 2 do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6d8b8-126">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-127">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="6d8b8-127">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-128">Não</span><span class="sxs-lookup"><span data-stu-id="6d8b8-128">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d8b8-129">Atualização Cumulativa 2 do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6d8b8-129">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-130">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="6d8b8-130">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-131">Não</span><span class="sxs-lookup"><span data-stu-id="6d8b8-131">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d8b8-132">Atualização Cumulativa 1 do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6d8b8-132">Lync Server 2013 Cumulative Update 1</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-133">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="6d8b8-133">Any</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-134">Não</span><span class="sxs-lookup"><span data-stu-id="6d8b8-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d8b8-135">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="6d8b8-135">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-136">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="6d8b8-136">Any</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-137">Não</span><span class="sxs-lookup"><span data-stu-id="6d8b8-137">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d8b8-138">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="6d8b8-138">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-139">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="6d8b8-139">Any</span></span></p></td>
<td><p><span data-ttu-id="6d8b8-140">Não</span><span class="sxs-lookup"><span data-stu-id="6d8b8-140">No</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supported-clients"></a><span data-ttu-id="6d8b8-141">Clientes com suporte</span><span class="sxs-lookup"><span data-stu-id="6d8b8-141">Supported Clients</span></span>

<span data-ttu-id="6d8b8-142">Os clientes do Lync que dão suporte Location-Based roteamento de reuniões do Lync são os mesmos clientes que dão suporte ao Lync Server 2013 Location-Based o roteamento.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-142">The Lync clients that support Location-Based Routing of Lync meetings are the same clients that support Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="6d8b8-143">Para obter mais informações, consulte [suporte do cliente e do servidor para Location-Based roteamento](lync-server-2013-client-and-server-support-for-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="6d8b8-143">For more information, please refer to [Client and Server Support for Location-Based Routing](lync-server-2013-client-and-server-support-for-location-based-routing.md).</span></span>

</div>

<div>

## <a name="mediation-server-requirements-for-consultative-call-transfers"></a><span data-ttu-id="6d8b8-144">Requisitos do servidor de mediação para transferências de chamadas consultivas</span><span class="sxs-lookup"><span data-stu-id="6d8b8-144">Mediation Server Requirements for Consultative Call Transfers</span></span>

<span data-ttu-id="6d8b8-145">O aplicativo de conferência de roteamento de Location-Based requer a implantação de servidores de mediação autônomos para impor Location-Based restrições de roteamento em transferências de chamadas consultivas.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-145">The Location-Based Routing Conferencing application requires deploying stand-alone Mediation Servers in order to enforce Location-Based Routing restrictions on consultative call transfers.</span></span>

<span data-ttu-id="6d8b8-146">Para impor Location-Based roteamento de transferências de chamadas consultivas, o servidor de mediação deve estar associado a apenas um par de servidor de mediação (isto é, PBX, gateway SIP etc.) nas regiões de rede onde o roteamento do Location-Based é necessário.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-146">To enforce Location-Based Routing of consultative call transfers, the Mediation Server must be associated with only one Mediation Server peer (i.e. PBX, SIP gateway, etc) in network regions where Location-Based Routing is required.</span></span> <span data-ttu-id="6d8b8-147">Se os pares do servidor de mediação adicionais estiverem implantados na mesma região de rede, o par do servidor de mediação deve estar associado a um servidor de mediação diferente.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-147">If additional Mediation Server peers are deployed in the same network region, the Mediation Server peer must be associated with a different Mediation Server .</span></span> <span data-ttu-id="6d8b8-148">Este requisito é detalhado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6d8b8-148">This Requirement is detailed as follows:</span></span>

  - <span data-ttu-id="6d8b8-149">Servidor de mediação único por vários pares de servidores de mediação quando uma transferência de chamadas consuldas é roteada para um servidor de mediação ponto a ponto por meio de um servidor de mediação que está configurado com vários troncos SIP para vários pares (ou seja, PBXs e gateways), a transferência de chamadas consultivas está bloqueada para evitar troncos SIP.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-149">Single Mediation Server per multiple Mediation Server peers When a consultative call transfer is routed to a Mediation Server peer through a Mediation Server that’s configured with multiple SIP trunks to multiple peers (i.e. PBXs and gateways), the consultative call transfer is blocked to prevent PSTN toll bypass if the consultative call transfer is permitted through some SIP trunks but disallowed through other SIP trunks.</span></span>
    
    <span data-ttu-id="6d8b8-150">Por exemplo, no caso de um único servidor de mediação servindo um peer do servidor de mediação PSTN e um peer do servidor de mediação do PBX, o seguinte comportamento será observado:</span><span class="sxs-lookup"><span data-stu-id="6d8b8-150">For example, in the case of a single Mediation Server servicing a PSTN Gateway Mediation Server Peer and a PBX Mediation Server Peer, the following behavior will be observed:</span></span>
    
      - <span data-ttu-id="6d8b8-151">Quando um usuário do Lync de um determinado site (ou seja, site 1) tenta transferir uma chamada com um ponto de extremidade PSTN para um usuário do Lync de um site diferente (ou seja, site 2) via transferência consultiva, a chamada será desautorizada para impedir que a chamada em PSTN seja ignorada.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-151">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PSTN endpoint to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed to prevent PSTN toll bypass.</span></span>
    
      - <span data-ttu-id="6d8b8-152">Quando um usuário do Lync de um determinado site (ou seja, site 1) tenta transferir uma chamada com um ponto de extremidade do PBX no mesmo site 1 (site 1) para um usuário do Lync de um site diferente (ou seja, site 2) via transferência consultiva, a chamada será desautorizada mesmo que não se incorra em uma possível chamada PSTN PSTN.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-152">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PBX endpoint in the same site (site 1) to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed even if it doesn’t incur in potential PSTN toll bypassing.</span></span>

  - <span data-ttu-id="6d8b8-153">Servidores de mediação separados por peer do servidor de mediação</span><span class="sxs-lookup"><span data-stu-id="6d8b8-153">Separate Mediation Servers per Mediation Server peer</span></span>
    
    <span data-ttu-id="6d8b8-154">Quando uma transferência consultiva for direcionada a um peer do servidor de mediação, a transferência consultiva será avaliada em relação ao serviço de servidor de mediação único do servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-154">When a consultative transfer is targeted at a Mediation Server Peer, the consultative transfer will be evaluated against the single Mediation Server Peer serviced by the Mediation Server.</span></span> <span data-ttu-id="6d8b8-155">A chamada será desautorizada ou permitida com base em seu potencial de incorrer em uma interligação de PSTN, independentemente de todas as outras mediações do servidor de mediação do site, pois elas são atendidas por servidores de mediação separados.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-155">The call will be disallowed or allowed based in its potential to incur in PSTN toll bypass regardless of all other Mediations Server Peers in the site as they’re serviced by separate Mediation Servers.</span></span>
    
    <span data-ttu-id="6d8b8-156">Por exemplo, no caso de um servidor de mediação separado servindo um peer do servidor de mediação de gateway PSTN e um peer do servidor de mediação do PBX, o seguinte comportamento será observado:</span><span class="sxs-lookup"><span data-stu-id="6d8b8-156">For example, in the case of a separate Mediation Servers servicing a PSTN Gateway Mediation Server Peer and a PBX Mediation Server Peer, the following behavior will be observed:</span></span>
    
      - <span data-ttu-id="6d8b8-157">Quando um usuário do Lync de um determinado site (ou seja, site 1) tenta transferir uma chamada com um ponto de extremidade PSTN para um usuário do Lync de um site diferente (ou seja, site 2) via transferência consultiva, a chamada será desautorizada para impedir que a chamada em PSTN seja ignorada.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-157">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PSTN endpoint to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed to prevent PSTN toll bypass.</span></span>
    
      - <span data-ttu-id="6d8b8-158">Quando um usuário do Lync de um determinado site (ou seja, site 1) tenta transferir uma chamada com um ponto de extremidade do PBX no mesmo site 1 (site 1) para um usuário do Lync de um site diferente (ou seja, site 2) via transferência consultiva, a chamada será permitida, pois ela não incorrerá em potencial para a chamada PSTN PSTN.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-158">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PBX endpoint in the same site (site 1) to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be allowed as it doesn’t incur in potential PSTN toll bypassing.</span></span>

</div>

<div>

## <a name="capabilities-not-supported-by-the-location-based-routing-conferencing-application"></a><span data-ttu-id="6d8b8-159">Recursos que não são compatíveis com o aplicativo de conferência de roteamento Location-Based</span><span class="sxs-lookup"><span data-stu-id="6d8b8-159">Capabilities Not Supported by the Location-Based Routing Conferencing Application</span></span>

<span data-ttu-id="6d8b8-160">Os recursos a seguir não são compatíveis com o aplicativo de conferência de roteamento de Location-Based:</span><span class="sxs-lookup"><span data-stu-id="6d8b8-160">The following capabilities are not supported by the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="6d8b8-161">Conferência discada.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-161">Dial-in conferencing.</span></span> <span data-ttu-id="6d8b8-162">Location-Based roteamento não pode ser imposto para conferência discada.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-162">Location-Based Routing cannot be enforced for Dial-in conferencing.</span></span> <span data-ttu-id="6d8b8-163">Qualquer solicitação de discagem para uma determinada conferência não será restringida pela Location-Based roteamento, mesmo que o organizador de conferências seja um usuário do Lync habilitado para Location-Based roteamento.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-163">Any dial-in request to a given conference will not be restricted by Location-Based Routing even if the conference organizer is a Lync user enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="6d8b8-164">É recomendável não configurar números de acesso à conferência em regiões em que Location-Based restrições de roteamento precisam ser impostas.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-164">It’s recommended not to provision conferencing access numbers in regions where Location-Based Routing restrictions need to be enforced.</span></span>

<span data-ttu-id="6d8b8-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6d8b8-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

