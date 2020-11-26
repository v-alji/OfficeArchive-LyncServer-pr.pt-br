---
title: Lync Server 2013; Criar rotas interregions de rede
description: Lync Server 2013; Crie rotas interregions de rede.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: admin
manager: serdars
f1.keywords:
- NOCSH
TOCTitle: Create network interregion routes
ms:assetid: 5555262a-a502-4b01-9593-836dd30064f5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398368(v=OCS.15)
ms:contentKeyID: 48184159
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: 44c8c62a86f7cfb6ca5b1148dc097c1d7786ad29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446160"
---
# <a name="create-network-interregion-routes-in-lync-server-2013"></a><span data-ttu-id="2b32c-103">Criar rotas de interregião de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b32c-103">Create network interregion routes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b32c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b32c-104">

<span> </span></span></span>

<span data-ttu-id="2b32c-105">_**Tópico da última modificação:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="2b32c-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="2b32c-106">Uma *rota interregião de rede* define a rota entre um par de regiões de rede.</span><span class="sxs-lookup"><span data-stu-id="2b32c-106">A *network interregion route* defines the route between a pair of network regions.</span></span> <span data-ttu-id="2b32c-107">Cada par de regiões de rede em sua implantação de controle de admissão de chamadas requer uma rota interregion de rede.</span><span class="sxs-lookup"><span data-stu-id="2b32c-107">Each pair of network regions in your call admission control deployment requires a network interregion route.</span></span> <span data-ttu-id="2b32c-108">Isso permite que cada região da rede dentro da implantação acesse todas as demais regiões.</span><span class="sxs-lookup"><span data-stu-id="2b32c-108">This enables every network region within the deployment to access every other region.</span></span>

<span data-ttu-id="2b32c-109">Embora os links de região definam as limitações de largura de banda nas conexões entre regiões, uma rota entre regiões determina qual caminho vinculado a conexão passará de uma região para outra.</span><span class="sxs-lookup"><span data-stu-id="2b32c-109">While region links set bandwidth limitations on the connections between regions, an interregion route determines which linked path the connection will traverse from one region to another.</span></span>

<span data-ttu-id="2b32c-110">Para obter detalhes sobre como trabalhar com rotas de interregião de rede, consulte a documentação do Shell de gerenciamento do Lync Server para os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2b32c-110">For details about working with network interregion routes, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="2b32c-111">New-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="2b32c-111">New-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterRegionRoute)

  - [<span data-ttu-id="2b32c-112">Get-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="2b32c-112">Get-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterRegionRoute)

  - [<span data-ttu-id="2b32c-113">Set-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="2b32c-113">Set-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterRegionRoute)

  - [<span data-ttu-id="2b32c-114">Remove-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="2b32c-114">Remove-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterRegionRoute)

<span data-ttu-id="2b32c-115">Na topologia de exemplo, as rotas interregion de rede devem ser definidas para cada um dos três pares de regiões: América do Norte/EMEA, EMEA/Ásia e América do Norte/Ásia-Pacífico.</span><span class="sxs-lookup"><span data-stu-id="2b32c-115">In the example topology, network interregion routes must be defined for each of the three region pairs: North America/EMEA, EMEA/APAC, and North America/APAC.</span></span>

<div>

## <a name="to-create-network-interregion-routes-by-using-lync-server-management-shell"></a><span data-ttu-id="2b32c-116">Para criar rotas de interregião de rede usando o Shell de gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="2b32c-116">To create network interregion routes by using Lync Server Management Shell</span></span>

1.  <span data-ttu-id="2b32c-117">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="2b32c-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="2b32c-118">Execute o cmdlet **New-CsNetworkInterRegionRoute** para definir as rotas necessárias.</span><span class="sxs-lookup"><span data-stu-id="2b32c-118">Run the **New-CsNetworkInterRegionRoute** cmdlet to define the required routes.</span></span> <span data-ttu-id="2b32c-119">Por exemplo, execute:</span><span class="sxs-lookup"><span data-stu-id="2b32c-119">For example, run:</span></span>
    
       ```PowerShell
        New-CsNetworkInterRegionRoute -Identity NorthAmerica_EMEA_Route -NetworkRegionID1 NorthAmerica -NetworkRegionID2 EMEA -NetworkRegionLinkIDs "NA-EMEA-LINK"
       ```
    
       ```PowerShell
        New-CsNetworkInterRegionRoute -Identity NorthAmerica_APAC_Route -NetworkRegionID1 NorthAmerica -NetworkRegionID2 APAC -NetworkRegionLinkIDs "NA-EMEA-LINK, EMEA-APAC-LINK"
       ```
    
       ```PowerShell
        New-CsNetworkInterRegionRoute -Identity EMEA_APAC_Route -NetworkRegionID1 EMEA -NetworkRegionID2 APAC -NetworkRegionLinkIDs "EMEA-APAC-LINK"
       ```
    
    <div class=" ">
    

    > [!NOTE]  
    > <span data-ttu-id="2b32c-120">A rota interregião da rede América do Norte/Ásia requer dois links de região de rede porque não há um link de região de rede direto entre eles.</span><span class="sxs-lookup"><span data-stu-id="2b32c-120">The North America/APAC network interregion route requires two network region links because there is no direct network region link between them.</span></span>

    
    </div>

