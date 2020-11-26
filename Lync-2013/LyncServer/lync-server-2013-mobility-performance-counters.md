---
title: 'Lync Server 2013: contadores de desempenho da mobilidade'
description: 'Lync Server 2013: contadores de desempenho da mobilidade.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mobility performance counters
ms:assetid: d18ed85a-673d-4695-aa3f-ac83a38ab90a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690046(v=OCS.15)
ms:contentKeyID: 48185441
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 922288f6c026f088d651dc61afdcb6ba04fed30a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425553"
---
# <a name="mobility-performance-counters-in-lync-server-2013"></a><span data-ttu-id="79999-103">Contadores de desempenho de mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="79999-103">Mobility performance counters in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="79999-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="79999-104">

<span> </span></span></span>

<span data-ttu-id="79999-105">_**Tópico da última modificação:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="79999-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="79999-106">As tabelas a seguir listam os nomes e descrições dos contadores de desempenho que você pode usar para monitorar servidores que executam a API da Web de comunicação unificada (UCWA) e o serviço de mobilidade do MCX do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="79999-106">The following tables list the names and descriptions of performance counters that you can use to monitor servers running the Unified Communications Web API (UCWA) and the Lync Server 2013 Mcx Mobility Service.</span></span>

<span data-ttu-id="79999-107">O nome da categoria para os contadores na tabela UCWA é **LS:WEB – UCWA**.</span><span class="sxs-lookup"><span data-stu-id="79999-107">The category name for the counters in the UCWA table is **LS:WEB – UCWA**.</span></span>

<span data-ttu-id="79999-108">O nome da categoria para os contadores na tabela do Serviço de Mobilidade Mcx é **LS:WEB – Mobile Communication Service**.</span><span class="sxs-lookup"><span data-stu-id="79999-108">The category name for the counters in the Mcx Mobility Service table is **LS:WEB - Mobile Communication Service**.</span></span>

<div>

