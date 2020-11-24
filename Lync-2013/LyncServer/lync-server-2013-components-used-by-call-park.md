---
title: 'Lync Server 2013: Componentes usados pelo Estacionamento de Chamadas'
description: 'Lync Server 2013: componentes usados pelo parque de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Call Park
ms:assetid: c7ffbee3-0ce1-48c0-bb56-af098b41d6d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398824(v=OCS.15)
ms:contentKeyID: 48185374
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 285af316fa2d49e8bebf68e11de6d9526e12ae29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389898"
---
# <a name="components-used-by-call-park-in-lync-server-2013"></a>Componentes usados pelo Estacionamento de Chamadas no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-13_

O aplicativo de estacionamento de chamadas é instalado automaticamente quando você implanta o Enterprise Voice. Para habilitar o estacionamento de chamadas, configure a política de voz. Os seguintes componentes do Lync Server 2013 suportam o aplicativo de estacionamento de chamadas:

  - **Serviço de aplicativo**   O serviço de aplicativo fornece uma plataforma para implantação, hospedagem e gerenciamento de aplicativos de comunicação unificada, como o aplicativo de estacionamento de chamada. O serviço de aplicativo é instalado automaticamente em todos os servidores front-end em um pool Front-end e em cada servidor Standard Edition.

  - **Aplicativo de estacionamento de chamadas**   O aplicativo de estacionamento de chamadas é um dos aplicativos de comunicação unificada hospedados pelo serviço de aplicativo. Ela é incluída automaticamente durante a implantação do Enterprise Voice. Ligue para parques e recupere chamadas e gerencie órbitas de estacionamento de chamadas.

  - **Música-em espera-arquivo**   Se a música estiver habilitada, o arquivo de música será reproduzido enquanto uma chamada estiver estacionada. Um arquivo de música padrão é incluído quando o aplicativo de estacionamento de chamada é instalado.

  - **Repositório de arquivos**   O aplicativo parque de chamadas usa o repositório de arquivos para armazenar arquivos de áudio personalizados.

  - **Painel de controle do Lync Server**   Você pode usar o painel de controle do Lync Server para configurar a tabela órbita do estacionamento de chamada e para habilitar o estacionamento de chamadas para os usuários.

  - **Shell de gerenciamento do Lync Server**   Todas as configurações do aplicativo de estacionamento de chamadas podem ser realizadas usando cmdlets do shell do Shell de gerenciamento do Lync Server.

</div>

<span> </span>

</div>

</div>

</div>

