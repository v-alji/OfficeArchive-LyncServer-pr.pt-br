---
title: 'Lync Server 2013: modo de exibição de mídia'
description: 'Lync Server 2013: modo de exibição de mídia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine view
ms:assetid: 132eca13-8913-4218-9eff-4960ced8c3dc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687972(v=OCS.15)
ms:contentKeyID: 49733560
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c61fcc15b46958622e6cddd66427255a6def154
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445943"
---
# <a name="medialine-view-in-lync-server-2013"></a><span data-ttu-id="e10af-103">Modo de exibição de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e10af-103">MediaLine view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e10af-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e10af-104">

<span> </span></span></span>

<span data-ttu-id="e10af-105">_**Tópico da última modificação:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="e10af-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="e10af-106">O modo de exibição de mídia armazena informações sobre cada linha de mídia no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e10af-106">The MediaLine View stores information about each media line in the database.</span></span> <span data-ttu-id="e10af-107">Uma sessão de áudio geralmente contém uma linha de mídia de áudio.</span><span class="sxs-lookup"><span data-stu-id="e10af-107">One audio session typically contains one audio media line.</span></span> <span data-ttu-id="e10af-108">Uma sessão de áudio e vídeo (A/V) geralmente contém uma linha de mídia de áudio e uma linha de mídia de vídeo; no entanto, a sessão pode conter duas linhas de mídia de vídeo se um dispositivo de conferência for usado ou se o modo de exibição de galeria for usado.</span><span class="sxs-lookup"><span data-stu-id="e10af-108">One audio and video (A/V) session typically contains one audio media line and one video media line; however, the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span> <span data-ttu-id="e10af-109">Este modo de exibição foi apresentado no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e10af-109">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e10af-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="e10af-110">Column</span></span></th>
<th><span data-ttu-id="e10af-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e10af-111">Data Type</span></span></th>
<th><span data-ttu-id="e10af-112">os</span><span class="sxs-lookup"><span data-stu-id="e10af-112">details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e10af-113">ConferenceDateTime</span><span class="sxs-lookup"><span data-stu-id="e10af-113">ConferenceDateTime</span></span></p></td>
<td><p><span data-ttu-id="e10af-114">datetime</span><span class="sxs-lookup"><span data-stu-id="e10af-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="e10af-115">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e10af-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-116">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="e10af-116">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="e10af-117">int</span><span class="sxs-lookup"><span data-stu-id="e10af-117">int</span></span></p></td>
<td><p><span data-ttu-id="e10af-118">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e10af-118">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-119">MediaLineLabel</span><span class="sxs-lookup"><span data-stu-id="e10af-119">MediaLineLabel</span></span></p></td>
<td><p><span data-ttu-id="e10af-120">tinyint</span><span class="sxs-lookup"><span data-stu-id="e10af-120">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e10af-121">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e10af-121">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-122">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="e10af-122">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="e10af-123">int</span><span class="sxs-lookup"><span data-stu-id="e10af-123">int</span></span></p></td>
<td><p><span data-ttu-id="e10af-124">Informações sobre o processo de estabelecimento de conectividade interativa (ICE) descrito em sinalizadores de bits para o chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-124">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="e10af-125">Para obter detalhes, consulte a especificação de protocolo de servidor de monitoração de experiência de qualidade.</span><span class="sxs-lookup"><span data-stu-id="e10af-125">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-126">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="e10af-126">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="e10af-127">int</span><span class="sxs-lookup"><span data-stu-id="e10af-127">int</span></span></p></td>
<td><p><span data-ttu-id="e10af-128">Informações sobre o processo de estabelecimento de conectividade interativa (ICE) descrito em sinalizadores de bits para o chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-128">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="e10af-129">Para obter detalhes, consulte a especificação de protocolo de servidor de monitoração de experiência de qualidade.</span><span class="sxs-lookup"><span data-stu-id="e10af-129">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-130">Segurança</span><span class="sxs-lookup"><span data-stu-id="e10af-130">Security</span></span></p></td>
<td><p><span data-ttu-id="e10af-131">tinyint</span><span class="sxs-lookup"><span data-stu-id="e10af-131">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e10af-132">Perfil de segurança em uso.</span><span class="sxs-lookup"><span data-stu-id="e10af-132">Security profile in use.</span></span> <span data-ttu-id="e10af-133">0 é nenhum, 1 é SRTP; 2 é v1.</span><span class="sxs-lookup"><span data-stu-id="e10af-133">0 is NONE, 1 is SRTP, 2 is V1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-134">SMTP</span><span class="sxs-lookup"><span data-stu-id="e10af-134">Transport</span></span></p></td>
<td><p><span data-ttu-id="e10af-135">tinyint</span><span class="sxs-lookup"><span data-stu-id="e10af-135">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e10af-136">Tipo de transporte.</span><span class="sxs-lookup"><span data-stu-id="e10af-136">Transport type.</span></span> <span data-ttu-id="e10af-137">0 é UDP; 1 é TCP.</span><span class="sxs-lookup"><span data-stu-id="e10af-137">0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-138">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="e10af-138">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="e10af-139">var (50)</span><span class="sxs-lookup"><span data-stu-id="e10af-139">var(50)</span></span></p></td>
<td><p><span data-ttu-id="e10af-140">Endereço IP do chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-140">IP address of the caller.</span></span> <span data-ttu-id="e10af-141">Pode ser um endereço IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="e10af-141">This can be either an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-142">CallerPort</span><span class="sxs-lookup"><span data-stu-id="e10af-142">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="e10af-143">int</span><span class="sxs-lookup"><span data-stu-id="e10af-143">int</span></span></p></td>
<td><p><span data-ttu-id="e10af-144">Porta usada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-144">Port used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-145">CallerInside</span><span class="sxs-lookup"><span data-stu-id="e10af-145">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="e10af-146">bit</span><span class="sxs-lookup"><span data-stu-id="e10af-146">bit</span></span></p></td>
<td><p><span data-ttu-id="e10af-147">Indica se o chamador está dentro da rede da organização.</span><span class="sxs-lookup"><span data-stu-id="e10af-147">Indicates whether or not the caller is inside the organization network.</span></span> <span data-ttu-id="e10af-148">1 significa que o chamador está dentro da rede da empresa.</span><span class="sxs-lookup"><span data-stu-id="e10af-148">1 means that the caller is inside the enterprise network.</span></span> <span data-ttu-id="e10af-149">0 significa que o chamador está fora da rede.</span><span class="sxs-lookup"><span data-stu-id="e10af-149">0 means that the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-150">CallerMacAddress</span><span class="sxs-lookup"><span data-stu-id="e10af-150">CallerMacAddress</span></span></p></td>
<td><p><span data-ttu-id="e10af-151">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-151">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-152">Endereço MAC da interface de rede usada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-152">MAC address of network interface used by caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-153">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="e10af-153">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="e10af-154">var (50)</span><span class="sxs-lookup"><span data-stu-id="e10af-154">var(50)</span></span></p></td>
<td><p><span data-ttu-id="e10af-155">Endereço IP do serviço de borda A/V usado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-155">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="e10af-156">Consulte a <a href="lync-server-2013-ipaddress-table.md">tabela IPAddress no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e10af-156">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-157">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="e10af-157">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="e10af-158">int</span><span class="sxs-lookup"><span data-stu-id="e10af-158">int</span></span></p></td>
<td><p><span data-ttu-id="e10af-159">Porta usada no serviço de borda A/V usado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-159">Port used on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-160">CallerReflexiveIPAddr</span><span class="sxs-lookup"><span data-stu-id="e10af-160">CallerReflexiveIPAddr</span></span></p></td>
<td><p><span data-ttu-id="e10af-161">var (50)</span><span class="sxs-lookup"><span data-stu-id="e10af-161">var(50)</span></span></p></td>
<td><p><span data-ttu-id="e10af-162">Endereço IP do chamador reportado pelo serviço de borda A/V.</span><span class="sxs-lookup"><span data-stu-id="e10af-162">Caller’s IP address as reported by the A/V Edge service.</span></span> <span data-ttu-id="e10af-163">Esse endereço pode ser diferente de CallerIPAddr se o cliente estiver localizado atrás de um NAT por exemplo.</span><span class="sxs-lookup"><span data-stu-id="e10af-163">This address may be different that the CallerIPAddr if the client is located behind a NAT for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-164">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="e10af-164">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="e10af-165">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-165">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-166">Nome do dispositivo de captura do chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-166">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-167">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="e10af-167">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="e10af-168">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-168">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-169">Nome do dispositivo de renderização do chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-169">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-170">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="e10af-170">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="e10af-171">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-171">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-172">Nome do driver do dispositivo de captura do chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-172">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-173">CallerRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="e10af-173">CallerRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="e10af-174">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-174">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-175">O nome do driver de dispositivo de renderização do chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-175">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-176">CallerWifiDriverDeviceDesc</span><span class="sxs-lookup"><span data-stu-id="e10af-176">CallerWifiDriverDeviceDesc</span></span></p></td>
<td><p><span data-ttu-id="e10af-177">varchar (256</span><span class="sxs-lookup"><span data-stu-id="e10af-177">varchar(256</span></span></p></td>
<td><p><span data-ttu-id="e10af-178">Descrição do driver WiFi do chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-178">Caller’s Wifi driver description.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-179">CallerWifiDriverVersion</span><span class="sxs-lookup"><span data-stu-id="e10af-179">CallerWifiDriverVersion</span></span></p></td>
<td><p><span data-ttu-id="e10af-180">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-180">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-181">Versão do driver WiFi do chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-181">Caller’s Wifi driver version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-182">CalleeNetworkConnectionDetail</span><span class="sxs-lookup"><span data-stu-id="e10af-182">CalleeNetworkConnectionDetail</span></span></p></td>
<td><p><span data-ttu-id="e10af-183">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-183">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-184">Detalhes da conexão de rede do chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-184">Details of caller’s network connection.</span></span> <span data-ttu-id="e10af-185">Consulte a <a href="lync-server-2013-networkconnectiondetail-table.md">tabela NetworkConnectionDetail no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e10af-185">See the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-186">CallerBssid</span><span class="sxs-lookup"><span data-stu-id="e10af-186">CallerBssid</span></span></p></td>
<td><p><span data-ttu-id="e10af-187">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-187">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-188">Identificador do conjunto de serviços básico usado pela conexão WiFi de chamadores.</span><span class="sxs-lookup"><span data-stu-id="e10af-188">Basic Service Set Identifier used by callers WiFi connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-189">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="e10af-189">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="e10af-190">bit</span><span class="sxs-lookup"><span data-stu-id="e10af-190">bit</span></span></p></td>
<td><p><span data-ttu-id="e10af-191">Indica se o chamador está conectado por meio de uma rede virtual privada.</span><span class="sxs-lookup"><span data-stu-id="e10af-191">Indicates whether the caller connected over a virtual private network.</span></span> <span data-ttu-id="e10af-192">1 é uma rede virtual privada (VPN), 0 não é VPN.</span><span class="sxs-lookup"><span data-stu-id="e10af-192">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-193">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="e10af-193">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="e10af-194">var (50)</span><span class="sxs-lookup"><span data-stu-id="e10af-194">var(50)</span></span></p></td>
<td><p><span data-ttu-id="e10af-195">Endereço IP do chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-195">IP address of the callee.</span></span> <span data-ttu-id="e10af-196">Pode ser um endereço IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="e10af-196">This can be either an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-197">CalleePort</span><span class="sxs-lookup"><span data-stu-id="e10af-197">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="e10af-198">int</span><span class="sxs-lookup"><span data-stu-id="e10af-198">int</span></span></p></td>
<td><p><span data-ttu-id="e10af-199">Porta usada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-199">Port used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-200">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="e10af-200">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="e10af-201">bit</span><span class="sxs-lookup"><span data-stu-id="e10af-201">bit</span></span></p></td>
<td><p><span data-ttu-id="e10af-202">Indica se a chamada está dentro da rede corporativa.</span><span class="sxs-lookup"><span data-stu-id="e10af-202">Indicates whether the callee is inside the enterprise network.</span></span> <span data-ttu-id="e10af-203">1 significa que a chamada está dentro da rede corporativa, 0 significa que o chamador está fora da rede.</span><span class="sxs-lookup"><span data-stu-id="e10af-203">1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-204">CalleeMacAddress</span><span class="sxs-lookup"><span data-stu-id="e10af-204">CalleeMacAddress</span></span></p></td>
<td><p><span data-ttu-id="e10af-205">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-205">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-206">Endereço MAC da interface de rede usada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-206">MAC address of network interface used by callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-207">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="e10af-207">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="e10af-208">var (50)</span><span class="sxs-lookup"><span data-stu-id="e10af-208">var(50)</span></span></p></td>
<td><p><span data-ttu-id="e10af-209">Endereço IP do serviço de borda A/V usado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-209">IP Address of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="e10af-210">Consulte a <a href="lync-server-2013-ipaddress-table.md">tabela IPAddress no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e10af-210">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-211">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="e10af-211">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="e10af-212">int</span><span class="sxs-lookup"><span data-stu-id="e10af-212">int</span></span></p></td>
<td><p><span data-ttu-id="e10af-213">Porta usada no serviço de borda A/V usado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-213">Port used on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-214">CalleeReflexiveIPAddr</span><span class="sxs-lookup"><span data-stu-id="e10af-214">CalleeReflexiveIPAddr</span></span></p></td>
<td><p><span data-ttu-id="e10af-215">var (50)</span><span class="sxs-lookup"><span data-stu-id="e10af-215">var(50)</span></span></p></td>
<td><p><span data-ttu-id="e10af-216">Endereço IP do chamador reportado pelo serviço de borda A/V.</span><span class="sxs-lookup"><span data-stu-id="e10af-216">Callee’s IP address as reported by the A/V Edge service.</span></span> <span data-ttu-id="e10af-217">Esse endereço pode ser diferente de CalleeIPAddr se o cliente estiver localizado atrás de um NAT por exemplo.</span><span class="sxs-lookup"><span data-stu-id="e10af-217">This address may be different that the CalleeIPAddr if the client is located behind a NAT for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-218">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="e10af-218">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="e10af-219">var (50)</span><span class="sxs-lookup"><span data-stu-id="e10af-219">var(50)</span></span></p></td>
<td><p><span data-ttu-id="e10af-220">Nome do dispositivo de captura do chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-220">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-221">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="e10af-221">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="e10af-222">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-222">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-223">Nome do dispositivo de renderização do Calle.</span><span class="sxs-lookup"><span data-stu-id="e10af-223">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-224">CalleeCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="e10af-224">CalleeCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="e10af-225">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-225">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-226">Nome do driver do dispositivo de captura do chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-226">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-227">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="e10af-227">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="e10af-228">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-228">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-229">Chame o nome do driver do dispositivo de processamento do recurso.</span><span class="sxs-lookup"><span data-stu-id="e10af-229">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-230">CalleeWifiDriverDeviceDesc</span><span class="sxs-lookup"><span data-stu-id="e10af-230">CalleeWifiDriverDeviceDesc</span></span></p></td>
<td><p><span data-ttu-id="e10af-231">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-231">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-232">Descrição do driver WiFi do Calle.</span><span class="sxs-lookup"><span data-stu-id="e10af-232">Callee’s Wifi driver description.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-233">CalleeWifiDriverVersion</span><span class="sxs-lookup"><span data-stu-id="e10af-233">CalleeWifiDriverVersion</span></span></p></td>
<td><p><span data-ttu-id="e10af-234">varchar (256</span><span class="sxs-lookup"><span data-stu-id="e10af-234">varchar(256</span></span></p></td>
<td><p><span data-ttu-id="e10af-235">Versão do driver WiFi do Calle.</span><span class="sxs-lookup"><span data-stu-id="e10af-235">Callee’s Wifi driver version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-236">CalleeNetworkConnectionDetail</span><span class="sxs-lookup"><span data-stu-id="e10af-236">CalleeNetworkConnectionDetail</span></span></p></td>
<td><p><span data-ttu-id="e10af-237">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-237">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-238">Detalhes da conexão de rede do Calle.</span><span class="sxs-lookup"><span data-stu-id="e10af-238">Details of callee’s network connection.</span></span> <span data-ttu-id="e10af-239">Consulte a <a href="lync-server-2013-networkconnectiondetail-table.md">tabela NetworkConnectionDetail no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e10af-239">See the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-240">CalleeBssid</span><span class="sxs-lookup"><span data-stu-id="e10af-240">CalleeBssid</span></span></p></td>
<td><p><span data-ttu-id="e10af-241">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-241">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-242">Identificador do conjunto de serviços básico usado pela conexão WiFi do chamador.</span><span class="sxs-lookup"><span data-stu-id="e10af-242">Basic Service Set Identifier used by callee’s WiFi connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-243">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="e10af-243">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="e10af-244">bit</span><span class="sxs-lookup"><span data-stu-id="e10af-244">bit</span></span></p></td>
<td><p><span data-ttu-id="e10af-245">Indica se o chamador está conectado por meio de uma rede virtual privada.</span><span class="sxs-lookup"><span data-stu-id="e10af-245">Indicates whether the callee connected over a virtual private network.</span></span> <span data-ttu-id="e10af-246">1 é uma rede virtual privada (VPN), 0 não é VPN.</span><span class="sxs-lookup"><span data-stu-id="e10af-246">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-247">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="e10af-247">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="e10af-248">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="e10af-248">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="e10af-249">O MOS de conversa de banda estreita das sessões de áudio (com base nos dois fluxos de áudio).</span><span class="sxs-lookup"><span data-stu-id="e10af-249">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-250">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="e10af-250">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="e10af-251">int</span><span class="sxs-lookup"><span data-stu-id="e10af-251">int</span></span></p></td>
<td><p><span data-ttu-id="e10af-252">Esta é a largura de banda real aplicada ao fluxo de envios do lado fornecido com várias configurações de política (ativar, API, SDP, servidor de política etc.).</span><span class="sxs-lookup"><span data-stu-id="e10af-252">This is the actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, etc.).</span></span> <span data-ttu-id="e10af-253">Isso não deve ser confundido com a largura de banda efetiva porque pode haver uma largura de banda mais econômica com base na estimativa de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="e10af-253">This should not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="e10af-254">Isso é basicamente a largura de banda máxima que o fluxo de envio pode ter limites de bloqueio impostos pela estimativa da largura de banda.</span><span class="sxs-lookup"><span data-stu-id="e10af-254">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-255">AppliedBandwidthSource</span><span class="sxs-lookup"><span data-stu-id="e10af-255">AppliedBandwidthSource</span></span></p></td>
<td><p><span data-ttu-id="e10af-256">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e10af-256">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e10af-257">Fonte do limite de largura de banda imposto.</span><span class="sxs-lookup"><span data-stu-id="e10af-257">Source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="e10af-258">Ele descreve para onde o limite de largura de banda é proveniente (por exemplo, "servidor de políticas", "Ativar servidor" ou "modalidade").</span><span class="sxs-lookup"><span data-stu-id="e10af-258">It describes where the bandwidth limit is coming from (for example, “Policy Server”, “TURN Server”, or “Modality”).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-259">Chamador</span><span class="sxs-lookup"><span data-stu-id="e10af-259">Caller</span></span></p></td>
<td><p><span data-ttu-id="e10af-260">bit</span><span class="sxs-lookup"><span data-stu-id="e10af-260">bit</span></span></p></td>
<td><p><span data-ttu-id="e10af-261">Indica se as métricas do autor foram recebidas; 1 é sim, 0 é não.</span><span class="sxs-lookup"><span data-stu-id="e10af-261">Indicates whether metrics from the caller were received; 1 is yes, 0 is no.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-262">Receptor</span><span class="sxs-lookup"><span data-stu-id="e10af-262">Callee</span></span></p></td>
<td><p><span data-ttu-id="e10af-263">bit</span><span class="sxs-lookup"><span data-stu-id="e10af-263">bit</span></span></p></td>
<td><p><span data-ttu-id="e10af-264">Indica se as métricas do receptor da chamada foram recebidas; 1 é sim, 0 é não.</span><span class="sxs-lookup"><span data-stu-id="e10af-264">Indicates whether metrics from the call receiver were received; 1 is yes, 0 is no.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-265">MidCallReport</span><span class="sxs-lookup"><span data-stu-id="e10af-265">MidCallReport</span></span></p></td>
<td><p><span data-ttu-id="e10af-266">bit</span><span class="sxs-lookup"><span data-stu-id="e10af-266">bit</span></span></p></td>
<td><p><span data-ttu-id="e10af-267">Indica se o relatório é para uma parte da chamada ou para a chamada completa.</span><span class="sxs-lookup"><span data-stu-id="e10af-267">Indicates whether the report is for a portion of the call or for the complete call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-268">ClassifiedPoorCall</span><span class="sxs-lookup"><span data-stu-id="e10af-268">ClassifiedPoorCall</span></span></p></td>
<td><p><span data-ttu-id="e10af-269">bit</span><span class="sxs-lookup"><span data-stu-id="e10af-269">bit</span></span></p></td>
<td><p><span data-ttu-id="e10af-270">Indica se uma chamada foi classificada como uma chamada deficiente (1) ou uma boa chamada (0).</span><span class="sxs-lookup"><span data-stu-id="e10af-270">Indicates whether a call was classified as a poor call (1) or as a good call (0).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e10af-271">CallerConnectivityICE</span><span class="sxs-lookup"><span data-stu-id="e10af-271">CallerConnectivityICE</span></span></p></td>
<td><p><span data-ttu-id="e10af-272">tinyint</span><span class="sxs-lookup"><span data-stu-id="e10af-272">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e10af-273">Indica se o chamador está conectado à rede usando o protocolo ICE (estabelecimento de conectividade com a Internet).</span><span class="sxs-lookup"><span data-stu-id="e10af-273">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e10af-274">CalleeConnectivityICE</span><span class="sxs-lookup"><span data-stu-id="e10af-274">CalleeConnectivityICE</span></span></p></td>
<td><p><span data-ttu-id="e10af-275">tinyint</span><span class="sxs-lookup"><span data-stu-id="e10af-275">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e10af-276">Indica se o usuário chamou conexão à rede usando o protocolo ICE (estabelecimento de conectividade com a Internet).</span><span class="sxs-lookup"><span data-stu-id="e10af-276">Indicates whether the user called connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e10af-277">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e10af-277">


</div>

<span> </span>

</div>

</div>

</span></span></div>

