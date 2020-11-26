---
title: 'Lync Server 2013: tblComplianceState'
description: 'Lync Server 2013: tblComplianceState.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceState
ms:assetid: ea82e56c-3cca-4d89-b4e6-6bcaeb1f2830
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615045(v=OCS.15)
ms:contentKeyID: 48185937
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6eaf35eee8b4e24ec4d04e607fa77fd91b91e4e8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423509"
---
# <a name="tblcompliancestate-in-lync-server-2013"></a>tblComplianceState no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-06-28_

tblComplianceState contém informações de estado de conformidade em todo o pool.

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
<td><p>lastProcessedEntryID</p></td>
<td><p>bigint, e não nulo</p></td>
<td><p>ID do evento de conformidade processado mais recente.</p></td>
</tr>
<tr class="even">
<td><p>activeServerID</p></td>
<td><p>int, não nulo</p></td>
<td><p>ID do servidor de conformidade que mantém o bloqueio exclusivo no banco de dados ou-1 se nenhum.</p></td>
</tr>
<tr class="odd">
<td><p>lockExpirationTime</p></td>
<td><p>datetime2, não nulo</p></td>
<td><p>Bloquear o tempo de expiração (se activeServerID não for-1).</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

