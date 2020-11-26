---
title: Ferramentas do kit de recursos de chat persistente do Lync Server 2013
description: Ferramentas do kit de recursos de chat persistente do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 Persistent Chat Resource Kit Tools
ms:assetid: 7a34d2ba-eb25-4e22-92d1-b9baf81b102c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945599(v=OCS.15)
ms:contentKeyID: 51541423
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 336e81c97da73da47eee654161a7d8d8956f9edb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438410"
---
# <a name="lync-server-2013-persistent-chat-resource-kit-tools"></a><span data-ttu-id="47a76-103">Ferramentas do kit de recursos de chat persistente do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47a76-103">Lync Server 2013 Persistent Chat Resource Kit Tools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="47a76-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="47a76-104">

<span> </span></span></span>

<span data-ttu-id="47a76-105">_**Tópico da última modificação:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="47a76-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="47a76-106">As ferramentas do kit de recursos de chat persistente do Lync Server 2013 ajudam a facilitar tarefas de rotina para administradores de ti que implantam e gerenciam o servidor de chat persistente do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="47a76-106">The Lync Server 2013 Persistent Chat Resource Kit tools help to make routine tasks easier for IT administrators who deploy and manage Lync Server 2013 Persistent Chat Server.</span></span> <span data-ttu-id="47a76-107">Além das instruções de instalação, este tópico descreve a finalidade de cada ferramenta e exemplos de seu uso.</span><span class="sxs-lookup"><span data-stu-id="47a76-107">In addition to installation instructions, this topic describes the purpose of each tool, and examples of its use.</span></span>

<div>

## <a name="installation-of-the-resource-kit-tools"></a><span data-ttu-id="47a76-108">Instalação das Ferramentas do Kit de Recursos</span><span class="sxs-lookup"><span data-stu-id="47a76-108">Installation of the Resource Kit Tools</span></span>

<span data-ttu-id="47a76-109">Para instalar o Lync Server 2013, ferramentas do Resource Kit, baixe **PersistentChatReskit.msi**.</span><span class="sxs-lookup"><span data-stu-id="47a76-109">To install the Lync Server 2013, Resource Kit Tools, download **PersistentChatReskit.msi**.</span></span> <span data-ttu-id="47a76-110">Execute **PersistentChatReskit.msi** para fazer uma instalação simples.</span><span class="sxs-lookup"><span data-stu-id="47a76-110">Run **PersistentChatReskit.msi** to do a simple installation.</span></span> <span data-ttu-id="47a76-111">O. msi instala todas as ferramentas no seguinte caminho: \\ **arquivos de programa \\ Microsoft Lync Server 2013 \\ persistent chat Server Resource Kit**.</span><span class="sxs-lookup"><span data-stu-id="47a76-111">The .msi installs all the tools in the following path: \\**Program Files\\ Microsoft Lync Server 2013\\Persistent Chat Server Resource Kit**.</span></span> <span data-ttu-id="47a76-112">As ferramentas que são executáveis autocontidos ficam nessa pasta.</span><span class="sxs-lookup"><span data-stu-id="47a76-112">Tools that are self-contained executables are in this folder.</span></span> <span data-ttu-id="47a76-113">As ferramentas que também têm arquivos estão em suas próprias subpastas.</span><span class="sxs-lookup"><span data-stu-id="47a76-113">Tools that also have files are in their own subfolders.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="47a76-114">Depois de instalar o Lync Server 2013, o Resource Kit Tools, você deve instalar o <STRONG>PsExec.exe</STRONG> e copiar <STRONG>PsExec.exe</STRONG> para o seguinte caminho: \\ <STRONG>arquivos de programas \ Microsoft Lync Server 2013 \ persistent chat Resource Server Kit\ChatStressTool</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="47a76-114">After installing the Lync Server 2013, Resource Kit Tools, you must install <STRONG>PsExec.exe</STRONG> and copy <STRONG>PsExec.exe</STRONG> to the following path: \\<STRONG>Program Files\ Microsoft Lync Server 2013\Persistent Chat Server Resource Kit\ChatStressTool</STRONG>.</span></span> <span data-ttu-id="47a76-115">Se você não copiar <STRONG>PsExec.exe</STRONG>, a ferramenta de stress de chat persistente gerará uma exceção de erro e não será executada corretamente.</span><span class="sxs-lookup"><span data-stu-id="47a76-115">If you do not copy <STRONG>PsExec.exe</STRONG>, the Persistent Chat Stress Tool will throw an error exception, and not perform correctly.</span></span> <span data-ttu-id="47a76-116">Certifique-se de que você atende a este requisito de pré-requisito antes de executar a ferramenta.</span><span class="sxs-lookup"><span data-stu-id="47a76-116">Make sure that you meet this prerequisite requirement prior to running the tool.</span></span> <span data-ttu-id="47a76-117">Para obter detalhes sobre como instalar o <STRONG>PsExec.exe</STRONG>, consulte <A href="https://go.microsoft.com/fwlink/p/?linkid=282246">https://go.microsoft.com/fwlink/p/?LinkId=282246</A> .</span><span class="sxs-lookup"><span data-stu-id="47a76-117">For details about installing <STRONG>PsExec.exe</STRONG>, see <A href="https://go.microsoft.com/fwlink/p/?linkid=282246">https://go.microsoft.com/fwlink/p/?LinkId=282246</A>.</span></span>



</div>

</div>

<div>

## <a name="supported-environments"></a><span data-ttu-id="47a76-118">Ambientes com suporte</span><span class="sxs-lookup"><span data-stu-id="47a76-118">Supported Environments</span></span>

<span data-ttu-id="47a76-119">Para obter o melhor desempenho, as ferramentas do Lync Server 2013, do Resource Kit devem ser instaladas no mesmo ambiente e com as mesmas especificações necessárias para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="47a76-119">For optimal performance, the Lync Server 2013, Resource Kit Tools should be installed in the same environment and with the same specifications that are required for Lync Server 2013.</span></span>

</div>

<div>

