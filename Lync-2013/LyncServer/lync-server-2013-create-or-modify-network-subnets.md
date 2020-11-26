---
title: 'Lync Server 2013: criar ou modificar sub-redes de rede'
description: 'Lync Server 2013: criar ou modificar sub-redes de rede.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify network subnets
ms:assetid: 1ba8c4e3-fbc7-4758-88ac-d651fef17bed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520957(v=OCS.15)
ms:contentKeyID: 48183548
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37695707bf39b10c351a4990b132c9799406f9c4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431649"
---
# <a name="create-or-modify-network-subnets-in-lync-server-2013"></a><span data-ttu-id="85149-103">Criar ou modificar sub-redes de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85149-103">Create or modify network subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85149-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85149-104">

<span> </span></span></span>

<span data-ttu-id="85149-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="85149-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="85149-106">Uma sub-rede de rede deve estar associada a um site de rede para fins de determinar a localização geográfica do host pertencente a essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="85149-106">A network subnet must be associated with a network site for the purposes of determining the geographic location of the host belonging to this subnet.</span></span> <span data-ttu-id="85149-107">Você pode usar o painel de controle do Lync Server para configurar sub-redes.</span><span class="sxs-lookup"><span data-stu-id="85149-107">You can use Lync Server Control Panel to configure subnets.</span></span> <span data-ttu-id="85149-108">No painel de controle do Lync Server, você pode criar, modificar ou excluir uma sub-rede de rede.</span><span class="sxs-lookup"><span data-stu-id="85149-108">From the Lync Server Control Panel, you can create, modify, or delete a network subnet.</span></span> <span data-ttu-id="85149-109">Para obter detalhes sobre como excluir sub-redes de rede, consulte [excluindo sub-redes de rede no Lync Server 2013](lync-server-2013-deleting-network-subnets.md).</span><span class="sxs-lookup"><span data-stu-id="85149-109">For details about deleting network subnets, see [Deleting network subnets in Lync Server 2013](lync-server-2013-deleting-network-subnets.md).</span></span>

