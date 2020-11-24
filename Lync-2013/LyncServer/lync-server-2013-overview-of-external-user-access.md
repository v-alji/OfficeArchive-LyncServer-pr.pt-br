---
title: 'Lync Server 2013: Visão geral de acesso de usuário externo'
description: 'Lync Server 2013: visão geral do acesso de usuários externos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of external user access
ms:assetid: 97aded6c-5fa3-4225-95a6-9ad094d61654
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398775(v=OCS.15)
ms:contentKeyID: 48184934
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d2900dde457da34c4438892878ae7ddb4f74723a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390239"
---
# <a name="overview-of-external-user-access-in-lync-server-2013"></a><span data-ttu-id="e3869-103">Visão geral de acesso de usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e3869-103">Overview of external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e3869-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e3869-104">

<span> </span></span></span>

<span data-ttu-id="e3869-105">_**Tópico da última modificação:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="e3869-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="e3869-106">Nesta documentação, usamos o termo *usuário externo* para definir uma grande categoria de usuários que se comunicam com os usuários do lync Server 2013 e do Lync 2013 de fora do firewall.</span><span class="sxs-lookup"><span data-stu-id="e3869-106">In this documentation, we use the term *external user* to define a large category of users who communicate with your Lync Server 2013 and Lync 2013 users from outside the firewall.</span></span> <span data-ttu-id="e3869-107">Os usuários externos que você pode autorizar a comunicar ao Lync Server 2013 com usuários internos (ou seja, os usuários que se conectarem ao Lync Server de dentro do firewall) podem incluir o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e3869-107">External users that you can authorize to communicate Lync Server 2013 with internal users (that is, users who sign in to Lync Server from inside the firewall) can include the following:</span></span>

  - <span data-ttu-id="e3869-108">**Usuários remotos**   Os usuários da sua organização que se conectarem ao Lync Server de fora do firewall.</span><span class="sxs-lookup"><span data-stu-id="e3869-108">**Remote users**   Users of your organization who sign in to Lync Server from outside the firewall.</span></span>

  - <span data-ttu-id="e3869-109">**Usuários federados**   Usuários que têm uma conta com uma organização de cliente ou parceiro confiável, como o Lync Server 2010, o Lync Server 2013 ou o Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="e3869-109">**Federated users**   Users who have an account with a trusted customer or partner organization, such as Lync Server 2010, Lync Server 2013 or Office Communications Server 2007 R2.</span></span> <span data-ttu-id="e3869-110">Os usuários federados também podem ser membros de organizações parceiras definidas usando o protocolo de mensagens extensíveis (XMPP) por meio do proxy XMPP no servidor de borda e do XMPP gateway do servidor ou pool de front-end.</span><span class="sxs-lookup"><span data-stu-id="e3869-110">Federated users can also be members of defined partner organizations using extensible messaging and presence protocol (XMPP) by way of the XMPP proxy on the Edge Server and XMPP gateway on the Front End Server or pool.</span></span> <span data-ttu-id="e3869-111">Uma relação de confiança definida, chamada de Federação, não está relacionada a ou dependente de uma relação de confiança dos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e3869-111">A defined trust relationship, called a federation, is not related to or dependent upon an Active Directory Domain Services trust relationship.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e3869-112">Uma data de fim da vida útil de junho de 2014 para AOL e Yahoo!</span><span class="sxs-lookup"><span data-stu-id="e3869-112">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="e3869-113">foi anunciado.</span><span class="sxs-lookup"><span data-stu-id="e3869-113">has been announced.</span></span> <span data-ttu-id="e3869-114">Para obter detalhes, consulte <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">suporte para conectividade de mensagens instantâneas públicas no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="e3869-114">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span>

    
    </div>

  - <span data-ttu-id="e3869-115">**Usuários de conectividade de mensagens instantâneas públicas**   Contatos que seus usuários estabelecem por meio de serviços públicos de conectividade de mensagens instantâneas (Windows Live, Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="e3869-115">**Public Instant Messaging Connectivity users**   Contacts that your users establish through public instant messaging connectivity services (Windows Live, Yahoo\!</span></span> <span data-ttu-id="e3869-116">e AOL).</span><span class="sxs-lookup"><span data-stu-id="e3869-116">and AOL).</span></span>

  - <span data-ttu-id="e3869-117">**Usuários móveis**   Os usuários que são membros da sua organização que usam um telefone inteligente ou tablet que executam um cliente móvel do Lync entram em sua implantação interna e podem se comunicar com as outras classes de usuários.</span><span class="sxs-lookup"><span data-stu-id="e3869-117">**Mobile users**   Users that are members of your organization that use a smart phone or tablet running a Lync Mobile client sign in to your internal deployment and are able to communicate with the other classes of users.</span></span> <span data-ttu-id="e3869-118">O usuário móvel usa os serviços de mobilidade publicados por meio do proxy reverso para acessar a implantação interna.</span><span class="sxs-lookup"><span data-stu-id="e3869-118">The mobile user uses mobility services that are published through the reverse proxy to access the internal deployment.</span></span> <span data-ttu-id="e3869-119">Para obter detalhes sobre os recursos e as funcionalidades disponíveis para o Lync Mobile, consulte as tabelas de comparação de clientes móveis em [https://go.microsoft.com/fwlink/p/?LinkID=234777](https://go.microsoft.com/fwlink/p/?linkid=234777) .</span><span class="sxs-lookup"><span data-stu-id="e3869-119">For details on features and capabilities available to Lync Mobile , see the Mobile Client Comparison Tables at [https://go.microsoft.com/fwlink/p/?LinkID=234777](https://go.microsoft.com/fwlink/p/?linkid=234777).</span></span>

  - <span data-ttu-id="e3869-120">**Usuários anônimos**   Os usuários que não têm uma conta de usuário nos serviços de domínio do Active Directory da sua organização ou em um domínio federado com suporte, mas que receberam convites para participarem remotamente em uma conferência local.</span><span class="sxs-lookup"><span data-stu-id="e3869-120">**Anonymous users**   Users who do not have a user account in your organization's Active Directory Domain Services or in a supported federated domain, but who have received invitations to participate remotely in an on-premises conference.</span></span>

<span data-ttu-id="e3869-121">Sua implantação de borda oferece acesso externo para os seguintes tipos de comunicação:</span><span class="sxs-lookup"><span data-stu-id="e3869-121">Your edge deployment provides external access for the following types of communication:</span></span>

  - <span data-ttu-id="e3869-122">**Mensagens instantâneas e presença**   Usuários externos autorizados podem participar de conversas e conferências de mensagens instantâneas, e eles podem obter informações sobre o status de presença de outro.</span><span class="sxs-lookup"><span data-stu-id="e3869-122">**IM and presence**   Authorized external users can participate in IM conversations and conferences, and they can get information about one another’s presence status.</span></span> <span data-ttu-id="e3869-123">Os usuários de provedores de serviços públicos de mensagens instantâneas podem participar de conversas de mensagens instantâneas com usuários individuais do Lync Server em sua organização e acessar as informações de presença, mas não podem participar de conferências com vários participantes usando o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e3869-123">Users of public IM service providers can participate in IM conversations with individual Lync Server users in your organization and access presence information, but they cannot participate in IM multiparty conferences using Lync Server.</span></span> <span data-ttu-id="e3869-124">É estritamente comunicação ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="e3869-124">It is strictly peer-to-peer communication.</span></span> <span data-ttu-id="e3869-125">Não há suporte para a transferência de arquivos para os usuários de provedores de serviços públicos de mensagens instantâneas e áudio/vídeo em comunicações ponto a ponto são compatíveis com usuários do Windows Messenger 2011, mas não para outros usuários de provedores de serviços públicos de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="e3869-125">File transfer is not supported for users of public IM service providers, and audio/video in peer-to-peer communications is supported for Windows Messenger 2011 users, but not other users of public IM service providers.</span></span>
    
    <span data-ttu-id="e3869-126">Há suporte para os protocolos SIP e XMPP.</span><span class="sxs-lookup"><span data-stu-id="e3869-126">Both SIP and XMPP protocols are supported.</span></span> <span data-ttu-id="e3869-127">Para fornecer serviços para o XMPP, consulte [planejando o SIP, a Federação do XMPP e mensagens instantâneas públicas no Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="e3869-127">To provide services for XMPP, see [Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md).</span></span>

  - <span data-ttu-id="e3869-128">**Conferência da Web**   Usuários externos autorizados podem participar de conferências hospedadas em sua implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e3869-128">**Web conferencing**   Authorized external users can participate in conferences that are hosted on your Lync Server deployment.</span></span> <span data-ttu-id="e3869-129">Usuários remotos, usuários federados e usuários anônimos podem ser habilitados para a participação na Web conferência, mas os usuários de mensagens de chat públicas não podem participar de conferências.</span><span class="sxs-lookup"><span data-stu-id="e3869-129">Remote users, federated users, and anonymous users can be enabled for participation in web conferencing, but public IM users cannot participate in conferences.</span></span> <span data-ttu-id="e3869-130">Dependendo das opções que você selecionar, os usuários habilitados para Webconferência podem participar do compartilhamento de área de trabalho e aplicativos e podem atuar como organizadores ou apresentadores da reunião.</span><span class="sxs-lookup"><span data-stu-id="e3869-130">Depending on the options that you select, web conferencing-enabled users can participate in desktop and application sharing and can act as meeting organizers or presenters.</span></span>

  - <span data-ttu-id="e3869-131">**Conferência A/V**   Usuários externos autorizados podem participar de conferências de áudio e vídeo que a implantação do Lync Server hospeda.</span><span class="sxs-lookup"><span data-stu-id="e3869-131">**A/V conferencing**   Authorized external users can participate in audio and video conferences that your Lync Server deployment hosts.</span></span> <span data-ttu-id="e3869-132">O áudio/vídeo em comunicações ponto a ponto é compatível com usuários do Windows Messenger 2011, mas não para outros usuários de provedores de serviços públicos de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="e3869-132">Audio/video in peer-to-peer communications is supported for Windows Messenger 2011 users, but not for other users of public IM service providers.</span></span>

<span data-ttu-id="e3869-133">Para controlar a comunicação, você pode configurar uma ou mais políticas que definem como os usuários dentro e fora da sua organização se comunicam.</span><span class="sxs-lookup"><span data-stu-id="e3869-133">In order to control communications, you can configure one or more policies that define how users inside and outside your organization communicate with each other.</span></span> <span data-ttu-id="e3869-134">Você também pode definir as configurações e aplicar políticas para usuários internos individuais ou para tipos específicos de usuários externos para controlar a comunicação com usuários externos.</span><span class="sxs-lookup"><span data-stu-id="e3869-134">You can also configure settings and apply policies for individual internal users or for specific types of external users to control communications with external users.</span></span>

<span data-ttu-id="e3869-135">Funções do Lync Server 2013 usadas para fornecer acesso externo:</span><span class="sxs-lookup"><span data-stu-id="e3869-135">Lync Server 2013 roles that are used to provide external access:</span></span>

<span data-ttu-id="e3869-136">**Servidor de borda**   O servidor de borda é um servidor ou um pool de servidores que executam os serviços que permitem acesso externo a mensagens instantâneas e presença, conferência, áudio/vídeo e outros tipos de mídia (por exemplo, transferência de arquivos).</span><span class="sxs-lookup"><span data-stu-id="e3869-136">**Edge Server**   The Edge Server is a server or a pool of servers that run the services that allow external access to IM and presence, conferencing, audio/video, and other media (for example, file transfer) services.</span></span> <span data-ttu-id="e3869-137">Opcionalmente, você pode configurar o servidor de borda para federar outras implantações do Lync Server ou do Office Communications Server 2007 R2 e outras implantações do XMPP.</span><span class="sxs-lookup"><span data-stu-id="e3869-137">Optionally, you can configure the Edge Server to federate with other Lync Server or Office Communications Server 2007 R2 deployments, and other XMPP deployments.</span></span> <span data-ttu-id="e3869-138">O recurso opcional de conectividade de mensagem instantânea pública está habilitado e configurado por meio do servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="e3869-138">The optional public IM connectivity feature is enabled and configured through the Edge Server.</span></span>

<span data-ttu-id="e3869-139">**Diretor**   O diretor é um servidor opcional ou um pool de servidores que executa a função de diretor do Lync Server 2013, que autentica previamente solicitações do usuário e roteia solicitações para o servidor front-end primário dos usuários ou o pool de front-end, mas não hospeda nenhuma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="e3869-139">**Director**   The Director is an optional server or server pool running the Lync Server 2013 Director role that pre-authenticates user requests and routes requests to the users’ home Front End Server or Front End pool, but does not home any user accounts.</span></span>

<span data-ttu-id="e3869-140">**Proxy reverso**   Um proxy reverso é um termo geral para servidores especializados que publicam recursos disponíveis na rede interna e recuperam informações para clientes do recurso publicado.</span><span class="sxs-lookup"><span data-stu-id="e3869-140">**Reverse Proxy**   A reverse proxy is a general term for specialized servers that publish resources available on the internal network and retrieve information for clients from the published resource.</span></span> <span data-ttu-id="e3869-141">O Lync Server 2013 usa o proxy inverso para publicar vários recursos, como reuniões de conferência, locais de ingresso em conferência, catálogo de endereços, expansão da lista de distribuição, download de conteúdo da reunião, atualizações de dispositivo, serviços de mobilidade e muito mais.</span><span class="sxs-lookup"><span data-stu-id="e3869-141">Lync Server 2013 uses the reverse proxy to publish a number of features, such as conferencing meetings, conference join locations, the address book, distribution list expansion, downloading meeting content, device updates, Mobility services, and more.</span></span> <span data-ttu-id="e3869-142">Qualquer proxy reverso que possa atender aos requisitos para publicação dos locais de recursos necessários pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="e3869-142">Any reverse proxy that can meet the requirements for publishing the necessary resource locations can be used.</span></span> <span data-ttu-id="e3869-143">O Microsoft Forefront Threat Management Gateway (TMG) 2010 é usado como um exemplo para a finalidade de ilustrar as regras de publicação necessárias, mas o Forefront TMG 2010 não é necessário.</span><span class="sxs-lookup"><span data-stu-id="e3869-143">Microsoft Forefront Threat Management Gateway (TMG) 2010 is used as an example for the purposes of illustrating the publishing rules necessary, but Forefront TMG 2010 is not required.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e3869-144">O Lync Server 2013 dá suporte a IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="e3869-144">Lync Server 2013 supports both IPv4 and IPv6.</span></span> <span data-ttu-id="e3869-145">O Windows Server &nbsp; 2008 &nbsp; R2, o windows Server 2012 e o windows Server 2012 R2 usam uma pilha dupla que pode usar o IPv4 e o IPv6 simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="e3869-145">Windows Server&nbsp;2008&nbsp;R2, Windows Server 2012, and Windows Server 2012 R2 use a dual stack that can use both IPv4 and IPv6 concurrently.</span></span> <span data-ttu-id="e3869-146">Isso é importante porque a natureza Transitional de uma implantação está migrando do IPv4 para o IPv6.</span><span class="sxs-lookup"><span data-stu-id="e3869-146">This is important because of the transitional nature of a deployment moving from IPv4 to IPv6.</span></span> <span data-ttu-id="e3869-147">O IPv4 pode ser compatível em algumas áreas, em que em outras áreas da implantação, o IPv6 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="e3869-147">IPv4 can be supported in some areas, where in other areas of the deployment, IPv6 can be used.</span></span> <span data-ttu-id="e3869-148">Isso é especialmente importante quando a Internet e as implantações internas se preocupam.</span><span class="sxs-lookup"><span data-stu-id="e3869-148">This is especially important where the Internet and internal deployments are concerned.</span></span> <span data-ttu-id="e3869-149">Os clientes externos devem se comunicar pelo proxy reverso para usar serviços como mobilidade, reuniões, download do catálogo de endereços e outros.</span><span class="sxs-lookup"><span data-stu-id="e3869-149">External clients must communicate through the reverse proxy to use services such as mobility, meetings, address book download, and others.</span></span> <span data-ttu-id="e3869-150">Atualmente, o Forefront Threat Management Gateway 2010 e o Internet Security and Acceleration Server 2006 não dão suporte ao endereçamento IPv6, independentemente da versão do sistema operacional em que eles são implantados.</span><span class="sxs-lookup"><span data-stu-id="e3869-150">Currently, Forefront Threat Management Gateway 2010 and Internet Security and Acceleration Server 2006 do not support IPv6 addressing, regardless of the operating system version that they are deployed on.</span></span> <span data-ttu-id="e3869-151">Você deve planejar adequadamente em relação ao uso do IPv6 e do IPv4, pois eles estão relacionados a clientes externos.</span><span class="sxs-lookup"><span data-stu-id="e3869-151">You must plan accordingly in relation to your use of IPv6 and IPv4 as they relate to external clients.</span></span>



<span data-ttu-id="e3869-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e3869-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

