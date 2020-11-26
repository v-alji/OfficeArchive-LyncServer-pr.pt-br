---
title: 'Lync Server 2013: detalhes do agendamento de reuniões'
description: 'Lync Server 2013: detalhes do agendamento de reuniões.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scheduling details
ms:assetid: 39ca6fff-2c15-4347-9f1f-6c8687a39a49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204823(v=OCS.15)
ms:contentKeyID: 48183910
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef7a6907aedbc880731b3fb474c9294c1c111b80
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442010"
---
# <a name="scheduling-details-for-meetings-in-lync-server-2013"></a><span data-ttu-id="4ed22-103">Detalhes de agendamento de reuniões no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4ed22-103">Scheduling details for meetings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4ed22-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4ed22-104">

<span> </span></span></span>

<span data-ttu-id="4ed22-105">_**Tópico da última modificação:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="4ed22-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="4ed22-106">Depois de fazer uma verificação para assegurar que nenhuma outra reunião esteja agendada na hora solicitada, a equipe de suporte a grandes reuniões, que lida com a solicitação, agenda a reunião no pool de grandes reuniões.</span><span class="sxs-lookup"><span data-stu-id="4ed22-106">After checking to ensure that no other meeting is scheduled at the requested time, the large meeting support staff that handles the request schedules the meeting on the large-meeting pool.</span></span> <span data-ttu-id="4ed22-107">Use o suplemento de reunião online para o Lync que está instalado com o cliente do Lync Server 2013 para executar essa tarefa, usando as credenciais de um usuário habilitado para o Lync Server no pool de reunião longa dedicada.</span><span class="sxs-lookup"><span data-stu-id="4ed22-107">Use the Online Meeting Add-in for Lync that is installed with the Lync Server 2013 client to perform this task, using the credentials of a user enabled for Lync Server in the dedicated large-meeting pool.</span></span>

