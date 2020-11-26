---
title: 'Lync Server 2013: atribuir uma política de plano de discagem por usuário'
description: 'Lync Server 2013: atribuir uma política de plano de discagem por usuário.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user dial plan policy
ms:assetid: 9fea861f-7770-4cae-9b1f-2a960595bfc9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688156(v=OCS.15)
ms:contentKeyID: 49733760
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 654c1f15ccb1efa4d1aa35d957df7a2654fa41d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443199"
---
# <a name="assign-a-per-user-dial-plan-policy-in-lync-server-2013"></a><span data-ttu-id="d8757-103">Atribuir uma política de plano de discagem por usuário no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8757-103">Assign a per-user dial plan policy in Lync Server 2013</span></span>

 


<span data-ttu-id="d8757-104">Para concluir a configuração da conta de usuário para usuários do Enterprise Voice ou usuários de conferências discadas, o usuário deve receber um plano de discagem.</span><span class="sxs-lookup"><span data-stu-id="d8757-104">To complete user account configuration for either users of Enterprise Voice or users of dial-in conferencing, the user must be assigned a dial plan.</span></span> <span data-ttu-id="d8757-105">As contas de usuário usarão automaticamente o plano de discagem global ou, se houver, o plano de discagem em nível de site quando você não atribui explicitamente um plano de discagem por usuário existente.</span><span class="sxs-lookup"><span data-stu-id="d8757-105">User accounts will automatically use the global dial plan or, if one exists, the site-level dial plan when you do not explicitly assign an existing per-user dial plan.</span></span> <span data-ttu-id="d8757-106">Se quiser usar o plano global ou de discagem de site para todos os usuários habilitados para o Enterprise Voice, você pode ignorar esta seção.</span><span class="sxs-lookup"><span data-stu-id="d8757-106">If you want to use the global or site dial plan for all users that are enabled for Enterprise Voice, you can skip this section.</span></span>

## <a name="to-assign-a-dial-plan-by-using-the-lync-server-2013-control-panel"></a><span data-ttu-id="d8757-107">Para atribuir um plano de discagem usando o painel de controle do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8757-107">To assign a dial plan by using the Lync Server 2013 Control Panel</span></span>

1.  <span data-ttu-id="d8757-108">Usando uma conta de usuário atribuída à função CsUserAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="d8757-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d8757-109">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d8757-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d8757-110">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d8757-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d8757-111">Na barra de navegação esquerda, clique em **Usuários**.</span><span class="sxs-lookup"><span data-stu-id="d8757-111">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="d8757-112">Na caixa **Pesquisar usuários**, digite todo ou parte do nome de exibição, nome, sobrenome, nome da conta SAM, endereço SIP ou URI de linha da conta do usuário que deseja habilitar e clique em **Localizar**.</span><span class="sxs-lookup"><span data-stu-id="d8757-112">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want to enable, and then click **Find**.</span></span>

5.  <span data-ttu-id="d8757-113">Na tabela, clique na conta de usuário para a qual você deseja atribuir um plano de discagem.</span><span class="sxs-lookup"><span data-stu-id="d8757-113">In the table, click the user account that you want to assign a dial plan.</span></span>

6.  <span data-ttu-id="d8757-114">No menu **Editar**, clique em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="d8757-114">On the **Edit** menu, click **Show details**.</span></span>

7.  <span data-ttu-id="d8757-115">Na página **Editar usuário do Lync Server** , em **telefonia**, clique em **Enterprise Voice**.</span><span class="sxs-lookup"><span data-stu-id="d8757-115">On the **Edit Lync Server User** page, under **Telephony**, click **Enterprise Voice**.</span></span>

8.  <span data-ttu-id="d8757-116">Clique em **política de plano de discagem** e escolha o plano de discagem desejado.</span><span class="sxs-lookup"><span data-stu-id="d8757-116">Click **Dial plan policy**, and then choose the desired dial plan.</span></span>

9.  <span data-ttu-id="d8757-117">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="d8757-117">Click **Commit**.</span></span>

<span data-ttu-id="d8757-118">Para obter detalhes sobre como configurar planos de discagem, consulte o tópico [Configurando planos de discagem no Lync Server 2013](lync-server-2013-configuring-dial-plans.md) .</span><span class="sxs-lookup"><span data-stu-id="d8757-118">For details about configuring dial plans, see the [Configuring dial plans in Lync Server 2013](lync-server-2013-configuring-dial-plans.md) topic.</span></span>

