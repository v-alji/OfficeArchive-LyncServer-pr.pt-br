---
title: 'Lync Server 2013: funções de usuário no servidor de chat persistente'
description: 'Lync Server 2013: funções de usuário no servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User roles in Persistent Chat Server
ms:assetid: 343a0563-9ca5-4ad0-b4f3-a72f1d7f1a81
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ676774(v=OCS.15)
ms:contentKeyID: 49361095
ms.date: 03/19/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aed64aaa9129e6667cd138bc4365acfb2a64d52c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439153"
---
# <a name="user-roles-in-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="208b6-103">Funções de usuário no servidor de chat persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="208b6-103">User roles in Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="208b6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="208b6-104">

<span> </span></span></span>

<span data-ttu-id="208b6-105">_**Tópico da última modificação:** 2015-03-19_</span><span class="sxs-lookup"><span data-stu-id="208b6-105">_**Topic Last Modified:** 2015-03-19_</span></span>

<span data-ttu-id="208b6-106">O servidor de chat persistente fornece o conceito de membros permitidos/negados, que se aplicam a categorias de chat persistentes e controles que podem acessar salas em uma categoria específica.</span><span class="sxs-lookup"><span data-stu-id="208b6-106">Persistent Chat Server provides the concept of Allowed/Denied members, which applies to Persistent Chat categories and controls who can access rooms in a particular category.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="208b6-107">Os membros permitidos/negados em uma categoria não são iguais a uma função de <STRONG>membro</STRONG> , que se aplica a uma sala de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="208b6-107">Allowed/Denied members in a Category is not the same as a <STRONG>Member</STRONG> role, which applies to a Persistent Chat room.</span></span><BR><span data-ttu-id="208b6-108">Pesquisas exibem todas as salas de chat abertas e fechadas para as quais o usuário que está realizando a pesquisa está na lista de membros permitidos/recusados.</span><span class="sxs-lookup"><span data-stu-id="208b6-108">Searches display all open and closed chat rooms for which the user performing the search is in the Allowed/Denied member list.</span></span> <span data-ttu-id="208b6-109">Salas secretas não são exibidas, a menos que o usuário que fez a pesquisa seja membro de uma delas.</span><span class="sxs-lookup"><span data-stu-id="208b6-109">Secret rooms are not displayed unless the user who performs the search is a member of the secret room.</span></span> <span data-ttu-id="208b6-110">O usuário pode pesquisar apenas as salas das quais ele já é membro ou às quais ele pode solicitar associação.</span><span class="sxs-lookup"><span data-stu-id="208b6-110">The user can search only for rooms that he or she is already a member of, or those for which they can request membership.</span></span>



</div>

<span data-ttu-id="208b6-111">O motivo principal para o conceito de membros permitidos/negados é paredes éticas.</span><span class="sxs-lookup"><span data-stu-id="208b6-111">The primary rationale for the concept of Allowed/Denied Members is ethical walls.</span></span> <span data-ttu-id="208b6-112">Por exemplo, é comum que instituições bancárias e financeiras tenham limites éticos que impeçam investidores e analistas de compartilharem comunicações enquanto implementam políticas e convenções.</span><span class="sxs-lookup"><span data-stu-id="208b6-112">For example, it is common in banking and financial institutions to have ethical boundaries that prevent traders and analysts from sharing communications while implementing policies and conventions.</span></span> <span data-ttu-id="208b6-113">Para cumprir esse requisito, um administrador pode criar categorias de modo que uma categoria permita que salas sejam criadas e usadas por investidores e a outra categoria, por analistas.</span><span class="sxs-lookup"><span data-stu-id="208b6-113">To address this requirement, an administrator can create categories so that one category allows rooms to be created and used by traders, and another category allows rooms to be created and used by analysts.</span></span> <span data-ttu-id="208b6-114">Com essa restrição, o sistema proíbe a adição de um usuário como membro da sala se a categoria pai a impedir.</span><span class="sxs-lookup"><span data-stu-id="208b6-114">With this constraint is designed into the system prohibits adding a user as a member of the room if the parent category prevents it.</span></span>

