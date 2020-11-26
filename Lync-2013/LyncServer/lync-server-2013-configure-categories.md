---
title: 'Lync Server 2013: Configurar categorias'
description: 'Lync Server 2013: configurar categorias.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure categories
ms:assetid: 4547f514-f0c0-404d-890f-092ddeeac852
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204859(v=OCS.15)
ms:contentKeyID: 48184033
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1342ea0f5ee32284a32ac0dcc8ab3d370bb1dd91
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434015"
---
# <a name="configure-categories-in-lync-server-2013"></a><span data-ttu-id="d9ac6-103">Configurar categorias no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d9ac6-103">Configure categories in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d9ac6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d9ac6-104">

<span> </span></span></span>

<span data-ttu-id="d9ac6-105">_**Tópico da última modificação:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="d9ac6-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="d9ac6-106">No painel de controle do Lync Server 2013, você pode usar a seção **categoria** da página de **chat persistente** para configurar categorias.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-106">In Lync Server 2013 Control Panel, you can use the **Category** section of the **Persistent Chat** page to configure categories.</span></span> <span data-ttu-id="d9ac6-107">Uma categoria de sala de chat persistente é uma estrutura lógica para organizar salas de chat.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-107">A Persistent Chat room category is a logical structure for organizing chat rooms.</span></span> <span data-ttu-id="d9ac6-108">Uma categoria define um conjunto padrão de listas de controle de acesso (ACLs) para controle dos usuários e dos grupos de usuários que podem criar ou ingressar em salas de chat.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-108">A category defines a default set of access control lists (ACLs) for controlling the users and user groups who may create or join the chat rooms.</span></span> <span data-ttu-id="d9ac6-109">É possível usar as categorias para aplicar paredes éticas entre diferentes subdivisões dentro de suas organizações.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-109">You can use categories enforce ethical walls between different subdivisions within their organizations.</span></span>

<span data-ttu-id="d9ac6-110">As categorias de sala de chat podem conter salas de chat, mas nenhuma outra categoria.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-110">Chat room categories may contain chat rooms, but not other categories.</span></span> <span data-ttu-id="d9ac6-111">Cada categoria descreve o conteúdo com metadados, como Name e Description.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-111">Each category describes its contents with metadata, such as Name and Description.</span></span> <span data-ttu-id="d9ac6-112">Além disso, a categoria tem propriedades as quais podem ser definidas para controlar o comportamento das salas de bate-papo pertencentes, como se as salas de chat permitissem  Invitations ou File Uploads ou contivessem Chat History.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-112">In addition, the category has properties which can be set to control the behavior of the chat rooms belonging to it, such as if the chat rooms allow Invitations or File Uploads, or contain Chat History.</span></span>

<div>

## <a name="to-configure-categories-for-chat-rooms"></a><span data-ttu-id="d9ac6-113">Para configurar categorias salas de bate-papo</span><span class="sxs-lookup"><span data-stu-id="d9ac6-113">To configure categories for chat rooms</span></span>

1.  <span data-ttu-id="d9ac6-114">A partir de uma conta de usuário com a função CsPersistentChatAdministrator ou CsAdministrator atribuída, faça o logon em qualquer computador na sua implementação interna.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-114">From a user account that is assigned to the CsPersistentChatAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d9ac6-115">No menu **Iniciar** , selecione o painel de controle do Lync Server ou abra uma janela do navegador e, em seguida, insira a URL de administração.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-115">From the **Start** menu, select the Lync Server Control Panel or open a browser window, and then enter the Admin URL.</span></span> <span data-ttu-id="d9ac6-116">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d9ac6-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="d9ac6-117">Você também pode usar cmdlets do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-117">You can also use Windows PowerShell cmdlets.</span></span> <span data-ttu-id="d9ac6-118">Para obter detalhes, consulte <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">Configurando o servidor de chat persistente usando cmdlets do Windows PowerShell</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-118">For details, see <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</A> in the Deployment documentation.</span></span>

    
    </div>

