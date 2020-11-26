---
title: 'Lync Server 2013: alterações feitas por Grant-CsOUPermission'
description: 'Lync Server 2013: alterações feitas por Grant-CsOUPermission.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by Grant-CsOUPermission
ms:assetid: d744d352-1ad9-4447-8e2b-28e768d2ed1b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205310(v=OCS.15)
ms:contentKeyID: 48185564
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10d3db0e9dde380628690bc016e2b4bd2ec85b54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435051"
---
# <a name="changes-made-by-grant-csoupermission-in-lync-server-2013"></a><span data-ttu-id="c9161-103">Alterações feitas por Grant-CsOUPermission no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c9161-103">Changes made by Grant-CsOUPermission in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c9161-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c9161-104">

<span> </span></span></span>

<span data-ttu-id="c9161-105">_**Tópico da última modificação:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="c9161-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="c9161-106">Para delegar a administração do Lync Server 2013, você pode adicionar permissões a unidades organizacionais (UOs) especificadas para que os membros dos grupos universais do RTC criados pela preparação da floresta possam acessar as UOs sem serem membros do grupo Domain admins.</span><span class="sxs-lookup"><span data-stu-id="c9161-106">To delegate Lync Server 2013 administration, you can add permissions to specified organizational units (OUs) so that members of the RTC universal groups created by forest preparation can access the OUs without being members of the Domain Admins group.</span></span>

<span data-ttu-id="c9161-107">O cmdlet **Grant-CsOuPermission** concede permissões a objetos na unidade organizacional especificada, conforme especificado nas tabelas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c9161-107">The **Grant-CsOuPermission** cmdlet grants permissions to objects in the specified OU as specified in the following tables.</span></span>

<div>

## <a name="granting-permission-for-user-objects"></a><span data-ttu-id="c9161-108">Concedendo permissão para objetos de usuário</span><span class="sxs-lookup"><span data-stu-id="c9161-108">Granting Permission for User Objects</span></span>

<span data-ttu-id="c9161-109">Quando você executa o cmdlet **Grant-CsOuPermission** para objetos de usuário em uma ou, os grupos recebem permissões para os grupos, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c9161-109">When you run the **Grant-CsOuPermission** cmdlet for User objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-user-objects"></a><span data-ttu-id="c9161-110">Permissões concedidas para objetos de usuário</span><span class="sxs-lookup"><span data-stu-id="c9161-110">Permissions Granted for User Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9161-111">Grupos</span><span class="sxs-lookup"><span data-stu-id="c9161-111">Group</span></span></th>
<th><span data-ttu-id="c9161-112">Permissão</span><span class="sxs-lookup"><span data-stu-id="c9161-112">Permission</span></span></th>
<th><span data-ttu-id="c9161-113">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="c9161-113">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9161-114">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="c9161-114">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="c9161-115">Replicando alterações de diretório</span><span class="sxs-lookup"><span data-stu-id="c9161-115">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="c9161-116">Somente este objeto</span><span class="sxs-lookup"><span data-stu-id="c9161-116">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9161-117">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="c9161-117">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="c9161-118">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="c9161-118">List contents</span></span></p>
<p><span data-ttu-id="c9161-119">Ler todas as propriedades</span><span class="sxs-lookup"><span data-stu-id="c9161-119">Read all properties</span></span></p>
<p><span data-ttu-id="c9161-120">Permissões de leitura</span><span class="sxs-lookup"><span data-stu-id="c9161-120">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="c9161-121">Somente este objeto</span><span class="sxs-lookup"><span data-stu-id="c9161-121">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9161-122">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="c9161-122">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="c9161-123">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="c9161-123">List contents</span></span></p>
<p><span data-ttu-id="c9161-124">Ler todas as propriedades</span><span class="sxs-lookup"><span data-stu-id="c9161-124">Read all properties</span></span></p>
<p><span data-ttu-id="c9161-125">Permissões de leitura</span><span class="sxs-lookup"><span data-stu-id="c9161-125">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="c9161-126">Somente este objeto</span><span class="sxs-lookup"><span data-stu-id="c9161-126">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9161-127">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="c9161-127">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="c9161-128">Ler RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-128">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="c9161-129">Ler RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-129">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="c9161-130">Ler RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-130">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="c9161-131">Ler Public-Information</span><span class="sxs-lookup"><span data-stu-id="c9161-131">Read Public-Information</span></span></p>
<p><span data-ttu-id="c9161-132">Ler General-Information</span><span class="sxs-lookup"><span data-stu-id="c9161-132">Read General-Information</span></span></p>
<p><span data-ttu-id="c9161-133">Ler restrições de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="c9161-133">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="c9161-134">Objetos de usuário descendentes</span><span class="sxs-lookup"><span data-stu-id="c9161-134">Descendant User objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9161-135">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="c9161-135">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="c9161-136">Escrever RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-136">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="c9161-137">Escrever msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="c9161-137">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="c9161-138">Escrever RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-138">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="c9161-139">Escrever RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-139">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="c9161-140">Escrever proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="c9161-140">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="c9161-141">Objetos de usuário descendentes</span><span class="sxs-lookup"><span data-stu-id="c9161-141">Descendant User objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-computer-objects"></a><span data-ttu-id="c9161-142">Concedendo permissão para objetos de computador</span><span class="sxs-lookup"><span data-stu-id="c9161-142">Granting Permission for Computer Objects</span></span>

