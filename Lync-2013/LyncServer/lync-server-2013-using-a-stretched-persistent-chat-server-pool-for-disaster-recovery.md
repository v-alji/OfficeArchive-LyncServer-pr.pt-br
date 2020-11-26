---
title: Usando o pool estendido de Chat Persistente Chat para recuperação de desastre
description: Usar um pool ampliado de servidor de chat persistente para recuperação de desastres.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using a stretched Persistent Chat Server pool for disaster recovery
ms:assetid: 74c5287e-d70d-490a-9adc-ab419917ddd9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205007(v=OCS.15)
ms:contentKeyID: 48184506
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b83a7226f7b9a49a2676b6222505f53247bd5abf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436087"
---
# <a name="using-a-stretched-persistent-chat-server-pool-for-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="bbe7a-103">Usando o pool estendido de Chat Persistente Chat para recuperação de desastre no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bbe7a-103">Using a stretched Persistent Chat Server pool for disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bbe7a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bbe7a-104">

<span> </span></span></span>

<span data-ttu-id="bbe7a-105">_**Tópico da última modificação:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="bbe7a-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="bbe7a-106">A solução de recuperação de desastres para o servidor de chat persistente baseia-se em um pool de servidores de chat persistentes ampliado.</span><span class="sxs-lookup"><span data-stu-id="bbe7a-106">The disaster recovery solution for Persistent Chat Server is built on a stretched Persistent Chat Server pool.</span></span> <span data-ttu-id="bbe7a-107">Isso é semelhante à resiliência de site metropolitana no Lync Server 2010; no entanto, não há nenhuma exigência para uma VLAN (rede local virtual) ampliada.</span><span class="sxs-lookup"><span data-stu-id="bbe7a-107">This is similar to metropolitan site resiliency in Lync Server 2010; however, there is no requirement for a stretched virtual local area network (VLAN).</span></span> <span data-ttu-id="bbe7a-108">Ao esticar um pool de servidores de chat persistente, você essencialmente configura um pool na topologia logicamente, mas coloca fisicamente os servidores no pool em dois data centers diferentes.</span><span class="sxs-lookup"><span data-stu-id="bbe7a-108">By stretching Persistent Chat Server pool, you essentially configure one pool in the topology logically, but you physically place the servers in the pool in two different data centers.</span></span> <span data-ttu-id="bbe7a-109">Configure o espelhamento do SQL Server para o banco de dados da mesma maneira e implante o banco de dados e o espelho no mesmo Data Center.</span><span class="sxs-lookup"><span data-stu-id="bbe7a-109">Configure SQL Server mirroring for the database in the same way, and deploy the database and the mirror in the same data center.</span></span> <span data-ttu-id="bbe7a-110">Você deve configurar um banco de dados de backup no data center secundário (com um espelho opcional para fornecer alta disponibilidade durante a recuperação de desastre).</span><span class="sxs-lookup"><span data-stu-id="bbe7a-110">You need to configure a backup database in the secondary data center (with an optional mirror to provide high availability during disaster recovery).</span></span> <span data-ttu-id="bbe7a-111">Esse é o banco de dados de backup usado para failover durante a recuperação de desastre.</span><span class="sxs-lookup"><span data-stu-id="bbe7a-111">This is the backup database used for failover during disaster recovery.</span></span>

<span data-ttu-id="bbe7a-112">Para obter detalhes sobre como configurar o espelhamento do SQL Server para alta disponibilidade, consulte [espelhamento do SQL Server no Lync Server 2013](lync-server-2013-sql-server-mirroring.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7a-112">For details about how to configure SQL Server mirroring for high availability, see [SQL Server mirroring in Lync Server 2013](lync-server-2013-sql-server-mirroring.md).</span></span> <span data-ttu-id="bbe7a-113">Para obter detalhes sobre como falhar sobre o banco de dados para recuperação de desastre, consulte [Configurando o envio de log do SQL Server no Lync Server 2013 para o banco de dados do servidor de chat persistente](lync-server-2013-setting-up-sql-server-log-shipping-for-the-persistent-chat-server-primary-database.md) e [Configurando o envio de log do SQL Server entre o espelho primário e o banco de dados secundário de envio de logs no Lync Server 2013](lync-server-2013-set-up-log-shipping-secondary-database.md)</span><span class="sxs-lookup"><span data-stu-id="bbe7a-113">For details about failing over the database for disaster recovery, see [Setting up SQL Server Log Shipping in Lync Server 2013 for the Persistent Chat Server primary database](lync-server-2013-setting-up-sql-server-log-shipping-for-the-persistent-chat-server-primary-database.md) and [Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database in Lync Server 2013](lync-server-2013-set-up-log-shipping-secondary-database.md).</span></span>

<span data-ttu-id="bbe7a-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bbe7a-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

