---
title: 'Lync Server 2013: Protegendo os bancos de dados'
description: 'Lync Server 2013: proteção e proteção de bancos de dados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardening and protecting the databases of Lync Server 2013
ms:assetid: 6953e721-3511-4235-b848-51bab093dc89
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518330(v=OCS.15)
ms:contentKeyID: 62625490
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af1ed8f54384e8ecac3b1e4ce6a4253a10bcc2c6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427758"
---
# <a name="hardening-and-protecting-the-databases-of-lync-server-2013"></a><span data-ttu-id="c1944-103">Protegendo os bancos de dados do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c1944-103">Hardening and protecting the databases of Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c1944-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c1944-104">

<span> </span></span></span>

<span data-ttu-id="c1944-105">_**Tópico da última modificação:** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="c1944-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="c1944-106">O Microsoft Lync Server 2013 também depende dos bancos de dados do SQL Server para armazenar informações do usuário, o estado da conferência, os dados de arquivamento e os registros de detalhes da chamada (CDRs).</span><span class="sxs-lookup"><span data-stu-id="c1944-106">Microsoft Lync Server 2013 also depends on SQL Server databases for storing user information, conference state, archiving data, and Call Detail Records (CDRs).</span></span> <span data-ttu-id="c1944-107">Você pode maximizar a disponibilidade dos dados do Lync Server 2013 em bancos de dados back-end do Lync Server, Particionando os dados do aplicativo de forma a melhorar a tolerância a falhas e simplificar a solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="c1944-107">You can maximize the availability of Lync Server 2013 data on Lync Server back-end databases, by partitioning the application data in a way that improves fault tolerance and simplifies troubleshooting.</span></span> <span data-ttu-id="c1944-108">Para alcançar essas metas, Particione os dados do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="c1944-108">To achieve these goals, partition the application data by:</span></span>

  - <span data-ttu-id="c1944-109">**Usando as práticas recomendadas de particionamento do servidor**   Separe o sistema operacional, o aplicativo e os arquivos de programas dos seus arquivos de dados.</span><span class="sxs-lookup"><span data-stu-id="c1944-109">**Using server partitioning best practices**   Separate your operating system, application, and program files from your data files.</span></span>

  - <span data-ttu-id="c1944-110">**Armazenando arquivos de log de transações e arquivos de banco de dados**   Armazene esses arquivos separadamente para aumentar a tolerância a falhas e otimizar a recuperação e armazená-los em um disco ou volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="c1944-110">**Storing transaction log files and database files**   Store these files separately to increase fault tolerance and optimize recovery, and store them on an encrypted disk or volume.</span></span>

  - <span data-ttu-id="c1944-111">**Usar o agrupamento do servidor**   Cluster os servidores back-end para otimizar a disponibilidade do sistema do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c1944-111">**Using server clustering**   Cluster the back-end servers to optimize Lync Server 2013 system availability.</span></span>

  - <span data-ttu-id="c1944-112">**Garantir que todos os backups de dados sejam criptografados e devidamente manipulados**   Uma mídia de backup perdida, descartada ou mal colocada pode representar uma ameaça significativa à segurança de dados para implantações do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c1944-112">**Ensure that all data backups are encrypted and properly handled**   Lost, discarded, or misplaced backup media can pose a significant threat to data security for Lync Server 2013 deployments</span></span>

