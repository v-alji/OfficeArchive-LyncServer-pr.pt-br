---
title: 'Lync Server 2013: Componentes usados pelo aplicativo Comunicado'
description: 'Lync Server 2013: componentes usados pelo aplicativo de anúncio.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by the Announcement application
ms:assetid: 7b1a0281-cf31-459d-a734-5f10a129089c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398608(v=OCS.15)
ms:contentKeyID: 48184595
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e5338ad097c814d5c6435bd89dbf7cfa8680feb8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389896"
---
# <a name="components-used-by-the-announcement-application-in-lync-server-2013"></a><span data-ttu-id="50de3-103">Componentes usados pelo aplicativo Comunicado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50de3-103">Components used by the Announcement application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="50de3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="50de3-104">

<span> </span></span></span>

<span data-ttu-id="50de3-105">_**Tópico da última modificação:** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="50de3-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<span data-ttu-id="50de3-106">No Lync Server 2013, o aplicativo de anúncio é um componente do aplicativo de grupo de resposta.</span><span class="sxs-lookup"><span data-stu-id="50de3-106">In Lync Server 2013, the Announcement application is a component of the Response Group application.</span></span> <span data-ttu-id="50de3-107">Quando você implanta o Enterprise Voice, o aplicativo de anúncio é automaticamente instalado e ativado juntamente com o aplicativo de grupo de resposta.</span><span class="sxs-lookup"><span data-stu-id="50de3-107">When you deploy Enterprise Voice, the Announcement application is automatically installed and activated along with the Response Group application.</span></span> <span data-ttu-id="50de3-108">Esta seção descreve os componentes que dão suporte ao aplicativo de anúncio.</span><span class="sxs-lookup"><span data-stu-id="50de3-108">This section describes the components that support the Announcement application.</span></span>

<div>

## <a name="announcement-application-components"></a><span data-ttu-id="50de3-109">Componentes do aplicativo de anúncio</span><span class="sxs-lookup"><span data-stu-id="50de3-109">Announcement Application Components</span></span>

<span data-ttu-id="50de3-110">Os seguintes componentes do Lync Server são compatíveis com o aplicativo de anúncio:</span><span class="sxs-lookup"><span data-stu-id="50de3-110">The following Lync Server components support the Announcement application:</span></span>

  - <span data-ttu-id="50de3-111">**Serviço de aplicativo**   O serviço de aplicativo fornece uma plataforma para implantação, hospedagem e gerenciamento de aplicativos de comunicação unificada.</span><span class="sxs-lookup"><span data-stu-id="50de3-111">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications.</span></span> <span data-ttu-id="50de3-112">O serviço de aplicativo é instalado automaticamente em todos os servidores front-end em um pool Front-end e em cada servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="50de3-112">Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="50de3-113">**Aplicativo de grupo de resposta**   O aplicativo de grupo de resposta é um dos aplicativos de comunicação unificada hospedados pelo serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="50de3-113">**Response Group application**   The Response Group application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="50de3-114">Quando um intervalo de números de telefone não atribuído está configurado para direcionar para um comunicado, o aplicativo grupo de resposta é necessário para direcionar as chamadas feitas para o número de telefone.</span><span class="sxs-lookup"><span data-stu-id="50de3-114">When an unassigned phone number range is configured to route to an announcement, the Response Group application is required to route the calls made to the phone number.</span></span> <span data-ttu-id="50de3-115">(O aplicativo de grupo de resposta não será necessário se todos os intervalos estiverem configurados para direcionar a UM (a) Unificação de mensagens do Exchange.)</span><span class="sxs-lookup"><span data-stu-id="50de3-115">(Response Group application is not required if all the ranges are configured to route to Exchange Unified Messaging (UM).)</span></span>

  - <span data-ttu-id="50de3-116">**Arquivos de áudio**   Os arquivos de áudio são usados para os comunicados.</span><span class="sxs-lookup"><span data-stu-id="50de3-116">**Audio files**   Audio files are used for the announcements.</span></span>

  - <span data-ttu-id="50de3-117">**Repositório de arquivos**   O aplicativo de anúncio usa o repositório de arquivos para armazenar seus arquivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="50de3-117">**File Store**   The Announcement application uses File Store to store its audio files.</span></span>

  - <span data-ttu-id="50de3-118">**Painel de controle do Lync Server**   Você pode usar o painel de controle do Lync Server para configurar a tabela numérica não atribuída.</span><span class="sxs-lookup"><span data-stu-id="50de3-118">**Lync Server Control Panel**   You can use Lync Server Control Panel to configure the unassigned number table.</span></span>

  - <span data-ttu-id="50de3-119">**Shell de gerenciamento do Lync Server**   Você pode usar cmdlets do Shell de gerenciamento do Lync Server para definir as configurações de anúncio e a tabela de números não atribuídos.</span><span class="sxs-lookup"><span data-stu-id="50de3-119">**Lync Server Management Shell**   You can use Lync Server Management Shell cmdlets to configure Announcement settings and the unassigned number table.</span></span>

<span data-ttu-id="50de3-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="50de3-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

