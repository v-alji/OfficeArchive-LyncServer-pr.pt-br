---
title: Topologia de referência do Lync Server 2013 para pequenas organizações
description: Topologia de referência do Lync Server 2013 para pequenas organizações.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reference topology for small organizations
ms:assetid: 0453aeee-c41f-44e6-a6e0-aaace526ca08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398095(v=OCS.15)
ms:contentKeyID: 48183272
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f2f23a963543c303e54f8f2773d499e8317a63a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436587"
---
# <a name="reference-topology-for-lync-server-2013-in-small-organizations"></a><span data-ttu-id="07f68-103">Topologia de referência para o Lync Server 2013 em pequenas organizações</span><span class="sxs-lookup"><span data-stu-id="07f68-103">Reference topology for Lync Server 2013 in small organizations</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="07f68-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="07f68-104">

<span> </span></span></span>

<span data-ttu-id="07f68-105">_**Tópico da última modificação:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="07f68-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="07f68-106">A topologia de referência para pequenas organizações mostra como você pode implantar uma solução robusta e altamente disponível implantando apenas três servidores que executam o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="07f68-106">The reference topology for small organizations shows how you can deploy a robust, highly available solution by deploying only three servers running Lync Server.</span></span>

<span data-ttu-id="07f68-107">**Topologia de referência em pequenas organizações**</span><span class="sxs-lookup"><span data-stu-id="07f68-107">**Reference topology for small organizations**</span></span>

