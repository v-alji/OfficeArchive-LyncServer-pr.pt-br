---
title: 'Lync Server 2013: Planejamento para acesso de usuário externo'
description: 'Lync Server 2013: planejando o acesso de usuários externos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for external user access
ms:assetid: ea098933-eff5-461e-aba3-e7f128784dc2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399048(v=OCS.15)
ms:contentKeyID: 48185903
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8f1854791ed837b963d4c80f3467e4e89555592
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389686"
---
# <a name="planning-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="c367b-103">Planejamento para acesso de usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c367b-103">Planning for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c367b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c367b-104">

<span> </span></span></span>

<span data-ttu-id="c367b-105">_**Tópico da última modificação:** 2013-01-19_</span><span class="sxs-lookup"><span data-stu-id="c367b-105">_**Topic Last Modified:** 2013-01-19_</span></span>

<span data-ttu-id="c367b-106">As comunicações na maioria das organizações envolvem serviços e usuários que não estão dentro da sua rede interna.</span><span class="sxs-lookup"><span data-stu-id="c367b-106">Communications in most organizations involve services and users that are not inside your internal network.</span></span> <span data-ttu-id="c367b-107">Esses serviços e usuários incluem funcionários que estão temporariamente ou permanentemente externos, funcionários de organizações de clientes ou parceiros, pessoas que usam serviços de mensagens instantâneas (IM) públicas e clientes potenciais, parceiros e usuários anônimos que você convidar para reuniões e apresentações.</span><span class="sxs-lookup"><span data-stu-id="c367b-107">These services and users include employees who are temporarily or permanently offsite, employees of customer or partner organizations, people who use public instant messaging (IM) services, and potential customers, partners and anonymous users whom you invite to meetings and presentations.</span></span> <span data-ttu-id="c367b-108">Nesta documentação, essas pessoas são chamadas coletivamente como *usuários externos*.</span><span class="sxs-lookup"><span data-stu-id="c367b-108">In this documentation, these people are collectively referred to as *external users*.</span></span>

<span data-ttu-id="c367b-109">Com o Microsoft Lync Server 2013, os usuários em sua organização podem usar mensagens instantâneas e presença para se comunicar com usuários externos, e podem participar de conferências de áudio/vídeo (A/V) e conferência via Web com seus funcionários externos e outros tipos de usuários externos.</span><span class="sxs-lookup"><span data-stu-id="c367b-109">With Microsoft Lync Server 2013, users in your organization can use IM and presence to communicate with external users, and they can participate in audio/video (A/V) conferencing and web conferencing with your offsite employees and other types of external users.</span></span> <span data-ttu-id="c367b-110">Você também pode dar suporte ao acesso externo de dispositivos móveis e do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="c367b-110">You can also support external access from mobile devices and over Enterprise Voice.</span></span> <span data-ttu-id="c367b-111">Os usuários externos que não são membros da sua organização podem participar de reuniões do Lync Server 2013, permitindo participantes anônimos.</span><span class="sxs-lookup"><span data-stu-id="c367b-111">External users who are not members of your organization can participate in Lync Server 2013 meetings, allowing anonymous attendees.</span></span>

<span data-ttu-id="c367b-112">Para dar suporte à comunicação no firewall da sua organização, implante o servidor de borda do Lync Server 2013 na sua rede de perímetro (também conhecido como DMZ, zona desmilitarizada e sub-rede filtrada).</span><span class="sxs-lookup"><span data-stu-id="c367b-112">To support communications across your organization’s firewall, you deploy Lync Server 2013 Edge Server in your perimeter network (also known as DMZ, demilitarized zone, and screened subnet).</span></span> <span data-ttu-id="c367b-113">O servidor de borda controla como os usuários de fora do firewall podem se conectar à sua implantação interna do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c367b-113">The Edge Server controls how users outside the firewall can connect to your internal Lync Server 2013 deployment.</span></span> <span data-ttu-id="c367b-114">Ele também controla comunicações com usuários externos que se originam dentro do firewall.</span><span class="sxs-lookup"><span data-stu-id="c367b-114">It also controls communications with external users that originate within the firewall.</span></span>

