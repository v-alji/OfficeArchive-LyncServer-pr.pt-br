---
title: Migrar dispositivos analógicos
description: Migrar dispositivos analógicos.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate analog devices
ms:assetid: ad072916-87ed-4d44-8289-aab87da86250
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721846(v=OCS.15)
ms:contentKeyID: 49733779
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63f7f92142fb6a3ced37cded1a223038ec1876d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443829"
---
# <a name="migrate-analog-devices"></a>Migrar dispositivos analógicos

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-10-16_

O Lync Server oferece suporte a dispositivos analógicos. Especificamente, os dispositivos analógicos suportados são telefones de áudio analógicos e máquinas de fax analógicas. Você pode configurar os gateways qualificados para dar suporte ao uso de dispositivos analógicos em seu ambiente do Lync Server. Depois de migrar do Lync Server 2010 para o Lync Server 2013, você também deve migrar os objetos de contato associados aos dispositivos analógicos. Use o Shell de gerenciamento do Lync Server para recuperar primeiro todos os objetos de contato associados aos dispositivos analógicos do Lync Server 2010 e mova esses objetos para o pool do Lync Server 2013.

<div>

## <a name="to-migrate-analog-devices"></a>Para migrar dispositivos analógicos

1.  Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.

2.  Na linha de comando, digite:
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsAnalogDevice -Target pool02.contoso.net

3.  Verifique se todos os objetos de contato foram movidos para o pool do Lync Server 2013. Na linha de comando, digite:
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool02.contoso.net"}

4.  Verifique se todos os objetos de contato agora estão associados ao pool do Lync Server 2013.

</div>

</div>

<span> </span>

</div>

</div>

</div>

