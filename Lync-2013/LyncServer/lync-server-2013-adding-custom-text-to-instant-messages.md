---
title: 'Lync Server 2013: Adicionando texto personalizado a mensagens instantâneas'
description: 'Lync Server 2013: adicionar texto personalizado a mensagens instantâneas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding custom text to instant messages
ms:assetid: cabcc3ec-9d35-42ac-a403-e21b7d538c2c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398847(v=OCS.15)
ms:contentKeyID: 48185458
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54f5cf031da0ba4d5bd0b6dbaa7f5ebc9d0b3a6c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439230"
---
# <a name="adding-custom-text-to-instant-messages-in-lync-server-2013"></a>Adicionando texto personalizado a mensagens instantâneas no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-02-20_

Adicione uma declaração de isenção ou aviso ao início de cada conversa de mensagem instantânea do Lync 2013 usando os cmdlets shell do Shell de gerenciamento do Lync Server **New-CSClientPolicy** ou **set-CSClientPolicy** com o parâmetro imwarning.

O comando no exemplo a seguir adiciona um lembrete de segurança na parte superior da janela de conversa sempre que uma nova conversa de mensagem instantânea começa:

    New-CsClientPolicy -Identity IMSecurityNotice -IMWarning 
    "Remember, security is everyone's responsibility. Keep it confidential."

Use **Grant-CSClientPolicy** para atribuir esta nova política aos usuários. Para obter detalhes, consulte **New-CSClientPolicy** and **Grant-CSClientPolicy** na documentação do Shell de gerenciamento do Lync Server.

</div>

<span> </span>

</div>

</div>

</div>

