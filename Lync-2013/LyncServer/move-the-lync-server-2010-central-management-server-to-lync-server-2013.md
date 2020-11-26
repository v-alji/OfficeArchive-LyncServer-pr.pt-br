---
title: Mover o servidor de gerenciamento central do Lync Server 2010 para o Lync Server 2013
description: Mova o servidor de gerenciamento central do Lync Server 2010 para o Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Move the Lync Server 2010 Central Management Server to Lync Server 2013
ms:assetid: 30cc98f2-1916-4dbe-99d0-8df5368ed3ec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688013(v=OCS.15)
ms:contentKeyID: 49733602
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 19d53d797375b1eb8fde72f6b999e509b97f85ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443290"
---
# <a name="move-the-lync-server-2010-central-management-server-to-lync-server-2013"></a><span data-ttu-id="c27ee-103">Mover o servidor de gerenciamento central do Lync Server 2010 para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c27ee-103">Move the Lync Server 2010 Central Management Server to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c27ee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c27ee-104">

<span> </span></span></span>

<span data-ttu-id="c27ee-105">_**Tópico da última modificação:** 2013-11-25_</span><span class="sxs-lookup"><span data-stu-id="c27ee-105">_**Topic Last Modified:** 2013-11-25_</span></span>

<span data-ttu-id="c27ee-106">Após a migração do Lync Server 2010 para o Lync Server 2013, você precisa mover o servidor de gerenciamento central do Lync Server 2010 para o servidor ou o pool de front-end do Lync Server 2013 para poder remover o servidor herdado do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c27ee-106">After migrating from Lync Server 2010 to Lync Server 2013, you need to move the Lync Server 2010 Central Management Server to the Lync Server 2013 Front End Server or pool, before you can remove the legacy Lync Server 2010 server.</span></span>

<span data-ttu-id="c27ee-107">O servidor de gerenciamento central é um único sistema de réplica mestra/múltipla, em que a cópia de leitura/gravação do banco de dados é mantida pelo servidor front-end que contém o servidor de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="c27ee-107">The Central Management Server is a single master/multiple replica system, where the read/write copy of the database is held by the Front End Server that contains the Central Management Server.</span></span> <span data-ttu-id="c27ee-108">Cada computador na topologia, incluindo o servidor front-end que contém o servidor de gerenciamento central, tem uma cópia somente leitura dos dados do repositório de gerenciamento central no banco de dados do SQL Server (chamado RTCLOCAL por padrão) instalado no computador durante a instalação e a implantação.</span><span class="sxs-lookup"><span data-stu-id="c27ee-108">Each computer in the topology, including the Front End Server that contains the Central Management Server, has a read-only copy of the Central Management store data in the SQL Server database (named RTCLOCAL by default) installed on the computer during setup and deployment.</span></span> <span data-ttu-id="c27ee-109">O banco de dados local recebe atualizações de réplica por meio do agente duplicador de réplica do Lync Server que é executado como um serviço em todos os computadores.</span><span class="sxs-lookup"><span data-stu-id="c27ee-109">The local database receives replica updates by way of the Lync Server Replica Replicator Agent that runs as a service on all computers.</span></span> <span data-ttu-id="c27ee-110">O nome do banco de dados real no servidor de gerenciamento central e na réplica local é XDS, que é composto pelos arquivos XDS. MDF e XDS. ldf.</span><span class="sxs-lookup"><span data-stu-id="c27ee-110">The name of the actual database on the Central Management Server and the local replica is XDS, which is made up of the xds.mdf and xds.ldf files.</span></span> <span data-ttu-id="c27ee-111">O local do banco de dados mestre é referenciado por um ponto de controle de serviço (SCP) nos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c27ee-111">The master database location is referenced by a service control point (SCP) in Active Directory Domain Services.</span></span> <span data-ttu-id="c27ee-112">Todas as ferramentas que usam o servidor de gerenciamento central para gerenciar e configurar o Lync Server usam o SCP para localizar o repositório de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="c27ee-112">All tools that use the Central Management Server to manage and configure Lync Server use the SCP to locate the Central Management store.</span></span>

