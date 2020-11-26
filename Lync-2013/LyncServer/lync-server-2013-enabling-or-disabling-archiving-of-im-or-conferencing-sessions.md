---
title: Habilitar ou desabilitar o arquivamento de sessões de mensagens instantâneas ou de conferência
description: Habilitar ou desabilitar o arquivamento de sessões de mensagens instantâneas ou de conferência.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling or disabling Archiving of IM or conferencing sessions
ms:assetid: aa4b5983-dbe1-4d64-8a18-fe2c33994e94
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182567(v=OCS.15)
ms:contentKeyID: 48185104
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9861024bbd4f4a1558287139a37559f782fcf008
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428780"
---
# <a name="enabling-or-disabling-archiving-of-im-or-conferencing-sessions-in-lync-server-2013"></a><span data-ttu-id="58177-103">Habilitar ou desabilitar o arquivamento de sessões de mensagens instantâneas ou de conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="58177-103">Enabling or disabling Archiving of IM or conferencing sessions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="58177-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="58177-104">

<span> </span></span></span>

<span data-ttu-id="58177-105">_**Tópico da última modificação:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="58177-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="58177-106">No painel de controle do Lync Server 2013, você usa configurações de arquivamento para habilitar e desabilitar o arquivamento de mensagens instantâneas, sessões de conferência ou ambas.</span><span class="sxs-lookup"><span data-stu-id="58177-106">In Lync Server 2013 Control Panel, you use Archiving configurations to enable and disable archiving of IM, conferencing sessions, or both.</span></span> <span data-ttu-id="58177-107">Isso inclui as seguintes configurações de arquivamento:</span><span class="sxs-lookup"><span data-stu-id="58177-107">This includes the following Archiving configurations:</span></span>

  - <span data-ttu-id="58177-108">Uma configuração global criada por padrão quando você implanta o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="58177-108">A global configuration that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="58177-109">Configurações opcionais de nível de site e de pool que você pode criar e usar para especificar como o arquivamento é implementado para sites ou pools específicos.</span><span class="sxs-lookup"><span data-stu-id="58177-109">Optional site-level and pool-level configurations that you can create and use to specify how archiving is implemented for specific sites or pools.</span></span>

<span data-ttu-id="58177-110">Inicialmente, você define o arquivamento de configurações ao implantar o arquivamento, mas pode alterar, adicionar e excluir configurações após a implantação.</span><span class="sxs-lookup"><span data-stu-id="58177-110">You initially set up Archiving configurations when you deploy Archiving, but you can change, add, and delete configurations after deployment.</span></span> <span data-ttu-id="58177-111">Para obter detalhes sobre como as configurações de arquivamento são implementadas, incluindo quais opções você pode especificar e a hierarquia de configurações de arquivamento, consulte [como o arquivamento funciona no Lync Server 2013](lync-server-2013-how-archiving-works.md) na documentação de planejamento, documentação de implantação ou documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="58177-111">For details about how Archiving configurations are implemented, including which options you can specify and the hierarchy of Archiving configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="58177-112">Para usar o arquivamento, configure as políticas de arquivamento para especificar se o arquivamento de comunicações internas deve ser habilitado, para comunicações externas ou para os usuários hospedados no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="58177-112">To use archiving, you must configure Archiving policies to specify whether to enable archiving for internal communications, for external communications, or for both for users homed on Lync Server 2013.</span></span> <span data-ttu-id="58177-113">Por padrão, o arquivamento não está habilitado para comunicações internas ou externas.</span><span class="sxs-lookup"><span data-stu-id="58177-113">By default, archiving is not enabled for either internal or external communications.</span></span> <span data-ttu-id="58177-114">Antes de habilitar o arquivamento em qualquer política, você deve especificar as configurações de arquivamento adequadas para a implantação e, opcionalmente, sites e pools específicos, conforme descrito nesta seção.</span><span class="sxs-lookup"><span data-stu-id="58177-114">Before enabling Archiving in any policies, you should specify the appropriate Archiving configurations for your deployment and, optionally, for specific sites and pools, as described in this section.</span></span> <span data-ttu-id="58177-115">Para obter detalhes sobre como habilitar o arquivamento, consulte <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">configurar e atribuir políticas de arquivamento no Lync Server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="58177-115">For details about enabling Archiving, see <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Configuring and assigning Archiving policies in Lync Server 2013</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="58177-116">Se você decidir após implantar o arquivamento em que deseja usar a integração do Microsoft Exchange para armazenar arquivos de arquivamento e arquivos nos servidores Exchange 2013 e todos os usuários estiverem hospedados em seus servidores Exchange 2013, você deve remover a configuração de banco de dados do SQL Server da sua topologia.</span><span class="sxs-lookup"><span data-stu-id="58177-116">If you decide after you deploy Archiving that you want to use Microsoft Exchange integration to store archiving data and files on Exchange 2013 servers and all your users are homed on your Exchange 2013 servers, you should remove the SQL Server database configuration from your topology.</span></span> <span data-ttu-id="58177-117">Você deve usar o construtor de topologias para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="58177-117">You must use Topology Builder to do this.</span></span> <span data-ttu-id="58177-118">Para obter detalhes, consulte <A href="lync-server-2013-changing-archiving-database-options.md">alterando as opções de arquivamento de banco de dados no Lync Server 2013</A> na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="58177-118">For details, see <A href="lync-server-2013-changing-archiving-database-options.md">Changing Archiving database options in Lync Server 2013</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="to-enable-or-disable-archiving-of-im-or-conferencing-sessions"></a><span data-ttu-id="58177-119">Para habilitar ou desabilitar o arquivamento de sessões de mensagens instantâneas ou de conferência</span><span class="sxs-lookup"><span data-stu-id="58177-119">To enable or disable archiving of IM or conferencing sessions</span></span>

