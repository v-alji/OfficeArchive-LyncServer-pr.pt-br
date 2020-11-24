---
title: 'Lync Server 2013: planejando a conectividade de mensagens instantâneas públicas'
description: 'Lync Server 2013: planejando a conectividade de mensagens instantâneas públicas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for public instant messaging connectivity
ms:assetid: e75e8884-05c7-414a-8014-bc9aa8126fb7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205349(v=OCS.15)
ms:contentKeyID: 48185698
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9a020a291a39d78aea9271926c99b508a8cd9827
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390461"
---
# <a name="planning-for-public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="f793c-103">Planejando a conectividade de mensagens instantâneas públicas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f793c-103">Planning for public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f793c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f793c-104">

<span> </span></span></span>

<span data-ttu-id="f793c-105">_**Tópico da última modificação:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="f793c-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="f793c-106">A conectividade de mensagens instantâneas públicas é uma classe de Federação e está configurada para permitir que os usuários internos e externos do Lync Server 2013 adicionem contatos de qualquer um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="f793c-106">Public Instant Messaging Connectivity is a class of federation, and is configured to allow your internal and external Lync Server 2013 users to add contacts from any of the following:</span></span>

  - <span data-ttu-id="f793c-107">Contatos do Messenger</span><span class="sxs-lookup"><span data-stu-id="f793c-107">Messenger contacts</span></span>

  - <span data-ttu-id="f793c-108">Instant\!</span><span class="sxs-lookup"><span data-stu-id="f793c-108">Yahoo\!</span></span> <span data-ttu-id="f793c-109">contatos</span><span class="sxs-lookup"><span data-stu-id="f793c-109">contacts</span></span>

  - <span data-ttu-id="f793c-110">Contatos do America Online (AOL)</span><span class="sxs-lookup"><span data-stu-id="f793c-110">America Online (AOL) contacts</span></span>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="f793c-111">A partir de 1º de setembro de 2012, a licença de assinatura de usuário da conectividade de mensagem de chat pública do Microsoft Lync (PIC USL) não está mais disponível para a compra de contratos novos ou de renovação.</span><span class="sxs-lookup"><span data-stu-id="f793c-111">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (PIC USL) is no longer available for the purchase for new or renewing agreements.</span></span> <span data-ttu-id="f793c-112">Os clientes com licenças ativas poderão continuar a federar-se com o Yahoo!</span><span class="sxs-lookup"><span data-stu-id="f793c-112">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="f793c-113">Messenger até a data de desligamento do serviço.</span><span class="sxs-lookup"><span data-stu-id="f793c-113">Messenger until the service shutdown date.</span></span> <span data-ttu-id="f793c-114">Uma data de fim da vida útil de junho de 2014 para AOL e Yahoo!</span><span class="sxs-lookup"><span data-stu-id="f793c-114">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="f793c-115">foi anunciado.</span><span class="sxs-lookup"><span data-stu-id="f793c-115">has been announced.</span></span> <span data-ttu-id="f793c-116">Para obter detalhes, consulte <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">suporte para conectividade de mensagens instantâneas públicas no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="f793c-116">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="f793c-117">O PIC USL é uma licença de assinatura por usuário e por mês necessária para o Lync Server ou o Office Communications Server se federar com o Yahoo!</span><span class="sxs-lookup"><span data-stu-id="f793c-117">The PIC USL is a per-user, per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="f793c-118">Spam.</span><span class="sxs-lookup"><span data-stu-id="f793c-118">Messenger.</span></span> <span data-ttu-id="f793c-119">O recurso da Microsoft para fornecer esse serviço tem o apoio acordado do Yahoo!, o contrato subjacente para o qual não será renovado.</span><span class="sxs-lookup"><span data-stu-id="f793c-119">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which will not be renewed.</span></span></P>
> <LI>
> <P><span data-ttu-id="f793c-120">Mais do que nunca, o Lync é uma ferramenta poderosa para a conexão entre organizações e pessoas ao redor do mundo.</span><span class="sxs-lookup"><span data-stu-id="f793c-120">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="f793c-121">A Federação com o Windows Live Messenger não requer licenças de usuário/dispositivo adicionais além da CAL padrão do Lync.</span><span class="sxs-lookup"><span data-stu-id="f793c-121">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="f793c-122">A Federação do Skype será adicionada a essa lista, permitindo que os usuários do Lync atinjam centenas de milhões de pessoas por meio de mensagens instantâneas e de voz.</span><span class="sxs-lookup"><span data-stu-id="f793c-122">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people through IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="f793c-123">Essa classe de Federação requer as seguintes considerações de planejamento:</span><span class="sxs-lookup"><span data-stu-id="f793c-123">This class of federation requires the following planning considerations:</span></span>

  - <span data-ttu-id="f793c-124">Os usuários do Windows Live Messenger podem ter áudio/comunicação visual ponto a ponto com usuários do Lync Server 2013, além de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="f793c-124">Windows Live Messenger users can have peer-to-peer audio/visual communication with Lync Server 2013 users, in addition to instant messaging.</span></span> <span data-ttu-id="f793c-125">Seus servidores de borda devem atender a requisitos específicos de portabilidade e protocolo.</span><span class="sxs-lookup"><span data-stu-id="f793c-125">Your Edge Servers must meet specific port and protocol requirements.</span></span> <span data-ttu-id="f793c-126">Para obter detalhes, consulte [determinar requisitos de firewall e porta externo A/V para o Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f793c-126">For details, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span></span>

  - <span data-ttu-id="f793c-127">O Yahoo mensagens instantâneas não tem requisitos exclusivos, além daqueles geralmente usados no planejamento e na implantação do servidor de borda típico que está fornecendo a Federação.</span><span class="sxs-lookup"><span data-stu-id="f793c-127">Yahoo instant messaging has no unique requirements, other than those typically used in the planning and deployment of the typical Edge Server that is providing federation.</span></span>

  - <span data-ttu-id="f793c-128">O America Online requer que o certificado do servidor de borda atribuído ao serviço de borda de acesso tenha um uso avançado de chave (EKU) do cliente.</span><span class="sxs-lookup"><span data-stu-id="f793c-128">America Online requires that your Edge Server certificate assigned to the Access Edge service has a client enhanced key usage (EKU).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f793c-129">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f793c-129">In This Section</span></span>

  - [<span data-ttu-id="f793c-130">Resumo do certificado-conectividade de mensagens instantâneas públicas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f793c-130">Certificate summary - Public instant messaging connectivity in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-public-instant-messaging-connectivity.md)

  - [<span data-ttu-id="f793c-131">Resumo de portabilidade-conectividade de mensagens instantâneas públicas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f793c-131">Port summary - Public instant messaging connectivity in Lync Server 2013</span></span>](lync-server-2013-port-summary-public-instant-messaging-connectivity.md)

  - <span data-ttu-id="f793c-132">[Resumo de DNS-conectividade de mensagens instantâneas públicas no Lync Server 2013](https://technet.microsoft.com/library/jj618375\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="f793c-132">[DNS summary - Public instant messaging connectivity in Lync Server 2013](https://technet.microsoft.com/library/jj618375\(v=ocs.15\))</span></span>

<span data-ttu-id="f793c-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f793c-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

