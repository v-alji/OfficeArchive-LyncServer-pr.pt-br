---
title: 'Lync Server 2013: Preparando Serviços de Domínio Active Directory bloqueado'
description: 'Lync Server 2013: preparando os serviços de domínio do Active Directory bloqueados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing a locked-down Active Directory Domain Services
ms:assetid: 68bde963-3fa3-4102-88d6-ac931c1dd2d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398492(v=OCS.15)
ms:contentKeyID: 48184377
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4aea04b138de2630935713eda7cbef9e4d21572a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424223"
---
# <a name="preparing-a-locked-down-active-directory-domain-services-in-lync-server-2013"></a>Preparando Serviços de Domínio Active Directory bloqueado no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-05-14_

Geralmente, as organizações bloqueiam os serviços de domínio do Active Directory para ajudar a reduzir os riscos de segurança. No entanto, um ambiente do Active Directory bloqueado pode limitar as permissões exigidas pelo Lync Server 2013. A preparação adequada de um ambiente do Active Directory bloqueado para o Lync Server 2013 envolve algumas considerações e etapas adicionais.

Duas maneiras comuns nas quais as permissões são limitadas em um ambiente bloqueado do Active Directory são as seguintes:

  - As entradas de controle de acesso do usuário autenticado (ACEs) são removidas dos contêineres.

  - A herança de permissões está desabilitada em contêineres de objetos de usuário, contato, InetOrgPerson ou computador.

<div>

## <a name="in-this-section"></a>Nesta seção

  - [Permissões de usuário autenticado são removidas no Lync Server 2013](lync-server-2013-authenticated-user-permissions-are-removed.md)

  - [Herança de permissões está desabilitado em computadores, usuários ou contêiners InetOrgPerson no Lync Server 2013](lync-server-2013-permissions-inheritance-is-disabled-on-computers-users-or-inetorgperson-containers.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

