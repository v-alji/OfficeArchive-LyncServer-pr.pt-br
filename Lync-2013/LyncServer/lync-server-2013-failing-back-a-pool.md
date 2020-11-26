---
title: 'Lync Server 2013: Failback de pool'
description: 'Lync Server 2013: falha no pool novamente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing back a pool
ms:assetid: 6232b644-ef57-4c9c-abec-14ff8ffc9fe7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204945(v=OCS.15)
ms:contentKeyID: 48184289
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1c1fc0ea4514d2f951dd936521590d47b809db38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428325"
---
# <a name="failing-back-a-pool-in-lync-server-2013"></a><span data-ttu-id="535b7-103">Failback de pool no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="535b7-103">Failing back a pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="535b7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="535b7-104">

<span> </span></span></span>

<span data-ttu-id="535b7-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="535b7-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="535b7-106">Após o pool que sofreu o desastre ficar online novamente (ou seja, Pool1 neste exemplo), siga as etapas a seguir para restaurar a implantação para o status de trabalho normal.</span><span class="sxs-lookup"><span data-stu-id="535b7-106">After the pool that experienced the disaster is back online (that is, Pool1 in this example), take the following steps to restore your deployment to regular working status.</span></span>

<span data-ttu-id="535b7-107">Observe que o processo de failback demora vários minutos para ser concluído.</span><span class="sxs-lookup"><span data-stu-id="535b7-107">Note that the failback process takes several minute to complete.</span></span>  <span data-ttu-id="535b7-108">Para referência, a expectativa é de até 60 minutos para um pool de 20.000 usuários.</span><span class="sxs-lookup"><span data-stu-id="535b7-108">For reference, it is expected to take up to 60 minutes for a pool of 20,000 users.</span></span>

1.  <span data-ttu-id="535b7-109">Reproduza os usuários que estavam originalmente hospedados no Pool1 e que falharam no Pool2 digitando o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="535b7-109">Fail back the users who were originally homed in Pool1 and have been failed over to Pool2 by typing the following cmdlet:</span></span>
    
        Invoke-CsPoolFailback -PoolFQDN <Pool1 FQDN> -Verbose

<span data-ttu-id="535b7-110">Nenhuma outra etapa é necessária.</span><span class="sxs-lookup"><span data-stu-id="535b7-110">No other steps are necessary.</span></span> <span data-ttu-id="535b7-111">Se você tiver reprovado o servidor central de gerenciamento, poderá deixá-lo no Pool2.</span><span class="sxs-lookup"><span data-stu-id="535b7-111">If you failed over the Central Management Server, you can leave it in Pool2.</span></span>

<span data-ttu-id="535b7-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="535b7-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

