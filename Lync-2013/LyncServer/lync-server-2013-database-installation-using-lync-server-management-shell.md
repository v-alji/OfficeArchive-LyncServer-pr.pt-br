---
title: 'Lync Server 2013: Instalação de banco de dados usando o Shell de Gerenciamento do Lync Server'
description: 'Lync Server 2013: instalação de banco de dados usando o Shell de gerenciamento do Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Database installation using Lync Server Management Shell
ms:assetid: c90a6449-4dd5-4b18-b21c-ea2c2a64dc3c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398832(v=OCS.15)
ms:contentKeyID: 48185401
ms.date: 06/16/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2d572984c94d280723b12c5343a92ddfaa12d4f0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431250"
---
# <a name="database-installation-using-lync-server-management-shell-in-lync-server-2013"></a><span data-ttu-id="dddbd-103">Instalação de banco de dados usando o Shell de Gerenciamento do Lync Server no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dddbd-103">Database installation using Lync Server Management Shell in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dddbd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dddbd-104">

<span> </span></span></span>

<span data-ttu-id="dddbd-105">_**Tópico da última modificação:** 2016-06-16_</span><span class="sxs-lookup"><span data-stu-id="dddbd-105">_**Topic Last Modified:** 2016-06-16_</span></span>

<span data-ttu-id="dddbd-106">A separação de funções e responsabilidades entre os administradores do servidor e os administradores do SQL Server podem resultar em atrasos na implementação.</span><span class="sxs-lookup"><span data-stu-id="dddbd-106">Separation of roles and responsibilities between server administrators and SQL Server administrators can result in delays in implementation.</span></span> <span data-ttu-id="dddbd-107">O Lync Server 2013 usa o controle de acesso baseado em função (RBAC) para atenuar essas dificuldades.</span><span class="sxs-lookup"><span data-stu-id="dddbd-107">Lync Server 2013 uses role-based access control (RBAC) to mitigate these difficulties.</span></span> <span data-ttu-id="dddbd-108">Em alguns casos, o administrador do SQL Server deve gerenciar a instalação de bancos de dados no servidor baseado no SQL Server fora de RBAC.</span><span class="sxs-lookup"><span data-stu-id="dddbd-108">In some instances, the SQL Server administrator must manage the installation of databases on the SQL Server-based server outside RBAC.</span></span> <span data-ttu-id="dddbd-109">O Shell de gerenciamento do Lync Server 2013 fornece uma maneira para o administrador do SQL Server executar cmdlets do Windows PowerShell projetados para configurar os bancos de dados com os dados e arquivos de log corretos.</span><span class="sxs-lookup"><span data-stu-id="dddbd-109">The Lync Server 2013 Management Shell provides a way for the SQL Server administrator to run Windows PowerShell cmdlets designed to configure the databases with the correct data and log files.</span></span> <span data-ttu-id="dddbd-110">Para obter detalhes, consulte [permissões de implantação do SQL Server no Lync Server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).</span><span class="sxs-lookup"><span data-stu-id="dddbd-110">For details, see [Deployment permissions for SQL Server in Lync Server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).</span></span>

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="dddbd-111">O procedimento a seguir pressupõe que pelo menos os objetos de gerenciamento do Lync Server 2013 OCSCore.msi, do SQL Server Native Client (sqlncli.msi) Microsoft SQL Server 2012, tipos CLR para Microsoft SQL Server 2012 e Microsoft SQL Server 2012 ADOMD.NET sejam instalados.</span><span class="sxs-lookup"><span data-stu-id="dddbd-111">The following procedure assumes that at a minimum the Lync Server 2013 OCSCore.msi, SQL Server Native Client (sqlncli.msi) Microsoft SQL Server 2012 Management Objects, CLR Types for Microsoft SQL Server 2012 and Microsoft SQL Server 2012 ADOMD.NET are installed.</span></span> <span data-ttu-id="dddbd-112">O OCSCore.msi está localizado na mídia de instalação no diretório \Setup\AMD64\Setup.</span><span class="sxs-lookup"><span data-stu-id="dddbd-112">The OCSCore.msi is located on the installation media in the \Setup\AMD64\Setup directory.</span></span> <span data-ttu-id="dddbd-113">Os componentes restantes estão localizados no \setup\amd64.</span><span class="sxs-lookup"><span data-stu-id="dddbd-113">The remaining components are located in \Setup\amd64.</span></span> <span data-ttu-id="dddbd-114">Além disso, a preparação do Active Directory para o Lync Server 2013 foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="dddbd-114">Additionally, Active Directory preparation for Lync Server 2013 has been successfully completed.</span></span>



