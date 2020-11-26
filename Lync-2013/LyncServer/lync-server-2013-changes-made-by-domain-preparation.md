---
title: 'Lync Server 2013: alterações feitas pela preparação do domínio'
description: 'Lync Server 2013: alterações feitas pela preparação do domínio.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by domain preparation
ms:assetid: 9191221e-6166-4c2b-837e-fa73d90fdf80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398742(v=OCS.15)
ms:contentKeyID: 48184845
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26400bd1c72c6ae3b8dc1f2d2d8f6c6906b80595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435114"
---
# <a name="changes-made-by-domain-preparation-in-lync-server-2013"></a><span data-ttu-id="df2a8-103">Alterações feitas por preparação do domínio no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df2a8-103">Changes made by domain preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="df2a8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="df2a8-104">

<span> </span></span></span>

<span data-ttu-id="df2a8-105">_**Tópico da última modificação:** 2010-10-18_</span><span class="sxs-lookup"><span data-stu-id="df2a8-105">_**Topic Last Modified:** 2010-10-18_</span></span>

<span data-ttu-id="df2a8-106">A tabela a seguir lista as entradas de controle de acesso (ACEs) que a preparação do domínio cria na raiz do domínio.</span><span class="sxs-lookup"><span data-stu-id="df2a8-106">The following table lists the access control entries (ACEs) that domain preparation creates on the domain root.</span></span> <span data-ttu-id="df2a8-107">Todas as ACEs são herdadas, a menos que indicado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="df2a8-107">All ACEs are inherited unless otherwise noted.</span></span>

<div id="sectionSection0" class="section">

