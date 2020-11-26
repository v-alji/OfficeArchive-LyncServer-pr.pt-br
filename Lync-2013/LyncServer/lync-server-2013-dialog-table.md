---
title: 'Lync Server 2013: Tabela Dialog'
description: 'Lync Server 2013: tabela da caixa de diálogo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dialog table
ms:assetid: 4d93424f-9072-43f5-83c2-3d539e3e9ca6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398313(v=OCS.15)
ms:contentKeyID: 48184068
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ae93b8ca9f1146b7dc164803f27cbeeadc66777
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429200"
---
# <a name="dialog-table-in-lync-server-2013"></a><span data-ttu-id="bb0eb-103">Tabela Dialog no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb0eb-103">Dialog table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bb0eb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bb0eb-104">

<span> </span></span></span>

<span data-ttu-id="bb0eb-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="bb0eb-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="bb0eb-106">A tabela de caixa de diálogo é uma tabela de suporte; cada registro representa uma caixa de diálogo SIP (protocolo de início de sessão).</span><span class="sxs-lookup"><span data-stu-id="bb0eb-106">The Dialog table is a supporting table; each record represents one Session Initiation Protocol (SIP) dialog.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb0eb-107"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="bb0eb-107"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="bb0eb-108"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="bb0eb-108"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="bb0eb-109"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="bb0eb-109"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="bb0eb-110"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="bb0eb-110"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb0eb-111"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="bb0eb-111"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="bb0eb-112">datetime</span><span class="sxs-lookup"><span data-stu-id="bb0eb-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="bb0eb-113">Primária</span><span class="sxs-lookup"><span data-stu-id="bb0eb-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="bb0eb-114">Tempo quando o agente de Quality of Excellence (QoE) recebe o primeiro relatório do chamador ou do receptor.</span><span class="sxs-lookup"><span data-stu-id="bb0eb-114">Time when the Quality of Excellence (QoE) agent receives the first report from either caller or callee.</span></span> <span data-ttu-id="bb0eb-115">Usado em conjunto com o SessionSeq para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="bb0eb-115">Used in conjunction with SessionSeq to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb0eb-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="bb0eb-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="bb0eb-117">int</span><span class="sxs-lookup"><span data-stu-id="bb0eb-117">int</span></span></p></td>
<td><p><span data-ttu-id="bb0eb-118">Primária</span><span class="sxs-lookup"><span data-stu-id="bb0eb-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="bb0eb-119">Número de sequência para diferenciar sessões quando elas tiverem o mesmo ConferenceDateTime.</span><span class="sxs-lookup"><span data-stu-id="bb0eb-119">Sequence number to differentiate sessions when they have the same ConferenceDateTime.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb0eb-120"><strong>Caixa de diálogo</strong></span><span class="sxs-lookup"><span data-stu-id="bb0eb-120"><strong>DialogID</strong></span></span></p></td>
<td><p><span data-ttu-id="bb0eb-121">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="bb0eb-121">varchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="bb0eb-122">IDENTIFICAÇÃO da caixa de diálogo que é globalmente exclusiva.</span><span class="sxs-lookup"><span data-stu-id="bb0eb-122">Dialog ID which is globally unique.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb0eb-123"><strong>DialogIDChecksum</strong></span><span class="sxs-lookup"><span data-stu-id="bb0eb-123"><strong>DialogIDChecksum</strong></span></span></p></td>
<td><p><span data-ttu-id="bb0eb-124">int</span><span class="sxs-lookup"><span data-stu-id="bb0eb-124">int</span></span></p></td>
<td><p><span data-ttu-id="bb0eb-125">dedo</span><span class="sxs-lookup"><span data-stu-id="bb0eb-125">index</span></span></p></td>
<td><p><span data-ttu-id="bb0eb-126">Checksum da ID da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bb0eb-126">Checksum of the Dialog ID.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bb0eb-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bb0eb-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

