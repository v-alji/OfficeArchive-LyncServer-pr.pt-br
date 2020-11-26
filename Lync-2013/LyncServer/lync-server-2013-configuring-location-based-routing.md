---
title: 'Lync Server 2013: Configurando o Roteamento Baseado em Local'
description: 'Lync Server 2013: Configurando o roteamento de Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Location-Based Routing
ms:assetid: 63cdc474-e80f-43b1-a237-9d9ed673300a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994036(v=OCS.15)
ms:contentKeyID: 51803946
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 080c2a3a82a8714fc35ce882b0c6cb1630552f27
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433036"
---
# <a name="configuring-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="09077-103">Configurando o Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09077-103">Configuring Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09077-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09077-104">

<span> </span></span></span>

<span data-ttu-id="09077-105">_**Tópico da última modificação:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="09077-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="09077-106">Lync Server 2013 CU1, Location-Based o roteamento é um recurso do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="09077-106">Lync Server 2013 CU1, Location-Based Routing is a feature of Enterprise Voice.</span></span> <span data-ttu-id="09077-107">Location-Based o roteamento é um recurso de gerenciamento de chamadas que controla como as chamadas são roteadas pelo Lync Server 2013 CU1.</span><span class="sxs-lookup"><span data-stu-id="09077-107">Location-Based Routing is a call management feature that controls how calls are routed by Lync Server 2013 CU1.</span></span> <span data-ttu-id="09077-108">Ele impõe restrições sobre se as chamadas podem ser roteadas para destinos PBX ou PSTN com base na localização do chamador do Lync.</span><span class="sxs-lookup"><span data-stu-id="09077-108">It enforces restrictions on whether calls can be routed to PBX or PSTN destinations based on the Lync caller’s location.</span></span> <span data-ttu-id="09077-109">Location-Based roteamento aplica regras de autorização de chamada a chamadas PSTN com base no local de rede do chamador.</span><span class="sxs-lookup"><span data-stu-id="09077-109">Location-Based Routing applies call authorization rules to PSTN calls based on the caller’s network location.</span></span> <span data-ttu-id="09077-110">O local do chamador é determinado com base no site de rede associado à sub-rede da rede na qual o chamador está conectado.</span><span class="sxs-lookup"><span data-stu-id="09077-110">The caller’s location is determined based on the network site associated with the network subnet the caller is connected on.</span></span> <span data-ttu-id="09077-111">Configurar o roteamento Location-Based requer primeiro a implantação do Enterprise Voice e, em seguida, a configuração de regiões de rede, sites e sub-redes.</span><span class="sxs-lookup"><span data-stu-id="09077-111">Configuring Location-Based Routing requires first deploying Enterprise Voice, then configuring network regions, sites and subnets.</span></span> <span data-ttu-id="09077-112">Isso configura a base para habilitar o roteamento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="09077-112">This sets up the foundation for enabling Location-Based Routing.</span></span>

<span data-ttu-id="09077-113">Antes de implantar o roteamento Location-Based, você deve primeiro implantar o Enterprise Voice e configurar regiões de rede, sites e associar sub-redes de rede a seus sites de rede.</span><span class="sxs-lookup"><span data-stu-id="09077-113">Before deploying Location-Based Routing, you must first deploy Enterprise Voice, and configure network regions, sites, and associate network subnets to your network sites.</span></span> <span data-ttu-id="09077-114">Uma vez concluído, você pode configurar o roteamento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="09077-114">Once completed, you can configure Location-Based Routing.</span></span> <span data-ttu-id="09077-115">Para ver as etapas sobre como configurar regiões de rede, sites e sub-redes, consulte [implantando recursos avançados do Enterprise Voice no Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md)</span><span class="sxs-lookup"><span data-stu-id="09077-115">For steps on how to configure network regions, sites and subnets, see [Deploying advanced Enterprise Voice features in Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md)</span></span>

