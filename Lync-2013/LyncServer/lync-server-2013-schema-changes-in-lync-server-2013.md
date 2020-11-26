---
title: 'Lync Server 2013: alterações de esquema no Lync Server 2013'
description: 'Lync Server 2013: alterações de esquema no Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema changes in Lync Server 2013
ms:assetid: d760cb93-77d4-4d64-adb7-416b808f36f8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398944(v=OCS.15)
ms:contentKeyID: 48185575
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9e914de48ace80fd2611f2d05b092894b11c534a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444921"
---
# <a name="schema-changes-in-lync-server-2013"></a><span data-ttu-id="5aed9-103">Alterações de esquema no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5aed9-103">Schema changes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5aed9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5aed9-104">

<span> </span></span></span>

<span data-ttu-id="5aed9-105">_**Tópico da última modificação:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="5aed9-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="5aed9-106">Antes de implantar e operar o Lync Server 2013, você deve preparar os serviços de domínio Active Directory estendendo o esquema.</span><span class="sxs-lookup"><span data-stu-id="5aed9-106">Before you deploy and operate Lync Server 2013, you must prepare Active Directory Domain Services by extending the schema.</span></span> <span data-ttu-id="5aed9-107">As extensões de esquema adicionam as classes e os atributos necessários para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5aed9-107">The schema extensions add the classes and attributes that are required by Lync Server 2013.</span></span>

<span data-ttu-id="5aed9-108">O Lync Server 2013 requer várias novas classes e atributos e modifica algumas classes e atributos existentes.</span><span class="sxs-lookup"><span data-stu-id="5aed9-108">Lync Server 2013 requires several new classes and attributes and modifies some existing classes and attributes.</span></span> <span data-ttu-id="5aed9-109">Além disso, muitas informações de configuração para o Lync Server 2013 são armazenadas no repositório de gerenciamento central, em vez de no AD DS, como nas versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="5aed9-109">In addition, much configuration information for Lync Server 2013 is stored in the Central Management store instead of in AD DS as in previous versions.</span></span> <span data-ttu-id="5aed9-110">As informações a seguir ainda são armazenadas no AD DS no Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="5aed9-110">The following information is still stored in AD DS in Lync Server 2013:</span></span>

  - <span data-ttu-id="5aed9-111">**Extensões de esquema**:</span><span class="sxs-lookup"><span data-stu-id="5aed9-111">**Schema extensions**:</span></span>
    
      - <span data-ttu-id="5aed9-112">Extensões de objetos de usuário</span><span class="sxs-lookup"><span data-stu-id="5aed9-112">User object extensions</span></span>
    
      - <span data-ttu-id="5aed9-113">Extensões para o Office Communications Server 2007 e o Office Communications Server 2007 R2 classes para manter a compatibilidade com versões anteriores com suporte</span><span class="sxs-lookup"><span data-stu-id="5aed9-113">Extensions for Office Communications Server 2007 and Office Communications Server 2007 R2 classes to maintain backward compatibility with supported previous versions</span></span>

<!-- end list -->

  - <span data-ttu-id="5aed9-114">**Dados** (armazenados no esquema estendido do Lync Server e em classes de esquema existentes):</span><span class="sxs-lookup"><span data-stu-id="5aed9-114">**Data** (stored in Lync Server extended schema and in existing schema classes):</span></span>
    
      - <span data-ttu-id="5aed9-115">URI (Uniform Resource Identifier) do usuário SIP e outras configurações do usuário</span><span class="sxs-lookup"><span data-stu-id="5aed9-115">User SIP Uniform Resource Identifier (URI) and other user settings</span></span>
    
      - <span data-ttu-id="5aed9-116">Objetos de contato para aplicativos como o assistente de grupo de resposta e conferência</span><span class="sxs-lookup"><span data-stu-id="5aed9-116">Contact objects for applications such as Response Group and Conferencing Attendant</span></span>
    
      - <span data-ttu-id="5aed9-117">Um ponteiro para o repositório de gerenciamento central</span><span class="sxs-lookup"><span data-stu-id="5aed9-117">A pointer to the Central Management store</span></span>
    
      - <span data-ttu-id="5aed9-118">Conta de autenticação Kerberos (um objeto de computador opcional)</span><span class="sxs-lookup"><span data-stu-id="5aed9-118">Kerberos Authentication Account (an optional computer object)</span></span>

