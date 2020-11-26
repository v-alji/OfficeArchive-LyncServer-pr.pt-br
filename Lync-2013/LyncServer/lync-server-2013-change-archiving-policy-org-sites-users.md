---
title: 'Lync Server 2013: alterar uma política de arquivamento para habilitar ou desabilitar o arquivamento de comunicações internas ou externas para sua organização, sites ou usuários'
description: 'Lync Server 2013: alterar uma política de arquivamento para habilitar ou desabilitar o arquivamento de comunicações internas ou externas para sua organização, sites ou usuários.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changing an Archiving policy to enable or disable Archiving of internal or external communications for your organization, sites, or users
ms:assetid: b85dc3fb-8ebd-4e3c-ac90-fc79270ac867
ms:mtpsurl: https://technet.microsoft.com/library/Gg182576(v=OCS.15)
ms:contentKeyID: 48185234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee24f3d72e447a778d434994dff1795baa04d420
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435177"
---
# <a name="changing-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-your-organization-sites-or-users"></a><span data-ttu-id="628e6-103">Alterar uma política de arquivamento no Lync Server 2013 para habilitar ou desabilitar o arquivamento de comunicações internas ou externas para sua organização, sites ou usuários</span><span class="sxs-lookup"><span data-stu-id="628e6-103">Changing an Archiving policy in Lync Server 2013 to enable or disable Archiving of internal or external communications for your organization, sites, or users</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="628e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="628e6-104">

<span> </span></span></span>

<span data-ttu-id="628e6-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="628e6-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="628e6-106">No Lync Server 2013, você usa políticas para habilitar e desabilitar o arquivamento para comunicações internas e comunicações externas para usuários hospedados no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="628e6-106">In Lync Server 2013, you use policies to enable and disable archiving for internal communications and external communications for users homed on Lync Server 2013.</span></span> <span data-ttu-id="628e6-107">Isso inclui as seguintes políticas de arquivamento:</span><span class="sxs-lookup"><span data-stu-id="628e6-107">This includes the following Archiving policies:</span></span>

  - <span data-ttu-id="628e6-108">Uma política global criada por padrão quando você implanta o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="628e6-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="628e6-109">Políticas opcionais no nível do site e no nível do usuário que você pode criar e usar para especificar como o arquivamento é implementado para sites ou usuários específicos.</span><span class="sxs-lookup"><span data-stu-id="628e6-109">Optional site-level and user-level policies that you can create and use to specify how archiving is implemented for specific sites or users.</span></span>

<span data-ttu-id="628e6-110">Inicialmente, você define as políticas de arquivamento ao implantar o arquivamento, mas pode alterar, adicionar e excluir políticas após a implantação.</span><span class="sxs-lookup"><span data-stu-id="628e6-110">You initially set up Archiving policies when you deploy Archiving, but you can change, add, and delete policies after deployment.</span></span> <span data-ttu-id="628e6-111">No painel de controle do Lync Server 2013, você pode usar a página **política de arquivamento** do grupo **arquivamento e monitoramento** para gerenciar políticas em nível global, nível de site e nível de usuário.</span><span class="sxs-lookup"><span data-stu-id="628e6-111">In Lync Server 2013 Control Panel, you can use the **Archiving Policy** page of the **Archiving and Monitoring** group to manage policies at the global level, site level, and user level.</span></span> <span data-ttu-id="628e6-112">Se você integrar o armazenamento do Lync Server ao armazenamento do Exchange 2013, as políticas de usuário do Exchange terão precedência sobre as políticas de arquivamento do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="628e6-112">If you integrate your Lync Server storage with Exchange 2013 storage, the Exchange user policies take precedence over the Lync Server 2013 archiving policies.</span></span>

