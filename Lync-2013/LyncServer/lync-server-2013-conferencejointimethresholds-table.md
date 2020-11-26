---
title: 'Lync Server 2013: tabela ConferenceJoinTimeThresholds'
description: 'Lync Server 2013: ConferenceJoinTimeThresholds Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceJoinTimeThresholds table
ms:assetid: 3944d724-bdd8-4d1c-a2af-933ee8141529
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204809(v=OCS.15)
ms:contentKeyID: 48183855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e38c8b99f444e16309882b6a8885d166fdceb9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434456"
---
# <a name="conferencejointimethresholds-table-in-lync-server-2013"></a><span data-ttu-id="a76d0-103">Tabela ConferenceJoinTimeThresholds no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a76d0-103">ConferenceJoinTimeThresholds table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a76d0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a76d0-104">

<span> </span></span></span>

<span data-ttu-id="a76d0-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="a76d0-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="a76d0-106">A tabela ConferenceJoinTimeThresholds contém os limites de classificação usados pelo relatório de Resumo de tempo de ingresso em conferência.</span><span class="sxs-lookup"><span data-stu-id="a76d0-106">The ConferenceJoinTimeThresholds table contains the classification boundaries used by the Conference Join Time Summary Report.</span></span> <span data-ttu-id="a76d0-107">O relatório de Resumo de tempo de ingresso em conferência resume o tempo necessário para que os usuários ingressem com êxito em uma conferência; esses valores de tempo são relatados como uma média e em uma das seguintes categorias:</span><span class="sxs-lookup"><span data-stu-id="a76d0-107">The Conference Join Time Summary Report summarizes the amount time required for users to successfully join a conference; these time values are reported both as an average and in one of the following categories:</span></span>

  - <span data-ttu-id="a76d0-108">Menos de 2 segundos.</span><span class="sxs-lookup"><span data-stu-id="a76d0-108">Less than 2 seconds.</span></span>

  - <span data-ttu-id="a76d0-109">Entre 2 e 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="a76d0-109">Between 2 second and 5 seconds.</span></span>

  - <span data-ttu-id="a76d0-110">Entre 5 segundos e 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="a76d0-110">Between 5 seconds and 10 seconds.</span></span>

  - <span data-ttu-id="a76d0-111">Mais de 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="a76d0-111">More than 10 seconds.</span></span>

<span data-ttu-id="a76d0-112">A tabela ConferenceJoinTimeThresholds contém os valores de classificação 2 segundos, 5 segundos e 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="a76d0-112">The ConferenceJoinTimeThresholds table contains the classification values 2 seconds, 5 seconds, and 10 seconds.</span></span>

<span data-ttu-id="a76d0-113">Esta tabela foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a76d0-113">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a76d0-114">Coluna</span><span class="sxs-lookup"><span data-stu-id="a76d0-114">Column</span></span></th>
<th><span data-ttu-id="a76d0-115">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a76d0-115">Data Type</span></span></th>
<th><span data-ttu-id="a76d0-116">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="a76d0-116">Key/Index</span></span></th>
<th><span data-ttu-id="a76d0-117">Detalhes</span><span class="sxs-lookup"><span data-stu-id="a76d0-117">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a76d0-118"><strong>Thresholdid</strong></span><span class="sxs-lookup"><span data-stu-id="a76d0-118"><strong>ThresholdId</strong></span></span></p></td>
<td><p><span data-ttu-id="a76d0-119">int</span><span class="sxs-lookup"><span data-stu-id="a76d0-119">int</span></span></p></td>
<td><p><span data-ttu-id="a76d0-120">Primária</span><span class="sxs-lookup"><span data-stu-id="a76d0-120">Primary</span></span></p></td>
<td><p><span data-ttu-id="a76d0-121">Identificador exclusivo da classificação.</span><span class="sxs-lookup"><span data-stu-id="a76d0-121">Unique identifier for the classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a76d0-122"><strong>ThresholdValue</strong></span><span class="sxs-lookup"><span data-stu-id="a76d0-122"><strong>ThresholdValue</strong></span></span></p></td>
<td><p><span data-ttu-id="a76d0-123">int</span><span class="sxs-lookup"><span data-stu-id="a76d0-123">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a76d0-124">Limite superior da classificação.</span><span class="sxs-lookup"><span data-stu-id="a76d0-124">Upper limit for the classification.</span></span> <span data-ttu-id="a76d0-125">Os valores permitidos são:</span><span class="sxs-lookup"><span data-stu-id="a76d0-125">Allowed values are:</span></span></p>
<ol>
<li><p><span data-ttu-id="a76d0-126">2</span><span class="sxs-lookup"><span data-stu-id="a76d0-126">2</span></span></p></li>
<li><p><span data-ttu-id="a76d0-127">5</span><span class="sxs-lookup"><span data-stu-id="a76d0-127">5</span></span></p></li>
<li><p><span data-ttu-id="a76d0-128">254</span><span class="sxs-lookup"><span data-stu-id="a76d0-128">10</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table><span data-ttu-id="a76d0-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a76d0-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

