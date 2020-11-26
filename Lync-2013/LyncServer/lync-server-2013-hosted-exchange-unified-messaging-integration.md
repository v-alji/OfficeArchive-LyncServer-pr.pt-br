---
title: 'Lync Server 2013: Integração de Unificação de Mensagens do Exchange hospedado'
description: 'Lync Server 2013: integração de Unificação de mensagens do Exchange hospedada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange Unified Messaging integration
ms:assetid: f4de0165-da3b-499e-98fc-28ddd0db02d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413027(v=OCS.15)
ms:contentKeyID: 48185829
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 980c0bc47258e9fae94ff623559342ca36eea145
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427527"
---
# <a name="hosted-exchange-unified-messaging-integration-in-lync-server-2013"></a><span data-ttu-id="e2317-103">Integração de Unificação de Mensagens do Exchange hospedado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2317-103">Hosted Exchange Unified Messaging integration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e2317-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e2317-104">

<span> </span></span></span>

<span data-ttu-id="e2317-105">_**Tópico da última modificação:** 2012-09-20_</span><span class="sxs-lookup"><span data-stu-id="e2317-105">_**Topic Last Modified:** 2012-09-20_</span></span>

<span data-ttu-id="e2317-106">Além do suporte que versões anteriores do Lync Server 2013 oferecidas para integração com implantações *locais* da Unificação de mensagens do Exchange (um), o Lync Server 2013 introduz o suporte para integração com o Exchange um *hospedado* .</span><span class="sxs-lookup"><span data-stu-id="e2317-106">In addition to the support that previous Lync Server 2013 releases have provided for integration with *on-premises* deployments of Exchange Unified Messaging (UM), Lync Server 2013 introduces support for integration with *hosted* Exchange UM.</span></span> <span data-ttu-id="e2317-107">Hosted Exchange UM permite que o Lync Server 2013 forneça mensagens de voz para seus usuários se você transferir alguns ou todos eles para um provedor de serviços do Exchange hospedado, como o Microsoft Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="e2317-107">Hosted Exchange UM enables Lync Server 2013 to provide voice messaging to your users if you transfer some or all of them to a hosted Exchange service provider such as Microsoft Exchange Online.</span></span>

<span data-ttu-id="e2317-108">Lync Server 2013 Enterprise Voice usa a infraestrutura de UM do Exchange para fornecer atendimento de chamada, notificação de chamada, acesso de voz (incluindo caixa postal) e serviços de atendedor automático.</span><span class="sxs-lookup"><span data-stu-id="e2317-108">Lync Server 2013 Enterprise Voice uses the Exchange UM infrastructure to provide call answering, call notification, voice access (including voice mail), and auto attendant services.</span></span> <span data-ttu-id="e2317-109">Para obter detalhes, consulte [recursos de Unificação de mensagens integrada e Lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="e2317-109">For details, see [Features of integrated Unified Messaging and Lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e2317-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="e2317-110">In This Section</span></span>

  - [<span data-ttu-id="e2317-111">Arquitetura e roteamento do Exchange UM hospedado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2317-111">Hosted Exchange UM architecture and routing in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-um-architecture-and-routing.md)

  - [<span data-ttu-id="e2317-112">Políticas de correio de voz hospedado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2317-112">Hosted voice mail policies in Lync Server 2013</span></span>](lync-server-2013-hosted-voice-mail-policies.md)

  - [<span data-ttu-id="e2317-113">Gerenciamento de usuário no Exchange hospedado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2317-113">Hosted Exchange user management in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-user-management.md)

  - [<span data-ttu-id="e2317-114">Gerenciamento de objeto de Contato no Exchange hospedado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2317-114">Hosted Exchange Contact object management in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-contact-object-management.md)

  - [<span data-ttu-id="e2317-115">Processo de implantação para integrar o Exchange UM hospedado ao Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2317-115">Deployment process for integrating hosted Exchange UM with Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-integrating-hosted-exchange-um.md)

<span data-ttu-id="e2317-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e2317-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

