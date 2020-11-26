---
title: Migrar a federação XMPP
description: Migrando a Federação do XMPP.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating XMPP federation
ms:assetid: b8d2b4b9-d0ed-4b48-820a-2c257fbdd2fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721861(v=OCS.15)
ms:contentKeyID: 49733794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e63c9f6fd3f1c1d45de77c27417987505678f74b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440357"
---
# <a name="migrating-xmpp-federation"></a>Migrar a federação XMPP

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-10-19_

As versões anteriores do Lync Server e do Office Communications Server forneciam um gateway de protocolo de presença e mensagens (XMPP) extensível que poderia ser implantado como uma função de servidor separada para permitir a Federação com implantações do XMPP. No Lync Server 2013, a funcionalidade XMPP pode ser implantada como um recurso. A funcionalidade XMPP é instalada em duas partes: como um proxy do XMPP que é executado no servidor de borda do Lync Server 2013 e o Gateway XMPP executado no servidor front-end do Lync Server 2013.

De uma perspectiva de migração, uma conta de usuário do Lync Server pode ser movida para um pool do Lync Server 2013 e continuar a usar o gateway herdado XMPP. Isso só é possível quando o parceiro federado XMPP não está configurado no Lync Server 2013.

Em resumo, se o Lync Server 2010 tiver sido implantado com o gateway do Office Communications Server 2007 R2 XMPP e a Federação do XMPP tiver sido habilitada para usuários herdados do Lync Server 2010, para migrar a Federação do XMPP para o Lync Server 2013:

1.  Implantar um pool do Lync Server 2013.

2.  Implantar um servidor de borda do Lync Server 2013.

3.  Mover todos os usuários para o pool do Lync Server 2013

4.  Criar políticas e certificados de acesso XMPP para o servidor de borda.

5.  Habilite a Federação do XMPP no Lync Server 2013. 

6.  Atualize as entradas de DNS para apontar para o gateway do Lync Server 2013 XMPP.

</div>

<span> </span>

</div>

</div>

</div>

