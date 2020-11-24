---
title: 'Lync Server 2013: monitorando o desempenho de armazenamento do Lync Server back-end'
description: 'Lync Server 2013: monitorando o desempenho de armazenamento do Lync Server de back-end.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring back end Lync Server 2013 storage performance
ms:assetid: 71627c70-1953-4ac2-afbe-f3ad85be0f44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720917(v=OCS.15)
ms:contentKeyID: 63969619
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7501418d3589b941b7e92d2b414492c1d27a3ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389878"
---
# <a name="monitoring-back-end-lync-server-2013-storage-performance"></a><span data-ttu-id="647b2-103">Monitorando o back-end do Lync Server 2013 Storage performance</span><span class="sxs-lookup"><span data-stu-id="647b2-103">Monitoring back end Lync Server 2013 storage performance</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="647b2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="647b2-104">

<span> </span></span></span>

<span data-ttu-id="647b2-105">_**Tópico da última modificação:** 2014-05-02_</span><span class="sxs-lookup"><span data-stu-id="647b2-105">_**Topic Last Modified:** 2014-05-02_</span></span>

<span data-ttu-id="647b2-106">Os bancos de dados back-end do Lync Server 2013 são uma parte muito importante da implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="647b2-106">The Lync Server 2013 back-end databases are a very important part of the Lync Server 2013 deployment.</span></span> <span data-ttu-id="647b2-107">Recomendamos que você monitore constantemente os bancos de dados e os respectivos registros de transações para ajudar a garantir que o back-end do Lync Server 2013 seja executado de forma ideal.</span><span class="sxs-lookup"><span data-stu-id="647b2-107">We recommend constantly monitoring the databases and respective transaction logs to help to make sure that the Lync Server 2013 back end is performing optimally.</span></span>

<span data-ttu-id="647b2-108">A tabela a seguir identifica contadores de desempenho que devem ser monitorados para obter informações sobre o desempenho do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="647b2-108">The following table identifies performance counters that should be monitored to learn information about Storage Performance.</span></span> <span data-ttu-id="647b2-109">Os valores da linha de base desses contadores devem ser determinados primeiro (quando o sistema está em sua carga normal, esperada) para entender as alterações de desempenho quando o sistema é testado.</span><span class="sxs-lookup"><span data-stu-id="647b2-109">The baseline values for these counters must be determined first (when system is at its normal, expected load) to understand the performance changes when system is stressed.</span></span>

### <a name="performance-counters-to-be-monitored"></a><span data-ttu-id="647b2-110">Contadores de desempenho a serem monitorados</span><span class="sxs-lookup"><span data-stu-id="647b2-110">Performance counters to be monitored</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="647b2-111">Contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="647b2-111">Performance Counter</span></span></th>
<th><span data-ttu-id="647b2-112">Limites da linha de base</span><span class="sxs-lookup"><span data-stu-id="647b2-112">Baseline thresholds</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="647b2-113">Transações/s (RTC)</span><span class="sxs-lookup"><span data-stu-id="647b2-113">Transactions/sec (RTC)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="647b2-114">Transações/s (RTCDyn)</span><span class="sxs-lookup"><span data-stu-id="647b2-114">Transactions/sec (rtcdyn)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="647b2-115">Transações/s (tempdb)</span><span class="sxs-lookup"><span data-stu-id="647b2-115">Transactions/sec (tempdb)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="647b2-116">Liberações de log/s (RTC)</span><span class="sxs-lookup"><span data-stu-id="647b2-116">Log Flushes/sec (RTC)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="647b2-117">Liberações de log/s (RTCDyn)</span><span class="sxs-lookup"><span data-stu-id="647b2-117">Log Flushes/sec (rtcdyn)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="647b2-118">Liberações de log/s (tempdb)</span><span class="sxs-lookup"><span data-stu-id="647b2-118">Log Flushes/sec (tempdb)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="647b2-119">Transferências de disco/s (leitura + gravação)-BD RTC</span><span class="sxs-lookup"><span data-stu-id="647b2-119">Disk Transfers/sec (read+write) - RTC db</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="647b2-120">Transferências de disco/s-log de RTC</span><span class="sxs-lookup"><span data-stu-id="647b2-120">Disk Transfers/sec - RTC log</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="647b2-121">Transferências de disco/s-RTCDyn DB</span><span class="sxs-lookup"><span data-stu-id="647b2-121">Disk Transfers/sec - rtcdyn db</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="647b2-122">Transferências de disco/log SEC-RTCDyn</span><span class="sxs-lookup"><span data-stu-id="647b2-122">Disk Transfers/sec - rtcdyn log</span></span></p></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="647b2-123">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="647b2-123">


</div>

<span> </span>

</div>

</div>

</span></span></div>

