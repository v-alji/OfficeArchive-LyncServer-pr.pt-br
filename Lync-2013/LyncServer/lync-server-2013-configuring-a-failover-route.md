---
title: 'Lync Server 2013: Configurando uma rota de failover'
description: 'Lync Server 2013: Configurando uma rota de failover.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a failover route
ms:assetid: 76e48df4-3b78-4fb7-b1f7-c1e604b81bad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398581(v=OCS.15)
ms:contentKeyID: 48184542
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7cfc45276931685a2d42103b1b7f1d5015dcd7e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433518"
---
# <a name="configuring-a-failover-route-in-lync-server-2013"></a><span data-ttu-id="4bba7-103">Configurando uma rota de failover no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4bba7-103">Configuring a failover route in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4bba7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4bba7-104">

<span> </span></span></span>

<span data-ttu-id="4bba7-105">_**Tópico da última modificação:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="4bba7-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="4bba7-p101">O exemplo abaixo mostra como um administrador pode definir uma rota de failover para utilizar se o Dallas-GW1 for desativado para manutenção ou estiver indisponível por qualquer outro motivo. As seguintes tabelas ilustram a alteração de configuração necessária.</span><span class="sxs-lookup"><span data-stu-id="4bba7-p101">The following example shows how an administrator can define a failover route for use if the Dallas-GW1 is down for maintenance or is otherwise unavailable. The following tables illustrate the required configuration change.</span></span>

