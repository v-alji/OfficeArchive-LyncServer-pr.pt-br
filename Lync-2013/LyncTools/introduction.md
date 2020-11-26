---
title: Introdução
description: Introdução.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Introduction
ms:assetid: 276395be-93df-4a16-97e2-cb468cd0f2e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945588(v=OCS.15)
ms:contentKeyID: 51541414
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8eb847c499bde077ccaf2aa050de801ceeedcc6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438740"
---
# <a name="introduction"></a><span data-ttu-id="75b0d-103">Introdução</span><span class="sxs-lookup"><span data-stu-id="75b0d-103">Introduction</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="75b0d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="75b0d-104">

<span> </span></span></span>

<span data-ttu-id="75b0d-105">_**Tópico da última modificação:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="75b0d-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="75b0d-106">A ferramenta de stress e desempenho do Lync Server 2013 (conhecida como LyncPerfTool) pode simular a carga do usuário dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="75b0d-106">The Lync Server 2013 Stress and Performance Tool (referred to as LyncPerfTool) can simulate user load of the following types:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75b0d-107">Mensagens instantâneas (IM) e presença</span><span class="sxs-lookup"><span data-stu-id="75b0d-107">Instant messaging (IM) and presence</span></span></p></td>
<td><p><span data-ttu-id="75b0d-108">Audioconferência</span><span class="sxs-lookup"><span data-stu-id="75b0d-108">Audio conferencing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b0d-109">Compartilhamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="75b0d-109">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="75b0d-110">Voz sobre IP (VoIP), incluindo simulação de rede telefônica pública comutada (PSTN)</span><span class="sxs-lookup"><span data-stu-id="75b0d-110">Voice over IP (VoIP), including public switched telephone network (PSTN) simulation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b0d-111">Conferência de cliente de acesso Web</span><span class="sxs-lookup"><span data-stu-id="75b0d-111">Web Access Client conferencing</span></span></p></td>
<td><p><span data-ttu-id="75b0d-112">Microsoft Lync 2013 Attendant</span><span class="sxs-lookup"><span data-stu-id="75b0d-112">Microsoft Lync 2013 Attendant</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b0d-113">Grupos de resposta</span><span class="sxs-lookup"><span data-stu-id="75b0d-113">Response Groups</span></span></p></td>
<td><p><span data-ttu-id="75b0d-114">Expansão da lista de distribuição</span><span class="sxs-lookup"><span data-stu-id="75b0d-114">Distribution list expansion</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b0d-115">Consulta de download e catálogo de endereços do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="75b0d-115">Address book download and address book query</span></span></p></td>
<td><p><span data-ttu-id="75b0d-116">Avançado 9-1-1 (E9-1-1) chamadas e perfil de local (plano de discagem)</span><span class="sxs-lookup"><span data-stu-id="75b0d-116">Enhanced 9-1-1 (E9-1-1) calls and location profile (dial plan)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b0d-117">Múltipla</span><span class="sxs-lookup"><span data-stu-id="75b0d-117">MultiView</span></span></p></td>
<td><p><span data-ttu-id="75b0d-118">Exibir vários fluxos de uma conferência</span><span class="sxs-lookup"><span data-stu-id="75b0d-118">Viewing multiple streams from a conference</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="75b0d-119">A ferramenta de stress e desempenho do Lync Server 2013 oferece suporte à geração e agrupamento de carga entre pools somente com a configuração avançada.</span><span class="sxs-lookup"><span data-stu-id="75b0d-119">The Lync Server 2013 Stress and Performance Tool supports cross-pool load generation and federation through advanced configuration only.</span></span>

<span data-ttu-id="75b0d-120">A ferramenta também não simula a carga do usuário para os seguintes clientes:</span><span class="sxs-lookup"><span data-stu-id="75b0d-120">The tool also does not simulate user load for the following clients:</span></span>

  - <span data-ttu-id="75b0d-121">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="75b0d-121">Office Live Meeting 2007</span></span>

  - <span data-ttu-id="75b0d-122">Chat persistente do Lync 2013</span><span class="sxs-lookup"><span data-stu-id="75b0d-122">Lync 2013 Persistent Chat</span></span>

