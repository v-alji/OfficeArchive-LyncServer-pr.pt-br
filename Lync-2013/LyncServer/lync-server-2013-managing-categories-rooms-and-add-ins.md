---
title: 'Lync Server 2013: Gerenciando categotias, salas e suplementos'
description: 'Lync Server 2013: gerenciar categorias, salas e suplementos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing categories, rooms, and add-ins
ms:assetid: a9807031-7369-4a51-9369-6f09bec24141
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412799(v=OCS.15)
ms:contentKeyID: 48185100
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba09ed3e021ba24f424d28bbb2c5c379ab975741
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425952"
---
# <a name="managing-categories-rooms-and-add-ins-in-lync-server-2013"></a><span data-ttu-id="165ae-103">Gerenciando categotias, salas e suplementos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="165ae-103">Managing categories, rooms, and add-ins in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="165ae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="165ae-104">

<span> </span></span></span>

<span data-ttu-id="165ae-105">_**Tópico da última modificação:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="165ae-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="165ae-106">No painel de controle do Lync Server 2013 ou usando cmdlets do Windows PowerShell, administradores de chat persistente podem usar a página de **chat persistente** para criar categorias e suplementos. Para gerenciar salas de chat persistente, os administradores podem usar cmdlets do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="165ae-106">In Lync Server 2013 Control Panel, or by using Windows PowerShell cmdlets, Persistent Chat Administrators can use the **Persistent Chat** page to create categories and add-ins. For managing Persistent Chat rooms, Administrators can use Windows PowerShell cmdlets.</span></span> <span data-ttu-id="165ae-107">Como alternativa, se o administrador de chat persistente também estiver habilitado para SIP, ele poderá usar o cliente do Lync para iniciar uma página da Web para criar e gerenciar salas de chat.</span><span class="sxs-lookup"><span data-stu-id="165ae-107">Alternatively, if the Persistent Chat administrator is also SIP-enabled, they can use the Lync client to launch a web page to create and manage chat rooms.</span></span>

<span data-ttu-id="165ae-108">Os tópicos a seguir descrevem como criar e trabalhar com categorias e salas de chat.</span><span class="sxs-lookup"><span data-stu-id="165ae-108">The following topics describe how to create and work with categories and chat rooms.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="165ae-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="165ae-109">In This Section</span></span>

  - [<span data-ttu-id="165ae-110">Criando ou editando uma nova categoria no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="165ae-110">Creating or editing a new category in Lync Server 2013</span></span>](lync-server-2013-creating-or-editing-a-new-category.md)

  - [<span data-ttu-id="165ae-111">Criando ou editando uma nova sala no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="165ae-111">Creating or editing a new room in Lync Server 2013</span></span>](lync-server-2013-creating-or-editing-a-new-room.md)

  - [<span data-ttu-id="165ae-112">Criando novos suplementos para salas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="165ae-112">Creating new add-ins for rooms in Lync Server 2013</span></span>](lync-server-2013-creating-new-add-ins-for-rooms.md)

  - [<span data-ttu-id="165ae-113">Determinar quem pode postar mensagens na sala de chat do auditório no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="165ae-113">Setting who can post messages in an auditorium chat room in Lync Server 2013</span></span>](lync-server-2013-setting-who-can-post-messages-in-an-auditorium-chat-room.md)

  - [<span data-ttu-id="165ae-114">Habilitar ou desabilitar uma sala de chat no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="165ae-114">Disabling or enabling a chat room in Lync Server 2013</span></span>](lync-server-2013-disabling-or-enabling-a-chat-room.md)

  - [<span data-ttu-id="165ae-115">Movendo uma sala de chat de uma categoria a outra no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="165ae-115">Moving a chat room from one category to another in Lync Server 2013</span></span>](lync-server-2013-moving-a-chat-room-from-one-category-to-another.md)

  - [<span data-ttu-id="165ae-116">Excluindo sala de chat ou categoria no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="165ae-116">Deleting a chat room or category in Lync Server 2013</span></span>](lync-server-2013-deleting-a-chat-room-or-category.md)

  - [<span data-ttu-id="165ae-117">Excluindo uma mensagem ou limpando mensagens obsoletas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="165ae-117">Deleting a message or purging obsolete messages in Lync Server 2013</span></span>](lync-server-2013-deleting-a-message-or-purging-obsolete-messages.md)

<span data-ttu-id="165ae-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="165ae-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

