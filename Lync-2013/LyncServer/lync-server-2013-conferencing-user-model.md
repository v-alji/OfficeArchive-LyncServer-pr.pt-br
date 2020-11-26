---
title: Modelo de usuário da conferência do Lync Server 2013
description: Modelo de usuário de conferência do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: The conferencing user model
ms:assetid: ba4bbba9-f2e3-4cab-8eba-b51f12133cab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205199(v=OCS.15)
ms:contentKeyID: 48185229
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 699f41303b82f4d8fd2864cbf1b29a1c601b826e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434274"
---
# <a name="the-conferencing-user-model-in-lync-server-2013"></a><span data-ttu-id="a9f26-103">O modelo de usuário de conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a9f26-103">The conferencing user model in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a9f26-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a9f26-104">

<span> </span></span></span>

<span data-ttu-id="a9f26-105">_**Tópico da última modificação:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="a9f26-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="a9f26-106">Uma parte crítica do modelo de usuário do Lync Server Conferencing é o tamanho da reunião.</span><span class="sxs-lookup"><span data-stu-id="a9f26-106">A critical part of the Lync Server conferencing user model is meeting size.</span></span> <span data-ttu-id="a9f26-107">Após coletar dados de vários pontos de dados (conforme descrito na seção anterior), determinamos o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a9f26-107">After collecting data from the multiple data points (as described in the previous section), we determined the following:</span></span>

  - <span data-ttu-id="a9f26-108">A maioria das reuniões é realmente pequena reunião colaborativa com uma média de quatro a seis participantes</span><span class="sxs-lookup"><span data-stu-id="a9f26-108">Most meetings are actually small collaborative meetings with an average of four to six participants</span></span>

  - <span data-ttu-id="a9f26-109">Aproximadamente 20 a 80% das reuniões têm menos de 20 participantes.</span><span class="sxs-lookup"><span data-stu-id="a9f26-109">Approximately 80 percent of meetings have fewer than 20 participants.</span></span>

  - <span data-ttu-id="a9f26-110">99,98% das reuniões têm menos de 100 participantes.</span><span class="sxs-lookup"><span data-stu-id="a9f26-110">99.98 percent of meetings have fewer than 100 participants.</span></span>

<span data-ttu-id="a9f26-111">Além do tamanho da reunião, o modelo de usuário da conferência também leva em conta uma variedade de fatores, como:</span><span class="sxs-lookup"><span data-stu-id="a9f26-111">In addition to meeting size, the conferencing user model also takes into account a variety of factors, such as:</span></span>

  - <span data-ttu-id="a9f26-112">**Reuniões simultâneas**   Quantos usuários devem estar em reuniões ao mesmo tempo?</span><span class="sxs-lookup"><span data-stu-id="a9f26-112">**Concurrent meetings**   How many users are expected to be in meetings at the same time?</span></span>

  - <span data-ttu-id="a9f26-113">**Mix de mídia**   Que tipos de mídia estão disponíveis e que devem ser usados por usuários em reuniões?</span><span class="sxs-lookup"><span data-stu-id="a9f26-113">**Media mix**   What types of media are available and expected to be used by users in meetings?</span></span>

  - <span data-ttu-id="a9f26-114">**Tipos de usuário**   Os usuários são usuários internos, usuários remotos, usuários federados ou usuários anônimos?</span><span class="sxs-lookup"><span data-stu-id="a9f26-114">**User types**   Are users internal users, remote users, federated users, or anonymous users?</span></span>

  - <span data-ttu-id="a9f26-115">**Tempo de crescimento da reunião**   Quanto tempo leva para que todos os usuários de uma reunião ingressem em uma reunião?</span><span class="sxs-lookup"><span data-stu-id="a9f26-115">**Meeting ramp up time**   How long does it take for all users of a meeting to join a meeting?</span></span>

<span data-ttu-id="a9f26-116">Para obter detalhes sobre o modelo de usuário, consulte [modelos de usuário no Lync Server 2013](lync-server-2013-user-models.md).</span><span class="sxs-lookup"><span data-stu-id="a9f26-116">For details about the user model, see [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

<span data-ttu-id="a9f26-117">Para determinar o número de reuniões e usuários a serem usados para testes, fizemos o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a9f26-117">To determine the number of meetings and users to use for testing, we did the following:</span></span>

  - <span data-ttu-id="a9f26-118">Gastou o número total de usuários em uma organização (por exemplo, 80.000 usuários) e o multiplicado pela taxa de simultaneidade da reunião (por exemplo, 5% de todos os usuários) para determinar o número total de usuários que devem estar em reuniões ao mesmo tempo (neste exemplo, 4000 usuários).</span><span class="sxs-lookup"><span data-stu-id="a9f26-118">Took the total number of users in an organization (for example, 80,000 users) and multiplied it by the meeting concurrency rate (for example, 5% of all users) to determine the total number of users expected to be in meetings at the same time (in this example, 4000 users).</span></span>

  - <span data-ttu-id="a9f26-119">Dividiu o número total de usuários pelo número de servidores do Lync Server 2013, front-end na implantação (por exemplo, 8 servidores) para determinar o número estimado de participantes da reunião por servidor front-end (neste exemplo, 500 usuários por servidor front-end).</span><span class="sxs-lookup"><span data-stu-id="a9f26-119">Divided the total number of users by the number of Lync Server 2013, Front End Servers in the deployment (for example, 8 servers) to determine the estimated number of meeting participants per Front End Server (in this example, 500 users per Front End Server).</span></span>

  - <span data-ttu-id="a9f26-120">Divida o número de usuários por servidor front-end pelo tamanho médio da reunião (por exemplo, 4 usuários) para determinar o número médio estimado de reuniões por servidor front-end (neste exemplo, reuniões do 125 por servidor front-end).</span><span class="sxs-lookup"><span data-stu-id="a9f26-120">Divided the number of users per Front End Server by the average meeting size (for example, 4 users) to determine the estimated average number of meetings per Front End Server (in this example, 125 meetings per Front End Server).</span></span>

  - <span data-ttu-id="a9f26-121">Para obter a carga por mídia em cada servidor front-end, estimamos o mix de mídia.</span><span class="sxs-lookup"><span data-stu-id="a9f26-121">To get the per media load on each Front End Server, we estimated the media mix.</span></span> <span data-ttu-id="a9f26-122">Por exemplo, pressupondo que 75% das reuniões exijam mais do que apenas o suporte a áudio e 50% dessas reuniões exigem compartilhamento de aplicativos, uma média de reuniões do 47 e os usuários da 188 se conectam simultaneamente a cada servidor front-end para compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a9f26-122">For example, assuming that 75% of the meetings require more than just audio support and 50% of those meetings require application sharing, an average of 47 meetings and 188 users connect concurrently to each Front End Server for application sharing.</span></span>

  - <span data-ttu-id="a9f26-123">Testou uma variedade de tamanhos de reunião (com base em nosso modelo de usuário de até 250 usuários em um pool compartilhado) para garantir a escalabilidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="a9f26-123">Tested a variety of meeting sizes (based our user model of up to 250 users in a shared pool) to ensure server scalability.</span></span>

<span data-ttu-id="a9f26-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a9f26-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

