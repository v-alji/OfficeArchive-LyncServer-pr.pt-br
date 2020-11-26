---
title: 'Lync Server 2013: Delegação'
description: 'Lync Server 2013: Delegação.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegation
ms:assetid: 89e76e5c-3cfb-4504-8d0d-7509c8ba9815
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994045(v=OCS.15)
ms:contentKeyID: 51803956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6dc25d0ea3dfd64ee1b71677e6bac55c1cb1ca32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430739"
---
# <a name="delegation-in-lync-server-2013"></a>Delegação no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-03-09_

Os recursos de delegação do Lync são afetados pelo roteamento Location-Based da seguinte maneira:

  - Quando um representante habilitado para Location-Based roteamento coloca uma chamada em nome de um gerente, a política de voz do representante é usada para autorizar a chamada e a política de roteamento de voz do site do representante será usada para direcionar a chamada

  - Para as chamadas de entrada PSTN para um gerente, as mesmas regras aplicáveis ao encaminhamento de chamadas ou ao toque simultâneo serão aplicadas conforme descrito nos tópicos Transferências e encaminhamento de chamadas e Toque Simultâneo.

  - Quando um delegado configura um ponto de extremidade do PSTN como um destino de toque simultâneo, para uma chamada de entrada para o gerente, a política de roteamento de voz do local associado ao tronco de entrada será utilizada para rotear a chamada para o ponto de extremidade do PSTN do delegado.

  - Para delegação, recomenda-se que o gerente e seus delegados associados estejam, em geral, localizados no mesmo local de rede.

<div>

## <a name="see-also"></a>Confira também


[Cenários para Roteamento Baseado em Local no Lync Server 2013](lync-server-2013-scenarios-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