<span data-ttu-id="c9161-143">Quando você executa o cmdlet **Grant-CsOuPermission** para objetos de computador em uma ou, os grupos recebem permissões para os grupos, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c9161-143">When you run the **Grant-CsOuPermission** cmdlet for Computer objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-computer-objects"></a><span data-ttu-id="c9161-144">Permissões concedidas para objetos de computador</span><span class="sxs-lookup"><span data-stu-id="c9161-144">Permissions Granted for Computer Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9161-145">Grupos</span><span class="sxs-lookup"><span data-stu-id="c9161-145">Group</span></span></th>
<th><span data-ttu-id="c9161-146">Permissão</span><span class="sxs-lookup"><span data-stu-id="c9161-146">Permission</span></span></th>
<th><span data-ttu-id="c9161-147">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="c9161-147">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9161-148">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="c9161-148">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="c9161-149">Replicando alterações de diretório</span><span class="sxs-lookup"><span data-stu-id="c9161-149">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="c9161-150">Somente este objeto</span><span class="sxs-lookup"><span data-stu-id="c9161-150">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9161-151">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="c9161-151">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="c9161-152">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="c9161-152">List contents</span></span></p>
<p><span data-ttu-id="c9161-153">Ler todas as propriedades</span><span class="sxs-lookup"><span data-stu-id="c9161-153">Read all properties</span></span></p>
<p><span data-ttu-id="c9161-154">Permissões de leitura</span><span class="sxs-lookup"><span data-stu-id="c9161-154">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="c9161-155">Somente este objeto</span><span class="sxs-lookup"><span data-stu-id="c9161-155">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9161-156">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="c9161-156">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="c9161-157">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="c9161-157">List contents</span></span></p>
<p><span data-ttu-id="c9161-158">Ler todas as propriedades</span><span class="sxs-lookup"><span data-stu-id="c9161-158">Read all properties</span></span></p>
<p><span data-ttu-id="c9161-159">Permissões de leitura</span><span class="sxs-lookup"><span data-stu-id="c9161-159">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="c9161-160">Somente este objeto</span><span class="sxs-lookup"><span data-stu-id="c9161-160">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9161-161">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="c9161-161">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="c9161-162">Ler Public-Information</span><span class="sxs-lookup"><span data-stu-id="c9161-162">Read Public-Information</span></span></p>
<p><span data-ttu-id="c9161-163">Leitura validada-DNS-nome do host</span><span class="sxs-lookup"><span data-stu-id="c9161-163">Read Validated-DNS-Host-Name</span></span></p></td>
<td><p><span data-ttu-id="c9161-164">Objetos de computador descendentes</span><span class="sxs-lookup"><span data-stu-id="c9161-164">Descendant Computer objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9161-165">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="c9161-165">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="c9161-166">Ler Public-Information</span><span class="sxs-lookup"><span data-stu-id="c9161-166">Read Public-Information</span></span></p>
<p><span data-ttu-id="c9161-167">Leitura validada-DNS-nome do host</span><span class="sxs-lookup"><span data-stu-id="c9161-167">Read Validated-DNS-Host-Name</span></span></p></td>
<td><p><span data-ttu-id="c9161-168">Objetos de computador descendentes</span><span class="sxs-lookup"><span data-stu-id="c9161-168">Descendant Computer objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-contact-or-appcontact-objects"></a><span data-ttu-id="c9161-169">Concedendo permissão para objetos de contato ou AppContact</span><span class="sxs-lookup"><span data-stu-id="c9161-169">Granting Permission for Contact or AppContact Objects</span></span>

