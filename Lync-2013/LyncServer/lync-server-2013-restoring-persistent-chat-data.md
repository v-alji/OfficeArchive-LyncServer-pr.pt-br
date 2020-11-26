---
title: 'Lync Server 2013: restaurando dados persistentes de chat'
description: 'Lync Server 2013: restaurando dados de chat persistentes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring Persistent Chat data
ms:assetid: c251a7fa-50da-434b-b39a-17f5978ce736
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945649(v=OCS.15)
ms:contentKeyID: 51541516
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7c75683e151daaadab8374ed5b41886da9a3aea3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442506"
---
# <a name="restoring-persistent-chat-data-in-lync-server-2013"></a>Restaurando dados de chat persistente no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-02-18_

Conteúdo da sala de chat persistente é armazenado no banco de dados de chat persistente (MGC. MDF). Esses dados são essenciais para os negócios, cujo backup deve ser feito regularmente. Além do conteúdo da sala de chat, as entidades de segurança (como usuários e grupos) e as funções e o acesso que elas precisam fazer para conversar com salas de chat e conteúdo da sala de chat, também são armazenados no banco de dados de chat persistente.

A maneira como você restaura seus dados de chat persistentes depende do método usado para fazer o backup.

  - Se você usou procedimentos de backup do SQL Server, então deve usar procedimentos de restauração do SQL Server.

  - Se você usou o cmdlet **Export-CsPersistentChatData** para fazer backup de dados de chat persistente, deve usar o cmdlet **Import-CsPersistentChatData** para restaurar os dados.

</div>

<span> </span>

</div>

</div>

</div>

