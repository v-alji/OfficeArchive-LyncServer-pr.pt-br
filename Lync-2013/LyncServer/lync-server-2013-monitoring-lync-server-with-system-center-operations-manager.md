---
title: 'Lync Server 2013: monitorando o Lync Server com o System Center Operations Manager'
description: 'Lync Server 2013: monitorando o Lync Server com o System Center Operations Manager.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring Lync 2013 with SCOM
ms:assetid: a74bde92-97ff-4d90-acb9-7a70272f0f31
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720343(v=OCS.15)
ms:contentKeyID: 63969636
ms.date: 05/06/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2ad93c47ab8d157b1e18b4bccc5094408f3d68ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425406"
---
# <a name="monitoring-lync-server-2013-with-system-center-operations-manager"></a><span data-ttu-id="c9f22-103">Monitorar o Lync Server 2013 com o System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="c9f22-103">Monitoring Lync Server 2013 with System Center Operations Manager</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c9f22-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c9f22-104">

<span> </span></span></span>

<span data-ttu-id="c9f22-105">_**Tópico da última modificação:** 2015-05-06_</span><span class="sxs-lookup"><span data-stu-id="c9f22-105">_**Topic Last Modified:** 2015-05-06_</span></span>

<span data-ttu-id="c9f22-106">O pacote de gerenciamento do Lync Server (MP) é a solução de monitoramento preferida para monitorar qualquer implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c9f22-106">The Lync Server Management Pack (MP) is your monitoring solution of choice for monitoring any Lync Server deployment.</span></span>

<span data-ttu-id="c9f22-107">O MP implementa a instrumentação de log de eventos e a instrumentação baseada em contador de desempenho e permite a instrumentação recentemente disponível no Lync Server, como eventos de par (falha/sucesso) para vários indicadores de integridade importantes e também implementa completamente as novas transações sintéticas (cmdlets do Windows PowerShell de teste-cs \* ).</span><span class="sxs-lookup"><span data-stu-id="c9f22-107">The MP implements traditional Event Log and Performance counter-based instrumentation and enables newly available instrumentation in Lync Server, such as pair events (failure/success) for several Key Health Indicators, and also fully implements the new Synthetic Transactions (Test-Cs\* Windows PowerShell cmdlets).</span></span>

<span data-ttu-id="c9f22-108">Você pode encontrar o pacote de gerenciamento do Lync Server 2013 e a documentação correspondente em [https://go.microsoft.com/fwlink/p/?LinkId=400468](https://go.microsoft.com/fwlink/p/?linkid=400468) .</span><span class="sxs-lookup"><span data-stu-id="c9f22-108">You can find the Lync Server 2013 Management Pack and its related documentation at [https://go.microsoft.com/fwlink/p/?LinkId=400468](https://go.microsoft.com/fwlink/p/?linkid=400468).</span></span> <span data-ttu-id="c9f22-109">Isso é recomendado se você estiver executando o System Center Operations Manager 2012.</span><span class="sxs-lookup"><span data-stu-id="c9f22-109">This is recommended if you are running System Center Operations Manager 2012.</span></span>

<span data-ttu-id="c9f22-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c9f22-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

