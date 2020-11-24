---
title: 'Lync Server 2013: Configurando um local de backup'
description: 'Lync Server 2013: Configurando um local de backup.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up a backup location
ms:assetid: 006732eb-3d44-414d-8010-227a855caa93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202158(v=OCS.15)
ms:contentKeyID: 51541440
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 344baea1b7e51454bb28d31d88451d29fd6aa3a4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390273"
---
# <a name="setting-up-a-backup-location-for-lync-server-2013"></a><span data-ttu-id="d02ee-103">Configurar um local de backup para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d02ee-103">Setting up a backup location for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d02ee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d02ee-104">

<span> </span></span></span>

<span data-ttu-id="d02ee-105">_**Tópico da última modificação:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="d02ee-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="d02ee-106">Antes de fazer o primeiro backup do Lync Server, configure o hardware e o software necessários para armazenar e manter os backups.</span><span class="sxs-lookup"><span data-stu-id="d02ee-106">Before you take your first backup of Lync Server, set up the hardware and software that you need in order to store and maintain the backups.</span></span> <span data-ttu-id="d02ee-107">Você precisa obter acesso à mídia e ao conteúdo, conforme apropriado, e fornecer conectividade de rede entre cada servidor para fazer backup e a mídia de backup.</span><span class="sxs-lookup"><span data-stu-id="d02ee-107">You need to obtain access to the media and content, as appropriate, and provide network connectivity between each server to be backed up and the backup media.</span></span> <span data-ttu-id="d02ee-108">A mídia e o local que você usa devem ser definidos na estratégia de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="d02ee-108">The media and location that you use should be defined in your backup and restoration strategy.</span></span> <span data-ttu-id="d02ee-109">O local que você usa para fazer backups regulares pode ser local ou remoto, mas ele deve ser seguro e deve estar acessível para backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="d02ee-109">The location that you use for regular backups can be local or remote, but it must be secure, and it must be accessible for both backup and restoration.</span></span> <span data-ttu-id="d02ee-110">Recomendamos usar um local remoto para se proteger contra um evento catastrófico em seu local principal.</span><span class="sxs-lookup"><span data-stu-id="d02ee-110">We recommend using a remote location to protect against a catastrophic event at your primary site.</span></span>

<span data-ttu-id="d02ee-111">Depois de configurar e testar os componentes individuais, verifique a acessibilidade aos backups de cada servidor.</span><span class="sxs-lookup"><span data-stu-id="d02ee-111">After you set up and test the individual components, verify accessibility to the backups from each server.</span></span>

<span data-ttu-id="d02ee-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d02ee-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

