---
title: 'Lync Server 2013: Visão geral de Arquivamento'
description: 'Lync Server 2013: visão geral do arquivamento.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Archiving
ms:assetid: 1e3c2ef1-f561-4f57-8b6a-7d78addc1ed1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204729(v=OCS.15)
ms:contentKeyID: 48183570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 548d82d6731fd28fafbde5816a7a0dc77a1fcc02
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424825"
---
# <a name="overview-of-archiving-in-lync-server-2013"></a><span data-ttu-id="6dcd0-103">Visão geral de Arquivamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6dcd0-103">Overview of Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6dcd0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6dcd0-104">

<span> </span></span></span>

<span data-ttu-id="6dcd0-105">_**Tópico da última modificação:** 2013-09-30_</span><span class="sxs-lookup"><span data-stu-id="6dcd0-105">_**Topic Last Modified:** 2013-09-30_</span></span>

<span data-ttu-id="6dcd0-106">O arquivamento no Lync Server 2013 fornece uma maneira de arquivar comunicações que são enviadas pelo Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dcd0-106">Archiving in Lync Server 2013 provides a way for you to archive communications that are sent through Lync Server 2013.</span></span>

<span data-ttu-id="6dcd0-107">Você pode implementar o arquivamento como parte da implantação inicial do Lync Server 2013 ou pode adicioná-lo a uma implantação existente.</span><span class="sxs-lookup"><span data-stu-id="6dcd0-107">You can implement Archiving as part of your initial Lync Server 2013 deployment, or you can add it to an existing deployment.</span></span> <span data-ttu-id="6dcd0-108">Para usar bancos de dados de arquivamento do Lync Server 2013 (bancos de dados do SQL Server) para armazenamento de dados de arquivamento, você usa o construtor de topologias para adicionar os bancos de dados à sua topologia e, em seguida, publicar a topologia novamente.</span><span class="sxs-lookup"><span data-stu-id="6dcd0-108">To use Lync Server 2013 Archiving databases (SQL Server databases) for storage of archiving data, you use Topology Builder to add the databases to your topology, and then publish the topology again.</span></span> <span data-ttu-id="6dcd0-109">Se todos os seus usuários estiverem hospedados no Exchange 2013 e tiverem suas caixas de correio colocadas em In-Place isenção, você não precisará atualizar a topologia, mas só precisa habilitar a integração do Microsoft Exchange para armazenar dados armazenados no Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="6dcd0-109">If all your users are homed on Exchange 2013 and have their mailboxes put on In-Place Hold, you do not have to update your topology, but only need to enable Microsoft Exchange integration to store archived data in Exchange 2013.</span></span>

<span data-ttu-id="6dcd0-110">Ao implementar o arquivamento, configure-o para especificar o que é arquivado.</span><span class="sxs-lookup"><span data-stu-id="6dcd0-110">When you implement Archiving, you configure it to specify what is archived.</span></span> <span data-ttu-id="6dcd0-111">Por padrão, nada é arquivado.</span><span class="sxs-lookup"><span data-stu-id="6dcd0-111">By default, nothing is archived.</span></span> <span data-ttu-id="6dcd0-112">Você configura e gerencia o arquivamento usando o painel de controle do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6dcd0-112">You configure and manage Archiving by using Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="6dcd0-113">Você pode implementar o arquivamento para comunicações internas, comunicações externas ou ambos.</span><span class="sxs-lookup"><span data-stu-id="6dcd0-113">You can implement Archiving for internal communications, external communications, or both.</span></span> <span data-ttu-id="6dcd0-114">Você pode definir as configurações de arquivamento de toda a sua organização e, opcionalmente, para sites específicos, pools específicos e usuários e grupos de usuários específicos.</span><span class="sxs-lookup"><span data-stu-id="6dcd0-114">You can configure archiving settings your entire organization and, optionally, for specific sites, specific pools, and specific users and user groups.</span></span> <span data-ttu-id="6dcd0-115">Para obter detalhes sobre como determinar as opções apropriadas para sua organização, consulte [definindo seus requisitos para o arquivamento no Lync Server 2013](lync-server-2013-defining-your-requirements-for-archiving.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="6dcd0-115">For details about determining the appropriate options for your organization, see [Defining your requirements for Archiving in Lync Server 2013](lync-server-2013-defining-your-requirements-for-archiving.md) in the Planning documentation.</span></span> <span data-ttu-id="6dcd0-116">Para obter detalhes sobre como as políticas e configurações de arquivamento são implementadas e detalhes sobre quais informações podem ou não ser arquivadas, consulte [como o arquivamento funciona no Lync Server 2013](lync-server-2013-how-archiving-works.md) na documentação de planejamento, documentação de implantação ou documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="6dcd0-116">For details about how Archiving policies and configurations are implemented, and details about what information can or cannot be archived, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<span data-ttu-id="6dcd0-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6dcd0-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

