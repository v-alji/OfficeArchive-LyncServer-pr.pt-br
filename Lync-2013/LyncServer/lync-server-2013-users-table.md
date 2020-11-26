---
title: 'Lync Server 2013: Tabela Users'
description: 'Lync Server 2013: tabela usuários.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Users table
ms:assetid: a8d71373-4b57-4245-9f02-f7fc0d9fcd3c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412791(v=OCS.15)
ms:contentKeyID: 48185032
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b1418e162a04e46ee0dfeca082aa66b0665fc77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436178"
---
# <a name="users-table-in-lync-server-2013"></a>Tabela Users no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-28_

A tabela usuários é uma tabela de suporte. Cada registro na tabela armazena informações sobre um usuário envolvido em chamadas ou sessões que têm registros no banco de dados.


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
<td><p><strong>NextUpdateTS</strong></p></td>
<td><p>datetime</p></td>
<td></td>
<td><p>Carimbo de data/hora para uso interno.</p></td>
</tr>
<tr class="even">
<td><p><strong>ID</strong></p></td>
<td><p>int</p></td>
<td><p>Primária</p></td>
<td><p>Número exclusivo que identifica esse usuário.</p></td>
</tr>
<tr class="odd">
<td><p><strong>UserUri</strong></p></td>
<td><p>nvarchar (450)</p></td>
<td><p> </p></td>
<td><p>URI de usuário.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tenantid</strong></p></td>
<td><p>int</p></td>
<td><p>Exterior</p></td>
<td><p>A ID de locatário deste usuário. Consulte a <a href="lync-server-2013-tenants-table.md">tabela locatários no Lync Server 2013</a> para obter mais informações.</p></td>
</tr>
<tr class="odd">
<td><p><strong>UriTypeId</strong></p></td>
<td><p>int</p></td>
<td><p>Exterior</p></td>
<td><p>O tipo de URI deste usuário. Consulte a <a href="lync-server-2013-uritypes-table.md">tabela UriTypes no Lync Server 2013</a> para obter mais informações.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