<span data-ttu-id="5aed9-119">Este tópico descreve as alterações de esquema do Active Directory exigidas pelo Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5aed9-119">This topic describes the Active Directory schema changes required by Lync Server 2013.</span></span> <span data-ttu-id="5aed9-120">Ele não descreve as alterações de esquema que foram introduzidas por versões anteriores do Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="5aed9-120">It does not describe schema changes that were introduced by previous versions of Office Communications Server.</span></span> <span data-ttu-id="5aed9-121">Para obter uma lista de classes e suas descrições, consulte [classes de esquema e descrições no Lync Server 2013](lync-server-2013-schema-classes-and-descriptions.md).</span><span class="sxs-lookup"><span data-stu-id="5aed9-121">For a list of classes and their descriptions, see [Schema classes and descriptions in Lync Server 2013](lync-server-2013-schema-classes-and-descriptions.md).</span></span> <span data-ttu-id="5aed9-122">Para obter uma lista de atributos e suas descrições, consulte [atributos e descrições do esquema no Lync Server 2013](lync-server-2013-schema-attributes-and-descriptions.md).</span><span class="sxs-lookup"><span data-stu-id="5aed9-122">For a list of attributes and their descriptions, see [Schema attributes and descriptions in Lync Server 2013](lync-server-2013-schema-attributes-and-descriptions.md).</span></span> <span data-ttu-id="5aed9-123">Para obter uma lista de classes com os atributos que elas podem conter, consulte [atributos de esquema por classe no Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span><span class="sxs-lookup"><span data-stu-id="5aed9-123">For a list of classes with the attributes they may contain, see [Schema attributes by class in Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span></span>

<span data-ttu-id="5aed9-124">O prefixo msRTCSIP identifica classes e atributos que são específicos do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5aed9-124">The msRTCSIP prefix identifies classes and attributes that are specific to Lync Server.</span></span>

<div>

## <a name="new-active-directory-attributes"></a><span data-ttu-id="5aed9-125">Novos atributos do Active Directory</span><span class="sxs-lookup"><span data-stu-id="5aed9-125">New Active Directory Attributes</span></span>

<span data-ttu-id="5aed9-126">A tabela a seguir descreve os atributos do Active Directory que são adicionados pelo Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5aed9-126">The following table describes the Active Directory attributes that are added by Lync Server 2013.</span></span>

### <a name="attributes-added-by-lync-server-2013"></a><span data-ttu-id="5aed9-127">Atributos adicionados pelo Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5aed9-127">Attributes Added by Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5aed9-128">Atributo</span><span class="sxs-lookup"><span data-stu-id="5aed9-128">Attribute</span></span></th>
<th><span data-ttu-id="5aed9-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="5aed9-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5aed9-130">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="5aed9-130">msExchUserHoldPolicies</span></span></p></td>
<td><p><span data-ttu-id="5aed9-131">Esse atributo de vários valores contém identificadores para políticas de retenção que se aplicam ao usuário.</span><span class="sxs-lookup"><span data-stu-id="5aed9-131">This multi-value attribute holds identifiers for hold policies that apply to the user.</span></span> <span data-ttu-id="5aed9-132">As políticas de retenção preservam os itens da caixa de correio para o usuário durante o período de espera.</span><span class="sxs-lookup"><span data-stu-id="5aed9-132">Hold policies preserve mailbox items for the user for the duration of the hold.</span></span> <span data-ttu-id="5aed9-133">Esse atributo é compartilhado com o Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="5aed9-133">This attribute is shared with Exchange 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aed9-134">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="5aed9-134">msRTCSIP-UserRoutingGroupId</span></span></p></td>
<td><p><span data-ttu-id="5aed9-135">Esta é a ID do grupo de roteamento SIP.</span><span class="sxs-lookup"><span data-stu-id="5aed9-135">This is the SIP routing group ID.</span></span> <span data-ttu-id="5aed9-136">Os usuários no mesmo grupo serão registrados no mesmo servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="5aed9-136">Users in the same group will register to the same Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aed9-137">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="5aed9-137">msRTCSIP-MirrorBackEndServer</span></span></p></td>
<td><p><span data-ttu-id="5aed9-138">Esse atributo é usado para armazenar o back-end do SQL Server espelhado usado pelo pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="5aed9-138">This attribute is used to store the mirrored SQL Server backend used by the Front End pool.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="modified-active-directory-classes"></a><span data-ttu-id="5aed9-139">Classes modificadas do Active Directory</span><span class="sxs-lookup"><span data-stu-id="5aed9-139">Modified Active Directory Classes</span></span>

