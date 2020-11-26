---
title: 'Lync Server 2013: Criar uma política de usuário para Chat Persistente'
description: 'Lync Server 2013: criar uma política de usuário para chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a user policy for Persistent Chat
ms:assetid: aa3774af-d442-4206-8a68-2fbb9102e9d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205170(v=OCS.15)
ms:contentKeyID: 48185103
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1fcbe761d535f8c58c2f83750cdc8808cfb62634
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432076"
---
# <a name="create-a-user-policy-for-persistent-chat-in-lync-server-2013"></a><span data-ttu-id="3b1a8-103">Criar uma política de usuário para Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3b1a8-103">Create a user policy for Persistent Chat in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3b1a8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3b1a8-104">

<span> </span></span></span>

<span data-ttu-id="3b1a8-105">_**Tópico da última modificação:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="3b1a8-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="3b1a8-106">No painel de controle do Lync Server, você define as políticas de usuário que podem ser atribuídas aos usuários nos **usuários**.</span><span class="sxs-lookup"><span data-stu-id="3b1a8-106">In the Lync Server Control Panel, you define user policies that can be assigned to users in **Users**.</span></span>

<span data-ttu-id="3b1a8-107">A política de usuário substitui as políticas globais e de site, mas apenas para os usuários específicos aos quais ela é atribuída.</span><span class="sxs-lookup"><span data-stu-id="3b1a8-107">The user policy overrides the global policy and site policies, but only for the specific users who are assigned the user policy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3b1a8-108">Para configurar e usar o servidor de chat persistente, você deve primeiro usar o construtor de topologias para adicionar suporte a servidor de chat persistente à topologia e, em seguida, publicar a topologia.</span><span class="sxs-lookup"><span data-stu-id="3b1a8-108">To configure and use Persistent Chat Server, you must first use Topology Builder to add Persistent Chat Server support to the topology, and then publish the topology.</span></span> <span data-ttu-id="3b1a8-109">Para obter detalhes, consulte <A href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">adicionando servidor de chat persistente à sua implantação no Lync Server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="3b1a8-109">For details, see <A href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Adding Persistent Chat Server to your deployment in Lync Server 2013</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="3b1a8-110">Para definir as configurações de servidor de chat persistente, consulte <A href="lync-server-2013-configure-persistent-chat-server-options-globally-or-for-persistent-chat-server-pool.md">Configurar opções do servidor de chat persistente globalmente ou para pool de servidores de chat persistente no Lync server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="3b1a8-110">To configure Persistent Chat Server configuration settings, see <A href="lync-server-2013-configure-persistent-chat-server-options-globally-or-for-persistent-chat-server-pool.md">Configure Persistent Chat Server options globally or for Persistent Chat Server pool in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-create-a-user-policy-for-persistent-chat"></a><span data-ttu-id="3b1a8-111">Para criar uma política de usuário para chat persistente</span><span class="sxs-lookup"><span data-stu-id="3b1a8-111">To create a user policy for Persistent Chat</span></span>

1.  <span data-ttu-id="3b1a8-112">Usando uma conta de usuário atribuída à função CsPersistentChatAdministrator, CsAdministrator, ou CsUserAdministrator faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="3b1a8-112">From a user account that is assigned to the CsPersistentChatAdministrator, CsAdministrator, or CsUserAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="3b1a8-113">No menu **Iniciar** , selecione o painel de controle do Lync Server ou abra uma janela do navegador e, em seguida, insira a URL de administração.</span><span class="sxs-lookup"><span data-stu-id="3b1a8-113">From the **Start** menu, select the Lync Server Control Panel or open a browser window, and then enter the Admin URL.</span></span> <span data-ttu-id="3b1a8-114">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3b1a8-114">For details about the different methods that you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="3b1a8-115">Você também pode usar cmdlets do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3b1a8-115">You can also use Windows PowerShell cmdlets.</span></span> <span data-ttu-id="3b1a8-116">Consulte <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">Configurando o servidor de chat persistente usando cmdlets do Windows PowerShell</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="3b1a8-116">See <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</A> in the Deployment documentation.</span></span>

    
    </div>

3.  <span data-ttu-id="3b1a8-117">Na barra de navegação esquerda, clique em **Chat Persistente** e, em seguida, clique em **Política de Chat Persistente**.</span><span class="sxs-lookup"><span data-stu-id="3b1a8-117">In the left navigation bar, click **Persistent Chat**, and then click **Persistent Chat Policy**.</span></span>

4.  <span data-ttu-id="3b1a8-118">Clique em **Novo** e em **Política de usuário**.</span><span class="sxs-lookup"><span data-stu-id="3b1a8-118">Click **New**, and then click **User policy**.</span></span>

5.  <span data-ttu-id="3b1a8-119">Em **Nova Política de Chat Persistente**, siga este procedimento:</span><span class="sxs-lookup"><span data-stu-id="3b1a8-119">In **New Persistent Chat Policy**, do the following:</span></span>
    
      - <span data-ttu-id="3b1a8-120">Em **Nome**, especifique um nome para a nova política de usuário.</span><span class="sxs-lookup"><span data-stu-id="3b1a8-120">In **Name**, specify a name for the new user policy.</span></span>
    
      - <span data-ttu-id="3b1a8-121">Em **Descrição**, forneça detalhes sobre o que é a política de usuário (por exemplo, política de chat persistente para um usuário específico).</span><span class="sxs-lookup"><span data-stu-id="3b1a8-121">In **Description**, provide details about what the user policy is (for example, Persistent Chat policy for specific user).</span></span>
    
      - <span data-ttu-id="3b1a8-122">Para controlar o chat persistente para todos os usuários que não são controlados especificamente por meio de uma política de usuário, marque ou desmarque a caixa de seleção **habilitar chat persistente** .</span><span class="sxs-lookup"><span data-stu-id="3b1a8-122">To control Persistent Chat for all users who are not specifically controlled through a user policy, select or clear the **Enable Persistent Chat** check box.</span></span>

6.  <span data-ttu-id="3b1a8-123">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="3b1a8-123">Click **Commit**.</span></span>

<span data-ttu-id="3b1a8-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3b1a8-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

