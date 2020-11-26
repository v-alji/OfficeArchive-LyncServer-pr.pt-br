---
title: 'Lync Server 2013: pôster: principais indicadores de integridade'
description: 'Lync Server 2013: pôster: principais indicadores de integridade.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Poster: Key Health Indicators'
ms:assetid: 8367dccf-adaa-4a0b-a4ed-bc9570cc5e24
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn593599(v=OCS.15)
ms:contentKeyID: 61084873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9962d1764d5d2c664bb8415261344d9b48c81149
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424231"
---
# <a name="key-health-indicators-in-lync-server-2013"></a><span data-ttu-id="e8b87-103">Principais indicadores de integridade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8b87-103">Key Health Indicators in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e8b87-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e8b87-104">

<span> </span></span></span>

<span data-ttu-id="e8b87-105">_**Tópico da última modificação:** 2014-02-10_</span><span class="sxs-lookup"><span data-stu-id="e8b87-105">_**Topic Last Modified:** 2014-02-10_</span></span>

<span data-ttu-id="e8b87-106">Este artigo é um complemento dos [principais indicadores de integridade: a base para manter](https://go.microsoft.com/fwlink/?linkid=391838) o pôster saudável dos servidores do Lync, que você pode baixar no centro de download.</span><span class="sxs-lookup"><span data-stu-id="e8b87-106">This article is a companion to the [Key Health Indicators: The Foundation for Maintaining Healthy Lync Servers](https://go.microsoft.com/fwlink/?linkid=391838) poster, which you can download from the Download Center.</span></span>

<span data-ttu-id="e8b87-107">![Cartaz descrevendo a solução de problemas com dados do KHI](images/Dn594589.b6fe82bd-d70f-4c1f-a812-b615ac5fa7d7(OCS.15).jpg "Cartaz descrevendo a solução de problemas com dados do KHI")</span><span class="sxs-lookup"><span data-stu-id="e8b87-107">![Poster describing troubleshooting using KHI data](images/Dn594589.b6fe82bd-d70f-4c1f-a812-b615ac5fa7d7(OCS.15).jpg "Poster describing troubleshooting using KHI data")</span></span>

<span data-ttu-id="e8b87-108">Você pode usar este pôster para saber mais sobre os principais indicadores de integridade (KHIs), contadores de desempenho com limiares que se destinam a revelar problemas da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="e8b87-108">You can use this poster to learn about Key Health Indicators (KHIs), performance counters with thresholds aimed at revealing user experience issues.</span></span> <span data-ttu-id="e8b87-109">A coleta de dados de KHI geralmente é o primeiro passo para implementar a metodologia de qualidade de chamada (CQM), que se concentra em garantir uma experiência de áudio de qualidade para usuários do Lync.</span><span class="sxs-lookup"><span data-stu-id="e8b87-109">Gathering KHI data is usually the first step to implementing the Call Quality Methodology (CQM), which is focused on ensuring a quality audio experience for Lync users.</span></span>

<span data-ttu-id="e8b87-110">Se tiver dúvidas sobre como usar o CQM, você pode enviar suas perguntas para cqmfeedback@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="e8b87-110">If you have questions about how to use CQM, you can submit your questions to cqmfeedback@microsoft.com.</span></span>

<span data-ttu-id="e8b87-111">O pôster explica as seguintes áreas:</span><span class="sxs-lookup"><span data-stu-id="e8b87-111">The poster explains the following areas:</span></span>

  - <span data-ttu-id="e8b87-112">Quais são os principais indicadores de integridade?</span><span class="sxs-lookup"><span data-stu-id="e8b87-112">What are Key Health Indicators?</span></span>

  - <span data-ttu-id="e8b87-113">Para coletar dados do KHI</span><span class="sxs-lookup"><span data-stu-id="e8b87-113">To Collect KHI Data</span></span>

  - <span data-ttu-id="e8b87-114">Fluxo de correção para todas as funções de servidor</span><span class="sxs-lookup"><span data-stu-id="e8b87-114">Remediation Flow for all Server Roles</span></span>

  - <span data-ttu-id="e8b87-115">Glossário</span><span class="sxs-lookup"><span data-stu-id="e8b87-115">Glossary</span></span>

  - <span data-ttu-id="e8b87-116">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="e8b87-116">Front-end Servers</span></span>

  - <span data-ttu-id="e8b87-117">Servidores SQL back-end</span><span class="sxs-lookup"><span data-stu-id="e8b87-117">Backend SQL Servers</span></span>

  - <span data-ttu-id="e8b87-118">Servidores de Mediação</span><span class="sxs-lookup"><span data-stu-id="e8b87-118">Mediation Servers</span></span>

  - <span data-ttu-id="e8b87-119">Servidores de Borda</span><span class="sxs-lookup"><span data-stu-id="e8b87-119">Edge Servers</span></span>

<span id="WhatIs"></span>

<div>

## <a name="what-are-key-health-indicators"></a><span data-ttu-id="e8b87-120">Quais são os principais indicadores de integridade?</span><span class="sxs-lookup"><span data-stu-id="e8b87-120">What are Key Health Indicators?</span></span>

<span data-ttu-id="e8b87-121">Os principais indicadores de integridade são contadores de desempenho com limiares que se destinam a revelar problemas da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="e8b87-121">Key Health Indicators are performance counters with thresholds aimed at revealing user experience issues.</span></span> <span data-ttu-id="e8b87-122">A coleta de dados de KHI geralmente é o primeiro passo para implementar a metodologia de qualidade de chamada (CQM), que se concentra em garantir uma experiência de áudio de qualidade para usuários do Lync.</span><span class="sxs-lookup"><span data-stu-id="e8b87-122">Gathering KHI data is usually the first step to implementing the Call Quality Methodology (CQM), which is focused on ensuring a quality audio experience for Lync users.</span></span>

<span data-ttu-id="e8b87-123">KHIs são usadas além das soluções de monitoramento padrão do Lync (por exemplo, System Center Operations Manager, transações sintéticas, Monitoring Server) e não em vez dessas soluções.</span><span class="sxs-lookup"><span data-stu-id="e8b87-123">KHIs are used in addition to standard Lync Monitoring Solutions (e.g. System Center Operations Manager, Synthetic Transactions, Monitoring Server) and not instead of those solutions.</span></span>

<span data-ttu-id="e8b87-124">Colete os contadores de desempenho do KHI e preencha a planilha do KHI que acompanha o guia de rede para produzir um scorecard que ajudará você a determinar a integridade do servidor de uma implantação do Lync.</span><span class="sxs-lookup"><span data-stu-id="e8b87-124">Collect the KHI performance counters and populate the KHI spreadsheet accompanying the Networking Guide to produce a scorecard that will help you determine the server health of a Lync deployment.</span></span> <span data-ttu-id="e8b87-125">Depois de preenchido, ele orienta você a reparar o ambiente e oferece uma visão adicional para outros participantes.</span><span class="sxs-lookup"><span data-stu-id="e8b87-125">Once populated, it guides you in repairing the environment and gives additional insight to other stakeholders.</span></span> <span data-ttu-id="e8b87-126">Avalie o KHIs mensalmente e incorpore-os aos processos operacionais contínuos de toda a implantação.</span><span class="sxs-lookup"><span data-stu-id="e8b87-126">Evaluate KHIs on a monthly basis and incorporate them into any deployment’s ongoing operational processes.</span></span>

<span data-ttu-id="e8b87-127">Baixe o [Guia de rede do Lync Server](https://go.microsoft.com/fwlink/p/?linkid=390677) para ver a lista completa de KHIs e obter as planilhas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e8b87-127">Download the [Lync Server Networking Guide](https://go.microsoft.com/fwlink/p/?linkid=390677) to see the full list of KHIs and to get the related spreadsheets.</span></span>

</div>

<span id="ToCollect"></span>

<div>

## <a name="to-collect-khi-data"></a><span data-ttu-id="e8b87-128">Para coletar dados do KHI</span><span class="sxs-lookup"><span data-stu-id="e8b87-128">To Collect KHI Data</span></span>

1.  <span data-ttu-id="e8b87-129">Execute o script KHI incluído no guia de rede do Lync Server em cada servidor do Lync.</span><span class="sxs-lookup"><span data-stu-id="e8b87-129">Run the KHI script included with the Lync Server Networking Guide on each Lync Server.</span></span> <span data-ttu-id="e8b87-130">Isso criará um coletor de dados dentro do monitor de desempenho e nomeá-lo KHI.</span><span class="sxs-lookup"><span data-stu-id="e8b87-130">This will create a Data Collector inside of Performance Monitor and name it KHI.</span></span> <span data-ttu-id="e8b87-131">Por padrão, os dados serão sondados a cada 15 segundos.</span><span class="sxs-lookup"><span data-stu-id="e8b87-131">By default, data will be polled every 15 seconds.</span></span>

2.  <span data-ttu-id="e8b87-132">Antes do início do dia útil da sua empresa, vá para cada servidor de Lync e inicie o coletor de dados KHI.</span><span class="sxs-lookup"><span data-stu-id="e8b87-132">Before the start of your company's business day, go to each Lync Server and start the KHI Data Collector.</span></span>

3.  <span data-ttu-id="e8b87-133">No final do dia, interrompa o coletor de dados do KHI e copie os dados em um local central.</span><span class="sxs-lookup"><span data-stu-id="e8b87-133">At the end of that day, stop the KHI Data Collector and copy the data to a central location.</span></span>

4.  <span data-ttu-id="e8b87-134">Depois de usar o monitor de desempenho para preencher a planilha do KHI incluída no download do guia de rede do Lync Server, compare os resultados com os alvos recomendados.</span><span class="sxs-lookup"><span data-stu-id="e8b87-134">After using Performance Monitor to fill in the KHI spreadsheet included with the Lync Server Networking Guide download, compare the results to the recommended targets.</span></span>

</div>

<span id="Remidiation"></span>

<div>

## <a name="remediation-flow-for-all-server-roles"></a><span data-ttu-id="e8b87-135">Fluxo de correção para todas as funções de servidor</span><span class="sxs-lookup"><span data-stu-id="e8b87-135">Remediation Flow for all Server Roles</span></span>

<span data-ttu-id="e8b87-136">Para cada servidor na implementação do Lync, comece verificando se o desempenho do sistema e a integridade do componente do servidor está no nível ou acima do nível desejado.</span><span class="sxs-lookup"><span data-stu-id="e8b87-136">For each server in your Lync implementation, begin by verifying that the server’s component health and system performance is at or above the desired level.</span></span> <span data-ttu-id="e8b87-137">Só depois disso, você deve observar os indicadores relacionados à função do servidor na implementação geral do Lync.</span><span class="sxs-lookup"><span data-stu-id="e8b87-137">Only after that should you look at the indicators relating to the server’s role in the overall Lync implementation.</span></span>

<span data-ttu-id="e8b87-138">Comece coletando dados de desempenho do KHI para todos os servidores.</span><span class="sxs-lookup"><span data-stu-id="e8b87-138">Begin by collecting KHI Performance Data for all servers.</span></span> <span data-ttu-id="e8b87-139">Para cada uma das funções do sistema (detalhes discutidos mais adiante neste documento) determine se os componentes básicos do sistema atendem aos alvos recomendados.</span><span class="sxs-lookup"><span data-stu-id="e8b87-139">For each of the system roles (details discussed later in this document) determine whether the basic system components meet the recommended targets.</span></span> <span data-ttu-id="e8b87-140">Se não fizerem isso, corrija o desempenho do sistema e, em seguida, colete novamente dados do KHI e garanta a integridade do sistema antes de examinar as métricas específicas da função do servidor na implementação do Lync.</span><span class="sxs-lookup"><span data-stu-id="e8b87-140">If they do not, remediate the system performance then re-collect KHI data and ensure system health before looking at the metrics specific to the server’s role in the Lync implementation.</span></span> <span data-ttu-id="e8b87-141">A integridade do componente para todas as funções é definida como:</span><span class="sxs-lookup"><span data-stu-id="e8b87-141">Component health for all roles is defined as:</span></span>

  - <span data-ttu-id="e8b87-142">Utilização da CPU \< 80%</span><span class="sxs-lookup"><span data-stu-id="e8b87-142">CPU Utilization \< 80%</span></span>

  - <span data-ttu-id="e8b87-143">Média de gravação em disco \< 10 ms</span><span class="sxs-lookup"><span data-stu-id="e8b87-143">Avg. Disk Write \< 10 ms</span></span>

  - <span data-ttu-id="e8b87-144">Média de leitura de disco \< 10 ms</span><span class="sxs-lookup"><span data-stu-id="e8b87-144">Avg. Disk Read \< 10 ms</span></span>

  - <span data-ttu-id="e8b87-145">Memória disponível de \> 20% do total de sistema em MB</span><span class="sxs-lookup"><span data-stu-id="e8b87-145">Available memory \>20% System Total MB</span></span>

  - <span data-ttu-id="e8b87-146">Comprimento da fila de rede \< 2</span><span class="sxs-lookup"><span data-stu-id="e8b87-146">Network Queue Length \< 2</span></span>

  - <span data-ttu-id="e8b87-147">Pacotes descartados (in/out) = 0</span><span class="sxs-lookup"><span data-stu-id="e8b87-147">Discarded Packets (in / out) = 0</span></span>

</div>

<span id="Glossary"></span>

<div>

## <a name="glossary"></a><span data-ttu-id="e8b87-148">Glossário</span><span class="sxs-lookup"><span data-stu-id="e8b87-148">Glossary</span></span>

<span data-ttu-id="e8b87-149">Os termos e acrônimos a seguir são usados neste cartaz:</span><span class="sxs-lookup"><span data-stu-id="e8b87-149">The following terms and acronyms are used in this poster:</span></span>

<span data-ttu-id="e8b87-150">Como MCU = unidade de controle de vários pontos do compartilhamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="e8b87-150">AS MCU = Application Sharing Multi-point Control Unit</span></span>

<span data-ttu-id="e8b87-151">AV MCU = áudio/vídeo MCU</span><span class="sxs-lookup"><span data-stu-id="e8b87-151">AV MCU = Audio/Video MCU</span></span>

<span data-ttu-id="e8b87-152">MENSAGEM instantânea MCU = mensagem instantânea MCU</span><span class="sxs-lookup"><span data-stu-id="e8b87-152">IM MCU = Instant Messaging MCU</span></span>

<span data-ttu-id="e8b87-153">UCWA = API Web de comunicação unificada</span><span class="sxs-lookup"><span data-stu-id="e8b87-153">UCWA = Unified Communications Web API</span></span>

<span data-ttu-id="e8b87-154">Borda de AV = travessia de áudio/vídeo via Edge</span><span class="sxs-lookup"><span data-stu-id="e8b87-154">AV Edge = Traversal of audio/video via edge</span></span>

<span data-ttu-id="e8b87-155">Autenticação de AV auth = áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="e8b87-155">AV Auth = Audio/Video Authentication</span></span>

<span data-ttu-id="e8b87-156">Pilha SIP = contém a implementação principal SIP do Lync</span><span class="sxs-lookup"><span data-stu-id="e8b87-156">SIP Stack = Contains Lync’s core SIP implementation</span></span>

<span data-ttu-id="e8b87-157">Proxy de dados = usado para a conferência de borda</span><span class="sxs-lookup"><span data-stu-id="e8b87-157">Data Proxy = Used for edge conferencing</span></span>

<span data-ttu-id="e8b87-158">LySS = serviço de armazenamento do Lync</span><span class="sxs-lookup"><span data-stu-id="e8b87-158">LySS = Lync Storage Service</span></span>

</div>

<span id="Front"></span>

<div>

## <a name="front-end-servers"></a><span data-ttu-id="e8b87-159">Servidores front-end</span><span class="sxs-lookup"><span data-stu-id="e8b87-159">Front-end Servers</span></span>

<span data-ttu-id="e8b87-160">Os seguintes destinos de KHI recomendados são específicos para servidores front-end, além da integridade básica do componente:</span><span class="sxs-lookup"><span data-stu-id="e8b87-160">The following recommended KHI targets are specific to front-end servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8b87-161">Área funcional</span><span class="sxs-lookup"><span data-stu-id="e8b87-161">Functional area</span></span></th>
<th><span data-ttu-id="e8b87-162">Métricas de destino</span><span class="sxs-lookup"><span data-stu-id="e8b87-162">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8b87-163">AS/AV/IM MCU</span><span class="sxs-lookup"><span data-stu-id="e8b87-163">AS/AV/IM MCU</span></span></p></td>
<td><p><span data-ttu-id="e8b87-164">Estado de integridade do MCU &lt; 2</span><span class="sxs-lookup"><span data-stu-id="e8b87-164">MCU Health State &lt;2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8b87-165">Componentes da Web</span><span class="sxs-lookup"><span data-stu-id="e8b87-165">Web Components</span></span></p></td>
<td><p><span data-ttu-id="e8b87-166">Tempo limite do anúncio de expansão da lista de distribuição &lt; 0</span><span class="sxs-lookup"><span data-stu-id="e8b87-166">Distribution List expansion AD timeouts &lt;0</span></span></p>
<p><span data-ttu-id="e8b87-167">Falhas de ABWQ = 0</span><span class="sxs-lookup"><span data-stu-id="e8b87-167">ABWQ failures = 0</span></span></p>
<p><span data-ttu-id="e8b87-168">Falhas de LIS = 0</span><span class="sxs-lookup"><span data-stu-id="e8b87-168">LIS failures = 0</span></span></p>
<p><span data-ttu-id="e8b87-169">Erros de autenticação &lt; 1/s</span><span class="sxs-lookup"><span data-stu-id="e8b87-169">Authentication Errors &lt; 1/sec</span></span></p>
<p><span data-ttu-id="e8b87-170">ASP.NET de solicitações v4 rejeitadas = 0</span><span class="sxs-lookup"><span data-stu-id="e8b87-170">ASP.NET v4 Requests Rejected = 0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8b87-171">Pilha SIP</span><span class="sxs-lookup"><span data-stu-id="e8b87-171">SIP Stack</span></span></p></td>
<td><p><span data-ttu-id="e8b87-172">Média de processamento de mensagens de entrada &lt; 1 s</span><span class="sxs-lookup"><span data-stu-id="e8b87-172">Avg. Incoming Message Processing &lt; 1 sec</span></span></p>
<p><span data-ttu-id="e8b87-173">Respostas de entrada ignoradas &lt; 1/s solicitações de entrada ignoradas &lt; 1/s</span><span class="sxs-lookup"><span data-stu-id="e8b87-173">Incoming Responses Dropped &lt; 1/sec Incoming Requests Dropped &lt; 1/sec</span></span></p>
<p><span data-ttu-id="e8b87-174">Latência da fila &lt; 100 ms</span><span class="sxs-lookup"><span data-stu-id="e8b87-174">Queue Latency &lt; 100 ms</span></span></p>
<p><span data-ttu-id="e8b87-175">SPROC latência de &lt; 100 ms</span><span class="sxs-lookup"><span data-stu-id="e8b87-175">Sproc Latency &lt; 100 ms</span></span></p>
<p><span data-ttu-id="e8b87-176">Solicitações limitadas = 0</span><span class="sxs-lookup"><span data-stu-id="e8b87-176">Throttled Requests = 0</span></span></p>
<p><span data-ttu-id="e8b87-177">Erros de autenticação &lt; 1/s</span><span class="sxs-lookup"><span data-stu-id="e8b87-177">Authentication Errors &lt; 1/sec</span></span></p>
<p><span data-ttu-id="e8b87-178">O tempo limite das mensagens de entrada expirou &lt; 2</span><span class="sxs-lookup"><span data-stu-id="e8b87-178">Incoming Messages Timed Out &lt; 2</span></span></p>
<p><span data-ttu-id="e8b87-179">Média de mensagens de entrada em espera de &lt; 1 s</span><span class="sxs-lookup"><span data-stu-id="e8b87-179">Avg. Incoming Message Hold &lt; 1 sec</span></span></p>
<p><span data-ttu-id="e8b87-180">Conexões controladas de fluxo &lt; 2</span><span class="sxs-lookup"><span data-stu-id="e8b87-180">Flow Controlled Connections &lt; 2</span></span></p>
<p><span data-ttu-id="e8b87-181">Média de atraso da fila de out &lt; 2 segundos</span><span class="sxs-lookup"><span data-stu-id="e8b87-181">Avg. Out Queue Delay &lt; 2 sec</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8b87-182">LySS</span><span class="sxs-lookup"><span data-stu-id="e8b87-182">LySS</span></span></p></td>
<td><p><span data-ttu-id="e8b87-183">% do espaço usado pelo serviço de armazenamento DB &lt; 80</span><span class="sxs-lookup"><span data-stu-id="e8b87-183">% of space used by Storage Service DB &lt; 80</span></span></p>
<p><span data-ttu-id="e8b87-184"># de falhas de replicação de réplica = 0</span><span class="sxs-lookup"><span data-stu-id="e8b87-184"># of replica replication failures = 0</span></span></p>
<p><span data-ttu-id="e8b87-185"># de eventos de perda de dados = 0</span><span class="sxs-lookup"><span data-stu-id="e8b87-185"># of data loss events = 0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8b87-186">Server</span><span class="sxs-lookup"><span data-stu-id="e8b87-186">SQL</span></span></p></td>
<td><p><span data-ttu-id="e8b87-187">Expectativa de vida da página de &gt; 300 segundos.</span><span class="sxs-lookup"><span data-stu-id="e8b87-187">Page life expectancy &gt; 300 Sec.</span></span></p>
<p><span data-ttu-id="e8b87-188">Solicitações em lote/s &lt; 2500</span><span class="sxs-lookup"><span data-stu-id="e8b87-188">Batch requests / sec &lt; 2500</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="BackEnd"></span>

<div>

## <a name="backend-sql-servers"></a><span data-ttu-id="e8b87-189">Servidores SQL back-end</span><span class="sxs-lookup"><span data-stu-id="e8b87-189">Backend SQL Servers</span></span>

<span data-ttu-id="e8b87-190">Os seguintes destinos KHI recomendados são específicos dos SQL Servers, além da integridade básica do componente:</span><span class="sxs-lookup"><span data-stu-id="e8b87-190">The following recommended KHI targets are specific to SQL servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8b87-191">Área funcional</span><span class="sxs-lookup"><span data-stu-id="e8b87-191">Functional area</span></span></th>
<th><span data-ttu-id="e8b87-192">Métricas de destino</span><span class="sxs-lookup"><span data-stu-id="e8b87-192">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8b87-193">Server</span><span class="sxs-lookup"><span data-stu-id="e8b87-193">SQL</span></span></p></td>
<td><p><span data-ttu-id="e8b87-194">Expectativa de vida da página de &gt; 300 segundos.</span><span class="sxs-lookup"><span data-stu-id="e8b87-194">Page life expectancy &gt; 300 Sec.</span></span></p>
<p><span data-ttu-id="e8b87-195">Solicitações em lote/s &lt; 2500</span><span class="sxs-lookup"><span data-stu-id="e8b87-195">Batch requests / sec &lt; 2500</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="Mediation"></span>

<div>

## <a name="mediation-servers"></a><span data-ttu-id="e8b87-196">Servidores de Mediação</span><span class="sxs-lookup"><span data-stu-id="e8b87-196">Mediation Servers</span></span>

<span data-ttu-id="e8b87-197">Os seguintes destinos de KHI recomendados são específicos para servidores de mediação além da integridade básica do componente:</span><span class="sxs-lookup"><span data-stu-id="e8b87-197">The following recommended KHI targets are specific to mediation servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8b87-198">Área funcional</span><span class="sxs-lookup"><span data-stu-id="e8b87-198">Functional area</span></span></th>
<th><span data-ttu-id="e8b87-199">Métricas de destino</span><span class="sxs-lookup"><span data-stu-id="e8b87-199">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8b87-200">Serviço do servidor de mediação</span><span class="sxs-lookup"><span data-stu-id="e8b87-200">Mediation Server Service</span></span></p></td>
<td><p><span data-ttu-id="e8b87-201">Índice de falha na chamada de carga = 0</span><span class="sxs-lookup"><span data-stu-id="e8b87-201">Load Call Failure Index = 0</span></span></p>
<p><span data-ttu-id="e8b87-202">Chamadas com falha devido ao proxy &lt; 10</span><span class="sxs-lookup"><span data-stu-id="e8b87-202">Failed Calls due to Proxy &lt;10</span></span></p>
<p><span data-ttu-id="e8b87-203">Chamadas com falha devido ao gateway &lt; 10</span><span class="sxs-lookup"><span data-stu-id="e8b87-203">Failed Calls due to Gateway &lt;10</span></span></p>
<p><span data-ttu-id="e8b87-204">Chamadas (in ou out) rejeitadas = 0</span><span class="sxs-lookup"><span data-stu-id="e8b87-204">Calls (in or out) rejected = 0</span></span></p>
<p><span data-ttu-id="e8b87-205">Candidatos à mídia ausentes = 0</span><span class="sxs-lookup"><span data-stu-id="e8b87-205">Media Candidates missing = 0</span></span></p>
<p><span data-ttu-id="e8b87-206">Falhas de verificação de conectividade de mídia = 0</span><span class="sxs-lookup"><span data-stu-id="e8b87-206">Media Connectivity Check Failures = 0</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="Edge"></span>

<div>

## <a name="edge-servers"></a><span data-ttu-id="e8b87-207">Servidores de Borda</span><span class="sxs-lookup"><span data-stu-id="e8b87-207">Edge Servers</span></span>

<span data-ttu-id="e8b87-208">Os seguintes destinos de KHI recomendados são específicos para servidores de borda além da integridade básica do componente:</span><span class="sxs-lookup"><span data-stu-id="e8b87-208">The following recommended KHI targets are specific to edge servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8b87-209">Área funcional</span><span class="sxs-lookup"><span data-stu-id="e8b87-209">Functional area</span></span></th>
<th><span data-ttu-id="e8b87-210">Métricas de destino</span><span class="sxs-lookup"><span data-stu-id="e8b87-210">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8b87-211">Autenticação por AV</span><span class="sxs-lookup"><span data-stu-id="e8b87-211">AV Auth</span></span></p></td>
<td><p><span data-ttu-id="e8b87-212">Solicitações incorretas &lt; 20/s</span><span class="sxs-lookup"><span data-stu-id="e8b87-212">Bad Requests &lt; 20/sec</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8b87-213">Borda de AV</span><span class="sxs-lookup"><span data-stu-id="e8b87-213">AV Edge</span></span></p></td>
<td><p><span data-ttu-id="e8b87-214">Erros de autenticação &lt; 20/s</span><span class="sxs-lookup"><span data-stu-id="e8b87-214">Auth. Failures &lt;20/sec</span></span></p>
<p><span data-ttu-id="e8b87-215">Falhas de alocação &lt; 20/s</span><span class="sxs-lookup"><span data-stu-id="e8b87-215">Allocation Failures &lt;20/sec</span></span></p>
<p><span data-ttu-id="e8b87-216">Pacotes ignorados &lt; 300/s</span><span class="sxs-lookup"><span data-stu-id="e8b87-216">Packets Dropped &lt;300/sec</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8b87-217">Proxy de dados</span><span class="sxs-lookup"><span data-stu-id="e8b87-217">Data Proxy</span></span></p></td>
<td><p><span data-ttu-id="e8b87-218">Conexões de servidor limitada &lt; 3</span><span class="sxs-lookup"><span data-stu-id="e8b87-218">Throttled Server connections &lt; 3</span></span></p>
<p><span data-ttu-id="e8b87-219">O sistema está limitando &lt; 1</span><span class="sxs-lookup"><span data-stu-id="e8b87-219">System is Throttling &lt;1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8b87-220">Pilha SIP</span><span class="sxs-lookup"><span data-stu-id="e8b87-220">SIP Stack</span></span></p></td>
<td><p><span data-ttu-id="e8b87-221">Conexões com limite ignorado &lt; 1</span><span class="sxs-lookup"><span data-stu-id="e8b87-221">Connections over limit dropped &lt; 1</span></span></p>
<p><span data-ttu-id="e8b87-222">Envios com tempo limite de &lt; 10</span><span class="sxs-lookup"><span data-stu-id="e8b87-222">Sends timed out &lt;10</span></span></p>
<p><span data-ttu-id="e8b87-223">Conexões controladas de fluxo &lt; 100</span><span class="sxs-lookup"><span data-stu-id="e8b87-223">Flow Controlled Connections &lt;100</span></span></p>
<p><span data-ttu-id="e8b87-224">Solicitações de entrada ignoradas &lt; 1/s</span><span class="sxs-lookup"><span data-stu-id="e8b87-224">Incoming requests dropped &lt; 1/sec</span></span></p>
<p><span data-ttu-id="e8b87-225">Média de processamento de mensagens &lt; 3 segundos</span><span class="sxs-lookup"><span data-stu-id="e8b87-225">Avg. Message Processing &lt; 3 sec</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e8b87-226">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8b87-226">See Also</span></span>


[<span data-ttu-id="e8b87-227">Guia de rede do Lync Server</span><span class="sxs-lookup"><span data-stu-id="e8b87-227">Lync Server Networking Guide</span></span>](https://go.microsoft.com/fwlink/p/?linkid=390677)  
[<span data-ttu-id="e8b87-228">Principais indicadores de integridade: a base para a manutenção de servidores de Lync saudáveis</span><span class="sxs-lookup"><span data-stu-id="e8b87-228">Key Health Indicators: The Foundation for Maintaining Healthy Lync Servers</span></span>](https://go.microsoft.com/fwlink/?linkid=391838)  
[<span data-ttu-id="e8b87-229">Metodologia de qualidade de chamada do Lync</span><span class="sxs-lookup"><span data-stu-id="e8b87-229">Lync Call Quality Methodology</span></span>](https://go.microsoft.com/fwlink/?linkid=391841)  
  

<span data-ttu-id="e8b87-230"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e8b87-230"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

