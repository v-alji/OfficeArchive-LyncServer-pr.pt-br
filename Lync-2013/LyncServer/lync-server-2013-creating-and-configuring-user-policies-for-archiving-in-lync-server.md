---
title: Criando e Configurando políticas de usuário para arquivamento no Lync Server
description: Criar e configurar políticas de usuário para arquivamento no Lync Server.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating and configuring user policies for Archiving in Lync Server
ms:assetid: 5af0e605-3563-4d6f-a3c6-511d204a3165
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204923(v=OCS.15)
ms:contentKeyID: 48184234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6dad260910f01e10c71dbbde67af98ea9a207e33
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431537"
---
# <a name="creating-and-configuring-user-policies-for-archiving-in-lync-server-2013"></a><span data-ttu-id="db26a-103">Criando e Configurando políticas de usuário para arquivamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db26a-103">Creating and configuring user policies for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="db26a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="db26a-104">

<span> </span></span></span>

<span data-ttu-id="db26a-105">_**Tópico da última modificação:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="db26a-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="db26a-106">Para habilitar ou desabilitar o arquivamento de usuários específicos hospedados no Lync Server, primeiro você deve criar uma política de usuário e, em seguida, aplicar a política a um ou mais usuários ou grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="db26a-106">To enable or disable Archiving for specific users homed on Lync Server, you must first create a user policy and then apply the policy to one or more users or user groups.</span></span> <span data-ttu-id="db26a-107">Para obter detalhes sobre como aplicar políticas de usuário a usuários específicos e grupos de usuários, consulte [aplicando uma política de arquivamento do Lync Server a um usuário no Lync Server 2013](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="db26a-107">For details about applying user policies to specific users and user groups, see [Applying a Lync Server Archiving policy to a user in Lync Server 2013](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) in the Deployment documentation.</span></span>

<span data-ttu-id="db26a-108">Para obter detalhes sobre como as políticas de arquivamento funcionam, incluindo a hierarquia para políticas globais, de site e de usuário, consulte [como o arquivamento funciona no Lync Server 2013](lync-server-2013-how-archiving-works.md) na documentação de planejamento, na documentação de implantação ou na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="db26a-108">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, in the Deployment documentation, or in the Operations documentation.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="db26a-109">Se você ativou a integração do Microsoft Exchange para a implantação, as políticas de retenção do Exchange In-Place controlam se o arquivamento está habilitado para os usuários hospedados no Exchange 2013 e se as caixas de correio são colocadas In-Place isenção.</span><span class="sxs-lookup"><span data-stu-id="db26a-109">If you enabled Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="db26a-110">Para obter detalhes, consulte <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Configurando políticas para arquivamento no Lync server 2013 ao usar a integração com o Exchange Server</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="db26a-110">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="db26a-111">Você deve especificar todas as opções adequadas nas configurações de arquivamento antes de habilitar o arquivamento.</span><span class="sxs-lookup"><span data-stu-id="db26a-111">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="db26a-112">Para obter detalhes, consulte <A href="lync-server-2013-configuring-archiving-options.md">Configurando opções de arquivamento no Lync Server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="db26a-112">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-configure-an-archiving-policy-for-users-homed-on-lync-server"></a><span data-ttu-id="db26a-113">Para configurar uma política de arquivamento para usuários hospedados no Lync Server</span><span class="sxs-lookup"><span data-stu-id="db26a-113">To configure an archiving policy for users homed on Lync Server</span></span>

1.  <span data-ttu-id="db26a-114">Usando uma conta de usuário atribuída à função CsArchivingAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="db26a-114">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="db26a-115">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="db26a-115">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="db26a-116">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server 2013, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="db26a-116">For details about the different methods that you can use to start Lync Server 2013 Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="db26a-117">Na barra de navegação da esquerda, clique em **Monitoramento e Arquivamento**, e depois, clique em **Política de Arquivamento**.</span><span class="sxs-lookup"><span data-stu-id="db26a-117">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="db26a-118">Clique em **Nova** e em **Política do usuário**.</span><span class="sxs-lookup"><span data-stu-id="db26a-118">Click **New**, and then click **User policy**.</span></span>

5.  <span data-ttu-id="db26a-119">Em **Nova Política de Arquivamento**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="db26a-119">In **New Archiving Policy**, do the following:</span></span>
    
      - <span data-ttu-id="db26a-120">Em **Nome**, especifique o nome da política de usuário.</span><span class="sxs-lookup"><span data-stu-id="db26a-120">In **Name**, specify the name for the user policy.</span></span>
    
      - <span data-ttu-id="db26a-121">Em **Descrição**, forneça informações sobre a política de usuário (por exemplo, política de usuário do departamento jurídico).</span><span class="sxs-lookup"><span data-stu-id="db26a-121">In **Description**, provide information about what the user policy is (for example, user policy for legal department).</span></span>
    
      - <span data-ttu-id="db26a-122">Para controlar o arquivamento das comunicações internas para a política de usuário, marque ou desmarque a caixa de seleção **Arquivar comunicações internas**.</span><span class="sxs-lookup"><span data-stu-id="db26a-122">To control archiving of internal communications for the user policy, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="db26a-123">Para controlar o arquivamento das comunicações externas para a política de usuário, marque ou desmarque a caixa de seleção **Arquivar comunicações externas**.</span><span class="sxs-lookup"><span data-stu-id="db26a-123">To control archiving of external communications for the user policy, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="db26a-124">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="db26a-124">Click **Commit**.</span></span>

<span data-ttu-id="db26a-125">Uma política de usuário aplica-se somente aos usuários aos quais você a atribui.</span><span class="sxs-lookup"><span data-stu-id="db26a-125">A user policy applies only to users to whom you assign the policy.</span></span> <span data-ttu-id="db26a-126">Para obter detalhes sobre como aplicar uma política de usuário a usuários específicos, consulte [aplicando uma política de arquivamento do Lync Server a um usuário no Lync Server 2013](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="db26a-126">For details about applying a user policy to specific users, see [Applying a Lync Server Archiving policy to a user in Lync Server 2013](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) in the Deployment documentation.</span></span>

<span data-ttu-id="db26a-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="db26a-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

