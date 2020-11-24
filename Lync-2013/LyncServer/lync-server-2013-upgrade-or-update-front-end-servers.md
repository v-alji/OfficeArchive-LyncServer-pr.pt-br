---
title: 'Lync Server 2013: atualizar ou atualizar servidores front-end'
description: 'Lync Server 2013: atualizar ou atualizar servidores front-end.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Upgrade or update Front End Servers
ms:assetid: 20fa39ae-ecfb-4c72-9cc4-8e183d3c752f
ms:mtpsurl: https://technet.microsoft.com/library/JJ204736(v=OCS.15)
ms:contentKeyID: 48183597
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5340ca5549aeff51b275798572573b2c9f017644
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390209"
---
# <a name="upgrade-or-update-front-end-servers-in-lync-server-2013"></a><span data-ttu-id="f7b33-103">Upgrade or update Front End Servers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7b33-103">Upgrade or update Front End Servers in Lync Server 2013</span></span>

<div data-xmlns="https://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="https://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f7b33-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f7b33-104">

<span> </span></span></span>

<span data-ttu-id="f7b33-105">_**Tópico da última modificação:** 2013-06-28_</span><span class="sxs-lookup"><span data-stu-id="f7b33-105">_**Topic Last Modified:** 2013-06-28_</span></span>

<span data-ttu-id="f7b33-106">Os servidores de front-end em um pool da edição Enterprise são organizados em *domínios de atualização*.</span><span class="sxs-lookup"><span data-stu-id="f7b33-106">The Front End Servers in an Enterprise Edition pool are organized into *upgrade domains*.</span></span> <span data-ttu-id="f7b33-107">Esses são subconjuntos de servidores front-end no pool.</span><span class="sxs-lookup"><span data-stu-id="f7b33-107">These are subsets of Front End Servers in the pool.</span></span> <span data-ttu-id="f7b33-108">Os domínios de atualização são criados automaticamente pelo construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="f7b33-108">Upgrade Domains are created automatically by Topology Builder.</span></span>

<span data-ttu-id="f7b33-109">Ao atualizar os servidores, você deve fazer um domínio de atualização de cada vez.</span><span class="sxs-lookup"><span data-stu-id="f7b33-109">When you upgrade servers, you must do so one Upgrade Domain at a time.</span></span> <span data-ttu-id="f7b33-110">Coloque cada servidor em um domínio de atualização abaixo, atualize-o e reinicie-o antes de passar para outro domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="f7b33-110">Bring each Server in one Upgrade Domain down, upgrade it, and then restart it before you move on to another Upgrade Domain.</span></span> <span data-ttu-id="f7b33-111">Certifique-se de acompanhar quais domínios e servidores de atualização você atualizou até agora.</span><span class="sxs-lookup"><span data-stu-id="f7b33-111">Be sure to keep track of which Upgrade Domains and Servers that you have upgraded so far.</span></span> <span data-ttu-id="f7b33-112">Use o diagrama de fluxograma a seguir ao atualizar cada servidor.</span><span class="sxs-lookup"><span data-stu-id="f7b33-112">Use the following flowchart diagram when upgrading each server.</span></span>

![Atualizar ou atualizar servidores front-end](images/upgradeupdatefrontendserverslync2013.png)

<div>

## <a name="to-apply-an-upgrade-to-the-front-end-servers-in-a-pool"></a><span data-ttu-id="f7b33-114">Para aplicar uma atualização aos servidores Front-End em um pool</span><span class="sxs-lookup"><span data-stu-id="f7b33-114">To apply an upgrade to the Front End servers in a pool</span></span>

