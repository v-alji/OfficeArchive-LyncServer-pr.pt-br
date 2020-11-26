---
title: 'Lync Server 2013: Recursos de mobilidade'
description: 'Lync Server 2013: recursos e funcionalidades da mobilidade.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mobility features and capabilities
ms:assetid: 12517a88-2531-44a5-bea5-d8884aff53eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh689983(v=OCS.15)
ms:contentKeyID: 48183457
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20713145c18260f22d9635c34af291e9a7c5ea9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445950"
---
# <a name="mobility-features-and-capabilities-in-lync-server-2013"></a><span data-ttu-id="09962-103">Recursos de mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09962-103">Mobility features and capabilities in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09962-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09962-104">

<span> </span></span></span>

<span data-ttu-id="09962-105">_**Tópico da última modificação:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="09962-105">_**Topic Last Modified:** 2013-02-19_</span></span>

    The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="09962-106">O recurso de mobilidade apresentado nas atualizações cumulativas do Lync Server 2013:2013 de fevereiro suporta a funcionalidade do Lync 2010 Mobile e do Lync 2013 para clientes móveis.</span><span class="sxs-lookup"><span data-stu-id="09962-106">The mobility feature introduced in the Cumulative Updates for Lync Server 2013: February 2013 supports Lync 2010 Mobile and Lync 2013 Mobile clients functionality.</span></span> <span data-ttu-id="09962-107">Ao implantar o serviço de mobilidade do Lync Server 2013, os usuários podem usar dispositivos móveis Apple iOS, Android e Windows Phone, ou dispositivos móveis Nokia Symbian para executar atividades como enviar e receber mensagens instantâneas, ver contatos e ver a presença.</span><span class="sxs-lookup"><span data-stu-id="09962-107">When you deploy the Lync Server 2013 Mobility Service, users can use supported Apple iOS, Android, and Windows Phone, or Nokia Symbian mobile devices to perform activities such as sending and receiving instant messages, viewing contacts, and viewing presence.</span></span> <span data-ttu-id="09962-108">Além disso, os dispositivos móveis dão suporte a alguns recursos de voz empresarial, como o clique para ingressar em uma conferência, fazer chamadas pelo trabalho, por um único número, por correio de voz e chamadas perdidas.</span><span class="sxs-lookup"><span data-stu-id="09962-108">In addition, mobile devices support some Enterprise Voice features, such as click to join a conference, Call via Work, single number reach, voice mail, and missed calls.</span></span> <span data-ttu-id="09962-109">Novos recursos apresentados nas atualizações cumulativas do Lync Server 2013: fevereiro de 2013 incluem recurso de voz sobre IP (VoIP) e vídeo (H. 264) para participantes da reunião.</span><span class="sxs-lookup"><span data-stu-id="09962-109">New features introduced in the Cumulative Updates for Lync Server 2013: February 2013 include Voice over IP (VoIP) capability and video (H.264) for meeting attendee.</span></span>

