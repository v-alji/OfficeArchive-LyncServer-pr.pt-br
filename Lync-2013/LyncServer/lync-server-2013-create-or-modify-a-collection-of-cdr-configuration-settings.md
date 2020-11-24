---
title: 'Lync Server 2013: criar ou modificar uma coleção de definições de configuração de CDR'
description: 'Lync Server 2013: crie ou modifique um conjunto de configurações de configuração de CDR.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a collection of CDR configuration settings
ms:assetid: c830be5a-2a82-468d-9c46-d3fec0f79fd0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721878(v=OCS.15)
ms:contentKeyID: 49733812
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3ba911607db55a7b7206645495e70a27ed453784
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390172"
---
# <a name="create-or-modify-a-collection-of-cdr-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="9a7e9-103">Criar ou modificar uma coleção de definições de configuração de CDR no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a7e9-103">Create or modify a collection of CDR configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a7e9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a7e9-104">

<span> </span></span></span>

<span data-ttu-id="9a7e9-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="9a7e9-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="9a7e9-p101">O registro de detalhes das chamadas (CDR) permite rastrear o uso de coisas como sessões de mensagens instantâneas ponto a ponto, telefonemas de protocolo VoIP (voz sobre Internet) e chamadas em conferência. Esses dados de uso incluem informações sobre quem ligou para quem, quando a ligação foi feita e quanto tempo durou a conversa.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-p101">Call detail recording (CDR) enables you to track usage of such things as peer-to-peer instant messaging sessions, Voice over Internet Protocol (VoIP) phone calls, and conferencing calls. This usage data includes information about who called whom, when they called, and how long they talked.</span></span>

<span data-ttu-id="9a7e9-108">Ao instalar o Microsoft Lync Server 2013, uma única coleção global de definições de configuração de CDR é criada para você.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-108">When you install Microsoft Lync Server 2013 a single, global collection of CDR configuration settings is created for you.</span></span> <span data-ttu-id="9a7e9-109">Os administradores também podem ter a opção de criar configurações personalizadas no escopo local.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-109">Administrators also have the option of creating custom settings at the site scope.</span></span> <span data-ttu-id="9a7e9-110">Sempre que essas configurações de escopo local forem usadas, elas terão precedência sobre as configurações globais.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-110">Whenever these site-scoped settings are used, they take precedence over the global settings.</span></span> <span data-ttu-id="9a7e9-111">Por exemplo, se você criar configurações de escopo local para o local Redmond, essas configurações (e não as configurações globais) serão usadas para gerenciar CDR em Redmond.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-111">For example, if you create site-scoped settings for the Redmond site then those settings (rather than the global settings) will be used to manage CDR in Redmond.</span></span>

