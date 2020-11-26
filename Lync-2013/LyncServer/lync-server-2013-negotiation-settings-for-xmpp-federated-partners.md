---
title: 'Lync Server 2013: Configurações de negociação para parceiros de XMPP federados'
description: 'Lync Server 2013: configurações de negociação para parceiros federados XMPP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Negotiation settings for XMPP federated partners
ms:assetid: ef773942-ef92-4f71-85a1-738dfebdfa00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552456(v=OCS.15)
ms:contentKeyID: 48679567
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ac3d9c69d407dc750a1afb35f0a448869a88f09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445580"
---
# <a name="negotiation-settings-for-xmpp-federated-partners-in-lync-server-2013"></a><span data-ttu-id="32eca-103">Configurações de negociação para parceiros de XMPP federados no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32eca-103">Negotiation settings for XMPP federated partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="32eca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="32eca-104">

<span> </span></span></span>

<span data-ttu-id="32eca-105">_**Tópico da última modificação:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="32eca-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="32eca-106">As configurações dos tipos de negociação na configuração de um parceiro do XMPP têm uma ampla variedade de combinações possíveis.</span><span class="sxs-lookup"><span data-stu-id="32eca-106">The settings for the negotiation types in the configuration of an XMPP Partner have a wide variety of possible combinations.</span></span> <span data-ttu-id="32eca-107">Nem todas essas combinações são válidas.</span><span class="sxs-lookup"><span data-stu-id="32eca-107">Not all of these combinations are valid.</span></span> <span data-ttu-id="32eca-108">A tabela detalhada neste tópico definirá as configurações válidas e inválidas.</span><span class="sxs-lookup"><span data-stu-id="32eca-108">The table detailed in this topic will define the valid and not valid settings.</span></span> <span data-ttu-id="32eca-109">As configurações comuns são apresentadas na primeira tabela, a segunda tabela que detalha todas as combinações possíveis.</span><span class="sxs-lookup"><span data-stu-id="32eca-109">Common configurations are presented in the first table, the second table detailing all possible combinations.</span></span> <span data-ttu-id="32eca-110">Observe que você não pode ter a *autenticação simples e a camada de segurança* (SASL) **, a menos** que o TLS ( *Transport Layer Security* ) também esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="32eca-110">Note that you cannot have *Simple Authentication and Security Layer* (SASL) **unless** *Transport Layer Security* (TLS) is also available.</span></span> <span data-ttu-id="32eca-111">SASL é enviada em um formato não criptografado (legível) e nunca deve ser transmitida, a menos que seja protegida por outro meio, como TLS.</span><span class="sxs-lookup"><span data-stu-id="32eca-111">SASL is sent in an unencrypted (readable) format and should never be transmitted unless protected by another means, such as TLS.</span></span>

