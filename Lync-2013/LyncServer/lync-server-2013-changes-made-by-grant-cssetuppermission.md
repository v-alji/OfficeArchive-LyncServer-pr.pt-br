---
title: 'Lync Server 2013: alterações feitas por Grant-CsSetupPermission'
description: 'Lync Server 2013: alterações feitas por Grant-CsSetupPermission.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by Grant-CsSetupPermission
ms:assetid: c5801f48-14e3-4fdd-8f14-d52e7af07a57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205250(v=OCS.15)
ms:contentKeyID: 48185360
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d2a9156c977c993dd32e38fc6816bd08d3f65c1f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435065"
---
# <a name="changes-made-by-grant-cssetuppermission-in-lync-server-2013"></a><span data-ttu-id="847fe-103">Alterações feitas por Grant-CsSetupPermission no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="847fe-103">Changes made by Grant-CsSetupPermission in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="847fe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="847fe-104">

<span> </span></span></span>

<span data-ttu-id="847fe-105">_**Tópico da última modificação:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="847fe-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="847fe-106">Para delegar a instalação, você pode conceder permissões ao grupo universal RTCUniversalServerAdmins para uma unidade organizacional (OU) específica do Active Directory, permitindo que os membros do grupo RTCUniversalServerAdmins dessa UO instalem o Lync Server 2013 no domínio especificado sem serem membros do grupo Domain admins.</span><span class="sxs-lookup"><span data-stu-id="847fe-106">To delegate setup, you can grant permissions to the RTCUniversalServerAdmins universal group for a specific Active Directory organizational unit (OU), enabling members of the RTCUniversalServerAdmins group in that OU to install Lync Server 2013 in the specified domain without being members of the Domain Admins group.</span></span>

<span data-ttu-id="847fe-107">O cmdlet **Grant-CsSetupPermission** concede as permissões do grupo RTCUniversalServerAdmins em uma UO, conforme especificado na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="847fe-107">The **Grant-CsSetupPermission** cmdlet grants the RTCUniversalServerAdmins group permissions on an OU, as specified in the following table:</span></span>

