---
title: 'Lync Server 2013: modo de exibição de registro'
description: 'Lync Server 2013: modo de exibição de registro.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registration view
ms:assetid: 8a42bc7d-3d4f-43c1-9e15-89b2ee419ade
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688120(v=OCS.15)
ms:contentKeyID: 49733718
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be169cafc324f89cacedda154ca49a8ff1ff39aa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389966"
---
# <a name="registration-view-in-lync-server-2013"></a><span data-ttu-id="097ff-103">Modo de exibição de registro no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="097ff-103">Registration view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="097ff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="097ff-104">

<span> </span></span></span>

<span data-ttu-id="097ff-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="097ff-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="097ff-106">O modo de exibição de registro armazena informações sobre o registro de usuário.</span><span class="sxs-lookup"><span data-stu-id="097ff-106">The Registration view stores information about user registration.</span></span> <span data-ttu-id="097ff-107">Este modo de exibição foi apresentado no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="097ff-107">This view was introduced in Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="097ff-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="097ff-108">Column</span></span></th>
<th><span data-ttu-id="097ff-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="097ff-109">Data Type</span></span></th>
<th><span data-ttu-id="097ff-110">Detalhes</span><span class="sxs-lookup"><span data-stu-id="097ff-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="097ff-111"><strong>Id_da_sessãotime</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-112">datetime</span><span class="sxs-lookup"><span data-stu-id="097ff-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="097ff-113">Tempo de solicitação de sessão.</span><span class="sxs-lookup"><span data-stu-id="097ff-113">Time of session request.</span></span> <span data-ttu-id="097ff-114">Usado em conjunto com o SessionIdSeq para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="097ff-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="097ff-115">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="097ff-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="097ff-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-117">int</span><span class="sxs-lookup"><span data-stu-id="097ff-117">int</span></span></p></td>
<td><p><span data-ttu-id="097ff-118">Número de identificação para identificar a sessão.</span><span class="sxs-lookup"><span data-stu-id="097ff-118">ID number to identify the session.</span></span> <span data-ttu-id="097ff-119">Usado em conjunto com a Identificação_da_sessãotime para identificar exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="097ff-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="097ff-120">Consulte a <a href="lync-server-2013-dialogs-table.md">tabela de diálogos no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="097ff-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="097ff-121"><strong>Registertime</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-121"><strong>RegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-122">datetime</span><span class="sxs-lookup"><span data-stu-id="097ff-122">datetime</span></span></p></td>
<td><p><span data-ttu-id="097ff-123">Hora em que ocorreu o registro.</span><span class="sxs-lookup"><span data-stu-id="097ff-123">Time at which registration occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="097ff-124"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-124"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-125">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="097ff-125">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="097ff-126">URL do usuário que se cadastrou.</span><span class="sxs-lookup"><span data-stu-id="097ff-126">URI of the user who registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="097ff-127"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-127"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="097ff-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="097ff-129">Tipo de URI do usuário que se cadastrou.</span><span class="sxs-lookup"><span data-stu-id="097ff-129">Type of URI of the user who registered.</span></span> <span data-ttu-id="097ff-130">Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="097ff-130">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="097ff-131"><strong>Userlocatário</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-131"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="097ff-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="097ff-133">Locatário do usuário que se cadastrou.</span><span class="sxs-lookup"><span data-stu-id="097ff-133">Tenant of the user who registered.</span></span> <span data-ttu-id="097ff-134">Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="097ff-134">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="097ff-135"><strong>Endpointid</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-135"><strong>EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-136">identificador</span><span class="sxs-lookup"><span data-stu-id="097ff-136">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="097ff-137">Identificador exclusivo do ponto de extremidade do usuário registrado.</span><span class="sxs-lookup"><span data-stu-id="097ff-137">Unique identifier of the endpoint of the user registered with.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="097ff-138"><strong>Ponteiro de fim</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-138"><strong>EndpointEra</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-139">identificador</span><span class="sxs-lookup"><span data-stu-id="097ff-139">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="097ff-140">Identificador exclusivo usado para diferenciar os registros que envolvem o mesmo usuário e o mesmo ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="097ff-140">Unique identifier used to differentiate registrations that involve the same user and the same endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="097ff-141"><strong>DeRegisterType</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-141"><strong>DeRegisterType</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-142">datetime</span><span class="sxs-lookup"><span data-stu-id="097ff-142">datetime</span></span></p></td>
<td><p><span data-ttu-id="097ff-143">Tempo em que o cancelamento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="097ff-143">Time at which deregistration occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="097ff-144"><strong>DeRegisterReason</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-144"><strong>DeRegisterReason</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-145">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="097ff-145">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="097ff-146">Motivo do cancelamento de registro.</span><span class="sxs-lookup"><span data-stu-id="097ff-146">Reason for deregistration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="097ff-147"><strong>ClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-147"><strong>ClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-148">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="097ff-148">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="097ff-149">Versão do cliente usada pelo usuário que se cadastrou.</span><span class="sxs-lookup"><span data-stu-id="097ff-149">Version of client used by the user who registered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="097ff-150"><strong>ClientType</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-150"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-151">int</span><span class="sxs-lookup"><span data-stu-id="097ff-151">int</span></span></p></td>
<td><p><span data-ttu-id="097ff-152">Cliente usado pelo usuário que se cadastrou.</span><span class="sxs-lookup"><span data-stu-id="097ff-152">Client used by the user who registered.</span></span> <span data-ttu-id="097ff-153">Consulte a <a href="lync-server-2013-useragentdef-table.md">tabela UserAgentDef no Lync Server 2013</a> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="097ff-153">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="097ff-154"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-154"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-155">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="097ff-155">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="097ff-156">Categoria do cliente usada pelo usuário que se cadastrou.</span><span class="sxs-lookup"><span data-stu-id="097ff-156">Category of the client used by the user who registered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="097ff-157"><strong>IP</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-157"><strong>IpAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-158">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="097ff-158">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="097ff-159">Endereço IP com o qual o usuário se cadastrou.</span><span class="sxs-lookup"><span data-stu-id="097ff-159">IP Address the user registered with.</span></span> <span data-ttu-id="097ff-160">Pode ser um endereço IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="097ff-160">This may be an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="097ff-161"><strong>Caixa de diálogo</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-161"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-162">VARSTRING (775)</span><span class="sxs-lookup"><span data-stu-id="097ff-162">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="097ff-163">ID da caixa de diálogo SIP.</span><span class="sxs-lookup"><span data-stu-id="097ff-163">SIP dialog ID.</span></span> <span data-ttu-id="097ff-164">O formato do é:</span><span class="sxs-lookup"><span data-stu-id="097ff-164">The format of the is:</span></span></p>
<p><span data-ttu-id="097ff-165">caixa de diálogo; de-marca; até-marca</span><span class="sxs-lookup"><span data-stu-id="097ff-165">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="097ff-166"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-166"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-167">int</span><span class="sxs-lookup"><span data-stu-id="097ff-167">int</span></span></p></td>
<td><p><span data-ttu-id="097ff-168">Código de resposta SIP para o convite da sessão.</span><span class="sxs-lookup"><span data-stu-id="097ff-168">SIP response code to the session invitation.</span></span> <span data-ttu-id="097ff-169">Geralmente, esse campo é preenchido por dados gerados da mensagem de convite inicial na sessão.</span><span class="sxs-lookup"><span data-stu-id="097ff-169">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="097ff-170">Se não houver nenhuma mensagem de convite, o campo será preenchido com a data e a hora da primeira mensagem SIP relevante (até mais, cancelamento, mensagem ou informações).</span><span class="sxs-lookup"><span data-stu-id="097ff-170">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="097ff-171"><strong>Diagnosticid</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-171"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-172">int</span><span class="sxs-lookup"><span data-stu-id="097ff-172">int</span></span></p></td>
<td><p><span data-ttu-id="097ff-173">ID de diagnóstico capturada do cabeçalho SIP.</span><span class="sxs-lookup"><span data-stu-id="097ff-173">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="097ff-174"><strong>Registrador</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-174"><strong>Registrar</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-175">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="097ff-175">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="097ff-176">FQDN do registrador.</span><span class="sxs-lookup"><span data-stu-id="097ff-176">FQDN of the Registrar.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="097ff-177"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-177"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-178">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="097ff-178">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="097ff-179">FQDN do pool que capturou os dados da sessão.</span><span class="sxs-lookup"><span data-stu-id="097ff-179">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="097ff-180"><strong>EdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-180"><strong>EdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-181">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="097ff-181">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="097ff-182">FQDN do servidor de borda usado pelo usuário que se cadastrou.</span><span class="sxs-lookup"><span data-stu-id="097ff-182">FQDN of the Edge Server used by the user who registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="097ff-183"><strong>IsInternal</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-183"><strong>IsInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-184">bit</span><span class="sxs-lookup"><span data-stu-id="097ff-184">bit</span></span></p></td>
<td><p><span data-ttu-id="097ff-185">Indica se o usuário está conectado à rede interna.</span><span class="sxs-lookup"><span data-stu-id="097ff-185">Indicates whether the user logged on from the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="097ff-186"><strong>IsUserServiceAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-186"><strong>IsUserServiceAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-187">bit</span><span class="sxs-lookup"><span data-stu-id="097ff-187">bit</span></span></p></td>
<td><p><span data-ttu-id="097ff-188">Indica se o UserService estava disponível no momento do registro.</span><span class="sxs-lookup"><span data-stu-id="097ff-188">Indicates whether the UserService was available at registration time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="097ff-189"><strong>IsPrimaryRegistrar</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-189"><strong>IsPrimaryRegistrar</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-190">bit</span><span class="sxs-lookup"><span data-stu-id="097ff-190">bit</span></span></p></td>
<td><p><span data-ttu-id="097ff-191">Indica se o registro foi com o registrador principal.</span><span class="sxs-lookup"><span data-stu-id="097ff-191">Indicates whether registration was with the primary Registrar.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="097ff-192"><strong>DeviceMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-192"><strong>DeviceMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-193">bigint</span><span class="sxs-lookup"><span data-stu-id="097ff-193">bigint</span></span></p></td>
<td><p><span data-ttu-id="097ff-194">Endereço MAC do dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="097ff-194">MAC Address of device registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="097ff-195"><strong>DeviceManufacturer</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-195"><strong>DeviceManufacturer</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="097ff-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="097ff-197">Fabricante do dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="097ff-197">Manufacturer of the device registered.</span></span> <span data-ttu-id="097ff-198">Consulte a <a href="lync-server-2013-manufacturers-table.md">tabela fabricantes no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="097ff-198">See the <a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="097ff-199"><strong>DeviceHardwareVersion</strong></span><span class="sxs-lookup"><span data-stu-id="097ff-199"><strong>DeviceHardwareVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="097ff-200">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="097ff-200">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="097ff-201">Versão de hardware do dispositivo registrada.</span><span class="sxs-lookup"><span data-stu-id="097ff-201">Hardware version of the device registered.</span></span> <span data-ttu-id="097ff-202">Consulte a <a href="lync-server-2013-hardwareversions-table.md">tabela HardwareVersions no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="097ff-202">See the <a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="097ff-203">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="097ff-203">


</div>

<span> </span>

</div>

</div>

</span></span></div>