<span data-ttu-id="09962-110">O recurso de mobilidade apresentado nas atualizações cumulativas do Lync Server 2013:2013 de fevereiro suporta a funcionalidade de cliente móvel do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="09962-110">The mobility feature introduced in the Cumulative Updates for Lync Server 2013: February 2013 supports Lync 2013 Mobile client functionality.</span></span> <span data-ttu-id="09962-111">As atualizações cumulativas do Lync Server 2013: fevereiro de 2013 instale a API da Web de comunicação unificada ou UCWA.</span><span class="sxs-lookup"><span data-stu-id="09962-111">The Cumulative Updates for Lync Server 2013: February 2013 install Unified Communications Web API, or UCWA.</span></span> <span data-ttu-id="09962-112">UCWA é o componente usado para clientes móveis do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="09962-112">UCWA is the component used for Lync 2013 Mobile clients.</span></span> <span data-ttu-id="09962-113">No Lync Server 2013, MCX é usado para clientes móveis do Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="09962-113">In Lync Server 2013, Mcx is used for Lync 2010 Mobile clients.</span></span> <span data-ttu-id="09962-114">Atualizações cumulativas do Lync Server 2013:2013 de fevereiro introduz UCWA como o novo ponto de entrada para serviços de mobilidade.</span><span class="sxs-lookup"><span data-stu-id="09962-114">Cumulative Updates for Lync Server 2013: February 2013 introduce UCWA as the new entry point for mobility services.</span></span> <span data-ttu-id="09962-115">O Lync Server 2013 implementa simultaneamente o serviço de mobilidade (MCX), introduzido nas atualizações cumulativas do Lync Server 2010: de novembro de 2011 e fornece suporte para o Lync 2010 Mobile.</span><span class="sxs-lookup"><span data-stu-id="09962-115">Lync Server 2013 concurrently implements the Mobility Service (Mcx), introduced in the Cumulative Updates for Lync Server 2010: November 2011, and provides support for Lync 2010 Mobile.</span></span> <span data-ttu-id="09962-116">Ao implantar as atualizações cumulativas do Lync Server 2013:2013 de fevereiro, os usuários podem usar dispositivos móveis do Windows Phone, Android e Windows Phone compatíveis para executar tais atividades como:</span><span class="sxs-lookup"><span data-stu-id="09962-116">When you deploy the Cumulative Updates for Lync Server 2013: February 2013, users can use supported Apple iOS, Android, and Windows Phone mobile devices to perform such activities as:</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="09962-117">Recursos compatíveis com o serviço de mobilidade nas atualizações cumulativas do Lync Server 2010: novembro de 2011 são observados com (MCX).</span><span class="sxs-lookup"><span data-stu-id="09962-117">Features supported by the Mobility Service from the Cumulative Updates for Lync Server 2010: November 2011 are noted with (Mcx).</span></span> <span data-ttu-id="09962-118">Todos os recursos listados são compatíveis com o UCWA, introduzidos nas atualizações cumulativas do Lync Server 2013:2013 de fevereiro.</span><span class="sxs-lookup"><span data-stu-id="09962-118">All listed features are supported by the UCWA, introduced in the Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

  - <span data-ttu-id="09962-119">Envie e receba mensagens instantâneas (MCX)</span><span class="sxs-lookup"><span data-stu-id="09962-119">Send and receive instant messages (Mcx)</span></span>

  - <span data-ttu-id="09962-120">Exibir presença (MCX)</span><span class="sxs-lookup"><span data-stu-id="09962-120">View presence (Mcx)</span></span>

  - <span data-ttu-id="09962-121">Exibir Contatos (MCX)</span><span class="sxs-lookup"><span data-stu-id="09962-121">View contacts (Mcx)</span></span>

  - <span data-ttu-id="09962-122">Clique para ingressar em uma conferência (MCX)</span><span class="sxs-lookup"><span data-stu-id="09962-122">Click to join a conference (Mcx)</span></span>

  - <span data-ttu-id="09962-123">Ligar por trabalho (MCX)</span><span class="sxs-lookup"><span data-stu-id="09962-123">Call via work (Mcx)</span></span>

  - <span data-ttu-id="09962-124">Alcance de número único (MCX)</span><span class="sxs-lookup"><span data-stu-id="09962-124">Single number reach (Mcx)</span></span>

  - <span data-ttu-id="09962-125">Caixa postal (MCX)</span><span class="sxs-lookup"><span data-stu-id="09962-125">Voice mail (Mcx)</span></span>

  - <span data-ttu-id="09962-126">Notificação de chamada perdida (MCX)</span><span class="sxs-lookup"><span data-stu-id="09962-126">Missed call notification (Mcx)</span></span>

  - <span data-ttu-id="09962-127">Voz sobre IP  (VoIP)</span><span class="sxs-lookup"><span data-stu-id="09962-127">Voice over IP (VoIP)</span></span>

  - <span data-ttu-id="09962-128">Vídeo de participante (H.264)</span><span class="sxs-lookup"><span data-stu-id="09962-128">Attendee video (H.264)</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="09962-129">O Lync 2010 Mobile forneceu um cliente para dispositivos Nokia Symbian.</span><span class="sxs-lookup"><span data-stu-id="09962-129">Lync 2010 Mobile provided a client for Nokia Symbian devices.</span></span> <span data-ttu-id="09962-130">O Lync 2013 Mobile não terá um cliente para dispositivos baseados em Nokia Symbian.</span><span class="sxs-lookup"><span data-stu-id="09962-130">Lync 2013 Mobile will not have a client for Nokia Symbian-based devices.</span></span>



