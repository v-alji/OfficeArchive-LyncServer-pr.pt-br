---
title: Visão geral da Conferência A/V do Lync Server 2013
description: Visão geral da Conferência A/V do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: A/V conferencing overview
ms:assetid: 9583de87-4618-4a99-a47a-45e8cc4cc221
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ619186(v=OCS.15)
ms:contentKeyID: 49733747
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 76ef4f76a4df0187a7c36394b2c95e99876df9be
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439545"
---
# <a name="overview-of-av-conferencing-in-lync-server-2013"></a><span data-ttu-id="5e4b8-103">Visão geral da Conferência A/V no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5e4b8-103">Overview of A/V conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5e4b8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5e4b8-104">

<span> </span></span></span>

<span data-ttu-id="5e4b8-105">_**Tópico da última modificação:** 2012-10-13_</span><span class="sxs-lookup"><span data-stu-id="5e4b8-105">_**Topic Last Modified:** 2012-10-13_</span></span>

<span data-ttu-id="5e4b8-106">A conferência A/V permite comunicações de áudio e vídeo em tempo real entre seus usuários.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-106">A/V conferencing enables real-time audio and video communications between your users.</span></span> <span data-ttu-id="5e4b8-107">Ao implantar uma conferência, você pode optar por habilitar e usar conferências via Web e conferência A/V ou apenas conferências na Web.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-107">When you deploy conferencing, you can choose to enable and use both web conferencing and A/V conferencing, or just web conferencing.</span></span>

<span data-ttu-id="5e4b8-108">Para planejar a conferência A/V, você precisa saber a largura de banda de rede necessária para o tipo de mídia de conferência que sua organização requer.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-108">To plan for A/V conferencing, you need to understand the network bandwidth required by the type of conferencing media that your organization requires.</span></span> <span data-ttu-id="5e4b8-109">Isso pode incluir áudio, vídeo e vídeo panorâmico.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-109">This could include audio, video, and panoramic video.</span></span>

