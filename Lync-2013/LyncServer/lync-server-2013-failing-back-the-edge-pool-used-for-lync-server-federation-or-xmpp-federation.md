---
title: Failback do pool de Borda usado para federação do Lync Server ou federação XMPP
description: Failback do pool de bordas usado para Federação do Lync Server ou Federação do XMPP.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing back the Edge pool used for Lync Server federation or XMPP federation
ms:assetid: d40097a1-1bed-44dc-aeb6-0871927ab2b9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721897(v=OCS.15)
ms:contentKeyID: 49733831
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 137910d71de1d6177356e0b7bacbd6d17022d71d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428297"
---
# <a name="failing-back-the-edge-pool-used-for-lync-server-federation-or-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="68a38-103">Failback do pool de Borda usado para federação do Lync Server ou federação XMPP no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68a38-103">Failing back the Edge pool used for Lync Server federation or XMPP federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="68a38-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="68a38-104">

<span> </span></span></span>

<span data-ttu-id="68a38-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="68a38-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="68a38-106">Depois que um pool de borda com falha que foi usado para hospedar a Federação foi colocado online novamente, use este procedimento para fazer failback do roteiro de Federação do Lync Server e/ou da rota de Federação do XMPP novamente para usar este pool de bordas restaurado.</span><span class="sxs-lookup"><span data-stu-id="68a38-106">After a failed Edge pool that used to host federation has been brought back online, use this procedure to fail back the Lync Server federation route and/or the XMPP federation route to again use this restored Edge pool.</span></span>

<div>

## <a name="failing-back-federation-to-a-restored-edge-pool"></a><span data-ttu-id="68a38-107">Falha ao fazer a Federação para um pool de bordas restaurado</span><span class="sxs-lookup"><span data-stu-id="68a38-107">Failing Back Federation to a Restored Edge Pool</span></span>

1.  <span data-ttu-id="68a38-108">No pool de bordas que agora está disponível novamente, inicie os serviços de borda.</span><span class="sxs-lookup"><span data-stu-id="68a38-108">On the Edge pool that is now available again, start the Edge Services.</span></span>

2.  <span data-ttu-id="68a38-109">Se você quiser fazer failback da rota de Federação do Lync Server para usar o servidor de borda restaurado, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="68a38-109">If you want to fail back the Lync Server federation route to use the restored Edge Server, do the following:</span></span>
    
      - <span data-ttu-id="68a38-110">Em um servidor front-end, abra o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="68a38-110">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="68a38-111">Expanda **pools de bordas**, clique com o botão direito do mouse no servidor de borda ou no pool do servidor de borda que está atualmente configurado para Federação.</span><span class="sxs-lookup"><span data-stu-id="68a38-111">Expand **Edge pools**, then right click the Edge server or Edge server pool that is currently configured for Federation.</span></span> <span data-ttu-id="68a38-112">Selecione **Editar propriedades**.</span><span class="sxs-lookup"><span data-stu-id="68a38-112">Select **Edit properties**.</span></span>
    
      - <span data-ttu-id="68a38-113">Em **Editar propriedades** em **geral**, desmarque **habilitar Federação para este pool de bordas (porta 5061)**.</span><span class="sxs-lookup"><span data-stu-id="68a38-113">In **Edit Properties** under **General**, clear **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="68a38-114">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="68a38-114">Click **OK**.</span></span>
    
      - <span data-ttu-id="68a38-115">Expanda **pools de bordas** e clique com o botão direito do mouse no servidor de borda original ou no pool do servidor de borda que você deseja usar novamente para a Federação.</span><span class="sxs-lookup"><span data-stu-id="68a38-115">Expand **Edge pools**, then right click the original Edge server or Edge server pool that you again want to use for Federation.</span></span> <span data-ttu-id="68a38-116">Selecione **Editar propriedades**.</span><span class="sxs-lookup"><span data-stu-id="68a38-116">Select **Edit properties**.</span></span>
    
      - <span data-ttu-id="68a38-117">Em **Editar propriedades** em **geral**, selecione **habilitar Federação para este pool de bordas (porta 5061)**.</span><span class="sxs-lookup"><span data-stu-id="68a38-117">In **Edit Properties** under **General**, select **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="68a38-118">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="68a38-118">Click **OK**.</span></span>
    
      - <span data-ttu-id="68a38-119">Clique em **ação**, selecione **topologia**, selecione **publicar**.</span><span class="sxs-lookup"><span data-stu-id="68a38-119">Click **Action**, select **Topology**, select **Publish**.</span></span> <span data-ttu-id="68a38-120">Quando solicitado em **publicar a topologia**, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="68a38-120">When prompted on **Publish the topology**, click **Next**.</span></span> <span data-ttu-id="68a38-121">Quando a publicação estiver concluída, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="68a38-121">When the Publish is finished, click **Finish**.</span></span>
    
      - <span data-ttu-id="68a38-122">No servidor de borda, abra o assistente de implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="68a38-122">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="68a38-123">Clique em **instalar ou atualizar o Lync Server System** e, em seguida, clique em **Configurar ou remover componentes do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="68a38-123">Click **Install or Update Lync Server System**, then click **Setup or Remove Lync Server Components**.</span></span> <span data-ttu-id="68a38-124">Clique em **executar novamente**.</span><span class="sxs-lookup"><span data-stu-id="68a38-124">Click **Run Again**.</span></span>
    
      - <span data-ttu-id="68a38-125">Em configurar componentes do Lync Server, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="68a38-125">At Setup Lync Server components, click **Next**.</span></span> <span data-ttu-id="68a38-126">A tela Resumo mostrará as ações conforme elas são executadas.</span><span class="sxs-lookup"><span data-stu-id="68a38-126">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="68a38-127">Depois que a implantação for concluída, clique em **Exibir log** para exibir os arquivos de log disponíveis.</span><span class="sxs-lookup"><span data-stu-id="68a38-127">Once the deployment is done, click **View Log** to view available log files.</span></span> <span data-ttu-id="68a38-128">Clique em **concluir** para concluir a implantação.</span><span class="sxs-lookup"><span data-stu-id="68a38-128">Click **Finish** to complete the deployment.</span></span>

