---
title: 'Lync Server 2013: atribuindo escopo da política de localização'
description: 'Lync Server 2013: atribuir o escopo da política de localização.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning location policy scope
ms:assetid: e4c66517-c593-4253-b900-7b4dd8bddf2f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205360(v=OCS.15)
ms:contentKeyID: 48185734
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9f6c46150241b0b224e8005556c0f2f594d8bce5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438299"
---
# <a name="assigning-location-policy-scope-in-lync-server-2013"></a><span data-ttu-id="db600-103">Atribuindo o escopo da política de localização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db600-103">Assigning location policy scope in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="db600-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="db600-104">

<span> </span></span></span>

<span data-ttu-id="db600-105">_**Tópico da última modificação:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="db600-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="db600-106">Assim como em outras políticas do Lync Server, as políticas de localização podem ser atribuídas em vários níveis de escopo: global, site e usuário.</span><span class="sxs-lookup"><span data-stu-id="db600-106">As with other Lync Server policies, location policies can be assigned at multiple scope levels: global, site, and user.</span></span> <span data-ttu-id="db600-107">No entanto, o escopo das políticas de localização em nível de usuário tem um pouco diferente do que as outras políticas do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="db600-107">However, the scope of user-level location policies behaves a bit differently than with other Lync Server policies.</span></span> <span data-ttu-id="db600-108">Não apenas as políticas de localização por usuário podem ser aplicadas a objetos de ponto de extremidade (como usuários e objetos de contato de telefone comum), também podem ser aplicadas a sites de rede do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="db600-108">Not only can per-user location policies be applied to endpoint objects (such as Users and Common Area Phone contact objects), they can also be applied to Lync Server network sites.</span></span> <span data-ttu-id="db600-109">Os sites de rede são agrupamentos de subredes de cliente associadas com um local geográfico (mas não necessariamente deve ser todas as subredes em um site central ou site de filial).</span><span class="sxs-lookup"><span data-stu-id="db600-109">Network sites are groupings of client subnets associated with a geographical location (but may not necessarily be all subnets in an entire central site or branch site).</span></span> <span data-ttu-id="db600-110">Qualquer cliente conectado às subredes de um site de rede obtém automaticamente a política de local atribuída a este site de rede.</span><span class="sxs-lookup"><span data-stu-id="db600-110">Any clients connected to the subnets in a network site automatically pick up the location policy assigned to that network site.</span></span> <span data-ttu-id="db600-111">Em casos onde uma política de local a nível de usuário é atribuída ao usuário e a um site de rede, a política de local baseada em site de rede substitui qualquer configuração de política por usuário.</span><span class="sxs-lookup"><span data-stu-id="db600-111">In cases where a user-level location policy is assigned both to a user and to a network site, the network site-based location policy overrides any per-user policy setting.</span></span>

<span data-ttu-id="db600-112">Cada local de rede possui uma política de rede atribuída e cada política possuirá diferentes valores de Usos de PSTN, URIs de notificação e URIs de conferência atribuídos.</span><span class="sxs-lookup"><span data-stu-id="db600-112">Each network site has a location policy assigned to it, and each policy will have different PSTN Usages, Notification URIs, and Conference URIs values assigned to it.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="db600-113">O motivo para esta política especial se comportar desta forma é porque quando um usuário hospedado em um pool em um local de escritório visita outro local e precisa fazer uma chamada de emergência, as configurações de roteamento de chamada E9-1-1 adequadas para este local de rede serão aplicadas não importando a qual pool ou local o usuário está atribuído.</span><span class="sxs-lookup"><span data-stu-id="db600-113">The reason for this special policy scoping behavior is so that when a user homed on a pool at one office site visits another site and has to make an emergency call, the E9-1-1 call routing settings appropriate to that network site will apply no matter what pool or site the user is assigned to.</span></span>



<span data-ttu-id="db600-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="db600-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

