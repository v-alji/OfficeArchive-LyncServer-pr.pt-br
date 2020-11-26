---
title: Migrar grupos de resposta
description: Migrar grupos de resposta.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate response groups
ms:assetid: 43741ae7-c871-4573-b660-f2f5febc0856
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204854(v=OCS.15)
ms:contentKeyID: 48184020
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 19da4d39b6f11931bffb5a6e422c2826e7351d69
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443766"
---
# <a name="migrate-response-groups"></a><span data-ttu-id="da673-103">Migrar grupos de resposta</span><span class="sxs-lookup"><span data-stu-id="da673-103">Migrate response groups</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="da673-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="da673-104">

<span> </span></span></span>

<span data-ttu-id="da673-105">_**Tópico da última modificação:** 2013-09-23_</span><span class="sxs-lookup"><span data-stu-id="da673-105">_**Topic Last Modified:** 2013-09-23_</span></span>

<span data-ttu-id="da673-106">Depois que os usuários forem movidos para pools do Lync Server 2013, você poderá migrar seus grupos de resposta.</span><span class="sxs-lookup"><span data-stu-id="da673-106">After your users are moved to Lync Server 2013 pools, you can migrate your response groups.</span></span> <span data-ttu-id="da673-107">Migrar grupos de resposta inclui a cópia de grupos de agente, filas, fluxos de trabalho, arquivos de áudio e movimentação de objetos de contato de grupo de resposta da implantação herdada para o pool do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="da673-107">Migrating response groups includes copying agent groups, queues, workflows, audio files, and moving Response Group contact objects from the legacy deployment to the Lync Server 2013 pool.</span></span> <span data-ttu-id="da673-108">Depois de migrar seus grupos de resposta herdados, as chamadas para os grupos de resposta são manipuladas pelo aplicativo grupo de resposta no pool do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="da673-108">After you migrate your legacy response groups, calls to the response groups are handled by the Response Group application in the Lync Server 2013 pool.</span></span> <span data-ttu-id="da673-109">As chamadas para grupos de resposta não são mais manipuladas pelo pool herdado.</span><span class="sxs-lookup"><span data-stu-id="da673-109">Calls to response groups are no longer handled by the legacy pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="da673-110">Embora seja possível migrar grupos de resposta antes de mover todos os usuários para o pool do Lync Server 2013, recomendamos que você mova todos os usuários primeiro.</span><span class="sxs-lookup"><span data-stu-id="da673-110">Although you can migrate response groups before you move all users to the Lync Server 2013 pool, we recommend that you move all users first.</span></span> <span data-ttu-id="da673-111">Em particular, os usuários que são agentes de grupo de resposta não terão funcionalidade completa dos novos recursos até serem movidos para o pool do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="da673-111">In particular, users who are response group agents will not have full functionality of new features until they are moved to the Lync Server 2013 pool.</span></span>



</div>

<span data-ttu-id="da673-112">Antes de migrar grupos de resposta, você deve ter implantado um pool do Lync Server 2013 que inclui o aplicativo do grupo de resposta.</span><span class="sxs-lookup"><span data-stu-id="da673-112">Before you migrate response groups, you must have deployed a Lync Server 2013 pool that includes the Response Group application.</span></span> <span data-ttu-id="da673-113">O aplicativo grupo de resposta é instalado e ativado por padrão ao implantar o Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="da673-113">The Response Group application is installed and activated by default when you deploy Enterprise Voice.</span></span> <span data-ttu-id="da673-114">Você pode garantir que o aplicativo do grupo de resposta seja instalado executando o cmdlet **Get-CsService-ApplicationServer** .</span><span class="sxs-lookup"><span data-stu-id="da673-114">You can ensure that the Response Group application is installed by running the **Get-CsService –ApplicationServer** cmdlet.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="da673-115">Você pode criar novos grupos de resposta do Lync Server 2013 no pool do Lync Server 2013 antes de migrar seus grupos de respostas herdadas.</span><span class="sxs-lookup"><span data-stu-id="da673-115">You can create new Lync Server 2013 response groups in the Lync Server 2013 pool before you migrate your legacy response groups.</span></span>



</div>