<span data-ttu-id="c367b-115">Dependendo dos seus requisitos, você pode implantar um ou mais servidores de borda em um ou mais locais.</span><span class="sxs-lookup"><span data-stu-id="c367b-115">Depending on your requirements, you can deploy one or more Edge Servers in one or more locations.</span></span> <span data-ttu-id="c367b-116">Esta seção descreve os cenários de acesso de usuários externos no Lync Server 2013, e explica como planejar a topologia de borda e de proxy inversa.</span><span class="sxs-lookup"><span data-stu-id="c367b-116">This section describes scenarios for external user access in Lync Server 2013, and it explains how to plan your edge and reverse proxy topology.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c367b-117">Embora você precise de um servidor de borda para dar suporte a acesso de usuário externo e de voz, esta seção enfoca o suporte para mensagens instantâneas, presença, conferência A/V, Federação, conferência via Web e Lync Mobile.</span><span class="sxs-lookup"><span data-stu-id="c367b-117">Although you need an Edge Server to support Enterprise Voice and external user access, this section focuses on support for IM, presence, A/V conferencing, federation, web conferencing, and Lync Mobile.</span></span> <span data-ttu-id="c367b-118">Para obter detalhes sobre o suporte para Enterprise Voice, consulte <A href="lync-server-2013-planning-for-enterprise-voice.md">planejamento para Enterprise Voice no Lync Server 2013</A> na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="c367b-118">For details about support for Enterprise Voice, see <A href="lync-server-2013-planning-for-enterprise-voice.md">Planning for Enterprise Voice in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c367b-119">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c367b-119">In This Section</span></span>

  - [<span data-ttu-id="c367b-120">Alterações no Lync Server 2013 que afetam o planejamento do Servidor de Borda</span><span class="sxs-lookup"><span data-stu-id="c367b-120">Changes in Lync Server 2013 that affect Edge Server planning</span></span>](lync-server-2013-changes-in-lync-server-that-affect-edge-server-planning.md)

  - [<span data-ttu-id="c367b-121">Requisitos do sistema para componentes de acesso de usuário externo para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c367b-121">System requirements for external user access components for Lync Server 2013</span></span>](lync-server-2013-system-requirements-for-external-user-access-components.md)

  - [<span data-ttu-id="c367b-122">Visão geral de acesso de usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c367b-122">Overview of external user access in Lync Server 2013</span></span>](lync-server-2013-overview-of-external-user-access.md)

  - [<span data-ttu-id="c367b-123">Compreendendo a descoberta automática no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c367b-123">Understanding Autodiscover in Lync Server 2013</span></span>](lync-server-2013-understanding-autodiscover.md)

  - [<span data-ttu-id="c367b-124">Escolhendo uma topologia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c367b-124">Choosing a topology in Lync Server 2013</span></span>](lync-server-2013-choosing-a-topology.md)

  - [<span data-ttu-id="c367b-125">Coleta de dados no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c367b-125">Data collection in Lync Server 2013</span></span>](lync-server-2013-data-collection.md)

  - [<span data-ttu-id="c367b-126">Determinar requisitios de DNS para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c367b-126">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)

  - [<span data-ttu-id="c367b-127">Determinar firewall A/V externo e requisitos de porta para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c367b-127">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)

  - [<span data-ttu-id="c367b-128">Planejar certificados do Servidor de Borda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c367b-128">Plan for Edge Server certificates in Lync Server 2013</span></span>](lync-server-2013-plan-for-edge-server-certificates.md)

  - [<span data-ttu-id="c367b-129">Cenários de acesso de usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c367b-129">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)

<span data-ttu-id="c367b-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c367b-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

