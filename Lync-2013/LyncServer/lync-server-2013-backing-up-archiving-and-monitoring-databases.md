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
# <a name="backing-up-archiving-and-monitoring-databases-in-lync-server-2013"></a><span data-ttu-id="9dc06-103">Fazer backup do arquivamento e do monitoramento de bancos de dados no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9dc06-103">Backing up Archiving and Monitoring databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9dc06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9dc06-104">

<span> </span></span></span>

<span data-ttu-id="9dc06-105">_**Tópico da última modificação:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="9dc06-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="9dc06-106">Se você implantou o arquivamento ou o monitoramento, é preciso fazer backup desses bancos de dados de acordo com a política de backup do SQL Server da sua organização.</span><span class="sxs-lookup"><span data-stu-id="9dc06-106">If you deployed Archiving or Monitoring, you need to back up these databases according to your organization's SQL Server backup policy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9dc06-107">As configurações de arquivamento e monitoramento são armazenadas em backup quando você fizer backup do repositório de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="9dc06-107">The settings for Archiving and Monitoring are backed up when you back up the Central Management store.</span></span> <span data-ttu-id="9dc06-108">Para obter detalhes, consulte <A href="lync-server-2013-backing-up-core-data-and-settings.md">fazendo backup de dados principais e configurações no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9dc06-108">For details, see <A href="lync-server-2013-backing-up-core-data-and-settings.md">Backing up core data and settings in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="9dc06-109">Para arquivamento e monitoramento, você pode usar uma ferramenta do SQL Server como o SQL Server Management Studio para executar um backup manual ou pode usar as ferramentas de gerenciamento do SQL Server para agendar backups automáticos regulares.</span><span class="sxs-lookup"><span data-stu-id="9dc06-109">For Archiving and Monitoring, you can use a SQL Server tool such as SQL Server Management Studio to perform a manual backup, or you can use SQL Server management tools to schedule regular, automatic backups.</span></span>

<span data-ttu-id="9dc06-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9dc06-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

