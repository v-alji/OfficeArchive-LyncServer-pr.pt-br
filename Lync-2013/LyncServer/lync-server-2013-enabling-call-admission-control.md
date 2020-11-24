---
title: 'Lync Server 2013: Habilitando o controle de admissão de chamadas'
description: 'Lync Server 2013: Habilitando o controle de admissão de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling call admission control
ms:assetid: 015f5c8f-2f90-4b9e-8149-b33767e90582
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520942(v=OCS.15)
ms:contentKeyID: 48183228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b2f5737f83a1965b920f2a23e1aabbbaec2af7b3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390154"
---
# <a name="enabling-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="aecdf-103">Habilitando o controle de admissão de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aecdf-103">Enabling call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aecdf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aecdf-104">

<span> </span></span></span>

<span data-ttu-id="aecdf-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="aecdf-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="aecdf-106">O serviço de controle de admissão de chamadas (CAC) é uma rede de regiões, sites e sub-redes que permite impor restrições às transmissões de áudio e vídeo com base na largura de banda disponível.</span><span class="sxs-lookup"><span data-stu-id="aecdf-106">Call admission control (CAC) is a network of regions, sites, and subnets that enable you to place restrictions on audio and video transmissions based on available bandwidth.</span></span> <span data-ttu-id="aecdf-107">Depois de configurar a rede do CAC, você deve habilitar o CAC para impor as limitações de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="aecdf-107">After you configure the CAC network, you must enable CAC to enforce the bandwidth limitations.</span></span> <span data-ttu-id="aecdf-108">Você pode usar o painel de controle do Lync Server para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="aecdf-108">You can use Lync Server Control Panel to do this.</span></span>

<div>

## <a name="to-enable-cac-from-lync-server-control-panel"></a><span data-ttu-id="aecdf-109">Para habilitar o CAC do painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="aecdf-109">To enable CAC from Lync Server Control Panel</span></span>

1.  <span data-ttu-id="aecdf-110">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="aecdf-110">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="aecdf-111">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="aecdf-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="aecdf-112">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="aecdf-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="aecdf-113">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **global**.</span><span class="sxs-lookup"><span data-stu-id="aecdf-113">In the left navigation bar, click **Network Configuration** and then click **Global**.</span></span>

4.  <span data-ttu-id="aecdf-114">Na página **global** , clique em configuração **global** .</span><span class="sxs-lookup"><span data-stu-id="aecdf-114">On the **Global** page, click the **Global** configuration.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="aecdf-115">Somente uma rede pode ser configurada para qualquer implantação do Microsoft Lync Server 2013, portanto, nunca haverá mais de uma configuração de rede na lista.</span><span class="sxs-lookup"><span data-stu-id="aecdf-115">Only one network can be configured for any Microsoft Lync Server 2013 deployment, so there will never be more than one network configuration in the list.</span></span> <span data-ttu-id="aecdf-116">Não é possível renomear a configuração global.</span><span class="sxs-lookup"><span data-stu-id="aecdf-116">You cannot rename the Global configuration.</span></span>

    
    </div>

5.  <span data-ttu-id="aecdf-117">No menu **Editar**, clique em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="aecdf-117">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="aecdf-118">Na página **Editar configuração global** , marque a caixa de seleção **habilitar controle de admissão de chamadas** e clique em **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="aecdf-118">On the **Edit Global Setting** page, select the **Enable call admission control** check box, and then click **Commit**.</span></span>

<span data-ttu-id="aecdf-119">Quando você clica em **confirmar**, executa um teste de configuração.</span><span class="sxs-lookup"><span data-stu-id="aecdf-119">When you click **Commit**, you run a test of the configuration.</span></span> <span data-ttu-id="aecdf-120">A caixa de diálogo **Editar configurações globais** é fechada, retornando você à página **global** .</span><span class="sxs-lookup"><span data-stu-id="aecdf-120">The **Edit Global Settings** dialog box closes, returning you to the **Global** page.</span></span> <span data-ttu-id="aecdf-121">Você receberá um aviso se quaisquer erros ou inconsistências forem descobertos em sua configuração de rede que o impedirá de funcionar corretamente (por exemplo, se cada região não estiver conectada a todas as outras regiões por meio de uma rota entre regiões).</span><span class="sxs-lookup"><span data-stu-id="aecdf-121">You will receive a warning if any errors or inconsistencies are discovered in your network configuration that will prevent it from working correctly (for example, if every region is not connected to every other region through an interregion route).</span></span>

<span data-ttu-id="aecdf-122">Se você fizer alterações em sua configuração de rede, poderá executar a verificação de validação novamente abrindo a configuração global e clicando em **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="aecdf-122">If you make changes to your network configuration, you can run the validation check again by opening the Global configuration and clicking **Commit**.</span></span> <span data-ttu-id="aecdf-123">Você não precisa desabilitar o CAC primeiro: Deixe a caixa de seleção marcada e clique em **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="aecdf-123">You do not need to disable CAC first: leave the check box checked and click **Commit**.</span></span> <span data-ttu-id="aecdf-124">Você pode fazer isso a qualquer momento sem fazer alterações de configuração.</span><span class="sxs-lookup"><span data-stu-id="aecdf-124">You can do this at any time without making any configuration changes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="aecdf-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="aecdf-125">See Also</span></span>


[<span data-ttu-id="aecdf-126">Visão geral do controle de admissão de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aecdf-126">Overview of call admission control in Lync Server 2013</span></span>](lync-server-2013-overview-of-call-admission-control.md)  


[<span data-ttu-id="aecdf-127">Planejamento para controle de admissão de chamada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aecdf-127">Planning for call admission control in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-admission-control.md)  
[<span data-ttu-id="aecdf-128">Configurar o controle de admissão de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aecdf-128">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)  
[<span data-ttu-id="aecdf-129">Get-CsNetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="aecdf-129">Get-CsNetworkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkConfiguration)  
[<span data-ttu-id="aecdf-130">Set-CsNetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="aecdf-130">Set-CsNetworkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkConfiguration)  
[<span data-ttu-id="aecdf-131">Remove-CsNetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="aecdf-131">Remove-CsNetworkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkConfiguration)  
  

<span data-ttu-id="aecdf-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aecdf-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

