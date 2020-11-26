---
title: Resumo da porta – Federação do protocolo de presença e de mensagens extensíveis (XMPP)
description: Resumo da porta – Federação do protocolo de presença e de mensagens extensíveis (XMPP).
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary -  Extensible messaging and presence protocol (XMPP) federation
ms:assetid: 62e98fab-7add-4983-a3fa-dbe74e1c3849
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618371(v=OCS.15)
ms:contentKeyID: 49105658
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9508bc8b9fbcca6fb6a37478def258a9fa52c373
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442800"
---
# <a name="port-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="c4463-103">Resumo de portas – Federação de protocolo de presença e mensagens extensíveis (XMPP) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4463-103">Port summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c4463-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c4463-104">

<span> </span></span></span>

<span data-ttu-id="c4463-105">_**Tópico da última modificação:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="c4463-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="c4463-106">As portas e protocolos definidos para o proxy de protocolo de presença e mensagens extensível (XMPP) implantadas no servidor de borda permitem comunicações do parceiro federado do XMPP com o servidor de borda e também permite a comunicação do servidor de borda com o parceiro federado do XMPP.</span><span class="sxs-lookup"><span data-stu-id="c4463-106">The ports and protocols defined for the extensible messaging and presence protocol (XMPP) proxy deployed on the Edge Server allow communications from the XMPP federated partner to the Edge Server, and also allows communication from your Edge Server to the XMPP federated partner.</span></span> <span data-ttu-id="c4463-107">Uma regra também é definida no firewall de face interna do servidor front-end ou do pool de front-ends para o servidor de borda ou o pool de bordas.</span><span class="sxs-lookup"><span data-stu-id="c4463-107">A rule is also defined on the internal-facing firewall from the Front End Server or Front End pool to the Edge Server or Edge pool.</span></span>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="c4463-108">Resumo de firewall para mensagens extensíveis e protocolo de presença</span><span class="sxs-lookup"><span data-stu-id="c4463-108">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c4463-109">Protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="c4463-109">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="c4463-110">Fonte (endereço IP)</span><span class="sxs-lookup"><span data-stu-id="c4463-110">Source (IP address)</span></span></th>
<th><span data-ttu-id="c4463-111">Destino (endereço IP)</span><span class="sxs-lookup"><span data-stu-id="c4463-111">Destination (IP address)</span></span></th>
<th><span data-ttu-id="c4463-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4463-112">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4463-113">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="c4463-113">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="c4463-114">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="c4463-114">Any</span></span></p></td>
<td><p><span data-ttu-id="c4463-115">Endereço IP da interface do serviço de borda do Access</span><span class="sxs-lookup"><span data-stu-id="c4463-115">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="c4463-116">Porta de comunicação de servidor para servidor padrão para XMPP.</span><span class="sxs-lookup"><span data-stu-id="c4463-116">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="c4463-117">Permite a comunicação com o servidor de borda XMPP o proxy de parceiros de XMPP federado</span><span class="sxs-lookup"><span data-stu-id="c4463-117">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4463-118">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="c4463-118">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="c4463-119">Endereço IP da interface do serviço de borda do Access</span><span class="sxs-lookup"><span data-stu-id="c4463-119">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="c4463-120">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="c4463-120">Any</span></span></p></td>
<td><p><span data-ttu-id="c4463-121">Porta de comunicação de servidor para servidor padrão para XMPP.</span><span class="sxs-lookup"><span data-stu-id="c4463-121">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="c4463-122">Permite a comunicação do proxy do servidor de borda XMPP com parceiros do XMPP federado</span><span class="sxs-lookup"><span data-stu-id="c4463-122">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4463-123">XMPP/MTLS/23456</span><span class="sxs-lookup"><span data-stu-id="c4463-123">XMPP/MTLS/23456</span></span></p></td>
<td><p><span data-ttu-id="c4463-124">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="c4463-124">Any</span></span></p></td>
<td><p><span data-ttu-id="c4463-125">IP de interface do servidor de borda interna</span><span class="sxs-lookup"><span data-stu-id="c4463-125">Internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="c4463-126">Tráfego de XMPP interno do Gateway XMPP no servidor front-end ou do pool de front-end para o servidor de borda</span><span class="sxs-lookup"><span data-stu-id="c4463-126">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c4463-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4463-127">See Also</span></span>


[<span data-ttu-id="c4463-128">Exemplo de configuração de XMPP no Lync Server 2013 – federação XMPP com Google Talk</span><span class="sxs-lookup"><span data-stu-id="c4463-128">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[<span data-ttu-id="c4463-129">Gerenciar parceiros XMPP federados no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4463-129">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
  

<span data-ttu-id="c4463-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c4463-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

