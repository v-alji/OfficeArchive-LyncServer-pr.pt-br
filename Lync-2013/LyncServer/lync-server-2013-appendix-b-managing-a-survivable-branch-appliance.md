---
title: 'Lync Server 2013: Anexo B: Gerenciando um Aplicativo de Filial Persistente'
description: 'Lync Server 2013: Apêndice B: gerenciar um aparelho de ramificação sobreviventes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Appendix B: Managing a Survivable Branch Appliance'
ms:assetid: 2ec9d505-6d39-491c-9524-8cf36866b855
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425797(v=OCS.15)
ms:contentKeyID: 48183773
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e66d97f538ee751d7bf12b0d0f70ff3a3f5576b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439937"
---
# <a name="appendix-b-managing-a-survivable-branch-appliance-in-lync-server-2013"></a><span data-ttu-id="9c536-103">Anexo B: Gerenciando um Aplicativo de Filial Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c536-103">Appendix B: Managing a Survivable Branch Appliance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c536-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c536-104">

<span> </span></span></span>

<span data-ttu-id="9c536-105">_**Tópico da última modificação:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="9c536-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="9c536-106">Este tópico descreve os procedimentos para gerenciar um aparelho de ramificação sobreviventes.</span><span class="sxs-lookup"><span data-stu-id="9c536-106">This topic describes the procedures for managing a Survivable Branch Appliance.</span></span> <span data-ttu-id="9c536-107">Especificamente, como substituir e renomear um aparelho de ramificação sobreviventes e como alterar o pool de front-ends do Lync Server 2013 ao qual o aparelho de ramificação sobreviventes está associado.</span><span class="sxs-lookup"><span data-stu-id="9c536-107">Specifically, how to replace and rename a Survivable Branch Appliance, and how to change the Lync Server 2013 Front End pool that the Survivable Branch Appliance is associated with.</span></span>

<div>

## <a name="to-replace-a-survivable-branch-appliance"></a><span data-ttu-id="9c536-108">Para substituir um aparelho de ramificação sobreviventes</span><span class="sxs-lookup"><span data-stu-id="9c536-108">To Replace a Survivable Branch Appliance</span></span>

1.  <span data-ttu-id="9c536-109">Pare todos os serviços do Lync Server 2013 no aparelho de ramificação sobreviventes.</span><span class="sxs-lookup"><span data-stu-id="9c536-109">Stop all Lync Server 2013 services on the Survivable Branch Appliance.</span></span> <span data-ttu-id="9c536-110">(Consulte a documentação do fornecedor da solução ramificada da ramificação.)</span><span class="sxs-lookup"><span data-stu-id="9c536-110">(See the Survivable Branch Appliance vendor documentation.)</span></span>

2.  <span data-ttu-id="9c536-111">Usar Remova o aparelho de ramificação sobreviventes do domínio.</span><span class="sxs-lookup"><span data-stu-id="9c536-111">(Recommended) Remove the Survivable Branch Appliance from the domain.</span></span>

3.  <span data-ttu-id="9c536-112">Exclua o objeto de computador de aparelho de ramificação sobreviventes nos serviços de domínio Active Directory, seguindo estas etapas:</span><span class="sxs-lookup"><span data-stu-id="9c536-112">Delete the Survivable Branch Appliance computer object in Active Directory Domain Services, by following these steps:</span></span>
    
      - <span data-ttu-id="9c536-113">Faça logon em um servidor membro como membro do grupo Administradores da empresa.</span><span class="sxs-lookup"><span data-stu-id="9c536-113">Log on to a member server as a member of the Enterprise Admins group.</span></span>
    
      - <span data-ttu-id="9c536-114">Clique em **Iniciar**, em **Ferramentas administrativas** e em **usuários e computadores do Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="9c536-114">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>
    
      - <span data-ttu-id="9c536-115">Clique com o botão direito do mouse no objeto de aparelho de ramificação sobreviventes e clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="9c536-115">Right-click the Survivable Branch Appliance object, and click **Delete**.</span></span>

