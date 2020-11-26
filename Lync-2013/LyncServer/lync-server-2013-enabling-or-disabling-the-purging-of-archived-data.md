---
title: 'Lync Server 2013: habilitando ou desabilitando a limpeza de dados arquivados'
description: 'Lync Server 2013: habilitando ou desabilitando a limpeza de dados arquivados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling or disabling the purging of archived data
ms:assetid: 28cef09f-0970-4fc3-8315-f26689e3e187
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520968(v=OCS.15)
ms:contentKeyID: 48183678
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 442b99e2cfa6db303ca8edd216cbdf3b5c13cea9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428745"
---
# <a name="enabling-or-disabling-the-purging-of-archived-data-in-lync-server-2013"></a><span data-ttu-id="a4cd9-103">Habilitar ou desabilitar a limpeza de dados arquivados no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4cd9-103">Enabling or disabling the purging of archived data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a4cd9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a4cd9-104">

<span> </span></span></span>

<span data-ttu-id="a4cd9-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="a4cd9-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="a4cd9-106">No painel de controle do Lync Server 2013, você usa configurações de arquivamento para habilitar e desabilitar a limpeza e configurar como a limpeza é implementada.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-106">In Lync Server 2013 Control Panel, you use Archiving configurations to enable and disable purging and configure how purging is implemented.</span></span> <span data-ttu-id="a4cd9-107">Isso inclui as seguintes configurações de arquivamento:</span><span class="sxs-lookup"><span data-stu-id="a4cd9-107">This includes the following Archiving configurations:</span></span>

  - <span data-ttu-id="a4cd9-108">Uma configuração global criada por padrão quando você implanta o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-108">A global configuration that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="a4cd9-109">Configurações opcionais de nível de site e de pool que você pode criar e usar para especificar como o arquivamento é implementado para sites ou pools específicos.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-109">Optional site-level and pool-level configurations that you can create and use to specify how archiving is implemented for specific sites or pools.</span></span>

<span data-ttu-id="a4cd9-110">Inicialmente, você define o arquivamento de configurações ao implantar o arquivamento, mas pode alterar, adicionar e excluir configurações após a implantação.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-110">You initially set up Archiving configurations when you deploy Archiving, but you can change, add, and delete configurations after deployment.</span></span> <span data-ttu-id="a4cd9-111">Para obter detalhes sobre como as configurações de arquivamento são implementadas, incluindo quais opções você pode especificar e a hierarquia de configurações de arquivamento, consulte [como o arquivamento funciona no Lync Server 2013](lync-server-2013-how-archiving-works.md) na documentação de planejamento, documentação de implantação ou documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-111">For details about how Archiving configurations are implemented, including which options you can specify and the hierarchy of Archiving configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a4cd9-112">Para usar o arquivamento para usuários que são hospedados no Lync Server 2013, configure as políticas de arquivamento para especificar se o arquivamento deve ser habilitado para comunicações internas, para comunicações externas ou para ambos.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-112">To use archiving for users who are homed on Lync Server 2013 you must configure Archiving policies to specify whether to enable archiving for internal communications, for external communications, or for both.</span></span> <span data-ttu-id="a4cd9-113">Por padrão, o arquivamento não está habilitado para comunicações internas ou externas.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-113">By default, archiving is not enabled for either internal or external communications.</span></span> <span data-ttu-id="a4cd9-114">Antes de habilitar o arquivamento em qualquer política, você deve especificar as configurações de arquivamento adequadas para sua implantação e, opcionalmente, para sites e pools específicos, conforme descrito nesta seção.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-114">Prior to enabling Archiving in any policies, you should specify the appropriate Archiving configurations for your deployment and, optionally, for specific sites and pools, as described in this section.</span></span> <span data-ttu-id="a4cd9-115">Para obter detalhes sobre como habilitar o arquivamento, consulte <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">configurar e atribuir políticas de arquivamento no Lync Server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-115">For details about enabling Archiving, see <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Configuring and assigning Archiving policies in Lync Server 2013</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="a4cd9-116">Se você decidir após implantar o arquivamento em que deseja usar a integração do Microsoft Exchange para armazenar arquivos de arquivamento e arquivos nos servidores Exchange 2013 e todos os usuários estiverem hospedados em seus servidores Exchange 2013, você deve remover a configuração de banco de dados do SQL Server da sua topologia.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-116">If you decide after you deploy Archiving that you want to use Microsoft Exchange integration to store archiving data and files on Exchange 2013 servers and all your users are homed on your Exchange 2013 servers, you should remove the SQL Server database configuration from your topology.</span></span> <span data-ttu-id="a4cd9-117">Você deve usar o construtor de topologias para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-117">You must use Topology Builder to do this.</span></span> <span data-ttu-id="a4cd9-118">Para obter detalhes, consulte <A href="lync-server-2013-changing-archiving-database-options.md">alterando as opções de arquivamento de banco de dados no Lync Server 2013</A> na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-118">For details, see <A href="lync-server-2013-changing-archiving-database-options.md">Changing Archiving database options in Lync Server 2013</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="to-enable-or-disable-purging-for-archiving"></a><span data-ttu-id="a4cd9-119">Para habilitar ou desabilitar a limpeza para arquivamento</span><span class="sxs-lookup"><span data-stu-id="a4cd9-119">To enable or disable purging for archiving</span></span>

