---
title: 'Lync Server 2013: Location-Based transferências de chamadas para roteamento e consultoria'
description: 'Lync Server 2013: Location-Based transferências de chamadas de roteamento e consultoria.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing and consultative call transfers
ms:assetid: b12460c2-36c8-481f-b867-fe10dc1c0bdf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362836(v=OCS.15)
ms:contentKeyID: 56335089
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d07cf6a33ff4d6ad57f8913a798fac3bc393a00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426548"
---
# <a name="location-based-routing-and-consultative-call-transfers-in-lync-server-2013"></a>Location-Based transferências de chamadas de roteamento e consultoria no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-07-31_

Além de impor o roteamento do Location-Based a reuniões do Lync, o aplicativo de conferência de roteamento de Location-Based impõe Location-Based restrições de roteamento em transferências de chamadas consultivas que entram em pontos de extremidade PSTN. Uma transferência de chamada consultiva é estabelecida entre duas partes em que uma delas transfere a chamada para um novo usuário. Por exemplo, um ponto de extremidade PSTN chama o usuário A (chamado do Lync). O usuário A determina que o usuário PSTN deve ser encaminhado para o usuário B (usuário do Lync). O usuário A coloca a chamada com o usuário PSTN em espera e liga para o usuário B. O usuário B concorda em falar com o usuário PSTN. O usuário A transfere a chamada espera para o usuário B.

**Fluxo da Transferência de Chamada Consultiva**

![Roteamento baseado em local para o diagrama de conferência](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "Roteamento baseado em local para o diagrama de conferência")

Quando um usuário habilitado para Location-Based roteamento inicia uma transferência de chamadas consuldas de um ponto de extremidade PSTN (conforme mostrado na figura anterior), isso cria duas chamadas ativas, uma chamada entre o usuário PSTN e o usuário do Lync a e a outra entre o usuário do Lync A e o usuário do Lync B. o comportamento a seguir é imposto pelo aplicativo Location-Based de audioconferência:

  - Se o encaminhamento de tronco SIP a chamada PSTN estiver autorizada a redirecionar a chamada PSTN para o site de rede onde o usuário do Lync B (ou seja, destino da transferência) estiver localizado, a transferência de chamada será permitida; caso contrário, a transferência de chamadas consultivas será bloqueada. Essa autorização é realizada caso o local da parte transferida seja no mesmo local de rede do tronco SIP que está encaminhando a chamada ativa para o ponto de extremidade PSTN.

  - Se o tronco SIP que faz a chamada PSTN não estiver autorizado a direcionar chamadas para o site de rede onde a parte transferida (usuário B do Lync) estiver localizada ou a parte transferidas estiver localizada em um site de rede desconhecido, a transferência de chamadas consuldas para o ponto de extremidade PSTN (ou seja, destino da transferência de chamada) será bloqueada.

A tabela a seguir descreve como as restrições de roteamento Location-Based são aplicadas pelo aplicativo Location-Based de audioconferência para transferências de chamadas consultivas. Embora os pontos de extremidade PBX não estejam associados diretamente a um local de rede, o tronco SIP ao qual o PBX está conectado pode ser atribuído a um local de rede. Portanto, o ponto de extremidade PBX pode ser indiretamente associado a um local de rede.


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Local de rede da parte transferida da chamada</p></td>
<td><p>Local de rede de destino da transferência de chamada</p></td>
<td><p>Comportamento</p></td>
</tr>
<tr class="even">
<td><p>Ponto de extremidade PSTN</p></td>
<td><p>Usuário do Lync no mesmo local de rede (por exemplo, site 1)</p></td>
<td><p>A transferência consultiva será permitida</p></td>
</tr>
<tr class="odd">
<td><p>Ponto de extremidade PSTN</p></td>
<td><p>Usuário do Lync em sites de rede diferentes (por exemplo, site 2)</p></td>
<td><p>A transferência consultiva não será permitida</p></td>
</tr>
<tr class="even">
<td><p>Ponto de extremidade PSTN</p></td>
<td><p>Usuário do Lync em um site de rede desconhecido</p></td>
<td><p>A transferência consultiva não será permitida</p></td>
</tr>
<tr class="odd">
<td><p>Ponto de extremidade PSTN</p></td>
<td><p>Usuário do Lync federado</p></td>
<td><p>A transferência consultiva não será permitida</p></td>
</tr>
<tr class="even">
<td><p>Ponto de extremidade PSTN</p></td>
<td><p>Ponto de extremidade do PBX no mesmo local (isto é, local 1)</p></td>
<td><p>A transferência consultiva será permitida</p></td>
</tr>
<tr class="odd">
<td><p>Ponto de extremidade PSTN</p></td>
<td><p>Ponto de extremidade PBX em locais diferentes (isto é, local 2)</p></td>
<td><p>A transferência consultiva não será permitida</p></td>
</tr>
<tr class="even">
<td><p>Ponto de extremidade do PBX no mesmo local (isto é, local 1)</p></td>
<td><p>Ponto de extremidade PSTN</p></td>
<td><p>A transferência consultiva será permitida</p></td>
</tr>
<tr class="odd">
<td><p>Ponto de extremidade do PBX em locais diferentes (i.e. local 2)</p></td>
<td><p>Ponto de extremidade PSTN</p></td>
<td><p>A transferência consultiva não será permitida</p></td>
</tr>
<tr class="even">
<td><p>Ponto de extremidade PBX em qualquer local</p></td>
<td><p>Usuário do Lync no mesmo local de rede (por exemplo, site 1)</p></td>
<td><p>A transferência consultiva será permitida</p></td>
</tr>
<tr class="odd">
<td><p>Ponto de extremidade PBX em qualquer local</p></td>
<td><p>Usuário do Lync em sites de rede diferentes (por exemplo, site 2)</p></td>
<td><p>A transferência consultiva será permitida</p></td>
</tr>
<tr class="even">
<td><p>Ponto de extremidade PBX em qualquer local</p></td>
<td><p>Usuário do Lync em um site de rede desconhecido</p></td>
<td><p>A transferência consultiva será permitida</p></td>
</tr>
<tr class="odd">
<td><p>Ponto de extremidade PBX em qualquer local</p></td>
<td><p>Usuário do Lync federado</p></td>
<td><p>A transferência consultiva será permitida</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

