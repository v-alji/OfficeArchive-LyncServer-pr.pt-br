---
title: Usando categorias para administrar o Servidor de Chat Persistente
description: Usar categorias para administrar o servidor de chat persistente.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Using categories to administer Persistent Chat Server
ms:assetid: dfcb3ad1-da90-467e-b08c-f4e68673b7b5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398988(v=OCS.15)
ms:contentKeyID: 48185628
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 181ecba944a042e3598b2964ad233590cf63349e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443159"
---
# <a name="using-categories-to-administer-persistent-chat-server"></a><span data-ttu-id="3d7ce-103">Usando categorias para administrar o Servidor de Chat Persistente</span><span class="sxs-lookup"><span data-stu-id="3d7ce-103">Using categories to administer Persistent Chat Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3d7ce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3d7ce-104">

<span> </span></span></span>

<span data-ttu-id="3d7ce-105">_**Tópico da última modificação:** 2013-10-01_</span><span class="sxs-lookup"><span data-stu-id="3d7ce-105">_**Topic Last Modified:** 2013-10-01_</span></span>

<span data-ttu-id="3d7ce-106">Sua implantação do servidor de chat persistente pode hospedar muitas salas de chat persistentes persistentes.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-106">Your Persistent Chat Server deployment can host many concurrent Persistent Chat rooms.</span></span> <span data-ttu-id="3d7ce-107">Essas salas podem ser organizadas em um conjunto de categorias no servidor.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-107">Chat rooms can be organized into a set of categories on the server.</span></span> <span data-ttu-id="3d7ce-108">Cada sala de chat pertence a uma categoria e herda algumas configurações dessa categoria.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-108">Each chat room belongs to one category, and inherits some settings from that category.</span></span> <span data-ttu-id="3d7ce-109">Essa organização cria uma estrutura útil para identificar conversas, com base no objetivo comercial, bem como facilita a administração delegada e o gerenciamento simplificado.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-109">This organization creates a useful structure for identifying conversations, based on their business purpose, and facilitates delegated administration and simplified management.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3d7ce-110">Embora muitos dos recursos de gerenciamento de salas de chat estejam disponíveis em computadores que executam o chat persistente (cliente do Lync) para o usuário, os administradores de chat persistente (na função <STRONG>cspersistentchatadministrator</STRONG> ) devem usar o painel de controle do Lync Server ou cmdlets do Windows PowerShell para criar ou gerenciar categorias.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-110">Although many of the management features of chat rooms are available in computers running Persistent Chat (Lync client) for the user, Persistent Chat Administrators (in the <STRONG>cspersistentchatadministrator</STRONG> role) must use the Lync Server Control Panel or Windows PowerShell cmdlets to create or manage categories.</span></span>



</div>

<span data-ttu-id="3d7ce-111">Administradores de chat persistentes usam o painel de controle do Lync Server ou cmdlets do Windows PowerShell para criar e gerenciar categorias e para criar acesso a salas de chat para os usuários de sua organização.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-111">Persistent Chat administrators use Lync Server Control Panel or Windows PowerShell cmdlets to create and manage categories, and to design access for chat rooms for the users in their organization.</span></span>

<span data-ttu-id="3d7ce-112">Os gerentes de sala de chat persistentes, que têm a capacidade de gerenciar uma ou mais salas de chat, podem usar o cliente do Lync para iniciar um aplicativo Web de gerenciamento de salas para criar e gerenciar salas (ou clientes podem criar soluções e fluxos de trabalho personalizados para serem invocados).</span><span class="sxs-lookup"><span data-stu-id="3d7ce-112">Persistent Chat room managers, who have the ability to manage one or more chat rooms, can use the Lync client to launch a room management Web application to create and manage rooms (or customers can create custom solutions and workflows to be invoked).</span></span> <span data-ttu-id="3d7ce-113">Os administradores de chat persistente também podem usar o painel de controle do Lync Server ou cmdlets do Windows PowerShell para criar e gerenciar salas.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-113">Persistent Chat administrators can also use Lync Server Control Panel or Windows PowerShell cmdlets to create and manage rooms.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3d7ce-114">Uma sala de chat persistente não pode ter o mesmo nome de uma categoria de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-114">A Persistent Chat room cannot have the same name as a Persistent Chat category.</span></span>



</div>

