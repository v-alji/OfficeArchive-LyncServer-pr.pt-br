---
title: Remover a associação do Servidor de Monitoramento
description: Remova a associação do Monitoring Server.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the Monitoring server association
ms:assetid: c45b22ae-fc06-484a-a05b-735bd1bb7448
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721877(v=OCS.15)
ms:contentKeyID: 49733810
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 852ea72f814d33022012bf565af9bc5f73e06956
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390415"
---
# <a name="remove-the-monitoring-server-association"></a><span data-ttu-id="36b2f-103">Remover a associação do Servidor de Monitoramento</span><span class="sxs-lookup"><span data-stu-id="36b2f-103">Remove the Monitoring server association</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="36b2f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="36b2f-104">

<span> </span></span></span>

<span data-ttu-id="36b2f-105">_**Tópico da última modificação:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="36b2f-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="36b2f-106">Para remover o Monitoring Server, você precisa alterar ou limpar a dependência do pool de front-ends associado, servidor front-end, aparelho para ramificação sobreviventes e servidor de ramificação sobreviventes.</span><span class="sxs-lookup"><span data-stu-id="36b2f-106">To remove the Monitoring Server, you need to change or clear the dependency on the associated Front End pool, Front End Server, Survivable Branch Appliance and Survivable Branch Server.</span></span> <span data-ttu-id="36b2f-107">Edite as propriedades do pool de front-end, servidor front-end, appliances para ramificação sobreviventes e servidor de ramificação sobreviventes para remover a dependência.</span><span class="sxs-lookup"><span data-stu-id="36b2f-107">You edit the properties of the Front End pool, Front End Server, Survivable Branch Appliance and Survivable Branch Server to remove the dependency.</span></span> <span data-ttu-id="36b2f-108">Depois de limpar a dependência e excluir o servidor no construtor de topologias, você será notificado de que o objeto de repositório de banco de dados associado também será excluído.</span><span class="sxs-lookup"><span data-stu-id="36b2f-108">After you clear the dependency and delete the server in Topology Builder, you are notified that the associated database store object in Topology Builder will also be deleted.</span></span>

<div>

## <a name="to-remove-the-monitoring-server-association"></a><span data-ttu-id="36b2f-109">Para remover a associação do Monitoring Server</span><span class="sxs-lookup"><span data-stu-id="36b2f-109">To remove the Monitoring Server association</span></span>

1.  <span data-ttu-id="36b2f-110">Abra o servidor front-end do Lync Server 2013, abra o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="36b2f-110">Open the Lync Server 2013 Front End Server, open Topology Builder.</span></span>

2.  <span data-ttu-id="36b2f-111">Navegue até o nó do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="36b2f-111">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="36b2f-112">No construtor de topologia, expanda **pools de front-end do Enterprise Edition**, **servidores front-end da edição padrão** ou **sites de filiais** com base em onde o servidor de monitoramento está definido.</span><span class="sxs-lookup"><span data-stu-id="36b2f-112">In Topology Builder, expand **Enterprise Edition Front End pools**, **Standard Edition Front End Servers**, or **Branch sites**, based on where the Monitoring Server is defined.</span></span>

4.  <span data-ttu-id="36b2f-113">Se você tiver um servidor de ramificação sobreviventes associado, expanda **sites de ramificação**, expanda o nome do site da filial e expanda **aparelhos de ramificação sobreviventes**.</span><span class="sxs-lookup"><span data-stu-id="36b2f-113">If you have Survivable Branch Server associated, expand **Branch sites**, expand the branch site name, and then expand **Survivable Branch Appliances**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="36b2f-114"><STRONG>Aparelhos de ramificação sobreviventes</STRONG> na interface do usuário se aplicam ao servidor de ramificação sobreviventes e ao aparelho de ramificação sobreviventes.</span><span class="sxs-lookup"><span data-stu-id="36b2f-114"><STRONG>Survivable Branch Appliances</STRONG> in the user interface applies to both Survivable Branch Server and Survivable Branch Appliance.</span></span>

    
    </div>

5.  <span data-ttu-id="36b2f-115">Clique com o botão direito do mouse no pool, no servidor ou no dispositivo associado ao Monitoring Server e clique em **Editar propriedades**.</span><span class="sxs-lookup"><span data-stu-id="36b2f-115">Right-click the pool, server, or device that is associated with the Monitoring Server, and then click **Edit Properties**.</span></span>

6.  <span data-ttu-id="36b2f-116">Em **Editar propriedades**, em **geral**, em **associações**, desmarque a caixa de seleção **associar o servidor de monitoramento** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="36b2f-116">In **Edit Properties**, under **General**, under **Associations**, clear the **Associate Monitoring Server** check box, and then click **OK**.</span></span>

7.  <span data-ttu-id="36b2f-117">Repita a etapa anterior para qualquer outro pool, servidor ou dispositivo associado ao servidor de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="36b2f-117">Repeat the previous step for any other pool, server or device associated with the Monitoring Server.</span></span>

8.  <span data-ttu-id="36b2f-118">Clique com o botão direito do mouse no servidor de monitoramento e clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="36b2f-118">Right-click the Monitoring Server, and then click **Delete**.</span></span>

9.  <span data-ttu-id="36b2f-119">Em **excluir repositórios dependentes**, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="36b2f-119">On **Delete Dependent Stores**, click **OK**.</span></span>

10. <span data-ttu-id="36b2f-120">Publique a topologia, verifique o status da replicação e execute o assistente de implantação do Lync Server conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="36b2f-120">Publish the topology, check replication status, and run the Lync Server Deployment Wizard as needed.</span></span>

<span data-ttu-id="36b2f-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="36b2f-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

