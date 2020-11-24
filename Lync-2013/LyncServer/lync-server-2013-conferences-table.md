---
title: 'Lync Server 2013: Tabela Conferences'
description: 'Lync Server 2013: tabela conferências.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferences table
ms:assetid: c3da6271-b3c6-4898-894f-10456ec794d0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412964(v=OCS.15)
ms:contentKeyID: 48185340
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e0d8c61e795dc0c8f9843b871d7e4efd1bec571
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390183"
---
# <a name="conferences-table-in-lync-server-2013"></a><span data-ttu-id="17c63-103">Tabela Conferences no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="17c63-103">Conferences table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="17c63-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="17c63-104">

<span> </span></span></span>

<span data-ttu-id="17c63-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="17c63-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="17c63-106">Cada registro desta tabela contém detalhes da chamada sobre uma conferência.</span><span class="sxs-lookup"><span data-stu-id="17c63-106">Each record in this table contains call details about one conference.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="17c63-107">Coluna</span><span class="sxs-lookup"><span data-stu-id="17c63-107">Column</span></span></th>
<th><span data-ttu-id="17c63-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="17c63-108">Data Type</span></span></th>
<th><span data-ttu-id="17c63-109">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="17c63-109">Key/Index</span></span></th>
<th><span data-ttu-id="17c63-110">Detalhes</span><span class="sxs-lookup"><span data-stu-id="17c63-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17c63-111"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="17c63-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="17c63-112">datetime</span><span class="sxs-lookup"><span data-stu-id="17c63-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="17c63-113">Primária</span><span class="sxs-lookup"><span data-stu-id="17c63-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="17c63-114">Hora em que a solicitação de conferência foi capturada pelo agente de CDR.</span><span class="sxs-lookup"><span data-stu-id="17c63-114">Time that the conference request was captured by the CDR agent.</span></span> <span data-ttu-id="17c63-115">Usado apenas como uma chave primária para identificar uma instância de conferência de forma exclusiva.</span><span class="sxs-lookup"><span data-stu-id="17c63-115">Used only as a primary key to uniquely identify a conference instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17c63-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="17c63-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="17c63-117">int</span><span class="sxs-lookup"><span data-stu-id="17c63-117">int</span></span></p></td>
<td><p><span data-ttu-id="17c63-118">Primária</span><span class="sxs-lookup"><span data-stu-id="17c63-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="17c63-119">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="17c63-119">ID number to identify the session.</span></span> <span data-ttu-id="17c63-120">Usado em conjunto com a <strong>identificação_da_sessãotime</strong> para identificar exclusivamente uma instância de conferência.</span><span class="sxs-lookup"><span data-stu-id="17c63-120">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> *</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17c63-121"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="17c63-121"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="17c63-122">int</span><span class="sxs-lookup"><span data-stu-id="17c63-122">int</span></span></p></td>
<td><p><span data-ttu-id="17c63-123">Exterior</span><span class="sxs-lookup"><span data-stu-id="17c63-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="17c63-124">URL da conferência.</span><span class="sxs-lookup"><span data-stu-id="17c63-124">Conference URI.</span></span> <span data-ttu-id="17c63-125">Consulte a <a href="lync-server-2013-conferenceuris-table.md">tabela ConferenceUris no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="17c63-125">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17c63-126"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="17c63-126"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="17c63-127">identificador</span><span class="sxs-lookup"><span data-stu-id="17c63-127">uniqueidentifier</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="17c63-128">Útil para conferências recorrentes; cada instância de uma conferência recorrente tem o mesmo <strong>ConferenceUri</strong>, mas terá um <strong>ConfInstance</strong>diferente.</span><span class="sxs-lookup"><span data-stu-id="17c63-128">Useful for recurring conferences; each instance of a recurring conference has the same <strong>ConferenceUri</strong>, but will have a different <strong>ConfInstance</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17c63-129"><strong>ConferenceStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="17c63-129"><strong>ConferenceStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="17c63-130">datetime</span><span class="sxs-lookup"><span data-stu-id="17c63-130">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="17c63-131">Hora de início da conferência.</span><span class="sxs-lookup"><span data-stu-id="17c63-131">Conference start time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17c63-132"><strong>ConferenceEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="17c63-132"><strong>ConferenceEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="17c63-133">datetime</span><span class="sxs-lookup"><span data-stu-id="17c63-133">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="17c63-134">Hora de início da conferência.</span><span class="sxs-lookup"><span data-stu-id="17c63-134">Conference start time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17c63-135"><strong>Poolid</strong></span><span class="sxs-lookup"><span data-stu-id="17c63-135"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="17c63-136">int</span><span class="sxs-lookup"><span data-stu-id="17c63-136">int</span></span></p></td>
<td><p><span data-ttu-id="17c63-137">Exterior</span><span class="sxs-lookup"><span data-stu-id="17c63-137">Foreign</span></span></p></td>
<td><p><span data-ttu-id="17c63-138">Número de identificação para identificar o pool no qual a conferência foi capturada.</span><span class="sxs-lookup"><span data-stu-id="17c63-138">ID number to identify the pool in which the conference was captured.</span></span> <span data-ttu-id="17c63-139">Consulte a <a href="lync-server-2013-pools-table.md">tabela de grupos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="17c63-139">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17c63-140"><strong>OrganizerId</strong></span><span class="sxs-lookup"><span data-stu-id="17c63-140"><strong>OrganizerId</strong></span></span></p></td>
<td><p><span data-ttu-id="17c63-141">Núm</span><span class="sxs-lookup"><span data-stu-id="17c63-141">Int</span></span></p></td>
<td><p><span data-ttu-id="17c63-142">Exterior</span><span class="sxs-lookup"><span data-stu-id="17c63-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="17c63-143">Número de identificação para identificar o URI do organizador dessa conferência.</span><span class="sxs-lookup"><span data-stu-id="17c63-143">ID number to identify the organizer URI of this conference.</span></span> <span data-ttu-id="17c63-144">Consulte a <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="17c63-144">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17c63-145"><strong>Sinalizador</strong></span><span class="sxs-lookup"><span data-stu-id="17c63-145"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="17c63-146">smallint</span><span class="sxs-lookup"><span data-stu-id="17c63-146">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="17c63-147">Uma máscara de bits que contém atributos de conferência.</span><span class="sxs-lookup"><span data-stu-id="17c63-147">A bit mask that contains Conference Attributes.</span></span> <span data-ttu-id="17c63-148">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="17c63-148">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="17c63-149">0X01</span><span class="sxs-lookup"><span data-stu-id="17c63-149">0X01</span></span></p></li>
<li><p><span data-ttu-id="17c63-150">Sintética</span><span class="sxs-lookup"><span data-stu-id="17c63-150">Synthetic</span></span></p></li>
<li><p><span data-ttu-id="17c63-151">Transação</span><span class="sxs-lookup"><span data-stu-id="17c63-151">Transaction</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17c63-152"><strong>Processe</strong></span><span class="sxs-lookup"><span data-stu-id="17c63-152"><strong>Processed</strong></span></span></p></td>
<td><p><span data-ttu-id="17c63-153">bit</span><span class="sxs-lookup"><span data-stu-id="17c63-153">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="17c63-154">Campo interno usado pelo serviço de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="17c63-154">Internal field used by the Monitoring service.</span></span></p>
<p><span data-ttu-id="17c63-155">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="17c63-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="17c63-156">\* Para a maioria das sessões, o SessionIdSeq terá o valor de 1.</span><span class="sxs-lookup"><span data-stu-id="17c63-156">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="17c63-157">Se duas sessões começarem exatamente ao mesmo tempo, o SessionIdSeq de uma será 1 e, para a outra, será 2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="17c63-157">If two sessions start at exactly the same time, the SessionIdSeq for one will be 1, and for the other will be 2, and so on.</span></span>

<span data-ttu-id="17c63-158"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="17c63-158"></div>

<span> </span>

</div>

</div>

</span></span></div>

