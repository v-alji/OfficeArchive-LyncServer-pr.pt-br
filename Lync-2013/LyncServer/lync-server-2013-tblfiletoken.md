---
title: 'Lync Server 2013: tblFileToken'
description: 'Lync Server 2013: tblFileToken.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblFileToken
ms:assetid: 49e7dd79-1607-443c-818a-88c160e4ed06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558646(v=OCS.15)
ms:contentKeyID: 48184073
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c0a0465bd769cff5c23c00a98f79e2346232175
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423525"
---
# <a name="tblfiletoken-in-lync-server-2013"></a>tblFileToken no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-12_

tblFileToken contém tokens temporários para fins de transferência de arquivo.

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
<td><p>Filetoken</p></td>
<td><p>nvarchar (50), NOT NULL</p></td>
<td><p>Token exclusivo (a GUID).</p></td>
</tr>
<tr class="even">
<td><p>fileTokenUserID</p></td>
<td><p>int, não nulo</p></td>
<td><p>ID da entidade de segurança que está transferindo o arquivo.</p></td>
</tr>
<tr class="odd">
<td><p>fileTokenChannelID</p></td>
<td><p>GUID, não nulo</p></td>
<td><p>GUID do nó da sala de chat.</p></td>
</tr>
<tr class="even">
<td><p>fileTokenExpireDate</p></td>
<td><p>DateTime, não nulo</p></td>
<td><p>Tempo de expiração. (Os tokens expiram após 30 minutos, a menos que sejam fixados (consulte as descrições a seguir nesta coluna).</p></td>
</tr>
<tr class="odd">
<td><p>fileTokenComplianceFileUrl</p></td>
<td><p>nvarchar(256)</p></td>
<td><p>URL do arquivo transferido (para uso do serviço de conformidade).</p></td>
</tr>
<tr class="even">
<td><p>fileTokenComplianceThumbnailUrl</p></td>
<td><p>nvarchar(256)</p></td>
<td><p>URL da miniatura do arquivo transferido (para uso do serviço de conformidade).</p></td>
</tr>
<tr class="odd">
<td><p>fileTokenComplianceTime</p></td>
<td><p>datetime2</p></td>
<td><p>Carimbo de data/hora para a operação de transferência de arquivo real (para uso do serviço de conformidade).</p></td>
</tr>
<tr class="even">
<td><p>fileTokenComplianceIsUpload</p></td>
<td><p>bit</p></td>
<td><p>Verdadeiro se for carregado; Falso se baixar (para uso do serviço de conformidade).</p></td>
</tr>
<tr class="odd">
<td><p>fileTokenCompliancePinned</p></td>
<td><p>bit, e não nulo</p></td>
<td><p>Verdadeiro se o token estiver fixado. Ele é usado para manter o token na tabela até que o serviço de conformidade tenha a chance de recuperar os campos relevantes dele.</p></td>
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
<td><p>Filetoken</p></td>
<td><p>Chave primária.</p></td>
</tr>
<tr class="even">
<td><p>fileTokenChannelID</p></td>
<td><p>Chave estrangeira com Lookup na tabela tblNode. nodeGuid.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

