---
title: Migração do Lync Server 2010, Chat em Grupo ou Office Communications Server 2007 R2 Group Chat para Lync Server 2013, Servidor de Chat Persistente
description: Migração do Lync Server 2010, chat em grupo ou Office Communications Server 2007 R2 Grupo chat para o Lync Server 2013, servidor de chat persistente.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server
ms:assetid: 5b4d3db1-6eba-4932-b49c-f60bcf9488f9
ms:mtpsurl: https://technet.microsoft.com/library/Gg615442(v=OCS.15)
ms:contentKeyID: 48184240
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6090d5924a203a960444d9a10700fd178d038887
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446854"
---
# <a name="migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server"></a><span data-ttu-id="a7f00-103">Migração do Lync Server 2010, Chat em Grupo ou Office Communications Server 2007 R2 Group Chat para Lync Server 2013, Servidor de Chat Persistente</span><span class="sxs-lookup"><span data-stu-id="a7f00-103">Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a7f00-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a7f00-104">

<span> </span></span></span>

<span data-ttu-id="a7f00-105">_**Tópico da última modificação:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="a7f00-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="a7f00-106">Os tópicos desta seção guiam você pelo processo de migração do Lync Server 2010, do chat em grupo ou do Office Communications Server 2007 R2 Group Chat para o Lync Server 2013, servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="a7f00-106">The topics in this section guide you through the process of migrating either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="a7f00-107">Se você pretende que o seu Lync Server 2013, a implantação persistente do servidor de chat coexista com um Lync Server 2010, o chat em grupo ou o Office Communications Server 2007 R2 implantação de chat em grupo, este guia também inclui algumas informações essenciais para operar nesse ambiente misto.</span><span class="sxs-lookup"><span data-stu-id="a7f00-107">If you intend for your Lync Server 2013, Persistent Chat Server deployment to coexist with a Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat deployment, this guide also includes some essential information for operating in this mixed environment.</span></span> <span data-ttu-id="a7f00-108">Este guia se concentra principalmente na migração de dados para o servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="a7f00-108">This guide primarily focuses on data migration for Persistent Chat Server.</span></span> <span data-ttu-id="a7f00-109">Para os usuários que estão migrando de versões herdadas do Lync Server para o Lync Server 2013, confira [migrar do Lync server 2010 para o Lync server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) e [migrar do Office communications Server 2007 R2 para o Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="a7f00-109">For users who are migrating from legacy versions of Lync Server to Lync Server 2013, see [Migration from Lync Server 2010 to Lync Server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) and [Migration from Office Communications Server 2007 R2 to Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a7f00-110">Este tópico pressupõe que você já instalou o Lync Server 2013 em coexistência com o Lync Server 2010 ou o Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="a7f00-110">This topic assumes that you have already installed Lync Server 2013 in coexistence with Lync Server 2010 or Office Communications Server 2007 R2.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a7f00-111">Este guia descreve as etapas geralmente necessárias para realizar cada fase da migração.</span><span class="sxs-lookup"><span data-stu-id="a7f00-111">This guide describes the steps generally required to accomplish each phase of migration.</span></span> <span data-ttu-id="a7f00-112">Ele não trata cada possível topologia de implantação herdada ou todos os possíveis cenários de migração.</span><span class="sxs-lookup"><span data-stu-id="a7f00-112">It does not address every possible legacy deployment topology or every possible migration scenario.</span></span> <span data-ttu-id="a7f00-113">Portanto, talvez você não precise executar todas as etapas descritas ou talvez seja necessário executar etapas adicionais, dependendo da sua implantação.</span><span class="sxs-lookup"><span data-stu-id="a7f00-113">Therefore, you may not need to perform every step that is described, or you may need to perform additional steps, depending on your deployment.</span></span> <span data-ttu-id="a7f00-114">O guia também fornece exemplos de etapas de verificação.</span><span class="sxs-lookup"><span data-stu-id="a7f00-114">The guide also provides examples of verification steps.</span></span> <span data-ttu-id="a7f00-115">Essas etapas de verificação são fornecidas para ajudá-lo a entender o que você precisa ter para se certificar de que cada fase seja concluída com êxito enquanto avança pela migração.</span><span class="sxs-lookup"><span data-stu-id="a7f00-115">These verification steps are provided to help you understand what you need to look for to be sure that each phase completes successfully as you progress through your migration.</span></span> <span data-ttu-id="a7f00-116">Você pode modificar essas etapas de verificação para seu processo de migração específico.</span><span class="sxs-lookup"><span data-stu-id="a7f00-116">You can modify these verification steps to your specific migration process.</span></span>



</div>

<span data-ttu-id="a7f00-117">Este guia fornece informações específicas para atualizar sua implantação existente.</span><span class="sxs-lookup"><span data-stu-id="a7f00-117">This guide provides information specific to upgrading your existing deployment.</span></span> <span data-ttu-id="a7f00-118">Ele não explica como alterar a topologia existente.</span><span class="sxs-lookup"><span data-stu-id="a7f00-118">It does not explain how to change your existing topology.</span></span> <span data-ttu-id="a7f00-119">Este guia não aborda a implementação de novos recursos.</span><span class="sxs-lookup"><span data-stu-id="a7f00-119">This guide does not cover the implementation of new features.</span></span> <span data-ttu-id="a7f00-120">Quando um procedimento detalhado for documentado em outro lugar, este guia direcionará você para a seção do documento ou documento apropriado.</span><span class="sxs-lookup"><span data-stu-id="a7f00-120">When a detailed procedure is documented elsewhere, this guide directs you to the appropriate document or document section.</span></span>

