---
title: 'Lync Server 2013: Implantar tipos de endereço IP em um Servidor de Borda'
description: 'Lync Server 2013: implantar tipos de endereço IP em um servidor de borda.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploy IP address types on an Edge Server
ms:assetid: 6e2fe7e8-6e90-4d1a-8fc5-e3be92c46571
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204984(v=OCS.15)
ms:contentKeyID: 48184435
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7798ca2f7b38865a2b4ea373546dd4e7203f5b8e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430191"
---
# <a name="deploy-ip-address-types-on-an-edge-server-for-lync-server-2013"></a><span data-ttu-id="78249-103">Implantar tipos de endereço IP em um Servidor de Borda para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="78249-103">Deploy IP address types on an Edge Server for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="78249-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="78249-104">

<span> </span></span></span>

<span data-ttu-id="78249-105">_**Tópico da última modificação:** 2012-06-14_</span><span class="sxs-lookup"><span data-stu-id="78249-105">_**Topic Last Modified:** 2012-06-14_</span></span>

<span data-ttu-id="78249-106">Usando o construtor de topologias, execute as etapas do procedimento a seguir para implantar tipos de endereços IP em um servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="78249-106">Using Topology Builder, perform the steps in the following procedure to deploy IP address types on an Edge Server.</span></span>

<div>

## <a name="to-deploy-ip-address-types-on-an-edge-server"></a><span data-ttu-id="78249-107">Para implantar tipos de endereço IP em um servidor de borda</span><span class="sxs-lookup"><span data-stu-id="78249-107">To deploy IP address types on an Edge Server</span></span>

1.  <span data-ttu-id="78249-108">Em Construtor de topologia, em **conjuntos de bordas**, clique com o botão direito do mouse no servidor dentro de um pool e selecione **Editar propriedades**.</span><span class="sxs-lookup"><span data-stu-id="78249-108">In Topology Builder, under **Edge pools**, right-click the server within a pool, and then select **Edit Properties**.</span></span> <span data-ttu-id="78249-109">(Como alternativa, selecione o servidor e clique em **Editar Propriedades** no menu **Ação**.)</span><span class="sxs-lookup"><span data-stu-id="78249-109">(Alternatively, select the server, and then click **Edit Properties** from the **Action** menu.)</span></span>

2.  <span data-ttu-id="78249-p102">Na janela **Editar Propriedades**, selecione a configuração de endereço IP para a qual deseja oferecer suporte. As figuras a seguir mostram uma configuração de pilha dupla para as interfaces interna e externa.</span><span class="sxs-lookup"><span data-stu-id="78249-p102">In the **Edit Properties** window, select the IP address configuration that you want to support. The following figures show a dual stack configuration for the internal interface and the external interface.</span></span>
    
    <span data-ttu-id="78249-112">**Interface interna do servidor de borda com pilha dupla**</span><span class="sxs-lookup"><span data-stu-id="78249-112">**Dual stacked Edge Server internal interface**</span></span>
    
    <span data-ttu-id="78249-113">![Página Propriedades gerais do Lync Server](images/JJ204984.5b0883ee-b9f2-4a21-91a9-3286d0beb63b(OCS.15).png "Página Propriedades gerais do Lync Server")</span><span class="sxs-lookup"><span data-stu-id="78249-113">![Lync Server general properties page](images/JJ204984.5b0883ee-b9f2-4a21-91a9-3286d0beb63b(OCS.15).png "Lync Server general properties page")</span></span>
    
    <span data-ttu-id="78249-114">**Interface externa do servidor de borda com pilha dupla**</span><span class="sxs-lookup"><span data-stu-id="78249-114">**Dual stacked Edge Server external interface**</span></span>
    
    <span data-ttu-id="78249-115">![Próxima página de configuração de salto/externo do Lync Server](images/JJ204984.2aa00ce2-ba50-40aa-bbf1-78636016daf9(OCS.15).png "Próxima página de configuração de salto/externo do Lync Server")</span><span class="sxs-lookup"><span data-stu-id="78249-115">![Lync Server next hop/external configuration page](images/JJ204984.2aa00ce2-ba50-40aa-bbf1-78636016daf9(OCS.15).png "Lync Server next hop/external configuration page")</span></span>

3.  <span data-ttu-id="78249-116">Para cada tipo de endereço selecionado, você deve fornecer os endereços internos e externos apropriados.</span><span class="sxs-lookup"><span data-stu-id="78249-116">For each address type that you select, you must supply appropriate internal and external addresses.</span></span>

<span data-ttu-id="78249-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="78249-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

