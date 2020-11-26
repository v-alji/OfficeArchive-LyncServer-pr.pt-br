---
title: 'Lync Server 2013: Tecnologias de virtualização suportadas e limitações conhecidas'
description: 'Lync Server 2013: tecnologias de virtualização compatíveis e limitações conhecidas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported virtualization technologies and known limitations
ms:assetid: 6d3d749d-e840-4c05-afae-d6e69e7616aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204982(v=OCS.15)
ms:contentKeyID: 48184428
ms.date: 02/07/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 745fa535462d29342f4c0a58674ee6487db42a6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423558"
---
# <a name="supported-virtualization-technologies-and-known-limitations-in-lync-server-2013"></a><span data-ttu-id="6aadc-103">Tecnologias de virtualização suportadas e limitações conhecidas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6aadc-103">Supported virtualization technologies and known limitations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6aadc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6aadc-104">

<span> </span></span></span>

<span data-ttu-id="6aadc-105">_**Tópico da última modificação:** 2017-02-06_</span><span class="sxs-lookup"><span data-stu-id="6aadc-105">_**Topic Last Modified:** 2017-02-06_</span></span>

<span data-ttu-id="6aadc-106">O plug-in VDI do Lync permite chamadas de áudio e vídeo para tecnologias de virtualização compatíveis.</span><span class="sxs-lookup"><span data-stu-id="6aadc-106">The Lync VDI plug-in allows audio and video calling for supported virtualization technologies.</span></span> <span data-ttu-id="6aadc-107">Isso estende a funcionalidade descrita para o Microsoft Lync Server 2010 no White Paper [virtualização do cliente no Microsoft lync 2010](https://go.microsoft.com/fwlink/?linkid=330447) .</span><span class="sxs-lookup"><span data-stu-id="6aadc-107">This extends the functionality outlined for Microsoft Lync Server 2010 in the [Client Virtualization in Microsoft Lync 2010](https://go.microsoft.com/fwlink/?linkid=330447) white paper.</span></span> <span data-ttu-id="6aadc-108">Em conformidade com os regulamentos de telefonia padrão, o suporte para o E911 também está incluído.</span><span class="sxs-lookup"><span data-stu-id="6aadc-108">In compliance with standard telephone regulations, support for E911 is also included.</span></span> <span data-ttu-id="6aadc-109">As seções a seguir descrevem as tecnologias de virtualização que são compatíveis com o plug-in VDI do Lync e as limitações de recursos conhecidos.</span><span class="sxs-lookup"><span data-stu-id="6aadc-109">The following sections describe the virtualization technologies that are supported by the Lync VDI plug-in and the known feature limitations.</span></span>

<div>

## <a name="support-for-virtualization-technologies"></a><span data-ttu-id="6aadc-110">Suporte para Tecnologias de Virtualização</span><span class="sxs-lookup"><span data-stu-id="6aadc-110">Support for Virtualization Technologies</span></span>

<span data-ttu-id="6aadc-111">O plug-in VDI do Lync é compatível com o Remoting da área de trabalho virtual no cenário de área de trabalho virtual pessoal, mas não no cenário da sessão da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="6aadc-111">The Lync VDI plug-in supports full desktop remoting in the personal virtual desktop scenario, but not in the remote desktop session scenario.</span></span> <span data-ttu-id="6aadc-112">Esses cenários podem ser descritos como segue:</span><span class="sxs-lookup"><span data-stu-id="6aadc-112">These scenarios can be described as follows:</span></span>

  - <span data-ttu-id="6aadc-113">**Com suporte: Áreas de Trabalho Virtuais Personalizadas ou Virtual Desktop Infrastructure (VDI).**</span><span class="sxs-lookup"><span data-stu-id="6aadc-113">**Supported: Personalized Virtual Desktops or Virtual Desktop Infrastructure (VDI).**</span></span>   <span data-ttu-id="6aadc-114">Neste cenário, cada usuário faz logon em uma área de trabalho virtual personalizável e pode salvar arquivos na área de trabalho que persiste entre as sessões.</span><span class="sxs-lookup"><span data-stu-id="6aadc-114">In this scenario, each user logs on to a customizable virtual desktop and is able to save files on the desktop that persist across sessions.</span></span> <span data-ttu-id="6aadc-115">Os serviços de área de trabalho remota da Microsoft, o modo de exibição horizonte do VMware e o Citrix XenDesktop são implementações que foram testadas para uso com o Lync.</span><span class="sxs-lookup"><span data-stu-id="6aadc-115">Microsoft Remote Desktop Services, VMware Horizon View, and Citrix XenDesktop are implementations that have been tested for use with Lync.</span></span> <span data-ttu-id="6aadc-116">Para obter informações sobre ambientes VDI específicos do fornecedor e hardware cliente que foram testados pela Microsoft, consulte [infraestrutura qualificada para Microsoft Lync](https://go.microsoft.com/fwlink/?linkid=313435).</span><span class="sxs-lookup"><span data-stu-id="6aadc-116">For information about vendor-specific VDI environments and client hardware that have been tested by Microsoft, see [Infrastructure qualified for Microsoft Lync](https://go.microsoft.com/fwlink/?linkid=313435).</span></span>

  - <span data-ttu-id="6aadc-117">**Sem suporte: Sessões de Área de Trabalho Remota.**</span><span class="sxs-lookup"><span data-stu-id="6aadc-117">**Not supported: Remote Desktop Sessions.**</span></span>   <span data-ttu-id="6aadc-118">Neste cenário, cada usuário registra-se em sessões de área de trabalho virtual genérica que não podem ser personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6aadc-118">In this scenario, each user logs on to a generic virtual desktop session that cannot be customized.</span></span> <span data-ttu-id="6aadc-119">Exemplos de implantações incluem Sessões de Área de Trabalho Remota da Microsoft (RDSH) e Citrix XenApp juntamente com o Citrix Receiver.</span><span class="sxs-lookup"><span data-stu-id="6aadc-119">Example implementations include Microsoft Remote Desktop Sessions (RDSH) and Citrix XenApp combined with Citrix Receiver.</span></span>

<span data-ttu-id="6aadc-120">O plug-in VDI do Lync não oferece suporte a outras tecnologias de virtualização, como a virtualização de aplicativos, que permite o uso de um aplicativo sem a necessidade de instalação do aplicativo completo localmente.</span><span class="sxs-lookup"><span data-stu-id="6aadc-120">The Lync VDI plug-in does not support other virtualization technologies, such as application virtualization, which allows the use of an application without requiring installation of the full application locally.</span></span> <span data-ttu-id="6aadc-121">Exemplos de implementações incluem o Citrix XenApp e a Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="6aadc-121">Example implementations include Citrix XenApp and Microsoft Application Virtualization (App-V).</span></span> <span data-ttu-id="6aadc-122">Aplicação de streaming, comunicação remota de aplicativos e modelos de virtualização mistos (por exemplo, comunicação remota de aplicativos em toda a área de trabalho remota) não são suportados.</span><span class="sxs-lookup"><span data-stu-id="6aadc-122">Application streaming, application remoting, and mixed virtualization modes (for example, application remoting in full desktop remoting) are not supported.</span></span>

<span data-ttu-id="6aadc-123">Para permitir a extensibilidade, o plug-in VDI do Lync foi projetado para usar APIs independentes de plataforma chamadas DVCs (canais virtuais dinâmicos).</span><span class="sxs-lookup"><span data-stu-id="6aadc-123">To allow extensibility, the Lync VDI plug-in was designed to use platform-independent APIs called Dynamic Virtual Channels (DVCs).</span></span> <span data-ttu-id="6aadc-124">Para cenários que não são explicitamente suportados pelo Lync, consulte declarações de suporte do provedor de soluções VDI.</span><span class="sxs-lookup"><span data-stu-id="6aadc-124">For scenarios that are not explicitly supported by Lync, refer to support statements from the VDI solution provider.</span></span>

</div>

<div>

## <a name="known-feature-limitations"></a><span data-ttu-id="6aadc-125">Limitações conhecidas dos recursos</span><span class="sxs-lookup"><span data-stu-id="6aadc-125">Known Feature Limitations</span></span>

<span data-ttu-id="6aadc-126">Veja a seguir as limitações conhecidas quando você usa o Lync 2013 em um ambiente VDI:</span><span class="sxs-lookup"><span data-stu-id="6aadc-126">The following are known limitations when you use Lync 2013 in a VDI environment:</span></span>

  - <span data-ttu-id="6aadc-127">Há suporte limitado para recursos de delegação de chamada e de anonimato do agente do grupo de resposta.</span><span class="sxs-lookup"><span data-stu-id="6aadc-127">There is limited support for Call Delegation and Response Group Agent Anonymization features.</span></span>

  - <span data-ttu-id="6aadc-128">Não há suporte aos seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="6aadc-128">There is no support for the following features:</span></span>
    
      - <span data-ttu-id="6aadc-129">Páginas de ajuste de dispositivo de áudio integrado e dispositivo de vídeo</span><span class="sxs-lookup"><span data-stu-id="6aadc-129">Integrated Audio Device and Video Device tuning pages.</span></span>
    
      - <span data-ttu-id="6aadc-130">Vídeo com modo de exibição múltipla.</span><span class="sxs-lookup"><span data-stu-id="6aadc-130">Multiple-view video.</span></span>
    
      - <span data-ttu-id="6aadc-131">Gravação de conversas.</span><span class="sxs-lookup"><span data-stu-id="6aadc-131">Recording of conversations.</span></span>
    
      - <span data-ttu-id="6aadc-132">Serviços de área de trabalho remota (RDS).</span><span class="sxs-lookup"><span data-stu-id="6aadc-132">Remote Desktop Services (RDS).</span></span>
    
      - <span data-ttu-id="6aadc-133">Ingressar em reuniões anonimamente (isto é, ingressando em reuniões do Lync hospedadas por uma organização que não se federa à sua organização).</span><span class="sxs-lookup"><span data-stu-id="6aadc-133">Joining meetings anonymously (that is, joining Lync meetings hosted by an organization that does not federate with your organization).</span></span>
    
      - <span data-ttu-id="6aadc-134">Usar o plug-in VDI do Lync juntamente com um dispositivo Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="6aadc-134">Using the Lync VDI plug-in along with a Lync Phone Edition device.</span></span>
    
      - <span data-ttu-id="6aadc-135">Continuidade de chamadas em caso de indisponibilidade da rede.</span><span class="sxs-lookup"><span data-stu-id="6aadc-135">Call continuity in case of a network outage.</span></span>
    
      - <span data-ttu-id="6aadc-136">Toques personalizados e recursos de música em espera.</span><span class="sxs-lookup"><span data-stu-id="6aadc-136">Customized ringtones and music-on-hold features.</span></span>

  - <span data-ttu-id="6aadc-137">O plug-in VDI do Lync não é compatível com um ambiente do Microsoft 365 ou do Office 365.</span><span class="sxs-lookup"><span data-stu-id="6aadc-137">The Lync VDI plug-in is not supported in a Microsoft 365 or Office 365 environment.</span></span>

<span data-ttu-id="6aadc-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6aadc-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