<span data-ttu-id="da673-116">Para migrar grupos de resposta de um pool herdado para o Lync Server 2013, execute o cmdlet **move-CsRgsConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="da673-116">To migrate response groups from a legacy pool to the Lync Server 2013, you run the **Move-CsRgsConfiguration** cmdlet.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="da673-117">O cmdlet de migração do grupo de resposta move a configuração do grupo de resposta para o pool inteiro.</span><span class="sxs-lookup"><span data-stu-id="da673-117">The Response Group migration cmdlet moves the Response Group configuration for the entire pool.</span></span> <span data-ttu-id="da673-118">Não é possível selecionar grupos, filas ou fluxos de trabalho específicos para migrar.</span><span class="sxs-lookup"><span data-stu-id="da673-118">You cannot select specific groups, queues, or workflows to migrate.</span></span>



</div>

<span data-ttu-id="da673-119">Depois de migrar os grupos de resposta, você precisará usar o painel de controle do Lync Server ou cmdlets do Shell de gerenciamento do Lync Server para verificar se todos os grupos de agente, filas e fluxos de trabalho foram movidos com êxito.</span><span class="sxs-lookup"><span data-stu-id="da673-119">After you migrate the response groups, you need to use Lync Server Control Panel or Lync Server Management Shell cmdlets to verify that all agent groups, queues, and workflows moved successfully.</span></span>

<span data-ttu-id="da673-120">Quando você migra grupos de resposta, os grupos de resposta do Lync Server 2010 não são removidos.</span><span class="sxs-lookup"><span data-stu-id="da673-120">When you migrate response groups, the Lync Server 2010 response groups are not removed.</span></span> <span data-ttu-id="da673-121">Ao gerenciar grupos de resposta após a migração usando o painel de controle do Lync Server ou o Shell de gerenciamento do Lync Server, você pode ver os grupos de resposta do Lync Server 2010 e os grupos de resposta do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="da673-121">When you manage response groups after migration by using either Lync Server Control Panel or Lync Server Management Shell, you can see both the Lync Server 2010 response groups and the Lync Server 2013 response groups.</span></span> <span data-ttu-id="da673-122">Você deve aplicar atualizações somente aos grupos de resposta do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="da673-122">You should apply updates only to the Lync Server 2013 response groups.</span></span> <span data-ttu-id="da673-123">Os grupos de resposta do Lync Server 2010 são mantidos somente para fins de recuperação.</span><span class="sxs-lookup"><span data-stu-id="da673-123">The Lync Server 2010 response groups are retained only for rollback purposes.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="da673-124">Após a conclusão da migração e os novos grupos de resposta terem sido criados, o painel de controle do Lync Server e o Shell de gerenciamento do Lync Server exibirão as versões do Lync Server 2010 e do Lync Server 2013 de cada grupo de resposta.</span><span class="sxs-lookup"><span data-stu-id="da673-124">After the migration has been completed and the new response groups have been created, the Lync Server Control Panel and the Lync Server Management Shell will display the Lync Server 2010 and Lync Server 2013 versions of each response group.</span></span> <span data-ttu-id="da673-125">Não use o painel de controle do Lync Server ou o Shell de gerenciamento do Lync Server para remover os grupos de resposta do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="da673-125">Do not use Lync Server Control Panel or Lync Server Management Shell to remove the Lync Server 2010 response groups.</span></span> <span data-ttu-id="da673-126">Se você remover um, o grupo de resposta correspondente criado durante a migração deixará de funcionar.</span><span class="sxs-lookup"><span data-stu-id="da673-126">If you do remove one, the corresponding response group that was created during migration will stop working.</span></span> <span data-ttu-id="da673-127">Os grupos de resposta do Lync Server 2010 serão removidos quando você encerrar o pool do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="da673-127">The Lync Server 2010 response groups will be removed when you decommission the Lync Server 2010 pool.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="da673-128">Recomendamos que você não remova dados de sua implantação anterior até encerrar o pool.</span><span class="sxs-lookup"><span data-stu-id="da673-128">We recommend that you do not remove any data from your previous deployment until you decommission the pool.</span></span> <span data-ttu-id="da673-129">Além disso, recomendamos enfaticamente que você exporte os grupos de resposta imediatamente após a migração.</span><span class="sxs-lookup"><span data-stu-id="da673-129">In addition, we strongly recommend that you export response groups immediately after you migrate.</span></span> <span data-ttu-id="da673-130">Se um grupo de resposta do Lync Server 2010 deve ser removido, você pode restaurar seus grupos de resposta do backup para obter os grupos de resposta do Lync Server 2013 sendo executados novamente.</span><span class="sxs-lookup"><span data-stu-id="da673-130">If a Lync Server 2010 response group should get removed, you can then restore your response groups from the backup to get Lync Server 2013 response groups running again.</span></span>



</div>

