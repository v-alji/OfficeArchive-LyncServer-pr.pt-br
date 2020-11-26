---
title: 'Lync Server 2013: Experiência do grupo de resposta durante falha no pool'
description: A experiência do grupo de resposta do Lync Server 2013 durante uma falha de pool.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Response group experience during pool failure
ms:assetid: 4e00fb38-64b1-4fd9-903d-7639177bc303
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204886(v=OCS.15)
ms:contentKeyID: 48184116
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d8d5904bc6934d4c330202bafa66d6dd8a16ff5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436241"
---
# <a name="response-group-experience-in-lync-server-2013-during-pool-failure"></a><span data-ttu-id="e6c68-103">Experiência do grupo de resposta no Lync Server 2013 durante falha no pool</span><span class="sxs-lookup"><span data-stu-id="e6c68-103">Response group experience in Lync Server 2013 during pool failure</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e6c68-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e6c68-104">

<span> </span></span></span>

<span data-ttu-id="e6c68-105">_**Tópico da última modificação:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="e6c68-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="e6c68-106">Esta seção descreve detalhadamente como a atividade do grupo de resposta é afetada nos seguintes estágios:</span><span class="sxs-lookup"><span data-stu-id="e6c68-106">This section describes in detail how response group activity is affected in the following stages:</span></span>

  - <span data-ttu-id="e6c68-107">Ocorre uma paralisação no pool primário, mas o failover ainda não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="e6c68-107">An outage occurs in the primary pool, but failover is not yet initiated.</span></span>

  - <span data-ttu-id="e6c68-108">O serviço falha no pool de backup.</span><span class="sxs-lookup"><span data-stu-id="e6c68-108">Service is failed over to the backup pool.</span></span>

  - <span data-ttu-id="e6c68-109">O serviço de volta ao pool primário.</span><span class="sxs-lookup"><span data-stu-id="e6c68-109">Service is failed back to the primary pool.</span></span>

<div>

## <a name="user-experience-when-outage-occurs"></a><span data-ttu-id="e6c68-110">Experiência do usuário quando ocorre uma falha</span><span class="sxs-lookup"><span data-stu-id="e6c68-110">User Experience When Outage Occurs</span></span>

