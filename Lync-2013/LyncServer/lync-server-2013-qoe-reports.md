---
title: 'Lync Server 2013: relatórios de QoE'
description: 'Lync Server 2013: relatórios de QoE.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: QoE reports
ms:assetid: 49c827af-b8dd-4c6e-b0dc-b4bc6d60e9a3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720913(v=OCS.15)
ms:contentKeyID: 63969601
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 55965d246b7f0ddd71eaeeec99d218eaf8819c2e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390055"
---
# <a name="qoe-reports-in-lync-server-2013"></a><span data-ttu-id="19e82-103">Relatórios de QoE no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="19e82-103">QoE reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19e82-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19e82-104">

<span> </span></span></span>

<span data-ttu-id="19e82-105">_**Tópico da última modificação:** 2014-05-01_</span><span class="sxs-lookup"><span data-stu-id="19e82-105">_**Topic Last Modified:** 2014-05-01_</span></span>

<div>

## <a name="qoe-summarytrend-reports"></a><span data-ttu-id="19e82-106">Relatórios de resumo/tendências de QoE</span><span class="sxs-lookup"><span data-stu-id="19e82-106">QoE summary/trend reports</span></span>

<span data-ttu-id="19e82-107">Os relatórios de resumo/tendências de QoE são úteis para encontrar os períodos de pico de uso do dia e examinar a qualidade da mídia durante esses horários para ajudar a garantir que os recursos de rede da sua organização sejam suficientes.</span><span class="sxs-lookup"><span data-stu-id="19e82-107">The QoE summary/trends reports are useful for finding the peak usage times of day and examining the media quality during those times to help assure that your organization's network resources are sufficient.</span></span> <span data-ttu-id="19e82-108">Sua organização também pode usar os vários filtros disponíveis no relatório para isolar números de desempenho de certos locais, tipos de cliente e dispositivos e servidores.</span><span class="sxs-lookup"><span data-stu-id="19e82-108">Your organization can also use the many filters available in the report to isolate performance numbers for certain locations, client and device types, and servers.</span></span>

<span data-ttu-id="19e82-109">Relatórios de resumo/tendências de QoE consistem em:</span><span class="sxs-lookup"><span data-stu-id="19e82-109">QoE summary/trend reports consist of:</span></span>

  - <span data-ttu-id="19e82-110">Relatório de Resumo de UC para UC/tendências</span><span class="sxs-lookup"><span data-stu-id="19e82-110">UC-to-UC Summary/Trend Report</span></span>

  - <span data-ttu-id="19e82-111">Relatório de resumo/tendência PSTN</span><span class="sxs-lookup"><span data-stu-id="19e82-111">PSTN Summary/Trend Report</span></span>

  - <span data-ttu-id="19e82-112">Relatório Resumo da Conferência/resumo de tendências</span><span class="sxs-lookup"><span data-stu-id="19e82-112">Conference Summary/Trend Report</span></span>

</div>

<div>

## <a name="qoe-performance-reports"></a><span data-ttu-id="19e82-113">Relatórios de desempenho de QoE</span><span class="sxs-lookup"><span data-stu-id="19e82-113">QoE performance reports</span></span>

<span data-ttu-id="19e82-114">Relatórios de desempenho de QoE fornecem detalhes sobre os três relatórios que se concentram no desempenho do QoE de servidores de mediação a/V e em locais de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="19e82-114">QoE performance reports provide details about the three reports that concentrate on the QoE performance of Mediation Servers, A/V Conferencing Servers, and endpoint locations.</span></span>

</div>

<div>

## <a name="mediation-server-performance-report"></a><span data-ttu-id="19e82-115">Relatório de desempenho do servidor de mediação</span><span class="sxs-lookup"><span data-stu-id="19e82-115">Mediation server performance report</span></span>

<span data-ttu-id="19e82-116">O relatório de desempenho do servidor de mediação lista as métricas obtidas por uma ou mais mediação durante o período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="19e82-116">The Mediation Server Performance report lists the metrics achieved by one or more Mediation during the specified time period.</span></span> <span data-ttu-id="19e82-117">As métricas do trecho do servidor de comunicação unificada (UC) para o servidor de mediação e o trecho do servidor de mediação para gateway de cada chamada são reportados separadamente.</span><span class="sxs-lookup"><span data-stu-id="19e82-117">The metrics for the unified communications (UC)-to-Mediation Server leg and the Mediation Server-to-Gateway leg of each call are reported separately.</span></span> <span data-ttu-id="19e82-118">Use esse relatório para comparar o volume e o desempenho dos vários servidores de mediação da sua organização.</span><span class="sxs-lookup"><span data-stu-id="19e82-118">Use this report to compare the volume and performance of your organization's various Mediation Servers.</span></span>

