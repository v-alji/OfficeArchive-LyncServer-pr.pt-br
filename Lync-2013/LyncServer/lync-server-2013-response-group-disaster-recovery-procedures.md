---
title: 'Lync Server 2013: Procedimento de recuperação de desastre do grupo de resposta'
description: Lync Server 2013 procedimentos de recuperação de desastres do grupo de resposta.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Response group disaster recovery procedures
ms:assetid: b49577b7-0ca3-4f20-b614-f3a2a0046b58
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205186(v=OCS.15)
ms:contentKeyID: 48185171
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9021fb75c8f937bfd298578a9241d6256d26d85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436297"
---
# <a name="response-group-disaster-recovery-procedures-in-lync-server-2013"></a><span data-ttu-id="d6179-103">Procedimento de recuperação de desastre do grupo de resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6179-103">Response group disaster recovery procedures in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d6179-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d6179-104">

<span> </span></span></span>

<span data-ttu-id="d6179-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="d6179-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="d6179-106">Durante a fase de failover da recuperação de desastres, os grupos de resposta residem em vários pools: no pool primário (que não está disponível) e no pool de backup.</span><span class="sxs-lookup"><span data-stu-id="d6179-106">During the failover phase of disaster recovery, the response groups reside in multiple pools: in the primary pool (which is unavailable) and in the backup pool.</span></span> <span data-ttu-id="d6179-107">Os grupos de resposta em ambos os pools têm o mesmo nome e o mesmo proprietário (o pool primário), mas têm pais diferentes.</span><span class="sxs-lookup"><span data-stu-id="d6179-107">The response groups in both pools have the same name and the same owner (the primary pool), but they have different parents.</span></span> <span data-ttu-id="d6179-108">Durante esse tempo, os cmdlets do grupo de resposta funcionam de maneira um pouco diferente.</span><span class="sxs-lookup"><span data-stu-id="d6179-108">During this time, Response Group cmdlets work a little differently.</span></span> <span data-ttu-id="d6179-109">Certifique-se de usar parâmetros conforme especificado no procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6179-109">Be sure to use parameters as specified in the following procedure.</span></span> <span data-ttu-id="d6179-110">Para obter detalhes sobre como os cmdlets funcionam durante a fase de failover, consulte artigo do blog NextHop "Lync Server 2013: Recuperando grupos de respostas durante a recuperação de desastres" em [https://go.microsoft.com/fwlink/p/?LinkId=263957](https://go.microsoft.com/fwlink/p/?linkid=263957) .</span><span class="sxs-lookup"><span data-stu-id="d6179-110">For details about how cmdlets work during the failover phase, see NextHop blog article "Lync Server 2013: Recovering Response Groups During Disaster Recovery" at [https://go.microsoft.com/fwlink/p/?LinkId=263957](https://go.microsoft.com/fwlink/p/?linkid=263957).</span></span> <span data-ttu-id="d6179-111">Este artigo de blog também se aplica à versão de lançamento do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d6179-111">This blog article also applies to the released version of Lync Server 2013.</span></span>

<span data-ttu-id="d6179-112">Use as etapas do procedimento a seguir para se preparar e executar a recuperação de desastres para o serviço do grupo de resposta do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d6179-112">Use the steps in the following procedure to prepare for and perform disaster recovery for Lync Server Response Group service.</span></span>

<div>

## <a name="to-fail-over-and-fail-back-response-group"></a><span data-ttu-id="d6179-113">Para fazer failover e failback do grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="d6179-113">To fail over and fail back Response Group</span></span>

1.  <span data-ttu-id="d6179-114">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="d6179-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="d6179-115">Fazer backups rotineiramente.</span><span class="sxs-lookup"><span data-stu-id="d6179-115">Routinely perform backups.</span></span> <span data-ttu-id="d6179-116">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-116">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<primary pool FQDN>" -FileName "<backup path and file name>"
    
    <span data-ttu-id="d6179-117">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-117">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:primary.contoso.com" -FileName "C:\RgsExportPrimary.zip"

