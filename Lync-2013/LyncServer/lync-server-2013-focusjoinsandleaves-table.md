---
title: 'Lync Server 2013: Tabela FocusJoinsAndLeaves'
description: 'Lync Server 2013: FocusJoinsAndLeaves Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FocusJoinsAndLeaves table
ms:assetid: e6f0212c-67e9-4061-8720-d0296e855991
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399026(v=OCS.15)
ms:contentKeyID: 48185690
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5796de16ed204ce4f33935d937cbaa425d63a67f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428101"
---
# <a name="focusjoinsandleaves-table-in-lync-server-2013"></a><span data-ttu-id="af183-103">Tabela FocusJoinsAndLeaves no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af183-103">FocusJoinsAndLeaves table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="af183-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="af183-104">

<span> </span></span></span>

<span data-ttu-id="af183-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="af183-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="af183-106">Cada registro desta tabela contém as informações de CDR sobre o ingresso de um usuário e as informações de licença de uma conferência.</span><span class="sxs-lookup"><span data-stu-id="af183-106">Each record in this table contains the CDR information about one user’s join and leave information for one conference.</span></span> <span data-ttu-id="af183-107">Cada conferência é representada por um registro por cada vez que um usuário entra e sai da conferência.</span><span class="sxs-lookup"><span data-stu-id="af183-107">Each conference is represented in this table by one record for each time a user joins and leaves the conference.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af183-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="af183-108">Column</span></span></th>
<th><span data-ttu-id="af183-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="af183-109">Data Type</span></span></th>
<th><span data-ttu-id="af183-110">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="af183-110">Key/Index</span></span></th>
<th><span data-ttu-id="af183-111">Detalhes</span><span class="sxs-lookup"><span data-stu-id="af183-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af183-112"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="af183-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="af183-113">datetime</span><span class="sxs-lookup"><span data-stu-id="af183-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="af183-114">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="af183-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="af183-115">Hora da ocorrência da conferência.</span><span class="sxs-lookup"><span data-stu-id="af183-115">Time of conference instance.</span></span> <span data-ttu-id="af183-116">Usado em conjunto com <strong>SessionIdSeq</strong> para identificar uma instância de conferência de maneira exclusiva.</span><span class="sxs-lookup"><span data-stu-id="af183-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="af183-117">Consulte a <a href="lync-server-2013-conferences-table.md">tabela conferências no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="af183-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af183-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="af183-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="af183-119">int</span><span class="sxs-lookup"><span data-stu-id="af183-119">int</span></span></p></td>
<td><p><span data-ttu-id="af183-120">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="af183-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="af183-121">Número de identificação para identificar a instância de conferência.</span><span class="sxs-lookup"><span data-stu-id="af183-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="af183-122">Usado em conjunto com a <strong>identificação_da_sessãotime</strong> para identificar exclusivamente uma instância de conferência.</span><span class="sxs-lookup"><span data-stu-id="af183-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="af183-123">Consulte a <a href="lync-server-2013-conferences-table.md">tabela conferências no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="af183-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af183-124"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="af183-124"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="af183-125">datetime</span><span class="sxs-lookup"><span data-stu-id="af183-125">datetime</span></span></p></td>
<td><p><span data-ttu-id="af183-126">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="af183-126">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="af183-127">Tempo de solicitação de sessão.</span><span class="sxs-lookup"><span data-stu-id="af183-127">Time of session request.</span></span> <span data-ttu-id="af183-128">Usado em conjunto com o <strong>SessionIdSeq</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="af183-128">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="af183-129">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="af183-129">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af183-130"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="af183-130"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="af183-131">int</span><span class="sxs-lookup"><span data-stu-id="af183-131">int</span></span></p></td>
<td><p><span data-ttu-id="af183-132">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="af183-132">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="af183-133">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="af183-133">ID number to identify the session.</span></span> <span data-ttu-id="af183-134">Usado em conjunto com a <strong>identificação_da_sessãotime</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="af183-134">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="af183-135">consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="af183-135">see the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af183-136"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="af183-136"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="af183-137">int</span><span class="sxs-lookup"><span data-stu-id="af183-137">int</span></span></p></td>
<td><p><span data-ttu-id="af183-138">Exterior</span><span class="sxs-lookup"><span data-stu-id="af183-138">Foreign</span></span></p></td>
<td><p><span data-ttu-id="af183-139">Número exclusivo que identifica esse usuário, referenciado pela <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="af183-139">Unique number identifying this user, referenced from the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af183-140"><strong>FocusUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="af183-140"><strong>FocusUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="af183-141">int</span><span class="sxs-lookup"><span data-stu-id="af183-141">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="af183-142">Se um usuário estiver conectado em vários computadores ou dispositivos ao mesmo tempo, o <strong>UserInstance</strong> será usado para identificar exclusivamente a combinação de usuário/dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af183-142">If a user is logged on at multiple computers or devices at the same time, <strong>UserInstance</strong> is used to uniquely identify the user/device combination.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af183-143"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="af183-143"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="af183-144">bit</span><span class="sxs-lookup"><span data-stu-id="af183-144">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="af183-145">Se o usuário está conectado de interno ou não.</span><span class="sxs-lookup"><span data-stu-id="af183-145">Whether the user logged on from internal or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af183-146"><strong>UserRole</strong></span><span class="sxs-lookup"><span data-stu-id="af183-146"><strong>UserRole</strong></span></span></p></td>
<td><p><span data-ttu-id="af183-147">int</span><span class="sxs-lookup"><span data-stu-id="af183-147">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="af183-148">A função deste usuário na conferência, como apresentador ou participante.</span><span class="sxs-lookup"><span data-stu-id="af183-148">This user’s role in the conference, such as Presenter or Attendee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af183-149"><strong>Userjointime</strong></span><span class="sxs-lookup"><span data-stu-id="af183-149"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="af183-150">datetime</span><span class="sxs-lookup"><span data-stu-id="af183-150">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="af183-151">A hora em que este usuário entra na conferência.</span><span class="sxs-lookup"><span data-stu-id="af183-151">The time this user joins the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af183-152"><strong>Userleavetime</strong></span><span class="sxs-lookup"><span data-stu-id="af183-152"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="af183-153">datetime</span><span class="sxs-lookup"><span data-stu-id="af183-153">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="af183-154">A hora em que esse usuário sai da conferência.</span><span class="sxs-lookup"><span data-stu-id="af183-154">The time this user leaves the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af183-155"><strong>ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="af183-155"><strong>ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="af183-156">int</span><span class="sxs-lookup"><span data-stu-id="af183-156">int</span></span></p></td>
<td><p><span data-ttu-id="af183-157">Exterior</span><span class="sxs-lookup"><span data-stu-id="af183-157">Foreign</span></span></p></td>
<td><p><span data-ttu-id="af183-158">Versão do software cliente do usuário, referenciada à <a href="lync-server-2013-clientversions-table.md">tabela ClientVersions no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="af183-158">Version of the user’s client software, referenced to the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af183-159"><strong>Userendpointid</strong></span><span class="sxs-lookup"><span data-stu-id="af183-159"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="af183-160">Identificador</span><span class="sxs-lookup"><span data-stu-id="af183-160">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="af183-161">Identificador global exclusivo (GUID) do ponto de extremidade usado na conferência.</span><span class="sxs-lookup"><span data-stu-id="af183-161">Globally unique identifier (GUID) of the endpoint used in the conference.</span></span></p>
<p><span data-ttu-id="af183-162">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="af183-162">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="af183-163">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="af183-163">


</div>

<span> </span>

</div>

</div>

</span></span></div>

