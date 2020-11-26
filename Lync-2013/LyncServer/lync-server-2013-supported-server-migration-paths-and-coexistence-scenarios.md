---
title: 'Lync Server 2013: Caminhos de migração de servidor suportado e cenários de coexistência'
description: 'Lync Server 2013: caminhos de migração de servidor com suporte e cenários de coexistência.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported server migration paths and coexistence scenarios
ms:assetid: 2a6a730f-7f80-45f9-9540-3edfdaa265fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425764(v=OCS.15)
ms:contentKeyID: 48183686
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44d0a40ac6cc6570cf79b56dc896277c83909b5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423628"
---
# <a name="supported-server-migration-paths-and-coexistence-scenarios-in-lync-server-2013"></a><span data-ttu-id="00204-103">Caminhos de migração de servidor suportado e cenários de coexistência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="00204-103">Supported server migration paths and coexistence scenarios in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="00204-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="00204-104">

<span> </span></span></span>

<span data-ttu-id="00204-105">_**Tópico da última modificação:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="00204-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="00204-106">O Lync Server 2013 oferece suporte à migração de qualquer um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="00204-106">Lync Server 2013 supports migration from either of the following:</span></span>

  - <span data-ttu-id="00204-107">Microsoft Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="00204-107">Microsoft Lync Server 2010</span></span>

  - <span data-ttu-id="00204-108">Microsoft Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="00204-108">Microsoft Office Communications Server 2007 R2</span></span>

<span data-ttu-id="00204-109">Não há suporte para a migração de um ambiente que executa ambas as versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="00204-109">Migration from an environment running both of these previous versions is not supported.</span></span> <span data-ttu-id="00204-110">Não há suporte para a migração de versões anteriores, como o Microsoft Office Communications Server 2007 ou o Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="00204-110">Migration from earlier versions, such as Microsoft Office Communications Server 2007 or Live Communications Server 2005, is not supported.</span></span> <span data-ttu-id="00204-111">Se sua implantação anterior incluiu o chat em grupo, você deve migrá-la separadamente.</span><span class="sxs-lookup"><span data-stu-id="00204-111">If your previous deployment included Group Chat, you must migrate it separately.</span></span>

<div>

## <a name="migration-methods"></a><span data-ttu-id="00204-112">Métodos de migração</span><span class="sxs-lookup"><span data-stu-id="00204-112">Migration Methods</span></span>

<span data-ttu-id="00204-113">Há suporte para a migração de todas as topologias do Lync Server e funções de servidor.</span><span class="sxs-lookup"><span data-stu-id="00204-113">Migration of all Lync Server topologies and server roles is supported.</span></span> <span data-ttu-id="00204-114">Você pode migrar de uma topologia para uma topologia diferente, incluindo do servidor Standard Edition para o servidor Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="00204-114">You can migrate from one topology to a different topology, including from Standard Edition server to Enterprise Edition server.</span></span>

<span data-ttu-id="00204-115">O Lync Server 2013 só oferece suporte ao seguinte método de migração:</span><span class="sxs-lookup"><span data-stu-id="00204-115">Lync Server 2013 supports only the following migration method:</span></span>

  - <span></span>  
    <span data-ttu-id="00204-116">**Migração lado a lado.**</span><span class="sxs-lookup"><span data-stu-id="00204-116">**Side-by-side migration.**</span></span> <span data-ttu-id="00204-117">Na migração lado a lado, o Lync Server 2013 é implantado juntamente com uma implantação existente do Microsoft Lync Server 2010 ou do Office Communications Server 2007 R2 e, em seguida, transfere operações para os novos servidores e move usuários para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="00204-117">In side-by-side migration, Lync Server 2013 is deployed alongside an existing Microsoft Lync Server 2010 or Office Communications Server 2007 R2 deployment, and then you transfer operations to the new servers and move users to Lync Server 2013.</span></span> <span data-ttu-id="00204-118">Esse método requer plataformas de servidor adicionais, incluindo hardware e software, durante a migração, e nomes de sistema e nomes de pool são diferentes na nova configuração.</span><span class="sxs-lookup"><span data-stu-id="00204-118">This method requires additional server platforms, including hardware and software, during migration, and system names and pool names are different in the new configuration.</span></span> <span data-ttu-id="00204-119">Se for necessário reverter para a versão anterior, você poderá mudar as operações de volta para os servidores anteriores.</span><span class="sxs-lookup"><span data-stu-id="00204-119">If it becomes necessary to roll back to the previous version, you can shift operations back to the previous servers.</span></span>

