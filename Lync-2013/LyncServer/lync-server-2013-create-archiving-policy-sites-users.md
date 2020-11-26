---
title: 'Lync Server 2013: criar uma política de arquivamento para habilitar ou desabilitar o arquivamento de comunicações internas ou externas para sites ou usuários específicos'
description: 'Lync Server 2013: criar uma política de arquivamento para habilitar ou desabilitar o arquivamento de comunicações internas ou externas para sites ou usuários específicos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating an Archiving policy to enable or disable Archiving of internal or external communications for specific sites or users
ms:assetid: 5864793a-ba72-470c-bb5b-9fb41e968896
ms:mtpsurl: https://technet.microsoft.com/library/Gg398385(v=OCS.15)
ms:contentKeyID: 48184193
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a23f952229df9fe950f2666914263a7cf46595f4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431985"
---
# <a name="creating-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-specific-sites-or-users"></a><span data-ttu-id="9b139-103">Criar uma política de arquivamento no Lync Server 2013 para habilitar ou desabilitar o arquivamento de comunicações internas ou externas para sites ou usuários específicos</span><span class="sxs-lookup"><span data-stu-id="9b139-103">Creating an Archiving policy in Lync Server 2013 to enable or disable Archiving of internal or external communications for specific sites or users</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9b139-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9b139-104">

<span> </span></span></span>

<span data-ttu-id="9b139-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="9b139-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="9b139-106">No Lync Server 2013, você usa políticas para habilitar e desabilitar o arquivamento para comunicações internas e comunicações externas para usuários hospedados no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9b139-106">In Lync Server 2013, you use policies to enable and disable archiving for internal communications and external communications for users homed on Lync Server 2013.</span></span> <span data-ttu-id="9b139-107">Isso inclui as seguintes políticas de arquivamento:</span><span class="sxs-lookup"><span data-stu-id="9b139-107">This includes the following Archiving policies:</span></span>

  - <span data-ttu-id="9b139-108">Uma política global criada por padrão quando você implanta o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9b139-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="9b139-109">Políticas opcionais no nível do site e no nível do usuário que você pode criar e usar para especificar como o arquivamento é implementado para sites ou usuários específicos.</span><span class="sxs-lookup"><span data-stu-id="9b139-109">Optional site-level and user-level policies that you can create and use to specify how archiving is implemented for specific sites or users.</span></span>

<span data-ttu-id="9b139-110">Inicialmente, você define as políticas de arquivamento ao implantar o arquivamento, mas pode alterar, adicionar e excluir políticas após a implantação.</span><span class="sxs-lookup"><span data-stu-id="9b139-110">You initially set up Archiving policies when you deploy Archiving, but you can change, add, and delete policies after deployment.</span></span> <span data-ttu-id="9b139-111">No painel de controle do Lync Server 2013, você pode usar a página **política de arquivamento** do grupo **arquivamento e monitoramento** para gerenciar políticas em nível global, nível de site e nível de usuário.</span><span class="sxs-lookup"><span data-stu-id="9b139-111">In Lync Server 2013 Control Panel, you can use the **Archiving Policy** page of the **Archiving and Monitoring** group to manage policies at the global level, site level, and user level.</span></span> <span data-ttu-id="9b139-112">Se você integrar o armazenamento do Lync Server ao armazenamento do Exchange 2013, as políticas de usuário do Exchange terão precedência sobre as políticas de arquivamento do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9b139-112">If you integrate your Lync Server storage with Exchange 2013 storage, the Exchange user policies take precedence over the Lync Server 2013 archiving policies.</span></span>

