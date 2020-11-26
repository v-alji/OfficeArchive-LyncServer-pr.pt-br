---
title: 'Lync Server 2013: gerenciar a coleta de chamadas em grupo durante a recuperação de desastres'
description: 'Lync Server 2013: gerenciar a coleta de chamadas em grupo durante a recuperação de desastres.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage Group Call Pickup during disaster recovery
ms:assetid: 2d32f19f-c649-4a72-a4fb-edd338e3a7cc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945618(v=OCS.15)
ms:contentKeyID: 51541455
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 04d85bc83cfe35571c2b0f47f707c9dcd8037d80
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426099"
---
# <a name="manage-group-call-pickup-during-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="4fdee-103">Gerenciar a coleta de chamadas em grupo durante a recuperação de desastres no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4fdee-103">Manage Group Call Pickup during disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4fdee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4fdee-104">

<span> </span></span></span>

<span data-ttu-id="4fdee-105">_**Tópico da última modificação:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="4fdee-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="4fdee-106">Quando um pool de front-end fica indisponível devido a um incidente não planejado, o serviço falha no pool de backup.</span><span class="sxs-lookup"><span data-stu-id="4fdee-106">When a Front End pool becomes unavailable due an unplanned incident, service is failed over to the backup pool.</span></span> <span data-ttu-id="4fdee-107">Durante o failover para o pool de backup, os usuários são redirecionados para o pool de backup e estão no modo de resiliência.</span><span class="sxs-lookup"><span data-stu-id="4fdee-107">During failover to the backup pool, users are redirected to the backup pool and are in resiliency mode.</span></span> <span data-ttu-id="4fdee-108">Enquanto estiver no modo de resiliência, os usuários não poderão atender as chamadas de outros usuários ou fazer com que as chamadas sejam selecionadas por outros usuários.</span><span class="sxs-lookup"><span data-stu-id="4fdee-108">While in resiliency mode, users cannot pick up other users' calls or have their calls picked up by other users.</span></span> <span data-ttu-id="4fdee-109">Quando o failover for concluído, os usuários poderão usar novamente o recurso de recebimento de chamadas em grupo normalmente.</span><span class="sxs-lookup"><span data-stu-id="4fdee-109">When failover is complete, users can again use Group Call Pickup as usual.</span></span>

<span data-ttu-id="4fdee-110">Durante o failback para o pool primário, os usuários são redirecionados para o pool primário e são novamente no modo de resiliência.</span><span class="sxs-lookup"><span data-stu-id="4fdee-110">During failback to the primary pool, users are redirected to the primary pool and are again in resiliency mode.</span></span> <span data-ttu-id="4fdee-111">A funcionalidade de recebimento de chamada de grupo não estará disponível até que os usuários estejam fora do modo de resiliência.</span><span class="sxs-lookup"><span data-stu-id="4fdee-111">Group Call Pickup functionality is not available until the users are out of resiliency mode.</span></span>

<span data-ttu-id="4fdee-112">Esta seção discute algumas considerações para o recebimento de chamadas em grupo durante a recuperação de desastres e também descreve a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="4fdee-112">This section discusses some considerations for Group Call Pickup during disaster recovery and also describes the user experience.</span></span>

<div>

## <a name="considerations-for-group-call-pickup-during-disaster-recovery"></a><span data-ttu-id="4fdee-113">Considerações sobre o recebimento de chamadas em grupo durante a recuperação de desastres</span><span class="sxs-lookup"><span data-stu-id="4fdee-113">Considerations for Group Call Pickup During Disaster Recovery</span></span>

<span data-ttu-id="4fdee-114">Durante a recuperação de desastres, os usuários que foram redirecionados para o pool de backup como parte do processo de failover usam o aplicativo de estacionamento de chamada executado no pool de backup para os números de grupo de recebimento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="4fdee-114">During disaster recovery, users who have been redirected to the backup pool as part of the failover process use the Call Park application running in the backup pool for the call pickup group numbers.</span></span> <span data-ttu-id="4fdee-115">Portanto, o suporte para o recebimento de chamadas em grupo durante a recuperação de desastres requer que o aplicativo parque de chamadas seja implantado e habilitado no pool primário e no pool de backup.</span><span class="sxs-lookup"><span data-stu-id="4fdee-115">Therefore, support for Group Call Pickup during disaster recovery requires the Call Park application to be deployed and enabled in both the primary pool and the backup pool.</span></span>

