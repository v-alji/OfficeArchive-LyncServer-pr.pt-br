---
title: Migração do Office Communications Server 2007 R2 para Lync Server 2013
description: Migração do Office Communications Server 2007 R2 para o Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Office Communications Server 2007 R2 to Lync Server 2013
ms:assetid: f3fa4f5f-e9a2-4fb7-a12d-20f04173e697
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205375(v=OCS.15)
ms:contentKeyID: 48185802
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0afdc754ae691bc674c200addb9fb97c1eb4199
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446146"
---
# <a name="migration-from-office-communications-server-2007-r2-to-lync-server-2013"></a><span data-ttu-id="5aa8c-103">Migração do Office Communications Server 2007 R2 para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5aa8c-103">Migration from Office Communications Server 2007 R2 to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5aa8c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5aa8c-104">

<span> </span></span></span>

<span data-ttu-id="5aa8c-105">_**Tópico da última modificação:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="5aa8c-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="5aa8c-106">Os tópicos desta seção guiam você pelo processo de migração do Office Communications Server 2007 R2 para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5aa8c-106">The topics in this section guide you through the process of migrating from Office Communications Server 2007 R2 to Lync Server 2013</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="5aa8c-107">Este documento descreve as etapas geralmente necessárias para realizar cada fase da migração.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-107">This document describes the steps generally required to accomplish each phase of migration.</span></span> <span data-ttu-id="5aa8c-108">Ele não trata cada possível topologia de implantação herdada ou todos os possíveis cenários de migração.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-108">It does not address every possible legacy deployment topology or every possible migration scenario.</span></span> <span data-ttu-id="5aa8c-109">Portanto, talvez você não precise executar todas as etapas descritas ou talvez seja necessário executar etapas adicionais, dependendo da sua implantação.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-109">Therefore, you may not need to perform every step described, or you may need to perform additional steps, depending on your deployment.</span></span> <span data-ttu-id="5aa8c-110">Este documento também fornece exemplos de etapas de verificação.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-110">This document also provides examples of verification steps.</span></span> <span data-ttu-id="5aa8c-111">Estas etapas de verificação são fornecidas para ajudá-lo a entender o que você precisa procurar para garantir que cada fase seja concluída com êxito enquanto avança pela migração.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-111">These verification steps are provided to help you understand what you need to look for to ensure that each phase completes successfully as you progress through your migration.</span></span> <span data-ttu-id="5aa8c-112">Personalize essas etapas de verificação para seu processo de migração específico.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-112">Tailor these verification steps to your specific migration process.</span></span>



</div>

<span data-ttu-id="5aa8c-113">Este guia fornece informações específicas para atualizar sua implantação existente.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-113">This guide provides information specific to upgrading your existing deployment.</span></span> <span data-ttu-id="5aa8c-114">Ele não explica como alterar a topologia existente.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-114">It does not explain how to change your existing topology.</span></span> <span data-ttu-id="5aa8c-115">Este guia não aborda a implementação de novos recursos.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-115">This guide does not cover the implementation of new features.</span></span> <span data-ttu-id="5aa8c-116">Quando um procedimento detalhado for documentado em outro lugar, este guia direcionará você para a seção do documento ou documento apropriado.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-116">When a detailed procedure is documented elsewhere, this guide directs you to the appropriate document or document section.</span></span>

<span data-ttu-id="5aa8c-117">Este documento define termos conforme especificado na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-117">This document defines terms as specified in the following list.</span></span>

  - <span data-ttu-id="5aa8c-118">*migração*</span><span class="sxs-lookup"><span data-stu-id="5aa8c-118">*migration*</span></span>  
    <span data-ttu-id="5aa8c-119">Mover a implantação de produção de uma versão anterior do Office Communications Server 2007 R2 para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-119">Moving your production deployment from a previous version of Office Communications Server 2007 R2 to Lync Server 2013.</span></span>

