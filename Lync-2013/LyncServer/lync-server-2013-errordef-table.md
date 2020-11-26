---
title: 'Lync Server 2013: Tabela ErrorDef'
description: 'Lync Server 2013: ErrorDef Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorDef table
ms:assetid: 6acf3b86-da61-4923-9812-300db6f66dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398503(v=OCS.15)
ms:contentKeyID: 48184403
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e58980a671b54007012bbbf6780e24c162aebe00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428535"
---
# <a name="errordef-table-in-lync-server-2013"></a><span data-ttu-id="96eb1-103">Tabela ErrorDef no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96eb1-103">ErrorDef table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="96eb1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="96eb1-104">

<span> </span></span></span>

<span data-ttu-id="96eb1-105">_**Tópico da última modificação:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="96eb1-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="96eb1-106">A tabela ErrorDef armazena informações sobre cada tipo de erro que pode ocorrer.</span><span class="sxs-lookup"><span data-stu-id="96eb1-106">The ErrorDef table stores information about each type of error that may occur.</span></span> <span data-ttu-id="96eb1-107">Cada registro é um tipo de erro.</span><span class="sxs-lookup"><span data-stu-id="96eb1-107">Each record is one type of error.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96eb1-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="96eb1-108">Column</span></span></th>
<th><span data-ttu-id="96eb1-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="96eb1-109">Data Type</span></span></th>
<th><span data-ttu-id="96eb1-110">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="96eb1-110">Key/Index</span></span></th>
<th><span data-ttu-id="96eb1-111">Detalhes</span><span class="sxs-lookup"><span data-stu-id="96eb1-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96eb1-112"><strong>ErrorID</strong></span><span class="sxs-lookup"><span data-stu-id="96eb1-112"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="96eb1-113">int</span><span class="sxs-lookup"><span data-stu-id="96eb1-113">int</span></span></p></td>
<td><p><span data-ttu-id="96eb1-114">Primária</span><span class="sxs-lookup"><span data-stu-id="96eb1-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="96eb1-115">Número de identificação exclusivo que identifica esse tipo de erro.</span><span class="sxs-lookup"><span data-stu-id="96eb1-115">Unique ID number identifying this type of error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96eb1-116"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="96eb1-116"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="96eb1-117">int</span><span class="sxs-lookup"><span data-stu-id="96eb1-117">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="96eb1-118">Código de resposta SIP padrão associado a esse erro.</span><span class="sxs-lookup"><span data-stu-id="96eb1-118">Standard SIP response code associated with this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96eb1-119"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="96eb1-119"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="96eb1-120">int</span><span class="sxs-lookup"><span data-stu-id="96eb1-120">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="96eb1-121">IDENTIFICAÇÃO do diagnóstico da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="96eb1-121">Microsoft Diagnostic ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96eb1-122"><strong>Callid</strong></span><span class="sxs-lookup"><span data-stu-id="96eb1-122"><strong>CallTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="96eb1-123">Núm</span><span class="sxs-lookup"><span data-stu-id="96eb1-123">Int</span></span></p></td>
<td><p><span data-ttu-id="96eb1-124">Exterior</span><span class="sxs-lookup"><span data-stu-id="96eb1-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="96eb1-125">Tipo de chamada.</span><span class="sxs-lookup"><span data-stu-id="96eb1-125">Type of the call.</span></span> <span data-ttu-id="96eb1-126">Consulte a <a href="lync-server-2013-calltype-table.md">tabela CallType no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="96eb1-126">See the <a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96eb1-127"><strong>RequestType</strong></span><span class="sxs-lookup"><span data-stu-id="96eb1-127"><strong>RequestType</strong></span></span></p></td>
<td><p><span data-ttu-id="96eb1-128">varbinary (33)</span><span class="sxs-lookup"><span data-stu-id="96eb1-128">varbinary(33)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="96eb1-129">Tipo de solicitação que falhou.</span><span class="sxs-lookup"><span data-stu-id="96eb1-129">Type of request that failed.</span></span></p>
<p><span data-ttu-id="96eb1-130">Esses dados podem ser convertidos em um formato de texto usando esta sintaxe:</span><span class="sxs-lookup"><span data-stu-id="96eb1-130">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(RequestType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96eb1-131"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="96eb1-131"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="96eb1-132">varbinary (257)</span><span class="sxs-lookup"><span data-stu-id="96eb1-132">varbinary(257)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="96eb1-133">Tipo de conteúdo da solicitação que falhou.</span><span class="sxs-lookup"><span data-stu-id="96eb1-133">Content type of the request that failed.</span></span></p>
<p><span data-ttu-id="96eb1-134">Esses dados podem ser convertidos em um formato de texto usando esta sintaxe:</span><span class="sxs-lookup"><span data-stu-id="96eb1-134">This data can be converted to text format by using this syntaxt:</span></span></p>
<p><code>cast(cast(ContentType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table><span data-ttu-id="96eb1-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="96eb1-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

