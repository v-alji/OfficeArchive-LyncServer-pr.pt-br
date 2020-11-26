---
title: Migração do Lync Server 2010 para o Lync Server 2013
description: Migração do Lync Server 2010 para o Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010 to Lync Server 2013
ms:assetid: ef99d4a9-a666-4a92-9994-4d7930f70d55
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205369(v=OCS.15)
ms:contentKeyID: 48185779
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbe1bc1b7745c5ddc89a7f8fb64295a82f52c9bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438593"
---
# <a name="migration-from-lync-server-2010-to-lync-server-2013"></a><span data-ttu-id="c67e9-103">Migração do Lync Server 2010 para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c67e9-103">Migration from Lync Server 2010 to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c67e9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c67e9-104">

<span> </span></span></span>

<span data-ttu-id="c67e9-105">_**Tópico da última modificação:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="c67e9-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="c67e9-106">Os tópicos desta seção guiam você pelo processo de migração do Lync Server 2010 para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c67e9-106">The topics in this section guide you through the process of migrating from Lync Server 2010 to Lync Server 2013.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c67e9-107">Este documento descreve as etapas geralmente necessárias para realizar cada fase da migração.</span><span class="sxs-lookup"><span data-stu-id="c67e9-107">This document describes the steps generally required to accomplish each phase of migration.</span></span> <span data-ttu-id="c67e9-108">Ele não trata cada possível topologia de implantação herdada ou todos os possíveis cenários de migração.</span><span class="sxs-lookup"><span data-stu-id="c67e9-108">It does not address every possible legacy deployment topology or every possible migration scenario.</span></span> <span data-ttu-id="c67e9-109">Portanto, talvez você não precise executar todas as etapas descritas ou talvez seja necessário executar etapas adicionais, dependendo da sua implantação.</span><span class="sxs-lookup"><span data-stu-id="c67e9-109">Therefore, you may not need to perform every step described, or you may need to perform additional steps, depending on your deployment.</span></span> <span data-ttu-id="c67e9-110">Este documento também fornece exemplos de etapas de verificação.</span><span class="sxs-lookup"><span data-stu-id="c67e9-110">This document also provides examples of verification steps.</span></span> <span data-ttu-id="c67e9-111">Estas etapas de verificação são fornecidas para ajudá-lo a entender o que você precisa procurar para garantir que cada fase seja concluída com êxito enquanto avança pela migração.</span><span class="sxs-lookup"><span data-stu-id="c67e9-111">These verification steps are provided to help you understand what you need to look for to ensure that each phase completes successfully as you progress through your migration.</span></span> <span data-ttu-id="c67e9-112">Personalize essas etapas de verificação para seu processo de migração específico.</span><span class="sxs-lookup"><span data-stu-id="c67e9-112">Tailor these verification steps to your specific migration process.</span></span>



</div>

<span data-ttu-id="c67e9-113">Este guia fornece informações específicas para atualizar sua implantação existente.</span><span class="sxs-lookup"><span data-stu-id="c67e9-113">This guide provides information specific to upgrading your existing deployment.</span></span> <span data-ttu-id="c67e9-114">Ele não explica como alterar a topologia existente.</span><span class="sxs-lookup"><span data-stu-id="c67e9-114">It does not explain how to change your existing topology.</span></span> <span data-ttu-id="c67e9-115">Este guia não aborda a implementação de novos recursos.</span><span class="sxs-lookup"><span data-stu-id="c67e9-115">This guide does not cover the implementation of new features.</span></span> <span data-ttu-id="c67e9-116">Quando um procedimento detalhado for documentado em outro lugar, este guia direcionará você para a seção do documento ou documento apropriado.</span><span class="sxs-lookup"><span data-stu-id="c67e9-116">When a detailed procedure is documented elsewhere, this guide directs you to the appropriate document or document section.</span></span>

<span data-ttu-id="c67e9-117">Este documento define termos conforme especificado na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="c67e9-117">This document defines terms as specified in the following list.</span></span>

  - <span data-ttu-id="c67e9-118">*migração*</span><span class="sxs-lookup"><span data-stu-id="c67e9-118">*migration*</span></span>  
    <span data-ttu-id="c67e9-119">Mover a implantação de produção de uma versão anterior do Lync Server 2010 para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c67e9-119">Moving your production deployment from a previous version of Lync Server 2010 to Lync Server 2013.</span></span>