<span data-ttu-id="a7f00-121">Este documento define termos conforme especificado na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7f00-121">This document defines terms as specified in the following list.</span></span>

  - <span data-ttu-id="a7f00-122">*migração*</span><span class="sxs-lookup"><span data-stu-id="a7f00-122">*migration*</span></span>  
    <span data-ttu-id="a7f00-123">Mover a implantação de uma versão anterior do servidor de chat persistente, anteriormente conhecida como servidor de chat em grupo, para o Lync Server 2013, servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="a7f00-123">Moving your deployment from a previous version of Persistent Chat Server, formerly known as Group Chat Server, to Lync Server 2013, Persistent Chat Server.</span></span>

<!-- end list -->

  - <span data-ttu-id="a7f00-124">*atualização*</span><span class="sxs-lookup"><span data-stu-id="a7f00-124">*upgrade*</span></span>  
    <span data-ttu-id="a7f00-125">Instalar uma versão mais recente do software em um computador cliente ou servidor.</span><span class="sxs-lookup"><span data-stu-id="a7f00-125">Installing a newer version of software on a server or client computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="a7f00-126">*coexistência*</span><span class="sxs-lookup"><span data-stu-id="a7f00-126">*coexistence*</span></span>  
    <span data-ttu-id="a7f00-127">O ambiente temporário que existe durante a migração, quando alguma funcionalidade foi migrada para o Lync Server 2013, servidor de chat persistente e outras funcionalidades ainda permanecem em uma versão anterior do servidor de chat de grupo.</span><span class="sxs-lookup"><span data-stu-id="a7f00-127">The temporary environment that exists during migration, when some functionality has been migrated to Lync Server 2013, Persistent Chat Server, and other functionality still remains on a prior version of Group Chat Server.</span></span>

<span data-ttu-id="a7f00-128">O servidor de chat persistente é uma extensão da infraestrutura do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a7f00-128">Persistent Chat Server is an extension of the Lync Server 2013 infrastructure.</span></span> <span data-ttu-id="a7f00-129">Dependendo da sua topologia, você pode migrar o Lync Server 2010, o chat em grupo ou o Office Communications Server 2007 R2 Grupo chat para o Lync Server 2013 servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="a7f00-129">Depending on your topology, you can migrate Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013 Persistent Chat Server.</span></span> <span data-ttu-id="a7f00-130">Para obter detalhes sobre topologias disponíveis e os requisitos técnicos e de software para migração de servidor de chat em grupo, consulte [planejando o servidor de chat persistente no Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="a7f00-130">For details about available topologies and the technical and software requirements for migrating Group Chat Server, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

<span data-ttu-id="a7f00-131">Se a sua organização exigir o suporte de conformidade, ele será automaticamente instalado em cada servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="a7f00-131">If your organization requires compliance support, it is now automatically installed with each Persistent Chat Server.</span></span> <span data-ttu-id="a7f00-132">Um servidor separado não é mais necessário para a conformidade.</span><span class="sxs-lookup"><span data-stu-id="a7f00-132">A separate server is no longer needed for compliance.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a7f00-133">O servidor de chat persistente deve ser instalado em um sistema de arquivos NTFS para ajudar a reforçar a segurança do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a7f00-133">Persistent Chat Server must be installed on an NTFS file system to help enforce file system security.</span></span> <span data-ttu-id="a7f00-134">FAT32 não é um sistema de arquivos com suporte para o servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="a7f00-134">FAT32 is not a supported file system for Persistent Chat Server.</span></span><BR><span data-ttu-id="a7f00-135">Se a sua organização exigir o suporte de conformidade, ele será automaticamente instalado em cada servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="a7f00-135">If your organization requires compliance support, it is now automatically installed with each Persistent Chat Server.</span></span> <span data-ttu-id="a7f00-136">Um servidor separado não é mais necessário para a conformidade.</span><span class="sxs-lookup"><span data-stu-id="a7f00-136">A separate server is no longer needed for compliance.</span></span> <span data-ttu-id="a7f00-137">Para obter mais detalhes sobre alterações no servidor de chat persistente do Lync Server 2013 &nbsp; , consulte <A href="lync-server-2013-new-persistent-chat-server-features.md">novos recursos persistentes do servidor de chat no lync Server 2013</A> na documentação de introdução.</span><span class="sxs-lookup"><span data-stu-id="a7f00-137">For more details about changes in Lync Server 2013&nbsp;Persistent Chat Server, see <A href="lync-server-2013-new-persistent-chat-server-features.md">New Persistent Chat Server features in Lync Server 2013</A> in the Getting Started documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a7f00-138">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a7f00-138">In This Section</span></span>

  - [<span data-ttu-id="a7f00-139">Cenário de migração padrão - nível alto</span><span class="sxs-lookup"><span data-stu-id="a7f00-139">Standard migration scenario - high-level</span></span>](standard-migration-scenario-high-level.md)

  - [<span data-ttu-id="a7f00-140">Processo de migração - detalhes</span><span class="sxs-lookup"><span data-stu-id="a7f00-140">Migration process - details</span></span>](migration-process-details.md)

  - [<span data-ttu-id="a7f00-141">Considerações de coexistência</span><span class="sxs-lookup"><span data-stu-id="a7f00-141">Coexistence considerations</span></span>](coexistence-considerations.md)

<span data-ttu-id="a7f00-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a7f00-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