<span data-ttu-id="208b6-115">Veja a seguir as quatro funções de usuário do servidor de chat persistente:</span><span class="sxs-lookup"><span data-stu-id="208b6-115">Following are the four user roles Persistent Chat Server:</span></span>

  - <span data-ttu-id="208b6-116">**Criador:** Usuários que têm permissões para criar salas de chat.</span><span class="sxs-lookup"><span data-stu-id="208b6-116">**Creator:** Users who have permissions to create chat rooms.</span></span> <span data-ttu-id="208b6-117">Esses usuários estão na lista Criadores de certas categorias: eles podem criar salas de chat naquela categoria e também atribuir associações de acordo com a categoria, bem como atribuir gerentes para administrarem a sala de chat.</span><span class="sxs-lookup"><span data-stu-id="208b6-117">These users are in the Creators list of certain categories: they can create chat rooms in that category, and they can also assign membership according to the category, and assign managers to manage the chat room.</span></span> <span data-ttu-id="208b6-118">O usuário que cria uma sala de chat é automaticamente adicionado como gerente da sala.</span><span class="sxs-lookup"><span data-stu-id="208b6-118">The user who creates a chat room is automatically added as a manager of the room.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="208b6-p104">A função de criador simplesmente concede direitos de criação de salas de chat. É a promoção automática a gerente que permite que o criador refine melhor as associações, os gerentes e assim por diante nos serviços de chat criados.</span><span class="sxs-lookup"><span data-stu-id="208b6-p104">Being a Creator simply provides rights for creating chat rooms. It is the automatic promotion to Manager that enables the Creator to further refine memberships, managers, and so on, on the created chat services.</span></span>

    
    </div>
    
    <span data-ttu-id="208b6-121">Esta função existe para lhe dar a opção de controlar quem cria salas de chat em sua organização, particularmente se quiser gerenciar centralmente a criação de salas de chat para impor políticas e convenções e, subsequentemente, delegar o gerenciamento das salas de chat a outros usuários na organização.</span><span class="sxs-lookup"><span data-stu-id="208b6-121">This role exists to give you the option of controlling who creates chat rooms in your organization, particularly if you want to centrally manage creating chat rooms to enforce policies and conventions, and subsequently delegate the chat room management to other users in the organization.</span></span>

  - <span data-ttu-id="208b6-122">**Gerente:** Usuários que gerenciam Propriedades de uma sala de chat.</span><span class="sxs-lookup"><span data-stu-id="208b6-122">**Manager:** Users who manage properties of a chat room.</span></span> <span data-ttu-id="208b6-123">Os gerentes de sala de chat podem modificar a lista de membros (adicionar e remover membros) e modificar a lista de gerentes da sala de chat (adicionar e remover gerentes).</span><span class="sxs-lookup"><span data-stu-id="208b6-123">Chat room managers can modify the member list (add and remove members), and modify the chat room managers list (add and remove managers).</span></span> <span data-ttu-id="208b6-124">Os gerentes de sala de chat podem adicionar a si próprios à lista de membros ou de apresentadores (para salas de auditório) para que possam participar da sala de chat.</span><span class="sxs-lookup"><span data-stu-id="208b6-124">Chat room managers can add themselves to the members or presenters list (for auditorium rooms) so they can participate in the chat room.</span></span> <span data-ttu-id="208b6-125">Os gerentes de sala de chat também podem desabilitar as salas de chat (os administradores podem consultar as salas de chat desabilitadas e excluí-las permanentemente).</span><span class="sxs-lookup"><span data-stu-id="208b6-125">Chat room managers can also disable chat rooms (administrators can query for disabled chat rooms and can permanently delete them).</span></span> <span data-ttu-id="208b6-126">Os gerentes podem alterar todas as propriedades de uma sala de chat, exceto sua categoria.</span><span class="sxs-lookup"><span data-stu-id="208b6-126">Managers can change all the properties of a chat room, except the category of the chat room.</span></span> <span data-ttu-id="208b6-127">Somente o administrador de chat persistente pode alterar a categoria após a criação da sala de chat.</span><span class="sxs-lookup"><span data-stu-id="208b6-127">Only the Persistent Chat Administrator can change the category after the chat room has been created.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="208b6-128">Se o gerente for também o criador em outra categoria, ele poderá alterar a categoria para que esteja autorizado a criar salas.</span><span class="sxs-lookup"><span data-stu-id="208b6-128">If the manager is also a Creator in another category, he or she can change the category to one where they are authorized to create rooms.</span></span>

    
    </div>

  - <span data-ttu-id="208b6-129">**Membro:** Usuários que são membros de uma sala de chat.</span><span class="sxs-lookup"><span data-stu-id="208b6-129">**Member:** Users who are members of a chat room.</span></span> <span data-ttu-id="208b6-130">Esses usuários podem ver as salas de chat no diretório (mesmo se a sala de chat for secreta), bem como assinar a sala de chat (incluindo opções de metadados, como mensagens não lidas, filtros ego e filtros de palavra-chave) e participar da sala de chat (pode postar, a menos que a sala seja uma sala Auditorium onde somente os apresentadores podem postar, obter conteúdo e Pesquisar</span><span class="sxs-lookup"><span data-stu-id="208b6-130">These users can see the chat rooms in the directory (even if the chat room is secret), as well as subscribe to the chat room (including metadata options such as unread messages, ego filters, and keyword filters), and participate in the chat room (can post, unless the room is an auditorium room where only presenters can post, get content, and search).</span></span> <span data-ttu-id="208b6-131">Os usuários que não são membros da sala de chat podem pesquisar a sala de chat se estiverem na lista de membros permitidos da categoria, mas precisarão solicitar acesso para participar dessas salas de chat para acessar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="208b6-131">Users who aren’t members of the chat room can search for the chat room if they are in the Allowed Members list of the category, but need to request access to join these chat rooms to access content.</span></span> <span data-ttu-id="208b6-132">(Não há nenhum acesso de solicitação ou aprovações embutidas no sistema; elas são feitas externamente por email, telefone ou outras formas de contato.)</span><span class="sxs-lookup"><span data-stu-id="208b6-132">(There is no request access or approvals built into the system; these are done externally by email, phone, or other forms of contact.)</span></span>

  - <span data-ttu-id="208b6-133">**Apresentador:** Usuários que podem postar em uma sala de Auditorium.</span><span class="sxs-lookup"><span data-stu-id="208b6-133">**Presenter:** Users who can post to an auditorium room.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="208b6-134">O servidor de chat persistente permite que os usuários criem e gerenciem a sala de chat para um site específico.</span><span class="sxs-lookup"><span data-stu-id="208b6-134">Persistent Chat Server lets users create and manage chat room for a specific site.</span></span> <span data-ttu-id="208b6-135">No entanto, os usuários não podem criar ou gerenciar salas de chat em outros sites na mesma topologia.</span><span class="sxs-lookup"><span data-stu-id="208b6-135">Users cannot, however, create or manage chat rooms on other sites within the same topology.</span></span> <span data-ttu-id="208b6-136">Certifique-se de especificar os criadores e gerentes da sala de chat para todos os sites da sua organização.</span><span class="sxs-lookup"><span data-stu-id="208b6-136">Be sure to specify chat room Creators and Managers for all the sites in your organization.</span></span>



</div>

<span data-ttu-id="208b6-137">As funções a seguir são funções de administrador para o servidor de chat persistente:</span><span class="sxs-lookup"><span data-stu-id="208b6-137">The following roles are administrator roles for Persistent Chat Server:</span></span>

  - <span data-ttu-id="208b6-138">**Administrador de chat persistente (CsPersistentChatAdministrator):** Esta é uma nova função de controle de acesso à Role-Based (RBAC) para administrar e gerenciar o servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="208b6-138">**Persistent Chat Administrator (CsPersistentChatAdministrator):** This is a new Role-Based Access Control (RBAC) role to administer and manage Persistent Chat Server.</span></span> <span data-ttu-id="208b6-139">Os usuários ou grupos de segurança designados como CsPersistentChatAdministrator são capazes de administrar o servidor de chat persistente usando cmdlets do Windows PowerShell remotamente (ou seja, de um computador que não seja o servidor de chat persistente).</span><span class="sxs-lookup"><span data-stu-id="208b6-139">Users or security groups designated as CsPersistentChatAdministrator are able administer Persistent Chat Server by using Windows PowerShell cmdlets remotely (that is, from a computer other than the Persistent Chat Server).</span></span> <span data-ttu-id="208b6-140">O servidor de chat persistente verifica se o administrador de chat persistente é membro do grupo local de administrador local do RTC no servidor de front-end do servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="208b6-140">Persistent Chat Server checks that the Persistent Chat Administrator is member of the RTC Local administrator local group on the Persistent Chat Server Front End Server.</span></span>
    
    <span data-ttu-id="208b6-141">A função CsPersistentChatAdministrator pode gerenciar salas de chat (modifique todas as propriedades, incluindo associação, gerentes, categorias, marcar salas como desabilitadas), bem como criar e gerenciar categorias de salas de chat que definem quem pode criar e acessar salas de chat.</span><span class="sxs-lookup"><span data-stu-id="208b6-141">The CsPersistentChatAdministrator role can manage chat rooms (modify all properties including membership, managers, categories, mark rooms as disabled), as well as create and manage chat room categories that define who can create and access chat rooms.</span></span> <span data-ttu-id="208b6-142">Administrators can also mark chat rooms as disabled and clean up chat rooms that are no longer active.</span><span class="sxs-lookup"><span data-stu-id="208b6-142">Administrators can also mark chat rooms as disabled and clean up chat rooms that are no longer active.</span></span> <span data-ttu-id="208b6-143">Administrators are not subject to the Creators or Allowed Members restrictions.</span><span class="sxs-lookup"><span data-stu-id="208b6-143">Administrators are not subject to the Creators or Allowed Members restrictions.</span></span> <span data-ttu-id="208b6-144">Administrators can create any kind of chat room and add themselves as a member to any chat room.</span><span class="sxs-lookup"><span data-stu-id="208b6-144">Administrators can create any kind of chat room and add themselves as a member to any chat room.</span></span> <span data-ttu-id="208b6-145">Os administradores também podem modificar e gerenciar a configuração de chat persistente (Propriedades do pool, configurações globais e configuração de conformidade) e também podem planejar e implementar a migração de uma implantação mais antiga do servidor de chat em grupo para o servidor de chat persistente do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="208b6-145">Administrators can also modify and manage Persistent Chat configuration (pool properties, global settings, and compliance configuration) and can also plan and implement migration from an older Group Chat Server deployment to Lync Server 2013 Persistent Chat Server.</span></span>

  - <span data-ttu-id="208b6-146">**Administrador do Lync:** Administrador corporativo geral do Lync Server 2013 responsável pela implantação.</span><span class="sxs-lookup"><span data-stu-id="208b6-146">**Lync Administrator:** Overall enterprise administrator for Lync Server 2013 responsible for deployment.</span></span>

  - <span data-ttu-id="208b6-147">**Gerenciador de operações:** Usuário responsável por gerenciar operações do dia a dia.</span><span class="sxs-lookup"><span data-stu-id="208b6-147">**Operations Manager:** User responsible for managing day-to-day operations.</span></span>

  - <span data-ttu-id="208b6-148">**Desenvolvedores e parceiros de terceiros:** Desenvolvedores de terceiros estendem o sistema, em particular, fornecendo uma solução de parede ética para conversas em grupo, suporte e ferramentas de conformidade, clientes da Web/móveis e uma estrutura para o desenvolvimento de bot.</span><span class="sxs-lookup"><span data-stu-id="208b6-148">**Third-party developers and partners:** Third-party developers extend the system, in particular providing an ethical wall solution for group conversations, compliance support and tools, web/mobile clients, and a framework for Bot development.</span></span>

<span data-ttu-id="208b6-149"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="208b6-149"></div>

<span> </span>

</div>

</div>

</span></span></div>

