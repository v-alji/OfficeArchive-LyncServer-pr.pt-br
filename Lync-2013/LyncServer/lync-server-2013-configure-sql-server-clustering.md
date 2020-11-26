---
title: 'Lync Server 2013: configurar o agrupamento do SQL Server'
description: 'Lync Server 2013: configurar o agrupamento do SQL Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure SQL Server clustering
ms:assetid: d7b52ef1-573c-48ed-bb94-34e37b49645c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn383982(v=OCS.15)
ms:contentKeyID: 56472032
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1f4b81b62d086de27659f564427ad6adde99ecac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433742"
---
# <a name="configure-sql-server-clustering-for-lync-server-2013"></a><span data-ttu-id="dc881-103">Configurar o cluster do SQL Server para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc881-103">Configure SQL Server clustering for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dc881-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dc881-104">

<span> </span></span></span>

<span data-ttu-id="dc881-105">_**Tópico da última modificação:** 2014-01-10_</span><span class="sxs-lookup"><span data-stu-id="dc881-105">_**Topic Last Modified:** 2014-01-10_</span></span>

<span data-ttu-id="dc881-106">O Microsoft Lync Server 2013 suporta clustering para SQL Server 2012 e SQL Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="dc881-106">Microsoft Lync Server 2013 supports clustering for SQL Server 2012 and SQL Server 2008 R2.</span></span> <span data-ttu-id="dc881-107">Para obter detalhes sobre o que é suportado, consulte [suporte a software de banco de dados no Lync Server 2013](lync-server-2013-database-software-support.md).</span><span class="sxs-lookup"><span data-stu-id="dc881-107">For details about what is supported, see [Database software support in Lync Server 2013](lync-server-2013-database-software-support.md).</span></span>

<span data-ttu-id="dc881-108">Você deve configurar e configurar o cluster do SQL Server antes de instalar e implantar o servidor front-end do Enterprise Edition e o banco de dados back-end.</span><span class="sxs-lookup"><span data-stu-id="dc881-108">You should set up and configure the SQL Server cluster before you install and deploy the Enterprise Edition Front End Server and back-end database.</span></span> <span data-ttu-id="dc881-109">Para obter práticas recomendadas e instruções de configuração para clustering de failover no SQL Server 2012, consulte <https://technet.microsoft.com/library/hh231721.aspx> .</span><span class="sxs-lookup"><span data-stu-id="dc881-109">For best practices and setup instructions for failover clustering in SQL Server 2012, see <https://technet.microsoft.com/library/hh231721.aspx>.</span></span> <span data-ttu-id="dc881-110">Para o cluster de failover no SQL Server 2008, consulte <https://technet.microsoft.com/library/ms189134(v=sql.105).aspx> .</span><span class="sxs-lookup"><span data-stu-id="dc881-110">For failover clustering in SQL Server 2008, see <https://technet.microsoft.com/library/ms189134(v=sql.105).aspx>.</span></span>

<span data-ttu-id="dc881-p103">Ao instalar o SQL Server, o SQL Server Management Studio deve ser instalado para gerenciar os locais de bases de dados e arquivos de log. O SQL Server Management Studio é instalado como componente opcional quando da instalação do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dc881-p103">When you install SQL Server, you should install SQL Server Management Studio to manage the locations for database and log file locations. SQL Server Management Studio is installed as an optional component when you install SQL Server.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="dc881-113">Para instalar e implantar os bancos de dados no servidor baseado no SQL Server, você deve ser membro do grupo sysadmin do SQL Server para o servidor baseado no SQL Server no qual está instalando os arquivos do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="dc881-113">To install and deploy the databases on the SQL Server-based server, you must be a member of the SQL Server sysadmin group for the SQL Server-based server where you are installing the database files.</span></span> <span data-ttu-id="dc881-114">Se você não for membro do grupo sysadmin do SQL Server, será necessário solicitar que você seja adicionado ao grupo até que os arquivos de banco de dados sejam implantados.</span><span class="sxs-lookup"><span data-stu-id="dc881-114">If you are not a member of the SQL Server sysadmin group, you will need to request that you be added to the group until the database files are deployed.</span></span> <span data-ttu-id="dc881-115">Se não for possível tornar um membro do grupo sysadmin, você deve fornecer ao administrador do banco de dados do SQL Server o script para configurar e implantar os bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="dc881-115">If you cannot be made a member of the sysadmin group, you should provide your SQL Server database administrator with the script to configure and deploy the databases.</span></span> <span data-ttu-id="dc881-116">Para obter detalhes sobre os direitos e permissões de usuário adequados que você precisa para executar os procedimentos, consulte <A href="lync-server-2013-deployment-permissions-for-sql-server.md">permissões de implantação do SQL Server no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="dc881-116">For details about the proper user rights and permissions that you need to accomplish the procedures, see <A href="lync-server-2013-deployment-permissions-for-sql-server.md">Deployment permissions for SQL Server in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-configure-sql-server-clustering"></a><span data-ttu-id="dc881-117">Para configurar o agrupamento do SQL Server</span><span class="sxs-lookup"><span data-stu-id="dc881-117">To configure SQL Server clustering</span></span>

