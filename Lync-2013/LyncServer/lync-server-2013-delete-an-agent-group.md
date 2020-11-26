---
title: 'Lync Server 2013: excluir um grupo de agente'
description: 'Lync Server 2013: excluir um grupo de agente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an agent group
ms:assetid: df385fd1-62f4-42b7-a349-4eb38dea50c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182597(v=OCS.15)
ms:contentKeyID: 48185670
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dded2db0957e37a624d7e8bf3a06e102f8d35cad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430641"
---
# <a name="delete-an-agent-group-in-lync-server-2013"></a><span data-ttu-id="6c329-103">Excluir um grupo de agente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c329-103">Delete an agent group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6c329-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6c329-104">

<span> </span></span></span>

<span data-ttu-id="6c329-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="6c329-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="6c329-106">Use um dos procedimentos a seguir para excluir um grupo de agente.</span><span class="sxs-lookup"><span data-stu-id="6c329-106">Use one of the following procedures to delete an agent group.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-delete-an-agent-group"></a><span data-ttu-id="6c329-107">Para usar o painel de controle do Lync Server para excluir um grupo de agente</span><span class="sxs-lookup"><span data-stu-id="6c329-107">To use Lync Server Control Panel to delete an agent group</span></span>

1.  <span data-ttu-id="6c329-108">Faça logon como um membro do grupo RTCUniversalServerAdmins ou como um membro de uma das funções administrativas predefinidas que oferecem suporte ao Grupo de Resposta.</span><span class="sxs-lookup"><span data-stu-id="6c329-108">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="6c329-109">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6c329-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="6c329-110">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6c329-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="6c329-111">Na barra de navegação à esquerda, clique em **Grupos de resposta** e depois em **Grupo**.</span><span class="sxs-lookup"><span data-stu-id="6c329-111">In the left navigation bar, click **Response Groups**, and then click **Group**.</span></span>

4.  <span data-ttu-id="6c329-112">Na página **grupos de resposta** , digite todo ou parte do nome do grupo de agente que você deseja excluir no campo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6c329-112">On the **Response Groups** page, type all or part of the name of the agent group that you want to delete in the search field.</span></span>

5.  <span data-ttu-id="6c329-113">Na lista resultante, clique no grupo que você deseja excluir, clique em **Editar** e, em seguida, clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="6c329-113">In the resulting list, click the group that you want to delete, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="6c329-114">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c329-114">Click **OK**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-an-agent-group"></a><span data-ttu-id="6c329-115">Para usar o Windows PowerShell para excluir um grupo de agente</span><span class="sxs-lookup"><span data-stu-id="6c329-115">To use Windows PowerShell to delete an agent group</span></span>

1.  <span data-ttu-id="6c329-116">Faça logon como um membro do grupo RTCUniversalServerAdmins ou como um membro de uma das funções administrativas predefinidas que oferecem suporte ao Grupo de Resposta.</span><span class="sxs-lookup"><span data-stu-id="6c329-116">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="6c329-117">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="6c329-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="6c329-118">Na linha de comando, execute:</span><span class="sxs-lookup"><span data-stu-id="6c329-118">At the command line, run:</span></span>
    
        Get-CsRgsAgentGroup -Identity <Application Server service> -Name "<name of agent group>" | Remove-CsRgsAgentGroup
    
    <span data-ttu-id="6c329-119">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6c329-119">For example:</span></span>
    
        Get-CsRgsAgentGroup -Identity service:ApplicationServer:redmond.contoso.com -Name "Human Resources" | Remove-CsRgsAgentGroup

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6c329-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c329-120">See Also</span></span>


[<span data-ttu-id="6c329-121">Criar ou modificar um grupo de agente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c329-121">Create or modify an agent group in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-agent-group.md)  


[<span data-ttu-id="6c329-122">Remove-CsRgsAgentGroup</span><span class="sxs-lookup"><span data-stu-id="6c329-122">Remove-CsRgsAgentGroup</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsRgsAgentGroup)  
[<span data-ttu-id="6c329-123">Get-CsRgsAgentGroup</span><span class="sxs-lookup"><span data-stu-id="6c329-123">Get-CsRgsAgentGroup</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsRgsAgentGroup)  
  

<span data-ttu-id="6c329-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6c329-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