<span data-ttu-id="c27ee-113">Depois de mover com êxito o servidor de gerenciamento central, você deve remover os bancos de dados do servidor de gerenciamento central do servidor front-end original.</span><span class="sxs-lookup"><span data-stu-id="c27ee-113">After you have successfully moved the Central Management Server, you should remove the Central Management Server databases from the original Front End Server.</span></span> <span data-ttu-id="c27ee-114">Para obter informações sobre como remover os bancos de dados do servidor de gerenciamento central, consulte [remover o banco de dados do SQL Server de um pool de front-ends](remove-the-sql-server-database-for-a-front-end-pool.md).</span><span class="sxs-lookup"><span data-stu-id="c27ee-114">For information on removing the Central Management Server databases, see [Remove the SQL Server database for a Front End pool](remove-the-sql-server-database-for-a-front-end-pool.md).</span></span>

<span data-ttu-id="c27ee-115">Use o cmdlet **move-CsManagementServer** do Windows PowerShell no Shell de gerenciamento do Lync Server para mover o banco de dados do banco de dados do SQL Server do lync Server 2010 para o banco de dados do lync Server 2013 SQL Server e, em seguida, atualizar o scp para apontar para o local do servidor de gerenciamento central do lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c27ee-115">You use the Windows PowerShell cmdlet **Move-CsManagementServer** in the Lync Server Management Shell to move the database from the Lync Server 2010 SQL Server database to the Lync Server 2013 SQL Server database, and then update the SCP to point to the Lync Server 2013 Central Management Server location.</span></span>

<div>

## <a name="preparing-lync-server-2013-front-end-servers-before-moving-the-central-management-server"></a><span data-ttu-id="c27ee-116">Preparando os servidores de front-end do Lync Server 2013 antes de mover o servidor central de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="c27ee-116">Preparing Lync Server 2013 Front End Servers before moving the Central Management Server</span></span>

<span data-ttu-id="c27ee-117">Use os procedimentos desta seção para preparar os servidores front-end do Lync Server 2013 antes de mover o servidor de gerenciamento central do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c27ee-117">Use the procedures in this section to prepare the Lync Server 2013 Front End Servers before you move the Lync Server 2010 Central Management Server.</span></span>

<div>

## <a name="to-prepare-an-enterprise-edition-front-end-pool"></a><span data-ttu-id="c27ee-118">Para preparar um pool de front-end do Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="c27ee-118">To prepare an Enterprise Edition Front End pool</span></span>

1.  <span data-ttu-id="c27ee-119">No pool de front-ends do Lync Server 2013 Enterprise Edition onde você deseja realocar o servidor de gerenciamento central: faça logon no computador em que o Shell de gerenciamento do Lync Server está instalado como membro do grupo **RTCUniversalServerAdmins** .</span><span class="sxs-lookup"><span data-stu-id="c27ee-119">On the Lync Server 2013 Enterprise Edition Front End pool where you want to relocate the Central Management Server: Log on to the computer where the Lync Server Management Shell is installed as a member of the **RTCUniversalServerAdmins** group.</span></span> <span data-ttu-id="c27ee-120">Você também deve ter direitos de usuário e permissões do banco de dados do SQL Server sysadmin no banco de dados onde deseja instalar o repositório de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="c27ee-120">You must also have SQL Server database sysadmin user rights and permissions on the database where you want to install the Central Management store.</span></span>

2.  <span data-ttu-id="c27ee-121">Abra o Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c27ee-121">Open the Lync Server Management Shell.</span></span>

3.  <span data-ttu-id="c27ee-122">Para criar o novo repositório de gerenciamento central no banco de dados do SQL Server do Lync Server 2013, no Shell de gerenciamento do Lync Server, digite:</span><span class="sxs-lookup"><span data-stu-id="c27ee-122">To create the new Central Management store in the Lync Server 2013 SQL Server database, in the Lync Server Management Shell, type:</span></span>
    
        Install-CsDatabase -CentralManagementDatabase -SQLServerFQDN <FQDN of your SQL Server> -SQLInstanceName <name of instance>

4.  <span data-ttu-id="c27ee-123">Confirme se o status do serviço **front-end do Lync Server** foi **iniciado**.</span><span class="sxs-lookup"><span data-stu-id="c27ee-123">Confirm that the status of the **Lync Server Front-End** service is **Started**.</span></span>

</div>

<div>

## <a name="to-prepare-a-standard-edition-front-end-server"></a><span data-ttu-id="c27ee-124">Para preparar um servidor front-end padrão da edição</span><span class="sxs-lookup"><span data-stu-id="c27ee-124">To prepare a Standard Edition Front End Server</span></span>