<span data-ttu-id="9a7e9-112">Você pode criar definições de configuração de CDR usando o painel de controle do Lync Server ou o cmdlet [New-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="9a7e9-112">You can create CDR configuration settings by using either Lync Server Control Panel or the [New-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration) cmdlet.</span></span> <span data-ttu-id="9a7e9-113">Você pode usar o painel de controle do Lync Server ou o cmdlet [set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) para modificar as configurações existentes.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-113">You can use Lync Server Control Panel or the [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) cmdlet to modify existing settings.</span></span> <span data-ttu-id="9a7e9-114">Se você estiver usando o painel de controle do Lync Server para criar ou modificar as configurações, as seguintes opções estarão disponíveis para você:</span><span class="sxs-lookup"><span data-stu-id="9a7e9-114">If you are using Lync Server Control Panel to create or modify settings, the following options will be available to you:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a7e9-115">Configuração de UI</span><span class="sxs-lookup"><span data-stu-id="9a7e9-115">UI Setting</span></span></th>
<th><span data-ttu-id="9a7e9-116">Parâmetro do PowerShell</span><span class="sxs-lookup"><span data-stu-id="9a7e9-116">PowerShell Parameter</span></span></th>
<th><span data-ttu-id="9a7e9-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a7e9-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a7e9-118">Nome</span><span class="sxs-lookup"><span data-stu-id="9a7e9-118">Name</span></span></p></td>
<td><p><span data-ttu-id="9a7e9-119">Identidade</span><span class="sxs-lookup"><span data-stu-id="9a7e9-119">Identity</span></span></p></td>
<td><p><span data-ttu-id="9a7e9-p104">Identificador exclusivo das definições de configuração CDR sendo criada. Estas configurações podem ser criadas apenas no escopo local.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-p104">Unique identifier for the CDR configuration settings being created. These settings can only be created at the site scope.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a7e9-122">Habilitar monitoramento de CDRs</span><span class="sxs-lookup"><span data-stu-id="9a7e9-122">Enable monitoring of CDRs</span></span></p></td>
<td><p><span data-ttu-id="9a7e9-123">EnableCDR</span><span class="sxs-lookup"><span data-stu-id="9a7e9-123">EnableCDR</span></span></p></td>
<td><p><span data-ttu-id="9a7e9-124">Indica se o CDR está habilitado ou não.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-124">Indicates whether or not CDR is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a7e9-125">Habilitar exclusão de CDRs</span><span class="sxs-lookup"><span data-stu-id="9a7e9-125">Enable purging of CDRs</span></span></p></td>
<td><p><span data-ttu-id="9a7e9-126">EnablePurging</span><span class="sxs-lookup"><span data-stu-id="9a7e9-126">EnablePurging</span></span></p></td>
<td><p><span data-ttu-id="9a7e9-127">Indica se os registros do CDR serão excluídos periodicamente ou não do banco de dados do CDR.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-127">Indicates whether or not CDR records will periodically be deleted from the CDR database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a7e9-128">Manter CDRs pela duração máxima (dias)</span><span class="sxs-lookup"><span data-stu-id="9a7e9-128">Keep CDRs for maximum duration (days)</span></span></p></td>
<td><p><span data-ttu-id="9a7e9-129">KeepCallDetailForDays</span><span class="sxs-lookup"><span data-stu-id="9a7e9-129">KeepCallDetailForDays</span></span></p></td>
<td><p><span data-ttu-id="9a7e9-p105">Indica o número de dias que os registros CDR serão mantidos no banco de dados de CDR. Qualquer registro anterior ao número de dias especificado será automaticamente excluído. (Observe que excluir ocorrerá apenas se a exclusão tiver habilitada.)</span><span class="sxs-lookup"><span data-stu-id="9a7e9-p105">Indicates the number of days that CDR records will be kept in the CDR database. Any records older than the specified number of days will automatically be deleted. (Note that purging will take only place if purging has been enabled.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a7e9-133">Manter os dados do relatório de erro pela duração máxima (dias)</span><span class="sxs-lookup"><span data-stu-id="9a7e9-133">Keep error report data for maximum duration (days)</span></span></p></td>
<td><p><span data-ttu-id="9a7e9-134">KeepErrorReportForDays</span><span class="sxs-lookup"><span data-stu-id="9a7e9-134">KeepErrorReportForDays</span></span></p></td>
<td><p><span data-ttu-id="9a7e9-p106">Indica o número de dias que os relatórios de erros do CDR são mantidos. Qualquer relatório mais antigo do que o número de dias especificado será automaticamente excluído. Os relatórios de erros do CDR são relatórios de diagnósticos carregados por aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-p106">Indicates the number of days that CDR error reports are kept. Any reports older than the specified number of days will automatically be deleted. CDR error reports are diagnostic reports uploaded by client applications.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="9a7e9-138">Os cmdlets New-CsCdrConfiguration e Set-CsCdrConfiguration incluem opções adicionais não disponíveis no painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-138">The New-CsCdrConfiguration and Set-CsCdrConfiguration cmdlets include additional options not available in Lync Server Control Panel.</span></span> <span data-ttu-id="9a7e9-139">Consulte os tópicos de ajuda <A href="https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration">New-CsCdrConfiguration</A> e <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration">set-CsCdrConfiguration</A> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-139">See the <A href="https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration">New-CsCdrConfiguration</A> and the <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration">Set-CsCdrConfiguration</A> help topics for more information.</span></span>



</div>

<div>

## <a name="to-create-cdr-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="9a7e9-140">Para criar definições de configuração de CDR usando o painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="9a7e9-140">To create CDR configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="9a7e9-141">No painel de controle do Lync Server, clique em **monitoramento e arquivamento**.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-141">In Lync Server Control Panel click **Monitoring and Archiving**.</span></span>

2.  <span data-ttu-id="9a7e9-142">Na guia **gravação de detalhes da chamada** , clique em **novo**.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-142">On the **Call Detail Recording** tab, click **New**.</span></span>

3.  <span data-ttu-id="9a7e9-p108">Na caixa de diálogo **Selecionar um local**, selecione o local onde as novas definições de configuração devem ser criadas. Se a caixa de diálogo estiver vazia, isso significa que a todos os seus locais já foi atribuído um conjunto de definições de configuração do CDR. Cada local é limitado a um único conjunto. Nesse caso, é possível excluir e recriar as configurações ou apenas modificar as configurações existentes.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-p108">In the **Select a Site** dialog box, select the site where the new configuration settings are to be created. If the dialog box is empty, that means all of your sites have already been assigned a collection of CDR configuration settings. Each site is limited to a single such collection. In that case you can either delete and then re-create the settings, or simply modify the existing settings.</span></span>

4.  <span data-ttu-id="9a7e9-147">Na caixa de diálogo **Nova configuração do Registro de detalhes das chamadas (CDR)**, faça as seleções desejadas e clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-147">In the **New Call Detail Recording (CDR) Setting** dialog, make the desired selections and then click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-existing-cdr-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="9a7e9-148">Para modificar as definições de configuração de CDR existentes usando o painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="9a7e9-148">To modify existing CDR configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="9a7e9-149">No painel de controle do Lync Server, clique em **monitoramento e arquivamento**.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-149">In Lync Server Control Panel click **Monitoring and Archiving**.</span></span>

2.  <span data-ttu-id="9a7e9-150">Clique duas vezes no conjunto de configurações a ser modificado ou selecione o conjunto e, em seguida, clique em **Editar** e em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-150">Double-click the collection of settings to be modified, or select the collection, click **Edit**, and then click **Show Details**.</span></span> <span data-ttu-id="9a7e9-151">Observe que você pode apenas modificar um único conjunto por vez.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-151">Note that you can only modify a single collection at a time.</span></span> <span data-ttu-id="9a7e9-152">Para fazer as mesmas alterações em várias coleções, use o Shell de gerenciamento do Lync Server em vez disso.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-152">To make the same changes to multiple collections, use the Lync Server Management Shell instead.</span></span>

3.  <span data-ttu-id="9a7e9-153">Na caixa de diálogo **Editar configurações de Registro de detalhes das chamadas (CDR)**, faça as seleções desejadas e clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-153">In the **Edit Call Detail Recording (CDR) Setting** dialog, make the desired selections and then click **Commit**.</span></span>

</div>

<div>

## <a name="creating-cdr-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="9a7e9-154">Como criar definições de configuração de CDR usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9a7e9-154">Creating CDR Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="9a7e9-155">Você pode criar definições de configuração de CDR também podem ser criadas usando o Windows PowerShell e o cmdlet **New-CsCdrConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="9a7e9-155">You can create CDR configuration settings can also be created by using Windows PowerShell and the **New-CsCdrConfiguration** cmdlet.</span></span> <span data-ttu-id="9a7e9-156">Você pode executar esse cmdlet a partir do Shell de gerenciamento do Lync Server 2013 ou de uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9a7e9-156">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="9a7e9-157">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="9a7e9-157">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-new-collection-of-cdr-configuration-settings"></a><span data-ttu-id="9a7e9-158">Para criar um novo conjunto de definições de configuração de CDR</span><span class="sxs-lookup"><span data-stu-id="9a7e9-158">To create a new collection of CDR configuration settings</span></span>

  - <span data-ttu-id="9a7e9-159">Este comando cria um novo conjunto de definições de configuração de CDR aplicadas ao local Redmond:</span><span class="sxs-lookup"><span data-stu-id="9a7e9-159">This command creates a new collection of CDR configuration settings applied to the Redmond site:</span></span>
    
        New-CsCdrConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-collection-of-cdr-configuration-settings-that-disable-call-detail-recording"></a><span data-ttu-id="9a7e9-160">Para criar um conjunto de definições de configuração de CDR que desabilitam o registro de detalhes das chamadas</span><span class="sxs-lookup"><span data-stu-id="9a7e9-160">To create a collection of CDR configuration settings that disable call detail recording</span></span>

  - <span data-ttu-id="9a7e9-p111">Como nenhum parâmetro (além do parâmetro obrigatório Identity) foi especificado no comando precedente, o novo conjunto de definições de configurações usará os valores padrão para todas as suas propriedades. Para criar configurações que usam valores de propriedade diferentes, basta incluir o parâmetro e o valor de parâmetro adequados. Por exemplo, para criar um conjunto de definições de configuração de Detalhes das Chamadas que, por padrão, permite desabilitar o registro de Detalhes das Chamadas, use um comando como este:</span><span class="sxs-lookup"><span data-stu-id="9a7e9-p111">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding command, the new collection of configuration settings will use the default values for all its properties. To create settings that use different property values, simply include the appropriate parameter and parameter value. For example, to create a collection of Call Detail configuration settings that, by default, allow disable Call Detail recording use a command like this:</span></span>
    
        New-CsCdrConfiguration -Identity "site:Redmond" -EnableCDR $False

</div>

<div>

## <a name="to-specify-multiple-property-values-when-creating-a-new-collection-of-cdr-configuration-settings"></a><span data-ttu-id="9a7e9-164">Para especificar vários valores de propriedade ao criar um novo conjunto de definições de configuração de CDR</span><span class="sxs-lookup"><span data-stu-id="9a7e9-164">To specify multiple property values when creating a new collection of CDR configuration settings</span></span>

  - <span data-ttu-id="9a7e9-p112">É possível modificar vários valores de propriedade incluindo vários parâmetros. Por exemplo, este comando define as novas configurações para manter registros de Detalhes das Chamadas por 30 dias e relatórios de erro por 90 dias:</span><span class="sxs-lookup"><span data-stu-id="9a7e9-p112">You can modify multiple property values by including multiple parameters. For example, this command configures the new settings to keep Call Detail records for 30 days and error reports for 90 days:</span></span>
    
        New-CsCdrConfiguration -Identity "site:Redmond" -KeepCallDetailForDays 30 -KeepErrorReportForDays 90

</div>

<span data-ttu-id="9a7e9-167">Para obter mais informações, consulte o tópico da ajuda para o cmdlet [New-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="9a7e9-167">For more information, see the help topic for the [New-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration) cmdlet.</span></span>

<span data-ttu-id="9a7e9-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a7e9-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

