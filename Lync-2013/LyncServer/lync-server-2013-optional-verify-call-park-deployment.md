---
title: 'Lync Server 2013: (opcional) verificar a implantação do estacionamento de chamadas'
description: 'Lync Server 2013: (opcional) Verifique a implantação do estacionamento de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Verify Call Park deployment
ms:assetid: fcfe0962-1a9c-4cbd-847c-fed40e3b1480
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413076(v=OCS.15)
ms:contentKeyID: 48185952
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 772392a3a791ed57c3220d80e9bd510d8803debb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424860"
---
# <a name="optional-verify-call-park-deployment-in-lync-server-2013"></a>Adicionais Verificar a implantação do estacionamento de chamadas no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-11_

Depois de instalar e configurar o parque de chamadas, você precisa verificar a configuração para garantir que o estacionamento e a recuperação de chamadas funcionarão como esperado. No mínimo, verifique o seguinte:

  - Ligue para um usuário que tenha o estacionamento de chamadas habilitado e tenha o usuário que estaciona a chamada.
    
    <div>
    

    > [!NOTE]  
    > Se você ativou o estacionamento de chamadas na política de voz antes de realizar esse teste, o usuário que está estacionando a chamada precisa sair do Lync Server e, em seguida, entrar novamente para poder ver a opção parque de chamadas na lista de chamadas de transferência.

    
    </div>

  - Disque o número de órbita para recuperar a chamada.

  - Estacione outra chamada, permita que o tempo da chamada estacionada esgote e não pegue o retorno de chamada. Verifique se a chamada que atingiu o tempo limite será corretamente roteada para o destino de fallback especificado para **OnTimeoutURI**.

</div>

<span> </span>

</div>

</div>

</div>

