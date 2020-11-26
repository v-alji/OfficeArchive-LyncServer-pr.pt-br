---
title: 'Lync Server 2013: Configurando o serviço de mobilidade para alto desempenho'
description: 'Lync Server 2013: Configurando o serviço de mobilidade para alto desempenho.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Mobility Service for high performance
ms:assetid: c2b8aadb-cffb-49f0-ba7a-e8541a1ff475
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690042(v=OCS.15)
ms:contentKeyID: 48185332
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4732d9f6a92c383a105a6f0d7162c9b6c798de24
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432881"
---
# <a name="configuring-mobility-service-for-high-performance-in-lync-server-2013"></a><span data-ttu-id="d5492-103">Configurando o serviço de mobilidade para alto desempenho no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d5492-103">Configuring Mobility Service for high performance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d5492-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d5492-104">

<span> </span></span></span>

<span data-ttu-id="d5492-105">_**Tópico da última modificação:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="d5492-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d5492-106">Este tópico se aplica apenas ao serviço de mobilidade do Lync Server 2013 (MCX) e não se aplica à API da Web de comunicação unificada (UCWA), conforme entregue nas atualizações cumulativas do Lync Server 2013:2013 de fevereiro.</span><span class="sxs-lookup"><span data-stu-id="d5492-106">This topic applies only to the Lync Server 2013 Mobility Service (Mcx), and does not apply to Unified Communications Web API (UCWA), as delivered in the Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

<span data-ttu-id="d5492-107">Quando você instala o serviço de mobilidade (MCX) em serviços de informações da Internet (IIS) 7,5, o instalador do serviço de mobilidade configura algumas configurações de desempenho no servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="d5492-107">When you install the Mobility Service (Mcx) on Internet Information Services (IIS) 7.5, the Mobility Service installer configures some performance settings on the Front End Server.</span></span> <span data-ttu-id="d5492-108">Recomendamos usar IIS 7.5 para mobilidade.</span><span class="sxs-lookup"><span data-stu-id="d5492-108">We recommend that you use IIS 7.5 for mobility.</span></span> <span data-ttu-id="d5492-109">As configurações afetam o número máximo de solicitações concomitantes de usuários e o número máximo de threads permitidos para o Mobility Service.</span><span class="sxs-lookup"><span data-stu-id="d5492-109">The settings affect the maximum number of concurrent user requests and the maximum number of threads that are allowed for the Mobility Service.</span></span>

<span data-ttu-id="d5492-110">Aqui estão as configurações de desempenho:</span><span class="sxs-lookup"><span data-stu-id="d5492-110">Here are the performance settings:</span></span>

<div>

## <a name="settings-for-mcx-on-iis-75"></a><span data-ttu-id="d5492-111">Configurações para Mcx no IIS 7.5</span><span class="sxs-lookup"><span data-stu-id="d5492-111">Settings for Mcx on IIS 7.5</span></span>

1.  <span data-ttu-id="d5492-112">**maxConcurrentThreadsPerCPU** está definido como zero (0).</span><span class="sxs-lookup"><span data-stu-id="d5492-112">**maxConcurrentThreadsPerCPU** is set to zero (0).</span></span>

2.  <span data-ttu-id="d5492-113">**maxConcurrentRequestsPerCPU** está definido como zero (0).</span><span class="sxs-lookup"><span data-stu-id="d5492-113">**maxConcurrentRequestsPerCPU** is set to zero (0).</span></span>

3.  <span data-ttu-id="d5492-114">O modelo de processo ASP.NET está definido como AutoConfig (somente para IIS 7.5).</span><span class="sxs-lookup"><span data-stu-id="d5492-114">ASP.NET process model is set to AutoConfig (for IIS 7.5 only).</span></span>

4.  <span data-ttu-id="d5492-115">O limite de fila HTTP.sys está definido como 1.000 (por padrão).</span><span class="sxs-lookup"><span data-stu-id="d5492-115">HTTP.sys queue limit is set to 1,000 (by default).</span></span>

<span data-ttu-id="d5492-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d5492-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

