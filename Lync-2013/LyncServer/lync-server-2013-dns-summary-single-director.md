---
title: 'Lync Server 2013: Resumo de DNS - Diretor Único'
description: 'Lync Server 2013: Resumo de DNS-diretor único.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Single Director
ms:assetid: 790ecb56-92cd-41f4-baf6-c290a707aa4d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205021(v=OCS.15)
ms:contentKeyID: 48184568
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 78ef19383df45644ad951ca5da69ef893b231980
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389702"
---
# <a name="dns-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="23c98-103">Resumo de DNS - Diretor Único no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="23c98-103">DNS summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="23c98-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="23c98-104">

<span> </span></span></span>

<span data-ttu-id="23c98-105">_**Tópico da última modificação:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="23c98-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="23c98-106">A tabela a seguir contém um resumo dos registros DNS necessários para dar suporte ao diretor único.</span><span class="sxs-lookup"><span data-stu-id="23c98-106">The following table contains a summary of the DNS records that are required to support the single Director.</span></span> <span data-ttu-id="23c98-107">A função do diretor requer registros DNS semelhantes ao servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="23c98-107">The role of the Director requires similar DNS records as the Front End Server.</span></span> <span data-ttu-id="23c98-108">O número de registros necessários se reflete nos nomes alternativos da entidade obrigatórios no certificado do diretor.</span><span class="sxs-lookup"><span data-stu-id="23c98-108">The number of records needed is reflected in the subject alternative names required on the Director certificate.</span></span> <span data-ttu-id="23c98-109">Diferente do servidor front-end, o diretor não hospeda contas de usuário nem hospeda os serviços de mobilidade.</span><span class="sxs-lookup"><span data-stu-id="23c98-109">Different from the Front End Server, the Director does not host user accounts or host the Mobility Services.</span></span>

### <a name="dns-records-required-for-the-director"></a><span data-ttu-id="23c98-110">Registros DNS necessários para o diretor</span><span class="sxs-lookup"><span data-stu-id="23c98-110">DNS Records Required for the Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23c98-111">Local/tipo/porta</span><span class="sxs-lookup"><span data-stu-id="23c98-111">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="23c98-112">Registro FQDN/DNS</span><span class="sxs-lookup"><span data-stu-id="23c98-112">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="23c98-113">Endereço IP/FQDN</span><span class="sxs-lookup"><span data-stu-id="23c98-113">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="23c98-114">Mapas para/comentários</span><span class="sxs-lookup"><span data-stu-id="23c98-114">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23c98-115">DNS interno/A</span><span class="sxs-lookup"><span data-stu-id="23c98-115">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="23c98-116">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="23c98-116">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="23c98-117">Diretor</span><span class="sxs-lookup"><span data-stu-id="23c98-117">Director</span></span></p></td>
<td><p><span data-ttu-id="23c98-118">Registro de host do diretor usado para replicação e servidor para servidor</span><span class="sxs-lookup"><span data-stu-id="23c98-118">Director host record used for replication and server to server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23c98-119">DNS interno/A</span><span class="sxs-lookup"><span data-stu-id="23c98-119">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="23c98-120">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="23c98-120">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="23c98-121">Diretor</span><span class="sxs-lookup"><span data-stu-id="23c98-121">Director</span></span></p></td>
<td><p><span data-ttu-id="23c98-122">Protocolo de iniciação de sessão de entrada (SIP) da interface de borda interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="23c98-122">Inbound session initiation protocol (SIP) from the internal Edge interface of the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23c98-123">DNS interno/A</span><span class="sxs-lookup"><span data-stu-id="23c98-123">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="23c98-124">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="23c98-124">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="23c98-125">Diretor</span><span class="sxs-lookup"><span data-stu-id="23c98-125">Director</span></span></p></td>
<td><p><span data-ttu-id="23c98-126">Serviços da discagem publicados do proxy reverso</span><span class="sxs-lookup"><span data-stu-id="23c98-126">Published dialin web services from reverse proxy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23c98-127">DNS interno/A</span><span class="sxs-lookup"><span data-stu-id="23c98-127">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="23c98-128">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="23c98-128">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="23c98-129">Diretor</span><span class="sxs-lookup"><span data-stu-id="23c98-129">Director</span></span></p></td>
<td><p><span data-ttu-id="23c98-130">Serviços Web de reunião publicados do proxy reverso</span><span class="sxs-lookup"><span data-stu-id="23c98-130">Published meet web services from reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23c98-131">DNS interno/A</span><span class="sxs-lookup"><span data-stu-id="23c98-131">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="23c98-132">webdirexternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="23c98-132">webdirexternal.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="23c98-133">Diretor</span><span class="sxs-lookup"><span data-stu-id="23c98-133">Director</span></span></p></td>
<td><p><span data-ttu-id="23c98-134">Publicado e definido pelos serviços Web externos de tíquete de proxy reverso para o diretor</span><span class="sxs-lookup"><span data-stu-id="23c98-134">Published and defined by the reverse proxy Web Ticket external web services for the Director</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="23c98-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="23c98-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

