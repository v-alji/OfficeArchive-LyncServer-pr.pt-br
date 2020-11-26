---
title: 'Lync Server 2013: desabilitar a retirada de chamadas em grupo para usuários'
description: 'Lync Server 2013: desabilitar a retirada de chamadas em grupo para usuários.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disable Group Call Pickup for users
ms:assetid: 91b06f9e-2840-45a2-bbb3-6a29179b9a9f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945638(v=OCS.15)
ms:contentKeyID: 51541492
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b3f5b4542cf7bb8ea5be524d2695701979ec2987
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429102"
---
# <a name="disable-group-call-pickup-for-users-in-lync-server-2013"></a>Desabilitar a retirada de chamadas em grupo para usuários no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-01-30_

Use o procedimento a seguir para desabilitar o recebimento de chamadas em grupo para um usuário.

<div>


> [!NOTE]  
> Quando você desativa o recurso de recebimento de chamadas em grupo para um usuário, o número do grupo de recebimento de chamadas atribuído ao usuário não é mantido. Se, em seguida, você quiser reabilitar o recebimento de chamadas em grupo para esse usuário, será necessário atribuir novamente o número do grupo de recebimento de chamada com o parâmetro/enablegrouppickup.



</div>

<div>

## <a name="to-disable-group-call-pickup-for-a-user"></a>Para desabilitar a retirada de chamadas em grupo para um usuário

1.  Realize logon no computador em que você instalou a ferramenta SEFAUtil com direitos de administrador.

2.  Na linha de comando, execute:
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /disablegrouppickup
    
    Por exemplo:
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /disablegrouppickup

</div>

<div>

## <a name="see-also"></a>Confira também


[Atribuir números de recebimento de chamadas em grupo aos usuários no Lync Server 2013](lync-server-2013-assign-group-call-pickup-numbers-to-users.md)  
[Habilitar a retirada de chamadas em grupo para usuários no Lync Server 2013](lync-server-2013-enable-group-call-pickup-for-users.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

