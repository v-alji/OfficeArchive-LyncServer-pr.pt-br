---
title: Remover um pool Front-End ou um servidor Standard Edition
description: Remova o pool de front-end ou o servidor Standard Edition.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove Front End pool or Standard Edition server
ms:assetid: 83c39a36-49a1-4ac6-9cc5-b0e441b1fdec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688115(v=OCS.15)
ms:contentKeyID: 49733713
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c878d56b073558f4f4b50f31b6742fd581c80241
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440273"
---
# <a name="remove-front-end-pool-or-standard-edition-server"></a><span data-ttu-id="5dc91-103">Remover um pool Front-End ou um servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="5dc91-103">Remove Front End pool or Standard Edition server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5dc91-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5dc91-104">

<span> </span></span></span>

<span data-ttu-id="5dc91-105">_**Tópico da última modificação:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="5dc91-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="5dc91-106">Este tópico fornece orientações sobre o processo de remoção de um pool de front-end ou um servidor front-end Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="5dc91-106">This topic guides you through the process of removing a Front End pool or a Standard Edition Front End Server.</span></span> <span data-ttu-id="5dc91-107">Quando você remove um pool de front-end, Remove cada servidor front-end que pertence ao pool como parte do processo de remoção de pool.</span><span class="sxs-lookup"><span data-stu-id="5dc91-107">When you remove a Front End pool, you remove each Front End Server that belongs to the pool as a part of the pool removal process.</span></span> <span data-ttu-id="5dc91-108">Quando você remove um servidor front-end padrão da edição, deve remover a definição do SQL Store do construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="5dc91-108">When you remove a Standard Edition Front End Server, you must remove the SQL Store definition from Topology Builder.</span></span>

<div>

## <a name="to-remove-a-front-end-server-pool"></a><span data-ttu-id="5dc91-109">Para remover um pool de servidores front-end</span><span class="sxs-lookup"><span data-stu-id="5dc91-109">To remove a Front End Server pool</span></span>

1.  <span data-ttu-id="5dc91-110">Abrir o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="5dc91-110">Open Topology Builder.</span></span>

2.  <span data-ttu-id="5dc91-111">Navegue até o nó do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="5dc91-111">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="5dc91-112">Expanda **pools de front-end do Enterprise Edition**, expanda o pool de front-ends, clique com o botão direito do mouse no pool de front-ends que você deseja remover e clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="5dc91-112">Expand **Enterprise Edition Front End pools**, expand the Front End pool, right-click the Front End pool that you want to remove, and then click **Delete**.</span></span>

4.  <span data-ttu-id="5dc91-113">Publique a topologia, verifique o status da replicação e execute o assistente de implantação do Lync Server conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="5dc91-113">Publish the topology, check replication status, and then run the Lync Server Deployment Wizard as needed.</span></span>

</div>

<div>

## <a name="to-remove-a-standard-edition-front-end-server"></a><span data-ttu-id="5dc91-114">Para remover um servidor front-end padrão da edição</span><span class="sxs-lookup"><span data-stu-id="5dc91-114">To remove a Standard Edition Front End server</span></span>

1.  <span data-ttu-id="5dc91-115">Abrir o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="5dc91-115">Open Topology Builder.</span></span>

2.  <span data-ttu-id="5dc91-116">Navegue até o nó do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="5dc91-116">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="5dc91-117">Expanda **servidores front-end padrão da edição**, clique com o botão direito do mouse no servidor front-end que você deseja remover e, em seguida, clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="5dc91-117">Expand **Standard Edition Front End servers**, right-click the Front End Server that you want to remove, and then click **Delete**.</span></span>

4.  <span data-ttu-id="5dc91-118">Expanda **repositórios SQL**, clique com o botão direito do mouse no banco de dados do SQL Server associado ao servidor front-end Standard Edition e clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="5dc91-118">Expand **SQL stores**, right-click the SQL Server database that is associated with the Standard Edition Front End Server, and then click **Delete**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="5dc91-119">Você deve remover a definição dos bancos de dados do SQL Server posicionado do servidor front-end da Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="5dc91-119">You must remove the definition of the collocated SQL Server databases from the Standard Edition Front End Server.</span></span>

    
    </div>

5.  <span data-ttu-id="5dc91-120">Publique a topologia, verifique o status da replicação e execute o assistente de implantação do Lync Server conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="5dc91-120">Publish the topology, check replication status, and then run the Lync Server Deployment Wizard as needed.</span></span>

<span data-ttu-id="5dc91-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5dc91-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