<span data-ttu-id="07f68-108">![Topologia de referência implantando três servidores diagrama](images/Gg398095.25196d0d-dd07-451b-83ba-94c0ddf59030(OCS.15).jpg "Topologia de referência implantando três servidores diagrama")</span><span class="sxs-lookup"><span data-stu-id="07f68-108">![Reference topology deploying three servers diagram](images/Gg398095.25196d0d-dd07-451b-83ba-94c0ddf59030(OCS.15).jpg "Reference topology deploying three servers diagram")</span></span>

  - <span data-ttu-id="07f68-109">**Par de servidores Standard Edition implantados**    Esta organização tem os usuários do 4.000 em seu site central.</span><span class="sxs-lookup"><span data-stu-id="07f68-109">**Pair of Standard Edition Servers Deployed**    This organization has 4,000 users at their central site.</span></span> <span data-ttu-id="07f68-110">A organização implantou dois servidores de edição padrão e os emparelharam para permitir alta disponibilidade e recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="07f68-110">The organization has deployed two Standard Edition servers and paired them together to enable high availability and disaster recovery.</span></span> <span data-ttu-id="07f68-111">Each server homes 2,000 users, but information about all users is synchronized between the two servers.</span><span class="sxs-lookup"><span data-stu-id="07f68-111">Each server homes 2,000 users, but information about all users is synchronized between the two servers.</span></span> <span data-ttu-id="07f68-112">If one goes down, an administrator can fail over those users to be served by the other server, with a minimum of disruption to users.</span><span class="sxs-lookup"><span data-stu-id="07f68-112">If one goes down, an administrator can fail over those users to be served by the other server, with a minimum of disruption to users.</span></span> <span data-ttu-id="07f68-113">Para obter mais informações sobre alta disponibilidade e recursos de recuperação de desastre no Lync Server 2013, consulte [planejando alta disponibilidade e recuperação de desastres no Lync server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="07f68-113">For more information about high availability and disaster recovery features in Lync Server 2013, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span>

  - <span data-ttu-id="07f68-114">**A implantação de um servidor de borda é recomendada.**</span><span class="sxs-lookup"><span data-stu-id="07f68-114">**Edge Server deployment is recommended.**</span></span>   <span data-ttu-id="07f68-115">Embora não seja necessário ter um servidor de borda para mensagens instantâneas internas, presença e conferência, nós o recomendamos até mesmo para pequenas implantações.</span><span class="sxs-lookup"><span data-stu-id="07f68-115">Although deploying an Edge Server is not required for internal IM, presence and conferencing, we recommend it even for small deployments.</span></span> <span data-ttu-id="07f68-116">Você pode maximizar o investimento do Lync Server implantando um servidor de borda para fornecer serviço para os usuários que estão fora de firewalls da sua organização.</span><span class="sxs-lookup"><span data-stu-id="07f68-116">You can maximize your Lync Server investment by deploying an Edge Server to provide service to users currently outside your organization’s firewalls.</span></span> <span data-ttu-id="07f68-117">Veja alguns dos benefícios:</span><span class="sxs-lookup"><span data-stu-id="07f68-117">The benefits include the following:</span></span>
    
      - <span data-ttu-id="07f68-118">Os próprios usuários da sua organização podem usar a funcionalidade do Lync Server, se estiverem trabalhando em casa ou estiverem em trânsito.</span><span class="sxs-lookup"><span data-stu-id="07f68-118">Your organization’s own users can use Lync Server functionality, if they are working from home or are out on the road.</span></span>
    
      - <span data-ttu-id="07f68-119">Os usuários da sua organização poderão convidar outros usuários para reuniões.</span><span class="sxs-lookup"><span data-stu-id="07f68-119">Your users can invite outside users to participate in meetings.</span></span>
    
      - <span data-ttu-id="07f68-120">Se você tiver um parceiro, fornecedor ou organização do cliente que também usa o Lync Server, você pode formar uma *relação federada* com essa organização.</span><span class="sxs-lookup"><span data-stu-id="07f68-120">If you have a partner, vendor or customer organization that also uses Lync Server, you can form a *federated relationship* with that organization.</span></span> <span data-ttu-id="07f68-121">A implantação do Lync Server reconheceria os usuários dessa organização federada, levando a uma melhor colaboração.</span><span class="sxs-lookup"><span data-stu-id="07f68-121">Your Lync Server deployment would then recognize users from that federated organization, leading to better collaboration.</span></span>
    
      - <span data-ttu-id="07f68-122">Seus usuários podem trocar mensagens de chat com usuários de serviços públicos de mensagens de chat, incluindo qualquer um dos itens a seguir ou todos eles: Windows Live, AOL, Yahoo \! e Google Talk.</span><span class="sxs-lookup"><span data-stu-id="07f68-122">Your users can exchange instant messages with users of public IM services, including any or all of the following: Windows Live, AOL, Yahoo\!, and Google Talk.</span></span> <span data-ttu-id="07f68-123">Uma licença separada pode ser necessária para conectividade de IM pública com esses serviços.</span><span class="sxs-lookup"><span data-stu-id="07f68-123">A separate license might be required for public IM connectivity with these services.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <UL>
        > <LI>
        > <P><span data-ttu-id="07f68-124">A partir de 1º de setembro de 2012, a licença de assinatura de usuário da conectividade de mensagem de chat pública do Microsoft Lync ("PIC USL") não está mais disponível para compra de contratos novos ou de renovação.</span><span class="sxs-lookup"><span data-stu-id="07f68-124">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="07f68-125">Os clientes com licenças ativas poderão continuar a federar-se com o Yahoo!</span><span class="sxs-lookup"><span data-stu-id="07f68-125">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="07f68-126">Messenger até a data de encerramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="07f68-126">Messenger until the service shut down date.</span></span> <span data-ttu-id="07f68-127">Uma data de fim da vida útil de junho de 2014 para AOL e Yahoo!</span><span class="sxs-lookup"><span data-stu-id="07f68-127">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="07f68-128">foi anunciado.</span><span class="sxs-lookup"><span data-stu-id="07f68-128">has been announced.</span></span> <span data-ttu-id="07f68-129">Para obter detalhes, consulte <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">suporte para conectividade de mensagens instantâneas públicas no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="07f68-129">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
        > <LI>
        > <P><span data-ttu-id="07f68-130">O PIC USL é uma licença de assinatura por usuário por mês necessária para o Lync Server ou o Office Communications Server se federar com o Yahoo!</span><span class="sxs-lookup"><span data-stu-id="07f68-130">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="07f68-131">Spam.</span><span class="sxs-lookup"><span data-stu-id="07f68-131">Messenger.</span></span> <span data-ttu-id="07f68-132">A capacidade da Microsoft de oferecer esse serviço por meio do suporte do Yahoo!, o contrato subjacente para o qual está prestes a ser enrolado.</span><span class="sxs-lookup"><span data-stu-id="07f68-132">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
        > <LI>
        > <P><span data-ttu-id="07f68-133">Mais do que nunca, o Lync é uma ferramenta poderosa para a conexão entre organizações e pessoas ao redor do mundo.</span><span class="sxs-lookup"><span data-stu-id="07f68-133">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="07f68-134">A Federação com o Windows Live Messenger não requer licenças de usuário/dispositivo adicionais além da CAL padrão do Lync.</span><span class="sxs-lookup"><span data-stu-id="07f68-134">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="07f68-135">A Federação do Skype será adicionada a essa lista, permitindo que os usuários do Lync atinjam centenas de milhões de pessoas com mensagens instantâneas e voz.</span><span class="sxs-lookup"><span data-stu-id="07f68-135">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>

        
        </div>

  - <span data-ttu-id="07f68-136">**Sobrevivência do site de filial.**</span><span class="sxs-lookup"><span data-stu-id="07f68-136">**Branch site survivability.**</span></span>   <span data-ttu-id="07f68-137">Esta organização está executando um programa piloto do recurso Enterprise Voice do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="07f68-137">This organization is running a pilot program of the Enterprise Voice feature of Lync Server.</span></span> <span data-ttu-id="07f68-138">Alguns usuários estão usando o Lync Server como uma única solução de voz.</span><span class="sxs-lookup"><span data-stu-id="07f68-138">Some users are using Lync Server as their sole voice solution.</span></span> <span data-ttu-id="07f68-139">Alguns desses usuários pilotos de voz estão localizados no site da filial.</span><span class="sxs-lookup"><span data-stu-id="07f68-139">Some of these Voice pilot users are located at the branch site.</span></span> <span data-ttu-id="07f68-140">O site de filial não tem um link de rede de longa distância (WAN) confiável para o site central, para que um aparelho de ramificação sobreviventes seja implantado.</span><span class="sxs-lookup"><span data-stu-id="07f68-140">The branch site does not have a reliable wide area network (WAN) link to the central site, so a Survivable Branch Appliance is deployed there.</span></span> <span data-ttu-id="07f68-141">Com essa implantação, mesmo que o link de WAN fique inativo, os usuários do site de filial ainda poderão fazer e receber chamadas (tanto chamadas dentro da organização quanto chamadas PSTN), contar com a funcionalidade de caixa postal e comunicar-se por mensagens instantâneas entre duas partes.</span><span class="sxs-lookup"><span data-stu-id="07f68-141">With this deployed, if the WAN link goes down, users at the branch site can still make and receive calls (both calls within the organization and PSTN calls), have voice mail functionality, and communicate with two-party instant messaging (IM).</span></span> <span data-ttu-id="07f68-142">Os usuários também poderão ser autenticados quando o link de WAN estiver indisponível.</span><span class="sxs-lookup"><span data-stu-id="07f68-142">Users can also be authenticated when the WAN link is unavailable as well.</span></span>

  - <span data-ttu-id="07f68-143">**Implantação de UM do Exchange.**</span><span class="sxs-lookup"><span data-stu-id="07f68-143">**Exchange UM deployment.**</span></span> <span data-ttu-id="07f68-144">Esta topologia de referência inclui um servidor de UM (Unificação de mensagens) do Exchange, que executa o Microsoft Exchange Server, não o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="07f68-144">This reference topology includes an Exchange Unified Messaging (UM) Server, which runs Microsoft Exchange Server, not Lync Server.</span></span>
    
    <span data-ttu-id="07f68-145">Para obter detalhes sobre o Exchange UM, consulte [planejando a integração de Unificação de mensagens do Exchange no Lync server 2013](lync-server-2013-planning-for-exchange-unified-messaging-integration.md) e [integração de Unificação de mensagens do Exchange no Lync Server 2013](lync-server-2013-hosted-exchange-unified-messaging-integration.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="07f68-145">For details about Exchange UM, see [Planning for Exchange Unified Messaging integration in Lync Server 2013](lync-server-2013-planning-for-exchange-unified-messaging-integration.md) and [Hosted Exchange Unified Messaging integration in Lync Server 2013](lync-server-2013-hosted-exchange-unified-messaging-integration.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="07f68-146">**Servidor do Office Web Apps.**</span><span class="sxs-lookup"><span data-stu-id="07f68-146">**Office Web Apps Server.**</span></span> <span data-ttu-id="07f68-147">Recomendamos implantar um servidor ou farm de servidores do Office Web Apps em todas as organizações que usem webconferência.</span><span class="sxs-lookup"><span data-stu-id="07f68-147">We recommend deploying an Office Web Apps Server or Office Web Apps Server farm in every organization that uses web conferencing.</span></span> <span data-ttu-id="07f68-148">O Office Web Apps Server permite que slides do PowerPoint sejam apresentados em conferências Web.</span><span class="sxs-lookup"><span data-stu-id="07f68-148">Office Web Apps Server makes it possible for PowerPoint slides to be presented in web conferences.</span></span> <span data-ttu-id="07f68-149">Para obter mais informações, consulte [Configurando a integração com o servidor do Office Web Apps e o Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="07f68-149">For more information, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

<span data-ttu-id="07f68-150"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="07f68-150"></div>

<span> </span>

</div>

</div>

</span></span></div>

