---
title: 'Lync Server 2013: Topologias suportadas'
description: Topologias compatíveis com o Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported topologies
ms:assetid: 3475d430-0394-491b-a09b-ba85bd62be70
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425833(v=OCS.15)
ms:contentKeyID: 48183832
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 39c19577fbda7e377e145abfd473d2cf8e6d4a1a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441428"
---
# <a name="supported-topologies-in-lync-server-2013"></a><span data-ttu-id="37a5e-103">Topologias suportadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37a5e-103">Supported topologies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="37a5e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="37a5e-104">

<span> </span></span></span>

<span data-ttu-id="37a5e-105">_**Tópico da última modificação:** 2014-01-14_</span><span class="sxs-lookup"><span data-stu-id="37a5e-105">_**Topic Last Modified:** 2014-01-14_</span></span>

<span data-ttu-id="37a5e-106">O Lync Server 2013 dá suporte à implantação de sites locais em uma organização e à integração de implantações locais com implantações do Lync Online, que é conhecida como uma implantação híbrida.</span><span class="sxs-lookup"><span data-stu-id="37a5e-106">Lync Server 2013 supports deployment of sites on premises in an organization and integration of on-premises deployments with Lync Online deployments, which is known as a hybrid deployment.</span></span> <span data-ttu-id="37a5e-107">Em uma implantação híbrida, alguns usuários são hospedados localmente e alguns usuários são hospedados online.</span><span class="sxs-lookup"><span data-stu-id="37a5e-107">In a hybrid deployment, some users are homed on-premises and some users are homed online.</span></span>

<span data-ttu-id="37a5e-108">Para implantações locais, o Lync Server 2013 é compatível com a implantação de um ou mais sites que podem ser dimensionados para atender aos requisitos de alta disponibilidade e local.</span><span class="sxs-lookup"><span data-stu-id="37a5e-108">For on-premises deployments, Lync Server 2013 supports deployment of one or more sites that can be scaled to meet high availability and location requirements.</span></span> <span data-ttu-id="37a5e-109">Você pode estruturar esses sites e seus componentes para atender aos requisitos de acesso e adaptabilidade da sua organização.</span><span class="sxs-lookup"><span data-stu-id="37a5e-109">You can structure these sites and their components to meet the access and resiliency requirements of your organization.</span></span>