### <a name="table-1-user-policy"></a><span data-ttu-id="4bba7-p102">Tabela 1. Política de usuário</span><span class="sxs-lookup"><span data-stu-id="4bba7-p102">Table 1. User Policy</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4bba7-110">Política de usuário</span><span class="sxs-lookup"><span data-stu-id="4bba7-110">User policy</span></span></th>
<th><span data-ttu-id="4bba7-111">Uso do telefone</span><span class="sxs-lookup"><span data-stu-id="4bba7-111">Phone usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bba7-112">Política de Chamada Padrão</span><span class="sxs-lookup"><span data-stu-id="4bba7-112">Default Calling Policy</span></span></p></td>
<td><p><span data-ttu-id="4bba7-113">Local</span><span class="sxs-lookup"><span data-stu-id="4bba7-113">Local</span></span></p>
<p><span data-ttu-id="4bba7-114">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="4bba7-114">GlobalPSTNHopoff</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bba7-115">Política Local de Redmond</span><span class="sxs-lookup"><span data-stu-id="4bba7-115">Redmond Local Policy</span></span></p></td>
<td><p><span data-ttu-id="4bba7-116">RedmondLocal</span><span class="sxs-lookup"><span data-stu-id="4bba7-116">RedmondLocal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bba7-117">Política de Chamada de Dallas</span><span class="sxs-lookup"><span data-stu-id="4bba7-117">Dallas Calling Policy</span></span></p></td>
<td><p><span data-ttu-id="4bba7-118">DallasUsers</span><span class="sxs-lookup"><span data-stu-id="4bba7-118">DallasUsers</span></span></p>
<p><span data-ttu-id="4bba7-119">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="4bba7-119">GlobalPSTNHopoff</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-2-routes"></a><span data-ttu-id="4bba7-p103">Tabela 2. Rotas</span><span class="sxs-lookup"><span data-stu-id="4bba7-p103">Table 2. Routes</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4bba7-122">Nome da rota</span><span class="sxs-lookup"><span data-stu-id="4bba7-122">Route name</span></span></th>
<th><span data-ttu-id="4bba7-123">Padrão do número</span><span class="sxs-lookup"><span data-stu-id="4bba7-123">Number pattern</span></span></th>
<th><span data-ttu-id="4bba7-124">Uso do telefone</span><span class="sxs-lookup"><span data-stu-id="4bba7-124">Phone usage</span></span></th>
<th><span data-ttu-id="4bba7-125">Tronco</span><span class="sxs-lookup"><span data-stu-id="4bba7-125">Trunk</span></span></th>
<th><span data-ttu-id="4bba7-126">Gateway</span><span class="sxs-lookup"><span data-stu-id="4bba7-126">Gateway</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bba7-127">Rota Local de Redmond</span><span class="sxs-lookup"><span data-stu-id="4bba7-127">Redmond Local Route</span></span></p></td>
<td><p><span data-ttu-id="4bba7-128">^\+1 (425 | 206 | 253) (\d) {7} $</span><span class="sxs-lookup"><span data-stu-id="4bba7-128">^\+1(425|206|253)(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="4bba7-129">Local</span><span class="sxs-lookup"><span data-stu-id="4bba7-129">Local</span></span></p>
<p><span data-ttu-id="4bba7-130">RedmondLocal</span><span class="sxs-lookup"><span data-stu-id="4bba7-130">RedmondLocal</span></span></p></td>
<td><p><span data-ttu-id="4bba7-131">Tronco 1</span><span class="sxs-lookup"><span data-stu-id="4bba7-131">Trunk1</span></span></p>
<p><span data-ttu-id="4bba7-132">Tronco 2</span><span class="sxs-lookup"><span data-stu-id="4bba7-132">Trunk2</span></span></p></td>
<td><p><span data-ttu-id="4bba7-133">Red-GW1</span><span class="sxs-lookup"><span data-stu-id="4bba7-133">Red-GW1</span></span></p>
<p><span data-ttu-id="4bba7-134">Red-GW2</span><span class="sxs-lookup"><span data-stu-id="4bba7-134">Red-GW2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bba7-135">Rota Local de Dallas</span><span class="sxs-lookup"><span data-stu-id="4bba7-135">Dallas Local Route</span></span></p></td>
<td><p><span data-ttu-id="4bba7-136">^\+1 (972 | 214 | 469) (\d {7} ) $</span><span class="sxs-lookup"><span data-stu-id="4bba7-136">^\+1(972|214|469)(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="4bba7-137">Local</span><span class="sxs-lookup"><span data-stu-id="4bba7-137">Local</span></span></p></td>
<td><p><span data-ttu-id="4bba7-138">Tronco 3</span><span class="sxs-lookup"><span data-stu-id="4bba7-138">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="4bba7-139">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="4bba7-139">Dallas-GW1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bba7-140">Rota Universal</span><span class="sxs-lookup"><span data-stu-id="4bba7-140">Universal Route</span></span></p></td>
<td><p><span data-ttu-id="4bba7-141">^\+? (\d \*) $</span><span class="sxs-lookup"><span data-stu-id="4bba7-141">^\+?(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="4bba7-142">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="4bba7-142">GlobalPSTNHopoff</span></span></p></td>
<td><p><span data-ttu-id="4bba7-143">Tronco 1</span><span class="sxs-lookup"><span data-stu-id="4bba7-143">Trunk1</span></span></p>
<p><span data-ttu-id="4bba7-144">Tronco 2</span><span class="sxs-lookup"><span data-stu-id="4bba7-144">Trunk2</span></span></p>
<p><span data-ttu-id="4bba7-145">Tronco 3</span><span class="sxs-lookup"><span data-stu-id="4bba7-145">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="4bba7-146">Red-GW1</span><span class="sxs-lookup"><span data-stu-id="4bba7-146">Red-GW1</span></span></p>
<p><span data-ttu-id="4bba7-147">Red-GW2</span><span class="sxs-lookup"><span data-stu-id="4bba7-147">Red-GW2</span></span></p>
<p><span data-ttu-id="4bba7-148">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="4bba7-148">Dallas-GW1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bba7-149">Rota de Usuários de Dallas</span><span class="sxs-lookup"><span data-stu-id="4bba7-149">Dallas Users Route</span></span></p></td>
<td><p><span data-ttu-id="4bba7-150">^\+? (\d \*) $</span><span class="sxs-lookup"><span data-stu-id="4bba7-150">^\+?(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="4bba7-151">DallasUsers</span><span class="sxs-lookup"><span data-stu-id="4bba7-151">DallasUsers</span></span></p></td>
<td><p><span data-ttu-id="4bba7-152">Tronco 3</span><span class="sxs-lookup"><span data-stu-id="4bba7-152">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="4bba7-153">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="4bba7-153">Dallas-GW1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4bba7-p104">Na tabela 1, um uso de telefone de GlobalPSTNHopoff é adicionado após o uso de telefone DallasUsers na Política de Chamada de Dallas. Isso permite que as chamadas com a política de chamada de Dallas usem rotas configuradas para o uso de telefone GlobalPSTNHopoff, caso uma rota para o uso do telefone DallasUsers não esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="4bba7-p104">In Table 1, a phone usage of GlobalPSTNHopoff is added after the DallasUsers phone usage in the Dallas Calling Policy. This enables calls with the Dallas Calling policy to use routes that are configured for the GlobalPSTNHopoff phone usage if a route for the DallasUsers phone usage is unavailable.</span></span>

<span data-ttu-id="4bba7-156"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4bba7-156"></div>

<span> </span>

</div>

</div>

</span></span></div>

