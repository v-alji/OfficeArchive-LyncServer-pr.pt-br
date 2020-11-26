---
title: 'Lync Server 2013: Configurar a tabela de órbita de Estacionamento de Chamadas'
description: 'Lync Server 2013: configurar a tabela órbita do parque de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the Call Park orbit table
ms:assetid: e5cc0c19-7b2c-48e7-a21d-cfb23c842f0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399020(v=OCS.15)
ms:contentKeyID: 48185666
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ce9fb35c2958a426888d83d075064c88ddae4bfa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433630"
---
# <a name="configure-the-call-park-orbit-table-in-lync-server-2013"></a><span data-ttu-id="51018-103">Configurar a tabela de órbita de Estacionamento de Chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51018-103">Configure the Call Park orbit table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="51018-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="51018-104">

<span> </span></span></span>

<span data-ttu-id="51018-105">_**Tópico da última modificação:** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="51018-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="51018-106">O parque de chamadas usa órbitas para chamadas de estacionamento.</span><span class="sxs-lookup"><span data-stu-id="51018-106">Call Park uses orbits for parking calls.</span></span> <span data-ttu-id="51018-107">Para que os usuários possam estacionar e recuperar chamadas, você deve configurar a tabela órbita do parque de chamadas.</span><span class="sxs-lookup"><span data-stu-id="51018-107">Before users can park and retrieve calls, you must configure the Call Park orbit table.</span></span> <span data-ttu-id="51018-108">Você precisa especificar os intervalos de números de ramal (órbitas) que a sua organização irá reservar para fazer chamadas de estacionamento e definir o roteamento para esses intervalos especificando qual o pool do estacionamento de chamadas manipula cada intervalo.</span><span class="sxs-lookup"><span data-stu-id="51018-108">You need to specify the ranges of extension numbers (orbits) that your organization will reserve for parking calls and define the routing for those ranges by specifying which Call Park pool handles each range.</span></span> <span data-ttu-id="51018-109">Quando você define intervalos de órbita, a meta é ter órbitas suficientes para que qualquer uma das órbitas não seja reutilizada rapidamente, mas não muitas órbitas que você limite o número de extensões disponíveis para usuários ou outros serviços.</span><span class="sxs-lookup"><span data-stu-id="51018-109">When you define orbit ranges, the goal is to have enough orbits so that any one orbit is not reused too quickly, but not so many orbits that you limit the number of extensions available for users or other services.</span></span> <span data-ttu-id="51018-110">Você pode criar várias faixas órbitas do estacionamento de chamada para cada pool do Lync Server onde o aplicativo de estacionamento de chamada é implantado.</span><span class="sxs-lookup"><span data-stu-id="51018-110">You can create multiple Call Park orbit ranges for each Lync Server pool where the Call Park application is deployed.</span></span> <span data-ttu-id="51018-111">Cada faixa de opções de estacionamento de chamadas deve ter um nome globalmente exclusivo e um conjunto exclusivo de extensões.</span><span class="sxs-lookup"><span data-stu-id="51018-111">Each Call Park orbit range must have a globally unique name and a unique set of extensions.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="51018-p102">Normalmente, um intervalo de órbitas engloba 100 órbitas ou menos. Cada intervalo pode ser muito maior, contanto que seja menor do que o máximo de 10.000 órbitas por intervalo e tenha menos de 50.000 órbitas por pool. Se o intervalo for muito pequeno, as órbitas serão reutilizadas mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="51018-p102">An orbit range typically encompasses 100 or fewer orbits. Each range can be much larger, as long as it is smaller than the maximum of 10,000 orbits per range and you have fewer than 50,000 orbits per pool. If a range is too small, the orbits are reused more quickly.</span></span>



</div>

<span data-ttu-id="51018-115">Use blocos de extensões virtuais (extensões sem um usuário ou telefone atribuído a elas) para intervalos de órbita.</span><span class="sxs-lookup"><span data-stu-id="51018-115">Use blocks of virtual extensions (extensions that have no user or phone assigned to them) for your orbit ranges.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="51018-116">Não há suporte para a atribuição de números do Direct Inward Dialing (DID) como números órbitas na tabela órbita do estacionamento de chamada.</span><span class="sxs-lookup"><span data-stu-id="51018-116">Assigning Direct Inward Dialing (DID) numbers as orbit numbers in the Call Park orbit table is not supported.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="51018-117">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="51018-117">In This Section</span></span>

[<span data-ttu-id="51018-118">Criar ou modificar uma faixa de opções do parque de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51018-118">Create or modify a Call Park orbit range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)

<span data-ttu-id="51018-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="51018-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

