---
title: 'Lync Server 2013: considerações de migração para reuniões'
description: 'Lync Server 2013: considerações de migração para reuniões.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration considerations for meetings
ms:assetid: a9807d58-99a3-4cff-b4c6-74950d106a2b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412800(v=OCS.15)
ms:contentKeyID: 61097556
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e238405acf7bc2a96fd2efd4cca761c1f1f258fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425581"
---
# <a name="migration-considerations-for-meetings-in-lync-server-2013"></a><span data-ttu-id="7240a-103">Considerações de migração para reuniões no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7240a-103">Migration considerations for meetings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7240a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7240a-104">

<span> </span></span></span>

<span data-ttu-id="7240a-105">_**Tópico da última modificação:** 2014-02-10_</span><span class="sxs-lookup"><span data-stu-id="7240a-105">_**Topic Last Modified:** 2014-02-10_</span></span>

<span data-ttu-id="7240a-106">Os tópicos a seguir são discutidos nesta seção:</span><span class="sxs-lookup"><span data-stu-id="7240a-106">The following topics are discussed in this section:</span></span>

  - <span data-ttu-id="7240a-107">Alterações nas reuniões no Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7240a-107">Changes to meetings in Microsoft Lync Server 2013</span></span>

  - <span data-ttu-id="7240a-108">Migrando usuários com base nas necessidades de conferência</span><span class="sxs-lookup"><span data-stu-id="7240a-108">Migrating users based on their conferencing needs</span></span>

  - <span data-ttu-id="7240a-109">Migrando reuniões e conteúdo de reunião existentes</span><span class="sxs-lookup"><span data-stu-id="7240a-109">Migrating existing meetings and meeting content</span></span>

  - <span data-ttu-id="7240a-110">Experiência do usuário durante a migração do Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="7240a-110">User experience during Lync Server 2010 migration</span></span>

  - <span data-ttu-id="7240a-111">Experiência do usuário durante a migração do Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="7240a-111">User Experience during Office Communications Server 2007 R2 migration</span></span>

  - <span data-ttu-id="7240a-112">Compatibilidade do Microsoft Lync 2013 com reuniões em versões anteriores do servidor</span><span class="sxs-lookup"><span data-stu-id="7240a-112">Microsoft Lync 2013 compatibility with meetings on earlier server versions</span></span>

<div>

## <a name="changes-to-meetings-in-lync-server-2013"></a><span data-ttu-id="7240a-113">Alterações nas reuniões no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7240a-113">Changes to Meetings in Lync Server 2013</span></span>

