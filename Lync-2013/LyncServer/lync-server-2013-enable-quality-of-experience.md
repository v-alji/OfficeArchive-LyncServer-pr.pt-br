---
title: 'Lync Server 2013: habilitar a qualidade da experiência'
description: 'Lync Server 2013: habilite a qualidade da experiência.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Quality of Experience
ms:assetid: c8bb3c67-b324-4d94-8158-00c792c7ac42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182583(v=OCS.15)
ms:contentKeyID: 48185385
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 43746227395477596ff5e39809cf819c110287ab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437529"
---
# <a name="enable-quality-of-experience-in-lync-server-2013"></a><span data-ttu-id="ba866-103">Habilitar a qualidade de experiência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba866-103">Enable Quality of Experience in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ba866-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ba866-104">

<span> </span></span></span>

<span data-ttu-id="ba866-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="ba866-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="ba866-106">A Qualidade de experiência (QoE) registra os dados numéricos que indicam a qualidade da mídia e informações sobre participantes, nome de dispositivos, drivers, endereços IP e tipos de pontos de extremidade envolvidos nas chamadas e sessões.</span><span class="sxs-lookup"><span data-stu-id="ba866-106">Quality of Experience (QoE) records numeric data that indicates the media quality and information about participants, device names, drivers, IP addresses, and endpoint types involved in calls and sessions.</span></span> <span data-ttu-id="ba866-107">Para obter detalhes, consulte [planejando a monitoração no Lync Server 2013](lync-server-2013-planning-for-monitoring.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="ba866-107">For details, see [Planning for monitoring in Lync Server 2013](lync-server-2013-planning-for-monitoring.md) in the Planning documentation.</span></span>

<span data-ttu-id="ba866-108">Use o procedimento a seguir para habilitar QoE para toda sua organização ou para cada site em sua organização.</span><span class="sxs-lookup"><span data-stu-id="ba866-108">Use the following procedure to enable QoE for your whole organization or each site in your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ba866-109">Para habilitar a QoE, é necessário primeiro configurar o monitoramento e um back-end de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="ba866-109">To enable QoE, you must first configure monitoring and a monitoring back-end database.</span></span> <span data-ttu-id="ba866-110">Para obter detalhes, consulte <A href="lync-server-2013-deploying-monitoring.md">implantando o monitoramento no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="ba866-110">For details, see <A href="lync-server-2013-deploying-monitoring.md">Deploying monitoring in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-enable-qoe-by-using-lync-server-control-panel"></a><span data-ttu-id="ba866-111">Para habilitar a QoE usando o painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="ba866-111">To enable QoE by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="ba866-112">Em uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes) ou atribuído à função CsServerAdministrator ou CsAdministrator, faça logon em qualquer computador que esteja na rede na qual você implantou o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ba866-112">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="ba866-113">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ba866-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ba866-114">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ba866-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ba866-115">Na barra de navegação esquerda, clique em **Monitoramento e arquivamento** e em **Dados de Qualidade da Experiência**.</span><span class="sxs-lookup"><span data-stu-id="ba866-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Quality of Experience Data**.</span></span>

4.  <span data-ttu-id="ba866-116">Na página **Dados de Qualidade da Experiência**, clique no conjunto adequado na tabela, clique em **Ação** e em **Habilitar QoE**.</span><span class="sxs-lookup"><span data-stu-id="ba866-116">On the **Quality of Experience Data** page, click the appropriate collection from the table, click **Action**, and then click **Enable QoE**.</span></span>

</div>

<div>

## <a name="enabling-qoe-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="ba866-117">Habilitando a QoE usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ba866-117">Enabling QoE by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="ba866-118">Você pode habilitar a QoE usando o Windows PowerShell e o cmdlet **set-CsQoEConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="ba866-118">You can enable QoE by using Windows PowerShell and the **Set-CsQoEConfiguration** cmdlet.</span></span> <span data-ttu-id="ba866-119">Você pode executar esse cmdlet a partir do Shell de gerenciamento do Lync Server 2013 ou de uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ba866-119">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ba866-120">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="ba866-120">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-qoe-for-a-single-location"></a><span data-ttu-id="ba866-121">Para habilitar a QoE para um único local</span><span class="sxs-lookup"><span data-stu-id="ba866-121">To enable QoE for a single location</span></span>

  - <span data-ttu-id="ba866-122">Para habilitar a QoE, defina o parâmetro EnableQoE para True ($True).</span><span class="sxs-lookup"><span data-stu-id="ba866-122">To enable QoE, set the EnableQoE parameter to True ($True).</span></span>
    
        Set-CsQoEConfiguration -Identity "site:Redmond" -EnableQoE $True

</div>

<div>

## <a name="to-disable-qoe-for-a-single-location"></a><span data-ttu-id="ba866-123">Para desabilitar a QoE para um único local</span><span class="sxs-lookup"><span data-stu-id="ba866-123">To disable QoE for a single location</span></span>

  - <span data-ttu-id="ba866-p105">Para desabilitar a QoE, defina o parâmetro EnableQoE para False ($False). Isso não desinstala o monitoramento; pausa o conjunto e armazena os dados de QoE.</span><span class="sxs-lookup"><span data-stu-id="ba866-p105">To disable QoE, set the EnableQoE parameter to False ($False). This does not uninstall monitoring. It pauses the collection and storage of QoE data.</span></span>
    
        Set-CsQoEConfiguration -Identity "site:Redmond" -EnableQoE $False

</div>

<div>

## <a name="to-use-a-single-command-to-enable-qoe-in-multiple-locations"></a><span data-ttu-id="ba866-127">Para usar um único comando para habilitar a QoE em vários locais</span><span class="sxs-lookup"><span data-stu-id="ba866-127">To use a single command to enable QoE in multiple locations</span></span>

  - <span data-ttu-id="ba866-128">Este comando habilita a QoE para todas as definições de configuração de QoE atualmente em uso na sua organização.</span><span class="sxs-lookup"><span data-stu-id="ba866-128">This command enables QoE for all the QoE configuration settings currently in use in your organization.</span></span>
    
        Get-CsQoEConfiguration | Set-CsQoEConfiguration "site:Redmond" -EnableQoE $True

</div>

<span data-ttu-id="ba866-129">Para obter detalhes, consulte [set-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsQoEConfiguration).</span><span class="sxs-lookup"><span data-stu-id="ba866-129">For details, see [Set-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsQoEConfiguration).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ba866-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba866-130">See Also</span></span>


[<span data-ttu-id="ba866-131">Planejamento de monitoramento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba866-131">Planning for monitoring in Lync Server 2013</span></span>](lync-server-2013-planning-for-monitoring.md)  
[<span data-ttu-id="ba866-132">Implantando o monitoramento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba866-132">Deploying monitoring in Lync Server 2013</span></span>](lync-server-2013-deploying-monitoring.md)  
  

<span data-ttu-id="ba866-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ba866-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