</div>

<span data-ttu-id="dddbd-115">**Install-CsDatabase** é o cmdlet do Windows PowerShell usado para instalar os bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="dddbd-115">**Install-CsDatabase** is the Windows PowerShell cmdlet you use to install the databases.</span></span> <span data-ttu-id="dddbd-116">O cmdlet **install-CsDatabase** tem um grande número de parâmetros, apenas alguns são discutidos aqui.</span><span class="sxs-lookup"><span data-stu-id="dddbd-116">The **Install-CsDatabase** cmdlet has a large number of parameters, only a few of which are discussed here.</span></span> <span data-ttu-id="dddbd-117">Para obter detalhes sobre os parâmetros possíveis, consulte a documentação do Shell de gerenciamento do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dddbd-117">For details about the possible parameters, see the Lync Server 2013 Management Shell documentation.</span></span>

<div class=" ">


> [!WARNING]  
> <span data-ttu-id="dddbd-118">Para evitar o desempenho e possíveis problemas de tempo limite, use sempre os FQDNs (nomes de domínio totalmente qualificados) ao se referir a servidores baseados no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dddbd-118">To avoid performance and possible time-out issues, always use fully qualified domain names (FQDNs) when referring to SQL Server-based servers.</span></span> <span data-ttu-id="dddbd-119">Evite o uso de referências somente a nomes de host.</span><span class="sxs-lookup"><span data-stu-id="dddbd-119">Avoid using host name-only references.</span></span> <span data-ttu-id="dddbd-120">Por exemplo, use sqlbe01.contoso.net, mas evite usar SQLBE01.</span><span class="sxs-lookup"><span data-stu-id="dddbd-120">For example, use sqlbe01.contoso.net, but avoid using SQLBE01.</span></span>



</div>

<span data-ttu-id="dddbd-121">Para a instalação de bancos de dados, **install-CsDatabase** usa três métodos principais para colocar os bancos de dados no servidor do SQL Server preparado:</span><span class="sxs-lookup"><span data-stu-id="dddbd-121">For installing databases, **Install-CsDatabase** uses three primary methods for placing the databases onto the prepared SQL Server-based server:</span></span>

  - <span data-ttu-id="dddbd-122">Execute **install-CsDatabase** sem databasepaths ou UseDefaultSqlPath.</span><span class="sxs-lookup"><span data-stu-id="dddbd-122">Run **Install-CsDatabase** without DatabasePaths or UseDefaultSqlPath.</span></span> <span data-ttu-id="dddbd-123">O cmdlet usa um algoritmo interno para determinar o melhor posicionamento para os arquivos de log e de dados.</span><span class="sxs-lookup"><span data-stu-id="dddbd-123">The cmdlet uses a built in algorithm to determine the best placement for the log and data files.</span></span> <span data-ttu-id="dddbd-124">O algoritmo só funciona em implementações de SQL Server autônomos.</span><span class="sxs-lookup"><span data-stu-id="dddbd-124">The algorithm only works for stand-alone SQL Server implementations.</span></span>

  - <span data-ttu-id="dddbd-125">Execute **install-CsDatabase** com o parâmetro databasepaths.</span><span class="sxs-lookup"><span data-stu-id="dddbd-125">Run **Install-CsDatabase** with the DatabasePaths parameter.</span></span> <span data-ttu-id="dddbd-126">O algoritmo interno para otimizar locais de arquivos de log e dados não será usado se o parâmetro databasepaths for definido.</span><span class="sxs-lookup"><span data-stu-id="dddbd-126">The built-in algorithm to optimize log and data file locations is not used if the DatabasePaths parameter is defined.</span></span> <span data-ttu-id="dddbd-127">Usar esse parâmetro permite que você defina os locais onde os arquivos de log e de dados serão implantados.</span><span class="sxs-lookup"><span data-stu-id="dddbd-127">Using this parameter allows you to define the locations where log and data files will be deployed.</span></span>

  - <span data-ttu-id="dddbd-128">Execute **install-CsDatabase** com UseDefaultSqlPaths.</span><span class="sxs-lookup"><span data-stu-id="dddbd-128">Run **Install-CsDatabase** with UseDefaultSqlPaths.</span></span> <span data-ttu-id="dddbd-129">Essa opção não usa o algoritmo interno para otimizar os locais dos arquivos de log e de dados.</span><span class="sxs-lookup"><span data-stu-id="dddbd-129">This option does not use the built-in algorithm to optimize the log and data file locations.</span></span> <span data-ttu-id="dddbd-130">O log e o arquivo de dados são implantados de acordo com os padrões definidos pelo administrador do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dddbd-130">Log and data file are deployed according to the defaults set by the SQL Server administrator.</span></span> <span data-ttu-id="dddbd-131">Esses caminhos geralmente são definidos para a finalidade da Administração automática de arquivos de log e de dados no SQL Server com antecedência e não são associados à configuração do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dddbd-131">These paths are typically set for the purpose of automatic administration of log and data files on the SQL Server in advance, and are not associated with the setup of Lync Server 2013.</span></span>

  - <span data-ttu-id="dddbd-132">O parâmetro DatabasePathMap também pode ser usado para especificar explicitamente um local para cada banco de dados e seu respectivo arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="dddbd-132">The DatabasePathMap parameter can also be used to explicitly specify a location for each database and its respective log file.</span></span>