1.  <span data-ttu-id="f7b33-115">Em um servidor front-end do pool, execute o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f7b33-115">On a Front End Server in the pool, run the following cmdlet:</span></span>
    
    <span data-ttu-id="f7b33-116">**Get-CsPoolUpgradeReadinessState**</span><span class="sxs-lookup"><span data-stu-id="f7b33-116">**Get-CsPoolUpgradeReadinessState**</span></span>
    
    <span data-ttu-id="f7b33-117">Se o valor de *PoolUpgradeState* estiver **ocupado**, aguarde 10 minutos e tente **Get-CsPoolUpgradeReadinessState** novamente.</span><span class="sxs-lookup"><span data-stu-id="f7b33-117">If the value of *PoolUpgradeState* is **Busy**, wait for 10 minutes, and then try **Get-CsPoolUpgradeReadinessState** again.</span></span> <span data-ttu-id="f7b33-118">Se você vir **ocupado** pelo menos três vezes consecutivos, após esperar 10 minutos entre cada tentativa, ou se vir qualquer resultado de **InsufficientActiveFrontEnds** para **PoolUpgradeState,** há um problema com o pool.</span><span class="sxs-lookup"><span data-stu-id="f7b33-118">If you see **Busy** for at least three consecutive times, after waiting 10 minutes in between each attempt, or if you see any result of **InsufficientActiveFrontEnds** for **PoolUpgradeState,** then there is an issue with the pool.</span></span> <span data-ttu-id="f7b33-119">Se esse pool estiver emparelhado com outro pool de front-ends em uma topologia de recuperação de desastre, você deverá fazer failover do pool para o pool de backup e, em seguida, atualizar os servidores nesse pool.</span><span class="sxs-lookup"><span data-stu-id="f7b33-119">If this pool is paired with another Front End pool in a disaster recovery topology, you should fail the pool over to the backup pool, and then update the servers in this pool.</span></span> <span data-ttu-id="f7b33-120">Para obter detalhes, consulte [falha em um pool no Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span><span class="sxs-lookup"><span data-stu-id="f7b33-120">For details, see [Failing over a pool in Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span></span>
    
    <span data-ttu-id="f7b33-121">Se o valor de *PoolUpgradeState* estiver **pronto**, vá para a etapa 2.</span><span class="sxs-lookup"><span data-stu-id="f7b33-121">If the value of *PoolUpgradeState* is **Ready**, go to step 2.</span></span>

2.  <span data-ttu-id="f7b33-122">O cmdlet **Get-CsPoolUpgradeReadinessState** também retorna informações sobre cada domínio de atualização do pool e sobre quais servidores de front-end estão em cada domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="f7b33-122">The **Get-CsPoolUpgradeReadinessState** cmdlet also returns information about each upgrade domain in the pool, and about which Front End Servers are in each upgrade domain.</span></span> <span data-ttu-id="f7b33-123">Se o valor de **ReadyforUpgrade** for **verdadeiro** para o domínio de atualização que contém o servidor ou servidores que você deseja atualizar, você pode atualizar os servidores com segurança agora.</span><span class="sxs-lookup"><span data-stu-id="f7b33-123">If the **ReadyforUpgrade** value is **True** for the upgrade domain that contains the server or servers you want to upgrade, you can safely upgrade those servers now.</span></span> <span data-ttu-id="f7b33-124">Para fazer isso, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f7b33-124">To do so, do the following:</span></span>
    
    1.  <span data-ttu-id="f7b33-125">Pare as novas conexões com os servidores front end que você vai atualizar usando o `Stop-CsWindowsService -Graceful -Verbose` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7b33-125">Stop new connections to the Front End Servers you are going to upgrade by using the `Stop-CsWindowsService -Graceful -Verbose` cmdlet.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="f7b33-126">Se você estiver executando essas atualizações do servidor durante um tempo de inatividade do servidor programado, poderá executar esse cmdlet sem o parâmetro '-<STRONG>normal</STRONG>', da seguinte maneira: <STRONG>Stop-CsWindowsService</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f7b33-126">If you are performing these server upgrades during a scheduled server downtime, you can run this cmdlet without the ‘-<STRONG>Graceful</STRONG>‘ parameter, as follows: <STRONG>Stop-CsWindowsService</STRONG>.</span></span> <span data-ttu-id="f7b33-127">Isso encerrará imediatamente os serviços, sem esperar que todas as solicitações de serviço existentes sejam preenchidas.</span><span class="sxs-lookup"><span data-stu-id="f7b33-127">This will immediately shut down services, without waiting for all existing service requests to be filled.</span></span>

        
        </div>
    
    2.  <span data-ttu-id="f7b33-128">Atualize os servidores associados a este domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="f7b33-128">Upgrade the servers associated with this the Upgrade Domain.</span></span>
    
    3.  <span data-ttu-id="f7b33-129">Reinicie os servidores e certifique-se de que eles estejam aceitando novas conexões.</span><span class="sxs-lookup"><span data-stu-id="f7b33-129">Restart the servers, and make sure they are accepting new connections.</span></span>

3.  <span data-ttu-id="f7b33-130">Repita as etapas 1 e 2 para cada outro domínio de atualização do pool, até que todos os servidores front end tenham sido atualizados.</span><span class="sxs-lookup"><span data-stu-id="f7b33-130">Repeat Steps 1 and 2 for each other Upgrade Domain in the pool, until all Front End Servers have been upgraded.</span></span>

<span data-ttu-id="f7b33-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f7b33-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

