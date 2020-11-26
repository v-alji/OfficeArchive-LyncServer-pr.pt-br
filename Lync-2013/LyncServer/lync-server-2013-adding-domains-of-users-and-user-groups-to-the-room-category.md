---
title: 'Lync Server 2013: Adicionando domínios de usuários e grupos de usuários à categoria da sala'
description: 'Lync Server 2013: adicionando domínios de usuários e grupos de usuários à categoria sala.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding domains of users and user groups to the room category
ms:assetid: ee03f2cf-1c84-41c4-b524-d0729be33b8c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215884(v=OCS.15)
ms:contentKeyID: 48706013
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 196a795547d5caa6dfd1732c3d6b4630ef79438a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439209"
---
# <a name="adding-domains-of-users-and-user-groups-to-the-room-category-in-lync-server-2013"></a><span data-ttu-id="2543a-103">Adicionando domínios de usuários e grupos de usuários à categoria da sala no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2543a-103">Adding domains of users and user groups to the room category in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2543a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2543a-104">

<span> </span></span></span>

<span data-ttu-id="2543a-105">_**Tópico da última modificação:** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="2543a-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<span data-ttu-id="2543a-106">Para adicionar grupos maiores de usuários a uma sala de chat, consulte [Configurar categorias no Lync Server 2013](lync-server-2013-configure-categories.md) e [gerenciar categorias](manage-categories.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="2543a-106">To add larger groups of users to a chat room, see [Configure categories in Lync Server 2013](lync-server-2013-configure-categories.md) and [Manage categories](manage-categories.md) in the Deployment documentation.</span></span> <span data-ttu-id="2543a-107">Por exemplo, esse comando adiciona todos os usuários da NorthAmericaUsers OU no Active Directory à sala de chat do América do América do América do usuário:</span><span class="sxs-lookup"><span data-stu-id="2543a-107">For example, this command adds all the users from the NorthAmericaUsers OU in active Directory to the NorthAmerica chat room:</span></span>

    Set-CsPersistentChatRoom -PersistentChatPoolFqdn "atl-cs-001.litwareinc.com\NorthAmerica" -Members @{Add="OU=NorthAmericaUsers,DC=litwareinc,DC=com"}

<span data-ttu-id="2543a-108">Seu comando adiciona todos os membros do grupo de distribuição Finance à mesma sala de chat:</span><span class="sxs-lookup"><span data-stu-id="2543a-108">His command adds all the members from the Finance distribution group to the same chat room:</span></span>

    Set-CsPersistentChatRoom -PersistentChatPoolFqdn "atl-cs-001.litwareinc.com\NorthAmerica" -Members @{Add="CN=Finance,OU=ExternalUsers,DC=litwareinc,DC=com"}

<span data-ttu-id="2543a-109"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2543a-109"></div>

<span> </span>

</div>

</div>

</span></span></div>