<div>

## <a name="to-use-windows-powershell-cmdlets-to-configure-the-sql-server-central-management-store"></a><span data-ttu-id="dddbd-133">Para usar cmdlets do Windows PowerShell para configurar o repositório de gerenciamento central do SQL Server</span><span class="sxs-lookup"><span data-stu-id="dddbd-133">To use Windows PowerShell cmdlets to configure the SQL Server Central Management store</span></span>

1.  <span data-ttu-id="dddbd-134">Em qualquer computador, faça logon com credenciais administrativas para criar bancos de dados no servidor baseado no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dddbd-134">On any computer, log on with administrative credentials for creating the databases on the SQL Server-based server.</span></span> <span data-ttu-id="dddbd-135">Para obter detalhes, consulte [permissões de implantação do SQL Server no Lync Server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).</span><span class="sxs-lookup"><span data-stu-id="dddbd-135">For details, see [Deployment permissions for SQL Server in Lync Server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).</span></span>

2.  <span data-ttu-id="dddbd-136">Abra o Shell de gerenciamento do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dddbd-136">Open the Lync Server 2013 Management Shell.</span></span> <span data-ttu-id="dddbd-137">Se você não tiver ajustado a política de execução do Windows PowerShell, será necessário ajustar a política para permitir que os scripts do Windows PowerShell sejam executados.</span><span class="sxs-lookup"><span data-stu-id="dddbd-137">If you have not adjusted the execution policy for Windows PowerShell, you must adjust the policy to allow Windows PowerShell scripts to run.</span></span> <span data-ttu-id="dddbd-138">Para obter detalhes, consulte "examinando a política de execução" em [https://go.microsoft.com/fwlink/p/?linkId=203093](https://go.microsoft.com/fwlink/p/?linkid=203093) .</span><span class="sxs-lookup"><span data-stu-id="dddbd-138">For details, see “Examining the Execution Policy” at [https://go.microsoft.com/fwlink/p/?linkId=203093](https://go.microsoft.com/fwlink/p/?linkid=203093).</span></span>

3.  <span data-ttu-id="dddbd-139">Use o cmdlet **install-CsDatabase** para instalar o repositório de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="dddbd-139">Use the **Install-CsDatabase** cmdlet to install the Central Management store.</span></span>
    
       ```powershell
        Install-CsDatabase -CentralManagementDatabase -SqlServerFqdn <fully qualified domain name of SQL Server> 
        -SqlInstanceName <named instance> -DatabasePaths <logfile path>,<database file path> 
        -Report <path to report file>
       ```
    
       ```powershell
        Install-CsDatabase -CentralManagementDatabase -SqlServerFqdn sqlbe.contoso.net -SqlInstanceName rtc -DatabasePaths "C:\CSDB-Logs","C:\CSDB-CMS" -Report "C:\Logs\InstallDatabases.html"
       ```
    
    <div class=" ">
    

    > [!TIP]  
    > <span data-ttu-id="dddbd-140">O parâmetro relatório é opcional, mas é útil se você está documentando o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="dddbd-140">The Report parameter is optional but is useful if you are documenting the installation process.</span></span>

    
    </div>