<span data-ttu-id="e6c68-111">Quando ocorre uma falha de pool ou site, mas o administrador ainda não iniciou o failover, a atividade do grupo de resposta é manipulada conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e6c68-111">When a pool or site outage occurs, but the administrator has not yet initiated failover, response group activity is handled as described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e6c68-112">Durante a recuperação de desastres, as chamadas se comportam de forma diferente dependendo se os grupos de resposta do pool primário foram importados para o pool de backup durante a recuperação</span><span class="sxs-lookup"><span data-stu-id="e6c68-112">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="e6c68-113">Na tabela a seguir, as referências a grupos de resposta importados significam que os grupos de resposta de pool primário foram importados para o pool de backup durante o modo de recuperação de desastre.</span><span class="sxs-lookup"><span data-stu-id="e6c68-113">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="outage-occurs"></a><span data-ttu-id="e6c68-114">Ocorre uma falha</span><span class="sxs-lookup"><span data-stu-id="e6c68-114">Outage Occurs</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6c68-115">Tipo de ação do usuário ou chamada</span><span class="sxs-lookup"><span data-stu-id="e6c68-115">Type of call or user action</span></span></th>
<th><span data-ttu-id="e6c68-116">Durante a interrupção</span><span class="sxs-lookup"><span data-stu-id="e6c68-116">During outage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6c68-117">Chamadas conectadas a um agente</span><span class="sxs-lookup"><span data-stu-id="e6c68-117">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-118">As chamadas normais permanecem conectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-118">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-119">As chamadas anônimas são desconectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-119">Anonymous calls are disconnected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6c68-120">Chamadas em andamento ainda não conectadas a um agente</span><span class="sxs-lookup"><span data-stu-id="e6c68-120">In progress calls not yet connected to an agent</span></span></p></td>
<td><p><span data-ttu-id="e6c68-121">As chamadas são desconectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-121">Calls are disconnected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6c68-122">Novas chamadas</span><span class="sxs-lookup"><span data-stu-id="e6c68-122">New calls</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-123">As chamadas são desconectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-123">Calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-124">Se os grupos de resposta foram importados, as chamadas conectam-se ao pool de backup, mas os agentes hospedados no pool primário são inacessíveis.</span><span class="sxs-lookup"><span data-stu-id="e6c68-124">If response groups were imported, calls connect to backup pool, but agents homed in primary pool are unreachable.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6c68-125">Chamadas de agente em nome do grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="e6c68-125">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="e6c68-126">O recurso está desativado durante este estágio.</span><span class="sxs-lookup"><span data-stu-id="e6c68-126">Feature is disabled during this stage.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6c68-127">Informações de entrada e agente do agente</span><span class="sxs-lookup"><span data-stu-id="e6c68-127">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-128">Grupos de agente pertencentes ao pool primário podem ser visualizados no console do agente, mas os agentes não podem entrar.</span><span class="sxs-lookup"><span data-stu-id="e6c68-128">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-129">Grupos de agente pertencentes ao pool de backup podem ser visualizados no console do agente e os agentes podem entrar.</span><span class="sxs-lookup"><span data-stu-id="e6c68-129">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-130">Os grupos de agente importados não são exibidos no console do agente.</span><span class="sxs-lookup"><span data-stu-id="e6c68-130">Imported agent groups are not displayed on agent console.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6c68-131">Configuração do grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="e6c68-131">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-132">Os grupos de resposta pertencentes ao pool primário podem ser exibidos, dependendo da disponibilidade do banco de dados back-end do pool primário, mas não podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="e6c68-132">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-133">Os grupos de resposta pertencentes ao pool de backup podem ser exibidos e modificados.</span><span class="sxs-lookup"><span data-stu-id="e6c68-133">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-134">Os grupos de resposta importados não podem ser exibidos com o painel de controle do Lync Server ou com a ferramenta de configuração de grupo de resposta, mas podem ser configurados usando cmdlets do Shell de gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="e6c68-134">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-experience-during-failover"></a><span data-ttu-id="e6c68-135">Experiência do usuário durante o failover</span><span class="sxs-lookup"><span data-stu-id="e6c68-135">User Experience During Failover</span></span>

