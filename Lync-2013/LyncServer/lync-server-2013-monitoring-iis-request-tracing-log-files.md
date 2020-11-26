---
title: 'Lync Server 2013: monitorar arquivos de log de rastreamento de solicitação do IIS'
description: 'Lync Server 2013: monitorar arquivos de log de rastreamento de solicitação do IIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring IIS request tracing log files
ms:assetid: b6730e92-6d74-4fa7-a83f-50b7bdadbffa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690034(v=OCS.15)
ms:contentKeyID: 48185215
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 09692b79b1cc59ad18ad520885c0a795736b53cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425413"
---
# <a name="monitoring-iis-request-tracing-log-files-in-lync-server-2013"></a><span data-ttu-id="b2a70-103">Monitorar arquivos de log de rastreamento de solicitação do IIS no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b2a70-103">Monitoring IIS request tracing log files in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b2a70-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b2a70-104">

<span> </span></span></span>

<span data-ttu-id="b2a70-105">_**Tópico da última modificação:** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="b2a70-105">_**Topic Last Modified:** 2013-02-14_</span></span>

    This topic applies to deployments supporting Lync 2010 Lync Mobile clients only, and is intended for the Mobility Service (Mcx).

<span data-ttu-id="b2a70-106">Quando você habilita o rastreamento de solicitação dos serviços de informações da Internet (IIS) para o serviço de mobilidade do Lync Server (MCX), os arquivos de log gerados podem consumir até três gigabytes de espaço em disco por dia.</span><span class="sxs-lookup"><span data-stu-id="b2a70-106">When you enable Internet Information Services (IIS) request tracing for the Lync Server Mobility Service (Mcx), the log files that are generated can consume up to three gigabytes of disk space per day.</span></span> <span data-ttu-id="b2a70-107">O registro em log do rastreamento IIS está habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="b2a70-107">IIS trace logging is enabled by default.</span></span> <span data-ttu-id="b2a70-108">Você deve monitorar os servidores de front-end para ter certeza de que eles não ficam sem espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="b2a70-108">You should monitor the Front End Servers to make sure that they do not run out of disk space.</span></span>

<span data-ttu-id="b2a70-109">Por padrão, o IIS armazena os arquivos de log em% SystemDrive% Inetpub registra arquivos de log \\ \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="b2a70-109">By default, IIS stores the log files at %SystemDrive%\\inetpub\\logs\\LogFiles.</span></span>

<span data-ttu-id="b2a70-110">Para desativar o rastreamento de solicitação IIS para todo um servidor, na linha de comando, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b2a70-110">To turn off IIS request tracing for an entire server, at the command line, type the following:</span></span>

    %SystemDrive%\Windows\System32\inetsrv\appcmd set config /section:httpLogging /dontLog:True

<span data-ttu-id="b2a70-111">Para obter detalhes sobre o comando **httpLogging** , consulte [https://go.microsoft.com/fwlink/p/?linkId=234927](https://go.microsoft.com/fwlink/p/?linkid=234927) .</span><span class="sxs-lookup"><span data-stu-id="b2a70-111">For details about the **httpLogging** command, see [https://go.microsoft.com/fwlink/p/?linkId=234927](https://go.microsoft.com/fwlink/p/?linkid=234927).</span></span>

<span data-ttu-id="b2a70-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b2a70-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

