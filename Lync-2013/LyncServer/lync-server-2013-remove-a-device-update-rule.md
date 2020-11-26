---
title: 'Lync Server 2013: remover uma regra de atualização de dispositivo'
description: 'Lync Server 2013: remover uma regra de atualização de dispositivo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove a Device Update rule
ms:assetid: ad6e0c6a-cda4-4147-92d5-48bc393ac456
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994066(v=OCS.15)
ms:contentKeyID: 51803977
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f0ed7436331377200a5b8719cf32a8195179402
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436493"
---
# <a name="remove-a-device-update-rule-in-lync-server-2013"></a><span data-ttu-id="02201-103">Remover uma regra de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="02201-103">Remove a Device Update rule in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="02201-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="02201-104">

<span> </span></span></span>

<span data-ttu-id="02201-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="02201-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="02201-106">Remover uma regra de atualização de dispositivo a retira permanentemente da fila de atualização de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="02201-106">Removing a device update rule takes it permanently out of the device update queue.</span></span>

<span data-ttu-id="02201-107">Remover uma regra é diferente de desinstalar uma atualização dos dispositivos na sua implantação ou dos seus dispositivos de teste.</span><span class="sxs-lookup"><span data-stu-id="02201-107">Removing a rule is different from uninstalling an update from the devices in your deployment or from your test devices.</span></span> <span data-ttu-id="02201-108">Para desinstalar uma atualização aprovada da sua implantação, *restaure* a regra de atualização de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="02201-108">To uninstall an approved update from your deployment, you *restore* the device update rule.</span></span> <span data-ttu-id="02201-109">Para obter detalhes, consulte [restaurar uma regra de atualização de dispositivo no Lync Server 2013](lync-server-2013-restore-a-device-update-rule.md).</span><span class="sxs-lookup"><span data-stu-id="02201-109">For details, see [Restore a Device Update rule in Lync Server 2013](lync-server-2013-restore-a-device-update-rule.md).</span></span> <span data-ttu-id="02201-110">Para desinstalar uma atualização que você não aprovou dos seus dispositivos de teste, você a *redefiniu* .</span><span class="sxs-lookup"><span data-stu-id="02201-110">To uninstall an update you haven’t approved from your test devices, you *reset* it.</span></span> <span data-ttu-id="02201-111">Para obter detalhes, consulte [redefinir uma regra de atualização de dispositivo no Lync Server 2013](lync-server-2013-reset-a-device-update-rule.md).</span><span class="sxs-lookup"><span data-stu-id="02201-111">For details, see [Reset a Device Update rule in Lync Server 2013](lync-server-2013-reset-a-device-update-rule.md).</span></span>

<span data-ttu-id="02201-112">Você pode remover uma regra de atualização de dispositivo usando o painel de controle do Lync Server ou o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="02201-112">You can remove a device update rule by using either Lync Server Control Panel or Windows PowerShell.</span></span>

<div>

## <a name="to-remove-device-update-rules-by-using-lync-server-control-panel"></a><span data-ttu-id="02201-113">Para remover regras de atualização de dispositivo usando o painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="02201-113">To remove device update rules by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="02201-114">Usando uma conta de usuário atribuída à função CsUserAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="02201-114">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="02201-115">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="02201-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="02201-116">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="02201-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="02201-117">Na barra de navegação à esquerda, clique em **clientes** e, em seguida, clique no botão de navegação de **atualização do dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="02201-117">In the left navigation bar, click **Clients**, and then click the **Device Update** navigation button.</span></span>

4.  <span data-ttu-id="02201-118">Na página **atualização do dispositivo** , siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="02201-118">On the **Device Update** page, do one of the following:</span></span>
    
      - <span data-ttu-id="02201-119">Para remover uma regra, selecione a regra que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="02201-119">To remove one rule, select the rule you want to delete.</span></span>
    
      - <span data-ttu-id="02201-120">Para remover todas as regras, clique no menu **Editar** e, em seguida, clique em **selecionar tudo**.</span><span class="sxs-lookup"><span data-stu-id="02201-120">To remove all rules, click the **Edit** menu, and then click **Select All**.</span></span>

5.  <span data-ttu-id="02201-121">Clique em **Editar** e então em **Excluir**.</span><span class="sxs-lookup"><span data-stu-id="02201-121">Click **Edit**, and then click **Delete**.</span></span>

</div>

<div>

## <a name="removing-device-update-rules-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="02201-122">Remover regras de atualização de dispositivo usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="02201-122">Removing Device Update Rules by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="02201-123">As regras de atualização de dispositivo também podem ser removidas usando o Windows PowerShell e o cmdlet **Remove-CsDeviceUpdateRule** .</span><span class="sxs-lookup"><span data-stu-id="02201-123">Device update rules can also be removed by using Windows PowerShell and the **Remove-CsDeviceUpdateRule** cmdlet.</span></span> <span data-ttu-id="02201-124">Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="02201-124">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="02201-125">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="02201-125">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-single-device-update-rule-from-a-server"></a><span data-ttu-id="02201-126">Para remover uma regra de atualização de dispositivo único de um servidor</span><span class="sxs-lookup"><span data-stu-id="02201-126">To remove a single device update rule from a server</span></span>

  - <span data-ttu-id="02201-127">O comando a seguir remove a regra de atualização de dispositivo d5ce3c10-2588-420A-82ac-dc2d9b1222ff9 do servidor Web em atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="02201-127">The following command removes the device update rule d5ce3c10-2588-420a-82ac-dc2d9b1222ff9 from the Web server on atl-cs-001.litwareinc.com.</span></span>
    
        Remove-CsDeviceUpdateRule -Identity "service:WebServer:atl-cs-001.litwareinc.com/d5ce3c10-2588-420a-82ac-dc2d9b1222ff9"

</div>

<div>

## <a name="to-remove-all-the-device-update-rules-from-a-server"></a><span data-ttu-id="02201-128">Para remover todas as regras de atualização de dispositivo de um servidor</span><span class="sxs-lookup"><span data-stu-id="02201-128">To remove all the device update rules from a server</span></span>

  - <span data-ttu-id="02201-129">Esse comando Remove todas as regras de atualização de dispositivo do servidor Web no atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="02201-129">This command removes all the device update rules from the web server on atl-cs-001.litwareinc.com.</span></span>
    
        Get-CsDeviceUpdateRule -Filter "service:WebServer:atl-cs-001.litwareinc.com*" | Remove-CsDeviceUpdateRule

</div>

<span data-ttu-id="02201-130">Para obter detalhes, consulte o tópico da ajuda para o cmdlet [Remove-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Remove-CsDeviceUpdateRule) .</span><span class="sxs-lookup"><span data-stu-id="02201-130">For details, see the Help topic for the [Remove-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Remove-CsDeviceUpdateRule) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="02201-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="02201-131">See Also</span></span>


[<span data-ttu-id="02201-132">Aprovar uma regra de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="02201-132">Approve a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-approve-a-device-update-rule.md)  
  

<span data-ttu-id="02201-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="02201-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

