---
title: 'Lync Server 2013: componentes usados pelo recurso de recebimento de chamadas em grupo'
description: 'Lync Server 2013: componentes usados por retirada de chamadas em grupo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Group Call Pickup
ms:assetid: 45db2f23-d486-4b20-a8cf-7b48a1f9fd3a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945625(v=OCS.15)
ms:contentKeyID: 51541470
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 517f75dcbac8bfed0e749c061a9696b7667e10ed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389897"
---
# <a name="components-used-by-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="7bef5-103">Componentes usados pela retirada de chamadas em grupo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7bef5-103">Components used by Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7bef5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7bef5-104">

<span> </span></span></span>

<span data-ttu-id="7bef5-105">_**Tópico da última modificação:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="7bef5-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="7bef5-106">O recebimento de chamadas em grupo é implantado automaticamente quando você implanta o Enterprise Voice e o aplicativo de estacionamento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="7bef5-106">Group Call Pickup is automatically deployed when you deploy Enterprise Voice and the Call Park application.</span></span> <span data-ttu-id="7bef5-107">Você permite o recebimento de chamadas em grupo Configurando a tabela órbita de estacionamento de chamada com intervalos separados de números designados como números de grupo de recebimento de chamadas e, em seguida, atribuindo aos usuários chamadas para grupos de retirada e habilitando os usuários para a retirada de chamadas em grupo.</span><span class="sxs-lookup"><span data-stu-id="7bef5-107">You enable Group Call Pickup by configuring the Call Park orbit table with separate ranges of numbers designated as call pickup group numbers, and then by assigning users to call pickup groups and enabling the users for Group Call Pickup.</span></span> <span data-ttu-id="7bef5-108">Os seguintes componentes do Lync Server suportam o recebimento de chamadas em grupo:</span><span class="sxs-lookup"><span data-stu-id="7bef5-108">The following Lync Server components support Group Call Pickup:</span></span>

  - <span data-ttu-id="7bef5-109">**Serviço de aplicativo**   O serviço de aplicativo fornece uma plataforma para implantação, hospedagem e gerenciamento de aplicativos de comunicação unificada, como o aplicativo de estacionamento de chamada.</span><span class="sxs-lookup"><span data-stu-id="7bef5-109">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications, such as the Call Park application.</span></span> <span data-ttu-id="7bef5-110">O serviço de aplicativo é instalado automaticamente em todos os servidores front-end em um pool Front-end e em cada servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="7bef5-110">Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="7bef5-111">**Aplicativo de estacionamento de chamadas**   O aplicativo de estacionamento de chamadas é um dos aplicativos de comunicação unificada hospedados pelo serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7bef5-111">**Call Park application**   The Call Park application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="7bef5-112">O recebimento de chamadas em grupo é baseado no aplicativo parque de chamadas.</span><span class="sxs-lookup"><span data-stu-id="7bef5-112">Group Call Pickup is based on the Call Park application.</span></span>

  - <span data-ttu-id="7bef5-113">**Shell de gerenciamento do Lync Server**   Você usa o Shell de gerenciamento do Lync Server para gerenciar grupos de recebimento de chamadas em grupo.</span><span class="sxs-lookup"><span data-stu-id="7bef5-113">**Lync Server Management Shell**   You use Lync Server Management Shell to manage Group Call Pickup groups.</span></span>

  - <span data-ttu-id="7bef5-114">**Ferramenta SEFAUtil Resource Kit**   Use o utilitário de ativação de recursos de extensão secundária (SEFAUtil) para atribuir usuários a um grupo de recebimento de chamadas e habilitar ou desabilitar o recebimento de chamadas para usuários.</span><span class="sxs-lookup"><span data-stu-id="7bef5-114">**SEFAUtil resource kit tool**   You use the secondary extension feature activation utility (SEFAUtil) to assign users to a call pickup group and to enable or disable call pickup for users.</span></span>

<span data-ttu-id="7bef5-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7bef5-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