<span data-ttu-id="c1944-113">Em qualquer servidor do Lync Server 2013, exceto o Standard Edition Server, a instância do SQL Server Express (instância RTCLOCAL) não é acessível remotamente, e nenhuma exceção de firewall local é criada, exceto para o SQL Server Express em um servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="c1944-113">On any Lync Server 2013 server except Standard Edition server, the SQL Server Express instance (RTCLOCAL instance) is not remotely accessible, and no local firewall exceptions are created, except for SQL Server Express on a Standard Edition server.</span></span> <span data-ttu-id="c1944-114">Em um servidor Standard Edition, o banco de dados back-end e o repositório de gerenciamento central (CMS) estão configurados para serem acessíveis remotamente.</span><span class="sxs-lookup"><span data-stu-id="c1944-114">On a Standard Edition server, both the back-end database and the Central Management store (CMS) are set up to be remotely accessible.</span></span> <span data-ttu-id="c1944-115">Para proteger bancos de dados do SQL Server, você pode fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c1944-115">To harden SQL Server databases, you can do the following:</span></span>

  - <span data-ttu-id="c1944-116">Personalize o Firewall do SQL Server Express nos servidores do Standard Edition, limitando o escopo de servidores que podem acessar o banco de dados remotamente.</span><span class="sxs-lookup"><span data-stu-id="c1944-116">Customize the SQL Server Express firewall on Standard Edition servers, limiting the scope of servers that can remotely access the database.</span></span> <span data-ttu-id="c1944-117">Por padrão, qualquer endereço IP pode acessar remotamente o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c1944-117">By default, any IP address can remotely access the database.</span></span>

  - <span data-ttu-id="c1944-118">Use o Gerenciador de configuração do SQL Server para especificar os protocolos, endereços IP e portas para o acesso remoto do SQL Server:</span><span class="sxs-lookup"><span data-stu-id="c1944-118">Use SQL Server Configuration Manager to specify the protocols, IP addresses, and ports for SQL Server remote access:</span></span>
    
      - <span data-ttu-id="c1944-119">O Lync Server 2013 usa o protocolo TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="c1944-119">Lync Server 2013 uses the TCP/IP protocol.</span></span> <span data-ttu-id="c1944-120">Ele dá suporte a IP versão 4 (IPv4), mas não IP versão 6 (IPv6).</span><span class="sxs-lookup"><span data-stu-id="c1944-120">It supports IP version 4 (IPv4), but not IP version 6 (IPv6).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="c1944-121">O Lync Server 2013 pode funcionar em uma rede com a pilha de IP duplo habilitada.</span><span class="sxs-lookup"><span data-stu-id="c1944-121">Lync Server 2013 can function in a network with dual IP stack enabled.</span></span>

        
        </div>
    
      - <span data-ttu-id="c1944-122">O Lync Server 2013 dá suporte a vários endereços IP (cartões de endereço de rede de hospedagem múltipla).</span><span class="sxs-lookup"><span data-stu-id="c1944-122">Lync Server 2013 supports multiple IP address (multi-homed network address cards).</span></span> <span data-ttu-id="c1944-123">Você pode especificar que o SQL Server escuta apenas em endereços IP específicos (endereço individual ou sub-rede) e usar somente protocolos específicos.</span><span class="sxs-lookup"><span data-stu-id="c1944-123">You can specify that SQL Server listen only to specific IP addresses (individual address or by subnet) and only use specific protocols.</span></span>
    
      - <span data-ttu-id="c1944-124">O Lync Server 2013 dá suporte a portas estáticas e dinâmicas do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c1944-124">Lync Server 2013 supports static and dynamic SQL Server ports.</span></span>

  - <span data-ttu-id="c1944-125">Execute o SQL Server em uma porta estática (não padrão) e não execute o navegador do SQL Server (para que ele não possa relatar a porta de escuta para o cliente).</span><span class="sxs-lookup"><span data-stu-id="c1944-125">Run SQL Server on a static (non-default) port, and do not run SQL Server Browser (so it cannot report the listening port to the client).</span></span> <span data-ttu-id="c1944-126">Isso requer uma configuração personalizada em cada cliente do SQL Server, incluindo servidores de front-end, Monitoring Server, servidor de arquivamento e consoles administrativos (executando o Shell de gerenciamento do Lync Server, o painel de controle do Lync Server ou o construtor de topologias) e todos os outros servidores que executam bancos de dados do Lync Server).</span><span class="sxs-lookup"><span data-stu-id="c1944-126">This requires a custom configuration on each SQL Server client, including Front End Servers, Monitoring Server, Archiving Server, and administrative consoles (running Lync Server Management Shell, Lync Server Control Panel, or Topology Builder), and all other servers running Lync Server databases).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c1944-127">O acesso a bancos de dados deve estar limitado a administradores de banco de dados confiáveis.</span><span class="sxs-lookup"><span data-stu-id="c1944-127">Access to databases must be limited to trusted database administrators.</span></span> <span data-ttu-id="c1944-128">Um administrador de banco de dados mal-intencionado pode inserir ou modificar dados em bancos de dados para obter privilégios nos servidores do Lync Server 2013 ou obter informações confidenciais dos serviços, mesmo se o administrador do banco de dados não tiver sido concedido acesso direto ou controle dos servidores do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c1944-128">A malicious database administrator could insert or modify data into the databases to acquire privileges over the Lync Server 2013 servers or obtain sensitive information from the services, even if the database administrator has not been granted direct access or control of the Lync Server 2013 servers.</span></span>



</div>

<span data-ttu-id="c1944-129">Para obter detalhes sobre configurações personalizadas e proteção de bancos de dados do SQL Server, consulte o artigo sobre o blog NextHop, "usando o Lync Server 2010 com uma configuração de rede personalizada do SQL Server" em [https://go.microsoft.com/fwlink/p/?LinkId=214008](https://go.microsoft.com/fwlink/p/?linkid=214008) .</span><span class="sxs-lookup"><span data-stu-id="c1944-129">For details about custom configurations and hardening SQL Server databases, see the NextHop blog article, "Using Lync Server 2010 with a Custom SQL Server Network Configuration," at [https://go.microsoft.com/fwlink/p/?LinkId=214008](https://go.microsoft.com/fwlink/p/?linkid=214008).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c1944-130">Você também pode proteger sistemas operacionais e servidores de aplicativos, e pode usar a política de grupo para implementar bloqueios de segurança na implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c1944-130">You can also harden operating systems and applications servers, and you can use Group Policy to implement security lockdowns in your Lync Server deployment.</span></span> <span data-ttu-id="c1944-131">Para obter detalhes, consulte <A href="lync-server-2013-hardening-and-protecting-servers-and-applications.md">protegendo e protegendo servidores e aplicativos para o Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="c1944-131">For details, see <A href="lync-server-2013-hardening-and-protecting-servers-and-applications.md">Hardening and protecting servers and applications for Lync Server 2013</A>.</span></span>



<span data-ttu-id="c1944-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c1944-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

