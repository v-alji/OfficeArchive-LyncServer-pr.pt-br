---
title: 'Lync Server 2013: Tabela Dialogs'
description: 'Lync Server 2013: tabela de caixas de diálogo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dialogs table
ms:assetid: 487a430b-af66-4ea6-b28e-4e33cfdb7f9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425954(v=OCS.15)
ms:contentKeyID: 48184001
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c2c9cf9ec59fc48f7f5ffc6232980e3f8aa68c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429179"
---
# <a name="dialogs-table-in-lync-server-2013"></a><span data-ttu-id="b828c-103">Tabela Dialogs no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b828c-103">Dialogs table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b828c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b828c-104">

<span> </span></span></span>

<span data-ttu-id="b828c-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="b828c-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="b828c-106">A tabela de caixas de diálogo é uma tabela de suporte que armazena as informações sobre DialogIDs em sessões ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="b828c-106">The Dialogs table is a supporting table that stores the information about DialogIDs for peer-to-peer sessions.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b828c-107">Coluna</span><span class="sxs-lookup"><span data-stu-id="b828c-107">Column</span></span></th>
<th><span data-ttu-id="b828c-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b828c-108">Data Type</span></span></th>
<th><span data-ttu-id="b828c-109">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="b828c-109">Key/Index</span></span></th>
<th><span data-ttu-id="b828c-110">Detalhes</span><span class="sxs-lookup"><span data-stu-id="b828c-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b828c-111"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="b828c-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b828c-112">datetime</span><span class="sxs-lookup"><span data-stu-id="b828c-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="b828c-113">Primária</span><span class="sxs-lookup"><span data-stu-id="b828c-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="b828c-114">Tempo de solicitação de sessão; usado em conjunto com o SessionIDSeq para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="b828c-114">Time of session request; used in conjunction with SessionIDSeq to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b828c-115"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="b828c-115"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="b828c-116">int</span><span class="sxs-lookup"><span data-stu-id="b828c-116">int</span></span></p></td>
<td><p><span data-ttu-id="b828c-117">Primária</span><span class="sxs-lookup"><span data-stu-id="b828c-117">Primary</span></span></p></td>
<td><p><span data-ttu-id="b828c-118">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="b828c-118">ID number to identify the session.</span></span> <span data-ttu-id="b828c-119">Usado em conjunto com a Identificação_da_sessãotime para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="b828c-119">Used in conjunction with SessionIDTime to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b828c-120"><strong>ExternalChecksum</strong></span><span class="sxs-lookup"><span data-stu-id="b828c-120"><strong>ExternalChecksum</strong></span></span></p></td>
<td><p><span data-ttu-id="b828c-121">int</span><span class="sxs-lookup"><span data-stu-id="b828c-121">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b828c-122">Checksum da externalId.</span><span class="sxs-lookup"><span data-stu-id="b828c-122">Checksum of the ExternalID.</span></span> <span data-ttu-id="b828c-123">Este campo é usado para aumentar a velocidade das pesquisas do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b828c-123">This field is used to increase the speed of database searches.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b828c-124"><strong>ExternalId</strong></span><span class="sxs-lookup"><span data-stu-id="b828c-124"><strong>ExternalId</strong></span></span></p></td>
<td><p><span data-ttu-id="b828c-125">varbinary (775)</span><span class="sxs-lookup"><span data-stu-id="b828c-125">varbinary(775)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b828c-126">ID da caixa de diálogo SIP, armazenada como um binário.</span><span class="sxs-lookup"><span data-stu-id="b828c-126">SIP dialog ID, stored as a binary.</span></span> <span data-ttu-id="b828c-127">O formato do binário é:</span><span class="sxs-lookup"><span data-stu-id="b828c-127">The format of the binary is:</span></span></p>
<p><span data-ttu-id="b828c-128">caixa de diálogo; de-marca; até-marca</span><span class="sxs-lookup"><span data-stu-id="b828c-128">dialog;from-tag;to-tag</span></span></p>
<p><span data-ttu-id="b828c-129">Esses dados podem ser convertidos em um formato de texto usando esta sintaxe:</span><span class="sxs-lookup"><span data-stu-id="b828c-129">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(ExternalId as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b828c-130">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b828c-130">


</div>

<span> </span>

</div>

</div>

</span></span></div>

