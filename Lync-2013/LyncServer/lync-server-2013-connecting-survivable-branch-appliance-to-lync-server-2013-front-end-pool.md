---
title: Conectando Aparelho de Filial Persistente ao pool Front-End do Lync Server 2013
description: Conectando um aparelho de ramificação sobreviventes ao pool de front-end do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Connecting Survivable Branch Appliance to Lync Server 2013 Front End pool
ms:assetid: 3c7ca33f-5295-4d82-9152-41d8bc6f35cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688026(v=OCS.15)
ms:contentKeyID: 49733616
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ef917d3db6a1d653ac716d6c078e1df240fb31d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432258"
---
# <a name="connecting-survivable-branch-appliance-to-lync-server-2013-front-end-pool"></a><span data-ttu-id="d4288-103">Conectando Aparelho de Filial Persistente ao pool Front-End do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d4288-103">Connecting Survivable Branch Appliance to Lync Server 2013 Front End pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d4288-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d4288-104">

<span> </span></span></span>

<span data-ttu-id="d4288-105">_**Tópico da última modificação:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="d4288-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="d4288-106">Cada aplicativo de ramificação sobreviventes (SBA) está associado a um pool de front-end, que atua como um registrador de backup para o SBA.</span><span class="sxs-lookup"><span data-stu-id="d4288-106">Every Survivable Branch Appliance (SBA) is associated with a Front End pool, which serves as a backup Registrar for the SBA.</span></span> <span data-ttu-id="d4288-107">Quando o pool de front-ends é atualizado para o Lync Server 2013, o SBA deve ser desassociado do pool de front-ends enquanto o pool de front-end é atualizado.</span><span class="sxs-lookup"><span data-stu-id="d4288-107">When the Front End pool is upgraded to Lync Server 2013, the SBA must be disassociated from the Front End pool while the Front End pool is upgraded.</span></span> <span data-ttu-id="d4288-108">Depois que o pool de front-ends é atualizado, o SBA pode ser associado novamente ao pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="d4288-108">After the Front End pool is upgraded, the SBA can be reassociated with the Front End pool.</span></span> <span data-ttu-id="d4288-109">Isso envolve excluir o SBA da topologia no construtor de topologias e, em seguida, adicionar SBA, novamente, ao construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="d4288-109">This involves deleting the SBA from the topology in Topology Builder and then adding the SBA, again, to Topology Builder.</span></span> <span data-ttu-id="d4288-110">Os usuários hospedados no SBA devem ser movidos para outro pool de front-end antes da remoção do SBA da topologia.</span><span class="sxs-lookup"><span data-stu-id="d4288-110">Users homed on the SBA must be moved to another Front End pool before removing the SBA from the topology.</span></span> <span data-ttu-id="d4288-111">Depois que o SBA é adicionado novamente à topologia, esses usuários podem retornar ao SBA.</span><span class="sxs-lookup"><span data-stu-id="d4288-111">After the SBA is added back to the topology, those users can be moved back to the SBA.</span></span>

<span data-ttu-id="d4288-112">Estas etapas estão resumidas abaixo:</span><span class="sxs-lookup"><span data-stu-id="d4288-112">These steps are summarized below:</span></span>

1.  <span data-ttu-id="d4288-113">Mova os usuários da ramificação hospedados no SBA para outro pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="d4288-113">Move branch users homed on SBA to another Front End pool.</span></span>

2.  <span data-ttu-id="d4288-114">Remova o SBA da sua topologia para desassociar o pool de front-end existente como registrador de backup.</span><span class="sxs-lookup"><span data-stu-id="d4288-114">Remove SBA from your topology to disassociate the existing Front End pool as the backup Registrar.</span></span>

3.  <span data-ttu-id="d4288-115">Atualize o pool de front-ends para o Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d4288-115">Upgrade Front End pool to Microsoft Lync Server 2013.</span></span>

4.  <span data-ttu-id="d4288-116">Adicione SBA de volta à sua topologia.</span><span class="sxs-lookup"><span data-stu-id="d4288-116">Add SBA back into your topology.</span></span>

5.  <span data-ttu-id="d4288-117">Associe o novo pool de front-ends ao SBA como um registrador de backup.</span><span class="sxs-lookup"><span data-stu-id="d4288-117">Associate the new Front End pool to the SBA as a backup Registrar.</span></span>

6.  <span data-ttu-id="d4288-118">Mova os usuários da ramificação de volta para o SBA.</span><span class="sxs-lookup"><span data-stu-id="d4288-118">Move branch users back to the SBA.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d4288-119">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d4288-119">In This Section</span></span>

  - [<span data-ttu-id="d4288-120">Adicionar Aparelho de Filial Persistente do Lync Server 2013 a sua topologia</span><span class="sxs-lookup"><span data-stu-id="d4288-120">Add Lync Server 2013 Survivable Branch Appliance branch site to your topology</span></span>](lync-server-2013-add-lync-server-2013-survivable-branch-appliance-branch-site-to-your-topology.md)

  - [<span data-ttu-id="d4288-121">Adicionar site de Aparelho de Filial Persistente do Lync Server 2010 a sua topologia</span><span class="sxs-lookup"><span data-stu-id="d4288-121">Add Lync Server 2010 Survivable Branch Appliance branch site to your topology</span></span>](lync-server-2013-add-lync-server-2010-survivable-branch-appliance-branch-site-to-your-topology.md)

<span data-ttu-id="d4288-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d4288-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

