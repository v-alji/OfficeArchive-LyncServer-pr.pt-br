---
title: 'Lync Server 2013: Funções do servidor'
description: Funções de servidor do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server roles
ms:assetid: 7137fc06-fca2-4e5f-9db5-10c7c29a788c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398536(v=OCS.15)
ms:contentKeyID: 48184456
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ee4636e602e5bfb8ce6eacdccb3d190f5728d1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441855"
---
# <a name="server-roles-in-lync-server-2013"></a><span data-ttu-id="ce468-103">Funções do servidor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce468-103">Server roles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ce468-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ce468-104">

<span> </span></span></span>

<span data-ttu-id="ce468-105">_**Tópico da última modificação:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="ce468-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="ce468-106">Cada servidor que executa o Lync Server executa uma ou mais *funções de servidor*.</span><span class="sxs-lookup"><span data-stu-id="ce468-106">Each server running Lync Server runs one or more *server roles*.</span></span> <span data-ttu-id="ce468-107">Uma função de servidor é um conjunto definido de funcionalidades do Lync Server fornecidas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="ce468-107">A server role is a defined set of Lync Server functionalities provided by that server.</span></span> <span data-ttu-id="ce468-108">Você não precisa implantar todas as funções de servidor disponíveis em sua rede.</span><span class="sxs-lookup"><span data-stu-id="ce468-108">You do not need to deploy all available server roles in your network.</span></span> <span data-ttu-id="ce468-109">Instale somente as funções que contêm a funcionalidade desejada.</span><span class="sxs-lookup"><span data-stu-id="ce468-109">Install only the server roles that contain the functionality that you want.</span></span>

<span data-ttu-id="ce468-110">Mesmo que você não esteja familiarizado com funções de servidor no Lync Server, a ferramenta de planejamento pode orientá-lo na melhor solução para os servidores que você precisa implantar, com base nos recursos desejados.</span><span class="sxs-lookup"><span data-stu-id="ce468-110">Even if you are not familiar with server roles in Lync Server, the Planning Tool can guide you to the best solution for the servers that you need to deploy, based on the features that you want.</span></span> <span data-ttu-id="ce468-111">Esta seção fornece uma breve visão geral das funções de servidor e os recursos gerais que elas fornecem:</span><span class="sxs-lookup"><span data-stu-id="ce468-111">This section provides a brief overview of the server roles and the general features that they provide:</span></span>

  - <span data-ttu-id="ce468-112">Servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="ce468-112">Standard Edition Server</span></span>

  - <span data-ttu-id="ce468-113">Servidor Front-End e Servidor Back-End</span><span class="sxs-lookup"><span data-stu-id="ce468-113">Front End Server and Back End Server</span></span>

  - <span data-ttu-id="ce468-114">Servidor de Borda</span><span class="sxs-lookup"><span data-stu-id="ce468-114">Edge Server</span></span>

  - <span data-ttu-id="ce468-115">Servidor de Mediação</span><span class="sxs-lookup"><span data-stu-id="ce468-115">Mediation Server</span></span>

  - <span data-ttu-id="ce468-116">Diretor</span><span class="sxs-lookup"><span data-stu-id="ce468-116">Director</span></span>

  - <span data-ttu-id="ce468-117">Servidor de front-end de bate-papo persistente</span><span class="sxs-lookup"><span data-stu-id="ce468-117">Persistent Chat Front End Server</span></span>

  - <span data-ttu-id="ce468-118">Repositório de chat persistente (servidor persistente de back-end de chat)</span><span class="sxs-lookup"><span data-stu-id="ce468-118">Persistent Chat Store (Persistent Chat Back End Server)</span></span>

  - <span data-ttu-id="ce468-119">Repositório de conformidade de chat persistente (servidor back-end de conformidade de chat persistente)</span><span class="sxs-lookup"><span data-stu-id="ce468-119">Persistent Chat Compliance Store (Persistent Chat Compliance Back End Server)</span></span>

