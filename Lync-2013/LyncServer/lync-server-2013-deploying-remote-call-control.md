---
title: 'Lync Server 2013: Implantando controle de chamada remota'
description: 'Lync Server 2013: Implantando o controle de chamada remota.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying remote call control
ms:assetid: 763037f7-7a2a-49ae-acc3-9781b0bff7e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558664(v=OCS.15)
ms:contentKeyID: 48184536
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4cc5e79f3ee44c354baf435585d304574d6a980c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429780"
---
# <a name="deploying-remote-call-control-in-lync-server-2013"></a><span data-ttu-id="bc475-103">Implantando controle de chamada remota no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc475-103">Deploying remote call control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bc475-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bc475-104">

<span> </span></span></span>

<span data-ttu-id="bc475-105">_**Tópico da última modificação:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="bc475-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="bc475-106">Esta seção orienta você no processo de implantação da funcionalidade de controle de chamada remota para os usuários da sua organização.</span><span class="sxs-lookup"><span data-stu-id="bc475-106">This section guides you through the process of deploying remote call control functionality to users in your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bc475-107">Embora os recursos de controle de chamada remota estejam disponíveis para usuários remotos enquanto estiverem fora do firewall da sua organização, os detalhes sobre a implantação de cenários de acesso externo estão fora do escopo desta documentação.</span><span class="sxs-lookup"><span data-stu-id="bc475-107">Although remote call control features are available to remote users while they are outside of your organization’s firewall, details about deploying external access scenarios are beyond the scope of this documentation.</span></span> <span data-ttu-id="bc475-108">Para obter detalhes sobre a implantação de acesso a usuários externos, consulte <A href="lync-server-2013-deploying-external-user-access.md">implantando o acesso de usuários externos no Lync Server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="bc475-108">For details about deploying external user access, see <A href="lync-server-2013-deploying-external-user-access.md">Deploying external user access in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="bc475-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="bc475-109">In This Section</span></span>

  - [<span data-ttu-id="bc475-110">Configurando o Lync Server 2013 para rotear para um gateway SIP/CSTA</span><span class="sxs-lookup"><span data-stu-id="bc475-110">Configuring Lync Server 2013 to route to a SIP/CSTA gateway</span></span>](lync-server-2013-configuring-lync-server-to-route-to-a-sip-csta-gateway.md)

  - [<span data-ttu-id="bc475-111">Configurar uma rota estática para controle de chamada remota no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc475-111">Configure a static route for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-static-route-for-remote-call-control.md)

  - [<span data-ttu-id="bc475-112">Configurar uma entrada de aplicativo confiável para controle de chamada remota no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc475-112">Configure a trusted application entry for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md)

  - <span data-ttu-id="bc475-113">[Definir um endereço IP do gateway SIP/CSTA no Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) (apenas se o gateway estiver configurado para usar TCP)</span><span class="sxs-lookup"><span data-stu-id="bc475-113">[Define a SIP/CSTA gateway IP address in Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) (only if the gateway is configured to use TCP)</span></span>

  - [<span data-ttu-id="bc475-114">Habilitar usuários do Lync para controle de chamada remota no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc475-114">Enable Lync users for remote call control in Lync Server 2013</span></span>](lync-server-2013-enable-lync-users-for-remote-call-control.md)

  - [<span data-ttu-id="bc475-115">Normalização de controle de chamada remota e de número de telefone no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc475-115">Remote call control and phone number normalization in Lync Server 2013</span></span>](lync-server-2013-remote-call-control-and-phone-number-normalization.md)

  - <span data-ttu-id="bc475-116">[Remover um host autorizado herdado do Lync Server 2013 (opcional)](lync-server-2013-remove-a-legacy-authorized-host-optional.md) (somente se você estiver migrando usuários anteriormente habilitados para controle de chamada remota)</span><span class="sxs-lookup"><span data-stu-id="bc475-116">[Remove a legacy authorized host in Lync Server 2013 (optional)](lync-server-2013-remove-a-legacy-authorized-host-optional.md) (only if you are migrating users previously enabled for remote call control)</span></span>

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="bc475-117">Seções Relacionadas</span><span class="sxs-lookup"><span data-stu-id="bc475-117">Related Sections</span></span>

[<span data-ttu-id="bc475-118">Planejando o controle de chamada remota no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc475-118">Planning for remote call control in Lync Server 2013</span></span>](lync-server-2013-planning-for-remote-call-control.md)

<span data-ttu-id="bc475-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bc475-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

