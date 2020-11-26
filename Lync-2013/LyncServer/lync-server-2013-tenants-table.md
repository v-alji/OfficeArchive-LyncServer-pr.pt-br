---
title: 'Lync Server 2013: Tabela Tenants'
description: 'Lync Server 2013: tabela de locatários.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Tenants table
ms:assetid: c1b070c1-2c59-4ca9-910b-43f673f97fda
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412950(v=OCS.15)
ms:contentKeyID: 48185309
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 96025dfd9fb42a6083f7f3daca98e243f01a8516
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441281"
---
# <a name="tenants-table-in-lync-server-2013"></a><span data-ttu-id="3b14c-103">Tabela Tenants no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3b14c-103">Tenants table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3b14c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3b14c-104">

<span> </span></span></span>

<span data-ttu-id="3b14c-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="3b14c-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="3b14c-106">A tabela locatários é uma tabela de suporte que armazena uma lista de vários locatários.</span><span class="sxs-lookup"><span data-stu-id="3b14c-106">The Tenants table is a supporting table that stores a list of the various tenants.</span></span> <span data-ttu-id="3b14c-107">Cada registro na tabela representa um locatário.</span><span class="sxs-lookup"><span data-stu-id="3b14c-107">Each record in the table represents one tenant.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3b14c-108">Na implantação local, o CDR usa a ID de locatário de compilação para indicar um tipo de autenticação diferente, como conectividade de mensagem de chat pública, federada e anônima.</span><span class="sxs-lookup"><span data-stu-id="3b14c-108">In on-premises deployment, CDR uses the build-in Tenant ID to indicate different authentication type, such as public IM connectivity, Federated and Anonymous.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b14c-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="3b14c-109">Column</span></span></th>
<th><span data-ttu-id="3b14c-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3b14c-110">Data Type</span></span></th>
<th><span data-ttu-id="3b14c-111">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="3b14c-111">Key/Index</span></span></th>
<th><span data-ttu-id="3b14c-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="3b14c-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b14c-113"><strong>Tenantid</strong></span><span class="sxs-lookup"><span data-stu-id="3b14c-113"><strong>TenantId</strong></span></span></p></td>
<td><p><span data-ttu-id="3b14c-114">int</span><span class="sxs-lookup"><span data-stu-id="3b14c-114">int</span></span></p></td>
<td><p><span data-ttu-id="3b14c-115">Primária</span><span class="sxs-lookup"><span data-stu-id="3b14c-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="3b14c-116">Número exclusivo que identifica esta ID de locatário.</span><span class="sxs-lookup"><span data-stu-id="3b14c-116">Unique number identifying this Tenant ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b14c-117"><strong>TenantKey</strong></span><span class="sxs-lookup"><span data-stu-id="3b14c-117"><strong>TenantKey</strong></span></span></p></td>
<td><p><span data-ttu-id="3b14c-118">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="3b14c-118">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3b14c-119">Valores permitidos:</span><span class="sxs-lookup"><span data-stu-id="3b14c-119">Allowed values:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b14c-120">00000000-0000-0000-0000-000000000000 – empresa</span><span class="sxs-lookup"><span data-stu-id="3b14c-120">00000000-0000-0000-0000-000000000000 – Enterprise</span></span></p></li>
<li><p><span data-ttu-id="3b14c-121">00000000-0000-0000-0000-000000000001 – federado</span><span class="sxs-lookup"><span data-stu-id="3b14c-121">00000000-0000-0000-0000-000000000001 – Federated</span></span></p></li>
<li><p><span data-ttu-id="3b14c-122">00000000-0000-0000-0000-000000000002 – anônimo</span><span class="sxs-lookup"><span data-stu-id="3b14c-122">00000000-0000-0000-0000-000000000002 – Anonymous</span></span></p></li>
<li><p><span data-ttu-id="3b14c-123">00000000-0000-0000-0000-000000000003 – conectividade de IM pública</span><span class="sxs-lookup"><span data-stu-id="3b14c-123">00000000-0000-0000-0000-000000000003 – Public IM connectivity</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="3b14c-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3b14c-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

