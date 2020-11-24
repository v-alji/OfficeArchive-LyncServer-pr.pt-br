---
title: 'Lync Server 2013: tabela PurgeSettings (QoE)'
description: 'Lync Server 2013: tabela PurgeSettings (QoE).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PurgeSettings table (QoE)
ms:assetid: 31b85d1c-3f32-4f67-94bf-9389cdd282c5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204788(v=OCS.15)
ms:contentKeyID: 48183777
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d515d799a7cc442dc6d34f2ece1a968de51cdad6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390061"
---
# <a name="purgesettings-table-qoe-in-lync-server-2013"></a><span data-ttu-id="93428-103">Tabela PurgeSettings (QoE) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93428-103">PurgeSettings table (QoE) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93428-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93428-104">

<span> </span></span></span>

<span data-ttu-id="93428-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="93428-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="93428-106">A tabela PurgeSettings contém informações que especificam se (e quando) os registros de qualidade desatualizadas da qualidade da experiência serão automaticamente excluídos do banco de dados de QoE.</span><span class="sxs-lookup"><span data-stu-id="93428-106">The PurgeSettings table contains information that specifies if (and when) outdated Quality of Experience records will automatically be deleted from the QoE database.</span></span> <span data-ttu-id="93428-107">Observe que as informações relacionadas à remoção também podem ser obtidas dentro do Shell de gerenciamento do Microsoft Lync Server 2013 executando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="93428-107">Note that purging-related information can also be obtained from within the Microsoft Lync Server 2013 Management Shell by running the following command:</span></span>

    Get-CsQoEConfiguration

<span data-ttu-id="93428-108">Esta tabela foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="93428-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93428-109"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="93428-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="93428-110"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="93428-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="93428-111"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="93428-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="93428-112"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="93428-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93428-113"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="93428-113"><strong>ID</strong></span></span></p></td>
<td><p><span data-ttu-id="93428-114">int</span><span class="sxs-lookup"><span data-stu-id="93428-114">int</span></span></p></td>
<td><p><span data-ttu-id="93428-115">Primária</span><span class="sxs-lookup"><span data-stu-id="93428-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="93428-116">Identificador exclusivo da coleção de configurações de limpeza de QoE.</span><span class="sxs-lookup"><span data-stu-id="93428-116">Unique identifier for the collection of QoE purge settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93428-117"><strong>EnablePurge</strong></span><span class="sxs-lookup"><span data-stu-id="93428-117"><strong>EnablePurge</strong></span></span></p></td>
<td><p><span data-ttu-id="93428-118">bit</span><span class="sxs-lookup"><span data-stu-id="93428-118">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="93428-119">Quando definido como true (1), o Microsoft Lync Server 2013 limpará periodicamente registros desatualizados do banco de dados de QoE.</span><span class="sxs-lookup"><span data-stu-id="93428-119">When set to True (1) Microsoft Lync Server 2013 will periodically purge outdated records from the QoE database.</span></span> <span data-ttu-id="93428-120">A limpeza ocorrerá a cada dia no Tomé especificado pela configuração PurgeHour.</span><span class="sxs-lookup"><span data-stu-id="93428-120">Purging will take place each day at the tome specified by the PurgeHour setting.</span></span> <span data-ttu-id="93428-121">Se definido como falso (0), os registros não serão automaticamente limpos do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="93428-121">If set to False (0) then records will not be automatically purged from the database.</span></span> <span data-ttu-id="93428-122">O valor padrão é True.</span><span class="sxs-lookup"><span data-stu-id="93428-122">The default value is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93428-123"><strong>KeepQoEDataForDays</strong></span><span class="sxs-lookup"><span data-stu-id="93428-123"><strong>KeepQoEDataForDays</strong></span></span></p></td>
<td><p><span data-ttu-id="93428-124">int</span><span class="sxs-lookup"><span data-stu-id="93428-124">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="93428-125">Especifica a idade dos registros de QoE (em dias) que serão removidos do banco de dados: se a limpeza estiver habilitada, os registros de QoE anteriores a esse valor serão removidos do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="93428-125">Specifies the age of QoE records (in days) that will be purged from the database: if purging is enabled, QoE records older than this value will be removed from the database.</span></span> <span data-ttu-id="93428-126">O valor padrão é 60 dias.</span><span class="sxs-lookup"><span data-stu-id="93428-126">The default value is 60 days.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93428-127"><strong>PurgeHour</strong></span><span class="sxs-lookup"><span data-stu-id="93428-127"><strong>PurgeHour</strong></span></span></p></td>
<td><p><span data-ttu-id="93428-128">int</span><span class="sxs-lookup"><span data-stu-id="93428-128">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="93428-129">Especifica a hora local do dia em que a limpeza do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="93428-129">Specifies the local time of day when database purging will take place.</span></span> <span data-ttu-id="93428-130">O horário é especificado utilizando-se um relógio de 24 horas, onde 0 representa a meia-noite (00:00) e 23 representa 23 horas.</span><span class="sxs-lookup"><span data-stu-id="93428-130">The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM.</span></span> <span data-ttu-id="93428-131">Observe que você só pode especificar a hora do dia: é permitido um valor de 10 (indicando 10:00 AM), mas um valor de 10:30 de 10,5 (indicando 10:30 AM) não é permitido.</span><span class="sxs-lookup"><span data-stu-id="93428-131">Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed.</span></span> <span data-ttu-id="93428-132">O valor padrão é 1 (1:00 AM).</span><span class="sxs-lookup"><span data-stu-id="93428-132">The default value is 1 (1:00 AM).</span></span> <span data-ttu-id="93428-133">Especifica a hora local do dia em que a limpeza do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="93428-133">Specifies the local time of day when database purging will take place.</span></span> <span data-ttu-id="93428-134">O horário é especificado utilizando-se um relógio de 24 horas, onde 0 representa a meia-noite (00:00) e 23 representa 23 horas.</span><span class="sxs-lookup"><span data-stu-id="93428-134">The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM.</span></span> <span data-ttu-id="93428-135">Observe que você só pode especificar a hora do dia: é permitido um valor de 10 (indicando 10:00 AM), mas um valor de 10:30 de 10,5 (indicando 10:30 AM) não é permitido.</span><span class="sxs-lookup"><span data-stu-id="93428-135">Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed.</span></span> <span data-ttu-id="93428-136">O valor padrão é 1 (1:00 AM).</span><span class="sxs-lookup"><span data-stu-id="93428-136">The default value is 1 (1:00 AM).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="93428-137">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93428-137">


</div>

<span> </span>

</div>

</div>

</span></span></div>

