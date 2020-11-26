---
title: 'Lync Server 2013: gerenciamento de alterações'
description: 'Lync Server 2013: gerenciamento de alterações.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Change management
ms:assetid: 73c774f5-c12f-4c72-be73-e07dc745b994
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720336(v=OCS.15)
ms:contentKeyID: 63969618
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69ea019f6366528c40b60a39ca8b646b49b336b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435121"
---
# <a name="change-management-in-lync-server-2013"></a><span data-ttu-id="0da5e-103">Gerenciamento de alterações no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0da5e-103">Change management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0da5e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0da5e-104">

<span> </span></span></span>

<span data-ttu-id="0da5e-105">_**Tópico da última modificação:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="0da5e-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="0da5e-106">As alterações no ambiente de ti são inevitáveis.</span><span class="sxs-lookup"><span data-stu-id="0da5e-106">Changes to the IT environment are unavoidable.</span></span> <span data-ttu-id="0da5e-107">As alterações incluem novas tecnologias, sistemas, aplicativos, hardware, ferramentas, processos e alterações em funções e responsabilidades.</span><span class="sxs-lookup"><span data-stu-id="0da5e-107">Changes include new technologies, systems, applications, hardware, tools, processes, and changes in roles and responsibilities.</span></span> <span data-ttu-id="0da5e-108">Um sistema de gerenciamento de alterações eficaz permite introduzir mudanças no ambiente de ti rapidamente e com interrupção mínima do serviço.</span><span class="sxs-lookup"><span data-stu-id="0da5e-108">An effective change management system lets you introduce changes to the IT environment quickly and with minimal service disruption.</span></span> <span data-ttu-id="0da5e-109">Um sistema de gerenciamento de alterações reúne as equipes envolvidas na alteração de um sistema.</span><span class="sxs-lookup"><span data-stu-id="0da5e-109">A change management system brings together the teams involved in changing a system.</span></span> <span data-ttu-id="0da5e-110">Por exemplo, decidir tirar proveito dos Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="0da5e-110">For example, deciding to take advantage of the Office Web Apps.</span></span> <span data-ttu-id="0da5e-111">Esse é um aplicativo de serviço do Lync integrado que permite aos usuários ler e editar documentos em um navegador.</span><span class="sxs-lookup"><span data-stu-id="0da5e-111">This is an integrated Lync Service application that enables users to read and edit documents in a browser.</span></span> <span data-ttu-id="0da5e-112">A implementação desse serviço, após você ter entrado em produção, requer o envolvimento de várias equipes:</span><span class="sxs-lookup"><span data-stu-id="0da5e-112">The implementation of this service, after you have gone into production, requires the involvement of several teams:</span></span>

  - <span data-ttu-id="0da5e-113">**Equipe de teste**   Esta carga de equipe testa o Office Web Apps em um servidor de teste, no processo, que fornece informações sobre os padrões de uso esperados e o desempenho esperado dos servidores de produção.</span><span class="sxs-lookup"><span data-stu-id="0da5e-113">**Test Team**   This team load-tests the Office Web Apps on a test server, in the process providing information about the expected usage patterns and expected performance of the production servers.</span></span>

  - <span data-ttu-id="0da5e-114">**Administradores do Lync**   Essa equipe determina a estratégia de implantação e os scripts que a instalação foi possível.</span><span class="sxs-lookup"><span data-stu-id="0da5e-114">**Lync Administrators**   This team determines the deployment strategy and scripts the installation where it was possible.</span></span> <span data-ttu-id="0da5e-115">A equipe é responsável por verificar se a alteração foi implantada no ambiente de produção e se é responsável por administração posteriormente.</span><span class="sxs-lookup"><span data-stu-id="0da5e-115">The team is responsible for making sure that the change is deployed on the production environment, and it is responsible for administration afterward.</span></span> <span data-ttu-id="0da5e-116">A equipe deve entender o efeito das alterações e incorporá-las nos procedimentos antes que as alterações sejam colocadas em produção</span><span class="sxs-lookup"><span data-stu-id="0da5e-116">The team must understand the effect of the changes and incorporate them in procedures before the changes are put into production</span></span>

  - <span data-ttu-id="0da5e-117">**Equipe de rede**   Esta equipe é responsável por alterações nas regras de firewall que permitem o acesso da Internet aos servidores do pool interno do Lync.</span><span class="sxs-lookup"><span data-stu-id="0da5e-117">**Network Team**   This team is responsible for changes to firewall rules that allow access from the Internet to the internal Lync pool servers.</span></span> <span data-ttu-id="0da5e-118">A equipe também é responsável por trabalhar com os administradores do Lync para garantir que a largura de banda disponível possa dar suporte à carga adicional.</span><span class="sxs-lookup"><span data-stu-id="0da5e-118">The team is also responsible in working with the Lync administrators for making sure that the available bandwidth can support the additional load.</span></span>

  - <span data-ttu-id="0da5e-119">**Equipe de segurança**   Esta equipe avalia a segurança e minimiza os riscos.</span><span class="sxs-lookup"><span data-stu-id="0da5e-119">**Security Team**   This team assesses security and minimizes risks.</span></span> <span data-ttu-id="0da5e-120">A equipe de segurança deve revisar as vulnerabilidades conhecidas e ajudar a garantir que os riscos de segurança sejam minimizados.</span><span class="sxs-lookup"><span data-stu-id="0da5e-120">The security team must review known vulnerabilities and help ensure that security risks are minimized.</span></span>

  - <span data-ttu-id="0da5e-121">**Equipe de aceitação do usuário**   Esta equipe é composta de usuários que estão dispostos a testar o sistema e oferecer comentários para melhorias.</span><span class="sxs-lookup"><span data-stu-id="0da5e-121">**User Acceptance Team**   This team is composed of users who are willing to test the system and offer feedback for improvements.</span></span>

