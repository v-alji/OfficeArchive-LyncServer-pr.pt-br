---
title: Interpretação dos resultados
description: Interpretação dos resultados.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Interpreting the Results
ms:assetid: dd7f199f-7075-4d88-bb84-49a7e05eb593
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945608(v=OCS.15)
ms:contentKeyID: 51541433
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8342a1ec1e15e42852fc5293f87342e98587a60
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443171"
---
# <a name="interpreting-the-results"></a><span data-ttu-id="bd4a8-103">Interpretação dos resultados</span><span class="sxs-lookup"><span data-stu-id="bd4a8-103">Interpreting the Results</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bd4a8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bd4a8-104">

<span> </span></span></span>

<span data-ttu-id="bd4a8-105">_**Tópico da última modificação:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="bd4a8-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="bd4a8-106">A ferramenta de stress e desempenho do Lync Server 2013 (LyncPerfTool.exe) tem muitos contadores que você pode usar para compreender o que o cliente está fazendo e se ele está encontrando problemas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-106">The Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe) has many counters that you can use to understand what the client is doing and whether it is encountering issues.</span></span>

<div>

## <a name="client-counters"></a><span data-ttu-id="bd4a8-107">Contadores de cliente</span><span class="sxs-lookup"><span data-stu-id="bd4a8-107">Client Counters</span></span>

<span data-ttu-id="bd4a8-108">Cada instância do LyncPerfTool.exe que está sendo executada tem uma instância separada dos contadores.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-108">Each instance of LyncPerfTool.exe that is running has a separate instance of the counters.</span></span> <span data-ttu-id="bd4a8-109">Cada instância é nomeada pela ID do processo.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-109">Each instance is named by its process ID.</span></span>

<span data-ttu-id="bd4a8-110">Se os clientes estiverem sobrecarregados, podem ocorrer problemas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-110">If the clients are overloaded, issues can occur.</span></span> <span data-ttu-id="bd4a8-111">Para evitar esses problemas, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="bd4a8-111">To prevent these issues, do the following:</span></span>

1.  <span data-ttu-id="bd4a8-112">Monitore a CPU e o uso da memória nos computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-112">Monitor the CPU and the memory usage on the client computers.</span></span> <span data-ttu-id="bd4a8-113">Se a CPU estiver consistentemente acima de 90%, reduza o número de usuários.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-113">If the CPU is consistently above 90 percent, reduce the number of users.</span></span>

2.  <span data-ttu-id="bd4a8-114">Se o espaço da memória for alto, você poderá ter problemas se o arquivo da página não for grande o suficiente.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-114">If the memory footprint is high, you could run into issues if the page file is not big enough.</span></span> <span data-ttu-id="bd4a8-115">Verifique se a carga comprometida não está atingindo o limite do computador.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-115">Verify that the Commit Charge is not hitting the limit on the computer.</span></span> <span data-ttu-id="bd4a8-116">Se você estiver executando limites de memória, considere aumentar o tamanho do arquivo da página ou reduzir o número de usuários</span><span class="sxs-lookup"><span data-stu-id="bd4a8-116">If you are running into memory limits, consider increasing the page file size or reducing the number of users</span></span>

<span data-ttu-id="bd4a8-117">As tabelas a seguir listam os principais contadores de desempenho do LyncPerfTool.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-117">The following tables list the key LyncPerfTool performance counters.</span></span>

