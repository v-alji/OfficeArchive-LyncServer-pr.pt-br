---
title: 'Lync Server 2013: Configurando a política global para arquivamento'
description: 'Lync Server 2013: Configurando a política global para arquivamento.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the global policy for Archiving
ms:assetid: 58341d6b-c3ff-4dd9-b1c7-0048f33861ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204906(v=OCS.15)
ms:contentKeyID: 48184192
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8f8125f458c4269626e0b1c929f2acb1a8de0b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432566"
---
# <a name="configuring-the-global-policy-for-archiving-in-lync-server-2013"></a><span data-ttu-id="fa171-103">Configurando a política global para arquivamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa171-103">Configuring the global policy for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fa171-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fa171-104">

<span> </span></span></span>

<span data-ttu-id="fa171-105">_**Tópico da última modificação:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="fa171-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="fa171-106">Quando você implanta seus servidores front-end, o Lync Server cria uma política global para arquivar.</span><span class="sxs-lookup"><span data-stu-id="fa171-106">When you deploy your Front End Servers, Lync Server creates a global policy for Archiving.</span></span> <span data-ttu-id="fa171-107">Por padrão, o arquivamento está desabilitado na política global.</span><span class="sxs-lookup"><span data-stu-id="fa171-107">By default, Archiving is disabled in the global policy.</span></span> <span data-ttu-id="fa171-108">A política global controla se o arquivamento está habilitado para comunicações internas e externas para toda a sua implantação, a menos que você configure políticas de site ou de usuário, que substituem a política global ou se você usa a integração do Microsoft Exchange para alguns ou todos os seus usuários.</span><span class="sxs-lookup"><span data-stu-id="fa171-108">The global policy controls whether archiving is enabled for internal and external communications for your entire deployment, unless you set up site or user policies, which override the global policy, or if you use Microsoft Exchange integration for some or all of your users.</span></span> <span data-ttu-id="fa171-109">Se você usar a integração com o Microsoft Exchange, a política global não se aplicará a nenhum usuário que estiver hospedado no Exchange 2013 e ter as caixas de correio colocadas em In-Place isenção.</span><span class="sxs-lookup"><span data-stu-id="fa171-109">If you use Microsoft Exchange integration, the global policy does not apply to any users who are homed on Exchange 2013 and have the mailboxes put on In-Place Hold.</span></span>

<span data-ttu-id="fa171-110">Para obter detalhes sobre como as políticas de arquivamento funcionam, incluindo a hierarquia para políticas globais, de site e de usuário, consulte [como o arquivamento funciona na documentação de planejamento do Lync Server 2013](lync-server-2013-how-archiving-works.md) , documentação de implantação ou documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="fa171-110">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fa171-111">Se você habilitar a integração do Microsoft Exchange para a implantação, as políticas de retenção do Exchange In-Place controlam se o arquivamento está habilitado para os usuários hospedados no Exchange 2013 e se as caixas de correio são colocadas In-Place isenção.</span><span class="sxs-lookup"><span data-stu-id="fa171-111">If you enable Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="fa171-112">Para obter detalhes, consulte <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Configurando políticas para arquivamento no Lync server 2013 ao usar a integração com o Exchange Server</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="fa171-112">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="fa171-113">Você deve especificar todas as opções adequadas nas configurações de arquivamento antes de habilitar o arquivamento.</span><span class="sxs-lookup"><span data-stu-id="fa171-113">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="fa171-114">Para obter detalhes, consulte <A href="lync-server-2013-configuring-archiving-options.md">Configurando opções de arquivamento no Lync Server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="fa171-114">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-configure-the-global-policy-for-archiving-when-using-lync-server-archiving-databases"></a><span data-ttu-id="fa171-115">Para configurar a política global para arquivamento ao usar bancos de dados de arquivamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="fa171-115">To configure the global policy for archiving when using Lync Server Archiving databases</span></span>

1.  <span data-ttu-id="fa171-116">Usando uma conta de usuário atribuída à função CsArchivingAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="fa171-116">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fa171-117">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fa171-117">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="fa171-118">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server 2013, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="fa171-118">For details about the different methods you can use to start Lync Server 2013 Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="fa171-119">Na barra de navegação da esquerda, clique em **Monitoramento e Arquivamento**, e depois, clique em **Política de Arquivamento**.</span><span class="sxs-lookup"><span data-stu-id="fa171-119">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="fa171-120">Na página **Política de Arquivamento**, clique em **Global**, clique em **Editar** e, em seguida, clique em **Mostrar detalhes**.</span><span class="sxs-lookup"><span data-stu-id="fa171-120">On the **Archiving Policy** page, click **Global**, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="fa171-121">Em **Editar Política de Arquivamento - Global**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fa171-121">In **Edit Archiving Policy - Global**, do the following:</span></span>
    
      - <span data-ttu-id="fa171-122">Em **Nome**, se não desejar usar o nome padrão da opção Global, especifique um novo nome para a política global.</span><span class="sxs-lookup"><span data-stu-id="fa171-122">In **Name**, if you do not want to use the default name of Global, specify a new name for the global policy.</span></span>
    
      - <span data-ttu-id="fa171-123">Em **Descrição**, forneça informações sobre o que a política é (por exemplo, a Política global para *divisionName*).</span><span class="sxs-lookup"><span data-stu-id="fa171-123">In **Description**, provide information about what the policy is (for example, Global policy for *divisionName*).</span></span>
    
      - <span data-ttu-id="fa171-124">Para controlar o arquivamento de comunicações internas para todos os locais e usuários que não estivem sendo controlados especificamente por meio de uma política de local ou de usuário, marque ou desmarque a caixa de seleção **Arquivar comunicações internas**.</span><span class="sxs-lookup"><span data-stu-id="fa171-124">To control archiving of internal communications for all sites and users not specifically controlled through a site policy or user policy, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="fa171-125">Para controlar o arquivamento de comunicações externas para todos os locais e usuários que não estivem sendo controlados especificamente por meio de uma política de local ou de usuário, marque ou desmarque a caixa de seleção **Arquivar comunicações externas**.</span><span class="sxs-lookup"><span data-stu-id="fa171-125">To control archiving of external communications for all sites and users not specifically controlled through a site policy or user policy, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="fa171-126">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="fa171-126">Click **Commit**.</span></span>

<span data-ttu-id="fa171-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fa171-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

