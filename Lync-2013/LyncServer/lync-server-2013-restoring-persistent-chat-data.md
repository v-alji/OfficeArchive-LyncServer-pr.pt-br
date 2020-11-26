---
title: 'Lync Server 2013: restaurando dados persistentes de chat'
description: 'Lync Server 2013: restaurando dados de chat persistentes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring Persistent Chat data
ms:assetid: c251a7fa-50da-434b-b39a-17f5978ce736
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945649(v=OCS.15)
ms:contentKeyID: 51541516
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7c75683e151daaadab8374ed5b41886da9a3aea3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442506"
---
# <a name="restoring-persistent-chat-data-in-lync-server-2013"></a><span data-ttu-id="b7502-103">Restaurando dados de chat persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7502-103">Restoring Persistent Chat data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7502-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7502-104">

<span> </span></span></span>

<span data-ttu-id="b7502-105">_**Tópico da última modificação:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="b7502-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="b7502-106">Conteúdo da sala de chat persistente é armazenado no banco de dados de chat persistente (MGC. MDF).</span><span class="sxs-lookup"><span data-stu-id="b7502-106">Persistent Chat room content is stored in the Persistent Chat database (mgc.mdf).</span></span> <span data-ttu-id="b7502-107">Esses dados são essenciais para os negócios, cujo backup deve ser feito regularmente.</span><span class="sxs-lookup"><span data-stu-id="b7502-107">This is business-critical data that should be backed up regularly.</span></span> <span data-ttu-id="b7502-108">Além do conteúdo da sala de chat, as entidades de segurança (como usuários e grupos) e as funções e o acesso que elas precisam fazer para conversar com salas de chat e conteúdo da sala de chat, também são armazenados no banco de dados de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="b7502-108">In addition to the chat room content, principals (such as users and groups) and the roles and access that they have to chat rooms and chat room content, is also stored in the Persistent Chat database.</span></span>

<span data-ttu-id="b7502-109">A maneira como você restaura seus dados de chat persistentes depende do método usado para fazer o backup.</span><span class="sxs-lookup"><span data-stu-id="b7502-109">How you restore your Persistent Chat data depends on the method that you used to back it up.</span></span>

  - <span data-ttu-id="b7502-110">Se você usou procedimentos de backup do SQL Server, então deve usar procedimentos de restauração do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b7502-110">If you used SQL Server backup procedures, you must use SQL Server restore procedures.</span></span>

  - <span data-ttu-id="b7502-111">Se você usou o cmdlet **Export-CsPersistentChatData** para fazer backup de dados de chat persistente, deve usar o cmdlet **Import-CsPersistentChatData** para restaurar os dados.</span><span class="sxs-lookup"><span data-stu-id="b7502-111">If you used the **Export-CsPersistentChatData** cmdlet to back up Persistent Chat data, then you must use the **Import-CsPersistentChatData** cmdlet to restore the data.</span></span>

<span data-ttu-id="b7502-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7502-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