4.  <span data-ttu-id="9c536-116">Adicione o objeto de computador de aparelho de ramificação sobreviventes novamente.</span><span class="sxs-lookup"><span data-stu-id="9c536-116">Add the Survivable Branch Appliance computer object again.</span></span> <span data-ttu-id="9c536-117">(Consulte [Adicionar um aparelho de ramificação sobreviventes ao Active Directory no Lync Server 2013](lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md).)</span><span class="sxs-lookup"><span data-stu-id="9c536-117">(See [Add a Survivable Branch Appliance to Active Directory in Lync Server 2013](lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md).)</span></span>

5.  <span data-ttu-id="9c536-118">Aguarde a duplicação do Active Directory ocorrer.</span><span class="sxs-lookup"><span data-stu-id="9c536-118">Wait for Active Directory replication to take place.</span></span>

6.  <span data-ttu-id="9c536-119">Abra o Shell de gerenciamento do Lync Server e digite **Enable-CSTopology**.</span><span class="sxs-lookup"><span data-stu-id="9c536-119">Open the Lync Server Management Shell, and type **Enable-CSTopology**.</span></span>

7.  <span data-ttu-id="9c536-120">Conecte o novo aplicativo de ramificação sobreviventes à rede e siga as etapas em [implantando um aplicativo ou aplicativo de ramificação sobreviventes com o Lync server 2013 – tarefas de site central](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md) e [implante um aplicativo ou aplicativo de ramificação sobreviventes com o Lync Server 2013-tarefa de site de filial](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md).</span><span class="sxs-lookup"><span data-stu-id="9c536-120">Connect the new Survivable Branch Appliance to the network, and follow the steps in [Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md) and [Deploy a Survivable Branch Appliance or Server with Lync Server 2013 - branch site task](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md).</span></span>

</div>

<div>

## <a name="to-rename-a-survivable-branch-appliance"></a><span data-ttu-id="9c536-121">Para renomear um aparelho de ramificação sobreviventes</span><span class="sxs-lookup"><span data-stu-id="9c536-121">To Rename a Survivable Branch Appliance</span></span>

1.  <span data-ttu-id="9c536-122">Mover usuários para o site central.</span><span class="sxs-lookup"><span data-stu-id="9c536-122">Move users to the central site.</span></span> <span data-ttu-id="9c536-123">Para obter detalhes, consulte [mover usuários para outro pool no Lync Server 2013](lync-server-2013-move-users-to-another-pool.md).</span><span class="sxs-lookup"><span data-stu-id="9c536-123">For details, see [Move users to another pool in Lync Server 2013](lync-server-2013-move-users-to-another-pool.md).</span></span>

2.  <span data-ttu-id="9c536-124">Pare todos os serviços do Lync Server 2013 no aparelho de ramificação sobreviventes.</span><span class="sxs-lookup"><span data-stu-id="9c536-124">Stop all Lync Server 2013 services on the Survivable Branch Appliance.</span></span> <span data-ttu-id="9c536-125">(Consulte a documentação do fornecedor da solução ramificada da ramificação.)</span><span class="sxs-lookup"><span data-stu-id="9c536-125">(See the Survivable Branch Appliance vendor documentation.)</span></span>

3.  <span data-ttu-id="9c536-126">Remova o aparelho de ramificação sobreviventes da topologia seguindo estas etapas:</span><span class="sxs-lookup"><span data-stu-id="9c536-126">Remove the Survivable Branch Appliance from the topology, by following these steps:</span></span>
    
      - <span data-ttu-id="9c536-127">Clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server** e, em seguida, clique em **Construtor de topologia do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="9c536-127">Click **Start**, click **All Programs**, click **Microsoft Lync Server**, and then click **Lync Server Topology Builder**.</span></span>
    
      - <span data-ttu-id="9c536-128">Na árvore do console, expanda **Branch sites**, clique no aparelho da ramificação sobreviventes e clique em **excluir** no painel ação.</span><span class="sxs-lookup"><span data-stu-id="9c536-128">In the console tree, expand **Branch Sites**, click the Survivable Branch Appliance, and then click **Delete** on the Action pane.</span></span>

