---
title: 'Lync Server 2013: Roteamento entre troncos'
description: 'Lync Server 2013: roteamento de intertronco.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Intertrunk routing
ms:assetid: d3a33b4a-8bf4-4a8c-a371-8ef79e740780
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205272(v=OCS.15)
ms:contentKeyID: 48185442
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 30c838ee94a2df0807195c172d7e2a3a393523af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426762"
---
# <a name="intertrunk-routing-in-lync-server-2013"></a><span data-ttu-id="e4901-103">Roteamento entre troncos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e4901-103">Intertrunk routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e4901-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e4901-104">

<span> </span></span></span>

<span data-ttu-id="e4901-105">_**Tópico da última modificação:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="e4901-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="e4901-106">O Lync Server 2013 pode interconectar um IP-PBX a um gateway PSTN (rede telefônica pública comutada) para que as chamadas de um telefone PBX possam ser roteadas para a PSTN, e chamadas PSTN de entrada possam ser roteadas para um telefone PBX (central privada de intercâmbio).</span><span class="sxs-lookup"><span data-stu-id="e4901-106">Lync Server 2013 can interconnect an IP-PBX to a public switched telephone network (PSTN) gateway so that calls from a PBX phone can be routed to the PSTN, and incoming PSTN calls can be routed to a private branch exchange (PBX) phone.</span></span> <span data-ttu-id="e4901-107">Da mesma forma, o Lync Server 2013 pode interconectar dois ou mais sistemas de PBX IP para que as chamadas possam ser feitas e recebidas entre telefones PBX dos diferentes sistemas de IP-PBX.</span><span class="sxs-lookup"><span data-stu-id="e4901-107">Similarly, Lync Server 2013 can interconnect two or more IP-PBX systems so that calls can be placed and received between PBX phones from the different IP-PBX systems.</span></span>

<span data-ttu-id="e4901-108">Este recurso de roteamento de intertronco pode ser configurado usando o cmdlet do Shell de gerenciamento do Lync Server, **set-CsTrunkConfiguration**, com o novo parâmetro PstnUsages.</span><span class="sxs-lookup"><span data-stu-id="e4901-108">This intertrunk routing feature can be configured by using the Lync Server Management Shell cmdlet, **Set-CsTrunkConfiguration**, with the new parameter, PstnUsages.</span></span> <span data-ttu-id="e4901-109">Esse parâmetro especifica o conjunto de registros de uso PSTN a ser usado.</span><span class="sxs-lookup"><span data-stu-id="e4901-109">This parameter specifies the set of PSTN usage records to use.</span></span> <span data-ttu-id="e4901-110">Um tronco usa esse uso de PSTN para determinar uma rota e para direcionar todas as chamadas de entrada de acordo.</span><span class="sxs-lookup"><span data-stu-id="e4901-110">A trunk uses this PSTN usage to determine a route and to route all incoming calls accordingly.</span></span>

    Set-CsTrunkConfiguration -Identity <TrunkId> -PstnUsages @{add="<UsageString>"}

<span data-ttu-id="e4901-111">O diagrama a seguir ilustra o Lync Server 2013 fornecendo interconectividade entre um gateway PSTN e um IP-PBX.</span><span class="sxs-lookup"><span data-stu-id="e4901-111">The following diagram illustrates Lync Server 2013 providing interconnectivity between a PSTN gateway and an IP-PBX.</span></span>

<span data-ttu-id="e4901-112">**Roteamento entre troncos entre gateway e PBX IP**</span><span class="sxs-lookup"><span data-stu-id="e4901-112">**Intertrunk routing between gateway and IP PBX**</span></span>

<span data-ttu-id="e4901-113">![O servidor do Lync conectando o diagrama PSTN gateway/IP-PBX](images/JJ721940.cc3858ca-2ee3-4d51-8a51-db078366b50b(OCS.15).jpg "O servidor do Lync conectando o diagrama PSTN gateway/IP-PBX")</span><span class="sxs-lookup"><span data-stu-id="e4901-113">![Lync Server connecting PSTN gateway/IP-PBX diagram](images/JJ721940.cc3858ca-2ee3-4d51-8a51-db078366b50b(OCS.15).jpg "Lync Server connecting PSTN gateway/IP-PBX diagram")</span></span>

<span data-ttu-id="e4901-114">O diagrama a seguir ilustra o Lync Server 2013 interconectando dois sistemas de PBX IP.</span><span class="sxs-lookup"><span data-stu-id="e4901-114">The following diagram illustrates Lync Server 2013 interconnecting two IP-PBX systems.</span></span>

<span data-ttu-id="e4901-115">**Roteamento entre troncos entre dois PBXs de IP**</span><span class="sxs-lookup"><span data-stu-id="e4901-115">**Intertrunk routing between two IP PBXs**</span></span>

<span data-ttu-id="e4901-116">![Diagrama de sistemas IP-PAX de interconexão do Lync Server](images/JJ721940.6ba18ec9-df70-498a-9cf7-7fc41e5ec432(OCS.15).jpg "Diagrama de sistemas IP-PAX de interconexão do Lync Server")</span><span class="sxs-lookup"><span data-stu-id="e4901-116">![Lync Server interconnecting IP-PAX systems diagram](images/JJ721940.6ba18ec9-df70-498a-9cf7-7fc41e5ec432(OCS.15).jpg "Lync Server interconnecting IP-PAX systems diagram")</span></span>

<span data-ttu-id="e4901-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e4901-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