<span data-ttu-id="3d7ce-p103">Os gerentes de salas de chat podem fazer alterações em todas as propriedades dessas salas, exceto alterar a sua categoria. Eles devem ter permissão para executar as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="3d7ce-p103">Chat room managers can make changes to all chat room properties, except for changing the category of the room. They cannot be restricted from performing the following actions:</span></span>

  - <span data-ttu-id="3d7ce-117">Desabilitar uma sala de chat</span><span class="sxs-lookup"><span data-stu-id="3d7ce-117">Disabling a chat room</span></span>

  - <span data-ttu-id="3d7ce-118">Alterar o nome de uma sala de chat</span><span class="sxs-lookup"><span data-stu-id="3d7ce-118">Changing a chat room name</span></span>

  - <span data-ttu-id="3d7ce-119">Alterar a descrição de uma sala de chat</span><span class="sxs-lookup"><span data-stu-id="3d7ce-119">Changing a chat room description</span></span>

  - <span data-ttu-id="3d7ce-120">Alterar um tipo de sala de chat (Auditório versus Normal)</span><span class="sxs-lookup"><span data-stu-id="3d7ce-120">Changing a chat room type (Auditorium versus Normal)</span></span>

  - <span data-ttu-id="3d7ce-121">Alterar a privacidade de uma sala (aberta verso fechada verso secreta)</span><span class="sxs-lookup"><span data-stu-id="3d7ce-121">Changing the privacy of a room (open versus closed versus secret)</span></span>

  - <span data-ttu-id="3d7ce-122">Adicionar ou remover membros</span><span class="sxs-lookup"><span data-stu-id="3d7ce-122">Adding or removing members</span></span>

  - <span data-ttu-id="3d7ce-123">Adicionar ou remover gerentes de salas de chat</span><span class="sxs-lookup"><span data-stu-id="3d7ce-123">Adding or removing chat room managers</span></span>

  - <span data-ttu-id="3d7ce-124">Adicionar ou remover um suplemento</span><span class="sxs-lookup"><span data-stu-id="3d7ce-124">Adding or removing an add-in</span></span>

  - <span data-ttu-id="3d7ce-125">Alterar configurações, como convites (de acordo com o que é permitido pela categoria)</span><span class="sxs-lookup"><span data-stu-id="3d7ce-125">Changing settings such as invitations (according to what’s permitted by the category)</span></span>

<div>

## <a name="delegated-administration"></a><span data-ttu-id="3d7ce-126">Administração delegada</span><span class="sxs-lookup"><span data-stu-id="3d7ce-126">Delegated Administration</span></span>

<span data-ttu-id="3d7ce-127">Criar e gerenciar salas de chat persistente é muito mais fácil com o uso correto de categorias.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-127">Creating and managing Persistent Chat rooms is much easier with the correct use of categories.</span></span> <span data-ttu-id="3d7ce-128">Um administrador de chat persistente pode definir **AllowedMembers** e **criadores** para cada categoria e também pode definir as configurações e os comportamentos padrão da sala de chat que serão aplicados a todas as salas de chat criadas na categoria.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-128">A Persistent Chat Administrator can define **AllowedMembers** and **Creators** for each category, and can also define the default chat room settings and behaviors that will be applied to all chat rooms created in the category.</span></span> <span data-ttu-id="3d7ce-129">Administradores de chat persistentes criam e gerenciam categorias usando o painel de controle do Lync Server ou cmdlets do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-129">Persistent Chat administrators create and manage categories by using Lync Server Control Panel or Windows PowerShell cmdlets.</span></span>

<span data-ttu-id="3d7ce-p105">Usuários, Unidades Organizacionais (OUs) e grupos de usuários identificados como Criadores da categoria são os únicos indivíduos e grupos que porem criar salas na categoria. Após a categoria ser criada, eles podem escolher usuários, OUs e grupos de usuários da lista  **AllowedMembers** da categoria como gerentes da sala de chat e membros para gerenciar e participar da sala.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-p105">Users, Organizational Units (OUs), and user groups that are identified as Creators of the category are the only individuals and groups that are allowed to create rooms in the category. After the category is created, they can choose users, OUs, and user groups from the category’s **AllowedMembers** list as chat room managers and members to manage and participate in the room.</span></span>

<span data-ttu-id="3d7ce-132">As salas de chat criadas em uma categoria aderem às políticas e configurações impostas pela categoria (por exemplo, quem pode estar na associação da sala, quem pode gerenciar a sala, se os carregamentos de arquivo são permitidos, se os convites são enviados e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="3d7ce-132">Chat rooms that are created in a category adhere to the policies and settings enforced by the category (such as who can be in the room’s membership, who can manage the room, whether file uploads are allowed, whether invitations are sent, and so on).</span></span>

<span data-ttu-id="3d7ce-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3d7ce-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

