---
title: 'Lync Server 2013: Novidades para clientes'
description: 'Lync Server 2013: o que há de novo para os clientes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: What's new for clients
ms:assetid: 5c144677-4d58-4fc3-8445-74b76c9fcf07
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204933(v=OCS.15)
ms:contentKeyID: 48184253
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 90c1b93666b556c7ce7c4f3d94bea583dbf9b1a1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390031"
---
# <a name="whats-new-for-clients-in-lync-server-2013"></a><span data-ttu-id="81579-103">Novidades para clientes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="81579-103">What's new for clients in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="81579-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="81579-104">

<span> </span></span></span>

<span data-ttu-id="81579-105">_**Tópico da última modificação:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="81579-105">_**Topic Last Modified:** 2013-02-19_</span></span>

<span data-ttu-id="81579-106">O Microsoft Lync 2013 tem uma interface de usuário reprojetada e novos recursos importantes.</span><span class="sxs-lookup"><span data-stu-id="81579-106">Microsoft Lync 2013 has a redesigned user interface and important new features.</span></span> <span data-ttu-id="81579-107">Para administradores, o cliente agora está incluído no programa de instalação do Office, fornecendo uma abordagem mais simplificada para implantar o Office e personalizar clientes em sua organização.</span><span class="sxs-lookup"><span data-stu-id="81579-107">For administrators, the client is now included with the Office setup program, providing a more streamlined approach to deploying Office and customizing clients in your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="81579-108">Para ver uma exibição ilustrada das atualizações da interface do usuário do Lync 2013, consulte "novidades do Lync 2013" em <A href="https://go.microsoft.com/fwlink/?linkid=273885">https://go.microsoft.com/fwlink/?LinkId=273885</A> .</span><span class="sxs-lookup"><span data-stu-id="81579-108">For an illustrated view of Lync 2013 user interface updates, see “What’s New in Lync 2013” at <A href="https://go.microsoft.com/fwlink/?linkid=273885">https://go.microsoft.com/fwlink/?LinkId=273885</A>.</span></span>



</div>

<div>

## <a name="integration-with-office-setup"></a><span data-ttu-id="81579-109">Integração com a instalação do Office</span><span class="sxs-lookup"><span data-stu-id="81579-109">Integration with Office Setup</span></span>

<span data-ttu-id="81579-110">O cliente do Lync 2013 e o suplemento de reunião online do Lync 2013, que dá suporte ao gerenciamento de reuniões, dentro do cliente de mensagens e colaboração do Outlook, agora estão incluídos no programa de instalação do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="81579-110">The Lync 2013 client and the Online Meeting Add-in for Lync 2013—which supports meeting management from within the Outlook messaging and collaboration client—are now both included with the Office 2013 Setup program.</span></span>

<span data-ttu-id="81579-111">Em versões anteriores do Lync e do Office Communicator, você pode usar as propriedades do Windows Installer para personalizar e controlar a instalação do Office.</span><span class="sxs-lookup"><span data-stu-id="81579-111">In previous versions of Lync and Office Communicator, you could use Windows Installer properties to customize and control the Office installation.</span></span> <span data-ttu-id="81579-112">Como o Lync 2013 está integrado à instalação do Office, você pode usar os seguintes métodos para personalizar a configuração do Lync 2013:</span><span class="sxs-lookup"><span data-stu-id="81579-112">Because Lync 2013 is integrated with Office setup, you can use the following methods to customize Lync 2013 setup:</span></span>

  - <span data-ttu-id="81579-113">Usar a OCT (Ferramenta de Personalização do Office)</span><span class="sxs-lookup"><span data-stu-id="81579-113">Use the Office Customization Tool (OCT)</span></span>

  - <span data-ttu-id="81579-114">Usar o Config.xml para executar tarefas de instalação</span><span class="sxs-lookup"><span data-stu-id="81579-114">Use the Config.xml to perform installation tasks</span></span>

  - <span data-ttu-id="81579-115">Usar as opções de Command-Line de configuração</span><span class="sxs-lookup"><span data-stu-id="81579-115">Use Setup Command-Line Options</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="81579-116">O programa de instalação do Lync 2013 não desinstala versões anteriores do Lync ou do Office Communicator.</span><span class="sxs-lookup"><span data-stu-id="81579-116">The Lync 2013 setup program does not uninstall previous versions of Lync or Office Communicator.</span></span> <span data-ttu-id="81579-117">O cliente do Lync 2013 é instalado lado a lado com outros clientes do Lync ou do Office Communicator</span><span class="sxs-lookup"><span data-stu-id="81579-117">The Lync 2013 client installs side-by-side with other Lync or Office Communicator clients</span></span>



</div>

<span data-ttu-id="81579-118">Para obter detalhes, consulte [implantando clientes do Lync no Lync Server 2013](lync-server-2013-deploying-lync-clients.md).</span><span class="sxs-lookup"><span data-stu-id="81579-118">For details, see [Deploying Lync clients in Lync Server 2013](lync-server-2013-deploying-lync-clients.md).</span></span>

</div>

<div>

