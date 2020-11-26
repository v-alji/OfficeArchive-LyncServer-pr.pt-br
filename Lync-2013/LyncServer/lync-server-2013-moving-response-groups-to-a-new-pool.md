---
title: 'Lync Server 2013: movendo grupos de resposta para um novo pool'
description: 'Lync Server 2013: movendo grupos de resposta para um novo pool.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Moving response groups to a new pool
ms:assetid: da0db765-41e5-430b-b5a7-5418ec5ff2a7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205298(v=OCS.15)
ms:contentKeyID: 48185538
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b696963a28abbcd258f53fae12c3e281efa6ae4d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425259"
---
# <a name="moving-response-groups-to-a-new-pool-in-lync-server-2013"></a><span data-ttu-id="98c33-103">Movendo grupos de resposta para um novo pool no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98c33-103">Moving response groups to a new pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98c33-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98c33-104">

<span> </span></span></span>

<span data-ttu-id="98c33-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="98c33-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="98c33-106">O Lync Server 2013 introduz novo cmdlet support para mover grupos de resposta de um pool para outro pool, mesmo quando o FQDN (nome de domínio totalmente qualificado) for diferente.</span><span class="sxs-lookup"><span data-stu-id="98c33-106">Lync Server 2013 introduces new cmdlet support for moving response groups from one pool to another pool, even when the fully qualified domain name (FQDN) is different.</span></span>

<span data-ttu-id="98c33-107">Use as etapas do procedimento a seguir para mover grupos de resposta de um pool de front-ends para outro pool de front-end com um FQDN diferente.</span><span class="sxs-lookup"><span data-stu-id="98c33-107">Use the steps in the following procedure to move response groups from one Front End pool to another Front End pool with a different FQDN.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="98c33-108">Em um ambiente de coexistência, você pode mover grupos de resposta somente entre os &nbsp; pools de front-end do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="98c33-108">In a coexistence environment, you can move response groups only between Lync Server 2013&nbsp;Front End pools.</span></span>



</div>

<div>

## <a name="to-move-response-groups-to-a-pool-with-a-different-fqdn"></a><span data-ttu-id="98c33-109">Para mover grupos de resposta para um pool com um FQDN diferente</span><span class="sxs-lookup"><span data-stu-id="98c33-109">To move response groups to a pool with a different FQDN</span></span>

1.  <span data-ttu-id="98c33-110">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="98c33-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="98c33-111">Exporte os grupos de resposta no pool de origem.</span><span class="sxs-lookup"><span data-stu-id="98c33-111">Export the response groups in the source pool.</span></span> <span data-ttu-id="98c33-112">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="98c33-112">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<source FQDN>" -FileName "<export file name>"
    
    <span data-ttu-id="98c33-113">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="98c33-113">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:source.contoso.com" -FileName "C:\RgsExportSource.zip"
    
    <span data-ttu-id="98c33-114">Para remover os grupos de resposta do pool de origem durante a exportação, inclua o parâmetro – RemoveExportedConfiguration.</span><span class="sxs-lookup"><span data-stu-id="98c33-114">To remove the response groups from the source pool during the export, include the –RemoveExportedConfiguration parameter.</span></span> <span data-ttu-id="98c33-115">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="98c33-115">For example:</span></span>
    
        Export-CsRgsConfiguration -Source ApplicationServer:source.contoso.com -FileName "C:\RgsExportSource.zip" -RemoveExportedConfiguration

3.  <span data-ttu-id="98c33-116">Importe os grupos de resposta para o pool de destino e atribua o pool de destino como o novo proprietário.</span><span class="sxs-lookup"><span data-stu-id="98c33-116">Import the response groups to the destination pool and assign the destination pool as the new owner.</span></span> <span data-ttu-id="98c33-117">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="98c33-117">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<destination pool>" -FileName "<export file name>" -OverwriteOwner
    
    <span data-ttu-id="98c33-118">Se você também quiser copiar as configurações de nível de aplicativo do grupo de resposta do pool de origem para o pool de destino, inclua o parâmetro – ReplaceExistingRgsSettings.</span><span class="sxs-lookup"><span data-stu-id="98c33-118">If you also want to copy the Response Group application-level settings from the source pool to the destination pool, include the –ReplaceExistingRgsSettings parameter.</span></span> <span data-ttu-id="98c33-119">Você pode definir apenas um conjunto de configurações do aplicativo por pool.</span><span class="sxs-lookup"><span data-stu-id="98c33-119">You can define only one set of application-level settings per pool.</span></span> <span data-ttu-id="98c33-120">Se você copiar as configurações no nível do aplicativo do pool de origem para o pool de destino, as configurações do pool de origem substituirão as configurações do pool de destino.</span><span class="sxs-lookup"><span data-stu-id="98c33-120">If you copy the application-level settings from the source pool to the destination pool, the settings from the source pool replace the settings for the destination pool.</span></span> <span data-ttu-id="98c33-121">Se você não copiar as configurações no nível do aplicativo a partir do pool de origem, as configurações existentes do pool de destino serão aplicadas aos grupos de resposta importados.</span><span class="sxs-lookup"><span data-stu-id="98c33-121">If you do not copy the application-level settings from the source pool, the existing settings from the destination pool apply to the imported response groups.</span></span>
    
    <span data-ttu-id="98c33-122">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="98c33-122">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:destination.contoso.com" -FileName "C:\RgsExportSource.zip" -OverwriteOwner -ReplaceExistingRgsSettings
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="98c33-123">As configurações de nível de aplicativo incluem a configuração de música em espera padrão, o arquivo de áudio de música em espera padrão, o período de cortesia do agente e a configuração do contexto de chamada.</span><span class="sxs-lookup"><span data-stu-id="98c33-123">Application-level settings include the default music-on-hold configuration, the default music-on-hold audio file, the agent ringback grace period, and the call context configuration.</span></span> <span data-ttu-id="98c33-124">Para exibir essas definições de configuração, execute o cmdlet <STRONG>Get-CsRgsConfiguration</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="98c33-124">To view these configuration settings, run the <STRONG>Get-CsRgsConfiguration</STRONG> cmdlet.</span></span> <span data-ttu-id="98c33-125">Para obter detalhes sobre esse cmdlet, confira <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsRgsConfiguration">Get-CsRgsConfiguration</A>.</span><span class="sxs-lookup"><span data-stu-id="98c33-125">For details about this cmdlet, see <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsRgsConfiguration">Get-CsRgsConfiguration</A>.</span></span>

    
    </div>

