---
title: 'Lync Server 2013: Tabela UserAgent'
description: 'Lync Server 2013: tabela UserAgent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgent table
ms:assetid: d6bda1c0-b053-457a-9ffa-2ae859788775
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398939(v=OCS.15)
ms:contentKeyID: 48185582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b701d8384313d0267dd566e0c32242f6cc077472
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439125"
---
# <a name="useragent-table-in-lync-server-2013"></a>Tabela UserAgent no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-05-25_

A tabela UserAgent é uma tabela de suporte que armazena uma lista de vários agentes de usuário que participaram de sessões registradas no banco de dados. Cada registro na tabela representa um agente do usuário


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Coluna</strong></th>
<th><strong>Tipo de dados</strong></th>
<th><strong>Chave/índice</strong></th>
<th><strong>Detalhes</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>UserAgentKey</strong></p></td>
<td><p>int</p></td>
<td><p>Primária</p></td>
<td><p>Número exclusivo que identifica esse agente de usuário.</p></td>
</tr>
<tr class="even">
<td><p><strong>UserAgent</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Exclusividade</p></td>
<td><p>Cadeia de caracteres do agente do usuário.</p></td>
</tr>
<tr class="odd">
<td><p><strong>UAType</strong></p></td>
<td><p>smallint</p></td>
<td><p> </p></td>
<td><p>1 é o servidor de mediação.</p>
<p>2 é um servidor de conferência A/V.</p>
<p>4 é o Lync.</p>
<p>8 é o telefone IP.</p>
<p>16 é o console do Live Meeting.</p>
<p>o 32 é uma ferramenta de validação de implantação (DVT).</p>
<p>o 64 é o Lync em computadores Macintosh.</p>
<p>o 128 é o Office Communications Server 2007 R2 Attendant.</p>
<p>o 256 é o serviço de anúncio de conferências.</p>
<p>o 512 é o atendedor automático da conferência.</p>
<p>o 1024 é um aplicativo de grupo de resposta.</p>
<p>2048 está fora do controle de voz.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

