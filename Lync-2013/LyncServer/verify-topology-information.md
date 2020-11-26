---
title: Verificar informações de topologia
description: Verifique as informações da topologia.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify topology information
ms:assetid: aa4c424e-f87c-4be6-8df6-a0cd193b11fc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205151(v=OCS.15)
ms:contentKeyID: 48185046
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2ed41cd95fffdca629e710dcf443631d0c74c69e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440110"
---
# <a name="verify-topology-information"></a><span data-ttu-id="8f9c7-103">Verificar informações de topologia</span><span class="sxs-lookup"><span data-stu-id="8f9c7-103">Verify topology information</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8f9c7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8f9c7-104">

<span> </span></span></span>

<span data-ttu-id="8f9c7-105">_**Tópico da última modificação:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="8f9c7-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="8f9c7-106">A primeira etapa na verificação da mesclagem concluída com êxito é exibir as informações de topologia do Office Communications Server 2007 R2 que você mesclou com o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-106">The first step in verifying the merge completed successfully is to view the Office Communications Server 2007 R2 topology information that you merged with Lync Server 2013.</span></span> <span data-ttu-id="8f9c7-107">No construtor de topologias, o nó **BackCompatSite** exibe o nome de domínio totalmente qualificado (FQDN) de cada pool e servidor do Office Communications Server 2007 R2 que você mesclou.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-107">In Topology Builder, the **BackCompatSite** node displays the fully qualified domain name (FQDN) of each Office Communications Server 2007 R2 pool and server that you merged.</span></span>

<div>

## <a name="to-view-backcompatsite-in-topology-builder"></a><span data-ttu-id="8f9c7-108">Para ver BackCompatSite no construtor de topologias</span><span class="sxs-lookup"><span data-stu-id="8f9c7-108">To view BackCompatSite in Topology Builder</span></span>

1.  <span data-ttu-id="8f9c7-109">No ambiente do Office Communications Server 2007 R2, abra a ferramenta administrativa do Office Communications Server 2007 R2 e anote os FQDNs dos pools e servidores herdados.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-109">In your Office Communications Server 2007 R2 environment, open the Office Communications Server 2007 R2 administrative tool and note the FQDNs of the legacy pools and servers.</span></span>

2.  <span data-ttu-id="8f9c7-110">No ambiente do Lync Server 2013, abra o construtor de topologias e, em seguida, expanda o nó **BackCompatSite** .</span><span class="sxs-lookup"><span data-stu-id="8f9c7-110">In your Lync Server 2013 environment, open Topology Builder and then expand the **BackCompatSite** node.</span></span>

3.  <span data-ttu-id="8f9c7-111">Verifique se os FQDNs dos pools e servidores que você mesclaram são exibidos.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-111">Verify that the FQDNs for the pools and servers that you merge are displayed.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8f9c7-112">Você não vê nenhuma informação no <STRONG>BackCompatSite</STRONG> para funções de servidor que estão posicionadas em um servidor front-end ou servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-112">You do not see any information in <STRONG>BackCompatSite</STRONG> for server roles that are collocated on a Front End Server or Standard Edition server.</span></span> <span data-ttu-id="8f9c7-113">Somente as funções de servidor que são necessárias para interoperabilidade entre o Office Communications Server 2007 R2 e o Lync Server 2013 são mostradas.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-113">Only server roles that are required for interoperability between Office Communications Server 2007 R2 and Lync Server 2013 are shown.</span></span>

    
    </div>

<span data-ttu-id="8f9c7-114">![Caixa de diálogo BackCompatSite do construtor de topologia](images/JJ205243.62751c76-f018-4c6d-bb48-c61ef8974d31(OCS.15).jpg "Caixa de diálogo BackCompatSite do construtor de topologia")</span><span class="sxs-lookup"><span data-stu-id="8f9c7-114">![Topology Builder BackCompatSite dialog box](images/JJ205243.62751c76-f018-4c6d-bb48-c61ef8974d31(OCS.15).jpg "Topology Builder BackCompatSite dialog box")</span></span>

<span data-ttu-id="8f9c7-115">Você também pode usar o painel de controle do Lync Server 2013 para exibir a topologia mesclada.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-115">You can also use Lync Server 2013 Control Panel to view your merged topology.</span></span> <span data-ttu-id="8f9c7-116">No painel de controle do Lync Server 2013, você pode ver cada FQDN do servidor, FQDN do pool e nome do site para a sua topologia mesclada.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-116">In Lync Server 2013 Control Panel, you can see each server FQDN, pool FQDN, and site name for your merged topology.</span></span> <span data-ttu-id="8f9c7-117">Os servidores mesclados têm um nome de **site** de **BackCompatSite**.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-117">Merged servers have a **Site** name of **BackCompatSite**.</span></span>

