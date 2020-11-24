---
title: 'Lync Server 2013: tblPrincipalType'
description: 'Lync Server 2013: tblPrincipalType.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalType
ms:assetid: 32e1c1d6-80f4-4624-bf4e-b4c77d3982fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558633(v=OCS.15)
ms:contentKeyID: 48183787
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba0f607d4499b54b16d7ecf8a4e7de603e874788
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389747"
---
# <a name="tblprincipaltype-in-lync-server-2013"></a><span data-ttu-id="8c6ed-103">tblPrincipalType no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c6ed-103">tblPrincipalType in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8c6ed-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8c6ed-104">

<span> </span></span></span>

<span data-ttu-id="8c6ed-105">_**Tópico da última modificação:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="8c6ed-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="8c6ed-106">tblPrincipalType contém tipos principais para categorizar o que está na tabela tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-106">tblPrincipalType contains principal types to categorize what is in the tblPrincipal table.</span></span>

### <a name="columns"></a><span data-ttu-id="8c6ed-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="8c6ed-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c6ed-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="8c6ed-108">Column</span></span></th>
<th><span data-ttu-id="8c6ed-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c6ed-109">Type</span></span></th>
<th><span data-ttu-id="8c6ed-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c6ed-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c6ed-111">ptypeID</span><span class="sxs-lookup"><span data-stu-id="8c6ed-111">ptypeID</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-112">smallint, não nulo</span><span class="sxs-lookup"><span data-stu-id="8c6ed-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-113">ID do tipo principal.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-113">Principal type ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6ed-114">ptypeDesc</span><span class="sxs-lookup"><span data-stu-id="8c6ed-114">ptypeDesc</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-115">nvarchar (256), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="8c6ed-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-116">Descrição do tipo.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-116">Description of the type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6ed-117">ptypeIsSystemUser</span><span class="sxs-lookup"><span data-stu-id="8c6ed-117">ptypeIsSystemUser</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-118">bit, e não nulo</span><span class="sxs-lookup"><span data-stu-id="8c6ed-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-119">Verdadeiro se o tipo corresponder às entidades de segurança usadas para fins internos.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-119">True if the type corresponds to the principals that are used for internal purposes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6ed-120">ptypeIsUser</span><span class="sxs-lookup"><span data-stu-id="8c6ed-120">ptypeIsUser</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-121">bit, e não nulo</span><span class="sxs-lookup"><span data-stu-id="8c6ed-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-122">Verdadeiro se o tipo for um tipo de usuário.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-122">True if the type is a user type.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="8c6ed-123">Chave</span><span class="sxs-lookup"><span data-stu-id="8c6ed-123">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c6ed-124">Coluna</span><span class="sxs-lookup"><span data-stu-id="8c6ed-124">Column</span></span></th>
<th><span data-ttu-id="8c6ed-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c6ed-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c6ed-126">ptypeID</span><span class="sxs-lookup"><span data-stu-id="8c6ed-126">ptypeID</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-127">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-127">Primary key.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="principal-values"></a><span data-ttu-id="8c6ed-128">Valores principais</span><span class="sxs-lookup"><span data-stu-id="8c6ed-128">Principal Values</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c6ed-129">ID</span><span class="sxs-lookup"><span data-stu-id="8c6ed-129">ID</span></span></th>
<th><span data-ttu-id="8c6ed-130">Função</span><span class="sxs-lookup"><span data-stu-id="8c6ed-130">Role</span></span></th>
<th><span data-ttu-id="8c6ed-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c6ed-131">Description</span></span></th>
<th><span data-ttu-id="8c6ed-132">Usuário</span><span class="sxs-lookup"><span data-stu-id="8c6ed-132">User</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c6ed-133">1</span><span class="sxs-lookup"><span data-stu-id="8c6ed-133">1</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-134">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="8c6ed-134">Any</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-135">Entidade de segurança genérica sem tipo conhecido.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-135">Generic principal with no known type.</span></span> <span data-ttu-id="8c6ed-136">Não usado na tabela tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-136">Not used in tblPrincipal table.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6ed-137">2</span><span class="sxs-lookup"><span data-stu-id="8c6ed-137">2</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-138">AnyUser</span><span class="sxs-lookup"><span data-stu-id="8c6ed-138">AnyUser</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-139">Entidade de usuário genérica do tipo de usuário.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-139">Generic principal of user type.</span></span> <span data-ttu-id="8c6ed-140">Não usado na tabela tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-140">Not used in tblPrincipal table.</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-141">Sim</span><span class="sxs-lookup"><span data-stu-id="8c6ed-141">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6ed-142">3</span><span class="sxs-lookup"><span data-stu-id="8c6ed-142">3</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-143">AnyGroup</span><span class="sxs-lookup"><span data-stu-id="8c6ed-143">AnyGroup</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-144">Entidade de segurança genérica com semântica de grupo.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-144">Generic principal with group semantic.</span></span> <span data-ttu-id="8c6ed-145">Não usado na tabela tblPrincipal.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-145">Not used in tblPrincipal table.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6ed-146">4</span><span class="sxs-lookup"><span data-stu-id="8c6ed-146">4</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-147">SystemUser</span><span class="sxs-lookup"><span data-stu-id="8c6ed-147">SystemUser</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-148">Principal usado internamente pelo servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-148">Principal used internally by Persistent Chat Server.</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6ed-149">5</span><span class="sxs-lookup"><span data-stu-id="8c6ed-149">5</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-150">Usuário</span><span class="sxs-lookup"><span data-stu-id="8c6ed-150">User</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-151">Usuário regular.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-151">Regular user.</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-152">Sim</span><span class="sxs-lookup"><span data-stu-id="8c6ed-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6ed-153">8</span><span class="sxs-lookup"><span data-stu-id="8c6ed-153">8</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-154">CLONA</span><span class="sxs-lookup"><span data-stu-id="8c6ed-154">DC</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-155">Controlador de domínio dos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-155">Active Directory Domain Services domain controller.</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6ed-156">9</span><span class="sxs-lookup"><span data-stu-id="8c6ed-156">9</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-157">Grupos</span><span class="sxs-lookup"><span data-stu-id="8c6ed-157">Group</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-158">Grupo de segurança do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-158">Active Directory security group.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6ed-159">254</span><span class="sxs-lookup"><span data-stu-id="8c6ed-159">10</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-160">Pasta</span><span class="sxs-lookup"><span data-stu-id="8c6ed-160">Folder</span></span></p></td>
<td><p><span data-ttu-id="8c6ed-161">Contêiner ou unidade organizacional do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8c6ed-161">Active Directory container or organizational unit.</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="8c6ed-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c6ed-162">See Also</span></span>


[<span data-ttu-id="8c6ed-163">tblPrincipal no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c6ed-163">tblPrincipal in Lync Server 2013</span></span>](lync-server-2013-tblprincipal.md)  
  

<span data-ttu-id="8c6ed-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8c6ed-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

