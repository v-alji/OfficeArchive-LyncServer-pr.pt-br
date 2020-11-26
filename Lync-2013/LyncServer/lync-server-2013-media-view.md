---
title: 'Lync Server 2013: modo de exibição de mídia'
description: 'Lync Server 2013: modo de exibição de mídia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media view
ms:assetid: 1a7b2e59-082e-4188-98ae-48ae9bd3494a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687981(v=OCS.15)
ms:contentKeyID: 49733570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74643986b12a30b1055a46a37febf90eeb70c514
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446034"
---
# <a name="media-view-in-lync-server-2013"></a><span data-ttu-id="335ff-103">Modo de exibição de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="335ff-103">Media view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="335ff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="335ff-104">

<span> </span></span></span>

<span data-ttu-id="335ff-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="335ff-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="335ff-106">O modo de exibição mídia armazena informações sobre um tipo de mídia usado em uma sessão ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="335ff-106">The Media view stores information about one media type used in a peer-to-peer session.</span></span> <span data-ttu-id="335ff-107">Uma sessão seria representada por vários registros na tabela, se mais de um tipo de mídia for usado.</span><span class="sxs-lookup"><span data-stu-id="335ff-107">One session would be represented by multiple records in the table, if more than one media type is used.</span></span> <span data-ttu-id="335ff-108">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="335ff-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="335ff-109">O modo de exibição de mídia não deve ser usado para calcular a duração da mídia de uma sessão.</span><span class="sxs-lookup"><span data-stu-id="335ff-109">The Media view should not be used to calculate the media duration for a session.</span></span> <span data-ttu-id="335ff-110">Este modo de exibição contém os detalhes de sinalização da troca de mídia em uma sessão.</span><span class="sxs-lookup"><span data-stu-id="335ff-110">This view contains the signaling details of media exchange in a session.</span></span> <span data-ttu-id="335ff-111">A troca de mídia é feita pela solicitação de convite e StartTime indica a hora em que o convite foi enviado. O tempo de convite não significa necessariamente a hora de início da mídia porque a mídia só inicia após a aceitação da sessão.</span><span class="sxs-lookup"><span data-stu-id="335ff-111">Media exchange is done by the INVITE request, and StartTime indicates the time that the INVITE was sent out. The invite time does not necessarily mean the media start time, because media starts only after the session is accepted.</span></span>



</div>

<span data-ttu-id="335ff-112">O modo de exibição de mídia contém todas as colunas na [exibição SessionDetails no Lync Server 2013](lync-server-2013-sessiondetails-view.md) , além das listadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="335ff-112">The Media view contains all of the columns in the [SessionDetails view in Lync Server 2013](lync-server-2013-sessiondetails-view.md) in addition the ones listed below.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="335ff-113">Coluna</span><span class="sxs-lookup"><span data-stu-id="335ff-113">Column</span></span></th>
<th><span data-ttu-id="335ff-114">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="335ff-114">Data Type</span></span></th>
<th><span data-ttu-id="335ff-115">Detalhes</span><span class="sxs-lookup"><span data-stu-id="335ff-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="335ff-116"><strong>Media</strong></span><span class="sxs-lookup"><span data-stu-id="335ff-116"><strong>Media</strong></span></span></p></td>
<td><p><span data-ttu-id="335ff-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="335ff-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="335ff-118">Tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="335ff-118">Media type.</span></span> <span data-ttu-id="335ff-119">Consulte a <a href="lync-server-2013-medialist-table.md">tabela medialist no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="335ff-119">See the <a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="335ff-120"><strong>MediaStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="335ff-120"><strong>MediaStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="335ff-121">datetime</span><span class="sxs-lookup"><span data-stu-id="335ff-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="335ff-122">Tempo em que uma solicitação de mídia foi enviada.</span><span class="sxs-lookup"><span data-stu-id="335ff-122">Time that a media request was sent out.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="335ff-123"><strong>MediaEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="335ff-123"><strong>MediaEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="335ff-124">datetime</span><span class="sxs-lookup"><span data-stu-id="335ff-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="335ff-125">Hora de término da sessão.</span><span class="sxs-lookup"><span data-stu-id="335ff-125">End time of the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="335ff-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="335ff-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