## <a name="group-policy-deployment"></a><span data-ttu-id="81579-119">Implantação de política de grupo</span><span class="sxs-lookup"><span data-stu-id="81579-119">Group Policy Deployment</span></span>

<span data-ttu-id="81579-120">Como o Lync 2013 agora está incluído no programa de instalação do Office, o método de implantação das configurações da política de grupo do Lync foi alterado.</span><span class="sxs-lookup"><span data-stu-id="81579-120">Because Lync 2013 is now included in Office setup, the method for deploying Lync Group Policy settings has changed.</span></span> <span data-ttu-id="81579-121">Em versões anteriores do Lync e do Office Communicator, você pode usar o Communicator. ADM para definir configurações de política de grupo, enquanto no Lync 2013 agora você pode usar os modelos administrativos do Lync e do ADML fornecidos juntamente com os modelos administrativos de política de grupo do Office.</span><span class="sxs-lookup"><span data-stu-id="81579-121">In previous versions of Lync and Office Communicator, you could use the Communicator.adm to define Group Policy settings, whereas in Lync 2013 you can now use the Lync ADMX and ADML administrative templates that are provided along with the Office Group Policy Administrative Templates.</span></span>

<span data-ttu-id="81579-122">Para obter detalhes, consulte [configurações de política de grupo para o Lync 2013](lync-server-2013-group-policy-settings-for-lync-2013.md).</span><span class="sxs-lookup"><span data-stu-id="81579-122">For details, see [Group Policy settings for Lync 2013](lync-server-2013-group-policy-settings-for-lync-2013.md).</span></span>

</div>

<div>

## <a name="outlook-scheduling-add-in-updates"></a><span data-ttu-id="81579-123">Atualizações do suplemento agendamento do Outlook</span><span class="sxs-lookup"><span data-stu-id="81579-123">Outlook Scheduling Add-in Updates</span></span>

