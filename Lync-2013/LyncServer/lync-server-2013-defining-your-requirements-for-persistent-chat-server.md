---
title: 'Lync Server 2013: Definindo seus requisitos para o Servidor de Chat Persistente'
description: 'Lync Server 2013: definindo seus requisitos de servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your organization's requirements for Persistent Chat Server
ms:assetid: 568674fb-c08a-4170-ac38-e2f8428c69e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398372(v=OCS.15)
ms:contentKeyID: 48184166
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6af3fab1d91b78a5993f723b8fc6b375e4ab7cee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430781"
---
# <a name="defining-your-organizations-requirements-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="ef98a-103">Definindo os requisitos de sua organização para o Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ef98a-103">Defining your organization's requirements for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ef98a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ef98a-104">

<span> </span></span></span>

<span data-ttu-id="ef98a-105">_**Tópico da última modificação:** 2014-01-15_</span><span class="sxs-lookup"><span data-stu-id="ef98a-105">_**Topic Last Modified:** 2014-01-15_</span></span>

<span data-ttu-id="ef98a-106">Antes de implantar o servidor de chat persistente para a sua organização, é essencial considerar as seguintes perguntas importantes para otimizar a implantação:</span><span class="sxs-lookup"><span data-stu-id="ef98a-106">Before you deploy Persistent Chat Server for your organization, it’s essential to consider the following key questions to optimize your deployment:</span></span>

  - <span data-ttu-id="ef98a-107">Quem (perfil do usuário) deve ser habilitado para o servidor de chat persistente?</span><span class="sxs-lookup"><span data-stu-id="ef98a-107">Who (user profile) should be enabled for Persistent Chat Server?</span></span> <span data-ttu-id="ef98a-108">O servidor de chat persistente está habilitado por uma política que pode ser definida em um nível global, de site, de grupo ou de usuário.</span><span class="sxs-lookup"><span data-stu-id="ef98a-108">Persistent Chat Server is enabled by a policy that can be set at a Global, Site, Pool or User level.</span></span>

  - <span data-ttu-id="ef98a-109">Quantos usuários (escala) devem ser habilitados para o servidor de chat persistente?</span><span class="sxs-lookup"><span data-stu-id="ef98a-109">How many users (scale) should be enabled for Persistent Chat Server?</span></span> <span data-ttu-id="ef98a-110">O servidor de chat persistente dá suporte ao 150.000 usuários provisionados (habilitados pela política) e um máximo de 80.000 usuários simultâneos que usam o servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="ef98a-110">Persistent Chat Server supports 150,000 provisioned users (enabled by policy), and a maximum of 80,000 concurrent users using Persistent Chat Server.</span></span> <span data-ttu-id="ef98a-111">Um único Servidor de Chat Persistente pode suportar 20.000 usuários conectados e um único pool de Servidor de Chat Persistente pode ter até 4 servidores ativos para um total de 80.000 usuários conectados simultâneos.</span><span class="sxs-lookup"><span data-stu-id="ef98a-111">A single Persistent Chat Server can support 20,000 connected users, and a single Persistent Chat Server pool can have up to 4 active servers for a total of 80,000 concurrently connected users.</span></span>

  - <span data-ttu-id="ef98a-112">Você está migrando de uma versão anterior do servidor de chat de grupo ou está implantando o servidor de chat persistente pela primeira vez?</span><span class="sxs-lookup"><span data-stu-id="ef98a-112">Are you migrating from a previous version of Group Chat Server, or are you deploying Persistent Chat Server for the first time?</span></span>

  - <span data-ttu-id="ef98a-113">Há requisitos de conformidade?</span><span class="sxs-lookup"><span data-stu-id="ef98a-113">Are there compliance requirements?</span></span> <span data-ttu-id="ef98a-114">O servidor de chat persistente dá suporte à conformidade.</span><span class="sxs-lookup"><span data-stu-id="ef98a-114">Persistent Chat Server supports compliance.</span></span> <span data-ttu-id="ef98a-115">O serviço de conformidade é executado no servidor front-end persistente do servidor de chat, ao contrário do requisito para um computador separado em implantações de servidor de chat de grupo anteriores.</span><span class="sxs-lookup"><span data-stu-id="ef98a-115">The compliance service runs collocated on the Persistent Chat Server Front End Server, as opposed to the requirement for a separate computer in previous Group Chat Server deployments.</span></span> <span data-ttu-id="ef98a-116">A conformidade é opcional e, se escolhida, requer um banco de dados de conformidade que deve ser configurado para armazenar dados de conformidade e eventos.</span><span class="sxs-lookup"><span data-stu-id="ef98a-116">Compliance is optional, and if chosen, requires a compliance database that must be configured to store compliance data and events.</span></span> <span data-ttu-id="ef98a-117">Você também pode configurar um adaptador para obter os dados do banco de dados de conformidade e convertê-los em outro formato (como arquivos XML ou arquivos hospedados pelo Exchange).</span><span class="sxs-lookup"><span data-stu-id="ef98a-117">You may want to also configure an adapter to take the data from the compliance database and convert to another format (such as XML files or Exchange-hosted archives).</span></span>

  - <span data-ttu-id="ef98a-118">Como você deseja controlar escopos, limites éticos e acesso?</span><span class="sxs-lookup"><span data-stu-id="ef98a-118">How do you want to control scopes, ethical boundaries, and access?</span></span> <span data-ttu-id="ef98a-119">Você pode definir **categorias** para segregar esses limites e escolher quem tem permissão para estar em salas criadas em cada uma dessas categorias.</span><span class="sxs-lookup"><span data-stu-id="ef98a-119">You can define **Categories** to segregate these boundaries, and choose who is allowed to be in rooms that are created in each of these categories.</span></span>

  - <span data-ttu-id="ef98a-120">Como você deseja controlar quem pode criar salas?</span><span class="sxs-lookup"><span data-stu-id="ef98a-120">How do you want to control who can create rooms?</span></span> <span data-ttu-id="ef98a-121">Você pode configurar os **criadores**, apropriadamente às suas categorias, que podem criar salas.</span><span class="sxs-lookup"><span data-stu-id="ef98a-121">You can configure **Creators**, appropriate to your categories, who can create rooms.</span></span> <span data-ttu-id="ef98a-122">Os criadores podem atribuir outros membros como **gerentes de sala de chat** para gerenciamento contínuo das salas (adicionando ou removendo membros adicionais), de acordo com o escopo para **AllowedMembers/DeniedMembers** configurado pela categoria.</span><span class="sxs-lookup"><span data-stu-id="ef98a-122">Creators can assign other members as **Chat Room Managers** for ongoing management of the rooms (adding or removing additional members), according to the scope for **AllowedMembers/DeniedMembers** configured by the category.</span></span>

  - <span data-ttu-id="ef98a-123">Como você deseja criar salas?</span><span class="sxs-lookup"><span data-stu-id="ef98a-123">How do you want to create rooms?</span></span> <span data-ttu-id="ef98a-124">O servidor de chat persistente fornece um recurso baseado na Web para a criação e o gerenciamento de salas.</span><span class="sxs-lookup"><span data-stu-id="ef98a-124">Persistent Chat Server provides a web-based feature for room creation and management.</span></span> <span data-ttu-id="ef98a-125">Isso pode ser iniciado pelo cliente do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="ef98a-125">This can be launched from the Lync 2013 client.</span></span> <span data-ttu-id="ef98a-126">Você pode optar por definir uma solução personalizada (usando o kit de desenvolvimento de software (SDK) do servidor de chat persistente) que implementa suas necessidades comerciais e fluxos de trabalho e configura o servidor de chat persistente para direcionar os usuários para sua solução personalizada.</span><span class="sxs-lookup"><span data-stu-id="ef98a-126">You can choose to define a custom solution (by using the Persistent Chat Server Software Development Kit (SDK)) that implements your business requirements and workflows, and configures Persistent Chat Server to direct users to your custom solution.</span></span>

  - <span data-ttu-id="ef98a-127">Que tipo de suplemento você deseja provisionar?</span><span class="sxs-lookup"><span data-stu-id="ef98a-127">What kind of add-ins do you want to provision?</span></span> <span data-ttu-id="ef98a-128">Os **suplementos** aprimoram a experiência da sala aproveitando o painel extensibilidade no cliente do Lync 2013 para fornecer contexto que é relevante para a sala.</span><span class="sxs-lookup"><span data-stu-id="ef98a-128">**Add-ins** enhance the in-room experience by leveraging the extensibility pane in the Lync 2013 client to provide context that is relevant to the room.</span></span> <span data-ttu-id="ef98a-129">É possível escolher quais suplementos gerais podem ser mais úteis (por exemplo, o site da sua empresa, documentos de colaboração interna etc.).</span><span class="sxs-lookup"><span data-stu-id="ef98a-129">You can choose what general add-ins might be most useful (for example, your company website, internal collaboration documents, and so on).</span></span> <span data-ttu-id="ef98a-130">Os gerentes das salas de chat podem escolher um dos suplementos registrados e associá-lo às salas, se desejado.</span><span class="sxs-lookup"><span data-stu-id="ef98a-130">Chat room managers can choose one of the registered add-ins and associate it with their rooms, if desired.</span></span>

  - <span data-ttu-id="ef98a-131">Que tipo de requisito de alta disponibilidade e recuperação de desastre você tem?</span><span class="sxs-lookup"><span data-stu-id="ef98a-131">What kind of high availability and disaster recovery requirements do you have?</span></span> <span data-ttu-id="ef98a-132">O servidor de chat persistente dá suporte ao espelhamento do SQL Server e ao agrupamento do SQL Server para alta disponibilidade e dá suporte a até 8 servidores (4 ativos e 4 em standby) em um pool ampliado com o envio de log do SQL Server para recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="ef98a-132">Persistent Chat Server supports SQL Server mirroring and SQL Server clustering for high availability and supports up to 8 servers (4 active and 4 standby) in a stretched pool with SQL Server log shipping for disaster recovery.</span></span>

  - <span data-ttu-id="ef98a-133">Há requisitos regulatórios?</span><span class="sxs-lookup"><span data-stu-id="ef98a-133">Are there regulatory requirements?</span></span> <span data-ttu-id="ef98a-134">Se a sua empresa estiver em um país/região onde os dados precisam ser mantidos dentro do país, talvez seja necessário implantar vários pools de servidores de chat persistentes, cada um local para uma geografia específica.</span><span class="sxs-lookup"><span data-stu-id="ef98a-134">If your company is in a country/region where data needs to be kept within the country, you may need to deploy multiple Persistent Chat Server pools, each local to a specific geography.</span></span> <span data-ttu-id="ef98a-135">Uma sala, categoria ou suplemento não abrange pools — ele pertence a apenas um pool persistente do servidor de chat.</span><span class="sxs-lookup"><span data-stu-id="ef98a-135">A room, category, or add-in does not span pools—it belongs to only one Persistent Chat Server pool.</span></span> <span data-ttu-id="ef98a-136">Você pode gerenciar o conjunto de categorias, suplementos e salas para cada pool de servidores de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="ef98a-136">You can manage the set of categories, add-ins and rooms for each Persistent Chat Server pool.</span></span> <span data-ttu-id="ef98a-137">Os usuários podem ser configurados para ter acesso a salas em um ou mais pools usando o escopo de associação do escopo ou da sala de AllowedMembers de categorias, dependendo de como projetar suas categorias.</span><span class="sxs-lookup"><span data-stu-id="ef98a-137">Users can be configured to have access to rooms in one or more pools using the category AllowedMembers scope or Room’s membership scope, depending on how you design your categories.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="ef98a-138">Ter vários pools de servidores de chat persistentes não oferece mais escalabilidade (você ainda pode ter apenas 80.000 usuários conectados simultaneamente em todos os seus pools de servidores de chat persistentes).</span><span class="sxs-lookup"><span data-stu-id="ef98a-138">Having multiple Persistent Chat Server pools does not give you more scale (you can still have only 80,000 concurrently connected users across all your Persistent Chat Server pools).</span></span> <span data-ttu-id="ef98a-139">O principal motivo para dar suporte a vários pools de servidores de chat persistentes é dar suporte a questões de regulamentação.</span><span class="sxs-lookup"><span data-stu-id="ef98a-139">The primary reason for supporting multiple Persistent Chat Server pools is to support regulatory concerns.</span></span>

    
    <span data-ttu-id="ef98a-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ef98a-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

