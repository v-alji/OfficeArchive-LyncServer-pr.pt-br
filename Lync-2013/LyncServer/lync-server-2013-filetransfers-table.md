---
title: 'Lync Server 2013: Tabela FileTransfers'
description: 'Lync Server 2013: tabela de transferência de File.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers table
ms:assetid: 5368e67c-d8a9-43a1-9472-a839950dedb3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398353(v=OCS.15)
ms:contentKeyID: 48184118
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ccde45fa3743a809499273676d567846ef292ecc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428164"
---
# <a name="filetransfers-table-in-lync-server-2013"></a><span data-ttu-id="d048f-103">Tabela FileTransfers no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d048f-103">FileTransfers table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d048f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d048f-104">

<span> </span></span></span>

<span data-ttu-id="d048f-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="d048f-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="d048f-106">Cada registro representa uma sessão de transferência de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d048f-106">Each record represents one file transfer session.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d048f-107">Coluna</span><span class="sxs-lookup"><span data-stu-id="d048f-107">Column</span></span></th>
<th><span data-ttu-id="d048f-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d048f-108">Data Type</span></span></th>
<th><span data-ttu-id="d048f-109">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="d048f-109">Key/Index</span></span></th>
<th><span data-ttu-id="d048f-110">Detalhes</span><span class="sxs-lookup"><span data-stu-id="d048f-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d048f-111"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="d048f-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d048f-112">datetime</span><span class="sxs-lookup"><span data-stu-id="d048f-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="d048f-113">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="d048f-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="d048f-114">Tempo de solicitação de sessão.</span><span class="sxs-lookup"><span data-stu-id="d048f-114">Time of session request.</span></span> <span data-ttu-id="d048f-115">Usado em conjunto com o <strong>SessionIdSeq</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="d048f-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="d048f-116">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d048f-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d048f-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="d048f-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="d048f-118">int</span><span class="sxs-lookup"><span data-stu-id="d048f-118">int</span></span></p></td>
<td><p><span data-ttu-id="d048f-119">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="d048f-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="d048f-120">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="d048f-120">ID number to identify the session.</span></span> <span data-ttu-id="d048f-121">Usado em conjunto com a <strong>identificação_da_sessãotime</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="d048f-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="d048f-122">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d048f-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d048f-123"><strong>Nome do arquivo</strong></span><span class="sxs-lookup"><span data-stu-id="d048f-123"><strong>File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d048f-124">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d048f-124">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d048f-125">Nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d048f-125">Name of the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d048f-126"><strong>Fileidentity</strong></span><span class="sxs-lookup"><span data-stu-id="d048f-126"><strong>FileIdentity</strong></span></span></p></td>
<td><p><span data-ttu-id="d048f-127">identificador</span><span class="sxs-lookup"><span data-stu-id="d048f-127">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d048f-128">Identificador exclusivo para distinguir entre as transferências de arquivo que envolvem o mesmo nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d048f-128">Unique identifier to distinguish between file transfers involving the same file name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d048f-129"><strong>Cookie</strong></span><span class="sxs-lookup"><span data-stu-id="d048f-129"><strong>Cookie</strong></span></span></p></td>
<td><p><span data-ttu-id="d048f-130">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="d048f-130">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="d048f-131">Primária</span><span class="sxs-lookup"><span data-stu-id="d048f-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="d048f-132">Usado para identificar todas as mensagens de acompanhamento como associadas a esta.</span><span class="sxs-lookup"><span data-stu-id="d048f-132">Used to identify every follow-up message as being associated with this one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d048f-133"><strong>Aceite</strong></span><span class="sxs-lookup"><span data-stu-id="d048f-133"><strong>Accept</strong></span></span></p></td>
<td><p><span data-ttu-id="d048f-134">bit</span><span class="sxs-lookup"><span data-stu-id="d048f-134">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d048f-135">Pode ser TRUE ou NULL.</span><span class="sxs-lookup"><span data-stu-id="d048f-135">Can be TRUE or NULL.</span></span> <span data-ttu-id="d048f-136">Se verdadeiro, rejeitar e cancelar será nulo.</span><span class="sxs-lookup"><span data-stu-id="d048f-136">If TRUE, then Reject and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d048f-137"><strong>Rejeitar</strong></span><span class="sxs-lookup"><span data-stu-id="d048f-137"><strong>Reject</strong></span></span></p></td>
<td><p><span data-ttu-id="d048f-138">bit</span><span class="sxs-lookup"><span data-stu-id="d048f-138">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d048f-139">Pode ser TRUE ou NULL.</span><span class="sxs-lookup"><span data-stu-id="d048f-139">Can be TRUE or NULL.</span></span> <span data-ttu-id="d048f-140">Se verdadeiro, aceitar e cancelar será nulo.</span><span class="sxs-lookup"><span data-stu-id="d048f-140">If TRUE, then Accept and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d048f-141"><strong>Cancelar</strong></span><span class="sxs-lookup"><span data-stu-id="d048f-141"><strong>Cancel</strong></span></span></p></td>
<td><p><span data-ttu-id="d048f-142">bit</span><span class="sxs-lookup"><span data-stu-id="d048f-142">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d048f-143">Pode ser TRUE ou NULL.</span><span class="sxs-lookup"><span data-stu-id="d048f-143">Can be TRUE or NULL.</span></span> <span data-ttu-id="d048f-144">Se verdadeiro, aceitar e rejeitar será nulo.</span><span class="sxs-lookup"><span data-stu-id="d048f-144">If TRUE, then Accept and Reject will be NULL.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d048f-145">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d048f-145">


</div>

<span> </span>

</div>

</div>

</span></span></div>

