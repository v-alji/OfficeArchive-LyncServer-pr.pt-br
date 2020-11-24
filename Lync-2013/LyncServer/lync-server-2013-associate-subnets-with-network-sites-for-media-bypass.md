---
title: 'Lync Server 2013: associar sub-redes a sites de rede para bypass de mídia'
description: 'Lync Server 2013: associar sub-redes a sites de rede para bypass de mídia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Associate subnets with network sites for media bypass
ms:assetid: 5bc632b7-1446-470f-b332-48ea0ca4d1fd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398401(v=OCS.15)
ms:contentKeyID: 48184244
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee03b51d29a88ff634cb87385c5889c35acd8884
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390374"
---
# <a name="associate-subnets-with-network-sites-for-media-bypass-in-lync-server-2013"></a><span data-ttu-id="e538d-103">Associar sub-redes a sites de rede para ignorar mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e538d-103">Associate subnets with network sites for media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e538d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e538d-104">

<span> </span></span></span>

<span data-ttu-id="e538d-105">_**Tópico da última modificação:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="e538d-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e538d-106">Este tópico pressupõe que você configurou as configurações globais de bypass de mídia e que configurou a região de rede e os sites de rede para bypass de mídia.</span><span class="sxs-lookup"><span data-stu-id="e538d-106">This topic assumes that you have configured media bypass global settings and that you have configured network region and network sites for media bypass.</span></span>



</div>

<span data-ttu-id="e538d-107">Todas as sub-redes na rede devem estar associadas a um site de rede específico.</span><span class="sxs-lookup"><span data-stu-id="e538d-107">Every subnet in your network must be associated with a specific network site.</span></span> <span data-ttu-id="e538d-108">Isso ocorre porque as informações de sub-rede são usadas para determinar o site de rede no qual se encontra um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="e538d-108">This is because subnet information is used to determine the network site on which an endpoint is located.</span></span> <span data-ttu-id="e538d-109">Quando os locais de ambas as partes de uma sessão são conhecidos, o bypass de mídia pode determinar para onde enviar mídia para processamento.</span><span class="sxs-lookup"><span data-stu-id="e538d-109">When the locations of both parties in a session are known, media bypass can determine where to send media for processing.</span></span>

<span data-ttu-id="e538d-110">O bypass de mídia não tem nenhum requisito especial para associar sub-redes a sites de rede.</span><span class="sxs-lookup"><span data-stu-id="e538d-110">Media bypass does not have any special requirements for associating subnets with network sites.</span></span> <span data-ttu-id="e538d-111">Para criar uma associação entre as sub-redes e os sites de rede em sua topologia, siga os procedimentos em [associar uma sub-rede a um site de rede no Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).</span><span class="sxs-lookup"><span data-stu-id="e538d-111">To create an association between the subnets and network sites in your topology, follow the procedures in [Associate a subnet with a network site in Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).</span></span>

<div>

## <a name="next-steps-create-bandwidth-policy-profiles"></a><span data-ttu-id="e538d-112">Próximas etapas: criar perfis de política de largura de banda</span><span class="sxs-lookup"><span data-stu-id="e538d-112">Next Steps: Create Bandwidth Policy Profiles</span></span>

<span data-ttu-id="e538d-113">Depois de associar sub-redes a sites de rede para bypass de mídia, você deve criar um ou mais perfis de política de largura de banda que particionem sub-redes em uma boa conectividade e aquelas sem, para fins de bypass de mídia.</span><span class="sxs-lookup"><span data-stu-id="e538d-113">After you associate subnets with network sites for media bypass, you must create one or more bandwidth policy profiles that will partition subnets into those with good connectivity and those without, for the purposes of media bypass.</span></span> <span data-ttu-id="e538d-114">Todas as sub-redes dentro de uma região de rede com sites de rede que não têm restrições de largura de banda têm boa conectividade e, portanto, essas sub-redes podem usar o bypass de mídia.</span><span class="sxs-lookup"><span data-stu-id="e538d-114">All subnets within a network region with network sites that do not have bandwidth constraints have good connectivity, and, therefore, those subnets can use media bypass.</span></span>

<span data-ttu-id="e538d-115">Para obter os procedimentos para configurar perfis de política de largura de banda, consulte [criar perfis de política de largura de banda no Lync Server 2013](lync-server-2013-create-bandwidth-policy-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="e538d-115">For procedures to configure bandwidth policy profiles, see [Create bandwidth policy profiles in Lync Server 2013](lync-server-2013-create-bandwidth-policy-profiles.md).</span></span>

<span data-ttu-id="e538d-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e538d-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

