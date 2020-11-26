---
title: 'Lync Server 2013: Protegendo dados em trânsito – bancos de dados do servidor de conformidade de arquivamento, monitoramento, chat em grupo'
description: 'Lync Server 2013: protegendo dados em trânsito – arquivamento, monitoramento, bancos de dados de servidor de conformidade de chat em grupo.'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Protecting data in transit – archiving, monitoring, group chat compliance server databases in Lync Server 2013
ms:assetid: ea219705-1015-43a7-890b-e7e67b451e7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518336(v=OCS.15)
ms:contentKeyID: 62625494
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: d4d4127bb0404bca376da450d0b0c58cf3b76560
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436843"
---
# <a name="protecting-data-in-transit--archiving-monitoring-group-chat-compliance-server-databases-in-lync-server-2013"></a><span data-ttu-id="0ecbf-103">Protegendo dados em trânsito – bancos de dados do servidor de conformidade de arquivamento, monitoramento, chat em grupo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ecbf-103">Protecting data in transit – archiving, monitoring, group chat compliance server databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ecbf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ecbf-104">

<span> </span></span></span>

<span data-ttu-id="0ecbf-105">_**Tópico da última modificação:** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="0ecbf-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="0ecbf-106">Servidor de arquivamento e monitoração do Microsoft Lync Server 2013 use o serviço de enfileiramento de mensagens (também conhecido como MSMQ) para coletar e mover mensagens de dados de forma confiável do ponto de coleta para os servidores do repositório.</span><span class="sxs-lookup"><span data-stu-id="0ecbf-106">Microsoft Lync Server 2013 Archiving Server and Monitoring Server both use the Message Queuing (also known as MSMQ) service to collect and reliably move data messages from the collection point to the repository servers.</span></span> <span data-ttu-id="0ecbf-107">O serviço de conformidade coleta dados em conjunto com o servidor de chat em grupo, que também usa o enfileiramento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0ecbf-107">Compliance service collects data in conjunction with the Group Chat Server, which also uses Message Queuing.</span></span>

<span data-ttu-id="0ecbf-108">No Lync Server 2013, não há proteção interna para dados no cabo; no entanto, se houver uma exigência para proteger esse tráfego, o serviço de enfileiramento de mensagens pode fornecer criptografia em um nível de mensagem na fila de mensagens de envio.</span><span class="sxs-lookup"><span data-stu-id="0ecbf-108">In Lync Server 2013, there is no internal protection for data on the wire; however, if there is a requirement to secure this traffic, the Message Queuing service can provide encryption at a message level on the sending message queue.</span></span> <span data-ttu-id="0ecbf-109">Isso é feito usando certificados que são gerenciados pelos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0ecbf-109">This is accomplished using certificates that are managed by the Active Directory Domain Services.</span></span> <span data-ttu-id="0ecbf-110">Para obter detalhes, consulte Apêndice D: Enfileiramento de mensagens e comunicação pela Internet no Windows Server 2008 em [https://go.microsoft.com/fwlink/p/?LinkId=145238](https://go.microsoft.com/fwlink/p/?linkid=145238) ou Apêndice I: Enfileiramento de mensagens e comunicação pela Internet no Windows server 2008 R2 no [https://go.microsoft.com/fwlink/p/?LinkId=211883](https://go.microsoft.com/fwlink/p/?linkid=211883) windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="0ecbf-110">For details, see Appendix D: Message Queuing and Internet Communication in Windows Server 2008 at [https://go.microsoft.com/fwlink/p/?LinkId=145238](https://go.microsoft.com/fwlink/p/?linkid=145238) or Appendix I: Message Queuing and Internet Communication in Windows Server 2008 R2 at [https://go.microsoft.com/fwlink/p/?LinkId=211883](https://go.microsoft.com/fwlink/p/?linkid=211883) for Windows Server 2008 R2.</span></span>

<span data-ttu-id="0ecbf-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ecbf-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

