---
title: Cenário de migração padrão - nível alto
description: Cenário de migração padrão-alto nível.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Standard migration scenario - high-level
ms:assetid: e768a7ca-44e3-4969-a6d9-7ed3e7029c5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205354(v=OCS.15)
ms:contentKeyID: 48185709
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a931b76e528b7e6468f6b7e7b9a718724d27501f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438754"
---
# <a name="standard-migration-scenario---high-level"></a><span data-ttu-id="8dcbd-103">Cenário de migração padrão - nível alto</span><span class="sxs-lookup"><span data-stu-id="8dcbd-103">Standard migration scenario - high-level</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8dcbd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8dcbd-104">

<span> </span></span></span>

<span data-ttu-id="8dcbd-105">_**Tópico da última modificação:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="8dcbd-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="8dcbd-106">Use os itens a seguir como ponto de partida ao migrar o Lync Server 2010, o chat de grupo ou o Office Communications Server 2007 R2 Grupo chat para o Lync Server 2013, servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="8dcbd-106">Use the following items as a starting point when migrating Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="8dcbd-107">O caminho de migração padrão do Lync Server 2013 é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8dcbd-107">The standard Lync Server 2013 migration path is as follows:</span></span>

  - <span data-ttu-id="8dcbd-108">Sua organização implantou anteriormente o Lync Server 2010, o chat em grupo ou o Office Communications Server 2007 R2 para o chat em grupo e você deseja implantar o Lync Server 2013, servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="8dcbd-108">Your organization has previously deployed Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat, and you want to deploy Lync Server 2013, Persistent Chat Server.</span></span>

  - <span data-ttu-id="8dcbd-109">Implante o Lync Server 2013 e, em seguida, implante os pools do servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="8dcbd-109">Deploy Lync Server 2013, and then deploy Persistent Chat Server pool(s).</span></span>

  - <span data-ttu-id="8dcbd-110">Prepare e planeje a migração de salas de chat persistentes e determine um tempo apropriado para desligar o sistema para a migração.</span><span class="sxs-lookup"><span data-stu-id="8dcbd-110">Prepare and plan for migration of your Persistent Chat rooms, and determine an appropriate time to shut down the system for migration.</span></span>

  - <span data-ttu-id="8dcbd-111">Execute os cmdlets do Windows PowerShell para a migração (**Export-CsPersistentChatData** e **Import-CsPersistentChatData**) para mover o conteúdo para o servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="8dcbd-111">Run the Windows PowerShell cmdlets for migration (**Export-CsPersistentChatData** and **Import-CsPersistentChatData**) to move content to Persistent Chat Server.</span></span>

  - <span data-ttu-id="8dcbd-112">Verifique se a migração foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8dcbd-112">Verify that migration has succeeded.</span></span>

  - <span data-ttu-id="8dcbd-113">Descomissionar sua implantação herdada.</span><span class="sxs-lookup"><span data-stu-id="8dcbd-113">Decommission your legacy deployment.</span></span>

  - <span data-ttu-id="8dcbd-114">Configure o servidor de chat persistente para que os clientes herdados possam se conectar ao Lync Server 2013, servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="8dcbd-114">Configure Persistent Chat Server so that legacy clients can connect to Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="8dcbd-115">Isso é necessário porque demora tempo para implantar novos clientes, e você deseja permitir que os usuários existentes com clientes herdados tenham acesso às suas salas de chat o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="8dcbd-115">This is necessary because it takes time to deploy new clients, and you want to enable existing users with legacy clients to have access to their chat rooms as soon as possible.</span></span>

  - <span data-ttu-id="8dcbd-116">Implante novos clientes e continue a garantir que trabalhadores com o chat de grupo herdado possam acessar suas salas de chat.</span><span class="sxs-lookup"><span data-stu-id="8dcbd-116">Deploy new clients, while continuing to help ensure that workers with legacy Group Chat (clients) can get to their chat rooms.</span></span>

<span data-ttu-id="8dcbd-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8dcbd-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