## <a name="performance-counters-for-ucwa"></a><span data-ttu-id="79999-109">Contadores de desempenho para UCWA</span><span class="sxs-lookup"><span data-stu-id="79999-109">Performance Counters for UCWA</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="79999-110">Contador</span><span class="sxs-lookup"><span data-stu-id="79999-110">Counter</span></span></th>
<th><span data-ttu-id="79999-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="79999-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79999-112">Contagem de aplicativos ativos</span><span class="sxs-lookup"><span data-stu-id="79999-112">Active Application Count</span></span></p></td>
<td><p><span data-ttu-id="79999-113">O número atual de aplicativos</span><span class="sxs-lookup"><span data-stu-id="79999-113">The current number of applications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-114">Contagem da modalidade de compartilhamento do aplicativo ativa</span><span class="sxs-lookup"><span data-stu-id="79999-114">Active Application Sharing Modality Count</span></span></p></td>
<td><p><span data-ttu-id="79999-115">O número atual da modalidade de compartilhamento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="79999-115">The current number of Application Sharing modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-116">Contagem da modalidade de áudio ativa</span><span class="sxs-lookup"><span data-stu-id="79999-116">Active Audio Modality Count</span></span></p></td>
<td><p><span data-ttu-id="79999-117">O número atual da modalidade de áudio</span><span class="sxs-lookup"><span data-stu-id="79999-117">The current number of Audio modality</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-118">Contagem da modalidade de colaboração de dados ativa</span><span class="sxs-lookup"><span data-stu-id="79999-118">Active Data Collaboration Modality Count</span></span></p></td>
<td><p><span data-ttu-id="79999-119">O número atual da modalidade de colaboração de dados</span><span class="sxs-lookup"><span data-stu-id="79999-119">The current number of Data Collaboration modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-120">Latência para baixar fotos do diretório ativo (ms)</span><span class="sxs-lookup"><span data-stu-id="79999-120">Active Directory Photo Get Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="79999-121">Esse contador mostra o tempo médio (em milissegundos) para obter uma foto do diretório ativo</span><span class="sxs-lookup"><span data-stu-id="79999-121">This counter shows the average time (in milliseconds) to retrieve a photo from active directory</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-122">Contagem da modalidade de tráfego de mensagens ativa</span><span class="sxs-lookup"><span data-stu-id="79999-122">Active Messaging Modality Count</span></span></p></td>
<td><p><span data-ttu-id="79999-123">O número atual da modalidade de tráfego de mensagens</span><span class="sxs-lookup"><span data-stu-id="79999-123">The current number of Messaging modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-124">Contagem da modalidade de vídeo panorâmico ativa</span><span class="sxs-lookup"><span data-stu-id="79999-124">Active Panoramic Video Modality Count</span></span></p></td>
<td><p><span data-ttu-id="79999-125">O número atual da modalidade de vídeo panorâmico</span><span class="sxs-lookup"><span data-stu-id="79999-125">The current number of Panoramic Video modality</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-126">Contagem de downloads pendentes ativos</span><span class="sxs-lookup"><span data-stu-id="79999-126">Active Pending Get Count</span></span></p></td>
<td><p><span data-ttu-id="79999-127">O número de downloads pendentes atualmente ativos; conexões de longa duração com o servidor</span><span class="sxs-lookup"><span data-stu-id="79999-127">The number of currently active pending gets; long-held connections to the server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-128">Contagem de sessões ativas</span><span class="sxs-lookup"><span data-stu-id="79999-128">Active Session Count</span></span></p></td>
<td><p><span data-ttu-id="79999-129">O número atual de pontos de extremidade registrados no UCWA por aplicativo e no total</span><span class="sxs-lookup"><span data-stu-id="79999-129">The current number of endpoints registered in UCWA per application and total</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-130">Contagem de instâncias de usuário ativas</span><span class="sxs-lookup"><span data-stu-id="79999-130">Active User Instance Count</span></span></p></td>
<td><p><span data-ttu-id="79999-131">O número atual de instâncias de usuário ativas</span><span class="sxs-lookup"><span data-stu-id="79999-131">The current number of user instances</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-132">Instâncias de usuário ativas sem aplicativo</span><span class="sxs-lookup"><span data-stu-id="79999-132">Active User Instances without Application</span></span></p></td>
<td><p><span data-ttu-id="79999-133">O número atual de instâncias de usuário sem aplicativo</span><span class="sxs-lookup"><span data-stu-id="79999-133">The current number of user instances without application</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-134">Contagem da modalidade de vídeo ativa</span><span class="sxs-lookup"><span data-stu-id="79999-134">Active Video Modality Count</span></span></p></td>
<td><p><span data-ttu-id="79999-135">O número atual da modalidade de vídeo</span><span class="sxs-lookup"><span data-stu-id="79999-135">The current number of Video modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-136">Solicitações de criação de aplicativo recebidas por segundo</span><span class="sxs-lookup"><span data-stu-id="79999-136">Application Creation Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="79999-137">A taxa de solicitações de criação de aplicativo recebidas por segundo</span><span class="sxs-lookup"><span data-stu-id="79999-137">The per second rate of received application creation requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-138">Falhas de entrada em MCU de AS</span><span class="sxs-lookup"><span data-stu-id="79999-138">AS MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="79999-139">O número de falhas de entrada em MCU de AS</span><span class="sxs-lookup"><span data-stu-id="79999-139">The number of AS MCU Join Failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-140">Falhas de entrada em MCU de AV</span><span class="sxs-lookup"><span data-stu-id="79999-140">AV MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="79999-141">O número de falhas de entrada em MCU de AV</span><span class="sxs-lookup"><span data-stu-id="79999-141">The number of AV MCU Join Failures</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-142">Tempo médio para inicialização do aplicativo (ms)</span><span class="sxs-lookup"><span data-stu-id="79999-142">Average Application Startup Time (ms)</span></span></p></td>
<td><p><span data-ttu-id="79999-143">O tempo médio para inicialização do aplicativo em milissegundos</span><span class="sxs-lookup"><span data-stu-id="79999-143">The average application startup time in Milliseconds</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-144">Tempo médio de duração por sessão (ms)</span><span class="sxs-lookup"><span data-stu-id="79999-144">Average Lifetime for Session (ms)</span></span></p></td>
<td><p><span data-ttu-id="79999-145">O tempo médio de vida de uma sessão em milissegundos</span><span class="sxs-lookup"><span data-stu-id="79999-145">The average lifetime for a session in milliseconds</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-146">Falhas de entrada em MCU de dados</span><span class="sxs-lookup"><span data-stu-id="79999-146">Data MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="79999-147">O número de falhas de entrada em MCU de dados</span><span class="sxs-lookup"><span data-stu-id="79999-147">The number of Data MCU Join Failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-148">Latência para pesquisa de contatos no Exchange (ms)</span><span class="sxs-lookup"><span data-stu-id="79999-148">Exchange Contact Search Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="79999-149">Esse contador mostra o tempo médio (em milissegundos) para se pesquisar contatos no Exchange</span><span class="sxs-lookup"><span data-stu-id="79999-149">This counter shows the average time (in milliseconds) to search contact in Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-150">Latência para baixar fotos em HD no Exchange (ms)</span><span class="sxs-lookup"><span data-stu-id="79999-150">Exchange HD Photo Get Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="79999-151">Esse contador mostra o tempo médio (em milissegundos) para se baixar uma foto no Exchange</span><span class="sxs-lookup"><span data-stu-id="79999-151">This counter shows the average time (in milliseconds) to retrieve a photo from Exchange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-152">Respostas/segundo do HTTP 4xx</span><span class="sxs-lookup"><span data-stu-id="79999-152">HTTP 4xx Responses/Second</span></span></p></td>
<td><p><span data-ttu-id="79999-153">A taxa de respostas por segundo com o código HTTP 4xx</span><span class="sxs-lookup"><span data-stu-id="79999-153">The per second rate of responses with HTTP 4xx code</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-154">Respostas/segundo do HTTP 5xx</span><span class="sxs-lookup"><span data-stu-id="79999-154">HTTP 5xx Responses/Second</span></span></p></td>
<td><p><span data-ttu-id="79999-155">A taxa de respostas por segundo com o código HTTP 5xx</span><span class="sxs-lookup"><span data-stu-id="79999-155">The per second rate of responses with HTTP 5xx code</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-156">Falhas de entrada em MCU de IM</span><span class="sxs-lookup"><span data-stu-id="79999-156">IM MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="79999-157">O número de falhas de entrada em MCU de IM</span><span class="sxs-lookup"><span data-stu-id="79999-157">The number of IM MCU Join Failures</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-158">Número de falhas ao baixar fotos do Active Directory</span><span class="sxs-lookup"><span data-stu-id="79999-158">Number of Active Directory Photo Get Failures</span></span></p></td>
<td><p><span data-ttu-id="79999-159">O número total de falhas ao baixar fotos do Active Directory</span><span class="sxs-lookup"><span data-stu-id="79999-159">The total number of failures to retrieve photos from Active Directory</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-160">Número de falhas ao pesquisar contatos</span><span class="sxs-lookup"><span data-stu-id="79999-160">Number of Contact Search failures</span></span></p></td>
<td><p><span data-ttu-id="79999-161">O número total de falhas ao pesquisar contatos no Exchange</span><span class="sxs-lookup"><span data-stu-id="79999-161">The total number of failures to search contacts in Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-162">Número de falhas de desserialização</span><span class="sxs-lookup"><span data-stu-id="79999-162">Number of Deserialization Failures</span></span></p></td>
<td><p><span data-ttu-id="79999-163">O número total de falhas de desserialização</span><span class="sxs-lookup"><span data-stu-id="79999-163">The total number of deserialization failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-164">Número de falhas de obtenção de foto HD</span><span class="sxs-lookup"><span data-stu-id="79999-164">Number of HD Photo Get Failures</span></span></p></td>
<td><p><span data-ttu-id="79999-165">O número total de falhas ao baixar fotos em HD do Exchange</span><span class="sxs-lookup"><span data-stu-id="79999-165">The total number of failures to retrieve HD photos from Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-166">Excesso de inscrições por aplicativo</span><span class="sxs-lookup"><span data-stu-id="79999-166">Over The Maximum Subscriptions Per Application</span></span></p></td>
<td><p><span data-ttu-id="79999-167">O número de solicitações de inscrição além do máximo permitido por aplicativo</span><span class="sxs-lookup"><span data-stu-id="79999-167">The number of Subscription requests over the maximum allowed per application</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-168">Excesso de inscrições por lote</span><span class="sxs-lookup"><span data-stu-id="79999-168">Over The Maximum Subscriptions Per Batch</span></span></p></td>
<td><p><span data-ttu-id="79999-169">O número de solicitações de inscrição além do máximo permitido por lote</span><span class="sxs-lookup"><span data-stu-id="79999-169">The number of Subscription requests over the maximum allowed per batch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-170">Falhas de inscrição de presença</span><span class="sxs-lookup"><span data-stu-id="79999-170">Presence Subscription Failures</span></span></p></td>
<td><p><span data-ttu-id="79999-171">O número de falhas ao realizar inscrições de presença</span><span class="sxs-lookup"><span data-stu-id="79999-171">The number of failures to subscribe presence</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-172">Falhas ao se registrar pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="79999-172">Registering Endpoint Failures</span></span></p></td>
<td><p><span data-ttu-id="79999-173">O número de falhas ao se registrar pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="79999-173">The number of failures to register endpoints</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-174">Solicitações recebidas/segundo</span><span class="sxs-lookup"><span data-stu-id="79999-174">Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="79999-175">A taxa de solicitações recebidas por segundo</span><span class="sxs-lookup"><span data-stu-id="79999-175">The per second rate of received requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-176">Solicitações bem-sucedidas/segundo</span><span class="sxs-lookup"><span data-stu-id="79999-176">Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="79999-177">A taxa por segundo de solicitações bem-sucedidas (códigos de resposta HTTP 2xx/3xx)</span><span class="sxs-lookup"><span data-stu-id="79999-177">The per second rate of successful requests (HTTP 2xx/3xx response codes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-178">Solicitações de criação de aplicativo bem-sucedidas/segundo</span><span class="sxs-lookup"><span data-stu-id="79999-178">Succeeded Create Application Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="79999-179">A taxa de solicitações de criação de aplicativo bem-sucedidas por segundo</span><span class="sxs-lookup"><span data-stu-id="79999-179">The per second rate of successful application creation requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-180">Contagem de downloads pendentes com tempo limite ultrapassado</span><span class="sxs-lookup"><span data-stu-id="79999-180">Timed Out Pending Get Count</span></span></p></td>
<td><p><span data-ttu-id="79999-181">O número de downloads pendentes que ultrapassaram o tempo limite</span><span class="sxs-lookup"><span data-stu-id="79999-181">The number of pending gets that timed out</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-182">Total de solicitações de criação de aplicativo recebidas</span><span class="sxs-lookup"><span data-stu-id="79999-182">Total Application Creation Requests Received</span></span></p></td>
<td><p><span data-ttu-id="79999-183">O número total de solicitações de criação de aplicativo recebidas desde que o serviço foi iniciado</span><span class="sxs-lookup"><span data-stu-id="79999-183">The total number of application creation requests received since the service was started</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-184">Total de respostas de HTTP 4xx</span><span class="sxs-lookup"><span data-stu-id="79999-184">Total HTTP 4xx Responses</span></span></p></td>
<td><p><span data-ttu-id="79999-185">O número total de respostas de HTTP 4xx</span><span class="sxs-lookup"><span data-stu-id="79999-185">The total number of HTTP 4xx responses</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-186">Total de respostas de HTTP 5xx</span><span class="sxs-lookup"><span data-stu-id="79999-186">Total HTTP 5xx Responses</span></span></p></td>
<td><p><span data-ttu-id="79999-187">O número total de respostas de HTTP 5xx</span><span class="sxs-lookup"><span data-stu-id="79999-187">The total number of HTTP 5xx responses</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-188">Total de solicitações recebidas no Canal de Comando</span><span class="sxs-lookup"><span data-stu-id="79999-188">Total Requests Received on the Command Channel</span></span></p></td>
<td><p><span data-ttu-id="79999-189">O número total de solicitações recebidas no canal do comando</span><span class="sxs-lookup"><span data-stu-id="79999-189">The total number of requests received on the command channel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-190">Total de solicitações bem-sucedidas</span><span class="sxs-lookup"><span data-stu-id="79999-190">Total Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="79999-191">O número total de solicitações que tiveram êxito</span><span class="sxs-lookup"><span data-stu-id="79999-191">The total number of requests that succeeded</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-192">Total de sessões iniciadas</span><span class="sxs-lookup"><span data-stu-id="79999-192">Total Sessions Initiated</span></span></p></td>
<td><p><span data-ttu-id="79999-193">O número total de sessões iniciadas desde a inicialização do serviço</span><span class="sxs-lookup"><span data-stu-id="79999-193">The total number of sessions that were initiated since the service was started</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-194">Total de sessões encerradas devido ao tempo limite de ociosidade</span><span class="sxs-lookup"><span data-stu-id="79999-194">Total Sessions Terminated Because of Idle Timeout</span></span></p></td>
<td><p><span data-ttu-id="79999-195">O número total de sessões encerradas devido ao tempo limite de usuário ocioso</span><span class="sxs-lookup"><span data-stu-id="79999-195">The total number of sessions that were terminated because of user idle timeout</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-196">Total de aplicativos limitados</span><span class="sxs-lookup"><span data-stu-id="79999-196">Total Throttled Applications</span></span></p></td>
<td><p><span data-ttu-id="79999-197">O número de aplicativos limitados</span><span class="sxs-lookup"><span data-stu-id="79999-197">The number of throttled applications</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div id="sectionSection1" class="section">

### <a name="performance-counters-for-mcx-mobility-service"></a><span data-ttu-id="79999-198">Contadores de desempenho para Mobility Service (Mcx)</span><span class="sxs-lookup"><span data-stu-id="79999-198">Performance Counters for Mcx Mobility Service</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="79999-199">Contador</span><span class="sxs-lookup"><span data-stu-id="79999-199">Counter</span></span></th>
<th><span data-ttu-id="79999-200">Descrição</span><span class="sxs-lookup"><span data-stu-id="79999-200">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79999-201">Tempo médio de vida de uma sessão em milissegundos</span><span class="sxs-lookup"><span data-stu-id="79999-201">Average Lifetime for a Session in Milliseconds</span></span></p></td>
<td><p><span data-ttu-id="79999-202">O tempo médio de vida de uma sessão em milissegundos</span><span class="sxs-lookup"><span data-stu-id="79999-202">The average lifetime for a session in milliseconds</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-203">Assinaturas atuais de notificação por push</span><span class="sxs-lookup"><span data-stu-id="79999-203">Current Push Notification Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="79999-p101">O número atual de assinaturas de notificação por push. Esse número, em conjunto com a Contagem de sessões atualmente ativas, representam o subconjunto de sessões atualmente ativas registradas para dispositivos Windows Mobile ou iPhone.</span><span class="sxs-lookup"><span data-stu-id="79999-p101">The current number of push notification subscriptions. This number, in conjunction with Currently Active Session Count, represents the subset of currently active sessions that are registered for Windows Mobile or iPhone devices.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-206">Contagem de polls de tempo limite de rede ativos no momento</span><span class="sxs-lookup"><span data-stu-id="79999-206">Currently Active Network Timeout Poll Count</span></span></p></td>
<td><p><span data-ttu-id="79999-207">O número de pools de rede que ultrapassaram o tempo limite</span><span class="sxs-lookup"><span data-stu-id="79999-207">The number of network polls that timed out</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-208">Contagem de pools ativos no momento</span><span class="sxs-lookup"><span data-stu-id="79999-208">Currently Active Poll Count</span></span></p></td>
<td><p><span data-ttu-id="79999-209">O número de polls atualmente ativos (conexões de longa duração com o servidor)</span><span class="sxs-lookup"><span data-stu-id="79999-209">The number of currently active polls (long-held connections to the server)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-210">Contagem de sessão ativa no momento</span><span class="sxs-lookup"><span data-stu-id="79999-210">Currently Active Session Count</span></span></p></td>
<td><p><span data-ttu-id="79999-211">Número atual de pontos de extremidade registrados no Mobility Service</span><span class="sxs-lookup"><span data-stu-id="79999-211">Current number of endpoints registered in the Mobility Service</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-212">Contagem de sessão ativa no momento com assinaturas de presença ativa</span><span class="sxs-lookup"><span data-stu-id="79999-212">Currently Active Session Count with Active Presence Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="79999-213">O número de sessões ativas no momento com assinaturas de presença ativa</span><span class="sxs-lookup"><span data-stu-id="79999-213">The number of currently active sessions with active presence subscriptions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-214">Solicitações de notificação por push sem êxito/segundo</span><span class="sxs-lookup"><span data-stu-id="79999-214">Push Notification Requests Failed/Second</span></span></p></td>
<td><p><span data-ttu-id="79999-215">A taxa de notificações por push sem êxito por segundo</span><span class="sxs-lookup"><span data-stu-id="79999-215">The per second rate of failed push notifications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-216">Solicitações de notificação por push bem-sucedidas/segundo</span><span class="sxs-lookup"><span data-stu-id="79999-216">Push Notification Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="79999-217">A taxa de notificações por push bem-sucedidas por segundo</span><span class="sxs-lookup"><span data-stu-id="79999-217">The per second rate of successful push notifications</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-218">Solicitações de notificação por push limitadas/segundo</span><span class="sxs-lookup"><span data-stu-id="79999-218">Push Notification Requests Throttled/Second</span></span></p></td>
<td><p><span data-ttu-id="79999-219">A taxa de notificações por push limitadas por segundo</span><span class="sxs-lookup"><span data-stu-id="79999-219">The per second rate of throttled push notifications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-220">Solicitações de notificação por push/segundo</span><span class="sxs-lookup"><span data-stu-id="79999-220">Push Notification Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="79999-221">A taxa de notificações por push enviadas por segundo</span><span class="sxs-lookup"><span data-stu-id="79999-221">The per second rate of sent push notifications</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-222">Solicitações sem êxito/segundo</span><span class="sxs-lookup"><span data-stu-id="79999-222">Requests Failed/Second</span></span></p></td>
<td><p><span data-ttu-id="79999-223">A taxa de solicitações sem êxito por segundo</span><span class="sxs-lookup"><span data-stu-id="79999-223">The per second rate of failed requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-224">Solicitações recebidas/segundo</span><span class="sxs-lookup"><span data-stu-id="79999-224">Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="79999-225">A taxa de solicitações recebidas por segundo</span><span class="sxs-lookup"><span data-stu-id="79999-225">The per second rate of received requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-226">Solicitações rejeitadas/segundo</span><span class="sxs-lookup"><span data-stu-id="79999-226">Requests Rejected/Second</span></span></p></td>
<td><p><span data-ttu-id="79999-227">A taxa de solicitações receitadas por segundo</span><span class="sxs-lookup"><span data-stu-id="79999-227">The per second rate of rejected requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-228">Solicitações bem-sucedidas/segundo</span><span class="sxs-lookup"><span data-stu-id="79999-228">Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="79999-229">A taxa de solicitações bem-sucedidas por segundo</span><span class="sxs-lookup"><span data-stu-id="79999-229">The per second rate of successful requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-230">Solicitações de início de sessão bem-sucedidas/segundo</span><span class="sxs-lookup"><span data-stu-id="79999-230">Succeeded Initiate Session Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="79999-p102">A taxa de solicitações de Obter localização bem-sucedidas por segundo. As solicitações de início de uma sessão consomem grande parte do CPU no servidor. A carga de pico suportada é de 12/segundo. A sustentabilidade depende de outras cargas no servidor. Iniciar uma sessão normalmente significa um logon de um usuário que ficou desconectado durante um período extenso de tempo.</span><span class="sxs-lookup"><span data-stu-id="79999-p102">The per second rate of successful Get Location requests. Requests to initiate a session consume the most CPU on the server. Peak supported load is 12/second. Sustainability depends on other loads on the server. Initiate a session typically means a sign-in for a user that has been signed out for an extended period of time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-236">Total de chamadas de voz de entrada recusadas</span><span class="sxs-lookup"><span data-stu-id="79999-236">Total Declined Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="79999-237">O número total de chamadas de voz de entrada recusadas</span><span class="sxs-lookup"><span data-stu-id="79999-237">The total number of inbound voice calls that were declined</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-238">Total de chamadas de voz de entrada sem êxito</span><span class="sxs-lookup"><span data-stu-id="79999-238">Total Failed Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="79999-239">O número total de chamadas de voz de entrada que não tiveram êxito</span><span class="sxs-lookup"><span data-stu-id="79999-239">The total number of inbound voice calls that failed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-240">Total de chamadas de voz de saída sem êxito</span><span class="sxs-lookup"><span data-stu-id="79999-240">Total Failed Outbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="79999-241">O número total de chamadas de voz de saída que não tiveram êxito</span><span class="sxs-lookup"><span data-stu-id="79999-241">The total number of outbound voice calls that failed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-242">Número total de sessões encerradas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="79999-242">Total number of sessions terminated by user</span></span></p></td>
<td><p><span data-ttu-id="79999-243">O número total de sessões encerradas por usuários</span><span class="sxs-lookup"><span data-stu-id="79999-243">The total number of sessions terminated by users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-244">Total de solicitações de notificação por push</span><span class="sxs-lookup"><span data-stu-id="79999-244">Total Push Notification Requests</span></span></p></td>
<td><p><span data-ttu-id="79999-245">O número total de solicitações de notificação por push</span><span class="sxs-lookup"><span data-stu-id="79999-245">The total number of push notification requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-246">Total de solicitações de notificação por push em êxito</span><span class="sxs-lookup"><span data-stu-id="79999-246">Total Push Notification Requests Failed</span></span></p></td>
<td><p><span data-ttu-id="79999-247">O número total de solicitações de notificação por push que não tiveram êxito</span><span class="sxs-lookup"><span data-stu-id="79999-247">The total number of push notification requests that failed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-248">Total de solicitações de notificação por push bem-sucedidas</span><span class="sxs-lookup"><span data-stu-id="79999-248">Total Push Notification Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="79999-249">O número total de solicitações de notificação por push bem-sucedidas</span><span class="sxs-lookup"><span data-stu-id="79999-249">The total number of push notification requests that were successful</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-250">Total de solicitações de notificação por push limitadas</span><span class="sxs-lookup"><span data-stu-id="79999-250">Total Push Notification Requests Throttled</span></span></p></td>
<td><p><span data-ttu-id="79999-251">O número total de solicitações de notificação por push limitadas</span><span class="sxs-lookup"><span data-stu-id="79999-251">The total number of push notification requests that were throttled</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-252">Total de solicitações sem êxito</span><span class="sxs-lookup"><span data-stu-id="79999-252">Total Requests Failed</span></span></p></td>
<td><p><span data-ttu-id="79999-253">O número total de solicitações que não tiveram êxito</span><span class="sxs-lookup"><span data-stu-id="79999-253">The total number of requests that failed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-254">Total de solicitações recebidas no Canal de Comando</span><span class="sxs-lookup"><span data-stu-id="79999-254">Total Requests received on the Command Channel</span></span></p></td>
<td><p><span data-ttu-id="79999-255">O número total de solicitações recebidas no canal do comando</span><span class="sxs-lookup"><span data-stu-id="79999-255">The total number of requests received on the command channel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-256">Total de solicitações rejeitadas</span><span class="sxs-lookup"><span data-stu-id="79999-256">Total Requests Rejected</span></span></p></td>
<td><p><span data-ttu-id="79999-257">O número total de solicitações rejeitadas</span><span class="sxs-lookup"><span data-stu-id="79999-257">The total number of requests that were rejected</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-258">Total de solicitações bem-sucedidas</span><span class="sxs-lookup"><span data-stu-id="79999-258">Total Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="79999-259">O número total de solicitações feitas ao Mobility Service que tiveram êxito</span><span class="sxs-lookup"><span data-stu-id="79999-259">The total number of requests made to the Mobility Service that succeeded</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-260">Contagem total de sessões iniciadas</span><span class="sxs-lookup"><span data-stu-id="79999-260">Total Session Initiated Count</span></span></p></td>
<td><p><span data-ttu-id="79999-261">O número total de sessões iniciadas desde a inicialização do Mobility Service</span><span class="sxs-lookup"><span data-stu-id="79999-261">The total number of sessions that were initiated since the Mobility Service was started</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-262">Total de sessões encerradas devido ao tempo limite de usuário ocioso</span><span class="sxs-lookup"><span data-stu-id="79999-262">Total Sessions Terminated Because of User Idle Timeout</span></span></p></td>
<td><p><span data-ttu-id="79999-263">O número total de sessões encerradas devido ao tempo limite de usuário ocioso</span><span class="sxs-lookup"><span data-stu-id="79999-263">The total number of sessions that were terminated because of user idle timeout</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79999-264">Total de chamadas de voz de entrada bem-sucedidas</span><span class="sxs-lookup"><span data-stu-id="79999-264">Total Successful Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="79999-265">O número total de chamadas de voz de entrada que tiveram êxito</span><span class="sxs-lookup"><span data-stu-id="79999-265">The total number of inbound voice calls that were successful</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79999-266">Total de chamadas de voz de saída bem-sucedidas</span><span class="sxs-lookup"><span data-stu-id="79999-266">Total Successful Outbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="79999-267">O número total de chamadas de voz de saída que tiveram êxito</span><span class="sxs-lookup"><span data-stu-id="79999-267">The total number of outbound voice calls that were successful</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="79999-268">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="79999-268">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

