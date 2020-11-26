---
title: 'Lync Server 2013: Tabela ErrorReport'
description: 'Lync Server 2013: ErrorReport Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorReport table
ms:assetid: ae0287b4-e8ca-4f8c-84ef-502897dcaa2a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412826(v=OCS.15)
ms:contentKeyID: 48185129
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c1cc65c396c16dc137255438f7ef7c32b2d0b78
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428514"
---
# <a name="errorreport-table-in-lync-server-2013"></a><span data-ttu-id="b673d-103">Tabela ErrorReport no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b673d-103">ErrorReport table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b673d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b673d-104">

<span> </span></span></span>

<span data-ttu-id="b673d-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="b673d-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="b673d-106">A tabela ErrorReport armazena informações sobre erros ocorridos.</span><span class="sxs-lookup"><span data-stu-id="b673d-106">The ErrorReport table stores information about errors that have occurred.</span></span> <span data-ttu-id="b673d-107">Cada registro é uma ocorrência de um erro.</span><span class="sxs-lookup"><span data-stu-id="b673d-107">Each record is one error occurrence.</span></span> <span data-ttu-id="b673d-108">Os erros são capturados pelo agente CDR executado no servidor front-end ou enviados do cliente.</span><span class="sxs-lookup"><span data-stu-id="b673d-108">The errors are captured either by the CDR agent running on the front-end server or sent from the client.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b673d-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="b673d-109">Column</span></span></th>
<th><span data-ttu-id="b673d-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b673d-110">Data Type</span></span></th>
<th><span data-ttu-id="b673d-111">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="b673d-111">Key/Index</span></span></th>
<th><span data-ttu-id="b673d-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="b673d-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b673d-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-114">datetime</span><span class="sxs-lookup"><span data-stu-id="b673d-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="b673d-115">Primária</span><span class="sxs-lookup"><span data-stu-id="b673d-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="b673d-116">Data e hora em que o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="b673d-116">Date and time the error occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b673d-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-118">int</span><span class="sxs-lookup"><span data-stu-id="b673d-118">int</span></span></p></td>
<td><p><span data-ttu-id="b673d-119">Primária</span><span class="sxs-lookup"><span data-stu-id="b673d-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="b673d-120">Número de identificação para identificar o relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="b673d-120">ID number to identify the error report.</span></span> <span data-ttu-id="b673d-121">Usado em conjunto com <strong>ErrorTime</strong> para identificar com exclusividade um relatório de erro.</span><span class="sxs-lookup"><span data-stu-id="b673d-121">Used in conjunction with <strong>ErrorTime</strong> to uniquely identify an error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b673d-122"><strong>ErrorID</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-122"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-123">int</span><span class="sxs-lookup"><span data-stu-id="b673d-123">int</span></span></p></td>
<td><p><span data-ttu-id="b673d-124">Exterior</span><span class="sxs-lookup"><span data-stu-id="b673d-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b673d-125">ID exclusiva do tipo de erro.</span><span class="sxs-lookup"><span data-stu-id="b673d-125">Unique ID of the error type.</span></span> <span data-ttu-id="b673d-126">Consulte a <a href="lync-server-2013-errordef-table.md">tabela ErrorDef no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b673d-126">See the <a href="lync-server-2013-errordef-table.md">ErrorDef table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b673d-127"><strong>FromUserId</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-127"><strong>FromUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-128">int</span><span class="sxs-lookup"><span data-stu-id="b673d-128">int</span></span></p></td>
<td><p><span data-ttu-id="b673d-129">Exterior</span><span class="sxs-lookup"><span data-stu-id="b673d-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b673d-130">Usuário que originou a solicitação que causou o erro.</span><span class="sxs-lookup"><span data-stu-id="b673d-130">User who originated the request that caused the error.</span></span> <span data-ttu-id="b673d-131">Consulte a <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b673d-131">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b673d-132"><strong>Parauserid</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-132"><strong>ToUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-133">int</span><span class="sxs-lookup"><span data-stu-id="b673d-133">int</span></span></p></td>
<td><p><span data-ttu-id="b673d-134">Exterior</span><span class="sxs-lookup"><span data-stu-id="b673d-134">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b673d-135">Usuário de destino para a solicitação que causou o erro.</span><span class="sxs-lookup"><span data-stu-id="b673d-135">Destination user for the request that caused the error.</span></span> <span data-ttu-id="b673d-136">Consulte a <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b673d-136">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b673d-137"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-137"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-138">int</span><span class="sxs-lookup"><span data-stu-id="b673d-138">int</span></span></p></td>
<td><p><span data-ttu-id="b673d-139">Exterior</span><span class="sxs-lookup"><span data-stu-id="b673d-139">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b673d-140">URL de conferência relacionada ao erro.</span><span class="sxs-lookup"><span data-stu-id="b673d-140">Conference URI related to the error.</span></span> <span data-ttu-id="b673d-141">Consulte a <a href="lync-server-2013-conferenceuris-table.md">tabela ConferenceUris no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b673d-141">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="b673d-142">Geralmente, se ConferenceUriId não for nulo, o FromUserId ou o parauserid será nulo.</span><span class="sxs-lookup"><span data-stu-id="b673d-142">Typically, if ConferenceUriId is not null, then either FromUserId or ToUserId will be null.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b673d-143"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-143"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-144">datetime</span><span class="sxs-lookup"><span data-stu-id="b673d-144">datetime</span></span></p></td>
<td><p><span data-ttu-id="b673d-145">Exterior</span><span class="sxs-lookup"><span data-stu-id="b673d-145">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b673d-146">Usado em conjunto com o <strong>SessionIdSeq</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="b673d-146">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="b673d-147">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b673d-147">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b673d-148"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-148"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-149">int</span><span class="sxs-lookup"><span data-stu-id="b673d-149">int</span></span></p></td>
<td><p><span data-ttu-id="b673d-150">Exterior</span><span class="sxs-lookup"><span data-stu-id="b673d-150">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b673d-151">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="b673d-151">ID number to identify the session.</span></span> <span data-ttu-id="b673d-152">Usado em conjunto com a <strong>identificação_da_sessãotime</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="b673d-152">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="b673d-153">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b673d-153">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b673d-154"><strong>SourceID</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-154"><strong>SourceId</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-155">int</span><span class="sxs-lookup"><span data-stu-id="b673d-155">int</span></span></p></td>
<td><p><span data-ttu-id="b673d-156">Exterior</span><span class="sxs-lookup"><span data-stu-id="b673d-156">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b673d-157">Servidor que enviou o relatório de erro (se o relatório estiver sendo enviado de um componente de servidor).</span><span class="sxs-lookup"><span data-stu-id="b673d-157">Server that sent the error report (if the report is being sent from a server component).</span></span> <span data-ttu-id="b673d-158">Consulte a <a href="lync-server-2013-servers-table.md">tabela servidores no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b673d-158">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="b673d-159">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b673d-159">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b673d-160"><strong>ApplicationId</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-160"><strong>ApplicationId</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-161">int</span><span class="sxs-lookup"><span data-stu-id="b673d-161">int</span></span></p></td>
<td><p><span data-ttu-id="b673d-162">Exterior</span><span class="sxs-lookup"><span data-stu-id="b673d-162">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b673d-163">Servidor que enviou o relatório de erro (se o relatório estiver sendo enviado de um componente de servidor).</span><span class="sxs-lookup"><span data-stu-id="b673d-163">Server that sent the error report (if the report is being sent from a server component).</span></span> <span data-ttu-id="b673d-164">Consulte a <a href="lync-server-2013-application-table.md">tabela de aplicativos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b673d-164">See the <a href="lync-server-2013-application-table.md">Application table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="b673d-165">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b673d-165">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b673d-166"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-166"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-167">imagem</span><span class="sxs-lookup"><span data-stu-id="b673d-167">image</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b673d-168">Mais informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="b673d-168">More information about the error.</span></span></p>
<p><span data-ttu-id="b673d-169">Esses dados podem ser convertidos em um formato de texto usando esta sintaxe:</span><span class="sxs-lookup"><span data-stu-id="b673d-169">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(Detail as varbinary(max)) as varchar(max)) </code></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b673d-170"><strong>ClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-170"><strong>ClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-171">int</span><span class="sxs-lookup"><span data-stu-id="b673d-171">int</span></span></p></td>
<td><p><span data-ttu-id="b673d-172">Exterior</span><span class="sxs-lookup"><span data-stu-id="b673d-172">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b673d-173">A versão do cliente do ponto de extremidade que envia o relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="b673d-173">The client version of endpoint that sends the error report.</span></span> <span data-ttu-id="b673d-174">Consulte a <a href="lync-server-2013-clientversions-table.md">tabela ClientVersions no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b673d-174">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b673d-175"><strong>IsCapturedByServer</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-175"><strong>IsCapturedByServer</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-176">bit</span><span class="sxs-lookup"><span data-stu-id="b673d-176">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b673d-177">É o relatório de erros capturado pelo agente CDR em execução no servidor front-end ou enviado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="b673d-177">Is the error report captured by the CDR agent running on the front-end server, or sent by the client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b673d-178"><strong>Sinalizador</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-178"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-179">smallint</span><span class="sxs-lookup"><span data-stu-id="b673d-179">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b673d-180">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="b673d-180">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b673d-181"><strong>Telemetria</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-181"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-182">Identificador</span><span class="sxs-lookup"><span data-stu-id="b673d-182">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b673d-183">Identificador exclusivo que correlaciona as informações de tempo de junção para os diferentes componentes envolvidos em uma conferência.</span><span class="sxs-lookup"><span data-stu-id="b673d-183">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p>
<p><span data-ttu-id="b673d-184">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b673d-184">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b673d-185"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-185"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-186">int</span><span class="sxs-lookup"><span data-stu-id="b673d-186">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b673d-187">Tempo (em milissegundos) necessário para um componente específico entrar em uma conferência.</span><span class="sxs-lookup"><span data-stu-id="b673d-187">Time (in milliseconds) required for a specific component to join a conference.</span></span></p>
<p><span data-ttu-id="b673d-188">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b673d-188">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b673d-189"><strong>ServerID</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-189"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-190">int</span><span class="sxs-lookup"><span data-stu-id="b673d-190">int</span></span></p></td>
<td><p><span data-ttu-id="b673d-191">Exterior</span><span class="sxs-lookup"><span data-stu-id="b673d-191">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b673d-192">Representa o nome de domínio totalmente qualificado do servidor que gerou o relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="b673d-192">Represents the fully qualified domain name of the server that generated the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b673d-193"><strong>Poolid</strong></span><span class="sxs-lookup"><span data-stu-id="b673d-193"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="b673d-194">int</span><span class="sxs-lookup"><span data-stu-id="b673d-194">int</span></span></p></td>
<td><p><span data-ttu-id="b673d-195">Exterior</span><span class="sxs-lookup"><span data-stu-id="b673d-195">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b673d-196">Representa o nome de domínio totalmente qualificado do pool onde o relatório de erro foi gerado.</span><span class="sxs-lookup"><span data-stu-id="b673d-196">Represents the fully qualified domain name of the pool where the error report was generated.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b673d-197">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b673d-197">


</div>

<span> </span>

</div>

</div>

</span></span></div>

