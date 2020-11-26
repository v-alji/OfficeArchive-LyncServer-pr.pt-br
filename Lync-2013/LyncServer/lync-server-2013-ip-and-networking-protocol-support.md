---
title: 'Lync Server 2013: Suporte a protocolo IP e de rede'
description: 'Lync Server 2013: suporte a protocolo IP e de rede.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IP and networking protocol support
ms:assetid: b0cffb10-3478-445c-89c7-8cb8b5027424
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412848(v=OCS.15)
ms:contentKeyID: 48185128
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbd8022dd7197524334e0c70ea0ad875a30446de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426743"
---
# <a name="ip-and-networking-protocol-support-in-lync-server-2013"></a><span data-ttu-id="3a6fc-103">Suporte a protocolo IP e de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3a6fc-103">IP and networking protocol support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3a6fc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3a6fc-104">

<span> </span></span></span>

<span data-ttu-id="3a6fc-105">_**Tópico da última modificação:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="3a6fc-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="3a6fc-106">O Lync Server 2013 dá suporte aos seguintes protocolos de IP e de rede:</span><span class="sxs-lookup"><span data-stu-id="3a6fc-106">Lync Server 2013 supports the following IP and networking protocols:</span></span>

  - <span data-ttu-id="3a6fc-107">**Protocolos IP.**</span><span class="sxs-lookup"><span data-stu-id="3a6fc-107">**IP Protocols.**</span></span>   <span data-ttu-id="3a6fc-108">O Lync Server 2013 oferece suporte ao IP versão 4 (IPv4) ou IP versão 6 (IPv6) para a rede do servidor.</span><span class="sxs-lookup"><span data-stu-id="3a6fc-108">Lync Server 2013 supports either IP version 4 (IPv4) or IP version 6 (IPv6) for the server network.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3a6fc-109">O Lync Server 2013 pode funcionar em uma rede com a pilha de IP duplo habilitada.</span><span class="sxs-lookup"><span data-stu-id="3a6fc-109">Lync Server 2013 can function in a network with dual IP stack enabled.</span></span>

    
    </div>

  - <span data-ttu-id="3a6fc-110">**Protocolos de transporte SIP.**</span><span class="sxs-lookup"><span data-stu-id="3a6fc-110">**SIP Transport Protocols.**</span></span>   <span data-ttu-id="3a6fc-111">Em geral, o SIP pode usar pelo menos três tipos de transporte: protocolo UDP, protocolo de controle de transmissão (TCP) e Transport Layer Security (TLS).</span><span class="sxs-lookup"><span data-stu-id="3a6fc-111">Generically, SIP can use at least three transport types: User Datagram Protocol (UDP), Transmission Control Protocol (TCP), and Transport Layer Security (TLS).</span></span> <span data-ttu-id="3a6fc-112">Na configuração de transporte SIP padrão, o TLS é executado sobre TCP.</span><span class="sxs-lookup"><span data-stu-id="3a6fc-112">In the default SIP transport configuration, TLS runs over TCP.</span></span> <span data-ttu-id="3a6fc-113">O TLS é usado na rede do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3a6fc-113">TLS is used within the Lync Server 2013 network.</span></span> <span data-ttu-id="3a6fc-114">Na borda da rede, o Lync Server 2013 pode interoperar via TCP.</span><span class="sxs-lookup"><span data-stu-id="3a6fc-114">At the edge of the network, Lync Server 2013 can interoperate over TCP.</span></span> <span data-ttu-id="3a6fc-115">O Lync Server 2013 não é compatível com o UDP para transporte SIP porque ele não atende aos padrões mínimos de segurança, confiabilidade e escalabilidade de comunicação corporativa.</span><span class="sxs-lookup"><span data-stu-id="3a6fc-115">Lync Server 2013 does not support UDP for SIP transport because it doesn’t meet the minimum standards for enterprise communications security, reliability, and scalability.</span></span> <span data-ttu-id="3a6fc-116">Para obter detalhes, consulte o artigo sobre o blog NextHop, "para UDP ou não para UDP, que é a pergunta" em [https://go.microsoft.com/fwlink/p/?linkId=185369](https://go.microsoft.com/fwlink/p/?linkid=185369) .</span><span class="sxs-lookup"><span data-stu-id="3a6fc-116">For details, see the NextHop blog article, "To UDP, or not to UDP, that is the question," at [https://go.microsoft.com/fwlink/p/?linkId=185369](https://go.microsoft.com/fwlink/p/?linkid=185369).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3a6fc-117">O conteúdo de cada blog e sua URL estão sujeitos a alterações sem aviso prévio.</span><span class="sxs-lookup"><span data-stu-id="3a6fc-117">The content of each blog and its URL are subject to change without notice.</span></span>

    
    <span data-ttu-id="3a6fc-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3a6fc-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