<span data-ttu-id="c9161-170">Quando você executa o cmdlet **Grant-CsOuPermission** para objetos de contato ou objetos AppContact em uma ou, os grupos recebem permissões como mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c9161-170">When you run the **Grant-CsOuPermission** cmdlet for Contact objects or AppContact objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-contact-or-appcontact-objects"></a><span data-ttu-id="c9161-171">Permissões concedidas para objetos de contato ou AppContact</span><span class="sxs-lookup"><span data-stu-id="c9161-171">Permissions Granted for Contact or AppContact Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9161-172">Grupos</span><span class="sxs-lookup"><span data-stu-id="c9161-172">Group</span></span></th>
<th><span data-ttu-id="c9161-173">Permissão</span><span class="sxs-lookup"><span data-stu-id="c9161-173">Permission</span></span></th>
<th><span data-ttu-id="c9161-174">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="c9161-174">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9161-175">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="c9161-175">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="c9161-176">Replicando alterações de diretório</span><span class="sxs-lookup"><span data-stu-id="c9161-176">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="c9161-177">Somente este objeto</span><span class="sxs-lookup"><span data-stu-id="c9161-177">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9161-178">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="c9161-178">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="c9161-179">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="c9161-179">List contents</span></span></p>
<p><span data-ttu-id="c9161-180">Ler todas as propriedades</span><span class="sxs-lookup"><span data-stu-id="c9161-180">Read all properties</span></span></p>
<p><span data-ttu-id="c9161-181">Permissões de leitura</span><span class="sxs-lookup"><span data-stu-id="c9161-181">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="c9161-182">Somente este objeto</span><span class="sxs-lookup"><span data-stu-id="c9161-182">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9161-183">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="c9161-183">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="c9161-184">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="c9161-184">List contents</span></span></p>
<p><span data-ttu-id="c9161-185">Ler todas as propriedades</span><span class="sxs-lookup"><span data-stu-id="c9161-185">Read all properties</span></span></p>
<p><span data-ttu-id="c9161-186">Permissões de leitura</span><span class="sxs-lookup"><span data-stu-id="c9161-186">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="c9161-187">Somente este objeto</span><span class="sxs-lookup"><span data-stu-id="c9161-187">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9161-188">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="c9161-188">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="c9161-189">Ler RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-189">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="c9161-190">Ler RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-190">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="c9161-191">Ler RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-191">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="c9161-192">Ler Public-Information</span><span class="sxs-lookup"><span data-stu-id="c9161-192">Read Public-Information</span></span></p>
<p><span data-ttu-id="c9161-193">Ler General-Information</span><span class="sxs-lookup"><span data-stu-id="c9161-193">Read General-Information</span></span></p>
<p><span data-ttu-id="c9161-194">Ler Personal-Information</span><span class="sxs-lookup"><span data-stu-id="c9161-194">Read Personal-Information</span></span></p>
<p><span data-ttu-id="c9161-195">Ler restrições de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="c9161-195">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="c9161-196">Objetos de contato descendentes</span><span class="sxs-lookup"><span data-stu-id="c9161-196">Descendant Contact objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9161-197">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="c9161-197">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="c9161-198">Escrever RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-198">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="c9161-199">Escrever otherIpPhone</span><span class="sxs-lookup"><span data-stu-id="c9161-199">Write otherIpPhone</span></span></p>
<p><span data-ttu-id="c9161-200">Escrever displayName</span><span class="sxs-lookup"><span data-stu-id="c9161-200">Write displayName</span></span></p>
<p><span data-ttu-id="c9161-201">Descrição da gravação</span><span class="sxs-lookup"><span data-stu-id="c9161-201">Write description</span></span></p>
<p><span data-ttu-id="c9161-202">Escrever telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="c9161-202">Write telephoneNumber</span></span></p>
<p><span data-ttu-id="c9161-203">Escrever msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="c9161-203">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="c9161-204">Escrever RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-204">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="c9161-205">Escrever RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-205">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="c9161-206">Escrever proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="c9161-206">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="c9161-207">Objetos de contato descendentes</span><span class="sxs-lookup"><span data-stu-id="c9161-207">Descendant Contact objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-device-objects"></a><span data-ttu-id="c9161-208">Concedendo permissão para objetos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="c9161-208">Granting Permission for Device Objects</span></span>

