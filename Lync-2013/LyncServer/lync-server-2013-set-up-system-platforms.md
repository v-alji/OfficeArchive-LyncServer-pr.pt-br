---
title: 'Lync Server 2013: Configurar plataformas de sistema'
description: 'Lync Server 2013: configurar plataformas do sistema.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up system platforms
ms:assetid: 2e72e49d-2737-4b5b-8c0a-60f6ecb15bf1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204783(v=OCS.15)
ms:contentKeyID: 48183756
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd02c519d5632b7aa5732fbd9b880f7d1084b50f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423964"
---
# <a name="set-up-system-platforms-in-lync-server-2013"></a><span data-ttu-id="5a1fb-103">Configurar plataformas de sistema no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1fb-103">Set up system platforms in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5a1fb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5a1fb-104">

<span> </span></span></span>

<span data-ttu-id="5a1fb-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="5a1fb-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="5a1fb-106">Antes de iniciar a implantação do servidor de chat persistente, você deve instalar o sistema operacional necessário em hardware que atenda aos requisitos do sistema em servidores:</span><span class="sxs-lookup"><span data-stu-id="5a1fb-106">Before starting the deployment of Persistent Chat Server, you must install the required operating system on hardware that meets system requirements on servers:</span></span>

<span data-ttu-id="5a1fb-107">Para obter detalhes sobre o hardware com suporte para servidores que executam o Lync Server 2013, servidores de banco de dados e servidores de arquivos, consulte [hardware com suporte para o Lync server 2013](lync-server-2013-supported-hardware.md) na documentação de suporte.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-107">For details about supported hardware for servers running Lync Server 2013, database servers, and file servers, see [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) in the Supportability documentation.</span></span> <span data-ttu-id="5a1fb-108">Para obter detalhes sobre os sistemas operacionais e o software de banco de dados com suporte, consulte [suporte a infraestrutura e software do servidor no Lync Server 2013](lync-server-2013-server-software-and-infrastructure-support.md) na documentação de suporte.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-108">For details about supported operating systems and database software, see [Server software and infrastructure support in Lync Server 2013](lync-server-2013-server-software-and-infrastructure-support.md) in the Supportability documentation.</span></span> <span data-ttu-id="5a1fb-109">Para obter detalhes sobre os requisitos do Windows Update, consulte [suporte e requisitos adicionais do servidor no Lync server 2013](lync-server-2013-additional-server-support-and-requirements.md) na documentação de suporte.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-109">For details about Windows update requirements, see [Additional server support and requirements in Lync Server 2013](lync-server-2013-additional-server-support-and-requirements.md) in the Supportability documentation.</span></span>

<span data-ttu-id="5a1fb-110">O servidor de front-end do servidor de chat persistente, **PersistentChatService**, pode ser implantado em um ou mais computadores autônomos em um pool do Lync Server 2013 Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-110">The Persistent Chat Server Front End Server, **PersistentChatService**, can be deployed on one or more stand-alone computers in a Lync Server 2013 Enterprise Edition pool.</span></span> <span data-ttu-id="5a1fb-111">Eles não podem ser posicionados nos servidores front-end do Lync Server Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-111">They cannot be collocated on the Lync Server Enterprise Edition Front End Servers.</span></span> <span data-ttu-id="5a1fb-112">O servidor de chat persistente pode ser implantado pelo bootstrapper, exatamente como outras funções do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-112">Persistent Chat Server can be deployed by the Bootstrapper, just like other Lync Server roles.</span></span> <span data-ttu-id="5a1fb-113">Os **Serviços Web de chat persistente para o download/download de arquivo** e os **Serviços Web de chat persistente para o gerenciamento de salas de chat** são componentes da Web implantados nos servidores de Front-End do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-113">The **Persistent Chat Web Services for File Upload/Download**, and **Persistent Chat Web Services for Chat Room Management** are web components deployed on the Lync Server 2013 Front End Servers.</span></span>

<span data-ttu-id="5a1fb-114">Um servidor front-end único de servidor de chat persistente pode oferecer suporte a usuários ativos do 20.000.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-114">A single Persistent Chat Server Front End Server can support 20,000 active users.</span></span> <span data-ttu-id="5a1fb-115">Você pode ter um pool de servidores de chat persistente com até 4 front-ends ativos oferecendo suporte a um total de 80.000 usuários simultâneos.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-115">You can have a Persistent Chat Server pool with up to 4 active front ends supporting a total of 80,000 concurrent users.</span></span> <span data-ttu-id="5a1fb-116">O servidor back-end de chat persistente, **PersistentChatStore**, armazena as salas de chat e as categorias.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-116">The Persistent Chat Back End Server, **PersistentChatStore**, stores the chat rooms and categories.</span></span> <span data-ttu-id="5a1fb-117">Recomendamos que você instale o **PersistentChatStore** em um servidor back-end do SQL Server dedicado no pool da Enterprise Edition; Embora possamos dar suporte à colocação do servidor back-end do Lync Server 2013 e **PersistentChatStore** na mesma instância do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-117">We recommend that you install the **PersistentChatStore** on a dedicated SQL Server Back End Server in your Enterprise Edition pool; although we support collocating Lync Server 2013 Back End Server and **PersistentChatStore** on the same SQL Server instance.</span></span>