## <a name="resource-kit-tools-overview"></a><span data-ttu-id="47a76-120">Visão geral das Ferramentas do Kit de Recursos</span><span class="sxs-lookup"><span data-stu-id="47a76-120">Resource Kit Tools Overview</span></span>

<span data-ttu-id="47a76-121">Aqui estão as ferramentas fornecidas no kit de recursos de chat persistente do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="47a76-121">Here are the tools that are provided in the Lync Server 2013 Persistent Chat Resource Kit.</span></span> <span data-ttu-id="47a76-122">A seção a seguir fornece uma descrição de cada ferramenta, incluindo requisitos e uso de exemplo.</span><span class="sxs-lookup"><span data-stu-id="47a76-122">The following section provides a description of each tool, including requirements and example usage.</span></span>

  - <span data-ttu-id="47a76-123">AffCheck</span><span class="sxs-lookup"><span data-stu-id="47a76-123">AffCheck</span></span>

  - <span data-ttu-id="47a76-124">ChatMonitoringSummary</span><span class="sxs-lookup"><span data-stu-id="47a76-124">ChatMonitoringSummary</span></span>

  - <span data-ttu-id="47a76-125">Ferramenta ChatStress</span><span class="sxs-lookup"><span data-stu-id="47a76-125">ChatStress Tool</span></span>

  - <span data-ttu-id="47a76-126">ChatUpgradeVerifier</span><span class="sxs-lookup"><span data-stu-id="47a76-126">ChatUpgradeVerifier</span></span>

  - <span data-ttu-id="47a76-127">ChatUsageReport</span><span class="sxs-lookup"><span data-stu-id="47a76-127">ChatUsageReport</span></span>

  - <span data-ttu-id="47a76-128">ScheduleADSyncforPrincipal</span><span class="sxs-lookup"><span data-stu-id="47a76-128">ScheduleADSyncforPrincipal</span></span>

</div>

<div>

## <a name="affcheck"></a><span data-ttu-id="47a76-129">AffCheck</span><span class="sxs-lookup"><span data-stu-id="47a76-129">AffCheck</span></span>

<div>

## <a name="description"></a><span data-ttu-id="47a76-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="47a76-130">Description</span></span>

<span data-ttu-id="47a76-131">A ferramenta AffCheck confirma que o usuário de banco de dados de chat back-end persistente e os registros de afiliação de grupo correspondem aos serviços de domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="47a76-131">The AffCheck tool confirms that the Persistent Chat back-end database user and group affiliation records match that of Active Directory Domain Services.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="47a76-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47a76-132">Requirements</span></span>

<span data-ttu-id="47a76-133">A ferramenta é instalada com o instalador do PersistentChatResKit em um computador associado a um domínio.</span><span class="sxs-lookup"><span data-stu-id="47a76-133">The tool is installed with the PersistentChatResKit installer on a domain joined machine.</span></span>

<span data-ttu-id="47a76-134">A conta de usuário sob a qual a ferramenta é executada deve ter acesso de leitura ao banco de dados de back-end de chat persistente e aos serviços de domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="47a76-134">The user account under which the tool is run must have Read access to the Persistent Chat back-end database and Active Directory Domain Services.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="47a76-135">Uso</span><span class="sxs-lookup"><span data-stu-id="47a76-135">Usage</span></span>

<span data-ttu-id="47a76-136">Configure o arquivo AffCheck.exe.config de acordo com as instruções no arquivo de configuração e execute a ferramenta AffCheck sem parâmetros de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="47a76-136">Configure the AffCheck.exe.config file according to the instructions in the config file and run the AffCheck tool without command-line parameters.</span></span> <span data-ttu-id="47a76-137">Veja a seguir o conteúdo da AffCheck.exe.config padrão.</span><span class="sxs-lookup"><span data-stu-id="47a76-137">Following are the contents of the default AffCheck.exe.config.</span></span>

<span data-ttu-id="47a76-138">**AffCheck.exe.config:**</span><span class="sxs-lookup"><span data-stu-id="47a76-138">**AffCheck.exe.config:**</span></span>

```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
      <appSettings>
        <!--Domain Controller IP Address-->
        <add key="LDAP" value="LDAP://0.0.0.0/"/>
        
        <!-- Domain DN  This is case sensitive, it must match exactly-->
        <add key="DomainComponent" value ="DC=DOMAIN,DC=COM"/>
        
        <!--Domain Administrator Login and Password-->
        <add key="DomainLogin" value="DOMAIN\Administrator"/>
        <add key="DomainPassword" value ="password"/>
        
        <!-- Connection string to Group Chat Database-->
        <add key="ConnectionString" value="data source=SQL_SERVER\INSTANCE;initial catalog=DATABASE_NAME;integrated security=SSPI"/>
        
        <!--Check group affiliations-->
        <add key="CheckGroups" value="true"/>
        
        <!--Check user affilations-->
        <add key="CheckUsers" value="true"/>
        
        <!--List all affiliations if there is a mismatch between database and active directory-->
        <add key="ListAffiliations" value="true"/>
    
        <!--If you need to offset the results of the number of affilations in AD(can be negative to add to AD parent count)-->
        <add key="Offset" value ="0"/>
    
        <!--If you need to ignore certain parents, provide a semi colon delimitted list.-->
        <add key="Ignore" value ="DC=uatest,DC=test,DC=contoso,DC=com;DC=test,DC=contoso,DC=com"/>
      </appSettings>
    </configuration>
  ```
</div>

</div>

<div>

## <a name="chatmonitoringsummary"></a><span data-ttu-id="47a76-139">ChatMonitoringSummary</span><span class="sxs-lookup"><span data-stu-id="47a76-139">ChatMonitoringSummary</span></span>

<div>

## <a name="description"></a><span data-ttu-id="47a76-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="47a76-140">Description</span></span>

