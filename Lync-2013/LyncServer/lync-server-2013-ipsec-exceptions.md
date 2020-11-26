---
title: Exceções IPsec do Lync Server 2013
description: Exceções IPsec do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IPsec exceptions
ms:assetid: 241f1eca-6f2f-44de-90b1-2cb659cbe27c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425719(v=OCS.15)
ms:contentKeyID: 48183627
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b01264171592ec352b778e1aa7eee5861801991
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426722"
---
# <a name="ipsec-exceptions-in-lync-server-2013"></a><span data-ttu-id="86f1e-103">Exceções de IPsec no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="86f1e-103">IPsec exceptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="86f1e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="86f1e-104">

<span> </span></span></span>

<span data-ttu-id="86f1e-105">_**Tópico da última modificação:** 2012-06-27_</span><span class="sxs-lookup"><span data-stu-id="86f1e-105">_**Topic Last Modified:** 2012-06-27_</span></span>

<span data-ttu-id="86f1e-106">Para redes corporativas onde a segurança do protocolo Internet (IPsec) (consulte IETF RFC 4301-4309) foi implantada, o IPsec deve ser desabilitado no intervalo de portas usado para a entrega de vídeo de áudio, vídeo e panorama.</span><span class="sxs-lookup"><span data-stu-id="86f1e-106">For enterprise networks where Internet Protocol security (IPsec) (see IETF RFC 4301-4309) has been deployed, IPsec must be disabled over the range of ports used for the delivery of audio, video, and panorama video.</span></span> <span data-ttu-id="86f1e-107">Essa recomendação existe porque é necessário evitar atrasos na alocação das portas de mídia por causa da negociação IPsec.</span><span class="sxs-lookup"><span data-stu-id="86f1e-107">The recommendation is motivated by the need to avoid any delay in the allocation of media ports due to IPsec negotiation.</span></span>

<span data-ttu-id="86f1e-108">A tabela a seguir explica as configurações de exceções recomendadas do IPsec.</span><span class="sxs-lookup"><span data-stu-id="86f1e-108">The following table explains the recommended IPsec exception settings.</span></span>