4.  <span data-ttu-id="dddbd-141">**Install-CsDatabase – Databasepaths** podem usar até seis parâmetros de caminho, cada um definindo os caminhos para as unidades definidas nos dados do SQL Server e na colocação de arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="dddbd-141">**Install-CsDatabase –DatabasePaths** can use up to six path parameters, each defining the paths for the drives as defined in SQL Server Data and Log File Placement.</span></span> <span data-ttu-id="dddbd-142">Pelas regras lógicas da configuração de banco de dados no Lync Server 2013, as unidades são analisadas em buckets de duas, quatro ou seis.</span><span class="sxs-lookup"><span data-stu-id="dddbd-142">By the logical rules of the database configuration in Lync Server 2013, drives are parsed out into buckets of two, four, or six.</span></span> <span data-ttu-id="dddbd-143">Dependendo da configuração do SQL Server e do número de buckets, você fornecerá dois caminhos, quatro caminhos ou seis caminhos.</span><span class="sxs-lookup"><span data-stu-id="dddbd-143">Depending on your SQL Server configuration and the number of buckets, you will supply two paths, four paths, or six paths.</span></span>
    
    <span data-ttu-id="dddbd-144">Se você tiver três unidades, o log terá prioridade e os arquivos de dados serão distribuídos após.</span><span class="sxs-lookup"><span data-stu-id="dddbd-144">If you have three drives, the log gets priority and the data files are distributed after.</span></span> <span data-ttu-id="dddbd-145">Um exemplo de um servidor baseado em SQL Server configurado com seis unidades:</span><span class="sxs-lookup"><span data-stu-id="dddbd-145">An example for a SQL Server-based server configured with six drives:</span></span>
    ```powershell
    Install-CsDatabase -ConfiguredDatases -SqlServerFqdn sqlbe.contoso.net -DatabasePaths "D:\CSDynLogs","E:\CSRtcLogs","F:\MonCdrArcLogs","G:\MonCdrArchData","H:\AbsAppLog","I:\DynRtcAbsAppData" -Report "C:\Logs\InstallDatabases.html"
    ```
5.  <span data-ttu-id="dddbd-146">Quando a instalação do banco de dados é concluída, você pode fechar o Shell de gerenciamento do Lync Server 2013 ou prosseguir para a instalação dos bancos de dados configurados do Lync Server 2013 definidos no construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="dddbd-146">When the database installation completes, you can close Lync Server 2013 Management Shell or proceed to the installation of the Lync Server 2013 configured databases defined in Topology Builder.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-cmdlets-to-configure-the-sql-server-topology-configured-databases"></a><span data-ttu-id="dddbd-147">Para usar cmdlets do Windows PowerShell para configurar os bancos de dados configurados para topologia do SQL Server</span><span class="sxs-lookup"><span data-stu-id="dddbd-147">To use Windows PowerShell cmdlets to configure the SQL Server topology configured databases</span></span>