4.  <span data-ttu-id="9c536-129">Remova o aparelho de ramificação sobreviventes do domínio.</span><span class="sxs-lookup"><span data-stu-id="9c536-129">Remove the Survivable Branch Appliance from the domain.</span></span>

5.  <span data-ttu-id="9c536-130">Exclua o objeto de computador de aparelho de ramificação sobreviventes do Active Directory seguindo estas etapas:</span><span class="sxs-lookup"><span data-stu-id="9c536-130">Delete the Survivable Branch Appliance computer object in Active Directory, by following these steps:</span></span>
    
      - <span data-ttu-id="9c536-131">Faça logon em um controlador de domínio como membro do grupo Administradores da empresa.</span><span class="sxs-lookup"><span data-stu-id="9c536-131">Log on to a domain controller as a member of the Enterprise Admins group.</span></span>
    
      - <span data-ttu-id="9c536-132">Clique em **Iniciar**, em **Ferramentas administrativas** e em **usuários e computadores do Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="9c536-132">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>
    
      - <span data-ttu-id="9c536-133">Clique com o botão direito do mouse no objeto de aparelho de ramificação sobreviventes e clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="9c536-133">Right-click the Survivable Branch Appliance object, and click **Delete**.</span></span>

6.  <span data-ttu-id="9c536-134">Restaure o aparelho de ramificação sobreviventes para os padrões de fábrica.</span><span class="sxs-lookup"><span data-stu-id="9c536-134">Restore the Survivable Branch Appliance to factory defaults.</span></span> <span data-ttu-id="9c536-135">(Consulte a documentação do fornecedor da solução ramificada da ramificação.)</span><span class="sxs-lookup"><span data-stu-id="9c536-135">(See the Survivable Branch Appliance vendor documentation.)</span></span>

7.  <span data-ttu-id="9c536-136">Siga as etapas em [implantando um aplicativo ou aplicativo de ramificação sobreviventes com o Lync server 2013 – tarefas de site central](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md) e [implante um aplicativo ou aplicativo de ramificação sobreviventes com o Lync Server 2013-tarefa do site de filial](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md).</span><span class="sxs-lookup"><span data-stu-id="9c536-136">Follow the steps in [Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md) and [Deploy a Survivable Branch Appliance or Server with Lync Server 2013 - branch site task](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md).</span></span>

8.  <span data-ttu-id="9c536-137">Mover usuários para o aparelho de ramificação renomeado.</span><span class="sxs-lookup"><span data-stu-id="9c536-137">Move users to the renamed Survivable Branch Appliance.</span></span> <span data-ttu-id="9c536-138">Para obter detalhes, consulte [mover usuários para outro pool no Lync Server 2013](lync-server-2013-move-users-to-another-pool.md).</span><span class="sxs-lookup"><span data-stu-id="9c536-138">For details, see [Move users to another pool in Lync Server 2013](lync-server-2013-move-users-to-another-pool.md).</span></span>

</div>

<div>

## <a name="to-change-the-lync-server-front-end-pool-that-the-survivable-branch-appliance-is-associated-with"></a><span data-ttu-id="9c536-139">Para alterar o pool de front-ends do Lync Server ao qual o aparelho de ramificação sobreviventes está associado</span><span class="sxs-lookup"><span data-stu-id="9c536-139">To Change the Lync Server Front End Pool that the Survivable Branch Appliance Is Associated With</span></span>

1.  <span data-ttu-id="9c536-140">Mova os usuários do aparelho de ramificação sobreviventes para o pool de front-ends do Lync Server no site central.</span><span class="sxs-lookup"><span data-stu-id="9c536-140">Move users from the Survivable Branch Appliance to the Lync Server Front End pool at the central site.</span></span> <span data-ttu-id="9c536-141">Para obter detalhes, consulte [mover usuários para outro pool no Lync Server 2013](lync-server-2013-move-users-to-another-pool.md).</span><span class="sxs-lookup"><span data-stu-id="9c536-141">For details, see [Move users to another pool in Lync Server 2013](lync-server-2013-move-users-to-another-pool.md).</span></span>

