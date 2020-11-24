---
title: Usando o Construtor de Topologia para configurar alta disponibilidade e recuperação de desastre
description: Usar o construtor de topologias para configurar a alta disponibilidade e a recuperação de desastres.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Topology Builder to configure high availability and disaster recovery
ms:assetid: abc1a25d-1f5e-46ef-91d2-0144fc847206
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205172(v=OCS.15)
ms:contentKeyID: 48185113
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 04764a58ac3ae1bbe0df97aadeabb03158ce8100
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390428"
---
# <a name="using-topology-builder-to-configure-high-availability-and-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="72272-103">Usando o Construtor de Topologia para configurar alta disponibilidade e recuperação de desastre no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="72272-103">Using Topology Builder to configure high availability and disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="72272-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="72272-104">

<span> </span></span></span>

<span data-ttu-id="72272-105">_**Tópico da última modificação:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="72272-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="72272-106">Execute as etapas a seguir no construtor de topologias para configurar a alta disponibilidade e a recuperação de desastres para o servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="72272-106">Perform the following steps within Topology Builder to configure high availability and disaster recovery for Persistent Chat Server.</span></span>

1.  <span data-ttu-id="72272-107">Adicione os bancos de dados espelho e os repositórios secundários do banco de dados do SQL Server de envio de log.</span><span class="sxs-lookup"><span data-stu-id="72272-107">Add the mirror databases and the log shipping secondary database SQL Server stores.</span></span>

2.  <span data-ttu-id="72272-108">Edite as propriedades do serviço do servidor de chat persistente para:</span><span class="sxs-lookup"><span data-stu-id="72272-108">Edit the Persistent Chat Server service properties to:</span></span>
    
    1.  <span data-ttu-id="72272-109">Ativar o espelhamento do banco de dados primário.</span><span class="sxs-lookup"><span data-stu-id="72272-109">Enable mirroring for the primary database.</span></span>
    
    2.  <span data-ttu-id="72272-110">Adicione a loja principal do SQL Server do espelho.</span><span class="sxs-lookup"><span data-stu-id="72272-110">Add the primary mirror SQL Server store.</span></span>
    
    3.  <span data-ttu-id="72272-111">Habilite o banco de dados de envio de log do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="72272-111">Enable the SQL Server Log Shipping database.</span></span>
    
    4.  <span data-ttu-id="72272-112">Adicione o repositório do SQL Server secundário de envio de logs do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="72272-112">Add the SQL Server Log Shipping secondary SQL Server store.</span></span>
    
    5.  <span data-ttu-id="72272-113">Adicione o espelho do SQL Server Store para o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="72272-113">Add the SQL Server store mirror for the secondary database.</span></span>
    
    6.  <span data-ttu-id="72272-114">Publique a topologia.</span><span class="sxs-lookup"><span data-stu-id="72272-114">Publish the topology.</span></span>

<span data-ttu-id="72272-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="72272-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

