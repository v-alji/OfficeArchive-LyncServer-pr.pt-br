---
title: 'Lync Server 2013: excluir regiões de rede existentes'
description: 'Lync Server 2013: excluindo regiões de rede existentes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting existing network regions
ms:assetid: c7293a2f-2b49-4c4a-903f-f7edcea2bc5f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721882(v=OCS.15)
ms:contentKeyID: 49733815
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b148f0bd92ad398ab7057a5a291bf3245df3e47e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430319"
---
# <a name="deleting-existing-network-regions-in-lync-server-2013"></a><span data-ttu-id="4f82e-103">Excluindo regiões de rede existentes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f82e-103">Deleting existing network regions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4f82e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4f82e-104">

<span> </span></span></span>

<span data-ttu-id="4f82e-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="4f82e-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="4f82e-106">Uma região de rede interconecta várias partes de uma rede em várias áreas geográficas.</span><span class="sxs-lookup"><span data-stu-id="4f82e-106">A network region interconnects various parts of a network across multiple geographic areas.</span></span> <span data-ttu-id="4f82e-107">Todas as regiões de rede devem estar associadas a um site central.</span><span class="sxs-lookup"><span data-stu-id="4f82e-107">Every network region must be associated with a central site.</span></span> <span data-ttu-id="4f82e-108">O site central é o site do Data Center no qual o serviço de política de largura de banda do controle de admissão de chamadas (CAC) está em execução.</span><span class="sxs-lookup"><span data-stu-id="4f82e-108">The central site is the data center site on which the call admission control (CAC) bandwidth policy service is running.</span></span> <span data-ttu-id="4f82e-109">Você pode usar o painel de controle do Lync Server para configurar regiões de rede.</span><span class="sxs-lookup"><span data-stu-id="4f82e-109">You can use Lync Server Control Panel to configure network regions.</span></span> <span data-ttu-id="4f82e-110">As regiões de rede incluem configurações que determinam se caminhos alternativos pela Internet são permitidos para conexões de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="4f82e-110">Network regions include settings that determine whether alternate paths through the Internet are allowed for audio and video connections.</span></span> <span data-ttu-id="4f82e-111">No painel de controle do Lync Server, você pode criar, modificar ou excluir uma região de rede.</span><span class="sxs-lookup"><span data-stu-id="4f82e-111">From the Lync Server Control Panel, you can create, modify, or delete a network region.</span></span> <span data-ttu-id="4f82e-112">Use este tópico para excluir regiões de rede existentes.</span><span class="sxs-lookup"><span data-stu-id="4f82e-112">Use this topic to delete existing network regions.</span></span> <span data-ttu-id="4f82e-113">Para obter detalhes sobre como criar ou modificar regiões de rede existentes, consulte [criando ou modificando regiões de rede no Lync Server 2013](lync-server-2013-creating-or-modifying-network-regions.md).</span><span class="sxs-lookup"><span data-stu-id="4f82e-113">For details about creating or modifying existing network regions, see [Creating or modifying network regions in Lync Server 2013](lync-server-2013-creating-or-modifying-network-regions.md).</span></span>

<div>

## <a name="to-delete-a-network-region"></a><span data-ttu-id="4f82e-114">Para excluir uma região de rede</span><span class="sxs-lookup"><span data-stu-id="4f82e-114">To delete a network region</span></span>

1.  <span data-ttu-id="4f82e-115">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="4f82e-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="4f82e-116">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="4f82e-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="4f82e-117">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4f82e-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="4f82e-118">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **região**.</span><span class="sxs-lookup"><span data-stu-id="4f82e-118">In the left navigation bar, click **Network Configuration** and then click **Region**.</span></span>

4.  <span data-ttu-id="4f82e-119">Na página **região** , clique na região que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="4f82e-119">On the **Region** page, click the region you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4f82e-120">Você pode excluir mais de uma região de cada vez.</span><span class="sxs-lookup"><span data-stu-id="4f82e-120">You can delete more than one region at a time.</span></span> <span data-ttu-id="4f82e-121">Para fazer isso, pressione CTRL e selecione várias regiões enquanto mantém a tecla CTRL pressionada.</span><span class="sxs-lookup"><span data-stu-id="4f82e-121">To do this, press CTRL and select multiple regions while holding down the CTRL key.</span></span> <span data-ttu-id="4f82e-122">Ou, para selecionar todas as regiões, clique em <STRONG>selecionar tudo</STRONG> no menu <STRONG>Editar</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="4f82e-122">Or, to select all regions, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="4f82e-123">No menu **Editar** , clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="4f82e-123">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="4f82e-124">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f82e-124">Click **OK**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="4f82e-125">Uma região de rede não poderá ser removida se estiver associada a um site de rede.</span><span class="sxs-lookup"><span data-stu-id="4f82e-125">A network region cannot be removed if it is associated with a network site.</span></span> <span data-ttu-id="4f82e-126">Se você tentar remover uma região associada a um site, receberá uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="4f82e-126">If you attempt to remove a region associated with a site you will receive an error message.</span></span> <span data-ttu-id="4f82e-127">Para ver se uma região está associada a qualquer site, selecione a região e clique em <STRONG>Mostrar detalhes</STRONG> no menu <STRONG>Editar</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="4f82e-127">To see if a region is associated with any sites, select the region and then click <STRONG>Show details</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4f82e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f82e-128">See Also</span></span>


[<span data-ttu-id="4f82e-129">Criando ou modificando regiões de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f82e-129">Creating or modifying network regions in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-regions.md)  
  

<span data-ttu-id="4f82e-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4f82e-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

