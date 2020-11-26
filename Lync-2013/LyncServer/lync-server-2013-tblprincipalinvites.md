---
title: 'Lync Server 2013: tblPrincipalInvites'
description: 'Lync Server 2013: tblPrincipalInvites.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalInvites
ms:assetid: 548ec156-4d1a-469d-a804-62cff226e5c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558650(v=OCS.15)
ms:contentKeyID: 48184141
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d30d741864ed2a3cfbec8329215be33c21b3b262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423502"
---
# <a name="tblprincipalinvites-in-lync-server-2013"></a>tblPrincipalInvites no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-06-25_

tblPrincipalInvites contém convites para todos os usuários provisionados para todos os nós com convite automático ativado.

### <a name="columns"></a>Colunas

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Coluna</th>
<th>Tipo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>multiimprimir</p></td>
<td><p>int, não nulo</p></td>
<td><p>ID da entidade de segurança.</p></td>
</tr>
<tr class="even">
<td><p>invID</p></td>
<td><p>int, não nulo</p></td>
<td><p>Número seqüencial exclusivo (por ID da entidade) gerado pela tabela tblLastInviteId.</p></td>
</tr>
<tr class="odd">
<td><p>NodeId</p></td>
<td><p>int, não nulo</p></td>
<td><p>ID do nó (somente sala de chat).</p></td>
</tr>
<tr class="even">
<td><p>criar</p></td>
<td><p>DateTime, não nulo</p></td>
<td><p>Hora da criação.</p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a>As

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Coluna</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;, NodeId&gt;</p></td>
<td><p>Chave primária.</p></td>
</tr>
<tr class="even">
<td><p>multiimprimir</p></td>
<td><p>Chave estrangeira com Lookup na tabela tblPrincipal. retoid.</p></td>
</tr>
<tr class="odd">
<td><p>NodeId</p></td>
<td><p>Chave estrangeira com Lookup na tabela tblNode. NodeId.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

