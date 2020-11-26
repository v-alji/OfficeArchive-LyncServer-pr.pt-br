---
title: Compatibilidade do Lync Server 2013 com resiliência de site metropolitano do Lync Server 2010
description: Compatibilidade do Lync Server 2013 com o Lync Server 2010 Metropolitana de recuperação de site.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2010 metropolitan site resiliency
ms:assetid: 18673ff6-b664-4a57-a89b-cbda8b129e6a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204715(v=OCS.15)
ms:contentKeyID: 48183526
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec72f261ac593b24bad13dcd400f495ba7ba0722
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434603"
---
# <a name="lync-server-2010-metropolitan-site-resiliency"></a>Resiliência de site metropolitano no Lync Server 2010

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2014-03-19_

A solução de resiliência de site metropolitana compatível com o Lync Server 2010 não é compatível com o Lync Server 2013. Esta solução envolve a inclusão de um único pool de front-end em dois data centers na mesma área metropolitana.

A solução Metropolitana de resiliência de site foi projetada para recuperar-se da perda de um data center completo. Quando você se estende pelo pool em dois datacenters, geralmente coloca metade dos seus front-ends em um datacenter e a outra metade do segundo datacenter. Se você perder um datacenter inteiro, perderá metade dos seus servidores front-end. Isso pode causar problemas com o novo modelo de sistema distribuído para pools de front-end no Lync Server 2013. Para obter mais informações, consulte [topologias e componentes para servidores front-end, mensagens instantâneas e presença no Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).

</div>

<span> </span>

</div>

</div>

</div>

