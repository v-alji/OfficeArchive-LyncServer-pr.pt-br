---
title: 'Lync Server 2013: Criando ou modificando rotas de região de rede'
description: 'Lync Server 2013: Criando ou modificando rotas de região de rede.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating or modifying network region routes
ms:assetid: 76993daa-76c2-4cec-8363-de8aebef0145
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521016(v=OCS.15)
ms:contentKeyID: 48184540
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 89106c905419778776ea16341f247027d49f1195
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431425"
---
# <a name="creating-or-modifying-network-region-routes-in-lync-server-2013"></a><span data-ttu-id="0cf10-103">Criando ou modificando rotas de região de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0cf10-103">Creating or modifying network region routes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0cf10-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0cf10-104">

<span> </span></span></span>

<span data-ttu-id="0cf10-105">_**Tópico da última modificação:** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="0cf10-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="0cf10-106">Todas as regiões em uma configuração de controle de admissão de chamadas (CAC) devem ter alguma maneira de acessar todas as outras regiões.</span><span class="sxs-lookup"><span data-stu-id="0cf10-106">Every region within a call admission control (CAC) configuration must have some way to access every other region.</span></span> <span data-ttu-id="0cf10-107">Enquanto links de região definem as limitações de largura de banda nas conexões entre regiões e também representam os links físicos, uma rota determina qual caminho vinculado a conexão passará de uma região para outra.</span><span class="sxs-lookup"><span data-stu-id="0cf10-107">While region links set bandwidth limitations on the connections between regions and also represent the physical links, a route determines which linked path the connection will traverse from one region to another.</span></span> <span data-ttu-id="0cf10-108">Você pode usar o painel de controle do Lync Server para configurar rotas de região de rede.</span><span class="sxs-lookup"><span data-stu-id="0cf10-108">You can use Lync Server Control Panel to configure network region routes.</span></span> <span data-ttu-id="0cf10-109">No painel de controle do Lync Server, você pode criar, modificar ou excluir uma rota de região de rede.</span><span class="sxs-lookup"><span data-stu-id="0cf10-109">From Lync Server Control Panel, you can create, modify, or delete a network region route.</span></span> <span data-ttu-id="0cf10-110">Use este tópico para criar ou modificar uma rota de região de rede.</span><span class="sxs-lookup"><span data-stu-id="0cf10-110">Use this topic to create or modify a network region route.</span></span> <span data-ttu-id="0cf10-111">Para obter detalhes sobre como excluir um roteiro de região de rede existente, consulte [excluindo rotas de região de rede existentes no Lync Server 2013](lync-server-2013-deleting-existing-network-region-routes.md).</span><span class="sxs-lookup"><span data-stu-id="0cf10-111">For details about deleting an existing network region routes, see [Deleting existing network region routes in Lync Server 2013](lync-server-2013-deleting-existing-network-region-routes.md).</span></span>

<div>

## <a name="to-create-a-network-region-route"></a><span data-ttu-id="0cf10-112">Para criar uma rota de região de rede</span><span class="sxs-lookup"><span data-stu-id="0cf10-112">To create a network region route</span></span>

1.  <span data-ttu-id="0cf10-113">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="0cf10-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="0cf10-114">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0cf10-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="0cf10-115">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0cf10-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="0cf10-116">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **rota de região**.</span><span class="sxs-lookup"><span data-stu-id="0cf10-116">In the left navigation bar, click **Network Configuration** and then click **Region Route**.</span></span>

4.  <span data-ttu-id="0cf10-117">Na página **rota de região** , clique em **novo**.</span><span class="sxs-lookup"><span data-stu-id="0cf10-117">On the **Region Route** page, click **New**.</span></span>

5.  <span data-ttu-id="0cf10-118">Em **nova rota de região**, digite um valor no campo **nome** .</span><span class="sxs-lookup"><span data-stu-id="0cf10-118">In **New Region Route**, type a value in the **Name** field.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0cf10-119">Esse valor deve ser exclusivo na implantação do Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0cf10-119">This value must be unique within your Microsoft Lync Server 2013 deployment.</span></span>

    
    </div>

6.  <span data-ttu-id="0cf10-120">Na lista suspensa **região de rede \# 1** , selecione uma das duas regiões a serem conectadas por essa rota.</span><span class="sxs-lookup"><span data-stu-id="0cf10-120">From the **Network region \#1** drop-down list, select one of the two regions to be connected by this route.</span></span>

7.  <span data-ttu-id="0cf10-121">Na lista suspensa **região de rede \# 2** , selecione a outra região para esta rota.</span><span class="sxs-lookup"><span data-stu-id="0cf10-121">From the **Network region \#2** drop-down list, select the other region for this route.</span></span> <span data-ttu-id="0cf10-122">Esta região deve ser diferente da região selecionada para a região de rede \# 1.</span><span class="sxs-lookup"><span data-stu-id="0cf10-122">This region must be different from the region selected for Network region \#1.</span></span>

8.  <span data-ttu-id="0cf10-123">Use a caixa de listagem de **links de região de rede** para adicionar links de região ao roteiro.</span><span class="sxs-lookup"><span data-stu-id="0cf10-123">Use the **Network region links** list box to add region links to the route.</span></span> <span data-ttu-id="0cf10-124">Clique no botão **Adicionar** para exibir a página de **link de região** .</span><span class="sxs-lookup"><span data-stu-id="0cf10-124">Click the **Add** button to display the **Region Link** page.</span></span> <span data-ttu-id="0cf10-125">Clique em um link de região para adicionar a essa rota e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="0cf10-125">Click a region link to add to this route, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0cf10-126">Continue a clicar no botão <STRONG>Adicionar</STRONG> para adicionar mais links ou selecionar um link e clicar em <STRONG>remover</STRONG> para remover um link.</span><span class="sxs-lookup"><span data-stu-id="0cf10-126">Continue to click the <STRONG>Add</STRONG> button to add more links, or select a link and click <STRONG>Remove</STRONG> to remove a link.</span></span>

    
    </div>

9.  <span data-ttu-id="0cf10-127">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="0cf10-127">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-network-region-route"></a><span data-ttu-id="0cf10-128">Para modificar uma rota de região de rede</span><span class="sxs-lookup"><span data-stu-id="0cf10-128">To modify a network region route</span></span>

1.  <span data-ttu-id="0cf10-129">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="0cf10-129">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="0cf10-130">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0cf10-130">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="0cf10-131">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0cf10-131">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="0cf10-132">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **rota de região**.</span><span class="sxs-lookup"><span data-stu-id="0cf10-132">In the left navigation bar, click **Network Configuration** and then click **Region Route**.</span></span>

4.  <span data-ttu-id="0cf10-133">Na página **rota de região** , clique na rota de região que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="0cf10-133">On the **Region Route** page, click the region route that you want to modify.</span></span>

5.  <span data-ttu-id="0cf10-134">No menu **Editar**, clique em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="0cf10-134">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="0cf10-135">Em **Editar rota de região**, você pode modificar as regiões Unidas por essa rota e os links de região associados à rota.</span><span class="sxs-lookup"><span data-stu-id="0cf10-135">In **Edit Region Route**, you can modify the regions joined by this route and the region links associated with the route.</span></span>

7.  <span data-ttu-id="0cf10-136">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="0cf10-136">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0cf10-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cf10-137">See Also</span></span>


[<span data-ttu-id="0cf10-138">Excluindo rotas de região de rede existentes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0cf10-138">Deleting existing network region routes in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-region-routes.md)  
  

<span data-ttu-id="0cf10-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0cf10-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

