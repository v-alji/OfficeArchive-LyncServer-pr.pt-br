---
title: Migrar telefones de área comum
description: Migrar telefones comuns de área.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Common Area Phones
ms:assetid: 31bd26fc-861b-45c6-8221-18df16e575de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688015(v=OCS.15)
ms:contentKeyID: 49733604
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b8df4d94a3db3274df7e4e82ed2185c3626de12
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443822"
---
# <a name="migrate-common-area-phones"></a>Migrar telefones de área comum

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-29_

Os telefones de área comuns são telefones IP que costumam residir em um espaço de trabalho compartilhado ou em uma área comum, como um lobby, uma cozinha ou um chão de fábrica. Os telefones de área comuns não precisam estar conectados a um computador para fornecer a funcionalidade de comunicação unificada do Lync Server. Depois de migrar uma implantação do Lync Server 2010 para o Lync Server 2013, você também deve migrar os objetos de contato associados ao telefone de área comum comum. Usando o Shell de gerenciamento do Lync Server, primeiro você recuperará todos os objetos de contato associados aos telefones da área comum do Lync Server 2010 e moverá esses objetos para o pool do Lync Server 2013.

**Migrar telefones de área comum**

1.  No servidor front-end do Lync Server 2013, abra o Shell de gerenciamento do Lync Server.

2.  Na linha de comando, digite o seguinte:
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsCommonAreaPhone -Target pool02.contoso.net

3.  Para verificar se todos os objetos de contato foram movidos para o pool do Lync Server 2013, no Shell de gerenciamento do Lync Server, digite o seguinte:
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool02.contoso.net"}
    
    Verifique se todos os objetos de contato estão agora associados ao pool do Lync Server 2013.

</div>

<span> </span>

</div>

</div>

</div>

