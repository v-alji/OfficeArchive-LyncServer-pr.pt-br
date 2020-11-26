---
title: 'Lync Server 2013: Tabela Devices'
description: 'Lync Server 2013: tabela de dispositivos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Devices table
ms:assetid: 532e2280-4bbc-4a6c-93da-45d9f80a30a0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398351(v=OCS.15)
ms:contentKeyID: 48184169
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 763e1788e2874f9f9831c089ffe8fa077621b030
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429336"
---
# <a name="devices-table-in-lync-server-2013"></a><span data-ttu-id="78acf-103">Tabela Devices no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="78acf-103">Devices table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="78acf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="78acf-104">

<span> </span></span></span>

<span data-ttu-id="78acf-105">_**Tópico da última modificação:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="78acf-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="78acf-106">A tabela dispositivos é uma tabela de suporte.</span><span class="sxs-lookup"><span data-stu-id="78acf-106">The Devices table is a supporting table.</span></span> <span data-ttu-id="78acf-107">Cada registro armazena informações sobre um dispositivo (telefone de mesa).</span><span class="sxs-lookup"><span data-stu-id="78acf-107">Each record stores information about one device (desk phone).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78acf-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="78acf-108">Column</span></span></th>
<th><span data-ttu-id="78acf-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="78acf-109">Data Type</span></span></th>
<th><span data-ttu-id="78acf-110">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="78acf-110">Key/Index</span></span></th>
<th><span data-ttu-id="78acf-111">Detalhes</span><span class="sxs-lookup"><span data-stu-id="78acf-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78acf-112"><strong>DeviceId</strong></span><span class="sxs-lookup"><span data-stu-id="78acf-112"><strong>DeviceId</strong></span></span></p></td>
<td><p><span data-ttu-id="78acf-113">int</span><span class="sxs-lookup"><span data-stu-id="78acf-113">int</span></span></p></td>
<td><p><span data-ttu-id="78acf-114">Primária</span><span class="sxs-lookup"><span data-stu-id="78acf-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="78acf-115">Número exclusivo que identifica esta versão de hardware.</span><span class="sxs-lookup"><span data-stu-id="78acf-115">Unique number identifying this hardware version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78acf-116"><strong>ManufacturerId</strong></span><span class="sxs-lookup"><span data-stu-id="78acf-116"><strong>ManufacturerId</strong></span></span></p></td>
<td><p><span data-ttu-id="78acf-117">int</span><span class="sxs-lookup"><span data-stu-id="78acf-117">int</span></span></p></td>
<td><p><span data-ttu-id="78acf-118">Exterior</span><span class="sxs-lookup"><span data-stu-id="78acf-118">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78acf-119">Fabricante do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78acf-119">Manufacturer of this device.</span></span> <span data-ttu-id="78acf-120">Consulte a <a href="lync-server-2013-manufacturers-table.md">tabela fabricantes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="78acf-120">See the <a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78acf-121"><strong>HardwareVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="78acf-121"><strong>HardwareVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="78acf-122">int</span><span class="sxs-lookup"><span data-stu-id="78acf-122">int</span></span></p></td>
<td><p><span data-ttu-id="78acf-123">Exterior</span><span class="sxs-lookup"><span data-stu-id="78acf-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78acf-124">Versão de hardware deste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78acf-124">Hardware version of this device.</span></span> <span data-ttu-id="78acf-125">Consulte a <a href="lync-server-2013-hardwareversions-table.md">tabela HardwareVersions no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="78acf-125">See the <a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78acf-126"><strong>MacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="78acf-126"><strong>MacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="78acf-127">bigint</span><span class="sxs-lookup"><span data-stu-id="78acf-127">bigint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78acf-128">Endereço MAC</span><span class="sxs-lookup"><span data-stu-id="78acf-128">MAC Address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="78acf-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="78acf-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

