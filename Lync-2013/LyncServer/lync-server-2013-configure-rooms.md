---
title: 'Lync Server 2013: Configurar salas'
description: 'Lync Server 2013: configurar salas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure rooms
ms:assetid: 8956bd2c-c863-4704-bc65-5c0d83556258
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205067(v=OCS.15)
ms:contentKeyID: 48184750
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e9f5b2ece8cf436fe69c000da73871cb92686d82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390176"
---
# <a name="configure-rooms-in-lync-server-2013"></a><span data-ttu-id="f427c-103">Configurar salas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f427c-103">Configure rooms in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f427c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f427c-104">

<span> </span></span></span>

<span data-ttu-id="f427c-105">_**Tópico da última modificação:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="f427c-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="f427c-106">Configurar salas de chat persistentes geralmente é manipulado por usuários ou outras equipes centrais usando a interface de linha de comando do Windows PowerShell; Geralmente, um administrador não gerencia as salas de chat.</span><span class="sxs-lookup"><span data-stu-id="f427c-106">Configuring Persistent Chat rooms is commonly handled by users or other central teams by using Windows PowerShell command-line interface; an administrator typically does not manage chat rooms.</span></span> <span data-ttu-id="f427c-107">No entanto, se você precisar criar e gerenciar salas de chat, poderá usar a interface de linha de comando do Windows PowerShell ou adicionar-se como membro a uma sala de chat e usar o cliente Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="f427c-107">However, if you have to create and manage chat rooms, you can use the Windows PowerShell command-line interface, or add yourself as a member to a chat room and use the Lync 2013 client.</span></span>

<span data-ttu-id="f427c-108">Para obter detalhes sobre como configurar salas de chat usando a interface de linha de comando do Windows PowerShell, consulte o "gerenciamento de sala" em [Configurando o servidor de chat persistente usando cmdlets do Windows PowerShell](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span><span class="sxs-lookup"><span data-stu-id="f427c-108">For details about configuring chat rooms by using the Windows PowerShell command-line interface, see "Room Management" in [Configuring Persistent Chat Server by using Windows PowerShell cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span></span>

<div>

## <a name="managing-data-in-chat-rooms"></a><span data-ttu-id="f427c-109">Gerenciando dados em salas de chat</span><span class="sxs-lookup"><span data-stu-id="f427c-109">Managing Data in Chat Rooms</span></span>

<span data-ttu-id="f427c-110">O servidor de chat persistente permite aos usuários colaborar enviando mensagens para salas de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="f427c-110">Persistent Chat Server lets users collaborate by posting messages into Persistent Chat rooms.</span></span> <span data-ttu-id="f427c-111">Os dados persistem no servidor e os membros da sala podem ter acesso aos dados, incluindo dados históricos.</span><span class="sxs-lookup"><span data-stu-id="f427c-111">The data is persisted on the server, and members of the room can have access to the data, including historical data.</span></span> <span data-ttu-id="f427c-112">No entanto, os usuários com funções diferentes têm acesso diferente aos dados persistentes, conforme descrito na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="f427c-112">However, users with different roles have different access to the persisted data, as outlined in the following list.</span></span>

  - <span data-ttu-id="f427c-113">Os administradores podem excluir qualquer conteúdo (por exemplo, conteúdo publicado antes de determinada data) de qualquer sala de chat para impedir que o banco de dados assuma proporções muito grandes.</span><span class="sxs-lookup"><span data-stu-id="f427c-113">Administrators can delete earlier content (for example, content that was posted before a certain date) from any chat room to keep the database from growing too large.</span></span> <span data-ttu-id="f427c-114">Ou podem remover ou substituir mensagens que são consideradas inapropriadamente para uma determinada sala de chat.</span><span class="sxs-lookup"><span data-stu-id="f427c-114">Or, they can remove or replace messages that are considered inappropriate for a particular chat room.</span></span>

  - <span data-ttu-id="f427c-115">Os usuários finais, inclusive os autores das mensagens, não podem excluir conteúdo de nenhuma sala de chat.</span><span class="sxs-lookup"><span data-stu-id="f427c-115">End users, including message authors, cannot delete content from any chat room.</span></span>

  - <span data-ttu-id="f427c-116">Os gerentes de salas de chat podem desabilitar salas, mas não podem excluir salas.</span><span class="sxs-lookup"><span data-stu-id="f427c-116">Chat room managers can disable rooms, but cannot delete rooms.</span></span> <span data-ttu-id="f427c-117">Somente os administradores podem excluir uma sala de chat depois que ela foi criada.</span><span class="sxs-lookup"><span data-stu-id="f427c-117">Only administrators can delete a chat room after it has been created.</span></span>

<span data-ttu-id="f427c-118">Quando uma mensagem é excluída, não é possível desfazer a ação.</span><span class="sxs-lookup"><span data-stu-id="f427c-118">When a message is deleted, you cannot undo the action.</span></span> <span data-ttu-id="f427c-119">No entanto, as mensagens excluídas podem ser restauradas se houver um backup.</span><span class="sxs-lookup"><span data-stu-id="f427c-119">However, deleted messages can be restored if there is a backup.</span></span> <span data-ttu-id="f427c-120">Se um servidor de conformidade de chat persistente estiver habilitado, as mensagens antigas serão mantidas no banco de dados de conformidade.</span><span class="sxs-lookup"><span data-stu-id="f427c-120">If a Persistent Chat Compliance server is enabled, old messages are persisted in the compliance database.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f427c-121">Este uso de dados da sala de chat aplica-se ao Lync Server 2013, aplicativo de API do servidor de chat persistente, exceto quando a função de administrador estiver envolvida.</span><span class="sxs-lookup"><span data-stu-id="f427c-121">This chat room data usage applies to the Lync Server 2013, Persistent Chat Server API application, except for the case when the administrator role is involved.</span></span> <span data-ttu-id="f427c-122">A API do servidor de chat persistente não pode ser usada para fazer qualquer uma das operações do administrador.</span><span class="sxs-lookup"><span data-stu-id="f427c-122">The Persistent Chat Server API cannot be used to do any of the administrator’s operations.</span></span> <span data-ttu-id="f427c-123">Você deve executar essas operações no Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f427c-123">You must perform these operations in the Lync Server Management Shell.</span></span>



<span data-ttu-id="f427c-124"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f427c-124"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

