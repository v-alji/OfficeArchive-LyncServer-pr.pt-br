---
title: 'Lync Server 2013: tblComplianceData'
description: 'Lync Server 2013: tblComplianceData.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceData
ms:assetid: 05b28f9b-4aba-4b69-ba8d-2ceeb6cbfaac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558606(v=OCS.15)
ms:contentKeyID: 48183308
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3c597d67054303de2753182b37419f68051d3af8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444473"
---
# <a name="tblcompliancedata-in-lync-server-2013"></a><span data-ttu-id="d16c9-103">tblComplianceData no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d16c9-103">tblComplianceData in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d16c9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d16c9-104">

<span> </span></span></span>

<span data-ttu-id="d16c9-105">_**Tópico da última modificação:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="d16c9-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="d16c9-106">tblComplianceData contém os eventos de conformidade que ainda não foram processados pelo adaptador de conformidade.</span><span class="sxs-lookup"><span data-stu-id="d16c9-106">tblComplianceData contains the compliance events that have not been processed by the compliance adapter yet.</span></span>

### <a name="columns"></a><span data-ttu-id="d16c9-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="d16c9-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d16c9-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="d16c9-108">Column</span></span></th>
<th><span data-ttu-id="d16c9-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d16c9-109">Type</span></span></th>
<th><span data-ttu-id="d16c9-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d16c9-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d16c9-111">cmplEventID</span><span class="sxs-lookup"><span data-stu-id="d16c9-111">cmplEventID</span></span></p></td>
<td><p><span data-ttu-id="d16c9-112">bigint, e não nulo</span><span class="sxs-lookup"><span data-stu-id="d16c9-112">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="d16c9-113">ID do evento.</span><span class="sxs-lookup"><span data-stu-id="d16c9-113">Event ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d16c9-114">entryDate</span><span class="sxs-lookup"><span data-stu-id="d16c9-114">entryDate</span></span></p></td>
<td><p><span data-ttu-id="d16c9-115">smalldatetime, não nulo</span><span class="sxs-lookup"><span data-stu-id="d16c9-115">smalldatetime, not null</span></span></p></td>
<td><p><span data-ttu-id="d16c9-116">Tempo de inserção (pode estar muito no futuro para cmplType = 9 porque a entrada é apenas um espaço reservado nesse caso).</span><span class="sxs-lookup"><span data-stu-id="d16c9-116">Time of insertion (may be far in the future for cmplType=9 because the entry is just a placeholder in that case).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d16c9-117">cmplType</span><span class="sxs-lookup"><span data-stu-id="d16c9-117">cmplType</span></span></p></td>
<td><p><span data-ttu-id="d16c9-118">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="d16c9-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="d16c9-119">Tipo de evento de conformidade:</span><span class="sxs-lookup"><span data-stu-id="d16c9-119">Type of compliance event:</span></span></p>
<ul>
<li><p><span data-ttu-id="d16c9-120">1: chat</span><span class="sxs-lookup"><span data-stu-id="d16c9-120">1: Chat</span></span></p></li>
<li><p><span data-ttu-id="d16c9-121">2: backchat</span><span class="sxs-lookup"><span data-stu-id="d16c9-121">2: Backchat</span></span></p></li>
<li><p><span data-ttu-id="d16c9-122">3: download de arquivo</span><span class="sxs-lookup"><span data-stu-id="d16c9-122">3: File download</span></span></p></li>
<li><p><span data-ttu-id="d16c9-123">4: carregamento de arquivo</span><span class="sxs-lookup"><span data-stu-id="d16c9-123">4: File upload</span></span></p></li>
<li><p><span data-ttu-id="d16c9-124">9: transferência de arquivo provisório</span><span class="sxs-lookup"><span data-stu-id="d16c9-124">9: Provisional file transfer</span></span></p></li>
<li><p><span data-ttu-id="d16c9-125">10: exclusão de chat (com replace)</span><span class="sxs-lookup"><span data-stu-id="d16c9-125">10: Chat deletion (with replace)</span></span></p></li>
<li><p><span data-ttu-id="d16c9-126">11: limpeza de chat</span><span class="sxs-lookup"><span data-stu-id="d16c9-126">11: Chat purging</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d16c9-127">cmplTime</span><span class="sxs-lookup"><span data-stu-id="d16c9-127">cmplTime</span></span></p></td>
<td><p><span data-ttu-id="d16c9-128">bigint, e não nulo</span><span class="sxs-lookup"><span data-stu-id="d16c9-128">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="d16c9-129">Carimbo de data/hora do evento.</span><span class="sxs-lookup"><span data-stu-id="d16c9-129">Time stamp for the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d16c9-130">cmplChannelUri</span><span class="sxs-lookup"><span data-stu-id="d16c9-130">cmplChannelUri</span></span></p></td>
<td><p><span data-ttu-id="d16c9-131">nvarchar (255), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="d16c9-131">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="d16c9-132">URI (Uniform Resource Identifier) do canal.</span><span class="sxs-lookup"><span data-stu-id="d16c9-132">Channel Uniform Resource Identifier (URI).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d16c9-133">cmplChatID</span><span class="sxs-lookup"><span data-stu-id="d16c9-133">cmplChatID</span></span></p></td>
<td><p><span data-ttu-id="d16c9-134">bigint</span><span class="sxs-lookup"><span data-stu-id="d16c9-134">bigint</span></span></p></td>
<td><p><span data-ttu-id="d16c9-135">ID de chat (correspondente à tabela tblChat. chatid).</span><span class="sxs-lookup"><span data-stu-id="d16c9-135">Chat ID (corresponding to tblChat.chatId table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d16c9-136">cmplUserID</span><span class="sxs-lookup"><span data-stu-id="d16c9-136">cmplUserID</span></span></p></td>
<td><p><span data-ttu-id="d16c9-137">int, não nulo</span><span class="sxs-lookup"><span data-stu-id="d16c9-137">int, not null</span></span></p></td>
<td><p><span data-ttu-id="d16c9-138">ID da entidade de segurança do pôster (correspondente à tabela tblPrincipal. retoid).</span><span class="sxs-lookup"><span data-stu-id="d16c9-138">Principal ID of the poster (corresponding to tblPrincipal.prinID table).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d16c9-139">cmplUserUri</span><span class="sxs-lookup"><span data-stu-id="d16c9-139">cmplUserUri</span></span></p></td>
<td><p><span data-ttu-id="d16c9-140">nvarchar (255), NOT NULL</span><span class="sxs-lookup"><span data-stu-id="d16c9-140">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="d16c9-141">URI de usuário.</span><span class="sxs-lookup"><span data-stu-id="d16c9-141">User URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d16c9-142">cmplMessage</span><span class="sxs-lookup"><span data-stu-id="d16c9-142">cmplMessage</span></span></p></td>
<td><p><span data-ttu-id="d16c9-143">nvarchar (max)</span><span class="sxs-lookup"><span data-stu-id="d16c9-143">nvarchar (max)</span></span></p></td>
<td><p><span data-ttu-id="d16c9-144">Mensagem (a codificação depende do cmplType).</span><span class="sxs-lookup"><span data-stu-id="d16c9-144">Message (encoding depends on cmplType).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="d16c9-145">Chave</span><span class="sxs-lookup"><span data-stu-id="d16c9-145">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d16c9-146">Coluna</span><span class="sxs-lookup"><span data-stu-id="d16c9-146">Column</span></span></th>
<th><span data-ttu-id="d16c9-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="d16c9-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d16c9-148">cmplEventID</span><span class="sxs-lookup"><span data-stu-id="d16c9-148">cmplEventID</span></span></p></td>
<td><p><span data-ttu-id="d16c9-149">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="d16c9-149">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d16c9-150">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d16c9-150">


</div>

<span> </span>

</div>

</div>

</span></span></div>

