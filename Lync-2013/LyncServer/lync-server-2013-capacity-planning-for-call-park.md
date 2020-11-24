---
title: 'Lync Server 2013: Planejamento de capacidade para Estacionamento de Chamada'
description: 'Lync Server 2013: planejamento de capacidade para estacionamento de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning for Call Park
ms:assetid: 75520310-760a-4b1b-bcc1-4d724d13f87a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg416493(v=OCS.15)
ms:contentKeyID: 48184529
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 053a6dabad9d10540e84e9e4f43de09057c295f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390373"
---
# <a name="capacity-planning-for-call-park-in-lync-server-2013"></a><span data-ttu-id="66c40-103">Planejamento de capacidade para Estacionamento de Chamada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="66c40-103">Capacity planning for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="66c40-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="66c40-104">

<span> </span></span></span>

<span data-ttu-id="66c40-105">_**Tópico da última modificação:** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="66c40-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<div id="sectionSection0" class="section">

<span data-ttu-id="66c40-106">A tabela a seguir descreve o modelo de usuário do parque de chamadas que você pode usar como base para requisitos de planejamento de capacidade.</span><span class="sxs-lookup"><span data-stu-id="66c40-106">The following table describes the Call Park user model that you can use as the basis for capacity planning requirements.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="66c40-107">Lembre-se de que, para o planejamento da capacidade de recuperação de desastres, cada pool de um pool emparelhado deve ser capaz de manipular as cargas de trabalho para serviços de estacionamento de chamadas em ambos os pools.</span><span class="sxs-lookup"><span data-stu-id="66c40-107">Keep in mind that, for disaster recovery capacity planning, each pool of a paired pool should be able to handle the workloads for Call Park services in both pools.</span></span>



</div>

### <a name="call-park-user-model"></a><span data-ttu-id="66c40-108">Modelo de usuário do estacionamento de chamada</span><span class="sxs-lookup"><span data-stu-id="66c40-108">Call Park User Model</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66c40-109">Indicador</span><span class="sxs-lookup"><span data-stu-id="66c40-109">Metric</span></span></th>
<th><span data-ttu-id="66c40-110">Por pool de front-end (com 8 servidores front end)</span><span class="sxs-lookup"><span data-stu-id="66c40-110">Per Front End pool (with 8 Front End Servers)</span></span></th>
<th><span data-ttu-id="66c40-111">Por servidor padrão da edição</span><span class="sxs-lookup"><span data-stu-id="66c40-111">Per Standard Edition server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66c40-112">Taxa de estacionamento</span><span class="sxs-lookup"><span data-stu-id="66c40-112">Park rate</span></span></p></td>
<td><p><span data-ttu-id="66c40-113">8 por minuto</span><span class="sxs-lookup"><span data-stu-id="66c40-113">8 per minute</span></span></p></td>
<td><p><span data-ttu-id="66c40-114">1 por minuto</span><span class="sxs-lookup"><span data-stu-id="66c40-114">1 per minute</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66c40-115">Recuperar a taxa de chamada estacionada</span><span class="sxs-lookup"><span data-stu-id="66c40-115">Retrieve parked call rate</span></span></p></td>
<td><p><span data-ttu-id="66c40-116">8 por minuto</span><span class="sxs-lookup"><span data-stu-id="66c40-116">8 per minute</span></span></p></td>
<td><p><span data-ttu-id="66c40-117">1 por minuto</span><span class="sxs-lookup"><span data-stu-id="66c40-117">1 per minute</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66c40-118">Duração média do estacionamento</span><span class="sxs-lookup"><span data-stu-id="66c40-118">Average park duration</span></span></p></td>
<td><p><span data-ttu-id="66c40-119">60 segundos</span><span class="sxs-lookup"><span data-stu-id="66c40-119">60 seconds</span></span></p></td>
<td><p><span data-ttu-id="66c40-120">60 segundos</span><span class="sxs-lookup"><span data-stu-id="66c40-120">60 seconds</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="66c40-121">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="66c40-121">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

