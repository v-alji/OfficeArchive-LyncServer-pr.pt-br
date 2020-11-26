---
title: 'Lync Server 2013: configurar regiões de rede para o CAC'
description: 'Lync Server 2013: configurar regiões de rede para o CAC.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure network regions for CAC
ms:assetid: ea3ff988-dd5a-4bc4-bec5-39a0fb09793a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399051(v=OCS.15)
ms:contentKeyID: 48185906
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f016e0c943963ea4ce9739bd486c6996da502e73
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433868"
---
# <a name="configure-network-regions-for-cac-in-lync-server-2013"></a><span data-ttu-id="bae90-103">Configurar regiões de rede para o CAC no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bae90-103">Configure network regions for CAC in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bae90-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bae90-104">

<span> </span></span></span>

<span data-ttu-id="bae90-105">_**Tópico da última modificação:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="bae90-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="bae90-106">Se você já tiver criado regiões de rede para o E9-1-1 ou bypass de mídia, poderá modificar as regiões de rede existentes adicionando configurações específicas para o controle de admissão de chamadas (CAC) usando o cmdlet <STRONG>set-CsNetworkRegion</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="bae90-106">If you have already created network regions for E9-1-1 or media bypass, you can modify the existing network regions by adding settings specific to call admission control (CAC) by using the <STRONG>Set-CsNetworkRegion</STRONG> cmdlet.</span></span> <span data-ttu-id="bae90-107">Para obter um exemplo de como modificar uma região de rede, consulte <A href="lync-server-2013-create-or-modify-a-network-region.md">criar ou modificar uma região de rede no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="bae90-107">For an example of how to modify a network region, see <A href="lync-server-2013-create-or-modify-a-network-region.md">Create or modify a network region in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="bae90-108">*Regiões de rede* são os hubs de rede ou backbones usados na configuração do CAC, do E9-1 e do bypass de mídia.</span><span class="sxs-lookup"><span data-stu-id="bae90-108">*Network regions* are the network hubs or backbones that are used in configuring CAC, E9-1-1, and media bypass.</span></span> <span data-ttu-id="bae90-109">Use o procedimento a seguir para criar regiões de rede alinhadas às regiões de rede na topologia de rede de exemplo para o CAC.</span><span class="sxs-lookup"><span data-stu-id="bae90-109">Use the following procedure to create network regions that align to network regions in the example network topology for CAC.</span></span> <span data-ttu-id="bae90-110">Para ver o exemplo de topologia de rede, consulte [exemplo: reunir seus requisitos de controle de admissão de chamadas no Lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="bae90-110">To view the example network topology, see [Example: Gathering your requirements for call admission control in Lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) in the Planning documentation.</span></span>

<span data-ttu-id="bae90-111">O exemplo de topologia de rede para o CAC tem três regiões: América do Norte, EMEA e Ásia-Pacífico.</span><span class="sxs-lookup"><span data-stu-id="bae90-111">The example network topology for CAC has three regions: North America, EMEA, and APAC.</span></span> <span data-ttu-id="bae90-112">Cada região tem um site central especificado.</span><span class="sxs-lookup"><span data-stu-id="bae90-112">Each region has a specified central site.</span></span> <span data-ttu-id="bae90-113">Para a região da América do Norte, o site central designado é chamado de CHICAGO.</span><span class="sxs-lookup"><span data-stu-id="bae90-113">For the North America region, the designated central site is named CHICAGO.</span></span> <span data-ttu-id="bae90-114">O procedimento a seguir mostra um exemplo de como você pode usar o cmdlet **New-CsNetworkRegion** para criar a região da América do Norte.</span><span class="sxs-lookup"><span data-stu-id="bae90-114">The following procedure shows an example of how you can use the **New-CsNetworkRegion** cmdlet to create the North America region.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bae90-115">No procedimento a seguir, o Shell de gerenciamento do Lync Server é usado para criar uma região de rede.</span><span class="sxs-lookup"><span data-stu-id="bae90-115">In the following procedure, Lync Server Management Shell is used to create a network region.</span></span> <span data-ttu-id="bae90-116">Para obter detalhes sobre como usar o painel de controle do Lync Server para criar uma região de rede, consulte <A href="lync-server-2013-create-or-modify-a-network-region.md">criar ou modificar uma região de rede no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="bae90-116">For details about using Lync Server Control Panel to create a network region, see <A href="lync-server-2013-create-or-modify-a-network-region.md">Create or modify a network region in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-create-a-network-region-for-call-admission-control"></a><span data-ttu-id="bae90-117">Para criar uma região de rede para o controle de admissão de chamadas</span><span class="sxs-lookup"><span data-stu-id="bae90-117">To create a network region for call admission control</span></span>

1.  <span data-ttu-id="bae90-118">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="bae90-118">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="bae90-119">Para cada região que você precisa criar, execute o cmdlet **New-CsNetworkRegion** .</span><span class="sxs-lookup"><span data-stu-id="bae90-119">For each region that you need to create, run the **New-CsNetworkRegion** cmdlet.</span></span> <span data-ttu-id="bae90-120">Por exemplo, para criar a região da América do Norte, execute:</span><span class="sxs-lookup"><span data-stu-id="bae90-120">For example, to create the North America region, run:</span></span>
    
        New-CsNetworkRegion -Identity NorthAmerica -CentralSite CHICAGO -Description "All North America Locations"

3.  <span data-ttu-id="bae90-121">Repita a etapa 2 para criar as regiões de rede, EMEA e Ásia-Pacífico.</span><span class="sxs-lookup"><span data-stu-id="bae90-121">Repeat step 2 to create the network regions, EMEA and APAC.</span></span>

<span data-ttu-id="bae90-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bae90-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