<span data-ttu-id="47a76-141">A ferramenta PersistentChatMonitoringSummary move as informações de monitoramento de chat persistente do banco de dados de monitoramento para um arquivo de log de CSV especificado.</span><span class="sxs-lookup"><span data-stu-id="47a76-141">The PersistentChatMonitoringSummary tool moves Persistent Chat monitoring information from the monitoring database into a specified CSV log file.</span></span>

<span data-ttu-id="47a76-142">O arquivo CSV conterá uma divisão de sessões de chat persistentes pelo número total de sessões, sessões bem-sucedidas, falhas inesperadas, falhas esperadas e uma divisão das falhas inesperadas por ID de diagnóstico, número de falhas e descrição de falha.</span><span class="sxs-lookup"><span data-stu-id="47a76-142">The CSV file will contain a breakdown of Persistent Chat sessions by number of total sessions, successful sessions, unexpected failures, expected failures, and a breakdown of the unexpected failures by diagnostic ID, number of failures, and failure description.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="47a76-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47a76-143">Requirements</span></span>

<span data-ttu-id="47a76-144">Instale as ferramentas do kit de recursos de chat persistente em uma máquina unida a um domínio que tenha acesso ao banco de dados de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="47a76-144">Install the Persistent Chat Resource Kit tools on a domain-joined machine that has access to the Monitoring database.</span></span>

<span data-ttu-id="47a76-145">A conta de usuário sob a qual a ferramenta é executada deve ter acesso de leitura ao banco de dados de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="47a76-145">The user account under which the tool runs must have Read access to the Monitoring database.</span></span>

<span data-ttu-id="47a76-146">O arquivo PersistentChatMonitoringSummary.exe.config deve conter uma \<connectionStrings\> seção que define a cadeia de conexão para o banco de dados de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="47a76-146">The file, PersistentChatMonitoringSummary.exe.config, must contain a \<connectionStrings\> section that defines the connection string to the Monitoring database.</span></span> <span data-ttu-id="47a76-147">Ele também deve conter uma chave para o PersistentChatEndpointUri para o qual os dados de monitoramento serão coletados e um caminho de arquivo para um local para o arquivo CSV que será gerado.</span><span class="sxs-lookup"><span data-stu-id="47a76-147">It must also contain a key for the PersistentChatEndpointUri that the monitoring data will be gathered for, and a file path to a location for the CSV file that will be generated.</span></span> <span data-ttu-id="47a76-148">Consulte o arquivo de configuração instalado para ver exemplos.</span><span class="sxs-lookup"><span data-stu-id="47a76-148">Refer to the installed config file for examples.</span></span> <span data-ttu-id="47a76-149">O arquivo deve estar localizado no mesmo diretório da ferramenta.</span><span class="sxs-lookup"><span data-stu-id="47a76-149">The file must be located in the same directory as the tool.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="47a76-150">Uso</span><span class="sxs-lookup"><span data-stu-id="47a76-150">Usage</span></span>

```Batch
    PersistentChatMonitoringSummary [-StartDateTime <date>] [-EndDateTime <date>]
```

<span data-ttu-id="47a76-151">Esses parâmetros definem a seleção dos dados:</span><span class="sxs-lookup"><span data-stu-id="47a76-151">These parameters define the selection of data:</span></span>

<span data-ttu-id="47a76-152">**StartDateTime:** Opcionalmente, especifica a data de início do período de seleção.</span><span class="sxs-lookup"><span data-stu-id="47a76-152">**StartDateTime:** Optionally specifies the start date of the selection period.</span></span> <span data-ttu-id="47a76-153">Padrão: 1/1/1753 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="47a76-153">Default: 1/1/1753 12:00:00 AM</span></span>

<span data-ttu-id="47a76-154">**EndDateTime:** Opcionalmente, especifica a última data do período de seleção.</span><span class="sxs-lookup"><span data-stu-id="47a76-154">**EndDateTime:** Optionally specifies the last date of the selection period.</span></span> <span data-ttu-id="47a76-155">Padrão: agora</span><span class="sxs-lookup"><span data-stu-id="47a76-155">Default: Now</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="47a76-156">Exemplo</span><span class="sxs-lookup"><span data-stu-id="47a76-156">Example</span></span>

```Batch
    C:\Users\Administrator.VDOMAIN>Desktop\PersistentChatMonitoringSummary.exe
    Reading database connection information, Persistent Chat endpoint uri, and csv output path information from the application config file...
    Connecting to Monitoring database with connection string specified in the application config file...
    Gathering Persistent Chat Session Summary information between "1/1/1753 12:00:00 AM" and "11/19/2012 10:11:25 AM" for Persistent Chat Endpoint Uri "persistentChatEndpointUri@domain.com"...
    Press enter to continue or hit ctr-c if these settings are incorrect...
    
    The summary information about Persistent Chat sessions from the Monitoring database has been output to C:\PersistentChatMonitoring_dd4ace24-4c8a-4a3d-8fd4-591bdfacf47b.csv
    Press enter to exit...
```

</div>

</div>

<div>

## <a name="persistent-chat-stress-tool"></a><span data-ttu-id="47a76-157">Ferramenta de stress de chat persistente</span><span class="sxs-lookup"><span data-stu-id="47a76-157">Persistent Chat Stress Tool</span></span>

<div>

## <a name="description"></a><span data-ttu-id="47a76-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="47a76-158">Description</span></span>

<span data-ttu-id="47a76-159">A ferramenta de carga de chat persistente oferece uma maneira fácil de simular o uso de chat persistente para testar o desempenho do mundo real, incluindo modelos de usuário diversos para se adequar melhor aos cenários de uso esperado.</span><span class="sxs-lookup"><span data-stu-id="47a76-159">The Persistent Chat Stress tool provides an easy way to simulate usage of Persistent Chat to test real-world performance, including varied user models to better fit your expected usage scenarios.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="47a76-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47a76-160">Requirements</span></span>

<span data-ttu-id="47a76-161">Instale as ferramentas do kit de recursos de chat persistentes em uma máquina unida a um domínio que tenha acesso ao banco de dados de back-end de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="47a76-161">Install the Persistent Chat Resource Kit tools onto a domain-joined machine that has access to the Persistent Chat back-end database.</span></span>

