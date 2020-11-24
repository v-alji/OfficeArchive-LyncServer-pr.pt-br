---
title: 'Lync Server 2013: visão geral do roteamento Location-Based'
description: 'Lync Server 2013: visão geral do roteamento do Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing
ms:assetid: 4aa494bd-0d66-4335-b9e8-f758d44a7202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994032(v=OCS.15)
ms:contentKeyID: 51803941
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b1e026791a8562629231b91b58d7e7eff569ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390282"
---
# <a name="overview-of-location-based-routing-in-lync-server-2013"></a>Visão geral do roteamento de Location-Based no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-02-21_

O roteamento baseado na localização introduz um novo conjunto de regras que modifica o roteamento de chamadas PSTN nacionais e internacionais para evitar desvio de tarifas. O roteamento baseado na localização oferece a flexibilidade para abranger essas regras em regiões específicas, gateways específicos ou somente conjunto de usuários específico.

Os cenários a seguir ilustram os principais tipos de restrições Location-Based o roteamento pode impor:

  - Chamadas de egresso – o roteamento Location-Based pode impor chamadas feitas para egresso a partir de um gateway PSTN localizado na mesma região onde o chamador é para impedir a interchamada PSTN PSTN, o que impede chamadas de saída de um gateway PSTN localizado em uma região diferente como o chamador.

  - Chamadas de ingresso – o roteamento Location-Based pode evitar chamadas PSTN de entrada para ligar pontos de extremidade do Lync se o gateway PSTN que faz a chamada de entrada não estiver localizado na mesma região que o usuário chamado do Lync.

  - Regiões desconhecidas – o roteamento de Location-Based restringe as chamadas PSTN de entrada e saída para e de usuários localizados em locais indeterminados (ou seja, usuários remotos que se conectam a partir da Internet ou localizados em regiões desconhecidas).

  - Regiões internacionais – o roteamento Location-Based reforça o roteamento de chamadas feitas por meio de gateways PSTN internacionais se um gateway local para o local do usuário não puder ser encontrado.

<div>

## <a name="see-also"></a>Confira também


[Planejamento de Roteamento Baseado em Local no Lync Server 2013](lync-server-2013-planning-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