<span data-ttu-id="da673-131">O Lync Server 2013 introduz um novo recurso de grupo de resposta chamado **tipo de fluxo de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="da673-131">Lync Server 2013 introduces a new Response Group feature called **Workflow Type**.</span></span> <span data-ttu-id="da673-132">O **tipo de fluxo de trabalho** pode ser **gerenciado** ou **não gerenciado**.</span><span class="sxs-lookup"><span data-stu-id="da673-132">**Workflow Type** can be **Managed** or **Unmanaged**.</span></span> <span data-ttu-id="da673-133">Todos os grupos de resposta são migrados com o **tipo de fluxo de trabalho** definido como **não gerenciado** e com uma lista de gerentes vazia.</span><span class="sxs-lookup"><span data-stu-id="da673-133">All response groups are migrated with **Workflow Type** set to **Unmanaged** and with an empty Manager list.</span></span>

<span data-ttu-id="da673-134">Quando você executa o cmdlet **move-CsRgsConfiguration** , os grupos de agente, filas, fluxos de trabalho e arquivos de áudio permanecem no pool herdado para fins de reversão.</span><span class="sxs-lookup"><span data-stu-id="da673-134">When you run the **Move-CsRgsConfiguration** cmdlet, the agent groups, queues, workflows, and audio files remain in the legacy pool for rollback purposes.</span></span> <span data-ttu-id="da673-135">No entanto, se você precisar reverter para o pool herdado, será necessário executar o cmdlet **move-CsApplicationEndpoint** para mover objetos de contato de volta para o pool herdado.</span><span class="sxs-lookup"><span data-stu-id="da673-135">If you do need to roll back to the legacy pool, however, you need to run the **Move-CsApplicationEndpoint** cmdlet to move contact objects back to the legacy pool.</span></span>

<span data-ttu-id="da673-136">O procedimento a seguir para migrar configurações de grupo de resposta pressupõe que você tenha uma relação um-para-um entre seus pools herdados e os pools do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="da673-136">The following procedure for migrating Response Group configurations assumes that you have a one-to-one relationship between your legacy pools and the Lync Server 2013 pools.</span></span> <span data-ttu-id="da673-137">Se você planeja consolidar ou dividir os pools durante a migração e a implantação, será necessário planejar quais pools herdados são mapeados para qual Lync Server 2013 pool.</span><span class="sxs-lookup"><span data-stu-id="da673-137">If you plan to consolidate or split up pools during your migration and deployment, you need to plan which legacy pool maps to which Lync Server 2013 pool.</span></span>

<div>

## <a name="to-migrate-response-group-configurations"></a><span data-ttu-id="da673-138">Migrar configurações de grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="da673-138">To migrate Response Group configurations</span></span>

1.  <span data-ttu-id="da673-139">Faça logon no computador com uma conta que seja membro do grupo RTCUniversalServerAdmins ou tenha direitos e permissões de administrador equivalentes.</span><span class="sxs-lookup"><span data-stu-id="da673-139">Log on to the computer with an account that is a member of the RTCUniversalServerAdmins group or has equivalent administrator rights and permissions.</span></span>

2.  <span data-ttu-id="da673-140">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="da673-140">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="da673-141">Execute:</span><span class="sxs-lookup"><span data-stu-id="da673-141">Run:</span></span>
    
        Move-CsRgsConfiguration -Source <source pool FQDN> -Destination <destination pool FQDN>
    
    <span data-ttu-id="da673-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="da673-142">For example:</span></span>
    
        Move-CsRgsConfiguration -Source lync-old.contoso.net -Destination lync-new.contoso.net

4.  <span data-ttu-id="da673-143">Depois de migrar grupos de resposta e agentes para o pool do Lync Server 2013, a URL usada pelos agentes para entrar e sair é uma URL do Lync Server 2013 e está disponível no menu **ferramentas** .</span><span class="sxs-lookup"><span data-stu-id="da673-143">After you migrate response groups and agents to the Lync Server 2013 pool, the URL that agents use to sign in and sign out is a Lync Server 2013 URL and is available from the **Tools** menu.</span></span> <span data-ttu-id="da673-144">Lembre os agentes para atualizar todas as referências, como indicadores, para a nova URL.</span><span class="sxs-lookup"><span data-stu-id="da673-144">Remind agents to update any references, such as bookmarks, to the new URL.</span></span>

</div>

<div>

