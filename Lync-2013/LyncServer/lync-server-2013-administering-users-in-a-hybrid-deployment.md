---
title: 'Lync Server 2013: administrando usuários em uma implantação híbrida'
description: 'Lync Server 2013: administrando usuários em uma implantação híbrida.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administering users in a hybrid deployment
ms:assetid: 6924ed7b-30a9-4be7-b952-90655625f2c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204967(v=OCS.15)
ms:contentKeyID: 48184381
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f1d7684a9f56eb013574a985ded0313378621c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389725"
---
# <a name="administering-users-in-a-hybrid-lync-server-2013-deployment"></a>Administrando usuários em uma implantação híbrida do Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2014-05-29_

Você pode gerenciar configurações de usuário e políticas para usuários migrados para o Lync Online usando os recursos de gerenciamento de usuários disponíveis no centro de administração do Microsoft 365. Faça login usando sua conta de administrador do locatário para executar tarefas administrativas.

<div>

## <a name="moving-users-back-to-on-premises"></a>Movendo usuários de volta para o local

<div class="">


> [!IMPORTANT]  
> Esta seção se aplica somente aos usuários que foram criados e habilitados para o Lync local e depois movidos de uma implantação local para o Lync Online. Se você quiser mover os usuários que foram criados no Lync Online (e ainda não habilitou o Lync em uma implantação local), consulte <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">movendo usuários do Lync Online para o Lync local no Lync Server 2013</A>.



</div>

  - Execute os seguintes cmdlets para mover um usuário do Lync Online de volta para o Lync local:
    
       ```PowerShell
        $cred=Get-Credential
       ```
    
       ```PowerShell
        Move-CsUser -Identity username@contoso.com -Target localpool.contoso.com -Credential $cred -HostedMigrationOverrideUrl <URL>
       ```

O formato da URL especificada para o parâmetro **HostedMigrationOverrideUrl** deve ser a URL para o pool no qual o Serviço de Migração Hospedada está sendo executado, no seguinte formato:

Https:// \<Pool FQDN\> /HostedMigration/hostedmigrationService.svc. Você pode determinar a URL do serviço de migração hospedada visualizando a URL do painel de controle do Lync Online para sua conta da organização do Microsoft 365 ou do Office 365.

**Para determinar a URL do serviço de migração hospedada para sua organização do Microsoft 365 ou do Office 365**

1.  Conecte-se à sua organização como administrador.

2.  Abra o **centro de administração do Lync**.

3.  Com o **centro de administração do Lync** exibido, selecione e copie a URL na barra de endereços até **Lync.com**. Uma URL de exemplo seria parecida com esta:
    
    `https://webdir0a.online.lync.com/lscp/?language=en-US&tenantID=`

4.  Substitua **webdir** na URL por **admin**, o que resulta no seguinte:
    
    `https://admin0a.online.lync.com`

5.  Anexe a cadeia de caracteres a seguir à URL: **/HostedMigration/hostedmigrationservice.svc**.
    
    A URL resultante, que tem o valor de **HostedMigrationOverrideUrl**, deverá ser parecida com esta:
    
    `https://admin0a.online.lync.com/HostedMigration/hostedmigrationservice.svc`

</div>

</div>

<span> </span>

</div>

</div>

</div>

