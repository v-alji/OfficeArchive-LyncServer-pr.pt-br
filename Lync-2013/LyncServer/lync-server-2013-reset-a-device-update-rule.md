---
title: 'Lync Server 2013: redefinir uma regra de atualização de dispositivo'
description: 'Lync Server 2013: redefinir uma regra de atualização de dispositivo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reset a Device Update rule
ms:assetid: d1f597e7-dffd-4756-af07-10613a5d8729
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994069(v=OCS.15)
ms:contentKeyID: 51803980
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8a4d42b6aee8f4cb3fd93839b4a8575059ba71cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436367"
---
# <a name="reset-a-device-update-rule-in-lync-server-2013"></a><span data-ttu-id="c37d1-103">Redefinir uma regra de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c37d1-103">Reset a Device Update rule in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c37d1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c37d1-104">

<span> </span></span></span>

<span data-ttu-id="c37d1-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="c37d1-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="c37d1-106">Se você não gostar da maneira como uma atualização funciona em seus dispositivos de teste, você pode redefinir a regra de atualização de dispositivo, que remove o status pendente da regra e desinstala a atualização dos dispositivos de teste.</span><span class="sxs-lookup"><span data-stu-id="c37d1-106">If you don’t like the way that an update works on your test devices, you can reset the device update rule, which removes the rule’s pending status and uninstalls the update from the test devices.</span></span>

<span data-ttu-id="c37d1-107">Você pode remover uma regra de atualização de dispositivo usando o painel de controle do Lync Server ou o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c37d1-107">You can remove a device update rule by using either Lync Server Control Panel or Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c37d1-108">Para desinstalar uma regra que você já aprovou (isto é, distribuída), restaure-a.</span><span class="sxs-lookup"><span data-stu-id="c37d1-108">To uninstall a rule that you’ve already approved (that is, rolled out), restore it.</span></span> <span data-ttu-id="c37d1-109">Para obter detalhes, consulte <A href="lync-server-2013-restore-a-device-update-rule.md">restaurar uma regra de atualização de dispositivo no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="c37d1-109">For details, see <A href="lync-server-2013-restore-a-device-update-rule.md">Restore a Device Update rule in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-reset-a-device-update-rule-by-using-lync-server-control-panel"></a><span data-ttu-id="c37d1-110">Para redefinir uma regra de atualização de dispositivo usando o painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="c37d1-110">To reset a device update rule by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="c37d1-111">Usando uma conta de usuário atribuída à função CsUserAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="c37d1-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="c37d1-112">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c37d1-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="c37d1-113">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="c37d1-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="c37d1-114">Na barra de navegação à esquerda, clique em **clientes** e, em seguida, clique no botão de navegação de **atualização do dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="c37d1-114">In the left navigation bar, click **Clients**, and then click the **Device Update** navigation button.</span></span>

4.  <span data-ttu-id="c37d1-115">Na página **atualização do dispositivo** , siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="c37d1-115">On the **Device Update** page, do one of the following:</span></span>
    
      - <span data-ttu-id="c37d1-116">Para redefinir uma regra, selecione a regra que você deseja redefinir.</span><span class="sxs-lookup"><span data-stu-id="c37d1-116">To reset one rule, select the rule you want to reset.</span></span>
    
      - <span data-ttu-id="c37d1-117">Para redefinir todas as regras, no menu **Editar** , clique em **selecionar tudo**.</span><span class="sxs-lookup"><span data-stu-id="c37d1-117">To reset all rules, on the **Edit** menu, click **Select All**.</span></span>
    
      - <span data-ttu-id="c37d1-118">Para redefinir todas as regras para uma marca, use o menu coluna **da marca** .</span><span class="sxs-lookup"><span data-stu-id="c37d1-118">To reset all rules for one brand, use the **Brand** column menu.</span></span>

