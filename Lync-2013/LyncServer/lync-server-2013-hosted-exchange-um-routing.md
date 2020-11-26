---
title: 'Lync Server 2013: Roteamento do Exchange UM hospedado'
description: 'Lync Server 2013: Hosted Routing Exchange UM.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange UM routing
ms:assetid: 6c90dc8b-6aef-4ce8-b483-37c7b5a553c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398512(v=OCS.15)
ms:contentKeyID: 48184422
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 72fbdee5550ae53d5ff5e7513ea384cedad62c5a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427584"
---
# <a name="hosted-exchange-um-routing-in-lync-server-2013"></a><span data-ttu-id="0b053-103">Roteamento do Exchange UM hospedado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b053-103">Hosted Exchange UM routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0b053-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0b053-104">

<span> </span></span></span>

<span data-ttu-id="0b053-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="0b053-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="0b053-106">O aplicativo de roteamento de UM do Exchange é executado no servidor front-end para direcionar chamadas, seja para uma implantação do Microsoft Exchange Server Unified Messaging (UM) local ou para o serviço UM do Exchange UM hospedado.</span><span class="sxs-lookup"><span data-stu-id="0b053-106">The Exchange UM Routing application runs on the Front End Server to route calls, either to an on-premises Microsoft Exchange Server Unified Messaging (UM) deployment or to hosted Exchange UM service.</span></span>

<div>

## <a name="the-exum-routing-application"></a><span data-ttu-id="0b053-107">O aplicativo de roteamento ExUM</span><span class="sxs-lookup"><span data-stu-id="0b053-107">The ExUM Routing Application</span></span>

<span data-ttu-id="0b053-108">O aplicativo de roteamento do Exchange UM do Lync Server 2013 usa as informações das configurações da conta do usuário e dos parâmetros da política de caixa postal hospedadas para determinar como direcionar chamadas para mensagens de voz hospedadas, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b053-108">The Lync Server 2013 Exchange UM Routing application uses information from user account settings and from hosted voice mail policy parameters to determine how to route calls for hosted voice messaging, as shown in the following diagram.</span></span>

<span data-ttu-id="0b053-109">**Exemplo de implantação mista de roteamento UM do Exchange**</span><span class="sxs-lookup"><span data-stu-id="0b053-109">**Example of mixed deployment Exchange UM routing**</span></span>

<span data-ttu-id="0b053-110">![Implantação do Exchange UM do Lync Server local](images/Gg398512.75258286-1f23-487b-bf46-d8538e7d540e(OCS.15).jpg "Implantação do Exchange UM do Lync Server local")</span><span class="sxs-lookup"><span data-stu-id="0b053-110">![On-premises Lync Server Exchange UM deployment](images/Gg398512.75258286-1f23-487b-bf46-d8538e7d540e(OCS.15).jpg "On-premises Lync Server Exchange UM deployment")</span></span>

<span data-ttu-id="0b053-111">O roteamento do Exchange UM pode ser configurado para direcionar chamadas para usuários que estão habilitados para o Exchange um local, para usuários que estão habilitados para um Exchange UM hospedado ou para uma combinação dos dois.</span><span class="sxs-lookup"><span data-stu-id="0b053-111">Exchange UM routing can be configured to route calls to users who are enabled for on-premises Exchange UM, to users who are enabled for hosted Exchange UM, or to a combination of the two.</span></span>

<span data-ttu-id="0b053-112">Por exemplo, suponha que a caixa de correio de Roy e o serviço do Exchange UM sejam hospedados em uma implantação local do Exchange.</span><span class="sxs-lookup"><span data-stu-id="0b053-112">For example, suppose that Roy’s mailbox and Exchange UM service are homed in an on-premises Exchange deployment.</span></span>

  - <span data-ttu-id="0b053-113">As informações de endereço proxy da conta de usuário Roy fornecem as informações que o aplicativo de roteamento ExUM usa para direcionar as chamadas para um servidor do Exchange UM local.</span><span class="sxs-lookup"><span data-stu-id="0b053-113">The proxy address information from Roy’s user account provides the information that the ExUM Routing application uses to route his calls to an on-premises Exchange UM server.</span></span>

