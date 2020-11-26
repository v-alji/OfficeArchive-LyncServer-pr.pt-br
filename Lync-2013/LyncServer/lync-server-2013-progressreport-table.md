---
title: 'Lync Server 2013: Tabela ProgressReport'
description: 'Lync Server 2013: ProgressReport Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ProgressReport table
ms:assetid: 38e5f060-5e9b-4185-87b2-7ef61c4bb75f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425864(v=OCS.15)
ms:contentKeyID: 48183847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d36ee2ab75410ea2462da4b647ef5b45afefb1bb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436864"
---
# <a name="progressreport-table-in-lync-server-2013"></a><span data-ttu-id="3c73e-103">Tabela ProgressReport no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3c73e-103">ProgressReport table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3c73e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3c73e-104">

<span> </span></span></span>

<span data-ttu-id="3c73e-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="3c73e-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="3c73e-106">Os relatórios de progresso são baseados em dados carregados pelo cliente para o banco de dados após a conclusão de uma chamada ou sessão.</span><span class="sxs-lookup"><span data-stu-id="3c73e-106">Progress reports are based on data uploaded by the client to the database after a call or session is completed.</span></span> <span data-ttu-id="3c73e-107">Os relatórios de progresso serão escritos apenas para chamadas e sessões que o Lync Server 2013 determina que podem ser úteis para fins de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="3c73e-107">Progress reports will be written only for calls and sessions that Lync Server 2013 determines might be useful for diagnostic purposes.</span></span>

