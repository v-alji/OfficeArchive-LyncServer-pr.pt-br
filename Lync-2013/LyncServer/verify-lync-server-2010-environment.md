---
title: Verificar ambiente do Lync Server 2010
description: Verifique o ambiente do Lync Server 2010.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify Lync Server 2010 environment
ms:assetid: bfc7c620-556a-43cd-b1ed-2c268ec2b5cc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205231(v=OCS.15)
ms:contentKeyID: 48185301
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 570fd2a9efdc90899ff4f91146b7aeb1991f6764
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440202"
---
# <a name="verify-lync-server-2010-environment"></a><span data-ttu-id="06a19-103">Verificar ambiente do Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="06a19-103">Verify Lync Server 2010 environment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06a19-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06a19-104">

<span> </span></span></span>

<span data-ttu-id="06a19-105">_**Tópico da última modificação:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="06a19-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="06a19-106">Antes de implantar o Lync Server 2013 em um estado de coexistência com o Lync Server 2010, você precisa verificar se os serviços do Lync Server 2010 foram configurados e iniciados.</span><span class="sxs-lookup"><span data-stu-id="06a19-106">Before deploying Lync Server 2013 in a coexistence state with Lync Server 2010, you need to verify that Lync Server 2010 services have been configured and started.</span></span> <span data-ttu-id="06a19-107">É importante identificar os principais serviços e recursos que existem em seu ambiente herdado antes de implantar um pool piloto do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="06a19-107">It is important to identify key services and features that exist in your legacy environment, prior to deploying a Lync Server 2013 pilot pool.</span></span> <span data-ttu-id="06a19-108">Antes de implantar o Microsoft Lync Server 2013 XMPP em um estado de coexistência com uma implantação herdada do XMPP, você precisa verificar se os serviços herdados do XMPP foram configurados e iniciados e identifica qual parceiro federado a configuração de XMPP herdada tem suporte.</span><span class="sxs-lookup"><span data-stu-id="06a19-108">Before deploying Microsoft Lync Server 2013 XMPP in a coexistence state with a legacy XMPP deployment, you need to verify the legacy XMPP services have been configured and started, and identify which federated partner the legacy XMPP configuration is supporting.</span></span> <span data-ttu-id="06a19-109">A verificação da implantação do Lync Server 2010 herdada envolve o seguinte:</span><span class="sxs-lookup"><span data-stu-id="06a19-109">Verifying your legacy Lync Server 2010 deployment entails the following:</span></span>

  - <span data-ttu-id="06a19-110">Verificando se os serviços do Lync Server 2010 foram iniciados</span><span class="sxs-lookup"><span data-stu-id="06a19-110">Verifying the Lync Server 2010 services are started</span></span>

  - <span data-ttu-id="06a19-111">Revisão da topologia e dos usuários no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="06a19-111">Reviewing the topology and users in Lync Server 2010.</span></span>

  - <span data-ttu-id="06a19-112">Verificar as configurações do servidor de Federação e de borda.</span><span class="sxs-lookup"><span data-stu-id="06a19-112">Verifying the federation and Edge server settings.</span></span>

  - <span data-ttu-id="06a19-113">Verificar os serviços do XMPP e os parceiros federados.</span><span class="sxs-lookup"><span data-stu-id="06a19-113">Verifying XMPP services and federated partners.</span></span>

<span data-ttu-id="06a19-114">**Verificar se os serviços do Lync Server 2010 foram iniciados**</span><span class="sxs-lookup"><span data-stu-id="06a19-114">**Verify Lync Server 2010 Services are started**</span></span>

1.  <span data-ttu-id="06a19-115">No servidor de front-end do Lync Server 2010, navegue até o \\ applet Serviços de ferramentas administrativas.</span><span class="sxs-lookup"><span data-stu-id="06a19-115">From the Lync Server 2010 Front End Server, navigate to the Administrative Tools\\Services applet.</span></span>

2.  <span data-ttu-id="06a19-116">Verifique se os seguintes serviços estão em execução no servidor front-end:</span><span class="sxs-lookup"><span data-stu-id="06a19-116">Verify that the following services are running on the Front End Server:</span></span>
    
    <span data-ttu-id="06a19-117">![Lista de serviços em execução no front-end Server](images/JJ205231.639f2729-b759-4d8e-b4ad-59d7f68adcd2(OCS.15).jpg "Lista de serviços em execução no front-end Server")</span><span class="sxs-lookup"><span data-stu-id="06a19-117">![List of services running on Front End Server](images/JJ205231.639f2729-b759-4d8e-b4ad-59d7f68adcd2(OCS.15).jpg "List of services running on Front End Server")</span></span>