### <a name="common-xmpp-federation-negotiation-methods"></a><span data-ttu-id="32eca-112">Métodos comuns de negociação de Federação XMPP</span><span class="sxs-lookup"><span data-stu-id="32eca-112">Common XMPP Federation Negotiation Methods</span></span>

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
<th><span data-ttu-id="32eca-113">Transport Layer Security (TLS)</span><span class="sxs-lookup"><span data-stu-id="32eca-113">Transport Layer Security (TLS)</span></span></th>
<th><span data-ttu-id="32eca-114">Camada de segurança e autenticação simples (SASL)</span><span class="sxs-lookup"><span data-stu-id="32eca-114">Simple Authentication and Security Layer (SASL)</span></span></th>
<th><span data-ttu-id="32eca-115">Autenticação Dialback</span><span class="sxs-lookup"><span data-stu-id="32eca-115">Dialback Authentication</span></span></th>
<th><span data-ttu-id="32eca-116">Método (s) de autenticação esperado (s)</span><span class="sxs-lookup"><span data-stu-id="32eca-116">Expected Authentication Method(s)</span></span></th>
<th><span data-ttu-id="32eca-117">Observações</span><span class="sxs-lookup"><span data-stu-id="32eca-117">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32eca-118">Obrigatório </span><span class="sxs-lookup"><span data-stu-id="32eca-118">Required</span></span></p></td>
<td><p><span data-ttu-id="32eca-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="32eca-119">Required</span></span></p></td>
<td><p><span data-ttu-id="32eca-120">Falso</span><span class="sxs-lookup"><span data-stu-id="32eca-120">False</span></span></p></td>
<td><p><span data-ttu-id="32eca-121">SASL sobre TLS</span><span class="sxs-lookup"><span data-stu-id="32eca-121">SASL over TLS</span></span></p></td>
<td><p><span data-ttu-id="32eca-122">O TLS e o SASL são necessários ajuda a garantir que o fluxo de mensagens SASL seja seguro.</span><span class="sxs-lookup"><span data-stu-id="32eca-122">TLS and SASL required helps to ensure that the SASL message stream is secure.</span></span> <span data-ttu-id="32eca-123">Dialback não está disponível e não pode ser usado para um método de fallback se o parceiro federado do XMPP não definiu o TLS como obrigatório ou opcional.</span><span class="sxs-lookup"><span data-stu-id="32eca-123">Dialback is not available and cannot be used for a fallback method if the XMPP federated partner has not set TLS to required or optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32eca-124">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="32eca-124">Required</span></span></p></td>
<td><p><span data-ttu-id="32eca-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="32eca-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eca-126">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="32eca-126">True</span></span></p></td>
<td><p><span data-ttu-id="32eca-127">SASL sobre TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="32eca-127">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="32eca-128">Ao exigir TLS, se o parceiro federado do XMPP tiver sido definido SASL para opcional ou obrigatório, o SASL será usado.</span><span class="sxs-lookup"><span data-stu-id="32eca-128">By requiring TLS, if the XMPP federated partner has set SASL to optional or required SASL is used.</span></span> <span data-ttu-id="32eca-129">Se SASL não estiver disponível, o Dialback em TLS será usado.</span><span class="sxs-lookup"><span data-stu-id="32eca-129">If SASL is not available, Dialback over TLS will be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32eca-130">Opcional </span><span class="sxs-lookup"><span data-stu-id="32eca-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eca-131">Opcional</span><span class="sxs-lookup"><span data-stu-id="32eca-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eca-132">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="32eca-132">True</span></span></p></td>
<td><p><span data-ttu-id="32eca-133">SASL sobre TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="32eca-133">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="32eca-134">Embora seja bastante flexível nos métodos de negociação oferecidos, essas configurações dependem das configurações do parceiro de Federação do XMPP.</span><span class="sxs-lookup"><span data-stu-id="32eca-134">While very flexible in the negotiation methods offered, these settings rely on the XMPP federation partner’s settings.</span></span> <span data-ttu-id="32eca-135">Se o parceiro tiver o TLS opcional ou obrigatório, mas o SASL não for compatível, o TLS Dialback estará disponível.</span><span class="sxs-lookup"><span data-stu-id="32eca-135">If the partner has TLS optional or required but SASL is not supported, TLS Dialback will be available.</span></span> <span data-ttu-id="32eca-136">Se o parceiro tiver TLS e SASL definido como opcional ou obrigatório, a seleção ideal de TLS sobre o SASL será usada.</span><span class="sxs-lookup"><span data-stu-id="32eca-136">If the partner has TLS and SASL set to optional or required, the optimal selection of TLS over SASL is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32eca-137">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="32eca-137">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="32eca-138">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="32eca-138">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="32eca-139">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="32eca-139">True</span></span></p></td>
<td><p><span data-ttu-id="32eca-140">TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="32eca-140">TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="32eca-141">Em muitos casos, o TCP Dialback é a única solução possível.</span><span class="sxs-lookup"><span data-stu-id="32eca-141">In many cases, TCP Dialback is the only possible solution.</span></span> <span data-ttu-id="32eca-142">Menos desejável do que outras opções, ele fornece um certo nível de confiança.</span><span class="sxs-lookup"><span data-stu-id="32eca-142">Less desirable than other options, it does provide some level of trust.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="xmpp-federation-negotiation-methods-matrix---complete"></a><span data-ttu-id="32eca-143">Matriz de métodos de negociação de Federação XMPP-concluída</span><span class="sxs-lookup"><span data-stu-id="32eca-143">XMPP Federation Negotiation Methods Matrix - Complete</span></span>

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
<th><span data-ttu-id="32eca-144">Transport Layer Security (TLS)</span><span class="sxs-lookup"><span data-stu-id="32eca-144">Transport Layer Security (TLS)</span></span></th>
<th><span data-ttu-id="32eca-145">Camada de segurança e autenticação simples (SASL)</span><span class="sxs-lookup"><span data-stu-id="32eca-145">Simple Authentication and Security Layer (SASL)</span></span></th>
<th><span data-ttu-id="32eca-146">Autenticação Dialback</span><span class="sxs-lookup"><span data-stu-id="32eca-146">Dialback Authentication</span></span></th>
<th><span data-ttu-id="32eca-147">Método de autenticação esperado</span><span class="sxs-lookup"><span data-stu-id="32eca-147">Expected Authentication Method</span></span></th>
<th><span data-ttu-id="32eca-148">Observações, aviso ou erro para uma configuração inválida</span><span class="sxs-lookup"><span data-stu-id="32eca-148">Notes, Warning or Error for Not Valid Configuration</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32eca-149">Obrigatório </span><span class="sxs-lookup"><span data-stu-id="32eca-149">Required</span></span></p></td>
<td><p><span data-ttu-id="32eca-150">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="32eca-150">Required</span></span></p></td>
<td><p><span data-ttu-id="32eca-151">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="32eca-151">True</span></span></p></td>
<td><p><span data-ttu-id="32eca-152">SASL sobre TLS</span><span class="sxs-lookup"><span data-stu-id="32eca-152">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="32eca-153">O Dialback não funcionará se o SASL e o TLS forem obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="32eca-153">Dialback will not operate if both SASL and TLS are required.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32eca-154">Obrigatório </span><span class="sxs-lookup"><span data-stu-id="32eca-154">Required</span></span></p></td>
<td><p><span data-ttu-id="32eca-155">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="32eca-155">Required</span></span></p></td>
<td><p><span data-ttu-id="32eca-156">Falso</span><span class="sxs-lookup"><span data-stu-id="32eca-156">False</span></span></p></td>
<td><p><span data-ttu-id="32eca-157">SASL sobre TLS</span><span class="sxs-lookup"><span data-stu-id="32eca-157">SASL over TLS</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32eca-158">Opcional</span><span class="sxs-lookup"><span data-stu-id="32eca-158">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eca-159">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="32eca-159">Required</span></span></p></td>
<td><p><span data-ttu-id="32eca-160">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="32eca-160">True</span></span></p></td>
<td><p><span data-ttu-id="32eca-161">SASL sobre TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="32eca-161">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="32eca-162">SASL requer TLS.</span><span class="sxs-lookup"><span data-stu-id="32eca-162">SASL requires TLS.</span></span> <span data-ttu-id="32eca-163">Permitir que o TLS seja opcional pode resultar em negociações de sessão com falha.</span><span class="sxs-lookup"><span data-stu-id="32eca-163">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32eca-164">Opcional</span><span class="sxs-lookup"><span data-stu-id="32eca-164">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eca-165">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="32eca-165">Required</span></span></p></td>
<td><p><span data-ttu-id="32eca-166">Falso</span><span class="sxs-lookup"><span data-stu-id="32eca-166">False</span></span></p></td>
<td><p><span data-ttu-id="32eca-167">SASL sobre TLS</span><span class="sxs-lookup"><span data-stu-id="32eca-167">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="32eca-168">SASL requer TLS.</span><span class="sxs-lookup"><span data-stu-id="32eca-168">SASL requires TLS.</span></span> <span data-ttu-id="32eca-169">Permitir que o TLS seja opcional pode resultar em negociações de sessão com falha.</span><span class="sxs-lookup"><span data-stu-id="32eca-169">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32eca-170">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="32eca-170">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="32eca-171">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="32eca-171">Required</span></span></p></td>
<td><p><span data-ttu-id="32eca-172">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="32eca-172">True</span></span></p></td>
<td><p><span data-ttu-id="32eca-173">TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="32eca-173">TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="32eca-174">SASL requer TLS.</span><span class="sxs-lookup"><span data-stu-id="32eca-174">SASL requires TLS.</span></span> <span data-ttu-id="32eca-175">Permitir que o TLS seja opcional pode resultar em negociações de sessão com falha.</span><span class="sxs-lookup"><span data-stu-id="32eca-175">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32eca-176">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="32eca-176">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="32eca-177">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="32eca-177">Required</span></span></p></td>
<td><p><span data-ttu-id="32eca-178">Falso</span><span class="sxs-lookup"><span data-stu-id="32eca-178">False</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="32eca-179">Configuração inválida</span><span class="sxs-lookup"><span data-stu-id="32eca-179">Not Valid Configuration</span></span>


