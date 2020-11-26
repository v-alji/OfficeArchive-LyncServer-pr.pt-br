---
title: 'Lync Server 2013: Suporte a cliente e servidor para Roteamento Baseado em Local'
description: 'Lync Server 2013: suporte a cliente e servidor para roteamento Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Client and server support for Location-Based Routing
ms:assetid: 26c2ca3d-026d-4dd7-94fa-15ebb4406953
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994024(v=OCS.15)
ms:contentKeyID: 51803933
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20dca7444f58ee62dbc36edbb7d9e1c976a97807
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434897"
---
# <a name="client-and-server-support-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="df243-103">Suporte a cliente e servidor para Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df243-103">Client and server support for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="df243-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="df243-104">

<span> </span></span></span>

<span data-ttu-id="df243-105">_**Tópico da última modificação:** 2013-06-18_</span><span class="sxs-lookup"><span data-stu-id="df243-105">_**Topic Last Modified:** 2013-06-18_</span></span>

<span data-ttu-id="df243-106">Location-Based roteamento é imposto pelo Lync Server.</span><span class="sxs-lookup"><span data-stu-id="df243-106">Location-Based Routing is enforced by Lync Server.</span></span> <span data-ttu-id="df243-107">O Lync Server pode identificar os sites de rede nos quais os usuários estão se conectando dentro da rede corporativa.</span><span class="sxs-lookup"><span data-stu-id="df243-107">Lync Server can identify the network sites where users are connecting from within the corporate network.</span></span> <span data-ttu-id="df243-108">Como os usuários remotos estão fora da rede corporativa, seu local é considerado desconhecido.</span><span class="sxs-lookup"><span data-stu-id="df243-108">Since remote users are outside the corporate network, their location is considered to be unknown.</span></span>

<div>

## <a name="lync-server-support"></a><span data-ttu-id="df243-109">Suporte ao Lync Server</span><span class="sxs-lookup"><span data-stu-id="df243-109">Lync Server Support</span></span>

<span data-ttu-id="df243-110">Location-Based o roteamento requer que o Lync Server 2013 CU1 seja implantado em todos os pools de front-end e servidores Standard Edition em uma determinada topologia.</span><span class="sxs-lookup"><span data-stu-id="df243-110">Location-Based Routing requires that Lync Server 2013 CU1 is deployed on all Front End pools and Standard Edition servers in a given topology.</span></span> <span data-ttu-id="df243-111">Se o Lync Server 2013 CU1 não estiver instalado em certos componentes do Lync na topologia, Location-Based restrições de roteamento não poderão ser totalmente impostas.</span><span class="sxs-lookup"><span data-stu-id="df243-111">If Lync Server 2013 CU1 is not installed on certain Lync components in the topology, Location-Based Routing restrictions cannot be fully enforced.</span></span>

<span data-ttu-id="df243-112">A tabela a seguir identifica a combinação de funções de servidor e versões com suporte para roteamento Location-Based.</span><span class="sxs-lookup"><span data-stu-id="df243-112">The following table identifies the combination of server roles and versions that is supported for Location-Based Routing.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="df243-113">Versão do pool</span><span class="sxs-lookup"><span data-stu-id="df243-113">Pool version</span></span></th>
<th><span data-ttu-id="df243-114">Versão do Servidor de Mediação</span><span class="sxs-lookup"><span data-stu-id="df243-114">Mediation Server version</span></span></th>
<th><span data-ttu-id="df243-115">Com suporte</span><span class="sxs-lookup"><span data-stu-id="df243-115">Supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df243-116">Atualização cumulativa de fevereiro de 2013 do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df243-116">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="df243-117">Atualização cumulativa de fevereiro de 2013 do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df243-117">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="df243-118">sim</span><span class="sxs-lookup"><span data-stu-id="df243-118">yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df243-119">Atualização cumulativa de fevereiro de 2013 do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df243-119">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="df243-120">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df243-120">Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="df243-121">não</span><span class="sxs-lookup"><span data-stu-id="df243-121">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df243-122">Atualização cumulativa de fevereiro de 2013 do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df243-122">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="df243-123">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="df243-123">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="df243-124">não</span><span class="sxs-lookup"><span data-stu-id="df243-124">no</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df243-125">Atualização cumulativa de fevereiro de 2013 do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df243-125">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="df243-126">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="df243-126">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="df243-127">não</span><span class="sxs-lookup"><span data-stu-id="df243-127">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df243-128">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df243-128">Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="df243-129">qualquer um</span><span class="sxs-lookup"><span data-stu-id="df243-129">any</span></span></p></td>
<td><p><span data-ttu-id="df243-130">não</span><span class="sxs-lookup"><span data-stu-id="df243-130">no</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df243-131">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="df243-131">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="df243-132">qualquer um</span><span class="sxs-lookup"><span data-stu-id="df243-132">any</span></span></p></td>
<td><p><span data-ttu-id="df243-133">não</span><span class="sxs-lookup"><span data-stu-id="df243-133">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df243-134">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="df243-134">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="df243-135">qualquer um</span><span class="sxs-lookup"><span data-stu-id="df243-135">any</span></span></p></td>
<td><p><span data-ttu-id="df243-136">não</span><span class="sxs-lookup"><span data-stu-id="df243-136">no</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="lync-client-support"></a><span data-ttu-id="df243-137">Suporte ao cliente do Lync</span><span class="sxs-lookup"><span data-stu-id="df243-137">Lync Client Support</span></span>