<!-- end list -->

  - <span data-ttu-id="c67e9-120">*atualização*</span><span class="sxs-lookup"><span data-stu-id="c67e9-120">*upgrade*</span></span>  
    <span data-ttu-id="c67e9-121">Instalar uma versão mais recente do software em um computador cliente ou servidor.</span><span class="sxs-lookup"><span data-stu-id="c67e9-121">Installing a newer version of software on a server or client computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="c67e9-122">*coexistência*</span><span class="sxs-lookup"><span data-stu-id="c67e9-122">*coexistence*</span></span>  
    <span data-ttu-id="c67e9-123">O ambiente temporário que existe durante a migração quando algumas funcionalidades foram migradas para o Lync Server 2013 e outras funcionalidades ainda permanecem em uma versão anterior do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c67e9-123">The temporary environment that exists during migration when some functionality has been migrated to Lync Server 2013 and other functionality still remains on a prior version of Lync Server 2010.</span></span>

<!-- end list -->

  - <span data-ttu-id="c67e9-124">*interoperabilidade*</span><span class="sxs-lookup"><span data-stu-id="c67e9-124">*interoperability*</span></span>  
    <span data-ttu-id="c67e9-125">A capacidade de sua implantação operar com sucesso durante o período de coexistência.</span><span class="sxs-lookup"><span data-stu-id="c67e9-125">The ability of your deployment to operate successfully during the period of coexistence.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c67e9-126">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c67e9-126">In This Section</span></span>

  - [<span data-ttu-id="c67e9-127">Antes de começar a migração</span><span class="sxs-lookup"><span data-stu-id="c67e9-127">Before you begin the migration</span></span>](before-you-begin-the-migration.md)

  - [<span data-ttu-id="c67e9-128">Fase 1: planejar a migração do Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="c67e9-128">Phase 1: Plan your migration from Lync Server 2010</span></span>](phase-1-plan-your-migration-from-lync-server-2010.md)

  - [<span data-ttu-id="c67e9-129">Fase 2: Preparar para migração</span><span class="sxs-lookup"><span data-stu-id="c67e9-129">Phase 2: Prepare for migration</span></span>](phase-2-prepare-for-migration.md)

  - [<span data-ttu-id="c67e9-130">Fase 3: implantar o pool piloto do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c67e9-130">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>](phase-3-deploy-lync-server-2013-pilot-pool.md)

  - [<span data-ttu-id="c67e9-131">Fase 4: mover os usuários de teste para o pool piloto</span><span class="sxs-lookup"><span data-stu-id="c67e9-131">Phase 4: Move test users to the pilot pool</span></span>](phase-4-move-test-users-to-the-pilot-pool.md)

  - [<span data-ttu-id="c67e9-132">Fase 5: Adicionar o servidor de borda do Lync Server 2013 ao pool piloto</span><span class="sxs-lookup"><span data-stu-id="c67e9-132">Phase 5: Add Lync Server 2013 Edge Server to pilot pool</span></span>](phase-5-add-lync-server-2013-edge-server-to-pilot-pool.md)

  - [<span data-ttu-id="c67e9-133">Fase 6: Mover da implantação piloto para produção</span><span class="sxs-lookup"><span data-stu-id="c67e9-133">Phase 6: Move from pilot deployment into production</span></span>](phase-6-move-from-pilot-deployment-into-production.md)

  - [<span data-ttu-id="c67e9-134">Fase 7: Concluir tarefas pós-migração</span><span class="sxs-lookup"><span data-stu-id="c67e9-134">Phase 7: Complete post-migration tasks</span></span>](phase-7-complete-post-migration-tasks.md)

  - [<span data-ttu-id="c67e9-135">Fase 8: Encerrar os pools herdados</span><span class="sxs-lookup"><span data-stu-id="c67e9-135">Phase 8: Decommission legacy pools</span></span>](phase-8-decommission-legacy-pools.md)

<span data-ttu-id="c67e9-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c67e9-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