</div></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="32eca-180">Como a SASL requer TLS, e o TLS não está disponível, o SASL/TLS não pode ser bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="32eca-180">Because SASL requires TLS, and TLS is not available, SASL/TLS cannot succeed.</span></span> <span data-ttu-id="32eca-181">TCP Dialback é definido como false e não pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="32eca-181">TCP Dialback is set to false, and cannot be used.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32eca-182">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="32eca-182">Required</span></span></p></td>
<td><p><span data-ttu-id="32eca-183">Opcional</span><span class="sxs-lookup"><span data-stu-id="32eca-183">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eca-184">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="32eca-184">True</span></span></p></td>
<td><p><span data-ttu-id="32eca-185">SASL sobre TLS, TLS Dialback</span><span class="sxs-lookup"><span data-stu-id="32eca-185">SASL over TLS, TLS Dialback</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32eca-186">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="32eca-186">Required</span></span></p></td>
<td><p><span data-ttu-id="32eca-187">Opcional</span><span class="sxs-lookup"><span data-stu-id="32eca-187">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eca-188">Falso</span><span class="sxs-lookup"><span data-stu-id="32eca-188">False</span></span></p></td>
<td><p><span data-ttu-id="32eca-189">SASL sobre TLS</span><span class="sxs-lookup"><span data-stu-id="32eca-189">SASL over TLS</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32eca-190">Opcional </span><span class="sxs-lookup"><span data-stu-id="32eca-190">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eca-191">Opcional</span><span class="sxs-lookup"><span data-stu-id="32eca-191">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eca-192">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="32eca-192">True</span></span></p></td>
<td><p><span data-ttu-id="32eca-193">SASL sobre TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="32eca-193">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="32eca-194">SASL requer TLS.</span><span class="sxs-lookup"><span data-stu-id="32eca-194">SASL requires TLS.</span></span> <span data-ttu-id="32eca-195">Permitir que o TLS seja opcional pode resultar em negociações de sessão com falha.</span><span class="sxs-lookup"><span data-stu-id="32eca-195">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32eca-196">Opcional </span><span class="sxs-lookup"><span data-stu-id="32eca-196">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eca-197">Opcional</span><span class="sxs-lookup"><span data-stu-id="32eca-197">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eca-198">Falso</span><span class="sxs-lookup"><span data-stu-id="32eca-198">False</span></span></p></td>
<td><p><span data-ttu-id="32eca-199">SASL sobre TLS</span><span class="sxs-lookup"><span data-stu-id="32eca-199">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="32eca-200">SASL requer TLS.</span><span class="sxs-lookup"><span data-stu-id="32eca-200">SASL requires TLS.</span></span> <span data-ttu-id="32eca-201">Permitir que o TLS seja opcional pode resultar em negociações de sessão com falha.</span><span class="sxs-lookup"><span data-stu-id="32eca-201">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32eca-202">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="32eca-202">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="32eca-203">Opcional</span><span class="sxs-lookup"><span data-stu-id="32eca-203">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eca-204">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="32eca-204">True</span></span></p></td>
<td><p><span data-ttu-id="32eca-205">TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="32eca-205">TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="32eca-206">SASL requer TLS.</span><span class="sxs-lookup"><span data-stu-id="32eca-206">SASL requires TLS.</span></span> <span data-ttu-id="32eca-207">Permitir que o TLS seja opcional pode resultar em negociações de sessão com falha.</span><span class="sxs-lookup"><span data-stu-id="32eca-207">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32eca-208">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="32eca-208">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="32eca-209">Opcional</span><span class="sxs-lookup"><span data-stu-id="32eca-209">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eca-210">Falso</span><span class="sxs-lookup"><span data-stu-id="32eca-210">False</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="32eca-211">Configuração inválida</span><span class="sxs-lookup"><span data-stu-id="32eca-211">Not Valid Configuration</span></span>


