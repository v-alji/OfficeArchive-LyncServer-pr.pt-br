---
title: Verificar coexistência de pool piloto com pool herdado
description: Verifique a coexistência do pool piloto com o pool herdado.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify pilot pool coexistence with legacy pool
ms:assetid: fe7e14bb-c7eb-4719-b154-009e99360520
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205420(v=OCS.15)
ms:contentKeyID: 48185964
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b910939b59fdaed6df32ae504eb2719435a0161e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440159"
---
# <a name="verify-pilot-pool-coexistence-with-legacy-pool"></a><span data-ttu-id="f8143-103">Verificar coexistência de pool piloto com pool herdado</span><span class="sxs-lookup"><span data-stu-id="f8143-103">Verify pilot pool coexistence with legacy pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f8143-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f8143-104">

<span> </span></span></span>

<span data-ttu-id="f8143-105">_**Tópico da última modificação:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="f8143-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="f8143-106">Depois de implantar o pool piloto, você precisa verificar a coexistência dos dois pools usando as ferramentas administrativas para exibir as informações de pool.</span><span class="sxs-lookup"><span data-stu-id="f8143-106">After you deploy the pilot pool, you need to verify the coexistence of the two pools by using the administrative tools to view the pool information.</span></span> <span data-ttu-id="f8143-107">Para os pools do Lync Server 2013 e pools herdados, você deve usar o painel de controle do Lync Server 2013 e ferramentas do construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="f8143-107">For the Lync Server 2013 pools and legacy pools, you must use the Lync Server 2013 Control Panel and Topology Builder tools.</span></span>

<div>

## <a name="verify-that-lync-server-2013-services-have-started"></a><span data-ttu-id="f8143-108">Verificar se os serviços do Lync Server 2013 começaram</span><span class="sxs-lookup"><span data-stu-id="f8143-108">Verify that Lync Server 2013 services have started</span></span>

1.  <span data-ttu-id="f8143-109">No servidor de front-end do Lync Server 2013, navegue até o \\ applet Serviços de ferramentas administrativas.</span><span class="sxs-lookup"><span data-stu-id="f8143-109">From the Lync Server 2013 Front End Server, navigate to the Administrative Tools\\Services applet.</span></span>

2.  <span data-ttu-id="f8143-110">Verifique se os seguintes serviços estão em execução no servidor front-end:</span><span class="sxs-lookup"><span data-stu-id="f8143-110">Verify that the following services are running on the Front End Server:</span></span>

<span data-ttu-id="f8143-111">**Serviços do Lync Server 2013**</span><span class="sxs-lookup"><span data-stu-id="f8143-111">**Lync Server 2013 services**</span></span>

<span data-ttu-id="f8143-112">![Lista de serviços do Lync Server iniciada](images/JJ205420.cfff9385-6bf6-461c-982c-e727c9f20b70(OCS.15).png "Lista de serviços do Lync Server iniciada")</span><span class="sxs-lookup"><span data-stu-id="f8143-112">![List of Lync Server Services Started](images/JJ205420.cfff9385-6bf6-461c-982c-e727c9f20b70(OCS.15).png "List of Lync Server Services Started")</span></span>

</div>

<div>

## <a name="open-the-lync-server-2013-control-panel"></a><span data-ttu-id="f8143-113">Abrir o painel de controle do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f8143-113">Open the Lync Server 2013 Control Panel</span></span>

<span data-ttu-id="f8143-114">No servidor front-end na implantação do Lync Server 2013, abra o painel de controle do Lync Server 2013 e selecione o pool do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="f8143-114">From the Front End Server in your Lync Server 2013 deployment, open the Lync Server 2013 Control Panel and select the Lync Server 2010 pool.</span></span> <span data-ttu-id="f8143-115">Repita o procedimento para abrir o pool do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f8143-115">Repeat the procedure to open the Lync Server 2013 pool.</span></span>

