---
title: 'Lync Server 2013: Normalização de controle de chamada remota e de número de telefone'
description: 'Lync Server 2013: controle de chamada remota e normalização do número de telefone.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remote call control and phone number normalization
ms:assetid: 291d9e87-4c65-4ea2-888f-517741391de5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558630(v=OCS.15)
ms:contentKeyID: 48183696
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: edcb50678da7111aba066745bce5e356dd1ac7f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436500"
---
# <a name="remote-call-control-and-phone-number-normalization-in-lync-server-2013"></a><span data-ttu-id="1248d-103">Normalização de controle de chamada remota e de número de telefone no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1248d-103">Remote call control and phone number normalization in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1248d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1248d-104">

<span> </span></span></span>

<span data-ttu-id="1248d-105">_**Tópico da última modificação:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="1248d-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="1248d-106">Os clientes do Lync baixam as regras de normalização do número de telefone como parte do download do arquivo ABS (serviço de catálogo de endereços).</span><span class="sxs-lookup"><span data-stu-id="1248d-106">Lync clients download phone number normalization rules as part of the Address Book Service (ABS) file download.</span></span> <span data-ttu-id="1248d-107">Em cenários de controle de chamada remota, as regras de normalização do número de telefone do serviço de catálogo de endereços são aplicadas às chamadas de controle de chamada remota de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="1248d-107">In remote call control scenarios, Address Book Service phone number normalization rules are applied to both incoming and outgoing remote call control calls.</span></span> <span data-ttu-id="1248d-108">Para chamadas recebidas para um usuário habilitado para controle de chamada remota, o número de telefone do chamador é inicialmente normalizado para o formato E. 164 pelo gateway de SIP/CSTA ou PBX (Agência telefônica privada).</span><span class="sxs-lookup"><span data-stu-id="1248d-108">For incoming calls to a remote call control-enabled user, the phone number of the caller is first normalized to E.164 format by either the SIP/CSTA gateway or private branch exchange (PBX).</span></span> <span data-ttu-id="1248d-109">Quando o Lync Server 2013 recebe a chamada do gateway, ele executa a pesquisa de número reverso (RNL) no número de telefone do chamador em relação ao número normalizado na lista de contatos do Microsoft Office Outlook ou a GAL (lista de endereços global) do Microsoft Office Outlook que está armazenada no serviço de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="1248d-109">When Lync Server 2013 receives the call from the gateway, it performs reverse number lookup (RNL) on the phone number of the caller against the normalized number in the callee’s Microsoft Office Outlook Contacts list or the global address list (GAL) that is stored in the Address Book Service.</span></span> <span data-ttu-id="1248d-110">Se a pesquisa de número reverso localizar uma correspondência com êxito, o chamador será identificado por nome na notificação de chamada de entrada.</span><span class="sxs-lookup"><span data-stu-id="1248d-110">If reverse number lookup successfully finds a match, the caller is identified by name in the incoming call notification.</span></span>

<span data-ttu-id="1248d-111">Para chamadas de controle de chamadas remotas de saída, o Lync aplica as regras de normalização de número de telefone do serviço de catálogo de endereços para o número discado antes de rotear a chamada para o gateway SIP/CSTA.</span><span class="sxs-lookup"><span data-stu-id="1248d-111">For outgoing remote call control calls, Lync applies the Address Book Service phone number normalization rules to the dialed number before routing the call to the SIP/CSTA gateway.</span></span>

<span data-ttu-id="1248d-112">Para obter detalhes sobre como criar regras de normalização de número de telefone para o controle de chamada remota, consulte [regras de discagem e planos de normalização no Lync Server 2013](lync-server-2013-dial-plans-and-normalization-rules.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="1248d-112">For details about creating phone number normalization rules for remote call control, see [Dial plans and normalization rules in Lync Server 2013](lync-server-2013-dial-plans-and-normalization-rules.md) in the Planning documentation.</span></span>

<div>

## <a name="migrating-phone-number-normalization-rules"></a><span data-ttu-id="1248d-113">Migrando regras de normalização de número de telefone</span><span class="sxs-lookup"><span data-stu-id="1248d-113">Migrating Phone Number Normalization Rules</span></span>

<span data-ttu-id="1248d-114">Se você estiver migrando usuários anteriormente habilitados para controle de chamada remota, consulte os tópicos a seguir na documentação de migração:</span><span class="sxs-lookup"><span data-stu-id="1248d-114">If you are migrating users previously enabled for remote call control, see the following topics in the Migration documentation:</span></span>

  - <span data-ttu-id="1248d-115">Para o Lync Server 2010, consulte [migrar catálogo de endereços](migrate-address-book.md) na documentação de migração.</span><span class="sxs-lookup"><span data-stu-id="1248d-115">For Lync Server 2010, see [Migrate Address Book](migrate-address-book.md) in the Migration documentation.</span></span>

  - <span data-ttu-id="1248d-116">Para o Communications Server 2007 R2, confira [migrar o catálogo de endereços](migrate-address-book.md) na documentação de migração.</span><span class="sxs-lookup"><span data-stu-id="1248d-116">For Communications Server 2007 R2, see [Migrate Address Book](migrate-address-book.md) in the Migration documentation.</span></span>

<span data-ttu-id="1248d-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1248d-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

