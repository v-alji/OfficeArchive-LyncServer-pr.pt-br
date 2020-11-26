---
title: 'Lync Server 2013: modo de exibição ConferenceSessionDetails'
description: 'Lync Server 2013: modo de exibição ConferenceSessionDetails.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceSessionDetails view
ms:assetid: 5858c84d-baed-421d-ad1d-3726e150e256
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688066(v=OCS.15)
ms:contentKeyID: 49733660
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d1c62f020413efecdbc0f909618256ccc7308d4f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434393"
---
# <a name="conferencesessiondetails-view-in-lync-server-2013"></a><span data-ttu-id="996b3-103">Exibição ConferenceSessionDetails no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="996b3-103">ConferenceSessionDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="996b3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="996b3-104">

<span> </span></span></span>

<span data-ttu-id="996b3-105">_**Tópico da última modificação:** 2012-11-12_</span><span class="sxs-lookup"><span data-stu-id="996b3-105">_**Topic Last Modified:** 2012-11-12_</span></span>

<span data-ttu-id="996b3-106">A exibição ConferenceSessionDetails armazena informações sobre sessões com vários participantes.</span><span class="sxs-lookup"><span data-stu-id="996b3-106">The ConferenceSessionDetails view stores information about multiparty sessions.</span></span> <span data-ttu-id="996b3-107">Cada registro representa uma sessão de conferência, que pode ser a sessão com foco ou a sessão com um servidor de conferência específico.</span><span class="sxs-lookup"><span data-stu-id="996b3-107">Each record represents one conference session, which could be either the session with Focus or the session with a specific conferencing server.</span></span> <span data-ttu-id="996b3-108">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="996b3-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="996b3-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="996b3-109">Column</span></span></th>
<th><span data-ttu-id="996b3-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="996b3-110">Data Type</span></span></th>
<th><span data-ttu-id="996b3-111">Detalhes</span><span class="sxs-lookup"><span data-stu-id="996b3-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="996b3-112"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-113">datetime</span><span class="sxs-lookup"><span data-stu-id="996b3-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="996b3-114">Tempo de solicitação de sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-114">Time of session request.</span></span> <span data-ttu-id="996b3-115">Usado em conjunto com o SessionIdSeq para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-115">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="996b3-116">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="996b3-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-118">int</span><span class="sxs-lookup"><span data-stu-id="996b3-118">int</span></span></p></td>
<td><p><span data-ttu-id="996b3-119">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-119">ID number to identify the session.</span></span> <span data-ttu-id="996b3-120">Usado em conjunto com a Identificação_da_sessãotime para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-120">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="996b3-121">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="996b3-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-122"><strong>Invitetime</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-122"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-123">datetime</span><span class="sxs-lookup"><span data-stu-id="996b3-123">datetime</span></span></p></td>
<td><p><span data-ttu-id="996b3-124">Hora da primeira solicitação INVITE.</span><span class="sxs-lookup"><span data-stu-id="996b3-124">Time of the first INVITE request.</span></span> <span data-ttu-id="996b3-125">Geralmente, esse campo é preenchido por dados gerados da mensagem de convite inicial na sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-125">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="996b3-126">Se não houver nenhuma mensagem de convite, o campo será preenchido com a data e a hora da primeira mensagem SIP relevante (até mais, cancelamento, mensagem ou informações).</span><span class="sxs-lookup"><span data-stu-id="996b3-126">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-127"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-127"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-128">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="996b3-128">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="996b3-129">URL da conferência.</span><span class="sxs-lookup"><span data-stu-id="996b3-129">URI of the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-130"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-130"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-131">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-131">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-132">Tipo de URI de conferência.</span><span class="sxs-lookup"><span data-stu-id="996b3-132">Type of conference URI.</span></span> <span data-ttu-id="996b3-133">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="996b3-133">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-134"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-134"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-135">identificador</span><span class="sxs-lookup"><span data-stu-id="996b3-135">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="996b3-136">Identificador que diferencia as instâncias de conferências recorrentes.</span><span class="sxs-lookup"><span data-stu-id="996b3-136">Identifier that differentiates between instances of recurring conferences.</span></span> <span data-ttu-id="996b3-137">Cada instância de conferência recorrente tem o mesmo ConferenceURI, mas um valor ConfInstance diferente.</span><span class="sxs-lookup"><span data-stu-id="996b3-137">Each recurring conference instance has the same ConferenceURI but a different ConfInstance value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-138"><strong>McuConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-138"><strong>McuConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="996b3-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="996b3-140">URL do servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="996b3-140">URI of the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-141"><strong>McuConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-141"><strong>McuConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-142">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-142">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-143">Tipo de URI do servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="996b3-143">Type of conferencing server URI.</span></span> <span data-ttu-id="996b3-144">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="996b3-144">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-145"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-145"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-146">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="996b3-146">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="996b3-147">O URI do usuário envolvido na sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-147">URI of the user involved in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-148"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-148"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-149">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-149">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-150">Tipo de URI do usuário cuja parte da sessão faz parte.</span><span class="sxs-lookup"><span data-stu-id="996b3-150">Type of URI of the user whose was part of the session.</span></span> <span data-ttu-id="996b3-151">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="996b3-151">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-152"><strong>Userlocatário</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-152"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-154">Locatário do usuário cuja parte da sessão faz parte.</span><span class="sxs-lookup"><span data-stu-id="996b3-154">Tenant of the user whose was part of the session.</span></span> <span data-ttu-id="996b3-155">Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="996b3-155">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-156"><strong>Userendpointid</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-156"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-157">identificador</span><span class="sxs-lookup"><span data-stu-id="996b3-157">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="996b3-158">Identificador exclusivo do usuário cuja parte da sessão faz parte.</span><span class="sxs-lookup"><span data-stu-id="996b3-158">Unique identifier of the user whose was part of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-159"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-159"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-160">datetime</span><span class="sxs-lookup"><span data-stu-id="996b3-160">datetime</span></span></p></td>
<td><p><span data-ttu-id="996b3-161">Hora de término da sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-161">End time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-162"><strong>ConferenceClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-162"><strong>ConferenceClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-163">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-163">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-164">Versão do servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="996b3-164">Version of conference server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-165"><strong>ConferenceClientType</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-165"><strong>ConferenceClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-166">int</span><span class="sxs-lookup"><span data-stu-id="996b3-166">int</span></span></p></td>
<td><p><span data-ttu-id="996b3-167">Tipo de servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="996b3-167">Type of conference server.</span></span> <span data-ttu-id="996b3-168">Consulte a <a href="lync-server-2013-useragentdef-table.md">tabela UserAgentDef no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="996b3-168">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-169"><strong>ConferenceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-169"><strong>ConferenceCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-170">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="996b3-170">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="996b3-171">Categoria do servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="996b3-171">Conference server category.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-172"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-172"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-173">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-173">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-174">Versão do cliente usada pelo usuário que participou na sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-174">Version of client used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-175"><strong>Userclienttype</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-175"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-176">int</span><span class="sxs-lookup"><span data-stu-id="996b3-176">int</span></span></p></td>
<td><p><span data-ttu-id="996b3-177">Cliente usado pelo usuário que participou na sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-177">Client used by the user who participated in the session.</span></span> <span data-ttu-id="996b3-178">Consulte a <a href="lync-server-2013-useragentdef-table.md">tabela UserAgentDef no Lync Server 2013</a> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="996b3-178">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-179"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-179"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-180">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="996b3-180">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="996b3-181">Nome da categoria do cliente usado pelo usuário que fazia parte da sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-181">Name of the category of the client used by the user who was part of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-182"><strong>OnBehalfOfUri</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-182"><strong>OnBehalfOfUri</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-183">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="996b3-183">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="996b3-184">O URI do usuário em nome do qual a sessão foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="996b3-184">URI of the user on whose behalf the session was started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-185"><strong>OnBehalfOfUriType</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-185"><strong>OnBehalfOfUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-186">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-186">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-187">Tipo de URI do usuário em nome do qual a sessão foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="996b3-187">Type of URI of the user on whose behalf the session was started.</span></span> <span data-ttu-id="996b3-188">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="996b3-188">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-189"><strong>OnBehalfOfTenant</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-189"><strong>OnBehalfOfTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-190">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-190">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-191">Locatário do usuário cujo nome da sessão foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="996b3-191">Tenant of the user whose on behalf the session was started.</span></span> <span data-ttu-id="996b3-192">Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="996b3-192">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-193"><strong>ReferredByUri</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-193"><strong>ReferredByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-194">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="996b3-194">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="996b3-195">URL do usuário que fez a chamada para a sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-195">URI of the user who referred the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-196"><strong>ReferredByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-196"><strong>ReferredByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-197">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-197">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-198">Tipo de URI do usuário que a fez referência à sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-198">Type of URI of the user who referred the session.</span></span> <span data-ttu-id="996b3-199">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="996b3-199">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-200"><strong>ReferredByUriTenant</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-200"><strong>ReferredByUriTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-201">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-201">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-202">Locatário do usuário que fez a chamada para a sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-202">Tenant of the user who referred the session.</span></span> <span data-ttu-id="996b3-203">Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="996b3-203">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-204"><strong>Caixa de diálogo</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-204"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-205">VARSTRING (775)</span><span class="sxs-lookup"><span data-stu-id="996b3-205">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="996b3-206">ID da caixa de diálogo SIP.</span><span class="sxs-lookup"><span data-stu-id="996b3-206">SIP dialog ID.</span></span> <span data-ttu-id="996b3-207">O formato é</span><span class="sxs-lookup"><span data-stu-id="996b3-207">The format is</span></span></p>
<p><span data-ttu-id="996b3-208">:d ialog; de-marca; até-marca</span><span class="sxs-lookup"><span data-stu-id="996b3-208">:dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-209"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-209"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-210">datetime</span><span class="sxs-lookup"><span data-stu-id="996b3-210">datetime</span></span></p></td>
<td><p><span data-ttu-id="996b3-211">Número de identificação para identificar a caixa de diálogo que foi substituída pela sessão atual.</span><span class="sxs-lookup"><span data-stu-id="996b3-211">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="996b3-212">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="996b3-212">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-213"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-213"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-214">int</span><span class="sxs-lookup"><span data-stu-id="996b3-214">int</span></span></p></td>
<td><p><span data-ttu-id="996b3-215">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-215">ID number to identify the session.</span></span> <span data-ttu-id="996b3-216">Usado em conjunto com ReplaceDialogIdTime para identificar exclusivamente uma sessão substituída por esta sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-216">Used in conjunction with ReplaceDialogIdTime to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="996b3-217">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="996b3-217">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-218"><strong>ReplacesDialogId</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-218"><strong>ReplacesDialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-219">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="996b3-219">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="996b3-220">ID da caixa de diálogo SIP a sessão substitui.</span><span class="sxs-lookup"><span data-stu-id="996b3-220">SIP dialog ID the session replaces.</span></span> <span data-ttu-id="996b3-221">O formato do é:</span><span class="sxs-lookup"><span data-stu-id="996b3-221">The format of the is:</span></span></p>
<p><span data-ttu-id="996b3-222">caixa de diálogo; de-marca; até-marca</span><span class="sxs-lookup"><span data-stu-id="996b3-222">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-223"><strong>IsStartedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-223"><strong>IsStartedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-224">bit</span><span class="sxs-lookup"><span data-stu-id="996b3-224">bit</span></span></p></td>
<td><p><span data-ttu-id="996b3-225">Indica se a sessão foi iniciada pelo servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="996b3-225">Indicates whether the session was started by the conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-226"><strong>IsEndedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-226"><strong>IsEndedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-227">bit</span><span class="sxs-lookup"><span data-stu-id="996b3-227">bit</span></span></p></td>
<td><p><span data-ttu-id="996b3-228">Indica se a sessão foi encerrada pelo servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="996b3-228">Indicates whether the session was ended by the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-229"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-229"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-230">bit</span><span class="sxs-lookup"><span data-stu-id="996b3-230">bit</span></span></p></td>
<td><p><span data-ttu-id="996b3-231">Indica se o usuário está conectado à rede interna.</span><span class="sxs-lookup"><span data-stu-id="996b3-231">Indicates whether the user logged on from the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-232"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-232"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-233">datetime</span><span class="sxs-lookup"><span data-stu-id="996b3-233">datetime</span></span></p></td>
<td><p><span data-ttu-id="996b3-234">Hora da resposta à primeira mensagem de convite.</span><span class="sxs-lookup"><span data-stu-id="996b3-234">Time of the response to the first INVITE message.</span></span> <span data-ttu-id="996b3-235">Geralmente, esse campo é preenchido por dados gerados da mensagem de convite inicial na sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-235">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="996b3-236">Se não houver nenhuma mensagem de convite, o campo será preenchido com a data e a hora da primeira mensagem SIP relevante (até mais, cancelamento, mensagem ou informações).</span><span class="sxs-lookup"><span data-stu-id="996b3-236">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-237"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-237"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-238">int</span><span class="sxs-lookup"><span data-stu-id="996b3-238">int</span></span></p></td>
<td><p><span data-ttu-id="996b3-239">Código de resposta SIP para o convite da sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-239">SIP response code to the session invitation.</span></span> <span data-ttu-id="996b3-240">Geralmente, esse campo é preenchido por dados gerados da mensagem de convite inicial na sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-240">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="996b3-241">Se não houver nenhuma mensagem de convite, o campo será preenchido com a data e a hora da primeira mensagem SIP relevante (até mais, cancelamento, mensagem ou informações).</span><span class="sxs-lookup"><span data-stu-id="996b3-241">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-242"><strong>Diagnosticid</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-242"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-243">int</span><span class="sxs-lookup"><span data-stu-id="996b3-243">int</span></span></p></td>
<td><p><span data-ttu-id="996b3-244">ID do diagnóstico capturada dos cabeçalhos SIP da sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-244">Diagnostic ID captured from session SIP headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-245"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-245"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-246">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-246">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-247">Tipo de conteúdo da sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-247">Content type for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-248"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-248"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-249">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-249">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-250">FQDN do servidor de front-end que capturou os dados para a sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-250">FQDN of the Front End server that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-251"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-251"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-252">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-252">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-253">FQDN do pool que capturou os dados da sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-253">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-254"><strong>MediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-254"><strong>MediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-255">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-255">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-256">Servidor de mediação usado pelo usuário que participou na sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-256">Mediation Server used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-257"><strong>Gateway</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-257"><strong>Gateway</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-258">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-258">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-259">O gateway usado pelo usuário que participou da sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-259">Gateway used by the user who participated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-260"><strong>EdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-260"><strong>EdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-261">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="996b3-261">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="996b3-262">FQDN do servidor de borda usado pelo usuário que participou na sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-262">FQDN of the Edge server used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996b3-263"><strong>Sinalizador</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-263"><strong>UserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-264">smallint</span><span class="sxs-lookup"><span data-stu-id="996b3-264">smallint</span></span></p></td>
<td><p><span data-ttu-id="996b3-265">Indica os atributos do usuário que participou na sessão.</span><span class="sxs-lookup"><span data-stu-id="996b3-265">Indicates the attributes of the user who participated in the session.</span></span> <span data-ttu-id="996b3-266">As definições de atributo a seguir são permitidas:</span><span class="sxs-lookup"><span data-stu-id="996b3-266">The following attribute definitions allowed:</span></span></p>
<p><span data-ttu-id="996b3-267">0x01-integrado ao telefone desktop</span><span class="sxs-lookup"><span data-stu-id="996b3-267">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996b3-268"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="996b3-268"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="996b3-269">smallint</span><span class="sxs-lookup"><span data-stu-id="996b3-269">smallint</span></span></p></td>
<td><p><span data-ttu-id="996b3-270">Indica os atributos da chamada.</span><span class="sxs-lookup"><span data-stu-id="996b3-270">Indicates the call attributes.</span></span> <span data-ttu-id="996b3-271">As definições de atributo a seguir são permitidas:</span><span class="sxs-lookup"><span data-stu-id="996b3-271">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="996b3-272">0x01-repetidas Session0</span><span class="sxs-lookup"><span data-stu-id="996b3-272">0x01 - Retried Session0</span></span></p>
<p><span data-ttu-id="996b3-273">X02-uma chamada feita pelo agente em nome de um grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="996b3-273">x02 - A call made by agent on behalf of a Response Group</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="996b3-274">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="996b3-274">


</div>

<span> </span>

</div>

</div>

</span></span></div>

