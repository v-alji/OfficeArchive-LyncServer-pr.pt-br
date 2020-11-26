---
title: 'Lync Server 2013: Planejamento de capacidade para Grupo de Resposta'
description: 'Lync Server 2013: planejamento de capacidade para grupo de resposta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning for Response Group
ms:assetid: a2459a69-1f45-4f2f-bca5-d4f442708e44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412754(v=OCS.15)
ms:contentKeyID: 48184951
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 78c543f558f67deaaeb781b308aa5f68d39cd785
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435527"
---
# <a name="capacity-planning-for-response-group-in-lync-server-2013"></a><span data-ttu-id="722e7-103">Planejamento de capacidade para Grupo de Resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="722e7-103">Capacity planning for Response Group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="722e7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="722e7-104">

<span> </span></span></span>

<span data-ttu-id="722e7-105">_**Tópico da última modificação:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="722e7-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<div id="sectionSection0" class="section">

<span data-ttu-id="722e7-106">A tabela a seguir descreve o modelo de usuário do grupo de resposta que você pode usar como base para requisitos de planejamento de capacidade.</span><span class="sxs-lookup"><span data-stu-id="722e7-106">The following table describes the Response Group user model that you can use as the basis for capacity planning requirements.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="722e7-107">Os números na tabela a seguir pressupõem que você use arquivos Wave de 16 bits (. wav) de 16 bits para todos os arquivos de áudio do grupo de resposta.</span><span class="sxs-lookup"><span data-stu-id="722e7-107">The numbers in the following table assume that you use 16 kHz, mono, 16-bit Wave (.wav) files for all response group audio files.</span></span> <span data-ttu-id="722e7-108">Se você usar outros formatos de arquivo, como o áudio do Windows Media (. WMA), os números podem variar.</span><span class="sxs-lookup"><span data-stu-id="722e7-108">If you use other file formats, such as Windows Media Audio (.wma), the numbers may vary.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="722e7-109">Lembre-se de que, para o planejamento da capacidade de recuperação de desastres, cada pool de um pool emparelhado deve ser capaz de manipular as cargas de trabalho para todos os grupos de resposta em ambos os pools.</span><span class="sxs-lookup"><span data-stu-id="722e7-109">Keep in mind that for disaster recovery capacity planning, each pool of a paired pool should be able to handle the workloads for all the response groups in both pools.</span></span>



</div>

### <a name="response-group-user-model"></a><span data-ttu-id="722e7-110">Modelo de usuário do grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="722e7-110">Response Group User Model</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="722e7-111">Indicador</span><span class="sxs-lookup"><span data-stu-id="722e7-111">Metric</span></span></th>
<th><span data-ttu-id="722e7-112">Por pool de edição para empresas (com 8 servidores front end)</span><span class="sxs-lookup"><span data-stu-id="722e7-112">Per Enterprise Edition pool (With 8 Front End Servers)</span></span></th>
<th><span data-ttu-id="722e7-113">Por servidor padrão da edição</span><span class="sxs-lookup"><span data-stu-id="722e7-113">Per Standard Edition server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="722e7-114">Chamadas recebidas por segundo</span><span class="sxs-lookup"><span data-stu-id="722e7-114">Incoming calls per second</span></span></p></td>
<td><p><span data-ttu-id="722e7-115">16</span><span class="sxs-lookup"><span data-stu-id="722e7-115">16</span></span></p></td>
<td><p><span data-ttu-id="722e7-116">2</span><span class="sxs-lookup"><span data-stu-id="722e7-116">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="722e7-117">Chamadas simultâneas conectadas ao IVR ou MoH</span><span class="sxs-lookup"><span data-stu-id="722e7-117">Concurrent calls connected to IVR or MoH</span></span></p></td>
<td><p><span data-ttu-id="722e7-118">480</span><span class="sxs-lookup"><span data-stu-id="722e7-118">480</span></span></p></td>
<td><p><span data-ttu-id="722e7-119">60</span><span class="sxs-lookup"><span data-stu-id="722e7-119">60</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="722e7-120">Sessões anônimas simultâneas (sem mensagens instantâneas)</span><span class="sxs-lookup"><span data-stu-id="722e7-120">Concurrent anonymous sessions (without IM)</span></span></p></td>
<td><p><span data-ttu-id="722e7-121">224</span><span class="sxs-lookup"><span data-stu-id="722e7-121">224</span></span></p></td>
<td><p><span data-ttu-id="722e7-122">28</span><span class="sxs-lookup"><span data-stu-id="722e7-122">28</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="722e7-123">Sessões anônimas simultâneas (com mensagens instantâneas)</span><span class="sxs-lookup"><span data-stu-id="722e7-123">Concurrent anonymous sessions (with IM)</span></span></p></td>
<td><p><span data-ttu-id="722e7-124">64</span><span class="sxs-lookup"><span data-stu-id="722e7-124">64</span></span></p></td>
<td><p><span data-ttu-id="722e7-125">8</span><span class="sxs-lookup"><span data-stu-id="722e7-125">8</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="722e7-126">Agentes ativos (formais e informais)</span><span class="sxs-lookup"><span data-stu-id="722e7-126">Active agents (formal and informal)</span></span></p></td>
<td><p><span data-ttu-id="722e7-127">1200</span><span class="sxs-lookup"><span data-stu-id="722e7-127">1200</span></span></p></td>
<td><p><span data-ttu-id="722e7-128">1200</span><span class="sxs-lookup"><span data-stu-id="722e7-128">1200</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="722e7-129">Número de grupos de busca</span><span class="sxs-lookup"><span data-stu-id="722e7-129">Number of hunt groups</span></span></p></td>
<td><p><span data-ttu-id="722e7-130">400</span><span class="sxs-lookup"><span data-stu-id="722e7-130">400</span></span></p></td>
<td><p><span data-ttu-id="722e7-131">400</span><span class="sxs-lookup"><span data-stu-id="722e7-131">400</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="722e7-132">Número de grupos IVR (usar reconhecimento de fala)</span><span class="sxs-lookup"><span data-stu-id="722e7-132">Number of IVR groups (use speech recognition)</span></span></p></td>
<td><p><span data-ttu-id="722e7-133">200</span><span class="sxs-lookup"><span data-stu-id="722e7-133">200</span></span></p></td>
<td><p><span data-ttu-id="722e7-134">200</span><span class="sxs-lookup"><span data-stu-id="722e7-134">200</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="722e7-135">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="722e7-135">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