<span data-ttu-id="81579-124">O suplemento reunião online do Lync 2013 inclui a personalização de convites de reunião e as novas opções de reunião.</span><span class="sxs-lookup"><span data-stu-id="81579-124">The Online Meeting Add-in for Lync 2013 includes meeting invite customization and new meeting options.</span></span>

  - <span data-ttu-id="81579-125">Os administradores podem personalizar os convites para reunião da organização adicionando um logotipo personalizado, uma URL de suporte, uma URL de isenção de responsabilidade legal ou texto de rodapé personalizado.</span><span class="sxs-lookup"><span data-stu-id="81579-125">Administrators can customize the organization’s meeting invitations by adding a custom logo, a support URL, a legal disclaimer URL, or custom footer text.</span></span> <span data-ttu-id="81579-126">Para obter detalhes, consulte [Personalizando o suplemento de reunião online no Lync Server 2013](lync-server-2013-customizing-the-online-meeting-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="81579-126">For details, see [Customizing the Online Meeting Add-in in Lync Server 2013](lync-server-2013-customizing-the-online-meeting-add-in.md).</span></span>

  - <span data-ttu-id="81579-127">Novos controles de mudo para participantes permitir que os organizadores da reunião agendem conferências que tenham áudio e vídeo de participantes com mudo ativado por padrão.</span><span class="sxs-lookup"><span data-stu-id="81579-127">New attendee mute controls allow meeting organizers to schedule conferences that have attendee audio and video muted by default.</span></span>

</div>

<div>

## <a name="virtual-desktop-infrastructure-plug-in"></a><span data-ttu-id="81579-128">Plug-in de infraestrutura de área de trabalho virtual</span><span class="sxs-lookup"><span data-stu-id="81579-128">Virtual Desktop Infrastructure Plug-in</span></span>

<span data-ttu-id="81579-129">O cliente Lync 2013 agora dá suporte a áudio e vídeo em um ambiente VDI (infraestrutura de área de trabalho virtual).</span><span class="sxs-lookup"><span data-stu-id="81579-129">The Lync 2013 client now supports audio and video in a Virtual Desktop Infrastructure (VDI) environment.</span></span> <span data-ttu-id="81579-130">Um usuário pode conectar um dispositivo de áudio ou de vídeo (por exemplo, um fone de ouvido com microfone ou uma câmera) ao computador local (por exemplo, um cliente leve ou um computador redefinido).</span><span class="sxs-lookup"><span data-stu-id="81579-130">A user can connect an audio or video device (for example, a headset or a camera) to the local computer (for example, a thin client or repurposed computer).</span></span> <span data-ttu-id="81579-131">O usuário pode se conectar à máquina virtual, entrar no cliente do Lync 2013 que está em execução na máquina virtual e participar de comunicações de áudio e vídeo em tempo real, como se o cliente estivesse em execução localmente.</span><span class="sxs-lookup"><span data-stu-id="81579-131">The user can connect to the virtual machine, sign in to the Lync 2013 client that is running on the virtual machine, and participate in real-time audio and video communication as though the client is running locally.</span></span> <span data-ttu-id="81579-132">Os recursos a seguir são suportados em um ambiente de área de trabalho virtual:</span><span class="sxs-lookup"><span data-stu-id="81579-132">The following features are supported in a virtual desktop environment:</span></span>

  - <span data-ttu-id="81579-133">Integração de dispositivos para áudio e vídeo, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="81579-133">Device integration for audio and video, including the following:</span></span>
    
      - <span data-ttu-id="81579-134">Controles de chamada do dispositivo</span><span class="sxs-lookup"><span data-stu-id="81579-134">Call controls from the device</span></span>
    
      - <span data-ttu-id="81579-135">Integração de presença no dispositivo</span><span class="sxs-lookup"><span data-stu-id="81579-135">Presence integration on the device</span></span>
    
      - <span data-ttu-id="81579-136">Suporte a vários HID (dispositivo de interface humana)</span><span class="sxs-lookup"><span data-stu-id="81579-136">Multiple HID (human interface device) support</span></span>

  - <span data-ttu-id="81579-137">Suporte a locais e serviços de emergência.</span><span class="sxs-lookup"><span data-stu-id="81579-137">Location and emergency services support.</span></span>

  - <span data-ttu-id="81579-138">Suporte para todas as modalidades do Lync, incluindo mensagens instantâneas, áudio, vídeo, compartilhamento de aplicativos, compartilhamento de área de trabalho, compartilhamento do PowerPoint, quadro de comunicações e transferência de arquivos.</span><span class="sxs-lookup"><span data-stu-id="81579-138">Support for all Lync modalities, including IM, audio, video, application sharing, desktop sharing, PowerPoint sharing, whiteboard, and file transfer.</span></span>

  - <span data-ttu-id="81579-139">Suporte a áudio e vídeo em chamadas de pessoa para pessoa e chamadas em conferência.</span><span class="sxs-lookup"><span data-stu-id="81579-139">Audio and video support in person-to-person calls and conference calls.</span></span>

<span data-ttu-id="81579-140">Para obter informações sobre a implantação do plug-in VDI, consulte [implantação do plug-in VDI do Lync no Lync Server 2013](lync-server-2013-deploying-the-lync-vdi-plug-in.md).</span><span class="sxs-lookup"><span data-stu-id="81579-140">For information about deploying the VDI plug-in, see [Deploying the Lync VDI plug-in in Lync Server 2013](lync-server-2013-deploying-the-lync-vdi-plug-in.md).</span></span>

</div>

<div>

## <a name="video-enhancements"></a><span data-ttu-id="81579-141">Melhorias de vídeo</span><span class="sxs-lookup"><span data-stu-id="81579-141">Video Enhancements</span></span>

<span data-ttu-id="81579-142">Vários novos recursos melhoram significativamente a experiência com vídeo para participantes de conferências.</span><span class="sxs-lookup"><span data-stu-id="81579-142">Several new features significantly enhance the video experience for conference participants.</span></span>

  - <span data-ttu-id="81579-143">Vídeo aprimorado com detecção de rosto e enquadramento inteligente, para que o vídeo de um participante se movimente para ajudar a mantê-los centralizados no quadro.</span><span class="sxs-lookup"><span data-stu-id="81579-143">Video is enhanced with face detection and smart framing, so that a participant’s video moves to help keep them centered in the frame.</span></span>

  - <span data-ttu-id="81579-144">O vídeo de alta definição agora é compatível com chamadas de dois participantes e conferências de vários participantes.</span><span class="sxs-lookup"><span data-stu-id="81579-144">High-definition video is now supported in two-party calls and multiparty conferences.</span></span> <span data-ttu-id="81579-145">Os usuários podem experimentar resoluções de até HD 1080P.</span><span class="sxs-lookup"><span data-stu-id="81579-145">Users can experience resolutions up to HD 1080P.</span></span>

  - <span data-ttu-id="81579-146">Os participantes podem selecionar um layout de reunião diferente: o modo de exibição de galeria mostra as imagens ou vídeos dos participantes; O modo de exibição do orador mostra o conteúdo da reunião e somente o vídeo ou a imagem atual do orador; Modo de exibição de apresentação mostra o conteúdo da reunião somente; O modo de exibição compacto mostra apenas os controles da reunião.</span><span class="sxs-lookup"><span data-stu-id="81579-146">Participants can select from different meeting layouts: Gallery View shows all participants’ pictures or videos; Speaker View shows the meeting content and only the current speaker’s video or picture; Presentation View shows meeting content only; Compact View shows just the meeting controls.</span></span>

  - <span data-ttu-id="81579-147">Com o novo recurso de galeria, os participantes podem ver várias alimentações de vídeo ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="81579-147">With the new Gallery feature, participants can see multiple video feeds at the same time.</span></span> <span data-ttu-id="81579-148">Se a conferência tiver mais de cinco participantes, as alimentações de vídeo apenas dos participantes ativos serão exibidos na linha superior e as imagens serão exibidas para os outros participantes.</span><span class="sxs-lookup"><span data-stu-id="81579-148">If the conference has more than five participants, video feeds of only the most active participants appear in the top row, and pictures appear for the other participants.</span></span>

  - <span data-ttu-id="81579-149">Os participantes podem usar a fixação de vídeo para selecionar um ou mais dos feeds de vídeo disponíveis para ficarem visíveis o tempo todo.</span><span class="sxs-lookup"><span data-stu-id="81579-149">Participants can use video pinning to select one or more of the available video feeds to be visible at all times.</span></span>

  - <span data-ttu-id="81579-150">Os apresentadores podem usar o recurso de Spotlight em vídeo para selecionar o feed de vídeo de uma pessoa para que todos os participantes da reunião vejam apenas esse participante.</span><span class="sxs-lookup"><span data-stu-id="81579-150">Presenters can use the Video Spotlight feature to select one person’s video feed so that every participant in the meeting sees that participant only.</span></span>

</div>

<div>

## <a name="chat-room-integration"></a><span data-ttu-id="81579-151">Integração da sala de chat</span><span class="sxs-lookup"><span data-stu-id="81579-151">Chat Room Integration</span></span>

<span data-ttu-id="81579-152">O Lync 2013 agora integra os recursos fornecidos anteriormente pelo Lync 2010 Group Chat.</span><span class="sxs-lookup"><span data-stu-id="81579-152">Lync 2013 now integrates the features previously provided by Lync 2010 Group Chat.</span></span> <span data-ttu-id="81579-153">Um cliente de chat em grupo separado não é mais necessário.</span><span class="sxs-lookup"><span data-stu-id="81579-153">A separate group chat client is no longer required.</span></span>

  - <span data-ttu-id="81579-154">De dentro do Lync 2013, os usuários podem procurar salas de chat, adicionar salas de chat a seus contatos, monitorar a atividade de salas de chat e ler e postar mensagens.</span><span class="sxs-lookup"><span data-stu-id="81579-154">From within Lync 2013, users can search for chat rooms, add chat rooms to their contacts, monitor chat room activity, and read and post messages.</span></span>

  - <span data-ttu-id="81579-155">Os usuários podem criar feeds de tópico para que sejam notificados se alguém em uma das salas de chat adicionar uma postagem contendo palavras-chave específicas.</span><span class="sxs-lookup"><span data-stu-id="81579-155">Users can create topic feeds so that they’ll be notified if someone in one of their chat rooms adds a post containing specific keywords.</span></span>

  - <span data-ttu-id="81579-156">Com a nova página de opções de **chat persistente** , os usuários podem definir alertas de notificação e sons que se aplicam quando as pessoas publicam mensagens em suas salas de chat.</span><span class="sxs-lookup"><span data-stu-id="81579-156">With the new **Persistent Chat** options page, users can set notification alerts and sounds that apply when people post messages to their chat rooms.</span></span>

</div>

<div>

## <a name="lync-web-app-updates"></a><span data-ttu-id="81579-157">Atualizações do Lync Web App</span><span class="sxs-lookup"><span data-stu-id="81579-157">Lync Web App Updates</span></span>

<span data-ttu-id="81579-158">O Lync Web App é o cliente de conferência baseado na Web para reuniões do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="81579-158">Lync Web App is the web-based conferencing client for Lync Server 2013 meetings.</span></span> <span data-ttu-id="81579-159">Nesta versão, a adição de áudio e vídeo do computador ao Lync Web App oferece uma experiência completa na reunião para qualquer pessoa que não tenha um cliente do Lync instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="81579-159">In this release, the addition of computer audio and video to Lync Web App provides a complete in-meeting experience for anyone who doesn’t have a Lync client installed locally.</span></span> <span data-ttu-id="81579-160">Os participantes de reunião têm acesso a todos os recursos de colaboração e compartilhamento e aos controles de reunião do apresentador.</span><span class="sxs-lookup"><span data-stu-id="81579-160">Meeting participants have access to all collaboration and sharing features and presenter meeting controls.</span></span>

<span data-ttu-id="81579-161">Quando um usuário tenta ingressar em uma reunião, mas não tem um cliente instalado localmente, o Lync Web App é aberto.</span><span class="sxs-lookup"><span data-stu-id="81579-161">When a user tries to join a meeting but doesn’t have a locally installed client, Lync Web App opens.</span></span> <span data-ttu-id="81579-162">Se quiser permitir opções adicionais para ingressar na reunião, você pode configurar a página ingressar na reunião; consulte [Configurando a página ingressar na reunião no Lync Server 2013](lync-server-2013-configuring-the-meeting-join-page.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="81579-162">If you want to allow additional options for joining the meeting, you can configure the Meeting Join page; see [Configuring the meeting join page in Lync Server 2013](lync-server-2013-configuring-the-meeting-join-page.md) in the Deployment documentation.</span></span>

<span data-ttu-id="81579-163">Devido aos aprimoramentos do Lync Web App, uma versão atualizada do participante não está disponível para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="81579-163">Because of the enhancements to Lync Web App, an updated version of Attendee isn’t available for Lync Server 2013.</span></span> <span data-ttu-id="81579-164">O Lync Web App é o cliente escolhido para participantes de fora da sua organização.</span><span class="sxs-lookup"><span data-stu-id="81579-164">Lync Web App is the client of choice for participants outside your organization.</span></span> <span data-ttu-id="81579-165">Não é necessária nenhuma instalação de cliente local, embora os recursos de áudio, vídeo e compartilhamento exijam que um plug-in seja instalado na primeira utilização.</span><span class="sxs-lookup"><span data-stu-id="81579-165">No local client installation is required, although audio, video, and sharing features require a plug-in to be installed at first use.</span></span>

</div>

<div>

## <a name="lync-2013-for-mobile-clients-updates"></a><span data-ttu-id="81579-166">Lync 2013 para atualizações de clientes móveis</span><span class="sxs-lookup"><span data-stu-id="81579-166">Lync 2013 for Mobile Clients Updates</span></span>

<span data-ttu-id="81579-167">Além de recursos avançados de presença, contatos e mensagens instantâneas, agora os clientes móveis do Lync 2013 fornecem chamadas de voz e vídeo pela Internet e conexões de dados da rede celular.</span><span class="sxs-lookup"><span data-stu-id="81579-167">In addition to enhanced presence, contacts, and IM capabilities, Lync 2013 mobile clients now provide voice and video calling over the Internet and cellular data connections.</span></span> <span data-ttu-id="81579-168">Com um único toque do link da reunião em um item de calendário, os usuários móveis podem ingressar em reuniões com voz e vídeo do Lync.</span><span class="sxs-lookup"><span data-stu-id="81579-168">With a single tap of the meeting link in a calendar item, mobile users can join Lync voice and video meetings.</span></span> <span data-ttu-id="81579-169">Para obter mais informações sobre clientes móveis do Lync 2013, consulte [planejando para clientes móveis no Lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span><span class="sxs-lookup"><span data-stu-id="81579-169">For more information about Lync 2013 mobile clients, see [Planning for mobile clients in Lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span></span>

</div>

<div>

## <a name="lync-2013-user-interface-updates"></a><span data-ttu-id="81579-170">Atualizações da interface do usuário do Lync 2013</span><span class="sxs-lookup"><span data-stu-id="81579-170">Lync 2013 User Interface Updates</span></span>

<div>

## <a name="accessibility-updates"></a><span data-ttu-id="81579-171">Atualizações de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="81579-171">Accessibility Updates</span></span>

<span data-ttu-id="81579-172">O Lync 2013 incorpora vários novos recursos de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="81579-172">Lync 2013 incorporates several new accessibility features.</span></span>

  - <span data-ttu-id="81579-173">O Lync 2013 suporta resolução de alta DPI, permitindo que os usuários dimensionem o texto e os elementos gráficos para 125% e 150% de pontos por polegada.</span><span class="sxs-lookup"><span data-stu-id="81579-173">Lync 2013 supports high DPI resolution, enabling users to scale text and graphics for 125% and 150% dots per inch.</span></span>

  - <span data-ttu-id="81579-174">O Lync fornece suporte de alto contraste para que a interface do usuário permaneça totalmente funcional quando usada com temas de alto contraste no Windows.</span><span class="sxs-lookup"><span data-stu-id="81579-174">Lync provides high-contrast support so that the user interface remains fully functional when used with high contrast themes in Windows.</span></span>

  - <span data-ttu-id="81579-175">O Lync oferece mais de 100 atalhos de teclado para que os usuários possam acessar funções importantes sem um mouse.</span><span class="sxs-lookup"><span data-stu-id="81579-175">Lync offers more than 100 keyboard shortcuts so that users can access important functions without a mouse.</span></span> <span data-ttu-id="81579-176">Por exemplo, os usuários podem pressionar Alt + C para aceitar uma chamada ou ALT + I para ignorá-la, sem precisar fazer a Tabulação ou definir o foco.</span><span class="sxs-lookup"><span data-stu-id="81579-176">For example, users can press Alt+C to accept a call, or Alt + I to ignore it, without having to tab or set the focus.</span></span> <span data-ttu-id="81579-177">Pressionar (ALT + Q) Finaliza uma chamada, (Ctrl + N) inicia o OneNote e (Alt + T) abre o menu ferramentas.</span><span class="sxs-lookup"><span data-stu-id="81579-177">Pressing (Alt+Q) ends a call, (Ctrl+N) starts OneNote, and (Alt+T) opens the Tools menu.</span></span>

  - <span data-ttu-id="81579-178">O suporte a leitor de tela extensivo no Lync 2013 garante que todas as notificações, solicitações de entrada e mensagens instantâneas sejam lidas em voz alta quando um leitor de tela estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="81579-178">Extensive screen reader support in Lync 2013 ensures that all notifications, incoming requests, and instant messages are read aloud when a screen reader is enabled.</span></span>

</div>

<div>

## <a name="presence-while-sharing"></a><span data-ttu-id="81579-179">Presença durante o compartilhamento</span><span class="sxs-lookup"><span data-stu-id="81579-179">Presence While Sharing</span></span>

<span data-ttu-id="81579-180">Quando o Lync detecta que um usuário está compartilhando, o Lync atribui automaticamente ao usuário um status de presença apresentando.</span><span class="sxs-lookup"><span data-stu-id="81579-180">When Lync detects that a user is sharing, Lync automatically assigns the user a Presenting presence status.</span></span> <span data-ttu-id="81579-181">Esse status bloqueia todas as comunicações de entrada, a menos que o remetente tenha atribuído a relação de privacidade do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="81579-181">This status blocks all incoming communications unless the sender is assigned the Workgroup privacy relationship.</span></span> <span data-ttu-id="81579-182">Se o usuário estiver usando o recurso de compartilhamento totalmente em um monitor secundário, o Lync não atribuirá um status de presença de apresentação.</span><span class="sxs-lookup"><span data-stu-id="81579-182">If the user is using the sharing feature entirely on a secondary monitor, Lync does not assign a Presenting presence status.</span></span>

</div>

<div>

## <a name="conversation-window-updates"></a><span data-ttu-id="81579-183">Atualizações da janela de conversa</span><span class="sxs-lookup"><span data-stu-id="81579-183">Conversation Window Updates</span></span>

<span data-ttu-id="81579-184">A janela de conversa reformulada fornece acesso mais rápido a recursos importantes.</span><span class="sxs-lookup"><span data-stu-id="81579-184">The redesigned Conversation window provides quicker access to important features.</span></span>

  - <span data-ttu-id="81579-185">Com o novo recurso conversas com guias, os usuários agora podem manter todas as salas de chat e chats em uma janela de conversa.</span><span class="sxs-lookup"><span data-stu-id="81579-185">With the new tabbed conversations feature, users can now keep all their IMs and chat rooms in one Conversation window.</span></span> <span data-ttu-id="81579-186">As guias no lado esquerdo da janela de conversa permitem que os usuários naveguem facilmente entre todas as conversas ativas.</span><span class="sxs-lookup"><span data-stu-id="81579-186">The tabs along the left side of the Conversation window let users navigate easily among all active conversations.</span></span>

  - <span data-ttu-id="81579-187">Os usuários podem mostrar uma conversa individual em uma janela separada e, em seguida, redimensionar a janela.</span><span class="sxs-lookup"><span data-stu-id="81579-187">Users can pop out an individual conversation into a separate window, and then resize the window.</span></span> <span data-ttu-id="81579-188">Eles também podem retornar a janela de volta à janela de conversa principal.</span><span class="sxs-lookup"><span data-stu-id="81579-188">They can also pop the window back into the main Conversation window.</span></span>

  - <span data-ttu-id="81579-189">O Lync 2013 reabre as conversas de um usuário quando o usuário se desconecta e entra novamente no Lync.</span><span class="sxs-lookup"><span data-stu-id="81579-189">Lync 2013 reopens a user’s conversations when the user signs out and signs back in to Lync.</span></span>

  - <span data-ttu-id="81579-190">Os usuários podem adicionar rapidamente mensagens instantâneas, vídeo, compartilhamento de programas, compartilhamento de área de trabalho ou ferramentas de Webconferência (quadro de comunicações, anotações da reunião, blocos de anotações compartilhados e anexos) a qualquer conversa.</span><span class="sxs-lookup"><span data-stu-id="81579-190">Users can quickly add IM, video, program sharing, desktop sharing, or web conferencing tools (whiteboard, meeting notes, shared notebooks, and attachments) to any conversation.</span></span>

  - <span data-ttu-id="81579-191">Em uma reunião na qual um vídeo ou conteúdo está sendo compartilhado, os usuários podem exibir o vídeo da reunião ou o conteúdo compartilhado e, em seguida, redimensionar a janela.</span><span class="sxs-lookup"><span data-stu-id="81579-191">In a meeting where video or content is being shared, users can pop out the meeting video or shared content, and then resize the window.</span></span>

</div>

<div>

## <a name="lync-main-window-updates"></a><span data-ttu-id="81579-192">Atualizações da janela principal do Lync</span><span class="sxs-lookup"><span data-stu-id="81579-192">Lync Main Window Updates</span></span>

<span data-ttu-id="81579-193">A nova aparência simplificada retém recursos conhecidos, como o **que está acontecendo hoje?** , o seletor de status e o seletor de **local definir seu local** .</span><span class="sxs-lookup"><span data-stu-id="81579-193">The new streamlined look retains familiar features such as the **What’s happening today?** note field, the status selector, and the **Set Your Location** selector.</span></span>

  - <span data-ttu-id="81579-194">Quando salas de chat estiverem habilitadas, os usuários verão um novo ícone de **salas de chat** na página principal do Lync.</span><span class="sxs-lookup"><span data-stu-id="81579-194">When chat rooms are enabled, users see a new **Chat Rooms** icon on the main Lync page.</span></span> <span data-ttu-id="81579-195">Com o ícone de **salas de chat** , os usuários podem acessar rapidamente seus respectivos filtros e salas de chat.</span><span class="sxs-lookup"><span data-stu-id="81579-195">With the **Chat Rooms** icon, users can quickly access their chat rooms and filters.</span></span>

  - <span data-ttu-id="81579-196">Os usuários podem clicar nos ícones de exibição para alternar para o modo de exibição **contatos** , o modo de exibição **salas de chat** , o modo de exibição **conversas** ou o modo de exibição **telefone**</span><span class="sxs-lookup"><span data-stu-id="81579-196">Users can click the view icons to switch to the **Contacts** view, **Chat Rooms** view, **Conversations** view, or **Phone** view.</span></span>

  - <span data-ttu-id="81579-197">Se os usuários foram migrados para o Exchange 2013, eles podem carregar uma imagem de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="81579-197">If users have been migrated to Exchange 2013, they can upload a high resolution picture.</span></span>

</div>

<div>

## <a name="contacts-view-and-contact-card-updates"></a><span data-ttu-id="81579-198">Modo de exibição contatos e atualizações de cartão de contato</span><span class="sxs-lookup"><span data-stu-id="81579-198">Contacts View and Contact Card Updates</span></span>

<span data-ttu-id="81579-199">O Lync 2013 oferece aos usuários diferentes maneiras de exibir contatos e grupos no modo de exibição **contatos** .</span><span class="sxs-lookup"><span data-stu-id="81579-199">Lync 2013 gives users different ways to view contacts and groups in their **Contacts** view.</span></span>

  - <span data-ttu-id="81579-200">Com o novo repositório de contatos unificado, após a migração dos contatos do Lync dos usuários para o Exchange 2013, os usuários podem acessar e gerenciar seus contatos no Lync 2013, no Outlook ou no Outlook Web App, e seus favoritos ficam sincronizados.</span><span class="sxs-lookup"><span data-stu-id="81579-200">With the new unified contact store, after users' Lync contacts are migrated to Exchange 2013, the users can access and manage their contacts from Lync 2013, Outlook, or Outlook Web App, and their Favorites stay synchronized.</span></span> <span data-ttu-id="81579-201">Por exemplo, se um usuário adicionar um contato aos favoritos no Outlook, o contato aparecerá no grupo favoritos no Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="81579-201">For example, if a user adds a contact to Favorites in Outlook, the contact appears in the Favorites group in Lync 2013.</span></span>

  - <span data-ttu-id="81579-202">Se você adicionou e configurou o proxy XMPP e o Gateway XMPP, os usuários podem adicionar contatos de parceiros baseados no XMPP para mensagens instantâneas e presença.</span><span class="sxs-lookup"><span data-stu-id="81579-202">If you have added and configured the XMPP proxy and XMPP gateway, users can add contacts from XMPP-based partners for instant messaging and presence.</span></span>

  - <span data-ttu-id="81579-203">Um novo recurso **Adicionar um contato que não está em minha organização** proporciona aos usuários uma maneira fácil de adicionar pessoas de fora da organização.</span><span class="sxs-lookup"><span data-stu-id="81579-203">A new **Add a Contact That’s Not in My Organization** feature gives users an easy way to add people who are external to the organization.</span></span>

  - <span data-ttu-id="81579-204">Um novo grupo **favoritos** permite que os usuários criem uma lista de pessoas que os usuários contatam com mais frequência para obter um acesso mais rápido.</span><span class="sxs-lookup"><span data-stu-id="81579-204">A new **Favorites** group lets users build a list of people users contact most often for quicker access.</span></span>

  - <span data-ttu-id="81579-205">Os usuários podem usar a nova página Opções da **lista de contatos** para escolher como os usuários desejam classificar e exibir contatos.</span><span class="sxs-lookup"><span data-stu-id="81579-205">Users can use the new **Contacts List** options page to choose how users want to sort and display contacts.</span></span> <span data-ttu-id="81579-206">Os usuários podem selecionar uma exibição expandida de duas linhas que mostre as imagens dos contatos ou uma exibição condensada de uma linha.</span><span class="sxs-lookup"><span data-stu-id="81579-206">Users can select an expanded, two-line view that shows contacts’ pictures, or a condensed one-line view.</span></span> <span data-ttu-id="81579-207">Os usuários também podem classificar os contatos em ordem alfabética ou por disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="81579-207">Users can also sort contacts alphabetically or by availability.</span></span>

</div>

<div>

## <a name="conferencing-updates"></a><span data-ttu-id="81579-208">Atualizações de conferência</span><span class="sxs-lookup"><span data-stu-id="81579-208">Conferencing Updates</span></span>

<span data-ttu-id="81579-209">O Lync 2013 oferece vários aprimoramentos em recursos de conferência.</span><span class="sxs-lookup"><span data-stu-id="81579-209">Lync 2013 offers several enhancements to conferencing features.</span></span>

  - <span data-ttu-id="81579-210">Dependendo do tipo de reunião, os usuários podem agora ativar o mudo da audiência e permitir ou bloquear o compartilhamento de vídeo ao agendar a reunião.</span><span class="sxs-lookup"><span data-stu-id="81579-210">Depending on the type of meeting, users can now mute the audience and allow or block video sharing when scheduling the meeting.</span></span> <span data-ttu-id="81579-211">Essas opções estão disponíveis na página **Opções de reunião** e são recomendadas para reuniões grandes com mais de 20 participantes.</span><span class="sxs-lookup"><span data-stu-id="81579-211">These options are available on the **Meeting Options** page and are recommended for large meetings with more than 20 participants.</span></span>

  - <span data-ttu-id="81579-212">Os controles de áudio fáceis de usar na sala de reuniões permitem que o usuário controle opções de áudio, como ativar mudo, desativar mudo, alterar dispositivo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="81579-212">Easy to use audio controls in the meeting room allow the user to control audio options, such as mute, unmute, change device, and so on.</span></span>

  - <span data-ttu-id="81579-213">Ao compartilhar programas, os usuários podem selecionar vários programas para compartilhar se precisarem trabalhar com mais de um programa.</span><span class="sxs-lookup"><span data-stu-id="81579-213">When sharing programs, users can select multiple programs to share if they need to work with more than one program.</span></span>

  - <span data-ttu-id="81579-214">Agora os usuários podem carregar apresentações que contenham clipes de vídeo carregando o arquivo do PowerPoint e apontando o mouse sobre o slide para exibir controles de vídeo, como controles de reprodução, pausa e áudio.</span><span class="sxs-lookup"><span data-stu-id="81579-214">Users can now upload presentations that contain video clips by uploading the PowerPoint file, and pointing the mouse over the slide to display video controls, such as play, pause, and audio controls.</span></span>

  - <span data-ttu-id="81579-215">Durante uma reunião, os usuários podem mesclar outra conversa aberta na reunião usando **mesclar esta chamada** no menu **mais opções** (**...**).</span><span class="sxs-lookup"><span data-stu-id="81579-215">While in a meeting, users can merge another open conversation into the meeting by using **Merge This Call Into** on the **More Options** (**…**) menu.</span></span>

  - <span data-ttu-id="81579-216">Para ver os nomes dos participantes, os usuários podem focalizar o mouse sobre o botão **Exibir participantes** ou clicar em **Mostrar lista de participantes** para encaixar o painel na reunião.</span><span class="sxs-lookup"><span data-stu-id="81579-216">To see the participants’ names, users can hover the mouse over the **View Participants** button, or click **Show Participant List** to dock the panel in the meeting.</span></span>

  - <span data-ttu-id="81579-217">Dependendo do tipo de reunião, os usuários podem selecionar entre vários modos de exibição de conteúdo e de participantes diferentes.</span><span class="sxs-lookup"><span data-stu-id="81579-217">Depending on the meeting type, users can select from several different content and participant views.</span></span>

  - <span data-ttu-id="81579-218">As gravações de reunião são salvas automaticamente em um formato que é reproduzido no Windows Media Player (MP4).</span><span class="sxs-lookup"><span data-stu-id="81579-218">Meeting recordings are automatically saved in a format that plays in Windows Media Player (MP4).</span></span> <span data-ttu-id="81579-219">Os usuários podem compartilhar facilmente o arquivo com qualquer pessoa ou usar o recurso **publicar** no Gerenciador de gravação para postar a gravação em um local compartilhado.</span><span class="sxs-lookup"><span data-stu-id="81579-219">Users can easily share the file with anyone, or use the **Publish** feature in recording manager to post the recording on a shared location.</span></span>

  - <span data-ttu-id="81579-220">O OneNote permite novas maneiras de colaborar em uma reunião.</span><span class="sxs-lookup"><span data-stu-id="81579-220">OneNote enables new ways to collaborate in a meeting.</span></span> <span data-ttu-id="81579-221">Durante uma reunião, os usuários podem fazer anotações com o OneNote para uso pessoal após a reunião ou usar blocos de anotações compartilhados e coedição com participantes da reunião em tempo real.</span><span class="sxs-lookup"><span data-stu-id="81579-221">During a meeting, users can take notes with OneNote for personal use after the meeting, or use shared notebooks and co-edit with meeting participants in real time.</span></span> <span data-ttu-id="81579-222">Todos os membros da equipe podem acessar as anotações compartilhadas em informações do Contribute, ideias ou usar as páginas do bloco de anotações como um quadro de comunicações virtual.</span><span class="sxs-lookup"><span data-stu-id="81579-222">All team members can access the shared notes to contribute information, brainstorm ideas, or use the notebook pages as a virtual whiteboard.</span></span> <span data-ttu-id="81579-223">As pessoas e o conteúdo compartilhado na reunião são adicionados automaticamente às anotações.</span><span class="sxs-lookup"><span data-stu-id="81579-223">People and content shared in the meeting are automatically added to the Notes.</span></span>

  - <span data-ttu-id="81579-224">Os usuários podem alternar entre tipos de conteúdo usando o **recurso compartilhar conteúdo e conduzir atividades da reunião** na parte inferior da sala de reunião.</span><span class="sxs-lookup"><span data-stu-id="81579-224">Users can switch between content types using **Share content and lead meeting activities** at the bottom of the meeting room.</span></span> <span data-ttu-id="81579-225">Os usuários também podem usar o menu **gerenciar conteúdo apresentável** para escolher o conteúdo que deseja compartilhar.</span><span class="sxs-lookup"><span data-stu-id="81579-225">Users can also use the **Manage Presentable Content** menu to choose which content they want to share.</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="81579-226">Confira também</span><span class="sxs-lookup"><span data-stu-id="81579-226">See Also</span></span>


[<span data-ttu-id="81579-227">Planejamento de clientes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="81579-227">Planning for clients in Lync Server 2013</span></span>](lync-server-2013-planning-for-clients.md)  
  

<span data-ttu-id="81579-228"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="81579-228"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