3.  <span data-ttu-id="d9ac6-119">Na barra de navegação esquerda, clique em **Chat Persistente** e clique em **Categoria**.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-119">In the left navigation bar, click **Persistent Chat**, and then click **Category**.</span></span>
    
    <span data-ttu-id="d9ac6-120">Para várias implantações de pool do servidor de chat persistente, selecione o pool apropriado na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-120">For multiple Persistent Chat Server pool deployments, select the appropriate pool from the drop-down list.</span></span>

4.  <span data-ttu-id="d9ac6-121">Na página **Categoria**, clique em **Novo** ou **Editar**.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-121">On the **Category** page, click **New** or **Edit**.</span></span>

5.  <span data-ttu-id="d9ac6-122">Em **selecionar um serviço**, selecione o serviço correspondente ao pool de servidores de chat persistente em que a categoria precisa ser criada.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-122">In **Select a Service**, select the service corresponding to the Persistent Chat Server pool on which the category needs to be created.</span></span> <span data-ttu-id="d9ac6-123">O serviço é o pool persistente do servidor de chat que o chat (cliente) persistente usa para identificar a qual pool a categoria pertence.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-123">The service is the Persistent Chat Server pool that the Persistent Chat (client) uses to identify which pool the category belongs to.</span></span> <span data-ttu-id="d9ac6-124">Uma categoria pode pertencer a apenas um pool de servidor de chat persistente e não pode ser movida para outra ou compartilhada com outro pool.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-124">A category can belong to only one Persistent Chat Server pool, and cannot be moved to another one, or shared with another pool.</span></span>

6.  <span data-ttu-id="d9ac6-125">Em **Nova categoria**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d9ac6-125">In **New Category**, do the following:</span></span>
    
    1.  <span data-ttu-id="d9ac6-126">Em  **Nome**, especifique um nome para a nova categoria de sala.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-126">In **Name**, specify a name for the new room category.</span></span>
    
    2.  <span data-ttu-id="d9ac6-127">Em  **Descrição**, forneça uma descrição detalhada para a categoria da sala (por exemplo, uma categoria de sala para Contoso).</span><span class="sxs-lookup"><span data-stu-id="d9ac6-127">In **Description**, provide a detailed description for the room category (for example, a room category for Contoso).</span></span>
    
    3.  <span data-ttu-id="d9ac6-128">Para controlar se os convites podem ser ativados por salas de chat que pertencem a tal categoria, selecione ou limpe a caixa de marcação **Habilitar convites**.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-128">To control whether invitations can be enabled for chat rooms that belong to this category, select or clear the **Enable invitations** check box.</span></span> <span data-ttu-id="d9ac6-129">Se marcado, as salas nesta categoria poderão ter convites ativados ou desativados; em caso de não marcado, as salas nessa categoria não podem ter convite.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-129">If selected, rooms in this category may have invitations on or off; if cleared, the rooms in this category are not allowed to have invitations.</span></span> <span data-ttu-id="d9ac6-130">Se uma sala tem convites em, quando um novo membro é adicionado a uma sala, ele recebe uma notificação da nova sala em seu cliente de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-130">If a room has invitations on, when a new member is added to a room, he or she gets a notification of the new room in their Persistent Chat client.</span></span>
    
    4.  <span data-ttu-id="d9ac6-p107">Para controlar o envio de arquivo nas salas de chat pertencentes a esta categoria, selecione ou desmarque a caixa de seleção **Habilitar carregamento de arquivo**. Se estiver marcada, as salas desta categoria podem habilitar ou desabilitar carregamentos de arquivos; se estiver desmarcada, as salas nesta categoria não podem ter arquivos carregados.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-p107">To control file uploads in chat rooms belonging to this category, select or clear the **Enable file upload** check box. If selected, the rooms of this category can enable or disable file uploads; if cleared, the rooms of this category are not allowed to have file uploads.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="d9ac6-133">Essa configuração é imposta no servidor porque aplicativos personalizados ou clientes de chat em grupo anterior que usam o servidor de chat de grupo do Office Communications Server 2007 R2 &nbsp; ou o Lync server 2010, o chat em grupo podem postar arquivos para uma sala.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-133">This setting is enforced on the server because custom applications or previous Group Chat clients that use Office Communications Server 2007 R2&nbsp;Group Chat Server or Lync Server 2010, Group Chat can post files to a room.</span></span> <span data-ttu-id="d9ac6-134">O cliente do Lync 2013 não tem recurso de carregamento/download de arquivo, portanto, se você tiver uma implantação do Lync 2013 ou do Lync 2013, não será possível postar arquivos em uma sala de chat do servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-134">The Lync 2013 client does not have file upload/download capability, so if you have a pure Lync 2013 deployment or Lync 2013 client, it is not possible to post files in a Persistent Chat Server chat room.</span></span>

        
        </div>
    
    5.  <span data-ttu-id="d9ac6-135">Para controlar o histórico de chats, marque ou desmarque a caixa de seleção **habilitar histórico de chats** .</span><span class="sxs-lookup"><span data-stu-id="d9ac6-135">To control chat history, select or clear the **Enable chat history** check box.</span></span> <span data-ttu-id="d9ac6-136">Se marcada, as salas de chat se tornam persistentes; caso contrário, as mensagens de chat não são persistentes.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-136">If selected, room chats become persistent; otherwise, chat messages are not persisted.</span></span> <span data-ttu-id="d9ac6-137">Se a conformidade estiver habilitada, as salas de chat serão salvas em conformidade, mas os usuários não poderão acessar mensagens antigas.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-137">If compliance is enabled, room chats will be saved in compliance, but users will not be able to access older messages.</span></span> <span data-ttu-id="d9ac6-138">Essa opção pode ser utilizada para salas designadas para colaborações em tempo real e ad hoc que não precisam do histórico de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-138">This option can be used for rooms designated for real-time, ad hoc collaborations that don’t need chat history to be persisted.</span></span>

