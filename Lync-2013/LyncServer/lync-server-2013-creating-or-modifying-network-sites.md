---
title: 'Lync Server 2013: Criando ou modificando sites de rede'
description: 'Lync Server 2013: Criando ou modificando sites de rede.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating or modifying network sites
ms:assetid: 358aa08a-c5bc-45fc-8017-19e6202f88c5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520975(v=OCS.15)
ms:contentKeyID: 48183801
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 700f089cfe190a8f46b5eefc05e656e7c62a59a9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431383"
---
# <a name="creating-or-modifying-network-sites-in-lync-server-2013"></a><span data-ttu-id="ede47-103">Criando ou modificando sites de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ede47-103">Creating or modifying network sites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ede47-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ede47-104">

<span> </span></span></span>

<span data-ttu-id="ede47-105">_**Tópico da última modificação:** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="ede47-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="ede47-106">Sites de rede são os escritórios ou locais configurados em cada região de um controle de admissão de chamadas (CAC) ou implantação 9-1-1 aprimorada.</span><span class="sxs-lookup"><span data-stu-id="ede47-106">Network sites are the offices or locations configured within each region of a call admission control (CAC) or Enhanced 9-1-1 deployment.</span></span> <span data-ttu-id="ede47-107">Você pode usar o painel de controle do Microsoft Lync Server 2013 para configurar sites e associá-los a regiões.</span><span class="sxs-lookup"><span data-stu-id="ede47-107">You can use the Microsoft Lync Server 2013 Control Panel to configure sites and associate them with regions.</span></span> <span data-ttu-id="ede47-108">Por exemplo, uma região de rede para a América do Norte pode estar associada a sites de redes como Chicago, Redmond e Vancouver.</span><span class="sxs-lookup"><span data-stu-id="ede47-108">For example, a network region for North America might be associated with networks sites such as Chicago, Redmond, and Vancouver.</span></span> <span data-ttu-id="ede47-109">Um site de rede do CAC deve ser criado para cada site dentro de uma organização, mesmo que esse site não tenha limitações de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="ede47-109">A CAC network site must be created for every site within an organization, even if that site has no bandwidth limitations.</span></span> <span data-ttu-id="ede47-110">No painel de controle do Lync Server, você pode criar, modificar e excluir sites de rede.</span><span class="sxs-lookup"><span data-stu-id="ede47-110">From the Lync Server Control Panel you can create, modify, and delete network sites.</span></span> <span data-ttu-id="ede47-111">Use os procedimentos a seguir para criar ou modificar um site de rede.</span><span class="sxs-lookup"><span data-stu-id="ede47-111">Use the following procedures to create or modify a network site.</span></span> <span data-ttu-id="ede47-112">Para obter detalhes sobre como excluir um site de rede existente, consulte [excluindo um site de rede existente no Lync Server 2013](lync-server-2013-deleting-an-existing-network-site.md).</span><span class="sxs-lookup"><span data-stu-id="ede47-112">For details on deleting an existing network site, see [Deleting an existing network site in Lync Server 2013](lync-server-2013-deleting-an-existing-network-site.md).</span></span>

<div>

## <a name="to-create-a-network-site"></a><span data-ttu-id="ede47-113">Para criar um site de rede</span><span class="sxs-lookup"><span data-stu-id="ede47-113">To create a network site</span></span>

1.  <span data-ttu-id="ede47-114">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="ede47-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ede47-115">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ede47-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ede47-116">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ede47-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ede47-117">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **site**.</span><span class="sxs-lookup"><span data-stu-id="ede47-117">In the left navigation bar, click **Network Configuration** and then click **Site**.</span></span>

4.  <span data-ttu-id="ede47-118">Na página do **site** , clique em **novo**.</span><span class="sxs-lookup"><span data-stu-id="ede47-118">On the **Site** page, click **New**.</span></span>

5.  <span data-ttu-id="ede47-119">Em **novo site**, digite um nome para este site no campo **nome** .</span><span class="sxs-lookup"><span data-stu-id="ede47-119">In **New Site**, type a name for this site in the **Name** field.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ede47-120">Os nomes dos sites devem ser exclusivos na implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ede47-120">Site names must be unique within the Lync Server 2013 deployment.</span></span>

    
    </div>

6.  <span data-ttu-id="ede47-121">Na lista suspensa **região** , selecione uma região de rede para associar a este site.</span><span class="sxs-lookup"><span data-stu-id="ede47-121">In the **Region** drop-down list, select a network region to associate with this site.</span></span>

