---
title: 'Lync Server 2013: usando o serviço de log centralizado'
description: 'Lync Server 2013: usando o serviço de log centralizado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using the Centralized Logging Service
ms:assetid: 7b05aaef-f0ea-4649-ba8a-02e68b0cdf23
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688101(v=OCS.15)
ms:contentKeyID: 49733700
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f8b9edf839de889e9f0b01c10311f6b5c70ced8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390440"
---
# <a name="using-the-centralized-logging-service-in-lync-server-2013"></a><span data-ttu-id="1fab9-103">Usar o serviço de log centralizado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fab9-103">Using the Centralized Logging Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1fab9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1fab9-104">

<span> </span></span></span>

<span data-ttu-id="1fab9-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="1fab9-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="1fab9-106">O serviço de log centralizado é um novo recurso do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1fab9-106">The Centralized Logging Service is a new feature in Lync Server 2013.</span></span> <span data-ttu-id="1fab9-107">É uma substituição aprimorada para as ferramentas **OCSLogger** e **OCSTracer** fornecidas em versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="1fab9-107">It is an enhanced replacement for the **OCSLogger** and **OCSTracer** tools that were provided in previous releases.</span></span> <span data-ttu-id="1fab9-108">Você pode usar o serviço de log centralizado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="1fab9-108">You can use the Centralized Logging Service to perform the following tasks:</span></span>

  - <span data-ttu-id="1fab9-109">Comece a fazer logon em um ou mais computadores e pools a partir de um único local e comando.</span><span class="sxs-lookup"><span data-stu-id="1fab9-109">Start logging on one or more computers and pools from a single location and command.</span></span>

  - <span data-ttu-id="1fab9-110">Parar de fazer logon em um ou mais computadores e pools a partir de um único local e comando.</span><span class="sxs-lookup"><span data-stu-id="1fab9-110">Stop logging on one or more computers and pools from a single location and command.</span></span>

  - <span data-ttu-id="1fab9-111">Pesquisar logs em um ou mais computadores e pools para um único local e comando.</span><span class="sxs-lookup"><span data-stu-id="1fab9-111">Search logs on one or more computers and pools for a single location and command.</span></span> <span data-ttu-id="1fab9-112">Você pode personalizar o comando Pesquisar para retornar toda a agregação de registros que foram capturados e armazenados em todas as máquinas ou retornar um resultado aparado que captura dados específicos.</span><span class="sxs-lookup"><span data-stu-id="1fab9-112">You can tailor the search command to return the entire aggregation of logs that were captured and stored on all machines, or return a trimmed-down result that captures specific data.</span></span>

  - <span data-ttu-id="1fab9-113">Configurar as sessões de registro em log conforme segue:</span><span class="sxs-lookup"><span data-stu-id="1fab9-113">Configure logging sessions as follows:</span></span>
    
      - <span data-ttu-id="1fab9-114">Definir um **Cenário** ou usar um cenário padrão.</span><span class="sxs-lookup"><span data-stu-id="1fab9-114">Define a **Scenario**, or use a default scenario.</span></span> <span data-ttu-id="1fab9-115">Um *cenário* no serviço de log centralizado é composto de escopo (global ou de site), um nome de cenário para identificar a finalidade do cenário e um ou mais provedores.</span><span class="sxs-lookup"><span data-stu-id="1fab9-115">A *scenario* in Centralized Logging Service is made up of scope (global or site), a scenario name to identify the purpose of the scenario, and one or more providers.</span></span> <span data-ttu-id="1fab9-116">Você pode executar dois cenários a qualquer momento em um computador.</span><span class="sxs-lookup"><span data-stu-id="1fab9-116">You can run two scenarios at any given time on a computer.</span></span>
    
      - <span data-ttu-id="1fab9-p104">Usar um *provedor* local ou criar um novo provedor. Um *provedor* define o que será coletado pela sessão de registro em log, o nível de detalhamento, quais componentes serão rastreados e quais sinalizadores serão aplicados.</span><span class="sxs-lookup"><span data-stu-id="1fab9-p104">Use an existing *provider* or create a new provider. A *provider* defines what the logging session collects, what level of detail, what components to trace, and what flags are applied.</span></span>
        
        <div>
        

        > [!TIP]  
        > <span data-ttu-id="1fab9-119">Se estiver familiarizado com OCSLogger, o termo <EM>provedores</EM> se refere à coleta de <STRONG>componentes</STRONG> (por exemplo, S4, SIPStack), um <STRONG>tipo de registro de log</STRONG> (por exemplo, WPP, EventLog ou IIS logfile), um <STRONG>nível de rastreamento</STRONG> (por exemplo, All, verbose, debug) e <STRONG>sinalizadores</STRONG> (por exemplo, TF_COMPONENT, TF_DIAG).</span><span class="sxs-lookup"><span data-stu-id="1fab9-119">If you are familiar with OCSLogger, the term <EM>providers</EM> refers to the collection of <STRONG>components</STRONG> (for example, S4, SIPStack), a <STRONG>logging type</STRONG> (for example, WPP, EventLog, or IIS logfile), a <STRONG>tracing level</STRONG> (for example, All, verbose, debug), and <STRONG>flags</STRONG> (for example, TF_COMPONENT, TF_DIAG).</span></span> <span data-ttu-id="1fab9-120">Esses itens são definidos no provedor (uma variável do Windows PowerShell) e passados para o comando de serviço de log centralizado.</span><span class="sxs-lookup"><span data-stu-id="1fab9-120">These items are defined in the provider (a Windows PowerShell variable) and passed into the Centralized Logging Service command.</span></span>

        
        </div>
    
      - <span data-ttu-id="1fab9-121">Configurar os computadores e os pools dos quais você deseja coletar logs.</span><span class="sxs-lookup"><span data-stu-id="1fab9-121">Configure the computers and pools that you want to collect logs from.</span></span>
    
      - <span data-ttu-id="1fab9-122">Defina o escopo da sessão de log no **site** de opções (execute o log de capturas somente em computadores nesse site) ou **global** (execute a captura de log em todos os computadores na implantação).</span><span class="sxs-lookup"><span data-stu-id="1fab9-122">Define the scope for the logging session from the options **Site** (run logging captures on computers in that site only), or **Global** (run logging capture on all computers in the deployment).</span></span>

