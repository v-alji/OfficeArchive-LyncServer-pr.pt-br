---
title: 'Lync Server 2013: Práticas recomendadas para controle de admissão de chamada'
description: 'Lync Server 2013: práticas recomendadas para controle de admissão de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for call admission control
ms:assetid: 97173cca-8175-4ae2-a247-eb7ef809da93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398770(v=OCS.15)
ms:contentKeyID: 48184913
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17c32af904dc7fb48a1a5d1903bd6ed1f81f4cb3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436066"
---
# <a name="best-practices-for-call-admission-control-in-lync-server-2013"></a>Práticas recomendadas para controle de admissão de chamada no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-22_

Para melhorar o desempenho e facilitar a implantação, aplique as seguintes práticas recomendadas ao implantar o controle de admissão de chamadas:

  - Garanta que as WANs sejam provisionadas de forma adequada para tráfego de mídia atual e previsto.
    
    <div>
    

    > [!NOTE]  
    > Recomendamos que você Fatore em um buffer para seus limites de largura de banda. Há cenários como condições de corrida que afetam a largura de banda total usada e podem resultar em situações em que o limite de largura de banda é excedido. Por exemplo, se duas chamadas tentam iniciar enquanto o tráfego de mídia está se aproximando de um limite de largura de banda, um deles pode ser negado porque o outro gerenciado para iniciar primeiro.

    
    </div>

  - Monitorar o uso da rede e os registros de detalhes da chamada para que você possa escolher as configurações de CAC otimizadas e atualizar as configurações de CAC como alterações de uso de rede.

  - Use as políticas de largura de banda do CAC para complementar as configurações de QoS.

  - Se você quiser redirecionar chamadas bloqueadas para a PSTN, verifique a funcionalidade e a funcionalidade da PSTN. Para obter detalhes, consulte [planejando o roteamento de voz de saída no Lync Server 2013](lync-server-2013-planning-outbound-voice-routing.md).
    
    <div>
    

    > [!NOTE]  
    > A capacidade se refere ao número de portas que você precisa abrir para dar suporte a redirecionamento PSTN potencial.

    
    </div>

</div>

<span> </span>

</div>

</div>

</div>

