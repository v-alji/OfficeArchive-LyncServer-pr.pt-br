---
title: 'Lync Server 2013: Planejamento para resiliência do Enterprise Voice'
description: 'Lync Server 2013: planejando a resiliência do Enterprise Voice.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Enterprise Voice resiliency
ms:assetid: ca116700-1055-4ca5-9b87-4c7f380c3655
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398840(v=OCS.15)
ms:contentKeyID: 48185408
ms.date: 10/17/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2adcf09b87264666924a16543a1b21e8e3cae39f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443003"
---
# <a name="planning-for-enterprise-voice-resiliency-in-lync-server-2013"></a><span data-ttu-id="c930b-103">Planejamento para resiliência do Enterprise Voice no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c930b-103">Planning for Enterprise Voice resiliency in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c930b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c930b-104">

<span> </span></span></span>

<span data-ttu-id="c930b-105">_**Tópico da última modificação:** 2014-10-17_</span><span class="sxs-lookup"><span data-stu-id="c930b-105">_**Topic Last Modified:** 2014-10-17_</span></span>

<span data-ttu-id="c930b-106">A resiliência de voz refere-se à capacidade de os usuários continuarem a fazer e receber chamadas se um site central que hospeda o Lync Server 2013 ficar indisponível, seja por meio de uma falha de rede de longa distância (WAN) ou outra causa.</span><span class="sxs-lookup"><span data-stu-id="c930b-106">Voice resiliency refers to the ability of users to continue making and receiving calls if a central site that hosts Lync Server 2013 becomes unavailable, whether through a wide area network (WAN) failure or another cause.</span></span> <span data-ttu-id="c930b-107">Se um local central falhar, o serviço do Enterprise Voice deverá continuar sem interrupções por meio de failover direto para um local de backup.</span><span class="sxs-lookup"><span data-stu-id="c930b-107">If a central site fails, Enterprise Voice service must continue uninterrupted through seamless failover to a backup site.</span></span> <span data-ttu-id="c930b-108">No caso de uma falha de WAN, as chamadas do local de filial deverão ser redirecionadas para um gateway PSTN local.</span><span class="sxs-lookup"><span data-stu-id="c930b-108">In the event of WAN failure, branch site calls must be redirected to a local PSTN gateway.</span></span> <span data-ttu-id="c930b-109">Esta seção discute o planejamento de resiliência de voz no caso de uma falha do local central ou de WAN.</span><span class="sxs-lookup"><span data-stu-id="c930b-109">This section discusses planning for voice resiliency in the event of central-site or WAN failure.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c930b-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c930b-110">In This Section</span></span>

  - [<span data-ttu-id="c930b-111">Planejamento de resiliência de voz do site central no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c930b-111">Planning for central site voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-central-site-voice-resiliency.md)

  - [<span data-ttu-id="c930b-112">Planejamento de resiliência de voz no site da filial no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c930b-112">Planning for branch-site voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-branch-site-voice-resiliency.md)

<span data-ttu-id="c930b-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c930b-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

