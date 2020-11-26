---
title: 'Lync Server 2013: implantação de recursos de gerenciamento de chamadas'
description: 'Lync Server 2013: implantação de recursos de gerenciamento de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying call management features
ms:assetid: 1667cfe4-76fa-4e10-91bb-b3efbedbf759
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204706(v=OCS.15)
ms:contentKeyID: 48183504
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aa89b75dbcae9de1069daf99986076b66e0411cc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430067"
---
# <a name="deploying-call-management-features-in-lync-server-2013"></a><span data-ttu-id="42169-103">Implantando recursos de gerenciamento de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42169-103">Deploying call management features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42169-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42169-104">

<span> </span></span></span>

<span data-ttu-id="42169-105">_**Tópico da última modificação:** 2012-12-18_</span><span class="sxs-lookup"><span data-stu-id="42169-105">_**Topic Last Modified:** 2012-12-18_</span></span>

<span data-ttu-id="42169-106">Os recursos de gerenciamento de chamadas do Enterprise Voice controlam como as chamadas de entrada são roteadas e respondidas.</span><span class="sxs-lookup"><span data-stu-id="42169-106">Enterprise Voice call management features control how incoming calls are routed and answered.</span></span> <span data-ttu-id="42169-107">O Lync Server 2013 fornece os seguintes recursos de gerenciamento de chamadas:</span><span class="sxs-lookup"><span data-stu-id="42169-107">Lync Server 2013 provides the following call management features:</span></span>

  - <span data-ttu-id="42169-108">**Estacionamento de chamadas:** Permite que os usuários de voz disquem temporariamente o estacionamento de uma chamada e a selecionem do mesmo telefone ou outro telefone.</span><span class="sxs-lookup"><span data-stu-id="42169-108">**Call Park:** Enables voice users to temporarily park a call and then pick it up from the same phone or another phone.</span></span>

  - <span data-ttu-id="42169-109">**Retirada em grupo:** Permite que os usuários atendam chamadas feitas a outro usuário atribuído a um grupo de coleta discando o número do grupo de recebimento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="42169-109">**Group Pickup:** Enables users to answer calls made to another user who is assigned to a pickup group by dialing the call pickup group number.</span></span>

  - <span data-ttu-id="42169-110">**Grupo de resposta:** Roteia chamadas para grupos de agentes usando grupos de busca ou perguntas e respostas de reação a chamadas de voz interativas (IVR).</span><span class="sxs-lookup"><span data-stu-id="42169-110">**Response Group:** Routes incoming calls to groups of agents by using hunt groups or interactive voice response (IVR) questions and answers.</span></span>

  - <span data-ttu-id="42169-111">**Lançamento:** Reproduz uma mensagem para chamadas feitas para um número não atribuído ou roteia a chamada para outro lugar ou ambos.</span><span class="sxs-lookup"><span data-stu-id="42169-111">**Announcement:** Plays a message for calls made to an unassigned number, or routes the call elsewhere, or both.</span></span>

<span data-ttu-id="42169-112">Esta seção descreve como configurar esses recursos de gerenciamento de chamadas durante uma implantação do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="42169-112">This section describes how to configure these call management features during an Enterprise Voice deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="42169-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="42169-113">In This Section</span></span>

  - [<span data-ttu-id="42169-114">Configurando Estacionamento de Chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42169-114">Configuring Call Park in Lync Server 2013</span></span>](lync-server-2013-configuring-call-park.md)

  - [<span data-ttu-id="42169-115">Configurando a coleta de chamadas em grupo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42169-115">Configuring Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-configuring-group-call-pickup.md)

  - [<span data-ttu-id="42169-116">Configurando Grupo de Resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42169-116">Configuring Response Group in Lync Server 2013</span></span>](lync-server-2013-configuring-response-group.md)

  - [<span data-ttu-id="42169-117">Configurando comunicados de números não atribuídos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42169-117">Configuring announcements for unassigned numbers in Lync Server 2013</span></span>](lync-server-2013-configuring-announcements-for-unassigned-numbers.md)

<span data-ttu-id="42169-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42169-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

