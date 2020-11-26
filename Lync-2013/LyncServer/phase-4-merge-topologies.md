---
title: 'Fase 4: topologias de mesclagem'
description: 'Fase 4: topologias de mesclagem.'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: 'Phase 4: Merge topologies'
ms:assetid: 81eb5bb2-1fd7-4611-a2aa-eb2393c8abc9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205044(v=OCS.15)
ms:contentKeyID: 48184668
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 421cb83a57979ae677d4db76d2c8c3535f8e0dcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438761"
---
# <a name="phase-4-merge-topologies"></a><span data-ttu-id="bde26-103">Fase 4: topologias de mesclagem</span><span class="sxs-lookup"><span data-stu-id="bde26-103">Phase 4: Merge topologies</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bde26-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bde26-104">

<span> </span></span></span>

<span data-ttu-id="bde26-105">_**Tópico da última modificação:** 2012-03-29_</span><span class="sxs-lookup"><span data-stu-id="bde26-105">_**Topic Last Modified:** 2012-03-29_</span></span>

<span data-ttu-id="bde26-106">Os tópicos a seguir descrevem as etapas necessárias para mesclar os pools do Microsoft Office Communications Server 2007 R2 para os pools do Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bde26-106">The following topics outline the steps needed to merge your Microsoft Office Communications Server 2007 R2 pools to Microsoft Lync Server 2013 pools.</span></span> <span data-ttu-id="bde26-107">Primeiro, use o assistente de mesclagem do construtor de topologias para mesclar as informações da topologia.</span><span class="sxs-lookup"><span data-stu-id="bde26-107">First, you use the Topology Builder Merge wizard to merge topology information.</span></span> <span data-ttu-id="bde26-108">Esta ferramenta coleta informações sobre o ambiente do Office Communications Server 2007 R2, incluindo informações do servidor de borda, e publica essas informações em um banco de dados compartilhado com o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bde26-108">This tool collects information about your Office Communications Server 2007 R2 environment, including Edge Server information, and publishes that information to a database shared with Lync Server 2013.</span></span> <span data-ttu-id="bde26-109">Após a publicação da topologia mesclada, o construtor de topologias é usado para exibir as informações de topologia do Office Communications Server 2007 R2 e informações sobre a topologia recém implantada do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bde26-109">After you publish the merged topology, Topology Builder is used to view the Office Communications Server 2007 R2 topology information and information about the newly deployed Lync Server 2013 topology.</span></span> <span data-ttu-id="bde26-110">Por fim, você usa cmdlets do Shell de gerenciamento do Lync Server para importar políticas e definições de configuração.</span><span class="sxs-lookup"><span data-stu-id="bde26-110">Finally, you use Lync Server Management Shell cmdlets to import policies and configuration settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="bde26-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="bde26-111">In This Section</span></span>

  - [<span data-ttu-id="bde26-112">Instalar o pacote de compatibilidade com versões anteriores do WMI</span><span class="sxs-lookup"><span data-stu-id="bde26-112">Install WMI Backward Compatibility package</span></span>](install-wmi-backward-compatibility-package.md)

  - [<span data-ttu-id="bde26-113">Mesclar usando o assistente de mesclagem do construtor de topologia</span><span class="sxs-lookup"><span data-stu-id="bde26-113">Merge using Topology Builder Merge wizard</span></span>](merge-using-topology-builder-merge-wizard.md)

  - [<span data-ttu-id="bde26-114">Importar políticas e configurações</span><span class="sxs-lookup"><span data-stu-id="bde26-114">Import policies and settings</span></span>](import-policies-and-settings.md)

  - [<span data-ttu-id="bde26-115">Verificar informações de topologia</span><span class="sxs-lookup"><span data-stu-id="bde26-115">Verify topology information</span></span>](verify-topology-information.md)

<span data-ttu-id="bde26-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bde26-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