<span data-ttu-id="628e6-113">Para obter detalhes sobre como as políticas são implementadas, incluindo a hierarquia de políticas, consulte [como o arquivamento funciona no Lync Server 2013](lync-server-2013-how-archiving-works.md) na documentação de planejamento, documentação de implantação ou documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="628e6-113">For details about how policies are implemented, including the hierarchy of policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="628e6-114">Se você tiver habilitado a integração do Microsoft Exchange para a implantação, as políticas do Exchange controlarão se o arquivamento está habilitado para os usuários que são hospedados no Exchange 2013 e ter suas caixas de correio colocadas em In-Place isenção.</span><span class="sxs-lookup"><span data-stu-id="628e6-114">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="628e6-115">Para obter detalhes, consulte <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Configurando políticas para arquivamento no Lync server 2013 ao usar a integração com o Exchange Server</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="628e6-115">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="628e6-116">Você deve especificar todas as opções adequadas nas configurações de arquivamento antes de habilitar o arquivamento.</span><span class="sxs-lookup"><span data-stu-id="628e6-116">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="628e6-117">Para obter detalhes, consulte <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Gerenciando opções de configuração de arquivamento no Lync Server 2013 para sua organização, sites e pools</A> na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="628e6-117">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="to-change-an-archiving-policy"></a><span data-ttu-id="628e6-118">Para alterar uma política de arquivamento</span><span class="sxs-lookup"><span data-stu-id="628e6-118">To change an archiving policy</span></span>

1.  <span data-ttu-id="628e6-119">Usando uma conta de usuário atribuída à função CsArchivingAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="628e6-119">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="628e6-120">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="628e6-120">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="628e6-121">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="628e6-121">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="628e6-122">Na barra de navegação da esquerda, clique em **Monitoramento e Arquivamento**, e depois, clique em **Política de Arquivamento**.</span><span class="sxs-lookup"><span data-stu-id="628e6-122">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="628e6-123">Na lista de políticas, faça um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="628e6-123">In the list of policies, do one of the following:</span></span>
    
      - <span data-ttu-id="628e6-124">Para alterar a política da implantação inteira, clique em **Global** na lista de políticas, clique em **Editar** e em **Mostrar detalhes**.</span><span class="sxs-lookup"><span data-stu-id="628e6-124">To change the policy for your entire deployment, click **Global** in the list of policies, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="628e6-125">Para alterar a política de um único site, clique no nome do site na lista de políticas, clique em **Editar** e em **Mostrar detalhes**.</span><span class="sxs-lookup"><span data-stu-id="628e6-125">To change the policy for a single site, click the site name in the list of policies, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="628e6-126">Para alterar a política de um único usuário ou grupo de usuários, clique no nome do usuário ou do grupo de usuários na lista de políticas, clique em **Editar** e em **Mostrar detalhes**.</span><span class="sxs-lookup"><span data-stu-id="628e6-126">To change the policy for a single user or user group, click the user or user group name in the list of policies, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="628e6-127">Na página **Editar política de arquivamento**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="628e6-127">On the **Edit Archiving Policy** page, do the following:</span></span>
    
      - <span data-ttu-id="628e6-128">Para habilitar ou desabilitar o arquivamento interno da política, marque ou desmarque a caixa de seleção **Arquivar comunicações internas**.</span><span class="sxs-lookup"><span data-stu-id="628e6-128">To enable or disable internal archiving for the policy, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="628e6-129">Para habilitar ou desabilitar o arquivamento externo da política, marque ou desmarque a caixa de seleção **Arquivar comunicações externas**.</span><span class="sxs-lookup"><span data-stu-id="628e6-129">To enable or disable external archiving for the policy, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="628e6-130">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="628e6-130">Click **Commit**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="628e6-131">As configurações de uma política do usuário se aplicam somente a usuários específicos e grupos de usuários aos quais você aplica a política.</span><span class="sxs-lookup"><span data-stu-id="628e6-131">The settings of a user policy only apply to the specific users and user groups to which you apply the policy.</span></span> <span data-ttu-id="628e6-132">Para obter detalhes, consulte <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">aplicando uma política de arquivamento a usuários no Lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="628e6-132">For details, see <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Applying an Archiving policy to users in Lync Server 2013</A></span></span>

    
    </div>