<span data-ttu-id="9b139-113">Para obter detalhes sobre como as políticas são implementadas, incluindo a hierarquia de políticas, consulte [como o arquivamento funciona no Lync Server 2013](lync-server-2013-how-archiving-works.md) na documentação de planejamento, documentação de implantação ou documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="9b139-113">For details about how policies are implemented, including the hierarchy of policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="9b139-114">Para controlar a implementação do arquivamento, você deve especificar opções em configurações de arquivamento, como se deseja arquivar mensagens instantâneas ou conferências, o uso do modo crítico e as opções de limpeza.</span><span class="sxs-lookup"><span data-stu-id="9b139-114">To control the implementation of Archiving, you must specify options in Archiving configurations, such as whether to archive IM or conferencing, the use of critical mode, and purging options.</span></span> <span data-ttu-id="9b139-115">Por padrão, nenhuma opção é habilitada na configuração de arquivamento global ou em qualquer configuração de arquivamento de site ou de pool.</span><span class="sxs-lookup"><span data-stu-id="9b139-115">By default no options are enabled in the global Archiving configuration or any site or pool Archiving configuration.</span></span> <span data-ttu-id="9b139-116">Você deve especificar todas as opções adequadas nas configurações de arquivamento antes de habilitar o arquivamento para comunicações internas ou externas nas políticas de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="9b139-116">You should specify all appropriate options in the Archiving configurations before enabling Archiving for internal or external communications in the Archiving policies.</span></span> <span data-ttu-id="9b139-117">Para obter detalhes, consulte <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Gerenciando opções de configuração de arquivamento no Lync Server 2013 para sua organização, sites e pools</A> na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="9b139-117">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span><BR><span data-ttu-id="9b139-118">Se você tiver habilitado a integração do Microsoft Exchange para a implantação, as políticas do Exchange controlarão se o arquivamento está habilitado para os usuários que são hospedados no Exchange 2013 e ter suas caixas de correio colocadas em In-Place isenção.</span><span class="sxs-lookup"><span data-stu-id="9b139-118">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="9b139-119">Para obter detalhes, consulte <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Configurando políticas para arquivamento no Lync server 2013 ao usar a integração com o Exchange Server</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="9b139-119">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site-or-users"></a><span data-ttu-id="9b139-120">Para criar uma política de arquivamento para um site ou usuários</span><span class="sxs-lookup"><span data-stu-id="9b139-120">To create an archiving policy for a site or users</span></span>

1.  <span data-ttu-id="9b139-121">Usando uma conta de usuário atribuída à função CsArchivingAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="9b139-121">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="9b139-122">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9b139-122">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="9b139-123">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="9b139-123">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="9b139-124">Na barra de navegação da esquerda, clique em **Monitoramento e Arquivamento**, e depois, clique em **Política de Arquivamento**.</span><span class="sxs-lookup"><span data-stu-id="9b139-124">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="9b139-125">Clique em **Novo** e execute uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="9b139-125">Click **New**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="9b139-126">Para criar uma política de arquivamento no nível do site, clique em **política do site** e, em **Selecione um site**, clique no site ao qual a política deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="9b139-126">To create a site-level archiving policy, click **Site policy** and then, in **Select a site**, click the site to which the policy is to be applied.</span></span>
    
      - <span data-ttu-id="9b139-127">Para criar uma política de arquivamento em nível do usuário, clique em **Política de usuário**.</span><span class="sxs-lookup"><span data-stu-id="9b139-127">To create a user-level archiving policy, click **User policy**.</span></span>

5.  <span data-ttu-id="9b139-128">Em **Nova Política de Arquivamento**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9b139-128">In **New Archiving Policy**, do the following:</span></span>
    
      - <span data-ttu-id="9b139-129">Em **Nome**, especifique um nome para a nova política (por exemplo, externalContoso).</span><span class="sxs-lookup"><span data-stu-id="9b139-129">In **Name**, specify a name for the new policy (for example, externalContoso).</span></span>
    
      - <span data-ttu-id="9b139-130">Em **Descrição**, forneça os detalhes sobre a política (por exemplo, a política de arquivamento de usuário externo da Contoso).</span><span class="sxs-lookup"><span data-stu-id="9b139-130">In **Description**, provide details about what the policy is (for example, External user archiving policy for Contoso).</span></span>
    
      - <span data-ttu-id="9b139-131">Para controlar o arquivamento das comunicações com usuários internos, marque ou desmarque a caixa de seleção **Arquivar comunicações internas**.</span><span class="sxs-lookup"><span data-stu-id="9b139-131">To control archiving of communications with internal users, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="9b139-132">Para controlar o arquivamento das comunicações com usuários externos, marque ou desmarque a caixa de seleção **Arquivar comunicações externas**.</span><span class="sxs-lookup"><span data-stu-id="9b139-132">To control archiving of communications with external users, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="9b139-133">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="9b139-133">Click **Commit**.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="9b139-134">As configurações de uma política do usuário se aplicam somente a usuários específicos e grupos de usuários aos quais você aplica a política.</span><span class="sxs-lookup"><span data-stu-id="9b139-134">The settings of a user policy only apply to the specific users and user groups to which you apply the policy.</span></span> <span data-ttu-id="9b139-135">Para obter detalhes, consulte <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">aplicando uma política de arquivamento a usuários no Lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="9b139-135">For details, see <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Applying an Archiving policy to users in Lync Server 2013</A></span></span>

    
    </div>

