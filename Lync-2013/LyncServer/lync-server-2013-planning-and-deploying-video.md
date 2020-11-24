---
title: 'Lync Server 2013: planejamento e implantação de vídeo'
description: 'Lync Server 2013: planejamento e implantação de vídeo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning and deploying video
ms:assetid: dadfb7f3-dfd6-4847-b137-17dacafd7368
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205307(v=OCS.15)
ms:contentKeyID: 48185558
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b9fd8a93f890295daebd2bc887414a2417b86395
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389875"
---
# <a name="planning-and-deploying-video-in-lync-server-2013"></a><span data-ttu-id="73927-103">Planejamento e implantação de vídeo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73927-103">Planning and deploying video in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="73927-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="73927-104">

<span> </span></span></span>

<span data-ttu-id="73927-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="73927-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="73927-106">O Lync Server 2013 apresenta os seguintes novos recursos de vídeo:</span><span class="sxs-lookup"><span data-stu-id="73927-106">Lync Server 2013 introduces the following new video features:</span></span>

  - <span data-ttu-id="73927-107">**Vídeo em HD**   Os usuários podem experimentar resoluções até alta definição (HD) (ou seja, 1920 x 1080) em chamadas de duas partes e em conferências com vários participantes.</span><span class="sxs-lookup"><span data-stu-id="73927-107">**HD video**   Users can experience resolutions up to full high definition (HD) (that is, 1920 x 1080) in two-party calls and multiparty conferences.</span></span>

  - <span data-ttu-id="73927-108">**Modo de exibição de galeria**   Em videoconferências com mais de duas pessoas, os usuários podem ver vídeos de participantes da conferência.</span><span class="sxs-lookup"><span data-stu-id="73927-108">**Gallery View**   In video conferences that have more than two people, users can see videos of participants in the conference.</span></span> <span data-ttu-id="73927-109">Se a conferência tiver mais de cinco participantes, o vídeo somente dos participantes ativos será exibido na linha superior, e uma foto será exibida para os outros participantes.</span><span class="sxs-lookup"><span data-stu-id="73927-109">If the conference has more than five participants, video of only the most active participants appears in the top row, and a photo appears for the other participants.</span></span>

  - <span data-ttu-id="73927-110">**Vídeo H. 264**   O codec de vídeo H. 264 agora é o padrão para codificar vídeo em clientes do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="73927-110">**H.264 video**   The H.264 video codec is now the default for encoding video on Lync 2013 clients.</span></span> <span data-ttu-id="73927-111">O vídeo H. 264 tem suporte para uma maior variedade de resoluções e taxas de quadros e melhora a escalabilidade de vídeo.</span><span class="sxs-lookup"><span data-stu-id="73927-111">H.264 video supports a greater range of resolutions and frame rates, and improves video scalability.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="73927-112">O Lync Server 2013 ainda oferece suporte ao codec VC1 para interoperabilidade com versões anteriores do Lync.</span><span class="sxs-lookup"><span data-stu-id="73927-112">Lync Server 2013 still supports the VC1 codec for interoperability with previous versions of Lync.</span></span> <span data-ttu-id="73927-113">Para obter detalhes e informações detalhadas sobre o novo codec de vídeo, consulte o artigo do blog do Jeff Schertz, "interoperabilidade de vídeo no Lync 2013", em <A class=uri href="http://blog.schertz.name/2012/07/video-interoperability-in-lync-2013/">http://blog.schertz.name/2012/07/video-interoperability-in-lync-2013/</A> .</span><span class="sxs-lookup"><span data-stu-id="73927-113">For details and background information about the new video codec, see Jeff Schertz's Blog article, "Video Interoperability in Lync 2013," at <A class=uri href="http://blog.schertz.name/2012/07/video-interoperability-in-lync-2013/">http://blog.schertz.name/2012/07/video-interoperability-in-lync-2013/</A>.</span></span>

    
    </div>

<span data-ttu-id="73927-114">Esta seção descreve como gerenciar a largura de banda de vídeo no Lync Server 2013 e como configurar recursos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="73927-114">This section describes how to manage bandwidth for video in Lync Server 2013 and how to configure video features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="73927-115">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="73927-115">In This Section</span></span>

  - [<span data-ttu-id="73927-116">Configurando a largura de banda do vídeo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73927-116">Configuring video bandwidth in Lync Server 2013</span></span>](lync-server-2013-configuring-video-bandwidth.md)

  - [<span data-ttu-id="73927-117">Configurando o modo de exibição de galeria no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73927-117">Configuring Gallery View in Lync Server 2013</span></span>](lync-server-2013-configuring-gallery-view.md)

  - [<span data-ttu-id="73927-118">Configurar cenários de exemplo de vídeo para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73927-118">Configuring video example scenarios for Lync Server 2013</span></span>](lync-server-2013-configuring-video-example-scenarios.md)

  - [<span data-ttu-id="73927-119">Considerações de interoperabilidade para videoconferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73927-119">Interoperability considerations for video conferencing in Lync Server 2013</span></span>](lync-server-2013-interoperability-considerations-for-video-conferencing.md)

<span data-ttu-id="73927-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="73927-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

