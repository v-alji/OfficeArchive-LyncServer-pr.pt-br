---
title: 'Lync Server 2013: Tabela AudioClientEvent'
description: 'Lync Server 2013: AudioClientEvent Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioClientEvent table
ms:assetid: fef73d8f-7261-4e5b-9769-82435b007979
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413086(v=OCS.15)
ms:contentKeyID: 48185967
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2200cd9567bdd10ac4ad8f5c269062c2f5614dcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438202"
---
# <a name="audioclientevent-table-in-lync-server-2013"></a><span data-ttu-id="5b793-103">Tabela AudioClientEvent no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5b793-103">AudioClientEvent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b793-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b793-104">

<span> </span></span></span>

<span data-ttu-id="5b793-105">_**Tópico da última modificação:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="5b793-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="5b793-106">Cada registro contém um evento de cliente para um ponto de extremidade em uma chamada de áudio.</span><span class="sxs-lookup"><span data-stu-id="5b793-106">Each record contains a client event for one endpoint in an audio call.</span></span> <span data-ttu-id="5b793-107">Geralmente, uma chamada tem dois registros, um para o chamador e outro para o receptor.</span><span class="sxs-lookup"><span data-stu-id="5b793-107">Usually, one call has two records, one for caller and one for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b793-108"><strong>Coluna</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="5b793-109"><strong>Tipo de dados</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="5b793-110"><strong>Chave/índice</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="5b793-111"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b793-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-113">datetime</span><span class="sxs-lookup"><span data-stu-id="5b793-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="5b793-114">Primária</span><span class="sxs-lookup"><span data-stu-id="5b793-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="5b793-115">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="5b793-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b793-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-117">int</span><span class="sxs-lookup"><span data-stu-id="5b793-117">int</span></span></p></td>
<td><p><span data-ttu-id="5b793-118">Primária</span><span class="sxs-lookup"><span data-stu-id="5b793-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="5b793-119">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="5b793-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b793-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="5b793-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="5b793-122">Primária</span><span class="sxs-lookup"><span data-stu-id="5b793-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="5b793-123">Referenciado da <a href="lync-server-2013-medialine-table.md">tabela de mídias no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="5b793-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b793-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-125">bit</span><span class="sxs-lookup"><span data-stu-id="5b793-125">bit</span></span></p></td>
<td><p><span data-ttu-id="5b793-126">Primária</span><span class="sxs-lookup"><span data-stu-id="5b793-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="5b793-127">0: dados do chamador</span><span class="sxs-lookup"><span data-stu-id="5b793-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="5b793-128">1: dados do chamador</span><span class="sxs-lookup"><span data-stu-id="5b793-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b793-129"><strong>NetworkSendQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-129"><strong>NetworkSendQualityEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-130">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-130">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5b793-131">Porcentagem da sessão o evento NetworkSendQuality foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="5b793-131">Percentage of session the NetworkSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="5b793-132">A qualidade da rede em termos de tremulação ou perda de pacote é grave e afetando a qualidade do áudio que está sendo enviado.</span><span class="sxs-lookup"><span data-stu-id="5b793-132">Network quality in terms of jitter or packet loss is severe and impacting the quality of audio being sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b793-133"><strong>NetworkReceiveQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-133"><strong>NetworkReceiveQualityEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-134">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-134">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5b793-135">Porcentagem da sessão o evento ReceiveSendQuality foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="5b793-135">Percentage of session the ReceiveSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="5b793-136">A qualidade da rede em termos de tremulação ou perda de pacote é severa e afeta a qualidade do áudio sendo recebido.</span><span class="sxs-lookup"><span data-stu-id="5b793-136">Network quality in terms of jitter or packet loss is severe and impacting the quality of audio being received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b793-137"><strong>NetworkDelayEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-137"><strong>NetworkDelayEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-138">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-138">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5b793-139">Porcentagem da sessão o evento Delay foi acionado para o estado ' Bad '.</span><span class="sxs-lookup"><span data-stu-id="5b793-139">Percentage of session the Delay event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="5b793-140">A latência da rede é severa e impacta a experiência ao impedir a comunicação interativa</span><span class="sxs-lookup"><span data-stu-id="5b793-140">Network latency is severe and impacting the experience by preventing interactive communication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b793-141"><strong>NetworkBandwidthLowEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-141"><strong>NetworkBandwidthLowEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-142">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-142">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5b793-143">Porcentagem da sessão o evento LowBandwidth foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="5b793-143">Percentage of session the LowBandwidth event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="5b793-144">A largura de banda disponível é insuficiente para uma experiência de voz aceitável.</span><span class="sxs-lookup"><span data-stu-id="5b793-144">The available bandwidth is insufficient for an acceptable voice experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b793-145"><strong>CPUInsufficientEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-145"><strong>CPUInsufficientEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-146">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-146">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5b793-147">Porcentagem da sessão o evento de CPU insuficiente foi acionado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="5b793-147">Percentage of session the insufficient CPU event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="5b793-148">Não há ciclos de CPU suficientes para processamento com as modalidades e aplicativos atuais em uso.</span><span class="sxs-lookup"><span data-stu-id="5b793-148">There are insufficient CPU cycles for processing with the current modalities and applications in use.</span></span> <span data-ttu-id="5b793-149">Isso causa distorções com o canal de áudio.</span><span class="sxs-lookup"><span data-stu-id="5b793-149">This causes distortions with the audio channel.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b793-150"><strong>DeviceHalfDuplexAECEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-150"><strong>DeviceHalfDuplexAECEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-151">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-151">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5b793-152">Porcentagem da sessão o evento DeviceHalfDuplexAEC foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="5b793-152">Percentage of session the DeviceHalfDuplexAEC event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="5b793-153">Para evitar eco, o sistema entra em Half duplex.</span><span class="sxs-lookup"><span data-stu-id="5b793-153">In order to prevent echo, the system has enter half duplex.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b793-154"><strong>DeviceRenderNotFunctioningEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-154"><strong>DeviceRenderNotFunctioningEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-155">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-155">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5b793-156">Porcentagem da sessão o evento DeviceRenderNotFunctioning foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="5b793-156">Percentage of session the DeviceRenderNotFunctioning event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="5b793-157">O dispositivo de renderização atualmente sendo usado para a sessão não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5b793-157">The render device currently being used for the session is not functioning correctly.</span></span> <span data-ttu-id="5b793-158">Isso pode causar problemas de áudio unidirecionais.</span><span class="sxs-lookup"><span data-stu-id="5b793-158">This can cause one-way audio issues.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b793-159"><strong>DeviceCaptureNotFunctioningEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-159"><strong>DeviceCaptureNotFunctioningEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-160">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-160">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5b793-161">Porcentagem da sessão o evento DeviceCaptureNotFunctioning foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="5b793-161">Percentage of session the DeviceCaptureNotFunctioning event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="5b793-162">O dispositivo de captura atualmente sendo usado para a sessão não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5b793-162">The capture device currently being used for the session is not functioning correctly.</span></span> <span data-ttu-id="5b793-163">Isso pode causar problemas de áudio unidirecionais.</span><span class="sxs-lookup"><span data-stu-id="5b793-163">This can cause one-way audio issues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b793-164"><strong>DeviceGlitchesEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-164"><strong>DeviceGlitchesEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-165">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-165">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5b793-166">Porcentagem da sessão o evento DeviceGlitches foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="5b793-166">Percentage of session the DeviceGlitches event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="5b793-167">Há graves problemas na renderização de áudio que está causando distorções.</span><span class="sxs-lookup"><span data-stu-id="5b793-167">There are severe glitches in the rendering of audio which is causing distortions.</span></span> <span data-ttu-id="5b793-168">Esses problemas podem ser causados por problemas de driver, Storm (chamadas de procedimento) adiadas (DPC) e alta utilização da CPU.</span><span class="sxs-lookup"><span data-stu-id="5b793-168">These glitches can be caused by driver issues, deferred procedure calls (DPC) storm (drivers), and high CPU usage.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b793-169"><strong>DeviceLowSNREventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-169"><strong>DeviceLowSNREventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-170">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-170">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5b793-171">Porcentagem da sessão o evento DeviceLowSNR foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="5b793-171">Percentage of session the DeviceLowSNR event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="5b793-172">A qualidade de captura é muito ruim, ou seja, muito ruidosa ou o usuário está falando muito longe do microfone.</span><span class="sxs-lookup"><span data-stu-id="5b793-172">The capture quality is very poor, either very noisy or user is talking too far away from the microphone.</span></span> <span data-ttu-id="5b793-173">Isso causará distorções.</span><span class="sxs-lookup"><span data-stu-id="5b793-173">This will cause distortions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b793-174"><strong>DeviceLowSpeechLevelEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-174"><strong>DeviceLowSpeechLevelEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-175">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-175">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5b793-176">Porcentagem da sessão o evento DeviceLowSpeechLevel foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="5b793-176">Percentage of session the DeviceLowSpeechLevel event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="5b793-177">O nível de fala do usuário é muito baixo e o sistema não pode aumentar ainda mais.</span><span class="sxs-lookup"><span data-stu-id="5b793-177">User‘s speech level is too low and the system cannot increase it any further.</span></span> <span data-ttu-id="5b793-178">Isso pode causar distorções ou ser percebida como um áudio unidirecional.</span><span class="sxs-lookup"><span data-stu-id="5b793-178">This can either cause distortions or perceived as one-way audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b793-179"><strong>DeviceClippingEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-179"><strong>DeviceClippingEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-180">Decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-180">Decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5b793-181">Porcentagem da sessão o evento DeviceClipping foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="5b793-181">Percentage of session the DeviceClipping event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="5b793-182">Quando a fala near-end corta o microfone, a distorção de alta distância é distorcido devido ao recorte.</span><span class="sxs-lookup"><span data-stu-id="5b793-182">When near-end speech clips the microphone, far-end hears distortion due to clipping.</span></span> <span data-ttu-id="5b793-183">É importante evitar o recorte de microfone near-end.</span><span class="sxs-lookup"><span data-stu-id="5b793-183">It is important to avoid near-end microphone clipping.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b793-184"><strong>DeviceEchoEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-184"><strong>DeviceEchoEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-185">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-185">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5b793-186">Porcentagem da sessão o evento DeviceEchoEvent foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="5b793-186">Percentage of session the DeviceEchoEvent event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="5b793-187">O dispositivo ou a instalação está causando eco além da capacidade do sistema de compensar.</span><span class="sxs-lookup"><span data-stu-id="5b793-187">Device or setup is causing echo beyond the ability of the system to compensate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b793-188"><strong>DeviceNearEndToEchoRatioEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-188"><strong>DeviceNearEndToEchoRatioEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-189">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-189">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5b793-190">Porcentagem da sessão o evento DeviceNearEndToEchoRatio foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="5b793-190">Percentage of session the DeviceNearEndToEchoRatio event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="5b793-191">A fala do usuário é muito baixa em comparação com o eco sendo capturado, o que afeta a experiência dos usuários porque limita como é fácil interromper um usuário.</span><span class="sxs-lookup"><span data-stu-id="5b793-191">The user’s speech is too low compared to the echo being captured which impacts the users experience because it limits how easy it is to interrupt a user.</span></span> <span data-ttu-id="5b793-192">Reduza o volume do alto-falante e aproxime o microfone do locutor.</span><span class="sxs-lookup"><span data-stu-id="5b793-192">Reduce speaker volume, move the microphone closer to the talker.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b793-193"><strong>DeviceMultipleEndpointsEventCount</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-193"><strong>DeviceMultipleEndpointsEventCount</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-194">int</span><span class="sxs-lookup"><span data-stu-id="5b793-194">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5b793-195">Número de vezes durante a sessão em que o evento DeviceMultipleEndpoints foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="5b793-195">Number of times during session the DeviceMultipleEndpoints event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="5b793-196">Vários pontos de extremidade de áudio na mesma sessão detectados e o sistema foi compensado por meio da redução do volume de renderização.</span><span class="sxs-lookup"><span data-stu-id="5b793-196">Multiple audio endpoints in the same session detected and the system has compensated by reducing render volume.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b793-197"><strong>DeviceHowlingEventCount</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-197"><strong>DeviceHowlingEventCount</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-198">int</span><span class="sxs-lookup"><span data-stu-id="5b793-198">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5b793-199">Número de vezes durante a sessão em que o evento DeviceHowlingEvent foi disparado para o estado ' ruim '.</span><span class="sxs-lookup"><span data-stu-id="5b793-199">Number of times during session the DeviceHowlingEvent event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="5b793-200">Loop de comentários sobre áudio detectado (causado por vários pontos de extremidade que compartilham o caminho de áudio).</span><span class="sxs-lookup"><span data-stu-id="5b793-200">Audio feedback loop detected (caused by multiple endpoints sharing audio path).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b793-201"><strong>DeviceRenderZeroVolumeEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-201"><strong>DeviceRenderZeroVolumeEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-202">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-202">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5b793-203">Porcentagem da sessão em que o evento DeviceRenderZeroVolume foi disparado para estar no estado "ruim".</span><span class="sxs-lookup"><span data-stu-id="5b793-203">Percentage of session the DeviceRenderZeroVolume event was fired for being in the “Bad’ state.</span></span> <span data-ttu-id="5b793-204">O dispositivo de renderização foi definido como volume zero.</span><span class="sxs-lookup"><span data-stu-id="5b793-204">The render device was set to zero volume.</span></span></p>
<p><span data-ttu-id="5b793-205">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5b793-205">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b793-206"><strong>DeviceRenderMuteEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5b793-206"><strong>DeviceRenderMuteEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="5b793-207">decimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="5b793-207">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5b793-208">Porcentagem da sessão em que o evento DeviceRenderMute foi disparado para estar no estado "ruim".</span><span class="sxs-lookup"><span data-stu-id="5b793-208">Percentage of session the DeviceRenderMute event was fired for being in the “Bad’ state.</span></span> <span data-ttu-id="5b793-209">O dispositivo de renderização estava com mudo ativado.</span><span class="sxs-lookup"><span data-stu-id="5b793-209">The render device was muted.</span></span></p>
<p><span data-ttu-id="5b793-210">Esta coluna foi introduzida no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5b793-210">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5b793-211">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b793-211">


</div>

<span> </span>

</div>

</div>

</span></span></div>

