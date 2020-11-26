---
title: 'Lync Server 2013: Movendo uma sala de chat de uma categoria a outra'
description: 'Lync Server 2013: movendo uma sala de chat de uma categoria para outra.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Moving a chat room from one category to another
ms:assetid: 7e93b8f6-5a18-4476-a432-3918e01bcfa6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215877(v=OCS.15)
ms:contentKeyID: 48706004
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4066732a90a94414b55d6a567fde0d496e4faf13
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425261"
---
# <a name="moving-a-chat-room-from-one-category-to-another-in-lync-server-2013"></a><span data-ttu-id="c085a-103">Movendo uma sala de chat de uma categoria a outra no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c085a-103">Moving a chat room from one category to another in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c085a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c085a-104">

<span> </span></span></span>

<span data-ttu-id="c085a-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="c085a-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="c085a-106">Recomendamos que você não altere a categoria de uma sala de chat persistente após a criação da sala de chat.</span><span class="sxs-lookup"><span data-stu-id="c085a-106">We recommend that you do not change the category of a Persistent Chat room after the chat room is created.</span></span> <span data-ttu-id="c085a-107">No entanto, se o gerente da sala de chat tem privilégios de **criador** em outra categoria, ele pode mover a sala de uma categoria para outra.</span><span class="sxs-lookup"><span data-stu-id="c085a-107">However, if the chat room manager has **Creator** privileges in another category, he or she can move the room from one category to another.</span></span> <span data-ttu-id="c085a-108">A sala não é excluída nem recriada.</span><span class="sxs-lookup"><span data-stu-id="c085a-108">The room is not deleted and recreated.</span></span> <span data-ttu-id="c085a-109">É uma alteração de associação dentro do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c085a-109">It is a change of association within the database.</span></span>

<span data-ttu-id="c085a-110">Alterar uma categoria de sala de chat raramente deve ser feito.</span><span class="sxs-lookup"><span data-stu-id="c085a-110">Changing a chat room category should be done rarely.</span></span> <span data-ttu-id="c085a-111">Uma categoria determina a associação permitida para a sala de chat, por isso, quando uma sala de chat muda de categoria, todas as listas de controle de acesso do sistema (SACLs) não mais suportadas pela nova categoria são purgadas.</span><span class="sxs-lookup"><span data-stu-id="c085a-111">A category determines the allowed membership for the chat room, so when a chat room is moved to another category, all the system access control lists (SACLs) that are no longer supported by the new category are purged.</span></span> <span data-ttu-id="c085a-112">Por exemplo, se um usuário era membro da sala e não é mais um **AllowedMember** na nova categoria, a participação da sala será modificada e o usuário será removido da sala.</span><span class="sxs-lookup"><span data-stu-id="c085a-112">For example, if a user was a member of the room and is no longer an **AllowedMember** in the new category, the room membership will be modified and the user will be removed from the room.</span></span>

<span data-ttu-id="c085a-113">Para obter detalhes sobre como mover uma sala de chat usando a interface de linha de comando do Windows PowerShell, consulte o "gerenciamento de sala" em [Configurando o servidor de chat persistente usando cmdlets do Windows PowerShell](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span><span class="sxs-lookup"><span data-stu-id="c085a-113">For details about moving a chat room by using the Windows PowerShell command-line interface, see "Room Management" in [Configuring Persistent Chat Server by using Windows PowerShell cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span></span>

<span data-ttu-id="c085a-114">Para obter detalhes sobre como configurar salas de chat, consulte [Configurar salas no Lync Server 2013](lync-server-2013-configure-rooms.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="c085a-114">For details about configuring chat rooms, see [Configure rooms in Lync Server 2013](lync-server-2013-configure-rooms.md) in the Deployment documentation.</span></span>

<span data-ttu-id="c085a-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c085a-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

