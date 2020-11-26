---
title: 'Lync Server 2013: Location-Based transferências de chamadas para roteamento e consultoria'
description: 'Lync Server 2013: Location-Based transferências de chamadas de roteamento e consultoria.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing and consultative call transfers
ms:assetid: b12460c2-36c8-481f-b867-fe10dc1c0bdf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362836(v=OCS.15)
ms:contentKeyID: 56335089
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d07cf6a33ff4d6ad57f8913a798fac3bc393a00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426548"
---
# <a name="location-based-routing-and-consultative-call-transfers-in-lync-server-2013"></a><span data-ttu-id="2448c-103">Location-Based transferências de chamadas de roteamento e consultoria no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2448c-103">Location-Based Routing and consultative call transfers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2448c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2448c-104">

<span> </span></span></span>

<span data-ttu-id="2448c-105">_**Tópico da última modificação:** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="2448c-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="2448c-106">Além de impor o roteamento do Location-Based a reuniões do Lync, o aplicativo de conferência de roteamento de Location-Based impõe Location-Based restrições de roteamento em transferências de chamadas consultivas que entram em pontos de extremidade PSTN.</span><span class="sxs-lookup"><span data-stu-id="2448c-106">In addition to enforcing Location-Based Routing to Lync meetings, the Location-Based Routing Conferencing application enforces Location-Based Routing restrictions on consultative call transfers that egress to PSTN endpoints.</span></span> <span data-ttu-id="2448c-107">Uma transferência de chamada consultiva é estabelecida entre duas partes em que uma delas transfere a chamada para um novo usuário.</span><span class="sxs-lookup"><span data-stu-id="2448c-107">A consultative call transfer is a call established between two parties where one of the parties transfers the call to a new user.</span></span> <span data-ttu-id="2448c-108">Por exemplo, um ponto de extremidade PSTN chama o usuário A (chamado do Lync).</span><span class="sxs-lookup"><span data-stu-id="2448c-108">For example, a PSTN endpoint calls user A (Lync callee).</span></span> <span data-ttu-id="2448c-109">O usuário A determina que o usuário PSTN deve ser encaminhado para o usuário B (usuário do Lync).</span><span class="sxs-lookup"><span data-stu-id="2448c-109">User A determines the PSTN user should be forwarded to user B (Lync user).</span></span> <span data-ttu-id="2448c-110">O usuário A coloca a chamada com o usuário PSTN em espera e liga para o usuário B. O usuário B concorda em falar com o usuário PSTN.</span><span class="sxs-lookup"><span data-stu-id="2448c-110">User A places the call with the PSTN user on hold, and calls user B. User B agrees to talk to the PSTN user.</span></span> <span data-ttu-id="2448c-111">O usuário A transfere a chamada espera para o usuário B.</span><span class="sxs-lookup"><span data-stu-id="2448c-111">User A transfers the call on-hold to user B.</span></span>

<span data-ttu-id="2448c-112">**Fluxo da Transferência de Chamada Consultiva**</span><span class="sxs-lookup"><span data-stu-id="2448c-112">**Consultative call transfer call flow**</span></span>

<span data-ttu-id="2448c-113">![Roteamento baseado em local para o diagrama de conferência](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "Roteamento baseado em local para o diagrama de conferência")</span><span class="sxs-lookup"><span data-stu-id="2448c-113">![Location-based routing for conferencing diagram](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "Location-based routing for conferencing diagram")</span></span>