<span data-ttu-id="37a5e-110">Uma implantação local do Lync Server 2013 consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="37a5e-110">A Lync Server 2013 on-premises deployment consists of the following:</span></span>

  - <span data-ttu-id="37a5e-111">Sua implantação deve incluir pelo menos um site central (também conhecido como um Data Center).</span><span class="sxs-lookup"><span data-stu-id="37a5e-111">Your deployment must include at least one central site (also known as a data center).</span></span> <span data-ttu-id="37a5e-112">Cada site central deve conter pelo menos um pool de front-end do Enterprise Edition ou um servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="37a5e-112">Each central site must contain at least one Enterprise Edition Front End pool or one Standard Edition server.</span></span> <span data-ttu-id="37a5e-113">Eles consistem nos seguintes:</span><span class="sxs-lookup"><span data-stu-id="37a5e-113">These consist of the following:</span></span>
    
      - <span data-ttu-id="37a5e-114">Pool de front-end do Enterprise Edition, que consiste em um ou mais servidores front-end (geralmente, pelo menos dois servidores front-end para escalabilidade) e um servidor back-end separado.</span><span class="sxs-lookup"><span data-stu-id="37a5e-114">Enterprise Edition Front End pool, which consists of one or more Front End Servers (typically, at least two Front End Servers for scalability) and a separate Back End Server.</span></span> <span data-ttu-id="37a5e-115">Um pool de front-ends pode conter no máximo doze servidores front end.</span><span class="sxs-lookup"><span data-stu-id="37a5e-115">A Front End pool can contain a maximum of twelve Front End Servers.</span></span> <span data-ttu-id="37a5e-116">O balanceamento de carga é necessário para vários servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="37a5e-116">Load balancing is required for multiple Front End Servers.</span></span> <span data-ttu-id="37a5e-117">Para o tráfego SIP, recomendamos o balanceamento de carga de DNS, mas também há suporte para o balanceamento de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="37a5e-117">For SIP traffic, we recommend DNS load balancing, but hardware load balancing is also supported.</span></span> <span data-ttu-id="37a5e-118">Se você usar o balanceamento de carga de DNS para o tráfego SIP, ainda precisará de um balanceador de carga de hardware para tráfego HTTP.</span><span class="sxs-lookup"><span data-stu-id="37a5e-118">If you use DNS load balancing for SIP traffic, you still need a hardware load balancer for HTTP traffic.</span></span> <span data-ttu-id="37a5e-119">Recomendamos o espelhamento do SQL Server para alta disponibilidade de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="37a5e-119">We recommend SQL Server mirroring for high availability of databases.</span></span> <span data-ttu-id="37a5e-120">O banco de dados back-end requer uma instância separada, mas você pode posicionar o banco de dados de arquivamento, o banco de dados de monitoramento, o banco de dados de chat persistente e o banco de dados de conformidade de chat persistente</span><span class="sxs-lookup"><span data-stu-id="37a5e-120">The back-end database requires a separate instance, but you can collocate the archiving database, monitoring database, persistent chat database, and persistent chat compliance database with it.</span></span> <span data-ttu-id="37a5e-121">O Lync Server 2013 oferece suporte ao uso de um cluster compartilhado para os compartilhamentos de arquivos na sua implantação.</span><span class="sxs-lookup"><span data-stu-id="37a5e-121">Lync Server 2013 supports the use of a shared cluster for the file shares in your deployment.</span></span> <span data-ttu-id="37a5e-122">Para obter detalhes sobre requisitos de armazenamento de banco de dados, consulte [suporte a software de banco de dados no Lync Server 2013](lync-server-2013-database-software-support.md).</span><span class="sxs-lookup"><span data-stu-id="37a5e-122">For details about database storage requirements, see [Database software support in Lync Server 2013](lync-server-2013-database-software-support.md).</span></span> <span data-ttu-id="37a5e-123">Para obter detalhes sobre requisitos de armazenamento de arquivos, consulte [suporte ao armazenamento de arquivos no Lync Server 2013](lync-server-2013-file-storage-support.md).</span><span class="sxs-lookup"><span data-stu-id="37a5e-123">For details about file storage requirements, see [File storage support in Lync Server 2013](lync-server-2013-file-storage-support.md).</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="37a5e-124">Se você posicionar bancos de dados do Lync Server, é altamente recomendável avaliar todos os fatores que podem afetar a disponibilidade e o desempenho.</span><span class="sxs-lookup"><span data-stu-id="37a5e-124">If you collocate Lync Server databases, we highly recommend assessing all factors that might affect availability and performance.</span></span> <span data-ttu-id="37a5e-125">Para verificar as capacidades de failover, recomendamos o teste de todos os cenários de failover.</span><span class="sxs-lookup"><span data-stu-id="37a5e-125">To verify failover capabilities, we recommend testing all failover scenarios.</span></span>

        
        </div>
    
      - <span data-ttu-id="37a5e-126">Standard Edition Server, que inclui um banco de dados do SQL Server Express posicionado.</span><span class="sxs-lookup"><span data-stu-id="37a5e-126">Standard Edition server, which includes a collocated SQL Server Express database.</span></span>

  - <span data-ttu-id="37a5e-127">Sua implantação também pode ter um ou mais sites de filiais associados a um site central.</span><span class="sxs-lookup"><span data-stu-id="37a5e-127">Your deployment can also have one or more branch sites associated with a central site.</span></span>