3.  <span data-ttu-id="68a38-129">Se você quiser fazer failback na rota de Federação do XMPP para usar o servidor de borda restaurado, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="68a38-129">If you want to fail back the XMPP federation route to use the restored Edge Server, do the following:</span></span>
    
      - <span data-ttu-id="68a38-130">Execute o cmdlet a seguir para redirecionar a rota de Federação do XMPP para o pool de borda que agora hospeda a Federação XMPP (neste exemplo, EdgeServer1):</span><span class="sxs-lookup"><span data-stu-id="68a38-130">Run the following cmdlet to repoint the XMPP federation route to the Edge pool which will now host XMPP federation (in this example, EdgeServer1):</span></span>
        
            Set-CsSite Site1 -XmppExternalFederationRoute EdgeServer1.contoso.com
        
        <span data-ttu-id="68a38-131">Neste exemplo, site1 é o site que contém o pool de borda que agora hospeda a rota de Federação do XMPP, e EdgeServer1.contoso.com é o FQDN de um servidor de borda nesse pool.</span><span class="sxs-lookup"><span data-stu-id="68a38-131">In this example, Site1 is the site containing the Edge pool which will now host the XMPP federation route, and EdgeServer1.contoso.com is the FQDN of an Edge Server in that pool.</span></span>
    
      - <span data-ttu-id="68a38-132">Se você ainda não tiver um registro SRV DNS para a Federação do XMPP, que é resolvido para o pool de borda que agora hospedará a Federação do XMPP, você deve adicioná-lo, como no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="68a38-132">If you do not already have a DNS SRV record for XMPP federation which resolves to the Edge pool which will now host XMPP federation, you must add it, as in the following example.</span></span> <span data-ttu-id="68a38-133">Esse registro SRV deve ter um valor de porta 5269.</span><span class="sxs-lookup"><span data-stu-id="68a38-133">This SRV record must have a port value of 5269.</span></span>
        
            _xmpp-server._tcp.contoso.com
    
      - <span data-ttu-id="68a38-134">No servidor DNS externo, altere o registro DNS a para a Federação XMPP para apontar para EdgeServer2.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="68a38-134">On the external DNS server, change the DNS A record for XMPP federation to point to EdgeServer2.contoso.com.</span></span>
    
      - <span data-ttu-id="68a38-135">Verifique se o pool de bordas que agora hospeda a Federação do XMPP tem a porta 5269 aberta externamente.</span><span class="sxs-lookup"><span data-stu-id="68a38-135">Verify that the Edge pool which will now host XMPP federation has port 5269 open externally.</span></span>

4.  <span data-ttu-id="68a38-136">Se os pools de front-end permanecerem sendo executados no site que contém o pool de borda que falhou e foi restaurado, você deverá atualizar o serviço de Webconferência e o serviço de conferência A/V nesses pools de front-ends para usar novamente os pools de borda em seu site local.</span><span class="sxs-lookup"><span data-stu-id="68a38-136">If the Front End pools remained running in the site containing the Edge pool that failed and has been restored, you should update the Web Conferencing Service and A/V Conferencing Service on these Front End pools to again use the Edge pools at their local site.</span></span> <span data-ttu-id="68a38-137">Para obter mais informações, consulte [alterando o pool de bordas associado a um pool de front-end no Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span><span class="sxs-lookup"><span data-stu-id="68a38-137">For more information, see [Changing the Edge pool associated with a Front End pool in Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span></span>

5.  <span data-ttu-id="68a38-138">Se o pool de front-ends no mesmo site do pool de borda com falha também falhar, agora você pode usar Invoke – CsPoolFailback para fazer failback do pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="68a38-138">If the Front End pool at the same site as the failed Edge pool also failed, you can now use Invoke–CsPoolFailback to fail back the Front End pool.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="68a38-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="68a38-139">See Also</span></span>


[<span data-ttu-id="68a38-140">Failover do pool de Borda usado para federação do Servidor Lync no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68a38-140">Failing over the Edge pool used for Lync Server federation in Lync Server 2013</span></span>](lync-server-2013-failing-over-the-edge-pool-used-for-lync-server-federation.md)  
[<span data-ttu-id="68a38-141">Failover do pool de Borda usado para federação de XMPP no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68a38-141">Failing over the Edge pool used for XMPP federation in Lync Server 2013</span></span>](lync-server-2013-failing-over-the-edge-pool-used-for-xmpp-federation.md)  


[<span data-ttu-id="68a38-142">Recuperação de desastres do servidor de borda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68a38-142">Edge Server disaster recovery in Lync Server 2013</span></span>](lync-server-2013-edge-server-disaster-recovery.md)  
  

<span data-ttu-id="68a38-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="68a38-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

