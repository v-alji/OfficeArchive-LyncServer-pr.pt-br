---
title: 'Lync Server 2013: Visão Geral do Diretor'
description: 'Lync Server 2013: visão geral do diretor.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of the Director
ms:assetid: cf9919b3-e16b-47c5-be1d-2c4bc64f44ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398879(v=OCS.15)
ms:contentKeyID: 48185393
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6686534e22bab5b02a2663789298e4cf7ea582c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424706"
---
# <a name="overview-of-the-director-in-lync-server-2013"></a>Visão Geral do Diretor no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-08_

Um diretor é um servidor que executa o Lync Server 2013 que autentica solicitações do usuário, mas não hospeda nenhuma conta de usuário. Opcionalmente, você pode implantar um diretor nos dois cenários a seguir:

  - Se você habilitar o acesso por usuários externos implantando servidores de borda, também deverá implantar um diretor. Nesse cenário, o diretor autentica os usuários externos e, em seguida, passa o tráfego deles para servidores internos. Quando um diretor é usado para autenticar usuários externos, ele libera os servidores de pool de front-end da sobrecarga de execução de autenticação desses usuários. Também ajuda a proteger pools de front-end internos contra tráfego mal-intencionado, como ataques de negação de serviço. Se a rede estiver inundada com tráfego externo inválido nesse tipo de ataque, esse tráfego terminará no diretor.

  - Se você implantar vários pools de front-end em um site central, adicionando um diretor ao site, você pode simplificar solicitações de autenticação e melhorar o desempenho. Nesse cenário, todas as solicitações entram primeiro no director, que, em seguida, as roteia para o pool de front-end correto.

</div>

<span> </span>

</div>

</div>

</div>