</div>

<span data-ttu-id="09962-131">Os usuários do iPad da Apple terão acesso às funcionalidades aprimoradas.</span><span class="sxs-lookup"><span data-stu-id="09962-131">Apple iPad users will have access to enhanced capabilities.</span></span> <span data-ttu-id="09962-132">Depois de ingressar em uma reunião usando o recurso de retorno de chamada de áudio, um usuário do iPad poderá exibir apresentações carregadas do Microsoft PowerPoint em uma reunião, compartilhar aplicativos e áreas de trabalho, exibir a lista de participantes da reunião e receber notificações de outros tipos de conteúdo que estão sendo compartilhados na reunião.</span><span class="sxs-lookup"><span data-stu-id="09962-132">After joining a meeting by using audio call back, an iPad user will be able to view uploaded Microsoft PowerPoint presentations within a meeting, share applications and desktops, view the meeting participant list, and receive notifications of other content types that are being shared within the meeting.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="09962-133">Com o alcance de um único número, um usuário recebe chamadas em um celular que foram discadas para o número do trabalho.</span><span class="sxs-lookup"><span data-stu-id="09962-133">With single number reach, a user receives calls on a mobile phone that were dialed to the work number.</span></span> <span data-ttu-id="09962-134">Com a chamada por meio do trabalho, o usuário insere uma chamada de saída do cliente móvel Lync usando um número de telefone comercial em vez do número de telefone celular.</span><span class="sxs-lookup"><span data-stu-id="09962-134">With Call via Work, the user places an outbound call from the Lync Mobile client by using a work phone number instead of the mobile phone number.</span></span> <span data-ttu-id="09962-135">Com o dial-out, o cliente envia uma solicitação para MCX ou UCWA (com base na versão do Lync Mobile) para fazer a chamada para ele.</span><span class="sxs-lookup"><span data-stu-id="09962-135">With dial-out, the client sends a request to Mcx or UCWA (based on the Lync Mobile version) to make the call for them.</span></span> <span data-ttu-id="09962-136">O servidor inicia a chamada e, em seguida, chama o usuário de volta no celular.</span><span class="sxs-lookup"><span data-stu-id="09962-136">The server initiates the call and then calls the user back on the mobile phone.</span></span> <span data-ttu-id="09962-137">Quando o usuário atende, o servidor conclui a chamada discando a outra pessoa.</span><span class="sxs-lookup"><span data-stu-id="09962-137">When the user answers, the server completes the call by dialing the other party.</span></span> <span data-ttu-id="09962-138">Ao usar a chamada por meio do trabalho, os usuários podem manter a identidade do trabalho durante uma chamada, o que significa que o destinatário da chamada não vê o número do celular do chamador, e o chamador evita cobranças de chamadas de saída.</span><span class="sxs-lookup"><span data-stu-id="09962-138">By using Call via Work, users can maintain their work identity during a call, which means that the call recipient does not see the caller's mobile number, and the caller avoids incurring outbound calling charges.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="09962-139">Nem todos os recursos funcionam exatamente da mesma forma em todos os dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="09962-139">Not all features work exactly the same on all mobile devices.</span></span> <span data-ttu-id="09962-140">Para obter detalhes sobre os recursos com suporte em dispositivos móveis, consulte as tabelas de comparação de clientes móveis em <A href="https://go.microsoft.com/fwlink/p/?linkid=234777">https://go.microsoft.com/fwlink/p/?LinkId=234777</A> .</span><span class="sxs-lookup"><span data-stu-id="09962-140">For details about features supported on mobile devices, see the Mobile Client Comparison Tables at <A href="https://go.microsoft.com/fwlink/p/?linkid=234777">https://go.microsoft.com/fwlink/p/?LinkId=234777</A>.</span></span> <span data-ttu-id="09962-141">Para obter detalhes sobre dispositivos e sistemas operacionais com suporte, consulte os tópicos de requisitos em <A href="lync-server-2013-planning-for-mobile-clients.md">planejando para clientes móveis no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="09962-141">For details about supported devices and operating systems, see the requirements topics under <A href="lync-server-2013-planning-for-mobile-clients.md">Planning for mobile clients in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="09962-142">Quando você usa o recurso de descoberta automática do Lync Server 2013, os aplicativos móveis podem localizar automaticamente os serviços Web do Lync Server 2013 sem exigir que os usuários insiram manualmente as URLs nas configurações do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09962-142">When you use the Lync Server 2013 Autodiscover feature, mobile applications can automatically locate Lync Server 2013 Web Services without requiring users to manually enter the URLs in their device settings.</span></span> <span data-ttu-id="09962-143">A inserção manual de URLs nas configurações do dispositivo móvel também é suportada, principalmente para fins de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="09962-143">Manually entering URLs in mobile device settings is also supported, primarily for troubleshooting purposes.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="09962-144">Os MCX e UCWA são serviços complementares e ambos são implantados para dar suporte aos clientes móveis do Lync 2010 e Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="09962-144">The Mcx and UCWA are complimentary services and both are deployed to support Lync 2010 Mobile and Lync 2013 Mobile clients.</span></span> <span data-ttu-id="09962-145">O Lync 2013 Mobile não poderá entrar nas implantações do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="09962-145">Lync 2013 Mobile will not be able to sign in to Lync Server 2010 deployments.</span></span> <span data-ttu-id="09962-146">O Lync 2010 móvel e o Lync 2013 Mobile poderão usar uma implantação do Lync Server 2013 com as atualizações cumulativas do Lync Server 2013:2013 de fevereiro aplicado.</span><span class="sxs-lookup"><span data-stu-id="09962-146">Lync 2010 Mobile and Lync 2013 Mobile will be able to use a Lync Server 2013 deployment with the Cumulative Updates for Lync Server 2013: February 2013 applied.</span></span>



