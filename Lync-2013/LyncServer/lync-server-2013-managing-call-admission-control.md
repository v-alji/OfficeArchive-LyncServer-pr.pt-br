---
title: 'Lync Server 2013: Gerenciando o controle de admissão de chamadas'
description: 'Lync Server 2013: Gerenciando o controle de admissão de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing call admission control
ms:assetid: b0bd4783-6f47-408d-b010-2e30f9bc1770
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721851(v=OCS.15)
ms:contentKeyID: 49733784
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0a1c01bff6d1dce48dea314b6704cc0f5ff7d6b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425959"
---
# <a name="managing-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="f7c8b-103">Gerenciando o controle de admissão de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7c8b-103">Managing call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f7c8b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f7c8b-104">

<span> </span></span></span>

<span data-ttu-id="f7c8b-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="f7c8b-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="f7c8b-106">O CAC (serviço de controle de admissão de chamadas) determina, com base na largura de banda da rede disponível, se será permitido estabelecer sessões de comunicação em tempo real, como chamadas de voz ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="f7c8b-106">Call admission control (CAC) determines, based on available network bandwidth, whether to allow real-time communications sessions such as voice or video calls to be established.</span></span> <span data-ttu-id="f7c8b-107">Use os procedimentos a seguir para gerenciar diferentes recursos do CAC para o seu ambiente do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f7c8b-107">Use the following procedures to manage different CAC features for your Lync Server 2013 environment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f7c8b-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f7c8b-108">In This Section</span></span>

  - [<span data-ttu-id="f7c8b-109">Habilitando o controle de admissão de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7c8b-109">Enabling call admission control in Lync Server 2013</span></span>](lync-server-2013-enabling-call-admission-control.md)

  - [<span data-ttu-id="f7c8b-110">Gerenciando perfis de política de largura de banda de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7c8b-110">Managing network bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-managing-network-bandwidth-policy-profiles.md)

  - [<span data-ttu-id="f7c8b-111">Regiões de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7c8b-111">Network regions in Lync Server 2013</span></span>](lync-server-2013-network-regions.md)

  - [<span data-ttu-id="f7c8b-112">Rotas de região de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7c8b-112">Network region routes in Lync Server 2013</span></span>](lync-server-2013-network-region-routes.md)

  - [<span data-ttu-id="f7c8b-113">Controle de admissão de chamadas para sites no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7c8b-113">Call admission control for sites in Lync Server 2013</span></span>](lync-server-2013-call-admission-control-for-sites.md)

  - [<span data-ttu-id="f7c8b-114">Habilitando e desabilitando o bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7c8b-114">Enabling and disabling media bypass in Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-media-bypass.md)

  - [<span data-ttu-id="f7c8b-115">Vinculando regiões de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7c8b-115">Linking network regions in Lync Server 2013</span></span>](lync-server-2013-linking-network-regions.md)

  - [<span data-ttu-id="f7c8b-116">Gerenciando sub-redes de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7c8b-116">Managing network subnets in Lync Server 2013</span></span>](lync-server-2013-managing-network-subnets.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f7c8b-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7c8b-117">See Also</span></span>


[<span data-ttu-id="f7c8b-118">Visão geral do controle de admissão de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7c8b-118">Overview of call admission control in Lync Server 2013</span></span>](lync-server-2013-overview-of-call-admission-control.md)  
  

<span data-ttu-id="f7c8b-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f7c8b-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