<span data-ttu-id="5aed9-140">A tabela a seguir descreve as classes do Active Directory modificadas pelo Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5aed9-140">The following table describes the Active Directory classes that are modified by Lync Server 2013.</span></span>

### <a name="classes-modified-by-lync-server-2013"></a><span data-ttu-id="5aed9-141">Classes modificadas pelo Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5aed9-141">Classes Modified by Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5aed9-142">Classe</span><span class="sxs-lookup"><span data-stu-id="5aed9-142">Class</span></span></th>
<th><span data-ttu-id="5aed9-143">Alteração</span><span class="sxs-lookup"><span data-stu-id="5aed9-143">Change</span></span></th>
<th><span data-ttu-id="5aed9-144">Classe ou atributo</span><span class="sxs-lookup"><span data-stu-id="5aed9-144">Class or Attribute</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5aed9-145">Usuário</span><span class="sxs-lookup"><span data-stu-id="5aed9-145">User</span></span></p></td>
<td><p><span data-ttu-id="5aed9-146">Adicionar: mayContain</span><span class="sxs-lookup"><span data-stu-id="5aed9-146">add: mayContain</span></span></p>
<p><span data-ttu-id="5aed9-147">Adicionar: mayContain</span><span class="sxs-lookup"><span data-stu-id="5aed9-147">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="5aed9-148">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="5aed9-148">ProxyAddresses</span></span></p>
<p><span data-ttu-id="5aed9-149">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="5aed9-149">msRTCSIP-UserRoutingGroupId</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aed9-150">Entrando</span><span class="sxs-lookup"><span data-stu-id="5aed9-150">Contact</span></span></p></td>
<td><p><span data-ttu-id="5aed9-151">Adicionar: mayContain</span><span class="sxs-lookup"><span data-stu-id="5aed9-151">add: mayContain</span></span></p>
<p><span data-ttu-id="5aed9-152">Adicionar: mayContain</span><span class="sxs-lookup"><span data-stu-id="5aed9-152">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="5aed9-153">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="5aed9-153">ProxyAddresses</span></span></p>
<p><span data-ttu-id="5aed9-154">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="5aed9-154">msRTCSIP-UserRoutingGroupId</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aed9-155">Mail-Recipient</span><span class="sxs-lookup"><span data-stu-id="5aed9-155">Mail-Recipient</span></span></p></td>
<td><p><span data-ttu-id="5aed9-156">Adicionar: mayContain</span><span class="sxs-lookup"><span data-stu-id="5aed9-156">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="5aed9-157">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="5aed9-157">msExchUserHoldPolicies</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aed9-158">msRTCSIP-GlobalTopologySetting</span><span class="sxs-lookup"><span data-stu-id="5aed9-158">msRTCSIP-GlobalTopologySetting</span></span></p></td>
<td><p><span data-ttu-id="5aed9-159">Adicionar: mayContain</span><span class="sxs-lookup"><span data-stu-id="5aed9-159">add: mayContain</span></span></p></td>
<td><p><span data-ttu-id="5aed9-160">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="5aed9-160">msRTCSIP-MirrorBackEndServer</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5aed9-161">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5aed9-161">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

