---
title: 'Lync Server 2013: Novo recurso de tronco'
description: 'Lync Server 2013: novo recurso de tronco.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New trunk feature
ms:assetid: 9b398bc8-2760-4218-b1a4-89b9694b1171
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688152(v=OCS.15)
ms:contentKeyID: 49733755
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d8f923ceada899608cc350bd1343345c12d0996b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445334"
---
# <a name="new-trunk-feature-in-lync-server-2013"></a>Novo recurso de tronco no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-21_

No Microsoft Lync Server 2013, vários troncos entre um servidor de mediação e um gateway podem ser definidos. O Microsoft Lync Server 2010 é permitido apenas para um único tronco entre um servidor de mediação e um gateway PSTN. Esse recurso fornece a flexibilidade para definir troncos adicionais. Um tronco é uma associação lógica entre um FQDN do servidor de mediação e uma porta de escuta e uma porta de escuta e FQDN do gateway PSTN. Essa nova funcionalidade permite uma definição de tronco fácil para resiliência (em que vários servidores de mediação podem ser usados para direcionar chamadas para o mesmo gateway PSTN), para a interoperabilidade de PBX, em que vários troncos com políticas associadas diferentes podem ser usados entre o IP-PBX e um servidor de mediação e as configurações de tronco SIP em que os servidores de mediação em sites diferentes têm troncos SIP para a portadora referenciada pelo mesmo FQDN da operadora.

<div>

## <a name="see-also"></a>Confira também


[Novos recursos do Enterprise Voice no Lync Server 2013](lync-server-2013-new-enterprise-voice-features.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

