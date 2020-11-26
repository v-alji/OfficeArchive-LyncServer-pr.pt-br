---
title: 'Lync Server 2013: Resumo de DNS - Cargas de DNS e de HLB balanceadas'
description: 'Lync Server 2013: Resumo de DNS-DNS e carga de HLB balanceada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - DNS and HLB load balanced
ms:assetid: d2132695-1956-4190-a98e-cd7255cbded6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205273(v=OCS.15)
ms:contentKeyID: 48185447
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81c191d653ce4025618e135b4c69bc673f79a6d9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437739"
---
# <a name="dns-summary---dns-and-hlb-load-balanced-in-lync-server-2013"></a><span data-ttu-id="973bb-103">Resumo de DNS - Cargas de DNS e de HLB balanceadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="973bb-103">DNS summary - DNS and HLB load balanced in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="973bb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="973bb-104">

<span> </span></span></span>

<span data-ttu-id="973bb-105">_**Tópico da última modificação:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="973bb-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="973bb-106">A tabela a seguir contém um resumo dos registros DNS necessários para dar suporte ao diretor de balanceamento de carga de hardware e carga balanceada do DNS.</span><span class="sxs-lookup"><span data-stu-id="973bb-106">The following table contains a summary of the DNS records that are required to support the DNS load balanced and hardware load balanced Director.</span></span> <span data-ttu-id="973bb-107">A função do diretor requer registros DNS semelhantes ao servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="973bb-107">The role of the Director requires similar DNS records as the Front End Server.</span></span> <span data-ttu-id="973bb-108">O número de registros necessários se reflete nos nomes alternativos da entidade obrigatórios no certificado do diretor.</span><span class="sxs-lookup"><span data-stu-id="973bb-108">The number of records needed is reflected in the subject alternative names required on the Director certificate.</span></span> <span data-ttu-id="973bb-109">Diferente do servidor front-end, o pool de directors não hospeda contas de usuário nem hospeda os serviços de mobilidade.</span><span class="sxs-lookup"><span data-stu-id="973bb-109">Different from the Front End Server, the Director pool does not host user accounts or host the Mobility Services.</span></span>

### <a name="dns-records-required-for-the-director-pool-using-dns-load-balancing-and-hardware-load-balancer"></a><span data-ttu-id="973bb-110">Registros DNS necessários para o pool de diretor que usa o balanceamento de carga de DNS e o balanceador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="973bb-110">DNS Records Required for the Director Pool using DNS Load Balancing and Hardware Load Balancer</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="973bb-111">Local/tipo/porta</span><span class="sxs-lookup"><span data-stu-id="973bb-111">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="973bb-112">Registro FQDN/DNS</span><span class="sxs-lookup"><span data-stu-id="973bb-112">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="973bb-113">Endereço IP/FQDN</span><span class="sxs-lookup"><span data-stu-id="973bb-113">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="973bb-114">Mapas para/comentários</span><span class="sxs-lookup"><span data-stu-id="973bb-114">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="973bb-115">DNS interno/A</span><span class="sxs-lookup"><span data-stu-id="973bb-115">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="973bb-116">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="973bb-116">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="973bb-117">Diretor</span><span class="sxs-lookup"><span data-stu-id="973bb-117">Director</span></span></p></td>
<td><p><span data-ttu-id="973bb-118">Registro de host do diretor usado para replicação e servidor para servidor</span><span class="sxs-lookup"><span data-stu-id="973bb-118">Director host record used for replication and server to server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="973bb-119">DNS interno/A</span><span class="sxs-lookup"><span data-stu-id="973bb-119">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="973bb-120">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="973bb-120">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="973bb-121">Pool de diretores</span><span class="sxs-lookup"><span data-stu-id="973bb-121">Director pool</span></span></p></td>
<td><p><span data-ttu-id="973bb-122">Registro de host para o pool de directors de carga balanceada do DNS do servidor para o servidor</span><span class="sxs-lookup"><span data-stu-id="973bb-122">Host record for the DNS load balanced Director pool for server to server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="973bb-123">DNS interno/A</span><span class="sxs-lookup"><span data-stu-id="973bb-123">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="973bb-124">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="973bb-124">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="973bb-125">Pool de diretores</span><span class="sxs-lookup"><span data-stu-id="973bb-125">Director pool</span></span></p></td>
<td><p><span data-ttu-id="973bb-126">Protocolo de iniciação de sessão de entrada (SIP) da interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="973bb-126">Inbound session initiation protocol (SIP) from the internal interface of the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="973bb-127">DNS interno/A</span><span class="sxs-lookup"><span data-stu-id="973bb-127">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="973bb-128">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="973bb-128">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="973bb-129">VIP de HLB do pool do diretor</span><span class="sxs-lookup"><span data-stu-id="973bb-129">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="973bb-130">Serviços Web de discagem com carga balanceada do hardware de proxy reverso</span><span class="sxs-lookup"><span data-stu-id="973bb-130">Hardware load balanced published dialin web services from reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="973bb-131">DNS interno/A</span><span class="sxs-lookup"><span data-stu-id="973bb-131">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="973bb-132">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="973bb-132">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="973bb-133">VIP de HLB do pool do diretor</span><span class="sxs-lookup"><span data-stu-id="973bb-133">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="973bb-134">Publicação de carga de hardware com balanceamento de carga de serviços Web de proxy reverso</span><span class="sxs-lookup"><span data-stu-id="973bb-134">Hardware load balanced published meet web services from reverse proxy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="973bb-135">DNS interno/A</span><span class="sxs-lookup"><span data-stu-id="973bb-135">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="973bb-136">webdirexternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="973bb-136">webdirexternal.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="973bb-137">VIP de HLB do pool do diretor</span><span class="sxs-lookup"><span data-stu-id="973bb-137">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="973bb-138">Carga balanceada de carga de hardware publicada e definida pelos serviços Web externos de tíquete de proxy reverso para o pool de diretor</span><span class="sxs-lookup"><span data-stu-id="973bb-138">Hardware load balanced published and defined by the reverse proxy Web Ticket external web services for the Director pool</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="973bb-139">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="973bb-139">


</div>

<span> </span>

</div>

</div>

</span></span></div>

