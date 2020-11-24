---
title: 'Lync Server 2013: detalhes da exibição de QoE'
description: 'Lync Server 2013: detalhes do modo de exibição de QoE.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: QoE view details
ms:assetid: 6a658318-a317-4546-a44c-a9c473d8e86a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688081(v=OCS.15)
ms:contentKeyID: 49733677
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b20eb083295a5f3d3ecb5be7a8c96d9c4b7cfab2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390053"
---
# <a name="qoe-view-details-in-lync-server-2013"></a><span data-ttu-id="b56c4-103">Detalhes do modo de exibição de QoE no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b56c4-103">QoE view details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b56c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b56c4-104">

<span> </span></span></span>

<span data-ttu-id="b56c4-105">_**Tópico da última modificação:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="b56c4-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="b56c4-106">Os modos de exibição abrangem os cenários mais comuns para retornar dados do banco de dados do QoE SQL.</span><span class="sxs-lookup"><span data-stu-id="b56c4-106">Views cover the most common scenarios for returning data from the QoE SQL database.</span></span> <span data-ttu-id="b56c4-107">Ele é recomendado para a criação de relatórios personalizados, em vez de acessar diretamente as tabelas de banco de dados; Isso porque os modos de exibição são mais prováveis de manter a compatibilidade retroativa com versões futuras.</span><span class="sxs-lookup"><span data-stu-id="b56c4-107">It is recommended views used for building custom reports instead of directly accessing the database tables; that’s because views are more likely to maintain backwards compatibility with future releases.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b56c4-108">Nome do modo de exibição</span><span class="sxs-lookup"><span data-stu-id="b56c4-108">View Name</span></span></th>
<th><span data-ttu-id="b56c4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b56c4-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b56c4-110"><a href="lync-server-2013-audiostreamdetail-view.md">Exibição AudioStreamDetail no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b56c4-110"><a href="lync-server-2013-audiostreamdetail-view.md">AudioStreamDetail view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="b56c4-111">Armazena informações sobre cada fluxo de áudio no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b56c4-111">Stores information about each audio stream in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56c4-112"><a href="lync-server-2013-medialine-view.md">Modo de exibição de mídia no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b56c4-112"><a href="lync-server-2013-medialine-view.md">MediaLine view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="b56c4-113">Armazena informações sobre cada linha de mídia no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b56c4-113">Stores information about each media line in the database.</span></span> <span data-ttu-id="b56c4-114">Uma sessão de áudio geralmente contém uma linha de mídia de áudio.</span><span class="sxs-lookup"><span data-stu-id="b56c4-114">One audio session typically contains one audio media line.</span></span> <span data-ttu-id="b56c4-115">Uma sessão de áudio e vídeo (A/V) geralmente contém uma linha de mídia de áudio e uma linha de mídia de vídeo; no entanto, a sessão pode conter duas linhas de mídia de vídeo se um dispositivo de conferência for usado ou se o modo de exibição de galeria for usado.</span><span class="sxs-lookup"><span data-stu-id="b56c4-115">One audio and video (A/V) session typically contains one audio media line and one video media line; however, the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56c4-116"><a href="lync-server-2013-networkconfigurationsettings-view.md">Exibição NetworkConfigurationSettings no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b56c4-116"><a href="lync-server-2013-networkconfigurationsettings-view.md">NetworkConfigurationSettings view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="b56c4-117">Armazena informações sobre a configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="b56c4-117">Stores information about the network configuration.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56c4-118"><a href="lync-server-2013-session-view.md">Modo de exibição de sessão no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b56c4-118"><a href="lync-server-2013-session-view.md">Session view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="b56c4-119">Armazena informações sobre sessões que têm registros no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b56c4-119">Stores information about sessions that have records in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b56c4-120"><a href="lync-server-2013-useragent-view.md">Modo de exibição do UserAgent no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b56c4-120"><a href="lync-server-2013-useragent-view.md">UserAgent view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="b56c4-121">Armazena informações sobre os agentes de usuário envolvidos em sessões que têm registros no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b56c4-121">Stores information about the user agents that have been involved in sessions that have records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b56c4-122"><a href="lync-server-2013-videostreamdetail-view.md">Exibição VideoStreamDetail no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b56c4-122"><a href="lync-server-2013-videostreamdetail-view.md">VideoStreamDetail view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="b56c4-123">Armazena informações sobre cada fluxo de vídeo no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b56c4-123">Stores information about each video stream in the database.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b56c4-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b56c4-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