</div>

<div>

## <a name="to-view-the-merged-topology-in-lync-server-2013-control-panel"></a><span data-ttu-id="8f9c7-118">Para exibir a topologia mesclada no painel de controle do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8f9c7-118">To view the merged topology in Lync Server 2013 Control Panel</span></span>

1.  <span data-ttu-id="8f9c7-119">Abra o painel de controle do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-119">Open Lync Server 2013 Control Panel.</span></span>

2.  <span data-ttu-id="8f9c7-120">Clique em **topologia**.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-120">Click **Topology**.</span></span>

3.  <span data-ttu-id="8f9c7-121">Na guia **status** , verifique se servidores e pools que você mesclou são exibidos procurando **BackCompatSite** na coluna do **site** .</span><span class="sxs-lookup"><span data-stu-id="8f9c7-121">On the **Status** tab, verify that servers and pools you merged appear by looking for **BackCompatSite** in the **Site** column.</span></span>

<span data-ttu-id="8f9c7-122">![Painel de controle do Lync Server mostrando topologia mesclada](images/JJ205151.f986ddd4-2040-454d-9389-7f6154b59cc9(OCS.15).jpg "Painel de controle do Lync Server mostrando topologia mesclada")</span><span class="sxs-lookup"><span data-stu-id="8f9c7-122">![Lync Server Control Panel showing merged topology](images/JJ205151.f986ddd4-2040-454d-9389-7f6154b59cc9(OCS.15).jpg "Lync Server Control Panel showing merged topology")</span></span>

<span data-ttu-id="8f9c7-123">Para ver mais detalhes sobre um pool mesclado, use o cmdlet **Get-CsPool** .</span><span class="sxs-lookup"><span data-stu-id="8f9c7-123">To see more detail about a merged pool, use the **Get-CsPool** cmdlet.</span></span> <span data-ttu-id="8f9c7-124">Além das informações que estão disponíveis no painel de controle Topology Builder e Lync Server 2013, esse cmdlet exibe os serviços executados no pool do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-124">In addition to the information that is available in Topology Builder and Lync Server 2013 Control Panel, this cmdlet displays the services that run on the Lync Server 2013 pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8f9c7-125">Quando você publica a topologia depois de executar o assistente de mesclagem no construtor de topologias, os diretórios de conferências são mesclados ao Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-125">When you publish the topology after running the Merge wizard in Topology Builder, conference directories are merged to Lync Server 2013.</span></span> <span data-ttu-id="8f9c7-126">Os diretórios de conferência podem ser verificados executando o cmdlet <STRONG>Get-CsConferenceDirectory</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="8f9c7-126">Conference directories can be verified by running the <STRONG>Get-CsConferenceDirectory</STRONG> cmdlet.</span></span>



</div>

</div>

<div>

## <a name="to-view-services-on-a-merged-pool"></a><span data-ttu-id="8f9c7-127">Para exibir serviços em um pool mesclado</span><span class="sxs-lookup"><span data-stu-id="8f9c7-127">To view services on a merged pool</span></span>

1.  <span data-ttu-id="8f9c7-128">Abra o Shell de gerenciamento do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-128">Open the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="8f9c7-129">Na linha de comando, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8f9c7-129">At the command line, type the following:</span></span>
    
        Get-CsPool [-Identity <FQDN of the pool>]
    
    <span data-ttu-id="8f9c7-130">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8f9c7-130">For example:</span></span>
    
        Get-CsPool -Identity pool02.contoso.net

</div>

<div>

## <a name="to-verify-conference-directories-merged"></a><span data-ttu-id="8f9c7-131">Para verificar se as pastas de conferência foram mescladas</span><span class="sxs-lookup"><span data-stu-id="8f9c7-131">To verify conference directories merged</span></span>

1.  <span data-ttu-id="8f9c7-132">Abra o Shell de gerenciamento do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-132">Open the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="8f9c7-133">Na linha de comando, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8f9c7-133">At the command line, type the following:</span></span>
    
        Get-CsConferenceDirectory

3.  <span data-ttu-id="8f9c7-134">Verifique se todos os diretórios de conferência do pool ou do servidor que você está mesclando estão agora no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-134">Verify that all the conference directories for the pool or server you are merging are now in Lync Server 2013.</span></span>

<span data-ttu-id="8f9c7-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8f9c7-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