<span data-ttu-id="37a5e-128">Esta seção descreve os sites e os componentes de uma implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="37a5e-128">This section describes the sites and components of a Lync Server 2013 deployment.</span></span> <span data-ttu-id="37a5e-129">Para obter detalhes sobre o site, a topologia e o planejamento de componentes do Lync Server 2013, consulte [noções básicas de topologia que você precisa saber antes de planejar o Lync server 2013](lync-server-2013-topology-basics-you-must-know-before-planning.md) e as [topologias de referência no Lync Server 2013](lync-server-2013-reference-topologies.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="37a5e-129">For details about Lync Server 2013 site, topology, and component planning, see [Topology basics you must know before planning for Lync Server 2013](lync-server-2013-topology-basics-you-must-know-before-planning.md) and [Reference topologies in Lync Server 2013](lync-server-2013-reference-topologies.md) in the Planning documentation.</span></span> <span data-ttu-id="37a5e-130">Para obter detalhes sobre a integração de componentes de versões anteriores, consulte [caminhos de migração e cenários de coexistência suportados no Lync Server 2013](lync-server-2013-supported-migration-paths-and-coexistence-scenarios.md).</span><span class="sxs-lookup"><span data-stu-id="37a5e-130">For details about integration of components of previous releases, see [Supported migration paths and coexistence scenarios in Lync Server 2013](lync-server-2013-supported-migration-paths-and-coexistence-scenarios.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="37a5e-131">Pools ampliados não são compatíveis com as funções de servidor front-end, Edge, Mediation e director.</span><span class="sxs-lookup"><span data-stu-id="37a5e-131">Stretched pools are not supported for the Front End, Edge, Mediation, and Director server roles.</span></span>



</div>

<div>

## <a name="central-site-topologies-and-components-on-premises"></a><span data-ttu-id="37a5e-132">Topologias e componentes de sites centrais (local)</span><span class="sxs-lookup"><span data-stu-id="37a5e-132">Central Site Topologies and Components (On-Premises)</span></span>

<span data-ttu-id="37a5e-133">Embora uma topologia de site central deva incluir um pool de front-end ou um servidor Standard Edition, cada site central também pode conter o seguinte:</span><span class="sxs-lookup"><span data-stu-id="37a5e-133">Although a central site topology must include one Front End pool or one Standard Edition server, each central site can also contain the following:</span></span>

  - <span data-ttu-id="37a5e-134">Vários pools de front-end, que podem estar no mesmo domínio ou domínios diferentes.</span><span class="sxs-lookup"><span data-stu-id="37a5e-134">Multiple Front End pools, which can be in the same domain or different domains.</span></span> <span data-ttu-id="37a5e-135">No entanto, todos os servidores de front-end em um pool de front-end e o servidor back-end desse pool devem estar no mesmo domínio.</span><span class="sxs-lookup"><span data-stu-id="37a5e-135">However, all Front End Servers in a Front End pool, and the Back End Server for that pool, must be in the same domain.</span></span>

  - <span data-ttu-id="37a5e-136">Vários servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="37a5e-136">Multiple Standard Edition servers.</span></span>

  - <span data-ttu-id="37a5e-137">Office Web Apps Server, que é usado com os aplicativos Web do Office no Lync Server 2013 para manipular o compartilhamento e a renderização de apresentações do Microsoft PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="37a5e-137">Office Web Apps Server, which is used with Office Web Applications in Lync Server 2013 to handle the sharing and rendering of Microsoft PowerPoint presentations.</span></span>

  - <span data-ttu-id="37a5e-138">Servidor de borda ou o pool de bordas na sua rede de perímetro, se você quiser que a implantação dê suporte a parceiros federados, conectividade de mensagem de chat pública, um gateway de protocolo de presença e mensagens (XMPP) extensível, acesso de usuário remoto, participação de usuários anônimos em reuniões ou Exchange Unified Messaging (UM).</span><span class="sxs-lookup"><span data-stu-id="37a5e-138">Edge Server or Edge pool in your perimeter network, if you want your deployment to support federated partners, public IM connectivity, an extensible messaging and presence protocol (XMPP) gateway, remote user access, participation of anonymous users in meetings, or Exchange Unified Messaging (UM).</span></span> <span data-ttu-id="37a5e-139">Você não pode colocar nenhuma outra função de servidor com um servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="37a5e-139">You cannot collocate any other server role with an Edge Server.</span></span> <span data-ttu-id="37a5e-140">Recomendamos o balanceamento de carga de DNS, quando apropriado, mas também há suporte para o balanceamento de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="37a5e-140">We recommend DNS load balancing, where appropriate, but hardware load balancing is also supported.</span></span> <span data-ttu-id="37a5e-141">As interfaces de Borda interna e externa precisam usar o mesmo tipo de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="37a5e-141">The internal Edge interface and external Edge interface must use the same type of load balancing.</span></span> <span data-ttu-id="37a5e-142">Não é possível usar balanceamento de carga DNS em uma interface de Borda e balanceamento de carga de hardware na outra interface de Borda.</span><span class="sxs-lookup"><span data-stu-id="37a5e-142">You cannot use DNS load balancing on one Edge interface and hardware load balancing on the other Edge interface.</span></span> <span data-ttu-id="37a5e-143">Para obter detalhes sobre requisitos e suporte de balanceamento de carga, consulte [planejando o acesso de usuários externos no Lync server 2013](lync-server-2013-planning-for-external-user-access.md) na documentação de planejamento e [implantando o acesso de usuários externos no Lync Server 2013](lync-server-2013-deploying-external-user-access.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="37a5e-143">For details about load balancing requirements and support, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span>

  - <span data-ttu-id="37a5e-144">Servidor de mediação ou pool, se você quiser dar suporte à conferência de voz ou discada em um pool de front-ends no site central.</span><span class="sxs-lookup"><span data-stu-id="37a5e-144">Mediation Server or pool, if you want to support Enterprise Voice or dial-in conferencing in a Front End pool at the central site.</span></span> <span data-ttu-id="37a5e-145">Dependendo de como você implantou o suporte do Enterprise Voice, pode colocar o servidor de mediação em um pool de front-end (o padrão) ou implantar um servidor ou pool autônomo de mediação.</span><span class="sxs-lookup"><span data-stu-id="37a5e-145">Depending on how you deploy Enterprise Voice support, you can collocate the Mediation Server in a Front End pool (the default) or deploy a stand-alone Mediation Server or pool.</span></span> <span data-ttu-id="37a5e-146">Você pode usar o DNS, o hardware ou o balanceamento de carga do aplicativo (quando adequado) para distribuir o tráfego de um peer de gateway do pool do servidor de mediação, incluindo um gateway PSTN, IP-PBX ou controle de borda de sessão de tronco SIP (SBC). Para obter detalhes sobre como planejar a topologia do servidor de mediação apropriada, consulte [diretrizes de implantação do servidor de mediação no Lync server 2013](lync-server-2013-deployment-guidelines-for-mediation-server.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="37a5e-146">You can use DNS, hardware, or application load balancing (when appropriate) to distribute traffic from a Mediation Server pool’s gateway peer, including a PSTN gateway, IP-PBX, or SIP trunk Session Border Control (SBC).For details about planning the appropriate Mediation Server topology, see [Deployment guidelines for Mediation Server in Lync Server 2013](lync-server-2013-deployment-guidelines-for-mediation-server.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="37a5e-147">Servidor de chat persistente, se você quiser que os usuários possam participar em conversas com vários participantes, com base em tópicos que persistem ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="37a5e-147">Persistent Chat Server, if you want to users to be able to participate in multiparty, topic-based conversations that persist over time.</span></span> <span data-ttu-id="37a5e-148">Para fornecer mais capacidade e maior confiabilidade, a topologia pode incluir vários computadores que executam o servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="37a5e-148">To provide more capacity and increased reliability, your topology can include multiple computers running Persistent Chat Server.</span></span> <span data-ttu-id="37a5e-149">Você não pode colocar o servidor de chat persistente com outras funções de servidor em um pool de empresas.</span><span class="sxs-lookup"><span data-stu-id="37a5e-149">You cannot collocate Persistent Chat Server with other server roles in an Enterprise pool.</span></span> <span data-ttu-id="37a5e-150">No entanto, você pode colocar o servidor de chat persistente em um servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="37a5e-150">However, you can collocate Persistent Chat Server on a Standard Edition server.</span></span> <span data-ttu-id="37a5e-151">O chat persistente exige um banco de dados e, se você implementar a conformidade persistente de chat, um banco de dados de conformidade de chat persistente, mas os bancos de dados puderem ficar posicionados com o banco de dados de arquivamento, monitorando o banco de dados ou no servidor back-end de um pool Front-end da edição Enterprise.</span><span class="sxs-lookup"><span data-stu-id="37a5e-151">Persistent chat requires a database and, if you implement persistent chat compliance, a persistent chat compliance database, but the databases can be collocated with the Archiving database, Monitoring database, or on the Back End Server of an Enterprise Edition Front End pool.</span></span> <span data-ttu-id="37a5e-152">Para obter detalhes sobre como planejar a topologia do servidor de chat persistente apropriada, consulte [planejando o servidor de chat persistente no Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="37a5e-152">For details about planning the appropriate Persistent Chat Server topology, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="37a5e-153">Monitoramento, se você quiser dar suporte a coleta de dados para a qualidade de qualidade de áudio/vídeo (QoE) e registro de detalhes de chamadas (CDR) para conferências do Enterprise Voice e de A/V na sua implantação.</span><span class="sxs-lookup"><span data-stu-id="37a5e-153">Monitoring, if you want to support data collection for audio/video Quality of Experience (QoE) and call detail recording (CDR) for Enterprise Voice and A/V conferences in your deployment.</span></span> <span data-ttu-id="37a5e-154">Opcionalmente, você pode instalar o Microsoft System Center Operations Manager (antigo Microsoft Operations Manager), que usa monitoramento de dados CDR e QoE para gerar alertas de tempo real, que mostram a integridade da confiabilidade das chamadas e a qualidade das mídias.</span><span class="sxs-lookup"><span data-stu-id="37a5e-154">Optionally, you can install the Microsoft System Center Operations Manager (formerly Microsoft Operations Manager), which uses Monitoring CDR and QoE data to generate near real-time alerts that show the health of call reliability and media quality.</span></span> <span data-ttu-id="37a5e-155">O monitoramento, quando implantado, é posicionado em servidores front-end ou em um servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="37a5e-155">Monitoring, when deployed, is collocated on Front End Servers or a Standard Edition server.</span></span> <span data-ttu-id="37a5e-156">O monitoramento exige um banco de dados, mas o banco de dados pode ficar posicionado com o banco de dados de arquivamento, banco de dados de chat persistente, banco de dados de conformidade de chat persistente ou no servidor back-end de um pool Front-end da Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="37a5e-156">Monitoring requires a database, but the database can be collocated with the Archiving database, persistent chat database, persistent chat compliance database, or on the Back End Server of an Enterprise Edition Front End pool.</span></span>

  - <span data-ttu-id="37a5e-157">Arquivamento, se você quiser arquivar comunicações de mensagem instantânea e conteúdo da reunião (por motivos de conformidade) em sua implantação.</span><span class="sxs-lookup"><span data-stu-id="37a5e-157">Archiving, if you want to archive IM communications and meeting content (for compliance reasons) in your deployment.</span></span> <span data-ttu-id="37a5e-158">O arquivamento, quando implantado, é posicionado em servidores front-end ou em um servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="37a5e-158">Archiving, when deployed, is collocated on Front End Servers or a Standard Edition server.</span></span> <span data-ttu-id="37a5e-159">O armazenamento de arquivamento requer a implantação de um banco de dados de arquivamento ou integração com o armazenamento do Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="37a5e-159">Archiving storage requires either deployment of an Archiving database or integration with Exchange 2013 storage.</span></span> <span data-ttu-id="37a5e-160">Se você usar ambos, que é conhecido como *modo misto*, o armazenamento do Exchange 2013 é usado para armazenar dados de arquivo morto para os usuários que são hospedados no Exchange 2013, e o banco de dados de arquivamento é usado para arquivar dados para todos os outros usuários na sua implantação.</span><span class="sxs-lookup"><span data-stu-id="37a5e-160">If you use both, which is known as *mixed mode*, Exchange 2013 storage is used to store archive data for users who are homed on Exchange 2013, and the Archiving database is used to archive data for all other users in your deployment.</span></span> <span data-ttu-id="37a5e-161">Se você precisar de um banco de dados de arquivamento, o banco de dados poderá ser posicionado no banco de dados de monitoramento, banco de dados persistente de chat, banco de dados de conformidade de chat persistente ou no servidor back-end de um pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="37a5e-161">If you require an Archiving database, the database can be collocated on the Monitoring database, persistent chat database, persistent chat compliance database, or on the Back End Server of a Front End pool.</span></span> <span data-ttu-id="37a5e-162">Para obter detalhes sobre como planejar a topologia de arquivamento apropriada, consulte [planejando o arquivamento no Lync Server 2013](lync-server-2013-planning-for-archiving.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="37a5e-162">For details about planning the appropriate Archiving topology, see [Planning for Archiving in Lync Server 2013](lync-server-2013-planning-for-archiving.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="37a5e-163">O director ou o pool do director, se você quiser facilitar a resiliência e o redirecionamento de solicitações de usuário do Lync Server 2013 para o pool primário do usuário, que pode ser um pool Front-end Enterprise Edition ou um servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="37a5e-163">Director or Director pool, if you want to facilitate resiliency and redirection of Lync Server 2013 user requests to the user’s home pool, which can be either an Enterprise Edition Front End pool or a Standard Edition server.</span></span> <span data-ttu-id="37a5e-164">Recomendamos que você implante um diretor ou um pool de diretor em cada site central compatível com acesso externo a usuários e em cada site central no qual você implanta um ou mais pools front-ends.</span><span class="sxs-lookup"><span data-stu-id="37a5e-164">We recommend that you deploy a Director or Director pool in each central site that supports external user access and in each central site in which you deploy one or more Front End pools.</span></span> <span data-ttu-id="37a5e-165">Cada pool de directors pode conter no máximo dez directors.</span><span class="sxs-lookup"><span data-stu-id="37a5e-165">Each Director pool can contain a maximum of ten Directors.</span></span> <span data-ttu-id="37a5e-166">Um diretor não pode ser posicionado com nenhuma outra função de servidor.</span><span class="sxs-lookup"><span data-stu-id="37a5e-166">A Director cannot be collocated with any other server role.</span></span> <span data-ttu-id="37a5e-167">Para obter detalhes sobre como planejar a topologia de diretor apropriada, consulte [cenários do diretor do Lync Server 2013](lync-server-2013-scenarios-for-the-director.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="37a5e-167">For details about planning the appropriate Director topology, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="37a5e-168">O proxy inverso, que não é um componente do Lync Server 2013, mas é necessário se você deseja dar suporte ao compartilhamento de conteúdo da Web para usuários federados ou dar suporte ao tráfego de mobilidade.</span><span class="sxs-lookup"><span data-stu-id="37a5e-168">Reverse proxy, which is not a Lync Server 2013 component, but is required if you want to support sharing of web content for federated users or to support Mobility traffic.</span></span> <span data-ttu-id="37a5e-169">Você não pode colocar um servidor proxy reverso com qualquer função de servidor do Lync Server 2013, mas pode implementar o suporte de proxy reverso para uma implantação do Lync Server 2013 Configurando o suporte em um servidor de proxy reverso existente em sua organização que é usado para outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="37a5e-169">You cannot collocate a reverse proxy server with any Lync Server 2013 server role, but you can implement reverse proxy support for a Lync Server 2013 deployment by configuring the support on an existing reverse proxy server in your organization that is used for other applications.</span></span> <span data-ttu-id="37a5e-170">Para obter detalhes sobre servidores proxy invertido, consulte [Configurando servidores proxy inversos para o Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="37a5e-170">For details about reverse proxy servers, see [Setting up reverse proxy servers for Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md) in the Deployment documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="37a5e-171">No Lync Server 2013, A conferência A/V, o monitoramento e o arquivamento são executados em servidores front-end e não são mais funções de servidor separadas.</span><span class="sxs-lookup"><span data-stu-id="37a5e-171">In Lync Server 2013, A/V Conferencing, Monitoring, and Archiving run on Front End Servers and are no longer separate server roles.</span></span>



</div>

<span data-ttu-id="37a5e-172">Todos os pools de front-end e servidores Standard Edition que você implanta em um site central compartilham qualquer um dos itens a serem implantados para o site central:</span><span class="sxs-lookup"><span data-stu-id="37a5e-172">All Front End pools and Standard Edition servers that you deploy at a central site share any of the following that you deploy for the central site:</span></span>

  - <span data-ttu-id="37a5e-173">Pool de directors ou diretor</span><span class="sxs-lookup"><span data-stu-id="37a5e-173">Director or Director pool</span></span>

  - <span data-ttu-id="37a5e-174">Servidor ou pool de mediação autônomo</span><span class="sxs-lookup"><span data-stu-id="37a5e-174">Stand-alone Mediation Server or pool</span></span>

  - <span data-ttu-id="37a5e-175">Servidor Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="37a5e-175">Office Web Apps Server</span></span>

  - <span data-ttu-id="37a5e-176">Servidor de borda ou o pool de bordas</span><span class="sxs-lookup"><span data-stu-id="37a5e-176">Edge Server or Edge pool</span></span>

  - <span data-ttu-id="37a5e-177">Servidor ou pool de chat persistente</span><span class="sxs-lookup"><span data-stu-id="37a5e-177">Persistent Chat Server or pool</span></span>

  - <span data-ttu-id="37a5e-178">Monitoramento</span><span class="sxs-lookup"><span data-stu-id="37a5e-178">Monitoring</span></span>

  - <span data-ttu-id="37a5e-179">Archiving</span><span class="sxs-lookup"><span data-stu-id="37a5e-179">Archiving</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="37a5e-180">Um servidor Exchange UM pode ser implementado com sua implantação do Lync Server 2013 se você quiser oferecer suporte à integração de mensagens unificadas do Exchange 2013, mas não é um componente do site do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="37a5e-180">An Exchange UM Server can be implemented with your Lync Server 2013 deployment if you want to support integration of Exchange 2013 Unified Messaging, but it is not a component of the Lync Server 2013 site.</span></span>



</div>

<span data-ttu-id="37a5e-181">Vários sites centrais também podem compartilhar qualquer um dos seguintes itens implantados em um site central:</span><span class="sxs-lookup"><span data-stu-id="37a5e-181">Multiple central sites can also share any of the following that you deploy in one central site:</span></span>

  - <span data-ttu-id="37a5e-182">Servidor ou pool de mediação autônomo</span><span class="sxs-lookup"><span data-stu-id="37a5e-182">Stand-alone Mediation Server or pool</span></span>

  - <span data-ttu-id="37a5e-183">Servidor de borda ou o pool de bordas</span><span class="sxs-lookup"><span data-stu-id="37a5e-183">Edge Server or Edge pool</span></span>

  - <span data-ttu-id="37a5e-184">Servidor ou pool de chat persistente</span><span class="sxs-lookup"><span data-stu-id="37a5e-184">Persistent Chat Server or pool</span></span>

  - <span data-ttu-id="37a5e-185">Archiving</span><span class="sxs-lookup"><span data-stu-id="37a5e-185">Archiving</span></span>

  - <span data-ttu-id="37a5e-186">Monitoramento</span><span class="sxs-lookup"><span data-stu-id="37a5e-186">Monitoring</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="37a5e-187">Um servidor Exchange UM pode ser implementado com a implantação do Lync Server 2013 e compartilhado por vários sites centrais, mas não é um componente do site do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="37a5e-187">An Exchange UM Server can be implemented with your Lync Server 2013 deployment and shared by multiple central sites, but it is not a component of the Lync Server 2013 site.</span></span>



</div>

<span data-ttu-id="37a5e-188">Para obter detalhes sobre funções e funcionalidades do servidor do Lync Server 2013, consulte [funções de servidor no Lync server 2013](lync-server-2013-server-roles.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="37a5e-188">For details about Lync Server 2013 server roles and functionality, see [Server roles in Lync Server 2013](lync-server-2013-server-roles.md) in the Planning documentation.</span></span>

<span data-ttu-id="37a5e-189">Para obter um resumo do suporte à colocação do servidor do Lync Server 2013, consulte [colocação do servidor com suporte no Lync server 2013](lync-server-2013-supported-server-collocation.md).</span><span class="sxs-lookup"><span data-stu-id="37a5e-189">For a summary of Lync Server 2013 server collocation support, see [Supported server collocation in Lync Server 2013](lync-server-2013-supported-server-collocation.md).</span></span>

<span data-ttu-id="37a5e-190">Além das funções de servidor e da funcionalidade abordada anteriormente nesta seção, o Lync Server 2013 tem componentes e opções adicionais, que podem incluir alguns ou todos os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="37a5e-190">In addition to the server roles and functionality covered previously in this section, Lync Server 2013 has additional components and options, which can include some or all of the following:</span></span>

  - <span data-ttu-id="37a5e-191">Firewalls</span><span class="sxs-lookup"><span data-stu-id="37a5e-191">Firewalls</span></span>

  - <span data-ttu-id="37a5e-192">Gateways PSTN (se a implantação do Enterprise Voice estiver sendo implantada)</span><span class="sxs-lookup"><span data-stu-id="37a5e-192">PSTN gateways (if deploying Enterprise Voice)</span></span>

  - <span data-ttu-id="37a5e-193">Servidor Exchange UM</span><span class="sxs-lookup"><span data-stu-id="37a5e-193">Exchange UM Server</span></span>

  - <span data-ttu-id="37a5e-194">Balanceamento de carga DNS</span><span class="sxs-lookup"><span data-stu-id="37a5e-194">DNS load balancing</span></span>

  - <span data-ttu-id="37a5e-195">Balanceadores de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="37a5e-195">Hardware load balancers</span></span>

  - <span data-ttu-id="37a5e-196">Bancos de dados do SQL Server</span><span class="sxs-lookup"><span data-stu-id="37a5e-196">SQL Server databases</span></span>

  - <span data-ttu-id="37a5e-197">Compartilhamentos de arquivo</span><span class="sxs-lookup"><span data-stu-id="37a5e-197">File shares</span></span>

<span data-ttu-id="37a5e-198">Para obter detalhes sobre todos os recursos, componentes e opções do Lync Server 2013, consulte a documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="37a5e-198">For details about all of the Lync Server 2013 features, components, and options, see the Planning documentation.</span></span>

</div>

<div>

## <a name="branch-site-topologies-and-components-on-premises"></a><span data-ttu-id="37a5e-199">Topologias e componentes de sites de ramificação (local)</span><span class="sxs-lookup"><span data-stu-id="37a5e-199">Branch Site Topologies and Components (On-Premises)</span></span>

<span data-ttu-id="37a5e-200">Um site de filial está associado a um site central, e cada aplicativo de ramificação sobreviventes em um site de filial está associado a um pool de front-end da edição Enterprise ou um servidor Standard Edition no site central associado.</span><span class="sxs-lookup"><span data-stu-id="37a5e-200">A branch site is associated with a central site, and each Survivable Branch Appliance in a branch site is associated with an Enterprise Edition Front End pool or a Standard Edition server in the associated central site.</span></span> <span data-ttu-id="37a5e-201">Os sites de filiais dependem do site central para a maioria da funcionalidade, para que os componentes em um site de filial contenham apenas os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="37a5e-201">Branch sites depend on the central site for most of their functionality, so components at a branch site contain only the following:</span></span>

  - <span data-ttu-id="37a5e-202">Um aparelho de ramificação sobreviventes que combina um gateway PSTN (rede telefônica pública comutada) com alguma funcionalidade do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="37a5e-202">A Survivable Branch Appliance, which combines a public switched telephone network (PSTN) gateway with some Lync Server functionality.</span></span> <span data-ttu-id="37a5e-203">Um servidor de mediação pode ser colocado na instância do registrador do aplicativo de ramificação sobreviventes, e você pode implantar um servidor autônomo de mediação ou um pool de servidores de mediação autônomos.</span><span class="sxs-lookup"><span data-stu-id="37a5e-203">A Mediation Server can be collocated with the instance of the Registrar on the Survivable Branch Appliance, and you can deploy a stand-alone Mediation Server or pool of Mediation Servers.</span></span>

  - <span data-ttu-id="37a5e-204">Um servidor de ramificação sobreviventes, que é um servidor que executa o Windows Server com software do Lync Server 2013 registrador e Media Server instalado.</span><span class="sxs-lookup"><span data-stu-id="37a5e-204">A Survivable Branch Server, which is a server running Windows Server that has Lync Server 2013 Registrar and Mediation Server software installed.</span></span>

  - <span data-ttu-id="37a5e-205">Um gateway PSTN autônomo (não faz parte do Appliance de ramificação sobreviventes) e um servidor de mediação autônomo.</span><span class="sxs-lookup"><span data-stu-id="37a5e-205">A stand-alone PSTN gateway (not part of the Survivable Branch Appliance) and a stand-alone Mediation Server.</span></span>

<span data-ttu-id="37a5e-206">Os requisitos para servidores de ramificações sobreviventes são os mesmos dos requisitos para qualquer função de servidor do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="37a5e-206">The requirements for Survivable Branch Servers are the same as the requirements for any Lync Server 2013 server role.</span></span>

<span data-ttu-id="37a5e-207"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="37a5e-207"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