1.  <span data-ttu-id="dc881-118">Depois de concluir a instalação e a configuração do cluster do SQL Server, defina a loja do SQL Server no construtor de topologias usando o nome do cluster virtual da instância do SQL Server (conforme configurado na configuração do agrupamento do SQL Server) e o nome da instância do banco de dados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dc881-118">After you have completed the installation and configuration of SQL Server clustering, you define the SQL Server store in Topology Builder by using the SQL Server instance virtual cluster name (as configured in the setup for SQL Server clustering) and the instance name of the SQL Server database.</span></span> <span data-ttu-id="dc881-119">Diferente de um único servidor baseado no SQL Server, você usará o nome de domínio totalmente qualificado (FQDN) do nó virtual para um servidor de cluster com SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dc881-119">Different from a single SQL Server-based server, you will use the virtual node fully qualified domain name (FQDN) for a clustered SQL Server-based server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="dc881-120">Os nós de clusters individuais do Windows Server não precisam ser configurados para o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="dc881-120">The individual Windows Server cluster nodes do not have to be configured for Topology Builder.</span></span> <span data-ttu-id="dc881-121">Você usará somente o nome do cluster do SQL Server virtual.</span><span class="sxs-lookup"><span data-stu-id="dc881-121">You will use only the virtual SQL Server cluster name.</span></span>

    
    </div>

2.  <span data-ttu-id="dc881-122">Se você estiver usando o construtor de topologias para implantar seus bancos de dados, você deve ser membro do grupo sysadmin do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dc881-122">If you are using Topology Builder to deploy your databases, you must be a member of the SQL Server sysadmin group.</span></span> <span data-ttu-id="dc881-123">Se você for membro do grupo sysadmin do SQL Server, mas não tiver privilégios no domínio (por exemplo, uma função de administrador de banco de dados do SQL Server), terá os direitos para criar os bancos de dados, mas não poderá ler as informações necessárias no Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dc881-123">If you are a member of the SQL Server sysadmin group, but you do not have privileges in the domain (for example, a SQL Server database administrator role), then you have the rights to create the databases but not to read necessary information in Lync Server.</span></span> <span data-ttu-id="dc881-124">Para obter detalhes sobre os direitos de usuário e as permissões necessárias para implantar o Lync Server, consulte [permissões de implantação do SQL Server no Lync Server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).</span><span class="sxs-lookup"><span data-stu-id="dc881-124">For details about the user rights and permissions necessary to deploying Lync Server, see [Deployment permissions for SQL Server in Lync Server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).</span></span>

3.  <span data-ttu-id="dc881-125">Verifique se a pasta de banco de dados e os padrões de pasta de arquivos de log estão mapeados corretamente para os discos compartilhados no cluster do SQL Server usando o SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="dc881-125">Ensure that the database folder and log files folder defaults are mapped correctly to the shared disks in the SQL Server cluster by using SQL Server Management Studio.</span></span> <span data-ttu-id="dc881-126">Esse será um procedimento obrigatório se você criar bancos de dados usando o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="dc881-126">This is a required procedure if you will create databases by using Topology Builder.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="dc881-127">Se você não instalou o SQL Server Management Studio, é possível instalá-lo executando novamente a instalação do SQL Server e selecionando a ferramenta de gerenciamento como um recurso adicionado para a implantação existente do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dc881-127">If you did not install SQL Server Management Studio, you can install it by rerunning the SQL Server installation, and then selecting the management tool as an added feature for the existing SQL Server deployment.</span></span>

    
    </div>

4.  <span data-ttu-id="dc881-128">Instale os bancos de dados para o servidor baseado no SQL Server usando o construtor de topologias ou cmdlets do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dc881-128">Install the databases for the SQL Server-based server by using either Topology Builder or Windows PowerShell cmdlets.</span></span> <span data-ttu-id="dc881-129">Para usar o construtor de topologias, use o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc881-129">To use Topology Builder, use the following procedure.</span></span> <span data-ttu-id="dc881-130">Para usar cmdlets do Windows PowerShell, consulte [instalação de banco de dados usando o Shell de gerenciamento do Lync Server no Lync server 2013](lync-server-2013-database-installation-using-lync-server-management-shell.md).</span><span class="sxs-lookup"><span data-stu-id="dc881-130">To use Windows PowerShell cmdlets, see [Database installation using Lync Server Management Shell in Lync Server 2013](lync-server-2013-database-installation-using-lync-server-management-shell.md).</span></span>

