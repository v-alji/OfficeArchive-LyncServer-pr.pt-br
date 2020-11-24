---
title: 'Lync Server 2013: Tabela Subnet'
description: 'Lync Server 2013: tabela de sub-rede.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Subnet table
ms:assetid: 76f5c995-96c8-4aa3-bc30-1d74991d7c42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398582(v=OCS.15)
ms:contentKeyID: 48184544
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d30c04ddf897e0a62551709b30211ba724a75cbf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389764"
---
# <a name="subnet-table-in-lync-server-2013"></a><span data-ttu-id="64f3d-103">Tabela Subnet no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64f3d-103">Subnet table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="64f3d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="64f3d-104">

<span> </span></span></span>

<span data-ttu-id="64f3d-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="64f3d-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="64f3d-106">A tabela de sub-rede é uma tabela de suporte.</span><span class="sxs-lookup"><span data-stu-id="64f3d-106">The Subnet table is a supporting table.</span></span> <span data-ttu-id="64f3d-107">Cada registro representa uma sub-rede definida na configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="64f3d-107">Each record represents one subnet defined in network configuration setting.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="64f3d-108"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="64f3d-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="64f3d-109"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="64f3d-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="64f3d-110"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="64f3d-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="64f3d-111"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="64f3d-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64f3d-112"><strong>SubnetIP</strong></span><span class="sxs-lookup"><span data-stu-id="64f3d-112"><strong>SubnetIP</strong></span></span></p></td>
<td><p><span data-ttu-id="64f3d-113">int</span><span class="sxs-lookup"><span data-stu-id="64f3d-113">int</span></span></p></td>
<td><p><span data-ttu-id="64f3d-114">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="64f3d-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="64f3d-115">Representação do inteiro para o IP da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="64f3d-115">Integer representation for the subnet IP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64f3d-116"><strong>Máscara_de_Sub-rede</strong></span><span class="sxs-lookup"><span data-stu-id="64f3d-116"><strong>SubnetMask</strong></span></span></p></td>
<td><p><span data-ttu-id="64f3d-117">int</span><span class="sxs-lookup"><span data-stu-id="64f3d-117">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="64f3d-118">Máscara de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="64f3d-118">Subnet mask.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64f3d-119"><strong>UserSiteKey</strong></span><span class="sxs-lookup"><span data-stu-id="64f3d-119"><strong>UserSiteKey</strong></span></span></p></td>
<td><p><span data-ttu-id="64f3d-120">int</span><span class="sxs-lookup"><span data-stu-id="64f3d-120">int</span></span></p></td>
<td><p><span data-ttu-id="64f3d-121">Exterior</span><span class="sxs-lookup"><span data-stu-id="64f3d-121">Foreign</span></span></p></td>
<td><p><span data-ttu-id="64f3d-122">Referenciado da <a href="lync-server-2013-usersite-table.md">tabela usersite no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="64f3d-122">Referenced from the <a href="lync-server-2013-usersite-table.md">UserSite table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64f3d-123"><strong>SubnetDescription</strong></span><span class="sxs-lookup"><span data-stu-id="64f3d-123"><strong>SubnetDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="64f3d-124">nvarchar (512)</span><span class="sxs-lookup"><span data-stu-id="64f3d-124">nvarchar(512)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="64f3d-125">A descrição da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="64f3d-125">The description for the subnet.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="64f3d-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="64f3d-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

