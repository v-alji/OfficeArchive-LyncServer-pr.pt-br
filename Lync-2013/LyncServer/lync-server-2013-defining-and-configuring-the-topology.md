---
title: 'Lync Server 2013: Definindo e configurando a topologia'
description: 'Lync Server 2013: definindo e configurando a topologia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining and configuring the topology
ms:assetid: 51d1601e-4f83-48d4-ad08-3b4d5e2003aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398339(v=OCS.15)
ms:contentKeyID: 48184146
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec444a1ddf434c5a80fdc2d56bdba27573da14ab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430998"
---
# <a name="defining-and-configuring-the-topology-in-lync-server-2013"></a><span data-ttu-id="2b24e-103">Definindo e configurando a topologia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b24e-103">Defining and configuring the topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b24e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b24e-104">

<span> </span></span></span>

<span data-ttu-id="2b24e-105">_**Tópico da última modificação:** 2012-09-14_</span><span class="sxs-lookup"><span data-stu-id="2b24e-105">_**Topic Last Modified:** 2012-09-14_</span></span>

<span data-ttu-id="2b24e-106">Você define e configura sua topologia usando o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="2b24e-106">You define and configure your topology by using Topology Builder.</span></span> <span data-ttu-id="2b24e-107">O construtor de topologias não requer que você seja membro do grupo Administradores local ou de um grupo de domínio privilegiado (como administradores de domínio).</span><span class="sxs-lookup"><span data-stu-id="2b24e-107">Topology Builder does not require you to be a member of the local Administrators group or a privileged domain group (such as Domain Admins).</span></span> <span data-ttu-id="2b24e-108">Você pode definir sua topologia como um usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="2b24e-108">You can define your topology as a standard user.</span></span> <span data-ttu-id="2b24e-109">Ao iniciar o construtor de topologia na primeira utilização e em sessões de edição subsequentes, você será solicitado a fornecer o local onde deseja que o construtor de topologias carregue o documento de configuração atual.</span><span class="sxs-lookup"><span data-stu-id="2b24e-109">When you start Topology Builder on first use and subsequent edit sessions, you are prompted for the location where you want Topology Builder to load the current configuration document.</span></span> <span data-ttu-id="2b24e-110">As opções são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="2b24e-110">The choices are the following:</span></span>

  - <span data-ttu-id="2b24e-111">Baixar topologia da implantação existente</span><span class="sxs-lookup"><span data-stu-id="2b24e-111">Download topology from existing deployment</span></span>

  - <span data-ttu-id="2b24e-112">Abrir a topologia de um arquivo local</span><span class="sxs-lookup"><span data-stu-id="2b24e-112">Open topology from a local file</span></span>

  - <span data-ttu-id="2b24e-113">Nova topologia</span><span class="sxs-lookup"><span data-stu-id="2b24e-113">New topology</span></span>

<span data-ttu-id="2b24e-114">Se já definiu uma topologia e estabeleceu o repositório de gerenciamento central, você deve optar por baixar uma topologia de uma implantação existente.</span><span class="sxs-lookup"><span data-stu-id="2b24e-114">If you have already defined a topology and have established the Central Management store, you should choose to download a topology from an existing deployment.</span></span> <span data-ttu-id="2b24e-115">O construtor de topologias lerá o banco de dados e recuperará a definição atual.</span><span class="sxs-lookup"><span data-stu-id="2b24e-115">Topology Builder will read the database and retrieve the current definition.</span></span> <span data-ttu-id="2b24e-116">Se você tiver um repositório de gerenciamento central existente, você deve sempre escolher essa opção.</span><span class="sxs-lookup"><span data-stu-id="2b24e-116">If you have an existing Central Management store, you should always choose this option.</span></span>