1.  <span data-ttu-id="dddbd-148">Para instalar os bancos de dados do construtor de topologias configurados para o Lync Server 2013, o administrador do Lync Server 2013 deve publicar a topologia.</span><span class="sxs-lookup"><span data-stu-id="dddbd-148">To install the Topology Builder configured databases for Lync Server 2013, the Lync Server 2013 administrator must publish the topology.</span></span> <span data-ttu-id="dddbd-149">Para obter detalhes, consulte [publicar a topologia no Lync Server 2013](lync-server-2013-publish-the-topology.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="dddbd-149">For details, see [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md) in the Deployment documentation.</span></span>

2.  <span data-ttu-id="dddbd-150">Em qualquer computador, faça logon com credenciais administrativas para criar bancos de dados no servidor baseado no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dddbd-150">On any computer, log on with administrative credentials for creating the databases on the SQL Server-based server.</span></span> <span data-ttu-id="dddbd-151">Consulte o tópico [permissões de implantação do SQL Server no Lync Server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).</span><span class="sxs-lookup"><span data-stu-id="dddbd-151">See the topic, [Deployment permissions for SQL Server in Lync Server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).</span></span>
    
    <div class=" ">
    

    > [!IMPORTANT]  
    > <span data-ttu-id="dddbd-152">Para poder configurar os bancos de dados baseados no SQL Server, certifique-se de que a conta de administrador do SQL Server usada para executar as etapas descritas aqui também é um membro do grupo sysadmins (ou equivalente) no servidor que executa o SQL Server e que mantém a função de servidor de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="dddbd-152">To be able to configure the SQL Server-based databases, make sure the SQL Server administrator account used to run the steps described here is also a member of the sysadmins group (or equivalent) on the server running SQL Server and holding the Central Management Server role.</span></span> <span data-ttu-id="dddbd-153">Isso é especialmente importante para verificar se há pools adicionais do Lync Server 2013 que exijam instalação ou configuração do banco de dados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dddbd-153">This is especially important to check for any additional Lync Server 2013 pools which require SQL Server database installation or configuration.</span></span> <span data-ttu-id="dddbd-154">Por exemplo, se você estiver implantando um segundo pool (pool02), mas a função de servidor de gerenciamento central estiver mantida pela pool01.</span><span class="sxs-lookup"><span data-stu-id="dddbd-154">For example, if you are deploying a second pool (pool02) but the Central Management Server role is held by pool01.</span></span> <span data-ttu-id="dddbd-155">O grupo sysadmin do SQL Server (ou equivalente) deve ter permissões em bancos de dados baseados no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dddbd-155">The SQL Server sysadmin group (or equivalent) must have permissions on both SQL Server-based databases.</span></span>

    
    </div>

3.  <span data-ttu-id="dddbd-156">Abra o Shell de gerenciamento do Lync Server 2013, se ele ainda não estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="dddbd-156">Open Lync Server 2013 Management Shell, if it’s not already open.</span></span>

4.  <span data-ttu-id="dddbd-157">Use o cmdlet **install-CsDatabase** para instalar os bancos de dados do construtor de topologias configurados.</span><span class="sxs-lookup"><span data-stu-id="dddbd-157">Use the **Install-CsDatabase** cmdlet to install the Topology Builder configured databases.</span></span>
    
       ```powershell
        Install-CsDatabase -ConfiguredDatabases -SqlServerFqdn <fully qualified domain name of SQL Server> 
         -DatabasePaths <logfile path>,<database file path> -Report <path to report file>
       ```
    
       ```powershell
        Install-CsDatabase -ConfiguredDatabases -SqlServerFqdn sqlbe.contoso.net 
        -Report "C:\Logs\InstallDatabases.html"
       ```
    
    <div class=" ">
    

    > [!TIP]  
    > <span data-ttu-id="dddbd-158">O parâmetro relatório é opcional, mas é útil se você está documentando o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="dddbd-158">The Report parameter is optional but is useful if you are documenting the installation process.</span></span>

    
    </div>

5.  <span data-ttu-id="dddbd-159">Quando a instalação do banco de dados for concluída, feche o Shell de gerenciamento do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dddbd-159">When the database installation completes, close Lync Server 2013 Management Shell.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-cmdlets-to-configure-the-sql-server-topology-using-the-databasepathmap-parameter"></a><span data-ttu-id="dddbd-160">Para usar cmdlets do Windows PowerShell para configurar a topologia do SQL Server usando o parâmetro DatabasePathMap</span><span class="sxs-lookup"><span data-stu-id="dddbd-160">To use Windows PowerShell cmdlets to configure the SQL Server topology using the DatabasePathMap parameter</span></span>

1.  <span data-ttu-id="dddbd-161">Para instalar bancos de dados do Lync Server 2013, o administrador do Lync Server deve criar os caminhos e implantar os arquivos de banco de dados e os arquivos de log de acordo com um conjunto de regras predefinido.</span><span class="sxs-lookup"><span data-stu-id="dddbd-161">To install databases for Lync Server 2013, the Lync Server administrator must create the paths and deploy the databases files and log files according to a predefined set of rules.</span></span>

2.  <span data-ttu-id="dddbd-162">Em qualquer computador, faça logon com credenciais administrativas para criar bancos de dados no servidor baseado no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dddbd-162">On any computer, log on with administrative credentials for creating the databases on the SQL Server-based server.</span></span> <span data-ttu-id="dddbd-163">Consulte o tópico [permissões de implantação do SQL Server no Lync Server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).</span><span class="sxs-lookup"><span data-stu-id="dddbd-163">See the topic, [Deployment permissions for SQL Server in Lync Server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).</span></span>
    
    <div class=" ">
    

    > [!IMPORTANT]  
    > <span data-ttu-id="dddbd-164">Para poder configurar os bancos de dados baseados no SQL Server, certifique-se de que a conta de administrador do SQL Server usada para executar as etapas descritas aqui também é um membro do grupo sysadmins (ou equivalente) no servidor que executa o SQL Server e que mantém a função de servidor de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="dddbd-164">To be able to configure the SQL Server-based databases, make sure the SQL Server administrator account used to run the steps described here is also a member of the sysadmins group (or equivalent) on the server running SQL Server and holding the Central Management Server role.</span></span> <span data-ttu-id="dddbd-165">Isso é especialmente importante para verificar se há outros pools do Lync Server que exijam instalação ou configuração do banco de dados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dddbd-165">This is especially important to check for any additional Lync Server pools which require SQL Server database installation or configuration.</span></span> <span data-ttu-id="dddbd-166">Por exemplo, se você estiver implantando um segundo pool (pool02), mas a função de servidor de gerenciamento central estiver mantida pela pool01.</span><span class="sxs-lookup"><span data-stu-id="dddbd-166">For example, if you are deploying a second pool (pool02) but the Central Management Server role is held by pool01.</span></span> <span data-ttu-id="dddbd-167">O grupo sysadmin do SQL Server (ou equivalente) deve ter permissões em bancos de dados baseados no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dddbd-167">The SQL Server sysadmin group (or equivalent) must have permissions on both SQL Server-based databases.</span></span>

    
    </div>

3.  <span data-ttu-id="dddbd-168">Abra o Shell de gerenciamento do Lync Server, se ele ainda não estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="dddbd-168">Open Lync Server Management Shell, if it’s not already open.</span></span>

4.  <span data-ttu-id="dddbd-169">Use o cmdlet **install-CsDatabase** com o parâmetro DatabasePathMap e uma tabela de hash do PowerShell para instalar os bancos de dados do construtor de topologias configurados.</span><span class="sxs-lookup"><span data-stu-id="dddbd-169">Use the **Install-CsDatabase** cmdlet with the DatabasePathMap parameter and a PowerShell hash table to install the Topology Builder configured databases.</span></span>

5.  <span data-ttu-id="dddbd-170">No código de exemplo, os caminhos definidos para os bancos de dados podem ser determinados de uma maneira granular usando-se o parâmetro – DatabasePathMap e uma tabela de hash definida da seguinte maneira (o exemplo usa "C: \\ CSData" para todos os arquivos de banco de dados (. MDF) e "C: \\ CSLogFiles" para todos os arquivos de log (. ldf).</span><span class="sxs-lookup"><span data-stu-id="dddbd-170">In the example code, the paths defined for the databases can be determined in a granular manner by using the –DatabasePathMap parameter and a defined hash table as follows (the example uses “C:\\CSData” for all database (.mdf) files, and “C:\\CSLogFiles” for all log (.ldf) files.</span></span> <span data-ttu-id="dddbd-171">A pasta será criada conforme necessário pelo install-CsDatabase):</span><span class="sxs-lookup"><span data-stu-id="dddbd-171">Folder will be created as needed by Install-CsDatabase):</span></span>
    ```powershell
    $pathmap = @{
    "BackendStore:BlobStore:DbPath"="C:\CsData";"BackendStore:BlobStore:LogPath"="C:\CsLogFiles"
    "BackendStore:RtcSharedDatabase:DbPath"="C:\CsData";"BackendStore:RtcSharedDatabase:LogPath"="C:\CsLogFiles"
    "ABSStore:AbsDatabase:DbPath"="C:\CsData";"ABSStore:AbsDatabase:LogPath"="C:\CsLogFiles"
    "ApplicationStore:RgsConfigDatabase:DbPath"="C:\CsData";"ApplicationStore:RgsConfigDatabase:LogPath"="C:\CsLogFiles"
    "ApplicationStore:RgsDynDatabase:DbPath"="C:\CsData";"ApplicationStore:RgsDynDatabase:LogPath"="C:\CsLogFiles"
    "ApplicationStore:CpsDynDatabase:DbPath"="C:\CsData";"ApplicationStore:CpsDynDatabase:LogPath"="C:\CsLogFiles"
    "ArchivingStore:ArchivingDatabase:DbPath"="C:\CsData";"ArchivingStore:ArchivingDatabase:LogPath"="C:\CsLogFiles"
    "MonitoringStore:MonitoringDatabase:DbPath"="C:\CsData";"MonitoringStore:MonitoringDatabase:LogPath"="C:\CsLogFiles"
    "MonitoringStore:QoEMetricsDatabase:DbPath"="C:\CsData";"MonitoringStore:QoEMetricsDatabase:LogPath"="C:\CsLogFiles"
    }
    Install-CsDatabase -ConfigureDatabases -SqlServerFqdn sqlbe01.contoso.net -DatabasePathMap $pathmap
    ```
6.  <span data-ttu-id="dddbd-172">Como o banco de dados e os arquivos de log são explicitamente nomeados com sua localização no servidor de banco de dados de destino, você pode definir locais específicos para cada tipo de serviço de banco de dados real e local de log.</span><span class="sxs-lookup"><span data-stu-id="dddbd-172">Because the database and log files are explicitly named with their location on the destination database server, you can define specific locations for each service type’s actual database and log location.</span></span> <span data-ttu-id="dddbd-173">O exemplo a seguir coloca os bancos de dados de cada tipo de serviço específico em discos separados e os arquivos de log associados em outro.</span><span class="sxs-lookup"><span data-stu-id="dddbd-173">The following example puts databases for each specific service type on separate disks, and associated log files on another.</span></span> <span data-ttu-id="dddbd-174">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="dddbd-174">For example:</span></span>
    
      - <span data-ttu-id="dddbd-175">Todos os bancos de dados RTC para "D: \\ RTCDatabase"</span><span class="sxs-lookup"><span data-stu-id="dddbd-175">All RTC databases to “D:\\RTCDatabase”</span></span>
    
      - <span data-ttu-id="dddbd-176">Todos os arquivos de log RTC para "E: \\ RTCLogs"</span><span class="sxs-lookup"><span data-stu-id="dddbd-176">All RTC log files to “E:\\RTCLogs”</span></span>
    
      - <span data-ttu-id="dddbd-177">Todos os bancos de dados da loja de aplicativos para "F: \\ CPSDatabases"</span><span class="sxs-lookup"><span data-stu-id="dddbd-177">All application store databases to “F:\\CPSDatabases”</span></span>
    
      - <span data-ttu-id="dddbd-178">Todos os logs da loja de aplicativos para "G: \\ CPSLogs"</span><span class="sxs-lookup"><span data-stu-id="dddbd-178">All application store logs to “G:\\CPSLogs”</span></span>
    
      - <span data-ttu-id="dddbd-179">Todos os bancos de dados de repositório do grupo de resposta para "H: \\ RGSDatabases"</span><span class="sxs-lookup"><span data-stu-id="dddbd-179">All response group store databases to “H:\\RGSDatabases”</span></span>
    
      - <span data-ttu-id="dddbd-180">Todos os logs do repositório do grupo de resposta para "I: \\ RGSLogs"</span><span class="sxs-lookup"><span data-stu-id="dddbd-180">All response group store logs to “I:\\RGSLogs”</span></span>
    
      - <span data-ttu-id="dddbd-181">Todos os bancos de dados do catálogo de endereços para "J: \\ ABSDatabases"</span><span class="sxs-lookup"><span data-stu-id="dddbd-181">All address book store databases to “J:\\ABSDatabases”</span></span>
    
      - <span data-ttu-id="dddbd-182">Todos os arquivos de registro do repositório de endereços para "K: \\ ABSLogs"</span><span class="sxs-lookup"><span data-stu-id="dddbd-182">All address book store log files to “K:\\ABSLogs”</span></span>
    
      - <span data-ttu-id="dddbd-183">Todos os bancos de dados do arquivamento da loja para "L: \\ ArchivingDatabases"</span><span class="sxs-lookup"><span data-stu-id="dddbd-183">All archiving store databases to “L:\\ArchivingDatabases”</span></span>
    
      - <span data-ttu-id="dddbd-184">Todos os logs do repositório de arquivamento para "M: \\ ArchivingLogs"</span><span class="sxs-lookup"><span data-stu-id="dddbd-184">All archiving store logs to “M:\\ArchivingLogs”</span></span>
    
      - <span data-ttu-id="dddbd-185">Todos os bancos de dados da loja de monitoramento para "N: \\ MonitoringDatabases"</span><span class="sxs-lookup"><span data-stu-id="dddbd-185">All monitoring store databases to “N:\\MonitoringDatabases”</span></span>
    
      - <span data-ttu-id="dddbd-186">Todos os arquivos de log da loja de monitoramento para "O: \\ MonitoringLogfiles"</span><span class="sxs-lookup"><span data-stu-id="dddbd-186">All monitoring store log files to “O:\\MonitoringLogfiles”</span></span>
    
    <!-- end list -->
    
    ```powershell    
    $pathmap = @{
    "BackendStore:BlobStore:DbPath"="D:\RTCDatabase";"BackendStore:BlobStore:LogPath"="E:\RTCLogs"
    "BackendStore:RtcSharedDatabase:DbPath"="D:\RTCDatabase";"BackendStore:RtcSharedDatabase:LogPath"="E:\RTCLogs"
    "ABSStore:AbsDatabase:DbPath"="J:\ABSDatabases";"ABSStore:AbsDatabase:LogPath"="K:\ABSLogs"
    "ApplicationStore:RgsConfigDatabase:DbPath"="H:\RGSDatabases";"ApplicationStore:RgsConfigDatabase:LogPath"="G:\CPSLogs"
    "ApplicationStore:RgsDynDatabase:DbPath"="H:\RGSDatabases";"ApplicationStore:RgsDynDatabase:LogPath"="I:\RGSLogs"
    "ApplicationStore:CpsDynDatabase:DbPath"="F:\CPSDatabases";"ApplicationStore:CpsDynDatabase:LogPath"="G:\CsLogFiles"
    "ArchivingStore:ArchivingDatabase:DbPath"="M:\ArchivingLogs";"ArchivingStore:ArchivingDatabase:LogPath"="N:\MonitoringDatabases"
    "MonitoringStore:MonitoringDatabase:DbPath"="N:\MonitoringDatabases";"MonitoringStore:MonitoringDatabase:LogPath"="O:\MonitoringLogfiles"
    "MonitoringStore:QoEMetricsDatabase:DbPath"="N:\MonitoringDatabases";"MonitoringStore:QoEMetricsDatabase:LogPath"="O:\MonitoringLogfiles"
    }
    
    Install-CsDatabase -ConfiguredDatabases -SqlServerFqdn sqlbe01.contoso.net -DatabasePathMap $pathmap
    ```
    
    <span data-ttu-id="dddbd-187">Usando o parâmetro – DatabasePathMap, você pode definir qualquer combinação de mapeamento de letras de unidade lógica que forneça a melhor solução para seus requisitos de desempenho e posicionamento do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dddbd-187">Using the –DatabasePathMap parameter, you can define any logical drive letter mapping combination that provides the best solution for your SQL Server performance and placement requirements.</span></span>

<span data-ttu-id="dddbd-188">Se você configurar seus arquivos de dados de banco de dados e arquivos de log usando o método **DatabasePathMap** , será necessário fazer uma pequena alteração no processo normal ao usar o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="dddbd-188">If you configure your database data files and log files by using the **DatabasePathMap** method, you will need to make a slight change to your normal process when using Topology Builder.</span></span> <span data-ttu-id="dddbd-189">Normalmente, você define suas opções de topologia, publica a topologia e escolhe implantar as seleções de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="dddbd-189">Typically, you would define your topology choices, publish the topology, and choose to deploy the database selections.</span></span>

<span data-ttu-id="dddbd-190">Se você usou o **DatabasePathMap** , já realizou a terceira parte do processo do construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="dddbd-190">If you have used **DatabasePathMap** you have already accomplished the third part of the Topology Builder process.</span></span> <span data-ttu-id="dddbd-191">No caso de ter um servidor de banco de dados completamente configurado antes do construtor de topologias em execução, você ainda pode definir todas as suas opções e funções de servidor, mas desmarque a opção para criar os bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="dddbd-191">In the case of having a completely configured database server in advance of running Topology Builder, you would still define all of your server roles and options, but deselect the option to create the databases.</span></span>

<span data-ttu-id="dddbd-192"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dddbd-192"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

