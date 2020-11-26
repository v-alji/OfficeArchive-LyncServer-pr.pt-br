---
title: 'Lync Server 2013: considerações de interoperabilidade para videoconferência'
description: 'Lync Server 2013: considerações de interoperabilidade para videoconferências.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Interoperability considerations for video conferencing
ms:assetid: 31ead3b5-ed95-42d4-96e2-7d9403d5c026
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204790(v=OCS.15)
ms:contentKeyID: 48183782
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 89675954ea4c4f188f50aab8fb2cb49494bcc247
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426785"
---
# <a name="interoperability-considerations-for-video-conferencing-in-lync-server-2013"></a><span data-ttu-id="8ef62-103">Considerações de interoperabilidade para videoconferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ef62-103">Interoperability considerations for video conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ef62-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ef62-104">

<span> </span></span></span>

<span data-ttu-id="8ef62-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="8ef62-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="8ef62-106">Esta seção descreve a experiência do usuário durante a fase de coexistência da migração, quando há interoperabilidade entre clientes herdados e um pool do Lync Server 2013 ou clientes do Lync Server 2013 e um pool herdado.</span><span class="sxs-lookup"><span data-stu-id="8ef62-106">This section describes the user experience during the coexistence phase of migration, when there is interoperability between legacy clients and a Lync Server 2013 pool or Lync Server 2013 clients and a legacy pool.</span></span>

<div>

## <a name="lync-server-2013-pools"></a><span data-ttu-id="8ef62-107">Pools do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ef62-107">Lync Server 2013 Pools</span></span>

<span data-ttu-id="8ef62-108">Os usuários perceberão o seguinte comportamento quando um cliente herdado for usado em um pool do Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="8ef62-108">Users will experience the following behavior when a legacy client is used in a Lync Server 2013 pool:</span></span>

  - <span data-ttu-id="8ef62-109">Para chamadas de dois participantes, a resolução de vídeo é a mesma do pool herdado.</span><span class="sxs-lookup"><span data-stu-id="8ef62-109">For two-party calls, video resolution is the same as in the legacy pool.</span></span>

  - <span data-ttu-id="8ef62-110">Para conferências com vários participantes, a resolução de vídeo e os recursos de videoconferência são iguais aos do pool herdado.</span><span class="sxs-lookup"><span data-stu-id="8ef62-110">For multiparty conferences, video resolution and video conferencing features are the same as in the legacy pool.</span></span> <span data-ttu-id="8ef62-111">O modo de exibição de galeria e alta resolução não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8ef62-111">Gallery View and high resolution are not available.</span></span>

</div>

<div>

## <a name="legacy-pools"></a><span data-ttu-id="8ef62-112">Pools herdados</span><span class="sxs-lookup"><span data-stu-id="8ef62-112">Legacy Pools</span></span>

<span data-ttu-id="8ef62-113">Os usuários perceberão o seguinte comportamento quando um cliente do Lync Server 2013 for usado em um pool herdado:</span><span class="sxs-lookup"><span data-stu-id="8ef62-113">Users will experience the following behavior when a Lync Server 2013 client is used in a legacy pool:</span></span>

  - <span data-ttu-id="8ef62-114">Para chamadas de dois participantes, os clientes do Lync Server 2013 podem usar novos recursos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8ef62-114">For two-party calls, Lync Server 2013 clients can use new features as follows:</span></span>
    
      - <span data-ttu-id="8ef62-115">H. 264 estará disponível se ambos os participantes estiverem usando os clientes do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8ef62-115">H.264 is available if both participants are using Lync Server 2013 clients.</span></span>
    
      - <span data-ttu-id="8ef62-116">O cliente do Lync Server 2013 usa o valor padrão para TotalReceiveVideoBitRateKb, uma vez que o servidor herdado não envia essas informações com o provisionamento em banda.</span><span class="sxs-lookup"><span data-stu-id="8ef62-116">The Lync Server 2013 client uses the default value for TotalReceiveVideoBitRateKb, since the legacy server doesn’t send this information with in-band provisioning.</span></span>

  - <span data-ttu-id="8ef62-117">Para conferências com vários participantes, a resolução de vídeo e os recursos de videoconferência são os mesmos que um cliente herdado no pool herdado.</span><span class="sxs-lookup"><span data-stu-id="8ef62-117">For multiparty conferences, video resolution and video conferencing features are the same as experienced by a legacy client in the legacy pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8ef62-118">Quando um servidor herdado hospeda um cliente do Lync Server 2013, é possível configurar a largura de banda de videoconferência para que todos os usuários do pool recebam somente vídeo de baixa resolução, mas enviem vídeo de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="8ef62-118">When a legacy server hosts a Lync Server 2013 client, it's possible to configure video conferencing bandwidth so that all users on the pool receive only low-resolution video, but send high-resolution video.</span></span> <span data-ttu-id="8ef62-119">Um exemplo disso é quando MaxVideoRateAllowed está definido como CIF-250K na configuração de mídia e VideoBitRateKb é definido como 2000 kbps na política de conferência.</span><span class="sxs-lookup"><span data-stu-id="8ef62-119">An example of this is when MaxVideoRateAllowed is set to CIF-250K in the media configuration and VideoBitRateKb is set to 2000 kbps in conferencing policy.</span></span> <span data-ttu-id="8ef62-120">Nesse caso, o efeito de alta resolução não é possível para os usuários do pool.</span><span class="sxs-lookup"><span data-stu-id="8ef62-120">The net effect in this situation is that high resolution is not possible for users on the pool.</span></span><BR><span data-ttu-id="8ef62-121">Como o MaxVideoRateAllowed não é mais usado para clientes do Lync Server 2013, ele não pode impedir que os clientes do Lync Server 2013 solicitem vídeo de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="8ef62-121">Because MaxVideoRateAllowed is no longer used for Lync Server 2013 clients, it cannot prevent Lync Server 2013 clients from requesting high-resolution video.</span></span> <span data-ttu-id="8ef62-122">Em vez disso, defina VideoBitRateKb na política de conferência para todos os usuários no pool para o mesmo valor que MaxVideoRateAllowed (ou seja, CIF é definido como 250 kbps ou VGA está definido como 600 kbps ou HD é definido como 1500 kbps).</span><span class="sxs-lookup"><span data-stu-id="8ef62-122">Instead, set VideoBitRateKb in conferencing policy for all users on the pool to the same value as MaxVideoRateAllowed (that is, CIF is set to 250 kbps, or VGA is set to 600 kbps, or HD is set to 1500 kbps).</span></span>



<span data-ttu-id="8ef62-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ef62-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