<span data-ttu-id="19e82-119">Para cada servidor de mediação (e para cada segmento de chamada), o relatório exibe o seguinte:</span><span class="sxs-lookup"><span data-stu-id="19e82-119">For each Mediation Server (and for each call leg), the report displays the following:</span></span>

  - <span data-ttu-id="19e82-120">Número de chamadas</span><span class="sxs-lookup"><span data-stu-id="19e82-120">Number of calls</span></span>

  - <span data-ttu-id="19e82-121">Perda de pacote</span><span class="sxs-lookup"><span data-stu-id="19e82-121">Packet Loss</span></span>

  - <span data-ttu-id="19e82-122">Tempo de viagem de ida e volta</span><span class="sxs-lookup"><span data-stu-id="19e82-122">Round Trip Time</span></span>

  - <span data-ttu-id="19e82-123">Tremulação</span><span class="sxs-lookup"><span data-stu-id="19e82-123">Jitter</span></span>

  - <span data-ttu-id="19e82-124">Pontuação média de opinião de conversa (MOS)</span><span class="sxs-lookup"><span data-stu-id="19e82-124">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="19e82-125">Como enviar MOS</span><span class="sxs-lookup"><span data-stu-id="19e82-125">Sending MOS</span></span>

  - <span data-ttu-id="19e82-126">MOS ouvindo</span><span class="sxs-lookup"><span data-stu-id="19e82-126">Listening MOS</span></span>

  - <span data-ttu-id="19e82-127">MOS de rede</span><span class="sxs-lookup"><span data-stu-id="19e82-127">Network MOS</span></span>

  - <span data-ttu-id="19e82-128">Degradação de MOS de rede</span><span class="sxs-lookup"><span data-stu-id="19e82-128">Network MOS Degradation</span></span>

  - <span data-ttu-id="19e82-129">Retorno de eco</span><span class="sxs-lookup"><span data-stu-id="19e82-129">Echo Return</span></span>

  - <span data-ttu-id="19e82-130">Nível do sinal</span><span class="sxs-lookup"><span data-stu-id="19e82-130">Signal Level</span></span>

</div>

<div>

## <a name="av-conferencing-server-performance-report"></a><span data-ttu-id="19e82-131">Relatório de desempenho do servidor de conferência A/V</span><span class="sxs-lookup"><span data-stu-id="19e82-131">A/V conferencing server performance report</span></span>

<span data-ttu-id="19e82-132">O relatório de desempenho do servidor de conferência A/V fornece listas de métricas obtidas por um ou mais servidores de conferência A/V durante o período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="19e82-132">The A/V Conferencing Server Performance report provides lists of metrics achieved by one or more A/V Conferencing Servers during the specified time period.</span></span> <span data-ttu-id="19e82-133">Esse relatório pode ser usado para comparar o volume e o desempenho dos vários servidores de conferência A/V da sua organização.</span><span class="sxs-lookup"><span data-stu-id="19e82-133">This report can be used to compare the volume and performance of your organization’s various A/V Conferencing Servers.</span></span> <span data-ttu-id="19e82-134">Sua organização também pode isolar o relatório para mostrar apenas a experiência de tipos específicos de cliente, como clientes do Lync ou clientes PSTN.</span><span class="sxs-lookup"><span data-stu-id="19e82-134">Your organization can also isolate the report to show only the experience for specific client types, such as Lync clients or PSTN clients.</span></span>