</div></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="32eca-212">SASL requer TLS.</span><span class="sxs-lookup"><span data-stu-id="32eca-212">SASL requires TLS.</span></span> <span data-ttu-id="32eca-213">Permitir que o TLS seja opcional pode resultar em negociações de sessão com falha.</span><span class="sxs-lookup"><span data-stu-id="32eca-213">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32eca-214">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="32eca-214">Required</span></span></p></td>
<td><p><span data-ttu-id="32eca-215">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="32eca-215">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="32eca-216">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="32eca-216">True</span></span></p></td>
<td><p><span data-ttu-id="32eca-217">TLS Dialback</span><span class="sxs-lookup"><span data-stu-id="32eca-217">TLS Dialback</span></span></p></td>
<td><p><span data-ttu-id="32eca-218">A configuração permite o TLS Dialback.</span><span class="sxs-lookup"><span data-stu-id="32eca-218">Configuration allows for TLS Dialback.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32eca-219">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="32eca-219">Required</span></span></p></td>
<td><p><span data-ttu-id="32eca-220">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="32eca-220">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="32eca-221">Falso</span><span class="sxs-lookup"><span data-stu-id="32eca-221">False</span></span></p></td>
<td><p><span data-ttu-id="32eca-222">Configuração inválida</span><span class="sxs-lookup"><span data-stu-id="32eca-222">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="32eca-223">SASL ou Dialback devem ser habilitados.</span><span class="sxs-lookup"><span data-stu-id="32eca-223">SASL or Dialback must be enabled.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32eca-224">Opcional</span><span class="sxs-lookup"><span data-stu-id="32eca-224">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eca-225">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="32eca-225">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="32eca-226">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="32eca-226">True</span></span></p></td>
<td><p><span data-ttu-id="32eca-227">TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="32eca-227">TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="32eca-228">Com base nas opções de negociação do outro ponto de extremidade, o TCP ou o TLS Dialback será aceito.</span><span class="sxs-lookup"><span data-stu-id="32eca-228">Based on negotiation choices of the other end point, TCP or TLS Dialback will be accepted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32eca-229">Opcional</span><span class="sxs-lookup"><span data-stu-id="32eca-229">Optional</span></span></p></td>
<td><p><span data-ttu-id="32eca-230">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="32eca-230">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="32eca-231">Falso</span><span class="sxs-lookup"><span data-stu-id="32eca-231">False</span></span></p></td>
<td><p><span data-ttu-id="32eca-232">Configuração inválida</span><span class="sxs-lookup"><span data-stu-id="32eca-232">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="32eca-233">SASL ou Dialback devem ser habilitados.</span><span class="sxs-lookup"><span data-stu-id="32eca-233">SASL or Dialback must be enabled.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32eca-234">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="32eca-234">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="32eca-235">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="32eca-235">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="32eca-236">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="32eca-236">True</span></span></p></td>
<td><p><span data-ttu-id="32eca-237">TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="32eca-237">TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="32eca-238">O TCP Dialback é o único método de negociação disponível</span><span class="sxs-lookup"><span data-stu-id="32eca-238">TCP Dialback is the only negotiation method available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32eca-239">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="32eca-239">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="32eca-240">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="32eca-240">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="32eca-241">Falso</span><span class="sxs-lookup"><span data-stu-id="32eca-241">False</span></span></p></td>
<td><p><span data-ttu-id="32eca-242">Configuração inválida</span><span class="sxs-lookup"><span data-stu-id="32eca-242">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="32eca-243">SASL ou Dialback devem ser habilitados.</span><span class="sxs-lookup"><span data-stu-id="32eca-243">SASL or Dialback must be enabled.</span></span>


<span data-ttu-id="32eca-244"></div></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="32eca-244"></div></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

