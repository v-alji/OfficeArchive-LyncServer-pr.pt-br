---
title: 'Lync Server 2013: Delegando o controle administrativo do Lync Server'
description: 'Lync Server 2013: delegando o controle administrativo do Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegating administrative control of Lync Server 2013
ms:assetid: 0f378eff-8ef4-4c60-9fd2-67d7ee259ef8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520951(v=OCS.15)
ms:contentKeyID: 48183418
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8d3710af2d194a5aa4ebdd7291be2ee58176507
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430760"
---
# <a name="delegating-administrative-control-of-lync-server-2013"></a><span data-ttu-id="79180-103">Delegando o controle administrativo do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="79180-103">Delegating administrative control of Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="79180-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="79180-104">

<span> </span></span></span>

<span data-ttu-id="79180-105">_**Tópico da última modificação:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="79180-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="79180-106">No Lync Server 2013, as tarefas administrativas são delegadas a usuários usando o novo recurso de controle de acesso baseado em função (RBAC).</span><span class="sxs-lookup"><span data-stu-id="79180-106">In Lync Server 2013, administrative tasks are delegated to users by using the new role-based access control (RBAC) feature.</span></span> <span data-ttu-id="79180-107">Quando você instala o Lync Server, várias funções RBAC são criadas para você.</span><span class="sxs-lookup"><span data-stu-id="79180-107">When you install Lync Server, a number of RBAC roles are created for you.</span></span> <span data-ttu-id="79180-108">Essas funções correspondem a grupos de segurança universais nos Serviços de Domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="79180-108">These roles correspond to universal security groups in Active Directory Domain Services.</span></span> <span data-ttu-id="79180-109">Por exemplo, a função RBAC CsHelpDesk corresponde ao grupo CsHelpDesk localizado no contêiner usuários nos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="79180-109">For example, the RBAC role CsHelpDesk corresponds to the CsHelpDesk group found in the Users container in Active Directory Domain Services.</span></span> <span data-ttu-id="79180-110">Além disso, cada função RBAC é associada a um conjunto de cmdlets do Windows PowerShell do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="79180-110">In addition, each RBAC role is associated with a set of Lync Server Windows PowerShell cmdlets.</span></span> <span data-ttu-id="79180-111">Esses cmdlets representam as tarefas que podem ser realizadas pelos usuários que receberam a função RBAC fornecida.</span><span class="sxs-lookup"><span data-stu-id="79180-111">These cmdlets represent the tasks that can be carried out by users who have been assigned the given RBAC role.</span></span> <span data-ttu-id="79180-112">Por exemplo, a função CsHelpDesk foi atribuída aos cmdlets Lock-CsClientPin e UnlockCsClientPin.</span><span class="sxs-lookup"><span data-stu-id="79180-112">For example, the CsHelpDesk role has been assigned the Lock-CsClientPin and UnlockCsClientPin cmdlets.</span></span> <span data-ttu-id="79180-113">Isso significa que os usuários que receberam a função CsHelpDesk podem bloquear e desbloquear números de PIN do usuário.</span><span class="sxs-lookup"><span data-stu-id="79180-113">That means users who have been assigned the CsHelpDesk role can lock and unlock user PIN numbers.</span></span> <span data-ttu-id="79180-114">No entanto, a função CsHelpDesk não foi atribuída ao cmdlet New-CsVoicePolicy.</span><span class="sxs-lookup"><span data-stu-id="79180-114">However, the CsHelpDesk role has not been assigned the New-CsVoicePolicy cmdlet.</span></span> <span data-ttu-id="79180-115">Isso significa que os usuários que receberam a função CsHelpDesk não poderão criar novas políticas de voz.</span><span class="sxs-lookup"><span data-stu-id="79180-115">That means that users who have been assigned the CsHelpDesk role cannot create new voice policies.</span></span>

<div>

## <a name="viewing-information-about-rbac-roles"></a><span data-ttu-id="79180-116">Exibir informações sobre as funções RBAC</span><span class="sxs-lookup"><span data-stu-id="79180-116">Viewing Information about RBAC Roles</span></span>

<span data-ttu-id="79180-117">Você pode recuperar informações básicas sobre as funções RBAC executando o seguinte comando no Shell de gerenciamento do Lync Server:</span><span class="sxs-lookup"><span data-stu-id="79180-117">You can retrieve basic information about your RBAC roles by running the following command from within the Lync Server Management Shell:</span></span>

    Get-CsAdminRole

<span data-ttu-id="79180-118">Lembre-se de que a identidade da função RBAC (por exemplo, CsVoiceAdministrator) tem um mapeamento direto para um grupo de segurança localizado no contêiner usuários nos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="79180-118">Keep in mind that the Identity of the RBAC role (for example, CsVoiceAdministrator) has a direct mapping to a security group found in the Users container in Active Directory Domain Services.</span></span>

