---
title: 'Lync Server 2013: Suporte ao sistema de mensagens instantâneas públicas'
description: 'Lync Server 2013: suporte público a mensagens instantâneas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Public instant messaging support
ms:assetid: 1f45163b-52c6-4a78-b9c8-dfe3abe4e5eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204732(v=OCS.15)
ms:contentKeyID: 48183582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e071e8b79be82d865a85a9488e48dd0a4264c7f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390082"
---
# <a name="public-instant-messaging-support-in-lync-server-2013"></a><span data-ttu-id="9a893-103">Suporte ao sistema de mensagens instantâneas públicas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a893-103">Public instant messaging support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a893-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a893-104">

<span> </span></span></span>

<span data-ttu-id="9a893-105">_**Tópico da última modificação:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="9a893-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="9a893-106">O Lync Server 2013 oferece suporte ao uso de provedores de conectividade de mensagens instantâneas (IM) licenciadas, bem como ao uso do protocolo de mensagens instantâneas (IM) licenciado, bem como ao uso de um servidor do Lync para acessar parceiros de domínio do XMPP configurados usando o cliente Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="9a893-106">Lync Server 2013 supports the use of licensed public instant messaging (IM) connectivity providers, as well as the use of eXtensible Messaging and Presence Protocol (XMPP) to implement a special type of federation that enables a Lync Server to access configured XMPP domain partners by using the Lync 2013 client.</span></span>

<div>

## <a name="public-im-connectivity-provider-support"></a><span data-ttu-id="9a893-107">Suporte a provedores de conectividade de mensagens de chat públicas</span><span class="sxs-lookup"><span data-stu-id="9a893-107">Public IM Connectivity Provider Support</span></span>

<span data-ttu-id="9a893-108">Os parceiros de conectividade de mensagens instantâneas públicas com suporte no momento são:</span><span class="sxs-lookup"><span data-stu-id="9a893-108">The currently supported public instant messaging connectivity partners are:</span></span>

  - <span data-ttu-id="9a893-109">America Online</span><span class="sxs-lookup"><span data-stu-id="9a893-109">America Online</span></span>

  - <span data-ttu-id="9a893-110">Windows Live</span><span class="sxs-lookup"><span data-stu-id="9a893-110">Windows Live</span></span>

  - <span data-ttu-id="9a893-111">Instant\!</span><span class="sxs-lookup"><span data-stu-id="9a893-111">Yahoo\!</span></span>

<span data-ttu-id="9a893-112">Para comunicações com usuários do Windows Live, o Lync Server 2013 suporta mensagens instantâneas ponto a ponto e chamadas de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="9a893-112">For communications with Windows Live users, Lync Server 2013 supports peer-to-peer IM and audio and video calls.</span></span> <span data-ttu-id="9a893-113">Para comunicações com AOL e Yahoo \! , o Lync Server 2013 dá suporte a im ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="9a893-113">For communications with AOL and Yahoo\!, Lync Server 2013 supports peer-to-peer IM.</span></span> <span data-ttu-id="9a893-114">Uma licença separada pode ser necessária.</span><span class="sxs-lookup"><span data-stu-id="9a893-114">A separate license may be required.</span></span>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="9a893-115">A partir de 1º de setembro de 2012, a licença de assinatura de usuário da conectividade de mensagem de chat pública do Microsoft Lync ("PIC USL") não está mais disponível para compra de contratos novos ou de renovação.</span><span class="sxs-lookup"><span data-stu-id="9a893-115">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="9a893-116">Os clientes com licenças ativas poderão continuar a federar-se com o Yahoo!</span><span class="sxs-lookup"><span data-stu-id="9a893-116">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="9a893-117">Messenger até a data de encerramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="9a893-117">Messenger until the service shut down date.</span></span> <span data-ttu-id="9a893-118">Uma data de fim da vida útil de junho de 2014 para AOL e Yahoo!</span><span class="sxs-lookup"><span data-stu-id="9a893-118">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="9a893-119">foi anunciado.</span><span class="sxs-lookup"><span data-stu-id="9a893-119">has been announced.</span></span> <span data-ttu-id="9a893-120">Para obter detalhes, consulte <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">suporte para conectividade de mensagens instantâneas públicas no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9a893-120">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="9a893-121">O PIC USL é uma licença de assinatura por usuário por mês necessária para o Lync Server ou o Office Communications Server se federar com o Yahoo!</span><span class="sxs-lookup"><span data-stu-id="9a893-121">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="9a893-122">Spam.</span><span class="sxs-lookup"><span data-stu-id="9a893-122">Messenger.</span></span> <span data-ttu-id="9a893-123">A capacidade da Microsoft de oferecer esse serviço por meio do suporte do Yahoo!, o contrato subjacente para o qual está prestes a ser enrolado.</span><span class="sxs-lookup"><span data-stu-id="9a893-123">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="9a893-124">Mais do que nunca, o Lync é uma ferramenta poderosa para a conexão entre organizações e pessoas ao redor do mundo.</span><span class="sxs-lookup"><span data-stu-id="9a893-124">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="9a893-125">A Federação com o Windows Live Messenger não requer licenças de usuário/dispositivo adicionais além da CAL padrão do Lync.</span><span class="sxs-lookup"><span data-stu-id="9a893-125">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="9a893-126">A Federação do Skype será adicionada a essa lista, permitindo que os usuários do Lync atinjam centenas de milhões de pessoas com mensagens instantâneas e voz.</span><span class="sxs-lookup"><span data-stu-id="9a893-126">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>



</div>

</div>

<div>

## <a name="xmpp-federation-support"></a><span data-ttu-id="9a893-127">Suporte à Federação do XMPP</span><span class="sxs-lookup"><span data-stu-id="9a893-127">XMPP Federation Support</span></span>

<span data-ttu-id="9a893-128">A Federação do XMPP oferece suporte à comunicação dos usuários do Lync com usuários de domínio do XMPP configurados que usam um provedor público, como GTalk.</span><span class="sxs-lookup"><span data-stu-id="9a893-128">XMPP federation supports Lync users communication with configured XMPP domain users who use a public provider, such as GTalk.</span></span> <span data-ttu-id="9a893-129">As comunicações com esses usuários podem incluir o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9a893-129">Communications with these users can include the following:</span></span>

  - <span data-ttu-id="9a893-130">Mensagem instantânea e presença ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="9a893-130">Peer-to-peer IM and presence</span></span>

  - <span data-ttu-id="9a893-131">Criação de contatos federados do XMPP no cliente do Lync</span><span class="sxs-lookup"><span data-stu-id="9a893-131">Creation of XMPP federated contacts in the Lync client</span></span>

<span data-ttu-id="9a893-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a893-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

