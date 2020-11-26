---
title: 'Lync Server 2013: Decidindo como implantar o Microsoft Lync'
description: 'Lync Server 2013: decidindo como implantar o Microsoft Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deciding how to deploy Microsoft Lync
ms:assetid: 6ca677d3-745d-4935-8f05-19274a8bccf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204979(v=OCS.15)
ms:contentKeyID: 48184423
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a800b51dfddc6f2c99e42c8f117056ed4091b6a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431229"
---
# <a name="deciding-how-to-deploy-lync-server-2013"></a>Decidindo como implantar o Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-10-03_

Ao planejar o Lync, a primeira decisão importante é como implantar o Microsoft Lync: como o Lync Server 2013 local ou o Lync Online com o Microsoft 365 ou o Office 365 na nuvem.

  - **Lync Server 2013 local** : esta opção fornece o conjunto de recursos completo do Lync e fornece a flexibilidade máxima para configurar, personalizar e operar a implantação. Todos os servidores são instalados no local e mantidos pela sua organização. Uma implantação local fornece a gama completa de recursos do Lync Server.

  - **Lync Online na nuvem** O Lync Online foi projetado para organizações que desejam os benefícios de custo e agilidade das mensagens instantâneas, presença e reuniões em nuvem sem sacrificar os recursos de classe empresarial do Lync Server. Com o Lync Online, a Microsoft implanta e mantém a infraestrutura de servidor necessária e manipula manutenção, patches e atualizações contínuas. Alguns recursos disponíveis em uma implantação local não estão disponíveis no Lync Online.

Qual tipo de implantação seria melhor para você depende das cargas de trabalho que você deseja implantar e o status geográfico e comercial da sua organização.

<div>

## <a name="lync-server"></a>Servidor Lync

Uma implantação do Lync Server local é melhor para os seguintes cenários:

  - **Recursos completos do Enterprise Voice**   Se você planeja implantar uma solução completa Enterprise Voice para substituir seu PBX ou que usa recursos de chamada avançada, uma implantação do Lync Server local será necessária. O local é compatível com a conectividade direta com sistemas PBX e troncos e recursos de telefone avançados, como grupos de resposta e estacionamento de chamadas. No momento, o Lync Online não oferece suporte a esses recursos.

  - **Controles de qualidade de mídia**   Se você quiser uma gama completa de recursos de garantia de qualidade de mídia, como o controle de admissão de chamadas (CAC) e os recursos de qualidade do serviço (QoS), será necessário uma implantação local.

  - **Chat persistente**   Se precisar implantar o chat persistente para a sua organização, você deverá escolher uma implantação local.

  - **aplicativos de servidor de terceiros**   Somente implantações locais podem funcionar com aplicativos de terceiros confiáveis que usam a API gerenciada de comunicação unificada da Microsoft (UCMA).

  - **Empresas multinacionais/de várias regiões que precisam de suporte regional**   Se você tiver datacenters em vários países ou regiões e precisar que os servidores sejam implantados e gerenciados de forma regional, uma implantação local será melhor, pois oferece esse tipo de recursos de gerenciamento regional.

  - **Controle completo sobre políticas, relatórios e atualizações**   Com uma implantação local do Lync Server, você tem acesso ao conjunto completo de políticas de servidor e de cliente, monitoramento e outros relatórios e tempo de atualização. O Lync Online fornece um subconjunto de relatórios e configurações de política e fornece uma janela limitada, embora significativa, para aceitar atualizações.

</div>

<div>

## <a name="lync-online"></a>Lync Online

Se nenhum dos fatores na lista anterior for essencial para você, talvez você queira escolher o Lync Online, para implantação e gerenciamento mais simples. O Lync Online oferece um conjunto robusto de recursos de chat, presença e conferência e também permite chamadas de voz e vídeo por IP entre os usuários da sua organização.

</div>

</div>

<span> </span>

</div>

</div>

</div>