2.  <span data-ttu-id="9c536-142">Pare todos os serviços do Lync Server no aparelho de ramificação sobreviventes.</span><span class="sxs-lookup"><span data-stu-id="9c536-142">Stop all Lync Server services on the Survivable Branch Appliance.</span></span> <span data-ttu-id="9c536-143">(Consulte a documentação do fornecedor da solução ramificada da ramificação).</span><span class="sxs-lookup"><span data-stu-id="9c536-143">(See the Survivable Branch Appliance vendor documentation).</span></span>

3.  <span data-ttu-id="9c536-144">Atualize o pool de front-ends do Lync Server ao qual o aparelho de ramificação sobreviventes está associado, seguindo estas etapas:</span><span class="sxs-lookup"><span data-stu-id="9c536-144">Update the Lync Server Front End pool that the Survivable Branch Appliance is associated with, by following these steps:</span></span>
    
      - <span data-ttu-id="9c536-145">Clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server** e, em seguida, clique em **Construtor de topologia do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="9c536-145">Click **Start**, click **All Programs**, click **Microsoft Lync Server**, and then click **Lync Server Topology Builder**.</span></span>
    
      - <span data-ttu-id="9c536-146">Expanda **sites de filiais**.</span><span class="sxs-lookup"><span data-stu-id="9c536-146">Expand **Branch Sites**.</span></span>
    
      - <span data-ttu-id="9c536-147">Clique com o botão direito do mouse no objeto de aparelho de ramificação sobreviventes para modificar e clique em **Editar propriedades** .</span><span class="sxs-lookup"><span data-stu-id="9c536-147">Right-click the Survivable Branch Appliance object to modify, and click **Edit Properties**</span></span>
    
      - <span data-ttu-id="9c536-148">Em resiliência, selecione o novo pool de front-ends ao qual o aparelho de ramificação sobreviventes deve estar associado e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="9c536-148">Under Resiliency, select the new Front End pool the Survivable Branch Appliance is to be associated to, and then click **Next**.</span></span>
    
      - <span data-ttu-id="9c536-149">Na árvore de console, clique com o botão direito do mouse no novo aplicativo de ramificação sobreviventes, clique em **topologia** e, em seguida, clique em **publicar**.</span><span class="sxs-lookup"><span data-stu-id="9c536-149">In the console tree, right-click the new Survivable Branch Appliance, click **Topology**, and then click **Publish**.</span></span>

4.  <span data-ttu-id="9c536-150">Reinicie todos os serviços do Lync Server no aparelho de ramificação sobreviventes.</span><span class="sxs-lookup"><span data-stu-id="9c536-150">Restart all Lync Server Services on the Survivable Branch Appliance.</span></span>

5.  <span data-ttu-id="9c536-151">Teste o aparelho de ramificação sobreviventes.</span><span class="sxs-lookup"><span data-stu-id="9c536-151">Test the Survivable Branch Appliance.</span></span> <span data-ttu-id="9c536-152">Para obter detalhes, consulte [usuários residenciais em um aplicativo ou aplicativo de ramificação sobreviventes no Lync Server 2013](lync-server-2013-home-users-on-a-survivable-branch-appliance-or-server.md).</span><span class="sxs-lookup"><span data-stu-id="9c536-152">For details, see [Home users on a Survivable Branch Appliance or Server in Lync Server 2013](lync-server-2013-home-users-on-a-survivable-branch-appliance-or-server.md).</span></span>

6.  <span data-ttu-id="9c536-153">Mova os usuários do pool de front-ends do Lync Server no site central para o aparelho de ramificação sobreviventes.</span><span class="sxs-lookup"><span data-stu-id="9c536-153">Move users from the Lync Server Front End pool at the central site to the Survivable Branch Appliance.</span></span>

<span data-ttu-id="9c536-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c536-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

