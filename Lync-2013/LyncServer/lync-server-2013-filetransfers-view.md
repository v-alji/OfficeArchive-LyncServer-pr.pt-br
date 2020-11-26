---
title: 'Lync Server 2013: modo de exibição de transferência de fileviews'
description: 'Lync Server 2013: modo de exibição de transferência de fileviews.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers view
ms:assetid: e52c3ad0-152e-4a18-af1c-1aff0d205151
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721914(v=OCS.15)
ms:contentKeyID: 49733848
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd2b084274a4d5daa093f2269617214f703ac03e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428150"
---
# <a name="filetransfers-view-in-lync-server-2013"></a>Modo de exibição de transferência de fileviews no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-10-01_

O modo de transferência de arquivo armazena informações sobre sessões de transferência de arquivos ponto a ponto. Este modo de exibição foi apresentado no Microsoft Lync Server 2013.

<div>


> [!NOTE]  
> O modo de exibição filetransfers contém todas as colunas na <A href="lync-server-2013-sessiondetails-view.md">exibição SessionDetails no Lync Server 2013</A> , além das colunas listadas abaixo.



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Coluna</th>
<th>Tipo de dados</th>
<th>Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>FileName</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Nome do arquivo transferido.</p></td>
</tr>
<tr class="even">
<td><p><strong>Cookie</strong></p></td>
<td><p>nvarchar(128</p></td>
<td><p>Usado para identificar todas as mensagens de acompanhamento como associadas a esta.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Fileidentity</strong></p></td>
<td><p>identificador</p></td>
<td><p>Identificador exclusivo para distinguir entre as transferências de arquivo que envolvem o mesmo nome de arquivo.</p></td>
</tr>
<tr class="even">
<td><p><strong>Aceite</strong></p></td>
<td><p>bit</p></td>
<td><p>Pode ser TRUE ou NULL. Se verdadeiro, rejeitar e cancelar será nulo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Rejeitar</strong></p></td>
<td><p>bit</p></td>
<td><p>Pode ser TRUE ou NULL. Se verdadeiro, aceitar e cancelar será nulo.</p></td>
</tr>
<tr class="even">
<td><p><strong>Cancelar</strong></p></td>
<td><p>bit</p></td>
<td><p>Pode ser TRUE ou NULL. Se verdadeiro, aceitar e rejeitar será nulo.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

