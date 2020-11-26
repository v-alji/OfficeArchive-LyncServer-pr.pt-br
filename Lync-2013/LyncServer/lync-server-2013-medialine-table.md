---
title: 'Lync Server 2013: Tabela MediaLine'
description: 'Lync Server 2013: tabela de mídia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine table
ms:assetid: 414b1d63-ae97-4c27-bac0-c9ad0f808ff0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425920(v=OCS.15)
ms:contentKeyID: 48183956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2acea8e14ba0608d9ebf72a48f888bfc4501fae3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425616"
---
# <a name="medialine-table-in-lync-server-2013"></a><span data-ttu-id="e774d-103">Tabela MediaLine no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e774d-103">MediaLine table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e774d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e774d-104">

<span> </span></span></span>

<span data-ttu-id="e774d-105">_**Tópico da última modificação:** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="e774d-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="e774d-106">Cada registro representa uma linha de mídia.</span><span class="sxs-lookup"><span data-stu-id="e774d-106">Each record represents one media line.</span></span> <span data-ttu-id="e774d-107">(Uma sessão de áudio geralmente contém uma linha de mídia de áudio.</span><span class="sxs-lookup"><span data-stu-id="e774d-107">(One audio session usually contains one audio media line.</span></span> <span data-ttu-id="e774d-108">Uma sessão de áudio e vídeo (A/V) geralmente contém uma linha de mídia de áudio e uma linha de mídia de vídeo, embora a sessão possa conter duas linhas de mídia de vídeo se um dispositivo de conferência for usado ou se o modo de exibição de galeria for usado.</span><span class="sxs-lookup"><span data-stu-id="e774d-108">One audio and video (A/V) session usually contains one audio media line and one video media line, although the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e774d-109"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="e774d-110"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="e774d-111"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="e774d-112"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e774d-113"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-113"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-114">datetime</span><span class="sxs-lookup"><span data-stu-id="e774d-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="e774d-115">Primária</span><span class="sxs-lookup"><span data-stu-id="e774d-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="e774d-116">Referenciado da <a href="lync-server-2013-session-table.md">tabela de sessão no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-116">Referenced from the <a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-117"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-117"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-118">int</span><span class="sxs-lookup"><span data-stu-id="e774d-118">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-119">Primária</span><span class="sxs-lookup"><span data-stu-id="e774d-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="e774d-120">Referenciado da <a href="lync-server-2013-session-table.md">tabela de sessão no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-120">Referenced from the <a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-121"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-121"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-122">tinyint</span><span class="sxs-lookup"><span data-stu-id="e774d-122">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e774d-123">Primária</span><span class="sxs-lookup"><span data-stu-id="e774d-123">Primary</span></span></p></td>
<td><p><span data-ttu-id="e774d-124">0 é o áudio principal, 1 é o vídeo principal e 2 é o vídeo panorâmico, 3 é o compartilhamento de aplicativos/desktop.</span><span class="sxs-lookup"><span data-stu-id="e774d-124">0 is main audio, 1 is main video, and 2 is panoramic video, 3 is Application/Desktop Sharing.</span></span> <span data-ttu-id="e774d-125">Esse rótulo deve ser exclusivo em uma única sessão.</span><span class="sxs-lookup"><span data-stu-id="e774d-125">This label must be unique within a single session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-126"><strong>ConnectivityIce</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-126"><strong>ConnectivityIce</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-127">tinyint</span><span class="sxs-lookup"><span data-stu-id="e774d-127">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e774d-128">Esta coluna está presente, mas não é usada no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e774d-128">This column is present but not used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="e774d-129">Informações sobre a conectividade usada para uma linha de mídia são capturadas nas colunas CallerConnectivityICE e CalleeConnectivityICE.</span><span class="sxs-lookup"><span data-stu-id="e774d-129">Information about the connectivity used for a media line is captured in the CallerConnectivityICE and CalleeConnectivityICE columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-130"><strong>CallerIceWarningFlags</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-130"><strong>CallerIceWarningFlags</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-131">int</span><span class="sxs-lookup"><span data-stu-id="e774d-131">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e774d-132">Informações sobre o processo de estabelecimento de conectividade interativa (ICE) descrito em sinalizadores de bits.</span><span class="sxs-lookup"><span data-stu-id="e774d-132">Information about Interactive Connectivity Establishment (ICE) process described in bits flags.</span></span> <span data-ttu-id="e774d-133">Para obter detalhes, consulte a <em>especificação de protocolo de servidor do monitoramento de qualidade de experiência</em>, disponível para download.</span><span class="sxs-lookup"><span data-stu-id="e774d-133">For details, refer to the <em>Quality of Experience Monitoring Server Protocol Specification</em>, available for download.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-134"><strong>CalleeIceWarningFlags</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-134"><strong>CalleeIceWarningFlags</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-135">int</span><span class="sxs-lookup"><span data-stu-id="e774d-135">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e774d-136">Mesmo que CallerIceWarningFlags, mas no lado do chamador.</span><span class="sxs-lookup"><span data-stu-id="e774d-136">Same as CallerIceWarningFlags, but on the callee side.</span></span> <span data-ttu-id="e774d-137">Para obter detalhes, consulte a <em>especificação de protocolo de servidor do monitoramento de qualidade de experiência</em>, disponível para download.</span><span class="sxs-lookup"><span data-stu-id="e774d-137">For details, refer to the <em>Quality of Experience Monitoring Server Protocol Specification</em>, available for download.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-138"><strong>Segurança</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-138"><strong>Security</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-139">tinyint</span><span class="sxs-lookup"><span data-stu-id="e774d-139">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e774d-140">O perfil de segurança em uso.</span><span class="sxs-lookup"><span data-stu-id="e774d-140">The security profile in use.</span></span> <span data-ttu-id="e774d-141">0 é nenhum, 1 é SRTP; 2 é v1.</span><span class="sxs-lookup"><span data-stu-id="e774d-141">0 is NONE, 1 is SRTP, 2 is V1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-142"><strong>SMTP</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-142"><strong>Transport</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-143">tinyint</span><span class="sxs-lookup"><span data-stu-id="e774d-143">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e774d-144">0 é UDP; 1 é TCP.</span><span class="sxs-lookup"><span data-stu-id="e774d-144">0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-145"><strong>CallerIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-145"><strong>CallerIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-146">int</span><span class="sxs-lookup"><span data-stu-id="e774d-146">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-147">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-147">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-148">Endereço IP do chamador.</span><span class="sxs-lookup"><span data-stu-id="e774d-148">IP Address of the caller.</span></span> <span data-ttu-id="e774d-149">Consulte a <a href="lync-server-2013-ipaddress-table.md">tabela IPAddress no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e774d-149">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-150"><strong>CallerPort</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-150"><strong>CallerPort</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-151">int</span><span class="sxs-lookup"><span data-stu-id="e774d-151">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e774d-152">Porta usada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e774d-152">Port used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-153"><strong>CallerSubnet</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-153"><strong>CallerSubnet</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-154">int</span><span class="sxs-lookup"><span data-stu-id="e774d-154">int</span></span></p></td>
<td><p> <span data-ttu-id="e774d-155">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-155">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-156">A sub-rede do chamador.</span><span class="sxs-lookup"><span data-stu-id="e774d-156">The subnet of the caller.</span></span> <span data-ttu-id="e774d-157">Consulte a <a href="lync-server-2013-ipaddress-table.md">tabela IPAddress no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e774d-157">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-158"><strong>CallerInside</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-158"><strong>CallerInside</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-159">bit</span><span class="sxs-lookup"><span data-stu-id="e774d-159">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e774d-160">1 significa que a chamada está dentro da rede corporativa, 0 significa que o chamador está fora da rede.</span><span class="sxs-lookup"><span data-stu-id="e774d-160">1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-161"><strong>CallerMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-161"><strong>CallerMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-162">int</span><span class="sxs-lookup"><span data-stu-id="e774d-162">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-163">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-163">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-164">Endereço MAC do chamador, referenciado na <a href="lync-server-2013-macaddress-table.md">tabela MACAddress no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-164">Caller’s mac address, referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-165"><strong>CallerRelayIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-165"><strong>CallerRelayIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-166">int</span><span class="sxs-lookup"><span data-stu-id="e774d-166">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-167">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-167">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-168">Endereço IP do serviço de borda a/V do Lync Server usado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e774d-168">IP Address of the Lync Server A/V Edge service used by the caller.</span></span> <span data-ttu-id="e774d-169">Consulte a <a href="lync-server-2013-ipaddress-table.md">tabela IPAddress no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e774d-169">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-170"><strong>CallerRelayPort</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-170"><strong>CallerRelayPort</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-171">int</span><span class="sxs-lookup"><span data-stu-id="e774d-171">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e774d-172">Porta usada no serviço de borda A/V pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e774d-172">Port used on the A/V Edge service by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-173"><strong>CallerCaptureDev</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-173"><strong>CallerCaptureDev</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-174">int</span><span class="sxs-lookup"><span data-stu-id="e774d-174">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-175">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-176">Dispositivo de captura usado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e774d-176">Capture device used by the caller.</span></span> <span data-ttu-id="e774d-177">Referenciado da <a href="lync-server-2013-device-table.md">tabela de dispositivos no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-177">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-178"><strong>CallerRenderDev</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-178"><strong>CallerRenderDev</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-179">int</span><span class="sxs-lookup"><span data-stu-id="e774d-179">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-180">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-180">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-181">Processar o dispositivo usado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e774d-181">Render device used by caller.</span></span> <span data-ttu-id="e774d-182">Referenciado da <a href="lync-server-2013-device-table.md">tabela de dispositivos no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-182">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-183"><strong>CallerCaptureDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-183"><strong>CallerCaptureDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-184">int</span><span class="sxs-lookup"><span data-stu-id="e774d-184">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-185">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-185">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-186">Driver para o dispositivo de captura do chamador, referenciado na <a href="lync-server-2013-devicedriver-table.md">tabela DeviceDriver no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-186">Driver for the caller’s capture device, referenced from the <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-187"><strong>CallerRenderDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-187"><strong>CallerRenderDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-188">int</span><span class="sxs-lookup"><span data-stu-id="e774d-188">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-189">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-189">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-190">Driver para o dispositivo de renderização do chamador, referenciado na <a href="lync-server-2013-devicedriver-table.md">tabela DeviceDriver no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-190">Driver for the caller’s render device, referenced from the <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-191"><strong>CallerNetworkConnectionType</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-191"><strong>CallerNetworkConnectionType</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-192">tinyint</span><span class="sxs-lookup"><span data-stu-id="e774d-192">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e774d-193">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-194">Indica como o chamador está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="e774d-194">Indicates how the caller connected to the network.</span></span> <span data-ttu-id="e774d-195">Os valores são obtidos na <a href="lync-server-2013-networkconnectiondetail-table.md">tabela NetworkConnectionDetail no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-195">Values are obtained from the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a>.</span></span> <span data-ttu-id="e774d-196">Os valores típicos são 0 para uma conexão com fio ' 1 para conexão WiFi; e 3 para uma conexão Ethernet.</span><span class="sxs-lookup"><span data-stu-id="e774d-196">Typical values are 0 for a wired connection’ 1 for a WiFi connection; and 3 for an Ethernet connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-197"><strong>CallerBssid</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-197"><strong>CallerBssid</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-198">int</span><span class="sxs-lookup"><span data-stu-id="e774d-198">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-199">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-199">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-200">BSSID do chamador se for usada uma conexão sem fio.</span><span class="sxs-lookup"><span data-stu-id="e774d-200">Caller’s BSSID if wireless is used.</span></span> <span data-ttu-id="e774d-201">Referenciado da <a href="lync-server-2013-macaddress-table.md">tabela MACAddress no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-201">Referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-202"><strong>CallerVPN</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-202"><strong>CallerVPN</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-203">bit</span><span class="sxs-lookup"><span data-stu-id="e774d-203">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e774d-204">O link do chamador.</span><span class="sxs-lookup"><span data-stu-id="e774d-204">The caller's link.</span></span> <span data-ttu-id="e774d-205">1 é uma rede virtual privada (VPN), 0 não é VPN.</span><span class="sxs-lookup"><span data-stu-id="e774d-205">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-206"><strong>CallerLinkSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-206"><strong>CallerLinkSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-207">decimal (18, 0)</span><span class="sxs-lookup"><span data-stu-id="e774d-207">decimal(18,0)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e774d-208">A velocidade do link de rede, em bps, para o ponto de extremidade do chamador.</span><span class="sxs-lookup"><span data-stu-id="e774d-208">The network link speed, in bps, for the caller's endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-209"><strong>CalleeIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-209"><strong>CalleeIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-210">int</span><span class="sxs-lookup"><span data-stu-id="e774d-210">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-211">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-211">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-212">Endereço IP do receptor da chamada.</span><span class="sxs-lookup"><span data-stu-id="e774d-212">IP Address of the call receiver.</span></span> <span data-ttu-id="e774d-213">Consulte a <a href="lync-server-2013-ipaddress-table.md">tabela IPAddress no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e774d-213">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-214"><strong>CalleePort</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-214"><strong>CalleePort</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-215">bit</span><span class="sxs-lookup"><span data-stu-id="e774d-215">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e774d-216">Porta usada pelo receptor da chamada.</span><span class="sxs-lookup"><span data-stu-id="e774d-216">Port used by the call receiver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-217"><strong>CalleeSubnet</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-217"><strong>CalleeSubnet</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-218">int</span><span class="sxs-lookup"><span data-stu-id="e774d-218">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-219">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-219">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-220">Sub-rede do chamado.</span><span class="sxs-lookup"><span data-stu-id="e774d-220">Subnet of callee.</span></span> <span data-ttu-id="e774d-221">Consulte a <a href="lync-server-2013-ipaddress-table.md">tabela IPAddress no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e774d-221">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-222"><strong>CalleeInside</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-222"><strong>CalleeInside</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-223">bit</span><span class="sxs-lookup"><span data-stu-id="e774d-223">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e774d-224">1 significa que o receptor da chamada está dentro da rede corporativa, 0 significa que o receptor da chamada está fora da rede.</span><span class="sxs-lookup"><span data-stu-id="e774d-224">1 means call receiver is inside the enterprise network, 0 means the call receiver is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-225"><strong>CalleeMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-225"><strong>CalleeMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-226">int</span><span class="sxs-lookup"><span data-stu-id="e774d-226">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-227">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-227">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-228">Endereço MAC do chamador.</span><span class="sxs-lookup"><span data-stu-id="e774d-228">Callee Mac address.</span></span> <span data-ttu-id="e774d-229">Referenciada na <a href="lync-server-2013-macaddress-table.md">tabela MACAddress no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-229">Referenced from the <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-230"><strong>CalleeRelayIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-230"><strong>CalleeRelayIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-231">int</span><span class="sxs-lookup"><span data-stu-id="e774d-231">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-232">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-232">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-233">Endereço IP do serviço de borda A/V usado pelo receptor de chamadas.</span><span class="sxs-lookup"><span data-stu-id="e774d-233">IP Address of the A/V Edge service used by the call receiver.</span></span> <span data-ttu-id="e774d-234">Consulte a <a href="lync-server-2013-ipaddress-table.md">tabela IPAddress no Lync Server 2013</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e774d-234">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-235"><strong>CalleeRelayPort</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-235"><strong>CalleeRelayPort</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-236">int</span><span class="sxs-lookup"><span data-stu-id="e774d-236">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e774d-237">Porta usada no serviço de borda a/V pelo receptor da chamada.</span><span class="sxs-lookup"><span data-stu-id="e774d-237">Port used on the A/V Edge Service by the call receiver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-238"><strong>CalleeCaptureDev</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-238"><strong>CalleeCaptureDev</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-239">int</span><span class="sxs-lookup"><span data-stu-id="e774d-239">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-240">exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-240">foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-241">Dispositivo de captura usado pelo receptor de chamadas.</span><span class="sxs-lookup"><span data-stu-id="e774d-241">Capture device used by the call receiver.</span></span> <span data-ttu-id="e774d-242">Referenciado da <a href="lync-server-2013-device-table.md">tabela de dispositivos no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-242">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-243"><strong>CalleeRenderDev</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-243"><strong>CalleeRenderDev</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-244">int</span><span class="sxs-lookup"><span data-stu-id="e774d-244">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-245">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-245">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-246">Processar o dispositivo usado pelo receptor da chamada.</span><span class="sxs-lookup"><span data-stu-id="e774d-246">Render device used by the call receiver.</span></span> <span data-ttu-id="e774d-247">Referenciado da <a href="lync-server-2013-device-table.md">tabela de dispositivos no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-247">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-248"><strong>CalleeCaptureDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-248"><strong>CalleeCaptureDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-249">int</span><span class="sxs-lookup"><span data-stu-id="e774d-249">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-250">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-250">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-251">Driver para o dispositivo de captura do receptor da chamada.</span><span class="sxs-lookup"><span data-stu-id="e774d-251">Driver for the call receiver’s capture device.</span></span> <span data-ttu-id="e774d-252">Referenciado pela <a href="lync-server-2013-devicedriver-table.md">tabela DeviceDriver no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-252">Referenced from <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-253"><strong>CalleeRenderDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-253"><strong>CalleeRenderDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-254">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e774d-254">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e774d-255">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-255">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-256">Driver para o dispositivo de renderização do receptor da chamada.</span><span class="sxs-lookup"><span data-stu-id="e774d-256">Driver for the call receiver’s render device.</span></span> <span data-ttu-id="e774d-257">Referenciado pela <a href="lync-server-2013-devicedriver-table.md">tabela DeviceDriver no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-257">Referenced from <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-258"><strong>CalleeNetworkConnectionType</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-258"><strong>CalleeNetworkConnectionType</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-259">tinyint</span><span class="sxs-lookup"><span data-stu-id="e774d-259">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e774d-260">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-260">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-261">Indica como o chamador está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="e774d-261">Indicates how the callee connected to the network.</span></span> <span data-ttu-id="e774d-262">Os valores são obtidos na <a href="lync-server-2013-networkconnectiondetail-table.md">tabela NetworkConnectionDetail no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-262">Values are obtained from the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a>.</span></span> <span data-ttu-id="e774d-263">Os valores típicos são 0 para uma conexão com fio ' 1 para conexão WiFi; e 3 para uma conexão Ethernet.</span><span class="sxs-lookup"><span data-stu-id="e774d-263">Typical values are 0 for a wired connection’ 1 for a WiFi connection; and 3 for an Ethernet connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-264"><strong>CalleeBssid</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-264"><strong>CalleeBssid</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-265">int</span><span class="sxs-lookup"><span data-stu-id="e774d-265">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-266">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-266">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-267">BSSID do chamador se for usada uma conexão sem fio.</span><span class="sxs-lookup"><span data-stu-id="e774d-267">Callee’s BSSID if wireless is used.</span></span> <span data-ttu-id="e774d-268">Referenciado da <a href="lync-server-2013-macaddress-table.md">tabela MACAddress no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-268">Referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-269"><strong>CalleeVPN</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-269"><strong>CalleeVPN</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-270">bit</span><span class="sxs-lookup"><span data-stu-id="e774d-270">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e774d-271">O link do receptor da chamada; 1 é uma rede virtual privada (VPN), 0 não é VPN.</span><span class="sxs-lookup"><span data-stu-id="e774d-271">The call receiver’s link; 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-272"><strong>CalleeLinkSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-272"><strong>CalleeLinkSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-273">decimal (18, 0)</span><span class="sxs-lookup"><span data-stu-id="e774d-273">decimal(18,0)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e774d-274">A velocidade do link de rede, em bps, para o ponto de extremidade do receptor da chamada.</span><span class="sxs-lookup"><span data-stu-id="e774d-274">The network link speed, in bps, for the call receiver’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-275"><strong>ConversationalMOS</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-275"><strong>ConversationalMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-276">decimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="e774d-276">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e774d-277">O MOS de conversa de banda estreita das sessões de áudio (com base nos dois fluxos de áudio).</span><span class="sxs-lookup"><span data-stu-id="e774d-277">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-278"><strong>AppliedBandwidthLimit</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-278"><strong>AppliedBandwidthLimit</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-279">int</span><span class="sxs-lookup"><span data-stu-id="e774d-279">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e774d-280">Esta é a largura de banda real aplicada ao fluxo de envios do lado fornecido com várias configurações de política (ativar, API, SDP, servidor de política e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="e774d-280">This is the actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="e774d-281">Isso não deve ser confundido com a largura de banda efetiva porque pode haver uma largura de banda mais econômica com base na estimativa de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="e774d-281">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="e774d-282">Isso é basicamente a largura de banda máxima que o fluxo de envio pode ter limites de bloqueio impostos pela estimativa da largura de banda.</span><span class="sxs-lookup"><span data-stu-id="e774d-282">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-283"><strong>AppliedBandwidthSourceKey</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-283"><strong>AppliedBandwidthSourceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-284">smallint</span><span class="sxs-lookup"><span data-stu-id="e774d-284">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e774d-285">Essa é a origem do limite de largura de banda que está sendo imposto.</span><span class="sxs-lookup"><span data-stu-id="e774d-285">This is the source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="e774d-286">Ele descreve onde o limite de largura de banda é proveniente de ("servidor de políticas", "Ativar servidor", "Janelarestritaidade" e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="e774d-286">It describes where the bandwidth limit is coming from (“Policy Server”, “TURN Server”, “Modality”, and so on).</span></span> <span data-ttu-id="e774d-287">Referenciado pela <a href="lync-server-2013-appliedbandwidthsource-table.md">tabela AppliedBandwidthSource no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e774d-287">Referenced from the <a href="lync-server-2013-appliedbandwidthsource-table.md">AppliedBandwidthSource table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-288"><strong>Chamador</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-288"><strong>Caller</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-289">bit</span><span class="sxs-lookup"><span data-stu-id="e774d-289">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e774d-290">Indica se as métricas do autor foram recebidas; 1 é sim, um valor nulo é não.</span><span class="sxs-lookup"><span data-stu-id="e774d-290">Indicates whether metrics from the caller were received; 1 is yes, a null value is no.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-291"><strong>Receptor</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-291"><strong>Callee</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-292">bit</span><span class="sxs-lookup"><span data-stu-id="e774d-292">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e774d-293">Indica se as métricas do receptor da chamada foram recebidas; 1 é sim, um valor nulo é não.</span><span class="sxs-lookup"><span data-stu-id="e774d-293">Indicates whether metrics from the call receiver were received; 1 is yes, a null value is no.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-294"><strong>MidCallReport</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-294"><strong>MidCallReport</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-295">bit</span><span class="sxs-lookup"><span data-stu-id="e774d-295">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e774d-296">Indica se o relatório é para uma parte da sessão ou para a sessão completa.</span><span class="sxs-lookup"><span data-stu-id="e774d-296">Indicates whether the report is for a portion of the session or for the complete session.</span></span></p>
<p><span data-ttu-id="e774d-297">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e774d-297">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-298"><strong>ClassifiedPoorCall</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-298"><strong>ClassifiedPoorCall</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-299">bit</span><span class="sxs-lookup"><span data-stu-id="e774d-299">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e774d-300">Indica se uma chamada foi classificada como uma chamada ruim (valor 1) ou uma boa chamada (0).</span><span class="sxs-lookup"><span data-stu-id="e774d-300">Indicates whether a call was classified as a poor call (value of 1) or as a good call (0).</span></span></p>
<p><span data-ttu-id="e774d-301">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e774d-301">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-302"><strong>CallerConnectivityICE</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-302"><strong>CallerConnectivityICE</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-303">tinyInt</span><span class="sxs-lookup"><span data-stu-id="e774d-303">tinyInt</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e774d-304">Indica se o chamador está conectado à rede usando o protocolo ICE (estabelecimento de conectividade com a Internet).</span><span class="sxs-lookup"><span data-stu-id="e774d-304">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p>
<p><span data-ttu-id="e774d-305">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e774d-305">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-306"><strong>CalleeConnectivityICE</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-306"><strong>CalleeConnectivityICE</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-307">tinyint</span><span class="sxs-lookup"><span data-stu-id="e774d-307">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e774d-308">Indica se o chamador está conectado à rede usando o protocolo ICE (estabelecimento de conectividade com a Internet).</span><span class="sxs-lookup"><span data-stu-id="e774d-308">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p>
<p><span data-ttu-id="e774d-309">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e774d-309">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-310"><strong>CallerReflexiveLocalIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-310"><strong>CallerReflexiveLocalIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-311">int</span><span class="sxs-lookup"><span data-stu-id="e774d-311">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-312">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-312">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-313">Endereço IP reflexivo do usuário que fez a chamada.</span><span class="sxs-lookup"><span data-stu-id="e774d-313">Reflexive IP address of the user who placed the call.</span></span> <span data-ttu-id="e774d-314">Em organizações que usam NAT (Network Address Translation), o endereço IP reflexivo é o endereço IP do servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="e774d-314">In organizations that use NAT (network address translation), the reflexive IP address is the IP address of the proxy server.</span></span></p>
<p><span data-ttu-id="e774d-315">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e774d-315">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-316"><strong>CallerWiFiDriverDevicesDesc</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-316"><strong>CallerWiFiDriverDevicesDesc</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-317">int</span><span class="sxs-lookup"><span data-stu-id="e774d-317">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-318">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-318">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-319">Descrição do dispositivo para o driver WiFi empregado pelo usuário que fez a chamada.</span><span class="sxs-lookup"><span data-stu-id="e774d-319">Device description for the WiFi driver employed by the user who placed the call.</span></span></p>
<p><span data-ttu-id="e774d-320">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e774d-320">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-321"><strong>CallerWiFiDriverVersion</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-321"><strong>CallerWiFiDriverVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-322">int</span><span class="sxs-lookup"><span data-stu-id="e774d-322">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-323">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-323">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-324">Número da versão do driver WiFi empregado pelo usuário que fez a chamada.</span><span class="sxs-lookup"><span data-stu-id="e774d-324">Version number for the WiFi driver employed by the user who placed the call.</span></span></p>
<p><span data-ttu-id="e774d-325">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e774d-325">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-326"><strong>CalleReflexiveLocalIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-326"><strong>CalleReflexiveLocalIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-327">int</span><span class="sxs-lookup"><span data-stu-id="e774d-327">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-328">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-328">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-329">Endereço IP reflexivo do usuário que recebeu a chamada.</span><span class="sxs-lookup"><span data-stu-id="e774d-329">Reflexive IP address of the user who received the call.</span></span> <span data-ttu-id="e774d-330">Em organizações que usam NAT (Network Address Translation), o endereço IP reflexivo é o endereço IP do servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="e774d-330">In organizations that use NAT (network address translation), the reflexive IP address is the IP address of the proxy server.</span></span></p>
<p><span data-ttu-id="e774d-331">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e774d-331">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e774d-332"><strong>CalleeWiFiDriverDevicesDesc</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-332"><strong>CalleeWiFiDriverDevicesDesc</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-333">int</span><span class="sxs-lookup"><span data-stu-id="e774d-333">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-334">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-334">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-335">Descrição do dispositivo para o driver WiFi empregado pelo usuário que recebeu a chamada.</span><span class="sxs-lookup"><span data-stu-id="e774d-335">Device description for the WiFi driver employed by the user who received the call.</span></span></p>
<p><span data-ttu-id="e774d-336">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e774d-336">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e774d-337"><strong>CalleeWiFiDriverVersion</strong></span><span class="sxs-lookup"><span data-stu-id="e774d-337"><strong>CalleeWiFiDriverVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="e774d-338">int</span><span class="sxs-lookup"><span data-stu-id="e774d-338">int</span></span></p></td>
<td><p><span data-ttu-id="e774d-339">Exterior</span><span class="sxs-lookup"><span data-stu-id="e774d-339">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e774d-340">Número da versão do driver WiFi empregado pelo usuário que recebeu a chamada.</span><span class="sxs-lookup"><span data-stu-id="e774d-340">Version number for the WiFi driver employed by the user who received the call.</span></span></p>
<p><span data-ttu-id="e774d-341">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e774d-341">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e774d-342">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e774d-342">


</div>

<span> </span>

</div>

</div>

</span></span></div>

