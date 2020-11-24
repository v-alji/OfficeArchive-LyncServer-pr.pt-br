---
title: 'Lync Server 2013: Componentes usados pelo Estacionamento de Chamadas'
description: 'Lync Server 2013: componentes usados pelo parque de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Call Park
ms:assetid: c7ffbee3-0ce1-48c0-bb56-af098b41d6d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398824(v=OCS.15)
ms:contentKeyID: 48185374
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 285af316fa2d49e8bebf68e11de6d9526e12ae29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389898"
---
# <a name="components-used-by-call-park-in-lync-server-2013"></a><span data-ttu-id="3adb5-103">Componentes usados pelo Estacionamento de Chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3adb5-103">Components used by Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3adb5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3adb5-104">

<span> </span></span></span>

<span data-ttu-id="3adb5-105">_**Tópico da última modificação:** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="3adb5-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<span data-ttu-id="3adb5-106">O aplicativo de estacionamento de chamadas é instalado automaticamente quando você implanta o Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="3adb5-106">The Call Park application is automatically installed when you deploy Enterprise Voice.</span></span> <span data-ttu-id="3adb5-107">Para habilitar o estacionamento de chamadas, configure a política de voz.</span><span class="sxs-lookup"><span data-stu-id="3adb5-107">You enable Call Park by configuring voice policy.</span></span> <span data-ttu-id="3adb5-108">Os seguintes componentes do Lync Server 2013 suportam o aplicativo de estacionamento de chamadas:</span><span class="sxs-lookup"><span data-stu-id="3adb5-108">The following Lync Server 2013 components support the Call Park application:</span></span>

  - <span data-ttu-id="3adb5-109">**Serviço de aplicativo**   O serviço de aplicativo fornece uma plataforma para implantação, hospedagem e gerenciamento de aplicativos de comunicação unificada, como o aplicativo de estacionamento de chamada.</span><span class="sxs-lookup"><span data-stu-id="3adb5-109">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications, such as the Call Park application.</span></span> <span data-ttu-id="3adb5-110">O serviço de aplicativo é instalado automaticamente em todos os servidores front-end em um pool Front-end e em cada servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="3adb5-110">Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="3adb5-111">**Aplicativo de estacionamento de chamadas**   O aplicativo de estacionamento de chamadas é um dos aplicativos de comunicação unificada hospedados pelo serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3adb5-111">**Call Park application**   The Call Park application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="3adb5-112">Ela é incluída automaticamente durante a implantação do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="3adb5-112">It is included automatically when you deploy Enterprise Voice.</span></span> <span data-ttu-id="3adb5-113">Ligue para parques e recupere chamadas e gerencie órbitas de estacionamento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="3adb5-113">Call Park parks and retrieves calls and manages call park orbits.</span></span>

  - <span data-ttu-id="3adb5-114">**Música-em espera-arquivo**   Se a música estiver habilitada, o arquivo de música será reproduzido enquanto uma chamada estiver estacionada.</span><span class="sxs-lookup"><span data-stu-id="3adb5-114">**Music-on hold-file**   If music in enabled, the music file is played while a call is parked.</span></span> <span data-ttu-id="3adb5-115">Um arquivo de música padrão é incluído quando o aplicativo de estacionamento de chamada é instalado.</span><span class="sxs-lookup"><span data-stu-id="3adb5-115">A default music file is included when the Call Park application is installed.</span></span>

  - <span data-ttu-id="3adb5-116">**Repositório de arquivos**   O aplicativo parque de chamadas usa o repositório de arquivos para armazenar arquivos de áudio personalizados.</span><span class="sxs-lookup"><span data-stu-id="3adb5-116">**File Store**   The Call Park application uses File Store to hold custom audio files.</span></span>

  - <span data-ttu-id="3adb5-117">**Painel de controle do Lync Server**   Você pode usar o painel de controle do Lync Server para configurar a tabela órbita do estacionamento de chamada e para habilitar o estacionamento de chamadas para os usuários.</span><span class="sxs-lookup"><span data-stu-id="3adb5-117">**Lync Server Control Panel**   You can use Lync Server Control Panel to configure the call park orbit table and to enable Call Park for users.</span></span>

  - <span data-ttu-id="3adb5-118">**Shell de gerenciamento do Lync Server**   Todas as configurações do aplicativo de estacionamento de chamadas podem ser realizadas usando cmdlets do shell do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3adb5-118">**Lync Server Management Shell**   All Call Park application configuration can be performed by using Lync Server Management Shell cmdlets.</span></span>

<span data-ttu-id="3adb5-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3adb5-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

