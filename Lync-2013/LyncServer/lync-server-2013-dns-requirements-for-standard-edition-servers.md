---
title: 'Lync Server 2013: requisitos dns para servidores Standard Edition'
description: 'Lync Server 2013: requisitos DNS para servidores Standard Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Standard Edition servers
ms:assetid: 3d6bbe65-e7ce-491b-a0bd-d2f7197f240d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425900(v=OCS.15)
ms:contentKeyID: 48183920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cc93549e07fb82304ad76b051730eab972530764
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389784"
---
# <a name="dns-requirements-for-standard-edition-servers-in-lync-server-2013"></a>Requisitos dns para servidores Standard Edition no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico Última Modificação:** 2012-06-19_

Esta seção descreve os registros DNS (Sistema de Nomes de Domínio) necessários para a implantação de servidores Standard Edition.

<div>

## <a name="dns-records-for-standard-edition-servers"></a>Registros DNS para servidores Standard Edition

A tabela a seguir especifica os requisitos DNS para a implantação do servidor Lync Server 2013 Standard Edition.

### <a name="dns-requirements-for-a-standard-edition-server"></a>Requisitos DNS para um Servidor Standard Edition

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Cenário da implantação</th>
<th>Requisitos de DNS</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Servidor Standard Edition</p></td>
<td><p>Um registro A interno que resolve o nome de domínio totalmente qualificado (FQDN) do servidor para seu endereço IP.</p></td>
</tr>
<tr class="even">
<td><p>Entrada automática do cliente</p></td>
<td><p>Para cada domínio SIP com suporte, um registro SRV para _sipinternaltls._tcp. &lt; domínio &gt; sobre a porta 5061 que mapeia para o FQDN do servidor Standard Edition que autentica e redireciona solicitações de cliente para entrada. Para obter detalhes, consulte REQUISITOS DNS para entrada automática do <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">cliente no Lync Server 2013</a>.</p></td>
</tr>
<tr class="odd">
<td><p>Descoberta do serviço Web de Atualização de Dispositivo por dispositivos UC (Comunicações Unificadas)</p></td>
<td><p>Um registro A interno com o nome ucupdates-r2. &lt; Domínio SIP que resolve para o endereço IP do servidor Standard Edition que hospeda &gt; o serviço Web de Atualização de Dispositivo. Na situação em que um dispositivo UC está ligado, mas um usuário nunca fez logons no dispositivo, o registro A permite que o dispositivo descubra o servidor que hospeda o serviço Web de Atualização de Dispositivo e obtenha atualizações. Caso contrário, os dispositivos obtêm essas informações por meio do provisionamento em banda na primeira vez que o usuário faz logon.</p></td>
</tr>
<tr class="even">
<td><p>Um proxy reverso para dar suporte ao tráfego HTTP</p></td>
<td><p>Um registro A externo que resolve o FQDN do farm web externo para o endereço IP externo do proxy reverso. Os clientes e dispositivos UC usam esse registro para se conectar ao proxy reverso. Para obter detalhes, <a href="lync-server-2013-determine-dns-requirements.md">consulte Determine DNS requirements for Lync Server 2013</a> na documentação planejamento.</p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

