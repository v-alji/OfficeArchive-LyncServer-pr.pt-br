---
title: 'Lync Server 2013: desenvolvendo uma estratégia e um plano de backup e restauração'
description: 'Lync Server 2013: desenvolvendo uma estratégia e um plano de backup e restauração.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Developing a backup and restoration strategy and plan
ms:assetid: 17599b76-1a84-4dd6-b695-c19637deb8a6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202164(v=OCS.15)
ms:contentKeyID: 51541447
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3d55eeb541cdde5c43d7d680ceb212d87da0d517
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429444"
---
# <a name="developing-a-backup-and-restoration-strategy-and-plan-for-lync-server-2013"></a><span data-ttu-id="1af53-103">Desenvolvendo uma estratégia de backup e restauração e um plano para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1af53-103">Developing a backup and restoration strategy and plan for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1af53-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1af53-104">

<span> </span></span></span>

<span data-ttu-id="1af53-105">_**Tópico da última modificação:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="1af53-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="1af53-106">A eficácia das operações de backup e restauração do Lync Server depende da estratégia e do plano de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="1af53-106">The effectiveness of your Lync Server backup and restoration operations depends on your backup and restoration strategy and plan.</span></span> <span data-ttu-id="1af53-107">Você deve estabelecer uma estratégia para fazer backup e restaurar o Lync Server que se adapta à estratégia geral da sua organização e um plano abrangente e conciso para fazer backup de dados e configurações e, no caso de uma interrupção, um plano para restaurar o serviço.</span><span class="sxs-lookup"><span data-stu-id="1af53-107">You should establish a strategy for backing up and restoring Lync Server that fits with your organization's overall strategy, and a comprehensive, concise plan for backing up data and settings, and, in the event of an outage, a plan for restoring service.</span></span>

<span data-ttu-id="1af53-108">Para a recuperação de desastres mais robusta de um pool de front-end, use a topologia de recuperação de desastres de pool emparelhada introduzida no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1af53-108">For the most robust disaster recovery of a Front End Pool, use the paired-pool disaster recovery topology introduced in Lync Server 2013.</span></span> <span data-ttu-id="1af53-109">Para obter mais informações, consulte [planejando a alta disponibilidade e a recuperação de desastres no Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="1af53-109">For more information, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="1af53-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="1af53-110">In This Section</span></span>

  - [<span data-ttu-id="1af53-111">Como estabelecer uma estratégia de backup e restauração para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1af53-111">Establishing a backup and restoration strategy for Lync Server 2013</span></span>](lync-server-2013-establishing-a-backup-and-restoration-strategy.md)

  - [<span data-ttu-id="1af53-112">Como estabelecer um plano de backup e restauração para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1af53-112">Establishing a backup and restoration plan for Lync Server 2013</span></span>](lync-server-2013-establishing-a-backup-and-restoration-plan.md)

  - [<span data-ttu-id="1af53-113">Configurar um local de backup para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1af53-113">Setting up a backup location for Lync Server 2013</span></span>](lync-server-2013-setting-up-a-backup-location.md)

<span data-ttu-id="1af53-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1af53-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

