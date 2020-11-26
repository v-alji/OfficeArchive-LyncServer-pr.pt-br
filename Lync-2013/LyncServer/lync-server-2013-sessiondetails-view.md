---
title: 'Lync Server 2013: modo de exibição SessionDetails'
description: 'Lync Server 2013: modo de exibição SessionDetails.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionDetails view
ms:assetid: ea328c6f-cf22-48dd-8f7f-f1666c9148c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721924(v=OCS.15)
ms:contentKeyID: 49733859
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c9f657257e54389defb805919be61adbdecad74
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424027"
---
# <a name="sessiondetails-view-in-lync-server-2013"></a><span data-ttu-id="29b96-103">Exibição SessionDetails no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="29b96-103">SessionDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="29b96-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="29b96-104">

<span> </span></span></span>

<span data-ttu-id="29b96-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="29b96-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="29b96-106">A exibição SessionDetails armazena informações sobre sessões ponto a ponto, que podem ser uma chamada telefônica VoIP-VoIP, uma sessão de mensagens instantâneas de dois participantes ou outro tipo de sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-106">The SessionDetails view stores information about peer-to-peer sessions, which could be a VoIP-VoIP phone call, two-party IM session, or other type of session.</span></span> <span data-ttu-id="29b96-107">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="29b96-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="29b96-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="29b96-108">Column</span></span></th>
<th><span data-ttu-id="29b96-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="29b96-109">Data Type</span></span></th>
<th><span data-ttu-id="29b96-110">Detalhes</span><span class="sxs-lookup"><span data-stu-id="29b96-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29b96-111"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-112">datetime</span><span class="sxs-lookup"><span data-stu-id="29b96-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="29b96-113">Tempo de solicitação de sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-113">Time of session request.</span></span> <span data-ttu-id="29b96-114">Usado em conjunto com o SessionIdSeq para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="29b96-115">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos na tabela do Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="29b96-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> Table for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-117">int</span><span class="sxs-lookup"><span data-stu-id="29b96-117">int</span></span></p></td>
<td><p><span data-ttu-id="29b96-118">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-118">ID number to identify the session.</span></span> <span data-ttu-id="29b96-119">Usado em conjunto com a Identificação_da_sessãotime para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="29b96-120">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="29b96-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-121"><strong>Invitetime</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-121"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-122">datetime</span><span class="sxs-lookup"><span data-stu-id="29b96-122">datetime</span></span></p></td>
<td><p><span data-ttu-id="29b96-123">Hora da primeira solicitação INVITE.</span><span class="sxs-lookup"><span data-stu-id="29b96-123">Time of the first INVITE request.</span></span> <span data-ttu-id="29b96-124">Geralmente, esse campo é preenchido por dados gerados da mensagem de convite inicial na sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-124">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="29b96-125">Se não houver nenhuma mensagem de convite, o campo será preenchido com a data e a hora da primeira mensagem SIP relevante (até mais, cancelamento, mensagem ou informações).</span><span class="sxs-lookup"><span data-stu-id="29b96-125">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span> <span data-ttu-id="29b96-126">Geralmente, esse campo é preenchido por dados gerados da mensagem de convite inicial na sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-126">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="29b96-127">Se não houver nenhuma mensagem de convite, o campo será preenchido com a data e a hora da primeira mensagem SIP relevante (até mais, cancelamento, mensagem ou informações).</span><span class="sxs-lookup"><span data-stu-id="29b96-127">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-128"><strong>FromUri</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-128"><strong>FromUri</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-129">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="29b96-129">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="29b96-130">URL do usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-130">URI of the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-131"><strong>ToUri</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-131"><strong>ToUri</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-132">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="29b96-132">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="29b96-133">URL do usuário que ingressou na sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-133">URI of the user who joined the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-134"><strong>FromUriType</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-134"><strong>FromUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-135">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="29b96-135">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="29b96-136">Tipo de URI do usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-136">Type of URI of the user who started the session.</span></span> <span data-ttu-id="29b96-137">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="29b96-137">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-138"><strong>ToUriType</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-138"><strong>ToUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-139">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="29b96-139">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="29b96-140">Tipo de URI do usuário que ingressou na sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-140">Type of URI of the user who joined the session.</span></span> <span data-ttu-id="29b96-141">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="29b96-141">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-142"><strong>FromTenant</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-142"><strong>FromTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-143">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="29b96-143">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="29b96-144">Locatário do usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-144">Tenant of the user who started the session.</span></span> <span data-ttu-id="29b96-145">Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="29b96-145">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-146"><strong>Tolocatário</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-146"><strong>ToTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-147">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="29b96-147">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="29b96-148">O locatário do usuário que ingressou na sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-148">The tenant of the user who joined the session.</span></span> <span data-ttu-id="29b96-149">Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="29b96-149">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-150"><strong>FromEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-150"><strong>FromEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-151">identificador</span><span class="sxs-lookup"><span data-stu-id="29b96-151">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="29b96-152">Identificador exclusivo do ponto de extremidade do usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-152">Unique identifier of the endpoint of the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-153"><strong>Toendpointid</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-153"><strong>ToEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-154">identificador</span><span class="sxs-lookup"><span data-stu-id="29b96-154">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="29b96-155">Identificador exclusivo do ponto de extremidade do usuário que ingressou na sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-155">Unique identifier of the endpoint of the user who joined the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-156"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-156"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-157">datetime</span><span class="sxs-lookup"><span data-stu-id="29b96-157">datetime</span></span></p></td>
<td><p><span data-ttu-id="29b96-158">Hora de término da sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-158">End time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-159"><strong>FromMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-159"><strong>FromMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-160">int</span><span class="sxs-lookup"><span data-stu-id="29b96-160">int</span></span></p></td>
<td><p><span data-ttu-id="29b96-161">Número de mensagens enviadas pelo usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-161">Number of messages sent by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-162"><strong>ToMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-162"><strong>ToMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-163">int</span><span class="sxs-lookup"><span data-stu-id="29b96-163">int</span></span></p></td>
<td><p><span data-ttu-id="29b96-164">Número de mensagens enviadas pelo usuário que ingressou na sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-164">Number of messages sent by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-165"><strong>FromClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-165"><strong>FromClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-166">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="29b96-166">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="29b96-167">Versão do cliente usada pelo usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-167">Version of client used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-168"><strong>FromClientType</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-168"><strong>FromClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-169">int</span><span class="sxs-lookup"><span data-stu-id="29b96-169">int</span></span></p></td>
<td><p><span data-ttu-id="29b96-170">Cliente usado pelo usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-170">Client used by the user who started the session.</span></span> <span data-ttu-id="29b96-171">Consulte a <a href="lync-server-2013-useragentdef-table.md">tabela UserAgentDef no Lync Server 2013</a> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="29b96-171">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-172"><strong>FromClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-172"><strong>FromClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-173">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="29b96-173">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="29b96-174">Nome da categoria do cliente usado pelo usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-174">Name of the category of the client used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-175"><strong>ToClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-175"><strong>ToClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-176">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="29b96-176">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="29b96-177">Versão do cliente usada pelo usuário que ingressou na sessão</span><span class="sxs-lookup"><span data-stu-id="29b96-177">Version of client used by the user who joined the session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-178"><strong>Toclientetype</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-178"><strong>ToClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-179">int</span><span class="sxs-lookup"><span data-stu-id="29b96-179">int</span></span></p></td>
<td><p><span data-ttu-id="29b96-180">Cliente usado pelo usuário que ingressou na sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-180">Client used by the user who joined the session.</span></span> <span data-ttu-id="29b96-181">Consulte a <a href="lync-server-2013-useragentdef-table.md">tabela UserAgentDef no Lync Server 2013</a> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="29b96-181">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-182"><strong>ToClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-182"><strong>ToClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-183">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="29b96-183">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="29b96-184">Nome da categoria do cliente usado pelo usuário que ingressou na sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-184">Name of the category of the client used by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-185"><strong>TargetUri</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-185"><strong>TargetUri</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-186">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="29b96-186">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="29b96-187">URL do usuário de destino da sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-187">URI of the target user of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-188"><strong>TargetUriType</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-188"><strong>TargetUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-189">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="29b96-189">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="29b96-190">Tipo de URI do usuário de destino da sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-190">Type of URI of the target user for the session.</span></span> <span data-ttu-id="29b96-191">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="29b96-191">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-192"><strong>OnBehalfOfUri</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-192"><strong>OnBehalfOfUri</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-193">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="29b96-193">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="29b96-194">O URI do usuário em nome do qual a sessão foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="29b96-194">URI of the user on whose behalf the session was started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-195"><strong>OnnnBehalfOfUriType</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-195"><strong>OnnnBehalfOfUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="29b96-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="29b96-197">Tipo de URI do usuário em nome do qual a sessão foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="29b96-197">Type of URI of the user on whose behalf the session was started.</span></span> <span data-ttu-id="29b96-198">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="29b96-198">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-199"><strong>OnBehalfOfTenant</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-199"><strong>OnBehalfOfTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-200">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="29b96-200">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="29b96-201">Locatário do usuário cujo nome da sessão foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="29b96-201">Tenant of the user whose on behalf the session was started.</span></span> <span data-ttu-id="29b96-202">Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="29b96-202">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-203"><strong>ReferredByUri</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-203"><strong>ReferredByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-204">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="29b96-204">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="29b96-205">URL do usuário que fez a chamada para a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-205">URI of the user who referred the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-206"><strong>ReferredByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-206"><strong>ReferredByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-207">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="29b96-207">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="29b96-208">Tipo de URI do usuário que a fez referência à sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-208">Type of URI of the user who referred the session.</span></span> <span data-ttu-id="29b96-209">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="29b96-209">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-210"><strong>ReferredByTenant</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-210"><strong>ReferredByTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-211">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="29b96-211">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="29b96-212">Locatário do usuário que fez a chamada para a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-212">Tenant of the user who referred the session.</span></span> <span data-ttu-id="29b96-213">Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="29b96-213">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-214"><strong>Caixa de diálogo</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-214"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-215">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="29b96-215">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="29b96-216">ID da caixa de diálogo SIP.</span><span class="sxs-lookup"><span data-stu-id="29b96-216">SIP dialog ID.</span></span> <span data-ttu-id="29b96-217">O formato é:</span><span class="sxs-lookup"><span data-stu-id="29b96-217">The format is:</span></span></p>
<p><span data-ttu-id="29b96-218">caixa de diálogo; de-marca; até-marca</span><span class="sxs-lookup"><span data-stu-id="29b96-218">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-219"><strong>CorrelationId</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-219"><strong>CorrelationId</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-220">identificador</span><span class="sxs-lookup"><span data-stu-id="29b96-220">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="29b96-221">GUID usado para correlacionar várias sessões.</span><span class="sxs-lookup"><span data-stu-id="29b96-221">GUID used to correlate multiple sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-222"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-222"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-223">datetime</span><span class="sxs-lookup"><span data-stu-id="29b96-223">datetime</span></span></p></td>
<td><p><span data-ttu-id="29b96-224">A hora da caixa de diálogo que foi substituída pela sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-224">Time of the dialog which was replaced by the session.</span></span> <span data-ttu-id="29b96-225">Usado em conjunto com ReplaceDialogIdSeq para identificar exclusivamente uma caixa de diálogo que é substituída pela sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-225">Used in conjunction with ReplaceDialogIdSeq to uniquely identify a dialog that is replaced by the session.</span></span> <span data-ttu-id="29b96-226">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="29b96-226">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-227"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-227"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-228">int</span><span class="sxs-lookup"><span data-stu-id="29b96-228">int</span></span></p></td>
<td><p><span data-ttu-id="29b96-229">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-229">ID number to identify the session.</span></span> <span data-ttu-id="29b96-230">Usado em conjunto com ReplaceDialogIdTime para identificar exclusivamente uma caixa de diálogo que é substituída pela sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-230">Used in conjunction with ReplaceDialogIdTime to uniquely identify a dialog that is replaced by the session.</span></span> <span data-ttu-id="29b96-231">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="29b96-231">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-232"><strong>ReplacesDialogId</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-232"><strong>ReplacesDialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-233">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="29b96-233">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="29b96-234">ID da caixa de diálogo SIP a sessão substitui.</span><span class="sxs-lookup"><span data-stu-id="29b96-234">SIP dialog ID the session replaces.</span></span> <span data-ttu-id="29b96-235">O formato é:</span><span class="sxs-lookup"><span data-stu-id="29b96-235">The format is:</span></span></p>
<p><span data-ttu-id="29b96-236">caixa de diálogo; de-marca; até-marca</span><span class="sxs-lookup"><span data-stu-id="29b96-236">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-237"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-237"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-238">datetime</span><span class="sxs-lookup"><span data-stu-id="29b96-238">datetime</span></span></p></td>
<td><p><span data-ttu-id="29b96-239">Hora da resposta à primeira mensagem de convite.</span><span class="sxs-lookup"><span data-stu-id="29b96-239">Time of the response to the first INVITE message.</span></span> <span data-ttu-id="29b96-240">Geralmente, esse campo é preenchido por dados gerados da mensagem de convite inicial na sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-240">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="29b96-241">Se não houver nenhuma mensagem de convite, o campo será preenchido com a data e a hora da primeira mensagem SIP relevante (até mais, cancelamento, mensagem ou informações).</span><span class="sxs-lookup"><span data-stu-id="29b96-241">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-242"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-242"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-243">int</span><span class="sxs-lookup"><span data-stu-id="29b96-243">int</span></span></p></td>
<td><p><span data-ttu-id="29b96-244">Código de resposta SIP para o convite da sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-244">SIP response code to the session invitation.</span></span> <span data-ttu-id="29b96-245">Geralmente, esse campo é preenchido por dados gerados da mensagem de convite inicial na sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-245">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="29b96-246">Se não houver nenhuma mensagem de convite, o campo será preenchido com a data e a hora da primeira mensagem SIP relevante (até mais, cancelamento, mensagem ou informações).</span><span class="sxs-lookup"><span data-stu-id="29b96-246">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-247"><strong>Diagnosticid</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-247"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-248">int</span><span class="sxs-lookup"><span data-stu-id="29b96-248">int</span></span></p></td>
<td><p><span data-ttu-id="29b96-249">ID de diagnóstico capturada de cabeçalhos SIP.</span><span class="sxs-lookup"><span data-stu-id="29b96-249">Diagnostic ID captured from SIP headers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-250"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-250"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-251">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="29b96-251">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="29b96-252">Tipo de conteúdo da sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-252">Type of content for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-253"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-253"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-254">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="29b96-254">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="29b96-255">FQDN do servidor de front-end que capturou os dados para a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-255">FQDN of the Front End server that captured the data for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-256"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-256"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-257">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="29b96-257">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="29b96-258">FQDN do pool que capturou os dados da sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-258">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-259"><strong>FromEdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-259"><strong>FromEdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-260">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="29b96-260">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="29b96-261">FQDN do servidor de borda usado pelo usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-261">FQDN of the Edge server used by the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-262"><strong>ToEdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-262"><strong>ToEdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-263">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="29b96-263">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="29b96-264">FQDN do servidor de borda usado pelo usuário que iniciou a sessão</span><span class="sxs-lookup"><span data-stu-id="29b96-264">FQDN of the Edge server used by the user who started the session</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-265"><strong>IsFromInternal</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-265"><strong>IsFromInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-266">bit</span><span class="sxs-lookup"><span data-stu-id="29b96-266">bit</span></span></p></td>
<td><p><span data-ttu-id="29b96-267">Indica se o usuário que iniciou a sessão está conectada a partir da rede interna.</span><span class="sxs-lookup"><span data-stu-id="29b96-267">Indicates whether the user who started the session logged on from the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-268"><strong>IsToInternal</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-268"><strong>IsToInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-269">bit</span><span class="sxs-lookup"><span data-stu-id="29b96-269">bit</span></span></p></td>
<td><p><span data-ttu-id="29b96-270">Indica se o usuário que ingressou na sessão que se conectou na rede interna.</span><span class="sxs-lookup"><span data-stu-id="29b96-270">Indicates whether the user who joined the session logged on from the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-271"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-271"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-272">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="29b96-272">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="29b96-273">Prioridade da chamada da sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-273">Call priority of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-274"><strong>FromUserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-274"><strong>FromUserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-275">smallint</span><span class="sxs-lookup"><span data-stu-id="29b96-275">smallint</span></span></p></td>
<td><p><span data-ttu-id="29b96-276">Indica os atributos do usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-276">Indicates the attributes of the user who started the session.</span></span> <span data-ttu-id="29b96-277">As definições de atributo a seguir são permitidas:</span><span class="sxs-lookup"><span data-stu-id="29b96-277">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="29b96-278">0x01-integrado ao telefone desktop</span><span class="sxs-lookup"><span data-stu-id="29b96-278">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-279"><strong>ToUserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-279"><strong>ToUserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-280">smallint</span><span class="sxs-lookup"><span data-stu-id="29b96-280">smallint</span></span></p></td>
<td><p><span data-ttu-id="29b96-281">Indica os atributos do usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="29b96-281">Indicates the attributes of the user who started the session.</span></span> <span data-ttu-id="29b96-282">As definições de atributo a seguir são permitidas:</span><span class="sxs-lookup"><span data-stu-id="29b96-282">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="29b96-283">0x01-integrado ao telefone desktop</span><span class="sxs-lookup"><span data-stu-id="29b96-283">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29b96-284"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-284"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-285">smallint</span><span class="sxs-lookup"><span data-stu-id="29b96-285">smallint</span></span></p></td>
<td><p><span data-ttu-id="29b96-286">Indica os atributos da chamada.</span><span class="sxs-lookup"><span data-stu-id="29b96-286">Indicates the call attributes.</span></span> <span data-ttu-id="29b96-287">As definições de atributo a seguir são permitidas:</span><span class="sxs-lookup"><span data-stu-id="29b96-287">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="29b96-288">0x01-sessão repetida</span><span class="sxs-lookup"><span data-stu-id="29b96-288">0x01 - Retried Session</span></span></p>
<p><span data-ttu-id="29b96-289">0x02-uma chamada feita pelo agente em nome de um grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="29b96-289">0x02 - A call made by agent on behalf of a Response Group</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29b96-290"><strong>Local</strong></span><span class="sxs-lookup"><span data-stu-id="29b96-290"><strong>Location</strong></span></span></p></td>
<td><p><span data-ttu-id="29b96-291">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="29b96-291">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="29b96-292">Local de chamada de emergência.</span><span class="sxs-lookup"><span data-stu-id="29b96-292">Location of emergency call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="29b96-293">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="29b96-293">


</div>

<span> </span>

</div>

</div>

</span></span></div>

