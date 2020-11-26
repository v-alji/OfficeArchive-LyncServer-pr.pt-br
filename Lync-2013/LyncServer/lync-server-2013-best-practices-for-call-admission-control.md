---
title: 'Lync Server 2013: Práticas recomendadas para controle de admissão de chamada'
description: 'Lync Server 2013: práticas recomendadas para controle de admissão de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for call admission control
ms:assetid: 97173cca-8175-4ae2-a247-eb7ef809da93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398770(v=OCS.15)
ms:contentKeyID: 48184913
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17c32af904dc7fb48a1a5d1903bd6ed1f81f4cb3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436066"
---
# <a name="best-practices-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="16d69-103">Práticas recomendadas para controle de admissão de chamada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="16d69-103">Best practices for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="16d69-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="16d69-104">

<span> </span></span></span>

<span data-ttu-id="16d69-105">_**Tópico da última modificação:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="16d69-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="16d69-106">Para melhorar o desempenho e facilitar a implantação, aplique as seguintes práticas recomendadas ao implantar o controle de admissão de chamadas:</span><span class="sxs-lookup"><span data-stu-id="16d69-106">To enhance performance and facilitate deployment, apply the following best practices when you deploy call admission control:</span></span>

  - <span data-ttu-id="16d69-107">Garanta que as WANs sejam provisionadas de forma adequada para tráfego de mídia atual e previsto.</span><span class="sxs-lookup"><span data-stu-id="16d69-107">Ensure that WANs are adequately provisioned for current and anticipated media traffic.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="16d69-108">Recomendamos que você Fatore em um buffer para seus limites de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="16d69-108">We recommend that you factor in a buffer to your bandwidth limits.</span></span> <span data-ttu-id="16d69-109">Há cenários como condições de corrida que afetam a largura de banda total usada e podem resultar em situações em que o limite de largura de banda é excedido.</span><span class="sxs-lookup"><span data-stu-id="16d69-109">There are scenarios such as race conditions that affect the total bandwidth used and can result in situations where the bandwidth limit is exceeded.</span></span> <span data-ttu-id="16d69-110">Por exemplo, se duas chamadas tentam iniciar enquanto o tráfego de mídia está se aproximando de um limite de largura de banda, um deles pode ser negado porque o outro gerenciado para iniciar primeiro.</span><span class="sxs-lookup"><span data-stu-id="16d69-110">For example, if two calls try to start while media traffic is approaching a bandwidth limit, one of them may be denied because the other managed to start first.</span></span>

    
    </div>

  - <span data-ttu-id="16d69-111">Monitorar o uso da rede e os registros de detalhes da chamada para que você possa escolher as configurações de CAC otimizadas e atualizar as configurações de CAC como alterações de uso de rede.</span><span class="sxs-lookup"><span data-stu-id="16d69-111">Monitor network usage and call detail records so that you can choose optimal CAC settings and update CAC settings as network usage changes.</span></span>

  - <span data-ttu-id="16d69-112">Use as políticas de largura de banda do CAC para complementar as configurações de QoS.</span><span class="sxs-lookup"><span data-stu-id="16d69-112">Use CAC bandwidth policies to complement QoS settings.</span></span>

  - <span data-ttu-id="16d69-113">Se você quiser redirecionar chamadas bloqueadas para a PSTN, verifique a funcionalidade e a funcionalidade da PSTN.</span><span class="sxs-lookup"><span data-stu-id="16d69-113">If you want to re-route blocked calls onto the PSTN, verify PSTN functionality and capacity.</span></span> <span data-ttu-id="16d69-114">Para obter detalhes, consulte [planejando o roteamento de voz de saída no Lync Server 2013](lync-server-2013-planning-outbound-voice-routing.md).</span><span class="sxs-lookup"><span data-stu-id="16d69-114">For details, see [Planning outbound voice routing in Lync Server 2013](lync-server-2013-planning-outbound-voice-routing.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="16d69-115">A capacidade se refere ao número de portas que você precisa abrir para dar suporte a redirecionamento PSTN potencial.</span><span class="sxs-lookup"><span data-stu-id="16d69-115">Capacity refers to the number of ports you need to open to support potential PSTN re-routing.</span></span>

    
    <span data-ttu-id="16d69-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="16d69-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