## <a name="to-verify-response-group-migration-by-using-lync-server-control-panel"></a><span data-ttu-id="da673-145">Para verificar a migração do grupo de resposta usando o painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="da673-145">To verify Response Group migration by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="da673-146">Faça logon no computador com uma conta que seja membro do grupo RTCUniversalReadOnlyAdmins ou que seja minimamente um membro da função CsViewOnlyAdministrator.</span><span class="sxs-lookup"><span data-stu-id="da673-146">Log on to the computer with an account that is a member of RTCUniversalReadOnlyAdmins group or is minimally a member of the CsViewOnlyAdministrator role.</span></span>

2.  <span data-ttu-id="da673-147">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="da673-147">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="da673-148">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="da673-148">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="da673-149">No painel de navegação esquerdo, clique em **grupos de resposta**.</span><span class="sxs-lookup"><span data-stu-id="da673-149">In the left navigation pane, click **Response Groups**.</span></span>

4.  <span data-ttu-id="da673-150">Na guia **fluxo de trabalho** , verifique se todos os fluxos de trabalho no ambiente do Lync Server 2010 estão incluídos na lista.</span><span class="sxs-lookup"><span data-stu-id="da673-150">On the **Workflow** tab, verify that all the workflows in your Lync Server 2010 environment are included in the list.</span></span>

5.  <span data-ttu-id="da673-151">Clique na guia **fila** e verifique se todas as filas em seu ambiente do Lync Server 2010 estão incluídas na lista.</span><span class="sxs-lookup"><span data-stu-id="da673-151">Click the **Queue** tab, and verify that all the queues in your Lync Server 2010 environment are included in the list.</span></span>

6.  <span data-ttu-id="da673-152">Clique na guia **grupo** e verifique se todos os grupos de agente no ambiente do Lync Server 2010 estão incluídos na lista.</span><span class="sxs-lookup"><span data-stu-id="da673-152">Click the **Group** tab, and verify that all the agent groups in your Lync Server 2010 environment are included in the list.</span></span>

</div>

<div>

## <a name="to-verify-response-group-migration-by-using-lync-server-management-shell"></a><span data-ttu-id="da673-153">Para verificar a migração do grupo de resposta usando o Shell de gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="da673-153">To verify Response Group migration by using Lync Server Management Shell</span></span>

1.  <span data-ttu-id="da673-154">Faça logon no computador com uma conta que seja membro do grupo RTCUniversalReadOnlyAdmins ou que seja minimamente um membro da função CsViewOnlyAdministrator.</span><span class="sxs-lookup"><span data-stu-id="da673-154">Log on to the computer with an account that is a member of RTCUniversalReadOnlyAdmins group or is minimally a member of the CsViewOnlyAdministrator role.</span></span>

2.  <span data-ttu-id="da673-155">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="da673-155">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>
    
    <span data-ttu-id="da673-156">Para obter detalhes sobre os seguintes cmdlets, execute:</span><span class="sxs-lookup"><span data-stu-id="da673-156">For details about the following cmdlets, run:</span></span>
    
        Get-Help <cmdlet name> -Detailed

3.  <span data-ttu-id="da673-157">Execute:</span><span class="sxs-lookup"><span data-stu-id="da673-157">Run:</span></span>
    
        Get-CsRgsAgentGroup

4.  <span data-ttu-id="da673-158">Verifique se todos os grupos de agente no ambiente do Lync Server 2010 estão incluídos na lista.</span><span class="sxs-lookup"><span data-stu-id="da673-158">Verify that all the agent groups in your Lync Server 2010 environment are included in the list.</span></span>

5.  <span data-ttu-id="da673-159">Execute:</span><span class="sxs-lookup"><span data-stu-id="da673-159">Run:</span></span>
    
        Get-CsRgsQueue

6.  <span data-ttu-id="da673-160">Verifique se todas as filas no ambiente do Lync Server 2010 estão incluídas na lista.</span><span class="sxs-lookup"><span data-stu-id="da673-160">Verify that all the queues in your Lync Server 2010 environment are included in the list.</span></span>

7.  <span data-ttu-id="da673-161">Execute:</span><span class="sxs-lookup"><span data-stu-id="da673-161">Run:</span></span>
    
        Get-CsRgsWorkflow

8.  <span data-ttu-id="da673-162">Verifique se todos os fluxos de trabalho no ambiente do Lync Server 2010 estão incluídos na lista.</span><span class="sxs-lookup"><span data-stu-id="da673-162">Verify that all the workflows in your Lync Server 2010 environment are included in the list.</span></span>

<span data-ttu-id="da673-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="da673-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

