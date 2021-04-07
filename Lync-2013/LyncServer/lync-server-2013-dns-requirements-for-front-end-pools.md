---
title: 'Lync Server 2013: requisitos DNS para pools de Front-End'
description: 'Lync Server 2013: requisitos DNS para pools de Front-End.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pools
ms:assetid: ba28919c-fbbe-4c54-8bf9-2b0cd3fa39c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412910(v=OCS.15)
ms:contentKeyID: 48185228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c0369e82bd8ed2ea63e2156728b41f9942b0148
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429067"
---
# <a name="dns-requirements-for-front-end-pools-in-lync-server-2013"></a>Requisitos dns para pools de front-end no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico Última Modificação:** 2012-11-07_

Esta seção descreve os registros DNS (Sistema de Nomes de Domínio) necessários para a implantação de pools de Front-End.

<div>

## <a name="dns-records-for-front-end-pools"></a>Registros DNS para pools de front-end

A tabela a seguir especifica os requisitos DNS para uma implantação de pool de Front-End do Lync Server 2013.

### <a name="dns-requirements-for-a-front-end-pool"></a>Requisitos DNS para um pool de front-end

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
<td><p>Pool de front-end com vários Servidores Front-End e um balanceador de carga de hardware (se o balanceamento de carga DNS também é implantado nesse pool)</p></td>
<td><p>Ao usar o balanceamento de carga DNS e um balanceador de carga de hardware, você precisa hospedar registros (A). Crie um registro A interno que resolva o FQDN (nome de domínio totalmente qualificado) do pool de Front-End para balanceamento de carga DNS. Crie um registro de host interno (A) para os serviços Web internos para o endereço IP virtual (VIP) do balanceador de carga. Você deve usar o nome dos serviços Web internos conforme definido no Construtor de Topologias.</p>
<p>Por exemplo, se você usar balanceamento de carga DNS e balanceamento de carga de hardware, terá um registro A para cada Servidor Front-End em um pool para balanceamento de carga DNS e um registro A para os serviços Web internos apontando para o IP virtual do balanceador de carga de hardware:</p>
<ul>
<li><p>Balanceamento de carga DNS: Pool01.contoso.net IP do pool 10.10.10.5</p>
<div>

> [!WARNING]  
> Cada Servidor Front-End também terá um registro A distinto:


</div>
<ol>
<li><p>FE01.contoso.net 10.10.10.1</p></li>
<li><p>FE02.contoso.net 10.10.10.2</p></li>
<li><p>FE03.contoso.net 10.10.10.3</p></li>
<li><p>FE04.contoso.net 10.10.10.4</p></li>
</ol></li>
<li><p>Balanceamento de carga de hardware: WebInternal.contoso.net IP do HLB VIP 192.168.10.5</p></li>
</ul>
<p>Todo o tráfego, exceto o tráfego HTTP/HTTPS, usará o Pool01.contoso.net registro. O tráfego HTTP/HTTPS usará o endereço de serviços Web interno definido de 192.168.10.5</p></td>
</tr>
<tr class="even">
<td><p>Pool de front-end com balanceamento de carga DNS implantado</p></td>
<td><p>Um conjunto de registros A internos que resolvem o FQDN do pool para o endereço IP de cada servidor no pool. Deve haver um registro A para cada servidor no pool.</p></td>
</tr>
<tr class="odd">
<td><p>Pool de front-end com balanceamento de carga DNS implantado</p></td>
<td><p>Um conjunto de registros A internos que resolvem o FQDN de cada servidor no pool para o endereço IP desse servidor. Para obter detalhes, <a href="lync-server-2013-dns-load-balancing.md">consulte Balanceamento de carga DNS no Lync Server 2013</a> na documentação planejamento.</p></td>
</tr>
<tr class="even">
<td><p>Pool de Front-End com um único Servidor Front-End e um banco de dados back-end dedicado, mas nenhum balanceador de carga</p></td>
<td><p>Um registro A interno que resolve o FQDN do pool de Front-End para o endereço IP do único Servidor Front-End enterprise edition.</p></td>
</tr>
<tr class="odd">
<td><p>Entrada automática do cliente</p></td>
<td><p>Para cada domínio SIP com suporte, um registro SRV para _sipinternaltls._tcp. &lt; domínio sobre a porta 5061 que mapeia para o &gt; FQDN do pool de Front-End que autentica e redireciona solicitações de cliente para entrada. Para obter detalhes, consulte REQUISITOS DNS para entrada automática do <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">cliente no Lync Server 2013</a>.</p></td>
</tr>
<tr class="even">
<td><p>Descoberta do serviço Web de Atualização de Dispositivo por dispositivos UC (Comunicações Unificadas)</p></td>
<td><p>Um registro A interno com o nome ucupdates-r2. &lt; Domínio SIP &gt; que resolve para o endereço IP do pool de Front-End que hospeda o serviço Web de Atualização de Dispositivo. Na situação em que um dispositivo UC está ligado, mas um usuário nunca fez logons no dispositivo, o registro A permite que o dispositivo descubra o pool de Front-End que hospeda o serviço Web de Atualização de Dispositivo e obtenha atualizações. Caso contrário, os dispositivos obterão essas informações, embora o provisionamento em banda na primeira vez em que um usuário faz logona.</p>
<div>

> [!IMPORTANT]  
> Se você tiver uma implantação existente do serviço Web de Atualização de Dispositivo no Lync Server 2010, já criou um registro A interno com o nome ucupdates. &lt; Domínio SIP &gt; . Para Microsoft Office Communications Server 2007 R2, você deve criar um registro DNS A adicional com o nome ucupdates-r2. &lt; Domínio SIP &gt; .


</div></td>
</tr>
<tr class="odd">
<td><p>Um proxy reverso para dar suporte ao tráfego HTTP</p></td>
<td><p>Um registro A externo que resolve o FQDN do farm web externo para o endereço IP externo do proxy reverso. Os clientes e dispositivos UC usam esse registro para se conectar ao proxy reverso. Para obter detalhes, <a href="lync-server-2013-determine-dns-requirements.md">consulte Determine DNS requirements for Lync Server 2013</a> na documentação planejamento.</p></td>
</tr>
</tbody>
</table>


A tabela a seguir mostra um exemplo dos registros DNS necessários para o FQDN do farm web interno.

### <a name="example-dns-records-for-internal-web-farm-fqdn"></a>Exemplo de registros DNS para FQDN do Farm Web Interno

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>FQDN do farm web interno</th>
<th>FQDN do pool</th>
<th>Registros DNS A( s)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>webcon.contoso.com</p></td>
<td><p>ee-pool.contoso.com</p></td>
<td><p>Registro DNS A para o ee-pool.contoso.com que resolve para o endereço VIP do balanceador de carga usado pelos Servidores front-end.</p>
<p>Registro DNS A para webcon.contoso.com que é resolvido para o endereço VIP do balanceador de carga usado pelos Servidores front-end.</p></td>
</tr>
<tr class="even">
<td><p>ee-pool.contoso.com</p></td>
<td><p>ee-pool.contoso.com</p></td>
<td><p>Registro DNS A para ee-pool.contoso.com que resolve para o endereço IP virtual (VIP) do balanceador de carga usado pelos Servidores Front-End Enterprise Edition no pool de Front-End.</p>
<p>Observe que, se você estiver usando o balanceamento de carga DNS neste pool, o pool de Front-End e o farm web interno não poderão ter o mesmo FQDN.</p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

