---
title: 'Lync Server 2013: Detalhes da tabela do Servidor de Chat Persistente'
description: 'Lync Server 2013: detalhes da tabela do servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat Server table details
ms:assetid: c22d4a76-da50-49de-9038-e0ed7b8e1b58
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615034(v=OCS.15)
ms:contentKeyID: 48185323
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a27feaaccf861d537127f06920cf903be5ae000
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443080"
---
# <a name="persistent-chat-server-table-details-in-lync-server-2013"></a><span data-ttu-id="ab797-103">Detalhes da tabela do Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-103">Persistent Chat Server table details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab797-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab797-104">

<span> </span></span></span>

<span data-ttu-id="ab797-105">_**Tópico da última modificação:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="ab797-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="ab797-106">Os tópicos a seguir detalham as colunas em cada uma das tabelas de esquema de banco de dados de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="ab797-106">The following topics detail the columns in each of the Persistent Chat database schema tables.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ab797-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ab797-107">In This Section</span></span>

  - [<span data-ttu-id="ab797-108">tblADCookie no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-108">tblADCookie in Lync Server 2013</span></span>](lync-server-2013-tbladcookie.md)

  - [<span data-ttu-id="ab797-109">tblPrincipalMemberDifference no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-109">tblPrincipalMemberDifference in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmemberdifference.md)

  - [<span data-ttu-id="ab797-110">tblADUpdates no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-110">tblADUpdates in Lync Server 2013</span></span>](lync-server-2013-tbladupdates.md)

  - [<span data-ttu-id="ab797-111">tblPrincipalMembers no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-111">tblPrincipalMembers in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmembers.md)

  - [<span data-ttu-id="ab797-112">tblPrincipalMeta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-112">tblPrincipalMeta in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmeta.md)

  - [<span data-ttu-id="ab797-113">tblSkippedAffiliations no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-113">tblSkippedAffiliations in Lync Server 2013</span></span>](lync-server-2013-tblskippedaffiliations.md)

  - [<span data-ttu-id="ab797-114">tblPrincipalType no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-114">tblPrincipalType in Lync Server 2013</span></span>](lync-server-2013-tblprincipaltype.md)

  - [<span data-ttu-id="ab797-115">tblPrincipal no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-115">tblPrincipal in Lync Server 2013</span></span>](lync-server-2013-tblprincipal.md)

  - [<span data-ttu-id="ab797-116">tblPrincipalAffiliations no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-116">tblPrincipalAffiliations in Lync Server 2013</span></span>](lync-server-2013-tblprincipalaffiliations.md)

  - [<span data-ttu-id="ab797-117">tblNode no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-117">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)

  - [<span data-ttu-id="ab797-118">tblRoleType no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-118">tblRoleType in Lync Server 2013</span></span>](lync-server-2013-tblroletype.md)

  - [<span data-ttu-id="ab797-119">tblScopePrincipal no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-119">tblScopePrincipal in Lync Server 2013</span></span>](lync-server-2013-tblscopeprincipal.md)

  - [<span data-ttu-id="ab797-120">tblPrincipalRole no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-120">tblPrincipalRole in Lync Server 2013</span></span>](lync-server-2013-tblprincipalrole.md)

  - [<span data-ttu-id="ab797-121">tblSiopWhiteList no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-121">tblSiopWhiteList in Lync Server 2013</span></span>](lync-server-2013-tblsiopwhitelist.md)

  - [<span data-ttu-id="ab797-122">tblEnumAttribute no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-122">tblEnumAttribute in Lync Server 2013</span></span>](lync-server-2013-tblenumattribute.md)

  - [<span data-ttu-id="ab797-123">tblEnumValue no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-123">tblEnumValue in Lync Server 2013</span></span>](lync-server-2013-tblenumvalue.md)

  - [<span data-ttu-id="ab797-124">tblPrincipalInvites no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-124">tblPrincipalInvites in Lync Server 2013</span></span>](lync-server-2013-tblprincipalinvites.md)

  - [<span data-ttu-id="ab797-125">tblChat no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-125">tblChat in Lync Server 2013</span></span>](lync-server-2013-tblchat.md)

  - [<span data-ttu-id="ab797-126">tblLastInviteId no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-126">tblLastInviteId in Lync Server 2013</span></span>](lync-server-2013-tbllastinviteid.md)

  - [<span data-ttu-id="ab797-127">tblLastChatId no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-127">tblLastChatId in Lync Server 2013</span></span>](lync-server-2013-tbllastchatid.md)

  - [<span data-ttu-id="ab797-128">tblPreference no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-128">tblPreference in Lync Server 2013</span></span>](lync-server-2013-tblpreference.md)

  - [<span data-ttu-id="ab797-129">tblFileToken no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-129">tblFileToken in Lync Server 2013</span></span>](lync-server-2013-tblfiletoken.md)

  - [<span data-ttu-id="ab797-130">tblServerIdentity no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-130">tblServerIdentity in Lync Server 2013</span></span>](lync-server-2013-tblserveridentity.md)

  - [<span data-ttu-id="ab797-131">tblAdminLock no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-131">tblAdminLock in Lync Server 2013</span></span>](lync-server-2013-tbladminlock.md)

  - [<span data-ttu-id="ab797-132">tblSystemRevision no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-132">tblSystemRevision in Lync Server 2013</span></span>](lync-server-2013-tblsystemrevision.md)

  - [<span data-ttu-id="ab797-133">tblActivePeers no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-133">tblActivePeers in Lync Server 2013</span></span>](lync-server-2013-tblactivepeers.md)

  - [<span data-ttu-id="ab797-134">tblConfig no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-134">tblConfig in Lync Server 2013</span></span>](lync-server-2013-tblconfig.md)

  - [<span data-ttu-id="ab797-135">tblComplianceData no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-135">tblComplianceData in Lync Server 2013</span></span>](lync-server-2013-tblcompliancedata.md)

  - [<span data-ttu-id="ab797-136">tblComplianceFanout no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-136">tblComplianceFanout in Lync Server 2013</span></span>](lync-server-2013-tblcompliancefanout.md)

  - [<span data-ttu-id="ab797-137">tblComplianceParticipant no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-137">tblComplianceParticipant in Lync Server 2013</span></span>](lync-server-2013-tblcomplianceparticipant.md)

  - [<span data-ttu-id="ab797-138">tblComplianceState no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab797-138">tblComplianceState in Lync Server 2013</span></span>](lync-server-2013-tblcompliancestate.md)

<span data-ttu-id="ab797-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab797-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

