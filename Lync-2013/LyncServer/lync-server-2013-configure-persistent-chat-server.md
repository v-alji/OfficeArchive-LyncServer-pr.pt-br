---
title: 'Lync Server 2013: Configurar o Servidor de Chat Persistente'
description: 'Lync Server 2013: configurar o servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Persistent Chat Server
ms:assetid: 85028aff-a38e-4748-958e-59e707a47532
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205054(v=OCS.15)
ms:contentKeyID: 48184709
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d45320e1fa6b247f13cfffa9945b45390f2ae6c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433812"
---
# <a name="configure-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="eba32-103">Configurar o Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eba32-103">Configure Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eba32-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eba32-104">

<span> </span></span></span>

<span data-ttu-id="eba32-105">_**Tópico da última modificação:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="eba32-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="eba32-106">Para criar uma nova configuração de chat persistente</span><span class="sxs-lookup"><span data-stu-id="eba32-106">To create a new Persistent Chat configuration</span></span>

    New-CsPersistentChatConfiguration -Identity <XdsIdentity> [-DefaultChatHistory <Integer>] [-MaxChatContentSizeMB <Integer>] [-MaxFileSizeKB <Integer>] [-ParticipantUpdateLimit <Integer>] [-FileServiceUrl <UrlForFileUpload>] [-RoomManagementUrl <RoomManagementUrl>] [-Instance <PSObject>] [-Force <Switch Parameter>] [-Confirm <Switch Parameter>] [-WhatIf <Switch Parameter>]

<span data-ttu-id="eba32-107">Para obter configuração de chat persistente</span><span class="sxs-lookup"><span data-stu-id="eba32-107">To get Persistent Chat configuration</span></span>

    Get-CsPersistentChatConfiguration [-LocalStore <Switch Parameter>] [-Identity <XdsIdentity>]

<span data-ttu-id="eba32-108">Para remover a configuração de chat persistente</span><span class="sxs-lookup"><span data-stu-id="eba32-108">To remove Persistent Chat configuration</span></span>

    Remove-CsPersistentChatConfiguration -Identity <XdsIdentity>

<span data-ttu-id="eba32-109">Para definir a configuração de chat persistente</span><span class="sxs-lookup"><span data-stu-id="eba32-109">To set Persistent Chat configuration</span></span>

    Set-CsPersistentChatConfiguration [-DefaultChatHistory <Integer>] [-MaxChatContentSizeMB <Integer>] [-MaxFileSizeKB <Integer>] [-ParticipantUpdateLimit <Integer>] [-FileServiceUrl <UrlForFileUpload>] [-RoomManagementUrl <RoomManagementUrl>] [-Instance <PSObject >] [-Force <Switch Parameter>] [-Confirm <Switch Parameter>] [-WhatIf <Switch Parameter>]

<span data-ttu-id="eba32-110">Para o Lync Server 2013, todo o tráfego do serviço Web é compatível com os servidores do Lync Server 2013, front-end.</span><span class="sxs-lookup"><span data-stu-id="eba32-110">For Lync Server 2013, all web service traffic is supported on the Lync Server 2013, Front End Servers.</span></span> <span data-ttu-id="eba32-111">Portanto, o endereço gcweb01 no servidor de chat persistente não é necessário.</span><span class="sxs-lookup"><span data-stu-id="eba32-111">Therefore, the gcweb01 address on Persistent Chat Server is not necessary.</span></span> <span data-ttu-id="eba32-112">Ainda damos suporte ao acesso ao serviço Web interno porque fornecemos o serviço de carregamento/download da Web ao site *interno* somente (não para o site *externo* para usuários remotos).</span><span class="sxs-lookup"><span data-stu-id="eba32-112">We still support internal web service access because we provide the File Upload/Download Web service to the *internal* website only (not to the *external* website for remote users).</span></span>

<span data-ttu-id="eba32-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eba32-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

