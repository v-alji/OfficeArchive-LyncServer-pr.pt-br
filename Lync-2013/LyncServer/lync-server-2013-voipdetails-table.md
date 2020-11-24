---
title: 'Lync Server 2013: Tabela VoipDetails'
description: 'Lync Server 2013: VoipDetails Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VoipDetails table
ms:assetid: 74ffbb71-569b-4018-be1f-4db2bbafcf36
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398566(v=OCS.15)
ms:contentKeyID: 48184522
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f23d991c1d577a15717de2572d744e1b65ba6bab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389685"
---
# <a name="voipdetails-table-in-lync-server-2013"></a><span data-ttu-id="48569-103">Tabela VoipDetails no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="48569-103">VoipDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="48569-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="48569-104">

<span> </span></span></span>

<span data-ttu-id="48569-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="48569-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="48569-106">Cada registro representa uma chamada de 1 2 a terceiros na qual pelo menos um usuário é um usuário de VoIP.</span><span class="sxs-lookup"><span data-stu-id="48569-106">Each record represents one two-party call in which at least one user is a VoIP user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48569-107">Coluna</span><span class="sxs-lookup"><span data-stu-id="48569-107">Column</span></span></th>
<th><span data-ttu-id="48569-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="48569-108">Data Type</span></span></th>
<th><span data-ttu-id="48569-109">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="48569-109">Key/Index</span></span></th>
<th><span data-ttu-id="48569-110">Detalhes</span><span class="sxs-lookup"><span data-stu-id="48569-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48569-111"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="48569-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="48569-112">datetime</span><span class="sxs-lookup"><span data-stu-id="48569-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="48569-113">Primária</span><span class="sxs-lookup"><span data-stu-id="48569-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="48569-114">Tempo de solicitação de sessão.</span><span class="sxs-lookup"><span data-stu-id="48569-114">Time of session request.</span></span> <span data-ttu-id="48569-115">Usado em conjunto com o <strong>SessionIdSeq</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="48569-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="48569-116">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="48569-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48569-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="48569-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="48569-118">int</span><span class="sxs-lookup"><span data-stu-id="48569-118">int</span></span></p></td>
<td><p><span data-ttu-id="48569-119">Primária</span><span class="sxs-lookup"><span data-stu-id="48569-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="48569-120">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="48569-120">ID number to identify the session.</span></span> <span data-ttu-id="48569-121">Usado em conjunto com a <strong>identificação_da_sessãotime</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="48569-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="48569-122">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="48569-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48569-123"><strong>FromNumberId</strong></span><span class="sxs-lookup"><span data-stu-id="48569-123"><strong>FromNumberId</strong></span></span></p></td>
<td><p><span data-ttu-id="48569-124">int</span><span class="sxs-lookup"><span data-stu-id="48569-124">int</span></span></p></td>
<td><p><span data-ttu-id="48569-125">Exterior</span><span class="sxs-lookup"><span data-stu-id="48569-125">Foreign</span></span></p></td>
<td><p><span data-ttu-id="48569-126">Identificação de <strong>telefone</strong> do chamador.</span><span class="sxs-lookup"><span data-stu-id="48569-126"><strong>PhoneId</strong> of the caller.</span></span> <span data-ttu-id="48569-127">Consulte a <a href="lync-server-2013-phones-table.md">tabela de telefones no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="48569-127">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="48569-128">Se não for nulo e <strong>FromGatewayId</strong> não for nulo, o chamador será um usuário PSTN.</span><span class="sxs-lookup"><span data-stu-id="48569-128">If not NULL and <strong>FromGatewayId</strong> is not NULL, then the caller was a PSTN user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48569-129"><strong>ConnectedNumberId</strong></span><span class="sxs-lookup"><span data-stu-id="48569-129"><strong>ConnectedNumberId</strong></span></span></p></td>
<td><p><span data-ttu-id="48569-130">int</span><span class="sxs-lookup"><span data-stu-id="48569-130">int</span></span></p></td>
<td><p><span data-ttu-id="48569-131">Exterior</span><span class="sxs-lookup"><span data-stu-id="48569-131">Foreign</span></span></p></td>
<td><p><span data-ttu-id="48569-132"><strong>Número de telefoneid</strong> do receptor da chamada.</span><span class="sxs-lookup"><span data-stu-id="48569-132"><strong>PhoneId</strong> of the call receiver.</span></span> <span data-ttu-id="48569-133">Consulte a <a href="lync-server-2013-phones-table.md">tabela de telefones no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="48569-133">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="48569-134">Se não for nulo e <strong>Togatewayid</strong> não for nulo, o receptor da chamada será um usuário PSTN.</span><span class="sxs-lookup"><span data-stu-id="48569-134">If not NULL and <strong>ToGatewayId</strong> is not NULL, then the call receiver was a PSTN user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48569-135"><strong>FromMediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="48569-135"><strong>FromMediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="48569-136">int</span><span class="sxs-lookup"><span data-stu-id="48569-136">int</span></span></p></td>
<td><p><span data-ttu-id="48569-137">Exterior</span><span class="sxs-lookup"><span data-stu-id="48569-137">Foreign</span></span></p></td>
<td><p><span data-ttu-id="48569-138">O servidor de mediação do qual a chamada está vindo.</span><span class="sxs-lookup"><span data-stu-id="48569-138">The Mediation Server the call is coming from.</span></span> <span data-ttu-id="48569-139">Consulte a <a href="lync-server-2013-mediationservers-table.md">tabela MediationServers no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="48569-139">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48569-140"><strong>ToMediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="48569-140"><strong>ToMediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="48569-141">int</span><span class="sxs-lookup"><span data-stu-id="48569-141">int</span></span></p></td>
<td><p><span data-ttu-id="48569-142">Exterior</span><span class="sxs-lookup"><span data-stu-id="48569-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="48569-143">O servidor de mediação chamado está indo para.</span><span class="sxs-lookup"><span data-stu-id="48569-143">The Mediation Server called is going to.</span></span> <span data-ttu-id="48569-144">Consulte a <a href="lync-server-2013-mediationservers-table.md">tabela MediationServers no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="48569-144">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48569-145"><strong>FromGatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="48569-145"><strong>FromGatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="48569-146">int</span><span class="sxs-lookup"><span data-stu-id="48569-146">int</span></span></p></td>
<td><p><span data-ttu-id="48569-147">Exterior</span><span class="sxs-lookup"><span data-stu-id="48569-147">Foreign</span></span></p></td>
<td><p><span data-ttu-id="48569-148">Gateway do qual a chamada está vindo.</span><span class="sxs-lookup"><span data-stu-id="48569-148">Gateway the call is coming from.</span></span> <span data-ttu-id="48569-149">Consulte a <a href="lync-server-2013-gateways-table.md">tabela gateways no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="48569-149">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48569-150"><strong>Togatewayid</strong></span><span class="sxs-lookup"><span data-stu-id="48569-150"><strong>ToGatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="48569-151">int</span><span class="sxs-lookup"><span data-stu-id="48569-151">int</span></span></p></td>
<td><p><span data-ttu-id="48569-152">Exterior</span><span class="sxs-lookup"><span data-stu-id="48569-152">Foreign</span></span></p></td>
<td><p><span data-ttu-id="48569-153">Gateway em que a chamada vai.</span><span class="sxs-lookup"><span data-stu-id="48569-153">Gateway the call is going to.</span></span> <span data-ttu-id="48569-154">Consulte a <a href="lync-server-2013-gateways-table.md">tabela gateways no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="48569-154">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48569-155"><strong>DisconnectedbyURIId</strong></span><span class="sxs-lookup"><span data-stu-id="48569-155"><strong>DisconnectedbyURIId</strong></span></span></p></td>
<td><p><span data-ttu-id="48569-156">int</span><span class="sxs-lookup"><span data-stu-id="48569-156">int</span></span></p></td>
<td><p><span data-ttu-id="48569-157">Exterior</span><span class="sxs-lookup"><span data-stu-id="48569-157">Foreign</span></span></p></td>
<td><p><span data-ttu-id="48569-158">URI do usuário que desconectou a chamada, se o usuário tiver um URI.</span><span class="sxs-lookup"><span data-stu-id="48569-158">URI of the user who disconnected the call, if the user has a URI.</span></span> <span data-ttu-id="48569-159">Consulte a <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="48569-159">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48569-160"><strong>DisconnectedbyPhoneId</strong></span><span class="sxs-lookup"><span data-stu-id="48569-160"><strong>DisconnectedbyPhoneId</strong></span></span></p></td>
<td><p><span data-ttu-id="48569-161">int</span><span class="sxs-lookup"><span data-stu-id="48569-161">int</span></span></p></td>
<td><p><span data-ttu-id="48569-162">Exterior</span><span class="sxs-lookup"><span data-stu-id="48569-162">Foreign</span></span></p></td>
<td><p><span data-ttu-id="48569-163">ID do telefone que desconectou a chamada foi desconectado de um telefone.</span><span class="sxs-lookup"><span data-stu-id="48569-163">ID of the phone that disconnected the call was disconnected from a phone.</span></span> <span data-ttu-id="48569-164">Consulte a <a href="lync-server-2013-phones-table.md">tabela de telefones no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="48569-164">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="48569-165">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="48569-165">


</div>

<span> </span>

</div>

</div>

</span></span></div>

