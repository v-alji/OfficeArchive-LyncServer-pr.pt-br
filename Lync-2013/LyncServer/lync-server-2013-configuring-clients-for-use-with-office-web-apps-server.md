---
title: 'Lync Server 2013: Configurando clientes para usar com o servidor do Office Web Apps'
description: 'Lync Server 2013: Configurando clientes para uso com o servidor do Office Web Apps.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring clients for use with Office Web Apps Server
ms:assetid: e5eaead7-0b32-42fb-97eb-ca203af59a9d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205339(v=OCS.15)
ms:contentKeyID: 48185668
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b9bd7cf1e76c481c40381234ba1a84cda5500dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390347"
---
# <a name="configuring-clients-of-lync-server-2013-for-use-with-office-web-apps-server"></a><span data-ttu-id="65b55-103">Configurar clientes do Lync Server 2013 para uso com o servidor do Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="65b55-103">Configuring clients of Lync Server 2013 for use with Office Web Apps Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="65b55-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="65b55-104">

<span> </span></span></span>

<span data-ttu-id="65b55-105">_**Tópico da última modificação:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="65b55-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="65b55-106">Se você quiser que os usuários tenham os recursos completos do Office Web App Server, atualize-os para o Microsoft Lync 2013; somente os usuários do Lync 2013 poderão fazer coisas como rolar pelos slides do PowerPoint independentemente da apresentação real do PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="65b55-106">If you want users to experience the full capabilities of Office Web App Server then you should upgrade those users to Microsoft Lync 2013; only users of Lync 2013 will be able to do such things as scroll through PowerPoint slides independent of the actual PowerPoint presentation.</span></span> <span data-ttu-id="65b55-107">(Ou seja, esses usuários podem ver qualquer slide da apresentação a qualquer momento, sem interferir em qualquer forma com a apresentação real.) Os usuários que não estiverem usando o Lync 2013 ainda poderão participar de conferências online e exibir a apresentação do PowerPoint; no entanto, eles não poderão rolar de forma independente nos slides nem poderão ver as transições de slide nem exibir vídeos inseridos.</span><span class="sxs-lookup"><span data-stu-id="65b55-107">(That is, these users can look at any slide in the presentation at any time, without interfering in any way with the actual presentation.) Users who are not using Lync 2013 will still be able to join online conferences and view the PowerPoint presentation; however, they will not be able to independently scroll through the slides, nor will they be able to see slide transitions or view embedded videos.</span></span>

<span data-ttu-id="65b55-108">Observe que esses recursos estarão sempre disponíveis para os usuários do Lync 2013; Isso é verdadeiro mesmo que o apresentador do PowerPoint esteja executando o Microsoft Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="65b55-108">Note that these capabilities will always be available to users of Lync 2013; this is true even if the PowerPoint presenter is running Microsoft Lync 2010.</span></span> <span data-ttu-id="65b55-109">Se uma apresentação do PowerPoint estiver sendo hospedada por um usuário que está executando o Lync 2010, o Lync Server 2013 irá coordenar com o servidor do Office Web Apps para garantir que os usuários do Lync 2013 exibirão a versão do servidor dos Office Web Apps dessa apresentação.</span><span class="sxs-lookup"><span data-stu-id="65b55-109">If a PowerPoint presentation is being hosted by a user running Lync 2010, Lync Server 2013 will coordinate with Office Web Apps Server to make sure that Lync 2013 users will view the Office Web Apps Server version of that presentation.</span></span> <span data-ttu-id="65b55-110">O Office Web Apps Server não fornece serviços do PowerPoint para usuários que executam clientes que não sejam o Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="65b55-110">Office Web Apps Server does not provide PowerPoint services for users running clients other than Lync 2013.</span></span> <span data-ttu-id="65b55-111">Em vez disso, esses usuários se conectam ao serviço do servidor de conferência e exibem apresentações do PowerPoint da mesma forma que no Microsoft Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="65b55-111">Instead, those users connect to the Conferencing server service and view PowerPoint presentations the same way they did in Microsoft Lync Server 2010.</span></span> <span data-ttu-id="65b55-112">Isso também significa que esses usuários terão acesso somente aos recursos mais limitados oferecidos pelo Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="65b55-112">This also means that these users will only have access to the more-limited capabilities offered by Lync Server 2010.</span></span>

<span data-ttu-id="65b55-113">Embora não seja necessária nenhuma configuração do cliente para o Office Web Apps Server (exceto para atualizar usuários para o Lync 2013), é recomendável que os participantes da conferência sejam atualizados para o Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="65b55-113">Although no client configuration is required for Office Web Apps Server (other than upgrading users to Lync 2013), it is recommended that conference attendees be upgrade to Internet Explorer 9.</span></span> <span data-ttu-id="65b55-114">Embora as conferências possam ser acessadas usando o Internet Explorer 8, há algumas limitações para usar o navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="65b55-114">Although conferences can be accessed using Internet Explorer 8, there are some limitations to using that Web browser.</span></span> <span data-ttu-id="65b55-115">Por exemplo, os usuários do Internet Explorer 8 não serão capazes de redimensionar a fase do PowerPoint para um tamanho personalizado; em vez disso, eles serão limitados a usar um dos três tamanhos de estágio predefinidos.</span><span class="sxs-lookup"><span data-stu-id="65b55-115">For example, users of Internet Explorer 8 will not be able to resize the PowerPoint stage to a custom size; instead, they will be limited to using one of three predefined stage sizes.</span></span> <span data-ttu-id="65b55-116">Da mesma forma, os usuários do Internet Explorer 8 não serão capazes de reproduzir arquivos de mídia.</span><span class="sxs-lookup"><span data-stu-id="65b55-116">Likewise, Internet Explorer 8 users will not be able to play media files.</span></span>

<span data-ttu-id="65b55-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="65b55-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

