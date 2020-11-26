---
title: 'Lync Server 2013: Resumo de porta - cargas de DNS e de HLB balanceadas'
description: 'Lync Server 2013: Resumo da porta-DNS e carga de HLB balanceada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - DNS and HLB load balanced
ms:assetid: b07c37e4-820e-46ee-a678-1da95d1b87af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205179(v=OCS.15)
ms:contentKeyID: 48185149
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be2e8204e792fd9c4718cb9171e90784af2d0104
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424335"
---
# <a name="port-summary---dns-and-hlb-load-balanced-in-lync-server-2013"></a><span data-ttu-id="35cd8-103">Resumo de porta - cargas de DNS e de HLB balanceadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="35cd8-103">Port summary - DNS and HLB load balanced in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="35cd8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="35cd8-104">

<span> </span></span></span>

<span data-ttu-id="35cd8-105">_**Tópico da última modificação:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="35cd8-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="35cd8-106">Os requisitos de porta do firewall para um único diretor consistem em portas que são usadas para estabelecer comunicação com o diretor da interface interna ou da rede de face interna do proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="35cd8-106">Firewall port requirements for a single Director consist of the ports that are used to establish communication with the Director from the internal interface or internal-facing network of the reverse proxy.</span></span> <span data-ttu-id="35cd8-107">O Microsoft Lync Server 2013 por padrão espera que as portas HTTP/TCP 8080 e HTTPS/TCP 4443 sejam abertas do proxy reverso para o diretor, bem como do pool de front-end e do servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="35cd8-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="35cd8-108">Além disso, deve haver comunicação SIP (Session Initiation Protocol) da interface interna do servidor de borda para o diretor e para o pool de front-end e o servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="35cd8-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="35cd8-109">O protocolo SIP usa SIP/MTLS/TCP 5061 do servidor de borda para o pool de front-ends e o servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="35cd8-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="35cd8-110">Uma regra que permita a comunicação SIP/MTLS/TCP 5061 do diretor, do pool de front-ends e do servidor front-end para a interface interna do servidor de borda também deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="35cd8-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="single-director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="35cd8-111">Portas e protocolos de director único para definições de firewall</span><span class="sxs-lookup"><span data-stu-id="35cd8-111">Single Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35cd8-112">Função/protocolo/TCP ou UDP/porta</span><span class="sxs-lookup"><span data-stu-id="35cd8-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="35cd8-113">Endereço IP de Origem</span><span class="sxs-lookup"><span data-stu-id="35cd8-113">Source IP address</span></span></th>
<th><span data-ttu-id="35cd8-114">Endereço IP de Destino</span><span class="sxs-lookup"><span data-stu-id="35cd8-114">Destination IP address</span></span></th>
<th><span data-ttu-id="35cd8-115">Notas</span><span class="sxs-lookup"><span data-stu-id="35cd8-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35cd8-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="35cd8-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="35cd8-117">Interface interna de proxy inversa</span><span class="sxs-lookup"><span data-stu-id="35cd8-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="35cd8-118">VIP do balanceador de carga de hardware do diretor</span><span class="sxs-lookup"><span data-stu-id="35cd8-118">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="35cd8-119">Inicialmente recebido pelo lado externo do proxy reverso, a comunicação é enviada para o diretor de serviços Web do diretor HLB VIP e servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="35cd8-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Server web services.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35cd8-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="35cd8-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="35cd8-121">Interface interna de proxy inversa</span><span class="sxs-lookup"><span data-stu-id="35cd8-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="35cd8-122">VIP do balanceador de carga de hardware do diretor</span><span class="sxs-lookup"><span data-stu-id="35cd8-122">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="35cd8-123">Inicialmente recebido pelo lado externo do proxy reverso, a comunicação é enviada para o diretor de serviços Web do diretor HLB VIP e servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="35cd8-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Server web services.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35cd8-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="35cd8-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="35cd8-125">Diretor</span><span class="sxs-lookup"><span data-stu-id="35cd8-125">Director</span></span></p></td>
<td><p><span data-ttu-id="35cd8-126">Pool de front-end ou servidor front-end</span><span class="sxs-lookup"><span data-stu-id="35cd8-126">Front End pool or Front End Server</span></span></p></td>
<td><p><span data-ttu-id="35cd8-127">Comunicação entre servidores entre o VIP do diretor HLB e o servidor front-end ou servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="35cd8-127">Inter-server communication between the Director HLB VIP and the Front End Server or Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35cd8-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="35cd8-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="35cd8-129">Clientes internos</span><span class="sxs-lookup"><span data-stu-id="35cd8-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="35cd8-130">VIP do balanceador de carga de hardware do diretor</span><span class="sxs-lookup"><span data-stu-id="35cd8-130">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="35cd8-131">O diretor fornece serviços Web para clientes internos e externos.</span><span class="sxs-lookup"><span data-stu-id="35cd8-131">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35cd8-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="35cd8-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="35cd8-133">Clientes internos</span><span class="sxs-lookup"><span data-stu-id="35cd8-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="35cd8-134">VIP do balanceador de carga de hardware do diretor</span><span class="sxs-lookup"><span data-stu-id="35cd8-134">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="35cd8-135">O diretor fornece serviços Web para clientes internos e externos.</span><span class="sxs-lookup"><span data-stu-id="35cd8-135">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35cd8-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="35cd8-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="35cd8-137">Interface interna do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="35cd8-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="35cd8-138">Diretor</span><span class="sxs-lookup"><span data-stu-id="35cd8-138">Director</span></span></p></td>
<td><p><span data-ttu-id="35cd8-139">Comunicação SIP do servidor de borda para o diretor, bem como os servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="35cd8-139">SIP communication from the Edge Server to the Director, as well as the Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35cd8-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="35cd8-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="35cd8-141">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="35cd8-141">Any</span></span></p></td>
<td><p><span data-ttu-id="35cd8-142">Diretor</span><span class="sxs-lookup"><span data-stu-id="35cd8-142">Director</span></span></p></td>
<td><p><span data-ttu-id="35cd8-143">Comandos do agente ou conjunto de serviços de log centralizado (ClsController.exe) ou do agente (ClsAgent.exe) e a coleção de logs</span><span class="sxs-lookup"><span data-stu-id="35cd8-143">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35cd8-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="35cd8-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="35cd8-145">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="35cd8-145">Any</span></span></p></td>
<td><p><span data-ttu-id="35cd8-146">Diretor</span><span class="sxs-lookup"><span data-stu-id="35cd8-146">Director</span></span></p></td>
<td><p><span data-ttu-id="35cd8-147">Comandos do agente ou conjunto de serviços de log centralizado (ClsController.exe) ou do agente (ClsAgent.exe) e a coleção de logs</span><span class="sxs-lookup"><span data-stu-id="35cd8-147">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35cd8-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="35cd8-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="35cd8-149">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="35cd8-149">Any</span></span></p></td>
<td><p><span data-ttu-id="35cd8-150">Diretor</span><span class="sxs-lookup"><span data-stu-id="35cd8-150">Director</span></span></p></td>
<td><p><span data-ttu-id="35cd8-151">Comandos do agente ou conjunto de serviços de log centralizado (ClsController.exe) ou do agente (ClsAgent.exe) e a coleção de logs</span><span class="sxs-lookup"><span data-stu-id="35cd8-151">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="35cd8-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="35cd8-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