<span data-ttu-id="3c73e-108">Os campos ErrorTime, ErrorReportSeq e ProgressReportSeq não se referem necessariamente a erros, mas a mensagens que indicam o status de chamadas ou mensagens.</span><span class="sxs-lookup"><span data-stu-id="3c73e-108">The ErrorTime, ErrorReportSeq and ProgressReportSeq fields don’t necessarily refer to errors but to messages that indicate the status of calls or messages.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3c73e-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="3c73e-109">Column</span></span></th>
<th><span data-ttu-id="3c73e-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3c73e-110">Data Type</span></span></th>
<th><span data-ttu-id="3c73e-111">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="3c73e-111">Key/Index</span></span></th>
<th><span data-ttu-id="3c73e-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="3c73e-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c73e-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="3c73e-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="3c73e-114">datetime</span><span class="sxs-lookup"><span data-stu-id="3c73e-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="3c73e-115">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="3c73e-115">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="3c73e-116">Data e hora do relatório de erro de progresso que contém este relatório de progresso.</span><span class="sxs-lookup"><span data-stu-id="3c73e-116">Date and time of the progress error report that contains this progress report.</span></span> <span data-ttu-id="3c73e-117">Consulte a <a href="lync-server-2013-errorreport-table.md">tabela errorreport no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="3c73e-117">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c73e-118"><strong>ErrorID</strong></span><span class="sxs-lookup"><span data-stu-id="3c73e-118"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="3c73e-119">int</span><span class="sxs-lookup"><span data-stu-id="3c73e-119">int</span></span></p></td>
<td><p><span data-ttu-id="3c73e-120">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="3c73e-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="3c73e-121">Número de identificação usado em conjunto com ErrorTime, ProgressReportSeq para identificar exclusivamente um relatório de progresso.</span><span class="sxs-lookup"><span data-stu-id="3c73e-121">ID number used in conjunction with ErrorTime, ProgressReportSeq to uniquely identify a progress report.</span></span> <span data-ttu-id="3c73e-122">Consulte a <a href="lync-server-2013-errorreport-table.md">tabela errorreport no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="3c73e-122">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c73e-123"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="3c73e-123"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="3c73e-124">int</span><span class="sxs-lookup"><span data-stu-id="3c73e-124">int</span></span></p></td>
<td><p><span data-ttu-id="3c73e-125">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="3c73e-125">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="3c73e-126">Número de identificação que identifica o relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="3c73e-126">ID number that identifies the error report.</span></span> <span data-ttu-id="3c73e-127">ErrorReporSeq é usado em conjunto com ErrorTime para identificar com exclusividade um relatório de erro.</span><span class="sxs-lookup"><span data-stu-id="3c73e-127">ErrorReporSeq is used in conjunction with ErrorTime to uniquely identify an error report.</span></span> <span data-ttu-id="3c73e-128">Consulte a <a href="lync-server-2013-errorreport-table.md">tabela errorreport no Lync Server 2013</a> para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="3c73e-128">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information</span></span></p>
<p><span data-ttu-id="3c73e-129">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3c73e-129">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c73e-130"><strong>ProgressReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="3c73e-130"><strong>ProgressReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="3c73e-131">int</span><span class="sxs-lookup"><span data-stu-id="3c73e-131">int</span></span></p></td>
<td><p><span data-ttu-id="3c73e-132">Primária</span><span class="sxs-lookup"><span data-stu-id="3c73e-132">Primary</span></span></p></td>
<td><p><span data-ttu-id="3c73e-133">Número de identificação para identificar o relatório de progresso.</span><span class="sxs-lookup"><span data-stu-id="3c73e-133">ID number to identify the progress report.</span></span> <span data-ttu-id="3c73e-134">Usado em conjunto com ErrorTime e ErrorReportSeq para identificar com exclusividade um relatório de progresso.</span><span class="sxs-lookup"><span data-stu-id="3c73e-134">Used in conjunction with ErrorTime and ErrorReportSeq to uniquely identify a progress report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c73e-135"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="3c73e-135"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="3c73e-136">int</span><span class="sxs-lookup"><span data-stu-id="3c73e-136">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3c73e-137">ID de diagnóstico do relatório de progresso.</span><span class="sxs-lookup"><span data-stu-id="3c73e-137">Diagnostic ID of the progress report.</span></span></p>
<p><span data-ttu-id="3c73e-138">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3c73e-138">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c73e-139"><strong>SourceID</strong></span><span class="sxs-lookup"><span data-stu-id="3c73e-139"><strong>SourceId</strong></span></span></p></td>
<td><p><span data-ttu-id="3c73e-140">int</span><span class="sxs-lookup"><span data-stu-id="3c73e-140">int</span></span></p></td>
<td><p><span data-ttu-id="3c73e-141">Exterior</span><span class="sxs-lookup"><span data-stu-id="3c73e-141">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3c73e-142">Servidor que enviou o relatório de erro (se o relatório foi enviado de um componente de servidor).</span><span class="sxs-lookup"><span data-stu-id="3c73e-142">Server that sent the error report (if the report was sent from a server component).</span></span> <span data-ttu-id="3c73e-143">Consulte a <a href="lync-server-2013-servers-table.md">tabela servidores no Lync Server 2013</a> para obter mais informações. Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3c73e-143">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c73e-144"><strong>ApplicationId</strong></span><span class="sxs-lookup"><span data-stu-id="3c73e-144"><strong>ApplicationId</strong></span></span></p></td>
<td><p><span data-ttu-id="3c73e-145">int</span><span class="sxs-lookup"><span data-stu-id="3c73e-145">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3c73e-146">O processo do Lync Server no qual o relatório se encontra.</span><span class="sxs-lookup"><span data-stu-id="3c73e-146">The Lync Server process that the report is about.</span></span> <span data-ttu-id="3c73e-147">Consulte a tabela de aplicativos para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="3c73e-147">See the Application Table for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c73e-148"><strong>Detalhe</strong></span><span class="sxs-lookup"><span data-stu-id="3c73e-148"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="3c73e-149">imagem</span><span class="sxs-lookup"><span data-stu-id="3c73e-149">image</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3c73e-150">Detalhes do relatório de progresso armazenados em formato binário para economizar espaço. Esses dados podem ser convertidos em um formato de texto usando esta sintaxe:</span><span class="sxs-lookup"><span data-stu-id="3c73e-150">Progress report details, stored in binary format to save space.This data can be converted to text format using this syntax:</span></span></p>
<p><span data-ttu-id="3c73e-151">Cast (Cast (detalhes como varbinary (max)) as varchar (max))</span><span class="sxs-lookup"><span data-stu-id="3c73e-151">cast(cast(Detail as varbinary(max)) as varchar(max))</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c73e-152"><strong>Telemetria</strong></span><span class="sxs-lookup"><span data-stu-id="3c73e-152"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="3c73e-153">Identificador</span><span class="sxs-lookup"><span data-stu-id="3c73e-153">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3c73e-154">Identificador exclusivo que correlaciona as informações de tempo de junção para os diferentes componentes envolvidos em uma conferência.</span><span class="sxs-lookup"><span data-stu-id="3c73e-154">Unique identifier that correlates join time information for the different components involved in a conference.</span></span></p>
<p><span data-ttu-id="3c73e-155">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3c73e-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c73e-156"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="3c73e-156"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="3c73e-157">int</span><span class="sxs-lookup"><span data-stu-id="3c73e-157">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3c73e-158">Tempo (em milissegundos) para um componente específico para ingressar em uma conferência.</span><span class="sxs-lookup"><span data-stu-id="3c73e-158">Time (in milliseconds) for a specific component to join a conference.</span></span></p>
<p><span data-ttu-id="3c73e-159">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3c73e-159">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3c73e-160">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3c73e-160">


</div>

<span> </span>

</div>

</div>

</span></span></div>