3.  <span data-ttu-id="d6179-118">Durante uma interrupção, após o failover do pool de backup, importe os grupos de resposta para o pool de backup.</span><span class="sxs-lookup"><span data-stu-id="d6179-118">During an outage, after failover to the backup pool, import the response groups to the backup pool.</span></span> <span data-ttu-id="d6179-119">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-119">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<backup pool FQDN>" -FileName "<backup path and file name>"
    
    <span data-ttu-id="d6179-120">Se você quiser substituir as configurações no nível do aplicativo no pool de backup pelas configurações do pool primário, inclua o parâmetro – ReplaceExistingSettings.</span><span class="sxs-lookup"><span data-stu-id="d6179-120">If you want to replace the application-level settings in the backup pool with the settings from the primary pool, include the –ReplaceExistingSettings parameter.</span></span> <span data-ttu-id="d6179-121">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-121">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:backup.contoso.com" -FileName "C:\RgsExportPrimary.zip" -ReplaceExistingSettings
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="d6179-122">Se você não substituir as configurações no pool de backup e o pool primário não puder ser recuperado, as configurações do pool primário serão perdidas.</span><span class="sxs-lookup"><span data-stu-id="d6179-122">If you do not replace the settings in the backup pool and the primary pool can't be recovered, the primary pool settings will be lost.</span></span> <span data-ttu-id="d6179-123">Para obter detalhes, consulte <A href="lync-server-2013-planning-for-response-group-disaster-recovery.md">planejando a recuperação de desastres do grupo de resposta no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="d6179-123">For details, see <A href="lync-server-2013-planning-for-response-group-disaster-recovery.md">Planning for response group disaster recovery in Lync Server 2013</A>.</span></span>

    
    </div>

4.  <span data-ttu-id="d6179-124">Verifique se a importação foi bem-sucedida exibindo os grupos de resposta importados.</span><span class="sxs-lookup"><span data-stu-id="d6179-124">Verify that the import was successful by displaying the imported response groups.</span></span> <span data-ttu-id="d6179-125">Os grupos de resposta importados ainda são pertencentes ao pool primário.</span><span class="sxs-lookup"><span data-stu-id="d6179-125">The imported response groups are still owned by the primary pool.</span></span> <span data-ttu-id="d6179-126">Siga este procedimento:</span><span class="sxs-lookup"><span data-stu-id="d6179-126">Do the following:</span></span>
    
      - <span data-ttu-id="d6179-127">Exiba todos os fluxos de trabalho do pool de backup que pertencem ao pool primário e verifique se todos os fluxos de trabalho do pool primário estão incluídos.</span><span class="sxs-lookup"><span data-stu-id="d6179-127">Display all the workflows in the backup pool that are owned by the primary pool, and verify that all the primary pool workflows are included.</span></span> <span data-ttu-id="d6179-128">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-128">At the command line, type:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="d6179-129">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-129">For example:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer:primary.contoso.com"
    
      - <span data-ttu-id="d6179-130">Exiba todas as filas do pool de backup que são Propriedade do pool primário e verifique se todas as filas do pool primário estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="d6179-130">Display all the queues in the backup pool that are owned by the primary pool, and verify that all the primary pool queues are included.</span></span> <span data-ttu-id="d6179-131">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-131">At the command line, type:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="d6179-132">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-132">For example:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
      - <span data-ttu-id="d6179-133">Exiba todos os grupos de agente no pool de backup que pertencem ao pool primário e verifique se todos os grupos de agente de pool primário estão incluídos.</span><span class="sxs-lookup"><span data-stu-id="d6179-133">Display all the agent groups in the backup pool that are owned by the primary pool, and verify that all the primary pool agent groups are included.</span></span> <span data-ttu-id="d6179-134">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-134">At the command line, type:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="d6179-135">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-135">For example:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
      - <span data-ttu-id="d6179-136">Exiba todas as horas de negócios no pool de backup que são Propriedade do pool primário e verifique se todas as horas de trabalho do pool primário estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="d6179-136">Display all the hours of business in the backup pool that are owned by the primary pool, and verify that all the primary pool hours of business are included.</span></span> <span data-ttu-id="d6179-137">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-137">At the command line, type:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="d6179-138">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-138">For example:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
      - <span data-ttu-id="d6179-139">Exiba todos os conjuntos de feriados no pool de backup que pertencem ao pool primário e verifique se todos os conjuntos de feriados do pool primário estão incluídos.</span><span class="sxs-lookup"><span data-stu-id="d6179-139">Display all the holiday sets in the backup pool that are owned by the primary pool, and verify that all the primary pool holiday sets are included.</span></span> <span data-ttu-id="d6179-140">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-140">At the command line, type:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="d6179-141">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-141">For example:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
    <span data-ttu-id="d6179-142">Como alternativa, você pode exibir todos os grupos de resposta no pool de backup, incluindo aqueles pertencentes ao pool primário e àqueles pertencentes ao pool de backup usando o parâmetro – ShowAll em vez do parâmetro – Owner.</span><span class="sxs-lookup"><span data-stu-id="d6179-142">Alternatively, you can display all the response groups in the backup pool, including the ones owned by the primary pool and the ones owned by the backup pool by using the –ShowAll parameter instead of the –Owner parameter.</span></span> <span data-ttu-id="d6179-143">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-143">For example:</span></span>
    
        Get-CsRgsWorkflow -Identity "service:ApplicationServer:<backup pool FQDN>" -ShowAll
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="d6179-144">Você deve usar o parâmetro – ShowAll ou o parâmetro – Owner.</span><span class="sxs-lookup"><span data-stu-id="d6179-144">You must use either the –ShowAll parameter or the –Owner parameter.</span></span> <span data-ttu-id="d6179-145">Se você não usar nenhum desses parâmetros, os grupos de resposta que você importou para o pool de backup não serão listados nos resultados retornados pelos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d6179-145">If you do not use either of these parameters, the response groups that you imported to the backup pool will not be listed in the results returned by the cmdlets.</span></span>

    
    </div>

