---
title: 'Lync Server 2013: Pré-requisitos e funções de configuração de Comunicado'
description: 'Lync Server 2013: pré-requisitos e funções de configuração do anúncio.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Announcement configuration prerequisites and roles
ms:assetid: 82f2dfe9-4c5e-4d65-96a1-96495d506ea4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398658(v=OCS.15)
ms:contentKeyID: 48184674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8e6e7009adc6826c255e28ddda925b0e9be5fd6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439965"
---
# <a name="announcement-configuration-prerequisites-and-roles-in-lync-server-2013"></a><span data-ttu-id="c4e65-103">Pré-requisitos e funções de configuração de Comunicado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4e65-103">Announcement configuration prerequisites and roles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c4e65-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c4e65-104">

<span> </span></span></span>

<span data-ttu-id="c4e65-105">_**Tópico da última modificação:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="c4e65-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="c4e65-106">O anúncio é um recurso de gerenciamento de chamadas de voz empresarial.</span><span class="sxs-lookup"><span data-stu-id="c4e65-106">Announcement is an Enterprise Voice call management feature.</span></span> <span data-ttu-id="c4e65-107">Este tópico descreve o que você precisa ter em vigor antes de poder configurar as atribuições de anúncio e de função necessárias para executar tarefas de configuração.</span><span class="sxs-lookup"><span data-stu-id="c4e65-107">This topic describes what you need to have in place before you can configure Announcement and the role assignments that you need to perform configuration tasks.</span></span>

<span data-ttu-id="c4e65-108">Esta seção pressupõe que você leu a documentação de planejamento relacionada ao anúncio (consulte [planejando os recursos de gerenciamento de chamadas no Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span><span class="sxs-lookup"><span data-stu-id="c4e65-108">This section assumes that you have read the planning documentation related to Announcement (see [Planning for call management features in Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span></span>

<div>

## <a name="announcement-configuration-prerequisites"></a><span data-ttu-id="c4e65-109">Pré-requisitos de configuração do comunicado</span><span class="sxs-lookup"><span data-stu-id="c4e65-109">Announcement Configuration Prerequisites</span></span>

<span data-ttu-id="c4e65-110">O aplicativo de anúncio requer os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="c4e65-110">The Announcement application requires the following components:</span></span>

  - <span data-ttu-id="c4e65-111">Serviço de aplicativos</span><span class="sxs-lookup"><span data-stu-id="c4e65-111">Application service</span></span>

  - <span data-ttu-id="c4e65-112">Aplicativo Grupo de Resposta</span><span class="sxs-lookup"><span data-stu-id="c4e65-112">Response Group application</span></span>

  - <span data-ttu-id="c4e65-113">Armazenamento de arquivos, para armazenar arquivos de áudio</span><span class="sxs-lookup"><span data-stu-id="c4e65-113">File Store, to hold audio files</span></span>

<span data-ttu-id="c4e65-114">Todos esses componentes são instalados por padrão quando você implanta o Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="c4e65-114">All of these components are installed by default when you deploy Enterprise Voice.</span></span>

</div>

<div>

## <a name="announcement-configuration-roles"></a><span data-ttu-id="c4e65-115">Funções de configuração do anúncio</span><span class="sxs-lookup"><span data-stu-id="c4e65-115">Announcement Configuration Roles</span></span>

<span data-ttu-id="c4e65-116">Você pode usar as seguintes ferramentas administrativas para configurar comunicados:</span><span class="sxs-lookup"><span data-stu-id="c4e65-116">You can use the following administrative tools to configure announcements:</span></span>

  - <span data-ttu-id="c4e65-117">Painel de Controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="c4e65-117">Lync Server Control Panel</span></span>

  - <span data-ttu-id="c4e65-118">Shell de Gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="c4e65-118">Lync Server Management Shell</span></span>

<span data-ttu-id="c4e65-119">A configuração do aplicativo de anúncio requer uma das seguintes funções administrativas:</span><span class="sxs-lookup"><span data-stu-id="c4e65-119">Configuring Announcement application requires one of the following administrative roles:</span></span>

  - <span data-ttu-id="c4e65-120">**CsVoiceAdministrator**   Essa função de administrador pode criar, configurar e gerenciar todas as configurações e políticas relacionadas a voz, incluindo configurações de anúncio.</span><span class="sxs-lookup"><span data-stu-id="c4e65-120">**CsVoiceAdministrator**   This administrator role can create, configure, and manage all voice-related settings and policies, including Announcement settings.</span></span>

  - <span data-ttu-id="c4e65-121">**CsServerAdministrator**   Essa função de administrador pode gerenciar, monitorar e solucionar problemas de servidores e serviços e configurar todas as configurações de anúncio.</span><span class="sxs-lookup"><span data-stu-id="c4e65-121">**CsServerAdministrator**   This administrator role can manage, monitor, and troubleshoot servers and services, and configure all Announcement settings.</span></span>

  - <span data-ttu-id="c4e65-122">**CsAdministrator**   Essa função de administrador pode executar todas as tarefas administrativas e modificar todas as configurações.</span><span class="sxs-lookup"><span data-stu-id="c4e65-122">**CsAdministrator**   This administrator role can perform all administrative tasks and modify all settings.</span></span>

  - <span data-ttu-id="c4e65-123">**CsViewOnlyAdministrator**   Essa função de administrador pode exibir a implantação para monitorar a integridade da implantação.</span><span class="sxs-lookup"><span data-stu-id="c4e65-123">**CsViewOnlyAdministrator**   This administrator role can view the deployment to monitor deployment health.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c4e65-124">Para obter detalhes sobre direitos de usuário administrativo, consulte <A href="lync-server-2013-planning-for-role-based-access-control.md">planejando o controle de acesso baseado em função no Lync Server 2013</A> na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="c4e65-124">For details about administrative user rights, see <A href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c4e65-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4e65-125">See Also</span></span>


[<span data-ttu-id="c4e65-126">Implantando o Enterprise Voice no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4e65-126">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  


[<span data-ttu-id="c4e65-127">Planejando os recursos de gerenciamento de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4e65-127">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="c4e65-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c4e65-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

