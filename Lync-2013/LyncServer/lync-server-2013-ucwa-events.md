---
title: 'Lync Server 2013: eventos do UCWA'
description: 'Lync Server 2013: UCWA eventos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UCWA events
ms:assetid: 26cb409d-f4e4-43c7-873f-b694702d491d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945621(v=OCS.15)
ms:contentKeyID: 51541461
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8104ce9c7533350f40ce194e1cde205bc3692792
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440462"
---
# <a name="ucwa-events-in-lync-server-2013"></a><span data-ttu-id="3cdd3-103">Eventos do UCWA no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3cdd3-103">UCWA events in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3cdd3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3cdd3-104">

<span> </span></span></span>

<span data-ttu-id="3cdd3-105">_**Tópico da última modificação:** 2013-02-15_</span><span class="sxs-lookup"><span data-stu-id="3cdd3-105">_**Topic Last Modified:** 2013-02-15_</span></span>

    The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="3cdd3-106">O Lync Server 2013 usa a API da Web de comunicação unificada (UCWA) para várias finalidades, desde o acesso ao Microsoft Exchange para pesquisas de contato até a atualização de presença para clientes móveis.</span><span class="sxs-lookup"><span data-stu-id="3cdd3-106">Lync Server 2013 uses the Unified Communications Web API (UCWA) for a number of purposes, from accessing Microsoft Exchange for contact searches to updating presence for mobile clients.</span></span>

