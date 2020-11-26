---
title: 'Lync Server 2013: Implantando sites de filial'
description: 'Lync Server 2013: Implantando sites de filiais.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying branch sites
ms:assetid: 1475dee0-66ae-4ee5-b6f1-7409b4bbff45
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398217(v=OCS.15)
ms:contentKeyID: 48183483
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d653e3f06de832693d97bfb229f122a67c28640e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430088"
---
# <a name="deploying-branch-sites-in-lync-server-2013"></a><span data-ttu-id="56a85-103">Implantando sites de filial no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="56a85-103">Deploying branch sites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="56a85-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="56a85-104">

<span> </span></span></span>

<span data-ttu-id="56a85-105">_**Tópico da última modificação:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="56a85-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="56a85-106">Os usuários do site de filiais obtêm a maioria da funcionalidade do Lync Server 2013 do servidor no site central ao qual o site de filial está associado.</span><span class="sxs-lookup"><span data-stu-id="56a85-106">Branch site users get most of their Lync Server 2013 functionality from the server at the central site that the branch site is associated with.</span></span> <span data-ttu-id="56a85-107">Cada site de filial está associado a um site central de exatamente.</span><span class="sxs-lookup"><span data-stu-id="56a85-107">Each branch site is associated with exactly one central site.</span></span> <span data-ttu-id="56a85-108">Para fornecer chamadas de e para a rede telefônica pública comutada (PSTN), um site de filial pode conter qualquer um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="56a85-108">To provide calls to and from the public switched telephone network (PSTN), a branch site might contain any of the following:</span></span>

  - <span data-ttu-id="56a85-109">Um gateway PSTN e, possivelmente, um servidor meditação</span><span class="sxs-lookup"><span data-stu-id="56a85-109">A PSTN gateway and possibly a Meditation Server</span></span>

  - <span data-ttu-id="56a85-110">Um tronco SIP</span><span class="sxs-lookup"><span data-stu-id="56a85-110">A SIP trunk</span></span>

  - <span data-ttu-id="56a85-111">Uma infraestrutura de voz existente com um PBX (Private Branch Exchange)</span><span class="sxs-lookup"><span data-stu-id="56a85-111">An existing voice infrastructure with a private branch exchange (PBX)</span></span>

  - <span data-ttu-id="56a85-112">Um aparelho de ramificação sobreviventes</span><span class="sxs-lookup"><span data-stu-id="56a85-112">A Survivable Branch Appliance</span></span>

  - <span data-ttu-id="56a85-113">Um servidor de ramificação sobreviventes</span><span class="sxs-lookup"><span data-stu-id="56a85-113">A Survivable Branch Server</span></span>

<span data-ttu-id="56a85-114">Os sites de filiais com um aparelho de ramificação sobreviventes ou um servidor de filiais sobreviventes são mais resistentes em tempo de falhas de rede de longa distância ou de locais centrais do que os sites de filiais sem uma dessas soluções.</span><span class="sxs-lookup"><span data-stu-id="56a85-114">Branch sites with a Survivable Branch Appliance or a Survivable Branch Server are more resilient in times of wide-area network or central site failures than branch sites without one of these solutions.</span></span> <span data-ttu-id="56a85-115">Por exemplo, em um site com um aparelho de ramificação sobreviventes ou um servidor de ramificação sobreviventes implantado, os usuários ainda poderão fazer e receber chamadas PSTN se a rede que conecta o site de filial ao site central estiver inativa.</span><span class="sxs-lookup"><span data-stu-id="56a85-115">For example, in a site with a Survivable Branch Appliance or a Survivable Branch Server deployed, users can still make and receive PSTN calls if the network connecting the branch site to the central site is down.</span></span> <span data-ttu-id="56a85-116">Outra maneira de obter resiliência de site de filial é usar um gateway PSTN ou um tronco SIP com uma implantação completa do Lync Server no site da filial.</span><span class="sxs-lookup"><span data-stu-id="56a85-116">Another way to achieve branch-site resiliency is by using a PSTN gateway or a SIP trunk with a full-scale Lync Server deployment at the branch site.</span></span>

<span data-ttu-id="56a85-117">Para obter detalhes sobre qual implantação de site de filial é ideal para sua organização, incluindo pré-requisitos e outras considerações de planejamento, consulte [planejando a conectividade PSTN no Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) e [planejando a resiliência de voz no site de filial no Lync Server 2013](lync-server-2013-planning-for-branch-site-voice-resiliency.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="56a85-117">For details about which branch site deployment is right for your organization, including prerequisites and other planning considerations, see [Planning for PSTN connectivity in Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) and [Planning for branch-site voice resiliency in Lync Server 2013](lync-server-2013-planning-for-branch-site-voice-resiliency.md) in the Planning documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="56a85-118">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="56a85-118">In This Section</span></span>

  - [<span data-ttu-id="56a85-119">Fornecendo conectividade de PSTN ao site da filial no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="56a85-119">Providing PSTN connectivity at a branch site in Lync Server 2013</span></span>](lync-server-2013-providing-pstn-connectivity-at-a-branch-site.md)

  - [<span data-ttu-id="56a85-120">Implantando Aplicativo ou Servidor de Filial Persistente com Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="56a85-120">Deploying a Survivable Branch Appliance or Server with Lync Server 2013</span></span>](lync-server-2013-deploying-a-survivable-branch-appliance-or-server.md)

<span data-ttu-id="56a85-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="56a85-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

