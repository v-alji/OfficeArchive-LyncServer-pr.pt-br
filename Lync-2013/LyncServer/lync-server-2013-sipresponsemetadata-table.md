---
title: 'Lync Server 2013: tabela SIPResponseMetaData'
description: 'Lync Server 2013: SIPResponseMetaData Table.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SIPResponseMetaData table
ms:assetid: cf723737-4a75-4352-829b-f4954aa59716
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205294(v=OCS.15)
ms:contentKeyID: 48185510
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 402cff331f81a9b46028d76de69deeaace8d5ae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444620"
---
# <a name="sipresponsemetadata-table-in-lync-server-2013"></a>Tabela SIPResponseMetaData no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-28_

O SIPResponseMetaDataTable contém uma lista de códigos de resposta SIP e a classificação e definição de cada um desses códigos. Esses códigos são gerados em resposta a eventos que afetam dispositivos SIP e sessões de comunicação SIP; por exemplo, o código de resposta 403 é gerado quando um dispositivo SIP faz uma solicitação, mas o servidor recusa para honrar essa solicitação.

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
<td><p><strong>ResponseCode</strong></p></td>
<td><p>int</p></td>
<td><p>Primária</p></td>
<td><p>Valor numérico que representa o código de resposta SIP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Classe</strong></p></td>
<td><p>int</p></td>
<td></td>
<td><p>Classificação geral do código de resposta. As classificações incluem:</p>
<ul>
<li><p>1 – respostas informativas</p></li>
<li><p>2 – respostas bem-sucedidas</p></li>
<li><p>3 – respostas de redirecionamento</p></li>
<li><p>4 – respostas de falha do cliente</p></li>
<li><p>5--respostas de falha do servidor</p></li>
<li><p>6 – resposta de falha global</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Descrição</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td></td>
<td><p>Descrição do código de resposta SIP. Por exemplo, o código de resposta 181 tem a seguinte descrição:</p>
<p>A chamada está sendo encaminhada</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

