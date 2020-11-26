---
title: 'Lync Server 2013: tblConfig'
description: 'Lync Server 2013: tblConfig.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblConfig
ms:assetid: 7445e7db-c574-46fa-b964-8640d77047a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558663(v=OCS.15)
ms:contentKeyID: 48184515
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8990e0b2c8724a5e90c36e706b92f9985f288772
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444459"
---
# <a name="tblconfig-in-lync-server-2013"></a><span data-ttu-id="eca50-103">tblConfig no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eca50-103">tblConfig in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eca50-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eca50-104">

<span> </span></span></span>

<span data-ttu-id="eca50-105">_**Tópico da última modificação:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="eca50-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="eca50-106">o tblConfig contém uma configuração sem suporte do servidor de chat persistente, em uma linha.</span><span class="sxs-lookup"><span data-stu-id="eca50-106">tblConfig contains some Persistent Chat Server unsupported configuration, in one row.</span></span>

### <a name="columns"></a><span data-ttu-id="eca50-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="eca50-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eca50-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="eca50-108">Column</span></span></th>
<th><span data-ttu-id="eca50-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="eca50-109">Type</span></span></th>
<th><span data-ttu-id="eca50-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="eca50-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eca50-111">configLabel</span><span class="sxs-lookup"><span data-stu-id="eca50-111">configLabel</span></span></p></td>
<td><p><span data-ttu-id="eca50-112">nvarchar (255), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="eca50-112">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="eca50-113">Contém &quot; pool.&quot;</span><span class="sxs-lookup"><span data-stu-id="eca50-113">Contains &quot;pool.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eca50-114">configContent</span><span class="sxs-lookup"><span data-stu-id="eca50-114">configContent</span></span></p></td>
<td><p><span data-ttu-id="eca50-115">nvarchar (max)</span><span class="sxs-lookup"><span data-stu-id="eca50-115">nvarchar (max)</span></span></p></td>
<td><p><span data-ttu-id="eca50-116">Conteúdo de configuração.</span><span class="sxs-lookup"><span data-stu-id="eca50-116">Configuration content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eca50-117">configPoolID</span><span class="sxs-lookup"><span data-stu-id="eca50-117">configPoolID</span></span></p></td>
<td><p><span data-ttu-id="eca50-118">GUID, não nulo</span><span class="sxs-lookup"><span data-stu-id="eca50-118">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="eca50-119">ID exclusiva da instância do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="eca50-119">Unique ID of the database instance.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="eca50-120">Chave</span><span class="sxs-lookup"><span data-stu-id="eca50-120">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eca50-121">Coluna</span><span class="sxs-lookup"><span data-stu-id="eca50-121">Column</span></span></th>
<th><span data-ttu-id="eca50-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="eca50-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eca50-123">configLabel</span><span class="sxs-lookup"><span data-stu-id="eca50-123">configLabel</span></span></p></td>
<td><p><span data-ttu-id="eca50-124">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="eca50-124">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="eca50-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eca50-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

