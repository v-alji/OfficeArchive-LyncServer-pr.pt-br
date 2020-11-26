---
title: 'Lync Server 2013: Tabela de registro'
description: 'Lync Server 2013: tabela de registro.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registration table
ms:assetid: 05ff9dd3-1aaa-4af0-bd69-8789fb8eaeb3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398114(v=OCS.15)
ms:contentKeyID: 48183298
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 806e1a4e944c9bc04ebdd167c41c80a57fde3f29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436563"
---
# <a name="registration-table-in-lync-server-2013"></a><span data-ttu-id="d64bb-103">Tabela de registro no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d64bb-103">Registration table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d64bb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d64bb-104">

<span> </span></span></span>

<span data-ttu-id="d64bb-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="d64bb-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="d64bb-106">Cada registro representa um evento de registro de usuário.</span><span class="sxs-lookup"><span data-stu-id="d64bb-106">Each record represents one user registration event.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d64bb-107">Coluna</span><span class="sxs-lookup"><span data-stu-id="d64bb-107">Column</span></span></th>
<th><span data-ttu-id="d64bb-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d64bb-108">Data Type</span></span></th>
<th><span data-ttu-id="d64bb-109">Chave/índice</span><span class="sxs-lookup"><span data-stu-id="d64bb-109">Key/Index</span></span></th>
<th><span data-ttu-id="d64bb-110">Detalhes</span><span class="sxs-lookup"><span data-stu-id="d64bb-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d64bb-111"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-112">datetime</span><span class="sxs-lookup"><span data-stu-id="d64bb-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="d64bb-113">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="d64bb-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="d64bb-114">Tempo de solicitação de sessão.</span><span class="sxs-lookup"><span data-stu-id="d64bb-114">Time of session request.</span></span> <span data-ttu-id="d64bb-115">Usado em conjunto com o <strong>SessionIdSeq</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="d64bb-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="d64bb-116">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d64bb-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d64bb-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-118">int</span><span class="sxs-lookup"><span data-stu-id="d64bb-118">int</span></span></p></td>
<td><p><span data-ttu-id="d64bb-119">Primário, estrangeiro</span><span class="sxs-lookup"><span data-stu-id="d64bb-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="d64bb-120">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="d64bb-120">ID number to identify the session.</span></span> <span data-ttu-id="d64bb-121">Usado em conjunto com a <strong>identificação_da_sessãotime</strong> para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="d64bb-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="d64bb-122">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d64bb-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d64bb-123"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-123"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-124">int</span><span class="sxs-lookup"><span data-stu-id="d64bb-124">int</span></span></p></td>
<td><p><span data-ttu-id="d64bb-125">Exterior</span><span class="sxs-lookup"><span data-stu-id="d64bb-125">Foreign</span></span></p></td>
<td><p><span data-ttu-id="d64bb-126">A ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="d64bb-126">The user ID.</span></span> <span data-ttu-id="d64bb-127">Consulte a <a href="lync-server-2013-users-table.md">tabela usuários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d64bb-127">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d64bb-128"><strong>Endpointid</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-128"><strong>EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-129">identificador</span><span class="sxs-lookup"><span data-stu-id="d64bb-129">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d64bb-130">Um GUID para identificar um ponto de extremidade de registro.</span><span class="sxs-lookup"><span data-stu-id="d64bb-130">A GUID to identify a registration endpoint.</span></span> <span data-ttu-id="d64bb-131">Geralmente, o evento Register do mesmo computador do mesmo usuário terá a mesma ID de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="d64bb-131">Usually the register event from the same computer of the same user will have the same endpoint ID.</span></span> <span data-ttu-id="d64bb-132">Máquinas diferentes têm uma ID de ponto de extremidade diferente.</span><span class="sxs-lookup"><span data-stu-id="d64bb-132">Different machines have a different endpoint ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d64bb-133"><strong>Ponteiro de fim</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-133"><strong>EndpointEra</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-134">Identificador</span><span class="sxs-lookup"><span data-stu-id="d64bb-134">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d64bb-135">ID usada para diferenciar os registros que envolvem o mesmo usuário e o mesmo ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="d64bb-135">ID used to differentiate registrations that involve the same user and the same endpoint.</span></span></p>
<p><span data-ttu-id="d64bb-136">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d64bb-136">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d64bb-137"><strong>ClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-137"><strong>ClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-138">int</span><span class="sxs-lookup"><span data-stu-id="d64bb-138">int</span></span></p></td>
<td><p><span data-ttu-id="d64bb-139">Exterior</span><span class="sxs-lookup"><span data-stu-id="d64bb-139">Foreign</span></span></p></td>
<td><p><span data-ttu-id="d64bb-140">Versão cliente do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="d64bb-140">Client version of current user.</span></span> <span data-ttu-id="d64bb-141">Consulte a <a href="lync-server-2013-clientversions-table.md">tabela ClientVersions no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d64bb-141">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d64bb-142"><strong>Registrador de registro</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-142"><strong>RegistrarId</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-143">int</span><span class="sxs-lookup"><span data-stu-id="d64bb-143">int</span></span></p></td>
<td><p><span data-ttu-id="d64bb-144">Exterior</span><span class="sxs-lookup"><span data-stu-id="d64bb-144">Foreign</span></span></p></td>
<td><p><span data-ttu-id="d64bb-145">ID do servidor de registrador usado para registro.</span><span class="sxs-lookup"><span data-stu-id="d64bb-145">ID of the Registrar Server used for registration.</span></span> <span data-ttu-id="d64bb-146">Consulte a <a href="lync-server-2013-servers-table.md">tabela servidores no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d64bb-146">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d64bb-147"><strong>Poolid</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-147"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-148">int</span><span class="sxs-lookup"><span data-stu-id="d64bb-148">int</span></span></p></td>
<td><p><span data-ttu-id="d64bb-149">Exterior</span><span class="sxs-lookup"><span data-stu-id="d64bb-149">Foreign</span></span></p></td>
<td><p><span data-ttu-id="d64bb-150">ID do pool no qual a sessão foi capturada.</span><span class="sxs-lookup"><span data-stu-id="d64bb-150">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="d64bb-151">Consulte a <a href="lync-server-2013-pools-table.md">tabela de grupos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d64bb-151">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d64bb-152"><strong>EdgeServerId</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-152"><strong>EdgeServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-153">int</span><span class="sxs-lookup"><span data-stu-id="d64bb-153">int</span></span></p></td>
<td><p><span data-ttu-id="d64bb-154">Exterior</span><span class="sxs-lookup"><span data-stu-id="d64bb-154">Foreign</span></span></p></td>
<td><p><span data-ttu-id="d64bb-155">Servidor de borda no qual o registro está indo.</span><span class="sxs-lookup"><span data-stu-id="d64bb-155">Edge Server the registration is going through.</span></span> <span data-ttu-id="d64bb-156">Consulte a <a href="lync-server-2013-edgeservers-table.md">tabela EdgeServers no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d64bb-156">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d64bb-157"><strong>IsInternal</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-157"><strong>IsInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-158">Bit</span><span class="sxs-lookup"><span data-stu-id="d64bb-158">Bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d64bb-159">Se o usuário está conectado de Internal ou not.</span><span class="sxs-lookup"><span data-stu-id="d64bb-159">Whether the user is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d64bb-160"><strong>IsUserServiceAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-160"><strong>IsUserServiceAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-161">bit</span><span class="sxs-lookup"><span data-stu-id="d64bb-161">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d64bb-162">Se o UserService está disponível ou não.</span><span class="sxs-lookup"><span data-stu-id="d64bb-162">Whether the UserService is available or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d64bb-163"><strong>IsPrimaryRegistrar</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-163"><strong>IsPrimaryRegistrar</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-164">bit</span><span class="sxs-lookup"><span data-stu-id="d64bb-164">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d64bb-165">Se registrar ao registrador principal ou não.</span><span class="sxs-lookup"><span data-stu-id="d64bb-165">Whether register to the primary Registrar or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d64bb-166"><strong>IsPrimaryRegistrarCentral</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-166"><strong>IsPrimaryRegistrarCentral</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-167">bit</span><span class="sxs-lookup"><span data-stu-id="d64bb-167">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d64bb-168">Indica se o usuário está ou não registrado em um aparelho de ramificação sobreviventes.</span><span class="sxs-lookup"><span data-stu-id="d64bb-168">Indicates whether or not the user is registered with a survivable branch appliance.</span></span></p>
<p><span data-ttu-id="d64bb-169">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d64bb-169">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d64bb-170"><strong>Registertime</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-170"><strong>RegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-171">datetime</span><span class="sxs-lookup"><span data-stu-id="d64bb-171">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d64bb-172">Hora do registro.</span><span class="sxs-lookup"><span data-stu-id="d64bb-172">Registration time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d64bb-173"><strong>Cancelar registro</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-173"><strong>DeRegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-174">datetime</span><span class="sxs-lookup"><span data-stu-id="d64bb-174">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d64bb-175">Tempo de De-Registration.</span><span class="sxs-lookup"><span data-stu-id="d64bb-175">De-Registration time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d64bb-176"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-176"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-177">int</span><span class="sxs-lookup"><span data-stu-id="d64bb-177">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d64bb-178">Código de resposta da solicitação de registro.</span><span class="sxs-lookup"><span data-stu-id="d64bb-178">Response code of the register request.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d64bb-179"><strong>Diagnosticid</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-179"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-180">int</span><span class="sxs-lookup"><span data-stu-id="d64bb-180">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d64bb-181">ID do diagnóstico da solicitação de registro.</span><span class="sxs-lookup"><span data-stu-id="d64bb-181">Diagnostic ID of the register request.</span></span> <span data-ttu-id="d64bb-182">Isso indica que o tipo de informações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="d64bb-182">This indicates that diagnostic information type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d64bb-183"><strong>DeviceId</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-183"><strong>DeviceId</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-184">int</span><span class="sxs-lookup"><span data-stu-id="d64bb-184">int</span></span></p></td>
<td><p><span data-ttu-id="d64bb-185">Exterior</span><span class="sxs-lookup"><span data-stu-id="d64bb-185">Foreign</span></span></p></td>
<td><p><span data-ttu-id="d64bb-186">O dispositivo do qual a solicitação de registro provém.</span><span class="sxs-lookup"><span data-stu-id="d64bb-186">The device that the register request is coming from.</span></span> <span data-ttu-id="d64bb-187">Consulte a <a href="lync-server-2013-devices-table.md">tabela de dispositivos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d64bb-187">See the <a href="lync-server-2013-devices-table.md">Devices table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d64bb-188"><strong>DeRegisterTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-188"><strong>DeRegisterTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-189">tinyint</span><span class="sxs-lookup"><span data-stu-id="d64bb-189">tinyint</span></span></p></td>
<td><p><span data-ttu-id="d64bb-190">Exterior</span><span class="sxs-lookup"><span data-stu-id="d64bb-190">Foreign</span></span></p></td>
<td><p><span data-ttu-id="d64bb-191">O motivo do cancelamento de registro, como ' iniciado pelo usuário ', ' registro expirado ', ' falha do cliente ' e muito mais.</span><span class="sxs-lookup"><span data-stu-id="d64bb-191">The reason of de-register, such as ‘user initiated’, ‘registration expired’, ‘client fail’, and more.</span></span> <span data-ttu-id="d64bb-192">Consulte a <a href="lync-server-2013-deregistertype-table.md">tabela Canregistertype no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d64bb-192">See the <a href="lync-server-2013-deregistertype-table.md">DeRegisterType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d64bb-193"><strong>IPAddress</strong></span><span class="sxs-lookup"><span data-stu-id="d64bb-193"><strong>IPAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="d64bb-194">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d64bb-194">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d64bb-195">Endereço IP do ponto de extremidade ao qual o usuário se cadastrou.</span><span class="sxs-lookup"><span data-stu-id="d64bb-195">IP address of the endpoint the user registered with.</span></span> <span data-ttu-id="d64bb-196">Pode ser um endereço IPv4 ou um endereço IPv6.</span><span class="sxs-lookup"><span data-stu-id="d64bb-196">This can be an IPv4 address or an IPv6 address.</span></span></p>
<p><span data-ttu-id="d64bb-197">Este campo foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d64bb-197">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d64bb-198">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d64bb-198">


</div>

<span> </span>

</div>

</div>

</span></span></div>