<span data-ttu-id="47a76-162">Além da máquina do *controlador* , você precisará de vários computadores *Loader* .</span><span class="sxs-lookup"><span data-stu-id="47a76-162">In addition to this *controller* machine, you will need several *loader* machines.</span></span> <span data-ttu-id="47a76-163">Para todos os usuários do 10K em seu modelo de usuário, você precisará pelo menos de 4 GB de RAM livres em um computador carregador.</span><span class="sxs-lookup"><span data-stu-id="47a76-163">For every 10K users in your user model, you will need at least 4GB of free RAM on a loader machine.</span></span> <span data-ttu-id="47a76-164">Por exemplo, uma execução com usuários do 80K exigirá cerca de 32 GB de RAM espalhada em todas as máquinas-carregador.</span><span class="sxs-lookup"><span data-stu-id="47a76-164">For example, a run with 80K users will require about 32GB of RAM spread across all loader machines.</span></span> <span data-ttu-id="47a76-165">Recomendamos que você tenha pelo menos três máquinas-carregador, independentemente da carga esperada.</span><span class="sxs-lookup"><span data-stu-id="47a76-165">We recommend that you have at least three loader machines, regardless of expected load.</span></span>

<span data-ttu-id="47a76-166">Os computadores carregador devem ter o .NET 4,5 Framework e também o redistribuível do Visual C++ 2012 instalado.</span><span class="sxs-lookup"><span data-stu-id="47a76-166">Loader machines must have the .NET 4.5 Framework as well as the Visual C++ 2012 Redistributable installed.</span></span>

</div>

<div>

## <a name="configuration"></a><span data-ttu-id="47a76-167">Configuração</span><span class="sxs-lookup"><span data-stu-id="47a76-167">Configuration</span></span>

<span data-ttu-id="47a76-168">Copie arquivos ChatStressTool para uma pasta compartilhada acessível a partir de todas as máquinas Loader.</span><span class="sxs-lookup"><span data-stu-id="47a76-168">Copy ChatStressTool files into a shared folder accessible from all loader machines.</span></span>

<span data-ttu-id="47a76-169">Crie usuários e canais para usar na execução de stress:</span><span class="sxs-lookup"><span data-stu-id="47a76-169">Create users and channels for use in the stress run:</span></span>

  - <span data-ttu-id="47a76-170">Crie quantos usuários forem as chamadas do modelo de usuário, habilite-os para o Lync e defina a política de chat persistente como habilitado.</span><span class="sxs-lookup"><span data-stu-id="47a76-170">Create as many users as your user model calls for, enable them for Lync, and set their Persistent Chat policy to Enabled.</span></span>

  - <span data-ttu-id="47a76-171">Crie uma categoria para seus canais de stress e, em seguida, crie quantas salas forem necessárias nessa categoria.</span><span class="sxs-lookup"><span data-stu-id="47a76-171">Create a category for your stress channels, and then create as many rooms as are needed under that category.</span></span> <span data-ttu-id="47a76-172">A categoria deve ter todos os usuários de stress na lista **permitida** (por meio da adição da UO) e as salas de stress devem ter uma configuração de privacidade **aberta**.</span><span class="sxs-lookup"><span data-stu-id="47a76-172">The category should have all stress users in its **Allowed** list (by way of adding their OU), and stress rooms should have a privacy setting of **Open**.</span></span>

  - <span data-ttu-id="47a76-173">Recomendamos a criação de salas de stress extras.</span><span class="sxs-lookup"><span data-stu-id="47a76-173">We recommend creating extra stress rooms.</span></span> <span data-ttu-id="47a76-174">Você pode criar salas de 50.000 com o seguinte comando de interface de linha de comando do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="47a76-174">You can create 50,000 rooms with the following Windows PowerShell command-line interface command:</span></span>
    ```Powershell
        for ($i = 0; $i -le 50000; $i++) { New-CsPersistentChatRoom -Category <parent category> -Name "StressChan_$i" -Privacy Open }
    ```    

<span data-ttu-id="47a76-175">Edite os arquivos de configuração de acordo com a sua topologia:</span><span class="sxs-lookup"><span data-stu-id="47a76-175">Edit the configuration files to fit your topology:</span></span>

<span data-ttu-id="47a76-176">Em **LoaderProcess.exe.config**, altere "Controller.contoso.com" para o nome de domínio totalmente qualificado (FQDN) do computador do controlador.</span><span class="sxs-lookup"><span data-stu-id="47a76-176">In **LoaderProcess.exe.config**, change “controller.contoso.com” to the controller machine’s fully qualified domain name (FQDN).</span></span>

<span data-ttu-id="47a76-177">Em **StressLauncher.exe.config:**</span><span class="sxs-lookup"><span data-stu-id="47a76-177">In **StressLauncher.exe.config:**</span></span>

1.  <span data-ttu-id="47a76-178">Altere o valor da configuração "LoaderBinary" para o caminho da pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="47a76-178">Change the “LoaderBinary” setting value to the shared folder’s path.</span></span>

2.  <span data-ttu-id="47a76-179">Altere "AdminUser"/"AdminPassword" para as credenciais que têm acesso de administrador a máquinas Loader.</span><span class="sxs-lookup"><span data-stu-id="47a76-179">Change “AdminUser”/”AdminPassword” to credentials that have admin access to loader machines.</span></span>

3.  <span data-ttu-id="47a76-180">Altere "ChannelCategory" para o nome da categoria na qual os canais de stress foram criados.</span><span class="sxs-lookup"><span data-stu-id="47a76-180">Change “ChannelCategory” to the name of the category that stress channels have been created under.</span></span>

4.  <span data-ttu-id="47a76-181">Altere "UserNamePattern" e "UserPasswordPattern" para um modelo que corresponda às suas credenciais de usuário de stress.</span><span class="sxs-lookup"><span data-stu-id="47a76-181">Change “UserNamePattern” and “UserPasswordPattern” to a template that matches your stress user credentials.</span></span> <span data-ttu-id="47a76-182">{0} é substituído pelo número de índice do usuário.</span><span class="sxs-lookup"><span data-stu-id="47a76-182">{0} is replaced with the user’s index number.</span></span>

