---
title: 'Lync Server 2013: Resumo de porta - Pool de Diretor em escala, balanceador de carga de hardware'
description: 'Lync Server 2013: Resumo da porta – pool do diretor dimensionado, balanceador de carga de hardware.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled Director pool, hardware load balancer
ms:assetid: 6ae2f4ac-5b64-4e45-8253-133308f5812d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204983(v=OCS.15)
ms:contentKeyID: 48184434
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10bfb3a3ad3a38b6cb0e46414bf22deecc71d7b5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442793"
---
# <a name="port-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="41d41-103">Resumo de porta - Pool de Diretor em escala, balanceador de carga de hardware no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41d41-103">Port summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="41d41-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="41d41-104">

<span> </span></span></span>

<span data-ttu-id="41d41-105">_**Tópico da última modificação:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="41d41-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="41d41-106">Os requisitos de porta do firewall para um pool de directors consistem nas portas usadas para estabelecer comunicação com o diretor da interface interna do servidor de borda ou da interface interna do proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="41d41-106">Firewall port requirements for a Director pool consist of the ports that are used to establish communication with the Director from the internal interface of the Edge Server or internal-facing interface of the reverse proxy.</span></span> <span data-ttu-id="41d41-107">O Microsoft Lync Server 2013 por padrão espera que as portas HTTP/TCP 8080 e HTTPS/TCP 4443 sejam abertas do proxy reverso para o diretor, bem como do pool de front-end e do servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="41d41-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="41d41-108">Além disso, deve haver comunicação SIP (Session Initiation Protocol) da interface interna do servidor de borda para o diretor e para o pool de front-end e o servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="41d41-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="41d41-109">O protocolo SIP usa SIP/MTLS/TCP 5061 do servidor de borda para o pool de front-ends e o servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="41d41-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="41d41-110">Uma regra que permita a comunicação SIP/MTLS/TCP 5061 do diretor, do pool de front-ends e do servidor front-end para a interface interna do servidor de borda também deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="41d41-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="41d41-111">Portas e protocolos do diretor para definições de firewall</span><span class="sxs-lookup"><span data-stu-id="41d41-111">Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="41d41-112">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="41d41-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="41d41-113">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="41d41-113">Source IP address</span></span></th>
<th><span data-ttu-id="41d41-114">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="41d41-114">Destination IP address</span></span></th>
<th><span data-ttu-id="41d41-115">Notas</span><span class="sxs-lookup"><span data-stu-id="41d41-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41d41-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="41d41-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="41d41-117">Interface interna de proxy inversa</span><span class="sxs-lookup"><span data-stu-id="41d41-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="41d41-118">VIP do balanceador de carga de hardware do diretor</span><span class="sxs-lookup"><span data-stu-id="41d41-118">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="41d41-119">Inicialmente recebido pelo lado externo do proxy reverso, a comunicação é enviada para o diretor HLB VIP e serviços Web de servidor front-end</span><span class="sxs-lookup"><span data-stu-id="41d41-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Servers web services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41d41-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="41d41-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="41d41-121">Interface interna de proxy inversa</span><span class="sxs-lookup"><span data-stu-id="41d41-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="41d41-122">VIP do balanceador de carga de hardware do diretor</span><span class="sxs-lookup"><span data-stu-id="41d41-122">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="41d41-123">Inicialmente recebido pelo lado externo do proxy reverso, a comunicação é enviada para o diretor HLB VIP e serviços Web de servidor front-end</span><span class="sxs-lookup"><span data-stu-id="41d41-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Servers web services</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41d41-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="41d41-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="41d41-125">Diretor</span><span class="sxs-lookup"><span data-stu-id="41d41-125">Director</span></span></p></td>
<td><p><span data-ttu-id="41d41-126">Servidor front-end ou pool de front-end</span><span class="sxs-lookup"><span data-stu-id="41d41-126">Front End Server or Front End pool</span></span></p></td>
<td><p><span data-ttu-id="41d41-127">Comunicação entre servidores entre o diretor HLB VIP e os servidores front-end</span><span class="sxs-lookup"><span data-stu-id="41d41-127">Inter-server communication between the Director HLB VIP and the Front End Servers</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41d41-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="41d41-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="41d41-129">Clientes internos</span><span class="sxs-lookup"><span data-stu-id="41d41-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="41d41-130">VIP do balanceador de carga de hardware do diretor</span><span class="sxs-lookup"><span data-stu-id="41d41-130">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="41d41-131">O diretor fornece serviços Web para clientes internos e externos.</span><span class="sxs-lookup"><span data-stu-id="41d41-131">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41d41-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="41d41-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="41d41-133">Clientes internos</span><span class="sxs-lookup"><span data-stu-id="41d41-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="41d41-134">VIP do balanceador de carga de hardware do diretor</span><span class="sxs-lookup"><span data-stu-id="41d41-134">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="41d41-135">O diretor fornece serviços Web para clientes internos e externos.</span><span class="sxs-lookup"><span data-stu-id="41d41-135">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41d41-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="41d41-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="41d41-137">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="41d41-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="41d41-138">VIP do balanceador de carga de hardware do diretor</span><span class="sxs-lookup"><span data-stu-id="41d41-138">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="41d41-139">Comunicação SIP do servidor de borda para o diretor e servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="41d41-139">SIP communication from the Edge Server to the Director, and Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41d41-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="41d41-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="41d41-141">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="41d41-141">Any</span></span></p></td>
<td><p><span data-ttu-id="41d41-142">Diretor</span><span class="sxs-lookup"><span data-stu-id="41d41-142">Director</span></span></p></td>
<td><p><span data-ttu-id="41d41-143">Comandos do agente ou conjunto de serviços de log centralizado (ClsController.exe) ou do agente (ClsAgent.exe) e a coleção de logs</span><span class="sxs-lookup"><span data-stu-id="41d41-143">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41d41-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="41d41-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="41d41-145">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="41d41-145">Any</span></span></p></td>
<td><p><span data-ttu-id="41d41-146">Diretor</span><span class="sxs-lookup"><span data-stu-id="41d41-146">Director</span></span></p></td>
<td><p><span data-ttu-id="41d41-147">Comandos do agente ou conjunto de serviços de log centralizado (ClsController.exe) ou do agente (ClsAgent.exe) e a coleção de logs</span><span class="sxs-lookup"><span data-stu-id="41d41-147">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41d41-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="41d41-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="41d41-149">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="41d41-149">Any</span></span></p></td>
<td><p><span data-ttu-id="41d41-150">Diretor</span><span class="sxs-lookup"><span data-stu-id="41d41-150">Director</span></span></p></td>
<td><p><span data-ttu-id="41d41-151">Comandos do agente ou conjunto de serviços de log centralizado (ClsController.exe) ou do agente (ClsAgent.exe) e a coleção de logs</span><span class="sxs-lookup"><span data-stu-id="41d41-151">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="41d41-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="41d41-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

