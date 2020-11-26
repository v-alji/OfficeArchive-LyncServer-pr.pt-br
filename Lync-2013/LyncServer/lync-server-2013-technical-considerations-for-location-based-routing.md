---
title: 'Lync Server 2013: Considerações técnicas para Roteamento Baseado em Local'
description: 'Lync Server 2013: considerações técnicas para roteamento de Location-Based.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical considerations for Location-Based Routing
ms:assetid: 2e2a9199-7c6f-48d3-9adb-3873fc4f8c4e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994027(v=OCS.15)
ms:contentKeyID: 51803936
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54a025af81ab148ad41f95d0a8cf4f900beb7e00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423425"
---
# <a name="technical-considerations-for-location-based-routing-in-lync-server-2013"></a>Considerações técnicas para Roteamento Baseado em Local no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-03-09_

Ao planejar Location-Based roteamento, considere o impacto para os cenários a seguir.

<div>

## <a name="disaster-recovery"></a>Recuperação de desastres

Durante um failover do pool primário para um pool de backup e também durante a restauração de operações normais para o pool primário, Location-Based roteamento permanece em vigor a qualquer momento durante um desastre e procedimento de recuperação.

</div>

<div>

## <a name="survivable-branch-appliance"></a>Aparelho de Filial Persistente

A configuração do roteamento de Location-Based afeta o planejamento de onde você implanta os gateways associados a seus aparelhos de ramificação sobreviventes. O gateway associado a seu SBA deve estar localizado no mesmo site de rede que o seu aparelho de ramificação sobreviventes; caso contrário, os usuários hospedados em seu aparelho de ramificação sobreviventes não terão permissão para fazer chamadas de saída se Location-Based roteamento estiver configurado. Quando a conexão de WAN entre seu aparelho de ramificação sobreviventes e o site central está inoperante, Location-Based restrições de roteamento permanecem impostas.

</div>

<div>

## <a name="see-also"></a>Confira também


[Planejamento de Roteamento Baseado em Local no Lync Server 2013](lync-server-2013-planning-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