<span data-ttu-id="bd4a8-118">**Informações gerais**</span><span class="sxs-lookup"><span data-stu-id="bd4a8-118">**General Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd4a8-119"><strong>Contador de desempenho</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-119"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bd4a8-120"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-120"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-121">Tempo gasto em minutos</span><span class="sxs-lookup"><span data-stu-id="bd4a8-121">Time Spent in Minutes</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-122">Tempo gasto desde o início do processo.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-122">Time spent since the process was started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-123">Pontos de extremidade ativos</span><span class="sxs-lookup"><span data-stu-id="bd4a8-123">Active Endpoints</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-124">Número de pontos de extremidade conectados ao servidor no momento.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-124">Number of endpoints currently connected to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-125">Logons com falha</span><span class="sxs-lookup"><span data-stu-id="bd4a8-125">Failed Logons</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-126">Número total de falhas de entrada de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-126">Total number of endpoint sign-in failures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-127">Tentativas de logon</span><span class="sxs-lookup"><span data-stu-id="bd4a8-127">Logon Attempts</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-128">Número total de tentativas de entrada no ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-128">Total number of endpoint sign-in attempts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-129">Pontos de extremidade desconectados</span><span class="sxs-lookup"><span data-stu-id="bd4a8-129">Endpoints Disconnected</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-130">Número total de pontos de extremidade desconectados.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-130">Total number of endpoints that have been disconnected.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd4a8-131">**Informações de presença**</span><span class="sxs-lookup"><span data-stu-id="bd4a8-131">**Presence Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd4a8-132"><strong>Contador de desempenho</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-132"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bd4a8-133"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-133"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-134">Chamadas de presença</span><span class="sxs-lookup"><span data-stu-id="bd4a8-134">SetPresence Calls</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-135">Número total de tentativas de alteração de presença.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-135">Total number of presence change attempts.</span></span> <span data-ttu-id="bd4a8-136">Para diferentes tipos de alterações de presença, consulte o contador de desempenho de chamadas de presença (tipo de presença).</span><span class="sxs-lookup"><span data-stu-id="bd4a8-136">For different types of presence changes, see the SetPresence (Presence Type) Calls Performance Counter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-137">Respostas de NNN para setpresence</span><span class="sxs-lookup"><span data-stu-id="bd4a8-137">NNN Responses for SetPresence</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-138">Número total de códigos de resposta de nnn recebidos do servidor.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-138">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-139">Chamadas de getpresence</span><span class="sxs-lookup"><span data-stu-id="bd4a8-139">GetPresence Calls</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-140">Número total de tentativas de obter solicitação de presença.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-140">Total number of get presence request attempts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-141">Respostas NNN para getpresence</span><span class="sxs-lookup"><span data-stu-id="bd4a8-141">NNN Responses for GetPresence</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-142">Número total de códigos de resposta de nnn recebidos do servidor.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-142">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd4a8-143">**Informações do serviço de catálogo de endereços**</span><span class="sxs-lookup"><span data-stu-id="bd4a8-143">**Address Book service Information**</span></span>

<span data-ttu-id="bd4a8-144">Esta categoria inclui contadores usados para monitorar downloads de arquivos do serviço de catálogo de endereços (ABS) e catálogo de endereços da Web consulta de serviço.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-144">This category includes counters used to monitor Address Book service (ABS) file downloads and Address Book Web Query service requests.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd4a8-145"><strong>Contador de desempenho</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-145"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bd4a8-146"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-146"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-147">Tentativas de download de arquivo completo/Delta da ABS</span><span class="sxs-lookup"><span data-stu-id="bd4a8-147">ABS Full/Delta File Downloads Attempted</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-148">Número total de solicitações de download de arquivos completas ou Delta tentadas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-148">Total number of full or delta file download requests attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-149">Downloads de arquivo completo/Delta do ABS bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="bd4a8-149">ABS Full/Delta File Downloads Succeeded</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-150">Número total de solicitações de download de arquivos completas ou Delta tentadas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-150">Total number of full or delta file download requests attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-151">Contadores relacionados ao serviço de consulta na Web do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="bd4a8-151">Address Book Web Query service related counters</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-152">Contadores relacionados ao download de arquivos do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-152">Address book file download related counters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-153">Chamadas de WS WS tentadas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-153">ABS WS Calls attempted</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-154">Número total de tentativas de solicitações de serviço de consulta à Web do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-154">Total number of Address Book Web Query service requests attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-155">Chamadas do WS para ABS bem-sucedidas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-155">ABS WS Calls Succeeded</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-156">Número total de solicitações de serviço de consulta à Web do catálogo de endereços que retornaram um código de resposta bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-156">Total number of Address Book Web Query service requests that returned a successful response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-157">Falha nas chamadas ABS WS</span><span class="sxs-lookup"><span data-stu-id="bd4a8-157">ABS WS Calls Failed</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-158">Número total de solicitações de serviço de consulta à Web do catálogo de endereços que retornaram um código de resposta de erro.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-158">Total number of Address Book Web Query service requests that returned an error response code.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd4a8-159">**Informações de lista de distribuição (DL)**</span><span class="sxs-lookup"><span data-stu-id="bd4a8-159">**Distribution List (DL) Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd4a8-160"><strong>Contador de desempenho</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-160"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bd4a8-161"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-161"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-162">Chamadas tentadas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-162">Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-163">Número total de solicitações de serviço Web de expansão da lista de distribuição (DLX) tentadas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-163">Total number of distribution list expansion (DLX) web service requests attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-164">Chamadas com êxito</span><span class="sxs-lookup"><span data-stu-id="bd4a8-164">Calls Succeeded</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-165">Número total de solicitações de serviço Web DLX que retornaram um código de resposta bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-165">Total number of DLX web service requests that returned a successful response code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-166">Falha nas chamadas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-166">Calls Failed</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-167">Número total de solicitações de serviço Web DLX que retornaram um código de resposta de erro.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-167">Total number of DLX web service requests that returned an error response code.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd4a8-168">**Informações básicas de VoIP**</span><span class="sxs-lookup"><span data-stu-id="bd4a8-168">**VoIP Basic Information**</span></span>

