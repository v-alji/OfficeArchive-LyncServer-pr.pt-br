---
title: 'Lync Server 2013: Sobre regiões de rede, sites e subredes'
description: 'Lync Server 2013: sobre regiões de rede, sites e sub-redes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: About network regions, sites, and subnets
ms:assetid: 6662123a-d011-408c-a290-92b2a8589943
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398467(v=OCS.15)
ms:contentKeyID: 48184335
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3c7f660f3c72003527e0721c3f9702865e9b9b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439517"
---
# <a name="about-network-regions-sites-and-subnets-in-lync-server-2013"></a><span data-ttu-id="51a5a-103">Sobre regiões de rede, sites e subredes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51a5a-103">About network regions, sites, and subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="51a5a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="51a5a-104">

<span> </span></span></span>

<span data-ttu-id="51a5a-105">_**Tópico da última modificação:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="51a5a-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="51a5a-106">Os recursos avançados de voz empresarial descritos nesta seção compartilham determinados requisitos de configuração para regiões de rede, sites de rede e sub-redes.</span><span class="sxs-lookup"><span data-stu-id="51a5a-106">The advanced Enterprise Voice features described in this section share certain configuration requirements for network regions, network sites, and subnets.</span></span> <span data-ttu-id="51a5a-107">Por exemplo, todos os três recursos avançados exigem que cada sub-rede na sua topologia seja associada a um *site de rede* específico, e cada site de rede deve estar associado a uma *região de rede*.</span><span class="sxs-lookup"><span data-stu-id="51a5a-107">For example, all three advanced features require that each subnet in your topology be associated with a specific *network site*, and each network site must be associated with a *network region*.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="51a5a-108">Antes de iniciar a configuração de rede para o controle de admissão de chamadas, o E9-1-1 ou o bypass de mídia, verifique se você revisou informações adicionais sobre as configurações de rede nas <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">configurações de voz do recurso Advanced Enterprise Voice do Lync Server 2013</A> na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="51a5a-108">Before you begin network configuration for call admission control, E9-1-1, or media bypass, make sure that you reviewed additional information about network settings in the <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">Network settings for the advanced Enterprise Voice features in Lync Server 2013</A> topic in the Planning documentation.</span></span> <span data-ttu-id="51a5a-109">Para obter detalhes sobre a configuração de rede principalmente sobre o controle de admissão de chamadas, consulte <A href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">definir seus requisitos de controle de admissão de chamadas no Lync Server 2013</A> na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="51a5a-109">For details about network configuration primarily about call admission control, also see <A href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<span data-ttu-id="51a5a-110">O controle de admissão de chamada e o E9-1-1 têm requisitos adicionais de configuração para os sites da rede:</span><span class="sxs-lookup"><span data-stu-id="51a5a-110">Call admission control and E9-1-1 have additional configuration requirements for network sites:</span></span>

  - <span data-ttu-id="51a5a-111">O serviço de controle de admissão de chamadas requer que um *perfil de política de largura de banda* seja especificado para cada site restrito pelas limitações de largura de banda WAN.</span><span class="sxs-lookup"><span data-stu-id="51a5a-111">Call admission control requires that a *bandwidth policy profile* be specified for each site that is constrained by WAN bandwidth limitations.</span></span> <span data-ttu-id="51a5a-112">Se você planeja implantar o controle de admissão de chamadas, deverá [criar perfis de política de largura de banda no Lync Server 2013](lync-server-2013-create-bandwidth-policy-profiles.md) antes de configurar seus sites de rede.</span><span class="sxs-lookup"><span data-stu-id="51a5a-112">If you plan to deploy call admission control, you must [Create bandwidth policy profiles in Lync Server 2013](lync-server-2013-create-bandwidth-policy-profiles.md) before you configure your network sites.</span></span>

  - <span data-ttu-id="51a5a-113">O E9-1-1 requer que uma *política local* seja especificada para cada site.</span><span class="sxs-lookup"><span data-stu-id="51a5a-113">E9-1-1 requires that a *location policy* be specified for each site.</span></span> <span data-ttu-id="51a5a-114">Se você planeja implantar o E9-1-1, será necessário [criar políticas de localização no Lync Server 2013](lync-server-2013-create-location-policies.md) antes de configurar seus sites de rede.</span><span class="sxs-lookup"><span data-stu-id="51a5a-114">If you plan to deploy E9-1-1, you must [Create location policies in Lync Server 2013](lync-server-2013-create-location-policies.md) before you configure your network sites.</span></span>

<div>

## <a name="create-or-modify-network-regions-network-sites-and-subnets"></a><span data-ttu-id="51a5a-115">Criar ou modificar regiões de rede, sites de rede e sub-redes</span><span class="sxs-lookup"><span data-stu-id="51a5a-115">Create or Modify Network Regions, Network Sites, and Subnets</span></span>

<span data-ttu-id="51a5a-116">Os tópicos a seguir fornecem etapas para criar ou modificar regiões de rede e sites de rede e para associar sub-redes a sites de rede.</span><span class="sxs-lookup"><span data-stu-id="51a5a-116">The following topics provide steps to create or modify network regions and network sites, and to associate subnets with network sites.</span></span> <span data-ttu-id="51a5a-117">Esses tópicos não são específicos para qualquer recurso avançado de Enterprise Voice específico.</span><span class="sxs-lookup"><span data-stu-id="51a5a-117">These topics are not specific to any particular advanced Enterprise Voice feature.</span></span>

  - [<span data-ttu-id="51a5a-118">Criar ou modificar uma região de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51a5a-118">Create or modify a network region in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-region.md)

  - [<span data-ttu-id="51a5a-119">Criar ou modificar um site da rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51a5a-119">Create or modify a network site in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-site.md)

  - [<span data-ttu-id="51a5a-120">Associar uma subrede a um site de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51a5a-120">Associate a subnet with a network site in Lync Server 2013</span></span>](lync-server-2013-associate-a-subnet-with-a-network-site.md)

<span data-ttu-id="51a5a-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="51a5a-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

