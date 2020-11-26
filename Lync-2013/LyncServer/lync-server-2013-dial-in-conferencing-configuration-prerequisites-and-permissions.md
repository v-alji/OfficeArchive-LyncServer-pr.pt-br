---
title: Pré-requisitos e permissões de configuração de conferência discada
description: Permissões e pré-requisitos de configuração da conferência discada.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dial-in conferencing configuration prerequisites and permissions
ms:assetid: b3b251e5-78ac-44a2-8c36-2a061c9b2314
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412865(v=OCS.15)
ms:contentKeyID: 48185165
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eced67f33e35c711c4fcd31120480b6d5c2e41ce
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429253"
---
# <a name="dial-in-conferencing-configuration-prerequisites-and-permissions-in-lync-server-2013"></a><span data-ttu-id="ffbbb-103">Pré-requisitos e permissões de configuração de conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ffbbb-103">Dial-in conferencing configuration prerequisites and permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ffbbb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ffbbb-104">

<span> </span></span></span>

<span data-ttu-id="ffbbb-105">_**Tópico da última modificação:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="ffbbb-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="ffbbb-106">A conferência discada é um componente opcional da carga de trabalho de conferência do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-106">Dial-in conferencing is an optional component of the Lync Server 2013 Conferencing workload.</span></span> <span data-ttu-id="ffbbb-107">Os componentes que você precisa instalar antes de configurar a conferência discada são implantados quando você usa o construtor de topologias para criar sua topologia e, em seguida, configurar seu pool de front-end ou o servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-107">The components you need to install before you can configure dial-in conferencing are deployed when you use the Topology Builder to design your topology and then set up your Front End pool or Standard Edition server.</span></span> <span data-ttu-id="ffbbb-108">Este tópico descreve o que você precisa ter feito antes de poder configurar a conferência discada.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-108">This topic describes what you need to have accomplished before you can configure dial-in conferencing.</span></span>

<span data-ttu-id="ffbbb-109">Esta seção pressupõe que você tenha lido as seções de planejamento relacionadas à carga de trabalho de conferência e conferência discada em particular.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-109">This section assumes that you have read the planning sections related to the Conferencing workload and dial-in conferencing in particular.</span></span>

<div>

## <a name="dial-in-conferencing-configuration-prerequisites"></a><span data-ttu-id="ffbbb-110">Pré-requisitos de configuração da conferência discada</span><span class="sxs-lookup"><span data-stu-id="ffbbb-110">Dial-in Conferencing Configuration Prerequisites</span></span>

<span data-ttu-id="ffbbb-111">A conferência discada requer os seguintes componentes do Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="ffbbb-111">Dial-in conferencing requires the following Lync Server 2013 components:</span></span>

  - <span data-ttu-id="ffbbb-112">UCAS (Unified Communications Application Service) (chamado de *Serviço de aplicativos*)</span><span class="sxs-lookup"><span data-stu-id="ffbbb-112">Unified Communications Application Service (UCAS) (called the *Application service*)</span></span>

  - <span data-ttu-id="ffbbb-113">Aplicativo Atendedor de Conferência</span><span class="sxs-lookup"><span data-stu-id="ffbbb-113">Conferencing Attendant application</span></span>

  - <span data-ttu-id="ffbbb-114">Aplicativo Comunicado de Conferência</span><span class="sxs-lookup"><span data-stu-id="ffbbb-114">Conferencing Announcement application</span></span>

  - <span data-ttu-id="ffbbb-115">Página da Web Configurações de Conferência Discada</span><span class="sxs-lookup"><span data-stu-id="ffbbb-115">Dial-in Conferencing Settings webpage</span></span>

  - <span data-ttu-id="ffbbb-116">Pelo menos um servidor de mediação do Lync Server 2013 e pelo menos um gateway PSTN</span><span class="sxs-lookup"><span data-stu-id="ffbbb-116">At least one Lync Server 2013 Mediation Server and at least one PSTN gateway</span></span>

