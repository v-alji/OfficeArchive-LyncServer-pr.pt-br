---
title: 'Lync Server 2013: excluir links de região de rede'
description: 'Lync Server 2013: excluindo links de região de rede.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting network region links
ms:assetid: 839273cd-d23f-4b38-84e6-d2dc972f49cd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688114(v=OCS.15)
ms:contentKeyID: 49733712
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5a17c1ec64460e0f7cb447597f94aadd7fd2a9ca
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430284"
---
# <a name="deleting-network-region-links-in-lync-server-2013"></a><span data-ttu-id="80441-103">Excluindo links de região de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="80441-103">Deleting network region links in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="80441-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="80441-104">

<span> </span></span></span>

<span data-ttu-id="80441-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="80441-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="80441-106">Você pode configurar links entre duas regiões de rede como parte do controle de admissão de chamadas (CAC).</span><span class="sxs-lookup"><span data-stu-id="80441-106">You can configure links between two network regions as part of call admission control (CAC).</span></span> <span data-ttu-id="80441-107">Regiões dentro de uma rede são vinculadas por meio de conectividade física de rede de longa distância (WAN).</span><span class="sxs-lookup"><span data-stu-id="80441-107">Regions within a network are linked through physical wide area network (WAN) connectivity.</span></span> <span data-ttu-id="80441-108">Você pode usar o painel de controle do Lync Server para excluir um link existente entre duas regiões de rede.</span><span class="sxs-lookup"><span data-stu-id="80441-108">You can use the Lync Server Control Panel to delete an existing link between two network regions.</span></span> <span data-ttu-id="80441-109">Para obter detalhes sobre como criar ou modificar o link de região de rede, consulte [Configurando links de região de rede no Lync Server 2013](lync-server-2013-configuring-network-region-links.md)</span><span class="sxs-lookup"><span data-stu-id="80441-109">For details about creating or modifying network region link, see [Configuring network region links in Lync Server 2013](lync-server-2013-configuring-network-region-links.md)</span></span>

<div>

## <a name="to-delete-a-network-region-link"></a><span data-ttu-id="80441-110">Para excluir um link de região de rede</span><span class="sxs-lookup"><span data-stu-id="80441-110">To delete a network region link</span></span>

1.  <span data-ttu-id="80441-111">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="80441-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="80441-112">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="80441-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="80441-113">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="80441-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="80441-114">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **link de região**.</span><span class="sxs-lookup"><span data-stu-id="80441-114">In the left navigation bar, click **Network Configuration** and then click **Region Link**.</span></span>

4.  <span data-ttu-id="80441-115">Na página **link de região** , clique no link de região que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="80441-115">On the **Region Link** page, click the region link that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="80441-116">Você pode excluir mais de um link de região de cada vez.</span><span class="sxs-lookup"><span data-stu-id="80441-116">You can delete more than one region link at a time.</span></span> <span data-ttu-id="80441-117">Para fazer isso, pressione CTRL e selecione vários links de região enquanto mantém a tecla CTRL pressionada.</span><span class="sxs-lookup"><span data-stu-id="80441-117">To do this, press CTRL and select multiple region links while holding down the CTRL key.</span></span> <span data-ttu-id="80441-118">Ou, para selecionar todos os links de região, clique em <STRONG>selecionar tudo</STRONG> no menu <STRONG>Editar</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="80441-118">Or, to select all region links, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="80441-119">No menu **Editar** , selecione **excluir**.</span><span class="sxs-lookup"><span data-stu-id="80441-119">From the **Edit** menu, select **Delete**.</span></span>

6.  <span data-ttu-id="80441-120">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="80441-120">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="80441-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="80441-121">See Also</span></span>


[<span data-ttu-id="80441-122">Configurar links de região de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="80441-122">Configuring network region links in Lync Server 2013</span></span>](lync-server-2013-configuring-network-region-links.md)  
  

<span data-ttu-id="80441-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="80441-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

