---
title: 'Lync Server 2013: como gerenciar fluxos de trabalho do grupo de resposta'
description: 'Lync Server 2013: gerenciamento de fluxos de trabalho de grupo de resposta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Response Group workflows
ms:assetid: 42cfccdd-2844-4875-b4e3-813e1df15f08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520986(v=OCS.15)
ms:contentKeyID: 48183974
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2223fed2b5b030a2c92e0b958ae8545a7717f848
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437221"
---
# <a name="managing-response-group-workflows-in-lync-server-2013"></a><span data-ttu-id="4216d-103">Gerenciamento de fluxos de trabalho de grupo de resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4216d-103">Managing Response Group workflows in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4216d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4216d-104">

<span> </span></span></span>

<span data-ttu-id="4216d-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="4216d-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="4216d-106">Um fluxo de trabalho de grupo de resposta define o comportamento de uma chamada no momento em que o telefone toca para a hora em que o agente atende a chamada.</span><span class="sxs-lookup"><span data-stu-id="4216d-106">A Response Group workflow defines the behavior of a call from the time that the phone rings to the time that an agent answers the call.</span></span> <span data-ttu-id="4216d-107">O fluxo de trabalho inclui informações de fila e roteamento e inclui informações de grupo de busca ou resposta de voz interativa (IVR).</span><span class="sxs-lookup"><span data-stu-id="4216d-107">The workflow includes queue and routing information, and includes either hunt group or interactive voice response (IVR) information.</span></span>

<span data-ttu-id="4216d-108">Os tópicos desta seção identificam as práticas recomendadas para a criação de fluxos de trabalho de IVR e explicam como criar conjuntos de horários comerciais personalizados e feriados, como criar ou modificar fluxos de trabalho e como excluir grupos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4216d-108">Topics in this section identify best practices for designing IVR workflows, and explain how to create customized business hours and holiday sets, how to create or modify workflows, and how to delete workgroups.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="4216d-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="4216d-109">In This Section</span></span>

  - [<span data-ttu-id="4216d-110">Projetar fluxos de chamada de resposta interativa de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4216d-110">Design interactive voice response call flows in Lync Server 2013</span></span>](lync-server-2013-design-interactive-voice-response-call-flows.md)

  - [<span data-ttu-id="4216d-111">Adicionais Definir o horário comercial do grupo de resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4216d-111">(Optional) Define Response Group business hours in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-business-hours.md)

  - [<span data-ttu-id="4216d-112">Adicionais Definir conjuntos de feriados do grupo de resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4216d-112">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-holiday-sets.md)

  - [<span data-ttu-id="4216d-113">Criar ou modificar um fluxo de trabalho no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4216d-113">Create or modify a workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-workflow.md)

  - [<span data-ttu-id="4216d-114">Excluir um fluxo de trabalho no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4216d-114">Delete a workflow in Lync Server 2013</span></span>](lync-server-2013-delete-a-workflow.md)

<span data-ttu-id="4216d-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4216d-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

