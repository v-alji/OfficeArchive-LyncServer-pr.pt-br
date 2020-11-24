---
title: 'Lync Server 2013: configurar números de grupo de recebimento de chamadas'
description: 'Lync Server 2013: configurar números de grupo de recebimento de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure call pickup group numbers
ms:assetid: 5cc67f0b-d70d-446a-8db1-befda8671121
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945631(v=OCS.15)
ms:contentKeyID: 51541479
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ddffae2e385ce6c3fd7a700a9b94a89b1b6679f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389709"
---
# <a name="configure-call-pickup-group-numbers-in-lync-server-2013"></a><span data-ttu-id="20811-103">Configurar números de grupo de recebimento de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20811-103">Configure call pickup group numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20811-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20811-104">

<span> </span></span></span>

<span data-ttu-id="20811-105">_**Tópico da última modificação:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="20811-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="20811-106">O recebimento de chamadas em grupo é baseado no aplicativo parque de chamadas.</span><span class="sxs-lookup"><span data-stu-id="20811-106">Group Call Pickup is based on the Call Park application.</span></span> <span data-ttu-id="20811-107">Ao implantar o recurso de recebimento de chamadas em grupo, configure a tabela órbita do estacionamento de chamada com intervalos de números de telefone designados como números de grupo de recebimento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="20811-107">When you deploy Group Call Pickup, you configure the call park orbit table with ranges of phone numbers that are designated as call pickup group numbers.</span></span> <span data-ttu-id="20811-108">Esses números do grupo são aqueles que os usuários discam para receber chamadas que estão tocando para outro usuário.</span><span class="sxs-lookup"><span data-stu-id="20811-108">These group numbers are the numbers that users dial to pick up calls that are ringing for another user.</span></span>

<span data-ttu-id="20811-109">Como os números da órbita de estacionamento de chamada, os números do grupo de recebimento de chamada precisam ser extensões virtuais, sem nenhum usuário ou telefone atribuído.</span><span class="sxs-lookup"><span data-stu-id="20811-109">Like call park orbit numbers, call pickup group numbers need to be virtual extensions that have no user or phone assigned to them.</span></span> <span data-ttu-id="20811-110">Cada pool de front-ends onde você implanta o recebimento de chamadas em grupo pode ter um ou mais intervalos de números de grupo de recebimento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="20811-110">Each Front End pool where you deploy Group Call Pickup can have one or more ranges of call pickup group numbers.</span></span> <span data-ttu-id="20811-111">Os intervalos de números de grupo devem ser globalmente exclusivos na implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="20811-111">The group number ranges must be globally unique across the Lync Server deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="20811-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="20811-112">In This Section</span></span>

[<span data-ttu-id="20811-113">Create or modify a Group Call Pickup number range in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20811-113">Create or modify a Group Call Pickup number range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-group-call-pickup-number-range.md)

<span data-ttu-id="20811-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20811-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

