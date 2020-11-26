---
title: 'Lync Server 2013: Exclusões de verificação de antivírus'
description: 'Lync Server 2013: exclusões de verificação antivírus.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Antivirus scanning exclusions for Lync Server 2013
ms:assetid: 71e1f1cc-2d16-4111-9864-9276bf24dfe0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440138(v=OCS.15)
ms:contentKeyID: 57793042
ms.date: 11/03/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20c395f529cad91993d003efdeb231bd66f4b9bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440658"
---
# <a name="antivirus-scanning-exclusions-for-lync-server-2013"></a><span data-ttu-id="a6baa-103">Exclusões de verificação de antivírus para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6baa-103">Antivirus scanning exclusions for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6baa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6baa-104">

<span> </span></span></span>

<span data-ttu-id="a6baa-105">_**Tópico da última modificação:** 2015-11-02_</span><span class="sxs-lookup"><span data-stu-id="a6baa-105">_**Topic Last Modified:** 2015-11-02_</span></span>

<span data-ttu-id="a6baa-106">Para garantir que o scanner antivírus não interfira com a operação do Lync Server 2013, você deve excluir processos e pastas específicos para cada função de servidor ou servidor do Lync Server 2013 na qual você executa um verificador de vírus.</span><span class="sxs-lookup"><span data-stu-id="a6baa-106">To ensure that the antivirus scanner does not interfere with the operation of Lync Server 2013, you must exclude specific processes and directories for each Lync Server 2013 server or server role on which you run an antivirus scanner.</span></span> <span data-ttu-id="a6baa-107">Os seguintes processos e diretórios devem ser excluídos:</span><span class="sxs-lookup"><span data-stu-id="a6baa-107">The following processes and directories should be excluded:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a6baa-108">Os locais de pasta e arquivo listados abaixo são os locais padrão do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a6baa-108">Folder and file locations listed below are the default locations for Lync Server 2013.</span></span> <span data-ttu-id="a6baa-109">Para quaisquer locais, para os quais você não usa o padrão, exclua os locais que você especificou para a sua organização em vez dos locais padrão especificados neste tópico.</span><span class="sxs-lookup"><span data-stu-id="a6baa-109">For any locations for which you did not use the default, exclude the locations you specified for your organization instead of the default locations specified in this topic.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a6baa-110">Observe que alguns programas antivírus podem precisar de caminhos absolutos e não relativos, para a sua lista de exclusão.</span><span class="sxs-lookup"><span data-stu-id="a6baa-110">Please note that some antivirus programs may need absolute, not relative paths, for their exclusion list.</span></span>