1.  <span data-ttu-id="c27ee-125">No servidor front-end do Lync Server 2013 Standard Edition no qual você deseja realocar o servidor de gerenciamento central: faça logon no computador em que o Shell de gerenciamento do Lync Server está instalado como membro do grupo **RTCUniversalServerAdmins** .</span><span class="sxs-lookup"><span data-stu-id="c27ee-125">On the Lync Server 2013 Standard Edition Front End Server where you want to relocate the Central Management Server: Log on to the computer where the Lync Server Management Shell is installed as a member of the **RTCUniversalServerAdmins** group.</span></span>

2.  <span data-ttu-id="c27ee-126">Abra o assistente de implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c27ee-126">Open the Lync Server Deployment Wizard.</span></span>

3.  <span data-ttu-id="c27ee-127">No assistente de implantação do Lync Server, clique em **preparar primeiro servidor Standard Edition**.</span><span class="sxs-lookup"><span data-stu-id="c27ee-127">In the Lync Server Deployment Wizard, click **Prepare first Standard Edition server**.</span></span>

4.  <span data-ttu-id="c27ee-128">Na página **comandos em execução** , o SQL Server Express é instalado como o servidor de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="c27ee-128">On the **Executing Commands** page, SQL Server Express is installed as the Central Management Server.</span></span> <span data-ttu-id="c27ee-129">Regras de firewall necessárias são criadas.</span><span class="sxs-lookup"><span data-stu-id="c27ee-129">Necessary firewall rules are created.</span></span> <span data-ttu-id="c27ee-130">Quando a instalação do banco de dados e do software de pré-requisito estiver concluída, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="c27ee-130">When the installation of the database and prerequisite software is completed, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c27ee-131">A instalação inicial pode levar algum tempo sem atualizações visíveis para a tela Resumo da saída do comando.</span><span class="sxs-lookup"><span data-stu-id="c27ee-131">The initial installation may take some time with no visible updates to the command output summary screen.</span></span> <span data-ttu-id="c27ee-132">Isso se deve à instalação do SQL Server Express.</span><span class="sxs-lookup"><span data-stu-id="c27ee-132">This is due to the installation of the SQL Server Express.</span></span> <span data-ttu-id="c27ee-133">Se você precisar monitorar a instalação do banco de dados, use o Gerenciador de tarefas para monitorar a configuração.</span><span class="sxs-lookup"><span data-stu-id="c27ee-133">If you need to monitor the installation of the database, use Task Manager to monitor the setup.</span></span>

    
    </div>

5.  <span data-ttu-id="c27ee-134">Para criar o novo repositório de gerenciamento central no servidor front-end do Lync Server 2013 Standard Edition, no Shell de gerenciamento do Lync Server, digite:</span><span class="sxs-lookup"><span data-stu-id="c27ee-134">To create the new Central Management store on the Lync Server 2013 Standard Edition Front End Server, in the Lync Server Management Shell, type:</span></span>
    
        Install-CsDatabase -CentralManagementDatabase -SQLServerFQDN <FQDN of your Standard Edition Server> -SQLInstanceName <name of instance - RTC by default>

6.  <span data-ttu-id="c27ee-135">Confirme se o status do serviço **front-end do Lync Server** foi **iniciado**.</span><span class="sxs-lookup"><span data-stu-id="c27ee-135">Confirm that the status of the **Lync Server Front-End** service is **Started**.</span></span>

</div>

</div>

<div>

## <a name="to-move-the-lync-server-2010-central-management-server-to-lync-server-2013"></a><span data-ttu-id="c27ee-136">Para mover o servidor de gerenciamento central do Lync Server 2010 para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c27ee-136">To move the Lync Server 2010 Central Management Server to Lync Server 2013</span></span>

1.  <span data-ttu-id="c27ee-137">No servidor do Lync Server 2013 que será o servidor de gerenciamento central: faça logon no computador em que o Shell de gerenciamento do Lync Server está instalado como membro do grupo **RTCUniversalServerAdmins** .</span><span class="sxs-lookup"><span data-stu-id="c27ee-137">On the Lync Server 2013 server that will be the Central Management Server: Log on to the computer where the Lync Server Management Shell is installed as a member of the **RTCUniversalServerAdmins** group.</span></span> <span data-ttu-id="c27ee-138">Você também deve ter direitos de usuário e permissões de administrador de banco de dados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c27ee-138">You must also have the SQL Server database administrator user rights and permissions.</span></span>

