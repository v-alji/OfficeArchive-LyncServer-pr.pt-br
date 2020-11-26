---
title: Compatibilidade do Lync Server 2013 com resiliência de site metropolitano do Lync Server 2010
description: Compatibilidade do Lync Server 2013 com o Lync Server 2010 Metropolitana de recuperação de site.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2010 metropolitan site resiliency
ms:assetid: 18673ff6-b664-4a57-a89b-cbda8b129e6a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204715(v=OCS.15)
ms:contentKeyID: 48183526
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec72f261ac593b24bad13dcd400f495ba7ba0722
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434603"
---
# <a name="lync-server-2010-metropolitan-site-resiliency"></a><span data-ttu-id="4a022-103">Resiliência de site metropolitano no Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="4a022-103">Lync Server 2010 metropolitan site resiliency</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4a022-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4a022-104">

<span> </span></span></span>

<span data-ttu-id="4a022-105">_**Tópico da última modificação:** 2014-03-19_</span><span class="sxs-lookup"><span data-stu-id="4a022-105">_**Topic Last Modified:** 2014-03-19_</span></span>

<span data-ttu-id="4a022-106">A solução de resiliência de site metropolitana compatível com o Lync Server 2010 não é compatível com o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4a022-106">The metropolitan site resiliency solution supported for Lync Server 2010 is not supported for Lync Server 2013.</span></span> <span data-ttu-id="4a022-107">Esta solução envolve a inclusão de um único pool de front-end em dois data centers na mesma área metropolitana.</span><span class="sxs-lookup"><span data-stu-id="4a022-107">This solution involved spanning a single Front End pool across two data centers in the same metropolitan area.</span></span>

<span data-ttu-id="4a022-108">A solução Metropolitana de resiliência de site foi projetada para recuperar-se da perda de um data center completo.</span><span class="sxs-lookup"><span data-stu-id="4a022-108">The metropolitan site resiliency solution was designed to recover from the loss of a full datacenter.</span></span> <span data-ttu-id="4a022-109">Quando você se estende pelo pool em dois datacenters, geralmente coloca metade dos seus front-ends em um datacenter e a outra metade do segundo datacenter.</span><span class="sxs-lookup"><span data-stu-id="4a022-109">When you span your pool across two datacenters, you typically put half of your front ends in one datacenter and the other half in the second datacenter.</span></span> <span data-ttu-id="4a022-110">Se você perder um datacenter inteiro, perderá metade dos seus servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="4a022-110">If you lose an entire datacenter, you have lost half of your Front End Servers.</span></span> <span data-ttu-id="4a022-111">Isso pode causar problemas com o novo modelo de sistema distribuído para pools de front-end no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4a022-111">This can cause issues with the new distributed system model for Front End Pools in Lync Server 2013.</span></span> <span data-ttu-id="4a022-112">Para obter mais informações, consulte [topologias e componentes para servidores front-end, mensagens instantâneas e presença no Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span><span class="sxs-lookup"><span data-stu-id="4a022-112">For more information, see [Topologies and components for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span></span>

<span data-ttu-id="4a022-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4a022-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

