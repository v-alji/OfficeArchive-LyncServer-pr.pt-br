---
title: 'Lync Server 2013: Suporte a Serviços de Domínio Active Directory'
description: 'Lync Server 2013: suporte a serviços de domínio Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory Domain Services support
ms:assetid: aeb62d5e-e424-473a-b795-9452150c98dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412831(v=OCS.15)
ms:contentKeyID: 48185136
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb2a85bab90557c28c4802721d4202f6188cb3f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389733"
---
# <a name="active-directory-domain-services-support-in-lync-server-2013"></a><span data-ttu-id="dafc7-103">Suporte a Serviços de Domínio Active Directory no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dafc7-103">Active Directory Domain Services support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dafc7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dafc7-104">

<span> </span></span></span>

<span data-ttu-id="dafc7-105">_**Tópico da última modificação:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="dafc7-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="dafc7-106">O Lync Server 2013 usa o repositório de gerenciamento central para armazenar dados de configuração para servidores e serviços, em vez de confiar nos serviços de domínio Active Directory para essas informações, como no passado.</span><span class="sxs-lookup"><span data-stu-id="dafc7-106">Lync Server 2013 uses the Central Management store to store configuration data for servers and services, instead of relying on Active Directory Domain Services for this information, as in the past.</span></span> <span data-ttu-id="dafc7-107">O Lync Server 2013 ainda armazena o seguinte no AD DS:</span><span class="sxs-lookup"><span data-stu-id="dafc7-107">Lync Server 2013 still stores the following in AD DS:</span></span>

  - <span data-ttu-id="dafc7-108">**Extensões de esquema**</span><span class="sxs-lookup"><span data-stu-id="dafc7-108">**Schema extensions**</span></span>
    
      - <span data-ttu-id="dafc7-109">Extensões de objetos de usuário</span><span class="sxs-lookup"><span data-stu-id="dafc7-109">User object extensions</span></span>
    
      - <span data-ttu-id="dafc7-110">Extensões para as classes do Lync Server 2010 e do Office Communications Server 2007 R2 para manter a compatibilidade com versões anteriores do suporte</span><span class="sxs-lookup"><span data-stu-id="dafc7-110">Extensions for Lync Server 2010 and Office Communications Server 2007 R2 classes to maintain backward compatibility with previous supported versions</span></span>

  - <span data-ttu-id="dafc7-111">**Dados** (armazenados no esquema estendido do Lync Server 2013 e em classes existentes)</span><span class="sxs-lookup"><span data-stu-id="dafc7-111">**Data** (stored in Lync Server 2013 extended schema and in existing classes)</span></span>
    
      - <span data-ttu-id="dafc7-112">URI do SIP do usuário e outras configurações de usuário</span><span class="sxs-lookup"><span data-stu-id="dafc7-112">User SIP URI and other user settings</span></span>
    
      - <span data-ttu-id="dafc7-113">Objetos de contato para aplicativos (por exemplo, o aplicativo do grupo de resposta e o aplicativo do atendente de conferência)</span><span class="sxs-lookup"><span data-stu-id="dafc7-113">Contact objects for applications (for example, the Response Group application and the Conferencing Attendant application)</span></span>
    
      - <span data-ttu-id="dafc7-114">Dados publicados para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="dafc7-114">Data published for backward compatibility</span></span>
    
      - <span data-ttu-id="dafc7-115">Um SCP (ponto de controle de serviço) para o repositório de gerenciamento central</span><span class="sxs-lookup"><span data-stu-id="dafc7-115">A service control point (SCP) for the Central Management store</span></span>
    
      - <span data-ttu-id="dafc7-116">Conta de autenticação Kerberos (um objeto de computador opcional)</span><span class="sxs-lookup"><span data-stu-id="dafc7-116">Kerberos Authentication Account (an optional computer object)</span></span>