<span data-ttu-id="ce468-120">Na maioria das funções de servidor, para fins de escalabilidade e alta disponibilidade, você pode implantar *pools* de vários servidores, todos executando a mesma função.</span><span class="sxs-lookup"><span data-stu-id="ce468-120">For most server roles, for scalability and high availability you can deploy *pools* of multiple servers all running the same server role.</span></span> <span data-ttu-id="ce468-121">Cada servidor de um pool deve executar funções idênticas de servidor.</span><span class="sxs-lookup"><span data-stu-id="ce468-121">Each server in a pool must run an identical server role or roles.</span></span> <span data-ttu-id="ce468-122">Para a maioria dos tipos de pools no Lync Server, você deve implantar um balanceador de carga para espalhar o tráfego entre os vários servidores do pool.</span><span class="sxs-lookup"><span data-stu-id="ce468-122">For most types of pools in Lync Server, you must deploy a load balancer to spread traffic between the various servers in the pool.</span></span> <span data-ttu-id="ce468-123">O Lync Server dá suporte ao balanceamento de carga do sistema de nomes de domínio (DNS) e ao equilíbrio de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="ce468-123">Lync Server supports both Domain Name System (DNS) load balancing and hardware load balancers.</span></span>

<div>

## <a name="standard-edition-server"></a><span data-ttu-id="ce468-124">Servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="ce468-124">Standard Edition Server</span></span>

<span data-ttu-id="ce468-125">O servidor Standard Edition foi projetado para pequenas organizações e para projetos pilotos de organizações de grande porte.</span><span class="sxs-lookup"><span data-stu-id="ce468-125">The Standard Edition server is designed for small organizations, and for pilot projects of large organizations.</span></span> <span data-ttu-id="ce468-126">Ele permite que muitos dos recursos do Lync Server, incluindo os bancos de dados necessários, sejam executados em um único servidor.</span><span class="sxs-lookup"><span data-stu-id="ce468-126">It enables many of the features of Lync Server, including the necessary databases, to run on a single server.</span></span> <span data-ttu-id="ce468-127">Isso permite que você tenha a funcionalidade do Lync Server por um custo menor, mas não oferece uma solução de alta disponibilidade real.</span><span class="sxs-lookup"><span data-stu-id="ce468-127">This enables you to have Lync Server functionality for a lower cost, but does not provide a true high-availability solution.</span></span>

<span data-ttu-id="ce468-128">O servidor Standard Edition permite que você use mensagens instantâneas (IM), presença, conferência e Enterprise Voice, tudo em execução em um servidor.</span><span class="sxs-lookup"><span data-stu-id="ce468-128">Standard Edition server enables you to use instant messaging (IM), presence, conferencing, and Enterprise Voice, all running on one server.</span></span>

<span data-ttu-id="ce468-129">Para uma solução de alta disponibilidade, use o Lync Server Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="ce468-129">For a high-availability solution, use Lync Server Enterprise Edition.</span></span>

</div>

<div>

## <a name="front-end-server-and-back-end-server"></a><span data-ttu-id="ce468-130">Servidor Front-End e Servidor Back-End</span><span class="sxs-lookup"><span data-stu-id="ce468-130">Front End Server and Back End Server</span></span>

<span data-ttu-id="ce468-131">No Lync Server Enterprise Edition, o servidor front-end é a função básica do servidor e executa muitas funções básicas do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ce468-131">In Lync Server Enterprise Edition, the Front End Server is the core server role, and runs many basic Lync Server functions.</span></span> <span data-ttu-id="ce468-132">O servidor front-end, juntamente com os servidores de back-end, são as únicas funções de servidor necessárias para a implantação do Lync Server Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="ce468-132">The Front End Server, along with the Back End Servers, are the only server roles required to be in any Lync Server Enterprise Edition deployment.</span></span>

<span data-ttu-id="ce468-133">Um *pool de front-ends* é um conjunto de servidores front-end configurados de maneira idêntica, que funcionam em conjunto para fornecer serviços para um grupo comum de usuários.</span><span class="sxs-lookup"><span data-stu-id="ce468-133">A *Front End pool* is a set of Front End Servers, configured identically, that work together to provide services for a common group of users.</span></span> <span data-ttu-id="ce468-134">Um pool de vários servidores que executa a mesma função fornece escalabilidade e o recurso de failover.</span><span class="sxs-lookup"><span data-stu-id="ce468-134">A pool of multiple servers running the same role provides scalability and failover capability.</span></span>