<span data-ttu-id="c9161-209">Quando você executa o cmdlet **Grant-CsOuPermission** para objetos de dispositivo em uma ou, os grupos recebem permissões como mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c9161-209">When you run the **Grant-CsOuPermission** cmdlet for Device objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-device-objects"></a><span data-ttu-id="c9161-210">Permissões concedidas para objetos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="c9161-210">Permissions Granted for Device Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9161-211">Grupos</span><span class="sxs-lookup"><span data-stu-id="c9161-211">Group</span></span></th>
<th><span data-ttu-id="c9161-212">Permissão</span><span class="sxs-lookup"><span data-stu-id="c9161-212">Permission</span></span></th>
<th><span data-ttu-id="c9161-213">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="c9161-213">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9161-214">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="c9161-214">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="c9161-215">Replicando alterações de diretório</span><span class="sxs-lookup"><span data-stu-id="c9161-215">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="c9161-216">Somente este objeto</span><span class="sxs-lookup"><span data-stu-id="c9161-216">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9161-217">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="c9161-217">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="c9161-218">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="c9161-218">List contents</span></span></p>
<p><span data-ttu-id="c9161-219">Ler todas as propriedades</span><span class="sxs-lookup"><span data-stu-id="c9161-219">Read all properties</span></span></p>
<p><span data-ttu-id="c9161-220">Permissões de leitura</span><span class="sxs-lookup"><span data-stu-id="c9161-220">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="c9161-221">Somente este objeto</span><span class="sxs-lookup"><span data-stu-id="c9161-221">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9161-222">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="c9161-222">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="c9161-223">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="c9161-223">List contents</span></span></p>
<p><span data-ttu-id="c9161-224">Ler todas as propriedades</span><span class="sxs-lookup"><span data-stu-id="c9161-224">Read all properties</span></span></p>
<p><span data-ttu-id="c9161-225">Permissões de leitura</span><span class="sxs-lookup"><span data-stu-id="c9161-225">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="c9161-226">Somente este objeto</span><span class="sxs-lookup"><span data-stu-id="c9161-226">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9161-227">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="c9161-227">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="c9161-228">Ler RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-228">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="c9161-229">Ler RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-229">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="c9161-230">Ler RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-230">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="c9161-231">Ler Public-Information</span><span class="sxs-lookup"><span data-stu-id="c9161-231">Read Public-Information</span></span></p>
<p><span data-ttu-id="c9161-232">Ler Personal-Information</span><span class="sxs-lookup"><span data-stu-id="c9161-232">Read Personal-Information</span></span></p>
<p><span data-ttu-id="c9161-233">Ler General-Information</span><span class="sxs-lookup"><span data-stu-id="c9161-233">Read General-Information</span></span></p>
<p><span data-ttu-id="c9161-234">Ler restrições de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="c9161-234">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="c9161-235">Objetos de contato descendentes</span><span class="sxs-lookup"><span data-stu-id="c9161-235">Descendant Contact objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9161-236">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="c9161-236">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="c9161-237">Criar filho</span><span class="sxs-lookup"><span data-stu-id="c9161-237">Create child</span></span></p>
<p><span data-ttu-id="c9161-238">Excluir filho</span><span class="sxs-lookup"><span data-stu-id="c9161-238">Delete child</span></span></p>
<p><span data-ttu-id="c9161-239">Excluir árvore</span><span class="sxs-lookup"><span data-stu-id="c9161-239">Delete tree</span></span></p></td>
<td><p><span data-ttu-id="c9161-240">Entrando</span><span class="sxs-lookup"><span data-stu-id="c9161-240">Contact</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9161-241">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="c9161-241">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="c9161-242">Escrever displayName</span><span class="sxs-lookup"><span data-stu-id="c9161-242">Write displayName</span></span></p>
<p><span data-ttu-id="c9161-243">Descrição da gravação</span><span class="sxs-lookup"><span data-stu-id="c9161-243">Write description</span></span></p>
<p><span data-ttu-id="c9161-244">Escrever telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="c9161-244">Write telephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="c9161-245">Objetos de usuário descendentes</span><span class="sxs-lookup"><span data-stu-id="c9161-245">Descendant User objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9161-246">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="c9161-246">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="c9161-247">Escrever RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-247">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="c9161-248">Escrever otherIpPhone</span><span class="sxs-lookup"><span data-stu-id="c9161-248">Write otherIpPhone</span></span></p>
<p><span data-ttu-id="c9161-249">Escrever displayName</span><span class="sxs-lookup"><span data-stu-id="c9161-249">Write displayName</span></span></p>
<p><span data-ttu-id="c9161-250">Descrição da gravação</span><span class="sxs-lookup"><span data-stu-id="c9161-250">Write description</span></span></p>
<p><span data-ttu-id="c9161-251">Escrever telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="c9161-251">Write telephoneNumber</span></span></p>
<p><span data-ttu-id="c9161-252">Escrever msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="c9161-252">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="c9161-253">Escrever RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-253">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="c9161-254">Escrever RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-254">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="c9161-255">Escrever proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="c9161-255">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="c9161-256">Objetos de contato descendentes</span><span class="sxs-lookup"><span data-stu-id="c9161-256">Descendant Contact objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-inetorgperson-objects"></a><span data-ttu-id="c9161-257">Concedendo permissão para objetos InetOrgPerson</span><span class="sxs-lookup"><span data-stu-id="c9161-257">Granting Permission for InetOrgPerson Objects</span></span>

