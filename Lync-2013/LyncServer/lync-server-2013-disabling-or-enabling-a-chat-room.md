---
title: 'Lync Server 2013: Habilitar ou desabilitar uma sala de chat'
description: 'Lync Server 2013: desativando ou ativando uma sala de chat.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disabling or enabling a chat room
ms:assetid: db0908fc-aae3-46e8-bc0b-245e9adfa1e2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215883(v=OCS.15)
ms:contentKeyID: 48706011
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b81ce2614cebcf554c0390369068d8fd8b8f932
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437844"
---
# <a name="disabling-or-enabling-a-chat-room-in-lync-server-2013"></a><span data-ttu-id="33ee9-103">Habilitar ou desabilitar uma sala de chat no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33ee9-103">Disabling or enabling a chat room in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="33ee9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="33ee9-104">

<span> </span></span></span>

<span data-ttu-id="33ee9-105">_**Tópico da última modificação:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="33ee9-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="33ee9-106">Se o tópico de uma sala de chat persistente não for mais relevante, você poderá deixar a sala de chat indisponível para os usuários desabilitá-la.</span><span class="sxs-lookup"><span data-stu-id="33ee9-106">If the topic of a Persistent Chat room is no longer relevant, you can make the chat room unavailable to users by disabling it.</span></span> <span data-ttu-id="33ee9-107">Quando uma sala de chat está desabilitada, todos os membros são desconectados imediatamente da sala.</span><span class="sxs-lookup"><span data-stu-id="33ee9-107">When a chat room is disabled, all members are immediately disconnected from the room.</span></span> <span data-ttu-id="33ee9-108">Após uma sala de chat ser desabilitada, os usuários não podem participar novamente ou encontrá-la nas pesquisas de sala de chat.</span><span class="sxs-lookup"><span data-stu-id="33ee9-108">After a chat room is disabled, users cannot rejoin it or find it in chat room searches.</span></span>

<span data-ttu-id="33ee9-109">Uma sala de chat desativada pode ser habilitada posteriormente por um administrador de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="33ee9-109">A disabled chat room can be enabled later by a Persistent Chat administrator.</span></span> <span data-ttu-id="33ee9-110">Se uma sala de chat for desabilitada, sua lista de associação e outras configurações serão preservadas.</span><span class="sxs-lookup"><span data-stu-id="33ee9-110">If a chat room is disabled, its membership list and other settings are preserved.</span></span> <span data-ttu-id="33ee9-111">Se você habilitar a sala novamente, não será necessário recriá-las manualmente.</span><span class="sxs-lookup"><span data-stu-id="33ee9-111">If you enable the room again, you do not need to manually re-create the settings.</span></span>

<span data-ttu-id="33ee9-112">Se o histórico da sala de chat persistir (a persistência do histórico de salas de chat é uma configuração opcional em uma categoria que se aplica a todas as salas dentro da categoria; o padrão é mantido, mas pode ser desativado Configurando o **histórico de habilitar o chat** como falso), o conteúdo é preservado quando a sala de chat está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="33ee9-112">If the chat room’s history persists (chat room history persistence is an optional setting on a category that applies to all rooms within the category; the default is that it is persisted, but can be turned off by setting the category’s **Enable Chat History** to false), the content is preserved when the chat room is disabled.</span></span> <span data-ttu-id="33ee9-113">Entretanto, o conteúdo não será exibido nas pesquisas durante o tempo em que a sala de chat permanecer no estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="33ee9-113">However, that content will not appear in searches during the time that the chat room remains in a disabled state.</span></span> <span data-ttu-id="33ee9-114">Se você habilitá-la mais tarde, os usuários poderão pesquisar mensagens que foram publicadas antes da sala de chat ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="33ee9-114">If you later enable the chat room, users can search for messages that were posted before the chat room was disabled.</span></span>

<span data-ttu-id="33ee9-115">Para obter detalhes sobre como desabilitar e habilitar as salas de chat usando a interface de linha de comando do Windows PowerShell, consulte o "gerenciamento de sala" em [Configurando o servidor de chat persistente usando cmdlets do Windows PowerShell](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span><span class="sxs-lookup"><span data-stu-id="33ee9-115">For details about disabling and enabling chat rooms by using the Windows PowerShell command-line interface, see "Room Management" in [Configuring Persistent Chat Server by using Windows PowerShell cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span></span> <span data-ttu-id="33ee9-116">Para desabilitar uma sala de chat, use um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="33ee9-116">To disable a chat room, use a command similar to this:</span></span>

    Set-CsPersistentChatRoom -Identity "atl-cs-001.litwareinc.com\ITChatRoom" -Disabled $True

<span data-ttu-id="33ee9-117">Para habilitar uma sala de chat, defina a propriedade disabled como false:</span><span class="sxs-lookup"><span data-stu-id="33ee9-117">To enabled a chat room, set the Disabled property to False:</span></span>

    Set-CsPersistentChatRoom -Identity "atl-cs-001.litwareinc.com\ITChatRoom" -Disabled $False

<span data-ttu-id="33ee9-118">Observe que as salas de chat não podem ser ativadas ou desativadas usando o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="33ee9-118">Note that chat rooms cannot be enabled or disabled by using the Lync Server Control Panel.</span></span>

<span data-ttu-id="33ee9-119">Para obter detalhes sobre como configurar salas de chat, consulte [Configurar salas no Lync Server 2013](lync-server-2013-configure-rooms.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="33ee9-119">For details about configuring chat rooms, see [Configure rooms in Lync Server 2013](lync-server-2013-configure-rooms.md) in the Deployment documentation.</span></span>

<span data-ttu-id="33ee9-120"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="33ee9-120"></div>

<span> </span>

</div>

</div>

</span></span></div>

