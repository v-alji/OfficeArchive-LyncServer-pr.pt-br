---
title: Opções de emparelhamento de pool compatível com o Lync Server 2013 e práticas recomendadas
description: Opções de emparelhamento de pool compatível com o Lync Server 2013 e práticas recomendadas.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported pool pairing options and best practices
ms:assetid: 142caf34-0f20-47f3-9d32-ce25ab622fad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204697(v=OCS.15)
ms:contentKeyID: 48183478
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 76d0f8331c0b6998008efff8af70ae3c4b43a9c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441414"
---
# <a name="supported-pool-pairing-options-and-best-practices-for-lync-server-2013"></a><span data-ttu-id="12336-103">Opções de emparelhamento de pool compatível e práticas recomendadas para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="12336-103">Supported pool pairing options and best practices for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="12336-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="12336-104">

<span> </span></span></span>

<span data-ttu-id="12336-105">_**Tópico da última modificação:** 2017-03-09_</span><span class="sxs-lookup"><span data-stu-id="12336-105">_**Topic Last Modified:** 2017-03-09_</span></span>

<span data-ttu-id="12336-106">Não há restrição na distância entre dois data centers que incluem pools front-ends emparelhados uns com os outros.</span><span class="sxs-lookup"><span data-stu-id="12336-106">There is no restriction on the distance between two data centers that are to include Front End pools paired with each other.</span></span> <span data-ttu-id="12336-107">Recomendamos que você use dois data centers na mesma região do mundo, com links de alta velocidade entre eles.</span><span class="sxs-lookup"><span data-stu-id="12336-107">We recommend that you use two data centers in the same world region, with high-speed links between them.</span></span> <span data-ttu-id="12336-108">É melhor se os dois data centers estiverem separados o suficiente para evitar um único desastre ao pressionar ambos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="12336-108">It is best if the two data centers are separated enough to avoid a single disaster hitting both at the same time.</span></span>

<span data-ttu-id="12336-109">Ter dois data centers nas regiões do mundo é possível, mas pode causar maior perda de dados devido à latência na replicação de dados.</span><span class="sxs-lookup"><span data-stu-id="12336-109">Having two data centers across world regions is possible, but could incur higher data loss due to latency in data replication.</span></span>

<span data-ttu-id="12336-110">Ao planejar quais pools emparelhar, você deve ter em mente que somente os emparelhamentos a seguir são aceitos:</span><span class="sxs-lookup"><span data-stu-id="12336-110">When you plan which pools to pair, you must keep in mind that only the following pairings are supported:</span></span>

  - <span data-ttu-id="12336-111">Os pools Enterprise Edition podem ser emparelhados somente com outros pools Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="12336-111">Enterprise Edition pools can be paired only with other Enterprise Edition pools.</span></span> <span data-ttu-id="12336-112">Da mesma forma, pools Standard Edition podem ser emparelhados somente com outros pools Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="12336-112">Similarly, Standard Edition pools can be paired only with other Standard Edition pools.</span></span>

  - <span data-ttu-id="12336-113">Os pools físicos somente podem ser emparelhados com outros pools físicos.</span><span class="sxs-lookup"><span data-stu-id="12336-113">Physical pools can be paired only with other physical pools.</span></span> <span data-ttu-id="12336-114">Da mesma forma, os pools virtuais somente podem ser emparelhados com outros pools virtuais.</span><span class="sxs-lookup"><span data-stu-id="12336-114">Similarly, virtual pools can be paired only with other virtual pools.</span></span>

  - <span data-ttu-id="12336-115">Os pools que estão emparelhados em conjunto devem estar executando o mesmo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="12336-115">Pools that are paired together must be running the same operating system.</span></span>

<span data-ttu-id="12336-p104">Nem o Construtor de Topologias nem a validação da topologia proibirão o emparelhamento de dois pools de uma forma que estas recomendações não sejam seguidas. Por exemplo, o Construtor de Topologias permite o emparelhamento de um pool Enterprise Edition com um pool Standard Edition. No entanto, estes tipos de emparelhamentos não são aceitos.</span><span class="sxs-lookup"><span data-stu-id="12336-p104">Neither Topology Builder nor topology validation will prohibit pairing two pools in a way that does not follow these recommendations. For example, Topology Builder allows you to pair an Enterprise Edition pool with a Standard Edition pool. However, these types of pairings are not supported.</span></span>

<span data-ttu-id="12336-119">Cada pool em um par deve ter capacidade para atender todos os usuários de ambos os pools no caso de um desastre.</span><span class="sxs-lookup"><span data-stu-id="12336-119">Each pool in a pair should have the capacity to serve all users from both pools in the event of a disaster.</span></span>

<span data-ttu-id="12336-120">Se você emparelhar pools da edição Enterprise, também é possível implementar a alta disponibilidade nos servidores back end, mas para pares de pools de edição padrão, somente os indicadores de recuperação de desastres estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="12336-120">If you pair Enterprise Edition pools, you can also implement high availability on the Back End Servers, but for pairs of Standard Edition pools only the disaster recovery measures are available.</span></span>

<span data-ttu-id="12336-121"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="12336-121"></div>

<span> </span>

</div>

</div>

</span></span></div>

