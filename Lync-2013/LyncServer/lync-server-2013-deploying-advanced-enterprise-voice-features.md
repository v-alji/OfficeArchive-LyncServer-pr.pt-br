---
title: 'Lync Server 2013: Implantando recursos avançados do Enterprise Voice'
description: 'Lync Server 2013: Implantando recursos avançados do Enterprise Voice.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying advanced Enterprise Voice features
ms:assetid: 286d9c0b-9442-448f-a6e5-95b3034278fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425753(v=OCS.15)
ms:contentKeyID: 48183675
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e5cab05de60e1df1611a14af1f5239c24402c6d9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430109"
---
# <a name="deploying-advanced-enterprise-voice-features-in-lync-server-2013"></a><span data-ttu-id="0c82b-103">Implantação de recursos avançados do Enterprise Voice no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c82b-103">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0c82b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0c82b-104">

<span> </span></span></span>

<span data-ttu-id="0c82b-105">_**Tópico da última modificação:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="0c82b-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="0c82b-106">Após configurar a funcionalidade básica do Enterprise Voice para sua organização, será possível implantar opcionalmente um ou mais recursos avançados do Enterprise Voice seguindo os procedimentos desta seção.</span><span class="sxs-lookup"><span data-stu-id="0c82b-106">After you have configured basic Enterprise Voice functionality for your organization, you can optionally deploy one or more advanced Enterprise Voice features by following the procedures in this section.</span></span>

<span data-ttu-id="0c82b-107">Para obter detalhes sobre os recursos avançados do Enterprise Voice, consulte as seguintes seções da documentação do [Planning for Lync Server 2013](lync-server-2013-planning.md) :</span><span class="sxs-lookup"><span data-stu-id="0c82b-107">For details about the advanced Enterprise Voice features, see the following sections of the [Planning for Lync Server 2013](lync-server-2013-planning.md) documentation:</span></span>

  - [<span data-ttu-id="0c82b-108">Planejamento para controle de admissão de chamada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c82b-108">Planning for call admission control in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-admission-control.md)

  - [<span data-ttu-id="0c82b-109">Planejamento para serviços de emergência (E9-1-1) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c82b-109">Planning for emergency services (E9-1-1) in Lync Server 2013</span></span>](lync-server-2013-planning-for-emergency-services-e9-1-1.md)

  - [<span data-ttu-id="0c82b-110">Planejamento de bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c82b-110">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)

<div>

## <a name="in-this-section"></a><span data-ttu-id="0c82b-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="0c82b-111">In This Section</span></span>

  - [<span data-ttu-id="0c82b-112">Sobre regiões de rede, sites e subredes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c82b-112">About network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-about-network-regions-sites-and-subnets.md)

  - [<span data-ttu-id="0c82b-113">Criar ou modificar uma região de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c82b-113">Create or modify a network region in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-region.md)

  - [<span data-ttu-id="0c82b-114">Criar ou modificar um site da rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c82b-114">Create or modify a network site in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-site.md)

  - [<span data-ttu-id="0c82b-115">Associar uma subrede a um site de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c82b-115">Associate a subnet with a network site in Lync Server 2013</span></span>](lync-server-2013-associate-a-subnet-with-a-network-site.md)

  - [<span data-ttu-id="0c82b-116">Configurar o controle de admissão de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c82b-116">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)

  - [<span data-ttu-id="0c82b-117">Configurar 9-1-1 Avançado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c82b-117">Configure Enhanced 9-1-1 in Lync Server 2013</span></span>](lync-server-2013-configure-enhanced-9-1-1.md)

  - [<span data-ttu-id="0c82b-118">Configurar bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c82b-118">Configure media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-media-bypass.md)

<span data-ttu-id="0c82b-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0c82b-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