2.  <span data-ttu-id="c27ee-139">Abra o Shell de Gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c27ee-139">Open Lync Server Management Shell.</span></span>

3.  <span data-ttu-id="c27ee-140">No Shell de gerenciamento do Lync Server, digite:</span><span class="sxs-lookup"><span data-stu-id="c27ee-140">In the Lync Server Management Shell, type:</span></span>
    
        Enable-CsTopology
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="c27ee-141">Se <CODE>Enable-CsTopology</CODE> o problema não for bem-sucedido, resolva o problema para impedir que o comando seja concluído antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="c27ee-141">If <CODE>Enable-CsTopology</CODE> is not successful, resolve the problem preventing the command from completing before continuing.</span></span> <span data-ttu-id="c27ee-142">Se <STRONG>Enable-CsTopology</STRONG> não for bem-sucedido, a mudança falhará e poderá deixar a sua topologia em um estado em que não haja repositório de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="c27ee-142">If <STRONG>Enable-CsTopology</STRONG> is not successful, the move will fail and it may leave your topology in a state where there is no Central Management store.</span></span>

    
    </div>

4.  <span data-ttu-id="c27ee-143">No servidor front-end do Lync Server 2013 ou no pool de front-end, no Shell de gerenciamento do Lync Server, digite:</span><span class="sxs-lookup"><span data-stu-id="c27ee-143">On the Lync Server 2013 Front End Server or Front End pool, in the Lync Server Management Shell, type:</span></span>
    
        Move-CsManagementServer

5.  <span data-ttu-id="c27ee-144">O Shell de gerenciamento do Lync Server exibe os servidores, armazenamentos de arquivos, repositórios de banco de dados e os pontos de conexão de serviço do estado atual e o Estado proposto.</span><span class="sxs-lookup"><span data-stu-id="c27ee-144">Lync Server Management Shell displays the servers, file stores, database stores, and the service connection points of the Current State and the Proposed State.</span></span> <span data-ttu-id="c27ee-145">Leia as informações com atenção e confirme se essa é a origem e o destino pretendidos.</span><span class="sxs-lookup"><span data-stu-id="c27ee-145">Read the information carefully and confirm that this is the intended source and destination.</span></span> <span data-ttu-id="c27ee-146">Digite **Y** para continuar ou **N** para interromper a movimentação.</span><span class="sxs-lookup"><span data-stu-id="c27ee-146">Type **Y** to continue, or **N** to stop the move.</span></span>

6.  <span data-ttu-id="c27ee-147">Revise todos os avisos ou erros gerados pelo comando **mover-CsManagementServer** e resolva-os.</span><span class="sxs-lookup"><span data-stu-id="c27ee-147">Review any warnings or errors generated by the **Move-CsManagementServer** command and resolve them.</span></span>

7.  <span data-ttu-id="c27ee-148">No servidor do Lync Server 2013, abra o assistente de implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c27ee-148">On the Lync Server 2013 server, open the Lync Server Deployment Wizard.</span></span>

8.  <span data-ttu-id="c27ee-149">No assistente de implantação do Lync Server, clique em **instalar ou atualizar o sistema do Lync Server**, clique em **etapa 2: configurar ou remover componentes do Lync Server**, clique em **Avançar**, examine o resumo e clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="c27ee-149">In Lync Server Deployment Wizard, click **Install or Update Lync Server System**, click **Step 2: Setup or Remove Lync Server Components**, click **Next**, review the summary, and then click **Finish**.</span></span>

9.  <span data-ttu-id="c27ee-150">No servidor do Lync Server 2010, abra o assistente de implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c27ee-150">On the Lync Server 2010 server, open the Lync Server Deployment Wizard.</span></span>

10. <span data-ttu-id="c27ee-151">No assistente de implantação do Lync Server, clique em **instalar ou atualizar o sistema do Lync Server**, clique em **etapa 2: configurar ou remover componentes do Lync Server**, clique em **Avançar**, examine o resumo e clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="c27ee-151">In Lync Server Deployment Wizard, click **Install or Update Lync Server System**, click **Step 2: Setup or Remove Lync Server Components**, click **Next**, review the summary, and then click **Finish**.</span></span>

