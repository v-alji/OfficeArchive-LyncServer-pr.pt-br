---
title: 'Lync Server 2013: Colocação em conjunto de servidor suportado para componentes de borda'
description: 'Lync Server 2013: colocação do servidor com suporte para componentes de borda.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported server collocation for edge components
ms:assetid: 435c4dd8-36af-4b71-9b88-3ffcf0fc5c65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425934(v=OCS.15)
ms:contentKeyID: 48183978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7bf253e5210e077ca62b3d00f7f130d54d8392a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423635"
---
# <a name="supported-server-collocation-for-edge-components-in-lync-server-2013"></a><span data-ttu-id="276a5-103">Colocação em conjunto de servidor suportado para componentes de borda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="276a5-103">Supported server collocation for edge components in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="276a5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="276a5-104">

<span> </span></span></span>

<span data-ttu-id="276a5-105">_**Tópico da última modificação:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="276a5-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="276a5-106">O serviço de borda de acesso, serviço de borda de webconferência, serviço de borda A/V e serviço de proxy da XMPP são posicionados nos servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="276a5-106">The Access Edge service, Web Conferencing Edge service, A/V Edge service and XMPP Proxy service are collocated on the Edge Servers.</span></span> <span data-ttu-id="276a5-107">Os seguintes servidores fornecem funções necessárias para acesso externo a usuários e devem ser implantados como servidores dedicados:</span><span class="sxs-lookup"><span data-stu-id="276a5-107">The following servers provide functions needed for external user access and must be deployed as dedicated servers:</span></span>

  - <span data-ttu-id="276a5-108">Servidor de Borda</span><span class="sxs-lookup"><span data-stu-id="276a5-108">Edge Server</span></span>

  - <span data-ttu-id="276a5-109">Director (opcional)</span><span class="sxs-lookup"><span data-stu-id="276a5-109">Director (Optional)</span></span>

  - <span data-ttu-id="276a5-110">Proxy reverso</span><span class="sxs-lookup"><span data-stu-id="276a5-110">Reverse proxy</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="276a5-111">O proxy inverso não precisa ser dedicado para atender apenas ao Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="276a5-111">The reverse proxy does not need to be dedicated to serving only Lync Server 2013.</span></span> <span data-ttu-id="276a5-112">Por exemplo, você pode fornecer serviços para publicar os serviços da Web do Lync Server e fornecer simultaneamente um site da Web publicado para outro site que não tenha nenhuma influência no Lync Server.</span><span class="sxs-lookup"><span data-stu-id="276a5-112">For example, you can provide services to publish the Lync Server Web services, and concurrently provide a published Web site for another Web site that has no bearing on Lync Server at all.</span></span> <span data-ttu-id="276a5-113">Se você já tiver um servidor proxy inverso na rede de perímetro para dar suporte a outros serviços, poderá usá-lo para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="276a5-113">If you already have a reverse proxy server in the perimeter network to support other services, you can use it for Lync Server 2013.</span></span>



<span data-ttu-id="276a5-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="276a5-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