<span data-ttu-id="e6c68-136">Quando um administrador invoca o failover para um pool de backup, a atividade do grupo de resposta é manipulada durante e após o failover conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e6c68-136">When an administrator invokes failover to a backup pool, response group activity is handled during and after the failover as described in the following table.</span></span> <span data-ttu-id="e6c68-137">A primeira coluna descreve o tipo de atividade que pode estar ocorrendo.</span><span class="sxs-lookup"><span data-stu-id="e6c68-137">The first column describes the type of activity that might be taking place.</span></span> <span data-ttu-id="e6c68-138">A coluna do meio descreve como cada atividade é manipulada durante o tempo curto necessário para failover para o pool de backup.</span><span class="sxs-lookup"><span data-stu-id="e6c68-138">The middle column describes how each activity is handled during the brief time that it takes to fail over to the backup pool.</span></span> <span data-ttu-id="e6c68-139">A última coluna descreve como a atividade é manipulada pela duração, após o término do processo de failover e o pool de backup se posicionar para o pool primário.</span><span class="sxs-lookup"><span data-stu-id="e6c68-139">The last column describes how the activity is handled for the duration, after the failover process is complete and the backup pool is standing in for the primary pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e6c68-140">Durante a recuperação de desastres, as chamadas se comportam de forma diferente dependendo se os grupos de resposta do pool primário foram importados para o pool de backup durante a recuperação</span><span class="sxs-lookup"><span data-stu-id="e6c68-140">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="e6c68-141">Na tabela a seguir, as referências a grupos de resposta importados significam que os grupos de resposta de pool primário foram importados para o pool de backup durante o modo de recuperação de desastre.</span><span class="sxs-lookup"><span data-stu-id="e6c68-141">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="failover-is-initiated"></a><span data-ttu-id="e6c68-142">O failover é iniciado</span><span class="sxs-lookup"><span data-stu-id="e6c68-142">Failover Is Initiated</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6c68-143">Tipo de ação do usuário ou chamada</span><span class="sxs-lookup"><span data-stu-id="e6c68-143">Type of call or user action</span></span></th>
<th><span data-ttu-id="e6c68-144">Durante o failover</span><span class="sxs-lookup"><span data-stu-id="e6c68-144">During Failover</span></span></th>
<th><span data-ttu-id="e6c68-145">Após a conclusão do failover</span><span class="sxs-lookup"><span data-stu-id="e6c68-145">After Failover Completes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6c68-146">Chamadas conectadas a um agente</span><span class="sxs-lookup"><span data-stu-id="e6c68-146">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-147">As chamadas normais permanecem conectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-147">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-148">As chamadas anônimas são desconectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-148">Anonymous calls are disconnected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-149">As chamadas normais permanecem conectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-149">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-150">Para grupos de resposta importados, chamadas anônimas que atingiram o pool de backup permanecerão conectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-150">For imported response groups, anonymous calls that have reached the backup pool remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6c68-151">Chamadas em andamento ainda não conectadas a um agente</span><span class="sxs-lookup"><span data-stu-id="e6c68-151">In progress calls not yet connected to an agent</span></span></p></td>
<td><p><span data-ttu-id="e6c68-152">As chamadas são desconectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-152">Calls are disconnected.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-153">Se os grupos de resposta não foram importados, nenhuma chamada está nesse status.</span><span class="sxs-lookup"><span data-stu-id="e6c68-153">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-154">Para os grupos de resposta importados, as chamadas que atingiram o pool de backup permanecerão conectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-154">For imported response groups, calls that have reached the backup pool remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6c68-155">Novas chamadas</span><span class="sxs-lookup"><span data-stu-id="e6c68-155">New calls</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-156">As chamadas são desconectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-156">Calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-157">Para grupos de resposta importados, chamadas conectam-se ao pool de backup, mas os agentes hospedados no pool primário não são acessíveis.</span><span class="sxs-lookup"><span data-stu-id="e6c68-157">For imported response groups, calls connect to the backup pool, but agents homed in the primary pool are unreachable.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-158">Se os grupos de resposta não foram importados, as chamadas serão desconectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-158">If response groups were not imported, calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-159">Para grupos de resposta importados, chamadas conectam-se ao pool de backup.</span><span class="sxs-lookup"><span data-stu-id="e6c68-159">For imported response groups, calls connect to the backup pool.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6c68-160">Chamadas de agente em nome do grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="e6c68-160">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="e6c68-161">O recurso está desativado durante este estágio</span><span class="sxs-lookup"><span data-stu-id="e6c68-161">Feature is disabled during this stage</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-162">Se os grupos de resposta não foram importados, as chamadas falharão.</span><span class="sxs-lookup"><span data-stu-id="e6c68-162">If response groups were not imported, calls fail.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-163">Para os grupos de resposta importados, as chamadas são bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-163">For imported response groups, calls succeed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6c68-164">Informações de entrada e agente do agente</span><span class="sxs-lookup"><span data-stu-id="e6c68-164">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-165">Grupos de agente pertencentes ao pool primário podem ser visualizados no console do agente, mas os agentes não podem entrar.</span><span class="sxs-lookup"><span data-stu-id="e6c68-165">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-166">Grupos de agente pertencentes ao pool de backup podem ser visualizados no console do agente e os agentes podem entrar.</span><span class="sxs-lookup"><span data-stu-id="e6c68-166">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-167">Grupos de agente importados são exibidos no console do agente e os agentes podem entrar.</span><span class="sxs-lookup"><span data-stu-id="e6c68-167">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-168">Grupos de agente pertencentes ao pool primário podem ser visualizados no console do agente, mas os agentes não podem entrar.</span><span class="sxs-lookup"><span data-stu-id="e6c68-168">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-169">Grupos de agente pertencentes ao pool de backup podem ser visualizados no console do agente e os agentes podem entrar.</span><span class="sxs-lookup"><span data-stu-id="e6c68-169">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-170">Grupos de agente importados são exibidos no console do agente e os agentes podem entrar.</span><span class="sxs-lookup"><span data-stu-id="e6c68-170">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6c68-171">Configuração do grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="e6c68-171">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-172">Os grupos de resposta pertencentes ao pool primário podem ser exibidos, dependendo da disponibilidade do banco de dados back-end do pool primário, mas não podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="e6c68-172">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-173">Os grupos de resposta pertencentes ao pool de backup podem ser exibidos e modificados.</span><span class="sxs-lookup"><span data-stu-id="e6c68-173">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-174">Os grupos de resposta importados não podem ser exibidos com o painel de controle do Lync Server ou com a ferramenta de configuração de grupo de resposta, mas podem ser configurados usando cmdlets do Shell de gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="e6c68-174">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-175">Os grupos de resposta pertencentes ao pool primário podem ser exibidos, dependendo da disponibilidade do banco de dados back-end, mas não podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="e6c68-175">Response groups owned by the primary pool can be viewed, depending on the availability of the back end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-176">Os grupos de resposta pertencentes ao pool de backup podem ser exibidos e modificados.</span><span class="sxs-lookup"><span data-stu-id="e6c68-176">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-177">Os grupos de resposta importados não podem ser exibidos com o painel de controle do Lync Server ou com a ferramenta de configuração de grupo de resposta, mas podem ser configurados usando cmdlets do Shell de gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="e6c68-177">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-experience-during-failback"></a><span data-ttu-id="e6c68-178">Experiência do usuário durante o failback</span><span class="sxs-lookup"><span data-stu-id="e6c68-178">User Experience During Failback</span></span>

