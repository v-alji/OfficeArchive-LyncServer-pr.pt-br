---
title: 'Lync Server 2013: tblPreference'
description: 'Lync Server 2013: tblPreference.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPreference
ms:assetid: f94eb128-f782-42ff-a568-ed3529573bc8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615052(v=OCS.15)
ms:contentKeyID: 48185913
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 86e8b81a6af93e9bf1d7673e54492579a1bed08e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441372"
---
# <a name="tblpreference-in-lync-server-2013"></a><span data-ttu-id="9b758-103">tblPreference no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9b758-103">tblPreference in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9b758-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9b758-104">

<span> </span></span></span>

<span data-ttu-id="9b758-105">_**Tópico da última modificação:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="9b758-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="9b758-106">tblPreference contém as preferências do cliente dos usuários.</span><span class="sxs-lookup"><span data-stu-id="9b758-106">tblPreference contains the users’ client preferences.</span></span> <span data-ttu-id="9b758-107">Isso geralmente é usado por clientes anteriores ao Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="9b758-107">This is generally used by clients previous to Lync 2013.</span></span>

### <a name="columns"></a><span data-ttu-id="9b758-108">Colunas</span><span class="sxs-lookup"><span data-stu-id="9b758-108">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b758-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="9b758-109">Column</span></span></th>
<th><span data-ttu-id="9b758-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b758-110">Type</span></span></th>
<th><span data-ttu-id="9b758-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b758-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b758-112">prefLabel</span><span class="sxs-lookup"><span data-stu-id="9b758-112">prefLabel</span></span></p></td>
<td><p><span data-ttu-id="9b758-113">nvarchar (255), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="9b758-113">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="9b758-114">Rótulo com um formato como: &lt; User SIP URI &gt; | username. &lt; conjunto de preferências &gt; .</span><span class="sxs-lookup"><span data-stu-id="9b758-114">Label with a format such as: &lt;user sip uri&gt;|username.&lt;preference set&gt;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b758-115">prefSeqID</span><span class="sxs-lookup"><span data-stu-id="9b758-115">prefSeqID</span></span></p></td>
<td><p><span data-ttu-id="9b758-116">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="9b758-116">int, not null</span></span></p></td>
<td><p><span data-ttu-id="9b758-117">Um número sequencial (por rótulo) para fins de controle de versão.</span><span class="sxs-lookup"><span data-stu-id="9b758-117">A sequential number (per label) for versioning purposes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b758-118">prefContent</span><span class="sxs-lookup"><span data-stu-id="9b758-118">prefContent</span></span></p></td>
<td><p><span data-ttu-id="9b758-119">nvarchar (max)</span><span class="sxs-lookup"><span data-stu-id="9b758-119">nvarchar (max)</span></span></p></td>
<td><p><span data-ttu-id="9b758-120">Conteúdo codificado.</span><span class="sxs-lookup"><span data-stu-id="9b758-120">Encoded content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b758-121">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="9b758-121">lastModifiedBy</span></span></p></td>
<td><p><span data-ttu-id="9b758-122">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="9b758-122">int, not null</span></span></p></td>
<td><p><span data-ttu-id="9b758-123">ID da entidade de segurança que atualizou a preferência.</span><span class="sxs-lookup"><span data-stu-id="9b758-123">ID of the principal that updated the preference.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="9b758-124">Chave</span><span class="sxs-lookup"><span data-stu-id="9b758-124">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b758-125">Coluna</span><span class="sxs-lookup"><span data-stu-id="9b758-125">Column</span></span></th>
<th><span data-ttu-id="9b758-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b758-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b758-127">&lt;prefLabel, prefSeqID&gt;</span><span class="sxs-lookup"><span data-stu-id="9b758-127">&lt;prefLabel, prefSeqID&gt;</span></span></p></td>
<td><p><span data-ttu-id="9b758-128">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="9b758-128">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9b758-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9b758-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

