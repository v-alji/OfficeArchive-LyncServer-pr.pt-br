---
title: 'Lync Server 2013: Definindo seus requisitos para Servidores Front-End Servers, sistema de mensagens instantâneas e presença'
description: 'Lync Server 2013: definindo seus requisitos para servidores front-end, mensagens instantâneas e presença.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your requirements for Front End Servers, instant messaging, and presence
ms:assetid: c21198bc-520c-4d17-8b84-7ff1475b9b0a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412956(v=OCS.15)
ms:contentKeyID: 48185319
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 923132b32d5aef80191b19a7b85c3f17276e5946
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430809"
---
# <a name="defining-your-requirements-for-front-end-servers-instant-messaging-and-presence-in-lync-server-2013"></a><span data-ttu-id="9b678-103">Definindo seus requisitos para Servidores Front-End Servers, sistema de mensagens instantâneas e presença no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9b678-103">Defining your requirements for Front End Servers, instant messaging, and presence in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9b678-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9b678-104">

<span> </span></span></span>

<span data-ttu-id="9b678-105">_**Tópico da última modificação:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="9b678-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="9b678-106">A principal tarefa de planejar mensagens instantâneas (IM) e presença é garantir que você tenha servidores front-end suficientes para os usuários.</span><span class="sxs-lookup"><span data-stu-id="9b678-106">The main task of planning for instant messaging (IM) and presence is ensuring that you have enough Front End Servers for your users.</span></span>

<div>

## <a name="enabling-communication-with-external-users"></a><span data-ttu-id="9b678-107">Habilitar a comunicação com usuários externos</span><span class="sxs-lookup"><span data-stu-id="9b678-107">Enabling Communication with External Users</span></span>

<span data-ttu-id="9b678-108">Você pode aumentar bastante as vantagens do seu investimento no Lync Server ao permitir que seus usuários se comuniquem com usuários externos.</span><span class="sxs-lookup"><span data-stu-id="9b678-108">You can greatly increase the benefits of your investment in Lync Server by enabling your users to communicate with external users.</span></span> <span data-ttu-id="9b678-109">Entre os usuários externos podem estar:</span><span class="sxs-lookup"><span data-stu-id="9b678-109">External users can include:</span></span>

  - <span data-ttu-id="9b678-110">**Usuários remotos**   Os próprios usuários da sua organização, quando estiverem trabalhando fora dos firewalls e estiverem usando seus laptops ou outros dispositivos do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9b678-110">**Remote users**   Your organization’s own users, when they are working outside your firewalls and are using their laptops or other Lync Server devices.</span></span>

  - <span data-ttu-id="9b678-111">**Usuários federados**   Usuários de empresas com quem você trabalha com quem também executa o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9b678-111">**Federated users**   Users from companies you work with who also run Lync Server.</span></span> <span data-ttu-id="9b678-112">Para habilitar que seus usuários entrem em contato facilmente com esses usuários, crie relacionamentos federados com essas empresas.</span><span class="sxs-lookup"><span data-stu-id="9b678-112">To enable your users to easily contact these users, you create federated relationships with these companies.</span></span>

  - <span data-ttu-id="9b678-113">**Usuários públicos**   Os usuários de serviços públicos de mensagens de chat, como serviços de IM fornecidos pela rede do Windows Live dos serviços de Internet, Yahoo \! e AOL, e usuários de provedores e servidores que usam o protocolo de mensagens extensíveis e presença (XMPP), como o Google Talk.</span><span class="sxs-lookup"><span data-stu-id="9b678-113">**Public users**   Users of public IM services, such as IM services provided by the Windows Live network of Internet services, Yahoo\!, and AOL, and users of providers and servers that use Extensible Messaging and Presence Protocol (XMPP), such as Google Talk.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9b678-114">Observe que uma licença separada pode ser necessária para conectividade de IM pública com Windows Live, AOL e Yahoo!</span><span class="sxs-lookup"><span data-stu-id="9b678-114">Note that a separate license might be required for public IM connectivity with Windows Live, AOL, and Yahoo!</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="9b678-115">A partir de 1º de setembro de 2012, a licença de assinatura de usuário da conectividade de mensagem de chat pública do Microsoft Lync ("PIC USL") não está mais disponível para compra de contratos novos ou de renovação.</span><span class="sxs-lookup"><span data-stu-id="9b678-115">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="9b678-116">Os clientes com licenças ativas poderão continuar a federar-se com o Yahoo!</span><span class="sxs-lookup"><span data-stu-id="9b678-116">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="9b678-117">Messenger até a data de encerramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="9b678-117">Messenger until the service shut down date.</span></span> <span data-ttu-id="9b678-118">Uma data de fim da vida útil de junho de 2014 para AOL e Yahoo!</span><span class="sxs-lookup"><span data-stu-id="9b678-118">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="9b678-119">foi anunciado.</span><span class="sxs-lookup"><span data-stu-id="9b678-119">has been announced.</span></span> <span data-ttu-id="9b678-120">Para obter detalhes, consulte <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">suporte para conectividade de mensagens instantâneas públicas no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9b678-120">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="9b678-121">O PIC USL é uma licença de assinatura por usuário por mês necessária para o Lync Server ou o Office Communications Server se federar com o Yahoo!</span><span class="sxs-lookup"><span data-stu-id="9b678-121">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="9b678-122">Spam.</span><span class="sxs-lookup"><span data-stu-id="9b678-122">Messenger.</span></span> <span data-ttu-id="9b678-123">A capacidade da Microsoft de oferecer esse serviço por meio do suporte do Yahoo!, o contrato subjacente para o qual está prestes a ser enrolado.</span><span class="sxs-lookup"><span data-stu-id="9b678-123">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="9b678-124">Mais do que nunca, o Lync é uma ferramenta poderosa para a conexão entre organizações e pessoas ao redor do mundo.</span><span class="sxs-lookup"><span data-stu-id="9b678-124">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="9b678-125">A Federação com o Windows Live Messenger não requer licenças de usuário/dispositivo adicionais além da CAL padrão do Lync.</span><span class="sxs-lookup"><span data-stu-id="9b678-125">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="9b678-126">A Federação do Skype será adicionada a essa lista, permitindo que os usuários do Lync atinjam centenas de milhões de pessoas com mensagens instantâneas e voz.</span><span class="sxs-lookup"><span data-stu-id="9b678-126">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>

    
    </div>

