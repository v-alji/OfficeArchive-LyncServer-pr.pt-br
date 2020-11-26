---
title: 'Lync Server 2013: Restaurando conteúdos de conferência usando o Serviço de Backup'
description: 'Lync Server 2013: restaurando o conteúdo da conferência usando o serviço de backup.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring conference contents using the Backup Service
ms:assetid: 3e0f18ec-7319-4c07-a59b-2938e7787bc9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688030(v=OCS.15)
ms:contentKeyID: 49733620
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3a0037af711948c008e74c5444373ed995f0e6e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442541"
---
# <a name="restoring-conference-contents-using-the-backup-service-in-lync-server-2013"></a><span data-ttu-id="efdcf-103">Restaurando conteúdos de conferência usando o Serviço de Backup no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="efdcf-103">Restoring conference contents using the Backup Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="efdcf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="efdcf-104">

<span> </span></span></span>

<span data-ttu-id="efdcf-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="efdcf-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="efdcf-106">Se as informações de conferência armazenadas no repositório de arquivos de um pool de front-ends ficarem indisponíveis.</span><span class="sxs-lookup"><span data-stu-id="efdcf-106">If the conference information stored in the file store of a Front End pool becomes unavailable.</span></span> <span data-ttu-id="efdcf-107">Você deve restaurar essas informações para que os usuários hospedados no pool mantenham seus dados de conferência.</span><span class="sxs-lookup"><span data-stu-id="efdcf-107">you must restore this information so that users homed on the pool retain their conference data.</span></span> <span data-ttu-id="efdcf-108">Se o pool de front-ends que perdeu dados de conferências estiver emparelhado com outro pool de front-end, você pode usar o serviço de backup para restaurar os dados.</span><span class="sxs-lookup"><span data-stu-id="efdcf-108">If the Front End pool which has lost conference data is paired with another Front End pool, you can use the Backup Service to restore the data.</span></span>

<span data-ttu-id="efdcf-109">Você também deve realizar essa tarefa se um pool inteiro tiver falhado e tiver que fazer failover de seus usuários para um pool de backup.</span><span class="sxs-lookup"><span data-stu-id="efdcf-109">You must also perform this task if an entire pool has failed and you have to fail over its users to a backup pool.</span></span> <span data-ttu-id="efdcf-110">Quando esses usuários falham novamente em seu pool original, você deve usar esse procedimento para copiar o conteúdo de conferência de volta para o pool original também.</span><span class="sxs-lookup"><span data-stu-id="efdcf-110">When these users are failed back over to their original pool, you must use this procedure to copy their conference content back to their original pool as well.</span></span>

<span data-ttu-id="efdcf-111">Suponha que o Pool1 está emparelhado com Pool2, e os dados de conferência no Pool1 são perdidos.</span><span class="sxs-lookup"><span data-stu-id="efdcf-111">Assume that Pool1 is paired with Pool2, and the conference data in Pool1 is lost.</span></span> <span data-ttu-id="efdcf-112">Você pode usar o cmdlet a seguir para invocar o serviço de backup para restaurar o conteúdo:</span><span class="sxs-lookup"><span data-stu-id="efdcf-112">You can use the following cmdlet to invoke the Backup Service to restore the contents:</span></span>

    Invoke-CsBackupServiceSync -PoolFqdn <Pool2 FQDN> -BackupModule ConfServices.DataConf

<span data-ttu-id="efdcf-113">A restauração do conteúdo da conferência pode levar algum tempo, dependendo do tamanho.</span><span class="sxs-lookup"><span data-stu-id="efdcf-113">Restoring the conference contents may take some time, depending on their size.</span></span> <span data-ttu-id="efdcf-114">Você pode usar o cmdlet a seguir para verificar o status do processo:</span><span class="sxs-lookup"><span data-stu-id="efdcf-114">You can use the following cmdlet to check the process status:</span></span>

    Get-CsBackupServiceStatus -PoolFqdn <Pool2 FQDN> -BackupModule ConfServices.DataConf

<span data-ttu-id="efdcf-115">O processo é feito quando esse cmdlet retorna um valor de estado Steady para o módulo de conferência de dados.</span><span class="sxs-lookup"><span data-stu-id="efdcf-115">The process is done when this cmdlet returns a value of Steady State for the data conference module.</span></span>

<span data-ttu-id="efdcf-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="efdcf-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

