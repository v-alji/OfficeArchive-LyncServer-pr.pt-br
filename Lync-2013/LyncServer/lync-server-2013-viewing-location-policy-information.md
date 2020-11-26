---
title: 'Lync Server 2013: exibindo informações de política de localização'
description: 'Lync Server 2013: exibindo informações de política de localização.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing location policy information
ms:assetid: 14e41bcb-ea0a-49c2-99b3-1f61fc34416d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520954(v=OCS.15)
ms:contentKeyID: 48183489
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2fecc5de5fb71014a1641038e9e09afba0e90cdb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443955"
---
# <a name="viewing-location-policy-information-in-lync-server-2013"></a><span data-ttu-id="0f14c-103">Exibindo informações de política de localização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0f14c-103">Viewing location policy information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0f14c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0f14c-104">

<span> </span></span></span>

<span data-ttu-id="0f14c-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="0f14c-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="0f14c-106">No Lync Server 2013, você pode usar a política de localização para aplicar configurações relacionadas à funcionalidade Enhanced 9-1-1 (E9-1-1) e às configurações de localização para usuários ou contatos.</span><span class="sxs-lookup"><span data-stu-id="0f14c-106">In Lync Server 2013, you can use the location policy to apply settings that relate to Enhanced 9-1-1 (E9-1-1) functionality and to location settings for users or contacts.</span></span> <span data-ttu-id="0f14c-107">A política de localização determina se um usuário está habilitado para E9-1-1 e, em caso afirmativo, qual é o comportamento de uma chamada de emergência.</span><span class="sxs-lookup"><span data-stu-id="0f14c-107">The location policy determines whether a user is enabled for E9-1-1, and if so what the behavior is of an emergency call.</span></span> <span data-ttu-id="0f14c-108">Por exemplo, você pode usar a política de localização para definir qual número constitui uma chamada de emergência (por exemplo, 911 nos Estados Unidos), se a segurança corporativa deve ser notificada automaticamente e como a chamada deve ser roteada.</span><span class="sxs-lookup"><span data-stu-id="0f14c-108">For example, you can use the location policy to define what number constitutes an emergency call (for example, 911 in the United States), whether corporate security should be automatically notified, and how the call should be routed.</span></span>

<span data-ttu-id="0f14c-109">Você pode configurar as políticas de localização do grupo de **configuração de rede** no painel de controle do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0f14c-109">You can configure location policies from the **Network Configuration** group in Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="0f14c-110">No painel de controle do Lync Server, você pode exibir, criar, modificar ou excluir políticas de localização.</span><span class="sxs-lookup"><span data-stu-id="0f14c-110">From Lync Server Control Panel you can view, create, modify, or delete location policies.</span></span> <span data-ttu-id="0f14c-111">Use o procedimento a seguir para exibir informações sobre as políticas de localização.</span><span class="sxs-lookup"><span data-stu-id="0f14c-111">Use the following procedure to view information about location policies.</span></span> <span data-ttu-id="0f14c-112">Para obter detalhes sobre como criar ou modificar as políticas de localização, consulte [criando ou modificando uma política de localização no Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md).</span><span class="sxs-lookup"><span data-stu-id="0f14c-112">For details on creating or modifying location policies, see [Creating or modifying a location policy in Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md).</span></span>

<div>

## <a name="to-view-information-about-a-location-policy"></a><span data-ttu-id="0f14c-113">Para exibir informações sobre uma política de localização</span><span class="sxs-lookup"><span data-stu-id="0f14c-113">To view information about a location policy</span></span>

1.  <span data-ttu-id="0f14c-114">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="0f14c-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="0f14c-115">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0f14c-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="0f14c-116">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0f14c-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="0f14c-117">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **política de localização**.</span><span class="sxs-lookup"><span data-stu-id="0f14c-117">In the left navigation bar, click **Network Configuration** and then click **Location Policy**.</span></span>

4.  <span data-ttu-id="0f14c-118">Na página **política de localização** , selecione a política de localização que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="0f14c-118">On the **Location Policy** page, select the location policy that you want to modify.</span></span>

5.  <span data-ttu-id="0f14c-119">No menu **Editar**, clique em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="0f14c-119">On the **Edit** menu, click **Show details**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0f14c-120">Você só pode exibir informações sobre uma política de localização de cada vez.</span><span class="sxs-lookup"><span data-stu-id="0f14c-120">You can only view information about one location policy at a time.</span></span>

    
    </div>

<span data-ttu-id="0f14c-121">Uma única política, chamada global, existe por padrão e não pode ser excluída ou renomeada.</span><span class="sxs-lookup"><span data-stu-id="0f14c-121">A single policy, called Global, exists by default and cannot be deleted or renamed.</span></span> <span data-ttu-id="0f14c-122">No entanto, você pode modificar a política global.</span><span class="sxs-lookup"><span data-stu-id="0f14c-122">However, you can modify the Global policy.</span></span> <span data-ttu-id="0f14c-123">Esta política será aplicada a todos os usuários e contatos, a menos que você crie políticas de site ou políticas por usuário.</span><span class="sxs-lookup"><span data-stu-id="0f14c-123">This policy will apply to all users and contacts, unless you create site policies or per-user policies.</span></span> <span data-ttu-id="0f14c-124">Políticas por usuário devem ser aplicadas a usuários específicos.</span><span class="sxs-lookup"><span data-stu-id="0f14c-124">Per-user policies must be applied to specific users.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0f14c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f14c-125">See Also</span></span>


[<span data-ttu-id="0f14c-126">Criando ou modificando uma política de localização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0f14c-126">Creating or modifying a location policy in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-a-location-policy.md)  
[<span data-ttu-id="0f14c-127">Criar políticas de localização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0f14c-127">Create location policies in Lync Server 2013</span></span>](lync-server-2013-create-location-policies.md)  
[<span data-ttu-id="0f14c-128">Criar ou modificar um site da rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0f14c-128">Create or modify a network site in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-site.md)  


[<span data-ttu-id="0f14c-129">New-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="0f14c-129">New-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsLocationPolicy)  
[<span data-ttu-id="0f14c-130">Set-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="0f14c-130">Set-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsLocationPolicy)  
[<span data-ttu-id="0f14c-131">Remove-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="0f14c-131">Remove-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsLocationPolicy)  
[<span data-ttu-id="0f14c-132">Get-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="0f14c-132">Get-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsLocationPolicy)  
  

<span data-ttu-id="0f14c-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0f14c-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

