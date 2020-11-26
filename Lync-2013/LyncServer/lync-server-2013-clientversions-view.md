---
title: 'Lync Server 2013: modo de exibição ClientVersions'
description: 'Lync Server 2013: modo de exibição ClientVersions.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ClientVersions view
ms:assetid: caf7678f-83a0-46c8-83cc-fee4c3991f52
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721891(v=OCS.15)
ms:contentKeyID: 49733825
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 42ede7107a59db3162ac7f5344e47e81a80d57df
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434729"
---
# <a name="clientversions-view-in-lync-server-2013"></a><span data-ttu-id="a0732-103">Exibição ClientVersions no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0732-103">ClientVersions view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0732-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0732-104">

<span> </span></span></span>

<span data-ttu-id="a0732-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="a0732-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="a0732-106">A exibição ClientVersions armazena informações sobre os vários tipos de cliente e versões que participaram de sessões registradas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a0732-106">The ClientVersions view stores information about the various client types and versions that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="a0732-107">Cada registro na exibição representa uma versão do cliente.</span><span class="sxs-lookup"><span data-stu-id="a0732-107">Each record in the view represents one client version.</span></span> <span data-ttu-id="a0732-108">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a0732-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a0732-109">Pode haver vários registros para determinadas colunas.</span><span class="sxs-lookup"><span data-stu-id="a0732-109">There may be multiple records for certain columns.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0732-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="a0732-110">Column</span></span></th>
<th><span data-ttu-id="a0732-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a0732-111">Data Type</span></span></th>
<th><span data-ttu-id="a0732-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="a0732-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0732-113"><strong>VersionId</strong></span><span class="sxs-lookup"><span data-stu-id="a0732-113"><strong>VersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="a0732-114">int</span><span class="sxs-lookup"><span data-stu-id="a0732-114">int</span></span></p></td>
<td><p><span data-ttu-id="a0732-115">Número exclusivo que identifica esse tipo de cliente e a versão.</span><span class="sxs-lookup"><span data-stu-id="a0732-115">Unique number identifying this client type and version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0732-116"><strong>Versão</strong></span><span class="sxs-lookup"><span data-stu-id="a0732-116"><strong>Version</strong></span></span></p></td>
<td><p><span data-ttu-id="a0732-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="a0732-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="a0732-118">Representa o agente do usuário.</span><span class="sxs-lookup"><span data-stu-id="a0732-118">Represents the user agent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0732-119"><strong>ClientType</strong></span><span class="sxs-lookup"><span data-stu-id="a0732-119"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="a0732-120">int</span><span class="sxs-lookup"><span data-stu-id="a0732-120">int</span></span></p></td>
<td><p><span data-ttu-id="a0732-121">Tipo de cliente.</span><span class="sxs-lookup"><span data-stu-id="a0732-121">Type of client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0732-122"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="a0732-122"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="a0732-123">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="a0732-123">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="a0732-124">Categoria à qual o cliente pertence.</span><span class="sxs-lookup"><span data-stu-id="a0732-124">Category that the client belongs to.</span></span> <span data-ttu-id="a0732-125">Por exemplo, o cliente Conferencing_Attendant_1 0 pertence à CAA ClientCategory.</span><span class="sxs-lookup"><span data-stu-id="a0732-125">For example, the client Conferencing_Attendant_1.0 belongs to the ClientCategory CAA.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a0732-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0732-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