<span data-ttu-id="4fdee-116">Os intervalos de números do recurso de chamada em grupo na tabela órbita do parque de chamadas devem ser redirecionados para o pool de backup após o término do processo de failover do pool de backup.</span><span class="sxs-lookup"><span data-stu-id="4fdee-116">The Group Call Pickup number ranges in the call park orbit table must be redirected to the backup pool after the failover process to the backup pool is complete.</span></span> <span data-ttu-id="4fdee-117">Os intervalos de números devem ser redirecionados para o pool primário após a conclusão do processo de failback para o pool primário.</span><span class="sxs-lookup"><span data-stu-id="4fdee-117">The number ranges must be redirected back to the primary pool after the failback process to the primary pool is complete.</span></span> <span data-ttu-id="4fdee-118">Para redirecionar os intervalos de recebimento da chamada em grupo, use o cmdlet **set-CsCallParkOrbit** .</span><span class="sxs-lookup"><span data-stu-id="4fdee-118">To redirect the Group Call Pickup ranges, use the **Set-CsCallParkOrbit** cmdlet.</span></span>

<span data-ttu-id="4fdee-119">Se você implantar um novo pool com um nome de domínio totalmente qualificado (FQDN) diferente para substituir o pool primário, será necessário reatribuir todos os intervalos de número de retirada de chamada de grupo que foram associados ao pool primário ao FQDN do novo pool.</span><span class="sxs-lookup"><span data-stu-id="4fdee-119">If you deploy a new pool with a different fully qualified domain name (FQDN) to replace the primary pool, you need to reassign all the Group Call Pickup number ranges that were associated with the primary pool to the FQDN of the new pool.</span></span> <span data-ttu-id="4fdee-120">Para reatribuir intervalos de números ao novo pool, você pode usar o cmdlet **set-CsCallParkOrbit** .</span><span class="sxs-lookup"><span data-stu-id="4fdee-120">To reassign number ranges to the new pool, you can use the **Set-CsCallParkOrbit** cmdlet.</span></span> <span data-ttu-id="4fdee-121">Para obter detalhes sobre o cmdlet **set-CsCallParkOrbit** , consulte [set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit).</span><span class="sxs-lookup"><span data-stu-id="4fdee-121">For details about the **Set-CsCallParkOrbit** cmdlet, see [Set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit).</span></span>

</div>

<div>

## <a name="group-call-pickup-experience-during-pool-failure"></a><span data-ttu-id="4fdee-122">Experiência de recebimento de chamadas em grupo durante falha de pool</span><span class="sxs-lookup"><span data-stu-id="4fdee-122">Group Call Pickup Experience During Pool Failure</span></span>

<span data-ttu-id="4fdee-123">A tabela a seguir resume a experiência de retirada de chamadas em grupo pelas fases da recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="4fdee-123">The following table summarizes the Group Call Pickup experience through the phases of disaster recovery.</span></span>

