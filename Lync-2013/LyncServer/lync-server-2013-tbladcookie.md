---
title: 'Lync Server 2013: tblADCookie'
description: 'Lync Server 2013: tblADCookie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblADCookie
ms:assetid: 0a9102c4-47aa-40ea-8a0d-20e72ab09848
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558610(v=OCS.15)
ms:contentKeyID: 48183366
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 41c3dde3730ede07b204a473c7fe0a5ab68054d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389965"
---
# <a name="tbladcookie-in-lync-server-2013"></a><span data-ttu-id="6aa67-103">tblADCookie no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6aa67-103">tblADCookie in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6aa67-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6aa67-104">

<span> </span></span></span>

<span data-ttu-id="6aa67-105">_**Tópico da última modificação:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="6aa67-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="6aa67-106">tblADCookie contém os atuais cookies de sincronização de LDAP (Lightweight Directory Access Protocol).</span><span class="sxs-lookup"><span data-stu-id="6aa67-106">tblADCookie contains the current Lightweight Directory Access Protocol (LDAP) Sync cookies.</span></span>

### <a name="columns"></a><span data-ttu-id="6aa67-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="6aa67-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6aa67-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="6aa67-108">Column</span></span></th>
<th><span data-ttu-id="6aa67-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="6aa67-109">Type</span></span></th>
<th><span data-ttu-id="6aa67-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6aa67-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6aa67-111">prinGuid</span><span class="sxs-lookup"><span data-stu-id="6aa67-111">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="6aa67-112">GUID, não nulo</span><span class="sxs-lookup"><span data-stu-id="6aa67-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="6aa67-113">GUID principal do domínio que está sendo monitorado.</span><span class="sxs-lookup"><span data-stu-id="6aa67-113">Principal GUID of the domain being monitored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa67-114">prinDCHost</span><span class="sxs-lookup"><span data-stu-id="6aa67-114">prinDCHost</span></span></p></td>
<td><p><span data-ttu-id="6aa67-115">nvarchar (255)</span><span class="sxs-lookup"><span data-stu-id="6aa67-115">nvarchar (255)</span></span></p></td>
<td><p><span data-ttu-id="6aa67-116">FQDN (nome de domínio totalmente qualificado) do controlador de domínio atual usado para a sincronização dos serviços de domínio Active Directory. Tem valor informativo.</span><span class="sxs-lookup"><span data-stu-id="6aa67-116">Fully qualified domain name (FQDN) of the current domain controller used for Active Directory Domain Services Sync. Has informational value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa67-117">adcContent</span><span class="sxs-lookup"><span data-stu-id="6aa67-117">adcContent</span></span></p></td>
<td><p><span data-ttu-id="6aa67-118">imagem (binário)</span><span class="sxs-lookup"><span data-stu-id="6aa67-118">image (binary)</span></span></p></td>
<td><p><span data-ttu-id="6aa67-119">Cookie de sincronização do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6aa67-119">Active Directory Sync cookie.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa67-120">lastUpdated</span><span class="sxs-lookup"><span data-stu-id="6aa67-120">lastUpdated</span></span></p></td>
<td><p><span data-ttu-id="6aa67-121">datetime</span><span class="sxs-lookup"><span data-stu-id="6aa67-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="6aa67-122">Carimbo de data/hora com o tempo de atualização de linha.</span><span class="sxs-lookup"><span data-stu-id="6aa67-122">Time stamp with the row update time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aa67-123">lockedUntil</span><span class="sxs-lookup"><span data-stu-id="6aa67-123">lockedUntil</span></span></p></td>
<td><p><span data-ttu-id="6aa67-124">datetime</span><span class="sxs-lookup"><span data-stu-id="6aa67-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="6aa67-125">Tempo até que a linha esteja bloqueada para alterações.</span><span class="sxs-lookup"><span data-stu-id="6aa67-125">Time until the row is locked for changes.</span></span> <span data-ttu-id="6aa67-126">Isso faz parte de um mecanismo de travamento do software que garante que apenas um dos serviços de chat faça a sincronização do Active Directory de cada vez.</span><span class="sxs-lookup"><span data-stu-id="6aa67-126">This is part of a software interlock mechanism that ensures that only one of the chat services does the Active Directory Sync at a time.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="6aa67-127">As</span><span class="sxs-lookup"><span data-stu-id="6aa67-127">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6aa67-128">Coluna (s)</span><span class="sxs-lookup"><span data-stu-id="6aa67-128">Column(s)</span></span></th>
<th><span data-ttu-id="6aa67-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="6aa67-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6aa67-130">prinGuid</span><span class="sxs-lookup"><span data-stu-id="6aa67-130">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="6aa67-131">Chave primária.</span><span class="sxs-lookup"><span data-stu-id="6aa67-131">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aa67-132">prinGuid</span><span class="sxs-lookup"><span data-stu-id="6aa67-132">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="6aa67-133">Chave estrangeira com pesquisa na tabela principal. prinGuid.</span><span class="sxs-lookup"><span data-stu-id="6aa67-133">Foreign key with lookup in Principal.prinGuid table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6aa67-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6aa67-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