<span data-ttu-id="0b053-114">A caixa de correio de Alice e o serviço do Exchange UM estão localizados em um data center do provedor de serviços do Exchange hospedado.</span><span class="sxs-lookup"><span data-stu-id="0b053-114">Alice’s mailbox and Exchange UM service are located at a hosted Exchange service provider’s data center.</span></span> <span data-ttu-id="0b053-115">O roteamento para suas chamadas de UM do Exchange é configurado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0b053-115">Routing for her Exchange UM calls is configured as follows:</span></span>

  - <span data-ttu-id="0b053-116">Os valores definidos no atributo msExchUCVoiceMailSettings da conta de usuário de Alice dizem para o aplicativo de roteamento ExUM verificar se há detalhes de roteamento em uma política de caixa postal hospedada.</span><span class="sxs-lookup"><span data-stu-id="0b053-116">The values set in the msExchUCVoiceMailSettings attribute of Alice’s user account tell the ExUM Routing application to check for routing details in a hosted voice mail policy.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0b053-117">O valor do atributo msExchUCVoiceMailSettings pode ser definido por um provedor de serviços do Exchange ou pelo administrador do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0b053-117">The value of the msExchUCVoiceMailSettings attribute can be set by either the Exchange service provider or the Lync Server 2013 administrator.</span></span> <span data-ttu-id="0b053-118">No exemplo mostrado no diagrama anterior, o valor (CsHostedVoiceMail = 1) foi definido pelo administrador do Lync Server 2013 para habilitar a caixa postal hospedada para Alice.</span><span class="sxs-lookup"><span data-stu-id="0b053-118">In the example shown in the preceding diagram, the value (CsHostedVoiceMail=1) was set by the Lync Server 2013 administrator to enable hosted voice mail for Alice.</span></span> <span data-ttu-id="0b053-119">Para obter detalhes sobre esse atributo, consulte <A href="lync-server-2013-hosted-exchange-user-management.md">Gerenciamento de usuários hospedados do Exchange no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="0b053-119">For details about this attribute, see <A href="lync-server-2013-hosted-exchange-user-management.md">Hosted Exchange user management in Lync Server 2013</A>.</span></span>

    
    </div>

  - <span data-ttu-id="0b053-120">A política de caixa postal hospedada que é atribuída à conta de usuário de Alice fornece detalhes de roteamento:</span><span class="sxs-lookup"><span data-stu-id="0b053-120">The hosted voice mail policy that is assigned to Alice’s user account provides routing details:</span></span>
    
      - <span data-ttu-id="0b053-121">Destino é o provedor de serviços de UM do Exchange UM (ls) hospedado. ExUm. \<hostedExchangeServer\> . com neste exemplo).</span><span class="sxs-lookup"><span data-stu-id="0b053-121">Destination is the hosted Exchange UM service provider (ls.ExUm.\<hostedExchangeServer\>.com in this example).</span></span>
    
      - <span data-ttu-id="0b053-122">As organizações são identificadas pelas IDs de locatários, que são os FQDNs de roteamento para as mensagens SIP para locatários do Exchange Server localizados em ls. ExUm. \<hostedExchangeServer\> . com (corp.contoso.com e corp.litwareinc.com neste exemplo).</span><span class="sxs-lookup"><span data-stu-id="0b053-122">Organizations are identified by the tenant IDs, which are the routing FQDNs for SIP messages for Exchange Server tenants that are located on ls.ExUm.\<hostedExchangeServer\>.com (corp.contoso.com and corp.litwareinc.com in this example).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="0b053-123">O FQDN para Exchange Online é exap.um.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="0b053-123">The FQDN for Exchange Online is exap.um.outlook.com.</span></span>

        
        </div>
        
        <span data-ttu-id="0b053-124">Para obter detalhes, consulte [políticas de caixa postal hospedadas no Lync Server 2013](lync-server-2013-hosted-voice-mail-policies.md).</span><span class="sxs-lookup"><span data-stu-id="0b053-124">For details, see [Hosted voice mail policies in Lync Server 2013](lync-server-2013-hosted-voice-mail-policies.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0b053-125">Se o atributo msExchUCVoiceMailSettings e as configurações de endereço de proxy de UM estiverem presentes em uma conta de usuário, o atributo msExchUCVoiceMailSettings terá precedência.</span><span class="sxs-lookup"><span data-stu-id="0b053-125">If both the msExchUCVoiceMailSettings attribute and the UM proxy address settings are present in a user account, the msExchUCVoiceMailSettings attribute takes precedence.</span></span>



<span data-ttu-id="0b053-126"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0b053-126"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

