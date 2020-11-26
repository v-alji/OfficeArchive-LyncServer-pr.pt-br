---
title: 'Lync Server 2013: Configurando opções de arquivamento'
description: 'Lync Server 2013: Configurando opções de arquivamento.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Archiving options
ms:assetid: b2f7f74d-e1ad-494e-9d46-5eb0efe5fb29
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205182(v=OCS.15)
ms:contentKeyID: 48185158
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 99d57f016d76f9ae6a538ef28663a4b4c965b0a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433308"
---
# <a name="configuring-archiving-options-in-lync-server-2013"></a><span data-ttu-id="cc61d-103">Configurando opções de arquivamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cc61d-103">Configuring Archiving options in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cc61d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cc61d-104">

<span> </span></span></span>

<span data-ttu-id="cc61d-105">_**Tópico da última modificação:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="cc61d-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="cc61d-106">No painel de controle do Lync Server 2013, você usa configurações de arquivamento para especificar como o arquivamento é implementado.</span><span class="sxs-lookup"><span data-stu-id="cc61d-106">In Lync Server 2013 Control Panel, you use Archiving configurations to specify how archiving is implemented.</span></span> <span data-ttu-id="cc61d-107">Isso inclui as seguintes configurações de arquivamento:</span><span class="sxs-lookup"><span data-stu-id="cc61d-107">This includes the following Archiving configurations:</span></span>

  - <span data-ttu-id="cc61d-108">Uma configuração global criada por padrão quando você implanta o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cc61d-108">A global configuration that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="cc61d-109">Configurações opcionais de nível de site e de pool que você pode criar e usar para especificar como o arquivamento é implementado para sites ou pools específicos.</span><span class="sxs-lookup"><span data-stu-id="cc61d-109">Optional site-level and pool-level configurations that you can create and use to specify how archiving is implemented for specific sites or pools.</span></span>

<span data-ttu-id="cc61d-110">Inicialmente, você define o arquivamento de configurações ao implantar o arquivamento, mas pode alterar, adicionar e excluir configurações após a implantação.</span><span class="sxs-lookup"><span data-stu-id="cc61d-110">You initially set up Archiving configurations when you deploy Archiving, but you can change, add, and delete configurations after deployment.</span></span> <span data-ttu-id="cc61d-111">No painel de controle do Lync Server 2013, você pode usar a página de **configuração de arquivamento** do grupo **arquivamento e monitoramento** para gerenciar as configurações no nível global, no nível do site e no nível do pool.</span><span class="sxs-lookup"><span data-stu-id="cc61d-111">In Lync Server 2013 Control Panel, you can use the **Archiving Configuration** page of the **Archiving and Monitoring** group to manage configurations at the global level, site level, and pool level.</span></span> <span data-ttu-id="cc61d-112">Para obter detalhes sobre como as configurações de arquivamento são implementadas, incluindo quais opções você pode especificar e a hierarquia de configurações de arquivamento, consulte [como o arquivamento funciona no Lync Server 2013](lync-server-2013-how-archiving-works.md) na documentação de planejamento, documentação de implantação ou documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="cc61d-112">For details about how Archiving configurations are implemented, including which options you can specify and the hierarchy of Archiving configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span> <span data-ttu-id="cc61d-113">Para obter detalhes sobre como gerenciar as configurações após a implantação, consulte [Gerenciando opções de configuração de arquivamento no Lync Server 2013 para sua organização, sites e pools](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md) na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="cc61d-113">For details about how to manage configurations after deployment, see [Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md) in the Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="cc61d-114">Para usar o arquivamento, configure as políticas de arquivamento para especificar se o arquivamento de comunicações internas deve ser habilitado, para comunicações externas ou para os usuários hospedados no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cc61d-114">To use archiving, you must configure Archiving policies to specify whether to enable archiving for internal communications, for external communications, or for both for users homed on Lync Server 2013.</span></span> <span data-ttu-id="cc61d-115">Por padrão, o arquivamento não está habilitado para comunicações internas ou externas.</span><span class="sxs-lookup"><span data-stu-id="cc61d-115">By default, archiving is not enabled for either internal or external communications.</span></span> <span data-ttu-id="cc61d-116">Antes de habilitar o arquivamento em qualquer política, você deve especificar as configurações de arquivamento adequadas para a implantação e, opcionalmente, sites e pools específicos, conforme descrito nesta seção.</span><span class="sxs-lookup"><span data-stu-id="cc61d-116">Before enabling Archiving in any policies, you should specify the appropriate Archiving configurations for your deployment and, optionally, for specific sites and pools, as described in this section.</span></span> <span data-ttu-id="cc61d-117">Para obter detalhes sobre como habilitar o arquivamento, consulte <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">configurar e atribuir políticas de arquivamento no Lync Server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="cc61d-117">For details about enabling Archiving, see <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Configuring and assigning Archiving policies in Lync Server 2013</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="cc61d-118">Se você não usar a integração do Microsoft Exchange para todos os usuários em sua implantação, configure as políticas de arquivamento para especificar se o arquivamento deve ser habilitado para comunicações internas, para comunicações externas ou para ambos.</span><span class="sxs-lookup"><span data-stu-id="cc61d-118">If you do not use Microsoft Exchange integration for all users in your deployment, you must configure Archiving policies to specify whether to enable archiving for internal communications, for external communications, or for both.</span></span> <span data-ttu-id="cc61d-119">Por padrão, o arquivamento não está habilitado para comunicações internas ou externas para o arquivamento de dados ao usar bancos de dados de arquivamento do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cc61d-119">By default, archiving is not enabled for either internal or external communications for archiving of data when using Lync Server 2013 Archiving databases.</span></span> <span data-ttu-id="cc61d-120">Antes de habilitar o arquivamento em qualquer política, você deve especificar as configurações de arquivamento adequadas para sua implantação e, opcionalmente, para sites e pools específicos, conforme descrito nesta seção.</span><span class="sxs-lookup"><span data-stu-id="cc61d-120">Prior to enabling Archiving in any policies, you should specify the appropriate Archiving configurations for your deployment and, optionally, for specific sites and pools, as described in this section.</span></span> <span data-ttu-id="cc61d-121">Para obter detalhes sobre como habilitar o arquivamento para uso com bancos de dados de arquivamento do Lync Server 2013, Confira como <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">configurar e atribuir políticas de arquivamento no Lync server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="cc61d-121">For details about enabling Archiving for use with Lync Server 2013 Archiving databases, see <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Configuring and assigning Archiving policies in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="cc61d-122">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="cc61d-122">In This Section</span></span>

  - [<span data-ttu-id="cc61d-123">Configuração de opções de arquivamento no nível global do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cc61d-123">Configuring Archiving options at the global level in Lync Server 2013</span></span>](lync-server-2013-configuring-archiving-options-at-the-global-level.md)

  - [<span data-ttu-id="cc61d-124">Configurando opções de arquivamento para um site no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cc61d-124">Configuring Archiving options for a site in Lync Server 2013</span></span>](lync-server-2013-configuring-archiving-options-for-a-site.md)

  - [<span data-ttu-id="cc61d-125">Configurando opções de arquivamento para um pool no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cc61d-125">Configuring Archiving options for a pool in Lync Server 2013</span></span>](lync-server-2013-configuring-archiving-options-for-a-pool.md)

<span data-ttu-id="cc61d-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cc61d-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