5.  <span data-ttu-id="47a76-183">Altere "Domain" para o domínio SIP da sua topologia de teste.</span><span class="sxs-lookup"><span data-stu-id="47a76-183">Change “Domain” to the SIP domain of your test topology.</span></span>

6.  <span data-ttu-id="47a76-184">Altere "ConnectionString" para uma cadeia de conexão para seu banco de dados back-end de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="47a76-184">Change “ConnectionString” to a connection string for your Persistent Chat back-end database.</span></span>

7.  <span data-ttu-id="47a76-185">Altere "UserIndexStart" para o índice do primeiro usuário de stress.</span><span class="sxs-lookup"><span data-stu-id="47a76-185">Change “UserIndexStart” to the index of the first stress user.</span></span>

8.  <span data-ttu-id="47a76-186">Altere "LyncFQDN" para o FQDN do seu pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="47a76-186">Change “LyncFQDN” to the FQDN of your Front End pool.</span></span>

9.  <span data-ttu-id="47a76-187">Modifique a lista "máquinas" para incluir nomes de máquinas para todas as máquinas-carregador.</span><span class="sxs-lookup"><span data-stu-id="47a76-187">Modify the “Machines” list to include machine names for all of your loader machines.</span></span>

10. <span data-ttu-id="47a76-188">Altere o baseAddress do ponto de extremidade do serviço (o padrão é "controller.contoso.com") para o FQDN do seu computador controlador.</span><span class="sxs-lookup"><span data-stu-id="47a76-188">Change the baseAddress of the service endpoint (default is “controller.contoso.com”) to the FQDN of your controller machine.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="47a76-189">Uso</span><span class="sxs-lookup"><span data-stu-id="47a76-189">Usage</span></span>

<span data-ttu-id="47a76-190">Depois que a configuração for concluída, abra StressLauncher.exe no computador do controlador.</span><span class="sxs-lookup"><span data-stu-id="47a76-190">After configuration is complete, open StressLauncher.exe on the controller machine.</span></span> <span data-ttu-id="47a76-191">Você pode iniciar o StressLauncher como qualquer usuário.</span><span class="sxs-lookup"><span data-stu-id="47a76-191">You can launch StressLauncher as any user.</span></span> <span data-ttu-id="47a76-192">As credenciais sob as quais os processos do carregador são iniciados nas máquinas Loader devem ser especificadas no arquivo config.</span><span class="sxs-lookup"><span data-stu-id="47a76-192">The credentials under which the loader processes start on the loader machines must be specified in the config file.</span></span> <span data-ttu-id="47a76-193">Você também deve fornecer uma cadeia de conexão com acesso de leitura ao banco de dados back-end de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="47a76-193">You also must give a connection string that has Read access to the Persistent Chat back-end database.</span></span> <span data-ttu-id="47a76-194">Se essa cadeia de conexão usar a autenticação integrada do Windows, você deve iniciar o StressLauncher como um usuário que tem esse acesso.</span><span class="sxs-lookup"><span data-stu-id="47a76-194">If this connection string uses integrated Windows authentication, you must launch StressLauncher as a user that has this access.</span></span>

<span data-ttu-id="47a76-195">Altere as configurações do modelo de usuário conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="47a76-195">Alter the user model settings as needed.</span></span> <span data-ttu-id="47a76-196">Clique em **Iniciar carregamento** para iniciar uma execução.</span><span class="sxs-lookup"><span data-stu-id="47a76-196">Click **Start Load** to initiate a run.</span></span> <span data-ttu-id="47a76-197">Após alguns minutos, os usuários começarão a se conectar e a barra de progresso começará a ser preenchida.</span><span class="sxs-lookup"><span data-stu-id="47a76-197">After a minute or so, users will start being signed in, and the progress bar will begin to fill.</span></span> <span data-ttu-id="47a76-198">Nesse ponto, você pode conseguir que a máquina do controlador funcione e tome medidas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="47a76-198">At this point, you may can the controller machine working and take performance measurements.</span></span>

</div>

</div>

<div>

## <a name="chatupgradeverifier"></a><span data-ttu-id="47a76-199">ChatUpgradeVerifier</span><span class="sxs-lookup"><span data-stu-id="47a76-199">ChatUpgradeVerifier</span></span>

<div>

## <a name="description"></a><span data-ttu-id="47a76-200">Descrição</span><span class="sxs-lookup"><span data-stu-id="47a76-200">Description</span></span>

<span data-ttu-id="47a76-201">ChatUpgradeVerifier é uma ferramenta de comparação de banco de dados específica de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="47a76-201">ChatUpgradeVerifier is a Persistent Chat specific database comparison tool.</span></span> <span data-ttu-id="47a76-202">A ferramenta compara o banco de dados do grupo chat 2007 R2 ou do 2010 chat em grupo (2007/2010Db) ao banco de dados de chat persistente 2013 (2013Db).</span><span class="sxs-lookup"><span data-stu-id="47a76-202">The tool compares either the Group Chat 2007 R2 or Group Chat 2010 Database (2007/2010Db) to the Persistent Chat 2013 Database (2013Db).</span></span>