<span data-ttu-id="0da5e-122">O processo de gerenciamento de alterações define as responsabilidades de cada equipe e agenda o trabalho a ser realizado, a incorporação de verificações e testes onde elas são necessárias.</span><span class="sxs-lookup"><span data-stu-id="0da5e-122">The change management process defines the responsibilities of each team and schedules the work to be performed, incorporating checks and tests where they are required.</span></span> <span data-ttu-id="0da5e-123">Os controles de alteração irão variar dependendo da complexidade e do efeito esperado de uma alteração.</span><span class="sxs-lookup"><span data-stu-id="0da5e-123">Change controls will vary depending on the complexity and expected effect of a change.</span></span> <span data-ttu-id="0da5e-124">Elas podem variar de acordo com a aprovação automática das alterações, para alterar reuniões de revisão até análises completas no nível do projeto.</span><span class="sxs-lookup"><span data-stu-id="0da5e-124">They can vary from automatic approval of minor changes, to change review meetings, to full project-level reviews.</span></span> <span data-ttu-id="0da5e-125">Para explicar isso melhor, os grupos de alterações são discutidos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="0da5e-125">To explain this better, the groups of changes are discussed in this section.</span></span>

  - <span data-ttu-id="0da5e-126">**Alterações importantes**   Alterações importantes têm um efeito global no sistema e podem exigir entrada de várias equipes.</span><span class="sxs-lookup"><span data-stu-id="0da5e-126">**Major Changes**   Major changes have a global effect on the system and may require input from various teams.</span></span> <span data-ttu-id="0da5e-127">Um exemplo disso é a atualização para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0da5e-127">An example of this is upgrading to Lync Server 2013.</span></span> <span data-ttu-id="0da5e-128">Alterações importantes afetam muitas equipes e, talvez, sistemas diferentes.</span><span class="sxs-lookup"><span data-stu-id="0da5e-128">Major changes affect many teams and perhaps different systems.</span></span> <span data-ttu-id="0da5e-129">O processo de gerenciamento de alterações provavelmente incluirá uma ou mais reuniões de revisão de alterações para informar as equipes que serão envolvidas na alteração ou que serão afetadas pela alteração.</span><span class="sxs-lookup"><span data-stu-id="0da5e-129">The change management process will probably include one or more change review meetings to inform the teams that will be involved in the change or be affected by the change.</span></span>

  - <span data-ttu-id="0da5e-130">**Alterações significativas**   Alterações significativas exigem recursos significativos para planejar, criar e implementar.</span><span class="sxs-lookup"><span data-stu-id="0da5e-130">**Significant Changes**   Significant changes require significant resources to plan, build, and implement.</span></span> <span data-ttu-id="0da5e-131">Os controles de alteração apropriados devem ser introduzidos para ajudar a garantir que o efeito da alteração seja entendido, que os procedimentos de implantação sejam testados e que os planos de reversão e contingência estejam prontos.</span><span class="sxs-lookup"><span data-stu-id="0da5e-131">Appropriate change controls should be introduced to help make ensure that the effect of the change is understood, deployment procedures are tested, and the rollback and contingency plans are ready.</span></span> <span data-ttu-id="0da5e-132">Um exemplo de uma alteração significativa é implantar uma nova atualização cumulativa.</span><span class="sxs-lookup"><span data-stu-id="0da5e-132">An example of a significant change is deploying a new cumulative update.</span></span>

  - <span data-ttu-id="0da5e-133">**Pequenas alterações**   Pequenas alterações não afetam significativamente o ambiente de ti, por exemplo, alterar determinadas políticas do Lync por meio do painel de controle do Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0da5e-133">**Minor Changes**   Minor changes do not significantly affect the IT environment, for example, changing certain Lync policies via the Microsoft Lync Server 2013 Control Panel.</span></span>

  - <span data-ttu-id="0da5e-134">**Alterações padrão**   As alterações padrão são executadas regularmente e são bem compreendidas e documentadas.</span><span class="sxs-lookup"><span data-stu-id="0da5e-134">**Standard Changes**   Standard changes are performed regularly and are well understood and documented.</span></span> <span data-ttu-id="0da5e-135">O processo de gerenciamento de alterações deve revisar todas as alterações nos procedimentos.</span><span class="sxs-lookup"><span data-stu-id="0da5e-135">The change management process should review all changes to the procedures.</span></span> <span data-ttu-id="0da5e-136">Ele não deve ser necessário para mudanças de rotina, como criar um banco de dados de conteúdo ou adicionar um usuário.</span><span class="sxs-lookup"><span data-stu-id="0da5e-136">It should not be needed for routine changes like creating a content database or adding a user.</span></span>

