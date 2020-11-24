---
title: Autorizar conexão com o servidor de borda do Office Communications Server 2007 R2
description: Autorize a conexão com o servidor do Office Communications Server 2007 R2 Edge.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Authorize connection to Office Communications Server 2007 R2 Edge Server
ms:assetid: 14f6798a-28d6-4b3d-8734-942192e1bbf5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204702(v=OCS.15)
ms:contentKeyID: 48183493
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: de8dadb2c476c892f4ffd548ce176d12d3b1a1cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389922"
---
# <a name="authorize-connection-to-office-communications-server-2007-r2-edge-server"></a><span data-ttu-id="6f561-103">Autorizar conexão com o servidor de borda do Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="6f561-103">Authorize connection to Office Communications Server 2007 R2 Edge Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f561-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f561-104">

<span> </span></span></span>

<span data-ttu-id="6f561-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="6f561-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="6f561-106">Para cada servidor front-end do Lync Server 2013 ou Standard Edition no pool piloto, você deve atualizar a lista de servidores internos que têm autorização para se conectar ao servidor do Office Communications Server 2007 R2 Edge Server.</span><span class="sxs-lookup"><span data-stu-id="6f561-106">For each Lync Server 2013 Front End Server or Standard Edition server in your pilot pool, you must update the list of internal servers that are authorized to connect to the Office Communications Server 2007 R2 Edge Server.</span></span> <span data-ttu-id="6f561-107">Sem essas atualizações, a conferência de áudio/visual (A/V) externa para usuários que ingressarem usando o servidor de borda herdada não funcionará.</span><span class="sxs-lookup"><span data-stu-id="6f561-107">Without these updates, external audio/visual (A/V) conferencing for users joining by using the legacy Edge Server will not work.</span></span>

<div>

## <a name="to-authorize-connection-to-office-communications-server-2007-r2-edge-server"></a><span data-ttu-id="6f561-108">Para autorizar a conexão com o servidor de borda do Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="6f561-108">To Authorize Connection to Office Communications Server 2007 R2 Edge Server</span></span>

1.  <span data-ttu-id="6f561-109">No servidor do Office Communications Server 2007 R2 Edge, a partir do grupo **Ferramentas administrativas** , abra o snap-in **Gerenciamento do computador** .</span><span class="sxs-lookup"><span data-stu-id="6f561-109">From the Office Communications Server 2007 R2 Edge Server, from the **Administrative Tools** group, open the **Computer Management** snap-in.</span></span>

2.  <span data-ttu-id="6f561-110">Na árvore de console, expanda **serviços e aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="6f561-110">In the console tree, expand **Services and Applications**.</span></span>

3.  <span data-ttu-id="6f561-111">Clique com o botão direito do mouse em **Office Communications Server 2007 R2** e, em seguida, clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="6f561-111">Right-click **Office Communications Server 2007 R2**, and then click **Properties**.</span></span>

4.  <span data-ttu-id="6f561-112">Clique na guia **interno** .</span><span class="sxs-lookup"><span data-stu-id="6f561-112">Click the **Internal** tab.</span></span>

5.  <span data-ttu-id="6f561-113">Em **Adicionar servidor**, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="6f561-113">Under **Add Server**, click **Add**.</span></span>

6.  <span data-ttu-id="6f561-114">Na caixa de diálogo **Adicionar o Office Communications Server** , insira as informações apropriadas:</span><span class="sxs-lookup"><span data-stu-id="6f561-114">In the **Add Office Communications Server** dialog box, enter the appropriate information:</span></span>
    
      - <span data-ttu-id="6f561-115">Especifique o nome de domínio totalmente qualificado (FQDN) de cada servidor front-end do Lync Server 2013 ou do servidor Standard Edition e do Lync Server 2013 pool.</span><span class="sxs-lookup"><span data-stu-id="6f561-115">Specify the fully qualified domain name (FQDN) of each Lync Server 2013 Front End Server or Standard Edition server, and Lync Server 2013 pool.</span></span>
    
      - <span data-ttu-id="6f561-116">Especifique o FQDN do diretor do Lync Server 2013 se você configurou uma rota estática no pool que especifica o próximo nó do computador pelo seu FQDN.</span><span class="sxs-lookup"><span data-stu-id="6f561-116">Specify the FQDN of the Lync Server 2013 Director if you configured a static route on the pool that specifies the next hop computer by its FQDN.</span></span>

7.  <span data-ttu-id="6f561-117">Depois de adicionar uma entrada para cada Lync Server 2013, servidor front-end, servidor Standard Edition, pool e diretor, clique em **aplicar** e, em seguida, clique em **OK** para fechar a página Propriedades.</span><span class="sxs-lookup"><span data-stu-id="6f561-117">After you have added an entry for each Lync Server 2013, Front End Server, Standard Edition server, pool, and Director, click **Apply** and then click **OK** to close the Properties page.</span></span>

<span data-ttu-id="6f561-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f561-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

