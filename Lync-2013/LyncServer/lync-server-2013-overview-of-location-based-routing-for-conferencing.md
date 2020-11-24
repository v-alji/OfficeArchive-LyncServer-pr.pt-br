---
title: 'Lync Server 2013: visão geral do roteamento Location-Based para conferência'
description: 'Lync Server 2013: visão geral do roteamento Location-Based para conferência.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing for conferencing
ms:assetid: 8b86740e-db95-4304-bb83-64d0cbb91d47
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362815(v=OCS.15)
ms:contentKeyID: 56335084
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a8fe9cdf4a797243c3ec04b3466011f374fb0d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390283"
---
# <a name="overview-of-location-based-routing-for-conferencing-in-lync-server-2013"></a>Visão geral do roteamento Location-Based para conferência no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-07-19_

O aplicativo de conferência de roteamento Location-Based fornece ao Lync conferências um mecanismo para impedir que a chamada em PSTN seja ignorada. O aplicativo monitora conferências ativas e aplica Location-Based restrições de roteamento com base no local dos usuários do Lync participantes.

O aplicativo de conferência de roteamento Location-Based determina se Location-Based roteamento deve ser imposto em uma reunião do Lync se os seguintes critérios forem atendidos:

  - O organizador da reunião está habilitado para Location-Based roteamento. Location-Based restrições de roteamento serão aplicadas somente a conferências organizadas por usuários que estão habilitados para Location-Based roteamento.

  - Pelo menos um participante da reunião é um ponto de extremidade PSTN. As restrições de roteamento Location-Based são aplicáveis somente para conferências que incluem pontos de extremidade PSTN.

  - O local da rede onde o gateway PSTN usado para fazer a ligação da conferência com o PSTN está localizado, bem como os locais de rede, de onde os organizadores e os participantes estão se conectando.

O aplicativo de conferência de roteamento Location-Based impede a participação de usuários do Lync e pontos de extremidade PSTN de diferentes sites de rede para a mesma conferência. Se o organizador de uma reunião estiver habilitado para roteamento Location-Based, o aplicativo de conferência forçará as seguintes restrições:

  - Os pontos de extremidade que podem ingressar em uma reunião do Lync dependem dos pontos de extremidade que já ingressaram na conferência, e essa restrição é ajustada quando os pontos de extremidade associados deixam e os novos pontos de extremidade entram na conferência. Se os organizadores e os participantes ingressarem em uma reunião do Lync a partir do mesmo local de rede, um ponto de extremidade PSTN, outro participante do mesmo local de rede, outro participante de um site de rede diferente ou um participante de um site de rede desconhecido tem permissão para ingressar.

  - Se os organizadores e os participantes estiverem ingressando na reunião de locais de rede diferentes ou desconhecidos, um ponto de extremidade PSTN não terá autorização para participar da reunião se a chamada PSTN ingressar de um tronco SIP habilitado para Roteamento Baseado na Localização.

  - Se os organizadores e participantes estiverem ingressando na reunião no mesmo local de rede e houver participantes ingressando na mesma reunião a partir da PSTN, um ponto de extremidade do Lync de um site de rede diferente não poderá ingressar na reunião.

Estas Location-Based restrições de roteamento são resumidas na tabela a seguir.


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Usuário(s) em uma conferência em um determinado ponto</p></td>
<td><p>Usuário(s) autorizados a ingressar na conferência</p></td>
<td><p>Usuário(s) não autorizados a ingressar na conferência</p></td>
</tr>
<tr class="even">
<td><p>Usuário (s) do cliente VoIP do Lync de um único site de rede</p></td>
<td><p>Usuário do cliente VoIP do Lync do mesmo local de rede</p>
<p>Usuário do cliente VoIP do Lync de um site de rede diferente</p>
<p>Usuário do cliente VoIP do Lync de um site de rede desconhecido</p>
<p>Usuário do cliente VoIP do Lync federado</p>
<p>Usuário ingressando a partir de um ponto de extremidade PSTN</p></td>
<td><p>Nenhum</p></td>
</tr>
<tr class="odd">
<td><p>Usuário (s) do cliente VoIP do Lync de um site de rede desconhecido</p></td>
<td><p>Usuário do cliente VoIP do Lync de qualquer site</p>
<p>Usuário do cliente VoIP do Lync de um site desconhecido</p>
<p>Usuário do cliente VoIP do Lync federado</p></td>
<td><p>Usuário ingressando por meio de um ponto de extremidade PSTN</p></td>
</tr>
<tr class="even">
<td><p>Usuários do cliente VoIP do Lync de diferentes sites de rede</p></td>
<td><p>Usuário do cliente VoIP do Lync de qualquer site de rede</p>
<p>Usuário do cliente VoIP do Lync de um site de rede desconhecido</p>
<p>Usuário do cliente VoIP do Lync federado</p></td>
<td><p>Usuário ingressando por meio de um ponto de extremidade PSTN</p></td>
</tr>
<tr class="odd">
<td><p>Usuários do cliente VoIP do Lync de um único site de rede e usuários que ingressam em um ponto de extremidade PSTN</p></td>
<td><p>Usuário do cliente VoIP do Lync do mesmo local de rede</p></td>
<td><p>Usuário do cliente VoIP do Lync de um site de rede diferente</p>
<p>Usuário do cliente VoIP do Lync de um site de rede desconhecido</p>
<p>Usuário do cliente VoIP do Lync federado</p></td>
</tr>
</tbody>
</table>


Veja a seguir as características adicionais do aplicativo de conferência de Location-Based de roteamento:

  - Quando um usuário não tem permissão para ingressar em uma conferência fornecida Location-Based restrições de roteamento, os usuários chamam para a conferência serão recusados e o cliente do Lync reportará que a chamada não foi concluída ou encerrada.

  - Um ponto de extremidade PSTN ingressando em uma conferência com Location-Based encaminhamentos de roteamento não será restringido a ingressar na conferência independentemente de seu estado se o ponto de extremidade se associar por meio de um tronco que não está habilitado para Location-Based roteamento.

  - Um sistema PBX conectado a um servidor de mediação por meio de um tronco SIP que não faz chamadas para a PSTN terá os mesmos enforces como usuários do Lync localizados no mesmo local de rede onde o tronco SIP está definido. Por exemplo, um ponto de extremidade PSTN poderá ingressar em uma conferência com um usuário do PBX e um usuário do Lync se eles estiverem localizados no mesmo site de rede; caso contrário, o ponto de extremidade PSTN não terá permissão para ingressar na conferência se o usuário do PBX estiver em um site de rede diferente do que o usuário do Lync.

</div>

<span> </span>

</div>

</div>

</div>