### <a name="user-experience-during-disaster-recovery"></a><span data-ttu-id="4fdee-124">Experiência do usuário durante a recuperação de desastres</span><span class="sxs-lookup"><span data-stu-id="4fdee-124">User Experience During Disaster Recovery</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4fdee-125">Estado da chamada</span><span class="sxs-lookup"><span data-stu-id="4fdee-125">Call state</span></span></th>
<th><span data-ttu-id="4fdee-126">Failover para pool de backup</span><span class="sxs-lookup"><span data-stu-id="4fdee-126">Failover to backup pool</span></span></th>
<th><span data-ttu-id="4fdee-127">Failback para pool primário</span><span class="sxs-lookup"><span data-stu-id="4fdee-127">Failback to primary pool</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4fdee-128">Novas chamadas</span><span class="sxs-lookup"><span data-stu-id="4fdee-128">New calls</span></span></p></td>
<td><p><span data-ttu-id="4fdee-129"><strong>Durante o processo de failover:</strong></span><span class="sxs-lookup"><span data-stu-id="4fdee-129"><strong>During failover process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4fdee-130">Retirada de chamadas em grupo não disponível para usuários no modo de resiliência</span><span class="sxs-lookup"><span data-stu-id="4fdee-130">Group Call Pickup not available for users in resiliency mode</span></span></p></li>
</ul>
<p><span data-ttu-id="4fdee-131"><strong>Após a conclusão do failover:</strong></span><span class="sxs-lookup"><span data-stu-id="4fdee-131"><strong>After failover is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4fdee-132">Retirada de chamadas em grupo disponível quando os usuários estiverem fora da resiliência e os intervalos de números de recebimento de chamadas em grupo forem redirecionados para o pool de backup</span><span class="sxs-lookup"><span data-stu-id="4fdee-132">Group Call Pickup available when users out of resiliency and Group Call Pickup number ranges are redirected to backup pool</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="4fdee-133"><strong>Durante o processo de failback:</strong></span><span class="sxs-lookup"><span data-stu-id="4fdee-133"><strong>During failback process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4fdee-134">Retirada de chamadas em grupo não disponível para usuários no modo de resiliência</span><span class="sxs-lookup"><span data-stu-id="4fdee-134">Group Call Pickup not available for users in resiliency mode</span></span></p></li>
</ul>
<p><span data-ttu-id="4fdee-135"><strong>Após concluir o failback:</strong></span><span class="sxs-lookup"><span data-stu-id="4fdee-135"><strong>After failback is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4fdee-136">Retirada de chamadas em grupo disponível quando os usuários estiverem fora da resiliência e os intervalos de números de recebimento de chamadas em grupo forem redirecionados para o pool primário</span><span class="sxs-lookup"><span data-stu-id="4fdee-136">Group Call Pickup available when users out of resiliency and Group Call Pickup number ranges are redirected back to primary pool</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fdee-137">Chamadas na fila de recebimento de chamadas em grupo</span><span class="sxs-lookup"><span data-stu-id="4fdee-137">Calls in Group Call Pickup queue</span></span></p></td>
<td><p><span data-ttu-id="4fdee-138"><strong>Durante o processo de failover:</strong></span><span class="sxs-lookup"><span data-stu-id="4fdee-138"><strong>During failover process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4fdee-139">As chamadas na fila não podem ser atendidas por meio da retirada de chamadas em grupo.</span><span class="sxs-lookup"><span data-stu-id="4fdee-139">Calls in queue cannot be answered through Group Call Pickup.</span></span></p></li>
</ul>
<p><span data-ttu-id="4fdee-140"><strong>Após a conclusão do failover:</strong></span><span class="sxs-lookup"><span data-stu-id="4fdee-140"><strong>After failover is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4fdee-141">Nenhuma chamada neste estado</span><span class="sxs-lookup"><span data-stu-id="4fdee-141">No calls in this state</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="4fdee-142"><strong>Durante o processo de failback:</strong></span><span class="sxs-lookup"><span data-stu-id="4fdee-142"><strong>During failback process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4fdee-143">As chamadas na fila não podem ser atendidas por meio da retirada de chamadas em grupo.</span><span class="sxs-lookup"><span data-stu-id="4fdee-143">Calls in queue cannot be answered through Group Call Pickup.</span></span></p></li>
</ul>
<p><span data-ttu-id="4fdee-144"><strong>Após concluir o failback:</strong></span><span class="sxs-lookup"><span data-stu-id="4fdee-144"><strong>After failback is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4fdee-145">As chamadas na fila não podem ser atendidas por meio da retirada de chamadas em grupo.</span><span class="sxs-lookup"><span data-stu-id="4fdee-145">Calls in queue cannot be answered through Group Call Pickup.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fdee-146">Chamada estabelecida</span><span class="sxs-lookup"><span data-stu-id="4fdee-146">Established call</span></span></p></td>
<td><p><span data-ttu-id="4fdee-147"><strong>Durante o processo de failover:</strong></span><span class="sxs-lookup"><span data-stu-id="4fdee-147"><strong>During failover process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4fdee-148">As chamadas permanecem conectadas</span><span class="sxs-lookup"><span data-stu-id="4fdee-148">Calls stay connected</span></span></p></li>
</ul>
<p><span data-ttu-id="4fdee-149"><strong>Após a conclusão do failover:</strong></span><span class="sxs-lookup"><span data-stu-id="4fdee-149"><strong>After failover is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4fdee-150">As chamadas permanecem conectadas</span><span class="sxs-lookup"><span data-stu-id="4fdee-150">Calls stay connected</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="4fdee-151"><strong>Durante o processo de failback:</strong></span><span class="sxs-lookup"><span data-stu-id="4fdee-151"><strong>During failback process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4fdee-152">As chamadas permanecem conectadas</span><span class="sxs-lookup"><span data-stu-id="4fdee-152">Calls stay connected</span></span></p></li>
</ul>
<p><span data-ttu-id="4fdee-153"><strong>Após concluir o failback:</strong></span><span class="sxs-lookup"><span data-stu-id="4fdee-153"><strong>After failback is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4fdee-154">As chamadas permanecem conectadas</span><span class="sxs-lookup"><span data-stu-id="4fdee-154">Calls stay connected</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="4fdee-155">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4fdee-155">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