<span data-ttu-id="dafc7-117">Esta seção descreve os requisitos de suporte do AD DS para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dafc7-117">This section describes the AD DS support requirements for Lync Server 2013.</span></span> <span data-ttu-id="dafc7-118">Para obter detalhes sobre o suporte à topologia, consulte [topologias do Active Directory com suporte no Lync Server 2013](lync-server-2013-supported-active-directory-topologies.md) na documentação de suporte.</span><span class="sxs-lookup"><span data-stu-id="dafc7-118">For details about topology support, see [Supported Active Directory topologies in Lync Server 2013](lync-server-2013-supported-active-directory-topologies.md) in the Supportability documentation.</span></span>

<div>

## <a name="supported-domain-controller-operating-systems"></a><span data-ttu-id="dafc7-119">Sistemas operacionais do controlador de domínio com suporte</span><span class="sxs-lookup"><span data-stu-id="dafc7-119">Supported Domain Controller Operating Systems</span></span>

<span data-ttu-id="dafc7-120">O Lync Server 2013 oferece suporte a controladores de domínio que executam os seguintes sistemas operacionais:</span><span class="sxs-lookup"><span data-stu-id="dafc7-120">Lync Server 2013 supports domain controllers running the following operating systems:</span></span>

  - <span data-ttu-id="dafc7-121">Sistema operacional Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dafc7-121">Windows Server 2012 R2 operating system</span></span>

  - <span data-ttu-id="dafc7-122">Sistema operacional Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dafc7-122">Windows Server 2012 operating system</span></span>

  - <span data-ttu-id="dafc7-123">Sistema operacional Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dafc7-123">Windows Server 2008 R2 operating system</span></span>

  - <span data-ttu-id="dafc7-124">Sistema operacional Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dafc7-124">Windows Server 2008 operating system</span></span>

  - <span data-ttu-id="dafc7-125">Windows Server 2008 Enterprise 32-bit</span><span class="sxs-lookup"><span data-stu-id="dafc7-125">Windows Server 2008 Enterprise 32-Bit</span></span>

  - <span data-ttu-id="dafc7-126">As versões de 32 bits ou 64 bits do sistema operacional Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dafc7-126">The 32-bit or 64-bit versions of the Window Server 2003 R2 operating system</span></span>

  - <span data-ttu-id="dafc7-127">As versões de 32 bits ou 64 bits do sistema operacional Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dafc7-127">The 32-bit or 64-bit versions of the Windows Server 2003 operating system</span></span>

</div>

<div>

## <a name="forest-and-domain-functional-level"></a><span data-ttu-id="dafc7-128">Nível funcional da floresta e do domínio</span><span class="sxs-lookup"><span data-stu-id="dafc7-128">Forest and Domain Functional Level</span></span>

<span data-ttu-id="dafc7-129">Você deve disparar todos os domínios nos quais implanta o Lync Server 2013 em um nível funcional de domínio do Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 ou pelo menos Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dafc7-129">You must raise all domains in which you deploy Lync Server 2013 to a domain functional level of Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, or at least Windows Server 2003.</span></span>

<span data-ttu-id="dafc7-130">Todas as florestas nas quais você implanta o Lync Server 2013 devem ser elevadas para um nível funcional de floresta do Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 ou pelo menos Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dafc7-130">All forests in which you deploy Lync Server 2013 must be raised to a forest functional level of Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, or at least Windows Server 2003.</span></span>

</div>

<div>

## <a name="support-for-read-only-domain-controllers"></a><span data-ttu-id="dafc7-131">Suporte para controladores de domínio do Read-Only</span><span class="sxs-lookup"><span data-stu-id="dafc7-131">Support for Read-Only Domain Controllers</span></span>

<span data-ttu-id="dafc7-132">O Lync Server 2013 dá suporte a implantações de serviços de domínio Active Directory que incluem controladores de domínio somente leitura ou servidores de catálogo global somente leitura, desde que existam controladores de domínio graváveis disponíveis.</span><span class="sxs-lookup"><span data-stu-id="dafc7-132">Lync Server 2013 supports Active Directory Domain Services deployments that include read-only domain controllers or read-only global catalog servers, as long as there are writable domain controllers available.</span></span>

