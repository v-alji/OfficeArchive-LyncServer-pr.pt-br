---
title: Migrar servidores de Arquivamento e de Monitoramento
description: Migrando servidores de arquivamento e monitoramento.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating Archiving and Monitoring servers
ms:assetid: 77831579-df45-4697-b8c5-207b74a07a40
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205015(v=OCS.15)
ms:contentKeyID: 48184550
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2dabd16fd38dbf463a4bc608fe77368e781571fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443745"
---
# <a name="migrating-archiving-and-monitoring-servers"></a><span data-ttu-id="82287-103">Migrar servidores de Arquivamento e de Monitoramento</span><span class="sxs-lookup"><span data-stu-id="82287-103">Migrating Archiving and Monitoring servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="82287-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="82287-104">

<span> </span></span></span>

<span data-ttu-id="82287-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="82287-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="82287-106">Se você implantou o servidor de arquivamento e monitorando o servidor em seu ambiente do Lync Server 2010, poderá implantar esses servidores no ambiente do Lync Server 2013 após migrar seus pools front-ends.</span><span class="sxs-lookup"><span data-stu-id="82287-106">If you deployed Archiving Server and Monitoring Server in your Lync Server 2010 environment, you can deploy these servers in your Lync Server 2013 environment after you migrate your Front End pools.</span></span> <span data-ttu-id="82287-107">No entanto, se a funcionalidade de arquivamento e monitoramento for essencial para a sua organização, você deverá adicionar arquivamento e monitoramento ao pool piloto do Lync Server 2013 antes de migrar para que a funcionalidade esteja disponível durante o processo de migração.</span><span class="sxs-lookup"><span data-stu-id="82287-107">If archiving and monitoring functionality are critical to your organization, however, you should add archiving and monitoring to your Lync Server 2013 pilot pool before you migrate so that the functionality is available during the migration process.</span></span>

<span data-ttu-id="82287-108">Se você quiser a funcionalidade de arquivamento e monitoramento durante o processo de migração, tenha em mente as seguintes considerações:</span><span class="sxs-lookup"><span data-stu-id="82287-108">If you want archiving and monitoring functionality during the migration process, keep the following considerations in mind:</span></span>

  - <span data-ttu-id="82287-109">O arquivamento de dados e monitoramento de dados não são movidos para a implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="82287-109">Archiving data and monitoring data are not moved to the Lync Server 2013 deployment.</span></span> <span data-ttu-id="82287-110">Os dados que você deve fazer backup antes de descomissionar o ambiente herdado serão o seu histórico de atividades no ambiente do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="82287-110">The data you back up prior to decommissioning the legacy environment will be your history of activity in the Lync Server 2010 environment.</span></span>

  - <span data-ttu-id="82287-111">A versão do Lync Server 2010 do servidor de arquivamento e o Monitoring Server podem ser associadas apenas a um pool de front-end do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="82287-111">The Lync Server 2010 version of Archiving Server and Monitoring Server can be associated only with a Lync Server 2010 Front End pool.</span></span> <span data-ttu-id="82287-112">No Lync Server 2013, o arquivamento e o monitoramento não são mais funções do servidor, mas serviços integrados ao pool de front-ends do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="82287-112">In Lync Server 2013, Archiving and Monitoring are no longer server roles, but services integrated into the Lync Server 2013 Front End pool.</span></span>

  - <span data-ttu-id="82287-113">Durante o tempo em que suas implantações do Lync Server e do Lync Server 2013 coexistem, a versão do Lync Server 2010 do servidor de arquivamento e o Monitoring Server coletam dados para os usuários hospedados nos pools do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="82287-113">During the time that your legacy and Lync Server 2013 deployments coexist, the Lync Server 2010 version of Archiving Server and Monitoring Server gather data for users homed on Lync Server 2010 pools.</span></span> <span data-ttu-id="82287-114">O arquivamento e o monitoramento no Lync Server 2013 coletam dados para usuários hospedados no Lync Server 2013 pools.</span><span class="sxs-lookup"><span data-stu-id="82287-114">Archiving and Monitoring in Lync Server 2013 gather data for users homed on Lync Server 2013 pools.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="82287-115">Durante a fase de migração, quando você ainda estiver usando o servidor de borda herdado com o novo pool piloto do Lync Server 2013, a versão do servidor de arquivamento do Lync Server 2010 continua a coletar dados para os usuários hospedados no Lync Server 2010 pools e o arquivamento no Lync Server 2013 coleta dados para usuários hospedados no Lync Server 2013 pools.</span><span class="sxs-lookup"><span data-stu-id="82287-115">During the phase of migration when you are still using your legacy Edge server with the new Lync Server 2013 pilot pool, the Lync Server 2010 version of Archiving Server continues to gather data for users homed on Lync Server 2010 pools and Archiving in Lync Server 2013 gathers data for users homed on Lync Server 2013 pools.</span></span>

    
    </div>

  - <span data-ttu-id="82287-116">Se você usar uma solução de arquivamento e monitoramento de terceiros em conjunto com o arquivamento e o monitoramento no Lync Server 2013, consulte o fornecedor sobre quando e como você precisa integrar a solução de terceiros com o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="82287-116">If you use a third-party archiving and monitoring solution in conjunction with Archiving and Monitoring in Lync Server 2013, consult with your vendor about when and how you need to integrate the third-party solution with Lync Server 2013.</span></span>

<span data-ttu-id="82287-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="82287-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

