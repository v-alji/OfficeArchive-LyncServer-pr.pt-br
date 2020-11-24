---
title: 'Lync Server 2013: exibindo informações do perfil da política de largura de banda de rede'
description: 'Lync Server 2013: exibindo informações do perfil da política de largura de banda de rede.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network bandwidth policy profile information
ms:assetid: eed453fc-04e9-4971-959c-6fad54bf1c96
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721931(v=OCS.15)
ms:contentKeyID: 49733866
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c72a3533ae6f49f91db91b2c3b515c0b5153ec27
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390033"
---
# <a name="viewing-network-bandwidth-policy-profile-information-in-lync-server-2013"></a><span data-ttu-id="bf0a9-103">Exibir informações de perfil da política de largura de banda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf0a9-103">Viewing network bandwidth policy profile information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bf0a9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bf0a9-104">

<span> </span></span></span>

<span data-ttu-id="bf0a9-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="bf0a9-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="bf0a9-106">Como parte do controle de admissão de chamadas (CAC), uma política de largura de banda é usada para definir limitações de largura de banda para determinadas modalidades.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-106">As part of call admission control (CAC), a bandwidth policy is used to define bandwidth limitations for certain modalities.</span></span> <span data-ttu-id="bf0a9-107">No Microsoft Lync Server 2013, somente as modalidades de áudio e vídeo podem ter limitações de largura de banda atribuídas.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-107">In Microsoft Lync Server 2013, only audio and video modalities can be assigned bandwidth limitations.</span></span> <span data-ttu-id="bf0a9-108">Você pode definir limitações gerais de largura de banda e limitações de sessão.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-108">You can set overall bandwidth limitations and session limitations.</span></span> <span data-ttu-id="bf0a9-109">Você pode usar o painel de controle do Lync Server para criar, modificar ou excluir um perfil de contêiner para essas políticas.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-109">You can use the Lync Server Control Panel to create, modify, or delete a container profile for these policies.</span></span> <span data-ttu-id="bf0a9-110">Cada perfil de política de largura de banda pode ser associado a um ou mais sites de rede.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-110">Each bandwidth policy profile can be associated with one or more network sites.</span></span> <span data-ttu-id="bf0a9-111">Use os procedimentos a seguir para exibir um perfil de política de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-111">Use the following procedures to view a bandwidth policy profile.</span></span> <span data-ttu-id="bf0a9-112">Para criar ou modificar um perfil de política de largura de banda, consulte [criando ou modificando perfis de política de largura de banda no Lync Server 2013](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="bf0a9-112">To create or modify a bandwidth policy profile, see [Creating or modifying bandwidth policy profiles in Lync Server 2013](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md).</span></span>

<div>

## <a name="to-view-a-bandwidth-policy-profile"></a><span data-ttu-id="bf0a9-113">Para exibir um perfil de política de largura de banda</span><span class="sxs-lookup"><span data-stu-id="bf0a9-113">To view a bandwidth policy profile</span></span>

1.  <span data-ttu-id="bf0a9-114">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="bf0a9-115">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="bf0a9-116">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="bf0a9-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="bf0a9-117">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, em política de **largura de banda**.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-117">In the left navigation bar, click **Network Configuration** and then click **Bandwidth Policy**.</span></span>

4.  <span data-ttu-id="bf0a9-118">Na página **política de largura de banda** , clique no perfil de política de largura de banda que você deseja exibir.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-118">On the **Bandwidth Policy** page, click the bandwidth policy profile that you want to view.</span></span>

5.  <span data-ttu-id="bf0a9-119">No menu **Editar**, clique em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-119">On the **Edit** menu, click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-network-bandwidth-policy-profile-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="bf0a9-120">Exibindo informações do perfil da política de largura de banda de rede usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bf0a9-120">Viewing Network Bandwidth Policy Profile Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="bf0a9-121">Os perfis de largura de banda de rede podem ser exibidos usando o Windows PowerShell e o cmdlet Get-CsNetworkBandwidthPolicyProfile.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-121">Network bandwidth profiles can be viewed by using Windows PowerShell and the Get-CsNetworkBandwidthPolicyProfile cmdlet.</span></span> <span data-ttu-id="bf0a9-122">Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bf0a9-122">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="bf0a9-123">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="bf0a9-123">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-bandwidth-policy-profile-information"></a><span data-ttu-id="bf0a9-124">Para ver as informações do perfil da política de largura de banda de rede</span><span class="sxs-lookup"><span data-stu-id="bf0a9-124">To view network bandwidth policy profile information</span></span>

  - <span data-ttu-id="bf0a9-125">Para exibir informações sobre todos os perfis da política de largura de banda de rede, digite o seguinte comando no Shell de gerenciamento do Lync Server e pressione ENTER:</span><span class="sxs-lookup"><span data-stu-id="bf0a9-125">To view information about all your network bandwidth policy profiles, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkBandwidthPolicyProfile
    
    <span data-ttu-id="bf0a9-126">Isso retornará informações parecidas com:</span><span class="sxs-lookup"><span data-stu-id="bf0a9-126">That will return information similar to this:</span></span>
    
        Identity          : RedmondBandwidthPolicy
        BWPolicy          : {BWLimit=200;BWSessionLimit=200;
                            BWPolicyModality=Audio, 
                            BWLimit=1400;BWSessionLimit=500;
                            BWPolicyModality=Video}
        BWPolicyProfileID : RedmondBandwidthPolicy
        Description       :

</div>

<span data-ttu-id="bf0a9-127">Para obter mais informações, consulte o tópico da ajuda para o cmdlet [Get-CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile) .</span><span class="sxs-lookup"><span data-stu-id="bf0a9-127">For more information, see the help topic for the [Get-CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bf0a9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf0a9-128">See Also</span></span>


[<span data-ttu-id="bf0a9-129">Criando ou modificando perfis de política de largura de banda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf0a9-129">Creating or modifying bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md)  
[<span data-ttu-id="bf0a9-130">Excluindo perfis de política de largura de banda de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf0a9-130">Deleting network bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-deleting-network-bandwidth-policy-profiles.md)  


[<span data-ttu-id="bf0a9-131">Configurar o controle de admissão de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf0a9-131">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)  
  

<span data-ttu-id="bf0a9-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bf0a9-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

