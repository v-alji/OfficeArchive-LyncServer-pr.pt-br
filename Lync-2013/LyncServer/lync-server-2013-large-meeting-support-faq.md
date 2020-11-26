---
title: 'Lync Server 2013: perguntas frequentes sobre suporte a reuniões grandes'
description: 'Lync Server 2013: perguntas frequentes de suporte a reuniões grandes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server large meeting support FAQ
ms:assetid: 34b4fb6a-e35c-47e8-8ab1-f8331741fed2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204804(v=OCS.15)
ms:contentKeyID: 48183837
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c8d206400b46fc32a3af7b21ad7d50663e85d069
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426687"
---
# <a name="large-meeting-support-faq-for-lync-server-2013"></a><span data-ttu-id="d457c-103">Perguntas frequentes sobre suporte a reuniões grandes do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d457c-103">Large meeting support FAQ for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d457c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d457c-104">

<span> </span></span></span>

<span data-ttu-id="d457c-105">_**Tópico da última modificação:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="d457c-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="d457c-106">As seções a seguir fornecem respostas a perguntas comuns para criar e executar reuniões grandes.</span><span class="sxs-lookup"><span data-stu-id="d457c-106">The following sections provide answers to common questions for creating and running large meetings.</span></span>

<div>

## <a name="q-how-many-users-can-participate-in-a-large-meeting"></a><span data-ttu-id="d457c-107">P: quantos usuários podem participar de uma reunião grande?</span><span class="sxs-lookup"><span data-stu-id="d457c-107">Q: How many users can participate in a large meeting?</span></span>

<span data-ttu-id="d457c-108">O modelo de usuário do Lync Server especifica os limites de usuários do 250 em um pool compartilhado ou 1000 usuários em um pool dedicado a reuniões grandes, mas esses números representam apenas o número de usuários que testamos e somente para o conjunto específico de hardwares que usamos em nossos testes.</span><span class="sxs-lookup"><span data-stu-id="d457c-108">The Lync Server user model specifies limits of 250 users in a shared pool or 1000 users in a pool dedicated to large meetings, but these numbers only represent the number of users we tested and only for the specific set of hardware that we used in our testing.</span></span> <span data-ttu-id="d457c-109">Com base em nossos testes, recomendamos os limites para os tamanhos máximos.</span><span class="sxs-lookup"><span data-stu-id="d457c-109">Based on our testing, we recommend those limits for maximum sizes.</span></span> <span data-ttu-id="d457c-110">No entanto, você controla o número real de participantes permitidos em reuniões em sua organização Configurando uma ou mais políticas de conferência (que você configura usando cmdlets do Windows PowerShell no Shell de gerenciamento do Lync Server ou usando o painel de controle do Lync Server).</span><span class="sxs-lookup"><span data-stu-id="d457c-110">However, you control the actual number of participants allowed in meetings in your organization by configuring one or more conferencing policies (which you configure using Windows PowerShell cmdlets in the Lync Server Management Shell or using the Lync Server Control Panel).</span></span> <span data-ttu-id="d457c-111">O número que você especificar em uma política de conferência pode ser qualquer número inteiro de 32 bits entre 1 e 4.294.967.295, mas o tamanho recomendado é entre 2 e 250 participantes, inclusive; e o valor padrão é 250.</span><span class="sxs-lookup"><span data-stu-id="d457c-111">The number that you specify in a conferencing policy can be any 32-bit whole number between 1 and 4,294,967,295, but the recommended size is between 2 and 250 participants, inclusive; and the default value is 250.</span></span>

</div>

<div>

## <a name="q-how-many-meetings-or-other-workloads-can-i-have-in-a-pool-that-is-dedicated-to-large-meetings"></a><span data-ttu-id="d457c-112">P: quantas reuniões ou outras cargas de trabalho posso ter em um pool dedicado a reuniões grandes?</span><span class="sxs-lookup"><span data-stu-id="d457c-112">Q: How many meetings or other workloads can I have in a pool that is dedicated to large meetings?</span></span>

<span data-ttu-id="d457c-113">Para garantir a melhor experiência do usuário em reuniões grandes de até 1000 participantes, recomendamos hospedar apenas uma única reunião grande de cada vez em um pool dedicado a reuniões grandes.</span><span class="sxs-lookup"><span data-stu-id="d457c-113">To ensure the best user experience in large meetings of up to 1000 participants, we recommend hosting only a single large meeting at a time on a pool that is dedicated to large meetings.</span></span> <span data-ttu-id="d457c-114">Também recomendamos que você não permita que outras cargas de trabalho sejam executadas nesse pool quando a reunião grande estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="d457c-114">We also recommend not allowing any other workloads to run on that pool when the large meeting is in progress.</span></span>

</div>

<div>

## <a name="q-should-the-organizers-of-large-meeting-be-homed-on-the-dedicated-pool"></a><span data-ttu-id="d457c-115">P: os organizadores de reuniões grandes devem ser hospedados no pool dedicado?</span><span class="sxs-lookup"><span data-stu-id="d457c-115">Q: Should the organizers of large meeting be homed on the dedicated pool?</span></span>

