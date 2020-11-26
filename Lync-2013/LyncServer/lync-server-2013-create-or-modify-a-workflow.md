---
title: 'Lync Server 2013: criar ou modificar um fluxo de trabalho'
description: 'Lync Server 2013: criar ou modificar um fluxo de trabalho.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a workflow
ms:assetid: 5ac1c0f3-e82f-40ca-b972-91950e38c05b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520997(v=OCS.15)
ms:contentKeyID: 48184225
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 053b80e313e497313e613a5f8b16bd5beeabf7ac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431726"
---
# <a name="create-or-modify-a-workflow-in-lync-server-2013"></a><span data-ttu-id="bc3ad-103">Criar ou modificar um fluxo de trabalho no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc3ad-103">Create or modify a workflow in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bc3ad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bc3ad-104">

<span> </span></span></span>

<span data-ttu-id="bc3ad-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="bc3ad-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="bc3ad-106">O Lync Server 2013 dá suporte a dois tipos de fluxos de trabalho: grupo de buscas e resposta de voz interativa (IVR).</span><span class="sxs-lookup"><span data-stu-id="bc3ad-106">Lync Server 2013 supports two types of workflows: hunt group and interactive voice response (IVR).</span></span> <span data-ttu-id="bc3ad-107">Ao criar um fluxo de trabalho, use a ferramenta de configuração de grupo de resposta para especificar a fila a ser usada e outras configurações, como uma mensagem de boas-vindas, música em espera, horário comercial e perguntas que o aplicativo do grupo de resposta pede para o chamador.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-107">When you create a workflow, you use the Response Group Configuration Tool to specify the queue to use and other settings, such as a welcome message, music on hold, business hours, and questions that the Response Group application asks the caller.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bc3ad-108">Você deve criar grupos de agente e filas antes de criar um fluxo de trabalho que os utiliza.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-108">You must create agent groups and queues before you create a workflow that uses them.</span></span> <span data-ttu-id="bc3ad-109">Se você quiser criar horários comerciais predefinidos e feriados que você pode usar para vários fluxos de trabalho, você também deve definir essas horas e feriados antes de criar um fluxo de trabalho que os use.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-109">If you want to create predefined business hours and holidays that you can use for multiple workflows, you must also define these hours and holidays before you create a workflow that uses them.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="bc3ad-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="bc3ad-110">In This Section</span></span>

  - [<span data-ttu-id="bc3ad-111">Criar ou modificar um fluxo de trabalho de grupo coletivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc3ad-111">Create or modify a hunt group workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-hunt-group-workflow.md)

  - [<span data-ttu-id="bc3ad-112">Criar ou modificar um fluxo de trabalho interativo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc3ad-112">Create or modify an interactive workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-interactive-workflow.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bc3ad-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc3ad-113">See Also</span></span>


[<span data-ttu-id="bc3ad-114">Criar ou modificar um grupo de agente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc3ad-114">Create or modify an agent group in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-agent-group.md)  
[<span data-ttu-id="bc3ad-115">Criar ou modificar uma fila no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc3ad-115">Create or modify a queue in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-queue.md)  
[<span data-ttu-id="bc3ad-116">Adicionais Definir conjuntos de feriados do grupo de resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc3ad-116">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-holiday-sets.md)  


[<span data-ttu-id="bc3ad-117">Adicionais Definir o horário comercial do grupo de resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc3ad-117">(Optional) Define Response Group business hours in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-business-hours.md)  
  

<span data-ttu-id="bc3ad-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bc3ad-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