4.  <span data-ttu-id="98c33-126">Verifique se a importação foi bem-sucedida exibindo a configuração do grupo de resposta importado fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="98c33-126">Verify that the import was successful by displaying the imported response group configuration by doing the following:</span></span>
    
      - <span data-ttu-id="98c33-127">Verifique se todos os fluxos de trabalho foram importados.</span><span class="sxs-lookup"><span data-stu-id="98c33-127">Verify that all the workflows were imported.</span></span> <span data-ttu-id="98c33-128">Na linha de comando, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="98c33-128">At the command line, type the following:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:<destination pool FQDN>"
    
      - <span data-ttu-id="98c33-129">Verifique se todas as filas foram importadas.</span><span class="sxs-lookup"><span data-stu-id="98c33-129">Verify that all the queues were imported.</span></span> <span data-ttu-id="98c33-130">Na linha de comando, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="98c33-130">At the command line, type the following:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:<destination pool FQDN>"
    
      - <span data-ttu-id="98c33-131">Verifique se todos os grupos de agente foram importados.</span><span class="sxs-lookup"><span data-stu-id="98c33-131">Verify that all the agent groups were imported.</span></span> <span data-ttu-id="98c33-132">Na linha de comando, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="98c33-132">At the command line, type the following:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:<destination pool FQDN>"
    
      - <span data-ttu-id="98c33-133">Verifique se todas as horas de negócios foram importadas.</span><span class="sxs-lookup"><span data-stu-id="98c33-133">Verify that all the hours of business were imported.</span></span> <span data-ttu-id="98c33-134">Na linha de comando, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="98c33-134">At the command line, type the following:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:<destination pool FQDN>" 
    
      - <span data-ttu-id="98c33-135">Verifique se todos os conjuntos de feriados foram importados.</span><span class="sxs-lookup"><span data-stu-id="98c33-135">Verify that all the holiday sets were imported.</span></span> <span data-ttu-id="98c33-136">Na linha de comando, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="98c33-136">At the command line, type the following:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:<destination pool FQDN>" 

5.  <span data-ttu-id="98c33-137">Verifique se a importação foi bem-sucedida fazendo uma chamada para um dos grupos de resposta e verificando se a chamada foi manipulada corretamente.</span><span class="sxs-lookup"><span data-stu-id="98c33-137">Verify that the import was successful by placing a call to one of the response groups and verifying that the call is handled correctly.</span></span>

6.  <span data-ttu-id="98c33-138">Solicite aos agentes que são membros de grupos de agentes formais para entrar em seus grupos de agente no pool de destino.</span><span class="sxs-lookup"><span data-stu-id="98c33-138">Request agents who are members of formal agent groups to sign in to their agent groups in the destination pool.</span></span>

7.  <span data-ttu-id="98c33-139">Se você não removeu anteriormente grupos de resposta do pool de origem, remova os grupos de resposta do pool de origem.</span><span class="sxs-lookup"><span data-stu-id="98c33-139">If you did not previously remove response groups from the source pool, remove the response groups from the source pool.</span></span> <span data-ttu-id="98c33-140">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="98c33-140">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<source pool FQDN> -RemoveExportedConfiguration -FileName "<temporary export file name>"
    
    <span data-ttu-id="98c33-141">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="98c33-141">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:source.contoso.com" -RemoveExportedConfiguration -FileName "C:\TempRGsConfiguration.zip"

<span data-ttu-id="98c33-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98c33-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