11. <span data-ttu-id="c27ee-152">Reinicie o servidor do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c27ee-152">Reboot the Lync Server 2013 server.</span></span> <span data-ttu-id="c27ee-153">Isso é necessário devido a uma alteração de associação do grupo para acessar o banco de dados do servidor de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="c27ee-153">This is required because of a group membership change to access Central Management Server database.</span></span>

12. <span data-ttu-id="c27ee-154">Para confirmar se a replicação com o novo repositório de gerenciamento central está ocorrendo, no Shell de gerenciamento do Lync Server, digite:</span><span class="sxs-lookup"><span data-stu-id="c27ee-154">To confirm that replication with the new Central Management store is occurring, in the Lync Server Management Shell, type:</span></span>
    
        Get-CsManagementStoreReplicationStatus
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c27ee-155">A replicação pode levar algum tempo para atualizar todas as réplicas atuais.</span><span class="sxs-lookup"><span data-stu-id="c27ee-155">The replication may take some time to update all current replicas.</span></span>

    
    </div>

</div>

<div>

## <a name="to-remove-lync-server-2010-central-management-store-files-after-a-move"></a><span data-ttu-id="c27ee-156">Para remover arquivos do repositório central de gerenciamento do Lync Server 2010 após uma mudança</span><span class="sxs-lookup"><span data-stu-id="c27ee-156">To remove Lync Server 2010 Central Management store files after a move</span></span>

1.  <span data-ttu-id="c27ee-157">No servidor do Lync Server 2010: faça logon no computador em que o Shell de gerenciamento do Lync Server está instalado como membro do grupo **RTCUniversalServerAdmins** .</span><span class="sxs-lookup"><span data-stu-id="c27ee-157">On the Lync Server 2010 server: Log on to the computer where the Lync Server Management Shell is installed as a member of the **RTCUniversalServerAdmins** group.</span></span> <span data-ttu-id="c27ee-158">Você também deve ter direitos de usuário e permissões de administrador de banco de dados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c27ee-158">You must also have the SQL Server database administrator user rights and permissions.</span></span>

2.  <span data-ttu-id="c27ee-159">Abrir o Shell de gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="c27ee-159">Open Lync Server Management Shell</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="c27ee-160">Não prossiga com a remoção dos arquivos de banco de dados anteriores até que a replicação seja concluída e seja estável.</span><span class="sxs-lookup"><span data-stu-id="c27ee-160">Do not proceed with the removal of the previous database files until replication is complete and is stable.</span></span> <span data-ttu-id="c27ee-161">Se você remover os arquivos antes de concluir a replicação, irá interromper o processo de replicação e deixar o servidor de gerenciamento central recentemente movido em um estado desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c27ee-161">If you remove the files prior to completing replication, you will disrupt the replication process and leave the newly moved Central Management Server in an unknown state.</span></span> <span data-ttu-id="c27ee-162">Use o cmdlet <STRONG>Get-CsManagementStoreReplicationStatus</STRONG> para confirmar o status de replicação.</span><span class="sxs-lookup"><span data-stu-id="c27ee-162">Use the cmdlet <STRONG>Get-CsManagementStoreReplicationStatus</STRONG> to confirm the replication status.</span></span>

    
    </div>

3.  <span data-ttu-id="c27ee-163">Para remover os arquivos de banco de dados do repositório de gerenciamento central do servidor do Lync Server 2010 central Management, digite:</span><span class="sxs-lookup"><span data-stu-id="c27ee-163">To remove the Central Management store database files from the Lync Server 2010 Central Management Server, type:</span></span>
    
        Uninstall-CsDatabase -CentralManagementDatabase -SqlServerFqdn <FQDN of SQL Server> -SqlInstanceName <Name of source server>
    
    <span data-ttu-id="c27ee-164">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c27ee-164">For example:</span></span>
    
        Uninstall-CsDatabase -CentralManagementDatabase -SqlServerFqdn sql.contoso.net -SqlInstanceName rtc
    
    <span data-ttu-id="c27ee-165">Onde \<FQDN of SQL Server\> está o servidor back-end do Lync Server 2010 em uma implantação Enterprise Edition ou o FQDN do servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="c27ee-165">Where the \<FQDN of SQL Server\> is either the Lync Server 2010 Back End Server in an Enterprise Edition deployment or the FQDN of the Standard Edition server.</span></span>

<span data-ttu-id="c27ee-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c27ee-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

