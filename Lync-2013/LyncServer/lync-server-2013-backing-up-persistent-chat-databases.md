---
title: 'Lync Server 2013: fazendo backup de bancos de dados de chat persistente'
description: 'Lync Server 2013: fazendo backup de bancos de dados de chat persistentes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up Persistent Chat databases
ms:assetid: b99ebdc0-a025-44d7-9d74-37a7365f330d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945646(v=OCS.15)
ms:contentKeyID: 51541507
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9885eaf0065f5b558922c056fb1f669a5b821460
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438019"
---
# <a name="backing-up-persistent-chat-databases-in-lync-server-2013"></a><span data-ttu-id="19f85-103">Fazer backup de bancos de dados de chat persistentes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="19f85-103">Backing up Persistent Chat databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19f85-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19f85-104">

<span> </span></span></span>

<span data-ttu-id="19f85-105">_**Tópico da última modificação:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="19f85-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="19f85-106">Conteúdo da sala de chat persistente é armazenado no banco de dados de chat persistente (MGC. MDF).</span><span class="sxs-lookup"><span data-stu-id="19f85-106">Persistent Chat room content is stored in the Persistent Chat database (Mgc.mdf).</span></span> <span data-ttu-id="19f85-107">Esses dados são essenciais para os negócios, cujo backup deve ser feito regularmente.</span><span class="sxs-lookup"><span data-stu-id="19f85-107">This is business-critical data that should be backed up regularly.</span></span> <span data-ttu-id="19f85-108">Além do conteúdo da sala de chat, o banco de dados de chat persistente também armazena informações sobre as entidades de segurança (como usuários e grupos de usuários) e as funções e o acesso de chat a salas de chat e salas de chat.</span><span class="sxs-lookup"><span data-stu-id="19f85-108">In addition to the chat room content, the Persistent Chat database also stores information about the principals (such as users and user groups), and the roles and access that they have to chat rooms and chat room.</span></span>

<span data-ttu-id="19f85-109">Há duas maneiras de fazer backup de dados de chat persistentes.</span><span class="sxs-lookup"><span data-stu-id="19f85-109">There are two ways of backing up Persistent Chat data.</span></span>

  - <span data-ttu-id="19f85-110">Backup do SQL Server</span><span class="sxs-lookup"><span data-stu-id="19f85-110">SQL Server Backup</span></span>

  - <span data-ttu-id="19f85-111">O `Export-CsPersistentChatData` cmdlet, que exporta dados de chat persistentes como um arquivo</span><span class="sxs-lookup"><span data-stu-id="19f85-111">The `Export-CsPersistentChatData` cmdlet, which exports Persistent Chat data as a file</span></span>

<span data-ttu-id="19f85-112">Os dados que são criados usando o backup do SQL Server exigem um espaço de disco significativamente maior, possivelmente 20 vezes mais, do que o criado por `Export-CsPersistentChatData` , mas o backup do SQL Server tem mais probabilidade de ser um procedimento com o qual os administradores estão familiarizados.</span><span class="sxs-lookup"><span data-stu-id="19f85-112">Data that is created by using SQL Server backup requires significantly more disk space—possibly 20 times more—than that created by `Export-CsPersistentChatData`, but SQL Server backup is more likely to be a procedure that administrators are familiar with.</span></span>

<span data-ttu-id="19f85-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="19f85-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

