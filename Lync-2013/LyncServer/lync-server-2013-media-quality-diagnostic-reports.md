---
title: 'Lync Server 2013: relatórios de diagnóstico de qualidade de mídia'
description: 'Lync Server 2013: relatórios de diagnóstico de qualidade de mídia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Diagnostic Reports
ms:assetid: ea61428e-a1d5-4189-aae6-3db19ddc5cf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615044(v=OCS.15)
ms:contentKeyID: 48185935
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2e346d0f9b8997158cb926ad830d5477950e846d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390394"
---
# <a name="media-quality-diagnostic-reports-in-lync-server-2013"></a><span data-ttu-id="48794-103">Relatórios de diagnóstico de qualidade de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="48794-103">Media Quality Diagnostic Reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="48794-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="48794-104">

<span> </span></span></span>

<span data-ttu-id="48794-105">_**Tópico da última modificação:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="48794-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="48794-106">Os Relatórios de Diagnóstico de Qualidade de Mídia oferecem informações sobre a qualidade de chamadas, sobre diagnóstico e sobre solução de problemas para chamadas com falhas.</span><span class="sxs-lookup"><span data-stu-id="48794-106">The Media Quality Diagnostic Reports provide information about call quality, and diagnostic and troubleshooting information for failed calls.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="48794-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="48794-107">In This Section</span></span>

  - <span data-ttu-id="48794-108">[Relatório de Resumo de qualidade de mídia no Lync Server 2013](lync-server-2013-media-quality-summary-report.md)   Fornece dados de qualidade gerais para diferentes tipos de ponto de extremidade, incluindo chamadas ponto a ponto do Enterprise Voice, chamadas de conferência do Enterprise Voice e chamadas que dependem, pelo menos em parte, na rede telefônica pública comutada (PSTN).</span><span class="sxs-lookup"><span data-stu-id="48794-108">[Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md)   Provides overall quality data for different endpoint types, including Enterprise Voice peer-to-peer calls, Enterprise Voice conference calls, and calls that rely, at least in part, on the public switched telephone network (PSTN).</span></span>

  - <span data-ttu-id="48794-109">[Relatório de comparação de qualidade de mídia no Lync Server 2013](lync-server-2013-media-quality-comparison-report.md)   Fornece uma comparação de valores de qualidade de chamada para diferentes tipos de chamadas de áudio (por exemplo, chamadas feitas em uma rede sem fio versus chamadas feitas em uma conexão com fio).</span><span class="sxs-lookup"><span data-stu-id="48794-109">[Media Quality Comparison Report in Lync Server 2013](lync-server-2013-media-quality-comparison-report.md)   Provides a comparison of call quality values for different types of audio calls (for example, calls made over a wireless network vs. calls made across a wired connection).</span></span>

  - <span data-ttu-id="48794-110">[Relatório de desempenho do servidor no Lync Server 2013](lync-server-2013-server-performance-report.md)   Lista os servidores que falharam na maioria dos problemas, com base em medidas de métricas de qualidade chave como degradação, perda de pacote e Tremulação.</span><span class="sxs-lookup"><span data-stu-id="48794-110">[Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md)   Lists the servers that have experienced the most problems, based on measurements of such key quality metrics as degradation, packet loss, and jitter.</span></span>

  - <span data-ttu-id="48794-111">[Relatório de localização no Lync Server 2013](lync-server-2013-location-report.md)   Fornece uma lista de locais de rede e um resumo da qualidade da mídia das chamadas que ocorrem em cada local.</span><span class="sxs-lookup"><span data-stu-id="48794-111">[Location Report in Lync Server 2013](lync-server-2013-location-report.md)   Provides a list of network locations and a summary of the media quality of the calls that occur at each location.</span></span> <span data-ttu-id="48794-112">Para este relatório, os locais se baseiam em sub-redes IP.</span><span class="sxs-lookup"><span data-stu-id="48794-112">For purposes of this report, locations are based on IP subnets.</span></span>

  - <span data-ttu-id="48794-113">[Relatório de dispositivo no Lync Server 2013](lync-server-2013-device-report.md)   Fornece um resumo dos dispositivos que são usados para chamadas do Enterprise Voice e inclui a qualidade média da mídia das chamadas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48794-113">[Device Report in Lync Server 2013](lync-server-2013-device-report.md)   Provides a summary of devices that are used for Enterprise Voice calls and it includes the average media quality of the calls by device.</span></span>

  - <span data-ttu-id="48794-114">[Relatório de lista de chamadas no Lync Server 2013](lync-server-2013-call-list-report.md)   Fornece informações detalhadas sobre chamadas telefônicas feitas ou recebidas em sua organização.</span><span class="sxs-lookup"><span data-stu-id="48794-114">[Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md)   Provides detailed information about phone calls made or received within your organization.</span></span>

  - <span data-ttu-id="48794-115">[Relatório de detalhes da chamada no Lync Server 2013](lync-server-2013-call-detail-report.md)   Fornece informações detalhadas sobre chamadas telefônicas feitas ou recebidas dentro da sua organização.</span><span class="sxs-lookup"><span data-stu-id="48794-115">[Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md)   Provides detailed information about phone calls made from or received within your organization.</span></span>

  - <span data-ttu-id="48794-116">[Relatório de tendências de qualidade de mídia do servidor no Lync Server 2013](lync-server-2013-server-media-quality-trend-report.md)   Fornece uma maneira de comparar graficamente até cinco servidores com métricas de qualidade de experiência, como volume de chamadas, porcentagem de chamadas deficientes, perda de pacotes e Tremulação.</span><span class="sxs-lookup"><span data-stu-id="48794-116">[Server Media Quality Trend Report in Lync Server 2013](lync-server-2013-server-media-quality-trend-report.md)   Provides a way for you to graphically compare up to 5 servers on Quality of Experience metrics such as call volume, poor call percentage, packet loss, and jitter.</span></span>

  - <span data-ttu-id="48794-117">[O relatório de distribuição de métricas de qualidade de mídia no Lync Server 2013](lync-server-2013-media-quality-metrics-distribution-report.md)   Fornece um gráfico que mostra os valores de distribuição para uma métrica de qualidade de experiência, como tremulação ou perda de pacote.</span><span class="sxs-lookup"><span data-stu-id="48794-117">[The Media Quality Metrics Distribution Report in Lync Server 2013](lync-server-2013-media-quality-metrics-distribution-report.md)   Provides a graph that shows the distribution values for a Quality of Experience metric such as jitter or packet loss.</span></span>

  - <span data-ttu-id="48794-118">[Relatório de tendências de localização no Lync Server 2013](lync-server-2013-location-trend-report.md)   Fornece informações de tendência de qualidade de chamada para locais de rede.</span><span class="sxs-lookup"><span data-stu-id="48794-118">[Location Trend Report in Lync Server 2013](lync-server-2013-location-trend-report.md)   Provides call quality trend information for network locations.</span></span>

<span data-ttu-id="48794-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="48794-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