<span data-ttu-id="75b0d-123">Como resultado, a ferramenta de stress e desempenho do Lync Server 2013 não será compatível com o teste dos seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="75b0d-123">As a result, the Lync Server 2013 Stress and Performance Tool will not support testing the following components:</span></span>

  - <span data-ttu-id="75b0d-124">Chat persistente do Lync 2013</span><span class="sxs-lookup"><span data-stu-id="75b0d-124">Lync 2013 Persistent Chat</span></span>

  - <span data-ttu-id="75b0d-125">Cenários de integração do Exchange</span><span class="sxs-lookup"><span data-stu-id="75b0d-125">Exchange integration scenarios</span></span>

<div>

## <a name="applications-and-files-included-with-the-lync-server-2013-stress-and-performance-tool"></a><span data-ttu-id="75b0d-126">Aplicativos e arquivos incluídos na ferramenta de stress e desempenho do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75b0d-126">Applications and Files Included with the Lync Server 2013 Stress and Performance Tool</span></span>

<span data-ttu-id="75b0d-127">Os seguintes aplicativos estão incluídos na ferramenta de stress e desempenho do Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="75b0d-127">The following applications are included in the Lync Server 2013 Stress and Performance Tool:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="75b0d-128">Ferramentas</span><span class="sxs-lookup"><span data-stu-id="75b0d-128">Tool</span></span></th>
<th><span data-ttu-id="75b0d-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="75b0d-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75b0d-130">UserProvisioningTool.exe</span><span class="sxs-lookup"><span data-stu-id="75b0d-130">UserProvisioningTool.exe</span></span></p></td>
<td><p><span data-ttu-id="75b0d-131">A ferramenta de provisionamento de usuário do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="75b0d-131">The Lync Server 2013 User Provisioning tool.</span></span> <span data-ttu-id="75b0d-132">Esta ferramenta é usada para criar usuários e contatos.</span><span class="sxs-lookup"><span data-stu-id="75b0d-132">This tool is used to create users and contacts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b0d-133">UserProfileGenerator.exe</span><span class="sxs-lookup"><span data-stu-id="75b0d-133">UserProfileGenerator.exe</span></span></p></td>
<td><p><span data-ttu-id="75b0d-134">A ferramenta de configuração de carregamento do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="75b0d-134">The Lync Server 2013 Load Configuration Tool.</span></span> <span data-ttu-id="75b0d-135">Esta ferramenta é usada para configurar as características da carga de usuário a ser simulada.</span><span class="sxs-lookup"><span data-stu-id="75b0d-135">This tool is used to configure the characteristics of the user load to simulate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b0d-136">LyncPerfTool.exe</span><span class="sxs-lookup"><span data-stu-id="75b0d-136">LyncPerfTool.exe</span></span></p></td>
<td><p><span data-ttu-id="75b0d-137">A ferramenta de stress e desempenho do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="75b0d-137">The Lync Server 2013 Stress and Performance Tool.</span></span> <span data-ttu-id="75b0d-138">LyncPerfTool é a ferramenta que simula a carga do usuário.</span><span class="sxs-lookup"><span data-stu-id="75b0d-138">LyncPerfTool is the tool that simulates the user load.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b0d-139">Default. TMX</span><span class="sxs-lookup"><span data-stu-id="75b0d-139">Default.tmx</span></span></p></td>
<td><p><span data-ttu-id="75b0d-140">Default. TMX é necessário para usar a ferramenta de log do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="75b0d-140">Default.tmx is required to use the Lync Server 2013 Logging Tool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b0d-141">Exemplo de scripts de provisionamento</span><span class="sxs-lookup"><span data-stu-id="75b0d-141">Example provisioning scripts</span></span></p></td>
<td><p><span data-ttu-id="75b0d-142">Esses exemplos são usados para configurar a topologia para executar testes de carga com base em cenários específicos</span><span class="sxs-lookup"><span data-stu-id="75b0d-142">These examples are used to configure the topology for running load tests, based on specific scenarios</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="75b0d-143">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="75b0d-143">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

