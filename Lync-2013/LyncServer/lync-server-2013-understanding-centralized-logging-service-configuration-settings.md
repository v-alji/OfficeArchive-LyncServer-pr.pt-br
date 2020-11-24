---
title: Compreendendo as configurações centralizadas de configuração do serviço de log
description: Compreendendo as configurações centralizadas de configuração do serviço de log.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding Centralized Logging Service configuration settings
ms:assetid: 3c34e600-0b91-43dc-b4cc-90b6a70ee12e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688029(v=OCS.15)
ms:contentKeyID: 49733619
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f99dbffe15c4b3f0dc13d231c3a2732a8554397
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390221"
---
# <a name="understanding-centralized-logging-service-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="73367-103">Compreendendo as configurações centralizadas de configuração do serviço de log no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73367-103">Understanding Centralized Logging Service configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="73367-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="73367-104">

<span> </span></span></span>

<span data-ttu-id="73367-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="73367-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="73367-106">O serviço de log centralizado é configurado para definir o que o serviço de log destina-se a coletar, como ele coleta, de onde será coletado, e quais são as configurações de log.</span><span class="sxs-lookup"><span data-stu-id="73367-106">The Centralized Logging Service is configured to define what the logging service is intended to collect, how it collects, where it will collect from, and what the log settings are.</span></span> <span data-ttu-id="73367-107">Você define essas configurações globalmente (ou seja, para toda a implantação) ou para um site (ou seja, um site nomeado na sua implantação).</span><span class="sxs-lookup"><span data-stu-id="73367-107">You define these settings globally (that is, for the entire deployment) or for a site (that is, a named site in your deployment).</span></span> <span data-ttu-id="73367-108">Qualquer log que você definir usará as configurações adequadas para a identidade usada para os comandos para iniciar, parar, liberar e pesquisar logs.</span><span class="sxs-lookup"><span data-stu-id="73367-108">Any logging that you define will use the settings that are appropriate for the identity that you use for commands to start, stop, flush, and search logs.</span></span>

<div>

## <a name="to-display-the-current-centralized-logging-service-configuration"></a><span data-ttu-id="73367-109">Para exibir a configuração atual do serviço de log centralizado</span><span class="sxs-lookup"><span data-stu-id="73367-109">To display the current Centralized Logging Service configuration</span></span>

