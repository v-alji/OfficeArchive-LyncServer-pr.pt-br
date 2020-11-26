---
title: 'Lync Server 2013: Novos recursos de recuperação de desastre e alta disponibilidade'
description: 'Lync Server 2013: novos recursos de recuperação de desastres e alta disponibilidade.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New disaster recovery and high availability features
ms:assetid: 4fa7cd0f-784b-4d3f-b839-432c2ecaf7c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204892(v=OCS.15)
ms:contentKeyID: 48184130
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92816f61b66d9eed76c16286aaa6c7392dca7708
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425106"
---
# <a name="new-disaster-recovery-and-high-availability-features-in-lync-server-2013"></a>Novos recursos de recuperação de desastre e alta disponibilidade no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-20_

Como no Lync Server 2010, o principal esquema de alta disponibilidade (HA) do Lync Server 2013 é baseado na redundância do servidor via pool. Se um servidor que executa determinada função falhar, os demais servidores do pool que executam a mesma função assumirão a carga desse servidor. Isso se aplica a Servidores Front-End, Servidores de Borda, Servidores de Mediação e Diretores.

O Lync Server 2013 adiciona novas medidas de recuperação de desastres permitindo que você emparelhe pools de front-end localizados em dois datacenters. Se um dos pools emparelhados ficar inativo, um administrador poderá fazer failover dos usuários desse pool para o outro pool do par, para dar continuidade ao serviço. Essa funcionalidade não requer soluções caras de rede ou hardware, como redes de armazenamento ou discos compartilhados.

O Lync Server 2013 também adiciona alta disponibilidade do servidor back-end. Esta é uma topologia opcional na qual você implanta dois servidores back-end para um pool de front-end e configura o espelhamento do SQL síncrono para todos os bancos de dados do Lync em execução nos servidores de back-end. Você pode escolher se deseja implantar uma testemunha para o espelho.

<div>

## <a name="see-also"></a>Confira também


[Planejamento para alta disponibilidade e recuperação de desastre no Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