</div>

<div>

## <a name="enabling-and-disabling-archiving-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="628e6-133">Habilitando e desabilitando o arquivamento usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="628e6-133">Enabling and Disabling Archiving by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="628e6-134">O arquivamento pode ser habilitado e desabilitado (para sessões de comunicação internas e externas) usando o cmdlet **set-CsArchivingPolicy** .</span><span class="sxs-lookup"><span data-stu-id="628e6-134">Archiving can be enabled and disabled (for both internal and external communication sessions) by using the **Set-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="628e6-135">Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="628e6-135">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="628e6-136">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="628e6-136">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-the-archiving-of-internal-communication-sessions"></a><span data-ttu-id="628e6-137">Para habilitar o arquivamento de sessões de comunicação interna</span><span class="sxs-lookup"><span data-stu-id="628e6-137">To enable the archiving of internal communication sessions</span></span>

  - <span data-ttu-id="628e6-138">Para habilitar o arquivamento de sessões de comunicação interna, defina o valor da propriedade **ArchiveInternal** como True ($true).</span><span class="sxs-lookup"><span data-stu-id="628e6-138">To enable archiving of internal communication sessions, set the value of the **ArchiveInternal** property to True ($True).</span></span> <span data-ttu-id="628e6-139">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="628e6-139">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-external-communication-sessions"></a><span data-ttu-id="628e6-140">Para habilitar o arquivamento de sessões de comunicação externa</span><span class="sxs-lookup"><span data-stu-id="628e6-140">To enable the archiving of external communication sessions</span></span>

  - <span data-ttu-id="628e6-141">Para habilitar o arquivamento de sessões de comunicação externa, defina o valor da propriedade **ArchiveExternal** como True ($true).</span><span class="sxs-lookup"><span data-stu-id="628e6-141">To enable archiving of external communication sessions, set the value of the **ArchiveExternal** property to True ($True).</span></span> <span data-ttu-id="628e6-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="628e6-142">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveExternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-both-internal-and-external-communication-sessions"></a><span data-ttu-id="628e6-143">Para habilitar o arquivamento de sessões de comunicação internas e externas</span><span class="sxs-lookup"><span data-stu-id="628e6-143">To enable the archiving of both internal and external communication sessions</span></span>

  - <span data-ttu-id="628e6-144">Para habilitar o arquivamento de sessões de comunicação internas e externas, defina as propriedades **ArchiveInternal** e **ArchiveExternal** como true:</span><span class="sxs-lookup"><span data-stu-id="628e6-144">To enable archiving of both internal and external communications sessions, set both the **ArchiveInternal** and the **ArchiveExternal** properties to True:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True -ArchiveExternal $True

</div>

<div>

## <a name="to-disable-archiving"></a><span data-ttu-id="628e6-145">Para desabilitar o arquivamento</span><span class="sxs-lookup"><span data-stu-id="628e6-145">To disable archiving</span></span>

  - <span data-ttu-id="628e6-146">Para desabilitar o arquivamento completamente, defina ambas as propriedades **ArchiveInternal** e **ArchiveExternal** como false ($false).</span><span class="sxs-lookup"><span data-stu-id="628e6-146">To disable archiving altogether, set both the **ArchiveInternal** and **ArchiveExternal** properties to False ($False).</span></span> <span data-ttu-id="628e6-147">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="628e6-147">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $False -ArchiveExternal $False

</div>

<span data-ttu-id="628e6-148">Para obter mais informações, consulte o tópico da ajuda para o cmdlet [set-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingPolicy) .</span><span class="sxs-lookup"><span data-stu-id="628e6-148">For more information, see the help topic for the [Set-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingPolicy) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="628e6-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="628e6-149">See Also</span></span>


[<span data-ttu-id="628e6-150">Gerenciar o arquivamento de comunicações internas e externas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="628e6-150">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="628e6-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="628e6-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

