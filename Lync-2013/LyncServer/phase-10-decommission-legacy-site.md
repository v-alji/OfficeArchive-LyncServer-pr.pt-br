---
title: 'Fase 10: descomissionar site herdado'
description: 'Fase 10: descomissionar site herdado.'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: 'Phase 10: Decommission legacy site'
ms:assetid: d591a310-3b5c-4092-b19e-0349616e40df
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205300(v=OCS.15)
ms:contentKeyID: 48185540
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9692301a1da38cfd69780ce2524f00dd428454e5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443269"
---
# <a name="phase-10-decommission-legacy-site"></a><span data-ttu-id="16709-103">Fase 10: descomissionar site herdado</span><span class="sxs-lookup"><span data-stu-id="16709-103">Phase 10: Decommission legacy site</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="16709-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="16709-104">

<span> </span></span></span>

<span data-ttu-id="16709-105">_**Tópico da última modificação:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="16709-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="16709-106">Os tópicos a seguir fornecem orientação sobre como descomissionar pools e para desativar e remover servidores e pools de uma implantação herdada do Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="16709-106">The following topics provide guidance in decommissioning pools, and deactivating and removing servers and pools from a legacy deployment of Office Communications Server 2007 R2.</span></span> <span data-ttu-id="16709-107">Nem todos os procedimentos listados nesta seção são necessários.</span><span class="sxs-lookup"><span data-stu-id="16709-107">Not all of the procedures listed in this section are required.</span></span> <span data-ttu-id="16709-108">Leia as informações em cada um desses tópicos para determinar o procedimento de descomissionamento a ser usado.</span><span class="sxs-lookup"><span data-stu-id="16709-108">Read the information in each of these topics to determine which decommissioning procedure to use.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="16709-109">Se você importou pastas de conferência para conferência discada para o Lync Server 2013, é importante migrar a propriedade do diretório de conferências para o Lync Server 2013 antes de começar a descomissionar seus pools.</span><span class="sxs-lookup"><span data-stu-id="16709-109">If you imported conference directories for dial-in conferencing to Lync Server 2013, it is important to transition conference directory ownership to Lync Server 2013 before you begin to decommission your pools.</span></span> <span data-ttu-id="16709-110">Se você encerrar um pool sem primeiro fazer a transição da Propriedade do diretório de conferência, o recurso de discagem para todas as reuniões migradas deixará de funcionar.</span><span class="sxs-lookup"><span data-stu-id="16709-110">If you decommission a pool without first transitioning conference directory ownership, the dial-in feature for all migrated meetings will no longer work.</span></span> <span data-ttu-id="16709-111">Você deve executar a etapa para fazer a transição da propriedade uma vez para cada diretório de conferência em seu pool herdado.</span><span class="sxs-lookup"><span data-stu-id="16709-111">You must perform the step to transition ownership once for each conference directory in your legacy pool.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="16709-112">Para obter informações sobre como migrar e atualizar aplicativos da API gerenciada do Microsoft Unified Communication (UCMA), antes de descomissionar o seu ambiente herdado, consulte <A href="https://go.microsoft.com/fwlink/p/?linkid=269555">https://go.microsoft.com/fwlink/p/?LinkId=269555</A></span><span class="sxs-lookup"><span data-stu-id="16709-112">For information on migrating and upgrading Microsoft Unified Communications Managed API (UCMA) applications, prior to decommissioning your legacy environment, see <A href="https://go.microsoft.com/fwlink/p/?linkid=269555">https://go.microsoft.com/fwlink/p/?LinkId=269555</A></span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="16709-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="16709-113">In This Section</span></span>

  - [<span data-ttu-id="16709-114">Mover diretórios de conferências</span><span class="sxs-lookup"><span data-stu-id="16709-114">Move conference directories</span></span>](move-conference-directories.md)

  - [<span data-ttu-id="16709-115">Atualizar registros de DNS SRV</span><span class="sxs-lookup"><span data-stu-id="16709-115">Update DNS SRV records</span></span>](update-dns-srv-records.md)

  - [<span data-ttu-id="16709-116">Descomissionar servidores e pools</span><span class="sxs-lookup"><span data-stu-id="16709-116">Decommissioning servers and pools</span></span>](decommissioning-servers-and-pools.md)

  - [<span data-ttu-id="16709-117">Remover BackCompatSite</span><span class="sxs-lookup"><span data-stu-id="16709-117">Remove BackCompatSite</span></span>](remove-backcompatsite.md)

<span data-ttu-id="16709-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="16709-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