<span data-ttu-id="2b24e-117">Se você não tiver estabelecido um repositório de gerenciamento central e quiser editar uma configuração salva anteriormente, deve optar por abrir a topologia a partir de um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="2b24e-117">If you have not established a Central Management store and want to edit a previously saved configuration, you should choose to open the topology from a local file.</span></span> <span data-ttu-id="2b24e-118">O arquivo que você abrir será o arquivo de configuração que foi salvo em uma sessão anterior.</span><span class="sxs-lookup"><span data-stu-id="2b24e-118">The file that you will open would be the configuration file that was saved in a previous session.</span></span> <span data-ttu-id="2b24e-119">Você pode usar essa opção para editar a topologia salva anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2b24e-119">You can use this option to edit the previously saved topology.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="2b24e-120">Se já tiver uma topologia publicada, você não deverá carregar um arquivo de configuração local.</span><span class="sxs-lookup"><span data-stu-id="2b24e-120">If you already have a published topology, you should not load a local configuration file.</span></span> <span data-ttu-id="2b24e-121">Você deve optar por baixar a topologia de uma implantação existente.</span><span class="sxs-lookup"><span data-stu-id="2b24e-121">You should choose to download the topology from an existing deployment.</span></span>



</div>

<span data-ttu-id="2b24e-122">Escolha se deseja criar uma nova topologia, se você quiser criar uma nova configuração do construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="2b24e-122">Choose to create a new topology, if you want to create a new Topology Builder configuration.</span></span> <span data-ttu-id="2b24e-123">Um design salvo anteriormente não será substituído, a menos que você opte por salvá-lo como o mesmo arquivo que você criou em uma sessão de design anterior.</span><span class="sxs-lookup"><span data-stu-id="2b24e-123">A previously saved design is not overwritten unless you choose to save it as the same file that you created in an earlier design session.</span></span>

<span data-ttu-id="2b24e-124">Em cada uma dessas opções, você será solicitado a fornecer um local para armazenar o arquivo de configuração do construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="2b24e-124">In each of these options, you will be prompted for a location to store the Topology Builder configuration file.</span></span> <span data-ttu-id="2b24e-125">O local para o arquivo pode ser um local local, um local compartilhado em um compartilhamento de arquivos estabelecido ou uma mídia removível.</span><span class="sxs-lookup"><span data-stu-id="2b24e-125">The location for the file could be a local location, a shared location on an established file share, or removable media.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2b24e-126">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="2b24e-126">In This Section</span></span>

  - [<span data-ttu-id="2b24e-127">Definir e configurar uma topologia no Construtor de Topologia para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b24e-127">Define and configure a topology in Topology Builder for Lync Server 2013</span></span>](lync-server-2013-define-and-configure-a-topology-in-topology-builder.md)

  - [<span data-ttu-id="2b24e-128">Definir e configurar um pool Front-End ou um servidor Standard Edition no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b24e-128">Define and configure a Front End pool or Standard Edition server in Lync Server 2013</span></span>](lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md)

  - [<span data-ttu-id="2b24e-129">Implantando pools Front-End emparelhados para recuperação de desastre no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b24e-129">Deploying paired Front End pools for disaster recovery in Lync Server 2013</span></span>](lync-server-2013-deploying-paired-front-end-pools-for-disaster-recovery.md)

  - [<span data-ttu-id="2b24e-130">Implantando espelhamento SQL para alta disponibilidade de Servidor Back-End no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b24e-130">Deploying SQL mirroring for Back End Server high availability in Lync Server 2013</span></span>](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md)

  - [<span data-ttu-id="2b24e-131">Editar ou configurar URLs simples no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b24e-131">Edit or configure simple URLs in Lync Server 2013</span></span>](lync-server-2013-edit-or-configure-simple-urls.md)

  - [<span data-ttu-id="2b24e-132">Selecionar o Servidor de Gerenciamento Central no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b24e-132">Select the Central Management Server in Lync Server 2013</span></span>](lync-server-2013-select-the-central-management-server.md)

<span data-ttu-id="2b24e-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b24e-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

