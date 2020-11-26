---
title: 'Lync Server 2013: Adicionando um link personalizado às mensagens de erro do Lync'
description: 'Lync Server 2013: adicionar um link personalizado para mensagens de erro do Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding a custom link to Lync error messages
ms:assetid: de756088-fcc3-4e47-bde8-4fa4cc852fd1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398979(v=OCS.15)
ms:contentKeyID: 48185607
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a5d333b6f27e10e5092de23fcdf1d37fd75e75a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439279"
---
# <a name="adding-a-custom-link-to-lync-error-messages-in-lync-server-2013"></a>Adicionando um link personalizado às mensagens de erro do Lync no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-02-20_

Personalize mensagens de erro do Lync 2013 adicionando um link para suas próprias informações de solução de problemas ou suporte técnico. Para fazer isso, use os cmdlets shell do Shell de gerenciamento do Lync Server **New-CSClientPolicy** ou **set-CSClientPolicy** com o parâmetro CustomLinkInErrorMessages. O texto do link personalizado é "clique aqui para obter tópicos de suporte do administrador" e não pode ser personalizado.

Por exemplo, o comando a seguir faz com que o link personalizado apareça na área de notas de rodapé de cada mensagem de erro do Lync 2013 e define o destino do link como http://contoso.com/help/LyncHelpDesk.aspx:

    New-CsClientPolicy -Identity LyncErrorLink -CustomLinkInErrorMessages "http://contoso/help/LyncHelpDesk.aspx"

Use **Grant-CSClientPolicy** para atribuir esta nova política aos usuários. Para obter detalhes, consulte **New-CSClientPolicy** and **Grant-CSClientPolicy** na documentação do Shell de gerenciamento do Lync Server.

</div>

<span> </span>

</div>

</div>

</div>

