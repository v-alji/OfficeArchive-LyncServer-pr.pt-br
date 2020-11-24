---
title: 'Lync Server 2013: atribuir políticas de presença por usuário'
description: 'Lync Server 2013: atribuir políticas de presença por usuário.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning per-user presence policies
ms:assetid: fd1097b7-248d-4b78-8c43-456b03257c18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182614(v=OCS.15)
ms:contentKeyID: 48185955
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c3d4b4bda0c4bb85065d546fdbb4b2578db0e3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390380"
---
# <a name="assigning-per-user-presence-policies-in-lync-server-2013"></a><span data-ttu-id="20165-103">Como atribuir políticas de presença por usuário no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20165-103">Assigning per-user presence policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20165-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20165-104">

<span> </span></span></span>

<span data-ttu-id="20165-105">_**Tópico da última modificação:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="20165-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="20165-106">Uma política de presença é um conjunto de limites e restrições que afetam a presença.</span><span class="sxs-lookup"><span data-stu-id="20165-106">A presence policy is a set of limits and restrictions that affect presence.</span></span> <span data-ttu-id="20165-107">A tabela a seguir descreve as configurações de política de presença disponíveis no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="20165-107">The following table describes the presence policy settings available in Lync Server 2013.</span></span>

### <a name="presence-policy-settings"></a><span data-ttu-id="20165-108">Configurações da política de presença</span><span class="sxs-lookup"><span data-stu-id="20165-108">Presence Policy Settings</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20165-109">Nome XML</span><span class="sxs-lookup"><span data-stu-id="20165-109">XML name</span></span></th>
<th><span data-ttu-id="20165-110">Nome para exibição</span><span class="sxs-lookup"><span data-stu-id="20165-110">Display name</span></span></th>
<th><span data-ttu-id="20165-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="20165-111">Description</span></span></th>
<th><span data-ttu-id="20165-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="20165-112">Type</span></span></th>
<th><span data-ttu-id="20165-113">Valor</span><span class="sxs-lookup"><span data-stu-id="20165-113">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20165-114">CategorySubscriptions</span><span class="sxs-lookup"><span data-stu-id="20165-114">CategorySubscriptions</span></span></p></td>
<td><p><span data-ttu-id="20165-115">Número máximo de assinaturas de categoria de assinante</span><span class="sxs-lookup"><span data-stu-id="20165-115">Maximum Number of Subscriber Category Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="20165-116">Limita o número de assinaturas de categoria do Assinante.</span><span class="sxs-lookup"><span data-stu-id="20165-116">Limits the number of subscriber category subscriptions.</span></span> <span data-ttu-id="20165-117">Por exemplo, quando o Communicator assina a presença de um usuário, ele obtém uma assinatura de categoria para cada um dos cartões de visita, dados de calendário, observações, serviços e categorias de estado.</span><span class="sxs-lookup"><span data-stu-id="20165-117">For example, when Communicator subscribes to a user’s presence, it obtains a category subscription for each of the contact card, calendar data, notes, services, and state categories.</span></span></p>
<p><span data-ttu-id="20165-118">Uma configuração de 0 significa que o objeto de contato ou usuário não pode ser inscrito por outras pessoas.</span><span class="sxs-lookup"><span data-stu-id="20165-118">A setting of 0 means that the user or contact object cannot be subscribed to by others.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="20165-119">Essa configuração pode ter um impacto significativo no desempenho se estiver definida como um número alto, e o usuário médio tiver um grande número de usuários assinando sua presença.</span><span class="sxs-lookup"><span data-stu-id="20165-119">This setting can have a significant impact on performance if it is set to a high number, and the average user has a large number of users subscribing to his or her presence.</span></span>


