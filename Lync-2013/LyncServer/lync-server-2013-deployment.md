---
title: 'Lync Server 2013: implantação'
description: 'Lync Server 2013: implantação.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment
ms:assetid: 83bd43ee-c1fe-4b38-bfa7-3eb382817bf9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398664(v=OCS.15)
ms:contentKeyID: 48184687
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 750dabf9659327b19e80006d1bca05090f22fd43
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429584"
---
# <a name="deployment-of-lync-server-2013"></a><span data-ttu-id="890b8-103">Implantação do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-103">Deployment of Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="890b8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="890b8-104">

<span> </span></span></span>

<span data-ttu-id="890b8-105">_**Tópico da última modificação:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="890b8-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="890b8-106">A implantação do software de comunicação do Lync Server 2013 inclui a preparação dos serviços de domínio do Active Directory, a implantação de servidores de front-end e outros componentes principais do Lync Server 2013 e a implantação de funções e recursos adicionais do servidor que sua organização pode exigir, como acesso a usuários externos e Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="890b8-106">Deployment of Lync Server 2013 communications software includes preparing Active Directory Domain Services, deploying the Front End Servers and other core Lync Server 2013 internal components, and then deploying any additional server roles and features that your organization may require, such as external user access and Enterprise Voice.</span></span>

<span data-ttu-id="890b8-107">Esta documentação descreve três cenários para a implantação do Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="890b8-107">This documentation describes three scenarios for deploying Lync Server 2013:</span></span>

  - <span data-ttu-id="890b8-108">Nova implantação do Lync Server 2013, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="890b8-108">New Deployment of Lync Server 2013, Enterprise Edition</span></span>

  - <span data-ttu-id="890b8-109">Nova implantação do Lync Server 2013, Standard Edition</span><span class="sxs-lookup"><span data-stu-id="890b8-109">New Deployment of Lync Server 2013, Standard Edition</span></span>

  - <span data-ttu-id="890b8-110">Nova implantação do Lync Server 2013 Standard Edition ou Enterprise Edition em uma implantação existente do Lync Server 2010 Standard Edition ou Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="890b8-110">New Deployment of Lync Server 2013 Standard Edition or Enterprise Edition into an existing Lync Server 2010 Standard Edition or Enterprise Edition deployment</span></span>

<span data-ttu-id="890b8-111">Para obter informações sobre a implantação do Lync Server 2013 em um ambiente existente do Microsoft Office Communications Server 2007 ou do Microsoft Office Communications Server 2007 R2, consulte a documentação de [migração](migration.md) .</span><span class="sxs-lookup"><span data-stu-id="890b8-111">For information about deploying Lync Server 2013 in an existing Microsoft Office Communications Server 2007 or Microsoft Office Communications Server 2007 R2 environment, see the [Migration](migration.md) documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="890b8-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="890b8-112">In This Section</span></span>

  - [<span data-ttu-id="890b8-113">Implantando o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-113">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)

  - [<span data-ttu-id="890b8-114">Implantação de acesso do usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-114">Deploying external user access in Lync Server 2013</span></span>](lync-server-2013-deploying-external-user-access.md)

  - [<span data-ttu-id="890b8-115">Implantando o Enterprise Voice no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-115">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)

  - [<span data-ttu-id="890b8-116">Implantando o monitoramento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-116">Deploying monitoring in Lync Server 2013</span></span>](lync-server-2013-deploying-monitoring.md)

  - [<span data-ttu-id="890b8-117">Implantando Arquivamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-117">Deploying Archiving in Lync Server 2013</span></span>](lync-server-2013-deploying-archiving.md)

  - [<span data-ttu-id="890b8-118">Configurando conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-118">Configuring dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-configuring-dial-in-conferencing.md)

  - [<span data-ttu-id="890b8-119">Planejamento e implantação de vídeo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-119">Planning and deploying video in Lync Server 2013</span></span>](lync-server-2013-planning-and-deploying-video.md)

  - [<span data-ttu-id="890b8-120">Implantando sites de filial no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-120">Deploying branch sites in Lync Server 2013</span></span>](lync-server-2013-deploying-branch-sites.md)

  - [<span data-ttu-id="890b8-121">Implantando Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-121">Deploying Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-deploying-persistent-chat-server.md)

  - [<span data-ttu-id="890b8-122">Implantando clientes e dispositivos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-122">Deploying clients and devices in Lync Server 2013</span></span>](lync-server-2013-deploying-clients-and-devices.md)

  - [<span data-ttu-id="890b8-123">Planejando e implantando o repositório de contatos unificado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-123">Planning and deploying unified contact store in Lync Server 2013</span></span>](lync-server-2013-planning-and-deploying-unified-contact-store.md)

  - [<span data-ttu-id="890b8-124">Gerenciamento de aplicativos de parceiros e autenticação de servidor para servidor (OAuth) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-124">Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013</span></span>](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md)

  - [<span data-ttu-id="890b8-125">Atualização da versão de avaliação do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-125">Updating from the evaluation version of Lync Server 2013</span></span>](lync-server-2013-updating-from-the-evaluation-version.md)

  - [<span data-ttu-id="890b8-126">Implantando controle de chamada remota no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-126">Deploying remote call control in Lync Server 2013</span></span>](lync-server-2013-deploying-remote-call-control.md)

  - [<span data-ttu-id="890b8-127">Implantando mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-127">Deploying mobility in Lync Server 2013</span></span>](lync-server-2013-deploying-mobility.md)

  - [<span data-ttu-id="890b8-128">Configurando a integração com o Office Web Apps Server e o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-128">Configuring integration with Office Web Apps Server and Lync Server 2013</span></span>](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md)

  - [<span data-ttu-id="890b8-129">Configuração de integridade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="890b8-129">Health configuration in Lync Server 2013</span></span>](lync-server-2013-health-configuration-in-lync-server.md)

<span data-ttu-id="890b8-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="890b8-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