<span data-ttu-id="85149-110">Na maioria das implantações do Microsoft Lync Server 2013 em que o controle de admissão de chamadas (CAC) é implementado, normalmente há um grande número de sub-redes.</span><span class="sxs-lookup"><span data-stu-id="85149-110">In most deployments of Microsoft Lync Server 2013 where call admission control (CAC) is implemented, there will typically be a large number of subnets.</span></span> <span data-ttu-id="85149-111">Por isso, geralmente é melhor configurar sub-redes a partir do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="85149-111">Because of this, it is often best to configure subnets from the Lync Server Management Shell.</span></span> <span data-ttu-id="85149-112">Em seguida, você pode chamar **New-CsNetworkSubnet** em conjunto com o cmdlet **Import-CSV** do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="85149-112">From there you can call **New-CsNetworkSubnet** in conjunction with the Windows PowerShell cmdlet **Import-CSV**.</span></span> <span data-ttu-id="85149-113">Ao usar esses cmdlets juntos, você pode ler as configurações de sub-rede a partir de um arquivo de valores separados por vírgulas (. csv) e criar várias sub-redes ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="85149-113">By using these cmdlets together, you can read in subnet settings from a comma-separated values (.csv) file and create multiple subnets at the same time.</span></span> <span data-ttu-id="85149-114">Para obter exemplos de como criar sub-redes a partir de um arquivo. csv, consulte [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span><span class="sxs-lookup"><span data-stu-id="85149-114">For examples of how to create subnets from a .csv file, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<div>

## <a name="to-create-a-network-subnet"></a><span data-ttu-id="85149-115">Para criar uma sub-rede de rede</span><span class="sxs-lookup"><span data-stu-id="85149-115">To create a network subnet</span></span>

1.  <span data-ttu-id="85149-116">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="85149-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="85149-117">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="85149-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="85149-118">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="85149-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="85149-119">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **sub-rede**.</span><span class="sxs-lookup"><span data-stu-id="85149-119">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="85149-120">Na página **sub-rede** , clique em **novo**.</span><span class="sxs-lookup"><span data-stu-id="85149-120">On the **Subnet** page, click **New**.</span></span>

5.  <span data-ttu-id="85149-121">Em **nova sub-rede**, insira um valor no campo **subnet ID** .</span><span class="sxs-lookup"><span data-stu-id="85149-121">In **New Subnet**, enter a value in the **Subnet ID** field.</span></span> <span data-ttu-id="85149-122">Deve ser um endereço IP (por exemplo, 174.11.12.0) e deve ser o primeiro endereço no intervalo de endereços IP definido pela sub-rede.</span><span class="sxs-lookup"><span data-stu-id="85149-122">This must be an IP address (for example, 174.11.12.0), and it must be the first address in the IP address range defined by the subnet.</span></span>

6.  <span data-ttu-id="85149-123">No campo **máscara** , insira um valor numérico de 1 a 32.</span><span class="sxs-lookup"><span data-stu-id="85149-123">In the **Mask** field, enter a numeric value from 1 through 32.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="85149-124">Esse valor é o bitmask que deve ser aplicado à sub-rede que está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="85149-124">This value is the bitmask that is to be applied to the subnet being created.</span></span>

    
    </div>

7.  <span data-ttu-id="85149-125">Em **ID de site de rede**, selecione o site ao qual esta sub-rede pertence.</span><span class="sxs-lookup"><span data-stu-id="85149-125">In **Network site ID**, select the site to which this subnet belongs.</span></span>

8.  <span data-ttu-id="85149-126">Adicionais Digite um valor no campo **Descrição** para fornecer mais informações sobre essa sub-rede que não pode ser expressa apenas pelo nome.</span><span class="sxs-lookup"><span data-stu-id="85149-126">(Optional) Type a value in the **Description** field to provide more information about this subnet that cannot be expressed by the name alone.</span></span>

9.  <span data-ttu-id="85149-127">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="85149-127">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-network-subnet"></a><span data-ttu-id="85149-128">Para modificar uma sub-rede de rede</span><span class="sxs-lookup"><span data-stu-id="85149-128">To modify a network subnet</span></span>

1.  <span data-ttu-id="85149-129">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="85149-129">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="85149-130">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="85149-130">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="85149-131">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="85149-131">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="85149-132">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **sub-rede**.</span><span class="sxs-lookup"><span data-stu-id="85149-132">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="85149-133">Na página **sub-rede** , clique na sub-rede que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="85149-133">On the **Subnet** page, click the subnet that you want to modify.</span></span>

5.  <span data-ttu-id="85149-134">No menu **Editar**, clique em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="85149-134">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="85149-135">Na página **Editar sub-rede** , você pode modificar o bitmask, o site de rede associado ou a descrição.</span><span class="sxs-lookup"><span data-stu-id="85149-135">On the **Edit Subnet** page, you can modify the bitmask, associated network site, or description.</span></span> <span data-ttu-id="85149-136">Se você modificar o bitmask, lembre-se de que a identificação da sub-rede ainda deve ser o primeiro endereço no intervalo de endereços IP definido pela sub-rede.</span><span class="sxs-lookup"><span data-stu-id="85149-136">If you modify the bitmask, keep in mind that the Subnet ID must still be the first address in the IP address range defined by the subnet.</span></span>

7.  <span data-ttu-id="85149-137">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="85149-137">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="85149-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="85149-138">See Also</span></span>


[<span data-ttu-id="85149-139">Excluindo sub-redes de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85149-139">Deleting network subnets in Lync Server 2013</span></span>](lync-server-2013-deleting-network-subnets.md)  


[<span data-ttu-id="85149-140">Sobre regiões de rede, sites e subredes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85149-140">About network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-about-network-regions-sites-and-subnets.md)  


[<span data-ttu-id="85149-141">New-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="85149-141">New-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet)  
[<span data-ttu-id="85149-142">Set-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="85149-142">Set-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkSubnet)  
[<span data-ttu-id="85149-143">Remove-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="85149-143">Remove-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkSubnet)  
[<span data-ttu-id="85149-144">Get-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="85149-144">Get-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSubnet)  
  

<span data-ttu-id="85149-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85149-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

