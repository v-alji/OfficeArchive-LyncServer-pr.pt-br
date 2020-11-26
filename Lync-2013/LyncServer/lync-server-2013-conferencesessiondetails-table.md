---
title: 'Lync Server 2013: Tabela ConferenceSessionDetails'
description: 'Lync Server 2013: ConferenceSessionDetails Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceSessionDetails table
ms:assetid: 9eae6a54-69fd-4966-aa17-7ecee1297ad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412741(v=OCS.15)
ms:contentKeyID: 48184925
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d101eb1607e366ab814e60acaeee80820fe87c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434414"
---
# <a name="conferencesessiondetails-table-in-lync-server-2013"></a><span data-ttu-id="8e147-103">Tabela ConferenceSessionDetails no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e147-103">ConferenceSessionDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e147-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e147-104">

<span> </span></span></span>

<span data-ttu-id="8e147-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="8e147-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="8e147-106">Cada registro representa uma sessão de conferência, que pode ser a sessão com foco ou a sessão com um servidor de conferência específico.</span><span class="sxs-lookup"><span data-stu-id="8e147-106">Each record represents one conference session, which could be either the session with Focus or the session with a specific conferencing server.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e147-107">Coluna</span><span class="sxs-lookup"><span data-stu-id="8e147-107">Column</span></span></th>
<th><span data-ttu-id="8e147-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8e147-108">Data Type</span></span></th>
<th><span data-ttu-id="8e147-109">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="8e147-109">Key/Index</span></span></th>
<th><span data-ttu-id="8e147-110">Detalhes</span><span class="sxs-lookup"><span data-stu-id="8e147-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e147-111"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-112">DateTime</span><span class="sxs-lookup"><span data-stu-id="8e147-112">Datetime</span></span></p></td>
<td><p><span data-ttu-id="8e147-113">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="8e147-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-114">Tempo de solicitação de sessão; usado em conjunto com <strong>SessionIdSeq</strong> para identificar uma sessão de conferência com exclusividade.</span><span class="sxs-lookup"><span data-stu-id="8e147-114">Time of session request; used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference session.</span></span> <span data-ttu-id="8e147-115">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e147-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-117">int</span><span class="sxs-lookup"><span data-stu-id="8e147-117">int</span></span></p></td>
<td><p><span data-ttu-id="8e147-118">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="8e147-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-119">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="8e147-119">ID number to identify the session.</span></span> <span data-ttu-id="8e147-120">Usado em conjunto com a <strong>identificação_da_sessãotime</strong> para identificar exclusivamente uma sessão de conferência.</span><span class="sxs-lookup"><span data-stu-id="8e147-120">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference session.</span></span> <span data-ttu-id="8e147-121">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span> *</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e147-122"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-122"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-123">int</span><span class="sxs-lookup"><span data-stu-id="8e147-123">int</span></span></p></td>
<td><p><span data-ttu-id="8e147-124">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-125">URI da conferência em foco relacionado a esta sessão.</span><span class="sxs-lookup"><span data-stu-id="8e147-125">Focus conference URI related to this session.</span></span> <span data-ttu-id="8e147-126">Consulte a <a href="lync-server-2013-conferenceuris-table.md">tabela ConferenceUris no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-126">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="8e147-127">Esse URI é um URI de conferência baseado em foco.</span><span class="sxs-lookup"><span data-stu-id="8e147-127">This URI is a Focus-based conference URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e147-128"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-128"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-129">Identificador</span><span class="sxs-lookup"><span data-stu-id="8e147-129">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8e147-130">Identificador que diferencia as instâncias de conferências recorrentes.</span><span class="sxs-lookup"><span data-stu-id="8e147-130">Identifier that differentiates between instances of recurring conferences.</span></span> <span data-ttu-id="8e147-131">Cada instância de conferência recorrente tem o mesmo ConferenceURI, mas um valor ConfInstance diferente.</span><span class="sxs-lookup"><span data-stu-id="8e147-131">Each recurring conference instance has the same ConferenceURI but a different ConfInstance value.</span></span></p>
<p><span data-ttu-id="8e147-132">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8e147-132">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e147-133"><strong>McuConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-133"><strong>McuConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-134">int</span><span class="sxs-lookup"><span data-stu-id="8e147-134">int</span></span></p></td>
<td><p><span data-ttu-id="8e147-135">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-135">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-136">URL de conferência do servidor de conferência relacionada a esta sessão.</span><span class="sxs-lookup"><span data-stu-id="8e147-136">Conferencing server conference URI related to this session.</span></span> <span data-ttu-id="8e147-137">Consulte a <a href="lync-server-2013-conferenceuris-table.md">tabela ConferenceUris no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-137">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="8e147-138">Esse URI é o URI da conferência baseada no servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="8e147-138">This URI is the conferencing server-based conference URI.</span></span> <span data-ttu-id="8e147-139">Para sessões de conferência de foco, esta coluna será nula.</span><span class="sxs-lookup"><span data-stu-id="8e147-139">For Focus conference sessions, this column will be null.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e147-140"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-140"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-141">int</span><span class="sxs-lookup"><span data-stu-id="8e147-141">int</span></span></p></td>
<td><p><span data-ttu-id="8e147-142">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-143">ID de um usuário na sessão de conferência.</span><span class="sxs-lookup"><span data-stu-id="8e147-143">ID of one user in the conference session.</span></span> <span data-ttu-id="8e147-144">Consulte a <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-144">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e147-145"><strong>Userendpointid</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-145"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-146">identificador</span><span class="sxs-lookup"><span data-stu-id="8e147-146">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8e147-147">Um GUID para identificar a instância do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8e147-147">A GUID to identify the instance of endpoint.</span></span> <span data-ttu-id="8e147-148">Por exemplo, se um usuário fizer logon em máquinas diferentes com a mesma conta, cada computador terá uma ID de ponto de extremidade diferente.</span><span class="sxs-lookup"><span data-stu-id="8e147-148">For example, if one user logs on to different machines with the same account, then each machine will have a different endpoint ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e147-149"><strong>OnBehalfOfId</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-149"><strong>OnBehalfOfId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-150">int</span><span class="sxs-lookup"><span data-stu-id="8e147-150">int</span></span></p></td>
<td><p><span data-ttu-id="8e147-151">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-151">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-152">Indica a ID do usuário de quem o chamador está em nome.</span><span class="sxs-lookup"><span data-stu-id="8e147-152">Indicates the ID of the user of who the caller is on behalf.</span></span> <span data-ttu-id="8e147-153">Consulte a <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-153">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e147-154"><strong>ReferredById</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-154"><strong>ReferredById</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-155">int</span><span class="sxs-lookup"><span data-stu-id="8e147-155">int</span></span></p></td>
<td><p><span data-ttu-id="8e147-156">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-156">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-157">ID do usuário por quem a chamada é referida.</span><span class="sxs-lookup"><span data-stu-id="8e147-157">ID of the user by who the call is referred.</span></span> <span data-ttu-id="8e147-158">Consulte a <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-158">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e147-159"><strong>UserClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-159"><strong>UserClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-160">int</span><span class="sxs-lookup"><span data-stu-id="8e147-160">int</span></span></p></td>
<td><p><span data-ttu-id="8e147-161">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-161">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-162">Versão do cliente usada pelo usuário da conferência.</span><span class="sxs-lookup"><span data-stu-id="8e147-162">Client version used by the conference user.</span></span> <span data-ttu-id="8e147-163">Consulte a <a href="lync-server-2013-clientversions-table.md">tabela ClientVersions no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-163">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e147-164"><strong>ConfClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-164"><strong>ConfClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-165">int</span><span class="sxs-lookup"><span data-stu-id="8e147-165">int</span></span></p></td>
<td><p><span data-ttu-id="8e147-166">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-166">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-167">Versão do cliente usada pelo servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="8e147-167">Client version used by the conference server.</span></span> <span data-ttu-id="8e147-168">Consulte a <a href="lync-server-2013-clientversions-table.md">tabela ClientVersions no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-168">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e147-169"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-169"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-170">datetime</span><span class="sxs-lookup"><span data-stu-id="8e147-170">datetime</span></span></p></td>
<td><p><span data-ttu-id="8e147-171">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-171">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-172">Número de identificação para identificar a caixa de diálogo que foi substituída pela sessão atual.</span><span class="sxs-lookup"><span data-stu-id="8e147-172">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="8e147-173">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-173">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e147-174"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-174"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-175">int</span><span class="sxs-lookup"><span data-stu-id="8e147-175">int</span></span></p></td>
<td><p><span data-ttu-id="8e147-176">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-176">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-177">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="8e147-177">ID number to identify the session.</span></span> <span data-ttu-id="8e147-178">Usado em conjunto com <strong>ReplacesDialogIdTime</strong> para identificar exclusivamente uma sessão substituída por esta sessão.</span><span class="sxs-lookup"><span data-stu-id="8e147-178">Used in conjunction with <strong>ReplacesDialogIdTime</strong> to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="8e147-179">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-179">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e147-180"><strong>IsStartedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-180"><strong>IsStartedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-181">bit</span><span class="sxs-lookup"><span data-stu-id="8e147-181">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8e147-182">Indica se a sessão foi iniciada pelo servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="8e147-182">Indicates if the session started by the conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e147-183"><strong>IsEndedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-183"><strong>IsEndedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-184">bit</span><span class="sxs-lookup"><span data-stu-id="8e147-184">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8e147-185">Indica se a sessão terminou pelo servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="8e147-185">Indicates if the session ended by the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e147-186"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-186"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-187">bit</span><span class="sxs-lookup"><span data-stu-id="8e147-187">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8e147-188">Se o usuário está conectado de Internal ou not.</span><span class="sxs-lookup"><span data-stu-id="8e147-188">Whether user is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e147-189"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-189"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-190">int</span><span class="sxs-lookup"><span data-stu-id="8e147-190">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8e147-191">Código de resposta do SIP (Session Initiation Protocol) para o convite da sessão.</span><span class="sxs-lookup"><span data-stu-id="8e147-191">Session Initiation Protocol (SIP) response code to the session invitation.</span></span> <span data-ttu-id="8e147-192">Geralmente, esse campo é preenchido por dados gerados da mensagem de convite inicial na sessão.</span><span class="sxs-lookup"><span data-stu-id="8e147-192">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="8e147-193">Se não houver nenhuma mensagem de convite, o campo será preenchido com a data e a hora da primeira mensagem SIP relevante (até mais, cancelamento, mensagem ou informações).</span><span class="sxs-lookup"><span data-stu-id="8e147-193">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e147-194"><strong>Diagnosticid</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-194"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-195">int</span><span class="sxs-lookup"><span data-stu-id="8e147-195">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8e147-196">ID de diagnóstico capturada do cabeçalho SIP.</span><span class="sxs-lookup"><span data-stu-id="8e147-196">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e147-197"><strong>ServerID</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-197"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-198">int</span><span class="sxs-lookup"><span data-stu-id="8e147-198">int</span></span></p></td>
<td><p><span data-ttu-id="8e147-199">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-199">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-200">ID do servidor front-end usado para esta sessão.</span><span class="sxs-lookup"><span data-stu-id="8e147-200">ID of the front-end server used for this session.</span></span> <span data-ttu-id="8e147-201">Consulte a <a href="lync-server-2013-servers-table.md">tabela servidores no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-201">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e147-202"><strong>Poolid</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-202"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-203">int</span><span class="sxs-lookup"><span data-stu-id="8e147-203">int</span></span></p></td>
<td><p><span data-ttu-id="8e147-204">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-204">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-205">ID do pool no qual a sessão foi capturada.</span><span class="sxs-lookup"><span data-stu-id="8e147-205">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="8e147-206">Consulte a <a href="lync-server-2013-pools-table.md">tabela de grupos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-206">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e147-207"><strong>MediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-207"><strong>MediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-208">int</span><span class="sxs-lookup"><span data-stu-id="8e147-208">int</span></span></p></td>
<td><p><span data-ttu-id="8e147-209">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-209">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-210">O servidor de mediação que a chamada está usando.</span><span class="sxs-lookup"><span data-stu-id="8e147-210">The Mediation Server the call is using.</span></span> <span data-ttu-id="8e147-211">Consulte a <a href="lync-server-2013-mediationservers-table.md">tabela MediationServers no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-211">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e147-212"><strong>Gatewayid</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-212"><strong>GatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-213">int</span><span class="sxs-lookup"><span data-stu-id="8e147-213">int</span></span></p></td>
<td><p><span data-ttu-id="8e147-214">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-214">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-215">O gateway que a chamada está usando.</span><span class="sxs-lookup"><span data-stu-id="8e147-215">The gateway the call is using.</span></span> <span data-ttu-id="8e147-216">Consulte a <a href="lync-server-2013-gateways-table.md">tabela gateways no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-216">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e147-217"><strong>EdgeServerId</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-217"><strong>EdgeServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-218">int</span><span class="sxs-lookup"><span data-stu-id="8e147-218">int</span></span></p></td>
<td><p><span data-ttu-id="8e147-219">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-219">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-220">O servidor de borda que a chamada está usando.</span><span class="sxs-lookup"><span data-stu-id="8e147-220">The Edge Server the call is using.</span></span> <span data-ttu-id="8e147-221">Consulte a <a href="lync-server-2013-edgeservers-table.md">tabela EdgeServers no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-221">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e147-222"><strong>ContentTypeid</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-222"><strong>ContentTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-223">int</span><span class="sxs-lookup"><span data-stu-id="8e147-223">int</span></span></p></td>
<td><p><span data-ttu-id="8e147-224">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-224">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-225">Tipo de conteúdo usado na sessão.</span><span class="sxs-lookup"><span data-stu-id="8e147-225">Content type used in the session.</span></span> <span data-ttu-id="8e147-226">Consulte a <a href="lync-server-2013-contenttypes-table.md">tabela ContentTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e147-226">See the <a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e147-227"><strong>Invitetime</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-227"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-228">datetime</span><span class="sxs-lookup"><span data-stu-id="8e147-228">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8e147-229">A hora da primeira solicitação INVITE.</span><span class="sxs-lookup"><span data-stu-id="8e147-229">The time of the first INVITE request.</span></span> <span data-ttu-id="8e147-230">Geralmente, esse campo é preenchido por dados gerados da mensagem de convite inicial na sessão.</span><span class="sxs-lookup"><span data-stu-id="8e147-230">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="8e147-231">Se não houver nenhuma mensagem de convite, o campo será preenchido com a data e a hora da primeira mensagem SIP relevante (até mais, cancelamento, mensagem ou informações).</span><span class="sxs-lookup"><span data-stu-id="8e147-231">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e147-232"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-232"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-233">datetime</span><span class="sxs-lookup"><span data-stu-id="8e147-233">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8e147-234">Hora da primeira resposta SIP.</span><span class="sxs-lookup"><span data-stu-id="8e147-234">Time of the first SIP RESPONSE.</span></span> <span data-ttu-id="8e147-235">Geralmente, esse campo é preenchido por dados gerados da mensagem de convite inicial na sessão.</span><span class="sxs-lookup"><span data-stu-id="8e147-235">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="8e147-236">Se não houver nenhuma mensagem de convite, o campo será preenchido com a data e a hora da primeira mensagem SIP relevante (até mais, cancelamento, mensagem ou informações).</span><span class="sxs-lookup"><span data-stu-id="8e147-236">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e147-237"><strong>SessionEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-237"><strong>SessionEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-238">datetime</span><span class="sxs-lookup"><span data-stu-id="8e147-238">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8e147-239">A hora de término da sessão.</span><span class="sxs-lookup"><span data-stu-id="8e147-239">The time when the session is ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e147-240"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-240"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-241">tinyint</span><span class="sxs-lookup"><span data-stu-id="8e147-241">tinyint</span></span></p></td>
<td><p><span data-ttu-id="8e147-242">Exterior</span><span class="sxs-lookup"><span data-stu-id="8e147-242">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8e147-243">Contém o valor do tipo URI de MCU da <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="8e147-243">Contains the MCU URI type value from the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a>.</span></span> <span data-ttu-id="8e147-244">Este campo é usado para melhorar o desempenho das consultas.</span><span class="sxs-lookup"><span data-stu-id="8e147-244">This field is used for improving query performance.</span></span></p>
<p><span data-ttu-id="8e147-245">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8e147-245">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e147-246"><strong>Sinalizador</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-246"><strong>UserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-247">smallint</span><span class="sxs-lookup"><span data-stu-id="8e147-247">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8e147-248">Um conjunto de bits que indica os atributos de usuário.</span><span class="sxs-lookup"><span data-stu-id="8e147-248">A bit set that indicates the user attributes.</span></span> <span data-ttu-id="8e147-249">As definições de atributo a seguir estão listadas:</span><span class="sxs-lookup"><span data-stu-id="8e147-249">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="8e147-250">Integrado ao telefone de mesa-1</span><span class="sxs-lookup"><span data-stu-id="8e147-250">Integrated with desktop phone - 1</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e147-251"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="8e147-251"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="8e147-252">smallint</span><span class="sxs-lookup"><span data-stu-id="8e147-252">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8e147-253">Um conjunto de bits que indica os atributos da chamada.</span><span class="sxs-lookup"><span data-stu-id="8e147-253">A bit set that indicates the call attributes.</span></span> <span data-ttu-id="8e147-254">As definições de atributo a seguir estão listadas:</span><span class="sxs-lookup"><span data-stu-id="8e147-254">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="8e147-255">Sessão 1 repetida</span><span class="sxs-lookup"><span data-stu-id="8e147-255">Retried Session - 1</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8e147-256">\* Para a maioria das sessões, o SessionIdSeq terá o valor de 1.</span><span class="sxs-lookup"><span data-stu-id="8e147-256">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="8e147-257">Se várias sessões começarem exatamente ao mesmo tempo, o SessionIdSeq de uma será 1, por outro será 2, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8e147-257">If multiple sessions start at exactly the same time, the SessionIdSeq for one will be 1, for another will be 2, and so on.</span></span>

<span data-ttu-id="8e147-258"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e147-258"></div>

<span> </span>

</div>

</div>

</span></span></div>

