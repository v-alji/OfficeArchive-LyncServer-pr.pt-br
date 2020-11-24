---
title: Conectar pool piloto aos Servidores de Borda herdados
description: Conecte o pool piloto a servidores de borda herdados.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Connect pilot pool to legacy Edge Servers
ms:assetid: c3b67220-5705-47f6-852e-415204f3626c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721875(v=OCS.15)
ms:contentKeyID: 49733808
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ede2256efabf561be6b3f99543437087cb5c3890
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389999"
---
# <a name="connect-pilot-pool-to-legacy-edge-servers"></a><span data-ttu-id="aac34-103">Conectar pool piloto aos Servidores de Borda herdados</span><span class="sxs-lookup"><span data-stu-id="aac34-103">Connect pilot pool to legacy Edge Servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aac34-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aac34-104">

<span> </span></span></span>

<span data-ttu-id="aac34-105">_**Tópico da última modificação:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="aac34-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="aac34-106">Após implantar o Lync Server 2013, você precisa configurar uma rota de Federação para seu site.</span><span class="sxs-lookup"><span data-stu-id="aac34-106">After deploying Lync Server 2013, you need to configure a federation route for your site.</span></span> <span data-ttu-id="aac34-107">Para usar a rota federada que está sendo usada pelo Lync Server 2010, o Lync Server 2013 deve ser configurado para usar essa rota.</span><span class="sxs-lookup"><span data-stu-id="aac34-107">In order to use the federated route that is being used by Lync Server 2010, Lync Server 2013 must be configured to use this route.</span></span>

<span data-ttu-id="aac34-108">Para habilitar o site do Lync Server 2013 para usar o diretor e o servidor de borda da implantação do Lync Server 2010, use o construtor de topologias para associar o pool de bordas herdado.</span><span class="sxs-lookup"><span data-stu-id="aac34-108">To enable the Lync Server 2013 site to use the Director and Edge Server of the Lync Server 2010 deployment, use Topology Builder to associate the legacy Edge pool.</span></span>

<div>

## <a name="to-associate-the-legacy-edge-pool-by-using-topology-builder"></a><span data-ttu-id="aac34-109">Para associar o pool de bordas herdado usando o construtor de topologias</span><span class="sxs-lookup"><span data-stu-id="aac34-109">To associate the legacy Edge pool by using Topology Builder</span></span>

1.  <span data-ttu-id="aac34-110">Abrir o **Construtor de topologias**.</span><span class="sxs-lookup"><span data-stu-id="aac34-110">Open **Topology Builder**.</span></span>

2.  <span data-ttu-id="aac34-111">Selecione seu site, que está diretamente abaixo do nó do **Lync Server** .</span><span class="sxs-lookup"><span data-stu-id="aac34-111">Select your site, which is directly below the **Lync Server** node.</span></span>

3.  <span data-ttu-id="aac34-112">No menu **ações** , clique em **Editar propriedades**.</span><span class="sxs-lookup"><span data-stu-id="aac34-112">On the **Actions** menu, click **Edit Properties**.</span></span>

4.  <span data-ttu-id="aac34-113">No painel esquerdo, selecione **roteiro de Federação**.</span><span class="sxs-lookup"><span data-stu-id="aac34-113">In the left pane, select **Federation route**.</span></span>

5.  <span data-ttu-id="aac34-114">Em **atribuição de rota de Federação do site**, selecione **habilitar Federação SIP** e, em seguida, selecione o diretor do Lync Server 2010 ou o servidor de borda do Lync Server 2010, se nenhum diretor estiver listado.</span><span class="sxs-lookup"><span data-stu-id="aac34-114">Under **Site federation route assignment**, select **Enable SIP federation**, and then select the Lync Server 2010 Director, or the Lync Server 2010 Edge Server if no Director is listed.</span></span>
    
    <span data-ttu-id="aac34-115">![Editar propriedades, página de roteiro de Federação](images/JJ721875.5f1d04c3-c724-426d-b27d-3fe89c6c5cfb(OCS.15).jpg "Editar propriedades, página de roteiro de Federação")</span><span class="sxs-lookup"><span data-stu-id="aac34-115">![Edit Properties, Federation route page](images/JJ721875.5f1d04c3-c724-426d-b27d-3fe89c6c5cfb(OCS.15).jpg "Edit Properties, Federation route page")</span></span>  

6.  <span data-ttu-id="aac34-116">Clique em **OK** para fechar a página **Editar propriedades** .</span><span class="sxs-lookup"><span data-stu-id="aac34-116">Click **OK** to close the **Edit Properties** page.</span></span>

7.  <span data-ttu-id="aac34-117">No construtor de topologias, no nó do Lync Server 2013, navegue até os pools do **servidor Standard Edition** ou do **front-end da edição Enterprise**, clique com o botão direito do mouse no pool e, em seguida, clique em **Editar propriedades**.</span><span class="sxs-lookup"><span data-stu-id="aac34-117">In Topology Builder, under the Lync Server 2013 node, navigate to the **Standard Edition server** or **Enterprise Edition Front End pools**, right-click the pool, and then click **Edit Properties**.</span></span>

8.  <span data-ttu-id="aac34-118">Em **associações**, marque a caixa de seleção ao lado de **associar o pool de bordas (para componentes de mídia)**.</span><span class="sxs-lookup"><span data-stu-id="aac34-118">Under **Associations**, select the check box next to **Associate Edge pool (for media components)**.</span></span>

9.  <span data-ttu-id="aac34-119">Na lista, selecione o servidor de borda herdado.</span><span class="sxs-lookup"><span data-stu-id="aac34-119">From the list, select the legacy Edge Server.</span></span>
    
    <span data-ttu-id="aac34-120">![Caixa de diálogo Editar propriedades, selecionando a borda herdada](images/JJ721875.feae8156-540e-4804-bb0a-2b5736ec2900(OCS.15).jpg "Caixa de diálogo Editar propriedades, selecionando a borda herdada")</span><span class="sxs-lookup"><span data-stu-id="aac34-120">![Edit Properties dialog, selecting the legacy Edge](images/JJ721875.feae8156-540e-4804-bb0a-2b5736ec2900(OCS.15).jpg "Edit Properties dialog, selecting the legacy Edge")</span></span>  

10. <span data-ttu-id="aac34-121">Clique em **OK** para fechar a página **Editar propriedades** .</span><span class="sxs-lookup"><span data-stu-id="aac34-121">Click **OK** to close the **Edit Properties** page.</span></span>

11. <span data-ttu-id="aac34-122">No **Construtor de topologias**, selecione o nó mais alto, **Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="aac34-122">In **Topology Builder**, select the top-most node, **Lync Server**.</span></span>

12. <span data-ttu-id="aac34-123">No menu **ação** , clique em **publicar topologia** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="aac34-123">From the **Action** menu, click **Publish Topology**, and then click **Next**.</span></span>

13. <span data-ttu-id="aac34-124">Quando o **Assistente de publicação** for concluído, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="aac34-124">When the **Publishing wizard** completes, click **Finish**.</span></span>

<span data-ttu-id="aac34-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aac34-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

