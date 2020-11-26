---
title: 'Lync Server 2013: fazer backup e restaurar o Lync Server'
description: 'Lync Server 2013: fazendo backup e restaurando o Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up and restoring Lync Server 2013
ms:assetid: 07dc1f5e-af66-4e18-bf39-881dceff8bc3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202160(v=OCS.15)
ms:contentKeyID: 51541443
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1a7024b2264fb895d1562a6da0775f9397644b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438138"
---
# <a name="backing-up-and-restoring-lync-server-2013"></a>Fazer backup e restaurar o Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-02-21_

Nesta seção, você encontrará as práticas recomendadas para fazer backup dos dados do Lync Server 2013 e para restaurá-lo se você tiver uma falha. Estas práticas recomendadas se aplicam às seguintes situações:

  - Um pool de qualquer tipo do Lync Server inteiro (servidor front-end, servidor de borda, servidor de mediação, servidor de chat persistente ou diretor) ou um servidor individual em um desses pools.

  - O servidor de gerenciamento central

  - Um servidor Standard Edition

  - Um servidor back-end do Enterprise Edition

  - Um repositório de arquivos

  - Um banco de dados de arquivamento, banco de dados de monitoramento ou banco de dados de chat persistente

Esta seção não inclui informações sobre como restaurar um site inteiro ou para desenvolver um site em espera. Para obter detalhes sobre o desenvolvimento de uma solução de recuperação de desastres com pools front-ends emparelhados, consulte [planejando a alta disponibilidade e a recuperação de desastres no Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md). Esse é o método recomendado para planejar a recuperação de desastres.

Se você implantou pools front-end emparelhados, se um desses pools falhar e se tornar irrecuperável, você pode restaurar esse pool com um novo nome de domínio totalmente qualificado (FQDN) de seu pool emparelhado. Para obter detalhes sobre as etapas para realizar essa recuperação, consulte [falha em um pool no Lync Server 2013](lync-server-2013-failing-over-a-pool.md). Além disso, se você quiser recriar mais tarde um pool com falha e irrecuperável que fazia parte de um par de front-end, você pode usar as etapas em [executando um failover de pool de front-end da ABC no Lync Server 2013](lync-server-2013-performing-an-abc-front-end-pool-failover.md).

A metodologia descrita neste documento envolve considerações especiais durante a fase de planejamento. Para obter detalhes, consulte [estabelecendo um plano de backup e restauração para o Lync Server 2013](lync-server-2013-establishing-a-backup-and-restoration-plan.md).

<div>

## <a name="in-this-section"></a>Nesta seção

  - [Preparando para backup e restauração do Lync Server 2013](lync-server-2013-preparing-for-lync-server-backup-and-restoration.md)

  - [Fazer backup de dados e configurações no Lync Server 2013](lync-server-2013-backing-up-data-and-settings.md)

  - [Restaurando dados e configurações no Lync Server 2013](lync-server-2013-restoring-data-and-settings.md)

  - [Planilhas de backup e restauração para o Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

