---
title: 'Lync Server 2013: aprovar uma regra de atualização de dispositivo'
description: 'Lync Server 2013: aprovar uma regra de atualização de dispositivo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Approve a Device Update rule
ms:assetid: 9dbb1c9a-be0f-4e13-9234-05501ab43ac5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994053(v=OCS.15)
ms:contentKeyID: 51803964
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 127d16dad6329e952b9033db07ac2f4a4fe9112c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440560"
---
# <a name="approve-a-device-update-rule-in-lync-server-2013"></a><span data-ttu-id="b735d-103">Aprovar uma regra de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b735d-103">Approve a Device Update rule in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b735d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b735d-104">

<span> </span></span></span>

<span data-ttu-id="b735d-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="b735d-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="b735d-106">Depois de importar uma regra de atualização de dispositivo, ela é instalada em seus dispositivos de teste.</span><span class="sxs-lookup"><span data-stu-id="b735d-106">After you import a device update rule, it’s installed on your test devices.</span></span> <span data-ttu-id="b735d-107">Se o teste for bem-sucedido e você quiser implantar a atualização em sua organização, aprove-a usando o painel de controle do Lync Server ou o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b735d-107">If your testing is successful, and you want to roll out the update to your organization, approve it by using either Lync Server Control Panel or Windows PowerShell.</span></span>

<div>

## <a name="to-approve-a-device-update-rule-by-using-lync-server-control-panel"></a><span data-ttu-id="b735d-108">Para aprovar uma regra de atualização de dispositivo usando o painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="b735d-108">To approve a device update rule by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="b735d-109">Usando uma conta de usuário atribuída à função CsUserAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="b735d-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="b735d-110">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b735d-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="b735d-111">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b735d-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="b735d-112">Na página **atualização do dispositivo** , siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="b735d-112">On the **Device Update** page, do one of the following:</span></span>
    
      - <span data-ttu-id="b735d-113">Para aprovar uma regra, selecione essa regra.</span><span class="sxs-lookup"><span data-stu-id="b735d-113">To approve one rule, select that rule.</span></span>
    
      - <span data-ttu-id="b735d-114">Para aprovar todas as regras, clique em **Editar** e, em seguida, clique em **selecionar tudo**.</span><span class="sxs-lookup"><span data-stu-id="b735d-114">To approve all rules, click **Edit**, and then click **Select All**.</span></span>

4.  <span data-ttu-id="b735d-115">Clique em **ação** e, em seguida, clique em **aprovar**.</span><span class="sxs-lookup"><span data-stu-id="b735d-115">Click **Action**, and then click **Approve**.</span></span>

</div>

<div>

## <a name="approving-a-device-update-rule-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="b735d-116">Aprovando uma regra de atualização de dispositivo usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b735d-116">Approving a Device Update Rule by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="b735d-117">As regras de atualização de dispositivo também podem ser aprovadas usando o Windows PowerShell e o cmdlet **Approve-CsDeviceUpdateRule** .</span><span class="sxs-lookup"><span data-stu-id="b735d-117">Device update rules can also be approved by using Windows PowerShell and the **Approve-CsDeviceUpdateRule** cmdlet.</span></span> <span data-ttu-id="b735d-118">Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b735d-118">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b735d-119">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="b735d-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>

## <a name="to-approve-a-single-device-update-rule"></a><span data-ttu-id="b735d-120">Para aprovar uma única regra de atualização de dispositivo</span><span class="sxs-lookup"><span data-stu-id="b735d-120">To approve a single device update rule</span></span>

  - <span data-ttu-id="b735d-121">O comando a seguir aprova a regra de atualização de dispositivo d5ce3c10-2588-420A-82ac-dc2d9b1222ff9 encontrada na atl-cs-001.litwareinc.com do servidor Web:</span><span class="sxs-lookup"><span data-stu-id="b735d-121">The following command approves the device update rule d5ce3c10-2588-420a-82ac-dc2d9b1222ff9 found on the Web server atl-cs-001.litwareinc.com:</span></span>
    
        Approve-CsDeviceUpdateRule -Identity service:WebServer:atl-cs-001.litwareinc.com/d5ce3c10-2588-420a-82ac-dc2d9b1222ff9

</div>

<div>

## <a name="to-approve-multiple-device-update-rules"></a><span data-ttu-id="b735d-122">Para aprovar várias regras de atualização de dispositivo</span><span class="sxs-lookup"><span data-stu-id="b735d-122">To approve multiple device update rules</span></span>

  - <span data-ttu-id="b735d-123">Esse comando aprova todas as regras de atualização de dispositivos para dispositivos com marca Microsoft:</span><span class="sxs-lookup"><span data-stu-id="b735d-123">This command approves all the device update rules for Microsoft-branded devices:</span></span>
    
        Get-CsDeviceUpdateRule | Where-Object {$_.Brand -eq "Microsoft"} | Approve-CsDeviceUpdateRule

</div>

<span data-ttu-id="b735d-124">Para obter detalhes, consulte o tópico da ajuda para o cmdlet [Approve-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Approve-CsDeviceUpdateRule) .</span><span class="sxs-lookup"><span data-stu-id="b735d-124">For details, see the Help topic for the [Approve-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Approve-CsDeviceUpdateRule) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b735d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b735d-125">See Also</span></span>


[<span data-ttu-id="b735d-126">Importar regras de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b735d-126">Import Device Update rules in Lync Server 2013</span></span>](lync-server-2013-import-device-update-rules.md)  
[<span data-ttu-id="b735d-127">Restaurar uma regra de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b735d-127">Restore a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-restore-a-device-update-rule.md)  
  

<span data-ttu-id="b735d-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b735d-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