5.  <span data-ttu-id="d6179-146">Verifique se a importação foi bem-sucedida fazendo uma chamada para um grupo de resposta importada e verificando se a chamada foi manipulada corretamente.</span><span class="sxs-lookup"><span data-stu-id="d6179-146">Verify that the import was successful by placing a call to an imported response group and verifying that the call is handled correctly.</span></span>

6.  <span data-ttu-id="d6179-147">Solicite aos agentes que são membros de grupos de agentes formais para entrar em seus grupos de agente no pool de backup.</span><span class="sxs-lookup"><span data-stu-id="d6179-147">Request agents who are members of formal agent groups to sign in to their agent groups in the backup pool.</span></span>

7.  <span data-ttu-id="d6179-148">Gerencie e modifique os grupos de resposta importados normalmente.</span><span class="sxs-lookup"><span data-stu-id="d6179-148">Manage and modify the imported response groups as usual.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="d6179-149">Enquanto os grupos de resposta estiverem no pool de backup, você precisará usar o Shell de gerenciamento do Lync Server para gerenciá-los.</span><span class="sxs-lookup"><span data-stu-id="d6179-149">While the response groups are in the backup pool, you need to use Lync Server Management Shell to manage them.</span></span> <span data-ttu-id="d6179-150">Você não pode usar o painel de controle do Lync Server para gerenciar os grupos de resposta importados para o pool de backup.</span><span class="sxs-lookup"><span data-stu-id="d6179-150">You cannot use Lync Server Control Panel to manage the response groups that you imported to the backup pool.</span></span>

    
    </div>

8.  <span data-ttu-id="d6179-151">Depois que o pool primário for restaurado e o failback estiver concluído, exporte os grupos de resposta de pool primário que foram importados para o pool de backup.</span><span class="sxs-lookup"><span data-stu-id="d6179-151">After the primary pool is restored and failback is complete, export the primary pool response groups that were imported to the backup pool.</span></span> <span data-ttu-id="d6179-152">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-152">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source ApplicationServer:<backup pool FQDN> -Owner ApplicationServer:<primary pool FQDN> -FileName "<backup path and file name>"

9.  <span data-ttu-id="d6179-153">Importe os grupos de resposta de volta para o pool primário.</span><span class="sxs-lookup"><span data-stu-id="d6179-153">Import the response groups back to the primary pool.</span></span> <span data-ttu-id="d6179-154">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-154">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<primary pool FQDN>" -OverwriteOwner -FileName "<exported path and file name>"
    
    <span data-ttu-id="d6179-155">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-155">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:primary.contoso.com" -OverwriteOwner -FileName "C:\RgsExportPrimaryUpdated.zip"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d6179-156">Se você recriar um pool durante a recuperação, seja com o mesmo ou um nome de domínio totalmente qualificado (FQDN) diferente, será necessário usar o parâmetro – OverwriteOwner.</span><span class="sxs-lookup"><span data-stu-id="d6179-156">If you rebuild a pool during recovery, whether with the same or a different fully qualified domain name (FQDN), you need to use the –OverwriteOwner parameter.</span></span> <span data-ttu-id="d6179-157">Como regra geral, você sempre pode usar o parâmetro – OverwriteOwner ao importar grupos de resposta de volta para o pool primário.</span><span class="sxs-lookup"><span data-stu-id="d6179-157">As a rule of thumb, you can always use the –OverwriteOwner parameter when you import response groups back to the primary pool.</span></span>

    
    </div>
    
    <span data-ttu-id="d6179-158">Se você implantou um novo pool (com o mesmo ou um FQDN diferente) para substituir o pool primário e deseja usar as configurações no nível do aplicativo a partir do pool de backup para o novo pool, inclua o parâmetro – ReplaceExistingSettings.</span><span class="sxs-lookup"><span data-stu-id="d6179-158">If you deployed a new pool (with the same or a different FQDN) to replace the primary pool, and you want to use the application-level settings from the backup pool for the new pool, include the –ReplaceExistingSettings parameter.</span></span> <span data-ttu-id="d6179-159">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-159">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<new primary pool FQDN>" -OverwriteOwner -FileName "<exported path and file name>" -ReplaceExistingSettings
    
    <span data-ttu-id="d6179-160">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-160">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:newprimary.contoso.com" -OverwriteOwner -FileName "C:\RgsExportPrimaryUpdated.zip" -ReplaceExistingSettings
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="d6179-161">Se você não quiser substituir as configurações no nível do aplicativo e o arquivo de áudio de música em espera padrão para o novo pool com as configurações do pool de backup, o novo pool usará as configurações padrão do aplicativo no nível do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6179-161">If you don't want to replace the application-level settings and default music-on-hold audio file for the new pool with the settings from the backup pool, the new pool will use the default application-level settings.</span></span>

    
    </div>