<span data-ttu-id="ce468-135">O servidor front-end inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ce468-135">The Front End Server includes the following:</span></span>

  - <span data-ttu-id="ce468-136">Autenticação e registro de usuários</span><span class="sxs-lookup"><span data-stu-id="ce468-136">User authentication and registration</span></span>

  - <span data-ttu-id="ce468-137">Informações de presença e troca de cartão de contato</span><span class="sxs-lookup"><span data-stu-id="ce468-137">Presence information and contact card exchange</span></span>

  - <span data-ttu-id="ce468-138">Expansão de serviços de catálogo de endereços e lista de distribuição</span><span class="sxs-lookup"><span data-stu-id="ce468-138">Address book services and distribution list expansion</span></span>

  - <span data-ttu-id="ce468-139">Funcionalidade de mensagens instantâneas, incluindo conferências de mensagens instantâneas com vários participantes</span><span class="sxs-lookup"><span data-stu-id="ce468-139">IM functionality, including multiparty IM conferences</span></span>

  - <span data-ttu-id="ce468-140">Conferência via Web, conferência discada de PSTN e conferência A/V (se implantada)</span><span class="sxs-lookup"><span data-stu-id="ce468-140">Web conferencing, PSTN Dial-in conferencing and A/V conferencing (if deployed)</span></span>

  - <span data-ttu-id="ce468-141">Hospedagem de aplicativos, para os dois aplicativos incluídos no Lync Server (por exemplo, o atendedor de conferência e o aplicativo de grupo de resposta) e aplicativos de terceiros</span><span class="sxs-lookup"><span data-stu-id="ce468-141">Application hosting, for both applications included with Lync Server (for example, Conferencing Attendant and Response Group application), and third-party applications</span></span>

  - <span data-ttu-id="ce468-142">Opcionalmente, Monitoramento, para coleta de informações de uso na forma de registros de detalhes das chamadas (CDRs) e registros de erros das chamadas (CERs).</span><span class="sxs-lookup"><span data-stu-id="ce468-142">Optionally, Monitoring, to collect usage information in the form of call detail records (CDRs) and call error records (CERs).</span></span> <span data-ttu-id="ce468-143">Essas informações fornecem métricas sobre a qualidade da mídia (áudio e vídeo) que atravessa a sua rede para chamadas de voz corporativa e conferências A/V.</span><span class="sxs-lookup"><span data-stu-id="ce468-143">This information provides metrics about the quality of the media (audio and video) traversing your network for both Enterprise Voice calls and A/V conferences.</span></span>

  - <span data-ttu-id="ce468-144">Componentes da Web para tarefas com suporte baseadas na Web, como agendador da Web e iniciador de ingresso.</span><span class="sxs-lookup"><span data-stu-id="ce468-144">Web components to supported web-based tasks such as web scheduler and join launcher.</span></span>

  - <span data-ttu-id="ce468-145">Opcionalmente, Arquivamento, para arquivar o conteúdo de reuniões e comunicações de IM por motivos de conformidade.</span><span class="sxs-lookup"><span data-stu-id="ce468-145">Optionally, Archiving, to archive IM communications and meeting content for compliance reasons.</span></span> <span data-ttu-id="ce468-146">Para obter detalhes, consulte [planejando o arquivamento no Lync Server 2013](lync-server-2013-planning-for-archiving.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="ce468-146">For details, see [Planning for Archiving in Lync Server 2013](lync-server-2013-planning-for-archiving.md) in the Planning documentation.</span></span>
    
    <span data-ttu-id="ce468-147">No Lync Server 2010 e em versões anteriores, o monitoramento e o arquivamento eram funções de servidor separadas, não posicionadas no servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="ce468-147">In Lync Server 2010 and prior versions, Monitoring and Archiving were separate server roles, not collocated on Front End Server.</span></span>

  - <span data-ttu-id="ce468-148">Opcionalmente, se o chat Persistente estiver habilitado, Serviços Web de Chat Persistente para Gerenciamento de Salas de Chat e Serviços Web de Chat Persistente para Upload/Download de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="ce468-148">Optionally, if Persistent chat is enabled, Persistent Chat Web Services for Chat Room Management and Persistent Chat Web Services for File Upload/Download.</span></span>

<span data-ttu-id="ce468-p109">Os Pools de Front-Ends também são o repositório principal de dados de usuários e conferências. As informações sobre cada usuário são replicadas em três Servidores Front-End do pool, e o seu backup é realizado nos Servidores Back-End.</span><span class="sxs-lookup"><span data-stu-id="ce468-p109">Front End Pools are also the primary store for user and conference data. Information about each user is replicated among three Front End Servers in the pool, and backed up on the Back End Servers.</span></span>

<span data-ttu-id="ce468-151">Além disso, um pool de front-end na implantação também executa o *servidor central de gerenciamento*, que gerencia e implanta dados de configuração básica em todos os servidores que executam o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ce468-151">Additionally, one Front End pool in the deployment also runs the *Central Management Server*, which manages and deploys basic configuration data to all servers running Lync Server.</span></span> <span data-ttu-id="ce468-152">O servidor central de gerenciamento também oferece recursos de shell e transferência de arquivos do Lync Server Management.</span><span class="sxs-lookup"><span data-stu-id="ce468-152">The Central Management Server also provides Lync Server Management Shell and file transfer capabilities.</span></span>

<span data-ttu-id="ce468-153">Os servidores de back-end são servidores de banco de dados executando o Microsoft SQL Server que fornecem os serviços de banco de dados para o pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="ce468-153">The Back End Servers are database servers running Microsoft SQL Server that provide the database services for the Front End pool.</span></span> <span data-ttu-id="ce468-154">Eles servem como repositórios de backup para os dados de conferências e de usuários do pool; além disso, eles são os repositórios principais para outros bancos de dados, como o banco de dados de Grupo de Resposta.</span><span class="sxs-lookup"><span data-stu-id="ce468-154">The Back End Servers serve as backup stores for the pool’s user and conference data, and are the primary stores for other databases such as the Response Group database.</span></span> <span data-ttu-id="ce468-155">Você pode ter um único servidor back-end, mas uma solução que usa o espelhamento do SQL Server é recomendada para failover.</span><span class="sxs-lookup"><span data-stu-id="ce468-155">You can have a single Back End Server, but a solution that uses SQL Server mirroring is recommended for failover.</span></span> <span data-ttu-id="ce468-156">Os servidores back-end não executam qualquer software do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ce468-156">Back End Servers do not run any Lync Server software.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ce468-157">Não recomendamos a colocação de bancos de dados do Lync Server com outros bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="ce468-157">We do not recommend collocating Lync Server databases with other databases.</span></span> <span data-ttu-id="ce468-158">Se isso for feito, a disponibilidade e o desempenho poderão ser afetados.</span><span class="sxs-lookup"><span data-stu-id="ce468-158">If you do so, availability and performance may be affected.</span></span>



</div>

<span data-ttu-id="ce468-159">As informações armazenadas nos bancos de dados do Servidor Back-End incluem informações de presença, listas de contatos dos usuários, dados de conferências, como dados persistentes sobre o estado de todas as conferências atuais, e dados de agendamento de conferências.</span><span class="sxs-lookup"><span data-stu-id="ce468-159">Information stored in the Back End Server databases includes presence information, users' Contacts lists, conferencing data, including persistent data about the state of all current conferences, and conference scheduling data.</span></span>

</div>

<div>

## <a name="edge-server"></a><span data-ttu-id="ce468-160">Servidor de Borda</span><span class="sxs-lookup"><span data-stu-id="ce468-160">Edge Server</span></span>

<span data-ttu-id="ce468-161">O servidor de borda permite que os usuários se comuniquem e colaborem com usuários de fora dos firewalls da organização.</span><span class="sxs-lookup"><span data-stu-id="ce468-161">Edge Server enables your users to communicate and collaborate with users outside the organization’s firewalls.</span></span> <span data-ttu-id="ce468-162">Esses usuários externos podem incluir os próprios usuários da organização que estão trabalhando externamente, usuários de organizações parceiras federadas e usuários externos que foram convidados a participar de conferências hospedadas na sua implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ce468-162">These external users can include the organization’s own users who are currently working offsite, users from federated partner organizations, and outside users who have been invited to join conferences hosted on your Lync Server deployment.</span></span> <span data-ttu-id="ce468-163">O Edge Server também permite a conectividade com serviços públicos de conectividade de IM, incluindo Windows Live, AOL, Yahoo \! e Google Talk.</span><span class="sxs-lookup"><span data-stu-id="ce468-163">Edge Server also enables connectivity to public IM connectivity services, including Windows Live, AOL, Yahoo\!, and Google Talk.</span></span>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="ce468-164">A partir de 1º de setembro de 2012, a licença de assinatura de usuário da conectividade de mensagem de chat pública do Microsoft Lync ("PIC USL") não está mais disponível para compra de contratos novos ou de renovação.</span><span class="sxs-lookup"><span data-stu-id="ce468-164">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="ce468-165">Os clientes com licenças ativas poderão continuar a federar-se com o Yahoo!</span><span class="sxs-lookup"><span data-stu-id="ce468-165">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="ce468-166">Messenger até a data de encerramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="ce468-166">Messenger until the service shut down date.</span></span> <span data-ttu-id="ce468-167">Uma data de fim da vida útil de junho de 2014 para AOL e Yahoo!</span><span class="sxs-lookup"><span data-stu-id="ce468-167">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="ce468-168">foi anunciado.</span><span class="sxs-lookup"><span data-stu-id="ce468-168">has been announced.</span></span> <span data-ttu-id="ce468-169">Para obter detalhes, consulte <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">suporte para conectividade de mensagens instantâneas públicas no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="ce468-169">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="ce468-170">O PIC USL é uma licença de assinatura por usuário por mês necessária para o Lync Server ou o Office Communications Server se federar com o Yahoo!</span><span class="sxs-lookup"><span data-stu-id="ce468-170">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="ce468-171">Spam.</span><span class="sxs-lookup"><span data-stu-id="ce468-171">Messenger.</span></span> <span data-ttu-id="ce468-172">A capacidade da Microsoft de oferecer esse serviço por meio do suporte do Yahoo!, o contrato subjacente para o qual está prestes a ser enrolado.</span><span class="sxs-lookup"><span data-stu-id="ce468-172">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="ce468-173">Mais do que nunca, o Lync é uma ferramenta poderosa para a conexão entre organizações e pessoas ao redor do mundo.</span><span class="sxs-lookup"><span data-stu-id="ce468-173">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="ce468-174">A Federação com o Windows Live Messenger não requer licenças de usuário/dispositivo adicionais além da CAL padrão do Lync.</span><span class="sxs-lookup"><span data-stu-id="ce468-174">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="ce468-175">A Federação do Skype será adicionada a essa lista, permitindo que os usuários do Lync atinjam centenas de milhões de pessoas com mensagens instantâneas e voz.</span><span class="sxs-lookup"><span data-stu-id="ce468-175">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="ce468-176">Implantar o Edge Server também permite serviços de mobilidade, que aceitam a funcionalidade do Lync em dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="ce468-176">Deploying Edge Server also enables mobility services, which supports Lync functionality on mobile devices.</span></span> <span data-ttu-id="ce468-177">Os usuários podem usar os dispositivos móveis Apple iOS, Android, Windows Phone ou Nokia com suporte para realizar atividades, como enviar e receber mensagens instantâneas, e exibir contatos e presença.</span><span class="sxs-lookup"><span data-stu-id="ce468-177">Users can use supported Apple iOS, Android, Windows Phone, or Nokia mobile devices to perform activities such as sending and receiving instant messages, viewing contacts, and viewing presence.</span></span> <span data-ttu-id="ce468-178">Além disso, os dispositivos móveis dão suporte a alguns recursos de voz empresarial, como o clique para ingressar em uma conferência, fazer chamadas pelo trabalho, por um único número, por correio de voz e chamadas perdidas.</span><span class="sxs-lookup"><span data-stu-id="ce468-178">In addition, mobile devices support some Enterprise Voice features, such as click to join a conference, Call via Work, single number reach, voice mail, and missed calls.</span></span> <span data-ttu-id="ce468-179">O recurso de mobilidade também oferece suporte a *notificações por push* em dispositivos móveis que não aceitam aplicativos executados em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="ce468-179">The mobility feature also supports *push notifications* for mobile devices that do not support applications running in the background.</span></span> <span data-ttu-id="ce468-180">Uma notificação por push é uma notificação enviada a um dispositivo móvel sobre um evento que ocorre enquanto o aplicativo móvel está inativo.</span><span class="sxs-lookup"><span data-stu-id="ce468-180">A push notification is a notification that is sent to a mobile device about an event that occurs while a mobile application is inactive.</span></span>

<span data-ttu-id="ce468-181">Os Servidores de Borda também incluem um proxy XMPP (Extensible Messaging and Presence Protocol) totalmente integrado, com um gateway XMPP nos Servidores Front-End.</span><span class="sxs-lookup"><span data-stu-id="ce468-181">Edge Servers also include a fully-integrated Extensible Messaging and Presence Protocol (XMPP) proxy, with an XMPP gateway included on Front End Servers.</span></span> <span data-ttu-id="ce468-182">Você pode configurar esses componentes do XMPP para permitir que os usuários do Lync Server 2013 adicionem contatos de parceiros baseados no XMPP (como Google Talk) para mensagens instantâneas e presença.</span><span class="sxs-lookup"><span data-stu-id="ce468-182">You can configure these XMPP components to enable your Lync Server 2013 users to add contacts from XMPP-based partners (such as Google Talk) for instant messaging and presence.</span></span>

<span data-ttu-id="ce468-183">Para obter detalhes, consulte [planejando o acesso de usuários externos no Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="ce468-183">For details, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="mediation-server"></a><span data-ttu-id="ce468-184">Servidor de Mediação</span><span class="sxs-lookup"><span data-stu-id="ce468-184">Mediation Server</span></span>

<span data-ttu-id="ce468-185">O servidor de mediação é um componente necessário para a implementação de conferência de voz e discada da empresa.</span><span class="sxs-lookup"><span data-stu-id="ce468-185">Mediation Server is a necessary component for implementing Enterprise Voice and dial-in conferencing.</span></span> <span data-ttu-id="ce468-186">O servidor de mediação traduz a sinalização e, em algumas configurações, mídia entre a infraestrutura interna do Lync Server e um gateway PSTN (rede telefônica pública comutada), IP-PBX ou um tronco SIP (Session Initiation Protocol).</span><span class="sxs-lookup"><span data-stu-id="ce468-186">Mediation Server translates signaling, and, in some configurations, media between your internal Lync Server infrastructure and a public switched telephone network (PSTN) gateway, IP-PBX, or a Session Initiation Protocol (SIP) trunk.</span></span> <span data-ttu-id="ce468-187">Você pode executar o servidor de mediação posicionado no mesmo servidor do front-end Server ou separado em um pool autônomo do servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="ce468-187">You can run Mediation Server collocated on the same server as Front End Server, or separated into a stand-alone Mediation Server pool.</span></span>

<span data-ttu-id="ce468-188">Para obter detalhes, consulte [componente do servidor de mediação no Lync server 2013](lync-server-2013-mediation-server-component.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="ce468-188">For details, see [Mediation Server component in Lync Server 2013](lync-server-2013-mediation-server-component.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="director"></a><span data-ttu-id="ce468-189">Diretor</span><span class="sxs-lookup"><span data-stu-id="ce468-189">Director</span></span>

<span data-ttu-id="ce468-190">Os diretores podem autenticar solicitações de usuário do Lync Server, mas não podem usar contas de usuário em casa nem fornecer serviços de presença ou de conferência.</span><span class="sxs-lookup"><span data-stu-id="ce468-190">Directors can authenticate Lync Server user requests, but they do not home user accounts or provide presence or conferencing services.</span></span> <span data-ttu-id="ce468-191">Eles são úteis principalmente para aumentar a segurança em implantações que permitem o acesso de usuários externos.</span><span class="sxs-lookup"><span data-stu-id="ce468-191">Directors are most useful to enhance security in deployments that enable external user access.</span></span> <span data-ttu-id="ce468-192">O Diretor pode autenticar as solicitações antes de enviá-las aos servidores internos.</span><span class="sxs-lookup"><span data-stu-id="ce468-192">The Director can authenticate requests before sending them on to internal servers.</span></span> <span data-ttu-id="ce468-193">Em caso de um ataque de negação de serviço, o ataque termina no Diretor e não atinge os servidores Front-End.</span><span class="sxs-lookup"><span data-stu-id="ce468-193">In the case of a denial-of-service attack, the attack ends with the Director and does not reach the Front End servers.</span></span> <span data-ttu-id="ce468-194">Para obter detalhes, consulte [cenários do diretor do Lync Server 2013](lync-server-2013-scenarios-for-the-director.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="ce468-194">For details, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="persistent-chat-server-roles"></a><span data-ttu-id="ce468-195">Funções de servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="ce468-195">Persistent Chat Server Roles</span></span>

<span data-ttu-id="ce468-p121">O chat persistente permite que os usuários participem de conversas baseadas em tópicos com vários participantes e que persistem ao longo do tempo. O Servidor Front-End de Chat Persistente executa o serviço de chat persistente. O Servidor Back-End de Chat Persistente armazena os dados de histórico de chat, bem como as informações sobre categorias e salas de chat. O Servidor Back-End de Conformidade de Chat Persistente (opcional) pode armazenar o conteúdo de chats e eventos de conformidade para fins de conformidade.</span><span class="sxs-lookup"><span data-stu-id="ce468-p121">Persistent chat enables users to participate in multiparty, topic-based conversations that persist over time. The Persistent Chat Front End Server runs the persistent chat service. The Persistent Chat Back End Server stores the chat history data, and information about categories and chat rooms. The optional Persistent Chat Compliance Back End Server can store the chat content and compliance events for the purpose of compliance.</span></span>

<span data-ttu-id="ce468-200">Os servidores que executam o Lync Server Standard Edition também podem executar o chat persistente posicionado no mesmo servidor.</span><span class="sxs-lookup"><span data-stu-id="ce468-200">Servers running Lync Server Standard Edition can also run Persistent chat collocated on the same server.</span></span> <span data-ttu-id="ce468-201">Você não pode colocar o servidor front-end do chat persistente com o servidor front-end do Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="ce468-201">You cannot collocate the Persistent Chat Front End Server with Enterprise Edition Front End Server.</span></span>

<span data-ttu-id="ce468-202">Para obter detalhes, consulte [planejando o servidor de chat persistente no Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="ce468-202">For details, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ce468-203">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce468-203">See Also</span></span>


[<span data-ttu-id="ce468-204">Componente servidor de mediação no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce468-204">Mediation Server component in Lync Server 2013</span></span>](lync-server-2013-mediation-server-component.md)  


[<span data-ttu-id="ce468-205">Planejando Arquivamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce468-205">Planning for Archiving in Lync Server 2013</span></span>](lync-server-2013-planning-for-archiving.md)  
[<span data-ttu-id="ce468-206">Planejamento para acesso de usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce468-206">Planning for external user access in Lync Server 2013</span></span>](lync-server-2013-planning-for-external-user-access.md)  
[<span data-ttu-id="ce468-207">Cenários para o Diretor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce468-207">Scenarios for the Director in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-the-director.md)  
[<span data-ttu-id="ce468-208">Planejando o Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce468-208">Planning for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-planning-for-persistent-chat-server.md)  
  

<span data-ttu-id="ce468-209"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ce468-209"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