<span data-ttu-id="d457c-116">Não.</span><span class="sxs-lookup"><span data-stu-id="d457c-116">No.</span></span> <span data-ttu-id="d457c-117">Recomendamos não agrupar outros usuários além da equipe dedicada que gerencia o agendamento de reuniões grandes no pool dedicado.</span><span class="sxs-lookup"><span data-stu-id="d457c-117">We recommend not homing any users other than the dedicated staff that manages scheduling of large meetings on the dedicated pool.</span></span> <span data-ttu-id="d457c-118">Isso impede que outro tráfego de comunicação em tempo real cause problemas com reuniões grandes hospedadas no pool.</span><span class="sxs-lookup"><span data-stu-id="d457c-118">This prevents other real-time communications traffic from causing problems with large meetings that are hosted in the pool.</span></span> <span data-ttu-id="d457c-119">Você deve agendar reuniões grandes no pool dedicado usando uma conta de usuário da grande equipe de agendamento de reunião.</span><span class="sxs-lookup"><span data-stu-id="d457c-119">You should schedule large meetings on the dedicated pool using a user account of the large meeting scheduling staff.</span></span> <span data-ttu-id="d457c-120">Você deve adicionar a conta de usuário do organizador da reunião (o usuário que solicita uma reunião grande) como apresentador da reunião grande.</span><span class="sxs-lookup"><span data-stu-id="d457c-120">You should add the user account of the meeting organizer (the user who requests a large meeting) as a presenter for the large meeting.</span></span>

</div>

<div>

## <a name="q-what-media-modalities-can-i-use-in-a-large-meeting"></a><span data-ttu-id="d457c-121">P: quais modalidades de mídia posso usar em uma reunião grande?</span><span class="sxs-lookup"><span data-stu-id="d457c-121">Q: What media modalities can I use in a large meeting?</span></span>

<span data-ttu-id="d457c-122">Reuniões grandes com até 1000 usuários podem incluir áudio, vídeo, compartilhamento do PowerPoint, quadros de comunicações e sondagem de presença.</span><span class="sxs-lookup"><span data-stu-id="d457c-122">Large meetings with up to 1000 users can include audio, video, PowerPoint sharing, whiteboards, and presence polling.</span></span>

</div>

<div>

## <a name="q-can-i-use-group-instant-messaging-im-in-large-meetings"></a><span data-ttu-id="d457c-123">P: posso usar mensagens instantâneas em grupo (IM) em reuniões grandes?</span><span class="sxs-lookup"><span data-stu-id="d457c-123">Q: Can I use group instant messaging (IM) in large meetings?</span></span>

<span data-ttu-id="d457c-124">Sim.</span><span class="sxs-lookup"><span data-stu-id="d457c-124">Yes.</span></span> <span data-ttu-id="d457c-125">No entanto, números grandes de mensagens de chat, especialmente quando enviados por um grande número de participantes da reunião, podem afetar a experiência do usuário devido a problemas com a rolagem rápida de texto na janela de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="d457c-125">However, large numbers of instant messages, especially when sent by a large number of meeting participants, can affect the user experience due to problems with fast text scrolling in the IM window.</span></span> <span data-ttu-id="d457c-126">Fornecendo uma grande quantidade de mensagens de chat para até 1000 os usuários também podem introduzir cargas de servidor significativas, que podem afetar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="d457c-126">Delivering a large amount of instant messages to up to 1000 users can also introduce significant server loads, which can affect performance.</span></span> <span data-ttu-id="d457c-127">Geralmente, as mensagens instantâneas são necessárias somente para perguntas e respostas (p \& as).</span><span class="sxs-lookup"><span data-stu-id="d457c-127">Generally, IM is only required for questions and answers (Q\&As).</span></span>

</div>

<div>

## <a name="can-users-join-large-meetings-by-dialing-in-from-a-phone"></a><span data-ttu-id="d457c-128">Os usuários podem ingressar em reuniões grandes ao discar de um telefone?</span><span class="sxs-lookup"><span data-stu-id="d457c-128">Can users join large meetings by dialing in from a phone?</span></span>

<span data-ttu-id="d457c-129">Sim.</span><span class="sxs-lookup"><span data-stu-id="d457c-129">Yes.</span></span> <span data-ttu-id="d457c-130">Se o pool do Lync Server 2013 estiver adequadamente implantado e habilitado para conferência discada, os usuários poderão ingressar nas reuniões grandes discando.</span><span class="sxs-lookup"><span data-stu-id="d457c-130">If the Lync Server 2013 pool is properly deployed and enabled for dial-in conferencing, users will be able to join the large meetings by dialing in.</span></span> <span data-ttu-id="d457c-131">Nosso teste mostrou que até 15% dos usuários do 1000 podem ingressar na reunião grande durante um período de 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="d457c-131">Our testing has shown that up to 15% of the 1000 users can join the large meeting over a 10 minute period.</span></span>

</div>

<div>

## <a name="q-can-i-host-large-meetings-in-a-virtual-topology"></a><span data-ttu-id="d457c-132">P: é possível hospedar reuniões grandes em uma topologia virtual?</span><span class="sxs-lookup"><span data-stu-id="d457c-132">Q: Can I host large meetings in a virtual topology?</span></span>

<span data-ttu-id="d457c-133">Não testamos reuniões grandes em uma topologia virtual, portanto, não oferecemos suporte ao uso de máquinas virtuais para hospedar um pool dedicado para reuniões grandes.</span><span class="sxs-lookup"><span data-stu-id="d457c-133">We have not tested large meetings in a virtual topology, so we do not support the use of virtual machines to host a dedicated pool for large meetings.</span></span>

<span data-ttu-id="d457c-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d457c-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

