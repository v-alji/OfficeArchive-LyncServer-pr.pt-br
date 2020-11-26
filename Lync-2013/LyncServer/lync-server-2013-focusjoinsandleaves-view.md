---
title: 'Lync Server 2013: modo de exibição FocusJoinsAndLeaves'
description: 'Lync Server 2013: modo de exibição FocusJoinsAndLeaves.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FocusJoinsAndLeaves view
ms:assetid: 226460ef-766f-4d61-80cb-f332b65a210d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687992(v=OCS.15)
ms:contentKeyID: 49733582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c6f68c44461e378e9ebedce1305ee6b384a7a8a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428102"
---
# <a name="focusjoinsandleaves-view-in-lync-server-2013"></a><span data-ttu-id="c9032-103">Exibição FocusJoinsAndLeaves no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c9032-103">FocusJoinsAndLeaves view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c9032-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c9032-104">

<span> </span></span></span>

<span data-ttu-id="c9032-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="c9032-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="c9032-106">A exibição FocusJoinsAndLeaves armazena informações sobre as informações de ingressar e sair de uma conferência.</span><span class="sxs-lookup"><span data-stu-id="c9032-106">The FocusJoinsAndLeaves view stores information about join and leave information for one conference.</span></span> <span data-ttu-id="c9032-107">Cada conferência é representada por um registro escrito a cada vez que um usuário entra e sai da conferência.</span><span class="sxs-lookup"><span data-stu-id="c9032-107">Each conference is represented in this view by a record written each time a user joins and leaves the conference.</span></span> <span data-ttu-id="c9032-108">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c9032-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9032-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="c9032-109">Column</span></span></th>
<th><span data-ttu-id="c9032-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c9032-110">Data Type</span></span></th>
<th><span data-ttu-id="c9032-111">Detalhes</span><span class="sxs-lookup"><span data-stu-id="c9032-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9032-112"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-113">datetime</span><span class="sxs-lookup"><span data-stu-id="c9032-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="c9032-114">Hora da ocorrência da conferência.</span><span class="sxs-lookup"><span data-stu-id="c9032-114">Time of conference instance.</span></span> <span data-ttu-id="c9032-115">Usado em conjunto com SessionIdSeq para identificar uma instância de conferência de maneira exclusiva.</span><span class="sxs-lookup"><span data-stu-id="c9032-115">Used in conjunction with SessionIdSeq to uniquely identify a conference instance.</span></span> <span data-ttu-id="c9032-116">Consulte a <a href="lync-server-2013-conferences-table.md">tabela conferências no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c9032-116">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9032-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-118">int</span><span class="sxs-lookup"><span data-stu-id="c9032-118">int</span></span></p></td>
<td><p><span data-ttu-id="c9032-119">Número de identificação para identificar a instância de conferência.</span><span class="sxs-lookup"><span data-stu-id="c9032-119">ID number to identify the conference instance.</span></span> <span data-ttu-id="c9032-120">Usado em conjunto com a Identificação_da_sessãotime para identificar exclusivamente uma instância de conferência.</span><span class="sxs-lookup"><span data-stu-id="c9032-120">Used in conjunction with SessionIdTime to uniquely identify a conference instance.</span></span> <span data-ttu-id="c9032-121">Consulte a <a href="lync-server-2013-conferences-table.md">tabela conferências no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c9032-121">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9032-122"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-122"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-123">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="c9032-123">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="c9032-124">URI do usuário cujas informações de associação/licença da conferência foram capturadas.</span><span class="sxs-lookup"><span data-stu-id="c9032-124">URI of the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9032-125"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-125"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c9032-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c9032-127">Tipo de URI do usuário cujas informações de associação/licença de conferência foram capturadas.</span><span class="sxs-lookup"><span data-stu-id="c9032-127">Type of URI of the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="c9032-128">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c9032-128">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9032-129"><strong>Userlocatário</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-129"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-130">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c9032-130">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c9032-131">Locatário do usuário cujas informações de associação/licença da conferência foram capturadas.</span><span class="sxs-lookup"><span data-stu-id="c9032-131">Tenant of the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="c9032-132">Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c9032-132">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9032-133"><strong>Userendpointid</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-133"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-134">identificador</span><span class="sxs-lookup"><span data-stu-id="c9032-134">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="c9032-135">Identificador exclusivo do usuário cujas informações de associação/licença da conferência foram capturadas.</span><span class="sxs-lookup"><span data-stu-id="c9032-135">Unique identifier of the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9032-136"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-136"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-137">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c9032-137">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c9032-138">Versão do cliente usada pelo usuário cujas informações de associação/licença da conferência foram capturadas.</span><span class="sxs-lookup"><span data-stu-id="c9032-138">Version of client used by the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9032-139"><strong>Userclienttype</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-139"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-140">int</span><span class="sxs-lookup"><span data-stu-id="c9032-140">int</span></span></p></td>
<td><p><span data-ttu-id="c9032-141">Cliente usado pelo usuário cujas informações de associação/licença da conferência foram capturadas.</span><span class="sxs-lookup"><span data-stu-id="c9032-141">Client used by the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="c9032-142">Consulte a <a href="lync-server-2013-useragentdef-table.md">tabela UserAgentDef no Lync Server 2013</a> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="c9032-142">See <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9032-143"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-143"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-144">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="c9032-144">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="c9032-145">Nome da categoria do cliente usado pelo usuário cujas informações de associação/licença da conferência foram capturadas.</span><span class="sxs-lookup"><span data-stu-id="c9032-145">Name of the category of the client used by the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9032-146"><strong>FocusUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-146"><strong>FocusUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-147">int</span><span class="sxs-lookup"><span data-stu-id="c9032-147">int</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9032-148"><strong>IsuserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-148"><strong>IsuserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-149">bit</span><span class="sxs-lookup"><span data-stu-id="c9032-149">bit</span></span></p></td>
<td><p><span data-ttu-id="c9032-150">Bit que representa se o usuário é um usuário interno ou não.</span><span class="sxs-lookup"><span data-stu-id="c9032-150">Bit that represents whether the user is an internal user or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9032-151"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-151"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-152">datetime</span><span class="sxs-lookup"><span data-stu-id="c9032-152">datetime</span></span></p></td>
<td><p><span data-ttu-id="c9032-153">Tempo de solicitação de sessão.</span><span class="sxs-lookup"><span data-stu-id="c9032-153">Time of session request.</span></span> <span data-ttu-id="c9032-154">Usado em conjunto com o SessionIdSeq para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="c9032-154">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="c9032-155">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c9032-155">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9032-156"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-156"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-157">int</span><span class="sxs-lookup"><span data-stu-id="c9032-157">int</span></span></p></td>
<td><p><span data-ttu-id="c9032-158">Se um usuário estiver conectado em vários computadores ou dispositivos ao mesmo tempo, o UserInstance será usado para identificar exclusivamente a combinação de usuário/dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9032-158">If a user is logged on at multiple computers or devices at the same time, UserInstance is used to uniquely identify the user/device combination.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9032-159"><strong>Caixa de diálogo</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-159"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-160">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="c9032-160">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="c9032-161">ID da caixa de diálogo SIP da sessão.</span><span class="sxs-lookup"><span data-stu-id="c9032-161">SIP dialog ID of the session.</span></span> <span data-ttu-id="c9032-162">O formato é: caixa de diálogo; de-marca; para-marca.</span><span class="sxs-lookup"><span data-stu-id="c9032-162">The format is: dialog;from-tag;to-tag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9032-163"><strong>Userjointime</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-163"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-164">datetime</span><span class="sxs-lookup"><span data-stu-id="c9032-164">datetime</span></span></p></td>
<td><p><span data-ttu-id="c9032-165">Hora em que o usuário ingressou na conferência.</span><span class="sxs-lookup"><span data-stu-id="c9032-165">Time that the user joined the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9032-166"><strong>Userleavetime</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-166"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-167">datetime</span><span class="sxs-lookup"><span data-stu-id="c9032-167">datetime</span></span></p></td>
<td><p><span data-ttu-id="c9032-168">Tempo em que o usuário saiu da conferência.</span><span class="sxs-lookup"><span data-stu-id="c9032-168">Time that the user left the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9032-169"><strong>UserRole</strong></span><span class="sxs-lookup"><span data-stu-id="c9032-169"><strong>UserRole</strong></span></span></p></td>
<td><p><span data-ttu-id="c9032-170">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c9032-170">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c9032-171">Função do usuário na conferência, como apresentador ou participante.</span><span class="sxs-lookup"><span data-stu-id="c9032-171">User’s role in the conference, such as Presenter or Attendee.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c9032-172">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c9032-172">


</div>

<span> </span>

</div>

</div>

</span></span></div>