<span data-ttu-id="c9161-258">Quando você executa o cmdlet **Grant-CsOuPermission** para objetos inetOrgPerson em uma ou, os grupos recebem permissões como mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c9161-258">When you run the **Grant-CsOuPermission** cmdlet for InetOrgPerson objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-inetorgperson-objects"></a><span data-ttu-id="c9161-259">Permissões concedidas para objetos InetOrgPerson</span><span class="sxs-lookup"><span data-stu-id="c9161-259">Permissions Granted for InetOrgPerson Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9161-260">Grupos</span><span class="sxs-lookup"><span data-stu-id="c9161-260">Group</span></span></th>
<th><span data-ttu-id="c9161-261">Permissão</span><span class="sxs-lookup"><span data-stu-id="c9161-261">Permission</span></span></th>
<th><span data-ttu-id="c9161-262">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="c9161-262">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9161-263">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="c9161-263">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="c9161-264">Replicando alterações de diretório</span><span class="sxs-lookup"><span data-stu-id="c9161-264">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="c9161-265">Somente este objeto</span><span class="sxs-lookup"><span data-stu-id="c9161-265">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9161-266">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="c9161-266">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="c9161-267">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="c9161-267">List contents</span></span></p>
<p><span data-ttu-id="c9161-268">Ler todas as propriedades</span><span class="sxs-lookup"><span data-stu-id="c9161-268">Read all properties</span></span></p>
<p><span data-ttu-id="c9161-269">Permissões de leitura</span><span class="sxs-lookup"><span data-stu-id="c9161-269">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="c9161-270">Somente este objeto</span><span class="sxs-lookup"><span data-stu-id="c9161-270">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9161-271">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="c9161-271">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="c9161-272">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="c9161-272">List contents</span></span></p>
<p><span data-ttu-id="c9161-273">Ler todas as propriedades</span><span class="sxs-lookup"><span data-stu-id="c9161-273">Read all properties</span></span></p>
<p><span data-ttu-id="c9161-274">Permissões de leitura</span><span class="sxs-lookup"><span data-stu-id="c9161-274">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="c9161-275">Somente este objeto</span><span class="sxs-lookup"><span data-stu-id="c9161-275">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9161-276">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="c9161-276">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="c9161-277">Ler RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-277">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="c9161-278">Ler RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-278">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="c9161-279">Ler RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-279">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="c9161-280">Ler Personal-Information</span><span class="sxs-lookup"><span data-stu-id="c9161-280">Read Personal-Information</span></span></p>
<p><span data-ttu-id="c9161-281">Ler Public-Information</span><span class="sxs-lookup"><span data-stu-id="c9161-281">Read Public-Information</span></span></p>
<p><span data-ttu-id="c9161-282">Ler General-Information</span><span class="sxs-lookup"><span data-stu-id="c9161-282">Read General-Information</span></span></p>
<p><span data-ttu-id="c9161-283">Ler restrições de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="c9161-283">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="c9161-284">Objetos inetOrgPerson descendentes</span><span class="sxs-lookup"><span data-stu-id="c9161-284">Descendant inetOrgPerson objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9161-285">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="c9161-285">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="c9161-286">Escrever RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-286">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="c9161-287">Escrever RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-287">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="c9161-288">Escrever RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="c9161-288">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="c9161-289">Escrever proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="c9161-289">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="c9161-290">Objetos inetOrgPerson descendentes</span><span class="sxs-lookup"><span data-stu-id="c9161-290">Descendant inetOrgPerson objects</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c9161-291">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c9161-291">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