<span data-ttu-id="f8143-116">**Abrir o painel de controle do Lync Server 2013**</span><span class="sxs-lookup"><span data-stu-id="f8143-116">**Open Lync Server 2013 Control Panel**</span></span>

<span data-ttu-id="f8143-117">![Caixa de diálogo Selecionar URL](images/JJ205420.b1f8e650-9c3c-4563-a403-5069f198342f(OCS.15).png "Caixa de diálogo Selecionar URL")</span><span class="sxs-lookup"><span data-stu-id="f8143-117">![Select URL dialog box](images/JJ205420.b1f8e650-9c3c-4563-a403-5069f198342f(OCS.15).png "Select URL dialog box")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f8143-118">No Lync Server 2013, você deve atualizar o Silverlight para o Silverlight versão 5 antes de usar o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f8143-118">On Lync Server 2013, you must upgrade Silverlight to Silverlight version 5 prior to using the Lync Server Control Panel.</span></span>



</div>

<span data-ttu-id="f8143-119">Essa topologia agora inclui funções do Lync Server 2010 e do Lync Server 2013 Server.</span><span class="sxs-lookup"><span data-stu-id="f8143-119">This topology now includes Lync Server 2010 and Lync Server 2013 server roles.</span></span>

<span data-ttu-id="f8143-120">**Página de topologia do painel de controle do Lync Server 2013**</span><span class="sxs-lookup"><span data-stu-id="f8143-120">**Lync Server 2013 Control Panel Topology page**</span></span>

<span data-ttu-id="f8143-121">![Painel de controle do Lync Server-página de topologia](images/JJ205420.4ed1cc7a-cb3e-42f6-82e2-6d4d71d19352(OCS.15).jpg "Painel de controle do Lync Server-página de topologia")</span><span class="sxs-lookup"><span data-stu-id="f8143-121">![Lync Server Control Panel - Topology page](images/JJ205420.4ed1cc7a-cb3e-42f6-82e2-6d4d71d19352(OCS.15).jpg "Lync Server Control Panel - Topology page")</span></span>

</div>

<div>

## <a name="dont-attempt-to-open-the-topology-in-lync-server-2010-topology-builder"></a><span data-ttu-id="f8143-122">Não tente abrir a topologia no construtor de topologias do Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="f8143-122">Don’t attempt to open the topology in Lync Server 2010 Topology Builder</span></span>

<span data-ttu-id="f8143-123">Se você tentar abrir a topologia usando o construtor de topologias do Lync Server 2010, o erro será encontrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="f8143-123">If you attempt to open the topology using Lync Server 2010 Topology Builder, you will encounter the error below.</span></span> <span data-ttu-id="f8143-124">A topologia só pode ser visualizada usando o construtor de topologias do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f8143-124">The topology can only be viewed using Lync Server 2013 Topology Builder.</span></span> <span data-ttu-id="f8143-125">O construtor de topologia do Lync Server 2013 deve ser usado para criar pools para o Lync Server 2013 e o Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="f8143-125">The Lync Server 2013 Topology Builder must be used to create pools for both Lync Server 2013 and Lync Server 2010.</span></span>

<span data-ttu-id="f8143-126">**Mensagem de erro do construtor de topologia do Lync Server 2010**</span><span class="sxs-lookup"><span data-stu-id="f8143-126">**Lync Server 2010 Topology Builder error message**</span></span>

<span data-ttu-id="f8143-127">![Erro de snap do MMC do construtor de topologia do Lync Server](images/JJ205420.f6666343-c348-4d81-ae0e-6ba5a44e16c4(OCS.15).png "Erro de snap do MMC do construtor de topologia do Lync Server")</span><span class="sxs-lookup"><span data-stu-id="f8143-127">![Lync Server Topology Builder MMC Snap Error](images/JJ205420.f6666343-c348-4d81-ae0e-6ba5a44e16c4(OCS.15).png "Lync Server Topology Builder MMC Snap Error")</span></span>

<span data-ttu-id="f8143-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f8143-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