1.  <span data-ttu-id="58177-120">Usando uma conta de usuário atribuída à função CsArchivingAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="58177-120">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="58177-121">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="58177-121">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="58177-122">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="58177-122">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="58177-123">Na barra de navegação da esquerda, clique em **Monitoramento e Arquivamento**, e depois, clique em **Configuração de Arquivamento**.</span><span class="sxs-lookup"><span data-stu-id="58177-123">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="58177-124">Selecione a configuração global, local ou de pool apropriada na lista de configurações de arquivamento, clique em **Editar**, **Exibir detalhes** e execute o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="58177-124">Select the appropriate global, site, or pool configuration from the list of archiving configurations, click **Edit**, click **Show details**, and then do the following:</span></span>
    
      - <span data-ttu-id="58177-125">Para habilitar o arquivamento apenas para sessões de mensagens instantâneas (IM), clique em **Arquivar sessões de IM**.</span><span class="sxs-lookup"><span data-stu-id="58177-125">To enable archiving only for instant messaging (IM) sessions, click **Archive IM sessions**.</span></span>
    
      - <span data-ttu-id="58177-126">Para habilitar o arquivamento para as sessões de IM e conferências, clique em **Arquivar sessões de IM e conferências**.</span><span class="sxs-lookup"><span data-stu-id="58177-126">To enable archiving for both IM sessions and conferences, click **Archive IM and conferencing sessions**.</span></span>
    
      - <span data-ttu-id="58177-127">Para desabilitar o arquivamento da política, clique em **Desabilitar arquivamento**.</span><span class="sxs-lookup"><span data-stu-id="58177-127">To disable archiving for the policy, click **Disable archiving**.</span></span>

5.  <span data-ttu-id="58177-128">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="58177-128">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="58177-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="58177-129">See Also</span></span>


[<span data-ttu-id="58177-130">Gerenciando opções de configuração de arquivamento no Lync Server 2013 para sua organização, sites e pools</span><span class="sxs-lookup"><span data-stu-id="58177-130">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</span></span>](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md)  
[<span data-ttu-id="58177-131">Configurar e atribuir políticas de arquivamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="58177-131">Configuring and assigning Archiving policies in Lync Server 2013</span></span>](lync-server-2013-configuring-and-assigning-archiving-policies.md)  
  

<span data-ttu-id="58177-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="58177-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

