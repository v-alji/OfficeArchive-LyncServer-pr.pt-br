---
title: 'Lync Server 2013: Configurar política de conferência para discagem'
description: 'Lync Server 2013: configurar a política de conferência para discagem.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure conferencing policy for dial-in
ms:assetid: 9bf926d6-0248-4352-98c3-9c5a333debbc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398810(v=OCS.15)
ms:contentKeyID: 48184979
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd8dee1d9e7e6391c6420b15a895199dfc7a8791
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390368"
---
# <a name="configure-conferencing-policy-for-dial-in-in-lync-server-2013"></a><span data-ttu-id="6a67c-103">Configurar política de conferência para discagem no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6a67c-103">Configure conferencing policy for dial-in in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6a67c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6a67c-104">

<span> </span></span></span>

<span data-ttu-id="6a67c-105">_**Tópico da última modificação:** 2014-03-21_</span><span class="sxs-lookup"><span data-stu-id="6a67c-105">_**Topic Last Modified:** 2014-03-21_</span></span>

<span data-ttu-id="6a67c-p101">A política de conferência é uma configuração de conta de usuário que especifica a experiência de conferência para os participantes. Você pode criar políticas de conferência com um escopo de site ou um escopo de usuário. As configurações de política de conferência englobam vários aspectos do agendamento da conferência e da participação. Várias configurações de política de conferência oferecem suporte à conferência discada para participantes. Ao configurar a conferência discada, você deve verificar se estes campos foram definidos adequadamente para sua organização e modificá-los conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="6a67c-p101">Conferencing policy is a user account setting that specifies the conferencing experience for participants. You can create conferencing policies with a site scope or a user scope. Conferencing policy settings encompass many aspects of conference scheduling and participation. Several conferencing policy settings support dial-in conferencing for participants. When you configure dial-in conferencing, you should verify that these fields are set appropriately for your organization, and modify them as necessary.</span></span>

<span data-ttu-id="6a67c-111">Verifique os seguintes campos na sua política de conferência:</span><span class="sxs-lookup"><span data-stu-id="6a67c-111">Verify the following fields in your conferencing policy:</span></span>

  - <span data-ttu-id="6a67c-112">**Permitir que os participantes convidem usuários anônimos**   Essa configuração permite que os organizadores de reunião convidem participantes anônimos (ou seja, não autenticados) para reuniões.</span><span class="sxs-lookup"><span data-stu-id="6a67c-112">**Allow participants to invite anonymous users**   This setting allows meeting organizers to invite anonymous (that is, unauthenticated) participants to meetings.</span></span> <span data-ttu-id="6a67c-113">Essa configuração é opcional para conferência discada.</span><span class="sxs-lookup"><span data-stu-id="6a67c-113">This setting is optional for dial-in conferencing.</span></span> <span data-ttu-id="6a67c-114">Essa configuração é selecionada por padrão na política de conferência global padrão.</span><span class="sxs-lookup"><span data-stu-id="6a67c-114">This setting is selected by default in the default global conferencing policy.</span></span>

  - <span data-ttu-id="6a67c-115">**Habilitar conferência discada PSTN**   Essa configuração permite que os usuários ingressem na parte de áudio de uma conferência discando da PSTN.</span><span class="sxs-lookup"><span data-stu-id="6a67c-115">**Enable PSTN dial-in conferencing**   This setting allows users to join the audio portion of a conference by dialing in from the PSTN.</span></span> <span data-ttu-id="6a67c-116">Essa configuração é necessária para conferência discada.</span><span class="sxs-lookup"><span data-stu-id="6a67c-116">This setting is required for dial-in conferencing.</span></span> <span data-ttu-id="6a67c-117">Essa configuração é selecionada por padrão na política de conferência global padrão.</span><span class="sxs-lookup"><span data-stu-id="6a67c-117">This setting is selected by default in the default global conferencing policy.</span></span>

  - <span data-ttu-id="6a67c-118">**Permitir que participantes anônimos disquem**   Essa configuração permite que usuários anônimos que já estão associados à reunião disquem para um número de telefone para ingressar na parte de áudio da conferência.</span><span class="sxs-lookup"><span data-stu-id="6a67c-118">**Allow anonymous participants to dial out**   This setting allows anonymous users who are already joined to the meeting to dial out to a phone number to join the audio portion of the conference.</span></span> <span data-ttu-id="6a67c-119">Essa configuração é opcional para conferência discada.</span><span class="sxs-lookup"><span data-stu-id="6a67c-119">This setting is optional for dial-in conferencing.</span></span> <span data-ttu-id="6a67c-120">Essa configuração não é selecionada por padrão na política de conferência global padrão.</span><span class="sxs-lookup"><span data-stu-id="6a67c-120">This setting is not selected by default in the default global conferencing policy.</span></span>

  - <span data-ttu-id="6a67c-121">**Permitir que os participantes não habilitados para discagem do Enterprise Voice**   Essa configuração permite que os participantes da reunião e os organizadores que não estão habilitados para o Enterprise Voice disquem para um número de telefone para ingressar na parte de áudio da conferência.</span><span class="sxs-lookup"><span data-stu-id="6a67c-121">**Allow participants not enabled for Enterprise Voice to dial out**   This setting allows meeting participants and organizers that are not enabled for Enterprise Voice to dial out to a phone number to join the audio portion of the conference.</span></span> <span data-ttu-id="6a67c-122">A chamada de discagem está autorizada com base na política de voz atribuída do organizador.</span><span class="sxs-lookup"><span data-stu-id="6a67c-122">The dial-out call is authorized based on the organizer’s assigned voice policy.</span></span> <span data-ttu-id="6a67c-123">Essa configuração não é selecionada por padrão na política de conferência global padrão.</span><span class="sxs-lookup"><span data-stu-id="6a67c-123">This setting is not selected by default in the default global conferencing policy.</span></span> <span data-ttu-id="6a67c-124">A configuração do valor padrão é desabilitada.</span><span class="sxs-lookup"><span data-stu-id="6a67c-124">The setting default value is disabled.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6a67c-125">Para habilitar esse recurso, o organizador da reunião que não está habilitado para o Enterprise Voice deve ter uma política de voz apropriada atribuída a ele para autorizar qualquer discagem de uma conferência organizada por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="6a67c-125">To enable this capability, a meeting organizer that is not enabled for Enterprise Voice should have an appropriate voice policy assigned to them to authorize any dial-out from a conference organized by that user.</span></span> <span data-ttu-id="6a67c-126">Uma política de voz pode ser atribuída a um usuário que não está habilitado para o Enterprise Voice do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6a67c-126">A voice policy can be assigned to a user that is not enabled for Enterprise Voice from the Lync Server Management Shell.</span></span> <span data-ttu-id="6a67c-127">Se o usuário não tiver uma política de voz explicitamente atribuída a ele, a política de voz do site será usada para autorizar a solicitação de discagem.</span><span class="sxs-lookup"><span data-stu-id="6a67c-127">If the user does not have a voice policy explicitly assigned to him, the site voice policy will be used to authorize the dial-out request.</span></span> <span data-ttu-id="6a67c-128">Se não houver uma política de voz do site, a política de voz global será usada.&nbsp;</span><span class="sxs-lookup"><span data-stu-id="6a67c-128">If there is no site voice policy, the global voice policy will be used.&nbsp;</span></span>

    
    </div>