<span data-ttu-id="2448c-114">Quando um usuário habilitado para Location-Based roteamento inicia uma transferência de chamadas consuldas de um ponto de extremidade PSTN (conforme mostrado na figura anterior), isso cria duas chamadas ativas, uma chamada entre o usuário PSTN e o usuário do Lync a e a outra entre o usuário do Lync A e o usuário do Lync B. o comportamento a seguir é imposto pelo aplicativo Location-Based de audioconferência:</span><span class="sxs-lookup"><span data-stu-id="2448c-114">When a user enabled for Location-Based Routing initiates a consultative call transfer of a PSTN endpoint (as shown in the preceding figure), this creates two active calls, one call between the PSTN user and Lync user A, and the other between Lync user A and Lync user B. the following behavior is enforced by the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="2448c-115">Se o encaminhamento de tronco SIP a chamada PSTN estiver autorizada a redirecionar a chamada PSTN para o site de rede onde o usuário do Lync B (ou seja, destino da transferência) estiver localizado, a transferência de chamada será permitida; caso contrário, a transferência de chamadas consultivas será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="2448c-115">If the SIP trunk routing the PSTN call is authorized to re-route the PSTN call to the network site where Lync user B (i.e. transfer target) is located,, then the call transfer will be allowed; otherwise, the consultative call transfer will be blocked.</span></span> <span data-ttu-id="2448c-116">Essa autorização é realizada caso o local da parte transferida seja no mesmo local de rede do tronco SIP que está encaminhando a chamada ativa para o ponto de extremidade PSTN.</span><span class="sxs-lookup"><span data-stu-id="2448c-116">This authorization is performed based on the transferred party’s location being in the same network site as the SIP trunk that is routing the active call to the PSTN endpoint.</span></span>

  - <span data-ttu-id="2448c-117">Se o tronco SIP que faz a chamada PSTN não estiver autorizado a direcionar chamadas para o site de rede onde a parte transferida (usuário B do Lync) estiver localizada ou a parte transferidas estiver localizada em um site de rede desconhecido, a transferência de chamadas consuldas para o ponto de extremidade PSTN (ou seja, destino da transferência de chamada) será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="2448c-117">If the SIP trunk routing the inbound PSTN call is not authorized to route calls to the network site where the transferred party (Lync user B) is located or the transferred party is located in an unknown network site, then the consultative call transfer to the PSTN endpoint (i.e. call transfer target) will be blocked.</span></span>

