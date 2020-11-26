---
title: 'Lync Server 2013: iniciar ou parar serviços do Lync Server'
description: 'Lync Server 2013: iniciar ou parar serviços do Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Start or stop Lync Server 2013 services
ms:assetid: 1c70b4ec-9de5-4f7a-a3c9-c0eb76710505
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520958(v=OCS.15)
ms:contentKeyID: 48183554
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d6e6520cbf6fda38676beab984c2d006061b019
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423677"
---
# <a name="start-or-stop-lync-server-2013-services"></a><span data-ttu-id="53aa4-103">Iniciar ou parar os serviços do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="53aa4-103">Start or stop Lync Server 2013 services</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="53aa4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="53aa4-104">

<span> </span></span></span>

<span data-ttu-id="53aa4-105">_**Tópico da última modificação:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="53aa4-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="53aa4-106">Você pode usar o painel de controle do Lync Server para iniciar ou parar todos os serviços do Lync Server 2013 em execução em um computador específico ou para iniciar ou parar um serviço específico.</span><span class="sxs-lookup"><span data-stu-id="53aa4-106">You can use Lync Server Control Panel to start or stop all the Lync Server 2013 services running on a specific computer or to start or stop a specific service.</span></span>

<div>

## <a name="to-start-or-stop-all-lync-server-services-on-a-computer"></a><span data-ttu-id="53aa4-107">Para iniciar ou parar todos os serviços do Lync Server em um computador</span><span class="sxs-lookup"><span data-stu-id="53aa4-107">To start or stop all Lync Server services on a computer</span></span>

1.  <span data-ttu-id="53aa4-108">Em uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes) ou atribuído à função CsServerAdministrator ou CsAdministrator, faça logon em qualquer computador que esteja na rede na qual você implantou o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="53aa4-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span> <span data-ttu-id="53aa4-109">Você pode determinar se você atribuiu o CsServerAdministrator ou a função RBAC CsAdministrator executando um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="53aa4-109">You can determine whether you have been assigned the CsServerAdministrator or the CsAdministrator RBAC role by running a command similar to the following:</span></span>
    
        Get-CsAdminRoleAssignment -Identity "kenmyer"

2.  <span data-ttu-id="53aa4-110">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="53aa4-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="53aa4-111">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="53aa4-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="53aa4-112">Na barra de navegação à esquerda, clique em **topologia** e, em seguida, clique em **status**.</span><span class="sxs-lookup"><span data-stu-id="53aa4-112">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="53aa4-113">Na página **status** , classifique ou pesquise a lista, conforme necessário, para localizar o computador que está executando os serviços que você deseja iniciar ou parar e, em seguida, clique nele.</span><span class="sxs-lookup"><span data-stu-id="53aa4-113">On the **Status** page, sort or search through the list as needed to find the computer that is running the services you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="53aa4-114">Clique em **ação**.</span><span class="sxs-lookup"><span data-stu-id="53aa4-114">Click **Action**.</span></span>

6.  <span data-ttu-id="53aa4-115">Clique em **Iniciar todos os serviços** ou **parar todos os serviços**.</span><span class="sxs-lookup"><span data-stu-id="53aa4-115">Click **Start All services** or **Stop All services**.</span></span>

</div>

<div>

## <a name="to-start-or-stop-a-specific-service"></a><span data-ttu-id="53aa4-116">Para iniciar ou parar um serviço específico</span><span class="sxs-lookup"><span data-stu-id="53aa4-116">To start or stop a specific service</span></span>

1.  <span data-ttu-id="53aa4-117">Usando uma conta de usuário atribuída à função CsUserAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="53aa4-117">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="53aa4-118">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="53aa4-118">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="53aa4-119">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="53aa4-119">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="53aa4-120">Na barra de navegação à esquerda, clique em **topologia** e, em seguida, clique em **status**.</span><span class="sxs-lookup"><span data-stu-id="53aa4-120">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="53aa4-121">Na página **status** , classifique ou pesquise a lista, conforme necessário, para localizar o computador que está executando o serviço que você deseja iniciar ou parar e, em seguida, clique nele.</span><span class="sxs-lookup"><span data-stu-id="53aa4-121">On the **Status** page, sort or search through the list as needed to find the computer that is running the service you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="53aa4-122">Clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="53aa4-122">Click **Properties**.</span></span>

6.  <span data-ttu-id="53aa4-123">Classifique a lista de serviços, se necessário, e clique no serviço que você deseja iniciar ou parar.</span><span class="sxs-lookup"><span data-stu-id="53aa4-123">Sort the list of services, if necessary, and click the service you want to start or stop.</span></span>

7.  <span data-ttu-id="53aa4-124">Clique em **ação**.</span><span class="sxs-lookup"><span data-stu-id="53aa4-124">Click **Action**.</span></span>

8.  <span data-ttu-id="53aa4-125">Clique em **Iniciar serviço** ou **parar serviço**.</span><span class="sxs-lookup"><span data-stu-id="53aa4-125">Click **Start service** or **Stop service**.</span></span>

9.  <span data-ttu-id="53aa4-126">Clique em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="53aa4-126">Click **Close**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="53aa4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="53aa4-127">See Also</span></span>


[<span data-ttu-id="53aa4-128">Evitar sessões para serviços no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="53aa4-128">Prevent sessions for services in Lync Server 2013</span></span>](lync-server-2013-prevent-sessions-for-services.md)  


[<span data-ttu-id="53aa4-129">Gerenciando a topologia do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="53aa4-129">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="53aa4-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="53aa4-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

