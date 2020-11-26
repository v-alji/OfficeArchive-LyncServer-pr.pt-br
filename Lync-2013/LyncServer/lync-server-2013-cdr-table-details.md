---
title: 'Lync Server 2013: Detalhes da tabela CDR'
description: 'Lync Server 2013: detalhes da tabela CDR.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: CDR table details
ms:assetid: 896198f5-672b-48ea-852f-0211c0c90857
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398693(v=OCS.15)
ms:contentKeyID: 48184730
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 331a3dfd4ffccac2ac4a442eeb9ad9171defb41c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435478"
---
# <a name="cdr-table-details-in-lync-server-2013"></a><span data-ttu-id="2311a-103">Detalhes da tabela CDR no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-103">CDR table details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2311a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2311a-104">

<span> </span></span></span>

<span data-ttu-id="2311a-105">_**Tópico da última modificação:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="2311a-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="2311a-106">Os tópicos a seguir detalham as colunas em cada tabela de esquema de banco de dados de registros de detalhes de chamadas (CDR).</span><span class="sxs-lookup"><span data-stu-id="2311a-106">The following topics detail the columns in each of the call detail records (CDR) database schema tables.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2311a-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="2311a-107">In This Section</span></span>

  - [<span data-ttu-id="2311a-108">Tabela de aplicativos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-108">Application table in Lync Server 2013</span></span>](lync-server-2013-application-table.md)

  - [<span data-ttu-id="2311a-109">Tabela CallPriorities no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-109">CallPriorities table in Lync Server 2013</span></span>](lync-server-2013-callpriorities-table.md)

  - [<span data-ttu-id="2311a-110">Tabela CallType no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-110">CallType table in Lync Server 2013</span></span>](lync-server-2013-calltype-table.md)

  - [<span data-ttu-id="2311a-111">Tabela ClientVersions no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-111">ClientVersions table in Lync Server 2013</span></span>](lync-server-2013-clientversions-table.md)

  - [<span data-ttu-id="2311a-112">Tabela ConferenceJoinTimeThresholds no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-112">ConferenceJoinTimeThresholds table in Lync Server 2013</span></span>](lync-server-2013-conferencejointimethresholds-table.md)

  - [<span data-ttu-id="2311a-113">Tabela ConferenceMessageCount no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-113">ConferenceMessageCount table in Lync Server 2013</span></span>](lync-server-2013-conferencemessagecount-table.md)

  - [<span data-ttu-id="2311a-114">Tabela Conferences no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-114">Conferences table in Lync Server 2013</span></span>](lync-server-2013-conferences-table.md)

  - [<span data-ttu-id="2311a-115">Tabela ConferenceSessionDetails no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-115">ConferenceSessionDetails table in Lync Server 2013</span></span>](lync-server-2013-conferencesessiondetails-table.md)

  - [<span data-ttu-id="2311a-116">Tabela ConferenceUris no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-116">ConferenceUris table in Lync Server 2013</span></span>](lync-server-2013-conferenceuris-table.md)

  - [<span data-ttu-id="2311a-117">Tabela ContentTypes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-117">ContentTypes table in Lync Server 2013</span></span>](lync-server-2013-contenttypes-table.md)

  - [<span data-ttu-id="2311a-118">Tabela DeRegisterType no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-118">DeRegisterType table in Lync Server 2013</span></span>](lync-server-2013-deregistertype-table.md)

  - [<span data-ttu-id="2311a-119">Tabela Devices no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-119">Devices table in Lync Server 2013</span></span>](lync-server-2013-devices-table.md)

  - [<span data-ttu-id="2311a-120">Tabela Dialogs no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-120">Dialogs table in Lync Server 2013</span></span>](lync-server-2013-dialogs-table.md)

  - [<span data-ttu-id="2311a-121">Tabela EdgeServers no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-121">EdgeServers table in Lync Server 2013</span></span>](lync-server-2013-edgeservers-table.md)

  - [<span data-ttu-id="2311a-122">Tabela ErrorCategory no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-122">ErrorCategory table in Lync Server 2013</span></span>](lync-server-2013-errorcategory-table.md)

  - [<span data-ttu-id="2311a-123">Tabela ErrorDef no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-123">ErrorDef table in Lync Server 2013</span></span>](lync-server-2013-errordef-table.md)

  - [<span data-ttu-id="2311a-124">Tabela ErrorReport no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-124">ErrorReport table in Lync Server 2013</span></span>](lync-server-2013-errorreport-table.md)

  - [<span data-ttu-id="2311a-125">Tabela FileTransfers no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-125">FileTransfers table in Lync Server 2013</span></span>](lync-server-2013-filetransfers-table.md)

  - [<span data-ttu-id="2311a-126">Tabela FocusJoinsAndLeaves no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-126">FocusJoinsAndLeaves table in Lync Server 2013</span></span>](lync-server-2013-focusjoinsandleaves-table.md)

  - [<span data-ttu-id="2311a-127">Tabela de front-end no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-127">FrontEnd table in Lync Server 2013</span></span>](lync-server-2013-frontend-table.md)

  - [<span data-ttu-id="2311a-128">Tabela Gateways no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-128">Gateways table in Lync Server 2013</span></span>](lync-server-2013-gateways-table.md)

  - [<span data-ttu-id="2311a-129">Tabela HardwareVersions no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-129">HardwareVersions table in Lync Server 2013</span></span>](lync-server-2013-hardwareversions-table.md)

  - [<span data-ttu-id="2311a-130">Tabela IMReportSummary no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-130">IMReportSummary table in Lync Server 2013</span></span>](lync-server-2013-imreportsummary-table.md)

  - [<span data-ttu-id="2311a-131">Tabela Locations no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-131">Locations table in Lync Server 2013</span></span>](lync-server-2013-locations-table.md)

  - [<span data-ttu-id="2311a-132">Tabela Manufacturers no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-132">Manufacturers table in Lync Server 2013</span></span>](lync-server-2013-manufacturers-table.md)

  - [<span data-ttu-id="2311a-133">Tabela McuJoinsAndLeaves no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-133">McuJoinsAndLeaves table in Lync Server 2013</span></span>](lync-server-2013-mcujoinsandleaves-table.md)

  - [<span data-ttu-id="2311a-134">Tabela Mcus no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-134">Mcus table in Lync Server 2013</span></span>](lync-server-2013-mcus-table.md)

  - [<span data-ttu-id="2311a-135">Tabela Media no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-135">Media table in Lync Server 2013</span></span>](lync-server-2013-media-table.md)

  - [<span data-ttu-id="2311a-136">Tabela MediaList no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-136">MediaList table in Lync Server 2013</span></span>](lync-server-2013-medialist-table.md)

  - [<span data-ttu-id="2311a-137">Tabela MediationServers no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-137">MediationServers table in Lync Server 2013</span></span>](lync-server-2013-mediationservers-table.md)

  - [<span data-ttu-id="2311a-138">Tabela MSMQProcessing no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-138">MSMQProcessing table in Lync Server 2013</span></span>](lync-server-2013-msmqprocessing-table.md)

  - [<span data-ttu-id="2311a-139">Tabela Phones no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-139">Phones table in Lync Server 2013</span></span>](lync-server-2013-phones-table.md)

  - [<span data-ttu-id="2311a-140">Tabela Pools no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-140">Pools table in Lync Server 2013</span></span>](lync-server-2013-pools-table.md)

  - [<span data-ttu-id="2311a-141">Tabela ProgressReport no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-141">ProgressReport table in Lync Server 2013</span></span>](lync-server-2013-progressreport-table.md)

  - [<span data-ttu-id="2311a-142">Tabela PurgeSettings no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-142">PurgeSettings table in Lync Server 2013</span></span>](lync-server-2013-purgesettings-table.md)

  - [<span data-ttu-id="2311a-143">Tabela de registro no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-143">Registration table in Lync Server 2013</span></span>](lync-server-2013-registration-table.md)

  - [<span data-ttu-id="2311a-144">Tabela Roles no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-144">Roles table in Lync Server 2013</span></span>](lync-server-2013-roles-table.md)

  - [<span data-ttu-id="2311a-145">Tabela de servidores no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-145">Servers table in Lync Server 2013</span></span>](lync-server-2013-servers-table.md)

  - [<span data-ttu-id="2311a-146">Tabela SessionDetails no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-146">SessionDetails table in Lync Server 2013</span></span>](lync-server-2013-sessiondetails-table.md)

  - [<span data-ttu-id="2311a-147">Tabela SIPResponseMetaData no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-147">SIPResponseMetaData table in Lync Server 2013</span></span>](lync-server-2013-sipresponsemetadata-table.md)

  - [<span data-ttu-id="2311a-148">Tabela sindicadores no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-148">Syndicators table in Lync Server 2013</span></span>](lync-server-2013-syndicators-table.md)

  - [<span data-ttu-id="2311a-149">Tabela SyndicatorsTenantMap no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-149">SyndicatorsTenantMap table in Lync Server 2013</span></span>](lync-server-2013-syndicatorstenantmap-table.md)

  - [<span data-ttu-id="2311a-150">Tabela de tarefas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-150">Task table in Lync Server 2013</span></span>](lync-server-2013-task-table.md)

  - [<span data-ttu-id="2311a-151">Tabela Tenants no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-151">Tenants table in Lync Server 2013</span></span>](lync-server-2013-tenants-table.md)

  - [<span data-ttu-id="2311a-152">Tabela UriTypes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-152">UriTypes table in Lync Server 2013</span></span>](lync-server-2013-uritypes-table.md)

  - [<span data-ttu-id="2311a-153">Tabela Users no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-153">Users table in Lync Server 2013</span></span>](lync-server-2013-users-table.md)

  - [<span data-ttu-id="2311a-154">Tabela UserAgentDef no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-154">UserAgentDef table in Lync Server 2013</span></span>](lync-server-2013-useragentdef-table.md)

  - [<span data-ttu-id="2311a-155">Tabela userstatistics no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-155">UserStatistics table in Lync Server 2013</span></span>](lync-server-2013-userstatistics-table.md)

  - [<span data-ttu-id="2311a-156">Tabela VoipDetails no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2311a-156">VoipDetails table in Lync Server 2013</span></span>](lync-server-2013-voipdetails-table.md)

<span data-ttu-id="2311a-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2311a-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

