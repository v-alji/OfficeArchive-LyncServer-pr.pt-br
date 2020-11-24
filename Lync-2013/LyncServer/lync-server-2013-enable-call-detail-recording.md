---
title: 'Lync Server 2013: habilitar a gravação de detalhes da chamada'
description: 'Lync Server 2013: habilitar a gravação de detalhes da chamada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable call detail recording
ms:assetid: 3b28e432-596f-45a5-a070-577d6fa748d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520980(v=OCS.15)
ms:contentKeyID: 48183865
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8d565c78571e34cead61777381875c9c8d23dae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390158"
---
# <a name="enable-call-detail-recording-in-lync-server-2013"></a><span data-ttu-id="edca6-103">Habilitar a gravação de detalhes de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="edca6-103">Enable call detail recording in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="edca6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="edca6-104">

<span> </span></span></span>

<span data-ttu-id="edca6-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="edca6-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="edca6-p101">O CDR (registro de detalhes das chamadas) registra informações de utilização e diagnóstico sobre atividades ponto a ponto, incluindo serviço de mensagens instantâneas, chamadas do protocolo VoIP, compartilhamento de aplicativos, transferência de arquivos e reuniões. Os dados de uso podem ser utilizados para calcular o ROI (retorno sobre o investimento), enquanto os dados de diagnóstico podem ser usados para solucionar problemas de atividades ponto a ponto e reuniões.</span><span class="sxs-lookup"><span data-stu-id="edca6-p101">Call detail recording (CDR) records usage and diagnostic information about peer-to-peer activities including instance messaging, Voice over Internet Protocol (VoIP) calls, application sharing, file transfer, and meetings. The usage data can be used to calculate return on investment (ROI) and the diagnostic data can be used to troubleshoot peer-to-peer activities and meetings.</span></span>

<span data-ttu-id="edca6-108">Use o procedimento a seguir para ativar o CDR para a organização inteira ou para cada local da organização.</span><span class="sxs-lookup"><span data-stu-id="edca6-108">Use the following procedure to enable CDR for your whole organization or each site in your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="edca6-109">Para habilitar o CDR, é preciso configurar o monitoramento e o banco de dados de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="edca6-109">In order to enable CDR you must configure monitoring and a monitoring database.</span></span> <span data-ttu-id="edca6-110">Para obter detalhes, consulte <A href="lync-server-2013-deploying-monitoring.md">implantando o monitoramento no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="edca6-110">For details, see <A href="lync-server-2013-deploying-monitoring.md">Deploying monitoring in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-enable-cdr-with-lync-server-control-panel"></a><span data-ttu-id="edca6-111">Para habilitar CDR com o painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="edca6-111">To enable CDR with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="edca6-112">Em uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes) ou atribuído à função CsServerAdministrator ou CsAdministrator, faça logon em qualquer computador que esteja na rede na qual você implantou o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="edca6-112">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="edca6-113">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="edca6-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="edca6-114">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="edca6-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="edca6-115">Na barra de navegação esquerda, clique em **Monitoramento e Arquivamento** e clique em **Registro de Detalhes das Chamadas**.</span><span class="sxs-lookup"><span data-stu-id="edca6-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Call Detail Recording**.</span></span>

4.  <span data-ttu-id="edca6-116">Na página **Registro de Detalhes das Chamadas**, clique no local apropriado na tabela, em **Ação** e em **Habilitar CDR**.</span><span class="sxs-lookup"><span data-stu-id="edca6-116">On the **Call Detail Recording** page, click the appropriate site from the table, click **Action**, and then click **Enable CDR**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="edca6-117">O CDR é ativado por padrão.</span><span class="sxs-lookup"><span data-stu-id="edca6-117">CDR is enabled by default.</span></span>

    
    </div>

</div>

<div>

## <a name="enabling-cdr-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="edca6-118">Como habilitar o CDR usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="edca6-118">Enabling CDR by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="edca6-119">Você pode habilitar o CDR usando o Windows PowerShell e o cmdlet **set-CsCdrConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="edca6-119">You can enable CDR by using Windows PowerShell and the **Set-CsCdrConfiguration** cmdlet.</span></span> <span data-ttu-id="edca6-120">Você pode executar esse cmdlet a partir do Shell de gerenciamento do Lync Server 2013 ou de uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="edca6-120">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="edca6-121">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="edca6-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-cdr-for-a-single-location"></a><span data-ttu-id="edca6-122">Para habilitar o CDR para um único local</span><span class="sxs-lookup"><span data-stu-id="edca6-122">To enable CDR for a single location</span></span>

  - <span data-ttu-id="edca6-123">Para desabilitar o CDR, defina o parâmetro EnableCDR como Verdadeiro ($True).</span><span class="sxs-lookup"><span data-stu-id="edca6-123">To disable CDR, set the EnableCDR parameter to True ($True).</span></span>
    
        Set-CsCdrConfiguration -Identity "site:Redmond" -EnableCDR $True

</div>

<div>

## <a name="to-disable-cdr-for-a-single-location"></a><span data-ttu-id="edca6-124">Para desabilitar o CDR para um único local</span><span class="sxs-lookup"><span data-stu-id="edca6-124">To disable CDR for a single location</span></span>

  - <span data-ttu-id="edca6-p105">Para desabilitar o CDR, defina o parâmetro EnableCDR como Falso ($False). Desabilitar o CDR não desinstalará o monitoramento, apenas pausará a coleta e o armazenamento de dados de CDR.</span><span class="sxs-lookup"><span data-stu-id="edca6-p105">To disable CDR, set the EnableCDR parameter to False ($False). Disabling CDR does not uninstall monitoring. It pauses the collection and storage of CDR data.</span></span>
    
        Set-CsCdrConfiguration -Identity "site:Redmond" -EnableCDR $False

</div>

<div>

## <a name="to-use-a-single-command-to-enable-cdr-in-multiple-locations"></a><span data-ttu-id="edca6-128">Para usar um único comando para habilitar o CDR em vários locais</span><span class="sxs-lookup"><span data-stu-id="edca6-128">To use a single command to enable CDR in multiple locations</span></span>

  - <span data-ttu-id="edca6-129">Este comando habilita o CDR para todas as configurações do CDR em uso na sua organização.</span><span class="sxs-lookup"><span data-stu-id="edca6-129">This command enables CDR for all the CDR configuration settings currently in use in your organization.</span></span>
    
        Get-CsCdrConfiguration | Set-CsCdrConfiguration "site:Redmond" -EnableCDR $True

</div>

<span data-ttu-id="edca6-130">Para obter mais informações, consulte o tópico da ajuda para o cmdlet [set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="edca6-130">For more information, see the help topic for the [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="edca6-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="edca6-131">See Also</span></span>


[<span data-ttu-id="edca6-132">Planejamento de monitoramento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="edca6-132">Planning for monitoring in Lync Server 2013</span></span>](lync-server-2013-planning-for-monitoring.md)  
[<span data-ttu-id="edca6-133">Implantando o monitoramento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="edca6-133">Deploying monitoring in Lync Server 2013</span></span>](lync-server-2013-deploying-monitoring.md)  
  

<span data-ttu-id="edca6-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="edca6-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

