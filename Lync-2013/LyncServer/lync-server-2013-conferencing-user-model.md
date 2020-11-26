---
title: Modelo de usuário da conferência do Lync Server 2013
description: Modelo de usuário de conferência do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: The conferencing user model
ms:assetid: ba4bbba9-f2e3-4cab-8eba-b51f12133cab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205199(v=OCS.15)
ms:contentKeyID: 48185229
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 699f41303b82f4d8fd2864cbf1b29a1c601b826e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434274"
---
# <a name="the-conferencing-user-model-in-lync-server-2013"></a>O modelo de usuário de conferência no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-10-22_

Uma parte crítica do modelo de usuário do Lync Server Conferencing é o tamanho da reunião. Após coletar dados de vários pontos de dados (conforme descrito na seção anterior), determinamos o seguinte:

  - A maioria das reuniões é realmente pequena reunião colaborativa com uma média de quatro a seis participantes

  - Aproximadamente 20 a 80% das reuniões têm menos de 20 participantes.

  - 99,98% das reuniões têm menos de 100 participantes.

Além do tamanho da reunião, o modelo de usuário da conferência também leva em conta uma variedade de fatores, como:

  - **Reuniões simultâneas**   Quantos usuários devem estar em reuniões ao mesmo tempo?

  - **Mix de mídia**   Que tipos de mídia estão disponíveis e que devem ser usados por usuários em reuniões?

  - **Tipos de usuário**   Os usuários são usuários internos, usuários remotos, usuários federados ou usuários anônimos?

  - **Tempo de crescimento da reunião**   Quanto tempo leva para que todos os usuários de uma reunião ingressem em uma reunião?

Para obter detalhes sobre o modelo de usuário, consulte [modelos de usuário no Lync Server 2013](lync-server-2013-user-models.md).

Para determinar o número de reuniões e usuários a serem usados para testes, fizemos o seguinte:

  - Gastou o número total de usuários em uma organização (por exemplo, 80.000 usuários) e o multiplicado pela taxa de simultaneidade da reunião (por exemplo, 5% de todos os usuários) para determinar o número total de usuários que devem estar em reuniões ao mesmo tempo (neste exemplo, 4000 usuários).

  - Dividiu o número total de usuários pelo número de servidores do Lync Server 2013, front-end na implantação (por exemplo, 8 servidores) para determinar o número estimado de participantes da reunião por servidor front-end (neste exemplo, 500 usuários por servidor front-end).

  - Divida o número de usuários por servidor front-end pelo tamanho médio da reunião (por exemplo, 4 usuários) para determinar o número médio estimado de reuniões por servidor front-end (neste exemplo, reuniões do 125 por servidor front-end).

  - Para obter a carga por mídia em cada servidor front-end, estimamos o mix de mídia. Por exemplo, pressupondo que 75% das reuniões exijam mais do que apenas o suporte a áudio e 50% dessas reuniões exigem compartilhamento de aplicativos, uma média de reuniões do 47 e os usuários da 188 se conectam simultaneamente a cada servidor front-end para compartilhamento de aplicativos.

  - Testou uma variedade de tamanhos de reunião (com base em nosso modelo de usuário de até 250 usuários em um pool compartilhado) para garantir a escalabilidade do servidor.

</div>

<span> </span>

</div>

</div>

</div>

