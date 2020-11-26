---
title: 'Lync Server 2013: modo de exibição McuJoinsAndLeaves'
description: 'Lync Server 2013: modo de exibição McuJoinsAndLeaves.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: McuJoinsAndLeaves view
ms:assetid: 6f00b8e7-b8b6-4657-ac5e-d8a571806ae2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688088(v=OCS.15)
ms:contentKeyID: 49733687
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f7f2f51c340d5bd4824a6e8eff1a0da172a758c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425728"
---
# <a name="mcujoinsandleaves-view-in-lync-server-2013"></a><span data-ttu-id="e01c0-103">Exibição McuJoinsAndLeaves no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e01c0-103">McuJoinsAndLeaves view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e01c0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e01c0-104">

<span> </span></span></span>

<span data-ttu-id="e01c0-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="e01c0-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="e01c0-106">A exibição McuJoinsAndLeaves armazena informações sobre como os usuários unem e deixam informações para um servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="e01c0-106">The McuJoinsAndLeaves view stores information about users join and leave information for one conference server.</span></span> <span data-ttu-id="e01c0-107">Cada registro nesse modo de exibição contém detalhes da chamada sobre uma combinação de um servidor de ingresso ou de saída e conferência do usuário.</span><span class="sxs-lookup"><span data-stu-id="e01c0-107">Each record in this view contains call details about one combination of a user join or leave and conferencing server.</span></span> <span data-ttu-id="e01c0-108">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e01c0-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e01c0-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="e01c0-109">Column</span></span></th>
<th><span data-ttu-id="e01c0-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e01c0-110">Data Type</span></span></th>
<th><span data-ttu-id="e01c0-111">Detalhes</span><span class="sxs-lookup"><span data-stu-id="e01c0-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e01c0-112"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-113">datetime</span><span class="sxs-lookup"><span data-stu-id="e01c0-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="e01c0-114">Hora da ocorrência da conferência.</span><span class="sxs-lookup"><span data-stu-id="e01c0-114">Time of conference instance.</span></span> <span data-ttu-id="e01c0-115">Usado em conjunto com SessionIdSeq para identificar uma instância de conferência de maneira exclusiva.</span><span class="sxs-lookup"><span data-stu-id="e01c0-115">Used in conjunction with SessionIdSeq to uniquely identify a conference instance.</span></span> <span data-ttu-id="e01c0-116">Consulte a <a href="lync-server-2013-conferences-table.md">tabela conferências no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e01c0-116">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e01c0-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-118">int</span><span class="sxs-lookup"><span data-stu-id="e01c0-118">int</span></span></p></td>
<td><p><span data-ttu-id="e01c0-119">Número de identificação para identificar a instância de conferência.</span><span class="sxs-lookup"><span data-stu-id="e01c0-119">ID number to identify the conference instance.</span></span> <span data-ttu-id="e01c0-120">Usado em conjunto com a Identificação_da_sessãotime para identificar exclusivamente uma instância de conferência.</span><span class="sxs-lookup"><span data-stu-id="e01c0-120">Used in conjunction with SessionIdTime to uniquely identify a conference instance.</span></span> <span data-ttu-id="e01c0-121">Consulte a <a href="lync-server-2013-conferences-table.md">tabela conferências no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e01c0-121">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e01c0-122"><strong>McuUri</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-122"><strong>McuUri</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-123">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e01c0-123">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e01c0-124">O URI do servidor de conferência ao qual o usuário se conectou.</span><span class="sxs-lookup"><span data-stu-id="e01c0-124">The URI of the conferencing server that the user connected to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e01c0-125"><strong>McuUriType</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-125"><strong>McuUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e01c0-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e01c0-127">O URI do servidor de conferência ao qual o usuário se conectou.</span><span class="sxs-lookup"><span data-stu-id="e01c0-127">The URI of the conferencing server that the user connected to.</span></span> <span data-ttu-id="e01c0-128">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e01c0-128">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e01c0-129"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-129"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-130">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="e01c0-130">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="e01c0-131">O URI do usuário cujas informações de associação/licença do servidor de conferência foram capturadas.</span><span class="sxs-lookup"><span data-stu-id="e01c0-131">The URI of the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e01c0-132"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-132"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-133">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e01c0-133">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e01c0-134">O tipo de URI do usuário cujas informações de associação/licença do servidor de conferência foram capturadas.</span><span class="sxs-lookup"><span data-stu-id="e01c0-134">The type of URI of the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="e01c0-135">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e01c0-135">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e01c0-136"><strong>Userlocatário</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-136"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-137">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e01c0-137">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e01c0-138">O locatário do usuário cujas informações de associação/licença do servidor de conferência foram capturadas.</span><span class="sxs-lookup"><span data-stu-id="e01c0-138">The tenant of the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="e01c0-139">Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e01c0-139">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e01c0-140"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-140"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e01c0-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e01c0-142">A versão do cliente usada pelo usuário cujas informações de associação/licença do servidor de conferência foram capturadas.</span><span class="sxs-lookup"><span data-stu-id="e01c0-142">The version of client used by the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e01c0-143"><strong>Userclienttype</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-143"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-144">int</span><span class="sxs-lookup"><span data-stu-id="e01c0-144">int</span></span></p></td>
<td><p><span data-ttu-id="e01c0-145">O cliente usado pelo usuário cujas informações de associação/licença do servidor de conferência foram capturadas.</span><span class="sxs-lookup"><span data-stu-id="e01c0-145">The client used by the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="e01c0-146">Consulte a <a href="lync-server-2013-useragentdef-table.md">tabela UserAgentDef no Lync Server 2013</a> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="e01c0-146">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e01c0-147"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-147"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-148">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="e01c0-148">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="e01c0-149">O nome da categoria do cliente usado pelo usuário cujas informações de associação/licença do servidor de conferência foram capturadas.</span><span class="sxs-lookup"><span data-stu-id="e01c0-149">The name of the category of the client used by the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e01c0-150"><strong>McuUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-150"><strong>McuUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-151">int</span><span class="sxs-lookup"><span data-stu-id="e01c0-151">int</span></span></p></td>
<td><p><span data-ttu-id="e01c0-152">Identifica exclusivamente a combinação de usuário/dispositivo para usuários conectados simultaneamente a vários dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e01c0-152">Uniquely identifies the user/device combination for users simultaneously logged on to multiple devices.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e01c0-153"><strong>IsUserFromPstn</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-153"><strong>IsUserFromPstn</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-154">bit</span><span class="sxs-lookup"><span data-stu-id="e01c0-154">bit</span></span></p></td>
<td><p><span data-ttu-id="e01c0-155">Bit que representa se o usuário é um usuário interno ou não.</span><span class="sxs-lookup"><span data-stu-id="e01c0-155">Bit that represents whether the user is an internal user or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e01c0-156"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-156"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-157">datetime</span><span class="sxs-lookup"><span data-stu-id="e01c0-157">datetime</span></span></p></td>
<td><p><span data-ttu-id="e01c0-158">Tempo de solicitação de sessão.</span><span class="sxs-lookup"><span data-stu-id="e01c0-158">Time of session request.</span></span> <span data-ttu-id="e01c0-159">Usado em conjunto com o SessionIdSeq para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="e01c0-159">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="e01c0-160">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e01c0-160">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e01c0-161"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-161"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-162">int</span><span class="sxs-lookup"><span data-stu-id="e01c0-162">int</span></span></p></td>
<td><p><span data-ttu-id="e01c0-163">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="e01c0-163">ID number to identify the session.</span></span> <span data-ttu-id="e01c0-164">Usado em conjunto com a Identificação_da_sessãotime para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="e01c0-164">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="e01c0-165">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e01c0-165">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e01c0-166"><strong>Caixa de diálogo</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-166"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-167">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="e01c0-167">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="e01c0-168">ID da caixa de diálogo SIP da sessão.</span><span class="sxs-lookup"><span data-stu-id="e01c0-168">SIP dialog ID of the session.</span></span> <span data-ttu-id="e01c0-169">O formato é: caixa de diálogo; de-marca; para-marca.</span><span class="sxs-lookup"><span data-stu-id="e01c0-169">The format is: dialog;from-tag;to-tag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e01c0-170"><strong>Userjointime</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-170"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-171">datetime</span><span class="sxs-lookup"><span data-stu-id="e01c0-171">datetime</span></span></p></td>
<td><p><span data-ttu-id="e01c0-172">Vez que o usuário ingressou no servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="e01c0-172">Time the user joined the conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e01c0-173"><strong>Userleavetime</strong></span><span class="sxs-lookup"><span data-stu-id="e01c0-173"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e01c0-174">datetime</span><span class="sxs-lookup"><span data-stu-id="e01c0-174">datetime</span></span></p></td>
<td><p><span data-ttu-id="e01c0-175">Vez que o usuário saiu do servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="e01c0-175">Time the user left the conferencing server.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e01c0-176">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e01c0-176">


</div>

<span> </span>

</div>

</div>

</span></span></div>