</div>

<span data-ttu-id="09962-147">O recurso de mobilidade também oferece suporte a *notificações por push* em dispositivos móveis que não aceitam aplicativos executados em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="09962-147">The mobility feature also supports *push notifications* for mobile devices that do not support applications running in the background.</span></span> <span data-ttu-id="09962-148">Uma notificação por push é uma notificação enviada a um dispositivo móvel sobre um evento que ocorre enquanto o aplicativo móvel está inativo.</span><span class="sxs-lookup"><span data-stu-id="09962-148">A push notification is a notification that is sent to a mobile device about an event that occurs while a mobile application is inactive.</span></span> <span data-ttu-id="09962-149">Por exemplo, um convite perdido de mensagens instantâneas (IM) pode resultar em uma notificação por push.</span><span class="sxs-lookup"><span data-stu-id="09962-149">For example, a missed instant messaging (IM) invitation can result in a push notification.</span></span>

<span data-ttu-id="09962-150">O MCX, o UCWA, o serviço de descoberta automática e o suporte para notificações por push são fornecidos no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="09962-150">Mcx, UCWA, Autodiscover Service, and support for push notifications are provided in Lync Server 2013.</span></span> <span data-ttu-id="09962-151">Recursos de cliente atualizados, recursos e o uso de UCWA como o ponto de entrada da mobilidade são introduzidos nas atualizações cumulativas do Lync Server 2013:2013 de fevereiro.</span><span class="sxs-lookup"><span data-stu-id="09962-151">Updated client features, capabilities, and the use of UCWA as the mobility entry point are introduced in the Cumulative Updates for Lync Server 2013: February 2013.</span></span>

<span data-ttu-id="09962-152"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09962-152"></div>

<span> </span>

</div>

</div>

</span></span></div>

