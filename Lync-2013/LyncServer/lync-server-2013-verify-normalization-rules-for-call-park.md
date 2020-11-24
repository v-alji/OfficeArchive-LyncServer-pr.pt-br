---
title: 'Lync Server 2013: verificar regras de normalização para estacionamento de chamada'
description: 'Lync Server 2013: Verifique as regras de normalização para o parque da chamada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify normalization rules for Call Park
ms:assetid: deaa170f-041e-45cb-8eab-f02931ab541e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398981(v=OCS.15)
ms:contentKeyID: 48185646
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2ac4c15091141e3069e7b77533d0e4148459f570
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390309"
---
# <a name="verify-normalization-rules-for-call-park-in-lync-server-2013"></a><span data-ttu-id="ee366-103">Verificar as regras de normalização para o parque de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee366-103">Verify normalization rules for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee366-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee366-104">

<span> </span></span></span>

<span data-ttu-id="ee366-105">_**Tópico da última modificação:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="ee366-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="ee366-106">As órbitas do estacionamento de chamada não devem ser normalizadas.</span><span class="sxs-lookup"><span data-stu-id="ee366-106">Call Park orbits must not be normalized.</span></span> <span data-ttu-id="ee366-107">Verifique seus planos de discagem para garantir que seus números de órbita não estão normalizados.</span><span class="sxs-lookup"><span data-stu-id="ee366-107">Check your dial plans to be sure that your orbit numbers are not normalized.</span></span> <span data-ttu-id="ee366-108">Se você deve criar uma regra de normalização adicional para impedir que as órbitas sejam normalizadas, siga o procedimento em [criar um plano de discagem no Lync Server 2013](lync-server-2013-create-a-dial-plan.md) para definir uma nova regra de normalização, para que o **padrão correspondente** identifique o intervalo de órbita e o **padrão de tradução** seja **$1**.</span><span class="sxs-lookup"><span data-stu-id="ee366-108">If you must create an additional normalization rule to prevent your orbits from being normalized, follow the procedure in [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md) to define a new normalization rule, so that **Pattern to match** identifies the orbit range and **Translation pattern** is **$1**.</span></span> <span data-ttu-id="ee366-109">Por exemplo, se a faixa de texto da sua chamada é 7000 – 7999, o **padrão a ser correspondido** é **^ (7 \\ d {3} ) $** e o **padrão de tradução** é **$1**.</span><span class="sxs-lookup"><span data-stu-id="ee366-109">For example, if your Call Park orbit range is 7000 – 7999, the **Pattern to match** is **^(7\\d{3})$** and **Translation pattern** is **$1**.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ee366-110">Certifique-se de que a regra de normalização padrão em seu plano de discagem não contém o <STRONG>^(\d\*)</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ee366-110">Be sure that the default normalization rule in your dial plans does not contain <STRONG>^(\d\*)</STRONG>.</span></span> <span data-ttu-id="ee366-111">Caso contrário, sua regra de normalização do estacionamento de chamada nunca será executada.</span><span class="sxs-lookup"><span data-stu-id="ee366-111">Otherwise, your Call Park normalization rule will never run.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ee366-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee366-112">See Also</span></span>


[<span data-ttu-id="ee366-113">Criar um plano de discagem no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee366-113">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)  
  

<span data-ttu-id="ee366-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee366-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