1.  <span data-ttu-id="73367-110">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="73367-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="73367-111">Digite o seguinte em uma linha de comando do prompt:</span><span class="sxs-lookup"><span data-stu-id="73367-111">Type the following at a command-line prompt:</span></span>
    
        Get-CsClsConfiguration
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="73367-112">Você pode restringir ou expandir o escopo das configurações que são retornadas definindo-se <CODE>-Identity</CODE> um escopo, como "site: Redmond", para retornar apenas o CsClsConfiguration para o site Redmond.</span><span class="sxs-lookup"><span data-stu-id="73367-112">You can narrow or expand the scope of the configuration settings that are returned by defining <CODE>-Identity</CODE> and a scope, such as "Site:Redmond" to return only the CsClsConfiguration for the site Redmond.</span></span> <span data-ttu-id="73367-113">Se quiser obter detalhes sobre uma determinada parte da configuração, você pode canalizar a saída para outro cmdlet do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="73367-113">If you want details about a given portion of the configuration, you can pipe the output into another Windows PowerShell cmdlet.</span></span> <span data-ttu-id="73367-114">Por exemplo, para obter detalhes sobre os cenários definidos na configuração do site "Redmond", digite: <CODE>Get-CsClsConfiguration -Identity "site:Redmond" | Select-Object -ExpandPropery Scenarios</CODE></span><span class="sxs-lookup"><span data-stu-id="73367-114">For example, to get details about the scenarios defined in the configuration for site "Redmond", type: <CODE>Get-CsClsConfiguration -Identity "site:Redmond" | Select-Object -ExpandPropery Scenarios</CODE></span></span>

    
    </div>
    
    <span data-ttu-id="73367-115">![Exemplo de saída do Get-CsClsConfiguration.](images/JJ688029.23f98ddc-fc48-499a-b6c5-752611f2a0b0(OCS.15).jpg "Exemplo de saída do Get-CsClsConfiguration.")</span><span class="sxs-lookup"><span data-stu-id="73367-115">![Sample output from Get-CsClsConfiguration.](images/JJ688029.23f98ddc-fc48-499a-b6c5-752611f2a0b0(OCS.15).jpg "Sample output from Get-CsClsConfiguration.")</span></span>
    
    <span data-ttu-id="73367-116">O resultado do cmdlet exibe a configuração atual do serviço de log centralizado.</span><span class="sxs-lookup"><span data-stu-id="73367-116">The result from the cmdlet displays the current configuration of the Centralized Logging Service.</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="73367-117">Definição da Configuração</span><span class="sxs-lookup"><span data-stu-id="73367-117">Configuration Setting</span></span></th>
    <th><span data-ttu-id="73367-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="73367-118">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="73367-119"><strong>Identidade</strong></span><span class="sxs-lookup"><span data-stu-id="73367-119"><strong>Identity</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-p103">Identifica o escopo e o nome para esta configuração. Há apenas uma configuração global e uma configuração por local.</span><span class="sxs-lookup"><span data-stu-id="73367-p103">Identifies the scope and name for this configuration. There is only one Global configuration, and one configuration per site.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="73367-122"><strong>Cenários</strong></span><span class="sxs-lookup"><span data-stu-id="73367-122"><strong>Scenarios</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-123">Lista de todos os cenários que são definidos para esta configuração.</span><span class="sxs-lookup"><span data-stu-id="73367-123">Listing of all scenarios that are defined for this configuration.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="73367-124"><strong>Termos de busca</strong></span><span class="sxs-lookup"><span data-stu-id="73367-124"><strong>SearchTerms</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-125">Termos de busca definidos para a configuração.</span><span class="sxs-lookup"><span data-stu-id="73367-125">Defined search terms for the configuration.</span></span> <span data-ttu-id="73367-126">Office 365 ou Microsoft 365, não implantações locais.</span><span class="sxs-lookup"><span data-stu-id="73367-126">Office 365 or Microsoft 365, not on-premises deployments.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="73367-127"><strong>SecurityGroups</strong></span><span class="sxs-lookup"><span data-stu-id="73367-127"><strong>SecurityGroups</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-128">Grupos de segurança definidos que controlam quem (isto é, membros dos grupos de segurança) podem ver computadores com base no local que estão.</span><span class="sxs-lookup"><span data-stu-id="73367-128">Defined security groups that control who (that is, members of the security groups) can see computers based on the site they are located in.</span></span> <span data-ttu-id="73367-129">O site, nesse contexto, é o site definido no construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="73367-129">Site, in this context, is the site as defined in Topology Builder.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="73367-130"><strong>Regiões</strong></span><span class="sxs-lookup"><span data-stu-id="73367-130"><strong>Regions</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-131">Regiões definidas são utilizadas para coletar SecurityGroups em uma região, por exemplo EMEA.</span><span class="sxs-lookup"><span data-stu-id="73367-131">Defined regions are used to collect SecurityGroups into a region, for example EMEA.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="73367-132"><strong>EtlFileFolder</strong></span><span class="sxs-lookup"><span data-stu-id="73367-132"><strong>EtlFileFolder</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-133">Caminho definido para o local onde os arquivos de log são gravados em computadores.</span><span class="sxs-lookup"><span data-stu-id="73367-133">Defined path to the location where log files are written on computers.</span></span> <span data-ttu-id="73367-134">O CLSAgent grava os arquivos de log e é executado sob o contexto do serviço de rede.</span><span class="sxs-lookup"><span data-stu-id="73367-134">CLSAgent writes the log files and runs under the context of the Network Service.</span></span> <span data-ttu-id="73367-135">Nesse caso,% TEMP% se expande para%WINDIR%\ServiceProfiles\NetworkService\AppData\Local</span><span class="sxs-lookup"><span data-stu-id="73367-135">In this case, %TEMP% expands to %WINDIR%\ServiceProfiles\NetworkService\AppData\Local</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="73367-136"><strong>EtlFileRolloverSizeMB</strong></span><span class="sxs-lookup"><span data-stu-id="73367-136"><strong>EtlFileRolloverSizeMB</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-p107">O parâmetro indica o tamanho máximo do arquivo de log antes que um log de rastreio de evento (.etl) novo seja criado. Um novo arquivo de log é criado quando o tamanho definido é atingido, mesmo se o tempo máximo definido no EtlFileRolloverMinutes não tiver sido atingido ainda.</span><span class="sxs-lookup"><span data-stu-id="73367-p107">The parameter indicates the maximum size of the log file before a new event trace log (.etl) file is created. A new log file is created when the defined size is reached even if the maximum time set in EtlFileRolloverMinutes has not yet been reached.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="73367-139"><strong>EtlFileRolloverMinutes</strong></span><span class="sxs-lookup"><span data-stu-id="73367-139"><strong>EtlFileRolloverMinutes</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-p108">Quantidade de tempo máxima definida, em minutos, que um log pode decorrer antes de um novo arquivo .etl ser criado. Um novo arquivo de log é criado quando o cronômetro expira, mesmo que o tamanho máximo definido em EtlFileRolloverSizeMB não tenha sido atingido ainda.</span><span class="sxs-lookup"><span data-stu-id="73367-p108">Defined maximum amount of time, in minutes, that a log can elapse before a new .etl file is created. A new log file is created when the timer expires even if the maximum size set in EtlFileRolloverSizeMB has not yet been reached.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="73367-142"><strong>TmfFileSearchPath</strong></span><span class="sxs-lookup"><span data-stu-id="73367-142"><strong>TmfFileSearchPath</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-143">Local para buscar por arquivos de formato de mensagens de rastreio.</span><span class="sxs-lookup"><span data-stu-id="73367-143">Location to search for the trace message format files.</span></span> <span data-ttu-id="73367-144">Os arquivos de formato de mensagem de rastreamento são usados para converter os arquivos binários em um formato legível por pessoas.</span><span class="sxs-lookup"><span data-stu-id="73367-144">The trace message format files are used to convert the binary files into a human readable format.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="73367-145"><strong>CacheFileLocalFolders</strong></span><span class="sxs-lookup"><span data-stu-id="73367-145"><strong>CacheFileLocalFolders</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-p110">Caminho definido para o local onde os arquivos de cache são gravados nos computadores. O CLSAgent grava os arquivos de cache e executa sob o contexto do Serviço de Rede. Neste caso, %TEMP% expande-se para %WINDIR%\ServiceProfiles\NetworkService\AppData\Local. Por padrão, os arquivos de log e cache são gravados no mesmo diretório.</span><span class="sxs-lookup"><span data-stu-id="73367-p110">Defined path to the location where cache files are written on computers. CLSAgent writes the cache files and runs under the context of the Network Service. In this case, %TEMP% expands to %WINDIR%\ServiceProfiles\NetworkService\AppData\Local. By default, cache files and log files are written to the same directory.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="73367-150"><strong>CacheFileNetworkFolder</strong></span><span class="sxs-lookup"><span data-stu-id="73367-150"><strong>CacheFileNetworkFolder</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-151">Você pode definir um caminho de convenção de nomenclatura universal (UNC) para receber os arquivos de cache durante operações de log.</span><span class="sxs-lookup"><span data-stu-id="73367-151">You can define a universal naming convention (UNC) path to receive the cache files during logging operations.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="73367-152"><strong>CacheFileLocalRetentionPeriod</strong></span><span class="sxs-lookup"><span data-stu-id="73367-152"><strong>CacheFileLocalRetentionPeriod</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-153">Definido como o tempo máximo em dias que os arquivos de cache são retidos.</span><span class="sxs-lookup"><span data-stu-id="73367-153">Defined as the maximum time, in days, that cache files are retained.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="73367-154"><strong>CacheFileMaxDiskUsage</strong></span><span class="sxs-lookup"><span data-stu-id="73367-154"><strong>CacheFileMaxDiskUsage</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-155">Definido como a porcentagem de espaço em disco que pode ser utilizado pelos arquivos de cache.</span><span class="sxs-lookup"><span data-stu-id="73367-155">Defined as the percentage of disk space that can be used by the cache files.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="73367-156"><strong>ComponentThrottleLimit</strong></span><span class="sxs-lookup"><span data-stu-id="73367-156"><strong>ComponentThrottleLimit</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-157">Definido como o número máximo de rastreamentos por segundo que um componente pode produzir antes de o limitador de aceleração automática é acionado.</span><span class="sxs-lookup"><span data-stu-id="73367-157">Defined as the maximum number of traces per second that a component can produce before the automatic throttle limiter is triggered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="73367-158"><strong>ComponentThrottleSample</strong></span><span class="sxs-lookup"><span data-stu-id="73367-158"><strong>ComponentThrottleSample</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-159">Número de vezes que o ComponentThrottleLimit pode ser excedido em 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="73367-159">Number of times in 60 seconds that the ComponentThrottleLimit can be exceeded.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="73367-160"><strong>MinimumClsAgentServiceVersion</strong></span><span class="sxs-lookup"><span data-stu-id="73367-160"><strong>MinimumClsAgentServiceVersion</strong></span></span></p></td>
    <td><p><span data-ttu-id="73367-161">A versão mínima do CLSAgent que pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="73367-161">The minimum version of the CLSAgent allowed to run.</span></span> <span data-ttu-id="73367-162">Esse elemento destina-se ao Office 365 ou ao Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="73367-162">This element is intended for Office 365 or Microsoft 365.</span></span></p></td>
    </tr>
    </tbody>
    </table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="73367-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="73367-163">See Also</span></span>


[<span data-ttu-id="73367-164">Visão geral do serviço de log centralizado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73367-164">Overview of the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-overview-of-the-centralized-logging-service.md)  


<span data-ttu-id="73367-165">[Set-CsClsConfiguration](https://technet.microsoft.com/library/JJ619182(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="73367-165">[Set-CsClsConfiguration](https://technet.microsoft.com/library/JJ619182(v=OCS.15))</span></span>  
<span data-ttu-id="73367-166">[Remove-CsClsConfiguration](https://technet.microsoft.com/library/JJ619191(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="73367-166">[Remove-CsClsConfiguration](https://technet.microsoft.com/library/JJ619191(v=OCS.15))</span></span>  
<span data-ttu-id="73367-167">[New-CsClsConfiguration](https://technet.microsoft.com/library/JJ619177(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="73367-167">[New-CsClsConfiguration](https://technet.microsoft.com/library/JJ619177(v=OCS.15))</span></span>  
<span data-ttu-id="73367-168">[Get-CsClsConfiguration](https://technet.microsoft.com/library/JJ619179(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="73367-168">[Get-CsClsConfiguration](https://technet.microsoft.com/library/JJ619179(v=OCS.15))</span></span>  
  

<span data-ttu-id="73367-169"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="73367-169"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