</div>

<div>

## <a name="to-create-databases-using-topology-builder"></a><span data-ttu-id="dc881-131">Para criar bancos de dados usando o construtor de topologias</span><span class="sxs-lookup"><span data-stu-id="dc881-131">To create databases using Topology Builder</span></span>

1.  <span data-ttu-id="dc881-132">Iniciar o construtor de topologias: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Construtor de topologias do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="dc881-132">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="dc881-133">O procedimento a seguir pressupõe que você definiu e configurou sua topologia no construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="dc881-133">The following procedure assumes that you have defined and configured your topology in Topology Builder.</span></span> <span data-ttu-id="dc881-134">Para obter detalhes sobre como definir sua topologia, consulte<A href="lync-server-2013-defining-and-configuring-the-topology.md">definindo e configurando a topologia no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="dc881-134">For details about defining your topology, see<A href="lync-server-2013-defining-and-configuring-the-topology.md">Defining and configuring the topology in Lync Server 2013</A>.</span></span> <span data-ttu-id="dc881-135">Para usar o construtor de topologias para publicar a topologia e configurar o banco de dados, você deve fazer logon como um usuário com os direitos de usuário e associações de grupo corretos.</span><span class="sxs-lookup"><span data-stu-id="dc881-135">To use Topology Builder to publish the topology and configure the database, you must log on as a user with the correct user rights and group memberships.</span></span> <span data-ttu-id="dc881-136">Para obter detalhes sobre os direitos obrigatórios e associações de grupo, consulte <A href="lync-server-2013-deployment-permissions-for-sql-server.md">permissões de implantação do SQL Server no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="dc881-136">For details about the required rights and group memberships, see <A href="lync-server-2013-deployment-permissions-for-sql-server.md">Deployment permissions for SQL Server in Lync Server 2013</A>.</span></span>

    
    </div>

2.  <span data-ttu-id="dc881-137">No construtor de topologia, à medida que você publica a topologia, na página **criar bancos de dados** , clique em **avançado**.</span><span class="sxs-lookup"><span data-stu-id="dc881-137">In Topology Builder, as you publish the topology, on the **Create databases** page, click **Advanced**.</span></span>

3.  <span data-ttu-id="dc881-138">A página **selecionar local do arquivo de banco de dados** tem duas opções que determinam como os arquivos de banco de dados serão implantados no cluster do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dc881-138">The **Select Database File Location** page has two options that determine how the database files will be deployed to the SQL Server cluster.</span></span> <span data-ttu-id="dc881-139">Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="dc881-139">Select one of the following:</span></span>
    
      - <span data-ttu-id="dc881-140">**Determine automaticamente o local do arquivo de banco de dados.**</span><span class="sxs-lookup"><span data-stu-id="dc881-140">**Automatically determine the database file location.**</span></span> <span data-ttu-id="dc881-141">Essa seleção usa um algoritmo para determinar os locais do log de banco de dados e do arquivo de dados com base na configuração da unidade no servidor baseado no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dc881-141">This selection uses an algorithm to determine the database log and data file locations based on the drive configuration on the SQL Server-based server.</span></span> <span data-ttu-id="dc881-142">Os arquivos serão distribuídos de forma a tentar fornecer o desempenho ideal.</span><span class="sxs-lookup"><span data-stu-id="dc881-142">The files will be distributed in such a way as to attempt to provide optimal performance.</span></span>
    
      - <span data-ttu-id="dc881-143">Usar padrões de instância do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dc881-143">Use SQL Server instance defaults.</span></span> <span data-ttu-id="dc881-144">Selecionar essa opção instalará os arquivos de log e de dados de acordo com as configurações da instância do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dc881-144">Selecting this option will install the log and data files according to the SQL Server instance settings.</span></span> <span data-ttu-id="dc881-145">Após a implantação dos arquivos de banco de dados no SQL Server, o administrador do banco de dados do SQL Server pode querer realocar os arquivos para otimizar o desempenho de seus requisitos de configuração específicos do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dc881-145">After deployment of the database files to the SQL Server, your SQL Server database administrator may want to relocate the files to optimize performance for your particular SQL Server configuration requirements.</span></span>

4.  <span data-ttu-id="dc881-146">Conclua a publicação da topologia e confirme se não houve erros durante a operação.</span><span class="sxs-lookup"><span data-stu-id="dc881-146">Complete the publishing of the topology and confirm that there were no errors during the operation.</span></span>

<span data-ttu-id="dc881-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dc881-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