5.  <span data-ttu-id="c37d1-119">Clique em **ação** e, em seguida, clique em **cancelar atualizações pendentes**.</span><span class="sxs-lookup"><span data-stu-id="c37d1-119">Click **Action**, and then click **Cancel pending updates**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="c37d1-120">Se tiver certeza de que nunca vai querer implementar as regras de atualização de dispositivo que você cancelou, talvez você queira excluí-las.</span><span class="sxs-lookup"><span data-stu-id="c37d1-120">If you’re sure you’ll never want to roll out the device update rule(s) that you cancelled, you might want to delete them.</span></span> <span data-ttu-id="c37d1-121">Para obter detalhes, consulte <A href="lync-server-2013-remove-a-device-update-rule.md">remover uma regra de atualização de dispositivo no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="c37d1-121">For details, see <A href="lync-server-2013-remove-a-device-update-rule.md">Remove a Device Update rule in Lync Server 2013</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="resetting-a-device-update-rule-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="c37d1-122">Redefinir uma regra de atualização de dispositivo usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c37d1-122">Resetting a Device Update Rule by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="c37d1-123">As regras de atualização de dispositivo também podem ser redefinidas usando o Windows PowerShell e o cmdlet **Reset-CsDeviceUpdateRule** .</span><span class="sxs-lookup"><span data-stu-id="c37d1-123">Device update rules can also be reset by using Windows PowerShell and the **Reset-CsDeviceUpdateRule** cmdlet.</span></span> <span data-ttu-id="c37d1-124">Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c37d1-124">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c37d1-125">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="c37d1-125">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>

## <a name="to-reset-a-specific-device-update-rule-on-a-server"></a><span data-ttu-id="c37d1-126">Para redefinir uma regra de atualização de dispositivo específica em um servidor</span><span class="sxs-lookup"><span data-stu-id="c37d1-126">To reset a specific device update rule on a server</span></span>

  - <span data-ttu-id="c37d1-127">O comando a seguir redefine a regra de atualização do dispositivo d5ce3c10-2588-420A-82ac-dc2d9b1222ff9 no servidor Web atl-cs-001.litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="c37d1-127">The following command resets the device update rule d5ce3c10-2588-420a-82ac-dc2d9b1222ff9 on the Web server atl-cs-001.litwareinc.com:</span></span>
    
        Reset-CsDeviceUpdateRule -Identity "service:WebServer:atl-cs-001.litwareinc.com/d5ce3c10-2588-420a-82ac-dc2d9b1222ff9"

</div>

<div>

## <a name="to-reset-all-the-device-update-rules-on-a-server"></a><span data-ttu-id="c37d1-128">Para redefinir todas as regras de atualização de dispositivo em um servidor</span><span class="sxs-lookup"><span data-stu-id="c37d1-128">To reset all the device update rules on a server</span></span>

  - <span data-ttu-id="c37d1-129">Esse comando redefine todas as regras de atualização de dispositivo no servidor Web atl-cs-001.litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="c37d1-129">This command resets all the device update rules on the Web server atl-cs-001.litwareinc.com:</span></span>
    
        Get-CsDeviceUpdateRule -Filter "service:WebServer:atl-cs-001.litwareinc.com*"  | Reset-CsDeviceUpdateRule

</div>

<div>

## <a name="to-reset-all-the-device-updates-rules-that-have-a-specific-brand"></a><span data-ttu-id="c37d1-130">Para redefinir todas as regras de atualizações de dispositivo que têm uma marca específica</span><span class="sxs-lookup"><span data-stu-id="c37d1-130">To reset all the device updates rules that have a specific brand</span></span>

  - <span data-ttu-id="c37d1-131">Neste exemplo, todas as atualizações de dispositivos em toda a organização com uma marca igual à Microsoft são redefinidas:</span><span class="sxs-lookup"><span data-stu-id="c37d1-131">In this example, all the device updates throughout the organization that have a Brand equal to Microsoft are reset:</span></span>
    
        Get-CsDeviceUpdateRule | Where-Object {$_.Brand -eq "Microsoft"} | Reset-CsDeviceUpdateRule

</div>

<span data-ttu-id="c37d1-132">Para obter detalhes, consulte o tópico da ajuda para o cmdlet [Reset-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Reset-CsDeviceUpdateRule) .</span><span class="sxs-lookup"><span data-stu-id="c37d1-132">For details, see the Help topic for the [Reset-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Reset-CsDeviceUpdateRule) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c37d1-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="c37d1-133">See Also</span></span>


[<span data-ttu-id="c37d1-134">Aprovar uma regra de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c37d1-134">Approve a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-approve-a-device-update-rule.md)  
  

<span data-ttu-id="c37d1-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c37d1-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

