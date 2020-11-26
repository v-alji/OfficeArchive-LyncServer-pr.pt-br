---
title: 'Lync Server 2013: Transferência e encaminhamento de chamadas'
description: 'Lync Server 2013: transferências de chamadas e encaminhamento de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call transfers and call forwarding
ms:assetid: 978610ec-63c7-4cf6-ad7a-9ef91559bf12
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994051(v=OCS.15)
ms:contentKeyID: 51803962
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9359cb64b386d022eab33e4523dfaccf784075b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435681"
---
# <a name="call-transfers-and-call-forwarding-in-lync-server-2013"></a><span data-ttu-id="9f0dd-103">Transferência e encaminhamento de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f0dd-103">Call transfers and call forwarding in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9f0dd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9f0dd-104">

<span> </span></span></span>

<span data-ttu-id="9f0dd-105">_**Tópico da última modificação:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="9f0dd-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="9f0dd-106">Quando um ponto de extremidade PSTN é envolvido, Location-Based roteamento analisa o local do ponto de extremidade do Calle e o ponto de extremidade para o qual a chamada será transferida ou encaminhada (isto é, transferência/destino para encaminhamento).</span><span class="sxs-lookup"><span data-stu-id="9f0dd-106">When a PSTN endpoint is involved, Location-Based Routing analyzes the location of the calle’s endpoint and the endpoint where the call will be transferred or forwarded to (i.e. transfer/forward target).</span></span> <span data-ttu-id="9f0dd-107">Location-Based o roteamento determina se a chamada deve ser transferida ou encaminhada dependendo do local de ambos os pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="9f0dd-107">Location-Based Routing determines whether the call should be transferred or forwarded depending on the location of both endpoints.</span></span>

<span data-ttu-id="9f0dd-108">A tabela a seguir ilustra o cenário de um usuário do Lync em uma chamada com um ponto de extremidade PSTN, e o usuário do Lync transfere a chamada para outro usuário do Lync.</span><span class="sxs-lookup"><span data-stu-id="9f0dd-108">The following table illustrates the scenario of a Lync user in a call with a PSTN endpoint, and the Lync user transfers the call to another Lync user.</span></span> <span data-ttu-id="9f0dd-109">Dependendo da localização do site de rede do ponto de extremidade do transportador, Location-Based o roteamento afeta o roteamento da transferência de chamadas ou encaminhar.</span><span class="sxs-lookup"><span data-stu-id="9f0dd-109">Depending on the network site location of the transferee’s endpoint, Location-Based Routing affects the routing of the call transfer or forward.</span></span>

### <a name="initiating-call-transfer-or-forward"></a><span data-ttu-id="9f0dd-110">Iniciando a transferência ou o encaminhamento de chamada</span><span class="sxs-lookup"><span data-stu-id="9f0dd-110">Initiating call transfer or forward</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f0dd-111">Usuário que inicia a transferência/encaminhamento da chamada</span><span class="sxs-lookup"><span data-stu-id="9f0dd-111">User initiating the call transfer/forward</span></span></th>
<th><span data-ttu-id="9f0dd-112">O ponto de extremidade de destino está no mesmo local de rede do usuário que inicia a transferência ou o encaminhamento da chamada</span><span class="sxs-lookup"><span data-stu-id="9f0dd-112">Target endpoint is in same network site as user initiating call transfer or forward</span></span></th>
<th><span data-ttu-id="9f0dd-113">O ponto de extremidade de destino está em um local de rede diferente do que o do usuário que inicia a transferência ou o encaminhamento da chamada</span><span class="sxs-lookup"><span data-stu-id="9f0dd-113">Target endpoint is in different network site as user initiating call transfer or forward</span></span></th>
<th><span data-ttu-id="9f0dd-114">O ponto de extremidade de destino está em um site de rede desconhecido ou site de rede não habilitado para roteamento de Location-Based</span><span class="sxs-lookup"><span data-stu-id="9f0dd-114">Target endpoint is in unknown network site or network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f0dd-115">Usuário do Lync</span><span class="sxs-lookup"><span data-stu-id="9f0dd-115">Lync user</span></span></p></td>
<td><p><span data-ttu-id="9f0dd-116">Encaminhamento ou transferência de chamada permitido</span><span class="sxs-lookup"><span data-stu-id="9f0dd-116">Call forward or transfer is allowed</span></span></p></td>
<td><p><span data-ttu-id="9f0dd-117">Encaminhamento ou transferência de chamada não permitido</span><span class="sxs-lookup"><span data-stu-id="9f0dd-117">Call forward or transfer is not allowed</span></span></p></td>
<td><p><span data-ttu-id="9f0dd-118">Encaminhamento ou transferência de chamada não permitido</span><span class="sxs-lookup"><span data-stu-id="9f0dd-118">Call forward or transfer is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="9f0dd-119">Por exemplo: um usuário do Lync em uma chamada com um ponto de extremidade PSTN transfere a chamada para outro usuário do Lync que esteja no mesmo site de rede.</span><span class="sxs-lookup"><span data-stu-id="9f0dd-119">For example: a Lync user in a call with a PSTN endpoint transfers the call to another Lync user that is in the same network site.</span></span> <span data-ttu-id="9f0dd-120">Nesse caso, a transferência de chamada é permitida.</span><span class="sxs-lookup"><span data-stu-id="9f0dd-120">In this case, the call transfer is allowed.</span></span>

