---
title: 'Lync Server 2013: tabela ConferenceJoinTimeThresholds'
description: 'Lync Server 2013: ConferenceJoinTimeThresholds Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceJoinTimeThresholds table
ms:assetid: 3944d724-bdd8-4d1c-a2af-933ee8141529
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204809(v=OCS.15)
ms:contentKeyID: 48183855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e38c8b99f444e16309882b6a8885d166fdceb9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434456"
---
# <a name="conferencejointimethresholds-table-in-lync-server-2013"></a>Tabela ConferenceJoinTimeThresholds no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-28_

A tabela ConferenceJoinTimeThresholds contém os limites de classificação usados pelo relatório de Resumo de tempo de ingresso em conferência. O relatório de Resumo de tempo de ingresso em conferência resume o tempo necessário para que os usuários ingressem com êxito em uma conferência; esses valores de tempo são relatados como uma média e em uma das seguintes categorias:

  - Menos de 2 segundos.

  - Entre 2 e 5 segundos.

  - Entre 5 segundos e 10 segundos.

  - Mais de 10 segundos.

A tabela ConferenceJoinTimeThresholds contém os valores de classificação 2 segundos, 5 segundos e 10 segundos.

Esta tabela foi introduzida no Microsoft Lync Server 2013.


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Coluna</th>
<th>Tipo de dados</th>
<th>Chave/índice</th>
<th>Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Thresholdid</strong></p></td>
<td><p>int</p></td>
<td><p>Primária</p></td>
<td><p>Identificador exclusivo da classificação.</p></td>
</tr>
<tr class="even">
<td><p><strong>ThresholdValue</strong></p></td>
<td><p>int</p></td>
<td></td>
<td><p>Limite superior da classificação. Os valores permitidos são:</p>
<ol>
<li><p>2</p></li>
<li><p>5</p></li>
<li><p>254</p></li>
</ol></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

