---
title: 'Lync Server 2013: Suporte à integração Exchange UM hospedado'
description: Suporte do Lync Server 2013 para a integração do Exchange UM hospedada.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Support for hosted Exchange UM integration
ms:assetid: c7573ec3-013c-48d9-b59b-2a5427e6da35
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398821(v=OCS.15)
ms:contentKeyID: 48185376
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 88920667d703bc634921903e8e3995cb65db6873
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389762"
---
# <a name="support-for-hosted-exchange-um-integration-in-lync-server-2013"></a><span data-ttu-id="371e2-103">Suporte à integração Exchange UM hospedado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="371e2-103">Support for hosted Exchange UM integration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="371e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="371e2-104">

<span> </span></span></span>

<span data-ttu-id="371e2-105">_**Tópico da última modificação:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="371e2-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="371e2-106">O aplicativo de roteamento ExUM do Lync Server 2013 é compatível com a integração com o Exchange Unified Messaging (UM) em um ambiente local, no qual o Lync Server 2013 e o Exchange UM são instalados localmente na sua empresa ou em UM host UM hospedado por um provedor de serviços, como mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="371e2-106">The Lync Server 2013 ExUM Routing application supports integration with Exchange Unified Messaging (UM) in an on-premises environment, where Lync Server 2013 and Exchange UM are both installed locally within your enterprise, or in with Exchange UM hosted by a service provider, as shown in the following diagram.</span></span>

<span data-ttu-id="371e2-107">![Implantação do Exchange UM do Lync Server local](images/Gg398821.d6498eb9-87ee-40f3-8ecd-852f91546590(OCS.15).jpg "Implantação do Exchange UM do Lync Server local")</span><span class="sxs-lookup"><span data-stu-id="371e2-107">![On-premises Lync Server Exchange UM Deployment](images/Gg398821.d6498eb9-87ee-40f3-8ecd-852f91546590(OCS.15).jpg "On-premises Lync Server Exchange UM Deployment")</span></span>

<span data-ttu-id="371e2-108">Há suporte para os seguintes modos:</span><span class="sxs-lookup"><span data-stu-id="371e2-108">The following modes are supported:</span></span>

  - <span data-ttu-id="371e2-109">**Modo local**   O Lync Server 2013 e o Exchange UM são implantados em servidores locais dentro da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="371e2-109">**On-premises Mode**   Lync Server 2013 and Exchange UM are both deployed on local servers within your enterprise.</span></span>

  - <span data-ttu-id="371e2-110">**Modo intersite**   O Lync Server 2013 é implantado em servidores locais na sua empresa e o Exchange UM está hospedado em um recurso do provedor de serviços online, como um Data Center online do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="371e2-110">**Cross-premises Mode**   Lync Server 2013 is deployed on local servers within your enterprise and Exchange UM is hosted in an online service provider’s facility, such as a Microsoft Exchange Online data center.</span></span>

  - <span data-ttu-id="371e2-111">**Modo misto**   A implantação do Lync Server 2013 tem algumas caixas de correio de usuário hospedadas em servidores locais que executam o Microsoft Exchange Server na sua empresa e algumas caixas de correio hospedadas em um data center do serviço do Exchange hospedado.</span><span class="sxs-lookup"><span data-stu-id="371e2-111">**Mixed Mode**   Your Lync Server 2013 deployment has some user mailboxes homed on local servers running Microsoft Exchange Server within your enterprise and some mailboxes homed in a hosted Exchange service data center.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="371e2-112">O modo misto pode ser usado como uma solução de transição durante a avaliação e Stepwise a migração de usuários para o Exchange UM hospedada ou como uma solução permanente se você optar por manter os serviços de UM dos usuários no local após a migração de outras pessoas.</span><span class="sxs-lookup"><span data-stu-id="371e2-112">Mixed mode can be used as a transitional solution during evaluation and stepwise migration of users to hosted Exchange UM, or as a permanent solution if you opt to keep some users’ Exchange UM services on-premises after migrating others.</span></span>

    
    </div>

<span data-ttu-id="371e2-113">Para integrar o Lync Server 2013 com o Exchange UM hospedado, você deve configurar um *espaço de endereço SIP compartilhado* (também chamado de *domínio dividido*).</span><span class="sxs-lookup"><span data-stu-id="371e2-113">To integrate Lync Server 2013 with hosted Exchange UM, you must configure a *shared SIP address space* (also called a *split domain*).</span></span> <span data-ttu-id="371e2-114">Nesta configuração, o Lync Server 2013 e o provedor de serviços do Exchange UM hospedado por terceiros podem acessar o mesmo espaço de endereço de domínio SIP.</span><span class="sxs-lookup"><span data-stu-id="371e2-114">In this configuration, both Lync Server 2013 and the third-party hosted Exchange UM service provider can access the same SIP domain address space.</span></span> <span data-ttu-id="371e2-115">Para obter detalhes, consulte [arquitetura de integração de um Exchange um hospedada no Lync Server 2013](lync-server-2013-hosted-exchange-um-integration-architecture.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="371e2-115">For details, see [Hosted Exchange UM integration architecture in Lync Server 2013](lync-server-2013-hosted-exchange-um-integration-architecture.md) in the Planning documentation.</span></span>

<span data-ttu-id="371e2-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="371e2-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