</div></td>
<td><p><span data-ttu-id="20165-120">Positivo</span><span class="sxs-lookup"><span data-stu-id="20165-120">Integer</span></span></p></td>
<td><p><span data-ttu-id="20165-121">0-3000</span><span class="sxs-lookup"><span data-stu-id="20165-121">0-3000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20165-122">PromptedSubscribers</span><span class="sxs-lookup"><span data-stu-id="20165-122">PromptedSubscribers</span></span></p></td>
<td><p><span data-ttu-id="20165-123">Número máximo de alertas de assinatura de presença em fila</span><span class="sxs-lookup"><span data-stu-id="20165-123">Maximum Number of Queued Presence Subscription Alerts</span></span></p></td>
<td><p><span data-ttu-id="20165-124">Limita o número de entradas na tabela de assinantes solicitados.</span><span class="sxs-lookup"><span data-stu-id="20165-124">Limits the number of entries in the prompted subscribers table.</span></span> <span data-ttu-id="20165-125">Essa configuração determina o número máximo de solicitações que podem ser enfileiradas para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="20165-125">This setting determines the maximum number of prompts that can be queued for a given user.</span></span> <span data-ttu-id="20165-126">Por exemplo, quando o usuário assina a presença do usuário B, o usuário B recebe uma solicitação que o usuário A já está inscrito para o usuário B, e um prompt de confirmação é criado na tabela de assinantes solicitados do usuário B.</span><span class="sxs-lookup"><span data-stu-id="20165-126">For example, when user A subscribes to user B’s presence, user B receives a prompt that user A is now subscribed to user B, and an acknowledgement prompt is created in user B’s prompted subscribers table.</span></span> <span data-ttu-id="20165-127">Depois que o usuário B aceita, ou reconhece, a assinatura, o prompt de confirmação é removido da tabela de assinantes solicitados do usuário B.</span><span class="sxs-lookup"><span data-stu-id="20165-127">After user B accepts, or acknowledges, the subscription, the acknowledgement prompt is removed from user B’s prompted subscribers table.</span></span></p>
<p><span data-ttu-id="20165-128">Uma configuração 0 significa que o usuário não é avisado quando alguém assina sua presença.</span><span class="sxs-lookup"><span data-stu-id="20165-128">A setting of 0 means that the user is not prompted when someone subscribes to his or her presence.</span></span></p></td>
<td><p><span data-ttu-id="20165-129">Número inteiro ou token</span><span class="sxs-lookup"><span data-stu-id="20165-129">Integer or Token</span></span></p></td>
<td><p><span data-ttu-id="20165-130">0-500</span><span class="sxs-lookup"><span data-stu-id="20165-130">0-500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="20165-131">Por padrão, a **política** e o **serviço padrão:** as políticas de presença média são instaladas quando você implanta o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="20165-131">By default, the **Default Policy** and **Service: Medium** presence policies are installed when you deploy Lync Server.</span></span> <span data-ttu-id="20165-132">A tabela a seguir descreve as configurações específicas das duas políticas de presença.</span><span class="sxs-lookup"><span data-stu-id="20165-132">The following table describes the specific settings of the two presence policies.</span></span>

### <a name="presence-policies"></a><span data-ttu-id="20165-133">Políticas de presença</span><span class="sxs-lookup"><span data-stu-id="20165-133">Presence Policies</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20165-134">Nome da política</span><span class="sxs-lookup"><span data-stu-id="20165-134">Policy name</span></span></th>
<th><span data-ttu-id="20165-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="20165-135">Description</span></span></th>
<th><span data-ttu-id="20165-136">CategorySubscriptions</span><span class="sxs-lookup"><span data-stu-id="20165-136">CategorySubscriptions</span></span></th>
<th><span data-ttu-id="20165-137">PromptedSubscribers</span><span class="sxs-lookup"><span data-stu-id="20165-137">PromptedSubscribers</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20165-138">Política padrão</span><span class="sxs-lookup"><span data-stu-id="20165-138">Default Policy</span></span></p></td>
<td><p><span data-ttu-id="20165-139">Política para usuários típicos.</span><span class="sxs-lookup"><span data-stu-id="20165-139">Policy for typical users.</span></span> <span data-ttu-id="20165-140">Esta é a política de presença padrão.</span><span class="sxs-lookup"><span data-stu-id="20165-140">This is the default presence policy.</span></span></p></td>
<td><p><span data-ttu-id="20165-141">1000</span><span class="sxs-lookup"><span data-stu-id="20165-141">1000</span></span></p></td>
<td><p><span data-ttu-id="20165-142">200</span><span class="sxs-lookup"><span data-stu-id="20165-142">200</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20165-143">Serviço: médio</span><span class="sxs-lookup"><span data-stu-id="20165-143">Service: Medium</span></span></p></td>
<td><p><span data-ttu-id="20165-144">Política para aplicativos que exigem que mais usuários assinem a presença do objeto.</span><span class="sxs-lookup"><span data-stu-id="20165-144">Policy for applications that require more users to subscribe to the object’s presence.</span></span></p></td>
<td><p><span data-ttu-id="20165-145">1000</span><span class="sxs-lookup"><span data-stu-id="20165-145">1000</span></span></p></td>
<td><p><span data-ttu-id="20165-146">0</span><span class="sxs-lookup"><span data-stu-id="20165-146">0</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="20165-147">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20165-147">


</div>

<span> </span>

</div>

</div>

</span></span></div>

