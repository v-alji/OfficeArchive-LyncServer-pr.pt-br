---
title: Evitar sessões de serviços
description: Evitar sessões para serviços.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Prevent sessions for services
ms:assetid: 4b541c72-cdc1-4f86-a5a8-c43c24f41d8b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688049(v=OCS.15)
ms:contentKeyID: 49733642
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a452f8091716daa0a15967e2a278e82c5bc8c4f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438460"
---
# <a name="prevent-sessions-for-services"></a>Evitar sessões de serviços

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-10-04_

Você pode usar o painel de controle do Microsoft Lync Server 2010 para impedir novas sessões para todos os serviços do Lync Server 2010 em execução em um computador específico ou para impedir novas sessões para um serviço específico do Lync Server 2010.

<div>

## <a name="to-prevent-new-sessions-for-all-lync-server-services-on-a-computer"></a>Para impedir novas sessões para todos os serviços do Lync Server em um computador

1.  Em uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes) ou atribuído à função CsServerAdministrator ou CsAdministrator, faça logon em qualquer computador que esteja na rede na qual você implantou o Lync Server 2013.

2.  Abra o Painel de Controle do Lync Server.

3.  Na barra de navegação à esquerda, clique em **topologia** e, em seguida, clique em **status**.

4.  Na página **status** , classifique ou pesquise a lista, conforme necessário, para localizar o computador que está executando os serviços para os quais você deseja impedir novas sessões e, em seguida, clique nela.

5.  Clique em **ação**.

6.  Clique em **impedir novas sessões para todos os serviços**.

</div>

<div>

## <a name="to-prevent-new-sessions-for-a-specific-service"></a>Para impedir novas sessões para um serviço específico

1.  Em uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes) ou atribuído à função CsServerAdministrator ou CsAdministrator, faça logon em qualquer computador que esteja na rede na qual você implantou o Lync Server 2013.

2.  Abra o Painel de Controle do Lync Server.

3.  Na barra de navegação à esquerda, clique em **topologia** e, em seguida, clique em **status**.

4.  Na página **status** , classifique ou pesquise a lista, conforme necessário, para localizar o computador que está executando o serviço que você deseja iniciar ou parar e, em seguida, clique nele.

5.  Clique em **Propriedades**.

6.  Classifique a lista de serviços, se necessário, e clique no serviço para o qual você deseja impedir novas sessões.

7.  Clique em **ação**.

8.  Clique em **impedir novas sessões para o serviço**.

9.  Clique em **Fechar**.

</div>

</div>

<span> </span>

</div>

</div>

</div>

