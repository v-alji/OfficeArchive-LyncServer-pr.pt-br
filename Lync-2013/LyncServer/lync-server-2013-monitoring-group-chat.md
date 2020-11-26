---
title: 'Lync Server 2013: monitorando o chat em grupo'
description: 'Lync Server 2013: monitorando o chat em grupo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring group chat
ms:assetid: bddcf0be-ebf3-46bc-90c7-2576877734fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720924(v=OCS.15)
ms:contentKeyID: 63969648
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 625e45f455e8dba50a5fa64240b62cb010623d16
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425420"
---
# <a name="monitoring-group-chat-in-lync-server-2013"></a><span data-ttu-id="2d9ad-103">Monitorar o chat em grupo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2d9ad-103">Monitoring group chat in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2d9ad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2d9ad-104">

<span> </span></span></span>

<span data-ttu-id="2d9ad-105">_**Tópico da última modificação:** 2014-08-04_</span><span class="sxs-lookup"><span data-stu-id="2d9ad-105">_**Topic Last Modified:** 2014-08-04_</span></span>

<span data-ttu-id="2d9ad-106">É altamente recomendável executar o [instalador de atualização cumulativa do servidor](https://support.microsoft.com/kb/968802) mais recente disponível no centro de download da Microsoft para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="2d9ad-106">We highly recommend running the most recent [Cumulative Server Update Installer](https://support.microsoft.com/kb/968802) available on the Microsoft Download Center for performance improvements.</span></span>

<span data-ttu-id="2d9ad-107">Pressupondo que você esteja executando a atualização cumulativa mais recente, use a seguinte tabela de teste de stress para métricas a fim de compreender se seus servidores de chat em grupo estão sendo executados na integridade ideal.</span><span class="sxs-lookup"><span data-stu-id="2d9ad-107">Assuming you are running latest cumulative update, use the following stress test table for metrics to understand if your Group Chat Servers are running at optimal health.</span></span>

### <a name="test-environment-and-user-model"></a><span data-ttu-id="2d9ad-108">Ambiente de teste e modelo de usuário</span><span class="sxs-lookup"><span data-stu-id="2d9ad-108">Test environment and user model</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d9ad-109">Três servidores de chat em grupo em um pool de chat em grupo, cada um com 8 GB de memória e 8 processadores.</span><span class="sxs-lookup"><span data-stu-id="2d9ad-109">Three Group Chat Servers in a Group Chat pool, each with 8 GB memory and 8 processors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9ad-110">Duas front-ends do Lync Server 2013 na Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="2d9ad-110">Two Lync Server 2013 Front Ends in Enterprise Edition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9ad-111">60.000 usuários simultâneos em três servidores de chat em grupo.</span><span class="sxs-lookup"><span data-stu-id="2d9ad-111">60,000 concurrent users across three Group Chat Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9ad-112">25.000 canais hospedados pelo pool de chat em grupo.</span><span class="sxs-lookup"><span data-stu-id="2d9ad-112">25,000 channels hosted by Group Chat Pool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9ad-113">Tamanho do canal:</span><span class="sxs-lookup"><span data-stu-id="2d9ad-113">Channel Size:</span></span></p>
<ul>
<li><p><span data-ttu-id="2d9ad-114">Tamanho do canal pequeno: 30</span><span class="sxs-lookup"><span data-stu-id="2d9ad-114">Small Channel Size: 30</span></span></p></li>
<li><p><span data-ttu-id="2d9ad-115">Tamanho médio do canal: 150</span><span class="sxs-lookup"><span data-stu-id="2d9ad-115">Medium Channel Size: 150</span></span></p></li>
<li><p><span data-ttu-id="2d9ad-116">Tamanho do canal grande: 2500</span><span class="sxs-lookup"><span data-stu-id="2d9ad-116">Large Channel Size: 2500</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9ad-117">Contagem de canais:</span><span class="sxs-lookup"><span data-stu-id="2d9ad-117">Channel Count:</span></span></p>
<ul>
<li><p><span data-ttu-id="2d9ad-118">Número pequeno de canais: 24.000</span><span class="sxs-lookup"><span data-stu-id="2d9ad-118">Number small channels: 24,000</span></span></p></li>
<li><p><span data-ttu-id="2d9ad-119">Número médio de canais médio 800</span><span class="sxs-lookup"><span data-stu-id="2d9ad-119">Number medium channels 800</span></span></p></li>
<li><p><span data-ttu-id="2d9ad-120">Número maior de canais 24</span><span class="sxs-lookup"><span data-stu-id="2d9ad-120">Number large channels 24</span></span></p></li>
<li><p><span data-ttu-id="2d9ad-121">Total de canais 24.824</span><span class="sxs-lookup"><span data-stu-id="2d9ad-121">Total Channels 24,824</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9ad-122">Convidar canais:</span><span class="sxs-lookup"><span data-stu-id="2d9ad-122">Invite channels:</span></span></p>
<ul>
<li><p><span data-ttu-id="2d9ad-123">Metade dos canais eram convidados canais</span><span class="sxs-lookup"><span data-stu-id="2d9ad-123">Half the channels were invite channels</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9ad-124">Número de canais que um usuário ingressa:</span><span class="sxs-lookup"><span data-stu-id="2d9ad-124">Number of channels a user joins:</span></span></p>
<ul>
<li><p><span data-ttu-id="2d9ad-125">Pequeno: 12</span><span class="sxs-lookup"><span data-stu-id="2d9ad-125">Small: 12</span></span></p></li>
<li><p><span data-ttu-id="2d9ad-126">Média: 2</span><span class="sxs-lookup"><span data-stu-id="2d9ad-126">Medium: 2</span></span></p></li>
<li><p><span data-ttu-id="2d9ad-127">Grande: 1</span><span class="sxs-lookup"><span data-stu-id="2d9ad-127">Large: 1</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9ad-128">Taxa de junção:</span><span class="sxs-lookup"><span data-stu-id="2d9ad-128">Join rate:</span></span></p>
<ul>
<li><p><span data-ttu-id="2d9ad-129">10 total/segundo, 3,33/segundo por servidor</span><span class="sxs-lookup"><span data-stu-id="2d9ad-129">10 total/second, 3.33/second per server</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9ad-130">Taxa de logout:</span><span class="sxs-lookup"><span data-stu-id="2d9ad-130">Logout rate:</span></span></p>
<ul>
<li><p><span data-ttu-id="2d9ad-131">10 total/segundo, 3,33/segundo por servidor</span><span class="sxs-lookup"><span data-stu-id="2d9ad-131">10 total/second, 3.33/second per server</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9ad-132">Tarifa de chat:</span><span class="sxs-lookup"><span data-stu-id="2d9ad-132">Chat rate:</span></span></p>
<ul>
<li><p><span data-ttu-id="2d9ad-133">20 totais/segundo, 6.66/segundo por servidor</span><span class="sxs-lookup"><span data-stu-id="2d9ad-133">20 total/second, 6.66/second per server</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <span data-ttu-id="2d9ad-134">Os seguintes números de contador de desempenho provavelmente variam quando são usadas diferentes especificações de hardware ou perfis de usuário.</span><span class="sxs-lookup"><span data-stu-id="2d9ad-134">The following performance counter numbers will likely vary when different hardware specifications or user profiles are used.</span></span>



</div>

### <a name="performance-counter-to-be-monitored"></a><span data-ttu-id="2d9ad-135">Contador de desempenho a ser monitorado</span><span class="sxs-lookup"><span data-stu-id="2d9ad-135">Performance counter to be monitored</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2d9ad-136">Contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="2d9ad-136">Performance Counter</span></span></th>
<th><span data-ttu-id="2d9ad-137">Limites</span><span class="sxs-lookup"><span data-stu-id="2d9ad-137">Thresholds</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d9ad-138">Processo (ChannelService)- &gt; % tempo do processador</span><span class="sxs-lookup"><span data-stu-id="2d9ad-138">Process(ChannelService)-&gt;%Processor Time</span></span></p></td>
<td><p><span data-ttu-id="2d9ad-139">Mín: 0</span><span class="sxs-lookup"><span data-stu-id="2d9ad-139">Min: 0</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2d9ad-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2d9ad-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