<span data-ttu-id="06a19-118">**Examine a topologia do Lync Server 2010 no painel de controle do Lync Server**</span><span class="sxs-lookup"><span data-stu-id="06a19-118">**Review the Lync Server 2010 topology in Lync Server Control Panel**</span></span>

1.  <span data-ttu-id="06a19-119">Faça logon no Servidor Front-end com uma conta que seja membro do grupo de RTCUniversalServerAdmins ou membro da função administrativa do CsAdministrator ou CsUserAdministrator.</span><span class="sxs-lookup"><span data-stu-id="06a19-119">Log on to the Front End Server with an account that is a member of the RTCUniversalServerAdmins group or a member of the CsAdministrator or CsUserAdministrator administrative role.</span></span>

2.  <span data-ttu-id="06a19-120">Abra o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="06a19-120">Open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="06a19-121">Selecione **topologia**.</span><span class="sxs-lookup"><span data-stu-id="06a19-121">Select **Topology**.</span></span> <span data-ttu-id="06a19-122">Verifique se os vários servidores na sua implantação do Lync Server 2010 estão listados.</span><span class="sxs-lookup"><span data-stu-id="06a19-122">Verify that the various servers in your Lync Server 2010 deployment are listed.</span></span>
    
    <span data-ttu-id="06a19-123">![Página de topologia do painel de controle do Lync Server 2010](images/JJ205231.338ce4fb-2162-4176-a249-ec4ae021fa6a(OCS.15).jpg "Página de topologia do painel de controle do Lync Server 2010")</span><span class="sxs-lookup"><span data-stu-id="06a19-123">![Lync Server 2010 Control Panel topology page](images/JJ205231.338ce4fb-2162-4176-a249-ec4ae021fa6a(OCS.15).jpg "Lync Server 2010 Control Panel topology page")</span></span>

<span data-ttu-id="06a19-124">**Para revisar os usuários do Lync Server 2010 no painel de controle do Lync Server**</span><span class="sxs-lookup"><span data-stu-id="06a19-124">**To review Lync Server 2010 users in Lync Server Control Panel**</span></span>

1.  <span data-ttu-id="06a19-125">Abra o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="06a19-125">Open the Lync Server Control Panel.</span></span>

2.  <span data-ttu-id="06a19-126">Selecione **usuários** e, em seguida, clique em **Localizar**.</span><span class="sxs-lookup"><span data-stu-id="06a19-126">Select **Users** and then click **Find**.</span></span>

3.  <span data-ttu-id="06a19-127">Verifique se a coluna **pool de registradores** aponta para o pool do Lync Server 2010 para cada usuário listado.</span><span class="sxs-lookup"><span data-stu-id="06a19-127">Verify that the **Registrar Pool** column points to the Lync Server 2010 pool for each user listed.</span></span>
    
    <span data-ttu-id="06a19-128">![Painel de controle do Lync Server 2010 listando usuários](images/JJ205231.a9378c40-7a52-4c78-ad83-1463847c9edb(OCS.15).jpg "Painel de controle do Lync Server 2010 listando usuários")</span><span class="sxs-lookup"><span data-stu-id="06a19-128">![Lync Server 2010 Control Panel listing users](images/JJ205231.a9378c40-7a52-4c78-ad83-1463847c9edb(OCS.15).jpg "Lync Server 2010 Control Panel listing users")</span></span>

<span data-ttu-id="06a19-129">**Para verificar as configurações de borda e Federação do Lync Server 2010**</span><span class="sxs-lookup"><span data-stu-id="06a19-129">**To verify Lync Server 2010 Edge and Federation Settings**</span></span>

1.  <span data-ttu-id="06a19-130">Iniciar o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="06a19-130">Start Topology Builder.</span></span>

2.  <span data-ttu-id="06a19-131">Selecione **baixar a topologia na implantação existente**.</span><span class="sxs-lookup"><span data-stu-id="06a19-131">Select **Download Topology from existing deployment**.</span></span>

3.  <span data-ttu-id="06a19-132">Escolha um nome de arquivo e salve a topologia com o tipo de arquivo default. tbxml.</span><span class="sxs-lookup"><span data-stu-id="06a19-132">Choose a file name and save the topology with the default .tbxml file type.</span></span>

