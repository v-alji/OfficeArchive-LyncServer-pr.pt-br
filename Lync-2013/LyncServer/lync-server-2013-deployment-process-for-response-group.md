---
title: 'Lync Server 2013: processo de implantação do grupo de respostas'
description: 'Lync Server 2013: processo de implantação para o grupo de resposta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for Response Group
ms:assetid: d390c8a1-dc6e-44d8-b386-2be1fca9877c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205270(v=OCS.15)
ms:contentKeyID: 48185437
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b50fb7903a2fcc301bbf435013b8f8df4e775a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429654"
---
# <a name="deployment-process-for-response-group-in-lync-server-2013"></a><span data-ttu-id="4d1b7-103">Processo de implantação para o grupo de resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4d1b7-103">Deployment process for Response Group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4d1b7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4d1b7-104">

<span> </span></span></span>

<span data-ttu-id="4d1b7-105">_**Tópico da última modificação:** 2012-09-27_</span><span class="sxs-lookup"><span data-stu-id="4d1b7-105">_**Topic Last Modified:** 2012-09-27_</span></span>

<span data-ttu-id="4d1b7-106">Esta seção fornece uma visão geral das fases e etapas envolvidas na implantação do aplicativo de grupo de resposta.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-106">This section provides an overview of the phases and steps involved in deploying the Response Group application.</span></span>