<span data-ttu-id="9b678-127">Para habilitar qualquer um desses cenários, você precisa implantar um servidor de borda para ajudar a habilitar comunicações seguras entre a implantação do Lync Server e os usuários externos.</span><span class="sxs-lookup"><span data-stu-id="9b678-127">To enable any or all of these scenarios, you need to deploy an Edge Server to help enable secure communications between your Lync Server deployment and external users.</span></span> <span data-ttu-id="9b678-128">Os usuários remotos de sua organização e os usuários em organizações federadas poderão ver a presença uns dos outros e se comunicar usando mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="9b678-128">Your organization’s remote users and users at federated organizations will be able to see each other’s presence and communicate using IM.</span></span> <span data-ttu-id="9b678-129">Para obter detalhes sobre como habilitar a comunicação com usuários externos, consulte [planejando o acesso de usuários externos no Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="9b678-129">For details about enabling communication with external users, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="archiving-im-content"></a><span data-ttu-id="9b678-130">Arquivar conteúdo de IM</span><span class="sxs-lookup"><span data-stu-id="9b678-130">Archiving IM Content</span></span>

<span data-ttu-id="9b678-131">O Lync Server fornece recursos que você pode usar se a sua organização deve seguir as normas de conformidade.</span><span class="sxs-lookup"><span data-stu-id="9b678-131">Lync Server provides features you can use if your organization must follow compliance regulations.</span></span> <span data-ttu-id="9b678-132">É possível usar a função Arquivamento para arquivar o conteúdo de mensagens instantâneas de todos os usuários de sua organização ou apenas de usuários específicos.</span><span class="sxs-lookup"><span data-stu-id="9b678-132">You can use Archiving to archive the content of IM messages for all users in your organization or for only certain users that you specify.</span></span> <span data-ttu-id="9b678-133">Para obter detalhes, consulte [planejando o arquivamento no Lync Server 2013](lync-server-2013-planning-for-archiving.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="9b678-133">For details, see [Planning for Archiving in Lync Server 2013](lync-server-2013-planning-for-archiving.md) in the Planning documentation.</span></span>

<span data-ttu-id="9b678-134">Se você também tiver o Microsoft Exchange Server 2013 implantado, poderá integrar o arquivamento dos dados do Exchange com o arquivamento dos dados do Lync Server e usar uma única ferramenta para pesquisar os dois tipos de dados arquivados.</span><span class="sxs-lookup"><span data-stu-id="9b678-134">If you also have Microsoft Exchange Server 2013 deployed, you can integrate the archiving of Exchange data with the archiving of Lync Server data, and use a single tool to search both types of archived data.</span></span> <span data-ttu-id="9b678-135">Para obter mais informações, consulte [Configurando o Microsoft Lync server 2013 para usar o Microsoft Exchange server 2013 Archiving](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="9b678-135">For more information, see [Configuring Microsoft Lync Server 2013 to use Microsoft Exchange Server 2013 archiving](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md).</span></span>

<span data-ttu-id="9b678-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9b678-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

