---
title: 'Lync Server 2013: Planejamento de monitoramento'
description: 'Lync Server 2013: planejando para monitoramento.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for monitoring
ms:assetid: 26cead5a-183c-42f1-a4b0-0e8d61c6159d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204752(v=OCS.15)
ms:contentKeyID: 48183671
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f8ee78f06423bc167e26455d399ce2dd16f24262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442926"
---
# <a name="planning-for-monitoring-in-lync-server-2013"></a><span data-ttu-id="645ff-103">Planejamento de monitoramento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="645ff-103">Planning for monitoring in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="645ff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="645ff-104">

<span> </span></span></span>

<span data-ttu-id="645ff-105">_**Tópico da última modificação:** 2012-09-05_</span><span class="sxs-lookup"><span data-stu-id="645ff-105">_**Topic Last Modified:** 2012-09-05_</span></span>

<span data-ttu-id="645ff-106">O serviço de monitoramento no Microsoft Lync Server 2013 fornece uma maneira para os administradores coletarem o uso, a tendência e os dados de qualidade de serviço para as sessões de comunicação que ocorrem na organização.</span><span class="sxs-lookup"><span data-stu-id="645ff-106">The monitoring service in Microsoft Lync Server 2013 provides a way for administrators to collect usage, trend, and quality of service data for the communication sessions that take place in their organization.</span></span> <span data-ttu-id="645ff-107">O monitoramento no Lync Server 2013 não requer mais uma função de servidor separada; em vez disso, o serviço de monitoramento é integrado a cada servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="645ff-107">Monitoring in Lync Server 2013 no longer requires a separate server role; instead, the monitoring service is built into each Front End server.</span></span> <span data-ttu-id="645ff-108">No entanto, por padrão, o monitoramento não está habilitado no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="645ff-108">However, by default monitoring is not enabled in Lync Server 2013.</span></span> <span data-ttu-id="645ff-109">Este documento ajudará você a determinar se o monitoramento deve ou não ser habilitado em sua organização.</span><span class="sxs-lookup"><span data-stu-id="645ff-109">This document will help you determine whether or not monitoring should be enabled in your organization.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="645ff-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="645ff-110">In This Section</span></span>

  - [<span data-ttu-id="645ff-111">Visão geral do monitoramento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="645ff-111">Overview of monitoring in Lync Server 2013</span></span>](lync-server-2013-overview-of-monitoring.md)

  - [<span data-ttu-id="645ff-112">Definindo seus requisitos de monitoramento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="645ff-112">Defining your requirements for monitoring in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-monitoring.md)

  - [<span data-ttu-id="645ff-113">Habilitando o monitoramento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="645ff-113">Enabling monitoring in Lync Server 2013</span></span>](lync-server-2013-enabling-monitoring.md)

  - [<span data-ttu-id="645ff-114">Acessando os dados de monitoramento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="645ff-114">Accessing monitoring data in Lync Server 2013</span></span>](lync-server-2013-accessing-monitoring-data.md)

  - [<span data-ttu-id="645ff-115">Componentes e topologia para monitoramento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="645ff-115">Components and topologies for monitoring in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-monitoring.md)

  - [<span data-ttu-id="645ff-116">Lista de verificação de implantação para monitoramento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="645ff-116">Deployment checklist for monitoring in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-monitoring.md)

<span data-ttu-id="645ff-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="645ff-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

