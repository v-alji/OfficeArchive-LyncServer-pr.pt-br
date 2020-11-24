---
title: 'Lync Server 2013: Configurando o armazenamento para arquivamento'
description: 'Lync Server 2013: Configurando o armazenamento para arquivamento.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up storage for Archiving
ms:assetid: f751245c-743e-454f-8325-968ae5e3de71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205392(v=OCS.15)
ms:contentKeyID: 48185858
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f7ee431b17b31c49ace7fae1f90d79ec6de2ada4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389767"
---
# <a name="setting-up-storage-for-archiving-in-lync-server-2013"></a><span data-ttu-id="42350-103">Configurando o armazenamento para arquivamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42350-103">Setting up storage for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42350-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42350-104">

<span> </span></span></span>

<span data-ttu-id="42350-105">_**Tópico da última modificação:** 2013-12-17_</span><span class="sxs-lookup"><span data-stu-id="42350-105">_**Topic Last Modified:** 2013-12-17_</span></span>

<span data-ttu-id="42350-106">O arquivamento de armazenamento do Lync Server 2013 inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="42350-106">Archiving storage for Lync Server 2013 includes the following:</span></span>

  - <span data-ttu-id="42350-107">**Armazenamento de dados**   O armazenamento de dados é necessário para armazenar o conteúdo de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="42350-107">**Data storage**   Data storage is required to store IM content.</span></span>

  - <span data-ttu-id="42350-108">**Armazenamento de arquivos**   O armazenamento de arquivos é necessário para armazenar o armazenamento de dados de conteúdo de conferência (reunião) e o armazenamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="42350-108">**File storage**   File storage is required to store conferencing (meeting) content data storage and file storage.</span></span>

<div>

## <a name="setting-up-data-storage"></a><span data-ttu-id="42350-109">Configurando o armazenamento de dados</span><span class="sxs-lookup"><span data-stu-id="42350-109">Setting Up Data Storage</span></span>

<span data-ttu-id="42350-110">Os requisitos para a configuração do armazenamento de dados para o arquivamento no Lync Server 2013 dependem de como você deseja armazenar dados de arquivamento:</span><span class="sxs-lookup"><span data-stu-id="42350-110">Requirements for setting up data storage for Archiving in Lync Server 2013 depend on how you want to store archiving data:</span></span>

  - <span data-ttu-id="42350-111">Integre o arquivamento do Lync Server 2013 com a implantação do Exchange para armazenar o arquivamento de dados usando o armazenamento do Exchange.</span><span class="sxs-lookup"><span data-stu-id="42350-111">Integrate Lync Server 2013 Archiving with your Exchange deployment to store Archiving data using Exchange storage.</span></span>

  - <span data-ttu-id="42350-112">Configurar servidores de banco de dados SQL Server separados para armazenar dados de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="42350-112">Set up separate SQL Server database servers to store Archiving data.</span></span>

<div>

## <a name="setting-up-exchange-storage-for-archiving-data"></a><span data-ttu-id="42350-113">Configurando o armazenamento do Exchange para arquivar dados</span><span class="sxs-lookup"><span data-stu-id="42350-113">Setting Up Exchange Storage for Archiving Data</span></span>

<span data-ttu-id="42350-114">A configuração do Exchange para armazenamento de dados de arquivamento requer que sua implantação do Exchange esteja executando o Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="42350-114">Setting up Exchange for storage of Archiving data requires that your Exchange deployment is running Exchange 2013.</span></span> <span data-ttu-id="42350-115">Além disso, as caixas de correio do usuário devem ser hospedadas no servidor Exchange 2013 e suas caixas de correio devem ser colocadas em In-Place isenção.</span><span class="sxs-lookup"><span data-stu-id="42350-115">Additionally, user mailboxes must be homed on the Exchange 2013 server and their mailboxes must be put on In-Place Hold.</span></span> <span data-ttu-id="42350-116">Para obter detalhes sobre como configurar o Exchange 2013, consulte a documentação do produto Exchange.</span><span class="sxs-lookup"><span data-stu-id="42350-116">For details about configuring Exchange 2013, see the Exchange product documentation.</span></span>

</div>

<div>

## <a name="setting-up-sql-server-database-servers-for-storage-of-archiving-data"></a><span data-ttu-id="42350-117">Configurando servidores de banco de dados SQL Server para armazenamento de dados de arquivamento</span><span class="sxs-lookup"><span data-stu-id="42350-117">Setting Up SQL Server Database Servers for Storage of Archiving Data</span></span>

<span data-ttu-id="42350-118">O arquivamento no Lync Server 2013 exige que o software de banco de dados do SQL Server armazene os dados arquivados, a menos que você integre a implantação com o Exchange.</span><span class="sxs-lookup"><span data-stu-id="42350-118">Archiving in Lync Server 2013 requires the SQL Server database software to store the archived data, unless you integrate your deployment with Exchange.</span></span>

