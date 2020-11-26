---
title: 'Lync Server 2013: modo de exibição de conferências'
description: 'Lync Server 2013: modo de exibição conferências.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferences view
ms:assetid: c0e5c4db-c135-401f-9296-e9a49f6499a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721871(v=OCS.15)
ms:contentKeyID: 49733803
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dee7fbb7c839c351fc9c81716a5800a678980549
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434421"
---
# <a name="conferences-view-in-lync-server-2013"></a><span data-ttu-id="409e3-103">Modo de exibição conferências no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="409e3-103">Conferences view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="409e3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="409e3-104">

<span> </span></span></span>

<span data-ttu-id="409e3-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="409e3-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="409e3-106">O modo de exibição conferências armazena informações sobre as conferências.</span><span class="sxs-lookup"><span data-stu-id="409e3-106">The Conferences View stores information about the conferences.</span></span> <span data-ttu-id="409e3-107">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="409e3-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="409e3-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="409e3-108">Column</span></span></th>
<th><span data-ttu-id="409e3-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="409e3-109">Data Type</span></span></th>
<th><span data-ttu-id="409e3-110">Detalhes</span><span class="sxs-lookup"><span data-stu-id="409e3-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="409e3-111"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="409e3-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="409e3-112">datetime</span><span class="sxs-lookup"><span data-stu-id="409e3-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="409e3-113">Tempo de solicitação de sessão.</span><span class="sxs-lookup"><span data-stu-id="409e3-113">Time of session request.</span></span> <span data-ttu-id="409e3-114">Usado em conjunto com o SessionIdSeq para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="409e3-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="409e3-115">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="409e3-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="409e3-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="409e3-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="409e3-117">int</span><span class="sxs-lookup"><span data-stu-id="409e3-117">int</span></span></p></td>
<td><p><span data-ttu-id="409e3-118">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="409e3-118">ID number to identify the session.</span></span> <span data-ttu-id="409e3-119">Usado em conjunto com a Identificação_da_sessãotime para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="409e3-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="409e3-120">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="409e3-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="409e3-121"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="409e3-121"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="409e3-122">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="409e3-122">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="409e3-123">URL para a conferência.</span><span class="sxs-lookup"><span data-stu-id="409e3-123">URI for the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="409e3-124"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="409e3-124"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="409e3-125">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="409e3-125">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="409e3-126">Tipo de URL da conferência.</span><span class="sxs-lookup"><span data-stu-id="409e3-126">Type of the conference URI.</span></span> <span data-ttu-id="409e3-127">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="409e3-127">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="409e3-128"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="409e3-128"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="409e3-129">identificador</span><span class="sxs-lookup"><span data-stu-id="409e3-129">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="409e3-130">Usado para conferências recorrentes.</span><span class="sxs-lookup"><span data-stu-id="409e3-130">Used for recurring conferences.</span></span> <span data-ttu-id="409e3-131">Cada instância de uma conferência recorrente tem o mesmo ConferenceUri, mas um ConfInstance diferente.</span><span class="sxs-lookup"><span data-stu-id="409e3-131">Each instance of a recurring conference has the same ConferenceUri but a different ConfInstance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="409e3-132"><strong>ConferenceStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="409e3-132"><strong>ConferenceStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="409e3-133">datetime</span><span class="sxs-lookup"><span data-stu-id="409e3-133">datetime</span></span></p></td>
<td><p><span data-ttu-id="409e3-134">Hora de início da conferência.</span><span class="sxs-lookup"><span data-stu-id="409e3-134">Starting time for the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="409e3-135"><strong>ConferenceEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="409e3-135"><strong>ConferenceEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="409e3-136">datetime</span><span class="sxs-lookup"><span data-stu-id="409e3-136">datetime</span></span></p></td>
<td><p><span data-ttu-id="409e3-137">Hora de término da conferência.</span><span class="sxs-lookup"><span data-stu-id="409e3-137">Ending time for the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="409e3-138"><strong>OrganizerUri</strong></span><span class="sxs-lookup"><span data-stu-id="409e3-138"><strong>OrganizerUri</strong></span></span></p></td>
<td><p><span data-ttu-id="409e3-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="409e3-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="409e3-140">URI do usuário que organizou a conferência.</span><span class="sxs-lookup"><span data-stu-id="409e3-140">URI of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="409e3-141"><strong>OrganizerType</strong></span><span class="sxs-lookup"><span data-stu-id="409e3-141"><strong>OrganizerType</strong></span></span></p></td>
<td><p><span data-ttu-id="409e3-142">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="409e3-142">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="409e3-143">Tipo de URI do usuário que organizou a conferência.</span><span class="sxs-lookup"><span data-stu-id="409e3-143">Type of URI of the user who organized the conference.</span></span> <span data-ttu-id="409e3-144">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="409e3-144">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="409e3-145"><strong>OrganizerTenant</strong></span><span class="sxs-lookup"><span data-stu-id="409e3-145"><strong>OrganizerTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="409e3-146">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="409e3-146">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="409e3-147">Locatário do usuário que organizou a conferência.</span><span class="sxs-lookup"><span data-stu-id="409e3-147">Tenant of the user who organized the conference.</span></span> <span data-ttu-id="409e3-148">Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="409e3-148">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="409e3-149"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="409e3-149"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="409e3-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="409e3-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="409e3-151">Nome de domínio totalmente qualificado do pool que hospeda a conferência.</span><span class="sxs-lookup"><span data-stu-id="409e3-151">Fully qualified domain name of the pool that hosted the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="409e3-152"><strong>Sinalizador</strong></span><span class="sxs-lookup"><span data-stu-id="409e3-152"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="409e3-153">smallint</span><span class="sxs-lookup"><span data-stu-id="409e3-153">smallint</span></span></p></td>
<td><p><span data-ttu-id="409e3-154">Máscara de bits que contém atributos de conferência.</span><span class="sxs-lookup"><span data-stu-id="409e3-154">Bit mask that contains Conference Attributes.</span></span> <span data-ttu-id="409e3-155">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="409e3-155">Possible values are:</span></span></p>
<p><span data-ttu-id="409e3-156">0X01 – transação sintética</span><span class="sxs-lookup"><span data-stu-id="409e3-156">0X01 – Synthetic Transaction</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="409e3-157">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="409e3-157">


</div>

<span> </span>

</div>

</div>

</span></span></div>