7.  <span data-ttu-id="ede47-122">Adicionais Se você quiser colocar as limitações de largura de banda em chamadas de áudio ou vídeo para este site, selecione o perfil da política de largura de banda com as configurações apropriadas na lista suspensa **política de largura de banda** .</span><span class="sxs-lookup"><span data-stu-id="ede47-122">(Optional) If you want to place bandwidth limitations on audio or video calls to this site, select the bandwidth policy profile with the appropriate settings from the **Bandwidth policy** drop-down list.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ede47-123">Você pode exibir os detalhes dos perfis da política de largura de banda disponíveis ou criar um novo perfil de política de largura de banda na página <STRONG>perfil da política</STRONG> do grupo <STRONG>configuração de rede</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="ede47-123">You can view the details of the available bandwidth policy profiles, or create a new bandwidth policy profile, on the <STRONG>Policy Profile</STRONG> page of the <STRONG>Network Configuration</STRONG> group.</span></span> <span data-ttu-id="ede47-124">Para obter detalhes, consulte <A href="lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md">criando ou modificando perfis de política de largura de banda no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="ede47-124">For details, see <A href="lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md">Creating or modifying bandwidth policy profiles in Lync Server 2013</A>.</span></span>

    
    </div>

8.  <span data-ttu-id="ede47-125">Adicionais Se você quiser fornecer configurações de localização para este site, selecione uma política de localização na lista suspensa **política de localização** .</span><span class="sxs-lookup"><span data-stu-id="ede47-125">(Optional) If you want to provide location settings for this site, select a location policy from the **Location policy** drop-down list.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ede47-126">A política de localização atribui configurações de localização avançada de 9-1-1 (E9-1-1) e de cliente de cliente (-1-1) específicas ao site.</span><span class="sxs-lookup"><span data-stu-id="ede47-126">The location policy assigns specific Enhanced 9-1-1 (E9-1-1) and client location settings to the site.</span></span> <span data-ttu-id="ede47-127">Você pode exibir os detalhes das políticas de localização disponíveis ou criar uma nova política de localização, na página <STRONG>política de localização</STRONG> do grupo de <STRONG>configuração de rede</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="ede47-127">You can view the details of the available location policies, or create a new location policy, from the <STRONG>Location Policy</STRONG> page of the <STRONG>Network Configuration</STRONG> group.</span></span> <span data-ttu-id="ede47-128">Para obter detalhes, consulte <A href="lync-server-2013-viewing-location-policy-information.md">exibindo informações de política de localização no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="ede47-128">For details, see <A href="lync-server-2013-viewing-location-policy-information.md">Viewing location policy information in Lync Server 2013</A>.</span></span>

    
    </div>

9.  <span data-ttu-id="ede47-129">Adicionais Digite um valor no campo **Descrição** para fornecer mais informações sobre esse site que não pode ser expresso apenas pelo nome.</span><span class="sxs-lookup"><span data-stu-id="ede47-129">(Optional) Type a value in the **Description** field to provide more information about this site that cannot be expressed by the name alone.</span></span>

10. <span data-ttu-id="ede47-130">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="ede47-130">Click **Commit**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ede47-131">Você não usa a tabela de <STRONG>sub-redes associadas</STRONG> quando cria um novo site de rede.</span><span class="sxs-lookup"><span data-stu-id="ede47-131">You do not use the <STRONG>Associated Subnets</STRONG> table when you create a new network site.</span></span> <span data-ttu-id="ede47-132">Você associa uma sub-rede a um site quando cria ou modifica a sub-rede.</span><span class="sxs-lookup"><span data-stu-id="ede47-132">You associate a subnet with a site when you create or modify the subnet.</span></span> <span data-ttu-id="ede47-133">Para obter detalhes, consulte <A href="lync-server-2013-create-or-modify-network-subnets.md">criar ou modificar sub-redes de rede no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="ede47-133">For details, see <A href="lync-server-2013-create-or-modify-network-subnets.md">Create or modify network subnets in Lync Server 2013</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="to-modify-a-network-site"></a><span data-ttu-id="ede47-134">Para modificar um site de rede</span><span class="sxs-lookup"><span data-stu-id="ede47-134">To modify a network site</span></span>

1.  <span data-ttu-id="ede47-135">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="ede47-135">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ede47-136">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ede47-136">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ede47-137">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ede47-137">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ede47-138">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **site**.</span><span class="sxs-lookup"><span data-stu-id="ede47-138">In the left navigation bar, click **Network Configuration** and then click **Site**.</span></span>

