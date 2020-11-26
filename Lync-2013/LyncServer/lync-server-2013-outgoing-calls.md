---
title: 'Lync Server 2013: Chamadas de saída'
description: 'Lync Server 2013: chamadas feitas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Outgoing calls
ms:assetid: 885ffe6f-cd51-4f21-8d4f-a1ff8d818858
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994049(v=OCS.15)
ms:contentKeyID: 51803960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e14f19dec35a6da47a2ddd62657d5d087a854f16
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424832"
---
# <a name="outgoing-calls-in-lync-server-2013"></a>Chamadas de saída no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-03-09_

O roteamento de chamadas de saída de usuários habilitados para roteamento Location-Based é afetado pelo local de rede do ponto de extremidade do usuário. A tabela a seguir ilustra como Location-Based o roteamento afeta o roteamento de chamadas de saída, dependendo da localização do ponto de extremidade do chamador.

### <a name="caller-placing-an-outbound-call-to-the-pstn"></a>Pessoa fazendo uma chamada de saída para o PSTN

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Ponto de extremidade do usuário localizado em um local de rede habilitado para o Roteamento com Base no Local</th>
<th>Ponto de extremidade do usuário localizado em um local de rede desconhecido ou não habilitado para o Roteamento com Base no Local</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Autorização de chamadas de saída</p></td>
<td><p>A chamada é autorizada com base na política de voz do usuário</p></td>
<td><p>A chamada é autorizada com base na política de voz do usuário</p></td>
</tr>
<tr class="even">
<td><p>Roteamento de chamada de saída</p></td>
<td><p>A chamada é roteada de acordo com a política de roteamento de voz do local de rede</p></td>
<td><p>A chamada é roteada de acordo com a política de voz do usuário e somente por meio de troncos não habilitados para o Roteamento com Base no Local (se disponível)</p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a>Confira também


[Cenários para Roteamento Baseado em Local no Lync Server 2013](lync-server-2013-scenarios-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