<span data-ttu-id="2448c-118">A tabela a seguir descreve como as restrições de roteamento Location-Based são aplicadas pelo aplicativo Location-Based de audioconferência para transferências de chamadas consultivas.</span><span class="sxs-lookup"><span data-stu-id="2448c-118">The following table describes how Location-Based Routing restrictions are applied by the Location-Based Routing Conferencing application for consultative call transfers.</span></span> <span data-ttu-id="2448c-119">Embora os pontos de extremidade PBX não estejam associados diretamente a um local de rede, o tronco SIP ao qual o PBX está conectado pode ser atribuído a um local de rede.</span><span class="sxs-lookup"><span data-stu-id="2448c-119">Although PBX endpoints are not directly associated with a network site, the SIP trunk the PBX is connected to can be assigned a network site.</span></span> <span data-ttu-id="2448c-120">Portanto, o ponto de extremidade PBX pode ser indiretamente associado a um local de rede.</span><span class="sxs-lookup"><span data-stu-id="2448c-120">Therefore, the PBX endpoint can be indirectly associated with a network site.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2448c-121">Local de rede da parte transferida da chamada</span><span class="sxs-lookup"><span data-stu-id="2448c-121">Network site of call transferred party</span></span></p></td>
<td><p><span data-ttu-id="2448c-122">Local de rede de destino da transferência de chamada</span><span class="sxs-lookup"><span data-stu-id="2448c-122">Network site of call transfer target</span></span></p></td>
<td><p><span data-ttu-id="2448c-123">Comportamento</span><span class="sxs-lookup"><span data-stu-id="2448c-123">Behavior</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2448c-124">Ponto de extremidade PSTN</span><span class="sxs-lookup"><span data-stu-id="2448c-124">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="2448c-125">Usuário do Lync no mesmo local de rede (por exemplo, site 1)</span><span class="sxs-lookup"><span data-stu-id="2448c-125">Lync user in the same network site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="2448c-126">A transferência consultiva será permitida</span><span class="sxs-lookup"><span data-stu-id="2448c-126">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2448c-127">Ponto de extremidade PSTN</span><span class="sxs-lookup"><span data-stu-id="2448c-127">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="2448c-128">Usuário do Lync em sites de rede diferentes (por exemplo, site 2)</span><span class="sxs-lookup"><span data-stu-id="2448c-128">Lync user in different network sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="2448c-129">A transferência consultiva não será permitida</span><span class="sxs-lookup"><span data-stu-id="2448c-129">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2448c-130">Ponto de extremidade PSTN</span><span class="sxs-lookup"><span data-stu-id="2448c-130">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="2448c-131">Usuário do Lync em um site de rede desconhecido</span><span class="sxs-lookup"><span data-stu-id="2448c-131">Lync user in an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="2448c-132">A transferência consultiva não será permitida</span><span class="sxs-lookup"><span data-stu-id="2448c-132">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2448c-133">Ponto de extremidade PSTN</span><span class="sxs-lookup"><span data-stu-id="2448c-133">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="2448c-134">Usuário do Lync federado</span><span class="sxs-lookup"><span data-stu-id="2448c-134">Federated Lync user</span></span></p></td>
<td><p><span data-ttu-id="2448c-135">A transferência consultiva não será permitida</span><span class="sxs-lookup"><span data-stu-id="2448c-135">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2448c-136">Ponto de extremidade PSTN</span><span class="sxs-lookup"><span data-stu-id="2448c-136">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="2448c-137">Ponto de extremidade do PBX no mesmo local (isto é, local 1)</span><span class="sxs-lookup"><span data-stu-id="2448c-137">PBX endpoint in the same site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="2448c-138">A transferência consultiva será permitida</span><span class="sxs-lookup"><span data-stu-id="2448c-138">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2448c-139">Ponto de extremidade PSTN</span><span class="sxs-lookup"><span data-stu-id="2448c-139">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="2448c-140">Ponto de extremidade PBX em locais diferentes (isto é, local 2)</span><span class="sxs-lookup"><span data-stu-id="2448c-140">PBX endpoint in a different sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="2448c-141">A transferência consultiva não será permitida</span><span class="sxs-lookup"><span data-stu-id="2448c-141">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2448c-142">Ponto de extremidade do PBX no mesmo local (isto é, local 1)</span><span class="sxs-lookup"><span data-stu-id="2448c-142">PBX endpoint in the same site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="2448c-143">Ponto de extremidade PSTN</span><span class="sxs-lookup"><span data-stu-id="2448c-143">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="2448c-144">A transferência consultiva será permitida</span><span class="sxs-lookup"><span data-stu-id="2448c-144">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2448c-145">Ponto de extremidade do PBX em locais diferentes (i.e. local 2)</span><span class="sxs-lookup"><span data-stu-id="2448c-145">PBX endpoint in a different site (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="2448c-146">Ponto de extremidade PSTN</span><span class="sxs-lookup"><span data-stu-id="2448c-146">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="2448c-147">A transferência consultiva não será permitida</span><span class="sxs-lookup"><span data-stu-id="2448c-147">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2448c-148">Ponto de extremidade PBX em qualquer local</span><span class="sxs-lookup"><span data-stu-id="2448c-148">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="2448c-149">Usuário do Lync no mesmo local de rede (por exemplo, site 1)</span><span class="sxs-lookup"><span data-stu-id="2448c-149">Lync user in the same network site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="2448c-150">A transferência consultiva será permitida</span><span class="sxs-lookup"><span data-stu-id="2448c-150">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2448c-151">Ponto de extremidade PBX em qualquer local</span><span class="sxs-lookup"><span data-stu-id="2448c-151">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="2448c-152">Usuário do Lync em sites de rede diferentes (por exemplo, site 2)</span><span class="sxs-lookup"><span data-stu-id="2448c-152">Lync user in different network sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="2448c-153">A transferência consultiva será permitida</span><span class="sxs-lookup"><span data-stu-id="2448c-153">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2448c-154">Ponto de extremidade PBX em qualquer local</span><span class="sxs-lookup"><span data-stu-id="2448c-154">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="2448c-155">Usuário do Lync em um site de rede desconhecido</span><span class="sxs-lookup"><span data-stu-id="2448c-155">Lync user in an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="2448c-156">A transferência consultiva será permitida</span><span class="sxs-lookup"><span data-stu-id="2448c-156">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2448c-157">Ponto de extremidade PBX em qualquer local</span><span class="sxs-lookup"><span data-stu-id="2448c-157">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="2448c-158">Usuário do Lync federado</span><span class="sxs-lookup"><span data-stu-id="2448c-158">Federated Lync user</span></span></p></td>
<td><p><span data-ttu-id="2448c-159">A transferência consultiva será permitida</span><span class="sxs-lookup"><span data-stu-id="2448c-159">Consultative transfer will be allowed</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2448c-160">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2448c-160">


</div>

<span> </span>

</div>

</div>

</span></span></div>

