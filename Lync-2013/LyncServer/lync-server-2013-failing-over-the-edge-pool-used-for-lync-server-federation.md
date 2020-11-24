---
title: 'Lync Server 2013: Failover do pool de Borda usado para federação do Servidor Lync'
description: 'Lync Server 2013: falha sobre o pool de bordas usado para Federação do Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over the Edge pool used for Lync Server federation
ms:assetid: 5c9da0f2-7429-40bb-bb3c-5cc4ecb5a13d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688071(v=OCS.15)
ms:contentKeyID: 49733665
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1e7e13ccd35a653d38174f55ace9dc6637ded04
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389879"
---
# <a name="failing-over-the-edge-pool-used-for-lync-server-federation-in-lync-server-2013"></a><span data-ttu-id="730b0-103">Failover do pool de Borda usado para federação do Servidor Lync no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="730b0-103">Failing over the Edge pool used for Lync Server federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="730b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="730b0-104">

<span> </span></span></span>

<span data-ttu-id="730b0-105">_**Tópico da última modificação:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="730b0-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="730b0-106">Se o pool de bordas em que você tem a Federação do Lync Server configurada ficar inativo, você deverá alterar a Federação para usar um pool de bordas diferente para o trabalho de Federação.</span><span class="sxs-lookup"><span data-stu-id="730b0-106">If the Edge pool where you have Lync Server federation configured goes down, you must change federation to use a different Edge pool for federation to work.</span></span>

<div>

## <a name="failing-over-the-edge-pool-used-for-lync-server-federation"></a><span data-ttu-id="730b0-107">Falha sobre o pool de bordas usado para a Federação do Lync Server</span><span class="sxs-lookup"><span data-stu-id="730b0-107">Failing Over the Edge Pool Used for Lync Server Federation</span></span>

1.  <span data-ttu-id="730b0-108">Em um servidor front-end, abra o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="730b0-108">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="730b0-109">Expanda **pools de bordas**, clique com o botão direito do mouse no servidor de borda ou no pool do servidor de borda que está atualmente configurado para Federação.</span><span class="sxs-lookup"><span data-stu-id="730b0-109">Expand **Edge pools**, then right click the Edge server or Edge server pool that is currently configured for Federation.</span></span> <span data-ttu-id="730b0-110">Selecione **Editar propriedades**.</span><span class="sxs-lookup"><span data-stu-id="730b0-110">Select **Edit properties**.</span></span>

2.  <span data-ttu-id="730b0-111">Em **Editar propriedades** em **geral**, desmarque **habilitar Federação para este pool de bordas (porta 5061)**.</span><span class="sxs-lookup"><span data-stu-id="730b0-111">In **Edit Properties** under **General**, clear **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="730b0-112">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="730b0-112">Click **OK**.</span></span>

3.  <span data-ttu-id="730b0-113">Expanda **pools de bordas** e clique com o botão direito do mouse no servidor de borda ou no pool do servidor de borda que você agora deseja usar para a Federação.</span><span class="sxs-lookup"><span data-stu-id="730b0-113">Expand **Edge pools**, then right click the Edge server or Edge server pool that you now want to use for Federation.</span></span> <span data-ttu-id="730b0-114">Selecione **Editar propriedades**.</span><span class="sxs-lookup"><span data-stu-id="730b0-114">Select **Edit properties**.</span></span>

4.  <span data-ttu-id="730b0-115">Em **Editar propriedades** em **geral**, selecione **habilitar Federação para este pool de bordas (porta 5061)**.</span><span class="sxs-lookup"><span data-stu-id="730b0-115">In **Edit Properties** under **General**, select **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="730b0-116">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="730b0-116">Click **OK**.</span></span>

5.  <span data-ttu-id="730b0-117">Clique em **ação**, selecione **topologia**, selecione **publicar**.</span><span class="sxs-lookup"><span data-stu-id="730b0-117">Click **Action**, select **Topology**, select **Publish**.</span></span> <span data-ttu-id="730b0-118">Quando solicitado em **publicar a topologia**, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="730b0-118">When prompted on **Publish the topology**, click **Next**.</span></span> <span data-ttu-id="730b0-119">Quando a publicação estiver concluída, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="730b0-119">When the Publish is finished, click **Finish**.</span></span>

6.  <span data-ttu-id="730b0-120">No servidor de borda, abra o assistente de implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="730b0-120">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="730b0-121">Clique em **instalar ou atualizar o Lync Server System** e, em seguida, clique em **Configurar ou remover componentes do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="730b0-121">Click **Install or Update Lync Server System**, then click **Setup or Remove Lync Server Components**.</span></span> <span data-ttu-id="730b0-122">Clique em **executar novamente**.</span><span class="sxs-lookup"><span data-stu-id="730b0-122">Click **Run Again**.</span></span>

7.  <span data-ttu-id="730b0-123">Em configurar componentes do Lync Server, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="730b0-123">At Setup Lync Server components, click **Next**.</span></span> <span data-ttu-id="730b0-124">A tela Resumo mostrará as ações conforme elas são executadas.</span><span class="sxs-lookup"><span data-stu-id="730b0-124">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="730b0-125">Depois que a implantação for concluída, clique em **Exibir log** para exibir os arquivos de log disponíveis.</span><span class="sxs-lookup"><span data-stu-id="730b0-125">Once the deployment is done, click **View Log** to view available log files.</span></span> <span data-ttu-id="730b0-126">Clique em **concluir** para concluir a implantação.</span><span class="sxs-lookup"><span data-stu-id="730b0-126">Click **Finish** to complete the deployment.</span></span>
    
    <span data-ttu-id="730b0-127">Se o site que contém o pool de bordas com falha contiver servidores front-end que ainda estão em execução, você deve atualizar o serviço de Webconferência e o serviço de conferência A/V nesses pools de front-ends para usar um pool de bordas em um site remoto que ainda esteja em execução.</span><span class="sxs-lookup"><span data-stu-id="730b0-127">If the site containing the failed Edge pool contains Front End Servers that are still running, you must update the Web Conferencing Service and A/V Conferencing Service on these Front End pools to use an Edge pool in a remote site that is still running.</span></span> <span data-ttu-id="730b0-128">Para obter mais informações, consulte [alterando o pool de bordas associado a um pool de front-end no Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span><span class="sxs-lookup"><span data-stu-id="730b0-128">For more information, see [Changing the Edge pool associated with a Front End pool in Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="730b0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="730b0-129">See Also</span></span>


[<span data-ttu-id="730b0-130">Failover do pool de Borda usado para federação de XMPP no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="730b0-130">Failing over the Edge pool used for XMPP federation in Lync Server 2013</span></span>](lync-server-2013-failing-over-the-edge-pool-used-for-xmpp-federation.md)  
[<span data-ttu-id="730b0-131">Failback do pool de Borda usado para federação do Lync Server ou federação XMPP no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="730b0-131">Failing back the Edge pool used for Lync Server federation or XMPP federation in Lync Server 2013</span></span>](lync-server-2013-failing-back-the-edge-pool-used-for-lync-server-federation-or-xmpp-federation.md)  


[<span data-ttu-id="730b0-132">Recuperação de desastres do servidor de borda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="730b0-132">Edge Server disaster recovery in Lync Server 2013</span></span>](lync-server-2013-edge-server-disaster-recovery.md)  
  

<span data-ttu-id="730b0-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="730b0-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