<span data-ttu-id="ffbbb-117">Você implanta esses componentes quando usa o construtor de topologias para definir e publicar sua topologia e, em seguida, implantar um pool de front-ends ou um servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-117">You deploy these components when you use the Topology Builder to define and publish your topology and then deploy a Front End pool or a Standard Edition server.</span></span> <span data-ttu-id="ffbbb-118">Se você estiver implantando o Enterprise Voice, deve implantá-lo antes de configurar a conferência discada.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-118">If you are deploying Enterprise Voice, you should deploy it before you configure dial-in conferencing.</span></span> <span data-ttu-id="ffbbb-119">Se você não estiver implantando o Enterprise Voice, poderá implantar um servidor de mediação e um gateway PSTN (rede telefônica pública comutada) ao implantar seu pool de front-end ou o servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-119">If you are not deploying Enterprise Voice, you can deploy a Mediation Server and a public switched telephone network (PSTN) gateway when you deploy your Front End pool or Standard Edition server.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="ffbbb-120">Se você estiver atualizando do Office Communications Server 2007 R2 para o Lync Server 2013, implante a conferência discada em todos os pools que planeja usar para hospedar conferências do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-120">If you are upgrading from Office Communications Server 2007 R2 to Lync Server 2013, deploy dial-in conferencing in every pool that you plan to use to host Lync Server 2013 conferences.</span></span> <span data-ttu-id="ffbbb-121">Para obter detalhes sobre a migração de conferência discada, consulte <A href="migration-from-office-communications-server-2007-r2-to-lync-server-2013.md">migração do Office Communications Server 2007 R2 para o Lync server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-121">For details about migrating dial-in conferencing, see <A href="migration-from-office-communications-server-2007-r2-to-lync-server-2013.md">Migration from Office Communications Server 2007 R2 to Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="ffbbb-122">Esta seção pressupõe que você tenha feito o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ffbbb-122">This section assumes that you have done the following:</span></span>

  - <span data-ttu-id="ffbbb-123">Aplicadas as atualizações mais recentes para o seu ambiente do Office Communications Server 2007 R2, se você estiver migrando para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-123">Applied the latest updates to your Office Communications Server 2007 R2 environment, if you are migrating to Lync Server 2013.</span></span>

  - <span data-ttu-id="ffbbb-124">Usou o construtor de topologias para projetar e configurar sua topologia.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-124">Used Topology Builder to design and configure your topology.</span></span> <span data-ttu-id="ffbbb-125">Ao especificar a carga de trabalho de conferência, você selecionou a opção de conferência discada.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-125">While specifying the Conferencing workload, you selected the dial-in conferencing option.</span></span> <span data-ttu-id="ffbbb-126">Para obter detalhes sobre como definir sua topologia, consulte [definindo e configurando a topologia no Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-126">For details about defining your topology, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md) in the Deployment documentation.</span></span>

  - <span data-ttu-id="ffbbb-127">Publicou sua topologia e configurar o pool de front-end ou o servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-127">Published your topology, and set up the Front End pool or Standard Edition server.</span></span> <span data-ttu-id="ffbbb-128">Para obter detalhes sobre como publicar a topologia e instalar o Lync Server 2013, consulte [implantação do Lync server 2013](lync-server-2013-deploying-lync-server.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-128">For details about publishing the topology and installing Lync Server 2013, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="ffbbb-129">Quando você instala sua topologia publicada, a página da Web configurações de conferência discada é instalada no servidor front-end ou no servidor Standard Edition como parte dos serviços Web.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-129">When you install your published topology, the Dial-in Conferencing Settings webpage is installed on the Front End Server or Standard Edition server as part of Web Services.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="ffbbb-130">Se você alterar o caminho para o repositório de arquivos no construtor de topologias depois de implantar o Lync Server 2013, será necessário reiniciar o atendedor de conferências e os aplicativos de anúncio de conferência para usar o novo caminho.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-130">If you change the path for the File Store in Topology Builder after you deploy Lync Server 2013, you need to restart the Conferencing Attendant and Conferencing Announcement applications to use the new path.</span></span>

    
    </div>

  - <span data-ttu-id="ffbbb-131">Enterprise Voice implantado.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-131">Deployed Enterprise Voice.</span></span> <span data-ttu-id="ffbbb-132">Se não estiver implantando o Enterprise Voice, você colocaria um servidor de mediação no servidor front-end do Enterprise Edition ou do servidor Standard Edition ou implantou um servidor de mediação autônomo e implantou um gateway PSTN.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-132">If you are not deploying Enterprise Voice, you either collocated a Mediation Server on the Enterprise Edition Front End Server or the Standard Edition server, or you deployed a stand-alone Mediation Server, and you deployed a PSTN gateway.</span></span> <span data-ttu-id="ffbbb-133">Para obter detalhes sobre a implantação do Enterprise Voice, consulte [implantação do Enterprise Voice no Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-133">For details about deploying Enterprise Voice, see [Deploying Enterprise Voice in Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) in the Deployment documentation.</span></span> <span data-ttu-id="ffbbb-134">Para obter detalhes sobre como instalar um servidor autônomo de mediação e um gateway PSTN, consulte [implantação de servidores de mediação e definição de pares no Lync Server 2013](lync-server-2013-deploying-mediation-servers-and-defining-peers.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-134">For details about installing a stand-alone Mediation Server and PSTN gateway, see [Deploying Mediation Servers and defining peers in Lync Server 2013](lync-server-2013-deploying-mediation-servers-and-defining-peers.md) in the Deployment documentation.</span></span>

<span data-ttu-id="ffbbb-135">O fluxograma a seguir mostra as etapas que você deve executar antes de poder configurar a conferência discada e as etapas que você executa para configurar a conferência discada.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-135">The following flowchart shows the steps that you must perform before you can configure dial-in conferencing and the steps that you perform to configure dial-in conferencing.</span></span>

<span data-ttu-id="ffbbb-136">**Implantando conferência discada**</span><span class="sxs-lookup"><span data-stu-id="ffbbb-136">**Deploying dial-in conferencing**</span></span>

<span data-ttu-id="ffbbb-137">![Fluxograma de implantação de conferência discada](images/Gg412865.fde8c246-b5ed-4323-a6e7-af1983a5ec86(OCS.15).jpg "Fluxograma de implantação de conferência discada")</span><span class="sxs-lookup"><span data-stu-id="ffbbb-137">![Dial-in Conferencing Deployment flowchart](images/Gg412865.fde8c246-b5ed-4323-a6e7-af1983a5ec86(OCS.15).jpg "Dial-in Conferencing Deployment flowchart")</span></span>

</div>

<div>

## <a name="dial-in-conferencing-permissions"></a><span data-ttu-id="ffbbb-138">Permissões de conferência discada</span><span class="sxs-lookup"><span data-stu-id="ffbbb-138">Dial-in Conferencing Permissions</span></span>

<span data-ttu-id="ffbbb-139">Para configurar a conferência discada, você precisará usar as seguintes ferramentas administrativas:</span><span class="sxs-lookup"><span data-stu-id="ffbbb-139">To configure dial-in conferencing, you need to use the following administrative tools:</span></span>

  - <span data-ttu-id="ffbbb-140">Painel de Controle do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ffbbb-140">Lync Server 2013 Control Panel</span></span>

  - <span data-ttu-id="ffbbb-141">Shell de Gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="ffbbb-141">Lync Server Management Shell</span></span>

<span data-ttu-id="ffbbb-142">Use essas ferramentas administrativas para configurar as configurações de conferência discada e os planos de discagem, as políticas e outras configurações necessárias para a conferência discada.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-142">You use these administrative tools to configure dial-in conferencing settings, and the dial plans, policies, and other settings that dial-in conferencing requires.</span></span>

<span data-ttu-id="ffbbb-143">A configuração da conferência discada requer qualquer uma das seguintes funções administrativas, dependendo da tarefa:</span><span class="sxs-lookup"><span data-stu-id="ffbbb-143">Configuring dial-in conferencing requires any of the following administrative roles, depending on the task:</span></span>

  - <span data-ttu-id="ffbbb-144">**CsVoiceAdministrator**   Essa função de administrador pode criar, configurar e gerenciar configurações e políticas relacionadas à voz.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-144">**CsVoiceAdministrator**   This administrator role can create, configure, and manage voice-related settings and policies.</span></span>

  - <span data-ttu-id="ffbbb-145">**CsUserAdministrator**   Essa função de administrador pode habilitar e desabilitar usuários do Lync Server e atribuir políticas existentes, como políticas de conferência e políticas de PIN, a usuários.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-145">**CsUserAdministrator**   This administrator role can enable and disable users for Lync Server and assign existing policies, such as conferencing policies and PIN policies, to users.</span></span>

  - <span data-ttu-id="ffbbb-146">**CsAdministrator**   Essa função de administrador pode executar todas as tarefas de CsVoiceAdministrator e CsUserAdministrator.</span><span class="sxs-lookup"><span data-stu-id="ffbbb-146">**CsAdministrator**   This administrator role can perform all of the tasks of CsVoiceAdministrator and CsUserAdministrator.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ffbbb-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffbbb-147">See Also</span></span>


[<span data-ttu-id="ffbbb-148">Implantando o Enterprise Voice no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ffbbb-148">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  
  

<span data-ttu-id="ffbbb-149"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ffbbb-149"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