### <a name="aces-added-to-domain-root"></a><span data-ttu-id="df2a8-108">ACEs adicionadas à raiz do domínio</span><span class="sxs-lookup"><span data-stu-id="df2a8-108">ACEs Added to Domain Root</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="df2a8-109">ACE</span><span class="sxs-lookup"><span data-stu-id="df2a8-109">ACE</span></span></th>
<th><span data-ttu-id="df2a8-110">RTCUniversal-userreadonly-Group</span><span class="sxs-lookup"><span data-stu-id="df2a8-110">RTCUniversal-UserReadOnly-Group</span></span></th>
<th><span data-ttu-id="df2a8-111">RTCUniversal-ServerReadOnly-Group</span><span class="sxs-lookup"><span data-stu-id="df2a8-111">RTCUniversal-ServerReadOnly-Group</span></span></th>
<th><span data-ttu-id="df2a8-112">RTCUniversal-UserAdmins</span><span class="sxs-lookup"><span data-stu-id="df2a8-112">RTCUniversal-UserAdmins</span></span></th>
<th><span data-ttu-id="df2a8-113">RTCHSUniversal-Services</span><span class="sxs-lookup"><span data-stu-id="df2a8-113">RTCHSUniversal-Services</span></span></th>
<th><span data-ttu-id="df2a8-114">Authenticated-Users</span><span class="sxs-lookup"><span data-stu-id="df2a8-114">Authenticated-Users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df2a8-115">Contêiner de leitura (não herdado)</span><span class="sxs-lookup"><span data-stu-id="df2a8-115">Read Container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="df2a8-116"><strong>Sim</strong></span><span class="sxs-lookup"><span data-stu-id="df2a8-116"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="df2a8-117"><strong>Sim</strong></span><span class="sxs-lookup"><span data-stu-id="df2a8-117"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="df2a8-118">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-118">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-119">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-119">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-120">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-120">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df2a8-121">Ler propriedades do usuário-User-Restriction-restrições de conta</span><span class="sxs-lookup"><span data-stu-id="df2a8-121">Read User PropertySet User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="df2a8-122"><strong>Sim</strong></span><span class="sxs-lookup"><span data-stu-id="df2a8-122"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="df2a8-123">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-123">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-124">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-124">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-125">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-125">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-126">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df2a8-127">Ler o usuário do PropertySet Personal-Information</span><span class="sxs-lookup"><span data-stu-id="df2a8-127">Read User PropertySet Personal-Information</span></span></p></td>
<td><p><span data-ttu-id="df2a8-128"><strong>Sim</strong></span><span class="sxs-lookup"><span data-stu-id="df2a8-128"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="df2a8-129">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-129">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-130">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-130">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-131">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-131">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-132">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-132">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df2a8-133">Ler o usuário do PropertySet General-Information</span><span class="sxs-lookup"><span data-stu-id="df2a8-133">Read User PropertySet General-Information</span></span></p></td>
<td><p><span data-ttu-id="df2a8-134"><strong>Sim</strong></span><span class="sxs-lookup"><span data-stu-id="df2a8-134"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="df2a8-135">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-135">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-136">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-136">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-137">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-137">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-138">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-138">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df2a8-139">Ler o usuário do PropertySet Public-Information</span><span class="sxs-lookup"><span data-stu-id="df2a8-139">Read User PropertySet Public-Information</span></span></p></td>
<td><p><span data-ttu-id="df2a8-140"><strong>Sim</strong></span><span class="sxs-lookup"><span data-stu-id="df2a8-140"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="df2a8-141">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-141">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-142">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-142">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-143">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-143">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-144">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-144">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df2a8-145">Ler o usuário do PropertySet RTCUserSearchProperty-Set</span><span class="sxs-lookup"><span data-stu-id="df2a8-145">Read User PropertySet RTCUserSearchProperty-Set</span></span></p></td>
<td><p><span data-ttu-id="df2a8-146"><strong>Sim</strong></span><span class="sxs-lookup"><span data-stu-id="df2a8-146"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="df2a8-147">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-147">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-148">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-148">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-149">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-149">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-150"><strong>Sim</strong></span><span class="sxs-lookup"><span data-stu-id="df2a8-150"><strong>Yes</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df2a8-151">Ler RTCPropertySet de propriedades do usuário</span><span class="sxs-lookup"><span data-stu-id="df2a8-151">Read User PropertySet RTCPropertySet</span></span></p></td>
<td><p><span data-ttu-id="df2a8-152"><strong>Sim</strong></span><span class="sxs-lookup"><span data-stu-id="df2a8-152"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="df2a8-153">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-153">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-154">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-154">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-155">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-155">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-156">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df2a8-157">Proxy-Addresses de propriedades de gravação do usuário</span><span class="sxs-lookup"><span data-stu-id="df2a8-157">Write User Property Proxy-Addresses</span></span></p></td>
<td><p><span data-ttu-id="df2a8-158">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-158">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-159">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-159">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-160"><strong>Sim</strong></span><span class="sxs-lookup"><span data-stu-id="df2a8-160"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="df2a8-161">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-161">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-162">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-162">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df2a8-163">Criar RTCUserSearchProperty-Set de propriedades do usuário</span><span class="sxs-lookup"><span data-stu-id="df2a8-163">Write User PropertySet RTCUserSearchProperty-Set</span></span></p></td>
<td><p><span data-ttu-id="df2a8-164">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-164">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-165">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-165">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-166"><strong>Sim</strong></span><span class="sxs-lookup"><span data-stu-id="df2a8-166"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="df2a8-167">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-167">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-168">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-168">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df2a8-169">Gravar usuário do RTCPropertySet de propriedades</span><span class="sxs-lookup"><span data-stu-id="df2a8-169">Write User PropertySet RTCPropertySet</span></span></p></td>
<td><p><span data-ttu-id="df2a8-170">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-170">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-171">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-171">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-172"><strong>Sim</strong></span><span class="sxs-lookup"><span data-stu-id="df2a8-172"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="df2a8-173">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-173">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-174">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-174">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df2a8-175">Ler PropertySet DS-Replication-Get-Changes de todos os objetos do Active Directory</span><span class="sxs-lookup"><span data-stu-id="df2a8-175">Read PropertySet DS-Replication-Get-Changes of all Active Directory objects</span></span></p></td>
<td><p><span data-ttu-id="df2a8-176">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-176">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-177">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-177">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-178">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-178">No</span></span></p></td>
<td><p><span data-ttu-id="df2a8-179"><strong>Sim</strong></span><span class="sxs-lookup"><span data-stu-id="df2a8-179"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="df2a8-180">Não</span><span class="sxs-lookup"><span data-stu-id="df2a8-180">No</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="df2a8-181">A tabela a seguir lista as ACEs que a preparação do domínio cria nos três contêineres internos: usuários, computadores e controladores de domínio.</span><span class="sxs-lookup"><span data-stu-id="df2a8-181">The following table lists the ACEs that domain preparation creates in the three built-in containers: Users, Computers, and Domain Controllers.</span></span> <span data-ttu-id="df2a8-182">Todas as ACEs são herdadas, a menos que indicado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="df2a8-182">All ACEs are inherited unless otherwise noted.</span></span>

### <a name="aces-added-to-built-in-containers"></a><span data-ttu-id="df2a8-183">ACEs adicionadas a contêineres internos</span><span class="sxs-lookup"><span data-stu-id="df2a8-183">ACEs Added to Built-in Containers</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="df2a8-184">ACE</span><span class="sxs-lookup"><span data-stu-id="df2a8-184">ACE</span></span></th>
<th><span data-ttu-id="df2a8-185">RTCUniversal-userreadonly-Group</span><span class="sxs-lookup"><span data-stu-id="df2a8-185">RTCUniversal-UserReadOnly-Group</span></span></th>
<th><span data-ttu-id="df2a8-186">RTCUniversal-ServerReadOnly-Group</span><span class="sxs-lookup"><span data-stu-id="df2a8-186">RTCUniversal-ServerReadOnly-Group</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df2a8-187">Contêiner de leitura (não herdado)</span><span class="sxs-lookup"><span data-stu-id="df2a8-187">Read Container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="df2a8-188"><strong>Sim</strong></span><span class="sxs-lookup"><span data-stu-id="df2a8-188"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="df2a8-189"><strong>Sim</strong></span><span class="sxs-lookup"><span data-stu-id="df2a8-189"><strong>Yes</strong></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="df2a8-190">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="df2a8-190">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