<span data-ttu-id="4ed22-108">Para assegurar a melhor experiência do usuário, é importante agendar a grande reunião com os níveis de acesso corretos e as configurações da reunião que são apropriadas para as necessidades do organizador da reunião.</span><span class="sxs-lookup"><span data-stu-id="4ed22-108">To ensure the best user experience, it is important to schedule the large meeting with the right access levels and meeting settings that are appropriate to the meeting organizer’s needs.</span></span> <span data-ttu-id="4ed22-109">Recomendamos as seguintes configurações de agendamento definidas nas opções de reunião do Lync:</span><span class="sxs-lookup"><span data-stu-id="4ed22-109">We recommend the following scheduling settings configured in Lync Meeting options:</span></span>

  - <span data-ttu-id="4ed22-110">Use um novo espaço de reunião para cada grande reunião em vez de reutilizar o espaço dedicado da reunião.</span><span class="sxs-lookup"><span data-stu-id="4ed22-110">Use a new meeting space for each large meeting instead of reusing the dedicated meeting space.</span></span>

  - <span data-ttu-id="4ed22-111">Especifique os níveis de acesso à reunião conforme segue:</span><span class="sxs-lookup"><span data-stu-id="4ed22-111">Specify the meeting access level as follows:</span></span>
    
      - <span data-ttu-id="4ed22-112">Se pelo menos um convidado for externo à organização, defina o tipo de acesso à reunião para **qualquer pessoa (sem restrições**).</span><span class="sxs-lookup"><span data-stu-id="4ed22-112">If at least one invitee is external to the organization, set the meeting access type to **Anyone (no restrictions**.</span></span> <span data-ttu-id="4ed22-113">Isso habilita você a evitar o gerenciamento de um possível grande lobby quando a reunião estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="4ed22-113">This enables you to avoid having to manage a potentially large lobby when the meeting is in progress.</span></span>
    
      - <span data-ttu-id="4ed22-114">Se a reunião for somente interna, defina o tipo de acesso à reunião como **Para qualquer pessoa da minha organização**.</span><span class="sxs-lookup"><span data-stu-id="4ed22-114">If the meeting is an internal-only meeting, set the meeting access type to **Anyone from my organization**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="4ed22-115">Evite definir o tipo de acesso à reunião como <STRONG>Pessoas que eu convidar da minha empresa</STRONG>, pois, quando essa configuração é usada, os organizadores devem adicionar todos os endereços de email em uma lista de convidados e você não poderá convidar um grupo de distribuição.</span><span class="sxs-lookup"><span data-stu-id="4ed22-115">Avoid setting the meeting access type to <STRONG>People I invite from my company</STRONG> because when you use this setting, organizers must add all user email addresses to the invitee list and you cannot invite a distribution group.</span></span><BR><span data-ttu-id="4ed22-116">Evite definir o tipo de acesso à reunião como <STRONG>Apenas eu, o organizador da reunião</STRONG>, pois essa configuração exige que todos os participantes da reunião, inclusive os apresentadores, sejam colocados no lobby durante a reunião.</span><span class="sxs-lookup"><span data-stu-id="4ed22-116">Avoid setting the meeting access type to <STRONG>Only me, the meeting organizer</STRONG> because this setting requires that every meeting participant, including presenters, must be put in the lobby at meeting run time.</span></span> <span data-ttu-id="4ed22-117">A pessoa responsável pela execução da grande reunião deverá monitorar a escalação do lobby e aceitar os novos usuários que estiverem no lobby.</span><span class="sxs-lookup"><span data-stu-id="4ed22-117">The person responsible for running the large meeting must then constantly monitor the lobby roster and admit new users who are in the lobby.</span></span>

        
        </div>

  - <span data-ttu-id="4ed22-118">Permita que usuários que ligam de telefones entrem na reunião automaticamente marcando a configuração **Chamadores entram diretamente**.</span><span class="sxs-lookup"><span data-stu-id="4ed22-118">Allow users who dial-in from phones to enter the meeting automatically by checking the **Callers get in directly** setting.</span></span>

  - <span data-ttu-id="4ed22-119">Convide explicitamente os seguintes usuários:</span><span class="sxs-lookup"><span data-stu-id="4ed22-119">Explicitly invite the following users:</span></span>
    
      - <span data-ttu-id="4ed22-120">Organizador e representante da reunião (solicitante)</span><span class="sxs-lookup"><span data-stu-id="4ed22-120">Meeting organizer and delegate (requester)</span></span>
    
      - <span data-ttu-id="4ed22-121">A lista de apresentadores fornecida pelo solicitante da reunião</span><span class="sxs-lookup"><span data-stu-id="4ed22-121">The list of presenters provided by a meeting requester</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4ed22-122">Se o tipo de acesso à reunião estiver definido como <STRONG>Pessoas que eu escolher</STRONG>, será preciso adicionar explicitamente cada participante da grande reunião como convidado da reunião.</span><span class="sxs-lookup"><span data-stu-id="4ed22-122">If the meeting access type is set to <STRONG>People I choose</STRONG>, you need to explicitly add each participant of a large meeting as an invitee of the meeting.</span></span>

    
    </div>

  - <span data-ttu-id="4ed22-p105">Gerencie explicitamente os apresentadores, em vez de definir a opção de apresentador como um dos valores promovidos automaticamente. Certifique-se de adicionar os seguintes usuários como apresentadores:</span><span class="sxs-lookup"><span data-stu-id="4ed22-p105">Explicitly manage presenters, instead of setting the presenter option to one of the auto-promote values. Be sure to add the following users as presenters:</span></span>
    
      - <span data-ttu-id="4ed22-125">Organizador e representante da reunião (solicitante)</span><span class="sxs-lookup"><span data-stu-id="4ed22-125">Meeting organizer and delegate (requester)</span></span>
    
      - <span data-ttu-id="4ed22-126">A lista de apresentadores fornecida pelo solicitantes da grande reunião</span><span class="sxs-lookup"><span data-stu-id="4ed22-126">The list of presenters provided by large meeting requesters</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4ed22-127">Ao gerenciar explicitamente os apresentadores, você pode controlar o número de apresentadores, para que você possa limitar apresentadores a um número pequeno o suficiente para que seja possível ter uma reunião grande em vigor.</span><span class="sxs-lookup"><span data-stu-id="4ed22-127">By explicitly managing presenters, you can control the number of presenters, so that you can limit presenters to a small enough number to make it possible to have an effective large meeting.</span></span> <span data-ttu-id="4ed22-128">Se a maioria dos participantes da reunião tiver a função de participante, serão reduzidas as chances de alguém acidentalmente assumir o controle da apresentação, excluir a apresentação do PowerPoint, ativar/desativar o áudio dos apresentadores e outras interrupções na reunião.</span><span class="sxs-lookup"><span data-stu-id="4ed22-128">If the majority of meeting participants have the attendee role, it helps reduce the chance of people accidentally taking control of the presentation, deleting a PowerPoint presentation, muting/unmuting presenters, and other disruptions to the meeting.</span></span>

    
    </div>

  - <span data-ttu-id="4ed22-129">Marque a configuração **Desativar o áudio de todos os participantes** para assegurar que apenas os apresentadores possam transmitir áudio para a reunião.</span><span class="sxs-lookup"><span data-stu-id="4ed22-129">Check the **Mute all attendees** setting to make sure that only presenters can broadcast audio into the meeting.</span></span>

  - <span data-ttu-id="4ed22-130">Marque a configuração **Bloquear vídeo dos participantes** para assegurar que apenas os apresentadores possam transmitir vídeo para a reunião.</span><span class="sxs-lookup"><span data-stu-id="4ed22-130">Check the **Block attendees’ video** setting to make sure only presenters can broadcast video into the meeting.</span></span>

<span data-ttu-id="4ed22-131">A figura a seguir mostra as configurações recomendadas para o suplemento de reunião online do Lync.</span><span class="sxs-lookup"><span data-stu-id="4ed22-131">The following figure shows the recommended settings for the Online Meeting Add-in for Lync.</span></span>

<span data-ttu-id="4ed22-132">![54e4e70d-06b0-45cd-8d94-bab649cd5dc0](images/JJ204823.54e4e70d-06b0-45cd-8d94-bab649cd5dc0(OCS.15).jpg "54e4e70d-06b0-45cd-8d94-bab649cd5dc0")</span><span class="sxs-lookup"><span data-stu-id="4ed22-132">![54e4e70d-06b0-45cd-8d94-bab649cd5dc0](images/JJ204823.54e4e70d-06b0-45cd-8d94-bab649cd5dc0(OCS.15).jpg "54e4e70d-06b0-45cd-8d94-bab649cd5dc0")</span></span>

<span data-ttu-id="4ed22-133"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4ed22-133"></div>

<span> </span>

</div>

</div>

</span></span></div>