<span data-ttu-id="9f0dd-121">A tabela a seguir ilustra o cenário de um usuário do Lync em uma chamada com outro usuário do Lync, e um dos usuários transfere a chamada para um ponto de extremidade PSTN.</span><span class="sxs-lookup"><span data-stu-id="9f0dd-121">The following table illustrates the scenario of a Lync user in a call with another Lync user, and one of the users transfers the call to a PSTN endpoint.</span></span> <span data-ttu-id="9f0dd-122">Dependendo do local do usuário para o qual a chamada está sendo transferida, a tabela detalhará como o Roteamento Baseado na Localização afeta a chamada.</span><span class="sxs-lookup"><span data-stu-id="9f0dd-122">Depending on the location of the user the call is being transferred to, the table details how Location-Based Routing affects the call.</span></span>

### <a name="call-transfer-or-forward-to-pstn-endpoint"></a><span data-ttu-id="9f0dd-123">Transferência ou encaminhamento de chamada para um ponto de extremidade PSTN</span><span class="sxs-lookup"><span data-stu-id="9f0dd-123">Call transfer or forward to PSTN endpoint</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f0dd-124">Destino do ponto de extremidade da transferência/encaminhamento de chamada</span><span class="sxs-lookup"><span data-stu-id="9f0dd-124">Call transfer/forward endpoint target</span></span></th>
<th><span data-ttu-id="9f0dd-125">Usuários do Lync no mesmo local de rede</span><span class="sxs-lookup"><span data-stu-id="9f0dd-125">Lync users in same network site</span></span></th>
<th><span data-ttu-id="9f0dd-126">Usuários do Lync em diferentes sites de rede</span><span class="sxs-lookup"><span data-stu-id="9f0dd-126">Lync users in different network sites</span></span></th>
<th><span data-ttu-id="9f0dd-127">Um ou ambos os usuários do Lync em um site de rede desconhecido ou site de rede não estão habilitados para roteamento Location-Based</span><span class="sxs-lookup"><span data-stu-id="9f0dd-127">One or both Lync users in unknown network site or network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f0dd-128">Ponto de extremidade PSTN</span><span class="sxs-lookup"><span data-stu-id="9f0dd-128">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="9f0dd-129">O encaminhamento ou a transferência de chamada é permitida pela política de roteamento de voz do local do usuário transferido</span><span class="sxs-lookup"><span data-stu-id="9f0dd-129">Call forward or transfer allowed by the transferred user’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="9f0dd-130">O encaminhamento ou a transferência de chamada é permitida pela política de roteamento de voz do local do usuário transferido</span><span class="sxs-lookup"><span data-stu-id="9f0dd-130">Call forward or transfer allowed by the transferred user’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="9f0dd-131">O encaminhamento ou a transferência da chamada é permitida pela política de voz do destinatário da transferência somente pelos troncos não habilitados para o Roteamento com Base no Local</span><span class="sxs-lookup"><span data-stu-id="9f0dd-131">Call forward or transfer allowed by the transferred user’s voice policy only through trunks not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="9f0dd-132">Por exemplo: um usuário do Lync em uma chamada com outro usuário do Lync que esteja no mesmo local de rede transfere a chamada para um ponto de extremidade PSTN e a transferência de chamada é permitida.</span><span class="sxs-lookup"><span data-stu-id="9f0dd-132">For example: a Lync user in a call with another Lync user that is in the same network site transfers the call to a PSTN endpoint and the call transfer is allowed.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="9f0dd-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f0dd-133">See Also</span></span>


[<span data-ttu-id="9f0dd-134">Cenários para Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f0dd-134">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="9f0dd-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9f0dd-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