<span data-ttu-id="df243-138">A tabela a seguir identifica os clientes aos quais Location-Based roteamento oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="df243-138">The following table identifies the clients that Location-Based Routing supports.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="df243-139">Tipo de cliente</span><span class="sxs-lookup"><span data-stu-id="df243-139">Client type</span></span></th>
<th><span data-ttu-id="df243-140">Com suporte</span><span class="sxs-lookup"><span data-stu-id="df243-140">Supported</span></span></th>
<th><span data-ttu-id="df243-141">Detalhes</span><span class="sxs-lookup"><span data-stu-id="df243-141">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df243-142">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="df243-142">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="df243-143">sim</span><span class="sxs-lookup"><span data-stu-id="df243-143">yes</span></span></p></td>
<td><p><span data-ttu-id="df243-144">Incluindo a atualização cumulativa do Lync 2013 de fevereiro de 2013</span><span class="sxs-lookup"><span data-stu-id="df243-144">Including Lync 2013 February 2013 Cumulative Update</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df243-145">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="df243-145">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="df243-146">sim</span><span class="sxs-lookup"><span data-stu-id="df243-146">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df243-147">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="df243-147">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="df243-148">não</span><span class="sxs-lookup"><span data-stu-id="df243-148">no</span></span></p></td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df243-149">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="df243-149">Lync Phone Edition</span></span></p></td>
<td><p><span data-ttu-id="df243-150">sim</span><span class="sxs-lookup"><span data-stu-id="df243-150">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df243-151">Lync Attendant</span><span class="sxs-lookup"><span data-stu-id="df243-151">Lync Attendant</span></span></p></td>
<td><p><span data-ttu-id="df243-152">sim</span><span class="sxs-lookup"><span data-stu-id="df243-152">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df243-153">Lync para Windows 8</span><span class="sxs-lookup"><span data-stu-id="df243-153">Lync for Windows 8</span></span></p></td>
<td><p><span data-ttu-id="df243-154">não</span><span class="sxs-lookup"><span data-stu-id="df243-154">no</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df243-155">Lync móvel 2013</span><span class="sxs-lookup"><span data-stu-id="df243-155">Lync Mobile 2013</span></span></p></td>
<td><p><span data-ttu-id="df243-156">não</span><span class="sxs-lookup"><span data-stu-id="df243-156">no</span></span></p></td>
<td><p><span data-ttu-id="df243-157">O VoIP deve ser desabilitado para os clientes do Lync Mobile 2013 se usado por usuários com roteamento Location-Based habilitado.</span><span class="sxs-lookup"><span data-stu-id="df243-157">VoIP must be disabled for Lync Mobile 2013 clients if used by users with Location-Based Routing enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df243-158">Lync móvel 2010</span><span class="sxs-lookup"><span data-stu-id="df243-158">Lync Mobile 2010</span></span></p></td>
<td><p><span data-ttu-id="df243-159">sim</span><span class="sxs-lookup"><span data-stu-id="df243-159">yes</span></span></p></td>
<td> </td>
</tr>
</tbody>
</table>

  

<div>


> [!NOTE]  
> <span data-ttu-id="df243-160">Para desabilitar o VoIP para clientes móveis do Lync 2013, atribua uma política de mobilidade com a configuração, áudio/vídeo IP, desabilitada para todos os usuários habilitados para roteamento baseado em localização.</span><span class="sxs-lookup"><span data-stu-id="df243-160">To disable VoIP for Lync Mobile 2013 clients, assign a mobility policy with the setting, IP Audio/Video, disabled for all users enabled for Location Based Routing.</span></span> <span data-ttu-id="df243-161">Para obter mais detalhes sobre política de mobilidade, consulte <A href="https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy">New-CsMobilityPolicy</A>.</span><span class="sxs-lookup"><span data-stu-id="df243-161">For more details about mobility policy, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy">New-CsMobilityPolicy</A>.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="df243-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="df243-162">See Also</span></span>


[<span data-ttu-id="df243-163">Planejamento de Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df243-163">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="df243-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="df243-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