<span data-ttu-id="19e82-135">Para cada servidor de conferência A/V, o relatório exibe o seguinte:</span><span class="sxs-lookup"><span data-stu-id="19e82-135">For each A/V Conferencing Server, the report displays the following:</span></span>

  - <span data-ttu-id="19e82-136">Número de conferências</span><span class="sxs-lookup"><span data-stu-id="19e82-136">Number of conferences</span></span>

  - <span data-ttu-id="19e82-137">Perda de pacote</span><span class="sxs-lookup"><span data-stu-id="19e82-137">Packet Loss</span></span>

  - <span data-ttu-id="19e82-138">Tempo de viagem de ida e volta</span><span class="sxs-lookup"><span data-stu-id="19e82-138">Round Trip Time</span></span>

  - <span data-ttu-id="19e82-139">Tremulação</span><span class="sxs-lookup"><span data-stu-id="19e82-139">Jitter</span></span>

  - <span data-ttu-id="19e82-140">Pontuação média de opinião de conversa (MOS)</span><span class="sxs-lookup"><span data-stu-id="19e82-140">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="19e82-141">Como enviar MOS</span><span class="sxs-lookup"><span data-stu-id="19e82-141">Sending MOS</span></span>

  - <span data-ttu-id="19e82-142">MOS ouvindo</span><span class="sxs-lookup"><span data-stu-id="19e82-142">Listening MOS</span></span>

  - <span data-ttu-id="19e82-143">MOS de rede</span><span class="sxs-lookup"><span data-stu-id="19e82-143">Network MOS</span></span>

  - <span data-ttu-id="19e82-144">Degradação de MOS de rede</span><span class="sxs-lookup"><span data-stu-id="19e82-144">Network MOS Degradation</span></span>

  - <span data-ttu-id="19e82-145">Retorno de eco</span><span class="sxs-lookup"><span data-stu-id="19e82-145">Echo Return</span></span>

  - <span data-ttu-id="19e82-146">Nível do sinal</span><span class="sxs-lookup"><span data-stu-id="19e82-146">Signal Level</span></span>

</div>

<div>

## <a name="location-based-performance-report"></a><span data-ttu-id="19e82-147">Relatório de desempenho baseado em local</span><span class="sxs-lookup"><span data-stu-id="19e82-147">Location-based performance report</span></span>

<span data-ttu-id="19e82-148">O relatório de desempenho Location-Based fornece uma lista de locais de rede e para cada local mostra o número de chamadas em cada intervalo de qualidade predeterminado.</span><span class="sxs-lookup"><span data-stu-id="19e82-148">The Location-Based Performance report provides a list of network locations and for each location shows the number of calls in each pre-determined range of quality.</span></span> <span data-ttu-id="19e82-149">O objetivo deste relatório é fornecer uma visão geral da qualidade da mídia do maior volume de chamadas telefônicas da sua organização para vários locais, de modo que você possa identificar locais mal satisfatórios e ver as diferentes classificações de qualidade da mídia nos diferentes locais da sua organização.</span><span class="sxs-lookup"><span data-stu-id="19e82-149">The goal of this report is to provide insight into the media quality of the bulk of your organization’s telephone calls for various locations so that you can identify poorly performing locations, and see the different grades of media quality in your organization’s different locations.</span></span>

<span data-ttu-id="19e82-150">Ao exibir o relatório, diferentes tabelas de métricas são exibidas — uma tabela para cada métrica à qual sua organização decide se reportar.</span><span class="sxs-lookup"><span data-stu-id="19e82-150">When displaying the report, different tables of metrics appear—one table for each metric your organization decides to report on.</span></span> <span data-ttu-id="19e82-151">Você pode escolher entre as seguintes métricas deste relatório:</span><span class="sxs-lookup"><span data-stu-id="19e82-151">You can choose from the following metrics for this report:</span></span>

  - <span data-ttu-id="19e82-152">Pontuação média de opinião de conversa (MOS)</span><span class="sxs-lookup"><span data-stu-id="19e82-152">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="19e82-153">MOS de rede</span><span class="sxs-lookup"><span data-stu-id="19e82-153">Network MOS</span></span>

  - <span data-ttu-id="19e82-154">Degradação de MOS de rede</span><span class="sxs-lookup"><span data-stu-id="19e82-154">Network MOS Degradation</span></span>

  - <span data-ttu-id="19e82-155">Como enviar MOS</span><span class="sxs-lookup"><span data-stu-id="19e82-155">Sending MOS</span></span>

  - <span data-ttu-id="19e82-156">MOS ouvindo</span><span class="sxs-lookup"><span data-stu-id="19e82-156">Listening MOS</span></span>

  - <span data-ttu-id="19e82-157">Perda de pacote</span><span class="sxs-lookup"><span data-stu-id="19e82-157">Packet Loss</span></span>

  - <span data-ttu-id="19e82-158">Tremulação</span><span class="sxs-lookup"><span data-stu-id="19e82-158">Jitter</span></span>

  - <span data-ttu-id="19e82-159">Latência</span><span class="sxs-lookup"><span data-stu-id="19e82-159">Latency</span></span>

<span data-ttu-id="19e82-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="19e82-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