</div>

<div>

## <a name="to-create-network-interregion-routes-by-using-lync-server-control-panel"></a><span data-ttu-id="2b32c-121">Para criar rotas de interregião de rede usando o painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="2b32c-121">To create network interregion routes by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="2b32c-122">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2b32c-122">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="2b32c-123">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2b32c-123">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="2b32c-124">Na barra de navegação esquerda, clique em **Configuração de rede**.</span><span class="sxs-lookup"><span data-stu-id="2b32c-124">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="2b32c-125">Clique no botão de navegações **Rota de Região**.</span><span class="sxs-lookup"><span data-stu-id="2b32c-125">Click the **Region Route** navigation button.</span></span>

4.  <span data-ttu-id="2b32c-126">Clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="2b32c-126">Click **New**.</span></span>

5.  <span data-ttu-id="2b32c-127">Na página **nova rota de região** , clique em **nome** e digite um nome para a rota interregião de rede.</span><span class="sxs-lookup"><span data-stu-id="2b32c-127">On the **New Region Route** page, click **Name** and then type a name for the network interregion route.</span></span>

6.  <span data-ttu-id="2b32c-128">Clique na **região de rede \# 1** e, em seguida, clique em uma região de rede na lista que você deseja direcionar para a região de rede \# 2.</span><span class="sxs-lookup"><span data-stu-id="2b32c-128">Click **Network Region \#1**, and then click a network region in the list that you want to route to Network Region \#2.</span></span>

7.  <span data-ttu-id="2b32c-129">Clique em **rede \# 2** e, em seguida, clique em uma região de rede na lista que você deseja direcionar para a região de rede \# 1.</span><span class="sxs-lookup"><span data-stu-id="2b32c-129">Click **Network Region \#2**, and then click a network region in the list that you want to route to Network Region \#1.</span></span>

8.  <span data-ttu-id="2b32c-130">Clique em **Adicionar** ao lado do campo de **links de região de rede** e, em seguida, adicione um link de região de rede que será usado na rota interregião de rede.</span><span class="sxs-lookup"><span data-stu-id="2b32c-130">Click **Add** beside the **Network Region Links** field, and then add a network region link that will be used in the network interregion route.</span></span>
    
    <div class=" ">
    

    > [!NOTE]  
    > <span data-ttu-id="2b32c-131">Se você estiver criando uma rota para duas regiões de rede que não têm um link de região de rede direta de rede entre elas, deverá adicionar todos os links necessários para concluir a rota.</span><span class="sxs-lookup"><span data-stu-id="2b32c-131">If you are creating a route for two network regions that do not have a direct network region link between them, you must add all the necessary links to complete the route.</span></span> <span data-ttu-id="2b32c-132">Por exemplo, a rota de interregião da rede América do Norte/Ásia requer dois links de região de rede porque não há um link de região de rede direto entre eles.</span><span class="sxs-lookup"><span data-stu-id="2b32c-132">For example, the North America/APAC network interregion route requires two network region links because there is no direct network region link between them.</span></span>

    
    </div>

9.  <span data-ttu-id="2b32c-133">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="2b32c-133">Click **Commit**.</span></span>

10. <span data-ttu-id="2b32c-134">Para concluir a criação de rotas interregions de rede para a sua topologia, repita as etapas de 4 a 9 com configurações para outras rotas interregions de rede.</span><span class="sxs-lookup"><span data-stu-id="2b32c-134">To finish creating network interregion routes for your topology, repeat steps 4 through 9 with settings for other network interregion routes.</span></span>

<span data-ttu-id="2b32c-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b32c-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