4.  <span data-ttu-id="ede47-139">Na página do **site** , clique no site que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="ede47-139">On the **Site** page, click the site that you want to modify.</span></span>

5.  <span data-ttu-id="ede47-140">No menu **Editar**, clique em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="ede47-140">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="ede47-141">Na página **Editar site** , você pode modificar a descrição, a região, o perfil da política de largura de banda e a política de localização associada ao site.</span><span class="sxs-lookup"><span data-stu-id="ede47-141">On the **Edit Site** page, you can modify the description, region, bandwidth policy profile, and location policy associated with the site.</span></span> <span data-ttu-id="ede47-142">Para obter detalhes, consulte a seção "para criar um site de rede" anteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="ede47-142">For details, see "To create a network site" section earlier in this topic.</span></span>

7.  <span data-ttu-id="ede47-143">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="ede47-143">Click **Commit**.</span></span>

<span data-ttu-id="ede47-144">Não é possível modificar a tabela de **sub-redes associadas** nesta página.</span><span class="sxs-lookup"><span data-stu-id="ede47-144">You cannot modify the **Associated Subnets** table on this page.</span></span> <span data-ttu-id="ede47-145">A lista de sub-redes associadas é fornecida para referência para que você saiba quais são as sub-redes que serão afetadas quando você modificar as configurações do site.</span><span class="sxs-lookup"><span data-stu-id="ede47-145">The list of associated subnets is provided for reference so that you are aware of what subnets will be affected when you modify the site settings.</span></span>

</div>

<div>

## <a name="to-delete-a-network-site"></a><span data-ttu-id="ede47-146">Para excluir um site de rede</span><span class="sxs-lookup"><span data-stu-id="ede47-146">To delete a network site</span></span>

1.  <span data-ttu-id="ede47-147">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="ede47-147">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ede47-148">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ede47-148">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ede47-149">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ede47-149">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ede47-150">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **site**.</span><span class="sxs-lookup"><span data-stu-id="ede47-150">In the left navigation bar, click **Network Configuration** and then click **Site**.</span></span>

4.  <span data-ttu-id="ede47-151">Na página do **site** , clique no site que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="ede47-151">On the **Site** page, click the site that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ede47-152">Você pode excluir mais de um site de cada vez.</span><span class="sxs-lookup"><span data-stu-id="ede47-152">You can delete more than one site at a time.</span></span> <span data-ttu-id="ede47-153">Para fazer isso, pressione CTRL e selecione vários sites enquanto mantém a tecla CTRL pressionada.</span><span class="sxs-lookup"><span data-stu-id="ede47-153">To do this, press CTRL and select multiple sites while holding down the CTRL key.</span></span> <span data-ttu-id="ede47-154">Ou, para selecionar todos os sites, clique em <STRONG>selecionar tudo</STRONG> no menu <STRONG>Editar</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="ede47-154">Or, to select all sites, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="ede47-155">No menu **Editar** , clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="ede47-155">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="ede47-156">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="ede47-156">Click **OK**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="ede47-157">Você não pode remover um site de rede se ele estiver associado a uma sub-rede de rede.</span><span class="sxs-lookup"><span data-stu-id="ede47-157">You cannot remove a network site if it is associated with a network subnet.</span></span> <span data-ttu-id="ede47-158">Se você tentar remover um site associado a uma sub-rede, receberá uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="ede47-158">If you attempt to remove a site associated with a subnet you will receive an error message.</span></span> <span data-ttu-id="ede47-159">Para ver se um site está associado a qualquer sub-rede, clique no site e, em seguida, clique em <STRONG>Mostrar detalhes</STRONG> no menu <STRONG>Editar</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="ede47-159">To see if a site is associated with any subnets, click the site and then click <STRONG>Show details</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ede47-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="ede47-160">See Also</span></span>


[<span data-ttu-id="ede47-161">Excluindo um site de rede existente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ede47-161">Deleting an existing network site in Lync Server 2013</span></span>](lync-server-2013-deleting-an-existing-network-site.md)  


[<span data-ttu-id="ede47-162">New-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="ede47-162">New-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite)  
[<span data-ttu-id="ede47-163">Set-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="ede47-163">Set-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkSite)  
[<span data-ttu-id="ede47-164">Remove-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="ede47-164">Remove-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkSite)  
[<span data-ttu-id="ede47-165">Get-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="ede47-165">Get-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSite)  
  

<span data-ttu-id="ede47-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ede47-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

