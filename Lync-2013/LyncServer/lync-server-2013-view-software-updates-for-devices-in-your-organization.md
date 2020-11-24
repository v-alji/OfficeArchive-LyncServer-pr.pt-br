---
title: 'Lync Server 2013: exibir atualizações de software para dispositivos em sua organização'
description: 'Lync Server 2013: exibir atualizações de software para dispositivos em sua organização.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View software updates for devices in your organization
ms:assetid: d2cca12b-ed43-4e1f-90ab-d14bca8b482c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182592(v=OCS.15)
ms:contentKeyID: 48185418
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 833ab25315847b760271c63bbfca3ba8357e41c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390126"
---
# <a name="view-software-updates-for-devices-in-lync-server-2013"></a><span data-ttu-id="69257-103">Exibir atualizações de software para dispositivos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="69257-103">View software updates for devices in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="69257-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="69257-104">

<span> </span></span></span>

<span data-ttu-id="69257-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="69257-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="69257-106">Com o Lync Server 2013, você usa o serviço Web de atualização de dispositivo para exibir e gerenciar atualizações de software para os dispositivos da sua organização.</span><span class="sxs-lookup"><span data-stu-id="69257-106">With Lync Server 2013, you use Device Update Web service to view and manage software updates for your organization’s devices.</span></span> <span data-ttu-id="69257-107">Essas atualizações estão disponíveis em arquivos. cab (Cabinet) a partir do website de suporte da Microsoft em [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091) .</span><span class="sxs-lookup"><span data-stu-id="69257-107">These updates are available in .cab (cabinet) files from the Microsoft Support website at [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091).</span></span> <span data-ttu-id="69257-108">Depois de baixar o arquivo. cab, execute o cmdlet **Import-CSDeviceUpdate** para importar as regras de atualização de dispositivo do arquivo. cab.</span><span class="sxs-lookup"><span data-stu-id="69257-108">After you download the .cab file, run the **Import-CSDeviceUpdate** cmdlet to import the device update rules from the .cab file.</span></span> <span data-ttu-id="69257-109">Para obter detalhes sobre o cmdlet **Import-CSDeviceUpdate** , consulte [importar-CSDeviceUpdate](https://docs.microsoft.com/powershell/module/skype/Import-CsDeviceUpdate) na documentação do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69257-109">For details about the **Import-CSDeviceUpdate** cmdlet, see [Import-CsDeviceUpdate](https://docs.microsoft.com/powershell/module/skype/Import-CsDeviceUpdate) in the Lync Server Management Shell documentation.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="69257-110">Antes de implantar uma nova atualização em sua organização, verifique se ela funciona corretamente em um dispositivo de teste.</span><span class="sxs-lookup"><span data-stu-id="69257-110">Before deploying a new update to your organization, verify that it functions correctly on a test device.</span></span>



</div>

<div>

## <a name="to-view-software-updates-for-uc-devices"></a><span data-ttu-id="69257-111">Para exibir atualizações de software para dispositivos de comunicação unificada</span><span class="sxs-lookup"><span data-stu-id="69257-111">To view software updates for UC devices</span></span>

1.  <span data-ttu-id="69257-112">Usando uma conta de usuário atribuída à função CsUserAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="69257-112">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="69257-113">No site de suporte da Microsoft em [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091) , baixe o arquivo. cab para um local em um computador com o Lync Server 2013 (por exemplo, C: \\ atualizações \\UCUpdates.cab).</span><span class="sxs-lookup"><span data-stu-id="69257-113">From the Microsoft Support website at [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091), download the .cab file to a location on a Lync Server 2013 computer (for example, C:\\Updates\\UCUpdates.cab).</span></span>

3.  <span data-ttu-id="69257-114">Importe as regras de atualização de dispositivo do arquivo C: \\ updates \\UCUpdates.cab executando um dos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="69257-114">Import the device update rules from the C:\\Updates\\UCUpdates.cab file by running one of the following cmdlets:</span></span>
    
      - <span data-ttu-id="69257-115">Se o arquivo. cab estiver localizado no mesmo computador que está executando o serviço a ser atualizado (serviço: Redmond-websvc-2), execute o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="69257-115">If the .cab file is located on the same computer as the one running the service to be updated (service:Redmond-websvc-2), run the following cmdlet:</span></span>
        
            Import-CsDeviceUpdate -Identity service:Redmond-websvc-2 -FileName C:\Updates\UCUpdates.cab
    
      - <span data-ttu-id="69257-116">Se o arquivo. cab estiver localizado em um computador diferente do que o que está executando o serviço a ser atualizado (serviço: Redmond-websvc-3), execute o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="69257-116">If the .cab file is located on a different computer than the one running the service to be updated (service:Redmond-websvc-3), run the following cmdlet:</span></span>
        
            Import-CsDeviceUpdate -Identity service:Redmond-websvc-3 -ByteInput C:\Updates\UCUpdates.cab

4.  <span data-ttu-id="69257-117">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69257-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="69257-118">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="69257-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

5.  <span data-ttu-id="69257-119">Na barra de navegação à esquerda, clique em **clientes** e em **atualização de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="69257-119">In the left navigation bar, click **Clients**, and then click **Device Update**.</span></span>

6.  <span data-ttu-id="69257-120">Na página **atualização do dispositivo** , clique em uma atualização na lista e siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="69257-120">On the **Device Update** page, click an update in the list, and then do one of the following:</span></span>
    
      - <span data-ttu-id="69257-121">**Cancelar uma atualização pendente.**</span><span class="sxs-lookup"><span data-stu-id="69257-121">**Cancel a pending update.**</span></span> <span data-ttu-id="69257-122">Para impedir que a atualização selecionada seja implantada nos dispositivos da sua organização, clique no menu **ação** e, em seguida, clique em **cancelar atualizações pendentes**.</span><span class="sxs-lookup"><span data-stu-id="69257-122">To prevent the selected update from being deployed to your organization’s devices, click the **Action** menu, and then click **Cancel pending updates**.</span></span>
    
      - <span data-ttu-id="69257-123">**Aprove uma atualização.**</span><span class="sxs-lookup"><span data-stu-id="69257-123">**Approve an update.**</span></span> <span data-ttu-id="69257-124">Para permitir que a atualização selecionada seja implantada nos dispositivos da sua organização, clique no menu **ação** e, em seguida, clique em **aprovar**.</span><span class="sxs-lookup"><span data-stu-id="69257-124">To allow the selected update to be deployed to your organization’s devices, click the **Action** menu, and then click **Approve**.</span></span>
    
      - <span data-ttu-id="69257-125">**Restaurar uma atualização.**</span><span class="sxs-lookup"><span data-stu-id="69257-125">**Restore an update.**</span></span> <span data-ttu-id="69257-126">Para permitir que uma atualização aprovada anteriormente seja implantada nos dispositivos da sua organização, clique no menu **ação** e, em seguida, clique em **restaurar**.</span><span class="sxs-lookup"><span data-stu-id="69257-126">To allow a previously approved update to be deployed to your organization’s devices, click the **Action** menu, and then click **Restore**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="69257-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="69257-127">See Also</span></span>


[<span data-ttu-id="69257-128">Gerenciando dispositivos, telefones e aplicativos do cliente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="69257-128">Managing devices, phones, and client applications in Lync Server 2013</span></span>](lync-server-2013-managing-devices-phones-and-client-applications.md)  
  

<span data-ttu-id="69257-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="69257-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