<span data-ttu-id="5a1fb-118">Se a sua organização requer suporte à conformidade, você pode instalá-la usando o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-118">If your organization requires compliance support, you can install it by using Topology Builder.</span></span> <span data-ttu-id="5a1fb-119">O serviço de conformidade do servidor de chat persistente está instalado no mesmo computador que o servidor front-end persistente do servidor de chat.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-119">The Persistent Chat Server Compliance service is installed on the same computer as the Persistent Chat Server Front End Server.</span></span> <span data-ttu-id="5a1fb-120">Um banco de dados separado é necessário para conformidade.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-120">A separate database is required for compliance.</span></span> <span data-ttu-id="5a1fb-121">Para obter detalhes sobre os requisitos de conformidade do servidor de chat persistente, consulte [planejando o servidor de chat persistente no Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-121">For details about compliance requirements for Persistent Chat Server, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

<span data-ttu-id="5a1fb-122">No mínimo, cada topologia requer um servidor com o Lync Server 2013 instalado e um servidor com software de banco de dados do SQL Server instalado.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-122">At a minimum, each topology requires a server with Lync Server 2013 installed and a server with SQL Server database software installed.</span></span> <span data-ttu-id="5a1fb-123">O construtor de topologias suporta vários pools de servidores de chat persistentes.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-123">Topology Builder supports multiple Persistent Chat Server pools.</span></span> <span data-ttu-id="5a1fb-124">Siga as mesmas instruções de implantação para implantar vários pools de servidores de chat persistentes como faria para qualquer pool de [implantação do Lync server 2013](lync-server-2013-deploying-lync-server.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-124">Follow the same deployment instructions for deploying multiple Persistent Chat Server pools as you would for any pool from [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="5a1fb-125">Você também pode implantar o servidor de chat persistente com o Lync Server 2013 Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-125">You can also deploy Persistent Chat Server with Lync Server 2013 Standard Edition.</span></span> <span data-ttu-id="5a1fb-126">Nesse caso, o servidor front-end **PersistentChatService** é posicionado no servidor Standard Edition, e você pode implantar o servidor back-end do **PersistentChatStore** na instância local do SQL Server Express.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-126">In this case, the **PersistentChatService** Front End Server is collocated on the Standard Edition server, and you can deploy the **PersistentChatStore** Back End Server on the local SQL Server Express instance.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="5a1fb-127">Não oferecemos suporte à edição do servidor de chat &nbsp; padrão persistente para alta disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-127">We do not support Persistent Chat Server&nbsp;Standard Edition for high availability.</span></span> <span data-ttu-id="5a1fb-128">O desempenho e a escala serão limitados.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-128">Performance and scale will be limited.</span></span> <span data-ttu-id="5a1fb-129">Além disso, oferecemos apenas novas implantações persistentes de servidor de edição de servidor de chat persistente &nbsp; .</span><span class="sxs-lookup"><span data-stu-id="5a1fb-129">Furthermore, we support only new Persistent Chat Server&nbsp;Standard Edition server deployments.</span></span> <span data-ttu-id="5a1fb-130">Não oferecemos suporte a uma atualização do Lync Server 2010, do servidor de chat em grupo para um servidor de chat persistente do Lync Server 2013 &nbsp; &nbsp; Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="5a1fb-130">We do not support an upgrade of Lync Server 2010, Group Chat Server to a Lync Server 2013&nbsp;Persistent Chat Server&nbsp;Standard Edition.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5a1fb-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a1fb-131">See Also</span></span>


[<span data-ttu-id="5a1fb-132">Suporte adicional e requisitos de servidor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1fb-132">Additional server support and requirements in Lync Server 2013</span></span>](lync-server-2013-additional-server-support-and-requirements.md)  


[<span data-ttu-id="5a1fb-133">Hardware suportado para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1fb-133">Supported hardware for Lync Server 2013</span></span>](lync-server-2013-supported-hardware.md)  
[<span data-ttu-id="5a1fb-134">Suporte a software e à infraestrutura de servidor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1fb-134">Server software and infrastructure support in Lync Server 2013</span></span>](lync-server-2013-server-software-and-infrastructure-support.md)  
[<span data-ttu-id="5a1fb-135">Planejando o Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1fb-135">Planning for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-planning-for-persistent-chat-server.md)  
[<span data-ttu-id="5a1fb-136">Implantando o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a1fb-136">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)  
  

<span data-ttu-id="5a1fb-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5a1fb-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