<span data-ttu-id="47a76-203">A ferramenta verificará, uma a uma, cada categoria, sala de chat persistente e suplemento em 2007/2010Db para ver se ela aparece no 2013Db.</span><span class="sxs-lookup"><span data-stu-id="47a76-203">The tool will check, one by one, each category, Persistent Chat room, and add-in in 2007/2010Db to see if it appears in the 2013Db.</span></span> <span data-ttu-id="47a76-204">A comparação inclui a verificação de todas as configurações da categoria, da sala de chat ou do suplemento, de qualquer entidade de segurança em escopo na categoria e de qualquer entidade de segurança em uma função na categoria ou na sala de chat.</span><span class="sxs-lookup"><span data-stu-id="47a76-204">The comparison includes checking all settings on the category, chat room, or add-in, any principals in scope on the category, and any principal in a role on either the category or the chat room.</span></span> <span data-ttu-id="47a76-205">Se uma categoria ou uma sala de chat não aparecer corretamente no 2013Db, as diferenças serão exibidas para um arquivo de conflitos.</span><span class="sxs-lookup"><span data-stu-id="47a76-205">If a category or a chat room does not appear correctly in the 2013Db, the differences will be output to a conflicts file.</span></span> <span data-ttu-id="47a76-206">Se, após a atualização, o 2007/2010Db for alterado e essa ferramenta for executada, haverá uma saída de diferenças para o arquivo de conflitos.</span><span class="sxs-lookup"><span data-stu-id="47a76-206">If, after the upgrade has occurred, the 2007/2010Db is changed and then this tool is run, there will be a differences output to the conflicts file.</span></span> <span data-ttu-id="47a76-207">Observe que esse aplicativo é uma ferramenta de comparação de banco de dados apenas e não valida o processo de atualização.</span><span class="sxs-lookup"><span data-stu-id="47a76-207">Note that this application is a database comparison tool only and does not validate the upgrade process.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="47a76-208">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47a76-208">Requirements</span></span>

<span data-ttu-id="47a76-209">Instale as ferramentas do kit de recursos de chat persistente em uma máquina unida a um domínio que tenha acesso aos bancos de dados de back-end de chat persistente (versões anteriores e atuais para chat persistente).</span><span class="sxs-lookup"><span data-stu-id="47a76-209">Install the Persistent Chat Resource Kit tools on a domain-joined machine that has access to the Persistent Chat back-end databases (previous and current versions for Persistent Chat).</span></span>

<span data-ttu-id="47a76-210">A conta de usuário sob a qual a ferramenta é executada deve ter acesso de leitura aos bancos de dados de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="47a76-210">The user account under which the tool runs must have Read access to the Persistent Chat databases.</span></span>

<span data-ttu-id="47a76-211">O arquivo ChatUpgradeVerifier.exe.config deve conter o parâmetro GroupChat2007R2Db ou o parâmetro GroupChat2010Db, com uma cadeia de conexão para o banco de dados de chat de grupo apropriado (Groupchat 2007R2 ou 2010).</span><span class="sxs-lookup"><span data-stu-id="47a76-211">The ChatUpgradeVerifier.exe.config file must contain either the GroupChat2007R2Db parameter or the GroupChat2010Db parameter, with a connection string to the appropriate Group Chat database (either Groupchat 2007R2 or 2010).</span></span> <span data-ttu-id="47a76-212">Ele também deve conter um parâmetro PersistentChat2013Db com uma cadeia de conexão para o banco de dados chat persistente 2013.</span><span class="sxs-lookup"><span data-stu-id="47a76-212">It must also contain a PersistentChat2013Db parameter, with a connection string to the Persistent Chat 2013 database.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="47a76-213">Uso</span><span class="sxs-lookup"><span data-stu-id="47a76-213">Usage</span></span>

<span data-ttu-id="47a76-214">Execute **ChatUpgradeVerifier** sem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="47a76-214">Run **ChatUpgradeVerifier** without any parameters.</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="47a76-215">Exemplo</span><span class="sxs-lookup"><span data-stu-id="47a76-215">Example</span></span>

<span data-ttu-id="47a76-216">![Executando ChatUpgradeVerifier.exe.](images/JJ945599.4c273bc3-7926-47c7-ade7-34522721ebf9(OCS.15).jpg "Executando ChatUpgradeVerifier.exe.")</span><span class="sxs-lookup"><span data-stu-id="47a76-216">![Running ChatUpgradeVerifier.exe.](images/JJ945599.4c273bc3-7926-47c7-ade7-34522721ebf9(OCS.15).jpg "Running ChatUpgradeVerifier.exe.")</span></span>

</div>

</div>

<div>

## <a name="persistent-chat-usage-report"></a><span data-ttu-id="47a76-217">Relatório de uso de chat persistente</span><span class="sxs-lookup"><span data-stu-id="47a76-217">Persistent Chat Usage Report</span></span>

<div>

## <a name="description"></a><span data-ttu-id="47a76-218">Descrição</span><span class="sxs-lookup"><span data-stu-id="47a76-218">Description</span></span>

<span data-ttu-id="47a76-219">A ferramenta ChatUsageReport gera um relatório HTML de uso do serviço de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="47a76-219">The ChatUsageReport tool generates an HTML report of Persistent Chat service usage.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="47a76-220">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47a76-220">Requirements</span></span>

<span data-ttu-id="47a76-221">Instale as ferramentas do kit de recursos de chat persistente em uma máquina unida a um domínio que tenha acesso ao banco de dados de back-end de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="47a76-221">Install the Persistent Chat Resource Kit tools on a domain-joined machine that has access to the Persistent Chat back-end database.</span></span>

<span data-ttu-id="47a76-222">A conta de usuário sob a qual a ferramenta é executada deve ter acesso de leitura ao banco de dados back-end de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="47a76-222">The user account under which the tool is run must have Read access to the Persistent Chat back-end database.</span></span>

<span data-ttu-id="47a76-223">O arquivo ChatUsageReport.exe.config deve conter uma \<connectionStrings\> seção que define a cadeia de conexão para o banco de dados back-end de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="47a76-223">The file, ChatUsageReport.exe.config, must contain a \<connectionStrings\> section defining the connection string to the Persistent Chat back-end database.</span></span> <span data-ttu-id="47a76-224">O conteúdo do arquivo de configuração padrão está incluído aqui para sua referência.</span><span class="sxs-lookup"><span data-stu-id="47a76-224">The contents of the default config file are included here, for your reference.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="47a76-225">Uso</span><span class="sxs-lookup"><span data-stu-id="47a76-225">Usage</span></span>

