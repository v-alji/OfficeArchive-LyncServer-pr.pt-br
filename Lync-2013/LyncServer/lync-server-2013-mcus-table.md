---
title: 'Lync Server 2013: Tabela Mcus'
description: 'Lync Server 2013: MCUs Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mcus table
ms:assetid: 271b7963-8fd8-4d92-a701-1a62aaf895ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425742(v=OCS.15)
ms:contentKeyID: 48183674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b0b5d0bcbebb5efc1d767776b4581b18d9f2ed18
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425742"
---
# <a name="mcus-table-in-lync-server-2013"></a><span data-ttu-id="3ccee-103">Tabela Mcus no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3ccee-103">Mcus table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3ccee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3ccee-104">

<span> </span></span></span>

<span data-ttu-id="3ccee-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="3ccee-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="3ccee-106">A tabela MCUs é uma tabela de suporte.</span><span class="sxs-lookup"><span data-stu-id="3ccee-106">The Mcus table is a supporting table.</span></span> <span data-ttu-id="3ccee-107">Cada registro armazena informações sobre um serviço de conferência.</span><span class="sxs-lookup"><span data-stu-id="3ccee-107">Each record stores information about one conferencing service.</span></span> <span data-ttu-id="3ccee-108">Eles podem incluir o serviço de conferência de mensagem instantânea e o serviço de conferência de telefonia (que são executados como processos em servidores front-end) e o serviço de conferência via Web e o serviço de conferência A/V.</span><span class="sxs-lookup"><span data-stu-id="3ccee-108">These can include the IM Conferencing service and the Telephony Conferencing service (which run as processes on front-end servers), and the Web Conferencing service and A/V Conferencing service.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ccee-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="3ccee-109">Column</span></span></th>
<th><span data-ttu-id="3ccee-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3ccee-110">Data Type</span></span></th>
<th><span data-ttu-id="3ccee-111">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="3ccee-111">Key/Index</span></span></th>
<th><span data-ttu-id="3ccee-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="3ccee-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ccee-113"><strong>McuId</strong></span><span class="sxs-lookup"><span data-stu-id="3ccee-113"><strong>McuId</strong></span></span></p></td>
<td><p><span data-ttu-id="3ccee-114">int</span><span class="sxs-lookup"><span data-stu-id="3ccee-114">int</span></span></p></td>
<td><p><span data-ttu-id="3ccee-115">Primária</span><span class="sxs-lookup"><span data-stu-id="3ccee-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="3ccee-116">Número exclusivo que identifica esse servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="3ccee-116">Unique number identifying this conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ccee-117"><strong>McuUri</strong></span><span class="sxs-lookup"><span data-stu-id="3ccee-117"><strong>McuUri</strong></span></span></p></td>
<td><p><span data-ttu-id="3ccee-118">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="3ccee-118">nvarchar(450)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ccee-119"><strong>McuTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="3ccee-119"><strong>McuTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="3ccee-120">inyint</span><span class="sxs-lookup"><span data-stu-id="3ccee-120">inyint</span></span></p></td>
<td><p> <span data-ttu-id="3ccee-121">Exterior</span><span class="sxs-lookup"><span data-stu-id="3ccee-121">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3ccee-122">Tipo de servidor de conferência, como conf: Chat (para IMs) ou conf: Audio-Video.</span><span class="sxs-lookup"><span data-stu-id="3ccee-122">Conferencing server type, such as conf:chat (for IMs) or conf:audio-video.</span></span> <span data-ttu-id="3ccee-123">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="3ccee-123">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3ccee-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3ccee-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

