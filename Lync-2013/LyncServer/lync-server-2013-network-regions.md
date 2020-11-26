---
title: 'Lync Server 2013: regiões de rede'
description: 'Lync Server 2013: regiões de rede.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Network regions
ms:assetid: 1818e9d2-bbb7-420a-93ea-4c3da3a55ad3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687979(v=OCS.15)
ms:contentKeyID: 49733567
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3506f3c543c0728f27bd091b9cd63991c4633da7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425154"
---
# <a name="network-regions-in-lync-server-2013"></a><span data-ttu-id="241fe-103">Regiões de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="241fe-103">Network regions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="241fe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="241fe-104">

<span> </span></span></span>

<span data-ttu-id="241fe-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="241fe-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="241fe-106">*Regiões de rede* são os hubs de rede ou backbones usados na configuração de controle de admissão de chamadas, E9-1-1 e bypass de mídia.</span><span class="sxs-lookup"><span data-stu-id="241fe-106">*Network regions* are the network hubs or backbones used in the configuration of call admission control, E9-1-1, and media bypass.</span></span> <span data-ttu-id="241fe-107">Use os procedimentos a seguir para exibir, criar ou modificar regiões de rede.</span><span class="sxs-lookup"><span data-stu-id="241fe-107">Use the following procedures to view, create, or modify network regions.</span></span> <span data-ttu-id="241fe-108">Por exemplo, se você já tiver criado regiões de rede para um recurso de voz, não precisará criar novas regiões de rede; outros recursos avançados do Enterprise Voice usarão essas mesmas regiões de rede.</span><span class="sxs-lookup"><span data-stu-id="241fe-108">For example, if you have already created network regions for one Voice feature, you do not need to create new network regions; other advanced Enterprise Voice features will use those same network regions.</span></span> <span data-ttu-id="241fe-109">No entanto, pode ser necessário modificar uma definição de região da rede existente para aplicar as configurações específicas do recurso.</span><span class="sxs-lookup"><span data-stu-id="241fe-109">You may, however, need to modify an existing network region definition to apply feature-specific settings.</span></span> <span data-ttu-id="241fe-110">Por exemplo, se você cria regiões da rede para o E9-1-1 (que não exige um local central associado) e depois implanta o serviço de controle de admissão de chamadas, precisará modificar as definições de região da rede para especificar um local central.</span><span class="sxs-lookup"><span data-stu-id="241fe-110">For example, if you have created network regions for E9-1-1 (which do not require an associated central site) and you then deploy call admission control, you need to modify the network region definitions to specify a central site.</span></span> <span data-ttu-id="241fe-111">Para obter detalhes, consulte [configurar regiões de rede para o CAC no Lync Server 2013](lync-server-2013-configure-network-regions-for-cac.md).</span><span class="sxs-lookup"><span data-stu-id="241fe-111">For details, see [Configure network regions for CAC in Lync Server 2013](lync-server-2013-configure-network-regions-for-cac.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="241fe-112">Qualquer requisito específico de recurso para definições de região de rede está documentado nos tópicos de implantação do recurso.</span><span class="sxs-lookup"><span data-stu-id="241fe-112">Any feature-specific requirements for network region definitions are documented in the Deployment topics for the feature.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="241fe-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="241fe-113">In This Section</span></span>

  - [<span data-ttu-id="241fe-114">Exibir informações de região de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="241fe-114">Viewing network region information in Lync Server 2013</span></span>](lync-server-2013-viewing-network-region-information.md)

  - [<span data-ttu-id="241fe-115">Criando ou modificando regiões de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="241fe-115">Creating or modifying network regions in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-regions.md)

  - [<span data-ttu-id="241fe-116">Excluindo regiões de rede existentes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="241fe-116">Deleting existing network regions in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-regions.md)

</div>

<div>

## <a name="reference"></a><span data-ttu-id="241fe-117">Referência</span><span class="sxs-lookup"><span data-stu-id="241fe-117">Reference</span></span>

[<span data-ttu-id="241fe-118">Implantação de recursos avançados do Enterprise Voice no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="241fe-118">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)

<span data-ttu-id="241fe-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="241fe-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

