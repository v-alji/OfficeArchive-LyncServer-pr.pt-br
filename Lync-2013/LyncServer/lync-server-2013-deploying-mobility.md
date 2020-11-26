---
title: 'Lync Server 2013: Implantando mobilidade'
description: 'Lync Server 2013: implantação de mobilidade.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying mobility
ms:assetid: f41e6b25-d2cd-43fd-a17b-22cfda8bcd4f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690055(v=OCS.15)
ms:contentKeyID: 48185805
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cf927b950f8b94884fb91224a87e196fc815fca1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429871"
---
# <a name="deploying-mobility-in-lync-server-2013"></a><span data-ttu-id="67bb1-103">Implantando mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67bb1-103">Deploying mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="67bb1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="67bb1-104">

<span> </span></span></span>

<span data-ttu-id="67bb1-105">_**Tópico da última modificação:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="67bb1-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="67bb1-106">Ao implantar o recurso de mobilidade do Lync Server 2013, os usuários móveis podem usar dispositivos móveis compatíveis com a funcionalidade do Lync, como mensagens instantâneas (IM), presença e contatos.</span><span class="sxs-lookup"><span data-stu-id="67bb1-106">When you deploy the Lync Server 2013 mobility feature, mobile users can use supported mobile devices for Lync functionality such as instant messaging (IM), presence, and contacts.</span></span>

<span data-ttu-id="67bb1-107">Para obter detalhes sobre os requisitos para a implantação do recurso de mobilidade, consulte planejando o recurso [de mobilidade no Lync Server 2013](lync-server-2013-planning-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="67bb1-107">For details about requirements for deploying the mobility feature, see [Planning for mobility in Lync Server 2013](lync-server-2013-planning-for-mobility.md).</span></span>

<span data-ttu-id="67bb1-108">Esta seção orienta você pelas etapas de implantação e verificação dos recursos de mobilidade e descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="67bb1-108">This section guides you through the steps for deploying and verifying the mobility and automatic discovery features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="67bb1-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="67bb1-109">In This Section</span></span>

  - [<span data-ttu-id="67bb1-110">Criando registros de DNS para o Serviço de Autodiscover no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67bb1-110">Creating DNS records for the Autodiscover Service in Lync Server 2013</span></span>](lync-server-2013-creating-dns-records-for-the-autodiscover-service.md)

  - [<span data-ttu-id="67bb1-111">Modificando certificados para mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67bb1-111">Modifying certificates for mobility in Lync Server 2013</span></span>](lync-server-2013-modifying-certificates-for-mobility.md)

  - [<span data-ttu-id="67bb1-112">Configurando o proxy reverso para mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67bb1-112">Configuring the reverse proxy for mobility in Lync Server 2013</span></span>](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md)

  - [<span data-ttu-id="67bb1-113">Configurando Autodiscover no Lync Server 2013 para mobilidade com implantações híbridas</span><span class="sxs-lookup"><span data-stu-id="67bb1-113">Configuring Autodiscover in Lync Server 2013 for mobility with hybrid deployments</span></span>](lync-server-2013-configuring-autodiscover-for-mobility-with-hybrid-deployments.md)

  - [<span data-ttu-id="67bb1-114">Verificando sua implantação de mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67bb1-114">Verifying your mobility deployment in Lync Server 2013</span></span>](lync-server-2013-verifying-your-mobility-deployment.md)

  - [<span data-ttu-id="67bb1-115">Configurando notificações por push no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67bb1-115">Configuring for push notifications in Lync Server 2013</span></span>](lync-server-2013-configuring-for-push-notifications.md)

  - [<span data-ttu-id="67bb1-116">Configurando a política de mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67bb1-116">Configuring mobility policy in Lync Server 2013</span></span>](lync-server-2013-configuring-mobility-policy.md)

<span data-ttu-id="67bb1-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="67bb1-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

