---
title: 'Lync Server 2013: modo de exibição ConferenceMessageCount'
description: 'Lync Server 2013: modo de exibição ConferenceMessageCount.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceMessageCount view
ms:assetid: 8ee3ee95-fb78-4d4e-bcdd-6ce5a0a23b44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688129(v=OCS.15)
ms:contentKeyID: 49733727
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 212d6e1a346253809fb70806424350cc7fc0dfe2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434428"
---
# <a name="conferencemessagecount-view-in-lync-server-2013"></a><span data-ttu-id="5813e-103">Exibição ConferenceMessageCount no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5813e-103">ConferenceMessageCount view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5813e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5813e-104">

<span> </span></span></span>

<span data-ttu-id="5813e-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="5813e-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="5813e-106">A exibição ConferenceMessageCount armazena informações sobre quantas mensagens foram enviadas por um usuário para uma conferência.</span><span class="sxs-lookup"><span data-stu-id="5813e-106">The ConferenceMessageCount view stores information about how many messages were sent by a user to a conference.</span></span> <span data-ttu-id="5813e-107">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5813e-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5813e-108">A exibição ConferenceMessageCount contém todas as colunas na <A href="lync-server-2013-conferencesessiondetails-view.md">exibição ConferenceSessionDetails do Lync Server 2013</A> , além das colunas listadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="5813e-108">The ConferenceMessageCount view contains all of the columns in the <A href="lync-server-2013-conferencesessiondetails-view.md">ConferenceSessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5813e-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="5813e-109">Column</span></span></th>
<th><span data-ttu-id="5813e-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5813e-110">Data Type</span></span></th>
<th><span data-ttu-id="5813e-111">Detalhes</span><span class="sxs-lookup"><span data-stu-id="5813e-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5813e-112"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="5813e-112"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="5813e-113">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="5813e-113">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5813e-114">URL do usuário que enviou a mensagem.</span><span class="sxs-lookup"><span data-stu-id="5813e-114">URI of the user who sent the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5813e-115"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="5813e-115"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="5813e-116">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5813e-116">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5813e-117">Tipo de URI do usuário que enviou as mensagens.</span><span class="sxs-lookup"><span data-stu-id="5813e-117">Type of URI of the user who sent the messages.</span></span> <span data-ttu-id="5813e-118">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="5813e-118">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5813e-119"><strong>Userlocatário</strong></span><span class="sxs-lookup"><span data-stu-id="5813e-119"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="5813e-120">identificador</span><span class="sxs-lookup"><span data-stu-id="5813e-120">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="5813e-121">Locatário do usuário que enviou as mensagens.</span><span class="sxs-lookup"><span data-stu-id="5813e-121">Tenant of user who sent the messages.</span></span> <span data-ttu-id="5813e-122">Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="5813e-122">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5813e-123"><strong>UserMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="5813e-123"><strong>UserMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="5813e-124">smallint</span><span class="sxs-lookup"><span data-stu-id="5813e-124">smallint</span></span></p></td>
<td><p><span data-ttu-id="5813e-125">Número de mensagens enviadas pelo usuário durante a sessão de conferência.</span><span class="sxs-lookup"><span data-stu-id="5813e-125">Number of messages sent by the user during the conference session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5813e-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5813e-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

