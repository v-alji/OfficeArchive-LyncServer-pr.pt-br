---
title: 'Lync Server 2013: Tabela SessionCorrelation'
description: 'Lync Server 2013: SessionCorrelation Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionCorrelation table
ms:assetid: 041705e1-7290-464f-95f8-96256cfa2e3e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398091(v=OCS.15)
ms:contentKeyID: 48183267
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 814b7e8539d89f87e7df60ceb03e70800553fb55
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424076"
---
# <a name="sessioncorrelation-table-in-lync-server-2013"></a><span data-ttu-id="1484b-103">Tabela SessionCorrelation no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1484b-103">SessionCorrelation table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1484b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1484b-104">

<span> </span></span></span>

<span data-ttu-id="1484b-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="1484b-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="1484b-106">A tabela SessionCorrelation é uma tabela de suporte.</span><span class="sxs-lookup"><span data-stu-id="1484b-106">The SessionCorrelation table is a supporting table.</span></span> <span data-ttu-id="1484b-107">Cada registro representa um CorrelationId, que é usado para correlacionar várias sessões.</span><span class="sxs-lookup"><span data-stu-id="1484b-107">Each record represents one CorrelationID which is used to correlate multiple sessions.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1484b-108"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="1484b-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="1484b-109"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="1484b-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="1484b-110"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="1484b-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="1484b-111"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="1484b-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1484b-112"><strong>Prova</strong></span><span class="sxs-lookup"><span data-stu-id="1484b-112"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="1484b-113">int</span><span class="sxs-lookup"><span data-stu-id="1484b-113">int</span></span></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1484b-114"><strong>CorrelationKey</strong></span><span class="sxs-lookup"><span data-stu-id="1484b-114"><strong>CorrelationKey</strong></span></span></p></td>
<td><p><span data-ttu-id="1484b-115">int</span><span class="sxs-lookup"><span data-stu-id="1484b-115">int</span></span></p></td>
<td><p><span data-ttu-id="1484b-116">Primária</span><span class="sxs-lookup"><span data-stu-id="1484b-116">Primary</span></span></p></td>
<td><p><span data-ttu-id="1484b-117">Número exclusivo que identifica esse servidor de conferência A/V.</span><span class="sxs-lookup"><span data-stu-id="1484b-117">Unique number identifying this A/V Conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1484b-118"><strong>CorrelationId</strong></span><span class="sxs-lookup"><span data-stu-id="1484b-118"><strong>CorrelationID</strong></span></span></p></td>
<td><p><span data-ttu-id="1484b-119">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1484b-119">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1484b-120">Exclusividade</span><span class="sxs-lookup"><span data-stu-id="1484b-120">Unique</span></span></p></td>
<td><p><span data-ttu-id="1484b-121">As sessões correlacionadas terão a mesma ID de correlação.</span><span class="sxs-lookup"><span data-stu-id="1484b-121">Sessions that are correlated will have the same correlation ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1484b-122"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="1484b-122"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="1484b-123">datetime</span><span class="sxs-lookup"><span data-stu-id="1484b-123">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1484b-124">Somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="1484b-124">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1484b-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1484b-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

