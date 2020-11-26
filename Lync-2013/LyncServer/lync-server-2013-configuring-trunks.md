---
title: 'Lync Server 2013: Configurando troncos'
description: 'Lync Server 2013: Configurando troncos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring trunks
ms:assetid: 0c339511-a185-484e-94f0-dbe918b7e48a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398170(v=OCS.15)
ms:contentKeyID: 48183389
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07d9503cd38419a7145796a6edf8484a14cdeb53
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432461"
---
# <a name="configuring-trunks-in-lync-server-2013"></a><span data-ttu-id="1a9ed-103">Configurando troncos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a9ed-103">Configuring trunks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1a9ed-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1a9ed-104">

<span> </span></span></span>

<span data-ttu-id="1a9ed-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="1a9ed-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="1a9ed-106">Como parte da implantação do Enterprise Voice, você pode configurar um tronco entre um servidor de mediação e um ou mais dos seguintes pares para fornecer conectividade PSTN (rede telefônica pública comutada) para clientes e dispositivos do Enterprise Voice em sua organização:</span><span class="sxs-lookup"><span data-stu-id="1a9ed-106">As part of Enterprise Voice deployment, you can configure a trunk between a Mediation Server and one or more of the following peers to provide public switched telephone network (PSTN) connectivity for Enterprise Voice clients and devices in your organization:</span></span>

  - <span data-ttu-id="1a9ed-107">Conexão tronco SIP em um provedor de serviço de telefonia por Internet (ITSP)</span><span class="sxs-lookup"><span data-stu-id="1a9ed-107">SIP trunk connection to an Internet telephony service provider (ITSP)</span></span>

  - <span data-ttu-id="1a9ed-108">Gateway PSTN</span><span class="sxs-lookup"><span data-stu-id="1a9ed-108">PSTN gateway</span></span>

  - <span data-ttu-id="1a9ed-109">Central privada de comutação telefônica (PBX)</span><span class="sxs-lookup"><span data-stu-id="1a9ed-109">Private branch exchange (PBX)</span></span>

<span data-ttu-id="1a9ed-110">Para obter detalhes, consulte [planejando a conectividade PSTN no Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="1a9ed-110">For details, see [Planning for PSTN connectivity in Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) in the Planning documentation.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="1a9ed-111">Antes de começar a configuração de tronco, verifique se a topologia foi criada e se o servidor de mediação e seu par foram configurados e associados uns com os outros.</span><span class="sxs-lookup"><span data-stu-id="1a9ed-111">Before you begin trunk configuration, verify that the topology has been created and that the Mediation Server and its peer have been configured and associated with one another.</span></span> <span data-ttu-id="1a9ed-112">Para obter detalhes, consulte <A href="lync-server-2013-define-a-gateway-in-topology-builder.md">definir um gateway no construtor de topologias no Lync Server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="1a9ed-112">For details, see <A href="lync-server-2013-define-a-gateway-in-topology-builder.md">Define a gateway in Topology Builder in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="1a9ed-113">Como parte da configuração de tronco, você pode habilitar o recurso de bypass de mídia do Lync Server 2013, que permite que a mídia ignore o servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="1a9ed-113">As a part of trunk configuration, you can enable the Lync Server 2013 media bypass feature, which enables media to bypass the Mediation Server.</span></span> <span data-ttu-id="1a9ed-114">Os troncos podem ser configurados com ou sem bypass de mídia habilitados, mas é altamente recomendável que você o habilite.</span><span class="sxs-lookup"><span data-stu-id="1a9ed-114">Trunks can be configured either with or without media bypass enabled, but we strongly recommend that you enable it.</span></span> <span data-ttu-id="1a9ed-115">Para obter detalhes, consulte <A href="lync-server-2013-planning-for-media-bypass.md">planejando o bypass de mídia no Lync Server 2013</A> na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="1a9ed-115">For details, see <A href="lync-server-2013-planning-for-media-bypass.md">Planning for media bypass in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="1a9ed-116">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="1a9ed-116">In This Section</span></span>

  - [<span data-ttu-id="1a9ed-117">Suporte a vários troncos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a9ed-117">Multiple trunk support in Lync Server 2013</span></span>](lync-server-2013-multiple-trunk-support.md)

  - [<span data-ttu-id="1a9ed-118">Roteamento inter-trunk no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a9ed-118">Inter-trunk routing in Lync Server 2013</span></span>](lync-server-2013-inter-trunk-routing.md)

  - [<span data-ttu-id="1a9ed-119">Exibir informações de configuração de tronco no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a9ed-119">View trunk configuration information in Lync Server 2013</span></span>](lync-server-2013-view-trunk-configuration-information.md)

  - [<span data-ttu-id="1a9ed-120">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a9ed-120">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)

  - [<span data-ttu-id="1a9ed-121">Configurar um tronco sem bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a9ed-121">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)

  - [<span data-ttu-id="1a9ed-122">Criar uma nova coleção de definições de configuração de tronco no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a9ed-122">Create a new collection of trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-a-new-collection-of-trunk-configuration-settings.md)

  - [<span data-ttu-id="1a9ed-123">Excluir uma coleção existente de definições de configuração de tronco SIP no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a9ed-123">Delete an existing collection of SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="1a9ed-124">Modificar as configurações de tronco SIP no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a9ed-124">Modify SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-modify-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="1a9ed-125">Testar as configurações de tronco SIP no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a9ed-125">Test SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-test-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="1a9ed-126">Exibir informações sobre troncos SIP individuais no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a9ed-126">View information about individual SIP trunks in Lync Server 2013</span></span>](lync-server-2013-view-information-about-individual-sip-trunks.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1a9ed-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a9ed-127">See Also</span></span>


[<span data-ttu-id="1a9ed-128">Definir um gateway no construtor de topologias no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a9ed-128">Define a gateway in Topology Builder in Lync Server 2013</span></span>](lync-server-2013-define-a-gateway-in-topology-builder.md)  


[<span data-ttu-id="1a9ed-129">Planejando a conectividade PSTN no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a9ed-129">Planning for PSTN connectivity in Lync Server 2013</span></span>](lync-server-2013-planning-for-pstn-connectivity.md)  
[<span data-ttu-id="1a9ed-130">Planejamento de bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a9ed-130">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="1a9ed-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1a9ed-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