## <a name="assign-a-per-user-dial-plan-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="d8757-119">Atribuir um plano de discagem Per-User usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d8757-119">Assign a Per-User Dial Plan by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="d8757-120">Você pode atribuir planos de discagem por usuário com o Windows PowerShell e o cmdlet **Grant-CsdialPlan** .</span><span class="sxs-lookup"><span data-stu-id="d8757-120">You can assign per-user dial plans with Windows PowerShell and the **Grant-CsdialPlan** cmdlet.</span></span> <span data-ttu-id="d8757-121">Você pode executar esse cmdlet a partir do Shell de gerenciamento do Lync Server 2013 ou de uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d8757-121">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="d8757-122">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="d8757-122">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

## <a name="to-assign-a-per-user-dial-plan-to-a-single-user"></a><span data-ttu-id="d8757-123">Atribuir um plano de discagem por usuário a um único usuário</span><span class="sxs-lookup"><span data-stu-id="d8757-123">To assign a per-user dial plan to a single user</span></span>

  - <span data-ttu-id="d8757-124">O comando a seguir atribui o plano de discagem por usuário RedmondDialPlan ao usuário Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="d8757-124">The following command assigns the per-user dial plan RedmondDialPlan to the user Ken Myer.</span></span>
    
        Grant-CsDialPlan -Identity "Ken Myer" -PolicyName "RedmondDialPlan"

## <a name="to-assign-a-per-user-dial-plan-to-multiple-users"></a><span data-ttu-id="d8757-125">Atribuir um plano de discagem por usuário a vários usuários</span><span class="sxs-lookup"><span data-stu-id="d8757-125">To assign a per-user dial plan to multiple users</span></span>

  - <span data-ttu-id="d8757-126">Esse comando atribui o plano de discagem por usuário RedmondDialPlan a todos os usuários que trabalham na cidade de Redmond.</span><span class="sxs-lookup"><span data-stu-id="d8757-126">This command assigns the per-user dial plan RedmondDialPlan to all the users who work in the city of Redmond.</span></span> <span data-ttu-id="d8757-127">Para obter mais informações sobre o parâmetro LdapFilter usado neste comando, consulte a documentação do cmdlet [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="d8757-127">For more information on the LdapFilter parameter used in this command, see the documentation for the [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) cmdlet.</span></span>
    
        Get-CsUser -LdapFilter "l=Redmond" | Grant-CsDialPlan -PolicyName "RedmondDialPlan"

## <a name="to-unassign-a-per-user-dial-plan"></a><span data-ttu-id="d8757-128">Retirar a atribuição de uma plano de discagem por usuário</span><span class="sxs-lookup"><span data-stu-id="d8757-128">To unassign a per-user dial plan</span></span>

  - <span data-ttu-id="d8757-129">O comando a seguir cancelará a atribuição de um plano de discagem por usuário anteriormente atribuído a Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="d8757-129">The following command unassigns any per-user dial plan previously assigned to Ken Myer.</span></span> <span data-ttu-id="d8757-130">Após a atribuição do plano de discagem por usuário, Ken Myer será automaticamente gerenciado usando o plano de discagem global, seu plano de discagem de site local (se houver) ou o plano de discagem de escopo de serviço atribuído ao registrador ou ao gateway PSTN.</span><span class="sxs-lookup"><span data-stu-id="d8757-130">After the per-user dial plan is unassigned, Ken Myer will automatically be managed by using the global dial plan, his local site dial plan (if one exists), or the service-scope dial plan assigned to his Registrar or PSTN gateway.</span></span> <span data-ttu-id="d8757-131">Um plano de discagem de escopo de serviço tem precedência sobre qualquer plano de discagem de site e um plano de discagem de site tem prioridade sobre o plano de discagem global.</span><span class="sxs-lookup"><span data-stu-id="d8757-131">A service scope dial plan takes precedence over any site dial plan, and a site dial plan takes precedence over the global dial plan.</span></span>
    
        Grant-CsDialPlan -Identity "Ken Myer" -PolicyName $Null

<span data-ttu-id="d8757-132">Para obter mais informações, consulte o tópico da ajuda para o cmdlet [Grant-CsDialPlan](https://technet.microsoft.com/library/gg398547\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="d8757-132">For more information, see the help topic for the [Grant-CsDialPlan](https://technet.microsoft.com/library/gg398547\(v=ocs.15\)) cmdlet.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8757-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8757-133">See Also</span></span>


[<span data-ttu-id="d8757-134">Configurando planos de discagem no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8757-134">Configuring dial plans in Lync Server 2013</span></span>](lync-server-2013-configuring-dial-plans.md)  
[<span data-ttu-id="d8757-135">Contas de usuário habilitadas para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8757-135">User accounts enabled for Lync Server 2013</span></span>](lync-server-2013-user-accounts-enabled-for-lync-server.md)

