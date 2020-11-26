---
title: 'Lync Server 2013: Configurando Grupo de Resposta'
description: 'Lync Server 2013: Configurando o grupo de resposta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Response Group
ms:assetid: c56db929-cb21-4af0-be3f-c8f807b78a5a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205249(v=OCS.15)
ms:contentKeyID: 48185359
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92674bb971ec5216051d75d788dc58b9c7ca641c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432685"
---
# <a name="configuring-response-group-in-lync-server-2013"></a><span data-ttu-id="86c12-103">Configurando Grupo de Resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86c12-103">Configuring Response Group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="86c12-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="86c12-104">

<span> </span></span></span>

<span data-ttu-id="86c12-105">_**Tópico da última modificação:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="86c12-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="86c12-106">O grupo de resposta é um recurso de voz empresarial que roteia e enfileira chamadas de entrada para grupos de pessoas, chamados *agentes*, como um suporte técnico ou uma mesa de atendimento ao cliente.</span><span class="sxs-lookup"><span data-stu-id="86c12-106">Response Group is an Enterprise Voice feature that routes and queues incoming calls to groups of people, called *agents*, such as a help desk or a customer service desk.</span></span>

<span data-ttu-id="86c12-107">Os componentes necessários para o grupo de resposta são instalados e habilitados automaticamente no servidor front-end ou no servidor Standard Edition ao implantar o Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="86c12-107">The components that Response Group requires are installed and enabled automatically on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="86c12-108">Para disponibilizar o grupo de resposta para os usuários, você deve configurar grupos de agente e, em seguida, filas e fluxos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="86c12-108">To make Response Group available to users, you must configure agent groups, then queues, and then workflows.</span></span> <span data-ttu-id="86c12-109">Além disso, um administrador de grupo de resposta pode delegar a configuração de um fluxo de trabalho existente a um gerente de grupo de resposta, que pode, em seguida, modificar e reconfigurar o fluxo de trabalho e seus grupos e filas de agente associados.</span><span class="sxs-lookup"><span data-stu-id="86c12-109">Additionally, a Response Group Administrator can delegate configuration of an existing workflow to a Response Group Manager, who can then modify and reconfigure the workflow and its associated agent groups and queues.</span></span>

<span data-ttu-id="86c12-110">Esta seção orienta você na configuração do grupo de respostas do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="86c12-110">This section guides you through the configuration of Lync Server 2013 Response Group.</span></span> <span data-ttu-id="86c12-111">Ele pressupõe que você já leu as seções de planejamento relacionadas ao grupo de resposta e implantou um servidor Enterprise Edition ou um servidor Standard Edition com Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="86c12-111">It assumes that you have already read the planning sections related to Response Group and have deployed an Enterprise Edition server or a Standard Edition server with Enterprise Voice.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="86c12-112">Para obter detalhes sobre como criar um grupo de resposta usando o Shell de gerenciamento do Lync Server, incluindo um exemplo de script, consulte "criando seu primeiro grupo de resposta usando o Shell de gerenciamento do Lync Server" em <A href="https://go.microsoft.com/fwlink/p/?linkid=204108">https://go.microsoft.com/fwlink/p/?linkId=204108</A> .</span><span class="sxs-lookup"><span data-stu-id="86c12-112">For details about creating a Response Group by using Lync Server Management Shell, including a sample script, see "Creating Your First Response Group Using Lync Server Management Shell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=204108">https://go.microsoft.com/fwlink/p/?linkId=204108</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="86c12-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="86c12-113">In This Section</span></span>

  - [<span data-ttu-id="86c12-114">Permissões e pré-requisitos de configuração de Grupo de Resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86c12-114">Response Group configuration permissions and prerequisites in Lync Server 2013</span></span>](lync-server-2013-response-group-configuration-permissions-and-prerequisites.md)

  - [<span data-ttu-id="86c12-115">Processo de implantação para o grupo de resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86c12-115">Deployment process for Response Group in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-response-group.md)

  - [<span data-ttu-id="86c12-116">Visão geral dos cenários de criação do fluxo de trabalho no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86c12-116">Overview of workflow creation scenarios in Lync Server 2013</span></span>](lync-server-2013-overview-of-workflow-creation-scenarios.md)

  - [<span data-ttu-id="86c12-117">Criar grupos de agente do Grupo de Resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86c12-117">Create Response Group agent groups Lync Server 2013</span></span>](lync-server-2013-create-response-group-agent-groups.md)

  - [<span data-ttu-id="86c12-118">Criar filas do Grupo de Resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86c12-118">Create Response Group queues in Lync Server 2013</span></span>](lync-server-2013-create-response-group-queues.md)

  - [<span data-ttu-id="86c12-119">Adicionais Definir o horário comercial do grupo de resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86c12-119">(Optional) Define Response Group business hours in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-business-hours.md)

  - [<span data-ttu-id="86c12-120">Adicionais Definir conjuntos de feriados do grupo de resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86c12-120">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-holiday-sets.md)

  - [<span data-ttu-id="86c12-121">Criar fluxos de trabalho de Grupo de Resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86c12-121">Create Response Group workflows in Lync Server 2013</span></span>](lync-server-2013-create-response-group-workflows.md)

  - [<span data-ttu-id="86c12-122">Adicionais Verificar a implantação do grupo de resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86c12-122">(Optional) Verify Response Group deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-response-group-deployment.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="86c12-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="86c12-123">See Also</span></span>


[<span data-ttu-id="86c12-124">Planejando os recursos de gerenciamento de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86c12-124">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="86c12-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="86c12-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

