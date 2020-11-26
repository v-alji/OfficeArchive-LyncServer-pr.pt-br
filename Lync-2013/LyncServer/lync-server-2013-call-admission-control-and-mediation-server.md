---
title: 'Lync Server 2013: Controle de admissão de chamada e Servidor de Mediação'
description: 'Lync Server 2013: controle de admissão de chamadas e servidor de mediação.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call admission control and Mediation Server
ms:assetid: 76faccdc-67d0-4c8b-8e47-1e23c93b02c6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398585(v=OCS.15)
ms:contentKeyID: 48184546
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 77e4b12a11f941923d50f3ffcab7a8f9b6a9edc5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435926"
---
# <a name="call-admission-control-and-mediation-server-in-lync-server-2013"></a>Controle de admissão de chamada e Servidor de Mediação no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-21_

O controle de admissão de chamadas (CAC), apresentado primeiro no Lync Server 2010, gerencia a determinação da sessão em tempo real, com base na largura de banda disponível, para ajudar a evitar má qualidade da experiência (QoE) para usuários em redes congestionadas. Para dar suporte a esse recurso, o servidor de mediação, que fornece sinalização e conversão de mídia entre a infraestrutura Enterprise Voice e um provedor de entroncamento SIP ou gateway, é responsável pelo gerenciamento de largura de banda para suas duas interações no lado do Lync Server e no lado do gateway. No controle de admissão de chamadas, a entidade de terminação de uma chamada lida com a reserva de largura de banda. Os pares de gateway (gateway PSTN, IP-PBX, SBC) com o qual o servidor de mediação interage no lado do gateway não dão suporte ao controle de admissão de chamadas do Lync Server 2013. Portanto, o servidor de mediação precisa manipular interações de largura de banda em nome de seu peer de gateway. Sempre que possível, o servidor de mediação reservará largura de banda antecipadamente. Se isso não for possível (por exemplo, se a localidade do ponto de extremidade de mídia final no lado do gateway for desconhecido de uma chamada de saída para o par de gateway), a largura de banda será reservada quando a chamada for feita. Esse comportamento poderá resultar em uma inscrição em excesso de assinatura da largura de banda, mas é a única maneira de impedir anéis falsos.

O bypass de mídia e a reserva de largura de banda são mutuamente exclusivos. Se um bypass de mídia for empregado para uma chamada, o controle de admissão de chamadas não será executado para essa chamada. Presume-se que não haja links envolvidos na chamada com a largura de banda restrita. Se o controle de admissão de chamadas for usado para uma chamada específica que envolva o servidor de mediação, essa chamada não poderá empregar o bypass de mídia.

Para obter detalhes sobre o bypass de mídia ou o controle de admissão de chamadas, consulte [planejando a bypass de mídia no Lync server 2013](lync-server-2013-planning-for-media-bypass.md) ou [planejando o controle de admissão de chamadas no Lync Server 2013](lync-server-2013-planning-for-call-admission-control.md) na documentação de planejamento.

</div>

<span> </span>

</div>

</div>

</div>