4.  <span data-ttu-id="06a19-133">Expanda o nó do Lync Server 2010 para revelar as várias funções de servidor na implantação.</span><span class="sxs-lookup"><span data-stu-id="06a19-133">Expand the Lync Server 2010 node to reveal the various server roles in the deployment.</span></span>

5.  <span data-ttu-id="06a19-134">Selecione o nó do site e verifique se um valor de **atribuição de roteiro de Federação do site** está definido.</span><span class="sxs-lookup"><span data-stu-id="06a19-134">Select the site node and verify if a **Site federation route assignment** value is set.</span></span>
    
    <span data-ttu-id="06a19-135">![Construtor de topologias, roteiro de Federação do site](images/JJ205231.87de3735-af7e-4280-8d72-c42cb0ea1c05(OCS.15).jpg "Construtor de topologias, roteiro de Federação do site")</span><span class="sxs-lookup"><span data-stu-id="06a19-135">![Topology Builder, Site Federation Route](images/JJ205231.87de3735-af7e-4280-8d72-c42cb0ea1c05(OCS.15).jpg "Topology Builder, Site Federation Route")</span></span>

6.  <span data-ttu-id="06a19-136">Em seguida, selecione o servidor Standard Edition ou o pool Front-end da edição Enterprise.</span><span class="sxs-lookup"><span data-stu-id="06a19-136">Next, select the Standard Edition Server or Enterprise Edition front end pool.</span></span> <span data-ttu-id="06a19-137">Determine se um pool de bordas foi configurado para mídia abaixo de **associações**.</span><span class="sxs-lookup"><span data-stu-id="06a19-137">Determine if an Edge pool has been configured for Media below **Associations**.</span></span>
    
    <span data-ttu-id="06a19-138">![Construtor de topologias mostrando servidores e pools](images/JJ205231.5ad5ea3b-b122-44dd-8968-f1147d6d45f1(OCS.15).jpg "Construtor de topologias mostrando servidores e pools")</span><span class="sxs-lookup"><span data-stu-id="06a19-138">![Topology Builder showing servers and pools](images/JJ205231.5ad5ea3b-b122-44dd-8968-f1147d6d45f1(OCS.15).jpg "Topology Builder showing servers and pools")</span></span>

7.  <span data-ttu-id="06a19-139">Por fim, selecione o pool de bordas e identifique se um próximo pool de saltos está configurado abaixo da **próxima seleção de salto**.</span><span class="sxs-lookup"><span data-stu-id="06a19-139">Finally, select the Edge pool and identify if a Next hop pool is configured below **Next hop selection**.</span></span>
    
    <span data-ttu-id="06a19-140">![Construtor de topologias, seleção do próximo salto](images/JJ205231.3121e723-fba7-498e-a786-bde7be1a55e2(OCS.15).jpg "Construtor de topologias, seleção do próximo salto")</span><span class="sxs-lookup"><span data-stu-id="06a19-140">![Topology Builder, Next hop selection](images/JJ205231.3121e723-fba7-498e-a786-bde7be1a55e2(OCS.15).jpg "Topology Builder, Next hop selection")</span></span>

<span data-ttu-id="06a19-141">**Verificar a configuração de parceiro federado do XMPP herdado**</span><span class="sxs-lookup"><span data-stu-id="06a19-141">**Verify legacy XMPP Federated Partner Configuration**</span></span>

1.  <span data-ttu-id="06a19-142">No servidor herdado XMPP, navegue até o applet Serviços de ferramentas administrativas \\ .</span><span class="sxs-lookup"><span data-stu-id="06a19-142">From the legacy XMPP server, navigate to the Administrative Tools\\Services applet.</span></span>

2.  <span data-ttu-id="06a19-143">Verifique se o serviço do Gateway XMPP do Office Communications Server foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="06a19-143">Verify that the Office Communications Server XMPP Gateway service is started.</span></span>
    
    <span data-ttu-id="06a19-144">![Serviço de Gateway XMPP do Office Communications Server](images/JJ721906.23223724-3c4b-4cb9-ace2-1cab2c3c91c3(OCS.15).jpg "Serviço de Gateway XMPP do Office Communications Server")</span><span class="sxs-lookup"><span data-stu-id="06a19-144">![Office Communications Server XMPP Gateway Service](images/JJ721906.23223724-3c4b-4cb9-ace2-1cab2c3c91c3(OCS.15).jpg "Office Communications Server XMPP Gateway Service")</span></span>

<span data-ttu-id="06a19-145"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06a19-145"></div>

<span> </span>

</div>

</div>

</span></span></div>

