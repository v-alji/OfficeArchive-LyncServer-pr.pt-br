---
title: Configurando o Servidor de Chat Persistente para alta disponibilidade e recuperação de desastre
description: Configurando o servidor de chat persistente para alta disponibilidade e recuperação de desastres.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Persistent Chat Server for high availability and disaster recovery
ms:assetid: eebc581c-e3a0-4b69-8a43-80b607b4d8f2
ms:mtpsurl: https://technet.microsoft.com/library/JJ205364(v=OCS.15)
ms:contentKeyID: 48185760
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 13935f2ec690deb7f896c13d185680ce1122a892
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432783"
---
# <a name="configuring-persistent-chat-server-for-high-availability-and-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="a7ec1-103">Configurando o Servidor de Chat Persistente para alta disponibilidade e recuperação de desastre no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a7ec1-103">Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a7ec1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a7ec1-104">

<span> </span></span></span>

<span data-ttu-id="a7ec1-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="a7ec1-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="a7ec1-106">Os serviços de servidor de chat persistente do Lync Server 2013 usam uma configuração de *pool ampliado* para recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="a7ec1-106">The Lync Server 2013, Persistent Chat Server services use a *stretched pool* configuration for disaster recovery.</span></span> <span data-ttu-id="a7ec1-107">Um pool ampliado é um pool que tem computadores distribuídos entre dois centros de dados físicos, mas está dentro de um único site lógico do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a7ec1-107">A stretched pool is a pool that has computers that are distributed between two physical data centers, but are within a single logical Lync Server site.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a7ec1-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a7ec1-108">In This Section</span></span>

  - [<span data-ttu-id="a7ec1-109">Recursos obrigatórios para Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a7ec1-109">Required resources for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-required-resources-for-persistent-chat-server.md)

  - [<span data-ttu-id="a7ec1-110">Usando o Construtor de Topologia para configurar alta disponibilidade e recuperação de desastre no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a7ec1-110">Using Topology Builder to configure high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-using-topology-builder-to-configure-high-availability-and-disaster-recovery.md)

  - [<span data-ttu-id="a7ec1-111">Usando o pool estendido de Chat Persistente Chat para recuperação de desastre no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a7ec1-111">Using a stretched Persistent Chat Server pool for disaster recovery in Lync Server 2013</span></span>](lync-server-2013-using-a-stretched-persistent-chat-server-pool-for-disaster-recovery.md)

  - [<span data-ttu-id="a7ec1-112">Espelhamento de SQL Server no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a7ec1-112">SQL Server mirroring in Lync Server 2013</span></span>](lync-server-2013-sql-server-mirroring.md)

  - [<span data-ttu-id="a7ec1-113">Configurando o envio de logs do SQL Server no Lync Server 2013 ao banco de dados primário do servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="a7ec1-113">Setting up SQL Server Log Shipping in Lync Server 2013 for the Persistent Chat Server primary database</span></span>](lync-server-2013-setting-up-sql-server-log-shipping-for-the-persistent-chat-server-primary-database.md)

  - [<span data-ttu-id="a7ec1-114">Configuração do Envio de Logs do Servidor SQL entre o espelho primário e o banco de dados secundário de Envio de Logs no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a7ec1-114">Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database in Lync Server 2013</span></span>](lync-server-2013-set-up-log-shipping-secondary-database.md)

<span data-ttu-id="a7ec1-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a7ec1-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

