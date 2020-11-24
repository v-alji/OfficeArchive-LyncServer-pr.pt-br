---
title: 'Lync Server 2013: configurar intervalos de números de recebimento de chamadas em grupo'
description: 'Lync Server 2013: configurar intervalos de números de recebimento de chamadas em grupo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Group Call Pickup number ranges
ms:assetid: f15f75f6-f965-4558-b612-f40cecdd5d8c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945657(v=OCS.15)
ms:contentKeyID: 51541529
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f0594bd681a157b8ff479846b2f6f1964a09cad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390184"
---
# <a name="configure-group-call-pickup-number-ranges-in-lync-server-2013"></a><span data-ttu-id="621a3-103">Configurar intervalos de números de recebimento de chamadas em grupo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="621a3-103">Configure Group Call Pickup number ranges in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="621a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="621a3-104">

<span> </span></span></span>

<span data-ttu-id="621a3-105">_**Tópico da última modificação:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="621a3-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="621a3-106">O recebimento de chamadas em grupo é baseado no aplicativo parque de chamadas.</span><span class="sxs-lookup"><span data-stu-id="621a3-106">Group Call Pickup is based on the Call Park application.</span></span> <span data-ttu-id="621a3-107">Ao implantar o recurso de recebimento de chamadas em grupo, configure a tabela órbita do estacionamento de chamada com intervalos de números de telefone designados como números de grupo de recebimento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="621a3-107">When you deploy Group Call Pickup, you configure the call park orbit table with ranges of phone numbers that are designated as call pickup group numbers.</span></span> <span data-ttu-id="621a3-108">Esses números do grupo são aqueles que os usuários discam para receber chamadas que estão tocando para outro usuário.</span><span class="sxs-lookup"><span data-stu-id="621a3-108">These group numbers are the numbers that users dial to pick up calls that are ringing for another user.</span></span>

<span data-ttu-id="621a3-109">Como os números da órbita de estacionamento de chamada, os números do grupo de recebimento de chamada precisam ser extensões virtuais, sem nenhum usuário ou telefone atribuído.</span><span class="sxs-lookup"><span data-stu-id="621a3-109">Like call park orbit numbers, call pickup group numbers need to be virtual extensions that have no user or phone assigned to them.</span></span> <span data-ttu-id="621a3-110">Cada pool de front-ends onde você implanta o recebimento de chamadas em grupo pode ter um ou mais intervalos de números de grupo de recebimento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="621a3-110">Each Front End pool where you deploy Group Call Pickup can have one or more ranges of call pickup group numbers.</span></span> <span data-ttu-id="621a3-111">Os intervalos de números de grupo devem ser globalmente exclusivos na implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="621a3-111">The group number ranges must be globally unique across the Lync Server deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="621a3-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="621a3-112">In This Section</span></span>

  - [<span data-ttu-id="621a3-113">Create or modify a Group Call Pickup number range in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="621a3-113">Create or modify a Group Call Pickup number range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-group-call-pickup-number-range.md)

  - [<span data-ttu-id="621a3-114">Excluir um intervalo de números de retirada de chamadas em grupo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="621a3-114">Delete a Group Call Pickup number range in Lync Server 2013</span></span>](lync-server-2013-delete-a-group-call-pickup-number-range.md)

<span data-ttu-id="621a3-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="621a3-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