<span data-ttu-id="00204-120">Não há suporte para a migração entre florestas dos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="00204-120">Migration across Active Directory Domain Services forests is not supported.</span></span>

<span data-ttu-id="00204-121">O caminho de migração recomendado é uma abordagem em fases.</span><span class="sxs-lookup"><span data-stu-id="00204-121">The recommended migration path is a phased approach.</span></span> <span data-ttu-id="00204-122">Para obter detalhes sobre a migração de uma versão anterior, incluindo o atributo Phase apropriado de implantação de componentes, consulte os seguintes tópicos na documentação de migração:</span><span class="sxs-lookup"><span data-stu-id="00204-122">For details about migrating from a previous release, including the appropriate phasing of component deployment, see the following topics in the Migration documentation:</span></span>

  - [<span data-ttu-id="00204-123">Migração do Lync Server 2010 para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="00204-123">Migration from Lync Server 2010 to Lync Server 2013</span></span>](migration-from-lync-server-2010-to-lync-server-2013.md)

  - [<span data-ttu-id="00204-124">Migração do Office Communications Server 2007 R2 para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="00204-124">Migration from Office Communications Server 2007 R2 to Lync Server 2013</span></span>](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md)

  - [<span data-ttu-id="00204-125">Migração do Lync Server 2010, Chat em Grupo ou Office Communications Server 2007 R2 Group Chat para Lync Server 2013, Servidor de Chat Persistente</span><span class="sxs-lookup"><span data-stu-id="00204-125">Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server</span></span>](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md)

</div>

<span id="BKMK_PhasedMigration"></span>

<div>

## <a name="coexistence-scenarios"></a><span data-ttu-id="00204-126">Cenários de coexistência</span><span class="sxs-lookup"><span data-stu-id="00204-126">Coexistence Scenarios</span></span>

<span data-ttu-id="00204-127">O Lync Server 2013 pode coexistir com componentes de uma implantação do Lync Server 2010 ou uma implantação do Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="00204-127">Lync Server 2013 can coexist with components of either a Lync Server 2010 deployment or an Office Communications Server 2007 R2 deployment.</span></span> <span data-ttu-id="00204-128">A implantação simultânea do Lync Server 2013 com o Lync Server 2010 e o Office Communications Server 2007 R2 (implantação simultânea de todas as três versões) não é suportada.</span><span class="sxs-lookup"><span data-stu-id="00204-128">Concurrent deployment of Lync Server 2013 with both Lync Server 2010 and Office Communications Server 2007 R2 (concurrent deployment of all three versions) is not supported.</span></span>

<span data-ttu-id="00204-129">Durante uma migração em fases na qual uma implantação do Lync Server 2010 ou do Office Communications Server 2007 R2 anterior coexiste temporariamente com a nova implantação do Lync Server 2013, o suporte para o roteamento de versão mista é limitado.</span><span class="sxs-lookup"><span data-stu-id="00204-129">During a phased migration in which a previous Lync Server 2010 or Office Communications Server 2007 R2 deployment coexists temporarily with the new Lync Server 2013 deployment, support for mixed version routing is limited.</span></span> <span data-ttu-id="00204-130">Para obter detalhes, consulte a documentação de migração.</span><span class="sxs-lookup"><span data-stu-id="00204-130">For details, see the Migration documentation.</span></span>