<span data-ttu-id="bd4a8-169">Os contadores de desempenho listados abaixo numeram os números de todas as chamadas de voz sobre IP (VoIP), incluindo chamadas para servidor de mediação, servidor de conferência A/V, servidor de borda, aplicativo de grupo de resposta e atendedor automático de conferência, quando esses cenários são habilitados.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-169">The performance counters listed below report numbers for all Voice over IP (VoIP) calls, including calls to Mediation Server, A/V Conferencing Server, Edge Server, Response Group application, and Conference Auto Attendant, when these scenarios are enabled.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd4a8-170"><strong>Contador de desempenho</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-170"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bd4a8-171"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-171"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-172">Chamadas ativas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-172">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-173">Número total de chamadas de voz de entrada/saída em andamento no momento.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-173">Total number of incoming/outgoing voice calls ongoing currently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-174">Chamadas terminadas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-174">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-175">Número total de chamadas de voz de entrada/saída já terminadas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-175">Total number of incoming/outgoing voice calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-176">Chamadas recusadas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-176">Calls Declined</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-177">Número total de chamadas de voz recebidas recusadas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-177">Total number of incoming voice calls declined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-178">Tentativa de fazer chamadas de entrada/saída</span><span class="sxs-lookup"><span data-stu-id="bd4a8-178">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-179">Número total de chamadas de voz de entrada/saída tentadas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-179">Total number of incoming/outgoing voice calls attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-180">Chamadas de entrada/saída estabelecidas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-180">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-181">Número total de chamadas de voz de entrada/saída estabelecidas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-181">Total number of incoming/outgoing voice calls established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-182">Chamadas recebidas NNN</span><span class="sxs-lookup"><span data-stu-id="bd4a8-182">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-183">Número total de códigos de resposta de nnn recebidos do servidor.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-183">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-184">Taxa de aprovação de VoIP (%)</span><span class="sxs-lookup"><span data-stu-id="bd4a8-184">VoIP Pass Rate (%)</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-185">Total de chamadas estabelecidas/total de chamadas tentadas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-185">Total calls established/Total calls attempted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd4a8-186">**Informações de chamada do serviço de grupo de resposta**</span><span class="sxs-lookup"><span data-stu-id="bd4a8-186">**Response Group service Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd4a8-187"><strong>Contador de desempenho</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-187"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bd4a8-188"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-188"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-189">Chamadas ativas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-189">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-190">Número total de chamadas ativas para o aplicativo de grupo de resposta.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-190">Total number of active calls to the Response Group application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-191">Chamadas tentadas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-191">Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-192">Número total de chamadas tentadas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-192">Total number of calls attempted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd4a8-193">**Informações de chamada de mensagens instantâneas (IM)**</span><span class="sxs-lookup"><span data-stu-id="bd4a8-193">**Instant Messaging (IM) Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd4a8-194"><strong>Contador de desempenho</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-194"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bd4a8-195"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-195"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-196">Chamadas ativas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-196">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-197">Número total de chamadas de mensagens instantâneas de entrada/saída contínuas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-197">Total number of ongoing incoming/outgoing instant messaging calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-198">Chamadas terminadas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-198">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-199">Número total de chamadas de entrada/saída de mensagens instantâneas já terminadas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-199">Total number of incoming/outgoing instant messaging calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-200">Chamadas recebidas NNN</span><span class="sxs-lookup"><span data-stu-id="bd4a8-200">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-201">Número total de códigos de resposta de nnn recebidos do servidor.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-201">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-202">Mensagens INSTANTÂNEAs recebidas/enviadas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-202">IM Messages Received/Sent</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-203">Número total de mensagens recebidas ou enviadas para todas as sessões.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-203">Total number of messages received or sent for all sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-204">Tentativa de fazer chamadas de entrada/saída</span><span class="sxs-lookup"><span data-stu-id="bd4a8-204">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-205">Número total de tentativas de entrada/saída de mensagens instantâneas feitas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-205">Total number of incoming/outgoing instant messaging calls attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-206">Chamadas de entrada/saída estabelecidas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-206">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-207">Número total de chamadas de entrada/saída de mensagens instantâneas estabelecidas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-207">Total number of incoming/outgoing instant message calls established.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd4a8-208">**Informações de chamada de compartilhamento de aplicativo**</span><span class="sxs-lookup"><span data-stu-id="bd4a8-208">**App Sharing Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd4a8-209"><strong>Contador de desempenho</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-209"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bd4a8-210"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-210"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-211">Chamadas ativas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-211">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-212">Número total de chamadas de compartilhamento de aplicativo de entrada/saída contínuas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-212">Total number of ongoing incoming/outgoing application sharing calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-213">Chamadas terminadas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-213">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-214">Número total de chamadas de compartilhamento de aplicativo de entrada/saída já terminadas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-214">Total number of incoming/outgoing application sharing calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-215">Chamadas recebidas NNN</span><span class="sxs-lookup"><span data-stu-id="bd4a8-215">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-216">Número total de códigos de resposta de nnn recebidos do servidor.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-216">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-217">Tentativa de fazer chamadas de entrada/saída</span><span class="sxs-lookup"><span data-stu-id="bd4a8-217">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-218">Número total de chamadas de compartilhamento de aplicativo de entrada/saída tentadas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-218">Total number of incoming/outgoing application sharing calls attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-219">Chamadas de entrada/saída estabelecidas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-219">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-220">Número total de chamadas de compartilhamento de aplicativo de entrada/saída estabelecidas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-220">Total number of incoming/outgoing application sharing calls established.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd4a8-221">**Informações de chamada do CAA**</span><span class="sxs-lookup"><span data-stu-id="bd4a8-221">**CAA Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd4a8-222"><strong>Contador de desempenho</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-222"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bd4a8-223"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-223"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-224">Chamadas ativas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-224">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-225">Número total de chamadas em PSTN (rede telefônica pública comutada) de entrada/saída em andamento no momento.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-225">Total number of incoming/outgoing public switched telephone network (PSTN) calls ongoing currently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-226">Chamadas terminadas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-226">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-227">Número total de chamadas PSTN de entrada/saída já terminadas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-227">Total number of incoming/outgoing PSTN calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-228">Tentativa de fazer chamadas de entrada/saída</span><span class="sxs-lookup"><span data-stu-id="bd4a8-228">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-229">Número total de chamadas de entrada PSTN de entrada/saída tentadas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-229">Total number of incoming/outgoing PSTN calls attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-230">Chamadas de entrada/saída estabelecidas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-230">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-231">Número total de chamadas PSTN de entrada/saída estabelecidas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-231">Total number of incoming/outgoing PSTN calls established.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd4a8-232">**Informações de conferência**</span><span class="sxs-lookup"><span data-stu-id="bd4a8-232">**Conference Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd4a8-233"><strong>Contador de desempenho</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-233"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bd4a8-234"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-234"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-235">Conferências de mensagens instantâneas ativas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-235">Active Instant Messaging Conferences</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-236">Número total de conferências de mensagens instantâneas em andamento.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-236">Total number of ongoing instant messaging conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-237">Conferências de áudio/vídeo ativas</span><span class="sxs-lookup"><span data-stu-id="bd4a8-237">Active Audio/Video Conferences</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-238">Número total de conferências contínuas de áudio/vídeo (A/V).</span><span class="sxs-lookup"><span data-stu-id="bd4a8-238">Total number of ongoing audio/video (A/V) conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-239">Conferências de compartilhamento de aplicativos ativos</span><span class="sxs-lookup"><span data-stu-id="bd4a8-239">Active Application Sharing Conferences</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-240">Número total de conferências de compartilhamento de aplicativos contínuas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-240">Total number of ongoing application sharing conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-241">Número de participantes</span><span class="sxs-lookup"><span data-stu-id="bd4a8-241">Number of Participants</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-242">Número total de participantes atualmente conectados a conferências.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-242">Total number of participants currently connected to conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-243">Falha no cronograma da conferência</span><span class="sxs-lookup"><span data-stu-id="bd4a8-243">Conference Schedule Failure</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-244">Número total de falhas ao tentar agendar uma conferência.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-244">Total number of failures while trying to schedule a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-245">Ingressar na falha na conferência</span><span class="sxs-lookup"><span data-stu-id="bd4a8-245">Join Conference Failure</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-246">Número total de falhas ao tentar se conectar a uma conferência.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-246">Total number of failures while trying to connect to a conference.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd4a8-247">**Contadores do cliente UCWA**</span><span class="sxs-lookup"><span data-stu-id="bd4a8-247">**UCWA Client Counters**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd4a8-248"><strong>Contador de desempenho</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-248"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bd4a8-249"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="bd4a8-249"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd4a8-250">Número total de junções de IMMCU bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="bd4a8-250">Total Number of IMMCU Joins Succeeded</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-251">Número total de conferências de mensagens instantâneas Unidas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-251">Total number of instant messaging conferences joined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd4a8-252">Número total de junções de DMCU bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="bd4a8-252">Total Number of DMCU Joins Succeeded</span></span></p></td>
<td><p><span data-ttu-id="bd4a8-253">Número total de conferências de A/V Unidas.</span><span class="sxs-lookup"><span data-stu-id="bd4a8-253">Total number of A/V conferences joined.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bd4a8-254">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bd4a8-254">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