<span data-ttu-id="79180-119">Para exibir uma lista dos cmdlets que foram atribuídos a uma função, use um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="79180-119">To view a list of the cmdlets that have been assigned to a role, use a command similar to this:</span></span>

    Get-CsAdminRole -Identity "CsHelpDesk" | Select-Object -ExpandProperty Cmdlets

</div>

<div>

## <a name="assigning-an-rbac-role-to-a-user"></a><span data-ttu-id="79180-120">Atribuindo uma função RBAC a um usuário</span><span class="sxs-lookup"><span data-stu-id="79180-120">Assigning an RBAC Role to a User</span></span>

<span data-ttu-id="79180-121">Para atribuir uma função RBAC a um usuário, você deve adicionar esse usuário ao grupo de segurança apropriado do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="79180-121">To assign an RBAC role to a user, you must add that user to the appropriate Active Directory security group.</span></span> <span data-ttu-id="79180-122">Por exemplo, para atribuir a função CsLocationAdministrator a um usuário, você deve adicionar esse usuário ao grupo CsLocationAdministrator.</span><span class="sxs-lookup"><span data-stu-id="79180-122">For example, to assign the CsLocationAdministrator role to a user, you must add that user to the CsLocationAdministrator group.</span></span> <span data-ttu-id="79180-123">Isso pode ser feito executando o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="79180-123">That can be done by carrying out the following procedure:</span></span>

<span data-ttu-id="79180-124">**Para atribuir um usuário a um grupo de segurança**</span><span class="sxs-lookup"><span data-stu-id="79180-124">**To assign a user to a security group**</span></span>

1.  <span data-ttu-id="79180-125">Usando uma conta que tenha permissão para modificar a associação de um grupo do Active Directory, faça logon em um computador onde usuários e computadores do Active Directory tenham sido instalados.</span><span class="sxs-lookup"><span data-stu-id="79180-125">Using an account that has permission to modify the membership of an Active Directory group, log on to a computer where Active Directory Users and Computers has been installed.</span></span>

2.  <span data-ttu-id="79180-126">Clique em **Iniciar**, em **todos os programas**, em **Ferramentas administrativas** e em **usuários e computadores do Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="79180-126">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

3.  <span data-ttu-id="79180-127">Em usuários e computadores do Active Directory, expanda o nome do seu domínio e clique no contêiner **usuários** .</span><span class="sxs-lookup"><span data-stu-id="79180-127">In Active Directory Users and Computers, expand the name of your domain and click the **Users** container.</span></span>

4.  <span data-ttu-id="79180-128">Clique com o botão direito do mouse no grupo de segurança **CsLocationAdministrator** e, em seguida, clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="79180-128">Right-click the security group **CsLocationAdministrator**, and then click **Properties**.</span></span>

5.  <span data-ttu-id="79180-129">Na caixa de diálogo **Propriedades** , na guia **Membros** , clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="79180-129">In the **Properties** dialog box, on the **Members** tab, click **Add**.</span></span>

6.  <span data-ttu-id="79180-130">Na caixa de diálogo **Selecionar usuários, computadores, contatos ou grupos** , digite o nome de usuário ou o nome para exibição do usuário a ser adicionado ao grupo (por exemplo, **Ken Myer**) na caixa **digite os nomes de objeto a serem selecionados** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="79180-130">In the **Select Users, Computers, Contacts, or Groups** dialog box, type the user name or display name of the user to be added to the group (for example, **Ken Myer**) in the **Enter the object names to select** box and then click **OK**.</span></span>

7.  <span data-ttu-id="79180-131">Na caixa de diálogo **Propriedades** , clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="79180-131">In the **Properties** dialog box, click **OK**.</span></span>

<span data-ttu-id="79180-132">Para verificar se a função RBAC foi atribuída, use o cmdlet [Get-CsAdminRoleAssignment](https://docs.microsoft.com/powershell/module/skype/Get-CsAdminRoleAssignment) , passando o cmdlet do sAMAccountName (nome de logon do Active Directory) do usuário.</span><span class="sxs-lookup"><span data-stu-id="79180-132">To verify that the RBAC role has been assigned, use the [Get-CsAdminRoleAssignment](https://docs.microsoft.com/powershell/module/skype/Get-CsAdminRoleAssignment) cmdlet, passing the cmdlet the SamAccountName (Active Directory logon name) of the user.</span></span> <span data-ttu-id="79180-133">Por exemplo, execute este comando dentro do Shell de gerenciamento do Lync Server:</span><span class="sxs-lookup"><span data-stu-id="79180-133">For example, run this command from within the Lync Server Management Shell:</span></span>

    Get-CsAdminRoleAssignment  -Identity "kenmyer"

<span data-ttu-id="79180-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="79180-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