<span data-ttu-id="3cdd3-p101">A UCWA gravará registros de comportamento operacional como tipos de evento Informacional, Aviso e Erro. A tabela a seguir descreve tais eventos que podem ser gravados com componentes da UCWA.</span><span class="sxs-lookup"><span data-stu-id="3cdd3-p101">UCWA will write records of operational behavior as event types Informational, Warning, and Error. The following table describes the events that can be written by the UCWA components.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3cdd3-109">ID do evento</span><span class="sxs-lookup"><span data-stu-id="3cdd3-109">Event ID</span></span></th>
<th><span data-ttu-id="3cdd3-110">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="3cdd3-110">Event Type</span></span></th>
<th><span data-ttu-id="3cdd3-111">Resumo</span><span class="sxs-lookup"><span data-stu-id="3cdd3-111">Summary</span></span></th>
<th><span data-ttu-id="3cdd3-112">Causa e resolução</span><span class="sxs-lookup"><span data-stu-id="3cdd3-112">Cause and Resolution</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cdd3-113">20001</span><span class="sxs-lookup"><span data-stu-id="3cdd3-113">20001</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-114">Informativo</span><span class="sxs-lookup"><span data-stu-id="3cdd3-114">Informational</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-115">UCWA inicializado</span><span class="sxs-lookup"><span data-stu-id="3cdd3-115">UCWA initialized</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-116">N/D</span><span class="sxs-lookup"><span data-stu-id="3cdd3-116">N/A</span></span></p>
<p><span data-ttu-id="3cdd3-117">N/D</span><span class="sxs-lookup"><span data-stu-id="3cdd3-117">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cdd3-118">20002</span><span class="sxs-lookup"><span data-stu-id="3cdd3-118">20002</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-119">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-119">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-120">A UCWA encontrou uma exceção inesperada durante a inicialização</span><span class="sxs-lookup"><span data-stu-id="3cdd3-120">UCWA encountered an unexpected exception during initialization</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-121">Ocorreu um erro inesperado durante a inicialização</span><span class="sxs-lookup"><span data-stu-id="3cdd3-121">An unexpected error has occurred during initialization</span></span></p>
<p><span data-ttu-id="3cdd3-122">Examine os detalhes da exceção na entrada de log do evento associado para determinar a possível causa</span><span class="sxs-lookup"><span data-stu-id="3cdd3-122">Examine the exception details in the associated event log entry to determine the possible cause</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cdd3-123">20003</span><span class="sxs-lookup"><span data-stu-id="3cdd3-123">20003</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-124">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-124">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-125">A UCWA encontrou uma exceção não manipulada</span><span class="sxs-lookup"><span data-stu-id="3cdd3-125">UCWA encountered an unhandled exception</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-126">Ocorreu uma exceção não manipulada</span><span class="sxs-lookup"><span data-stu-id="3cdd3-126">An unhandled exception happened</span></span></p>
<p><span data-ttu-id="3cdd3-p102">Reinicie o servidor. Se o problema persistir, entre em contato com o suporte do produto</span><span class="sxs-lookup"><span data-stu-id="3cdd3-p102">Restart the server. If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cdd3-129">20004</span><span class="sxs-lookup"><span data-stu-id="3cdd3-129">20004</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-130">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-130">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-131">Não é possível acessar o Exchange para foto HD</span><span class="sxs-lookup"><span data-stu-id="3cdd3-131">Cannot access Exchange for HD photo</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-132">A conexão com o Exchange não está disponível</span><span class="sxs-lookup"><span data-stu-id="3cdd3-132">Connection to Exchange is not available</span></span></p>
<p><span data-ttu-id="3cdd3-133">Certifique-se de que a conexão com o Exchange está disponível</span><span class="sxs-lookup"><span data-stu-id="3cdd3-133">Make sure the connection to Exchange is available</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cdd3-134">20005</span><span class="sxs-lookup"><span data-stu-id="3cdd3-134">20005</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-135">Informativo</span><span class="sxs-lookup"><span data-stu-id="3cdd3-135">Informational</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-136">Recuperação de uma falha ao acessar o Exchange para foto HD</span><span class="sxs-lookup"><span data-stu-id="3cdd3-136">Recovered from failing to access Exchange for HD photo</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-137">N/D</span><span class="sxs-lookup"><span data-stu-id="3cdd3-137">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cdd3-138">20006</span><span class="sxs-lookup"><span data-stu-id="3cdd3-138">20006</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-139">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-139">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-140">Não é possível acessar o Exchange para pesquisa de contato</span><span class="sxs-lookup"><span data-stu-id="3cdd3-140">Cannot access Exchange for contact search</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-141">A conexão com o Exchange não está disponível</span><span class="sxs-lookup"><span data-stu-id="3cdd3-141">Connection to Exchange is not available</span></span></p>
<p><span data-ttu-id="3cdd3-142">Certifique-se de que a conexão com o Exchange está disponível</span><span class="sxs-lookup"><span data-stu-id="3cdd3-142">Make sure the connection to Exchange is available</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cdd3-143">20007</span><span class="sxs-lookup"><span data-stu-id="3cdd3-143">20007</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-144">Informativo</span><span class="sxs-lookup"><span data-stu-id="3cdd3-144">Informational</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-145">Recuperação de uma falha em pesquisar contato no Exchange</span><span class="sxs-lookup"><span data-stu-id="3cdd3-145">Recovered from failing to search contact in Exchange</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-146">N/D</span><span class="sxs-lookup"><span data-stu-id="3cdd3-146">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cdd3-147">20008</span><span class="sxs-lookup"><span data-stu-id="3cdd3-147">20008</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-148">Aviso</span><span class="sxs-lookup"><span data-stu-id="3cdd3-148">Warning</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-149">Tente assinar mais de uma assinatura de presença permitida por aplicativo</span><span class="sxs-lookup"><span data-stu-id="3cdd3-149">Attempt to subscribe more than the allowed presence subscriptions per application</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-150">Tente assinar mais de uma assinatura de presença permitida por aplicativo</span><span class="sxs-lookup"><span data-stu-id="3cdd3-150">Attempt to subscribe more than the allowed presence subscriptions per application</span></span></p>
<p><span data-ttu-id="3cdd3-151">Verifique se os clientes possuem assinaturas desnecessárias</span><span class="sxs-lookup"><span data-stu-id="3cdd3-151">Check the clients for unnecessary subscriptions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cdd3-152">20009</span><span class="sxs-lookup"><span data-stu-id="3cdd3-152">20009</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-153">Aviso</span><span class="sxs-lookup"><span data-stu-id="3cdd3-153">Warning</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-154">Tente assinar mais de uma assinatura de presença permitida por lote</span><span class="sxs-lookup"><span data-stu-id="3cdd3-154">Attempt to subscribe more than the allowed presence subscriptions per batch</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-155">Tente assinar mais de uma assinatura de presença permitida por lote</span><span class="sxs-lookup"><span data-stu-id="3cdd3-155">Attempt to subscribe more than the allowed presence subscriptions per batch</span></span></p>
<p><span data-ttu-id="3cdd3-156">Verifique se os clientes possuem assinaturas desnecessárias</span><span class="sxs-lookup"><span data-stu-id="3cdd3-156">Check the clients for unnecessary subscriptions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cdd3-157">20010</span><span class="sxs-lookup"><span data-stu-id="3cdd3-157">20010</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-158">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-158">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-159">Não é possível recuperar os dados inband</span><span class="sxs-lookup"><span data-stu-id="3cdd3-159">Cannot retrieve inband data</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-160">Não é possível recuperar os dados inband</span><span class="sxs-lookup"><span data-stu-id="3cdd3-160">Cannot retrieve inband data</span></span></p>
<p><span data-ttu-id="3cdd3-161">Se o problema persistir entre em contato com o suporte do produto</span><span class="sxs-lookup"><span data-stu-id="3cdd3-161">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cdd3-162">20011</span><span class="sxs-lookup"><span data-stu-id="3cdd3-162">20011</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-163">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-163">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-164">Não é possível assinar a presença</span><span class="sxs-lookup"><span data-stu-id="3cdd3-164">Cannot subscribe presence</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-165">Não é possível assinar a presença</span><span class="sxs-lookup"><span data-stu-id="3cdd3-165">Cannot subscribe presence</span></span></p>
<p><span data-ttu-id="3cdd3-166">Se o problema persistir entre em contato com o suporte do produto</span><span class="sxs-lookup"><span data-stu-id="3cdd3-166">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cdd3-167">20012</span><span class="sxs-lookup"><span data-stu-id="3cdd3-167">20012</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-168">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-168">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-169">Falha ao registrar o ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="3cdd3-169">Failed to register endpoint</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-170">Falha ao registrar o ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="3cdd3-170">Failed to register endpoint</span></span></p>
<p><span data-ttu-id="3cdd3-171">Se o problema persistir entre em contato com o suporte do produto</span><span class="sxs-lookup"><span data-stu-id="3cdd3-171">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cdd3-172">20013</span><span class="sxs-lookup"><span data-stu-id="3cdd3-172">20013</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-173">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-173">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-174">A MCU de IM não está disponível</span><span class="sxs-lookup"><span data-stu-id="3cdd3-174">IM MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-175">A MCU de IM não está disponível</span><span class="sxs-lookup"><span data-stu-id="3cdd3-175">IM MCU is unavailable</span></span></p>
<p><span data-ttu-id="3cdd3-176">Consulte se a MCU de IM está sendo executada</span><span class="sxs-lookup"><span data-stu-id="3cdd3-176">See whether IM MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cdd3-177">20014</span><span class="sxs-lookup"><span data-stu-id="3cdd3-177">20014</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-178">Informativo</span><span class="sxs-lookup"><span data-stu-id="3cdd3-178">Informational</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-179">Recuperação de uma falha ao conectar ao MCU de IM</span><span class="sxs-lookup"><span data-stu-id="3cdd3-179">Recovered from failing to connect to IM MCU</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-180">N/D</span><span class="sxs-lookup"><span data-stu-id="3cdd3-180">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cdd3-181">20015</span><span class="sxs-lookup"><span data-stu-id="3cdd3-181">20015</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-182">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-182">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-183">A MCU de AV não está disponível</span><span class="sxs-lookup"><span data-stu-id="3cdd3-183">AV MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-184">A MCU de AV não está disponível</span><span class="sxs-lookup"><span data-stu-id="3cdd3-184">AV MCU is unavailable</span></span></p>
<p><span data-ttu-id="3cdd3-185">Consulte se a MCU de AV está sendo executada</span><span class="sxs-lookup"><span data-stu-id="3cdd3-185">See whether AV MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cdd3-186">20016</span><span class="sxs-lookup"><span data-stu-id="3cdd3-186">20016</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-187">Informativo</span><span class="sxs-lookup"><span data-stu-id="3cdd3-187">Informational</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-188">Recuperação de uma falha ao conectar ao MCU de AV</span><span class="sxs-lookup"><span data-stu-id="3cdd3-188">Recovered from failing to connect to AV MCU</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-189">N/D</span><span class="sxs-lookup"><span data-stu-id="3cdd3-189">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cdd3-190">20017</span><span class="sxs-lookup"><span data-stu-id="3cdd3-190">20017</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-191">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-191">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-192">A MCU de AS não está disponível</span><span class="sxs-lookup"><span data-stu-id="3cdd3-192">AS MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-193">A MCU de AS não está disponível</span><span class="sxs-lookup"><span data-stu-id="3cdd3-193">AS MCU is unavailable</span></span></p>
<p><span data-ttu-id="3cdd3-194">Consulte se a MCU de AS está sendo executada</span><span class="sxs-lookup"><span data-stu-id="3cdd3-194">See whether AS MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cdd3-195">20018</span><span class="sxs-lookup"><span data-stu-id="3cdd3-195">20018</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-196">Informativo</span><span class="sxs-lookup"><span data-stu-id="3cdd3-196">Informational</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-197">Recuperação de uma falha ao conectar ao MCU de AS</span><span class="sxs-lookup"><span data-stu-id="3cdd3-197">Recovered from failing to connect to AS MCU</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-198">N/D</span><span class="sxs-lookup"><span data-stu-id="3cdd3-198">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cdd3-199">20019</span><span class="sxs-lookup"><span data-stu-id="3cdd3-199">20019</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-200">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-200">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-201">A MCU de Dados não está disponível</span><span class="sxs-lookup"><span data-stu-id="3cdd3-201">Data MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-202">A MCU de Dados não está disponível</span><span class="sxs-lookup"><span data-stu-id="3cdd3-202">Data MCU is unavailable</span></span></p>
<p><span data-ttu-id="3cdd3-203">Consulte se a MCU de Dados está sendo executada</span><span class="sxs-lookup"><span data-stu-id="3cdd3-203">See whether Data MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cdd3-204">20020</span><span class="sxs-lookup"><span data-stu-id="3cdd3-204">20020</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-205">Informativo</span><span class="sxs-lookup"><span data-stu-id="3cdd3-205">Informational</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-206">Recuperação de uma falha ao conectar ao MCU de dados</span><span class="sxs-lookup"><span data-stu-id="3cdd3-206">Recovered from failing to connect to Data MCU</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-207">N/D</span><span class="sxs-lookup"><span data-stu-id="3cdd3-207">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cdd3-208">20021</span><span class="sxs-lookup"><span data-stu-id="3cdd3-208">20021</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-209">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-209">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-210">Não é possível participar da MCU de IM</span><span class="sxs-lookup"><span data-stu-id="3cdd3-210">Cannot join IM MCU</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-211">Não é possível participar da MCU de IM</span><span class="sxs-lookup"><span data-stu-id="3cdd3-211">Cannot join IM MCU</span></span></p>
<p><span data-ttu-id="3cdd3-212">Consulte se a MCU de IM está sendo executada</span><span class="sxs-lookup"><span data-stu-id="3cdd3-212">See whether IM MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cdd3-213">20022</span><span class="sxs-lookup"><span data-stu-id="3cdd3-213">20022</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-214">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-214">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-215">Não é possível participar da MCU de AV</span><span class="sxs-lookup"><span data-stu-id="3cdd3-215">Cannot join AV MCU</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-216">Não é possível participar da MCU de AV</span><span class="sxs-lookup"><span data-stu-id="3cdd3-216">Cannot join AV MCU</span></span></p>
<p><span data-ttu-id="3cdd3-217">Consulte se a MCU de AV está sendo executada</span><span class="sxs-lookup"><span data-stu-id="3cdd3-217">See whether AV MCU is running</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cdd3-218">20023</span><span class="sxs-lookup"><span data-stu-id="3cdd3-218">20023</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-219">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-219">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-220">Não é possível participar da MCU de AS</span><span class="sxs-lookup"><span data-stu-id="3cdd3-220">Cannot join AS MCU</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-221">Não é possível participar da MCU de AS</span><span class="sxs-lookup"><span data-stu-id="3cdd3-221">Cannot join AS MCU</span></span></p>
<p><span data-ttu-id="3cdd3-222">Consulte se a MCU de AS está sendo executada</span><span class="sxs-lookup"><span data-stu-id="3cdd3-222">See whether AS MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cdd3-223">20024</span><span class="sxs-lookup"><span data-stu-id="3cdd3-223">20024</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-224">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-224">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-225">Não é possível participar da MCU de Dados</span><span class="sxs-lookup"><span data-stu-id="3cdd3-225">Cannot join Data MCU</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-226">Não é possível participar da MCU de Dados</span><span class="sxs-lookup"><span data-stu-id="3cdd3-226">Cannot join Data MCU</span></span></p>
<p><span data-ttu-id="3cdd3-227">Consulte se a MCU de Dados está sendo executada</span><span class="sxs-lookup"><span data-stu-id="3cdd3-227">See whether Data MCU is running</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cdd3-228">20025</span><span class="sxs-lookup"><span data-stu-id="3cdd3-228">20025</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-229">Erro</span><span class="sxs-lookup"><span data-stu-id="3cdd3-229">Error</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-230">Não é possível acessar o diretório ativo para foto</span><span class="sxs-lookup"><span data-stu-id="3cdd3-230">Cannot access active directory for photo</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-231">A conexão com o diretório ativo não está disponível</span><span class="sxs-lookup"><span data-stu-id="3cdd3-231">Connection to active directory is not available</span></span></p>
<p><span data-ttu-id="3cdd3-232">Certifique-se de que a conexão com o diretório ativo está disponível</span><span class="sxs-lookup"><span data-stu-id="3cdd3-232">Make sure the connection to active directory is available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cdd3-233">20026</span><span class="sxs-lookup"><span data-stu-id="3cdd3-233">20026</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-234">Informativo</span><span class="sxs-lookup"><span data-stu-id="3cdd3-234">Informational</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-235">Recuperação de falha ao acessar o diretório ativo para foto</span><span class="sxs-lookup"><span data-stu-id="3cdd3-235">Recovered from failing to access active directory for photo</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-236">N/D</span><span class="sxs-lookup"><span data-stu-id="3cdd3-236">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cdd3-237">20027</span><span class="sxs-lookup"><span data-stu-id="3cdd3-237">20027</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-238">Aviso</span><span class="sxs-lookup"><span data-stu-id="3cdd3-238">Warning</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-239">Não é possível desserializar</span><span class="sxs-lookup"><span data-stu-id="3cdd3-239">Cannot deserialize</span></span></p></td>
<td><p><span data-ttu-id="3cdd3-240">Não é possível desserializar</span><span class="sxs-lookup"><span data-stu-id="3cdd3-240">Cannot deserialize</span></span></p>
<p><span data-ttu-id="3cdd3-241">Se o problema persistir entre em contato com o suporte do produto</span><span class="sxs-lookup"><span data-stu-id="3cdd3-241">If the problem persists contact product support</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3cdd3-242">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3cdd3-242">


</div>

<span> </span>

</div>

</div>

</span></span></div>