7.  <span data-ttu-id="d9ac6-139">Em  **Editar categoria**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d9ac6-139">In **Edit Category**, do the following:</span></span>
    
      - <span data-ttu-id="d9ac6-140">Em **Associação**, na seção **Membros permitidos** , adicione ou remova usuários e outras entidades de segurança dos serviços de domínio Active Directory (usuários, grupos de distribuição, unidades organizacionais e assim por diante) que podem ser adicionados como membros de salas de chat pertencentes à categoria.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-140">In **Membership**, in the **Allowed members** section, add or remove users and other Active Directory Domain Services principals (users, distribution groups, organizational units, and so on) that are permitted to be added as members of chat rooms belonging to the category.</span></span> <span data-ttu-id="d9ac6-141">As entidades permitidas por uma categoria podem pesquisar por salas na categoria (a menos que uma sala esteja oculta, caso o qual apenas membros da sala podem pesquisar por ela no diretório).</span><span class="sxs-lookup"><span data-stu-id="d9ac6-141">Principals permitted by a category can search for the rooms in the category (unless the room is hidden, in which case only members of the room can search for it in the directory).</span></span>
    
      - <span data-ttu-id="d9ac6-142">Em **Associação**, na seção **Membros negados** , adicione ou remova usuários e outras entidades de segurança do Active Directory associadas a membros sendo negados da sala.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-142">In **Membership**, in the **Denied members** section, add or remove users and other Active Directory principals associated with members being denied from the room.</span></span>
    
      - <span data-ttu-id="d9ac6-143">Em **Associação**, na seção **criadores** , adicione ou remova usuários e outras entidades de segurança do Active Directory associadas aos criadores para a categoria.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-143">In **Membership**, in the **Creators** section, add or remove users and other Active Directory principals associated with creators for the category.</span></span> <span data-ttu-id="d9ac6-144">Um criador é um usuário que tem permissões de criar salas de chat e atribuir gerentes e membros de sala de chat.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-144">A creator is a user who has permissions to create chat rooms and assign chat room managers and members.</span></span>

8.  <span data-ttu-id="d9ac6-145">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="d9ac6-145">Click **Commit**.</span></span>

<span data-ttu-id="d9ac6-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d9ac6-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