```Powershell
    ChatUsageReport [-StartDate {date}] [-EndDate {date}] [-TopActiveUsers {n}] [-TopActiveRooms {n}] [-LeastActiveRooms {n}] [-RoomsInactiveSince {Date}] [-OutputFolder {path}]
```
<span data-ttu-id="47a76-226">Esses parâmetros definem a seleção dos dados:</span><span class="sxs-lookup"><span data-stu-id="47a76-226">These parameters define the selection of data:</span></span>

<span data-ttu-id="47a76-227">**StartDate:** Opcionalmente, especifica a data de início do UTC do período de seleção.</span><span class="sxs-lookup"><span data-stu-id="47a76-227">**StartDate:** Optionally specifies the UTC start date of the selection period.</span></span> <span data-ttu-id="47a76-228">Padrão: data mais antiga</span><span class="sxs-lookup"><span data-stu-id="47a76-228">Default: Earliest Date</span></span>

<span data-ttu-id="47a76-229">**EndDate:** Opcionalmente, especifica a data de término UTC do período de seleção.</span><span class="sxs-lookup"><span data-stu-id="47a76-229">**EndDate:** Optionally specifies the UTC end date of the selection period.</span></span> <span data-ttu-id="47a76-230">Padrão: agora</span><span class="sxs-lookup"><span data-stu-id="47a76-230">Default: Now</span></span>

<span data-ttu-id="47a76-231">Esses parâmetros definem como e quais dados são exibidos:</span><span class="sxs-lookup"><span data-stu-id="47a76-231">These parameters define how and what data is displayed:</span></span>

<span data-ttu-id="47a76-232">**TopActiveUsers:** Se for especificado, o relatório incluirá os n usuários mais ativos em termos do número de mensagens que o usuário publicou na sala de chat para o período selecionado.</span><span class="sxs-lookup"><span data-stu-id="47a76-232">**TopActiveUsers:** If this is specified, the report will include the n most active users in terms of the number of messages the user has posted in the chat room for the selected period.</span></span> <span data-ttu-id="47a76-233">Padrão: 10</span><span class="sxs-lookup"><span data-stu-id="47a76-233">Default: 10</span></span>

<span data-ttu-id="47a76-234">**TopActiveRooms:** Se for especificado, o relatório incluirá o n salas de chat mais ativos em termos do número de mensagens postadas na sala para o período selecionado.</span><span class="sxs-lookup"><span data-stu-id="47a76-234">**TopActiveRooms:** If this is specified, the report will include the n most active chat rooms in terms of the number of messages posted in the room for the selected period.</span></span> <span data-ttu-id="47a76-235">Padrão: 10</span><span class="sxs-lookup"><span data-stu-id="47a76-235">Default: 10</span></span>

<span data-ttu-id="47a76-236">**LeastActiveRooms:** Se for especificado, o relatório incluirá as n menos salas de chat ativa em termos do número de mensagens postadas na sala de chat do período selecionado.</span><span class="sxs-lookup"><span data-stu-id="47a76-236">**LeastActiveRooms:** If this is specified, the report will include the n least active chat rooms in terms of the number of messages posted in the chat room for the selected period.</span></span> <span data-ttu-id="47a76-237">As salas terão pelo menos uma mensagem postada.</span><span class="sxs-lookup"><span data-stu-id="47a76-237">Rooms will have at least one message posted.</span></span> <span data-ttu-id="47a76-238">Padrão: 10</span><span class="sxs-lookup"><span data-stu-id="47a76-238">Default: 10</span></span>

<span data-ttu-id="47a76-239">**RoomsInactiveSince:** Se for especificado, o relatório incluirá uma lista de salas de chat que foram inativas desde a data especificada.</span><span class="sxs-lookup"><span data-stu-id="47a76-239">**RoomsInactiveSince:** If this is specified, the report will include a list of chat rooms that have been inactive since the specified date.</span></span> <span data-ttu-id="47a76-240">Padrão: hora inteira</span><span class="sxs-lookup"><span data-stu-id="47a76-240">Default: Entire Time</span></span>

<span data-ttu-id="47a76-241">**OutputFolder:** A pasta na qual as imagens do ChatUsageReport.html e do gráfico serão colocadas.</span><span class="sxs-lookup"><span data-stu-id="47a76-241">**OutputFolder:** The folder where the ChatUsageReport.html and the graph images will be placed.</span></span> <span data-ttu-id="47a76-242">Isso deve ser definido no arquivo de configuração ou na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="47a76-242">This must be defined in the config file or on the command line.</span></span>

<span data-ttu-id="47a76-243">Todos os valores de parâmetro de linha de comando também podem ser especificados no arquivo ChatUsageReport.exe.config localizado no mesmo diretório da ferramenta.</span><span class="sxs-lookup"><span data-stu-id="47a76-243">All of the command line parameter values can also be specified in the ChatUsageReport.exe.config file that is located in the same directory as the tool.</span></span> <span data-ttu-id="47a76-244">Se algum valor for especificado no arquivo de configuração e na linha de comando, o valor de linha de comando substituirá o valor do arquivo config.</span><span class="sxs-lookup"><span data-stu-id="47a76-244">If any value is specified in both the config file and the command line, the command line value will override the config file value.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="47a76-245">Resultado</span><span class="sxs-lookup"><span data-stu-id="47a76-245">Output</span></span>

