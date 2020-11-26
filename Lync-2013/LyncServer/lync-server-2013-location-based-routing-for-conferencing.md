---
title: 'Lync Server 2013: Location-Based roteamento para conferência'
description: 'Lync Server 2013: Location-Based roteamento para conferência.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing for conferencing
ms:assetid: e1acb1ba-0ed2-4abf-8a7b-1ca3049e95e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362849(v=OCS.15)
ms:contentKeyID: 56335087
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 979c835e03bbf87c9a9bf86b030cb9a8f4e138e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426540"
---
# <a name="location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="fda13-103">Location-Based o roteamento para conferências no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fda13-103">Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fda13-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fda13-104">

<span> </span></span></span>

<span data-ttu-id="fda13-105">_**Tópico da última modificação:** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="fda13-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="fda13-106">Location-Based o roteamento torna possível restringir o roteamento de chamadas entre pontos de extremidade VoIP e pontos de extremidade PSTN com base no local das partes na chamada.</span><span class="sxs-lookup"><span data-stu-id="fda13-106">Location-Based Routing makes it possible to restrict the routing of calls between VoIP endpoints and PSTN endpoints based on the location of the parties in the call.</span></span> <span data-ttu-id="fda13-107">Com a atualização cumulativa 2 do Lync Server 2013, Location-Based regras de roteamento podem ser impostas em reuniões do Lync (por exemplo, conferências) para impedir o bypass da PSTN.</span><span class="sxs-lookup"><span data-stu-id="fda13-107">With Cumulative Update 2 of Lync Server 2013, Location-Based Routing rules can be enforced on Lync meetings (i.e. conferences) to prevent PSTN toll bypass.</span></span> <span data-ttu-id="fda13-108">O aplicativo monitora uma conferência ativa e aplica Location-Based restrições de roteamento com base na localização dos usuários participantes.</span><span class="sxs-lookup"><span data-stu-id="fda13-108">The application monitors an active conference and enforces Location-Based Routing restrictions based on the location of users participating.</span></span> <span data-ttu-id="fda13-109">O aplicativo de conferência de roteamento Location-Based Adicionalmente permite a imposição de Location-Based restrições de roteamento para transferências consultivas envolvendo pontos de extremidade PSTN.</span><span class="sxs-lookup"><span data-stu-id="fda13-109">The Location-Based Routing Conferencing application additionally enables the enforcement of Location-Based Routing restrictions to consultative transfers involving PSTN endpoints.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="fda13-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="fda13-110">In This Section</span></span>

  - [<span data-ttu-id="fda13-111">Visão geral do roteamento Location-Based para conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fda13-111">Overview of Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-overview-of-location-based-routing-for-conferencing.md)

  - [<span data-ttu-id="fda13-112">Roteamento baseado em localização e transferências de chamadas consultivas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fda13-112">Location-Based Routing and consultative call transfers in Lync Server 2013</span></span>](lync-server-2013-location-based-routing-and-consultative-call-transfers.md)

  - [<span data-ttu-id="fda13-113">Requisitos para o Location-Based roteamento de conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fda13-113">Requirements for Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-requirements-for-location-based-routing-for-conferencing.md)

  - [<span data-ttu-id="fda13-114">Configuração do Roteamento Baseado em Local para conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fda13-114">Configuration of Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-configuration-of-location-based-routing-for-conferencing.md)

<span data-ttu-id="fda13-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fda13-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

