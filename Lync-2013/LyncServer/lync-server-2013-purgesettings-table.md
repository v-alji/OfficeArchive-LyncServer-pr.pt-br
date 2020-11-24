---
title: 'Lync Server 2013: tabela PurgeSettings'
description: 'Lync Server 2013: PurgeSettings Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PurgeSettings table
ms:assetid: 9ff2c8fc-4ae8-4f22-96a8-1f4d5eecbf2d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205121(v=OCS.15)
ms:contentKeyID: 48184932
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ec2d1508d8362988bddbab2fe7303a23a8ee2d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390060"
---
# <a name="purgesettings-table-in-lync-server-2013"></a><span data-ttu-id="40893-103">Tabela PurgeSettings no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="40893-103">PurgeSettings table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="40893-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="40893-104">

<span> </span></span></span>

<span data-ttu-id="40893-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="40893-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="40893-106">A tabela PurgeSettings contém informações que especificam se (e quando) registros de detalhes de chamadas desatualizados serão automaticamente excluídos do banco de dados CDR.</span><span class="sxs-lookup"><span data-stu-id="40893-106">The PurgeSettings table contains information that specifies if (and when) outdated call detail records will automatically be deleted from the CDR database.</span></span> <span data-ttu-id="40893-107">Observe que as informações relacionadas à remoção também podem ser obtidas dentro do Shell de gerenciamento do Microsoft Lync Server 2013 executando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="40893-107">Note that purging-related information can also be obtained from within the Microsoft Lync Server 2013 Management Shell by running the following command:</span></span>

    Get-CsCdrConfiguration

<span data-ttu-id="40893-108">Os administradores devem tratar a tabela PurgeSettings como somente leitura: as alterações nas configurações de limpeza de detalhes da chamada devem ser feitas somente usando cmdlets [New-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration) ou [set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="40893-108">Administrators should treat the PurgeSettings table as read-only: changes to the call detail purge settings should only be made using the [New-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration) or [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) cmdlets.</span></span>

<span data-ttu-id="40893-109">Esta tabela foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="40893-109">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40893-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="40893-110">Column</span></span></th>
<th><span data-ttu-id="40893-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="40893-111">Data Type</span></span></th>
<th><span data-ttu-id="40893-112">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="40893-112">Key/Index</span></span></th>
<th><span data-ttu-id="40893-113">Detalhes</span><span class="sxs-lookup"><span data-stu-id="40893-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40893-114"><strong>%</strong></span><span class="sxs-lookup"><span data-stu-id="40893-114"><strong>Id</strong></span></span></p></td>
<td><p><span data-ttu-id="40893-115">int</span><span class="sxs-lookup"><span data-stu-id="40893-115">int</span></span></p></td>
<td><p><span data-ttu-id="40893-116">Primária</span><span class="sxs-lookup"><span data-stu-id="40893-116">Primary</span></span></p></td>
<td><p><span data-ttu-id="40893-117">Identificador exclusivo da coleção de configurações de limpeza de CDR.</span><span class="sxs-lookup"><span data-stu-id="40893-117">Unique identifier for the collection of CDR purge settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40893-118"><strong>EnablePurge</strong></span><span class="sxs-lookup"><span data-stu-id="40893-118"><strong>EnablePurge</strong></span></span></p></td>
<td><p><span data-ttu-id="40893-119">bit</span><span class="sxs-lookup"><span data-stu-id="40893-119">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="40893-120">Quando definido como true (1), o Microsoft Lync Server 2013 limpará periodicamente registros desatualizados do banco de dados CDR.</span><span class="sxs-lookup"><span data-stu-id="40893-120">When set to True (1) Microsoft Lync Server 2013 will periodically purge outdated records from the CDR database.</span></span> <span data-ttu-id="40893-121">A limpeza ocorrerá a cada dia no Tomé especificado pela configuração PurgeHour.</span><span class="sxs-lookup"><span data-stu-id="40893-121">Purging will take place each day at the tome specified by the PurgeHour setting.</span></span> <span data-ttu-id="40893-122">Se definido como falso (0), os registros não serão automaticamente limpos do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="40893-122">If set to False (0) then records will not be automatically purged from the database.</span></span> <span data-ttu-id="40893-123">O valor padrão é True.</span><span class="sxs-lookup"><span data-stu-id="40893-123">The default value is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40893-124"><strong>KeepCallDetailForDays</strong></span><span class="sxs-lookup"><span data-stu-id="40893-124"><strong>KeepCallDetailForDays</strong></span></span></p></td>
<td><p><span data-ttu-id="40893-125">int</span><span class="sxs-lookup"><span data-stu-id="40893-125">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="40893-126">Especifica a idade dos registros CDR (em dias) que serão removidos do banco de dados: se a limpeza estiver habilitada, os registros CDR mais antigos do que esse valor serão removidos do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="40893-126">Specifies the age of CDR records (in days) that will be purged from the database: if purging is enabled, CDR records older than this value will be removed from the database.</span></span> <span data-ttu-id="40893-127">O valor padrão é 60 dias.</span><span class="sxs-lookup"><span data-stu-id="40893-127">The default value is 60 days.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40893-128"><strong>KeepErrorReportForDays</strong></span><span class="sxs-lookup"><span data-stu-id="40893-128"><strong>KeepErrorReportForDays</strong></span></span></p></td>
<td><p><span data-ttu-id="40893-129">int</span><span class="sxs-lookup"><span data-stu-id="40893-129">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="40893-130">Especifica a idade dos registros de relatório de tempo (em dias) que serão removidos do banco de dados: se a limpeza estiver habilitada, os registros de relatório de erros anteriores a esse valor serão removidos do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="40893-130">Specifies the age of error report records (in days) that will be purged from the database: if purging is enabled, error report records older than this value will be removed from the database.</span></span> <span data-ttu-id="40893-131">O valor padrão é 60 dias.</span><span class="sxs-lookup"><span data-stu-id="40893-131">The default value is 60 days.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40893-132"><strong>PurgeHour</strong></span><span class="sxs-lookup"><span data-stu-id="40893-132"><strong>PurgeHour</strong></span></span></p></td>
<td><p><span data-ttu-id="40893-133">int</span><span class="sxs-lookup"><span data-stu-id="40893-133">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="40893-134">Especifica a hora local do dia em que a limpeza do banco de dados ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="40893-134">Specifies the local time of day when database purging will take place.</span></span> <span data-ttu-id="40893-135">O horário é especificado utilizando-se um relógio de 24 horas, onde 0 representa a meia-noite (00:00) e 23 representa 23 horas.</span><span class="sxs-lookup"><span data-stu-id="40893-135">The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM.</span></span> <span data-ttu-id="40893-136">Observe que você só pode especificar a hora do dia: é permitido um valor de 10 (indicando 10:00 AM), mas um valor de 10:30 de 10,5 (indicando 10:30 AM) não é permitido.</span><span class="sxs-lookup"><span data-stu-id="40893-136">Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed.</span></span> <span data-ttu-id="40893-137">O valor padrão é 2 (2:00).</span><span class="sxs-lookup"><span data-stu-id="40893-137">The default value is 2 (2:00 AM).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="40893-138">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="40893-138">


</div>

<span> </span>

</div>

</div>

</span></span></div>

