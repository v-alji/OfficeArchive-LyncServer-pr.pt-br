---
title: 'Lync Server 2013: excluir uma fila de grupo de resposta'
description: 'Lync Server 2013: excluir uma fila de grupo de resposta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a Response Group queue
ms:assetid: 67c7a489-8c5f-4c6b-9387-9d4c11d43695
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521008(v=OCS.15)
ms:contentKeyID: 48184356
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 76b00257a12b872615ebc124abff595268b120e1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430683"
---
# <a name="delete-a-response-group-queue-in-lync-server-2013"></a><span data-ttu-id="7fbd8-103">Excluir uma fila do grupo de resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7fbd8-103">Delete a Response Group queue in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7fbd8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7fbd8-104">

<span> </span></span></span>

<span data-ttu-id="7fbd8-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="7fbd8-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="7fbd8-106">Use um dos procedimentos a seguir para excluir uma fila.</span><span class="sxs-lookup"><span data-stu-id="7fbd8-106">Use one of the following procedures to delete a queue.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-delete-a-queue"></a><span data-ttu-id="7fbd8-107">Para usar o painel de controle do Lync Server para excluir uma fila</span><span class="sxs-lookup"><span data-stu-id="7fbd8-107">To use Lync Server Control Panel to delete a queue</span></span>

1.  <span data-ttu-id="7fbd8-108">Faça logon como um membro do grupo RTCUniversalServerAdmins ou como um membro de uma das funções administrativas predefinidas que oferecem suporte ao Grupo de Resposta.</span><span class="sxs-lookup"><span data-stu-id="7fbd8-108">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="7fbd8-109">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7fbd8-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="7fbd8-110">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="7fbd8-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="7fbd8-111">Na barra de navegação esquerda, clique em **Grupos de Resposta** e clique em **Fila**.</span><span class="sxs-lookup"><span data-stu-id="7fbd8-111">In the left navigation bar, click **Response Groups**, and then click **Queue**.</span></span>

4.  <span data-ttu-id="7fbd8-112">No campo de pesquisa, digite parte ou todo o nome da fila que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="7fbd8-112">In the search field, type part or all of the name of the queue you want to delete.</span></span>

5.  <span data-ttu-id="7fbd8-113">Na lista de filas, clique na fila desejada, clique em **Editar** e, em seguida, clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="7fbd8-113">In the list of queues, click the queue that you want, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="7fbd8-114">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fbd8-114">Click **OK**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-a-queue"></a><span data-ttu-id="7fbd8-115">Para usar o Windows PowerShell para excluir uma fila</span><span class="sxs-lookup"><span data-stu-id="7fbd8-115">To use Windows PowerShell to delete a queue</span></span>

1.  <span data-ttu-id="7fbd8-116">Faça logon como um membro do grupo RTCUniversalServerAdmins ou como um membro de uma das funções administrativas predefinidas que oferecem suporte ao Grupo de Resposta.</span><span class="sxs-lookup"><span data-stu-id="7fbd8-116">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="7fbd8-117">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="7fbd8-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="7fbd8-118">Na linha de comando, execute:</span><span class="sxs-lookup"><span data-stu-id="7fbd8-118">At the command line, run:</span></span>
    
        Get-CsRgsQueue -Identity <Application Server service> -Name "<name of queue>" | Remove-CsRgsQueue
    
    <span data-ttu-id="7fbd8-119">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="7fbd8-119">For example:</span></span>
    
        Get-CsRgsQueue -Identity service:ApplicationServer:redmond.contoso.com -Name "Help Desk" | Remove-CsRgsQueue

<span data-ttu-id="7fbd8-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7fbd8-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

