---
title: 'Lync Server 2013: Habilitar ou desabilitar uma sala de chat'
description: 'Lync Server 2013: desativando ou ativando uma sala de chat.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disabling or enabling a chat room
ms:assetid: db0908fc-aae3-46e8-bc0b-245e9adfa1e2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215883(v=OCS.15)
ms:contentKeyID: 48706011
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b81ce2614cebcf554c0390369068d8fd8b8f932
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437844"
---
# <a name="disabling-or-enabling-a-chat-room-in-lync-server-2013"></a>Habilitar ou desabilitar uma sala de chat no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2014-02-05_

Se o tópico de uma sala de chat persistente não for mais relevante, você poderá deixar a sala de chat indisponível para os usuários desabilitá-la. Quando uma sala de chat está desabilitada, todos os membros são desconectados imediatamente da sala. Após uma sala de chat ser desabilitada, os usuários não podem participar novamente ou encontrá-la nas pesquisas de sala de chat.

Uma sala de chat desativada pode ser habilitada posteriormente por um administrador de chat persistente. Se uma sala de chat for desabilitada, sua lista de associação e outras configurações serão preservadas. Se você habilitar a sala novamente, não será necessário recriá-las manualmente.

Se o histórico da sala de chat persistir (a persistência do histórico de salas de chat é uma configuração opcional em uma categoria que se aplica a todas as salas dentro da categoria; o padrão é mantido, mas pode ser desativado Configurando o **histórico de habilitar o chat** como falso), o conteúdo é preservado quando a sala de chat está desabilitada. Entretanto, o conteúdo não será exibido nas pesquisas durante o tempo em que a sala de chat permanecer no estado desabilitado. Se você habilitá-la mais tarde, os usuários poderão pesquisar mensagens que foram publicadas antes da sala de chat ser desabilitada.

Para obter detalhes sobre como desabilitar e habilitar as salas de chat usando a interface de linha de comando do Windows PowerShell, consulte o "gerenciamento de sala" em [Configurando o servidor de chat persistente usando cmdlets do Windows PowerShell](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md). Para desabilitar uma sala de chat, use um comando semelhante a este:

    Set-CsPersistentChatRoom -Identity "atl-cs-001.litwareinc.com\ITChatRoom" -Disabled $True

Para habilitar uma sala de chat, defina a propriedade disabled como false:

    Set-CsPersistentChatRoom -Identity "atl-cs-001.litwareinc.com\ITChatRoom" -Disabled $False

Observe que as salas de chat não podem ser ativadas ou desativadas usando o painel de controle do Lync Server.

Para obter detalhes sobre como configurar salas de chat, consulte [Configurar salas no Lync Server 2013](lync-server-2013-configure-rooms.md) na documentação de implantação.

</div>

<span> </span>

</div>

</div>

</div>

