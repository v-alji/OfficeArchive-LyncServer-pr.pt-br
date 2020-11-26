---
title: 'Lync Server 2013: habilitar ou desabilitar um dispositivo de conferência'
description: 'Lync Server 2013: habilitar ou desabilitar um dispositivo de conferência.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable a conferencing device
ms:assetid: d5140e38-d015-4706-9bde-cf2fa748c36b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994070(v=OCS.15)
ms:contentKeyID: 51803981
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 761bc19536c889cced68ff586753f6800df0da59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437571"
---
# <a name="enable-or-disable-a-conferencing-device-in-lync-server-2013"></a>Habilitar ou desabilitar um dispositivo de conferência no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-02-20_

Habilite e desabilite um dispositivo de conferência usando o cmdlet **Enable-CsMeetingRoom** e o cmdlet **Disable-CsMeetingRoom** . Esses cmdlets podem ser executados no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.

<div>


> [!NOTE]  
> Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .



</div>

<div>


<div>

## <a name="enabling-a-conferencing-device"></a>Habilitando um dispositivo de conferência

  - Para habilitar um dispositivo de conferência, use o cmdlet **Enable-CsMeetingRoom** . Ao habilitar um dispositivo de conferência, você deve incluir uma) a identidade do dispositivo de conferência, b) o pool de registrador onde a conta da sala será hospedada e c) o endereço SIP a ser atribuído a essa conta.
    
        Enable-CsMeetingRoom -Identity "Redmond Conferencing device" -RegistrarPool "atl-cs-001.litwareinc.com" -SipAddress "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<div>

## <a name="disabling-a-conferencing-device"></a>Desativando um dispositivo de conferência

  - Para desabilitar um dispositivo de conferência, use o cmdlet **Disable-CsMeetingRoom** . Certifique-se de especificar a identidade do dispositivo de conferência a ser desativado:
    
        Disable-CsMeetingRoom -Identity "sip:RedmondMeetingRoom@litwareinc.com"

</div>

Para obter detalhes, consulte os tópicos da ajuda para o cmdlet [Enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) e o cmdlet [Disable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Disable-CsMeetingRoom) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

