---
title: Remover BackCompatSite
description: Remova o BackCompatSite.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove BackCompatSite
ms:assetid: 039650e3-541b-45c2-a682-c4fa08423118
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204637(v=OCS.15)
ms:contentKeyID: 48183265
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 809324320ec1869ac0c9d324b8fc270a3cf8f174
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440295"
---
# <a name="remove-backcompatsite"></a><span data-ttu-id="13a52-103">Remover BackCompatSite</span><span class="sxs-lookup"><span data-stu-id="13a52-103">Remove BackCompatSite</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13a52-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13a52-104">

<span> </span></span></span>

<span data-ttu-id="13a52-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="13a52-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="13a52-106">Após a desativação de todos os pools e a desinstalação de todos os servidores de borda, execute o assistente de mesclagem do construtor de topologias para remover o **BackCompatSite**.</span><span class="sxs-lookup"><span data-stu-id="13a52-106">After all pools are deactivated and all Edge Servers have been uninstalled, run the Topology Builder Merge wizard to remove the **BackCompatSite**.</span></span>

<div>

## <a name="to-remove-backcompat-site-from-topology-builder"></a><span data-ttu-id="13a52-107">Para remover o site de adcompatibilidade do construtor de topologias</span><span class="sxs-lookup"><span data-stu-id="13a52-107">To remove BackCompat site from Topology Builder</span></span>

1.  <span data-ttu-id="13a52-108">Abrir uma implantação existente do construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="13a52-108">Open an existing deployment from Topology Builder.</span></span>

2.  <span data-ttu-id="13a52-109">No menu **ação** , clique em **Merge 2007 R2 Topology**.</span><span class="sxs-lookup"><span data-stu-id="13a52-109">In the **Action** menu, click **Merge 2007 R2 Topology**.</span></span>

3.  <span data-ttu-id="13a52-110">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="13a52-110">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="13a52-111">Na página **especificar borda herdada** , certifique-se de que a lista de servidores de borda está vazia.</span><span class="sxs-lookup"><span data-stu-id="13a52-111">On the **Specify Legacy Edge** page, ensure that list of Edge Servers is empty.</span></span> <span data-ttu-id="13a52-112">Se a lista não estiver vazia, use o botão **remover** para remover todos os servidores de borda herdados e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="13a52-112">If the list is not empty, use the **Remove** button to remove all the legacy Edge Servers, and then click **Next**.</span></span>
    
    <span data-ttu-id="13a52-113">![Assistente de topologia de mesclagem, especificar a página de configuração de borda](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "Assistente de topologia de mesclagem, especificar a página de configuração de borda")</span><span class="sxs-lookup"><span data-stu-id="13a52-113">![Merge Topology Wizard, Specify Edge Setup page](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "Merge Topology Wizard, Specify Edge Setup page")</span></span>  

5.  <span data-ttu-id="13a52-114">Na página **especificar a configuração da porta SIP interna** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="13a52-114">On the **Specify Internal SIP port setting** page, click **Next**.</span></span>

6.  <span data-ttu-id="13a52-115">Na página **Resumo** , clique em **Avançar** para começar a mesclar as topologias e remover o site herdado.</span><span class="sxs-lookup"><span data-stu-id="13a52-115">On the **Summary** page, click **Next** to begin merging the topologies to remove the legacy site.</span></span>

7.  <span data-ttu-id="13a52-116">Na coluna **status** , verifique se o valor é **êxito** e clique em **concluir** para fechar o assistente.</span><span class="sxs-lookup"><span data-stu-id="13a52-116">In the **Status** column, verify that the value is **Success** and then click **Finish** to close the wizard.</span></span>

8.  <span data-ttu-id="13a52-117">No painel esquerdo do construtor de topologias, expanda o BackCompatSite e assegure-se de que nenhum servidor esteja listado.</span><span class="sxs-lookup"><span data-stu-id="13a52-117">In the left pane of Topology Builder, expand the BackCompatSite and ensure no servers are listed.</span></span>

9.  <span data-ttu-id="13a52-118">Clique com o botão direito do mouse no **BackCompatSite** e, em seguida, clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="13a52-118">Right-click the **BackCompatSite**, and then click **Delete**.</span></span>

10. <span data-ttu-id="13a52-119">Em **Construtor de topologia**, selecione o nó mais superior do **Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="13a52-119">In **Topology Builder**, select the top-most node **Lync Server**.</span></span>

11. <span data-ttu-id="13a52-120">No menu **ação** , selecione **publicar topologia** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="13a52-120">From the **Action** menu, select **Publish Topology** and then click **Next**.</span></span>

12. <span data-ttu-id="13a52-121">Quando o **Assistente de publicação** for concluído, clique em **concluir** para fechar o assistente.</span><span class="sxs-lookup"><span data-stu-id="13a52-121">When the **Publishing wizard** completes, click **Finish** to close the wizard.</span></span>

<span data-ttu-id="13a52-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13a52-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

