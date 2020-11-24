---
title: 'Lync Server 2013: Local do gateway PSTN'
description: 'Lync Server 2013: localização do gateway PSTN.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN gateway's location
ms:assetid: 49693a35-fad3-49ee-a71e-c7e4537b79aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994031(v=OCS.15)
ms:contentKeyID: 51803940
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f793249908bd1f064f9038ddd90c7f5b01a61d5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390087"
---
# <a name="pstn-gateways-location-in-lync-server-2013"></a>Local do gateway PSTN no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-03-09_

Chamadas roteadas por meio de gateways PSTN e PBXs podem exigir restrições de roteamento Location-Based dependendo do local de tais sistemas. Location-Based roteamento pode ser habilitado na granularidade com base em cada tronco.

Location-Based roteamento introduz o seguinte conjunto de regras quando habilitado em um tronco:

  - Quando o roteamento do Location-Based está habilitado em uma base por tronco, as regras definidas nesse tronco serão aplicadas somente a chamadas roteadas por meio desse tronco.

  - Para evitar que as tarifas PSTNs ignorem onde as chamadas são originadas de um site de rede diferente que o site de rede onde o gateway PSTN está localizado, Location-Based roteamento introduz a associação de um site de rede para um determinado tronco. Isso definirá o local de rede que permite o encaminhamento de chamadas para um tronco específico.

Os troncos podem ser habilitados para roteamento de Location-Based de duas maneiras:

  - O tronco é definido para um gateway PSTN que egressa chamadas para a PSTN. As chamadas de entrada encaminhadas por um tronco desse tipo serão encaminhadas apenas para os pontos de extremidade localizados dentro do mesmo local de rede do tronco.

  - O tronco é definido para um peer do servidor de mediação que não faz chamadas para os usuários de serviços PSTN e PSTN com telefones herdados em locais estáticos (por exemplo, telefones PBX). Para essa configuração específica, todas as chamadas de entrada encaminhadas por um tronco desse tipo serão consideradas como originadas do mesmo local de rede do tronco. As chamadas de usuários do PBX terão a mesma imposição de roteamento Location-Based como usuários do Lync que estão localizados no mesmo local de rede que o tronco. Se dois sistemas PBX localizados em sites de rede separados estiverem conectados pelo Lync Server, Location-Based roteamento permitirá o roteamento de um ponto de extremidade de PBX em um site de rede para outro ponto de extremidade de PBX no outro site de rede. Esse cenário não será bloqueado pelo roteamento Location-Based. Além desse cenário e de maneira semelhante a um usuário do Lync no mesmo local, os pontos de extremidade conectados a um servidor de mediação ponto a ponto com essa configuração poderão fazer ou receber chamadas para e a partir de outros Peers do servidor de mediação que não roteiam chamadas para a PSTN (ou seja, um ponto de extremidade conectado a um PBX diferente) independentemente do site de rede ao qual o peer do servidor de mediação está associado. Todas as chamadas recebidas, chamadas de saída, transferências de chamadas e encaminhamentos de chamadas que envolvem pontos de extremidade PSTN estarão sujeitas ao roteamento baseado em localização para usar somente gateways PSTN definidos como locais para o peer do servidor de mediação.

<div>

## <a name="see-also"></a>Confira também


[Orientação para Roteamento Baseado em Local no Lync Server 2013](lync-server-2013-guidance-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