</div>

<div>

## <a name="creating-an-archiving-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="9b139-136">Criando uma política de arquivamento usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9b139-136">Creating an Archiving Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="9b139-137">As políticas de arquivamento podem ser criadas usando o Windows PowerShell e o cmdlet **Remove-CsArchivingPolicy** .</span><span class="sxs-lookup"><span data-stu-id="9b139-137">Archiving policies can be created by using Windows PowerShell and the **Remove-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="9b139-138">Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9b139-138">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="9b139-139">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="9b139-139">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-site-scope"></a><span data-ttu-id="9b139-140">Para criar uma nova política de arquivamento no escopo do site</span><span class="sxs-lookup"><span data-stu-id="9b139-140">To create a new archiving policy at the site scope</span></span>

  - <span data-ttu-id="9b139-141">Este comando cria uma nova política de arquivamento para o site de Redmond:</span><span class="sxs-lookup"><span data-stu-id="9b139-141">This command creates a new archiving policy for the Redmond site:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-per-user-scope"></a><span data-ttu-id="9b139-142">Para criar uma nova política de arquivamento no escopo por usuário</span><span class="sxs-lookup"><span data-stu-id="9b139-142">To create a new archiving policy at the per-user scope</span></span>

  - <span data-ttu-id="9b139-143">Para criar uma nova política de arquivamento no escopo por usuário, basta especificar uma identidade exclusiva ao criar a política:</span><span class="sxs-lookup"><span data-stu-id="9b139-143">To create a new archiving policy at the per-user scope, simply specify a unique Identity when creating the policy:</span></span>
    
        New-CsArchivingPolicy -Identity "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-internal-communication-sessions"></a><span data-ttu-id="9b139-144">Para criar uma nova política de arquivamento que permita o arquivamento de sessões de comunicação interna</span><span class="sxs-lookup"><span data-stu-id="9b139-144">To create a new archiving policy that enables archiving of internal communication sessions</span></span>

  - <span data-ttu-id="9b139-145">Como nenhum parâmetros foi especificado (além do parâmetro obrigatório Identity) nos comandos anteriores, as novas políticas utilizarão os valores padrão para todas as suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9b139-145">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding commands, the new policies will use the default values for all their properties.</span></span> <span data-ttu-id="9b139-146">Para criar políticas que utilizam valores de propriedades diferentes, basta incluir o parâmetro e o valor de parâmetro apropriado.</span><span class="sxs-lookup"><span data-stu-id="9b139-146">To create policies that use different property values, simply include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="9b139-147">Por exemplo, para criar uma política de arquivamento que permita o arquivamento de sessões de mensagens instantâneas internas, use um comando como este:</span><span class="sxs-lookup"><span data-stu-id="9b139-147">For example, to create an archiving policy that permits archiving of internal instant messaging sessions use a command like this:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-both-internal-and-external-communication-sessions"></a><span data-ttu-id="9b139-148">Para criar uma nova política de arquivamento que permita o arquivamento de sessões de comunicação interna e externa</span><span class="sxs-lookup"><span data-stu-id="9b139-148">To create a new archiving policy that enables archiving of both internal and external communication sessions</span></span>

  - <span data-ttu-id="9b139-149">Vários valores de propriedade podem ser modificados, incluindo vários parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9b139-149">Multiple property values can be modified by including multiple parameters.</span></span> <span data-ttu-id="9b139-150">Por exemplo, esse comando configura a nova política para arquivar sessões de mensagens instantâneas internas e externas:</span><span class="sxs-lookup"><span data-stu-id="9b139-150">For example, this command configures the new policy to archiving both internal and external instant messaging sessions:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True -ArchiveExternal $True

</div>

<span data-ttu-id="9b139-151">Para obter mais informações, consulte o tópico da ajuda para o cmdlet [New-CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="9b139-151">For more information, see the help topic for the [New-CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9b139-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b139-152">See Also</span></span>


[<span data-ttu-id="9b139-153">Gerenciar o arquivamento de comunicações internas e externas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9b139-153">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="9b139-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9b139-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

