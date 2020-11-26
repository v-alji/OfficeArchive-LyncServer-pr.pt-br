---
title: 'Lync Server 2013: modo de exibição ProgressReport'
description: 'Lync Server 2013: modo de exibição ProgressReport.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ProgressReport view
ms:assetid: b49f3fc7-0e2f-498f-8505-aaaf54e435f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721857(v=OCS.15)
ms:contentKeyID: 49733790
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b95086012f254499644e778e43cafdf70ffc8f9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436850"
---
# <a name="progressreport-view-in-lync-server-2013"></a><span data-ttu-id="a0334-103">Exibição ProgressReport no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0334-103">ProgressReport view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0334-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0334-104">

<span> </span></span></span>

<span data-ttu-id="a0334-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="a0334-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="a0334-106">A exibição ProgressReport armazena informações sobre sessões concluídas.</span><span class="sxs-lookup"><span data-stu-id="a0334-106">The ProgressReport view stores information about completed sessions.</span></span> <span data-ttu-id="a0334-107">Os relatórios de progresso serão escritos apenas para chamadas e sessões que o Lync Server 2013 determina que podem ser úteis para fins de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="a0334-107">Progress reports will be written only for calls and sessions that Lync Server 2013 determines might be useful for diagnostic purposes.</span></span> <span data-ttu-id="a0334-108">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a0334-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a0334-109">Os campos ErrorTime, ErrorReportSeq e ProgressReportSeq não se referem necessariamente a erros, mas a mensagens que indicam o status de chamadas ou mensagens.</span><span class="sxs-lookup"><span data-stu-id="a0334-109">The ErrorTime, ErrorReportSeq and ProgressReportSeq fields don’t necessarily refer to errors but to messages that indicate the status of calls or messages.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0334-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="a0334-110">Column</span></span></th>
<th><span data-ttu-id="a0334-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a0334-111">Data Type</span></span></th>
<th><span data-ttu-id="a0334-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="a0334-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0334-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="a0334-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a0334-114">datetime</span><span class="sxs-lookup"><span data-stu-id="a0334-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="a0334-115">Ocorreu um erro de hora.</span><span class="sxs-lookup"><span data-stu-id="a0334-115">Time of error occurred.</span></span> <span data-ttu-id="a0334-116">Usado em conjunto com ErrorReportSeq para identificar um erro exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="a0334-116">Used in conjunction with ErrorReportSeq to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0334-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="a0334-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="a0334-118">int</span><span class="sxs-lookup"><span data-stu-id="a0334-118">int</span></span></p></td>
<td><p><span data-ttu-id="a0334-119">Número de identificação para identificar o erro.</span><span class="sxs-lookup"><span data-stu-id="a0334-119">ID number to identify the error.</span></span> <span data-ttu-id="a0334-120">Usado em conjunto com ErrorTime para identificar um erro com exclusividade.</span><span class="sxs-lookup"><span data-stu-id="a0334-120">Used in conjunction with ErrorTime to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0334-121"><strong>ProgressReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="a0334-121"><strong>ProgressReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="a0334-122">int</span><span class="sxs-lookup"><span data-stu-id="a0334-122">int</span></span></p></td>
<td><p><span data-ttu-id="a0334-123">ID para identificar o relatório de progresso.</span><span class="sxs-lookup"><span data-stu-id="a0334-123">ID to identify the progress report.</span></span> <span data-ttu-id="a0334-124">Usado para distinguir relatórios de progresso do mesmo relatório de erro.</span><span class="sxs-lookup"><span data-stu-id="a0334-124">Used to distinguish progress reports of the same error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0334-125"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="a0334-125"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="a0334-126">int</span><span class="sxs-lookup"><span data-stu-id="a0334-126">int</span></span></p></td>
<td><p><span data-ttu-id="a0334-127">ID de diagnóstico do relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="a0334-127">Diagnostic ID for the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0334-128"><strong>Origem</strong></span><span class="sxs-lookup"><span data-stu-id="a0334-128"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="a0334-129">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="a0334-129">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="a0334-130">Nome do servidor que originou o erro (se o relatório foi enviado a partir de um componente de servidor).</span><span class="sxs-lookup"><span data-stu-id="a0334-130">Name of server that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0334-131"><strong>Aplicativo</strong></span><span class="sxs-lookup"><span data-stu-id="a0334-131"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="a0334-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="a0334-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="a0334-133">Nome do aplicativo que originou o erro (se o relatório foi enviado a partir de um componente de servidor).</span><span class="sxs-lookup"><span data-stu-id="a0334-133">Name of application that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0334-134"><strong>Telemetria</strong></span><span class="sxs-lookup"><span data-stu-id="a0334-134"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="a0334-135">identificador</span><span class="sxs-lookup"><span data-stu-id="a0334-135">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="a0334-136">Identificador exclusivo que correlaciona as informações de tempo de junção para os diferentes componentes envolvidos em uma conferência.</span><span class="sxs-lookup"><span data-stu-id="a0334-136">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0334-137"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="a0334-137"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a0334-138">int</span><span class="sxs-lookup"><span data-stu-id="a0334-138">int</span></span></p></td>
<td><p><span data-ttu-id="a0334-139">Tempo (em milissegundos) necessário para um componente específico entrar em uma conferência.</span><span class="sxs-lookup"><span data-stu-id="a0334-139">Time (in milliseconds) required for a specific component to join a conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0334-140"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="a0334-140"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="a0334-141">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="a0334-141">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="a0334-142">Informações adicionais sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="a0334-142">Additional error information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a0334-143">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0334-143">


</div>

<span> </span>

</div>

</div>

</span></span></div>

