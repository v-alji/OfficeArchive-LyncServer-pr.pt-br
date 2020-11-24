---
title: 'Lync Server 2013: Configuração do Roteamento Baseado em Local para conferência'
description: 'Lync Server 2013: configuração do roteamento Location-Based para conferência.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration of Location-Based Routing for conferencing
ms:assetid: d8c708cc-a1b1-48b1-808c-a64df15f7701
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362846(v=OCS.15)
ms:contentKeyID: 56335088
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a87f9c799e565f64b0dd30ce025a4e7a3174625
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390372"
---
# <a name="configuration-of-location-based-routing-for-conferencing-in-lync-server-2013"></a>Configuração do Roteamento Baseado em Local para conferência no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-09-11_

O aplicativo de conferência de roteamento Location-Based depende da configuração do Lync Server 2013 Location-Based Routing. Estas são as principais configurações:

  - O local dos participantes que ingressam em uma reunião é determinado com base em seus locais de rede. Um site de rede e suas sub-redes de rede associadas devem ser definidos no Lync Server para impor Location-Based roteamento.

  - Para aplicar Location-Based roteamento de reuniões, os participantes do Lync devem ser habilitados para Location-Based roteamento.

  - Para aplicar Location-Based roteamento de pontos de extremidade PSTN ingressando em reuniões, o tronco SIP usado para conectar os pontos de extremidade PSTN devem ser configurados para Location-Based roteamento.

Para obter informações adicionais sobre como implantar e configurar o roteamento Location-Based do Lync Server 2013, consulte Configurando o [roteamento baseado em local](lync-server-2013-configuring-location-based-routing.md).

<div>

## <a name="enabling-the-location-based-routing-conferencing-application"></a>Habilitando o aplicativo de conferência de roteamento de Location-Based

O aplicativo de conferência de roteamento Location-Based está desabilitado por padrão. Antes de habilitá-lo, determine a prioridade certa para atribuir a ele. Para determinar essa prioridade, execute o seguinte cmdlet no Shell de gerenciamento do Lync Server:

```powershell
Get-CsServerApplication -Identity Service:Registrar:<Pool FQDN>
```

Nesse cmdlet, \<Pool FQDN\> é o pool no qual o aplicativo de conferência de roteamento Location-Based está habilitado.

Esse cmdlet retornará a lista dos aplicativos hospedados pelo Lync Server e o valor de prioridade para cada um deles. O aplicativo de conferência de roteamento Location-Based precisa ser atribuído um valor de prioridade maior do que o aplicativo "UdcAgent" e menor do que os aplicativos "defaultrouting", "ExumRouting" e "OutboundRouting". Recomendamos que você atribua o aplicativo de videoconferência Location-Based um valor de prioridade que seja um ponto maior do que o valor de prioridade do aplicativo "UdcAgent".

Por exemplo, se o aplicativo "UdcAgent" tem um valor de prioridade "2", o aplicativo "defaultrouting" tem um valor de prioridade de "8", o aplicativo "ExumRouting" tem um valor de prioridade de "9" e o aplicativo "OutboundRouting" tem um valor de prioridade de "10", então você deve atribuir o aplicativo de videoconferência Location-Based um valor de prioridade "3" Isso colocaria a prioridade dos aplicativos na seguinte ordem: outros aplicativos (prioridades: de 0 a 1), "UdcAgent" (prioridade: 2), Location-Based aplicativo de conferência de roteamento (prioridade: 3), outros aplicativos (prioridades: 4 a 8), "defaultrouting" (prioridade: 9), "ExumRouting" (prioridade: 10) e "OutboundRouting" (prioridade: 11)

Depois de encontrar o valor de prioridade correto para o aplicativo de videoconferência de Location-Based, digite o seguinte cmdlet para cada servidor de Front-End pool ou Standard Edition que os usuários habilitarem para o roteamento Location-Based:

```powershell
New-CsServerApplication -Identity Service:Registrar:<Pool FQDN>/LBRouting -Priority <Application Priority> -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

Por exemplo:

```powershell
New-CsServerApplication -Identity Service:Registrar:LS2013CU2LBRPool.contoso.com/LBRouting -Priority 3 -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

Depois de usar esse cmdlet, reinicie todos os servidores front-end no pool ou os servidores Standard Edition nos quais o aplicativo de audioconferência Location-Based está habilitado.

<div>


> [!IMPORTANT]  
> Location-Based os enforcementos de roteamento para conferências ou transferências consuldas não serão impostos até que todos os servidores de front-end nos pools aplicáveis ou servidores padrão da edição sejam reiniciados.



</div>

Depois que o aplicativo de conferência de roteamento Location-Based foi habilitado com êxito e todos os servidores de Lync aplicáveis foram reiniciados, todas as conferências organizadas pelos usuários do Lync habilitados para Location-Based roteamento serão monitoradas para evitar a interligação PSTN em desvio

</div>

</div>

<span> </span>

</div>

</div>

</div>

