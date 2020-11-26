---
title: 'Lync Server 2013: tblFileToken'
description: 'Lync Server 2013: tblFileToken.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblFileToken
ms:assetid: 49e7dd79-1607-443c-818a-88c160e4ed06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558646(v=OCS.15)
ms:contentKeyID: 48184073
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c0a0465bd769cff5c23c00a98f79e2346232175
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423525"
---
# <a name="tblfiletoken-in-lync-server-2013"></a><span data-ttu-id="8e5f8-103">tblFileToken no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e5f8-103">tblFileToken in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e5f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e5f8-104">

<span> </span></span></span>

<span data-ttu-id="8e5f8-105">_**Tópico da última modificação:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="8e5f8-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="8e5f8-106">tblFileToken contém tokens temporários para fins de transferência de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8e5f8-106">tblFileToken contains temporary tokens for file transfer purposes.</span></span>

### <a name="columns"></a><span data-ttu-id="8e5f8-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="8e5f8-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e5f8-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="8e5f8-108">Column</span></span></th>
<th><span data-ttu-id="8e5f8-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8e5f8-109">Type</span></span></th>
<th><span data-ttu-id="8e5f8-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e5f8-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e5f8-111">Filetoken</span><span class="sxs-lookup"><span data-stu-id="8e5f8-111">fileToken</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-112">nvarchar (50), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="8e5f8-112">nvarchar (50), not null</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-113">Token exclusivo (a GUID).</span><span class="sxs-lookup"><span data-stu-id="8e5f8-113">Unique token (a GUID).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e5f8-114">fileTokenUserID</span><span class="sxs-lookup"><span data-stu-id="8e5f8-114">fileTokenUserID</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-115">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="8e5f8-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-116">ID da entidade de segurança que está transferindo o arquivo.</span><span class="sxs-lookup"><span data-stu-id="8e5f8-116">ID of the principal that is transferring the file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e5f8-117">fileTokenChannelID</span><span class="sxs-lookup"><span data-stu-id="8e5f8-117">fileTokenChannelID</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-118">GUID, não nulo</span><span class="sxs-lookup"><span data-stu-id="8e5f8-118">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-119">GUID do nó da sala de chat.</span><span class="sxs-lookup"><span data-stu-id="8e5f8-119">GUID of the chat room node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e5f8-120">fileTokenExpireDate</span><span class="sxs-lookup"><span data-stu-id="8e5f8-120">fileTokenExpireDate</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-121">DateTime, não nulo</span><span class="sxs-lookup"><span data-stu-id="8e5f8-121">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-122">Tempo de expiração.</span><span class="sxs-lookup"><span data-stu-id="8e5f8-122">Expiration time.</span></span> <span data-ttu-id="8e5f8-123">(Os tokens expiram após 30 minutos, a menos que sejam fixados (consulte as descrições a seguir nesta coluna).</span><span class="sxs-lookup"><span data-stu-id="8e5f8-123">(Tokens expire after 30 minutes, unless pinned (see the following descriptions in this column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e5f8-124">fileTokenComplianceFileUrl</span><span class="sxs-lookup"><span data-stu-id="8e5f8-124">fileTokenComplianceFileUrl</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-125">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="8e5f8-125">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-126">URL do arquivo transferido (para uso do serviço de conformidade).</span><span class="sxs-lookup"><span data-stu-id="8e5f8-126">URL of the transferred file (for Compliance service use).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e5f8-127">fileTokenComplianceThumbnailUrl</span><span class="sxs-lookup"><span data-stu-id="8e5f8-127">fileTokenComplianceThumbnailUrl</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="8e5f8-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-129">URL da miniatura do arquivo transferido (para uso do serviço de conformidade).</span><span class="sxs-lookup"><span data-stu-id="8e5f8-129">URL of the thumbnail for the transferred file (for Compliance service use).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e5f8-130">fileTokenComplianceTime</span><span class="sxs-lookup"><span data-stu-id="8e5f8-130">fileTokenComplianceTime</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-131">datetime2</span><span class="sxs-lookup"><span data-stu-id="8e5f8-131">datetime2</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-132">Carimbo de data/hora para a operação de transferência de arquivo real (para uso do serviço de conformidade).</span><span class="sxs-lookup"><span data-stu-id="8e5f8-132">Timestamp for the actual file transfer operation (for Compliance service use).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e5f8-133">fileTokenComplianceIsUpload</span><span class="sxs-lookup"><span data-stu-id="8e5f8-133">fileTokenComplianceIsUpload</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-134">bit</span><span class="sxs-lookup"><span data-stu-id="8e5f8-134">bit</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-135">Verdadeiro se for carregado; Falso se baixar (para uso do serviço de conformidade).</span><span class="sxs-lookup"><span data-stu-id="8e5f8-135">True if upload; False if download (for Compliance service use).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e5f8-136">fileTokenCompliancePinned</span><span class="sxs-lookup"><span data-stu-id="8e5f8-136">fileTokenCompliancePinned</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-137">bit, e não nulo</span><span class="sxs-lookup"><span data-stu-id="8e5f8-137">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-138">Verdadeiro se o token estiver fixado.</span><span class="sxs-lookup"><span data-stu-id="8e5f8-138">True if token is pinned.</span></span> <span data-ttu-id="8e5f8-139">Ele é usado para manter o token na tabela até que o serviço de conformidade tenha a chance de recuperar os campos relevantes dele.</span><span class="sxs-lookup"><span data-stu-id="8e5f8-139">It’s used to keep the token in the table until Compliance service has a chance to retrieve the relevant fields from it.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="8e5f8-140">As</span><span class="sxs-lookup"><span data-stu-id="8e5f8-140">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e5f8-141">Coluna</span><span class="sxs-lookup"><span data-stu-id="8e5f8-141">Column</span></span></th>
<th><span data-ttu-id="8e5f8-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e5f8-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e5f8-143">Filetoken</span><span class="sxs-lookup"><span data-stu-id="8e5f8-143">fileToken</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-144">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="8e5f8-144">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e5f8-145">fileTokenChannelID</span><span class="sxs-lookup"><span data-stu-id="8e5f8-145">fileTokenChannelID</span></span></p></td>
<td><p><span data-ttu-id="8e5f8-146">Chave estrangeira com Lookup na tabela tblNode. nodeGuid.</span><span class="sxs-lookup"><span data-stu-id="8e5f8-146">Foreign key with lookup in tblNode.nodeGuid table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8e5f8-147">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e5f8-147">


</div>

<span> </span>

</div>

</div>

</span></span></div>