1.  <span data-ttu-id="a4cd9-120">Usando uma conta de usuário atribuída à função CsArchivingAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-120">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="a4cd9-121">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-121">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a4cd9-122">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a4cd9-122">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a4cd9-123">Na barra de navegação da esquerda, clique em **Monitoramento e Arquivamento**, e depois, clique em **Configuração de Arquivamento**.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-123">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="a4cd9-124">Clique no nome da configuração apropriada de pool, site ou global na lista de configurações de arquivamento, clique em **Editar**, **Mostrar detalhes** e faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a4cd9-124">Click the name of the appropriate global, site, or pool configuration in the list of archiving configurations, click **Edit**, click **Show details**, and then do the following:</span></span>
    
      - <span data-ttu-id="a4cd9-125">Para habilitar a limpeza, marque a caixa de seleção **Habilitar limpeza de dados de arquivamento** e execute uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="a4cd9-125">To enable purging, select the **Enable purging of archiving data** check box and then do one of the following:</span></span>
        
          - <span data-ttu-id="a4cd9-126">Para limpar todos os registros, clique em **Limpar dados de arquivamento exportados e armazenados após um período máximo de (dias)** e especifique o número de dias.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-126">To purge all records, click the **Purge exported archiving data and stored archiving data after maximum duration (days)**, and then specify the number of days.</span></span>
        
          - <span data-ttu-id="a4cd9-127">Para limpar somente os dados exportados, clique em **Limpar somente dados de arquivamento exportados**.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-127">To purge only the data that has been exported, click **Purge exported archiving data only**.</span></span>
    
      - <span data-ttu-id="a4cd9-128">Para desabilitar a limpeza, desmarque a caixa de seleção **Habilitar limpeza de dados de arquivamento**.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-128">To disable purging, clear the **Enable purging of archiving data** check box.</span></span>

5.  <span data-ttu-id="a4cd9-129">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-129">Click **Commit**.</span></span>

</div>

<div>

## <a name="enabling-or-disabling-the-purging-of-archiving-data-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="a4cd9-130">Habilitar ou desabilitar o descarte do arquivamento de dados usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a4cd9-130">Enabling or Disabling the Purging of Archiving Data by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="a4cd9-131">Habilitar e desabilitar a limpeza automática de dados de arquivamento pode ser gerenciado usando o Windows PowerShell e o cmdlet **set-CsArchivingConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="a4cd9-131">Enabling and disabling the automated purging of archiving data can be managed by using Windows PowerShell and the **Set-CsArchivingConfiguration** cmdlet.</span></span> <span data-ttu-id="a4cd9-132">Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a4cd9-132">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="a4cd9-133">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="a4cd9-133">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-the-purging-of-all-archiving-data"></a><span data-ttu-id="a4cd9-134">Para habilitar a remoção de todos os dados de arquivamento</span><span class="sxs-lookup"><span data-stu-id="a4cd9-134">To enable the purging of all archiving data</span></span>

  - <span data-ttu-id="a4cd9-135">Para habilitar a remoção de todos os dados de arquivamento defina a propriedade **EnablePurging** como true ($true).</span><span class="sxs-lookup"><span data-stu-id="a4cd9-135">To enable the purging of all archiving data set the **EnablePurging** property to true ($True).</span></span> <span data-ttu-id="a4cd9-136">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a4cd9-136">For example:</span></span>
    
        Set-CsArchivingConfiguration -Identity "site:Redmond" -EnablePurging $True
    
    <span data-ttu-id="a4cd9-137">Depois que esse comando for executado, cada dia do Lync Server limpará todos os registros de arquivamento anteriores ao valor especificado para a propriedade **KeepArchivingDataForDays** .</span><span class="sxs-lookup"><span data-stu-id="a4cd9-137">After this command is run, then every day Lync Server will purge all archiving records older than the value specified for the **KeepArchivingDataForDays** property.</span></span>