<!-- end list -->

  - <span data-ttu-id="5aa8c-120">*atualização*</span><span class="sxs-lookup"><span data-stu-id="5aa8c-120">*upgrade*</span></span>  
    <span data-ttu-id="5aa8c-121">Instalar uma versão mais recente do software em um computador cliente ou servidor.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-121">Installing a newer version of software on a server or client computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="5aa8c-122">*coexistência*</span><span class="sxs-lookup"><span data-stu-id="5aa8c-122">*coexistence*</span></span>  
    <span data-ttu-id="5aa8c-123">O ambiente temporário que existe durante a migração quando algumas funcionalidades foram migradas para o Lync Server 2013 e outras funcionalidades ainda permanecem em uma versão anterior do Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-123">The temporary environment that exists during migration when some functionality has been migrated to Lync Server 2013 and other functionality still remains on a prior version of Office Communications Server 2007 R2.</span></span>

<!-- end list -->

  - <span data-ttu-id="5aa8c-124">*interoperabilidade*</span><span class="sxs-lookup"><span data-stu-id="5aa8c-124">*interoperability*</span></span>  
    <span data-ttu-id="5aa8c-125">A capacidade de sua implantação operar com sucesso durante o período de coexistência.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-125">The ability of your deployment to operate successfully during the period of coexistence.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5aa8c-126">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5aa8c-126">In This Section</span></span>

  - [<span data-ttu-id="5aa8c-127">Antes de começar a migração</span><span class="sxs-lookup"><span data-stu-id="5aa8c-127">Before you begin the migration</span></span>](before-you-begin-the-migration.md)

  - [<span data-ttu-id="5aa8c-128">Fases de migração</span><span class="sxs-lookup"><span data-stu-id="5aa8c-128">Migration phases</span></span>](migration-phases.md)

  - [<span data-ttu-id="5aa8c-129">Fase 1: planejar a migração do Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="5aa8c-129">Phase 1: Plan your migration from Office Communications Server 2007 R2</span></span>](phase-1-plan-your-migration-from-office-communications-server-2007-r2.md)

  - [<span data-ttu-id="5aa8c-130">Fase 2: Preparar para migração</span><span class="sxs-lookup"><span data-stu-id="5aa8c-130">Phase 2: Prepare for migration</span></span>](phase-2-prepare-for-migration.md)

  - [<span data-ttu-id="5aa8c-131">Fase 3: implantar o pool piloto do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5aa8c-131">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>](phase-3-deploy-lync-server-2013-pilot-pool.md)

  - [<span data-ttu-id="5aa8c-132">Fase 4: topologias de mesclagem</span><span class="sxs-lookup"><span data-stu-id="5aa8c-132">Phase 4: Merge topologies</span></span>](phase-4-merge-topologies.md)

  - [<span data-ttu-id="5aa8c-133">Fase 5: configurar o pool piloto</span><span class="sxs-lookup"><span data-stu-id="5aa8c-133">Phase 5: Configure the pilot pool</span></span>](phase-5-configure-the-pilot-pool.md)

  - [<span data-ttu-id="5aa8c-134">Fase 6: mover usuários para o pool piloto</span><span class="sxs-lookup"><span data-stu-id="5aa8c-134">Phase 6: Move users to the pilot pool</span></span>](phase-6-move-users-to-the-pilot-pool.md)

  - [<span data-ttu-id="5aa8c-135">Fase 7: Adicionar o servidor de borda do Lync Server 2013 ao pool piloto</span><span class="sxs-lookup"><span data-stu-id="5aa8c-135">Phase 7: Add Lync Server 2013 Edge Server to pilot pool</span></span>](phase-7-add-lync-server-2013-edge-server-to-pilot-pool.md)

  - [<span data-ttu-id="5aa8c-136">Fase 8: mover da implantação piloto para produção</span><span class="sxs-lookup"><span data-stu-id="5aa8c-136">Phase 8: Move from pilot deployment into production</span></span>](phase-8-move-from-pilot-deployment-into-production.md)

  - [<span data-ttu-id="5aa8c-137">Fase 9: concluir tarefas posteriores à migração</span><span class="sxs-lookup"><span data-stu-id="5aa8c-137">Phase 9: Complete post-migration tasks</span></span>](phase-9-complete-post-migration-tasks.md)

  - [<span data-ttu-id="5aa8c-138">Fase 10: descomissionar site herdado</span><span class="sxs-lookup"><span data-stu-id="5aa8c-138">Phase 10: Decommission legacy site</span></span>](phase-10-decommission-legacy-site.md)

<span data-ttu-id="5aa8c-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5aa8c-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