### <a name="response-group-deployment-process"></a><span data-ttu-id="4d1b7-107">Processo de implantação do grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="4d1b7-107">Response Group Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d1b7-108">Fase</span><span class="sxs-lookup"><span data-stu-id="4d1b7-108">Phase</span></span></th>
<th><span data-ttu-id="4d1b7-109">Etapas</span><span class="sxs-lookup"><span data-stu-id="4d1b7-109">Steps</span></span></th>
<th><span data-ttu-id="4d1b7-110">Permissões</span><span class="sxs-lookup"><span data-stu-id="4d1b7-110">Permissions</span></span></th>
<th><span data-ttu-id="4d1b7-111">Documentação de Implantação</span><span class="sxs-lookup"><span data-stu-id="4d1b7-111">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d1b7-112">Instalar o aplicativo grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="4d1b7-112">Install the Response Group application</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-113">O aplicativo grupo de resposta é instalado e ativado por padrão ao implantar o Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-113">The Response Group application is installed and activated by default when you deploy Enterprise Voice.</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-114">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="4d1b7-114">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-115"><a href="lync-server-2013-deploying-enterprise-voice.md">Implantando o Enterprise Voice no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4d1b7-115"><a href="lync-server-2013-deploying-enterprise-voice.md">Deploying Enterprise Voice in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d1b7-116">Instalar componentes para o grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="4d1b7-116">Install components for Response Group</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-117">Cmdlets do Lync Server, o painel de controle do Lync Server, a ferramenta de configuração do grupo de resposta, o console de entrada e saída do agente e o serviço Web do cliente do grupo de resposta são instalados como parte dos serviços Web.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-117">Lync Server cmdlets, the Lync Server Control Panel, Response Group Configuration Tool, agents' sign-in and sign-out console, and Response Group Client Web service are installed as part of Web Services.</span></span> <span data-ttu-id="4d1b7-118">Os serviços Web são instalados quando você implanta um pool da edição Enterprise ou um servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-118">Web Services is installed when you deploy an Enterprise Edition pool or a Standard Edition server.</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-119">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="4d1b7-119">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-120"><a href="lync-server-2013-deploying-lync-server.md">Implantando o Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4d1b7-120"><a href="lync-server-2013-deploying-lync-server.md">Deploying Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d1b7-121">Habilitar usuários do Lync 2013 e do Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="4d1b7-121">Enable users for Lync 2013 and for Enterprise Voice</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-122">Habilite os usuários que serão agentes do Lync Server e do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-122">Enable users who will be agents for Lync Server and Enterprise Voice.</span></span> <span data-ttu-id="4d1b7-123">Os usuários devem ser habilitados para que você possa adicioná-los a grupos de agente.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-123">Users must be enabled before you can add them to agent groups.</span></span> <span data-ttu-id="4d1b7-124">Normalmente, os usuários estão habilitados para o Lync Server durante a implantação do servidor Enterprise Edition ou Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-124">Typically, users are enabled for Lync Server during the Enterprise Edition or Standard Edition server deployment.</span></span> <span data-ttu-id="4d1b7-125">Os usuários estão habilitados para o Enterprise Voice durante a implantação do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-125">Users are enabled for Enterprise Voice during the Enterprise Voice deployment.</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-126">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="4d1b7-126">RTCUniversalUserAdmins</span></span></p>
<p><span data-ttu-id="4d1b7-127">CsUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d1b7-127">CsUserAdministrator</span></span></p>
<p><span data-ttu-id="4d1b7-128">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d1b7-128">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-129"><a href="lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md">Desabilitar ou habilitar novamente a conta de usuário para o Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4d1b7-129"><a href="lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md">Disable or re-enable user account for Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="4d1b7-130"><a href="lync-server-2013-enable-users-for-enterprise-voice.md">Habilitar usuários para Enterprise Voice no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4d1b7-130"><a href="lync-server-2013-enable-users-for-enterprise-voice.md">Enable users for Enterprise Voice in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d1b7-131">Criar e configurar grupos de resposta, que consistem em grupos de agentes, filas e fluxos de trabalho</span><span class="sxs-lookup"><span data-stu-id="4d1b7-131">Create and configure response groups, which consist of agent groups, queues, and workflows</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="4d1b7-132">Use o painel de controle do Lync Server ou o Shell de gerenciamento do Lync Server para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4d1b7-132">Use the Lync Server Control Panel or Lync Server Management Shell to do the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="4d1b7-133">Criar e configurar grupos de agentes.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-133">Create and configure agent groups.</span></span></p></li>
<li><p><span data-ttu-id="4d1b7-134">Criar e configurar filas.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-134">Create and configure queues.</span></span></p></li>
</ol></li>
<li><p><span data-ttu-id="4d1b7-135">Opcionalmente, use o Shell de gerenciamento do Lync Server para criar grupos de resposta predefinidos e horários comerciais e feriados.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-135">Optionally, use Lync Server Management Shell to create predefined response group business hours and holidays.</span></span></p></li>
<li><p><span data-ttu-id="4d1b7-136">Use a ferramenta de configuração de grupo de resposta ou o Shell de gerenciamento do Lync Server para criar fluxos de trabalho (grupos de chamadas ou fluxos de chamadas de voz interativa (IVR), incluindo o horário comercial do grupo de respostas e feriados.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-136">Use the Response Group Configuration Tool or Lync Server Management Shell to create workflows (hunt groups or interactive voice response (IVR) call flows), including custom response group business hours and holidays.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="4d1b7-137">Você pode acessar a ferramenta de configuração de grupo de resposta por meio do painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-137">You can access the Response Group Configuration Tool through Lync Server Control Panel.</span></span>


</div></li>
</ol></td>
<td><p><span data-ttu-id="4d1b7-138">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="4d1b7-138">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="4d1b7-139">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d1b7-139">CsResponseGroupAdministrator</span></span></p>
<p><span data-ttu-id="4d1b7-140">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d1b7-140">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="4d1b7-141">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d1b7-141">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="4d1b7-142">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d1b7-142">CsAdministrator</span></span></p>
<p><span data-ttu-id="4d1b7-143">CsResponseGroupManager</span><span class="sxs-lookup"><span data-stu-id="4d1b7-143">CsResponseGroupManager</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-144"><a href="lync-server-2013-create-response-group-agent-groups.md">Criar grupos de agente do Grupo de Resposta no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4d1b7-144"><a href="lync-server-2013-create-response-group-agent-groups.md">Create Response Group agent groups Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="4d1b7-145"><a href="lync-server-2013-create-response-group-queues.md">Criar filas do Grupo de Resposta no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4d1b7-145"><a href="lync-server-2013-create-response-group-queues.md">Create Response Group queues in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="4d1b7-146"><a href="lync-server-2013-optional-define-response-group-business-hours.md">Adicionais Definir o horário comercial do grupo de resposta no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4d1b7-146"><a href="lync-server-2013-optional-define-response-group-business-hours.md">(Optional) Define Response Group business hours in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="4d1b7-147"><a href="lync-server-2013-optional-define-response-group-holiday-sets.md">Adicionais Definir conjuntos de feriados do grupo de resposta no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4d1b7-147"><a href="lync-server-2013-optional-define-response-group-holiday-sets.md">(Optional) Define Response Group holiday sets in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="4d1b7-148"><a href="lync-server-2013-create-or-modify-a-workflow.md">Criar ou modificar um fluxo de trabalho no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4d1b7-148"><a href="lync-server-2013-create-or-modify-a-workflow.md">Create or modify a workflow in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d1b7-149">(Opcional) Personalizar configurações no nível de aplicativo</span><span class="sxs-lookup"><span data-stu-id="4d1b7-149">(Optional) Customize application-level settings</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-150">Use o Shell de gerenciamento do Lync Server para personalizar a configuração de música em espera padrão, o arquivo de áudio de música em espera padrão, o período de cortesia do agente e a configuração do contexto de chamada.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-150">Use Lync Server Management Shell to customize the default music-on-hold configuration, the default music-on-hold audio file, the agent ringback grace period, and the call context configuration.</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-151">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="4d1b7-151">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="4d1b7-152">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d1b7-152">CsResponseGroupAdministrator</span></span></p>
<p><span data-ttu-id="4d1b7-153">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d1b7-153">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="4d1b7-154">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d1b7-154">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="4d1b7-155">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d1b7-155">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-156"><a href="lync-server-2013-managing-application-level-response-group-settings.md">Gerenciando configurações de grupo de resposta no nível do aplicativo no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4d1b7-156"><a href="lync-server-2013-managing-application-level-response-group-settings.md">Managing application-level Response Group settings in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d1b7-157">(Opcional) Delegar o gerenciamento dos grupos de resposta</span><span class="sxs-lookup"><span data-stu-id="4d1b7-157">(Optional) Delegate management of response groups</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-158">Atribua aos usuários a função CsResponseGroupManager para delegar a configuração de grupos de resposta.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-158">Assign users the CsResponseGroupManager role to delegate configuration of response groups.</span></span> <span data-ttu-id="4d1b7-159">Os gerentes do grupo de resposta podem então configurar os grupos de resposta atribuídos a eles.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-159">Response Group Managers can then configure the response groups assigned to them.</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-160">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="4d1b7-160">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="4d1b7-161">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d1b7-161">CsResponseGroupAdministrator</span></span></p>
<p><span data-ttu-id="4d1b7-162">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d1b7-162">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="4d1b7-163">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d1b7-163">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="4d1b7-164">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d1b7-164">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-165"><a href="lync-server-2013-planning-for-role-based-access-control.md">Planejamento de controle de acesso baseado em função no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4d1b7-165"><a href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d1b7-166">Verificar a implantação do grupo de respostas</span><span class="sxs-lookup"><span data-stu-id="4d1b7-166">Verify your Response Group deployment</span></span></p></td>
<td><p><span data-ttu-id="4d1b7-167">Teste o atendimento de chamadas para seus fluxos de trabalho de resposta interativa de voz e grupos de busca, a fim de garantir que sua configuração funcione da maneira esperada.</span><span class="sxs-lookup"><span data-stu-id="4d1b7-167">Test answering calls to your hunt group and interactive voice response workflows to ensure that your configuration works as expected.</span></span></p></td>
<td><p>-</p></td>
<td><p>-</p></td>
</tr><span data-ttu-id="4d1b7-168">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4d1b7-168">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