### <a name="recommended-ipsec-exceptions"></a><span data-ttu-id="86f1e-109">Exceções recomendadas do IPsec</span><span class="sxs-lookup"><span data-stu-id="86f1e-109">Recommended IPsec Exceptions</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="86f1e-110">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="86f1e-110">Rule name</span></span></th>
<th><span data-ttu-id="86f1e-111">IP de origem</span><span class="sxs-lookup"><span data-stu-id="86f1e-111">Source IP</span></span></th>
<th><span data-ttu-id="86f1e-112">IP de destino</span><span class="sxs-lookup"><span data-stu-id="86f1e-112">Destination IP</span></span></th>
<th><span data-ttu-id="86f1e-113">Protocolo</span><span class="sxs-lookup"><span data-stu-id="86f1e-113">Protocol</span></span></th>
<th><span data-ttu-id="86f1e-114">Porta de origem</span><span class="sxs-lookup"><span data-stu-id="86f1e-114">Source port</span></span></th>
<th><span data-ttu-id="86f1e-115">Porta de destino</span><span class="sxs-lookup"><span data-stu-id="86f1e-115">Destination port</span></span></th>
<th><span data-ttu-id="86f1e-116">Requisito de autenticação</span><span class="sxs-lookup"><span data-stu-id="86f1e-116">Authentication Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86f1e-117">Entrada interna do Servidor de Borda A/V</span><span class="sxs-lookup"><span data-stu-id="86f1e-117">A/V Edge Server Internal Inbound</span></span></p></td>
<td><p><span data-ttu-id="86f1e-118">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-118">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-119">Interno do Servidor de Borda A/V</span><span class="sxs-lookup"><span data-stu-id="86f1e-119">A/V Edge Server Internal</span></span></p></td>
<td><p><span data-ttu-id="86f1e-120">UDP e TCP</span><span class="sxs-lookup"><span data-stu-id="86f1e-120">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="86f1e-121">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-121">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-122">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-122">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-123">Não autenticar</span><span class="sxs-lookup"><span data-stu-id="86f1e-123">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86f1e-124">Entrada externa do Servidor de Borda A/V</span><span class="sxs-lookup"><span data-stu-id="86f1e-124">A/V Edge Server External Inbound</span></span></p></td>
<td><p><span data-ttu-id="86f1e-125">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-125">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-126">Externo do Servidor de Borda A/V</span><span class="sxs-lookup"><span data-stu-id="86f1e-126">A/V Edge Server External</span></span></p></td>
<td><p><span data-ttu-id="86f1e-127">UDP e TCP</span><span class="sxs-lookup"><span data-stu-id="86f1e-127">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="86f1e-128">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-128">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-129">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-129">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-130">Não autenticar</span><span class="sxs-lookup"><span data-stu-id="86f1e-130">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86f1e-131">Saída interna do Servidor de Borda A/V</span><span class="sxs-lookup"><span data-stu-id="86f1e-131">A/V Edge Server Internal Outbound</span></span></p></td>
<td><p><span data-ttu-id="86f1e-132">Interno do Servidor de Borda A/V</span><span class="sxs-lookup"><span data-stu-id="86f1e-132">A/V Edge Server Internal</span></span></p></td>
<td><p><span data-ttu-id="86f1e-133">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-133">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-134">UDP &amp; TCP</span><span class="sxs-lookup"><span data-stu-id="86f1e-134">UDP &amp; TCP</span></span></p></td>
<td><p><span data-ttu-id="86f1e-135">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-135">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-136">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-136">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-137">Não autenticar</span><span class="sxs-lookup"><span data-stu-id="86f1e-137">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86f1e-138">Saída externa do Servidor de Borda A/V</span><span class="sxs-lookup"><span data-stu-id="86f1e-138">A/V Edge Server External Outbound</span></span></p></td>
<td><p><span data-ttu-id="86f1e-139">Externo do Servidor de Borda A/V</span><span class="sxs-lookup"><span data-stu-id="86f1e-139">A/V Edge Server External</span></span></p></td>
<td><p><span data-ttu-id="86f1e-140">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-140">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-141">UDP e TCP</span><span class="sxs-lookup"><span data-stu-id="86f1e-141">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="86f1e-142">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-142">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-143">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-143">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-144">Não autenticar</span><span class="sxs-lookup"><span data-stu-id="86f1e-144">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86f1e-145">Entrada do Servidor de Mediação</span><span class="sxs-lookup"><span data-stu-id="86f1e-145">Mediation Server Inbound</span></span></p></td>
<td><p><span data-ttu-id="86f1e-146">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-146">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-147">Mediação</span><span class="sxs-lookup"><span data-stu-id="86f1e-147">Mediation</span></span></p>
<p><span data-ttu-id="86f1e-148">Servidor(es)</span><span class="sxs-lookup"><span data-stu-id="86f1e-148">Server(s)</span></span></p></td>
<td><p><span data-ttu-id="86f1e-149">UDP e TCP</span><span class="sxs-lookup"><span data-stu-id="86f1e-149">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="86f1e-150">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-150">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-151">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-151">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-152">Não autenticar</span><span class="sxs-lookup"><span data-stu-id="86f1e-152">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86f1e-153">Saída do Servidor de Mediação</span><span class="sxs-lookup"><span data-stu-id="86f1e-153">Mediation Server Outbound</span></span></p></td>
<td><p><span data-ttu-id="86f1e-154">Mediação</span><span class="sxs-lookup"><span data-stu-id="86f1e-154">Mediation</span></span></p>
<p><span data-ttu-id="86f1e-155">Servidor(es)</span><span class="sxs-lookup"><span data-stu-id="86f1e-155">Server(s)</span></span></p></td>
<td><p><span data-ttu-id="86f1e-156">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-156">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-157">UDP e TCP</span><span class="sxs-lookup"><span data-stu-id="86f1e-157">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="86f1e-158">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-158">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-159">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-159">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-160">Não autenticar</span><span class="sxs-lookup"><span data-stu-id="86f1e-160">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86f1e-161">Entrada do Atendedor de Conferência</span><span class="sxs-lookup"><span data-stu-id="86f1e-161">Conferencing Attendant Inbound</span></span></p></td>
<td><p><span data-ttu-id="86f1e-162">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-162">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-163">Servidor Front-End executando o Atendedor de Conferência</span><span class="sxs-lookup"><span data-stu-id="86f1e-163">Front End Server running Conferencing Attendant</span></span></p></td>
<td><p><span data-ttu-id="86f1e-164">UDP e TCP</span><span class="sxs-lookup"><span data-stu-id="86f1e-164">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="86f1e-165">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-165">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-166">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-166">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-167">Não autenticar</span><span class="sxs-lookup"><span data-stu-id="86f1e-167">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86f1e-168">Saída do Atendedor de Conferência</span><span class="sxs-lookup"><span data-stu-id="86f1e-168">Conferencing Attendant Outbound</span></span></p></td>
<td><p><span data-ttu-id="86f1e-169">Servidor Front-End executando o Atendedor de Conferência</span><span class="sxs-lookup"><span data-stu-id="86f1e-169">Front End Server running Conferencing Attendant</span></span></p></td>
<td><p><span data-ttu-id="86f1e-170">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-170">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-171">UDP e TCP</span><span class="sxs-lookup"><span data-stu-id="86f1e-171">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="86f1e-172">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-172">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-173">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-173">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-174">Não autenticar</span><span class="sxs-lookup"><span data-stu-id="86f1e-174">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86f1e-175">Entrada de Conferência A/V</span><span class="sxs-lookup"><span data-stu-id="86f1e-175">A/V Conferencing Inbound</span></span></p></td>
<td><p><span data-ttu-id="86f1e-176">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-176">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-177">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="86f1e-177">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="86f1e-178">UDP e TCP</span><span class="sxs-lookup"><span data-stu-id="86f1e-178">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="86f1e-179">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-179">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-180">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-180">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-181">Não autenticar</span><span class="sxs-lookup"><span data-stu-id="86f1e-181">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86f1e-182">Saída de Conferência A/V</span><span class="sxs-lookup"><span data-stu-id="86f1e-182">A/V Conferencing Outbound</span></span></p></td>
<td><p><span data-ttu-id="86f1e-183">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="86f1e-183">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="86f1e-184">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-184">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-185">UDP e TCP</span><span class="sxs-lookup"><span data-stu-id="86f1e-185">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="86f1e-186">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-186">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-187">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-187">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-188">Não autenticar</span><span class="sxs-lookup"><span data-stu-id="86f1e-188">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86f1e-189">Entrada do Exchange</span><span class="sxs-lookup"><span data-stu-id="86f1e-189">Exchange Inbound</span></span></p></td>
<td><p><span data-ttu-id="86f1e-190">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-190">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-191">Unificação de Mensagens do Exchange</span><span class="sxs-lookup"><span data-stu-id="86f1e-191">Exchange Unified Messaging</span></span></p></td>
<td><p><span data-ttu-id="86f1e-192">UDP e TCP</span><span class="sxs-lookup"><span data-stu-id="86f1e-192">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="86f1e-193">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-193">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-194">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-194">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-195">Não autenticar</span><span class="sxs-lookup"><span data-stu-id="86f1e-195">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86f1e-196">Entrada dos Servidores de Compartilhamento de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="86f1e-196">Application Sharing Servers Inbound</span></span></p></td>
<td><p><span data-ttu-id="86f1e-197">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-197">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-198">Servidores de Compartilhamento de Aplicativos</span><span class="sxs-lookup"><span data-stu-id="86f1e-198">Application Sharing Servers</span></span></p></td>
<td><p><span data-ttu-id="86f1e-199">TCP</span><span class="sxs-lookup"><span data-stu-id="86f1e-199">TCP</span></span></p></td>
<td><p><span data-ttu-id="86f1e-200">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-200">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-201">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-201">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-202">Não autenticar</span><span class="sxs-lookup"><span data-stu-id="86f1e-202">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86f1e-203">Saída do Servidor de Compartilhamento de Aplicativos</span><span class="sxs-lookup"><span data-stu-id="86f1e-203">Application Sharing Server Outbound</span></span></p></td>
<td><p><span data-ttu-id="86f1e-204">Servidores de Compartilhamento de Aplicativos</span><span class="sxs-lookup"><span data-stu-id="86f1e-204">Application Sharing Servers</span></span></p></td>
<td><p><span data-ttu-id="86f1e-205">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-205">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-206">TCP</span><span class="sxs-lookup"><span data-stu-id="86f1e-206">TCP</span></span></p></td>
<td><p><span data-ttu-id="86f1e-207">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-207">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-208">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-208">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-209">Não autenticar</span><span class="sxs-lookup"><span data-stu-id="86f1e-209">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86f1e-210">Saída do Exchange</span><span class="sxs-lookup"><span data-stu-id="86f1e-210">Exchange Outbound</span></span></p></td>
<td><p><span data-ttu-id="86f1e-211">Unificação de Mensagens do Exchange</span><span class="sxs-lookup"><span data-stu-id="86f1e-211">Exchange Unified Messaging</span></span></p></td>
<td><p><span data-ttu-id="86f1e-212">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-212">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-213">UDP e TCP</span><span class="sxs-lookup"><span data-stu-id="86f1e-213">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="86f1e-214">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-214">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-215">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-215">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-216">Não autenticar</span><span class="sxs-lookup"><span data-stu-id="86f1e-216">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86f1e-217">Clientes</span><span class="sxs-lookup"><span data-stu-id="86f1e-217">Clients</span></span></p></td>
<td><p><span data-ttu-id="86f1e-218">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-218">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-219">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-219">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-220">UDP</span><span class="sxs-lookup"><span data-stu-id="86f1e-220">UDP</span></span></p></td>
<td><p><span data-ttu-id="86f1e-221">Intervalo especificado de portas de mídia</span><span class="sxs-lookup"><span data-stu-id="86f1e-221">Specified media port range</span></span></p></td>
<td><p><span data-ttu-id="86f1e-222">Qualquer um</span><span class="sxs-lookup"><span data-stu-id="86f1e-222">Any</span></span></p></td>
<td><p><span data-ttu-id="86f1e-223">Não autenticar</span><span class="sxs-lookup"><span data-stu-id="86f1e-223">Do not authenticate</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="86f1e-224">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="86f1e-224">


</div>

<span> </span>

</div>

</div>

</span></span></div>