</div>

<div>

## <a name="domain-names"></a><span data-ttu-id="dafc7-133">Nomes de domínio</span><span class="sxs-lookup"><span data-stu-id="dafc7-133">Domain Names</span></span>

<span data-ttu-id="dafc7-134">O Lync Server não dá suporte a domínios com rótulo único.</span><span class="sxs-lookup"><span data-stu-id="dafc7-134">Lync Server does not support single-labeled domains.</span></span> <span data-ttu-id="dafc7-135">Por exemplo, uma floresta com um domínio raiz chamado **contoso. local** tem suporte, mas não há suporte para um domínio raiz chamado **local** .</span><span class="sxs-lookup"><span data-stu-id="dafc7-135">For example, a forest with a root domain named **contoso.local** is supported, but a root domain named **local** is not supported.</span></span> <span data-ttu-id="dafc7-136">Para obter detalhes, consulte o artigo 300684 da base de dados de conhecimento Microsoft, "informações sobre como configurar o Windows para domínios com nomes DNS de rótulo único" em [https://go.microsoft.com/fwlink/p/?linkId=143752](https://go.microsoft.com/fwlink/p/?linkid=143752) .</span><span class="sxs-lookup"><span data-stu-id="dafc7-136">For details, see Microsoft Knowledge Base article 300684, “Information about configuring Windows for domains with single-label DNS names,” at [https://go.microsoft.com/fwlink/p/?linkId=143752](https://go.microsoft.com/fwlink/p/?linkid=143752).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="dafc7-137">O Lync Server não permite a renomeação de domínios.</span><span class="sxs-lookup"><span data-stu-id="dafc7-137">Lync Server does not support renaming domains.</span></span> <span data-ttu-id="dafc7-138">Se você precisar renomear um domínio onde o Lync Server está implantado, primeiro você precisa desinstalar o Lync Server, depois renomear o domínio e depois reinstalar o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dafc7-138">If you need to rename a domain where Lync Server is deployed, you need to first uninstall Lync Server, then rename the domain, and then reinstall Lync Server.</span></span>



</div>

</div>

<div>

## <a name="locked-down-ad-ds-environments"></a><span data-ttu-id="dafc7-139">Ambientes AD DS bloqueados</span><span class="sxs-lookup"><span data-stu-id="dafc7-139">Locked Down AD DS Environments</span></span>

<span data-ttu-id="dafc7-140">Em um ambiente do AD DS bloqueado, usuários e objetos de computador geralmente são colocados em unidades organizacionais específicas (UOs) com herança de permissões desabilitada para ajudar a proteger a delegação administrativa e habilitar o uso de objetos de política de grupo (GPOs) para aplicar políticas de segurança.</span><span class="sxs-lookup"><span data-stu-id="dafc7-140">In a locked-down AD DS environment, Users and Computer objects are often placed in specific organizational units (OUs) with permissions inheritance disabled to help secure administrative delegation and to enable use of Group Policy objects (GPOs) to enforce security policies.</span></span> <span data-ttu-id="dafc7-141">O Lync Server 2013 pode ser implantado em um ambiente do Active Directory bloqueado.</span><span class="sxs-lookup"><span data-stu-id="dafc7-141">Lync Server 2013 can be deployed in a locked-down Active Directory environment.</span></span> <span data-ttu-id="dafc7-142">Para obter detalhes sobre o que é necessário para implantar o Lync Server em um ambiente bloqueado, consulte [preparando os serviços de domínio do Active Directory bloqueados no Lync Server 2013](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="dafc7-142">For details about what is required to deploy Lync Server in a locked-down environment, see [Preparing a locked-down Active Directory Domain Services in Lync Server 2013](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md) in the Deployment documentation.</span></span>

<span data-ttu-id="dafc7-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dafc7-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