<span data-ttu-id="09077-116">Esta seção orienta você na configuração do roteamento Location-Based usando o exemplo a seguir como ilustração.</span><span class="sxs-lookup"><span data-stu-id="09077-116">This section guides you through the configuration of Location-Based Routing using the following example as illustration.</span></span>

<span data-ttu-id="09077-117">![Exemplo de roteamento baseado na localização do Enterprise Voice](images/JJ994036.b6ef5afc-36ac-406f-8ec2-a87532b20612(OCS.15).png "Exemplo de roteamento baseado na localização do Enterprise Voice")</span><span class="sxs-lookup"><span data-stu-id="09077-117">![Enterprise Voice location-based routing example](images/JJ994036.b6ef5afc-36ac-406f-8ec2-a87532b20612(OCS.15).png "Enterprise Voice location-based routing example")</span></span>

  
<span data-ttu-id="09077-118">A tabela a seguir representa os usuários definidos neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="09077-118">The following table represents the users defined in this example.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09077-119">Tipo de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="09077-119">Endpoint type</span></span></th>
<th><span data-ttu-id="09077-120">Local</span><span class="sxs-lookup"><span data-stu-id="09077-120">Location</span></span></th>
<th><span data-ttu-id="09077-121">Usuários</span><span class="sxs-lookup"><span data-stu-id="09077-121">Users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09077-122">Lync</span><span class="sxs-lookup"><span data-stu-id="09077-122">Lync</span></span></p></td>
<td><p><span data-ttu-id="09077-123">Escritório corporativo da Délhi</span><span class="sxs-lookup"><span data-stu-id="09077-123">Delhi corporate office</span></span></p></td>
<td><p><span data-ttu-id="09077-124">DEL-LYNC-1, DEL-LYNC-2, DEL-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="09077-124">DEL-LYNC-1,DEL-LYNC-2,DEL-LYNC-3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09077-125">Lync</span><span class="sxs-lookup"><span data-stu-id="09077-125">Lync</span></span></p></td>
<td><p><span data-ttu-id="09077-126">Escritório corporativo Hyderabad</span><span class="sxs-lookup"><span data-stu-id="09077-126">Hyderabad corporate office</span></span></p></td>
<td><p><span data-ttu-id="09077-127">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="09077-127">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09077-128">Lync</span><span class="sxs-lookup"><span data-stu-id="09077-128">Lync</span></span></p></td>
<td><p><span data-ttu-id="09077-129">Desconhecido (isto é, Hotel)</span><span class="sxs-lookup"><span data-stu-id="09077-129">Unknown (i.e. hotel)</span></span></p></td>
<td><p><span data-ttu-id="09077-130">UNK-LYNC-1</span><span class="sxs-lookup"><span data-stu-id="09077-130">UNK-LYNC-1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09077-131">RESPECTIVA</span><span class="sxs-lookup"><span data-stu-id="09077-131">PBX</span></span></p></td>
<td><p><span data-ttu-id="09077-132">Escritório corporativo da Délhi</span><span class="sxs-lookup"><span data-stu-id="09077-132">Delhi corporate office</span></span></p></td>
<td><p><span data-ttu-id="09077-133">DEL-PBX-1, DEL-PBX-2</span><span class="sxs-lookup"><span data-stu-id="09077-133">DEL-PBX-1, DEL-PBX-2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09077-134">RESPECTIVA</span><span class="sxs-lookup"><span data-stu-id="09077-134">PBX</span></span></p></td>
<td><p><span data-ttu-id="09077-135">Escritório corporativo Hyderabad</span><span class="sxs-lookup"><span data-stu-id="09077-135">Hyderabad corporate office</span></span></p></td>
<td><p><span data-ttu-id="09077-136">HYD-PBX-1, HYD-PBX-2</span><span class="sxs-lookup"><span data-stu-id="09077-136">HYD-PBX-1, HYD-PBX-2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09077-137">PSTN</span><span class="sxs-lookup"><span data-stu-id="09077-137">PSTN</span></span></p></td>
<td><p><span data-ttu-id="09077-138">Sabe</span><span class="sxs-lookup"><span data-stu-id="09077-138">Unknown</span></span></p></td>
<td><p><span data-ttu-id="09077-139">PSTN-1, PSTN-2, PSTN-3</span><span class="sxs-lookup"><span data-stu-id="09077-139">PSTN-1, PSTN-2, PSTN-3</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="09077-140">A tabela a seguir representa os sistemas ilustrados neste ambiente de exemplo.</span><span class="sxs-lookup"><span data-stu-id="09077-140">The following table represents the systems illustrated in this example environment.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09077-141">Sistema</span><span class="sxs-lookup"><span data-stu-id="09077-141">System</span></span></th>
<th><span data-ttu-id="09077-142">Local</span><span class="sxs-lookup"><span data-stu-id="09077-142">Location</span></span></th>
<th><span data-ttu-id="09077-143">Nome</span><span class="sxs-lookup"><span data-stu-id="09077-143">Name</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09077-144">Pool CU1 do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09077-144">Lync Server 2013 CU1 pool</span></span></p></td>
<td><p><span data-ttu-id="09077-145">qualquer um</span><span class="sxs-lookup"><span data-stu-id="09077-145">any</span></span></p></td>
<td><p><span data-ttu-id="09077-146">LS-PL1</span><span class="sxs-lookup"><span data-stu-id="09077-146">LS-PL1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09077-147">Lync Server 2013 CU1, servidor de mediação</span><span class="sxs-lookup"><span data-stu-id="09077-147">Lync Server 2013 CU1, Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="09077-148">qualquer um</span><span class="sxs-lookup"><span data-stu-id="09077-148">any</span></span></p></td>
<td><p><span data-ttu-id="09077-149">MS-PL1</span><span class="sxs-lookup"><span data-stu-id="09077-149">MS-PL1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09077-150">Gateway PSTN 1</span><span class="sxs-lookup"><span data-stu-id="09077-150">PSTN gateway 1</span></span></p></td>
<td><p><span data-ttu-id="09077-151">Delhi</span><span class="sxs-lookup"><span data-stu-id="09077-151">Delhi</span></span></p></td>
<td><p><span data-ttu-id="09077-152">DEL-GW</span><span class="sxs-lookup"><span data-stu-id="09077-152">DEL-GW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09077-153">Gateway PSTN 2</span><span class="sxs-lookup"><span data-stu-id="09077-153">PSTN gateway 2</span></span></p></td>
<td><p><span data-ttu-id="09077-154">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="09077-154">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="09077-155">HYD-GW</span><span class="sxs-lookup"><span data-stu-id="09077-155">HYD-GW</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09077-156">PBX 1</span><span class="sxs-lookup"><span data-stu-id="09077-156">PBX 1</span></span></p></td>
<td><p><span data-ttu-id="09077-157">Delhi</span><span class="sxs-lookup"><span data-stu-id="09077-157">Delhi</span></span></p></td>
<td><p><span data-ttu-id="09077-158">DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="09077-158">DEL-PBX</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09077-159">PBX 2</span><span class="sxs-lookup"><span data-stu-id="09077-159">PBX 2</span></span></p></td>
<td><p><span data-ttu-id="09077-160">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="09077-160">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="09077-161">RED-PBX</span><span class="sxs-lookup"><span data-stu-id="09077-161">RED-PBX</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="09077-162">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="09077-162">In This Section</span></span>

  - [<span data-ttu-id="09077-163">Configurando o Enterprise Voice no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09077-163">Configuring Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-configuring-enterprise-voice.md)

  - [<span data-ttu-id="09077-164">Implantando regiões de rede, sites e sub-redes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09077-164">Deploying network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-deploying-network-regions-sites-and-subnets.md)

  - [<span data-ttu-id="09077-165">Habilitando o roteamento de Location-Based no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09077-165">Enabling Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-enabling-location-based-routing.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="09077-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="09077-166">See Also</span></span>


[<span data-ttu-id="09077-167">Implantação de recursos avançados do Enterprise Voice no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09077-167">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)  
  

<span data-ttu-id="09077-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09077-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

