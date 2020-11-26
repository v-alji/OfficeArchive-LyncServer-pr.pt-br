---
title: 'Lync Server 2013: tblPrincipal'
description: 'Lync Server 2013: tblPrincipal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipal
ms:assetid: 79a24502-b4ce-41f0-8979-8caddf535338
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558667(v=OCS.15)
ms:contentKeyID: 48184571
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f07b37ac4c8ceed5c044b5c263eeee6370adfdc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444410"
---
# <a name="tblprincipal-in-lync-server-2013"></a><span data-ttu-id="57495-103">tblPrincipal no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57495-103">tblPrincipal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="57495-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="57495-104">

<span> </span></span></span>

<span data-ttu-id="57495-105">_**Tópico da última modificação:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="57495-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="57495-106">tblPrincipal contém todas as entidades, incluindo usuários, pastas e grupos.</span><span class="sxs-lookup"><span data-stu-id="57495-106">tblPrincipal contains all principals, including users, folders, and groups.</span></span>

### <a name="columns"></a><span data-ttu-id="57495-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="57495-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57495-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="57495-108">Column</span></span></th>
<th><span data-ttu-id="57495-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="57495-109">Type</span></span></th>
<th><span data-ttu-id="57495-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="57495-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57495-111">multiimprimir</span><span class="sxs-lookup"><span data-stu-id="57495-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="57495-112">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="57495-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="57495-113">ID da entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="57495-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57495-114">prinGuid</span><span class="sxs-lookup"><span data-stu-id="57495-114">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="57495-115">GUID, não nulo</span><span class="sxs-lookup"><span data-stu-id="57495-115">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="57495-116">GUID principal.</span><span class="sxs-lookup"><span data-stu-id="57495-116">Principal GUID.</span></span> <span data-ttu-id="57495-117">Isso é amplamente usado como uma chave primária alternativa porque o significado é cruzado para o espaço dos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="57495-117">This is broadly used as an alternate primary key because its meaning crosses over into the Active Directory Domain Services space.</span></span> <span data-ttu-id="57495-118">(O GUID de uma entidade do cache é igual à GUID do objeto do Active Directory correspondente.)</span><span class="sxs-lookup"><span data-stu-id="57495-118">(The GUID for a cached principal is equal to the corresponding Active Directory object GUID.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57495-119">prinUri</span><span class="sxs-lookup"><span data-stu-id="57495-119">prinUri</span></span></p></td>
<td><p><span data-ttu-id="57495-120">nvarchar (256), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="57495-120">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="57495-121">URI principal.</span><span class="sxs-lookup"><span data-stu-id="57495-121">Principal URI.</span></span> <span data-ttu-id="57495-122">O esquema SIP é usado para os usuários, e o ma-GRP é usado para praticamente tudo o mais.</span><span class="sxs-lookup"><span data-stu-id="57495-122">The SIP scheme is used for users, and ma-grp is used for almost everything else.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57495-123">imprimir</span><span class="sxs-lookup"><span data-stu-id="57495-123">prinName</span></span></p></td>
<td><p><span data-ttu-id="57495-124">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="57495-124">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="57495-125">Nome comum.</span><span class="sxs-lookup"><span data-stu-id="57495-125">Common name.</span></span> <span data-ttu-id="57495-126">Usado apenas por tipos de usuário.</span><span class="sxs-lookup"><span data-stu-id="57495-126">Used only by user types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57495-127">prinDisplayName</span><span class="sxs-lookup"><span data-stu-id="57495-127">prinDisplayName</span></span></p></td>
<td><p><span data-ttu-id="57495-128">Nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="57495-128">Nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="57495-129">Nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="57495-129">Display name.</span></span> <span data-ttu-id="57495-130">Usado apenas por tipos de usuário.</span><span class="sxs-lookup"><span data-stu-id="57495-130">Used only by user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57495-131">prinCompanyName</span><span class="sxs-lookup"><span data-stu-id="57495-131">prinCompanyName</span></span></p></td>
<td><p><span data-ttu-id="57495-132">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="57495-132">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="57495-133">Nome da empresa.</span><span class="sxs-lookup"><span data-stu-id="57495-133">Company name.</span></span> <span data-ttu-id="57495-134">Usado apenas por tipos de usuário.</span><span class="sxs-lookup"><span data-stu-id="57495-134">Used only by user types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57495-135">prinEmail</span><span class="sxs-lookup"><span data-stu-id="57495-135">prinEmail</span></span></p></td>
<td><p><span data-ttu-id="57495-136">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="57495-136">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="57495-137">Email.</span><span class="sxs-lookup"><span data-stu-id="57495-137">Email.</span></span> <span data-ttu-id="57495-138">Usado apenas por tipos de usuário.</span><span class="sxs-lookup"><span data-stu-id="57495-138">Used only by user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57495-139">prinADPath</span><span class="sxs-lookup"><span data-stu-id="57495-139">prinADPath</span></span></p></td>
<td><p><span data-ttu-id="57495-140">nvarchar (384)</span><span class="sxs-lookup"><span data-stu-id="57495-140">nvarchar (384)</span></span></p></td>
<td><p><span data-ttu-id="57495-141">Nome do domínio do objeto do Active Directory que a entidade de segurança é uma versão em cache de.</span><span class="sxs-lookup"><span data-stu-id="57495-141">Domain name of the Active Directory object that the principal is a cached version of.</span></span> <span data-ttu-id="57495-142">Pode ser NULL para tipos que não sejam objetos do Active Directory (como usuários do sistema).</span><span class="sxs-lookup"><span data-stu-id="57495-142">Can be Null for types that are not Active Directory objects (such as system users).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57495-143">prinADUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="57495-143">prinADUserPrincipalName</span></span></p></td>
<td><p><span data-ttu-id="57495-144">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="57495-144">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="57495-145">Nome UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="57495-145">User’s user principal name (UPN).</span></span> <span data-ttu-id="57495-146">Usado apenas por tipos de usuário regulares.</span><span class="sxs-lookup"><span data-stu-id="57495-146">Used only by regular user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57495-147">prinDisabled</span><span class="sxs-lookup"><span data-stu-id="57495-147">prinDisabled</span></span></p></td>
<td><p><span data-ttu-id="57495-148">smallint, não nulo</span><span class="sxs-lookup"><span data-stu-id="57495-148">smallint, not null</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="57495-149">0: a entidade de segurança está ativa.</span><span class="sxs-lookup"><span data-stu-id="57495-149">0: Principal is active.</span></span></p></li>
<li><p><span data-ttu-id="57495-150">1: o principal está desabilitado porque as funcionalidades SIP do usuário estão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="57495-150">1: Principal is disabled because user’s SIP capabilities are disabled.</span></span></p></li>
<li><p><span data-ttu-id="57495-151">2: o principal é excluído porque o objeto do anúncio associado foi excluído.</span><span class="sxs-lookup"><span data-stu-id="57495-151">2: Principal is deleted because associated AD object has been deleted.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57495-152">prinTypeID</span><span class="sxs-lookup"><span data-stu-id="57495-152">prinTypeID</span></span></p></td>
<td><p><span data-ttu-id="57495-153">smallint, não nulo</span><span class="sxs-lookup"><span data-stu-id="57495-153">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="57495-154">Tipo de entidade de segurança (da tabela tblPrincipalType).</span><span class="sxs-lookup"><span data-stu-id="57495-154">Principal type (from tblPrincipalType table).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57495-155">prinPoolID</span><span class="sxs-lookup"><span data-stu-id="57495-155">prinPoolID</span></span></p></td>
<td><p><span data-ttu-id="57495-156">Núm</span><span class="sxs-lookup"><span data-stu-id="57495-156">Int</span></span></p></td>
<td><p><span data-ttu-id="57495-157">Atribuição de pool do Lync para a entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="57495-157">Lync pool assignment for the principal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57495-158">prinPolicyID</span><span class="sxs-lookup"><span data-stu-id="57495-158">prinPolicyID</span></span></p></td>
<td><p><span data-ttu-id="57495-159">Núm</span><span class="sxs-lookup"><span data-stu-id="57495-159">Int</span></span></p></td>
<td><p><span data-ttu-id="57495-160">Valor da política do servidor de chat persistente para o usuário, se a política de tipo de marca estiver presente.</span><span class="sxs-lookup"><span data-stu-id="57495-160">Persistent Chat Server policy value for user, if tag type policy is present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57495-161">prinAddedBy</span><span class="sxs-lookup"><span data-stu-id="57495-161">prinAddedBy</span></span></p></td>
<td><p><span data-ttu-id="57495-162">int</span><span class="sxs-lookup"><span data-stu-id="57495-162">int</span></span></p></td>
<td><p><span data-ttu-id="57495-163">ID da entidade de segurança do criador.</span><span class="sxs-lookup"><span data-stu-id="57495-163">Principal ID of the creator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57495-164">prinAddedOn</span><span class="sxs-lookup"><span data-stu-id="57495-164">prinAddedOn</span></span></p></td>
<td><p><span data-ttu-id="57495-165">bigint, e não nulo</span><span class="sxs-lookup"><span data-stu-id="57495-165">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="57495-166">Carimbo de data/hora para a hora da criação.</span><span class="sxs-lookup"><span data-stu-id="57495-166">Time stamp for the creation time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57495-167">prinUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="57495-167">prinUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="57495-168">int</span><span class="sxs-lookup"><span data-stu-id="57495-168">int</span></span></p></td>
<td><p><span data-ttu-id="57495-169">ID da entidade de segurança que atualizou pela última vez.</span><span class="sxs-lookup"><span data-stu-id="57495-169">ID of the principal that last updated this.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57495-170">prinUpdatedOn</span><span class="sxs-lookup"><span data-stu-id="57495-170">prinUpdatedOn</span></span></p></td>
<td><p><span data-ttu-id="57495-171">bigint, e não nulo</span><span class="sxs-lookup"><span data-stu-id="57495-171">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="57495-172">Carimbo de data/hora para a última atualização.</span><span class="sxs-lookup"><span data-stu-id="57495-172">Time stamp for the last update.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57495-173">prinVerifiedOn</span><span class="sxs-lookup"><span data-stu-id="57495-173">prinVerifiedOn</span></span></p></td>
<td><p><span data-ttu-id="57495-174">DateTime, não nulo</span><span class="sxs-lookup"><span data-stu-id="57495-174">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="57495-175">Data e hora da última atualização de sincronização do Active Directory para a entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="57495-175">Date and time of the last Active Directory Sync refresh for the principal.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="57495-176">As</span><span class="sxs-lookup"><span data-stu-id="57495-176">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57495-177">Coluna</span><span class="sxs-lookup"><span data-stu-id="57495-177">Column</span></span></th>
<th><span data-ttu-id="57495-178">Descrição</span><span class="sxs-lookup"><span data-stu-id="57495-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57495-179">multiimprimir</span><span class="sxs-lookup"><span data-stu-id="57495-179">prinID</span></span></p></td>
<td><p><span data-ttu-id="57495-180">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="57495-180">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57495-181">prinTypeID</span><span class="sxs-lookup"><span data-stu-id="57495-181">prinTypeID</span></span></p></td>
<td><p><span data-ttu-id="57495-182">Chave estrangeira com Lookup na tabela tblPrincipalType. ptypeID.</span><span class="sxs-lookup"><span data-stu-id="57495-182">Foreign key with lookup in tblPrincipalType.ptypeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="57495-183">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="57495-183">


</div>

<span> </span>

</div>

</div>

</span></span></div>