<span data-ttu-id="1fab9-123">O serviço de registro centralizado é extremamente eficiente e atende a praticamente todas as necessidades para solucionar problemas, sejam grandes ou pequenos.</span><span class="sxs-lookup"><span data-stu-id="1fab9-123">The Centralized Logging Service is extremely powerful and can meet nearly all of the needs for troubleshooting problems—large or small.</span></span> <span data-ttu-id="1fab9-124">Da análise de causa raiz para problemas de desempenho, o serviço de registro em log centralizado pode ser uma ferramenta importante para qualquer administrador.</span><span class="sxs-lookup"><span data-stu-id="1fab9-124">From root cause analysis to performance problems, the Centralized Logging Service can be an important tool for any administrator.</span></span> <span data-ttu-id="1fab9-125">Todos os exemplos são exibidos usando o Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1fab9-125">All examples are shown using the Lync Server Management Shell.</span></span> <span data-ttu-id="1fab9-126">Há um componente de linha de comando para o serviço de log centralizado chamado **CLSController.exe**.</span><span class="sxs-lookup"><span data-stu-id="1fab9-126">There is a command-line component for the Centralized Logging Service called **CLSController.exe**.</span></span> <span data-ttu-id="1fab9-127">A ajuda é fornecida para a ferramenta de linha de comando por meio da própria ferramenta.</span><span class="sxs-lookup"><span data-stu-id="1fab9-127">Help is provided for the command-line tool through the tool itself.</span></span> <span data-ttu-id="1fab9-128">No entanto, há um conjunto limitado de funções que você pode executar a partir da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="1fab9-128">However, there is a limited set of functions that you can execute from the command line.</span></span> <span data-ttu-id="1fab9-129">Ao usar o Shell de gerenciamento do Lync Server, você tem acesso a um conjunto muito maior e muito mais configurável de recursos.</span><span class="sxs-lookup"><span data-stu-id="1fab9-129">By using Lync Server Management Shell, you have access to a much larger and much more configurable set of features.</span></span> <span data-ttu-id="1fab9-130">Você sempre deve considerar o Shell de gerenciamento do Lync Server como o principal método ao usar o serviço de log centralizado.</span><span class="sxs-lookup"><span data-stu-id="1fab9-130">You should always consider Lync Server Management Shell as the first and foremost method when using the Centralized Logging Service.</span></span>

<span data-ttu-id="1fab9-131">Os tópicos desta seção explicam como usar o serviço de log centralizado e exemplos de como usar seus muitos recursos.</span><span class="sxs-lookup"><span data-stu-id="1fab9-131">The topics in this section explain how to use the Centralized Logging Service and examples of how to use its many features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="1fab9-132">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="1fab9-132">In This Section</span></span>

  - [<span data-ttu-id="1fab9-133">Visão geral do serviço de log centralizado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fab9-133">Overview of the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-overview-of-the-centralized-logging-service.md)

  - [<span data-ttu-id="1fab9-134">Gerenciar as configurações centralizadas de configuração do serviço de log no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fab9-134">Managing the Centralized Logging Service configuration settings in Lync Server 2013</span></span>](lync-server-2013-managing-the-centralized-logging-service-configuration-settings.md)

  - [<span data-ttu-id="1fab9-135">Compreendendo as configurações centralizadas de configuração do serviço de log no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fab9-135">Understanding Centralized Logging Service configuration settings in Lync Server 2013</span></span>](lync-server-2013-understanding-centralized-logging-service-configuration-settings.md)

  - [<span data-ttu-id="1fab9-136">Usar o Start para o serviço de log centralizado para capturar logs no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fab9-136">Using Start for the Centralized Logging Service to capture logs in Lync Server 2013</span></span>](lync-server-2013-using-start-for-the-centralized-logging-service-to-capture-logs.md)

  - [<span data-ttu-id="1fab9-137">Usar stop para o serviço de log centralizado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fab9-137">Using Stop for the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-using-stop-for-the-centralized-logging-service.md)

  - [<span data-ttu-id="1fab9-138">Usar a pesquisa em logs de captura criados pelo serviço de log centralizado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fab9-138">Using search on capture logs created by the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-using-search-on-capture-logs-created-by-the-centralized-logging-service.md)

  - [<span data-ttu-id="1fab9-139">Ler logs de captura do serviço de log centralizado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fab9-139">Reading capture logs from the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-reading-capture-logs-from-the-centralized-logging-service.md)

<span data-ttu-id="1fab9-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1fab9-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

