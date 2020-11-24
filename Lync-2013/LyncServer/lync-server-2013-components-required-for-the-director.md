---
title: 'Lync Server 2013: Componentes necessários para o diretor'
description: 'Lync Server 2013: componentes necessários para o diretor.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components required for the Director
ms:assetid: 15c7c8d4-b93f-4386-b2d1-d76dab8f801e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398228(v=OCS.15)
ms:contentKeyID: 48183502
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 57f717b9ddb9557f212321cdab075713a4b85c2d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389802"
---
# <a name="components-required-for-the-director-in-lync-server-2013"></a><span data-ttu-id="89e5e-103">Componentes necessários para o diretor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89e5e-103">Components required for the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="89e5e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="89e5e-104">

<span> </span></span></span>

<span data-ttu-id="89e5e-105">_**Tópico da última modificação:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="89e5e-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="89e5e-106">O único componente necessário para criar e configurar um diretor é implantar a função de servidor diretor.</span><span class="sxs-lookup"><span data-stu-id="89e5e-106">The only component required to create and configure a Director is to deploy the Director server role.</span></span> <span data-ttu-id="89e5e-107">Isso é feito usando o construtor de topologias e define um único pool de computadores ou um pool de vários computadores no nó do pool de diretor.</span><span class="sxs-lookup"><span data-stu-id="89e5e-107">You do this by using Topology Builder and define either a single computer pool or a multiple computer pool in the Director pool node.</span></span> <span data-ttu-id="89e5e-108">Depois de definir o diretor ou o pool do diretor, execute o assistente de implantação do Lync Server no computador que será um diretor.</span><span class="sxs-lookup"><span data-stu-id="89e5e-108">After you have defined the Director or Director pool, run the Lync Server Deployment Wizard on the computer that will be a Director.</span></span> <span data-ttu-id="89e5e-109">No caso de um pool de diretor, você executa o assistente de implantação do Lync Server em cada servidor que será membro do pool.</span><span class="sxs-lookup"><span data-stu-id="89e5e-109">In the case of a Director pool, you run the Lync Server Deployment Wizard on each server that will be a member of the pool.</span></span>

<div>

## <a name="topologies"></a><span data-ttu-id="89e5e-110">Topologia</span><span class="sxs-lookup"><span data-stu-id="89e5e-110">Topologies</span></span>

<span data-ttu-id="89e5e-111">Você pode implementar um único servidor de director ou um pool de directors.</span><span class="sxs-lookup"><span data-stu-id="89e5e-111">You can implement a single Director server or a Director pool.</span></span> <span data-ttu-id="89e5e-112">O diretor é sempre um servidor ou pool separado, não posicionado com nenhuma outra função de servidor no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="89e5e-112">The Director is always a separate server or pool, not collocated with any other server role in Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="89e5e-113">Se você não implantar diretores, o servidor front-end ou o pool de front-end assumirá a função de diretor.</span><span class="sxs-lookup"><span data-stu-id="89e5e-113">If you do not deploy Directors, the Front End Server or Front End pool will assume the Director role.</span></span>



</div>

<span data-ttu-id="89e5e-114">É necessário balancear A carga de um pool de diretores.</span><span class="sxs-lookup"><span data-stu-id="89e5e-114">A pool of Directors must be load balanced.</span></span> <span data-ttu-id="89e5e-115">Você pode executar uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="89e5e-115">You can do one of the following:</span></span>

  - <span data-ttu-id="89e5e-116">Crie uma topologia que use um balanceador de carga de hardware para serviços Web e balanceamento de carga DNS (Domain Name System) para os outros tipos de tráfego.</span><span class="sxs-lookup"><span data-stu-id="89e5e-116">Create a topology that uses a hardware load balancer for web services and Domain Name System (DNS) load balancing for the other traffic types.</span></span>
    
    [<span data-ttu-id="89e5e-117">Pool de diretores em escala - balanceamento de carga de DNS e balanceador de carga de hardware no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89e5e-117">Scaled Director pool - DNS load balancing and hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-scaled-director-pool-dns-load-balancing-and-hardware-load-balancer.md)

  - <span data-ttu-id="89e5e-118">Crie uma topologia que use um balanceador de carga de hardware para o balanceamento de carga necessário para o pool de diretor.</span><span class="sxs-lookup"><span data-stu-id="89e5e-118">Create a topology that uses a hardware load balancer for load balancing needed for the Director pool.</span></span>
    
    [<span data-ttu-id="89e5e-119">Pool de diretores em escala - balanceador de carga de hardware no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89e5e-119">Scaled Director pool - hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-scaled-director-pool-hardware-load-balancer.md)

<span data-ttu-id="89e5e-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="89e5e-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