</div>

<div>

## <a name="to-enable-the-purging-only-of-exported-archiving-data"></a><span data-ttu-id="a4cd9-138">Para habilitar a limpeza apenas dos dados de arquivamento exportados</span><span class="sxs-lookup"><span data-stu-id="a4cd9-138">To enable the purging only of exported archiving data</span></span>

  - <span data-ttu-id="a4cd9-139">Para limitar a limpeza para arquivar registros que foram exportados para um arquivo de dados (usando o cmdlet [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) ), você também deve definir a propriedade PurgeExportedArchivesOnly como True ($true).</span><span class="sxs-lookup"><span data-stu-id="a4cd9-139">To limit purging to archiving records that have been exported to a data file (by using the [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) cmdlet) you must also set the PurgeExportedArchivesOnly property to True ($True).</span></span> <span data-ttu-id="a4cd9-140">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a4cd9-140">For example:</span></span>
    
        Set-CsArchivingConfiguration -Identity "site:Redmond" -EnablePurging $True -PurgeExportedArchivesOnly $True
    
    <span data-ttu-id="a4cd9-141">Depois que esse comando for executado, o Lync Server somente limpará o arquivamento de registros que atendam a dois critérios: 1) eles são mais antigos do que o valor especificado para a propriedade **KeepArchivingDataForDays** ; e 2) eles foram exportados usando o cmdlet **Export-CsArchivingData** .</span><span class="sxs-lookup"><span data-stu-id="a4cd9-141">After this command is run, Lync Server will only purge archiving records that meet two criteria: 1) they are older than the value specified for the **KeepArchivingDataForDays** property; and, 2) they have been exported by using the **Export-CsArchivingData** cmdlet.</span></span>

</div>

<div>

## <a name="to-disable-the-purging-of-all-archiving-data"></a><span data-ttu-id="a4cd9-142">Para desativar a remoção de todos os dados de arquivamento</span><span class="sxs-lookup"><span data-stu-id="a4cd9-142">To disable the purging of all archiving data</span></span>

  - <span data-ttu-id="a4cd9-143">Para desabilitar a limpeza automatizada de registros de arquivamento, defina a propriedade **EnablePurging** como False ($false).</span><span class="sxs-lookup"><span data-stu-id="a4cd9-143">To disable the automated purging of archiving records, set the **EnablePurging** property to False ($False).</span></span> <span data-ttu-id="a4cd9-144">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a4cd9-144">For example:</span></span>
    
        Set-CsArchivingConfiguration -Identity "site:Redmond" -EnablePurging $False

</div>

<span data-ttu-id="a4cd9-145">Para obter mais informações, incluindo opções adicionais para limpar dados de arquivamento, consulte o tópico da ajuda para o cmdlet [set-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="a4cd9-145">For more information, including additional options for purging archiving data, see the help topic for the [Set-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a4cd9-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4cd9-146">See Also</span></span>


[<span data-ttu-id="a4cd9-147">Como o arquivamento funciona no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4cd9-147">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)  


[<span data-ttu-id="a4cd9-148">Configurar e atribuir políticas de arquivamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4cd9-148">Configuring and assigning Archiving policies in Lync Server 2013</span></span>](lync-server-2013-configuring-and-assigning-archiving-policies.md)  
[<span data-ttu-id="a4cd9-149">Gerenciando opções de configuração de arquivamento no Lync Server 2013 para sua organização, sites e pools</span><span class="sxs-lookup"><span data-stu-id="a4cd9-149">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</span></span>](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md)  
  

<span data-ttu-id="a4cd9-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a4cd9-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