<span data-ttu-id="7240a-114">**Recursos do Lync Server 2013.**</span><span class="sxs-lookup"><span data-stu-id="7240a-114">**Lync Server 2013 features.**</span></span>   <span data-ttu-id="7240a-115">O Lync Server 2013 oferece novos recursos de conferência que se tornam disponíveis para os usuários após suas contas serem movidos para o Lync Server 2013 e que entram com o cliente Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="7240a-115">Lync Server 2013 provides new conferencing features that become available to users after their accounts are moved to Lync Server 2013 and they sign in with the Lync 2013 client.</span></span> <span data-ttu-id="7240a-116">Novos recursos estão descritos nos [novos recursos de conferência do Lync server 2013](lync-server-2013-new-conferencing-features.md) e novidades [para clientes no Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span><span class="sxs-lookup"><span data-stu-id="7240a-116">New features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="7240a-117">**URL da reunião.**</span><span class="sxs-lookup"><span data-stu-id="7240a-117">**Meeting URL.**</span></span>   <span data-ttu-id="7240a-118">Como no Lync Server 2010, todas as reuniões agendadas recentemente no Lync Server 2013 têm um prefixo de URL de https://e as reuniões existentes são migradas juntamente com as contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="7240a-118">As in Lync Server 2010, all newly scheduled meetings in Lync Server 2013 have a URL prefix of https:// and existing meetings migrate along with user accounts.</span></span> <span data-ttu-id="7240a-119">No entanto, o Lync Server 2013 não é compatível com a chamada em conferência do Office Communications Server 2007 R2 (prefixo da URL conf://) ou conferência via Web (prefixo da URL meet://).</span><span class="sxs-lookup"><span data-stu-id="7240a-119">However, Lync Server 2013 does not support the Office Communications Server 2007 R2 conference call (conf:// URL prefix) or web conference (meet:// URL prefix).</span></span> <span data-ttu-id="7240a-120">Consulte "migrando reuniões do Office Communications Server 2007 R2" mais adiante neste tópico para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="7240a-120">See “Migrating Meetings from Office Communications Server 2007 R2” later in this topic for more information.</span></span>

<span data-ttu-id="7240a-121">**Suporte ao cliente.**</span><span class="sxs-lookup"><span data-stu-id="7240a-121">**Client support.**</span></span>   <span data-ttu-id="7240a-122">Ao contrário do Lync Server 2010, o Lync Server 2013 não é compatível com clientes do Office Communicator para conferência.</span><span class="sxs-lookup"><span data-stu-id="7240a-122">Unlike Lync Server 2010, Lync Server 2013 does not support Office Communicator clients for conferencing.</span></span> <span data-ttu-id="7240a-123">Você não pode usar os seguintes clientes para ingressar em reuniões agendadas por meio do suplemento de reunião online do Lync 2013:</span><span class="sxs-lookup"><span data-stu-id="7240a-123">You cannot use the following clients to join meetings scheduled through the Online Meeting Add-in for Lync 2013:</span></span>

  - <span data-ttu-id="7240a-124">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="7240a-124">Office Communicator 2007 R2</span></span>

  - <span data-ttu-id="7240a-125">Microsoft Office Communications Server 2007 R2 Attendant</span><span class="sxs-lookup"><span data-stu-id="7240a-125">Microsoft Office Communications Server 2007 R2 Attendant</span></span>

  - <span data-ttu-id="7240a-126">Office Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="7240a-126">Office Communicator 2007</span></span>

  - <span data-ttu-id="7240a-127">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="7240a-127">Office Live Meeting 2007</span></span>

<span data-ttu-id="7240a-128">Durante a migração, os usuários do Office Communicator 2007 R2 devem usar o Lync Web App 2013 para ingressar em reuniões do Lync Server 2013 até que seus clientes sejam atualizados.</span><span class="sxs-lookup"><span data-stu-id="7240a-128">During migration, Office Communicator 2007 R2 users should use Lync Web App 2013 to join Lync Server 2013 meetings until their clients are upgraded.</span></span> <span data-ttu-id="7240a-129">Observe que os usuários do Office Communicator 2007 R2 podem continuar a usar o cliente existente no Lync Server 2013 para recursos de presença e IM, mas os recursos de conferência não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="7240a-129">Note that Office Communicator 2007 R2 users can continue to use their existing client against Lync Server 2013 for presence and IM features, but conferencing features are not supported.</span></span>

<div>


</div>

</div>

<div>

## <a name="migrating-users-based-on-their-conferencing-needs"></a><span data-ttu-id="7240a-130">Migrando usuários com base nas necessidades de conferência</span><span class="sxs-lookup"><span data-stu-id="7240a-130">Migrating Users Based on Their Conferencing Needs</span></span>

<span data-ttu-id="7240a-131">**Organizadores de reuniões frequentes.**</span><span class="sxs-lookup"><span data-stu-id="7240a-131">**Frequent meeting organizers.**</span></span>   <span data-ttu-id="7240a-132">Considere migrar os organizadores de reunião frequentes no início do processo para que possam aproveitar os novos recursos do Lync Server 2013 e do Lync 2013 descritos nos [novos recursos de conferência do Lync server 2013](lync-server-2013-new-conferencing-features.md) e novidades [para clientes no Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span><span class="sxs-lookup"><span data-stu-id="7240a-132">Consider migrating frequent meeting organizers early in the process so that they can take advantage of the new Lync Server 2013 and Lync 2013 features outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="7240a-133">**Usuários do Live Meeting.**</span><span class="sxs-lookup"><span data-stu-id="7240a-133">**Live Meeting users.**</span></span>   <span data-ttu-id="7240a-134">Se você estiver migrando do Office Communications Server 2007 R2 e tiver usuários que precisem de recursos de Webconferência específicos do Live Meeting, particularmente o suporte para reuniões grandes e salas de desativação, você terá as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="7240a-134">If you are migrating from Office Communications Server 2007 R2 and you have users who need web conferencing features specific to Live Meeting—particularly support for large meetings and break-out rooms—you have the following options:</span></span>

  - <span data-ttu-id="7240a-135">Organizadores de recomendação para usar o serviço Live Meeting, se disponível em sua organização.</span><span class="sxs-lookup"><span data-stu-id="7240a-135">Advise organizers to use the Live Meeting service, if available in your organization.</span></span>

  - <span data-ttu-id="7240a-136">Deixe os organizadores em casa na versão anterior do Office Communications Server, para que eles possam continuar a agendar conferências da Web de reunião ao vivo baseadas em servidor.</span><span class="sxs-lookup"><span data-stu-id="7240a-136">Leave the organizers homed on the earlier version of Office Communications Server, so they can continue to schedule server-based Live Meeting web conferences.</span></span>

</div>

<div>

## <a name="migrating-existing-meetings-and-meeting-content"></a><span data-ttu-id="7240a-137">Migrando reuniões e conteúdo de reunião existentes</span><span class="sxs-lookup"><span data-stu-id="7240a-137">Migrating Existing Meetings and Meeting Content</span></span>

<div>

## <a name="migrating-meetings-from-lync-server-2010"></a><span data-ttu-id="7240a-138">Migrando reuniões do Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="7240a-138">Migrating Meetings from Lync Server 2010</span></span>

<span data-ttu-id="7240a-139">Quando você move um usuário do Lync Server 2010 para o Lync Server 2013, as seguintes informações se movem com a conta do usuário:</span><span class="sxs-lookup"><span data-stu-id="7240a-139">When you move a user from Lync Server 2010 to Lync Server 2013, the following information moves with the user’s account:</span></span>

  - <span data-ttu-id="7240a-140">Reuniões já programadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="7240a-140">Meetings already scheduled by the user.</span></span> <span data-ttu-id="7240a-141">Isso inclui diretórios de conferência e dados de conferência.</span><span class="sxs-lookup"><span data-stu-id="7240a-141">This includes conferencing directories and conferencing data.</span></span>

  - <span data-ttu-id="7240a-142">O PIN (número de identificação pessoal) do usuário.</span><span class="sxs-lookup"><span data-stu-id="7240a-142">The user’s personal identification number (PIN).</span></span> <span data-ttu-id="7240a-143">O PIN atual do usuário continua a funcionar até que ele expire ou que o usuário solicitou um novo PIN.</span><span class="sxs-lookup"><span data-stu-id="7240a-143">The user’s current PIN continues to work until it expires or the user requests a new PIN.</span></span>

<span data-ttu-id="7240a-144">No entanto, as seguintes informações da conta de usuário não se movem para o novo servidor:</span><span class="sxs-lookup"><span data-stu-id="7240a-144">However, the following user account information does not move to the new server:</span></span>

  - <span data-ttu-id="7240a-145">Conteúdo da reunião, por exemplo, apresentações do PowerPoint, conteúdo do quadro de comunicações e dados de votação</span><span class="sxs-lookup"><span data-stu-id="7240a-145">Meeting content, for example PowerPoint presentations, whiteboard content, and poll data</span></span>

<span data-ttu-id="7240a-146">Para mover o conteúdo que foi compartilhado em reuniões, use o parâmetro MoveMeetingContent do cmdlet Move-CsUser.</span><span class="sxs-lookup"><span data-stu-id="7240a-146">To move the content that has been shared in meetings, use the MoveMeetingContent parameter of the Move-CsUser cmdlet.</span></span> <span data-ttu-id="7240a-147">Para obter detalhes sobre como usar esse cmdlet, consulte [move-CsUser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) na documentação de cmdlets do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7240a-147">For details about using this cmdlet, see [Move-CsUser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) in the Lync Server 2013 cmdlets documentation.</span></span>

</div>

<div>

## <a name="migrating-meetings-from-office-communications-server-2007-r2"></a><span data-ttu-id="7240a-148">Migrando reuniões do Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="7240a-148">Migrating Meetings from Office Communications Server 2007 R2</span></span>

<span data-ttu-id="7240a-149">As reuniões do Office Communications Server 2007 R2 são chamadas em conferência (prefixo de URL conf://) ou conferências via Web (prefixo de URL meet://).</span><span class="sxs-lookup"><span data-stu-id="7240a-149">Office Communications Server 2007 R2 meetings are either conference calls (conf:// URL prefix) or web conferences (meet:// URL prefix).</span></span> <span data-ttu-id="7240a-150">O Lync Server 2013 não é compatível com essas conferências anteriores do conf://e do meet://, e elas não são migradas juntamente com a conta do usuário.</span><span class="sxs-lookup"><span data-stu-id="7240a-150">Lync Server 2013 does not support these earlier conf:// and meet:// conferences, and they are not migrated along with the user account.</span></span> <span data-ttu-id="7240a-151">Após a migração, você deve instruir os usuários a atualizar os links para todas as reuniões online agendadas.</span><span class="sxs-lookup"><span data-stu-id="7240a-151">After migration, you should instruct users to update the links for any online meetings they have scheduled.</span></span> <span data-ttu-id="7240a-152">Isso pode fazer isso após a instalação do cliente do Lync 2013 abrindo um convite de reunião agendada, que atualiza a URL da reunião, e reenvia o convite aos participantes.</span><span class="sxs-lookup"><span data-stu-id="7240a-152">They can do this after installing the Lync 2013 client by opening a scheduled meeting invitation—which updates the meeting URL—and resending the invitation to participants.</span></span>

</div>

</div>

<div>

## <a name="user-experience-during-lync-server-2010-migration"></a><span data-ttu-id="7240a-153">Experiência do usuário durante a migração do Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="7240a-153">User Experience during Lync Server 2010 Migration</span></span>

<span data-ttu-id="7240a-154">Esta seção fornece um resumo da experiência de Conferência dos usuários durante a migração do Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="7240a-154">This section provides a summary of users’ conferencing experience when migrating from Lync 2010.</span></span> <span data-ttu-id="7240a-155">Para obter mais detalhes sobre como os clientes do Lync Server 2013 podem coexistir e interagir com versões anteriores do cliente e do servidor, consulte [interoperabilidade do cliente no Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span><span class="sxs-lookup"><span data-stu-id="7240a-155">For more details about how Lync Server 2013 clients can coexist and interact with previous client and server versions, see [Client interoperability in Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span></span>

<div>

## <a name="joining-lync-server-2010-meetings-with-a-lync-2013-client"></a><span data-ttu-id="7240a-156">Ingressando em reuniões do Lync Server 2010 com um cliente do Lync 2013</span><span class="sxs-lookup"><span data-stu-id="7240a-156">Joining Lync Server 2010 Meetings with a Lync 2013 Client</span></span>

<span data-ttu-id="7240a-157">Durante a migração do Lync Server 2010, pode haver um período de coexistência quando os usuários ingressam em reuniões do Lync Server 2010 com um cliente Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="7240a-157">During migration from Lync Server 2010, there may be a period of coexistence when users join Lync Server 2010 meetings with a Lync 2013 client.</span></span> <span data-ttu-id="7240a-158">Esses usuários têm acesso aos recursos do cliente do Lync 2013 com as seguintes exceções:</span><span class="sxs-lookup"><span data-stu-id="7240a-158">These users have access to Lync 2013 client features with the following exceptions:</span></span>

  - <span data-ttu-id="7240a-159">Nas opções de gerenciamento de **participantes** , que podem ser acessadas apontando para o ícone pessoas na janela da reunião, a opção **nenhuma mensagem instantânea de reunião** não funciona.</span><span class="sxs-lookup"><span data-stu-id="7240a-159">In the **Participants** management options, which are accessible by pointing to the people icon in the meeting window, the **No Meeting IM** option does not function.</span></span>

  - <span data-ttu-id="7240a-160">O modo de exibição de galeria não funciona em videoconferências.</span><span class="sxs-lookup"><span data-stu-id="7240a-160">Gallery View does not function in video conferences.</span></span> <span data-ttu-id="7240a-161">O usuário vê apenas o alto-falante ativo em vez de todos os alto-falantes.</span><span class="sxs-lookup"><span data-stu-id="7240a-161">The user sees only the active speaker instead of all speakers.</span></span> <span data-ttu-id="7240a-162">Na lista de opções **escolher um layout** , o **modo de exibição Galeria** não está disponível</span><span class="sxs-lookup"><span data-stu-id="7240a-162">In the list of **Pick a Layout** options, **Gallery View** is unavailable</span></span>

  - <span data-ttu-id="7240a-163">A lista de participantes é exibida por padrão em videoconferências.</span><span class="sxs-lookup"><span data-stu-id="7240a-163">The participant list displays by default in video conferences.</span></span>

  - <span data-ttu-id="7240a-164">Ao clicar com o botão direito do mouse em um usuário na lista de participantes, o botão **bloquear as opções de gerenciamento de participantes do vídeo** e **fixar em Galeria** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="7240a-164">When right-clicking a user in the participants list, the **Lock the Video Spotlight** and **Pin to Gallery** participant management options are unavailable.</span></span>

</div>

</div>

<div>

## <a name="user-experience-during-office-communications-server-2007-r2-migration"></a><span data-ttu-id="7240a-165">Experiência do usuário durante a migração do Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="7240a-165">User Experience during Office Communications Server 2007 R2 Migration</span></span>

<span data-ttu-id="7240a-166">Esta seção fornece um resumo da experiência de Conferência dos usuários ao migrar do Office Communications Server 2007 R2, antes e depois que o Lync 2013 está instalado.</span><span class="sxs-lookup"><span data-stu-id="7240a-166">This section provides a summary of users’ conferencing experience when migrating from Office Communications Server 2007 R2, both before and after Lync 2013 is installed.</span></span> <span data-ttu-id="7240a-167">Para obter mais detalhes sobre como os clientes do Lync Server 2013 podem coexistir e interagir com versões anteriores do cliente e do servidor, consulte [interoperabilidade do cliente no Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span><span class="sxs-lookup"><span data-stu-id="7240a-167">For more details about how Lync Server 2013 clients can coexist and interact with previous client and server versions, see [Client interoperability in Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span></span>

<div>

## <a name="after-user-account-is-migrated-before-lync-2013-is-installed"></a><span data-ttu-id="7240a-168">Após a migração da conta de usuário, antes que o Lync 2013 seja instalado</span><span class="sxs-lookup"><span data-stu-id="7240a-168">After User Account is Migrated, Before Lync 2013 Is Installed</span></span>

<span data-ttu-id="7240a-169">Após a migração de um usuário para o servidor do Lync Server 2013, mas antes de novos clientes serem instalados, os usuários do Office Communicator 2007 R2 podem continuar a usar o cliente existente no Lync Server 2013 para recursos de presença e IM, mas os recursos de conferência não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="7240a-169">After a user is migrated to the Lync Server 2013 server, but before new clients are installed, Office Communicator 2007 R2 users can continue to use their existing client against Lync Server 2013 for presence and IM features, but conferencing features are not supported.</span></span>

</div>

<div>

## <a name="after-user-account-is-migrated-after-lync-2013-is-installed"></a><span data-ttu-id="7240a-170">Após a migração da conta de usuário, após a instalação do Lync 2013</span><span class="sxs-lookup"><span data-stu-id="7240a-170">After User Account is Migrated, After Lync 2013 Is Installed</span></span>

<span data-ttu-id="7240a-171">Quando um usuário migrado instalar o Lync 2013, o suplemento de reunião online do Lync 2013 também será instalado.</span><span class="sxs-lookup"><span data-stu-id="7240a-171">When a migrated user installs Lync 2013, the Online Meeting Add-in for Lync 2013 is installed too.</span></span> <span data-ttu-id="7240a-172">Isso tem os seguintes efeitos:</span><span class="sxs-lookup"><span data-stu-id="7240a-172">This has the following effects:</span></span>

  - <span data-ttu-id="7240a-173">Todas as reuniões agendadas subsequentemente usam o novo formato de reunião, que usa um endereço https://em vez do endereço herdado do Live Meeting do meet://.</span><span class="sxs-lookup"><span data-stu-id="7240a-173">All subsequently scheduled meetings use the new meeting format, which uses an https:// address instead of the legacy meet:// Live Meeting address.</span></span>

  - <span data-ttu-id="7240a-174">Em uma implantação gerenciada por ti do Lync 2013, o administrador tem a opção de desinstalar o suplemento de conferência do Microsoft Office Outlook, que é usado para agendar reuniões com base em serviço e servidor de reunião ao vivo.</span><span class="sxs-lookup"><span data-stu-id="7240a-174">In an IT-managed deployment of Lync 2013, the administrator has the option of uninstalling the Conferencing Add-in for Microsoft Office Outlook, which is used to schedule Live Meeting server and service-based meetings.</span></span> <span data-ttu-id="7240a-175">No entanto, você pode ter usuários que precisam continuar a agendar reuniões do serviço Live Meeting.</span><span class="sxs-lookup"><span data-stu-id="7240a-175">However, you may have users who need to continue to schedule Live Meeting service meetings.</span></span> <span data-ttu-id="7240a-176">Nesse caso, você pode permitir que ambos os suplementos coexistam.</span><span class="sxs-lookup"><span data-stu-id="7240a-176">In this case, you can allow both add-ins to coexist.</span></span>

</div>

<div>

## <a name="meetings-with-federated-organizations-that-use-previous-clients"></a><span data-ttu-id="7240a-177">Reuniões com organizações federadas que usam clientes anteriores</span><span class="sxs-lookup"><span data-stu-id="7240a-177">Meetings with Federated Organizations that Use Previous Clients</span></span>

<span data-ttu-id="7240a-178">Os usuários de organizações federadas que estiverem usando o Microsoft Office Communicator 2007 não poderão ingressar em reuniões do Lync Server 2013 em sua organização se essas reuniões estiverem bloqueadas pelo organizador.</span><span class="sxs-lookup"><span data-stu-id="7240a-178">Users in federated organizations who are using Microsoft Office Communicator 2007 cannot join Lync Server 2013 meetings in your organization if those meetings are locked by the organizer.</span></span> <span data-ttu-id="7240a-179">Você precisa reagendar essas reuniões no Lync Server 2013 para que os participantes federados ingressem na reunião usando a nova URL de reunião do https://, eles podem usar o Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="7240a-179">You have to reschedule these meetings in Lync Server 2013 so when federated participants join the meeting by using the new https:// meeting URL, they can use Lync Web App.</span></span>

<span data-ttu-id="7240a-180"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7240a-180"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

