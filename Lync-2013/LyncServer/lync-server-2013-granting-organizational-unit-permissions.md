---
title: 'Lync Server 2013: Concedendo permissões de unidade organizacional'
description: 'Lync Server 2013: concedendo permissões de unidade organizacional.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting organizational unit permissions
ms:assetid: 95ee5ffa-39b1-4d80-87a2-27bb364f7396
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398763(v=OCS.15)
ms:contentKeyID: 48184849
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 47ad862241e409190620afa7dbf4fa73adf339de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427891"
---
# <a name="granting-organizational-unit-permissions-in-lync-server-2013"></a>Concedendo permissões de unidade organizacional no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-05-14_

Você pode usar o cmdlet **Grant-CsOuPermission** para conceder permissões a objetos em unidades organizacionais (UOs) especificadas para que os membros dos grupos universais do RTC criados pela preparação da floresta possam acessá-los sem serem membros do grupo Domain admins. As permissões adicionadas à UO especificada são as mesmas permissões que o cmdlet **Enable-CsAdDomain** adiciona aos recipientes computadores e usuários durante a preparação do domínio.

Use o cmdlet **Test-CsOuPermission** para verificar as permissões configuradas usando o cmdlet **Grant-CsOuPermission** .

Você pode usar o cmdlet **REVOKE-CsOuPermission** para remover permissões concedidas usando o cmdlet **Grant-CsOuPermission** .

<div>

## <a name="to-grant-ou-permissions"></a>Para conceder permissões de OU

1.  Faça logon em um computador que esteja executando o Lync Server 2013 no domínio em que você deseja conceder permissões de OU. Use uma conta que seja membro do grupo Domain admins ou do grupo Administradores de empresa se a UO estiver em um domínio filho diferente.

2.  Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.

3.  Execute:
    
        Grant-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    Se você não especificar o parâmetro Domain, o valor padrão será o domínio local.

</div>

<div>

## <a name="to-verify-ou-permissions"></a>Para verificar permissões de OU

1.  Faça logon em um computador que esteja executando o Lync Server 2013 no domínio em que você deseja verificar as permissões de OU que você concedeu usando o cmdlet **Grant-CsOuPermission** . Use uma conta que seja membro do grupo Domain admins ou do grupo Administradores de empresa se a UO estiver em um domínio filho diferente.

2.  Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.

3.  Execute:
    
        Test-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    Se você não especificar o parâmetro Domain, o valor padrão será o domínio local.

</div>

<div>

## <a name="to-revoke-ou-permissions"></a>Para revogar permissões de OU

1.  Faça logon em um computador que esteja executando o Lync Server 2013 no domínio em que você deseja revogar permissões de OU que foram concedidas pelo cmdlet **Grant-CsOuPermission** . Use uma conta que seja membro do grupo Domain admins ou do grupo Administradores de empresa se a UO estiver em um domínio filho diferente.

2.  Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.

3.  Execute:
    
        Revoke-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    Se você não especificar o parâmetro Domain, o valor padrão será o domínio local.

</div>

</div>

<span> </span>

</div>

</div>

</div>

