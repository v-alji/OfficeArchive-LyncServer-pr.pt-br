---
title: Opções de emparelhamento de pool compatível com o Lync Server 2013 e práticas recomendadas
description: Opções de emparelhamento de pool compatível com o Lync Server 2013 e práticas recomendadas.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported pool pairing options and best practices
ms:assetid: 142caf34-0f20-47f3-9d32-ce25ab622fad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204697(v=OCS.15)
ms:contentKeyID: 48183478
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 76d0f8331c0b6998008efff8af70ae3c4b43a9c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441414"
---
# <a name="supported-pool-pairing-options-and-best-practices-for-lync-server-2013"></a>Opções de emparelhamento de pool compatível e práticas recomendadas para o Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2017-03-09_

Não há restrição na distância entre dois data centers que incluem pools front-ends emparelhados uns com os outros. Recomendamos que você use dois data centers na mesma região do mundo, com links de alta velocidade entre eles. É melhor se os dois data centers estiverem separados o suficiente para evitar um único desastre ao pressionar ambos ao mesmo tempo.

Ter dois data centers nas regiões do mundo é possível, mas pode causar maior perda de dados devido à latência na replicação de dados.

Ao planejar quais pools emparelhar, você deve ter em mente que somente os emparelhamentos a seguir são aceitos:

  - Os pools Enterprise Edition podem ser emparelhados somente com outros pools Enterprise Edition. Da mesma forma, pools Standard Edition podem ser emparelhados somente com outros pools Standard Edition.

  - Os pools físicos somente podem ser emparelhados com outros pools físicos. Da mesma forma, os pools virtuais somente podem ser emparelhados com outros pools virtuais.

  - Os pools que estão emparelhados em conjunto devem estar executando o mesmo sistema operacional.

Nem o Construtor de Topologias nem a validação da topologia proibirão o emparelhamento de dois pools de uma forma que estas recomendações não sejam seguidas. Por exemplo, o Construtor de Topologias permite o emparelhamento de um pool Enterprise Edition com um pool Standard Edition. No entanto, estes tipos de emparelhamentos não são aceitos.

Cada pool em um par deve ter capacidade para atender todos os usuários de ambos os pools no caso de um desastre.

Se você emparelhar pools da edição Enterprise, também é possível implementar a alta disponibilidade nos servidores back end, mas para pares de pools de edição padrão, somente os indicadores de recuperação de desastres estão disponíveis.

</div>

<span> </span>

</div>

</div>

</div>

