---
title: 'Lync Server 2013: solução de problemas e principais indicadores de integridade'
description: 'Lync Server 2013: solução de problemas e principais indicadores de integridade.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Troubleshooting and Key Health Indicators
ms:assetid: 14ec9e21-aa2b-4d65-9be4-ef2adfbe9a8b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720322(v=OCS.15)
ms:contentKeyID: 63969585
ms.date: 05/18/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8fdb214d4ce8472800272a05e81b0402d3bf820e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436213"
---
# <a name="troubleshooting-and-key-health-indicators-in-lync-server-2013"></a><span data-ttu-id="6449c-103">Solução de problemas e principais indicadores de integridade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6449c-103">Troubleshooting and Key Health Indicators in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6449c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6449c-104">

<span> </span></span></span>

<span data-ttu-id="6449c-105">_**Tópico da última modificação:** 2015-05-18_</span><span class="sxs-lookup"><span data-stu-id="6449c-105">_**Topic Last Modified:** 2015-05-18_</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6449c-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6449c-106">In This Section</span></span>

<span data-ttu-id="6449c-107">Para atender aos SLAs de arquitetura de referência e garantir uma transição tranqüila para nossas equipes de suporte, uma abordagem de solução de problemas comum deve ser definida juntamente com um conjunto obrigatório de ferramentas e abordagens de solução de problemas conforme definido no [Guia de rede](https://go.microsoft.com/fwlink/p/?linkid=390677) do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6449c-107">To meet the Reference Architecture SLAs and to ensure a smooth transition to our support teams, a common troubleshooting approach must be defined together with a required set of troubleshooting tools and approaches as defined in the Lync Server [Networking guide](https://go.microsoft.com/fwlink/p/?linkid=390677) .</span></span>

<span data-ttu-id="6449c-108">É altamente recomendável que o System Center Operations Manager seja usado para monitorar a integridade do sistema do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6449c-108">We strongly recommend that System Center Operations Manager be used to monitor the health of the Lync Server 2013 system.</span></span> <span data-ttu-id="6449c-109">Além disso, confira a discussão sobre o KHIs no guia de [rede](https://go.microsoft.com/fwlink/p/?linkid=390677) do Lync Server 2013 e a planilha do Excel para usar com o Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="6449c-109">Also, refer to the discussion of KHIs in the Lync Server 2013 [Networking guide](https://go.microsoft.com/fwlink/p/?linkid=390677) and the Excel spreadsheet for use with Lync 2013.</span></span>

</div>

<div>

## <a name="reference"></a><span data-ttu-id="6449c-110">Referência</span><span class="sxs-lookup"><span data-stu-id="6449c-110">Reference</span></span>

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="6449c-111">Seções Relacionadas</span><span class="sxs-lookup"><span data-stu-id="6449c-111">Related Sections</span></span>

<span data-ttu-id="6449c-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6449c-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

