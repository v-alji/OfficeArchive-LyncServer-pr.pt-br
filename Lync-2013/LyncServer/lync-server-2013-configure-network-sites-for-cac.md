---
title: 'Lync Server 2013: configurar sites de rede para o CAC'
description: 'Lync Server 2013: configurar sites de rede para o CAC.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure network sites for CAC
ms:assetid: afcea38f-5789-45ec-97af-c6e38364950c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412840(v=OCS.15)
ms:contentKeyID: 48185144
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 24adbbb1f5ee46618c685e072d519a338cb9b0af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433847"
---
# <a name="configure-network-sites-for-cac-in-lync-server-2013"></a><span data-ttu-id="440ce-103">Configurar sites de rede para o CAC no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="440ce-103">Configure network sites for CAC in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="440ce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="440ce-104">

<span> </span></span></span>

<span data-ttu-id="440ce-105">_**Tópico da última modificação:** 2012-09-05_</span><span class="sxs-lookup"><span data-stu-id="440ce-105">_**Topic Last Modified:** 2012-09-05_</span></span>

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="440ce-106">Se você já tiver criado sites de rede para o E9-1-1 ou bypass de mídia, poderá modificar os sites de rede existentes para aplicar um perfil de política de largura de banda usando o cmdlet <STRONG>set-CsNetworkSite</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="440ce-106">If you have already created network sites for E9-1-1 or media bypass, you can modify the existing network sites to apply a bandwidth policy profile by using the <STRONG>Set-CsNetworkSite</STRONG> cmdlet.</span></span> <span data-ttu-id="440ce-107">Para obter um exemplo de como modificar um site de rede, consulte <A href="lync-server-2013-create-or-modify-a-network-site.md">criar ou modificar um site de rede no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="440ce-107">For an example of how to modify a network site, see <A href="lync-server-2013-create-or-modify-a-network-site.md">Create or modify a network site in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="440ce-108">*Sites de rede* são os escritórios ou locais em cada região de rede do controle de admissão de chamadas (CAC), E9-1-1 e implantações de bypass de mídia.</span><span class="sxs-lookup"><span data-stu-id="440ce-108">*Network sites* are the offices or locations within each network region of call admission control (CAC), E9-1-1, and media bypass deployments.</span></span> <span data-ttu-id="440ce-109">Use os procedimentos a seguir para criar sites de rede alinhados a sites de rede na topologia de rede de exemplo para o CAC.</span><span class="sxs-lookup"><span data-stu-id="440ce-109">Use the following procedures to create network sites that align to network sites in the example network topology for CAC.</span></span> <span data-ttu-id="440ce-110">Esses procedimentos mostram como criar e configurar sites de rede que são restringidos pela largura de banda WAN e, portanto, exigem políticas de largura de banda que limitam o fluxo de tráfego de áudio ou vídeo em tempo real.</span><span class="sxs-lookup"><span data-stu-id="440ce-110">These procedures show how to create and configure network sites that are constrained by WAN bandwidth and therefore require bandwidth policies that limit real-time audio or video traffic flow.</span></span>

<span data-ttu-id="440ce-111">No exemplo de implantação de CAC, a região da América do Norte tem seis sites.</span><span class="sxs-lookup"><span data-stu-id="440ce-111">In the example CAC deployment, the North America region has six sites.</span></span> <span data-ttu-id="440ce-112">Três desses sites são restringidos pela largura de banda de WAN: Reno, Portland e Albuquerque.</span><span class="sxs-lookup"><span data-stu-id="440ce-112">Three of these sites are constrained by WAN bandwidth: Reno, Portland, and Albuquerque.</span></span> <span data-ttu-id="440ce-113">Os outros três sites, que *não* são restringidos pela largura de banda de WAN: Nova York, Chicago e Detroit.</span><span class="sxs-lookup"><span data-stu-id="440ce-113">The other three sites, which are *not* constrained by WAN bandwidth: New York, Chicago, and Detroit.</span></span> <span data-ttu-id="440ce-114">Para obter um exemplo de como criar ou modificar esses outros sites de rede, consulte [criar ou modificar um site de rede no Lync Server 2013](lync-server-2013-create-or-modify-a-network-site.md).</span><span class="sxs-lookup"><span data-stu-id="440ce-114">For an example of how to create or modify those other network sites, see [Create or modify a network site in Lync Server 2013](lync-server-2013-create-or-modify-a-network-site.md).</span></span>

<span data-ttu-id="440ce-115">Para ver o exemplo de topologia de rede, consulte [exemplo: reunir seus requisitos de controle de admissão de chamadas no Lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="440ce-115">To view the example network topology, see [Example: Gathering your requirements for call admission control in Lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) in the Planning documentation.</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="440ce-116">No procedimento a seguir, o Shell de gerenciamento do Lync Server é usado para criar um site de rede.</span><span class="sxs-lookup"><span data-stu-id="440ce-116">In the following procedure, Lync Server Management Shell is used to create a network site.</span></span> <span data-ttu-id="440ce-117">Para obter detalhes sobre como usar o painel de controle do Lync Server para criar um site de rede, consulte <A href="lync-server-2013-create-or-modify-a-network-site.md">criar ou modificar um site de rede no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="440ce-117">For details about using Lync Server Control Panel to create a network site, see <A href="lync-server-2013-create-or-modify-a-network-site.md">Create or modify a network site in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-create-network-sites-for-call-admission-control"></a><span data-ttu-id="440ce-118">Para criar sites de rede para controle de admissão de chamadas</span><span class="sxs-lookup"><span data-stu-id="440ce-118">To create network sites for call admission control</span></span>

1.  <span data-ttu-id="440ce-119">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="440ce-119">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="440ce-120">Execute o cmdlet **New-CsNetworkSite** para criar sites de rede e aplicar um perfil de política de largura de banda apropriado para cada site.</span><span class="sxs-lookup"><span data-stu-id="440ce-120">Run the **New-CsNetworkSite** cmdlet to create network sites and apply an appropriate bandwidth policy profile to each site.</span></span> <span data-ttu-id="440ce-121">Por exemplo, execute:</span><span class="sxs-lookup"><span data-stu-id="440ce-121">For example, run:</span></span>
    
       ```powershell
        New-CsNetworkSite -NetworkSiteID Reno -Description "NA:Branch office for sales force" -NetworkRegionID NorthAmerica -BWPolicyProfileID 10MB_Link
       ```
    
       ```powershell
        New-CsNetworkSite -NetworkSiteID Portland -Description "NA:Branch office for marketing force" -NetworkRegionID NorthAmerica -BWPolicyProfileID 5MB_Link
       ```
    
       ```powershell
        New-CsNetworkSite -NetworkSiteID Albuquerque -Description "NA:Branch office for SouthWest sales" -NetworkRegionID EMEA -BWPolicyProfileID 10MB_Link
       ```

3.  <span data-ttu-id="440ce-122">Para concluir a criação de sites de rede para toda a topologia de exemplo, repita a etapa 2 para os sites de rede com largura de banda restrita nas regiões da EMEA e da Ásia-Pacífico.</span><span class="sxs-lookup"><span data-stu-id="440ce-122">To finish creating network sites for the entire example topology, repeat step 2 for the bandwidth-constrained network sites in the EMEA and APAC regions.</span></span>

<span data-ttu-id="440ce-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="440ce-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

