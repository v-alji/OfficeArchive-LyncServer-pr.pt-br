---
title: 'Lync Server 2013: híbrido e dividido-Domain-descoberta automática'
description: 'Lync Server 2013: híbrido e dividir-Domain-descoberta automática.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hybrid and split-domain - Autodiscover
ms:assetid: c855bcc5-b656-4d2d-92d6-f016f2797d3a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945652(v=OCS.15)
ms:contentKeyID: 51541520
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 972233fd10d2b68a002d2d3a203f61bb0bd29574
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427436"
---
# <a name="hybrid-and-split-domain---autodiscover-in-lync-server-2013"></a><span data-ttu-id="61b91-103">Descoberta automática de domínio híbrido e dividido no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="61b91-103">Hybrid and split-domain - Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="61b91-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="61b91-104">

<span> </span></span></span>

<span data-ttu-id="61b91-105">_**Tópico da última modificação:** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="61b91-105">_**Topic Last Modified:** 2013-02-14_</span></span>

<span data-ttu-id="61b91-106">Um espaço de endereço SIP compartilhado, também conhecido como uma implantação de *domínio dividido* , ou uma implantação *híbrida* , é uma configuração na qual os usuários são implantados em uma implantação local e em um ambiente online.</span><span class="sxs-lookup"><span data-stu-id="61b91-106">A shared SIP address space, also known as a *split-domain* deployment, or a *hybrid* deployment, is a configuration where users are deployed across an on-premise deployment and an online environment.</span></span> <span data-ttu-id="61b91-107">O resultado desejado é ter um usuário, independentemente de onde o servidor local está localizado (local ou online), fazer logon na implantação e ser redirecionado para o local do servidor de casa.</span><span class="sxs-lookup"><span data-stu-id="61b91-107">The desired outcome is to have a user, regardless of where their home server is located (on-premise or online), log into the deployment and be redirected to their home server location.</span></span> <span data-ttu-id="61b91-108">Para fazer isso, o recurso descoberta automática do Lync Server 2013 é usado para redirecionar o usuário online para a topologia online.</span><span class="sxs-lookup"><span data-stu-id="61b91-108">To accomplish this, the Autodiscover feature of Lync Server 2013 is used to redirect the online user to the online topology.</span></span> <span data-ttu-id="61b91-109">Você pode fazer isso Configurando o localizador de recursos uniforme (URL) da descoberta automática usando o Shell de gerenciamento do Lync Server, o cmdlet **Get-CsHostingProvider** e o cmdlet **set-CsHostingProvider** .</span><span class="sxs-lookup"><span data-stu-id="61b91-109">You can do this by configuring the Autodiscover uniform resource locator (URL) by using the Lync Server Management Shell, the **Get-CsHostingProvider** cmdlet, and the **Set-CsHostingProvider** cmdlet.</span></span>

<div>

## <a name="mobility-for-the-split-domain-deployment"></a><span data-ttu-id="61b91-110">Mobilidade para a implantação de domínio dividido</span><span class="sxs-lookup"><span data-stu-id="61b91-110">Mobility for the Split Domain Deployment</span></span>

<span data-ttu-id="61b91-111">Será preciso coletar e gravar os seguintes atributos implantados:</span><span class="sxs-lookup"><span data-stu-id="61b91-111">You will need to collect and record the following deployed attributes:</span></span>

  - <span data-ttu-id="61b91-112">No Shell de gerenciamento do Lync Server, digite</span><span class="sxs-lookup"><span data-stu-id="61b91-112">From the Lync Server Management Shell, type</span></span>
    
        Get-CsHostingProvider

  - <span data-ttu-id="61b91-113">Nos resultados, localize o provedor online com o atributo **ProxyFQDN**.</span><span class="sxs-lookup"><span data-stu-id="61b91-113">In the results, find the online provider with the attribute **ProxyFQDN**.</span></span> <span data-ttu-id="61b91-114">Por exemplo, sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="61b91-114">For example, sipfed.online.lync.com.</span></span>

  - <span data-ttu-id="61b91-115">Grave o valor do ProxyFQDN.</span><span class="sxs-lookup"><span data-stu-id="61b91-115">Record the value of the ProxyFQDN.</span></span>

  - <span data-ttu-id="61b91-116">Habilite a Federação no painel de controle do Lync Server local, permitindo Federação com o provedor online.</span><span class="sxs-lookup"><span data-stu-id="61b91-116">Enable federation in the on-premise Lync Server Control Panel, allowing federation with the online provider.</span></span>

  - <span data-ttu-id="61b91-117">Habilite a Federação para o provedor online.</span><span class="sxs-lookup"><span data-stu-id="61b91-117">Enable federation for the online provider.</span></span> <span data-ttu-id="61b91-118">Por padrão, todos os usuários online estão habilitados para Federação de domínio e podem se comunicar com todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="61b91-118">By default, all online users are enabled for domain federation and can communicate with all domains.</span></span>

  - <span data-ttu-id="61b91-119">Se você definirá domínios bloqueados e permitidos, determine os domínios que você permitirá explicitamente ou bloqueará explicitamente.</span><span class="sxs-lookup"><span data-stu-id="61b91-119">If you will define blocked and allowed domains, determine the domains that you will explicitly allow or explicitly block.</span></span>

  - <span data-ttu-id="61b91-120">Para a Federação online, você deve planejar exceções de firewall, certificados e host DNS (A ou AAAA, se estiver usando IPv6) registros.</span><span class="sxs-lookup"><span data-stu-id="61b91-120">For online federation, you must plan for firewall exceptions, certificates, and DNS host (A or AAAA, if using IPv6) records.</span></span> <span data-ttu-id="61b91-121">Além disso, você deve configurar políticas de Federação.</span><span class="sxs-lookup"><span data-stu-id="61b91-121">Additionally, you must configure federation policies.</span></span> <span data-ttu-id="61b91-122">Para obter detalhes, consulte [planejando a Federação para o Lync server 2013 e o Office Communications Server](lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md).</span><span class="sxs-lookup"><span data-stu-id="61b91-122">For details, see [Planning for Lync Server 2013 and Office Communications Server federation](lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md).</span></span>

<span data-ttu-id="61b91-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="61b91-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

