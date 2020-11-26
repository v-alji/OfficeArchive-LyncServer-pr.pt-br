---
title: 'Lync Server 2013: Fornecendo conectividade de PSTN ao site da filial'
description: 'Lync Server 2013: fornecendo conectividade PSTN em um site de filial.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Providing PSTN connectivity at a branch site
ms:assetid: d78d76fb-2dd1-42cb-b25a-bfaff9650a70
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398945(v=OCS.15)
ms:contentKeyID: 48185633
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63cbc03f78a27bda14c2906e31cc68bed5870878
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436731"
---
# <a name="providing-pstn-connectivity-at-a-branch-site-in-lync-server-2013"></a><span data-ttu-id="a4f6d-103">Fornecendo conectividade de PSTN ao site da filial no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4f6d-103">Providing PSTN connectivity at a branch site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a4f6d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a4f6d-104">

<span> </span></span></span>

<span data-ttu-id="a4f6d-105">_**Tópico da última modificação:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="a4f6d-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="a4f6d-106">Recomendamos usar o Microsoft Lync Server 2013, a ferramenta de planejamento para adicionar sites de filiais à sua topologia e para configurar sua infraestrutura de voz em sites de filiais.</span><span class="sxs-lookup"><span data-stu-id="a4f6d-106">We recommend using the Microsoft Lync Server 2013, Planning Tool to add branch sites to your topology and to set up your voice infrastructure in branch sites.</span></span>

<span data-ttu-id="a4f6d-107">Se você não estiver usando a ferramenta de planejamento, use os procedimentos nos tópicos desta seção — primeiro, para adicionar os sites de ramificação e, em seguida, para configurar sua infraestrutura de voz definindo o gateway PSTN (rede telefônica comutada de IP/pública) e/ou configurando o tronco SIP (com ou sem bypass de mídia).</span><span class="sxs-lookup"><span data-stu-id="a4f6d-107">If you are not using the Planning Tool, use the procedures in the topics in this section—first, to add the branch sites, and then, to set up your voice infrastructure by defining the IP/public switched telephone network (PSTN) gateway and/or by configuring the SIP trunk (with or without media bypass).</span></span> <span data-ttu-id="a4f6d-108">Conectar um PBX (Private Branch Exchange) ao site da filial é outra opção.</span><span class="sxs-lookup"><span data-stu-id="a4f6d-108">Connecting a private branch exchange (PBX) to the branch site is another option.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a4f6d-109">Se você quiser fornecer resiliência em filiais, você deve implantar um aparelho de ramificação sobreviventes, um servidor de ramificação sobreviventes ou um servidor Standard Edition no site da filial.</span><span class="sxs-lookup"><span data-stu-id="a4f6d-109">If you want to provide branch-site resiliency, you must deploy a Survivable Branch Appliance, a Survivable Branch Server, or Standard Edition server at the branch site.</span></span> <span data-ttu-id="a4f6d-110">Para obter detalhes, consulte <A href="lync-server-2013-deploying-a-survivable-branch-appliance-or-server.md">implantando um servidor ou um aplicativo de ramificação sobreviventes com o Lync server 2013</A> ou <A href="lync-server-2013-deploying-lync-server.md">implantando o Lync Server 2013</A>, conforme apropriado, na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="a4f6d-110">For details, see <A href="lync-server-2013-deploying-a-survivable-branch-appliance-or-server.md">Deploying a Survivable Branch Appliance or Server with Lync Server 2013</A> or <A href="lync-server-2013-deploying-lync-server.md">Deploying Lync Server 2013</A>, as appropriate, in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a4f6d-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a4f6d-111">In This Section</span></span>

  - [<span data-ttu-id="a4f6d-112">Adicionar sites de filial a sua topologia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4f6d-112">Add branch sites to your topology in Lync Server 2013</span></span>](lync-server-2013-add-branch-sites-to-your-topology.md)

  - [<span data-ttu-id="a4f6d-113">Definir um gateway de PSTN para um site de filial no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4f6d-113">Define a PSTN gateway for a branch site in Lync Server 2013</span></span>](lync-server-2013-define-a-pstn-gateway-for-a-branch-site.md)

  - [<span data-ttu-id="a4f6d-114">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4f6d-114">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)

  - [<span data-ttu-id="a4f6d-115">Configurar um tronco sem bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4f6d-115">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a4f6d-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4f6d-116">See Also</span></span>


[<span data-ttu-id="a4f6d-117">Planejamento de bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4f6d-117">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
[<span data-ttu-id="a4f6d-118">Planejando a conectividade PSTN no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4f6d-118">Planning for PSTN connectivity in Lync Server 2013</span></span>](lync-server-2013-planning-for-pstn-connectivity.md)  
  

<span data-ttu-id="a4f6d-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a4f6d-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