<span data-ttu-id="e6c68-179">Quando um administrador invoca o failback para o pool primário, a atividade do grupo de resposta é manipulada durante e após o failback, conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e6c68-179">When an administrator invokes failback to the primary pool, response group activity is handled during and after the failback as described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e6c68-180">Durante a recuperação de desastres, as chamadas se comportam de forma diferente dependendo se os grupos de resposta do pool primário foram importados para o pool de backup durante a recuperação</span><span class="sxs-lookup"><span data-stu-id="e6c68-180">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="e6c68-181">Na tabela a seguir, as referências a grupos de resposta importados significam que os grupos de resposta de pool primário foram importados para o pool de backup durante o modo de recuperação de desastre.</span><span class="sxs-lookup"><span data-stu-id="e6c68-181">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="call-handling-in-failback"></a><span data-ttu-id="e6c68-182">Tratamento de chamadas em failback</span><span class="sxs-lookup"><span data-stu-id="e6c68-182">Call Handling in Failback</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6c68-183">Tipo de ação do usuário ou chamada</span><span class="sxs-lookup"><span data-stu-id="e6c68-183">Type of call or user action</span></span></th>
<th><span data-ttu-id="e6c68-184">Durante o failback</span><span class="sxs-lookup"><span data-stu-id="e6c68-184">During Failback</span></span></th>
<th><span data-ttu-id="e6c68-185">Após a conclusão do failback</span><span class="sxs-lookup"><span data-stu-id="e6c68-185">After Failback Completes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6c68-186">Chamadas conectadas a um agente</span><span class="sxs-lookup"><span data-stu-id="e6c68-186">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-187">As chamadas normais permanecem conectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-187">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-188">Se os grupos de resposta não foram importados, não há chamadas anônimas nesse status.</span><span class="sxs-lookup"><span data-stu-id="e6c68-188">If response groups were not imported, no anonymous calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-189">Para grupos de resposta importados, as chamadas anônimas permanecem conectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-189">For imported response groups, anonymous calls remain connected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-190">As chamadas normais permanecem conectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-190">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-191">Se os grupos de resposta não foram importados, não há chamadas anônimas nesse status.</span><span class="sxs-lookup"><span data-stu-id="e6c68-191">If response groups were not imported, no anonymous calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-192">Para grupos de resposta importados, as chamadas anônimas permanecem conectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-192">For imported response groups, anonymous calls remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6c68-193">Chamadas em andamento ainda não conectadas a um agente</span><span class="sxs-lookup"><span data-stu-id="e6c68-193">In progress calls not yet connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-194">Se os grupos de resposta não foram importados, nenhuma chamada está nesse status.</span><span class="sxs-lookup"><span data-stu-id="e6c68-194">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-195">Para os grupos de resposta importados, as chamadas serão desconectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-195">For imported response groups, calls will be disconnected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-196">Se os grupos de resposta não foram importados, nenhuma chamada está nesse status.</span><span class="sxs-lookup"><span data-stu-id="e6c68-196">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-197">Para os grupos de resposta importados, as chamadas serão desconectadas.</span><span class="sxs-lookup"><span data-stu-id="e6c68-197">For imported response groups, calls will be disconnected.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6c68-198">Novas chamadas</span><span class="sxs-lookup"><span data-stu-id="e6c68-198">New calls</span></span></p></td>
<td><p><span data-ttu-id="e6c68-199">Chamadas conectadas ao pool primário, mas os agentes hospedados no pool primário não são acessíveis.</span><span class="sxs-lookup"><span data-stu-id="e6c68-199">Calls connect to the primary pool, but agents homed in the primary pool are unreachable.</span></span></p></td>
<td><p><span data-ttu-id="e6c68-200">Chamadas conectadas ao pool primário.</span><span class="sxs-lookup"><span data-stu-id="e6c68-200">Calls connect to the primary pool.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6c68-201">Chamadas de agente em nome do grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="e6c68-201">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="e6c68-202">O recurso está desativado durante este estágio.</span><span class="sxs-lookup"><span data-stu-id="e6c68-202">Feature is disabled during this stage.</span></span></p></td>
<td><p><span data-ttu-id="e6c68-203">Chamadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="e6c68-203">Calls succeed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6c68-204">Informações de entrada e agente do agente</span><span class="sxs-lookup"><span data-stu-id="e6c68-204">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-205">Grupos de agente pertencentes ao pool primário podem ser visualizados no console do agente, mas os agentes não podem entrar.</span><span class="sxs-lookup"><span data-stu-id="e6c68-205">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-206">Grupos de agente pertencentes ao pool de backup podem ser visualizados no console do agente e os agentes podem entrar.</span><span class="sxs-lookup"><span data-stu-id="e6c68-206">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-207">Grupos de agente importados são exibidos no console do agente e os agentes podem entrar.</span><span class="sxs-lookup"><span data-stu-id="e6c68-207">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-208">Grupos de agente pertencentes ao pool primário podem ser visualizados no console do agente e os agentes podem entrar.</span><span class="sxs-lookup"><span data-stu-id="e6c68-208">Agent groups owned by the primary pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-209">Grupos de agente pertencentes ao pool de backup podem ser visualizados no console do agente e os agentes podem entrar.</span><span class="sxs-lookup"><span data-stu-id="e6c68-209">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-210">Os grupos de agente importados não são exibidos no console do agente.</span><span class="sxs-lookup"><span data-stu-id="e6c68-210">Imported agent groups are not displayed on agent console.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6c68-211">Configuração do grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="e6c68-211">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-212">Os grupos de resposta pertencentes ao pool primário podem ser exibidos, dependendo da disponibilidade do banco de dados back-end do pool primário, mas não podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="e6c68-212">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-213">Os grupos de resposta pertencentes ao pool de backup podem ser exibidos e modificados.</span><span class="sxs-lookup"><span data-stu-id="e6c68-213">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-214">Os grupos de resposta importados não podem ser exibidos com o painel de controle do Lync Server ou com a ferramenta de configuração de grupo de resposta, mas podem ser configurados usando cmdlets do Shell de gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="e6c68-214">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="e6c68-215">Os grupos de resposta pertencentes ao pool primário podem ser exibidos e modificados.</span><span class="sxs-lookup"><span data-stu-id="e6c68-215">Response groups owned by the primary pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-216">Os grupos de resposta pertencentes ao pool de backup podem ser exibidos e modificados.</span><span class="sxs-lookup"><span data-stu-id="e6c68-216">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="e6c68-217">Os grupos de resposta importados não podem ser exibidos com o painel de controle do Lync Server ou com a ferramenta de configuração de grupo de resposta, mas podem ser configurados usando cmdlets do Shell de gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="e6c68-217">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="e6c68-218">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e6c68-218">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

