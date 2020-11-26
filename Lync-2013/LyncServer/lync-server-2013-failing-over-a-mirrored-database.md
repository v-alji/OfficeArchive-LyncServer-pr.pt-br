---
title: 'Lync Server 2013: Failover de banco de dados espelhado'
description: 'Lync Server 2013: falha em um banco de dados espelhado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over a mirrored database
ms:assetid: 70185476-e3d4-440a-9316-fa24b226343e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204991(v=OCS.15)
ms:contentKeyID: 48184450
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fc7c401157c79762f674721ca717296c0fe502db
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428290"
---
# <a name="failing-over-a-mirrored-database-in-lync-server-2013"></a><span data-ttu-id="e0e02-103">Failover de banco de dados espelhado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0e02-103">Failing over a mirrored database in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e0e02-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e0e02-104">

<span> </span></span></span>

<span data-ttu-id="e0e02-105">_**Tópico da última modificação:** 2014-03-14_</span><span class="sxs-lookup"><span data-stu-id="e0e02-105">_**Topic Last Modified:** 2014-03-14_</span></span>

<span data-ttu-id="e0e02-106">Se você tiver configurado seu banco de dados back-end para usar o espelhamento sincronizado com uma testemunha, o failover será automático.</span><span class="sxs-lookup"><span data-stu-id="e0e02-106">If you have configured your back-end database to use synchronized mirroring with a witness, failover is automatic.</span></span> <span data-ttu-id="e0e02-107">Se você configurou o espelhamento sincronizado sem uma testemunha, poderá usar os procedimentos a seguir para fazer failover e failback do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e0e02-107">If you have configured synchronized mirroring without a witness, you can use the following procedures to failover and failback your database.</span></span> <span data-ttu-id="e0e02-108">Você também pode usar esses procedimentos para fazer failover e failback manualmente dos bancos de dados, mesmo se tiver configurado uma testemunha.</span><span class="sxs-lookup"><span data-stu-id="e0e02-108">You can also use these procedures to manually failover and failback your databases even if you have configured a witness.</span></span>

<div>

## <a name="to-fail-over-your-back-end-database"></a><span data-ttu-id="e0e02-109">Para fazer failover em seu banco de dados back-end</span><span class="sxs-lookup"><span data-stu-id="e0e02-109">To fail over your back-end database</span></span>

1.  <span data-ttu-id="e0e02-110">Antes de realizar o failover, determine qual banco de dados back-end é o principal e qual é o espelho digitando o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e0e02-110">Before failing over, determine which back-end database is the principal and which is the mirror by typing the following cmdlet:</span></span>
    
        Get-CsDatabaseMirrorState -PoolFqdn <poolFQDN> -DatabaseType User

2.  <span data-ttu-id="e0e02-111">Se o repositório de gerenciamento central estiver hospedado nesse pool, digite o cmdlet a seguir para determinar qual é a entidade de segurança e qual é o espelho do repositório de gerenciamento central:</span><span class="sxs-lookup"><span data-stu-id="e0e02-111">If the Central Management store is hosted in this pool, type the following cmdlet to determine which is the principal and which is the mirror for the Central Management store:</span></span>
    
        Get-CsDatabaseMirrorState -PoolFqdn <poolFQDN> -DatabaseType CentralMgmt

3.  <span data-ttu-id="e0e02-112">Executar o failover do banco de dados do usuário:</span><span class="sxs-lookup"><span data-stu-id="e0e02-112">Perform the failover of the user database:</span></span>
    
      - <span data-ttu-id="e0e02-113">Se o principal falhar e você estiver falhando no espelho, digite:</span><span class="sxs-lookup"><span data-stu-id="e0e02-113">If the primary has failed and you are failing over to the mirror, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType User -NewPrincipal mirror -Verbose
    
      - <span data-ttu-id="e0e02-114">Se o espelhamento falhar e você estiver falhando para o principal, digite:</span><span class="sxs-lookup"><span data-stu-id="e0e02-114">If the mirror has failed and you are failing over to the primary, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType User -NewPrincipal primary -Verbose

4.  <span data-ttu-id="e0e02-115">Se o pool hospedar o servidor central de gerenciamento, realize o failover do repositório de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="e0e02-115">If the pool hosts the Central Management Server, perform the failover of the Central Management store.</span></span>
    
      - <span data-ttu-id="e0e02-116">Se o principal falhar e você estiver falhando no espelho, digite:</span><span class="sxs-lookup"><span data-stu-id="e0e02-116">If the primary has failed and you are failing over to the mirror, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType CentralMgmt -NewPrincipal mirror -Verbose
    
      - <span data-ttu-id="e0e02-117">Se o espelhamento falhar e você estiver falhando para o principal, digite:</span><span class="sxs-lookup"><span data-stu-id="e0e02-117">If the mirror has failed and you are failing over to the primary, type:</span></span>
        
            Invoke-CsDatabaseFailover -PoolFqdn <poolFQDN> -DatabaseType CentralMgmt -NewPrincipal primary -Verbose

<span data-ttu-id="e0e02-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e0e02-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