<span data-ttu-id="6a67c-129">O procedimento nesta seção explica como modificar a política de conferência.</span><span class="sxs-lookup"><span data-stu-id="6a67c-129">The procedure in this section explains how to modify conferencing policy.</span></span> <span data-ttu-id="6a67c-130">Para obter detalhes sobre como configurar todas as configurações que definem a experiência do participante na política de conferência padrão, consulte [criar ou modificar uma coleção de definições de configuração de reunião no Lync Server 2013](lync-server-2013-create-or-modify-a-collection-of-meeting-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="6a67c-130">For details about how to configure all of the settings that define the participant experience in the default conferencing policy, see [Create or modify a collection of meeting configuration settings in Lync Server 2013](lync-server-2013-create-or-modify-a-collection-of-meeting-configuration-settings.md).</span></span> <span data-ttu-id="6a67c-131">Para obter detalhes sobre como criar uma política de conferência para um usuário ou grupo de usuários específico, consulte [criar ou modificar uma política de conferência no Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md).</span><span class="sxs-lookup"><span data-stu-id="6a67c-131">For details about how to create a conferencing policy for a specific user or group of users, see [Create or modify a conferencing policy in Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md).</span></span> <span data-ttu-id="6a67c-132">Para obter uma lista de todas as configurações de política de conferência disponíveis, consulte [referência de configurações de política de conferência para o Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).</span><span class="sxs-lookup"><span data-stu-id="6a67c-132">For a list of all available conferencing policy settings, see [Conferencing policy settings reference for Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).</span></span>

<div>

## <a name="to-modify-the-conferencing-policy-for-dial-in"></a><span data-ttu-id="6a67c-133">Para modificar a política de conferência para discagem</span><span class="sxs-lookup"><span data-stu-id="6a67c-133">To modify the conferencing policy for dial-in</span></span>

1.  <span data-ttu-id="6a67c-134">Faça logon no computador como membro do grupo RTCUniversalServerAdmins ou como membro da função **cs-ServerAdministrator** ou **CsAdministrator** .</span><span class="sxs-lookup"><span data-stu-id="6a67c-134">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-ServerAdministrator** or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="6a67c-135">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6a67c-135">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="6a67c-136">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6a67c-136">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="6a67c-137">Na barra de navegação esquerda, clique em **Conferência**.</span><span class="sxs-lookup"><span data-stu-id="6a67c-137">In the left navigation bar, click **Conferencing**.</span></span>

4.  <span data-ttu-id="6a67c-138">Na guia **política de conferência** , clique duas vezes em um nome de política de conferência para abrir a caixa de diálogo **Editar política de conferência** .</span><span class="sxs-lookup"><span data-stu-id="6a67c-138">On the **Conferencing Policy** tab, double-click a conferencing policy name to open the **Edit Conferencing Policy** dialog box.</span></span>

5.  <span data-ttu-id="6a67c-139">Verifique se os campos para conferência discada são adequados para sua organização e modifique as configurações, se necessário.</span><span class="sxs-lookup"><span data-stu-id="6a67c-139">Verify that the fields for dial-in conferencing are appropriate for your organization, and modify the settings if necessary.</span></span>

6.  <span data-ttu-id="6a67c-140">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="6a67c-140">Click **Commit**.</span></span>

<span data-ttu-id="6a67c-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6a67c-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

