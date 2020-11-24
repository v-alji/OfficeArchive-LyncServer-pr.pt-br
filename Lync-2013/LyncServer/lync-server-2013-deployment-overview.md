---
title: 'Lync Server 2013: Visão geral de implantação'
description: 'Lync Server 2013: visão geral da implantação.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment overview
ms:assetid: da67555e-f410-4c37-9996-d511f37da8d1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205305(v=OCS.15)
ms:contentKeyID: 48185555
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5bb3bac4261783a765b64ab2e81adb107599496b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390259"
---
# <a name="deployment-overview-for-lync-server-2013"></a><span data-ttu-id="6bb27-103">Visão geral de implantação para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6bb27-103">Deployment overview for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6bb27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6bb27-104">

<span> </span></span></span>

<span data-ttu-id="6bb27-105">_**Tópico da última modificação:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="6bb27-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="6bb27-106">A principal diferença entre o Lync Server 2013 Enterprise Edition e o Lync Server 2013 Standard Edition é que a edição padrão não é compatível com os recursos de alta disponibilidade incluídos na Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="6bb27-106">The main difference between Lync Server 2013 Enterprise Edition and Lync Server 2013 Standard Edition is that Standard Edition does not support the high availability features included with Enterprise Edition.</span></span> <span data-ttu-id="6bb27-107">Para alta disponibilidade, você precisa implantar vários servidores front-end em um pool e, em seguida, pode espelhar o servidor que executa o SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6bb27-107">For high availability, you need to deploy multiple Front End Servers to a pool and then you can mirror the server running SQL Server.</span></span> <span data-ttu-id="6bb27-108">Com a Enterprise Edition, você pode optar por posicionar ou definir um servidor autônomo de mediação.</span><span class="sxs-lookup"><span data-stu-id="6bb27-108">With Enterprise Edition you can choose to collocate or define a stand-alone Mediation Server.</span></span> <span data-ttu-id="6bb27-109">O servidor de monitoramento e o servidor de arquivamento podem usar um servidor autônomo que executa o SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6bb27-109">The Monitoring Server and Archiving Server can use a stand-alone server running SQL Server.</span></span> <span data-ttu-id="6bb27-110">Ou podem ter instâncias do SQL Server em execução no servidor de banco de dados para os servidores e pools de front-end.</span><span class="sxs-lookup"><span data-stu-id="6bb27-110">Or, they can have instances of SQL Server running on the database server for the Front End Servers and pools.</span></span>

<span data-ttu-id="6bb27-111">Os servidores que executam o Lync Server 2013 Standard Edition são destinados a organizações menores e locais remotos, que são geograficamente removidos da implantação principal da organização.</span><span class="sxs-lookup"><span data-stu-id="6bb27-111">Servers running Lync Server 2013 Standard Edition are intended for smaller organizations and remote locations, which are geographically removed from the organization’s main deployment.</span></span> <span data-ttu-id="6bb27-112">Dois servidores de servidor Standard Edition emparelhados juntos para failover em caso de desastre podem oferecer suporte a até 5.000 usuários.</span><span class="sxs-lookup"><span data-stu-id="6bb27-112">Two Standard Edition server servers paired together for failover in case of disaster can support up to 5,000 users.</span></span> <span data-ttu-id="6bb27-113">Você não pode pools de servidores padrão da edição, como os servidores front-end na Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="6bb27-113">You cannot pool Standard Edition servers like you can Front End Servers in Enterprise Edition.</span></span> <span data-ttu-id="6bb27-114">Além disso, o banco de dados SQL Server que a edição padrão usa é um servidor posicionado que executa o SQL Server Express projetado para manipular as cargas de trabalho padrão do servidor da edição.</span><span class="sxs-lookup"><span data-stu-id="6bb27-114">Also, the SQL Server database that Standard Edition uses is a collocated server running SQL Server Express that is designed to handle Standard Edition server workloads.</span></span> <span data-ttu-id="6bb27-115">Isso não significa que todas as funções devem residir em um servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="6bb27-115">This is not to say that all roles must reside on a Standard Edition server.</span></span> <span data-ttu-id="6bb27-116">Você pode ter servidores de mediação autônomos e servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="6bb27-116">You can have stand-alone Mediation Servers and Edge Servers.</span></span> <span data-ttu-id="6bb27-117">O banco de dados do SQL Server para o repositório de gerenciamento central e para os fins do Lync Server 2013 deve residir no servidor Standard Edition posicionado com o servidor que executa o SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6bb27-117">The SQL Server database for the Central Management store and for the purposes of Lync Server 2013 must reside on the Standard Edition server collocated with the server running SQL Server.</span></span> <span data-ttu-id="6bb27-118">O servidor de monitoramento e o servidor de arquivamento usam um servidor autônomo com o banco de dados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6bb27-118">The Monitoring Server and Archiving Server use a stand-alone server with the SQL Server database.</span></span>

<span data-ttu-id="6bb27-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6bb27-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

