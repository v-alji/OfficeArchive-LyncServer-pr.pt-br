---
title: 'Lync Server 2013: monitorar o serviço de mobilidade e o uso do UCWA'
description: 'Lync Server 2013: monitorar o serviço de mobilidade e o uso do UCWA.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring Mobility Service and UCWA usage
ms:assetid: 8389b37a-ca3e-4047-8b51-85bc07da87e8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690025(v=OCS.15)
ms:contentKeyID: 48184683
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6575941faf904e46cd1f66d7226a16c88e8cbaa3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425392"
---
# <a name="monitoring-mobility-service-and-ucwa-usage-in-lync-server-2013"></a>Monitorar o serviço de mobilidade e o uso do UCWA no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-02-14_

Continuamente, você deve monitorar a CPU e a memória usadas pelo Lync Server Mobility Service (MCX) e pela API Web de comunicação unificada (UCWA). Para monitorar o uso, você pode usar uma das opções a seguir:

**Para Unified Communications Web API (UCWA):**

  - O processo de trabalho do **LyncUcwa** no Gerenciador dos serviços de informações da Internet (IIS). No painel **Processos de Trabalho**, examine as colunas (memória) **CPU %** e **Bytes Particulares (KB)**.

  - Os contadores de desempenho da **CPU** e do **Processador**.

Na maioria das implantações, o uso da CPU do UWCA deve estar abaixo de 15%, em média. O uso da memória deve ficar dentro dos limites descritos em [monitoramento para limites de capacidade de memória do servidor no Lync server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md).

Além de contadores de uso de CPU e memória, você pode usar os contadores de desempenho a seguir para ajudar a determinar quando um servidor está sobrecarregado com solicitações:

  - **Ls: Web – limitação e autenticação \\ WEB – total de solicitações em processamento**, que indica o número de solicitações de Web pendentes no servidor. Quando esse contador chegar a 10.000, as solicitações subsequentes falharão com o erro "503 - serviço indisponível".

  - **ASP.NET \\ Solicitações enfileiradas** (sempre devem ser zero).

<div>


> [!NOTE]  
> Se você atender ou ultrapassar esses valores, consulte novamente e recalcule o planejamento de capacidade para o dimensionamento correto da CPU, número de núcleos e memória para os computadores que hospedam os serviços Web.



</div>

**Para o Mobility Service (Mcx):**

  - Os processos de trabalho do **CSIntMcxAppPool** e do **CSExtMcxAppPool** no Gerenciador dos serviços de informações da Internet (IIS). No painel **Processos de Trabalho**, examine as colunas (memória) **CPU %** e **Bytes Particulares (KB)**.

  - Os contadores de desempenho da **CPU** e do **Processador**.

Na maioria das implantações o uso da CPU do Mobility Service deve estar abaixo de 15%, em média. O uso da memória deve ficar dentro dos limites descritos em [monitoramento para limites de capacidade de memória do servidor no Lync server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md).

Além de contadores de uso de CPU e memória, você pode usar os contadores de desempenho ASP.NET a seguir para ajudar a determinar quando um servidor está sobrecarregado com solicitações:

  - **ASP.NET v 2.0.50727 \\ Solicitações Current**, que indicam o número de solicitações de Web pendentes no servidor. Quando esse contador chegar a 5.000, as solicitações subsequentes falharão com o erro "503 - serviço indisponível".

  - **ASP.NET \\ Solicitações enfileiradas** (sempre devem ser zero).

<div>


> [!NOTE]  
> Se você satisfaz ou supera esses valores, deve revisitar e recalcular o planejamento da capacidade para o dimensionamento correto da CPU, número de núcleos e memória para os computadores que hospedam os serviços Web.



</div>

<div>

## <a name="see-also"></a>Confira também


[Monitorar os limites de capacidade de memória do servidor no Lync Server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