<span data-ttu-id="47a76-246">O relatório irá sempre incluir a seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="47a76-246">The report will always include the following output:</span></span>

  - <span data-ttu-id="47a76-247">N mais alto salas de chat ativas pelo número de postagens de mensagem para o período selecionado.</span><span class="sxs-lookup"><span data-stu-id="47a76-247">Top n most active chat rooms by number of message posts for selected period.</span></span>

  - <span data-ttu-id="47a76-248">N primeiros da maioria dos usuários ativos por número de postagens de mensagem para o período selecionado.</span><span class="sxs-lookup"><span data-stu-id="47a76-248">Top n most active users by number of message posts for selected period.</span></span>

  - <span data-ttu-id="47a76-249">Top n menos salas de chat ativa por número de postagens de mensagem para o período selecionado.</span><span class="sxs-lookup"><span data-stu-id="47a76-249">Top n least active chat rooms by number of message posts for selected period.</span></span>

  - <span data-ttu-id="47a76-250">Salas de chat que estão inativas para toda a vida do banco de dados ou desde a data especificada.</span><span class="sxs-lookup"><span data-stu-id="47a76-250">Chat rooms that are inactive for the entire life of the database, or since the specified date.</span></span>

  - <span data-ttu-id="47a76-251">Tendência da postagem de mensagem diária para o período selecionado.</span><span class="sxs-lookup"><span data-stu-id="47a76-251">Daily message post trend for selected period.</span></span>

  - <span data-ttu-id="47a76-252">Tendência da postagem de mensagem semanal para o período selecionado.</span><span class="sxs-lookup"><span data-stu-id="47a76-252">Weekly message post trend for selected period.</span></span>

  - <span data-ttu-id="47a76-253">Tendência da postagem da mensagem mensal do período selecionado.</span><span class="sxs-lookup"><span data-stu-id="47a76-253">Monthly message post trend for selected period.</span></span>

  - <span data-ttu-id="47a76-254">Total de postagens de mensagem para o período selecionado.</span><span class="sxs-lookup"><span data-stu-id="47a76-254">Total message posts for selected period.</span></span>

  - <span data-ttu-id="47a76-255">Número total de salas habilitadas.</span><span class="sxs-lookup"><span data-stu-id="47a76-255">Total number of enabled rooms.</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="47a76-256">Exemplo</span><span class="sxs-lookup"><span data-stu-id="47a76-256">Example</span></span>

<span data-ttu-id="47a76-257">O exemplo a seguir gera um relatório de uso do ano inteiro 2001 e coloca o relatório no OutputFolder especificado no ChatUsageReport.exe.config.</span><span class="sxs-lookup"><span data-stu-id="47a76-257">The following example generates a usage report for the entire year 2001 and places the report in the OutputFolder specified in the ChatUsageReport.exe.config.</span></span>

```Powershell
    ChatUsageReport -RoomsInactiveSince 06-20-2010
```
<span data-ttu-id="47a76-258">ChatUsageReport.exe.config:</span><span class="sxs-lookup"><span data-stu-id="47a76-258">ChatUsageReport.exe.config:</span></span>

```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
      <connectionStrings>
        <!-- The PersistentChat connection string must be defined in this file. -->
        <add name="PersistentChat" connectionString="Data Source=contoso.com\RTC;Initial Catalog=mgc;Integrated Security=SSPI"/>
      </connectionStrings>
      <appSettings>
        <!-- The OutputFolder must be defined here or on the command line. -->
        <add key="OutputFolder" value="."/>
        <!-- The values below are the same as the application defaults. -->
        <add key="StartDate" value="01/01/0001"/>
        <add key="EndDate" value="12/31/9999"/>
        <add key="TopActiveUsers" value="10"/>
        <add key="TopActiveRooms" value="10"/>
        <add key="LeastActiveRooms" value="10"/>
        <add key="RoomsInactiveSince" value="01/01/0001"/>
      </appSettings>
    </configuration></configuration>
```
</div>

</div>

<div>

## <a name="scheduleadsyncforprincipal"></a><span data-ttu-id="47a76-259">ScheduleADSyncForPrincipal</span><span class="sxs-lookup"><span data-stu-id="47a76-259">ScheduleADSyncForPrincipal</span></span>

<div>

## <a name="description"></a><span data-ttu-id="47a76-260">Descrição</span><span class="sxs-lookup"><span data-stu-id="47a76-260">Description</span></span>

<span data-ttu-id="47a76-261">O ScheduleADSyncForPrincipal é um script do Microsoft SQL Server 2012 que deve ser executado diretamente no SQL Server Management Studio quando conectado ao banco de dados de back-end de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="47a76-261">ScheduleADSyncForPrincipal is a Microsoft SQL Server 2012 script that must be run directly from within SQL Server Management Studio when connected to the Persistent Chat back-end database.</span></span> <span data-ttu-id="47a76-262">Esse script permite forçar o chat persistente a sincronizar seus registros de um usuário com aqueles dos serviços de domínio Active Directory, em vez de aguardar o tempo de sincronização agendado.</span><span class="sxs-lookup"><span data-stu-id="47a76-262">This script enables you to force Persistent Chat to synchronize its records of a user with those of Active Directory Domain Services, rather than waiting for the scheduled synchronization time.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="47a76-263">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47a76-263">Requirements</span></span>

<span data-ttu-id="47a76-264">A conta de usuário sob a qual o script é executado deve ter acesso proprietário ao banco de dados de back-end de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="47a76-264">The user account under which the script is run must have owner access to the Persistent Chat back-end database.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="47a76-265">Uso</span><span class="sxs-lookup"><span data-stu-id="47a76-265">Usage</span></span>

<span data-ttu-id="47a76-266">Veja a seguir o conteúdo do script padrão:</span><span class="sxs-lookup"><span data-stu-id="47a76-266">Following are the contents of the default script:</span></span>

```Powershell
    /*
    This script will schedule a principal for a forced AD synchronization cycle
    
    If you're using Sql Server Management Studio, pressing Ctrl+Shift+M will 
    allow you to specify values for the template parameter.
    */
    
        insert into
          tblPrincipalMeta
          (
           prinID
          ,prinAffiliationsDirty
          ,prinAttributesDirty
          ,prinDeleted
          )
          select
            prinID
           ,1
           ,1
           ,0
          from
            tblPrincipal
          where
            prinID not in (select prinID from tblPrincipalMeta) and
            prinID = <PrinID,int,0>
     
        update
          tblPrincipalMeta
        set
          prinAffiliationsDirty = 1
         ,prinAttributesDirty = 1
         ,tryCount = 0
         ,nextTry = null
        where
         prinID = <PrinID,int,0>
```

<span data-ttu-id="47a76-267"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="47a76-267"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

