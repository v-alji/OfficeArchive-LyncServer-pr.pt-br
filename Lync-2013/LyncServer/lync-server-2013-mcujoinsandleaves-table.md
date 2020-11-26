---
title: 'Lync Server 2013: Tabela McuJoinsAndLeaves'
description: 'Lync Server 2013: McuJoinsAndLeaves Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: McuJoinsAndLeaves table
ms:assetid: 4e073366-0b5d-45b4-a3f6-d63dd5fd9f25
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398316(v=OCS.15)
ms:contentKeyID: 48184115
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee7d9473892ac357dcefd80b0d52382c5dd7d930
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425749"
---
# <a name="mcujoinsandleaves-table-in-lync-server-2013"></a><span data-ttu-id="542bb-103">Tabela McuJoinsAndLeaves no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="542bb-103">McuJoinsAndLeaves table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="542bb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="542bb-104">

<span> </span></span></span>

<span data-ttu-id="542bb-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="542bb-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="542bb-106">Cada registro desta tabela contém detalhes da chamada sobre uma combinação de um servidor de ingresso ou de saída e conferência do usuário.</span><span class="sxs-lookup"><span data-stu-id="542bb-106">Each record in this table contains call details about one combination of a user join or leave and conferencing server.</span></span> <span data-ttu-id="542bb-107">Por exemplo, se um usuário ingressar em uma conferência que inclui a conferência da Web e os elementos de áudio/vídeo, um registro seria criado para a sua associação de Webconferência do usuário e outro registro será criado para a reunião de conferência de áudio/vídeo do usuário.</span><span class="sxs-lookup"><span data-stu-id="542bb-107">For example, if a user joins a conference that includes web conferencing and audio/video elements, one record would be created for that user’s web conferencing join, and another record would be created for the user’s audio/video conferencing join.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="542bb-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="542bb-108">Column</span></span></th>
<th><span data-ttu-id="542bb-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="542bb-109">Data Type</span></span></th>
<th><span data-ttu-id="542bb-110">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="542bb-110">Key/Index</span></span></th>
<th><span data-ttu-id="542bb-111">Detalhes</span><span class="sxs-lookup"><span data-stu-id="542bb-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="542bb-112"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="542bb-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="542bb-113">datetime</span><span class="sxs-lookup"><span data-stu-id="542bb-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="542bb-114">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="542bb-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="542bb-115">Hora da ocorrência da conferência.</span><span class="sxs-lookup"><span data-stu-id="542bb-115">Time of conference instance.</span></span> <span data-ttu-id="542bb-116">Usado em conjunto com <strong>SessionIdSeq</strong> para identificar uma instância de conferência de maneira exclusiva.</span><span class="sxs-lookup"><span data-stu-id="542bb-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="542bb-117">Consulte a <a href="lync-server-2013-conferences-table.md">tabela conferências no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="542bb-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="542bb-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="542bb-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="542bb-119">int</span><span class="sxs-lookup"><span data-stu-id="542bb-119">int</span></span></p></td>
<td><p><span data-ttu-id="542bb-120">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="542bb-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="542bb-121">Número de identificação para identificar a instância de conferência.</span><span class="sxs-lookup"><span data-stu-id="542bb-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="542bb-122">Usado em conjunto com a <strong>identificação_da_sessãotime</strong> para identificar exclusivamente uma instância de conferência.</span><span class="sxs-lookup"><span data-stu-id="542bb-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="542bb-123">Consulte a <a href="lync-server-2013-conferences-table.md">tabela conferências no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="542bb-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="542bb-124"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="542bb-124"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="542bb-125">int</span><span class="sxs-lookup"><span data-stu-id="542bb-125">int</span></span></p></td>
<td><p><span data-ttu-id="542bb-126">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="542bb-126">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="542bb-127">Número exclusivo que identifica esse usuário.</span><span class="sxs-lookup"><span data-stu-id="542bb-127">Unique number identifying this user.</span></span> <span data-ttu-id="542bb-128">Consulte a <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="542bb-128">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="542bb-129"><strong>McuUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="542bb-129"><strong>McuUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="542bb-130">int</span><span class="sxs-lookup"><span data-stu-id="542bb-130">int</span></span></p></td>
<td><p><span data-ttu-id="542bb-131">Primária</span><span class="sxs-lookup"><span data-stu-id="542bb-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="542bb-132">Se um usuário estiver conectado em vários computadores ou dispositivos de uma vez, o McuUserInstance identifica exclusivamente a combinação de usuário/dispositivo.</span><span class="sxs-lookup"><span data-stu-id="542bb-132">If a user is logged on at multiple computers or devices at once, McuUserInstance uniquely identifies the user/device combination.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="542bb-133"><strong>IsFromPstn</strong></span><span class="sxs-lookup"><span data-stu-id="542bb-133"><strong>IsFromPstn</strong></span></span></p></td>
<td><p><span data-ttu-id="542bb-134">bit</span><span class="sxs-lookup"><span data-stu-id="542bb-134">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="542bb-135">Se o usuário está ingressando de uma PSTN ou não.</span><span class="sxs-lookup"><span data-stu-id="542bb-135">Whether the user is joining from a PSTN or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="542bb-136"><strong>McuId</strong></span><span class="sxs-lookup"><span data-stu-id="542bb-136"><strong>McuId</strong></span></span></p></td>
<td><p><span data-ttu-id="542bb-137">int</span><span class="sxs-lookup"><span data-stu-id="542bb-137">int</span></span></p></td>
<td><p><span data-ttu-id="542bb-138">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="542bb-138">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="542bb-139">Número exclusivo que identifica esse servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="542bb-139">Unique number identifying this conferencing server.</span></span> <span data-ttu-id="542bb-140">Consulte a <a href="lync-server-2013-mcus-table.md">tabela MCUs no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="542bb-140">See the <a href="lync-server-2013-mcus-table.md">Mcus table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="542bb-141"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="542bb-141"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="542bb-142">datetime</span><span class="sxs-lookup"><span data-stu-id="542bb-142">datetime</span></span></p></td>
<td><p><span data-ttu-id="542bb-143">Exterior</span><span class="sxs-lookup"><span data-stu-id="542bb-143">Foreign</span></span></p></td>
<td><p><span data-ttu-id="542bb-144">Tempo de solicitação de sessão.</span><span class="sxs-lookup"><span data-stu-id="542bb-144">Time of session request.</span></span> <span data-ttu-id="542bb-145">Usado em conjunto com o <strong>SessionIdSeq</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="542bb-145">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="542bb-146">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="542bb-146">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="542bb-147"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="542bb-147"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="542bb-148">int</span><span class="sxs-lookup"><span data-stu-id="542bb-148">int</span></span></p></td>
<td><p><span data-ttu-id="542bb-149">Exterior</span><span class="sxs-lookup"><span data-stu-id="542bb-149">Foreign</span></span></p></td>
<td><p><span data-ttu-id="542bb-150">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="542bb-150">ID number to identify the session.</span></span> <span data-ttu-id="542bb-151">Usado em conjunto com a <strong>identificação_da_sessãotime</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="542bb-151">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="542bb-152">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="542bb-152">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="542bb-153"><strong>Userjointime</strong></span><span class="sxs-lookup"><span data-stu-id="542bb-153"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="542bb-154">datetime</span><span class="sxs-lookup"><span data-stu-id="542bb-154">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="542bb-155">A hora em que este usuário entra neste servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="542bb-155">The time this user joins this conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="542bb-156"><strong>Userleavetime</strong></span><span class="sxs-lookup"><span data-stu-id="542bb-156"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="542bb-157">datetime</span><span class="sxs-lookup"><span data-stu-id="542bb-157">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="542bb-158">O horário em que este usuário sai deste servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="542bb-158">The time this user leaves this conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="542bb-159"><strong>ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="542bb-159"><strong>ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="542bb-160">int</span><span class="sxs-lookup"><span data-stu-id="542bb-160">int</span></span></p></td>
<td><p><span data-ttu-id="542bb-161">Exterior</span><span class="sxs-lookup"><span data-stu-id="542bb-161">Foreign</span></span></p></td>
<td><p><span data-ttu-id="542bb-162">Identificador que especifica o número da versão do software cliente usado na conferência.</span><span class="sxs-lookup"><span data-stu-id="542bb-162">Identifier that specifies the version number of the client software use in the conference.</span></span> <span data-ttu-id="542bb-163">Consulte a <a href="lync-server-2013-clientversions-table.md">tabela ClientVersions no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="542bb-163">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="542bb-164">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="542bb-164">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="542bb-165">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="542bb-165">


</div>

<span> </span>

</div>

</div>

</span></span></div>

