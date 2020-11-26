---
title: 'Lync Server 2013: criar políticas entre sites de rede'
description: 'Lync Server 2013: criar políticas entre sites de rede.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create network intersite policies
ms:assetid: b0714aae-55dc-4587-b718-34a03f596b22
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412844(v=OCS.15)
ms:contentKeyID: 48185148
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9666efcb9c6da459a8e50eeae66cd1a513b46f65
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431936"
---
# <a name="create-network-intersite-policies-in-lync-server-2013"></a><span data-ttu-id="10c82-103">Criar políticas entre sites de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="10c82-103">Create network intersite policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="10c82-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="10c82-104">

<span> </span></span></span>

<span data-ttu-id="10c82-105">_**Tópico da última modificação:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="10c82-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="10c82-106">Uma *política* entre sites de rede define limitações de largura de banda entre sites que têm links diretos de WAN entre eles.</span><span class="sxs-lookup"><span data-stu-id="10c82-106">A *network intersite policy* defines bandwidth limitations between sites that have direct WAN links between them.</span></span>

<span data-ttu-id="10c82-107">Para obter detalhes, consulte a documentação do Shell de gerenciamento do Lync Server para os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="10c82-107">For details, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="10c82-108">New-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="10c82-108">New-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterSitePolicy)

  - [<span data-ttu-id="10c82-109">Get-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="10c82-109">Get-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterSitePolicy)

  - [<span data-ttu-id="10c82-110">Set-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="10c82-110">Set-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterSitePolicy)

  - [<span data-ttu-id="10c82-111">Remove-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="10c82-111">Remove-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterSitePolicy)

<div>


> [!IMPORTANT]  
> <span data-ttu-id="10c82-112">Uma política entre sites de rede será necessária <EM>somente</EM> se houver um link cruzado direto entre dois sites de rede.</span><span class="sxs-lookup"><span data-stu-id="10c82-112">A network intersite policy is required <EM>only</EM> if there is a direct cross link between two network sites.</span></span>



</div>

<span data-ttu-id="10c82-113">Na região América do Norte da topologia de exemplo, existe um link direto entre os sites Reno e Albuquerque.</span><span class="sxs-lookup"><span data-stu-id="10c82-113">In the example topology North America region, there is a direct link between the Reno and Albuquerque sites.</span></span> <span data-ttu-id="10c82-114">Esses dois sites exigem uma política entre sites que aplica um perfil de política de largura de banda apropriado.</span><span class="sxs-lookup"><span data-stu-id="10c82-114">These two sites require an intersite policy that applies an appropriate bandwidth policy profile.</span></span> <span data-ttu-id="10c82-115">O exemplo a seguir aplica o perfil do link de 20 MB \_ .</span><span class="sxs-lookup"><span data-stu-id="10c82-115">The following example applies the 20Mb\_Link profile.</span></span>

<div>

## <a name="to-create-a-network-intersite-policy"></a><span data-ttu-id="10c82-116">Para criar uma política entre sites de rede</span><span class="sxs-lookup"><span data-stu-id="10c82-116">To create a network intersite policy</span></span>

1.  <span data-ttu-id="10c82-117">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="10c82-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="10c82-118">Execute o cmdlet New-CsNetworkInterSitePolicy para criar políticas entre sites de rede e aplicar um perfil de política de largura de banda apropriado para dois sites que têm um link cruzado direto.</span><span class="sxs-lookup"><span data-stu-id="10c82-118">Run the New-CsNetworkInterSitePolicy cmdlet to create network intersite policies and apply an appropriate bandwidth policy profile for two sites that have a direct cross link.</span></span> <span data-ttu-id="10c82-119">Por exemplo, execute:</span><span class="sxs-lookup"><span data-stu-id="10c82-119">For example, run:</span></span>
    
        New-CsNetworkInterSitePolicy -InterNetworkSitePolicyID Reno_Albuquerque -NetworkSiteID1 Reno -NetworkSiteID2 Albuquerque -BWPolicyProfileID 20Mb_Link

3.  <span data-ttu-id="10c82-120">Repita a etapa 2 conforme necessário para criar políticas entre sites de rede para todos os pares de sites de rede que têm um link cruzado direto.</span><span class="sxs-lookup"><span data-stu-id="10c82-120">Repeat step 2 as needed to create network intersite policies for all network sites pairs that have a direct cross link.</span></span>

<span data-ttu-id="10c82-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="10c82-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