<span data-ttu-id="0da5e-137">O exemplo a seguir de gerenciamento de alterações examina como as diferentes equipes interagem e as ações que são executadas quando um novo Service Pack é implantado.</span><span class="sxs-lookup"><span data-stu-id="0da5e-137">The following example of change management examines how different teams interact and the actions that are performed when a new service pack is deployed.</span></span> <span data-ttu-id="0da5e-138">Essas ações são organizadas e gerenciadas pelo processo de gerenciamento de alterações.</span><span class="sxs-lookup"><span data-stu-id="0da5e-138">These actions are organized and managed by the change management process.</span></span>

  - <span data-ttu-id="0da5e-139">**Disparar uma solicitação de alteração**   A equipe de segurança avaliou o Service Pack mais recente e confirmou que ele resolve uma possível vulnerabilidade no sistema de produção.</span><span class="sxs-lookup"><span data-stu-id="0da5e-139">**Raise a change request**   The security team has assessed the latest service pack and confirmed that it resolves a possible vulnerability in the production system.</span></span> <span data-ttu-id="0da5e-140">A equipe eleva uma solicitação de alteração para ter a nova atualização cumulativa aplicada a todos os servidores que executam o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0da5e-140">The team raises a change request to have the new cumulative update applied to all servers that are running Lync Server.</span></span>

  - <span data-ttu-id="0da5e-141">**Análise das notas de versão do Service Pack**   A equipe de administradores do Lync revisa as notas de versão do Service Pack para identificar o efeito no sistema.</span><span class="sxs-lookup"><span data-stu-id="0da5e-141">**Service pack release notes review**   The Lync administrator team reviews the service pack release notes to identify the effect on the system.</span></span>

  - <span data-ttu-id="0da5e-142">**Uma série de testes de laboratório é realizada**   A equipe do administrador do Lync deve executar atualizações de teste em um servidor em um ambiente de teste para decidir se o Service Pack pode ser aplicado com êxito sem afetar qualquer um dos aplicativos e sistemas de servidor instalados.</span><span class="sxs-lookup"><span data-stu-id="0da5e-142">**A series of lab tests is performed**   The Lync administrator team must perform test updates on a server in a test environment to decide whether the service pack can be applied successfully without affecting any of the installed applications and server systems.</span></span> <span data-ttu-id="0da5e-143">Se houver aplicativos de terceiros ou criados internamente que fazem interface com o Lync Server em um ambiente de produção, eles também deverão ser testados.</span><span class="sxs-lookup"><span data-stu-id="0da5e-143">If there are third-party or internally created applications that interface with Lync Server in a production environment, these should be also tested.</span></span> <span data-ttu-id="0da5e-144">Esses testes também podem ser usados para estimar o tempo necessário para executar as atualizações.</span><span class="sxs-lookup"><span data-stu-id="0da5e-144">These tests can also be used to estimate the time that is required to perform the upgrades.</span></span>

  - <span data-ttu-id="0da5e-145">**Os usuários são informados sobre a interrupção**   A equipe do administrador do Lync, a equipe de comunicações ou o suporte técnico do usuário informa todos os usuários afetados sobre o ciclo de manutenção planejado e por quanto tempo o serviço estará indisponível.</span><span class="sxs-lookup"><span data-stu-id="0da5e-145">**Users are informed of the outage**   The Lync administrator team, communications team, or user help desk informs all affected users about the planned maintenance cycle and how long the service will be unavailable.</span></span>

  - <span data-ttu-id="0da5e-146">**Um backup completo do Lync é executado antes da atualização**   A equipe de administrador do Lync deve verificar se há um backup válido que pode ser usado para reverter para o estado do sistema original se a instalação do Service Pack falhar.</span><span class="sxs-lookup"><span data-stu-id="0da5e-146">**A full backup of Lync is performed before the upgrade**   The Lync administrator team must verify that there is a valid backup that can be used to revert to the original system state if the service pack installation fails.</span></span> <span data-ttu-id="0da5e-147">Recomendamos que o backup seja restaurado para um servidor em standby para que esse sistema seja imediatamente disponibilizado se houver problemas.</span><span class="sxs-lookup"><span data-stu-id="0da5e-147">We recommend that the backup be restored to a standby server to have this system readily available if there are issues.</span></span>

  - <span data-ttu-id="0da5e-148">**A atualização cumulativa está implantada**   A equipe do administrador do Lync faz a instalação durante o ciclo de manutenção planejado.</span><span class="sxs-lookup"><span data-stu-id="0da5e-148">**The cumulative update is deployed**   The Lync administrator team does the installation during the planned maintenance cycle.</span></span>

