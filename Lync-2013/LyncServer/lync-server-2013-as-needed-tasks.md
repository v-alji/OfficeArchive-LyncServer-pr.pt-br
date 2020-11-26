---
title: 'Lync Server 2013: tarefas necessárias'
description: 'Lync Server 2013: tarefas necessárias.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: As-needed tasks
ms:assetid: b66bc6fe-f138-4cf4-ba7f-aee9a3e0497e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn722431(v=OCS.15)
ms:contentKeyID: 63969643
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 91fe249d9615bb619426c58b22606c3ef182f9a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440546"
---
# <a name="as-needed-tasks-in-lync-server-2013"></a><span data-ttu-id="19a1b-103">Tarefas o mais necessárias no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="19a1b-103">As-needed tasks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19a1b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19a1b-104">

<span> </span></span></span>

<span data-ttu-id="19a1b-105">_**Tópico da última modificação:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="19a1b-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="19a1b-106">Execute as seguintes tarefas, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="19a1b-106">Perform the following tasks as necessary.</span></span> <span data-ttu-id="19a1b-107">Eles também são cobertos pelos procedimentos padrão com frequência:</span><span class="sxs-lookup"><span data-stu-id="19a1b-107">They are frequently also covered by standard procedures:</span></span>

  - <span data-ttu-id="19a1b-108">\* \* Auditoria de segurança completa \* \* você pode executar essa auditoria regularmente, em resposta a uma atualização ou reformulação do sistema de mensagens ou em resposta a uma falha de segurança tentada (ou bem-sucedida).</span><span class="sxs-lookup"><span data-stu-id="19a1b-108">\*\*Full Security Auditing   \*\*You can perform this audit regularly, in response to an upgrade or redesign of the messaging system, or in response to an attempted (or successful) security breach.</span></span> <span data-ttu-id="19a1b-109">O procedimento pode envolver verificações de porta em servidores e firewalls, auditorias de correções de segurança e testes de penetração de terceiros.</span><span class="sxs-lookup"><span data-stu-id="19a1b-109">The procedure may involve port scans on servers and firewalls, audits of security fixes, and third-party penetration tests.</span></span>

  - <span data-ttu-id="19a1b-110">**Substituir certificados prestes a expirar**   Verificar se os certificados do Lync Server é uma das tarefas semanais regulares e, como parte do procedimento, um administrador deve ter um registro de todas as datas de vencimento dos certificados.</span><span class="sxs-lookup"><span data-stu-id="19a1b-110">**Replace Certificates about to Expire**   Checking Lync Server Certificates is one of regular weekly tasks, and as part of the procedure an administrator should have a record of all certificates’ expiry dates.</span></span> <span data-ttu-id="19a1b-111">Este registro permite que um administrador crie uma notificação quando um certificado específico estiver prestes a expirar e ser substituído conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="19a1b-111">This record enables an administrator to create a notification when a particular certificate is about to be expired and replaced as needed.</span></span>

  - <span data-ttu-id="19a1b-112">**Atualizando linhas de base de desempenho**   Atualize as linhas de base de desempenho após uma atualização ou alteração de configuração.</span><span class="sxs-lookup"><span data-stu-id="19a1b-112">**Updating Performance Baselines**   Update performance baselines after an upgrade or configuration change.</span></span> <span data-ttu-id="19a1b-113">Sua organização pode usar linhas de base para medir alterações de desempenho e detectar problemas que afetam o desempenho do sistema.</span><span class="sxs-lookup"><span data-stu-id="19a1b-113">Your organization can use baselines to measure performance changes and to detect issues that affect system performance.</span></span>

  - <span data-ttu-id="19a1b-114">**Gerenciando o pool corporativo**   A configuração inicial de pools corporativos, servidores Standard Edition e quaisquer outros servidores no ambiente da sua organização foram realizadas durante a implantação dos servidores individuais.</span><span class="sxs-lookup"><span data-stu-id="19a1b-114">**Managing Enterprise Pool**   Initial configuration of Enterprise pools, Standard Edition servers, and any other servers in your organization's environment were done during deployment of the individual servers.</span></span> <span data-ttu-id="19a1b-115">O gerenciamento pós-implantação de servidores e pools para servidores Standard Edition e pools corporativos inclui as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="19a1b-115">Post-deployment management of servers and pools for Standard Edition servers and Enterprise pools includes the following tasks:</span></span>
    
      - <span data-ttu-id="19a1b-116">Gerenciamento de servidores front-end</span><span class="sxs-lookup"><span data-stu-id="19a1b-116">Managing Front End Servers</span></span>
    
      - <span data-ttu-id="19a1b-117">Como gerenciar a conferência via Web</span><span class="sxs-lookup"><span data-stu-id="19a1b-117">Managing Web Conferencing</span></span>
    
      - <span data-ttu-id="19a1b-118">Como gerenciar a conferência</span><span class="sxs-lookup"><span data-stu-id="19a1b-118">Managing Conferencing</span></span>
    
      - <span data-ttu-id="19a1b-119">Alterar as credenciais da conta de serviço</span><span class="sxs-lookup"><span data-stu-id="19a1b-119">Changing Service Account Credentials</span></span>
    
      - <span data-ttu-id="19a1b-120">Como gerenciar bancos de dados</span><span class="sxs-lookup"><span data-stu-id="19a1b-120">Managing Databases</span></span>
    
      - <span data-ttu-id="19a1b-121">Iniciando e parando serviços e desativando funções de servidor</span><span class="sxs-lookup"><span data-stu-id="19a1b-121">Starting and Stopping Services and Deactivating Server Roles</span></span>
    
      - <span data-ttu-id="19a1b-122">Removendo servidores e funções de servidor, removendo pools e descomissionando servidores e pools</span><span class="sxs-lookup"><span data-stu-id="19a1b-122">Removing Servers and Server Roles, Removing Pools, and Decommissioning Servers and Pools</span></span>

  - <span data-ttu-id="19a1b-123">**Gerenciando o uso**   Você pode configurar o Lync Server 2013 para fornecer os recursos e funcionalidades mais apropriados para a sua organização.</span><span class="sxs-lookup"><span data-stu-id="19a1b-123">**Managing Usage**   You can configure Lync Server 2013 to provide the features and functionality that are most appropriate for your organization.</span></span> <span data-ttu-id="19a1b-124">Isso inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="19a1b-124">This includes the following:</span></span>
    
      - <span data-ttu-id="19a1b-125">Gerenciando o suporte para reuniões do Web conferência locais</span><span class="sxs-lookup"><span data-stu-id="19a1b-125">Managing Support for On-Premise Web Conferencing Meetings</span></span>
    
      - <span data-ttu-id="19a1b-126">Gerenciar o uso de grupos de distribuição para enviar mensagens instantâneas</span><span class="sxs-lookup"><span data-stu-id="19a1b-126">Managing the Use of Distribution Groups to Send Instant Messages</span></span>
    
      - <span data-ttu-id="19a1b-127">Gerenciando contatos, presença e consultas</span><span class="sxs-lookup"><span data-stu-id="19a1b-127">Managing Contacts, Presence, and Queries</span></span>
    
      - <span data-ttu-id="19a1b-128">Configurando a filtragem de versão do cliente</span><span class="sxs-lookup"><span data-stu-id="19a1b-128">Configuring Client Version Filtering</span></span>
    
      - <span data-ttu-id="19a1b-129">Configurando a filtragem inteligente de IM</span><span class="sxs-lookup"><span data-stu-id="19a1b-129">Configuring Intelligent IM Filtering</span></span>
    
      - <span data-ttu-id="19a1b-130">Configurando o arquivamento, a gravação de detalhes da chamada e a conformidade da reunião</span><span class="sxs-lookup"><span data-stu-id="19a1b-130">Configuring Archiving, Call Detail Recording, and Meeting Compliance</span></span>

  - <span data-ttu-id="19a1b-131">**Gerenciando a conectividade do servidor de borda**   O gerenciamento contínuo dos servidores e das configurações necessárias para fornecer conectividade externa inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="19a1b-131">**Managing Edge Server Connectivity**   Ongoing management of the servers and settings required to provide external connectivity includes the following:</span></span>
    
      - <span data-ttu-id="19a1b-132">Gerenciando a conectividade entre servidores internos e servidores de borda</span><span class="sxs-lookup"><span data-stu-id="19a1b-132">Managing Connectivity between Internal Servers and Edge Servers</span></span>
    
      - <span data-ttu-id="19a1b-133">Configurando interfaces internas e externas e certificados para servidores Edge</span><span class="sxs-lookup"><span data-stu-id="19a1b-133">Configuring Internal and External Interfaces and Certificates for Edge Servers</span></span>
    
      - <span data-ttu-id="19a1b-134">Gerenciando o acesso de parceiro federado</span><span class="sxs-lookup"><span data-stu-id="19a1b-134">Managing Federated Partner Access</span></span>

  - <span data-ttu-id="19a1b-135">**Administrar o catálogo de endereços**   Administrar servidores de catálogo de endereços inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="19a1b-135">**Administering the Address Book**   Administering Address Book Servers includes the following:</span></span>
    
      - <span data-ttu-id="19a1b-136">Configurando a normalização do telefone do servidor catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="19a1b-136">Configuring Address Book Server phone normalization</span></span>
    
      - <span data-ttu-id="19a1b-137">Gerenciando o servidor de catálogo de endereços na linha de comando</span><span class="sxs-lookup"><span data-stu-id="19a1b-137">Managing the Address Book Server from the command line</span></span>

  - <span data-ttu-id="19a1b-138">**Gerenciando contas de usuário**   O gerenciamento de contas de usuário inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="19a1b-138">**Managing User Accounts**   Management of user accounts includes the following:</span></span>
    
      - <span data-ttu-id="19a1b-139">Habilitando contas de usuário para o Lync Server</span><span class="sxs-lookup"><span data-stu-id="19a1b-139">Enabling User Accounts for Lync Server</span></span>
    
      - <span data-ttu-id="19a1b-140">Configurar usuários do Lync Server usando o assistente</span><span class="sxs-lookup"><span data-stu-id="19a1b-140">Configuring Lync Server Users using the Wizard</span></span>
    
      - <span data-ttu-id="19a1b-141">Configurar propriedades individuais da conta de usuário do Lync Server</span><span class="sxs-lookup"><span data-stu-id="19a1b-141">Configuring Individual Lync Server User Account Properties</span></span>
    
      - <span data-ttu-id="19a1b-142">Procurando usuários do Lync Server</span><span class="sxs-lookup"><span data-stu-id="19a1b-142">Searching for Lync Server Users</span></span>
    
      - <span data-ttu-id="19a1b-143">Movendo usuários do Lync Server</span><span class="sxs-lookup"><span data-stu-id="19a1b-143">Moving Lync Server Users</span></span>
    
      - <span data-ttu-id="19a1b-144">Excluindo usuários do Lync Server</span><span class="sxs-lookup"><span data-stu-id="19a1b-144">Deleting Lync Server Users</span></span>

  - <span data-ttu-id="19a1b-145">**Analisando arquivos de log do Lync Server 2013**   Uma ferramenta muito útil, geralmente usada para solução de problemas, é a ferramenta de log do Lync Server 2013 descrita em detalhes em [usando a ferramenta de log do Lync server 2013](https://technet.microsoft.com/library/gg558599.aspx).</span><span class="sxs-lookup"><span data-stu-id="19a1b-145">**Analyzing Lync Server 2013 Log Files**   One very helpful tool, generally used for troubleshooting, is the Lync Server 2013 Logging Tool described in detail in [Using Lync Server 2013 Logging Tool](https://technet.microsoft.com/library/gg558599.aspx).</span></span>

<span data-ttu-id="19a1b-146">Como a ferramenta de log gera arquivos de log (em uma base por servidor), esses arquivos de log podem ser visualizados e analisados usando-se a ferramenta de rastreamento, se as ferramentas do Microsoft Office Server 12 Resource Kit estiverem instaladas no computador.</span><span class="sxs-lookup"><span data-stu-id="19a1b-146">Because the Logging Tool generates log files (on a per-server basis), these log files can be viewed and analyzed by using the Snooper tool, if the Microsoft Office Server 12 Resource Kit Tools are installed on the computer.</span></span> <span data-ttu-id="19a1b-147">Caso contrário, os logs também podem ser analisados usando um editor de texto, que é muito menos transparente e mais complexo do que usar o utilitário de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="19a1b-147">Otherwise, logs can also be analyzed by using a text editor, which is much less transparent and more complex than using the Snooper utility.</span></span>

<span data-ttu-id="19a1b-148">Para exibir e analisar mensagens de protocolo</span><span class="sxs-lookup"><span data-stu-id="19a1b-148">To View and Analyze Protocol Messages</span></span>

<span data-ttu-id="19a1b-149">Na ferramenta de log, quando você tiver encerrado a sessão de depuração, clique em analisar arquivos de log para ver os arquivos de log usando a ferramenta de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="19a1b-149">In the Logging Tool, when you have ended the debug session, click Analyze Log Files to view the log files by using the Snooper tool.</span></span> <span data-ttu-id="19a1b-150">Você pode analisar logs de protocolo para os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="19a1b-150">You can analyze protocol logs for the following components:</span></span>

  - <span data-ttu-id="19a1b-151">Lync Server SipStack (SIP)</span><span class="sxs-lookup"><span data-stu-id="19a1b-151">Lync Server SipStack (SIP)</span></span>

  - <span data-ttu-id="19a1b-152">A S4 (SIP) do Lync Server</span><span class="sxs-lookup"><span data-stu-id="19a1b-152">Lync Server S4 (SIP)</span></span>

  - <span data-ttu-id="19a1b-153">Tráfego de sinalização do Lync Server Conferencing (C3P), incluindo a MCU-C3P e o foco C3P</span><span class="sxs-lookup"><span data-stu-id="19a1b-153">Lync Server Conferencing signaling traffic (C3P), including MCU Infra C3P and Focus C3P</span></span>

  - <span data-ttu-id="19a1b-154">Tráfego da webconferência do Lync Server (PSOM)</span><span class="sxs-lookup"><span data-stu-id="19a1b-154">Lync Server Web conferencing traffic (PSOM)</span></span>

  - <span data-ttu-id="19a1b-155">Cliente da plataforma de cliente de comunicação unificada do Lync Server (UCCP)</span><span class="sxs-lookup"><span data-stu-id="19a1b-155">Lync Server Unified Communications Client Platform client (UCCP)</span></span>

  - <span data-ttu-id="19a1b-156">Relatórios de erros do banco de dados de arquivamento</span><span class="sxs-lookup"><span data-stu-id="19a1b-156">Error reports from the archiving database</span></span>

<span data-ttu-id="19a1b-157">Para ajudar a organizar o desempenho das tarefas necessárias, consulte As-Needed lista de verificação de operações.</span><span class="sxs-lookup"><span data-stu-id="19a1b-157">To help organize the performance of as-needed tasks, see As-Needed Operations Checklist.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="19a1b-158">Para obter procedimentos detalhados de administração e gerenciamento, consulte o guia de administração do Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="19a1b-158">For detailed administration and management procedures, see the Microsoft Lync Server 2013 Administration Guide.</span></span>



</div>

<div>

## <a name="backup-and-restore-policies-or-configuration-settings"></a><span data-ttu-id="19a1b-159">Políticas de backup (e restauração) ou configurações de configuração</span><span class="sxs-lookup"><span data-stu-id="19a1b-159">Backup (and restore) policies or configuration settings</span></span>

<span data-ttu-id="19a1b-160">O Lync Server 2013 permite que você faça backup e restaure todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="19a1b-160">Lync Server 2013 lets you back up and restore the whole system.</span></span> <span data-ttu-id="19a1b-161">IIf que você deseja fazer backup (e, em seguida, talvez um dia restaurar) uma única política ou um único conjunto de configurações, recuperar a política apropriada e, em seguida, canalizar esse objeto para o cmdlet Export-Clixml, que salva as informações da política como um arquivo XML:</span><span class="sxs-lookup"><span data-stu-id="19a1b-161">Iif you want to back up (and then maybe someday restore) a single policy or a single collection of configuration settings, retrieve the appropriate policy, and then pipe that object to the Export-Clixml cmdlet, which saves the policy information as an XML file:</span></span>

`Get-CsClientPolicy -Identity "RedmondClientPolicy" | Export-Clixml -Path C:\Backup\RedmondClientPolicy.xml`

<span data-ttu-id="19a1b-162">Agora você pode experimentar o RedmondClientPolicy e alterar muitas das configurações.</span><span class="sxs-lookup"><span data-stu-id="19a1b-162">You may now experiment with RedmondClientPolicy and change lots of the settings.</span></span> <span data-ttu-id="19a1b-163">Se, em vez disso, você decidir restaurar a política antiga, digite:</span><span class="sxs-lookup"><span data-stu-id="19a1b-163">If you decide instead to restore the old policy, enter:</span></span>

`$x = Import-Clixml -Path C:\Backup\RedmondClientPolicy.xml`

`Set-CsClientPolicy -Instance $x`

<span data-ttu-id="19a1b-164">Observe que essa abordagem funciona para a maioria das políticas e configurações, mas não funciona com alguns dos itens mais complexos, itens que contêm vários subobjetos (como as configurações de roteamento, que contêm muitas rotas de voz separadas).</span><span class="sxs-lookup"><span data-stu-id="19a1b-164">Note that this approach will work for most policies and settings but it won't work with some of the more complex items—items that contain multiple sub-objects (like routing configuration settings, which contain many separate voice routes).</span></span>

<span data-ttu-id="19a1b-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="19a1b-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