<span data-ttu-id="00204-131">Você deve usar computadores separados e distintos que executam o Microsoft SQL Server 2008 R2 ou o Microsoft SQL Server 2012 para suas instâncias de banco de dados do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="00204-131">You must use separate and distinct computers running Microsoft SQL Server 2008 R2 or Microsoft SQL Server 2012 for your Lync Server 2013 database instances.</span></span> <span data-ttu-id="00204-132">Não é possível usar a mesma instância do SQL Server para um pool de front-end do Lync Server 2013 que você usa para um pool de front-end do Lync Server 2010 ou do Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="00204-132">You cannot use the same instance of SQL Server for a Lync Server 2013 Front End pool that you use for a Lync Server 2010 or Office Communications Server 2007 R2 Front End pool.</span></span> <span data-ttu-id="00204-133">Se você definir e configurar o Lync Server 2013 no construtor de topologias para uma implantação que já tenha o Lync Server 2010 ou o Office Communications Server 2007 R2 implantado, o construtor de topologias não permitirá que você defina uma instância de um Lync Server 2013 que já está em uso na topologia.</span><span class="sxs-lookup"><span data-stu-id="00204-133">If you define and configure Lync Server 2013 in Topology Builder for a deployment that already has Lync Server 2010 or Office Communications Server 2007 R2 deployed, Topology Builder will not allow you to define an instance of a Lync Server 2013 that is already in use in the topology.</span></span>

<span data-ttu-id="00204-134">O construtor de topologias exibirá a seguinte mensagem para informá-lo sobre esse problema: "o \[ FQDN do SQL Server do servidor \] já contém um repositório de usuários da função de hospedagem da instância do SQL".</span><span class="sxs-lookup"><span data-stu-id="00204-134">Topology Builder will display the following message to inform you of this issue: "The SQL server \[FQDN of the server\] already contains a SQL instance hosting role 'User Store."</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="00204-135">Se você pretende implantar funções de servidor que são novas na implantação do Lync Server 2013, primeiro atualize a implantação existente, conforme descrito na documentação de migração e a documentação de implantação e, em seguida, implante as novas funções de servidor, conforme descrito na documentação de planejamento e documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="00204-135">If you intend to deploy server roles that are new to your Lync Server 2013 deployment, you should first upgrade your existing deployment as described in the Migration documentation and the Deployment documentation, and then deploy the new server roles as described in the Planning documentation and Deployment documentation.</span></span> <span data-ttu-id="00204-136">Se você estiver migrando uma versão anterior do chat em grupo, migre-a por último, depois de concluir o processo de migração de todos os outros componentes do Lync Server 2010 ou do Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="00204-136">If you are migrating a previous version of Group Chat, migrate it last, after completing the process for migrating all other components from Lync Server 2010 or Office Communications Server 2007 R2.</span></span>



</div>

<span data-ttu-id="00204-137">Para obter requisitos de coexistência específicos e outros detalhes sobre a coexistência e a migração dos componentes do Lync Server 2010 ou do Office Communications Server 2007 R2 e do Lync Server 2013, consulte [migração do Lync server 2010 para o Lync server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) e [migração do Office communications Server 2007 R2 para o Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md) na documentação de migração.</span><span class="sxs-lookup"><span data-stu-id="00204-137">For specific coexistence requirements and other details about coexistence and migration of Lync Server 2010 or Office Communications Server 2007 R2 and Lync Server 2013 components, see [Migration from Lync Server 2010 to Lync Server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) and [Migration from Office Communications Server 2007 R2 to Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md) in the Migration documentation.</span></span> <span data-ttu-id="00204-138">Para obter detalhes sobre o suporte a versões mistas para clientes, consulte [clientes compatíveis de implantações anteriores no Lync Server 2013](lync-server-2013-supported-clients-from-previous-deployments.md).</span><span class="sxs-lookup"><span data-stu-id="00204-138">For details about mixed version support for clients, see [Supported clients from previous deployments in Lync Server 2013](lync-server-2013-supported-clients-from-previous-deployments.md).</span></span>

<span data-ttu-id="00204-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="00204-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

