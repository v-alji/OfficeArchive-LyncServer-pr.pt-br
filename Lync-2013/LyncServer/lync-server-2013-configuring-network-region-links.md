---
title: 'Lync Server 2013: Configurando links de região de rede'
description: 'Lync Server 2013: Configurando links de região de rede.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring network region links
ms:assetid: 952bc93e-e6aa-4539-85c7-2b15f14eb382
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182551(v=OCS.15)
ms:contentKeyID: 48184829
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b92593f3b8fcd5fe3307a9c193ed7cddcf6dfce0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432923"
---
# <a name="configuring-network-region-links-in-lync-server-2013"></a><span data-ttu-id="06152-103">Configurar links de região de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06152-103">Configuring network region links in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06152-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06152-104">

<span> </span></span></span>

<span data-ttu-id="06152-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="06152-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="06152-106">Você pode configurar links entre duas regiões de rede como parte do controle de admissão de chamadas (CAC).</span><span class="sxs-lookup"><span data-stu-id="06152-106">You can configure links between two network regions as part of call admission control (CAC).</span></span> <span data-ttu-id="06152-107">Regiões dentro de uma rede são vinculadas por meio de conectividade física de rede de longa distância (WAN).</span><span class="sxs-lookup"><span data-stu-id="06152-107">Regions within a network are linked through physical wide area network (WAN) connectivity.</span></span> <span data-ttu-id="06152-108">Você pode usar o painel de controle do Lync Server para definir um link entre duas regiões de rede e definir as limitações de largura de banda em conexões de áudio e vídeo entre essas regiões.</span><span class="sxs-lookup"><span data-stu-id="06152-108">You can use the Lync Server Control Panel to define a link between two network regions and set the bandwidth limitations on audio and video connections between these regions.</span></span> <span data-ttu-id="06152-109">Para obter detalhes sobre como excluir um link de região de rede existente, consulte [excluindo links de região de rede no Lync Server 2013](lync-server-2013-deleting-network-region-links.md).</span><span class="sxs-lookup"><span data-stu-id="06152-109">For details about deleting an existing network region link, see [Deleting network region links in Lync Server 2013](lync-server-2013-deleting-network-region-links.md).</span></span>

<div>

## <a name="to-create-a-network-region-link"></a><span data-ttu-id="06152-110">Para criar um link de região de rede</span><span class="sxs-lookup"><span data-stu-id="06152-110">To create a network region link</span></span>

1.  <span data-ttu-id="06152-111">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="06152-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="06152-112">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="06152-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="06152-113">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="06152-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="06152-114">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **link de região**.</span><span class="sxs-lookup"><span data-stu-id="06152-114">In the left navigation bar, click **Network Configuration** and then click **Region Link**.</span></span>

4.  <span data-ttu-id="06152-115">Na página **link de região** , clique em **novo**.</span><span class="sxs-lookup"><span data-stu-id="06152-115">On the **Region Link** page, click **New**.</span></span>

5.  <span data-ttu-id="06152-116">Em **novo link de região**, digite um valor no campo **nome** .</span><span class="sxs-lookup"><span data-stu-id="06152-116">In **New Region Link**, type a value in the **Name** field.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="06152-117">Esse valor deve ser exclusivo na implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="06152-117">This value must be unique within your Lync Server 2013 deployment.</span></span>

    
    </div>

6.  <span data-ttu-id="06152-118">Na lista suspensa **região de rede \# 1** , selecione uma das duas regiões a ser vinculada.</span><span class="sxs-lookup"><span data-stu-id="06152-118">From the **Network region \#1** drop-down list, select one of the two regions to be linked.</span></span>

7.  <span data-ttu-id="06152-119">Na lista suspensa **região de rede \# 2** , selecione a outra região a ser vinculada.</span><span class="sxs-lookup"><span data-stu-id="06152-119">From the **Network region \#2** drop-down list, select the other region to be linked.</span></span> <span data-ttu-id="06152-120">Esta região deve ser diferente da região selecionada para a região de rede \# 1.</span><span class="sxs-lookup"><span data-stu-id="06152-120">This region must be different from the region selected for Network region \#1.</span></span>

8.  <span data-ttu-id="06152-121">Adicionais Se você quiser colocar as limitações de largura de banda em chamadas de áudio ou de vídeo entre essas regiões, selecione um perfil de política de largura de banda na lista suspensa **política de largura de banda** .</span><span class="sxs-lookup"><span data-stu-id="06152-121">(Optional) If you want to place bandwidth limitations on audio or video calls between these regions, select a bandwidth policy profile from the **Bandwidth policy** drop-down list.</span></span>

9.  <span data-ttu-id="06152-122">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="06152-122">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-network-region-link"></a><span data-ttu-id="06152-123">Para modificar um link de região de rede</span><span class="sxs-lookup"><span data-stu-id="06152-123">To modify a network region link</span></span>

1.  <span data-ttu-id="06152-124">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="06152-124">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="06152-125">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="06152-125">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="06152-126">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="06152-126">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="06152-127">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **link de região**.</span><span class="sxs-lookup"><span data-stu-id="06152-127">In the left navigation bar, click **Network Configuration** and then click **Region Link**.</span></span>

4.  <span data-ttu-id="06152-128">Na página **link de região** , clique no link de região que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="06152-128">On the **Region Link** page, click the region link that you want to modify.</span></span>

5.  <span data-ttu-id="06152-129">No menu **Editar**, clique em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="06152-129">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="06152-130">No **link para editar região**, você pode modificar as regiões vinculadas ou o perfil de política de largura de banda para esse link.</span><span class="sxs-lookup"><span data-stu-id="06152-130">In **Edit Region Link**, you can modify the regions that are linked or the bandwidth policy profile for this link.</span></span>

7.  <span data-ttu-id="06152-131">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="06152-131">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="06152-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="06152-132">See Also</span></span>


[<span data-ttu-id="06152-133">Excluindo links de região de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06152-133">Deleting network region links in Lync Server 2013</span></span>](lync-server-2013-deleting-network-region-links.md)  


[<span data-ttu-id="06152-134">New-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="06152-134">New-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegionLink)  
[<span data-ttu-id="06152-135">Set-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="06152-135">Set-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkRegionLink)  
[<span data-ttu-id="06152-136">Remove-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="06152-136">Remove-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkRegionLink)  
[<span data-ttu-id="06152-137">Get-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="06152-137">Get-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink)  
  

<span data-ttu-id="06152-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06152-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
