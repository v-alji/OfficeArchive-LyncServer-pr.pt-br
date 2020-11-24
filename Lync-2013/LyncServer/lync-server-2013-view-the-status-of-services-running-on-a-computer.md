---
title: 'Lync Server 2013: exibir o status dos serviços em execução em um computador'
description: 'Lync Server 2013: exibir o status dos serviços em execução em um computador.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View the status of services running on a computer
ms:assetid: f41918e7-4c02-431e-840a-88a1f36ae499
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182606(v=OCS.15)
ms:contentKeyID: 48185804
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22aeb13f2beb5d3b0ee5eec8109eceeb14e40213
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390122"
---
# <a name="view-the-status-of-services-running-on-a-computer-in-lync-server-2013"></a><span data-ttu-id="fd80f-103">Exibir o status dos serviços em execução em um computador no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd80f-103">View the status of services running on a computer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fd80f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fd80f-104">

<span> </span></span></span>

<span data-ttu-id="fd80f-105">_**Tópico da última modificação:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="fd80f-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="fd80f-106">Você pode usar o painel de controle do Lync Server 2013 para exibir todos os serviços que estão sendo executados em um computador específico na sua topologia do Lync Server e ver o status de cada serviço.</span><span class="sxs-lookup"><span data-stu-id="fd80f-106">You can use Lync Server 2013 Control Panel to view all the services that are running on a specific computer in your Lync Server topology and see the status of each service.</span></span>

<div>

## <a name="to-view-the-status-of-services-running-on-a-computer"></a><span data-ttu-id="fd80f-107">Para exibir o status dos serviços em execução em um computador</span><span class="sxs-lookup"><span data-stu-id="fd80f-107">To view the status of services running on a computer</span></span>

1.  <span data-ttu-id="fd80f-108">Usando uma conta de usuário atribuída à função CsUserAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="fd80f-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fd80f-109">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fd80f-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="fd80f-110">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="fd80f-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="fd80f-111">Na barra de navegação à esquerda, clique em **topologia**.</span><span class="sxs-lookup"><span data-stu-id="fd80f-111">In the left navigation bar, click **Topology**.</span></span>

4.  <span data-ttu-id="fd80f-112">Na página **status** , classifique ou pesquise a lista, conforme necessário, para localizar o computador no qual você está interessado e, em seguida, clique no nome do computador.</span><span class="sxs-lookup"><span data-stu-id="fd80f-112">On the **Status** page, sort or search the list, as required, to find the computer you’re interested in, and then click the computer name.</span></span>

5.  <span data-ttu-id="fd80f-113">Execute qualquer uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="fd80f-113">Do any of the following:</span></span>
    
      - <span data-ttu-id="fd80f-114">Para ver o status mais recente dos serviços em execução no computador, clique em **obter status do serviço**.</span><span class="sxs-lookup"><span data-stu-id="fd80f-114">To see the latest status of services running on the computer, click **Get service status**.</span></span>
    
      - <span data-ttu-id="fd80f-115">Para ver uma lista de serviços específicos em execução no computador e o status de cada serviço, clique em **Propriedades** e, em seguida, clique em **fechar** para retornar à lista.</span><span class="sxs-lookup"><span data-stu-id="fd80f-115">To see a list of specific services running on the computer and the status of each service, click **Properties**, and then click **Close** to return to the list.</span></span>

</div>

<div>

## <a name="viewing-service-status-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="fd80f-116">Visualizando o status do serviço usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fd80f-116">Viewing Service Status by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="fd80f-117">Você também pode exibir o status do serviço usando o Windows PowerShell e o cmdlet **Get-CsWindowsService** .</span><span class="sxs-lookup"><span data-stu-id="fd80f-117">You can also view service status by using Windows PowerShell and the **Get-CsWindowsService** cmdlet.</span></span> <span data-ttu-id="fd80f-118">Você pode executar esse cmdlet a partir do Shell de gerenciamento do Lync Server 2013 ou de uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fd80f-118">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="fd80f-119">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="fd80f-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-service-status"></a><span data-ttu-id="fd80f-120">Para exibir o status do serviço</span><span class="sxs-lookup"><span data-stu-id="fd80f-120">To view service status</span></span>

  - <span data-ttu-id="fd80f-121">Para exibir o status do serviço em um computador, digite um comando semelhante ao seguinte no Shell de gerenciamento do Lync Server e pressione ENTER:</span><span class="sxs-lookup"><span data-stu-id="fd80f-121">To view service status on a computer, type a command similar to the following in the Lync Server Management Shell and then press Enter:</span></span>
    
        Get-CsWindowsService -ComputerName atl-cs-001.litwareinc.com | Select-Object RoleName, Status
    
    <span data-ttu-id="fd80f-122">Este comando retorna informações semelhantes para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fd80f-122">This command returns information similar to the following:</span></span>
    
        RoleName                                  Status
        --------                                  ------
        {W3SVC}                                   Running
        {CentralManagement}                       Running
        {ClsAgent}                                Running
        {Registrar, UserServer, EdgeServer}       Running
        {ApplicationServer}                       Running
        {ConferencingServer}                      Running
        {MediationServer}                         Running

</div>

<span data-ttu-id="fd80f-123">Para obter detalhes, consulte [Get-CsWindowsService](https://docs.microsoft.com/powershell/module/skype/Get-CsWindowsService).</span><span class="sxs-lookup"><span data-stu-id="fd80f-123">For details, see [Get-CsWindowsService](https://docs.microsoft.com/powershell/module/skype/Get-CsWindowsService).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fd80f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd80f-124">See Also</span></span>


[<span data-ttu-id="fd80f-125">Gerenciando dispositivos, telefones e aplicativos do cliente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd80f-125">Managing devices, phones, and client applications in Lync Server 2013</span></span>](lync-server-2013-managing-devices-phones-and-client-applications.md)  
  

<span data-ttu-id="fd80f-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fd80f-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

