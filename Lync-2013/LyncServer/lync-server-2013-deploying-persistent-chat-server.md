---
title: 'Lync Server 2013: Implantando Servidor de Chat Persistente'
description: 'Lync Server 2013: Implantando o servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Persistent Chat Server
ms:assetid: e3b930fb-6855-47f0-b6b3-7dfae386540d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205357(v=OCS.15)
ms:contentKeyID: 48185717
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b85c0070ab4bcd60d80d57738c25daac1de4faf1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429808"
---
# <a name="deploying-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="005e8-103">Implantando Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="005e8-103">Deploying Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="005e8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="005e8-104">

<span> </span></span></span>

<span data-ttu-id="005e8-105">_**Tópico da última modificação:** 2014-03-31_</span><span class="sxs-lookup"><span data-stu-id="005e8-105">_**Topic Last Modified:** 2014-03-31_</span></span>

<span data-ttu-id="005e8-106">Lync Server 2013, servidor de chat persistente faz parte da infraestrutura do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="005e8-106">Lync Server 2013, Persistent Chat Server is part of the Lync Server 2013 infrastructure.</span></span>

<span data-ttu-id="005e8-107">A implantação do servidor de chat persistente exige que você:</span><span class="sxs-lookup"><span data-stu-id="005e8-107">Deploying Persistent Chat Server requires that you:</span></span>

  - <span data-ttu-id="005e8-108">Use o construtor de topologias para definir ou importar e publicar subseqüentemente a topologia e os componentes que você deseja implantar.</span><span class="sxs-lookup"><span data-stu-id="005e8-108">Use Topology Builder to define, or import, and subsequently publish your topology and the components that you want to deploy.</span></span>

  - <span data-ttu-id="005e8-109">Preparar seu ambiente para a implantação de componentes persistentes do servidor de chat.</span><span class="sxs-lookup"><span data-stu-id="005e8-109">Prepare your environment for deploying Persistent Chat Server components.</span></span>

  - <span data-ttu-id="005e8-110">Instalar e configurar componentes do servidor de chat persistente para a sua implantação.</span><span class="sxs-lookup"><span data-stu-id="005e8-110">Install and configure Persistent Chat Server components for your deployment.</span></span>

<span data-ttu-id="005e8-111">O servidor de chat persistente está disponível no Lync Server 2013 Enterprise Edition como um pool separado (não vem com os servidores front-end da Enterprise Edition).</span><span class="sxs-lookup"><span data-stu-id="005e8-111">Persistent Chat Server is available with Lync Server 2013 Enterprise Edition as a separate pool (not collocated with the Enterprise Edition Front End Servers).</span></span> <span data-ttu-id="005e8-112">O servidor de chat persistente exige um servidor back-end do SQL Server no pool da edição Enterprise para armazenar o conteúdo da sala de chat e outros metadados relevantes.</span><span class="sxs-lookup"><span data-stu-id="005e8-112">Persistent Chat Server requires a SQL Server Back End Server in your Enterprise Edition pool to store the chat room content and other relevant metadata.</span></span> <span data-ttu-id="005e8-113">Recomendamos que você instale o **PersistentChatStore** em um servidor back-end do SQL Server dedicado, embora a colocação do servidor back-end do Lync Server 2013 e do **PersistentChatStore** na mesma instância do SQL Server seja compatível.</span><span class="sxs-lookup"><span data-stu-id="005e8-113">We recommend that you install the **PersistentChatStore** on a dedicated SQL Server Back End Server, although collocating Lync Server 2013 Back End Server and **PersistentChatStore** on the same SQL Server instance is supported.</span></span>

<span data-ttu-id="005e8-114">O servidor de chat persistente também pode ser implantado com o Lync Server 2013 Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="005e8-114">Persistent Chat Server can also be deployed with Lync Server 2013 Standard Edition.</span></span> <span data-ttu-id="005e8-115">Nesse caso, o servidor front-end **PersistentChatService** é posicionado no computador com a Standard Edition, e o servidor back-end do **PersistentChatStore** pode ser implantado na instância local do SQL Server Express.</span><span class="sxs-lookup"><span data-stu-id="005e8-115">In this case, the **PersistentChatService** Front End Server is collocated on the Standard Edition computer, and the **PersistentChatStore** Back End Server can be deployed on the local SQL Server Express instance.</span></span>

