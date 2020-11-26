---
title: 'Lync Server 2013: Habilitar política de Servidor de Chat Persistente'
description: 'Lync Server 2013: habilitar a política de servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Persistent Chat Server policy
ms:assetid: 87063d6c-2e38-4970-b76d-2aa15f0de29e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205056(v=OCS.15)
ms:contentKeyID: 48184718
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e58da577679795f00492af72b43ca72106d40f4f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428836"
---
# <a name="enable-persistent-chat-server-policy-in-lync-server-2013"></a><span data-ttu-id="e5396-103">Habilitar política de Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5396-103">Enable Persistent Chat Server policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e5396-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e5396-104">

<span> </span></span></span>

<span data-ttu-id="e5396-105">_**Tópico da última modificação:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="e5396-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="e5396-106">No painel de controle do Lync Server 2013, você pode usar a página **política de chat persistente** do grupo de **chat persistente** para gerenciar políticas em um nível global, de pool, de site ou de usuário, incluindo a configuração da política global padrão e a criação de uma ou mais políticas de usuário e de site adicionais para a sua implantação.</span><span class="sxs-lookup"><span data-stu-id="e5396-106">In the Lync Server 2013 Control Panel, you can use the **Persistent Chat Policy** page of the **Persistent Chat** group to manage policies at a global, pool, site, or user level, including configuring the default global policy and creating one or more additional user and site policies for your deployment.</span></span> <span data-ttu-id="e5396-107">Se um usuário estiver habilitado para o servidor de chat persistente por política, o ambiente do servidor de chat persistente aparecerá no cliente do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="e5396-107">If a user is enabled for Persistent Chat Server by policy, then the Persistent Chat Server environment appears in their Lync 2013 client.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e5396-108">Na topologia, as políticas de site do servidor de chat persistente se aplicam globalmente, o pool de cada usuário ou o site de cada usuário ou por usuário.</span><span class="sxs-lookup"><span data-stu-id="e5396-108">In the topology, Persistent Chat Server site policies apply globally, per user’s pool, or per user’s site, or per user.</span></span>



</div>

<span data-ttu-id="e5396-109">A política global é criada automaticamente quando você implanta um servidor de chat persistente, e pode ser configurada, mas não excluída.</span><span class="sxs-lookup"><span data-stu-id="e5396-109">The global policy is created automatically when you deploy Persistent Chat Server, and it can be configured, but not deleted.</span></span> <span data-ttu-id="e5396-110">Como ela se aplica a todos os usuários, não é necessário defini-la por usuário.</span><span class="sxs-lookup"><span data-stu-id="e5396-110">Because the global policy applies to all users, it doesn’t have to be set per user.</span></span>

<span data-ttu-id="e5396-111">Você pode criar e configurar várias políticas de site e de usuário, juntamente com a política global, habilitar usuários para o servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="e5396-111">You can create and configure multiple site and user policies which, together with the global policy, enable users for Persistent Chat Server.</span></span> <span data-ttu-id="e5396-112">As políticas de servidor de chat persistente do pool e do site substituem a política global de servidor de chat persistente, mas somente para os usuários desse site.</span><span class="sxs-lookup"><span data-stu-id="e5396-112">Pool and site Persistent Chat Server policies override the global Persistent Chat Server policy, but only for users of that site.</span></span> <span data-ttu-id="e5396-113">As políticas de usuário substituem as políticas globais, de pool e de site para os usuários aos quais são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="e5396-113">User policies override both global, pool, and site policies for the users to whom the user policy is assigned.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e5396-114">Para configurar e usar o servidor de chat persistente, você deve primeiro usar o construtor de topologias para adicionar suporte a servidor de chat persistente à topologia e, em seguida, publicar a topologia.</span><span class="sxs-lookup"><span data-stu-id="e5396-114">To configure and use Persistent Chat Server, you must first use Topology Builder to add Persistent Chat Server support to the topology, and then publish the topology.</span></span> <span data-ttu-id="e5396-115">Para obter detalhes, consulte <A href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">adicionando servidor de chat persistente à sua implantação no Lync Server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="e5396-115">For details, see <A href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Adding Persistent Chat Server to your deployment in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e5396-116">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="e5396-116">In This Section</span></span>

  - [<span data-ttu-id="e5396-117">Configurar a política global para Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5396-117">Configure the global policy for Persistent Chat in Lync Server 2013</span></span>](lync-server-2013-configure-the-global-policy-for-persistent-chat.md)

  - [<span data-ttu-id="e5396-118">Criar uma política de site para chat persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5396-118">Create a site policy for Persistent Chat in Lync Server 2013</span></span>](lync-server-2013-create-a-site-policy-for-persistent-chat.md)

  - [<span data-ttu-id="e5396-119">Criar uma política de usuário para Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5396-119">Create a user policy for Persistent Chat in Lync Server 2013</span></span>](lync-server-2013-create-a-user-policy-for-persistent-chat.md)

  - [<span data-ttu-id="e5396-120">Aplicar uma política de Chat Persistente a um usuário ou grupo de usuários no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5396-120">Apply a Persistent Chat policy to a user or user group in Lync Server 2013</span></span>](lync-server-2013-apply-a-persistent-chat-policy-to-a-user-or-user-group.md)

<span data-ttu-id="e5396-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e5396-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

