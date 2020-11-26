---
title: 'Lync Server 2013: Configurar registros de Host DNS'
description: 'Lync Server 2013: Configurar registros de host DNS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS Host records
ms:assetid: 78a1afcf-41c8-4da5-8740-c6570c19078c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398593(v=OCS.15)
ms:contentKeyID: 48184577
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7fd403402d0d2f089d7fc92a62296a56df0cf2e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434036"
---
# <a name="configure-dns-host-records-for-lync-server-2013"></a><span data-ttu-id="8d2d6-103">Configurar registros de Host DNS para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8d2d6-103">Configure DNS Host records for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8d2d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8d2d6-104">

<span> </span></span></span>

<span data-ttu-id="8d2d6-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="8d2d6-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="8d2d6-106">Para concluir esse procedimento com êxito, você deve estar conectado ao servidor ou domínio no mínimo como membro do grupo Domain admins ou um membro do grupo DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="8d2d6-106">To successfully complete this procedure, you should be logged on to the server or domain at minimum as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<div>

## <a name="to-configure-dns-host-a-records"></a><span data-ttu-id="8d2d6-107">Para configurar registros do host DNS A</span><span class="sxs-lookup"><span data-stu-id="8d2d6-107">To configure DNS Host A records</span></span>

1.  <span data-ttu-id="8d2d6-108">No servidor DNS (sistema de nomes de domínio), clique em **Iniciar**, clique em **Ferramentas administrativas** e clique em **DNS**.</span><span class="sxs-lookup"><span data-stu-id="8d2d6-108">On the Domain Name System (DNS) server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="8d2d6-109">Na árvore de console do seu domínio, expanda **zonas de pesquisa direta** e clique com o botão direito do mouse no domínio no qual o Lync Server 2013 será instalado.</span><span class="sxs-lookup"><span data-stu-id="8d2d6-109">In the console tree for your domain, expand **Forward Lookup Zones**, and then right-click the domain in which Lync Server 2013 will be installed.</span></span>

3.  <span data-ttu-id="8d2d6-110">Clique em **novo host (A ou aaaa)**.</span><span class="sxs-lookup"><span data-stu-id="8d2d6-110">Click **New Host (A or AAAA)**.</span></span>

4.  <span data-ttu-id="8d2d6-111">Clique em **nome**, digite o nome do host do pool (o nome do domínio é presumido na zona em que o registro é definido e não precisa ser inserido como parte do registro a).</span><span class="sxs-lookup"><span data-stu-id="8d2d6-111">Click **Name**, type the host name for the pool (the domain name is assumed from the zone that the record is defined in and does not need to be entered as part of the A record).</span></span>

5.  <span data-ttu-id="8d2d6-112">Clique em **endereço IP**, digite o IP virtual (VIP) do balanceador de carga do pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="8d2d6-112">Click **IP Address**, type the virtual IP (VIP) of the load balancer for the Front End pool.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="8d2d6-113">Em implantações que usam um pool de directors, os registros de host (A) para as URLs simples devem apontar para o VIP do balanceador de carga do diretor.</span><span class="sxs-lookup"><span data-stu-id="8d2d6-113">In deployments that use a Director pool, the host (A) records for the simple URLs should point to the VIP of the Director load balancer.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8d2d6-114">Se você implantar apenas um servidor ou diretor da Enterprise Edition que esteja conectado à topologia sem um balanceador de carga ou se implantar um servidor Standard Edition, digite o endereço IP do servidor Enterprise Edition, do servidor Standard Edition ou do director.</span><span class="sxs-lookup"><span data-stu-id="8d2d6-114">If you deploy only one Enterprise Edition server or Director that is connected to the topology without a load balancer, or if you deploy a Standard Edition server, type the IP address of the Enterprise Edition server, Standard Edition server, or Director.</span></span> <span data-ttu-id="8d2d6-115">Um balanceador de carga será necessário se você implantar mais de um servidor ou diretor Enterprise Edition em um pool.</span><span class="sxs-lookup"><span data-stu-id="8d2d6-115">A load balancer is required if you deploy more than one Enterprise Edition server or Director in a pool.</span></span> <span data-ttu-id="8d2d6-116">Balanceadores de carga não são usados com servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="8d2d6-116">Load balancers are not used with Standard Edition servers.</span></span>

    
    </div>

6.  <span data-ttu-id="8d2d6-117">Clique em **Adicionar host** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d2d6-117">Click **Add Host**, and then click **OK**.</span></span>

7.  <span data-ttu-id="8d2d6-118">Para criar um registro adicional adicional, repita as etapas 4 e 5.</span><span class="sxs-lookup"><span data-stu-id="8d2d6-118">To create an additional A record, repeat steps 4 and 5.</span></span>

8.  <span data-ttu-id="8d2d6-119">Quando terminar de criar todos os registros necessários, clique em **concluído**.</span><span class="sxs-lookup"><span data-stu-id="8d2d6-119">When you are finished creating all the A records that you need, click **Done**.</span></span>

<span data-ttu-id="8d2d6-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8d2d6-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

