---
title: 'Lync Server 2013: tabela IMReportSummary'
description: 'Lync Server 2013: IMReportSummary Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IMReportSummary table
ms:assetid: 27ff9453-53f2-4fae-b637-70a086c9df96
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204753(v=OCS.15)
ms:contentKeyID: 48183673
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dfafa81d1605845b29a3627321fcbc0f72ca7ac7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427310"
---
# <a name="imreportsummary-table-in-lync-server-2013"></a><span data-ttu-id="8ddd8-103">Tabela IMReportSummary no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ddd8-103">IMReportSummary table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ddd8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ddd8-104">

<span> </span></span></span>

<span data-ttu-id="8ddd8-105">_**Tópico da última modificação:** 2012-08-20_</span><span class="sxs-lookup"><span data-stu-id="8ddd8-105">_**Topic Last Modified:** 2012-08-20_</span></span>

<span data-ttu-id="8ddd8-106">O IMReportSummaryTable fornece um relatório geral sobre as sessões de mensagens instantâneas contidas em uma organização.</span><span class="sxs-lookup"><span data-stu-id="8ddd8-106">The IMReportSummaryTable provides an overall report on the instant messaging sessions held in an organization.</span></span> <span data-ttu-id="8ddd8-107">Esta tabela foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8ddd8-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ddd8-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="8ddd8-108">Column</span></span></th>
<th><span data-ttu-id="8ddd8-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8ddd8-109">Data Type</span></span></th>
<th><span data-ttu-id="8ddd8-110">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="8ddd8-110">Key/Index</span></span></th>
<th><span data-ttu-id="8ddd8-111">Detalhes</span><span class="sxs-lookup"><span data-stu-id="8ddd8-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ddd8-112"><strong>StartTime </strong></span><span class="sxs-lookup"><span data-stu-id="8ddd8-112"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddd8-113">datetime</span><span class="sxs-lookup"><span data-stu-id="8ddd8-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="8ddd8-114">Primária</span><span class="sxs-lookup"><span data-stu-id="8ddd8-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="8ddd8-115">Data e hora de início da sessão de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="8ddd8-115">Date and time that the instant messaging session began.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddd8-116"><strong>Período de tempo</strong></span><span class="sxs-lookup"><span data-stu-id="8ddd8-116"><strong>TimePeriod</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddd8-117">caractere (1)</span><span class="sxs-lookup"><span data-stu-id="8ddd8-117">char(1)</span></span></p></td>
<td><p><span data-ttu-id="8ddd8-118">Primária</span><span class="sxs-lookup"><span data-stu-id="8ddd8-118">Primary</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddd8-119"><strong>PoolFQDN</strong></span><span class="sxs-lookup"><span data-stu-id="8ddd8-119"><strong>PoolFQDN</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddd8-120">nvarchar (257)</span><span class="sxs-lookup"><span data-stu-id="8ddd8-120">nvarchar(257)</span></span></p></td>
<td><p><span data-ttu-id="8ddd8-121">Primária</span><span class="sxs-lookup"><span data-stu-id="8ddd8-121">Primary</span></span></p></td>
<td><p><span data-ttu-id="8ddd8-122">Nome de domínio totalmente qualificado do pool que hospeda a sessão.</span><span class="sxs-lookup"><span data-stu-id="8ddd8-122">Fully qualified domain name of the pool hosting the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddd8-123"><strong>AuthType</strong></span><span class="sxs-lookup"><span data-stu-id="8ddd8-123"><strong>AuthType</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddd8-124">int</span><span class="sxs-lookup"><span data-stu-id="8ddd8-124">int</span></span></p></td>
<td><p><span data-ttu-id="8ddd8-125">Primária</span><span class="sxs-lookup"><span data-stu-id="8ddd8-125">Primary</span></span></p></td>
<td><p><span data-ttu-id="8ddd8-126">Prioridade (por exemplo, urgente ou não urgente) da chamada.</span><span class="sxs-lookup"><span data-stu-id="8ddd8-126">Priority (for example, urgent or non-urgent) of the call.</span></span> <span data-ttu-id="8ddd8-127">As informações de prioridade são armazenadas na <a href="lync-server-2013-callpriorities-table.md">tabela CallPriorities no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="8ddd8-127">Priority information is stored in the <a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddd8-128"><strong>SessionCount</strong></span><span class="sxs-lookup"><span data-stu-id="8ddd8-128"><strong>SessionCount</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddd8-129">bigint</span><span class="sxs-lookup"><span data-stu-id="8ddd8-129">bigint</span></span></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddd8-130"><strong>MsgCount</strong></span><span class="sxs-lookup"><span data-stu-id="8ddd8-130"><strong>MsgCount</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddd8-131">bigint</span><span class="sxs-lookup"><span data-stu-id="8ddd8-131">bigint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8ddd8-132">Número total de mensagens instantâneas trocadas durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="8ddd8-132">Total number of instant messages exchanged during the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8ddd8-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ddd8-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

