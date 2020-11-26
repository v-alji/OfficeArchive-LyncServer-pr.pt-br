---
title: 'Lync Server 2013: modo de exibição ErrorReport'
description: 'Lync Server 2013: modo de exibição ErrorReport.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorReport view
ms:assetid: ca873f7e-b18b-4eaf-8db0-5f9d5a9b60a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721887(v=OCS.15)
ms:contentKeyID: 49733821
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50fb0a362c71d8dfb5873157e7b1ed3d3eb680ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428521"
---
# <a name="errorreport-view-in-lync-server-2013"></a><span data-ttu-id="382c2-103">Exibição ErrorReport no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="382c2-103">ErrorReport view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="382c2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="382c2-104">

<span> </span></span></span>

<span data-ttu-id="382c2-105">_**Tópico da última modificação:** 2013-01-22_</span><span class="sxs-lookup"><span data-stu-id="382c2-105">_**Topic Last Modified:** 2013-01-22_</span></span>

<span data-ttu-id="382c2-106">A exibição ErrorReport armazena informações sobre erros relatados.</span><span class="sxs-lookup"><span data-stu-id="382c2-106">The ErrorReport view stores information about errors reported.</span></span> <span data-ttu-id="382c2-107">Cada registro é uma ocorrência de um erro.</span><span class="sxs-lookup"><span data-stu-id="382c2-107">Each record is one error occurrence.</span></span> <span data-ttu-id="382c2-108">Os erros são capturados pelo agente CDR executado no servidor front-end ou enviados do cliente.</span><span class="sxs-lookup"><span data-stu-id="382c2-108">The errors are captured either by the CDR agent running on the front-end server or sent from the client.</span></span> <span data-ttu-id="382c2-109">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="382c2-109">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="382c2-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="382c2-110">Column</span></span></th>
<th><span data-ttu-id="382c2-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="382c2-111">Data Type</span></span></th>
<th><span data-ttu-id="382c2-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="382c2-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="382c2-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-114">datetime</span><span class="sxs-lookup"><span data-stu-id="382c2-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="382c2-115">Ocorreu um erro de hora.</span><span class="sxs-lookup"><span data-stu-id="382c2-115">Time of error occurred.</span></span> <span data-ttu-id="382c2-116">Usado em conjunto com ErrorReportSeq para identificar um erro exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="382c2-116">Used in conjunction with ErrorReportSeq to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="382c2-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-118">int</span><span class="sxs-lookup"><span data-stu-id="382c2-118">int</span></span></p></td>
<td><p><span data-ttu-id="382c2-119">Número de identificação para identificar o erro.</span><span class="sxs-lookup"><span data-stu-id="382c2-119">ID number to identify the error.</span></span> <span data-ttu-id="382c2-120">Usado em conjunto com ErrorTime para identificar um erro com exclusividade.</span><span class="sxs-lookup"><span data-stu-id="382c2-120">Used in conjunction with ErrorTime to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="382c2-121"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-121"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-122">int</span><span class="sxs-lookup"><span data-stu-id="382c2-122">int</span></span></p></td>
<td><p><span data-ttu-id="382c2-123">ID de diagnóstico do relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="382c2-123">Diagnostic ID for the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="382c2-124"><strong>FromUri</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-124"><strong>FromUri</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-125">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="382c2-125">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="382c2-126">URL do usuário que originou o erro.</span><span class="sxs-lookup"><span data-stu-id="382c2-126">URI of the user who originated the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="382c2-127"><strong>FromUriType</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-127"><strong>FromUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="382c2-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="382c2-129">Tipo de URI do usuário que originou o erro.</span><span class="sxs-lookup"><span data-stu-id="382c2-129">Type of URI of the user who originated the error.</span></span> <span data-ttu-id="382c2-130">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="382c2-130">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="382c2-131"><strong>FromTenant</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-131"><strong>FromTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="382c2-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="382c2-133">Locatário do usuário que originou o erro.</span><span class="sxs-lookup"><span data-stu-id="382c2-133">Tenant of the user who originated the error.</span></span> <span data-ttu-id="382c2-134">Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="382c2-134">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="382c2-135"><strong>ToUri</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-135"><strong>ToUri</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-136">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="382c2-136">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="382c2-137">URI do usuário que foi o destino do relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="382c2-137">URI of the user who was the target of the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="382c2-138"><strong>ToUriType</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-138"><strong>ToUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-139">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="382c2-139">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="382c2-140">Tipo de URI do usuário que direciona o relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="382c2-140">Type of URI of the user who target of the error report.</span></span> <span data-ttu-id="382c2-141">Consulte a tabela UriTypes para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="382c2-141">See the UriTypes Table for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="382c2-142"><strong>Tolocatário</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-142"><strong>ToTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-143">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="382c2-143">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="382c2-144">Locatário do usuário que direciona o relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="382c2-144">Tenant of the user who target of the error report.</span></span> <span data-ttu-id="382c2-145">Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="382c2-145">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="382c2-146"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-146"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="382c2-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="382c2-148">URL da conferência que foi o alvo do relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="382c2-148">URI of the conference that was the target of the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="382c2-149"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-149"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="382c2-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="382c2-151">Tipo de URI da conferência que foi o destino do relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="382c2-151">URI type of the conference that was the target of the error report.</span></span> <span data-ttu-id="382c2-152">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="382c2-152">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="382c2-153"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-153"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-154">datetime</span><span class="sxs-lookup"><span data-stu-id="382c2-154">datetime</span></span></p></td>
<td><p><span data-ttu-id="382c2-155">Tempo de solicitação de sessão que originou o relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="382c2-155">Time of session request that originated the error report.</span></span> <span data-ttu-id="382c2-156">Usado em conjunto com o SessionIdSeq para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="382c2-156">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="382c2-157">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="382c2-157">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="382c2-158"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-158"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-159">int</span><span class="sxs-lookup"><span data-stu-id="382c2-159">int</span></span></p></td>
<td><p><span data-ttu-id="382c2-160">Número de identificação para identificar a solicitação de sessão que originou o relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="382c2-160">ID number to identify the session request that originated the error report.</span></span> <span data-ttu-id="382c2-161">Usado em conjunto com a Identificação_da_sessãotime para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="382c2-161">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="382c2-162">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="382c2-162">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="382c2-163"><strong>Caixa de diálogo</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-163"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-164">VARSTRING (775)</span><span class="sxs-lookup"><span data-stu-id="382c2-164">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="382c2-165">ID da caixa de diálogo SIP da sessão que originou o erro.</span><span class="sxs-lookup"><span data-stu-id="382c2-165">SIP dialog ID of session that originated the error.</span></span> <span data-ttu-id="382c2-166">O formato é:</span><span class="sxs-lookup"><span data-stu-id="382c2-166">The format is:</span></span></p>
<p><span data-ttu-id="382c2-167">caixa de diálogo; de-marca; até-marca</span><span class="sxs-lookup"><span data-stu-id="382c2-167">dialog;from-tag;to-tag</span></span></p>
<p><span data-ttu-id="382c2-168">Esses dados podem ser convertidos em um formato de texto usando esta sintaxe:</span><span class="sxs-lookup"><span data-stu-id="382c2-168">This data can be converted to text format by using this syntax:</span></span></p>
<p><span data-ttu-id="382c2-169">Cast (castid (externalId como varbinary (max)) como varchar (max))</span><span class="sxs-lookup"><span data-stu-id="382c2-169">cast(cast(ExternalId as varbinary(max)) as varchar(max))</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="382c2-170"><strong>ClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-170"><strong>ClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-171">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="382c2-171">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="382c2-172">Versão do cliente usada pelo usuário que originou o erro.</span><span class="sxs-lookup"><span data-stu-id="382c2-172">Version of client used by the user who originated the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="382c2-173"><strong>ClientType</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-173"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-174">int</span><span class="sxs-lookup"><span data-stu-id="382c2-174">int</span></span></p></td>
<td><p><span data-ttu-id="382c2-175">Cliente usado pelo usuário que originou o erro.</span><span class="sxs-lookup"><span data-stu-id="382c2-175">Client used by the user who originated the error.</span></span> <span data-ttu-id="382c2-176">Consulte a <a href="lync-server-2013-useragentdef-table.md">tabela UserAgentDef no Lync Server 2013</a> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="382c2-176">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="382c2-177"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-177"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-178">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="382c2-178">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="382c2-179">Nome da categoria do cliente usado pelo usuário que originou o erro.</span><span class="sxs-lookup"><span data-stu-id="382c2-179">Name of the category of the client used by the user who originated the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="382c2-180"><strong>Origem</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-180"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-181">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="382c2-181">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="382c2-182">Nome do servidor que originou o erro (se o relatório foi enviado a partir de um componente de servidor).</span><span class="sxs-lookup"><span data-stu-id="382c2-182">Name of server that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="382c2-183"><strong>Aplicativo</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-183"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-184">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="382c2-184">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="382c2-185">Nome do aplicativo que originou o erro (se o relatório foi enviado a partir de um componente de servidor).</span><span class="sxs-lookup"><span data-stu-id="382c2-185">Name of application that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="382c2-186"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-186"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-187">int</span><span class="sxs-lookup"><span data-stu-id="382c2-187">int</span></span></p></td>
<td><p><span data-ttu-id="382c2-188">Código de resposta SIP para a sessão da mensagem SIP que contém o relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="382c2-188">SIP response code to the session of the SIP message containing the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="382c2-189"><strong>RequestType</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-189"><strong>RequestType</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-190">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="382c2-190">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="382c2-191">Tipo de solicitação que falhou.</span><span class="sxs-lookup"><span data-stu-id="382c2-191">Type of request that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="382c2-192"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-192"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-193">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="382c2-193">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="382c2-194">Tipo de conteúdo da solicitação que falhou.</span><span class="sxs-lookup"><span data-stu-id="382c2-194">Content type of the request that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="382c2-195"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-195"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="382c2-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="382c2-197">Tipo de sessão.</span><span class="sxs-lookup"><span data-stu-id="382c2-197">Type of session.</span></span> <span data-ttu-id="382c2-198">Consulte a <a href="lync-server-2013-calltype-table.md">tabela CallType no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="382c2-198">See the <a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="382c2-199"><strong>Telemetria</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-199"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-200">identificador</span><span class="sxs-lookup"><span data-stu-id="382c2-200">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="382c2-201">Identificador exclusivo que correlaciona as informações de tempo de junção para os diferentes componentes envolvidos em uma conferência.</span><span class="sxs-lookup"><span data-stu-id="382c2-201">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="382c2-202"><strong>Setuptime</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-202"><strong>SetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-203">int</span><span class="sxs-lookup"><span data-stu-id="382c2-203">int</span></span></p></td>
<td><p><span data-ttu-id="382c2-204">Tempo (em milissegundos) necessário para um componente específico entrar em uma conferência.</span><span class="sxs-lookup"><span data-stu-id="382c2-204">Time (in milliseconds) required for a specific component to join a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="382c2-205"><strong>IsCapturedByServer</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-205"><strong>IsCapturedByServer</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-206">bit</span><span class="sxs-lookup"><span data-stu-id="382c2-206">bit</span></span></p></td>
<td><p><span data-ttu-id="382c2-207">Indica se o relatório de erros foi capturado pelo agente CDR em execução no servidor front-end ou enviado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="382c2-207">Indicates whether the error report was captured by the CDR agent running on the Front End server, or sent by the client.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="382c2-208"><strong>Sinalizador</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-208"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-209">smallint</span><span class="sxs-lookup"><span data-stu-id="382c2-209">smallint</span></span></p></td>
<td><p><span data-ttu-id="382c2-210">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="382c2-210">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="382c2-211"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-211"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-212">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="382c2-212">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="382c2-213">Informações adicionais sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="382c2-213">Additional information about the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="382c2-214"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-214"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-215">nvarchar</span><span class="sxs-lookup"><span data-stu-id="382c2-215">nvarchar</span></span></p></td>
<td><p><span data-ttu-id="382c2-216">Nome de domínio totalmente qualificado do servidor front-end que enviou o relatório.</span><span class="sxs-lookup"><span data-stu-id="382c2-216">Fully qualified domain name of the Front End server that submitted the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="382c2-217"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="382c2-217"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="382c2-218">nvarchar</span><span class="sxs-lookup"><span data-stu-id="382c2-218">nvarchar</span></span></p></td>
<td><p><span data-ttu-id="382c2-219">Nome de domínio totalmente qualificado do pool que contém o servidor front-end que enviou o relatório.</span><span class="sxs-lookup"><span data-stu-id="382c2-219">Fully qualified domain name of the pool containing the Front End server that submitted the report.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="382c2-220">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="382c2-220">


</div>

<span> </span>

</div>

</div>

</span></span></div>