<span data-ttu-id="005e8-116">Para obter detalhes sobre as configurações de colocalização com suporte, consulte [colocação de servidor com suporte no Lync server 2013](lync-server-2013-supported-server-collocation.md).</span><span class="sxs-lookup"><span data-stu-id="005e8-116">For details about supported colocation configurations, see [Supported server collocation in Lync Server 2013](lync-server-2013-supported-server-collocation.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="005e8-117">Não oferecemos suporte à alta disponibilidade para o servidor de chat persistente &nbsp; Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="005e8-117">We do not support high availability for Persistent Chat Server&nbsp;Standard Edition.</span></span> <span data-ttu-id="005e8-118">O desempenho e a escala serão limitados.</span><span class="sxs-lookup"><span data-stu-id="005e8-118">Performance and scale will be limited.</span></span> <span data-ttu-id="005e8-119">Além disso, oferecemos suporte somente para o novo servidor persistente do servidor de chat persistente &nbsp; .</span><span class="sxs-lookup"><span data-stu-id="005e8-119">Furthermore, we support only new Persistent Chat Server&nbsp;Standard Edition server.</span></span> <span data-ttu-id="005e8-120">Não oferecemos suporte à atualização do Lync Server 2010, do servidor de chat em grupo para um servidor de chat persistente do Lync Server 2013 &nbsp; &nbsp; Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="005e8-120">We do not support upgrading Lync Server 2010, Group Chat Server to a Lync Server 2013&nbsp;Persistent Chat Server&nbsp;Standard Edition.</span></span>



</div>

<span data-ttu-id="005e8-121">Se a sua organização requer suporte à conformidade, você pode instalar o serviço de conformidade do servidor de chat persistente no servidor front-end do servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="005e8-121">If your organization requires compliance support, you can install the Persistent Chat Server Compliance service on the Persistent Chat Server Front End Server.</span></span> <span data-ttu-id="005e8-122">Um banco de dados separado é necessário para conformidade.</span><span class="sxs-lookup"><span data-stu-id="005e8-122">A separate database is required for compliance.</span></span>

<span data-ttu-id="005e8-123">No mínimo, cada topologia requer um servidor com o Lync Server 2013 instalado e um servidor com software de banco de dados do SQL Server instalado.</span><span class="sxs-lookup"><span data-stu-id="005e8-123">At a minimum, each topology requires a server with Lync Server 2013 installed and a server with SQL Server database software installed.</span></span>

<span data-ttu-id="005e8-124">Use o construtor de topologias para adicionar um servidor de chat persistente a suas implantações do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="005e8-124">Use Topology Builder to add Persistent Chat Server to your Lync Server 2013 deployments.</span></span> <span data-ttu-id="005e8-125">Você pode optar por adicionar um ou mais pools de servidores de chat persistentes usando o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="005e8-125">You can choose to add one or more Persistent Chat Server pools using Topology Builder.</span></span> <span data-ttu-id="005e8-126">Siga as mesmas instruções de implantação para implantar vários pools persistentes do servidor de chat como faria com qualquer pool.</span><span class="sxs-lookup"><span data-stu-id="005e8-126">Follow the same deployment instructions for deploying multiple Persistent Chat Server pools as you would for any pool.</span></span> <span data-ttu-id="005e8-127">Para obter detalhes, consulte [implantando o Lync Server 2013](lync-server-2013-deploying-lync-server.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="005e8-127">For details, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="005e8-128">Para obter detalhes sobre topologias disponíveis e os requisitos técnicos e de software para a instalação do servidor de chat persistente, consulte [planejando o servidor de chat persistente no Lync server 2013](lync-server-2013-planning-for-persistent-chat-server.md) na documentação de planejamento, [como o servidor de chat persistente funciona no Lync Server 2013](lync-server-2013-how-persistent-chat-server-works.md) na documentação de planejamento, documentação de implantação ou documentação de operações e hardware compatível com o [Lync Server 2013](lync-server-2013-supported-hardware.md) na documentação de suporte.</span><span class="sxs-lookup"><span data-stu-id="005e8-128">For details about available topologies and the technical and software requirements for installing Persistent Chat Server, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation, [How Persistent Chat Server works in Lync Server 2013](lync-server-2013-how-persistent-chat-server-works.md) in the Planning documentation, Deployment documentation, or Operations documentation, and [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) in the Supportability documentation.</span></span>

<span data-ttu-id="005e8-129">Para obter detalhes sobre como adquirir certificados, criar o banco de dados do SQL Server e criar armazenamentos de arquivos, consulte [implantando o Lync Server 2013](lync-server-2013-deploying-lync-server.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="005e8-129">For details about acquiring certificates, creating the SQL Server database, and creating file stores, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="005e8-130">Um servidor front-end único de servidor de chat persistente pode oferecer suporte a usuários ativos do 20.000.</span><span class="sxs-lookup"><span data-stu-id="005e8-130">A single Persistent Chat Server Front End Server can support 20,000 active users.</span></span> <span data-ttu-id="005e8-131">Você pode ter um pool de servidores de chat persistente com até quatro servidores front-end ativos que dão suporte a um total de 80.000 usuários simultâneos.</span><span class="sxs-lookup"><span data-stu-id="005e8-131">You can have a Persistent Chat Server pool with up to 4 active Front End Servers supporting a total of 80,000 concurrent users.</span></span>

<span data-ttu-id="005e8-132">Também há suporte para o servidor de chat persistente em um servidor virtual.</span><span class="sxs-lookup"><span data-stu-id="005e8-132">Persistent Chat Server is also supported on a virtual server.</span></span> <span data-ttu-id="005e8-133">O servidor virtual pode oferecer suporte a até 20.000 usuários simultâneos se ele corresponder às especificações do servidor físico.</span><span class="sxs-lookup"><span data-stu-id="005e8-133">The virtual server can support up to 20,000 concurrent users if it matches the specifications of the physical server.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="005e8-134">O servidor de chat persistente deve ser instalado em um sistema de arquivos NTFS para ajudar a reforçar a segurança do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="005e8-134">Persistent Chat Server must be installed on an NTFS file system to help enforce file system security.</span></span> <span data-ttu-id="005e8-135">FAT32 não é um sistema de arquivos com suporte para o servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="005e8-135">FAT32 is not a supported file system for Persistent Chat Server.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="005e8-136">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="005e8-136">In This Section</span></span>

  - [<span data-ttu-id="005e8-137">Como o servidor de chat persistente funciona no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="005e8-137">How Persistent Chat Server works in Lync Server 2013</span></span>](lync-server-2013-how-persistent-chat-server-works.md)

  - [<span data-ttu-id="005e8-138">Lista de verificação de implantação para o Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="005e8-138">Deployment checklist for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-persistent-chat-server.md)

  - [<span data-ttu-id="005e8-139">Requisitos técnicos para servidor de chat persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="005e8-139">Technical requirements for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="005e8-140">Configurar sistemas e infraestrutura para o Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="005e8-140">Setting up systems and infrastructure for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-setting-up-systems-and-infrastructure-for-persistent-chat-server.md)

  - [<span data-ttu-id="005e8-141">Adicionando Servidor de Chat Persistente em sua implantação no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="005e8-141">Adding Persistent Chat Server to your deployment in Lync Server 2013</span></span>](lync-server-2013-adding-persistent-chat-server-to-your-deployment.md)

  - [<span data-ttu-id="005e8-142">Instalando o Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="005e8-142">Installing Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-installing-persistent-chat-server.md)

  - [<span data-ttu-id="005e8-143">Adicionando um administrador de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="005e8-143">Adding a Persistent Chat administrator in Lync Server 2013</span></span>](lync-server-2013-adding-a-persistent-chat-administrator.md)

  - [<span data-ttu-id="005e8-144">Configurando o Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="005e8-144">Configuring Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-configuring-persistent-chat-server.md)

  - [<span data-ttu-id="005e8-145">Configurando Servidor de Chat Persistente usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="005e8-145">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</span></span>](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md)

  - [<span data-ttu-id="005e8-146">Configuração de solução de problemas do Servidor de Chat Persistente usando cmdlets do Windows PowerShell no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="005e8-146">Troubleshooting Persistent Chat Server configuration using Windows PowerShell cmdlets in Lync Server 2013</span></span>](lync-server-2013-troubleshooting-persistent-chat-server-configuration-using-windows-powershell-cmdlets.md)

  - [<span data-ttu-id="005e8-147">Configurando o Servidor de Chat Persistente para alta disponibilidade e recuperação de desastre no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="005e8-147">Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md)

  - [<span data-ttu-id="005e8-148">Failouver e failback do Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="005e8-148">Failing over and failing back Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-failing-over-and-failing-back-persistent-chat-server.md)

<span data-ttu-id="005e8-149"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="005e8-149"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