10. <span data-ttu-id="d6179-162">Verifique se a importação de volta para o pool primário foi bem-sucedida exibindo a configuração do grupo de resposta importado.</span><span class="sxs-lookup"><span data-stu-id="d6179-162">Verify that the import back to the primary pool was successful by displaying the imported response group configuration.</span></span> <span data-ttu-id="d6179-163">Siga este procedimento:</span><span class="sxs-lookup"><span data-stu-id="d6179-163">Do the following:</span></span>
    
      - <span data-ttu-id="d6179-164">Exiba todos os fluxos de trabalho no pool primário e verifique se todos os fluxos de trabalho importados estão incluídos.</span><span class="sxs-lookup"><span data-stu-id="d6179-164">Display all the workflows in the primary pool, and verify that all the imported workflows are included.</span></span> <span data-ttu-id="d6179-165">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-165">At the command line, type:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="d6179-166">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-166">For example:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer: primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="d6179-167">Exiba todas as filas no pool primário e verifique se todas as filas importadas estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="d6179-167">Display all the queues in the primary pool, and verify that all the imported queues are included.</span></span> <span data-ttu-id="d6179-168">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-168">At the command line, type:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="d6179-169">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-169">For example:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="d6179-170">Exiba todos os grupos de agente no pool primário e verifique se todos os grupos de agentes importados estão incluídos.</span><span class="sxs-lookup"><span data-stu-id="d6179-170">Display all the agent groups in the primary pool, and verify that all the imported agent groups are included.</span></span> <span data-ttu-id="d6179-171">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-171">At the command line, type:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer: <primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="d6179-172">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-172">For example:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="d6179-173">Exiba todas as horas de negócios no pool principal e verifique se todas as horas de trabalho importadas estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="d6179-173">Display all the hours of business in the primary pool, and verify that all the imported hours of business are included.</span></span> <span data-ttu-id="d6179-174">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-174">At the command line, type:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="d6179-175">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-175">For example:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="d6179-176">Exiba todos os conjuntos de feriados no pool primário e verifique se todos os conjuntos de feriados importados estão incluídos.</span><span class="sxs-lookup"><span data-stu-id="d6179-176">Display all the holiday sets in the primary pool, and verify that all the imported holiday sets are included.</span></span> <span data-ttu-id="d6179-177">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-177">At the command line, type:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="d6179-178">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-178">For example:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll

11. <span data-ttu-id="d6179-179">Verifique se a importação foi bem-sucedida fazendo uma chamada para um grupo de resposta importada e verificando se a chamada foi manipulada corretamente.</span><span class="sxs-lookup"><span data-stu-id="d6179-179">Verify that the import was successful by placing a call to an imported response group and verifying that the call is handled correctly.</span></span>

12. <span data-ttu-id="d6179-180">Opcionalmente, remova os grupos de resposta pertencentes ao pool principal do pool de backup.</span><span class="sxs-lookup"><span data-stu-id="d6179-180">Optionally, remove the response groups owned by the primary pool from the backup pool.</span></span> <span data-ttu-id="d6179-181">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="d6179-181">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer:<primary pool FQDN>" -FileName "<backup path and file name>" -RemoveExportedConfiguration
    
    <span data-ttu-id="d6179-182">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d6179-182">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer:primary.contoso.com" -FileName "C:\RgsExportPrimaryUpdated.zip" -RemoveExportedConfiguration
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d6179-183">Esta etapa cria um novo arquivo com a configuração exportada e, em seguida, remove-o do pool de backup.</span><span class="sxs-lookup"><span data-stu-id="d6179-183">This step creates a new file with the exported configuration, and then removes it from the backup pool.</span></span>

    
    <span data-ttu-id="d6179-184"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d6179-184"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

