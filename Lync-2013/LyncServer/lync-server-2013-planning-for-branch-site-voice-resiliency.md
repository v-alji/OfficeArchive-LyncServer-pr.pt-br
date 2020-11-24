---
title: 'Lync Server 2013: Planejamento de resiliência de voz no site da filial'
description: 'Lync Server 2013: planejando a resiliência de voz do site de filial.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for branch-site voice resiliency
ms:assetid: 67713f57-3ded-4127-ac37-57d8099bf384
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398477(v=OCS.15)
ms:contentKeyID: 48184351
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9ce7eb25e1d3078cd2114fc26428f4c8c2ff6508
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390235"
---
# <a name="planning-for-branch-site-voice-resiliency-in-lync-server-2013"></a><span data-ttu-id="5a000-103">Planejamento de resiliência de voz no site da filial no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a000-103">Planning for branch-site voice resiliency in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5a000-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5a000-104">

<span> </span></span></span>

<span data-ttu-id="5a000-105">_**Tópico da última modificação:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="5a000-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="5a000-106">Se você quiser fornecer resiliência de filial do site, ou seja, serviço Enterprise Voice de alta disponibilidade, terá três opções para fazer isso:</span><span class="sxs-lookup"><span data-stu-id="5a000-106">If you want to provide branch-site resiliency, that is, high-availability Enterprise Voice service, you have three options for doing so:</span></span>

  - <span data-ttu-id="5a000-107">Aparelho de Filial Persistente</span><span class="sxs-lookup"><span data-stu-id="5a000-107">Survivable Branch Appliance</span></span>

  - <span data-ttu-id="5a000-108">Servidor de Filial Persistente</span><span class="sxs-lookup"><span data-stu-id="5a000-108">Survivable Branch Server</span></span>

  - <span data-ttu-id="5a000-109">Uma implantação completa do Lync Server no site da filial</span><span class="sxs-lookup"><span data-stu-id="5a000-109">A full Lync Server deployment at the branch site</span></span>

<span data-ttu-id="5a000-p101">Este guia ajudará você a avaliar qual solução de resiliência é melhor para a organização e, com base em sua solução de resiliência, a solução de conectividade PSTN a ser usada. Ele também o ajuda a se preparar para implantar a solução escolhida, descrevendo os pré-requisitos e outras considerações de planejamento.</span><span class="sxs-lookup"><span data-stu-id="5a000-p101">This guide will help you evaluate which resiliency solution is best for your organization and, based on your resiliency solution, which PSTN-connectivity solution to use. It will also help you prepare to deploy the solution that you choose by describing prerequisites and other planning considerations.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5a000-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5a000-112">In This Section</span></span>

  - [<span data-ttu-id="5a000-113">Recursos de resiliência do site de filial no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a000-113">Branch-site resiliency features in Lync Server 2013</span></span>](lync-server-2013-branch-site-resiliency-features.md)

  - [<span data-ttu-id="5a000-114">Soluções de resiliência do site de filial no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a000-114">Branch-site resiliency solutions in Lync Server 2013</span></span>](lync-server-2013-branch-site-resiliency-solutions.md)

  - [<span data-ttu-id="5a000-115">Requisitos de resiliência do site da filial para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a000-115">Branch-site resiliency requirements for Lync Server 2013</span></span>](lync-server-2013-branch-site-resiliency-requirements.md)

<span data-ttu-id="5a000-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5a000-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