<span data-ttu-id="42350-119">Para bancos de dados de arquivamento do SQL Server, você deve instalar o SQL Server no computador que irá hospedar o banco de dados de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="42350-119">For SQL Server archiving databases, you must install SQL Server on the computer that will host the Archiving database.</span></span> <span data-ttu-id="42350-120">Você pode usar a mesma instância SQL que você usa para o banco de dados back-end de um pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="42350-120">You can use the same SQL instance that you use for the back-end database of a Front End pool.</span></span> <span data-ttu-id="42350-121">Para obter o melhor desempenho, você deve implantar o banco de dados de arquivamento em um computador separado do repositório de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="42350-121">For best performance, you should deploy the Archiving database on a computer that is separate from the Central Management store.</span></span> <span data-ttu-id="42350-122">Para obter detalhes sobre a colocação de componentes do Lync Server 2013, consulte [colocação do servidor com suporte no Lync server 2013](lync-server-2013-supported-server-collocation.md) na documentação de suporte.</span><span class="sxs-lookup"><span data-stu-id="42350-122">For details about collocating Lync Server 2013 components, see [Supported server collocation in Lync Server 2013](lync-server-2013-supported-server-collocation.md) in the Supportability documentation.</span></span>

<span data-ttu-id="42350-123">Cada servidor de banco de dados deve estar executando uma versão com suporte do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="42350-123">Each database server must be running a supported version of SQL Server.</span></span> <span data-ttu-id="42350-124">Para obter detalhes sobre as versões com suporte, consulte [requisitos técnicos para arquivamento no Lync Server 2013](lync-server-2013-technical-requirements-for-archiving.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="42350-124">For details about the supported versions, see [Technical requirements for Archiving in Lync Server 2013](lync-server-2013-technical-requirements-for-archiving.md) in the Planning documentation.</span></span>

<span data-ttu-id="42350-125">Você deve configurar as plataformas do SQL Server antes de implantar e habilitar o arquivamento.</span><span class="sxs-lookup"><span data-stu-id="42350-125">You must set up the SQL Server platforms prior to deploying and enabling Archiving.</span></span> <span data-ttu-id="42350-126">Se a conta utilizada para publicar a topologia tiver os direitos e permissões apropriados, é possível criar o banco de dados de arquivamento (LcsLog) ao publicar a topologia.</span><span class="sxs-lookup"><span data-stu-id="42350-126">If the account to be used to publish the topology has the appropriate administrator rights and permissions, you can create the Archiving database (LcsLog) when you publish your topology.</span></span> <span data-ttu-id="42350-127">Você também pode criar o banco de dados posteriormente, incluindo como parte do procedimento de instalação.</span><span class="sxs-lookup"><span data-stu-id="42350-127">You can also create the database later, including as part of the installation procedure.</span></span> <span data-ttu-id="42350-128">Para obter detalhes sobre o SQL Server, consulte o TechCenter do SQL Server em [https://go.microsoft.com/fwlink/p/?linkID=129045](https://go.microsoft.com/fwlink/p/?linkid=129045) .</span><span class="sxs-lookup"><span data-stu-id="42350-128">For details about SQL Server, see the SQL Server TechCenter at [https://go.microsoft.com/fwlink/p/?linkID=129045](https://go.microsoft.com/fwlink/p/?linkid=129045).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="42350-129">Verifique se o tipo de inicialização do serviço do SQL Server Agent é automático e se o serviço do SQL Server Agent está em execução para a instância do SQL que está segurando o banco de dados de arquivamento, para que o trabalho de manutenção do arquivamento do SQL Server possa ser executado na base agendada sob o controle do serviço do SQL Server Agent.</span><span class="sxs-lookup"><span data-stu-id="42350-129">Ensure that the SQL Server Agent Service Startup Type is Automatic and the SQL Server Agent Service is running for the SQL Instance which is holding the Archiving database, so that the Default Archiving SQL Server Maintenance Job can run on its scheduled basis under the control of the SQL Server Agent Service.</span></span>



</div>

</div>

</div>

<div>

## <a name="setting-up-file-storage"></a><span data-ttu-id="42350-130">Configurar o armazenamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="42350-130">Setting Up File Storage</span></span>

<span data-ttu-id="42350-131">O arquivamento usa o compartilhamento de arquivos do Lync Server 2013 especificado quando você configura seu pool de front-end ou o servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="42350-131">Archiving uses the Lync Server 2013 file share that you specified when you set up your Front End pool or Standard Edition server.</span></span> <span data-ttu-id="42350-132">Não é possível alterar o compartilhamento de arquivos usado para arquivamento.</span><span class="sxs-lookup"><span data-stu-id="42350-132">You cannot change the file share used for Archiving.</span></span> <span data-ttu-id="42350-133">Para obter detalhes sobre sistemas de armazenamento de arquivos com suporte, consulte [suporte de armazenamento de arquivos no Lync Server 2013](lync-server-2013-file-storage-support.md) na documentação de suporte.</span><span class="sxs-lookup"><span data-stu-id="42350-133">For details about supported file storage systems, see [File storage support in Lync Server 2013](lync-server-2013-file-storage-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="42350-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42350-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