</div>

  - <span data-ttu-id="a6baa-111">Processos do Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="a6baa-111">Lync Server 2013 processes:</span></span>
    
      - <span data-ttu-id="a6baa-112">ABServer.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-112">ABServer.exe</span></span>
    
      - <span data-ttu-id="a6baa-113">AcpMcuSvc.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-113">AcpMcuSvc.exe</span></span>
    
      - <span data-ttu-id="a6baa-114">ASMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-114">ASMCUSvc.exe</span></span>
    
      - <span data-ttu-id="a6baa-115">AVMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-115">AVMCUSvc.exe</span></span>
    
      - <span data-ttu-id="a6baa-116">ChannelService.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-116">ChannelService.exe</span></span>
    
      - <span data-ttu-id="a6baa-117">ClsAgent.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-117">ClsAgent.exe</span></span>
    
      - <span data-ttu-id="a6baa-118">ComplianceService.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-118">ComplianceService.exe</span></span>
    
      - <span data-ttu-id="a6baa-119">DataMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-119">DataMCUSvc.exe</span></span>
    
      - <span data-ttu-id="a6baa-120">DataProxy.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-120">DataProxy.exe</span></span>
    
      - <span data-ttu-id="a6baa-121">FileTransferAgent.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-121">FileTransferAgent.exe</span></span>
    
      - <span data-ttu-id="a6baa-122">IMMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-122">IMMCUSvc.exe</span></span>
    
      - <span data-ttu-id="a6baa-123">LysSvc.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-123">LysSvc.exe</span></span>
    
      - <span data-ttu-id="a6baa-124">MasterReplicatorAgent.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-124">MasterReplicatorAgent.exe</span></span>
    
      - <span data-ttu-id="a6baa-125">MediaRelaySvc.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-125">MediaRelaySvc.exe</span></span>
    
      - <span data-ttu-id="a6baa-126">MediationServerSvc.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-126">MediationServerSvc.exe</span></span>
    
      - <span data-ttu-id="a6baa-127">MRASSvc.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-127">MRASSvc.exe</span></span>
    
      - <span data-ttu-id="a6baa-128">OcsAppServerHost.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-128">OcsAppServerHost.exe</span></span>
    
      - <span data-ttu-id="a6baa-129">ReplicaReplicatorAgent.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-129">ReplicaReplicatorAgent.exe</span></span>
    
      - <span data-ttu-id="a6baa-130">ReplicationApp.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-130">ReplicationApp.exe</span></span>
    
      - <span data-ttu-id="a6baa-131">RtcHost.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-131">RtcHost.exe</span></span>
    
      - <span data-ttu-id="a6baa-132">RTCSrv.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-132">RTCSrv.exe</span></span>
    
      - <span data-ttu-id="a6baa-133">XmppProxy.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-133">XmppProxy.exe</span></span>
    
      - <span data-ttu-id="a6baa-134">XmppTGW.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-134">XmppTGW.exe</span></span>

  - <span data-ttu-id="a6baa-135">Processos de Serviço de Host do Windows Fabric:</span><span class="sxs-lookup"><span data-stu-id="a6baa-135">Windows Fabric Host Service processes:</span></span>
    
      - <span data-ttu-id="a6baa-136">Fabric.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-136">Fabric.exe</span></span>
    
      - <span data-ttu-id="a6baa-137">FabricDCA.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-137">FabricDCA.exe</span></span>
    
      - <span data-ttu-id="a6baa-138">FabricHost.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-138">FabricHost.exe</span></span>

  - <span data-ttu-id="a6baa-139">Processos IIS:</span><span class="sxs-lookup"><span data-stu-id="a6baa-139">IIS processes:</span></span>
    
      - <span data-ttu-id="a6baa-140">% SystemRoot% \\ System32 \\ inetsrv \\w3wp.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-140">%systemroot%\\system32\\inetsrv\\w3wp.exe</span></span>
    
      - <span data-ttu-id="a6baa-141">% SystemRoot% \\ SysWOW64 \\ inetsrv \\w3wp.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-141">%systemroot%\\SysWOW64\\inetsrv\\w3wp.exe</span></span>

  - <span data-ttu-id="a6baa-142">Processos SQL Server Back-End:</span><span class="sxs-lookup"><span data-stu-id="a6baa-142">SQL Server Back-End processes:</span></span>
    
      - <span data-ttu-id="a6baa-143">% ProgramFiles% \\ Microsoft SQL Server \\ MSSQL11. MSSQLSERVER \\ MSSQL \\ Binn \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-143">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.MSSQLSERVER\\MSSQL\\Binn\\SQLServr.exe</span></span>
    
      - <span data-ttu-id="a6baa-144">% ProgramFiles% \\ Microsoft SQL Server \\ MSRS11. O \\ Reporting Services \\ ReportServer \\ bin \\ReportingServicesService.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-144">%ProgramFiles%\\Microsoft SQL Server\\MSRS11.MSSQLSERVER\\Reporting Services\\ReportServer\\Bin\\ReportingServicesService.exe</span></span>
    
      - <span data-ttu-id="a6baa-145">% ProgramFiles% \\ Microsoft SQL Server \\ MSAS11.MSMDSrv.exe da lixeira do MSSQLSERVER \\ OLAP \\ \\</span><span class="sxs-lookup"><span data-stu-id="a6baa-145">%ProgramFiles%\\Microsoft SQL Server\\MSAS11.MSSQLSERVER\\OLAP\\Bin\\MSMDSrv.exe</span></span>

  - <span data-ttu-id="a6baa-146">Processos SQL Server Front-End:</span><span class="sxs-lookup"><span data-stu-id="a6baa-146">SQL Server Front-End processes:</span></span>
    
      - <span data-ttu-id="a6baa-147">% ProgramFiles% \\ Microsoft SQL Server \\ MSSQL11. LYNCLOCAL \\ MSSQL \\ Binn \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-147">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.LYNCLOCAL\\MSSQL\\Binn\\SQLServr.exe</span></span>
    
      - <span data-ttu-id="a6baa-148">% ProgramFiles% \\ Microsoft SQL Server \\ MSSQL11. RTCLOCAL \\ MSSQL \\ Binn \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="a6baa-148">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.RTCLOCAL\\MSSQL\\Binn\\SQLServr.exe</span></span>

  - <span data-ttu-id="a6baa-149">Diretórios e arquivos:</span><span class="sxs-lookup"><span data-stu-id="a6baa-149">Directories and files:</span></span>
    
      - <span data-ttu-id="a6baa-150">% SystemRoot% \\ System32 \\ LogFiles</span><span class="sxs-lookup"><span data-stu-id="a6baa-150">%systemroot%\\System32\\LogFiles</span></span>
    
      - <span data-ttu-id="a6baa-151">% SystemRoot% \\ SysWOW64 \\ LogFiles</span><span class="sxs-lookup"><span data-stu-id="a6baa-151">%systemroot%\\SysWow64\\LogFiles</span></span>
    
      - <span data-ttu-id="a6baa-152">% SystemRoot% \\ Microsoft.NET \\ assembly \\ GAC \_ MSIL</span><span class="sxs-lookup"><span data-stu-id="a6baa-152">%systemroot%\\Microsoft.NET\\assembly\\GAC\_MSIL</span></span>
    
      - <span data-ttu-id="a6baa-153">% ProgramFiles% \\ Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6baa-153">%programfiles%\\Microsoft Lync Server 2013</span></span>
    
      - <span data-ttu-id="a6baa-154">% ProgramFiles% \\ Arquivos comuns \\ \\ nó do Inspetor do Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6baa-154">%programfiles%\\Common Files\\Microsoft Lync Server 2013\\Watcher Node</span></span>
    
      - <span data-ttu-id="a6baa-155">% ProgramFiles% \\ Arquivos comuns \\ Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6baa-155">%programfiles%\\Common Files\\Microsoft Lync Server 2013</span></span>
    
      - <span data-ttu-id="a6baa-156">% SystemDrive% \\ RtcReplicaRoot</span><span class="sxs-lookup"><span data-stu-id="a6baa-156">%SystemDrive%\\RtcReplicaRoot</span></span>
    
      - <span data-ttu-id="a6baa-157">Repositório de compartilhamento de arquivo(específico no Construtor de Topologias).</span><span class="sxs-lookup"><span data-stu-id="a6baa-157">File share store (specified in Topology Builder).</span></span> <span data-ttu-id="a6baa-158">Os repositórios de arquivos são especificados no Construtor de Topologias.</span><span class="sxs-lookup"><span data-stu-id="a6baa-158">File stores are specified in Topology Builder.</span></span>
    
      - <span data-ttu-id="a6baa-159">Os arquivos de logs e dados do SQL Server, incluindo aqueles para o banco de dados de back-end, armazenamento de usuário, arquivamento, monitoramento, e repositório de application.</span><span class="sxs-lookup"><span data-stu-id="a6baa-159">SQL Server data and log files, including those for the back-end database, user store, archiving store, monitoring store, and application store.</span></span> <span data-ttu-id="a6baa-160">Os arquivos da base de dados e os logs podem ser especificados no Construtor de Topologias.</span><span class="sxs-lookup"><span data-stu-id="a6baa-160">Database and log files can be specified in Topology Builder.</span></span> <span data-ttu-id="a6baa-161">Para obter detalhes sobre os dados e arquivos de log para cada banco de dados, incluindo nomes padrão, consulte [dados do SQL Server e posicionamento do arquivo de log para o Lync Server 2013](lync-server-2013-sql-server-data-and-log-file-placement.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="a6baa-161">For details about the data and log files for each database, including default names, see [SQL Server data and log file placement for Lync Server 2013](lync-server-2013-sql-server-data-and-log-file-placement.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="a6baa-162">Dados e arquivos de log do SQL Server, incluindo aqueles para o banco de dados front-end, a loja do Lync e a loja do RtcDatabase.</span><span class="sxs-lookup"><span data-stu-id="a6baa-162">SQL Server data and log files, including those for the Front-end database, Lync store, and RtcDatabase store.</span></span> <span data-ttu-id="a6baa-163">Eles estão normalmente em% Unidade_Local% \\ CSData.</span><span class="sxs-lookup"><span data-stu-id="a6baa-163">They are normally under %localdrive%\\CSData.</span></span>

<span data-ttu-id="a6baa-164"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6baa-164"></div>

<span> </span>

</div>

</div>

</span></span></div>

