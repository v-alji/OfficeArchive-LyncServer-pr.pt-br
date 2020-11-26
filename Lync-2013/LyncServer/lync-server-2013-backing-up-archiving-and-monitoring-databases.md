---
title: 'Lync Server 2013: fazendo backup do arquivamento e monitoramento de bancos de dados'
description: 'Lync Server 2013: fazendo backup do arquivamento e monitoramento de bancos de dados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up Archiving and Monitoring databases
ms:assetid: c120db81-b02c-4a4c-90cd-8aca6cff64f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202188(v=OCS.15)
ms:contentKeyID: 51541515
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 49b4fa194bffa27a52f32d61a729eeaa31cc0ad3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438117"
---
# <a name="backing-up-archiving-and-monitoring-databases-in-lync-server-2013"></a>Fazer backup do arquivamento e do monitoramento de bancos de dados no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-02-17_

Se você implantou o arquivamento ou o monitoramento, é preciso fazer backup desses bancos de dados de acordo com a política de backup do SQL Server da sua organização.

<div>


> [!NOTE]  
> As configurações de arquivamento e monitoramento são armazenadas em backup quando você fizer backup do repositório de gerenciamento central. Para obter detalhes, consulte <A href="lync-server-2013-backing-up-core-data-and-settings.md">fazendo backup de dados principais e configurações no Lync Server 2013</A>.



</div>

Para arquivamento e monitoramento, você pode usar uma ferramenta do SQL Server como o SQL Server Management Studio para executar um backup manual ou pode usar as ferramentas de gerenciamento do SQL Server para agendar backups automáticos regulares.

</div>

<span> </span>

</div>

</div>

</div>

