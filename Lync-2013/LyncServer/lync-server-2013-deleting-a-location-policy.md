---
title: 'Lync Server 2013: excluindo uma política de localização'
description: 'Lync Server 2013: excluindo uma política de localização.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting a location policy
ms:assetid: 8ca9ba10-f45f-435a-b39c-519d251e9085
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688125(v=OCS.15)
ms:contentKeyID: 49733724
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 88935c00a60de377c9812a4d119708fd610338ab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430417"
---
# <a name="deleting-a-location-policy-in-lync-server-2013"></a><span data-ttu-id="b2084-103">Excluindo uma política de localização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b2084-103">Deleting a location policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b2084-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b2084-104">

<span> </span></span></span>

<span data-ttu-id="b2084-105">_**Tópico da última modificação:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="b2084-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="b2084-106">No Lync Server 2013, você pode usar a política de localização para aplicar configurações relacionadas à funcionalidade Enhanced 9-1-1 (E9-1-1) e às configurações de localização para usuários ou contatos.</span><span class="sxs-lookup"><span data-stu-id="b2084-106">In Lync Server 2013, you can use the location policy to apply settings that relate to Enhanced 9-1-1 (E9-1-1) functionality and to location settings for users or contacts.</span></span> <span data-ttu-id="b2084-107">A política de localização determina se um usuário está habilitado para E9-1-1 e, em caso afirmativo, qual é o comportamento de uma chamada de emergência.</span><span class="sxs-lookup"><span data-stu-id="b2084-107">The location policy determines whether a user is enabled for E9-1-1, and if so what the behavior is of an emergency call.</span></span> <span data-ttu-id="b2084-108">Por exemplo, você pode usar a política de localização para definir qual número constitui uma chamada de emergência (por exemplo, 911 nos Estados Unidos), se a segurança corporativa deve ser notificada automaticamente e como a chamada deve ser roteada.</span><span class="sxs-lookup"><span data-stu-id="b2084-108">For example, you can use the location policy to define what number constitutes an emergency call (for example, 911 in the United States), whether corporate security should be automatically notified, and how the call should be routed.</span></span>

<span data-ttu-id="b2084-109">Você pode configurar as políticas de localização do grupo de **configuração de rede** no painel de controle do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b2084-109">You can configure location policies from the **Network Configuration** group in Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="b2084-110">No painel de controle do Lync Server, você pode exibir, criar, modificar ou excluir políticas de localização.</span><span class="sxs-lookup"><span data-stu-id="b2084-110">From Lync Server Control Panel you can view, create, modify, or delete location policies.</span></span> <span data-ttu-id="b2084-111">Use os procedimentos a seguir para excluir uma política de localização.</span><span class="sxs-lookup"><span data-stu-id="b2084-111">Use the following procedures delete a location policy.</span></span> <span data-ttu-id="b2084-112">Para obter detalhes sobre como criar ou modificar as políticas de localização, consulte [criando ou modificando uma política de localização no Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md).</span><span class="sxs-lookup"><span data-stu-id="b2084-112">For details on creating or modifying location policies, see [Creating or modifying a location policy in Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md).</span></span>

<div>

## <a name="to-delete-a-location-policy"></a><span data-ttu-id="b2084-113">Para excluir uma política de localização</span><span class="sxs-lookup"><span data-stu-id="b2084-113">To delete a location policy</span></span>

1.  <span data-ttu-id="b2084-114">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="b2084-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="b2084-115">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b2084-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="b2084-116">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b2084-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="b2084-117">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **política de localização**.</span><span class="sxs-lookup"><span data-stu-id="b2084-117">In the left navigation bar, click **Network Configuration** and then click **Location Policy**.</span></span>

4.  <span data-ttu-id="b2084-118">Na página **política de localização** , selecione a política de localização que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="b2084-118">On the **Location Policy** page, select the location policy that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b2084-119">Você pode excluir mais de uma política de localização de cada vez.</span><span class="sxs-lookup"><span data-stu-id="b2084-119">You can delete more than one location policy at a time.</span></span> <span data-ttu-id="b2084-120">Para fazer isso, pressione CTRL e selecione várias políticas enquanto mantém a tecla CTRL pressionada.</span><span class="sxs-lookup"><span data-stu-id="b2084-120">To do this, press CTRL and select multiple policies while holding down the CTRL key.</span></span> <span data-ttu-id="b2084-121">Ou, para selecionar todas as políticas, clique em <STRONG>selecionar tudo</STRONG> no menu <STRONG>Editar</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="b2084-121">Or, to select all policies, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="b2084-122">No menu **Editar** , clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="b2084-122">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="b2084-123">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2084-123">Click **OK**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b2084-124">Não é possível excluir a política de localização global.</span><span class="sxs-lookup"><span data-stu-id="b2084-124">You cannot delete the Global location policy.</span></span> <span data-ttu-id="b2084-125">Se você tentar excluir a política global, receberá uma mensagem de aviso e essa política será redefinida para seus valores padrão.</span><span class="sxs-lookup"><span data-stu-id="b2084-125">If you attempt to delete the Global policy you will receive a warning message and that policy will be reset to its default values.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b2084-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2084-126">See Also</span></span>


[<span data-ttu-id="b2084-127">Criando ou modificando uma política de localização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b2084-127">Creating or modifying a location policy in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-a-location-policy.md)  
[<span data-ttu-id="b2084-128">Exibindo informações de política de localização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b2084-128">Viewing location policy information in Lync Server 2013</span></span>](lync-server-2013-viewing-location-policy-information.md)  
  

<span data-ttu-id="b2084-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b2084-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

