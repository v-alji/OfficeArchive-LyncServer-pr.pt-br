---
title: 'Lync Server 2013: modo de exibição de transferência de fileviews'
description: 'Lync Server 2013: modo de exibição de transferência de fileviews.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers view
ms:assetid: e52c3ad0-152e-4a18-af1c-1aff0d205151
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721914(v=OCS.15)
ms:contentKeyID: 49733848
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd2b084274a4d5daa093f2269617214f703ac03e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428150"
---
# <a name="filetransfers-view-in-lync-server-2013"></a><span data-ttu-id="1b279-103">Modo de exibição de transferência de fileviews no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1b279-103">FileTransfers view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1b279-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1b279-104">

<span> </span></span></span>

<span data-ttu-id="1b279-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="1b279-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="1b279-106">O modo de transferência de arquivo armazena informações sobre sessões de transferência de arquivos ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="1b279-106">The FileTransfer view stores information about peer-to-peer file transfer sessions.</span></span> <span data-ttu-id="1b279-107">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1b279-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1b279-108">O modo de exibição filetransfers contém todas as colunas na <A href="lync-server-2013-sessiondetails-view.md">exibição SessionDetails no Lync Server 2013</A> , além das colunas listadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="1b279-108">The FileTransfers view contains all of the columns in the <A href="lync-server-2013-sessiondetails-view.md">SessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b279-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="1b279-109">Column</span></span></th>
<th><span data-ttu-id="1b279-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1b279-110">Data Type</span></span></th>
<th><span data-ttu-id="1b279-111">Detalhes</span><span class="sxs-lookup"><span data-stu-id="1b279-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b279-112"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="1b279-112"><strong>FileName</strong></span></span></p></td>
<td><p><span data-ttu-id="1b279-113">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1b279-113">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1b279-114">Nome do arquivo transferido.</span><span class="sxs-lookup"><span data-stu-id="1b279-114">Name of the file transferred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b279-115"><strong>Cookie</strong></span><span class="sxs-lookup"><span data-stu-id="1b279-115"><strong>Cookie</strong></span></span></p></td>
<td><p><span data-ttu-id="1b279-116">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="1b279-116">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="1b279-117">Usado para identificar todas as mensagens de acompanhamento como associadas a esta.</span><span class="sxs-lookup"><span data-stu-id="1b279-117">Used to identify every follow-up message as being associated with this one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b279-118"><strong>Fileidentity</strong></span><span class="sxs-lookup"><span data-stu-id="1b279-118"><strong>FileIdentity</strong></span></span></p></td>
<td><p><span data-ttu-id="1b279-119">identificador</span><span class="sxs-lookup"><span data-stu-id="1b279-119">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="1b279-120">Identificador exclusivo para distinguir entre as transferências de arquivo que envolvem o mesmo nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1b279-120">Unique identifier to distinguish between file transfers involving the same file name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b279-121"><strong>Aceite</strong></span><span class="sxs-lookup"><span data-stu-id="1b279-121"><strong>Accept</strong></span></span></p></td>
<td><p><span data-ttu-id="1b279-122">bit</span><span class="sxs-lookup"><span data-stu-id="1b279-122">bit</span></span></p></td>
<td><p><span data-ttu-id="1b279-123">Pode ser TRUE ou NULL.</span><span class="sxs-lookup"><span data-stu-id="1b279-123">Can be TRUE or NULL.</span></span> <span data-ttu-id="1b279-124">Se verdadeiro, rejeitar e cancelar será nulo.</span><span class="sxs-lookup"><span data-stu-id="1b279-124">If TRUE, then Reject and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b279-125"><strong>Rejeitar</strong></span><span class="sxs-lookup"><span data-stu-id="1b279-125"><strong>Reject</strong></span></span></p></td>
<td><p><span data-ttu-id="1b279-126">bit</span><span class="sxs-lookup"><span data-stu-id="1b279-126">bit</span></span></p></td>
<td><p><span data-ttu-id="1b279-127">Pode ser TRUE ou NULL.</span><span class="sxs-lookup"><span data-stu-id="1b279-127">Can be TRUE or NULL.</span></span> <span data-ttu-id="1b279-128">Se verdadeiro, aceitar e cancelar será nulo.</span><span class="sxs-lookup"><span data-stu-id="1b279-128">If TRUE, then Accept and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b279-129"><strong>Cancelar</strong></span><span class="sxs-lookup"><span data-stu-id="1b279-129"><strong>Cancel</strong></span></span></p></td>
<td><p><span data-ttu-id="1b279-130">bit</span><span class="sxs-lookup"><span data-stu-id="1b279-130">bit</span></span></p></td>
<td><p><span data-ttu-id="1b279-131">Pode ser TRUE ou NULL.</span><span class="sxs-lookup"><span data-stu-id="1b279-131">Can be TRUE or NULL.</span></span> <span data-ttu-id="1b279-132">Se verdadeiro, aceitar e rejeitar será nulo.</span><span class="sxs-lookup"><span data-stu-id="1b279-132">If TRUE, then Accept and Reject will be NULL.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1b279-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1b279-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