### <a name="permissions-granted-to-objects-in-the-ou"></a><span data-ttu-id="847fe-108">Permissões concedidas a objetos na OU</span><span class="sxs-lookup"><span data-stu-id="847fe-108">Permissions granted to Objects in the OU</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="847fe-109">As permissões se aplicam a:</span><span class="sxs-lookup"><span data-stu-id="847fe-109">Permissions apply to:</span></span></th>
<th><span data-ttu-id="847fe-110">Permissões concedidas são:</span><span class="sxs-lookup"><span data-stu-id="847fe-110">Permissions granted are:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="847fe-111">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="847fe-111">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="847fe-112">Acesso especial:</span><span class="sxs-lookup"><span data-stu-id="847fe-112">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="847fe-113">Leia servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="847fe-113">Read servicePrincipalName</span></span></p></li>
<li><p><span data-ttu-id="847fe-114">Gravar servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="847fe-114">Write servicePrincipalName</span></span></p></li>
<li><p><span data-ttu-id="847fe-115">Excluir árvore</span><span class="sxs-lookup"><span data-stu-id="847fe-115">Delete tree</span></span></p></li>
<li><p><span data-ttu-id="847fe-116">Replicando alterações de diretório</span><span class="sxs-lookup"><span data-stu-id="847fe-116">Replicating directory changes</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="847fe-117">Objetos serviceConnectionPoint do descendant</span><span class="sxs-lookup"><span data-stu-id="847fe-117">Descendant serviceConnectionPoint objects</span></span></p></td>
<td><p><span data-ttu-id="847fe-118">Acesso especial:</span><span class="sxs-lookup"><span data-stu-id="847fe-118">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="847fe-119">Permissões de leitura</span><span class="sxs-lookup"><span data-stu-id="847fe-119">Read permissions</span></span></p></li>
<li><p><span data-ttu-id="847fe-120">Permissões de gravação</span><span class="sxs-lookup"><span data-stu-id="847fe-120">Write permissions</span></span></p></li>
<li><p><span data-ttu-id="847fe-121">Criar filho</span><span class="sxs-lookup"><span data-stu-id="847fe-121">Create child</span></span></p></li>
<li><p><span data-ttu-id="847fe-122">Excluir filho</span><span class="sxs-lookup"><span data-stu-id="847fe-122">Delete child</span></span></p></li>
<li><p><span data-ttu-id="847fe-123">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="847fe-123">List contents</span></span></p></li>
<li><p><span data-ttu-id="847fe-124">Propriedade de gravação</span><span class="sxs-lookup"><span data-stu-id="847fe-124">Write property</span></span></p></li>
<li><p><span data-ttu-id="847fe-125">Propriedade ler</span><span class="sxs-lookup"><span data-stu-id="847fe-125">Read property</span></span></p></li>
<li><p><span data-ttu-id="847fe-126">Excluir árvore</span><span class="sxs-lookup"><span data-stu-id="847fe-126">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="847fe-127">Objetos msRTCSIP-Server descendentes</span><span class="sxs-lookup"><span data-stu-id="847fe-127">Descendant msRTCSIP-Server objects</span></span></p></td>
<td><p><span data-ttu-id="847fe-128">Acesso especial:</span><span class="sxs-lookup"><span data-stu-id="847fe-128">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="847fe-129">Propriedade de gravação</span><span class="sxs-lookup"><span data-stu-id="847fe-129">Write property</span></span></p></li>
<li><p><span data-ttu-id="847fe-130">Propriedade ler</span><span class="sxs-lookup"><span data-stu-id="847fe-130">Read property</span></span></p></li>
<li><p><span data-ttu-id="847fe-131">Excluir árvore</span><span class="sxs-lookup"><span data-stu-id="847fe-131">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="847fe-132">Objetos msRTCSIP descendentes-WebComponents</span><span class="sxs-lookup"><span data-stu-id="847fe-132">Descendant msRTCSIP-WebComponents objects</span></span></p></td>
<td><p><span data-ttu-id="847fe-133">Acesso especial:</span><span class="sxs-lookup"><span data-stu-id="847fe-133">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="847fe-134">Propriedade de gravação</span><span class="sxs-lookup"><span data-stu-id="847fe-134">Write property</span></span></p></li>
<li><p><span data-ttu-id="847fe-135">Propriedade ler</span><span class="sxs-lookup"><span data-stu-id="847fe-135">Read property</span></span></p></li>
<li><p><span data-ttu-id="847fe-136">Excluir árvore</span><span class="sxs-lookup"><span data-stu-id="847fe-136">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="847fe-137">Objetos descendentes msRTCSIP-MCU</span><span class="sxs-lookup"><span data-stu-id="847fe-137">Descendant msRTCSIP-MCU objects</span></span></p></td>
<td><p><span data-ttu-id="847fe-138">Acesso especial:</span><span class="sxs-lookup"><span data-stu-id="847fe-138">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="847fe-139">Propriedade de gravação</span><span class="sxs-lookup"><span data-stu-id="847fe-139">Write property</span></span></p></li>
<li><p><span data-ttu-id="847fe-140">Propriedade ler</span><span class="sxs-lookup"><span data-stu-id="847fe-140">Read property</span></span></p></li>
<li><p><span data-ttu-id="847fe-141">Excluir árvore</span><span class="sxs-lookup"><span data-stu-id="847fe-141">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="847fe-142">Objetos msRTCSIP-MediationServer descendentes</span><span class="sxs-lookup"><span data-stu-id="847fe-142">Descendant msRTCSIP-MediationServer objects</span></span></p></td>
<td><p><span data-ttu-id="847fe-143">Acesso especial:</span><span class="sxs-lookup"><span data-stu-id="847fe-143">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="847fe-144">Propriedade de gravação</span><span class="sxs-lookup"><span data-stu-id="847fe-144">Write property</span></span></p></li>
<li><p><span data-ttu-id="847fe-145">Propriedade ler</span><span class="sxs-lookup"><span data-stu-id="847fe-145">Read property</span></span></p></li>
<li><p><span data-ttu-id="847fe-146">Excluir árvore</span><span class="sxs-lookup"><span data-stu-id="847fe-146">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="847fe-147">Objetos msRTCSIP-ApplicationServer descendentes</span><span class="sxs-lookup"><span data-stu-id="847fe-147">Descendant msRTCSIP-ApplicationServer objects</span></span></p></td>
<td><p><span data-ttu-id="847fe-148">Acesso especial:</span><span class="sxs-lookup"><span data-stu-id="847fe-148">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="847fe-149">Propriedade de gravação</span><span class="sxs-lookup"><span data-stu-id="847fe-149">Write property</span></span></p></li>
<li><p><span data-ttu-id="847fe-150">Propriedade ler</span><span class="sxs-lookup"><span data-stu-id="847fe-150">Read property</span></span></p></li>
<li><p><span data-ttu-id="847fe-151">Excluir árvore</span><span class="sxs-lookup"><span data-stu-id="847fe-151">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="847fe-152">Objetos descendentes msRTCSIP-ConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="847fe-152">Descendant msRTCSIP-ConnectionPoint objects</span></span></p></td>
<td><p><span data-ttu-id="847fe-153">Acesso especial:</span><span class="sxs-lookup"><span data-stu-id="847fe-153">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="847fe-154">Propriedade de gravação</span><span class="sxs-lookup"><span data-stu-id="847fe-154">Write property</span></span></p></li>
<li><p><span data-ttu-id="847fe-155">Propriedade ler</span><span class="sxs-lookup"><span data-stu-id="847fe-155">Read property</span></span></p></li>
<li><p><span data-ttu-id="847fe-156">Excluir árvore</span><span class="sxs-lookup"><span data-stu-id="847fe-156">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="847fe-157">Objetos de computador descendentes</span><span class="sxs-lookup"><span data-stu-id="847fe-157">Descendant Computer objects</span></span></p></td>
<td><p><span data-ttu-id="847fe-158">Acesso especial para serviceConnectionPoint:</span><span class="sxs-lookup"><span data-stu-id="847fe-158">Special access for serviceConnectionPoint:</span></span></p>
<ul>
<li><p><span data-ttu-id="847fe-159">Criar objetos filho</span><span class="sxs-lookup"><span data-stu-id="847fe-159">Create child objects</span></span></p></li>
<li><p><span data-ttu-id="847fe-160">Excluir objetos filho</span><span class="sxs-lookup"><span data-stu-id="847fe-160">Delete child objects</span></span></p></li>
<li><p><span data-ttu-id="847fe-161">Excluir árvore</span><span class="sxs-lookup"><span data-stu-id="847fe-161">Delete tree</span></span></p></li>
</ul>
<p><span data-ttu-id="847fe-162">Acesso especial para informações públicas:</span><span class="sxs-lookup"><span data-stu-id="847fe-162">Special access for public information:</span></span></p>
<ul>
<li><p><span data-ttu-id="847fe-163">Propriedade ler</span><span class="sxs-lookup"><span data-stu-id="847fe-163">Read property</span></span></p></li>
</ul>
<p><span data-ttu-id="847fe-164">Acesso especial para o nome do host DNS:</span><span class="sxs-lookup"><span data-stu-id="847fe-164">Special access for DNS host name:</span></span></p>
<ul>
<li><p><span data-ttu-id="847fe-165">Propriedade ler</span><span class="sxs-lookup"><span data-stu-id="847fe-165">Read property</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="847fe-166">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="847fe-166">


</div>

<span> </span>

</div>

</div>

</span></span></div>