<div>

## <a name="managing-the-timing-of-changes"></a><span data-ttu-id="0da5e-149">Gerenciando o intervalo de alterações</span><span class="sxs-lookup"><span data-stu-id="0da5e-149">Managing the timing of changes</span></span>

<span data-ttu-id="0da5e-150">Recomendamos que você implemente um procedimento para agendar alterações para evitar interrupções em seções sobrepostas do seu trabalho.</span><span class="sxs-lookup"><span data-stu-id="0da5e-150">We recommend that you implement a procedure for scheduling changes to avoid disruptions in overlapping sections of your work.</span></span> <span data-ttu-id="0da5e-151">Por exemplo, duas equipes podem estar planejando uma pequena alteração para um sistema.</span><span class="sxs-lookup"><span data-stu-id="0da5e-151">For example, two teams may both be planning a minor change to a system.</span></span> <span data-ttu-id="0da5e-152">Uma equipe pode estar aplicando uma atualização cumulativa em um pool enquanto outra equipe está migrando os usuários herdados para esse pool.</span><span class="sxs-lookup"><span data-stu-id="0da5e-152">One team may be applying a cumulative update on a pool while another team is migrating legacy users into that pool.</span></span> <span data-ttu-id="0da5e-153">Nenhuma equipe é afetada pelas alterações que a outra equipe está planejando, e cada equipe pode não necessariamente saber sobre alterações que a outra equipe está planejando.</span><span class="sxs-lookup"><span data-stu-id="0da5e-153">Neither team is affected by the changes that the other team is planning, and each team may not necessarily know about changes that the other team is planning.</span></span> <span data-ttu-id="0da5e-154">Se ambas as alterações ocorrerem ao mesmo tempo, pode haver problemas para implementar as alterações.</span><span class="sxs-lookup"><span data-stu-id="0da5e-154">If both changes occurred at the same time, there might be issues implementing the changes.</span></span> <span data-ttu-id="0da5e-155">Além disso, se houver problemas após a aplicação das alterações, por exemplo, se a migração do usuário falhar, pode ser difícil decidir qual alteração deve ser revertida.</span><span class="sxs-lookup"><span data-stu-id="0da5e-155">Also, if there are issues after the changes were applied, for example, if the user migration fails, it may be difficult to decide which change should be rolled back.</span></span> <span data-ttu-id="0da5e-156">Deve haver períodos de manutenção regulares configurados entre ti e gerenciamento para testar as alterações e aceitá-las.</span><span class="sxs-lookup"><span data-stu-id="0da5e-156">There should be regular maintenance periods set up between IT and management to test the changes and accept them.</span></span>

<span data-ttu-id="0da5e-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0da5e-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