<span data-ttu-id="5e4b8-110">Antes de habilitar usuários para conferência A/V, verifique se sua rede pode manipular a carga resultante.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-110">Before you enable users for A/V conferencing, ensure that your network can handle the resulting load.</span></span> <span data-ttu-id="5e4b8-111">Sem largura de banda suficiente, a experiência do usuário pode ser gravemente prejudicada.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-111">Without sufficient network bandwidth, the user experience may be severely degraded.</span></span> <span data-ttu-id="5e4b8-112">Você pode usar o controle de admissão de chamadas (CAC) para gerenciar a largura de banda de rede usada por uma conferência A/V.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-112">You can use call admission control (CAC) to manage the network bandwidth used by A/V Conferencing.</span></span> <span data-ttu-id="5e4b8-113">Isso é importante para redes restritas, como links limitados de largura de banda entre sites centrais e filiais.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-113">This is important for restricted networks, such as limited bandwidth links between central and branch sites.</span></span> <span data-ttu-id="5e4b8-114">Para obter detalhes, consulte [visão geral do controle de admissão de chamadas no Lync Server 2013](lync-server-2013-overview-of-call-admission-control.md).</span><span class="sxs-lookup"><span data-stu-id="5e4b8-114">For details, see [Overview of call admission control in Lync Server 2013](lync-server-2013-overview-of-call-admission-control.md).</span></span> <span data-ttu-id="5e4b8-115">Para obter detalhes sobre requisitos de largura de banda de mídia, consulte [requisitos de largura de banda de rede para tráfego de mídia no Lync Server 2013](lync-server-2013-network-bandwidth-requirements-for-media-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="5e4b8-115">For details about media bandwidth requirements, see [Network bandwidth requirements for media traffic in Lync Server 2013](lync-server-2013-network-bandwidth-requirements-for-media-traffic.md).</span></span>

<span data-ttu-id="5e4b8-116">Se você implantar uma conferência de áudio na sua rede, os usuários precisarão de dispositivos de áudio, como fones de ouvido, para participar de uma conferência.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-116">If you deploy audio conferencing in your network, your users will need audio devices such as headsets to participate in an audio conference.</span></span> <span data-ttu-id="5e4b8-117">Se você implantar conferência de vídeo, precisará implantar dispositivos de vídeo, como webcams para usuários.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-117">If you deploy video conferencing, you need to deploy video devices, such as webcams for users.</span></span> <span data-ttu-id="5e4b8-118">Recomendamos que você use dispositivos de comunicação unificada (UC) certificados pela Microsoft para todos os tipos de dispositivos, para garantir uma experiência de usuário ideal.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-118">We recommend that you use unified communications (UC) devices that are certified by Microsoft for all device types, to ensure an optimal user experience.</span></span> <span data-ttu-id="5e4b8-119">Para obter detalhes sobre dispositivos certificados pela UC, consulte "telefones e dispositivos para Lync" em [https://go.microsoft.com/fwlink/p/?LinkId=263861](https://go.microsoft.com/fwlink/p/?linkid=263861) .</span><span class="sxs-lookup"><span data-stu-id="5e4b8-119">For details about UC-certified devices, see "Phones and Devices for Lync" at [https://go.microsoft.com/fwlink/p/?LinkId=263861](https://go.microsoft.com/fwlink/p/?linkid=263861).</span></span> <span data-ttu-id="5e4b8-120">Para dispositivos de áudio ou de vídeo, a implantação de dispositivos e o treinamento do usuário são etapas importantes para você considerar e planejar.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-120">For either audio or video devices, device deployment, and user training are important steps for you to consider and plan for.</span></span>

<span data-ttu-id="5e4b8-121">As seções a seguir descrevem os recursos de videoconferência e videoconferência, incluindo informações sobre o gerenciamento de largura de banda e a seleção dos clientes adequados.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-121">The following sections describe the features for audio and video conferencing, including information about managing bandwidth and selecting the appropriate clients.</span></span>

<div>

## <a name="audio-conferencing-features"></a><span data-ttu-id="5e4b8-122">Recursos de conferência de áudio</span><span class="sxs-lookup"><span data-stu-id="5e4b8-122">Audio Conferencing Features</span></span>

<span data-ttu-id="5e4b8-123">O Lync Server 2013 fornece vários recursos que você pode usar para configurar a experiência de audioconferência para o usuário, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5e4b8-123">Lync Server 2013 provides several features that you can use to configure the audio conferencing experience for the user, including the following:</span></span>

  - <span data-ttu-id="5e4b8-124">**Público mudo**   O apresentador pode usar essa configuração para ativar o mudo de todos os participantes de áudio na conferência e colocá-la em um estado em que os não-apresentadores não possam desativar o mudo.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-124">**Audience mute**   The presenter can use this setting to mute all the audio participants in the conference and put the conference in a state where non-presenters cannot unmute themselves.</span></span>

  - <span data-ttu-id="5e4b8-125">**Comunicados de entrada/saída de conferência**   Se você tiver habilitado a conferência discada, os apresentadores poderão usar essa configuração para ativar ou desativar anúncios de entrada e saída para minimizar distrações enquanto uma conferência estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-125">**Conferencing Entry/Exit Announcements**   If you have enabled dial-in conferencing, presenters can use this setting to turn entry and exit announcements on or off to minimize distractions while a conference is in progress.</span></span>

  - <span data-ttu-id="5e4b8-126">**Adicionando um usuário ao discar**   Os apresentadores e os participantes que receberam permissão podem adicionar números PSTN às conferências e fazer com que a conferência disque para esses números.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-126">**Adding a user by dialing out**   Presenters and attendees that have been given permission, can add PSTN numbers to the conferences and have the conference dial-out to those numbers.</span></span>

</div>

<div>

## <a name="video-conferencing-features"></a><span data-ttu-id="5e4b8-127">Recursos de videoconferência</span><span class="sxs-lookup"><span data-stu-id="5e4b8-127">Video Conferencing Features</span></span>

<span data-ttu-id="5e4b8-128">O Lync Server 2013 fornece vários recursos que você pode usar para configurar a experiência de videoconferência para o usuário, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5e4b8-128">Lync Server 2013 provides several features that you can use to configure the video conferencing experience for the user, including the following:</span></span>

  - <span data-ttu-id="5e4b8-129">**Modo de exibição de galeria**   Em videoconferências com mais de duas pessoas, os usuários visualizam automaticamente todas as pessoas na conferência.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-129">**Gallery View**   In video conferences that have more than two people, users automatically see everyone in the conference.</span></span> <span data-ttu-id="5e4b8-130">Se a conferência tiver mais de cinco participantes, o vídeo dos participantes mais ativos serão exibidos na linha superior e apenas a foto dos outros participantes será exibida.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-130">If the conference has more than five participants, the video of the most active participants appear in the top row and only the photo appears for the other participants.</span></span> <span data-ttu-id="5e4b8-131">O vídeo de vários participantes está ativado como padrão.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-131">Multiparty video is turned on by default.</span></span> <span data-ttu-id="5e4b8-132">Para obter detalhes sobre como configurar ou desativar o vídeo de vários participantes, consulte [Configurando a largura de banda do vídeo no Lync Server 2013](lync-server-2013-configuring-video-bandwidth.md).</span><span class="sxs-lookup"><span data-stu-id="5e4b8-132">For details about configuring or turning off multiparty video, see [Configuring video bandwidth in Lync Server 2013](lync-server-2013-configuring-video-bandwidth.md).</span></span>

  - <span data-ttu-id="5e4b8-133">**Vídeo panorâmico**   Se um dispositivo de videoconferência da mesa redonda estiver instalado na sala de conferência, esse recurso fornecerá uma visão completa de 360 graus da sala de conferência.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-133">**Panoramic Video**   If a RoundTable video conferencing device is installed in the conferencing room, this feature provides a full 360 degree view of the conference room.</span></span> <span data-ttu-id="5e4b8-134">A faixa de vídeo panorâmico está disponível apenas com dispositivos RoundTable.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-134">The panoramic video strip is only available with RoundTable devices.</span></span>

  - <span data-ttu-id="5e4b8-135">**Modo de vídeo do apresentador somente**   Os apresentadores podem configurar a reunião para que somente o vídeo do apresentador seja mostrado.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-135">**Presenter only video mode**   Presenters can configure the meeting so that only the video from the presenter is shown.</span></span> <span data-ttu-id="5e4b8-136">Isso evita distrações em reuniões grandes, quando várias transmissões de vídeo estão disponíveis e bloqueadas para diferentes fontes.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-136">This prevents distractions in large meetings when multiple video streams are available and locking to different sources.</span></span> <span data-ttu-id="5e4b8-137">Esse modo também se aplica ao vídeo capturado e fornecido por dispositivos RoundTable.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-137">This mode also applies to video captured and provided by RoundTable devices.</span></span>

  - <span data-ttu-id="5e4b8-138">**Vídeo em HD**   Os usuários podem experimentar resoluções de até HD 1080P em chamadas de dois participantes e em conferências de vários participantes.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-138">**HD video**   Users can experience resolutions up to HD 1080P in two-party calls and multiparty conferences.</span></span>

  - <span data-ttu-id="5e4b8-139">**Vídeo em destaque**   Os apresentadores podem configurar a reunião para que somente o vídeo de um participante selecionado que é uma fonte de vídeo seja visto pelos outros participantes da conferência.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-139">**Video Spotlight**   Presenters can configure the meeting so that only the video from a selected participant who is a video source is seen by the other participants in the conference.</span></span> <span data-ttu-id="5e4b8-140">Esse modo também se aplica ao vídeo capturado e fornecido pelos dispositivos RoundTable para vídeo panorâmico.</span><span class="sxs-lookup"><span data-stu-id="5e4b8-140">This mode also applies to video captured and provided by RoundTable devices for panoramic video.</span></span>

<span data-ttu-id="5e4b8-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5e4b8-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

