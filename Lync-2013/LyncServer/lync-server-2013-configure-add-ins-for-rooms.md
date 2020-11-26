---
title: 'Lync Server 2013: Configurar suplementos para salas'
description: 'Lync Server 2013: configurar suplementos para salas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure add-ins for rooms
ms:assetid: 4eeaf19e-8369-4f6f-af65-a283cf7daa1c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204878(v=OCS.15)
ms:contentKeyID: 48184090
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 803bff81fa76bf5a7d2d408c93ba9247ead72510
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434150"
---
# <a name="configure-add-ins-for-rooms-in-lync-server-2013"></a><span data-ttu-id="0244c-103">Configurar suplementos para salas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0244c-103">Configure add-ins for rooms in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0244c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0244c-104">

<span> </span></span></span>

<span data-ttu-id="0244c-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="0244c-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="0244c-106">No painel de controle do Lync Server 2013, você pode usar a seção de **suplemento** da página de **chat persistente** para associar URLs a salas de chat persistentes.</span><span class="sxs-lookup"><span data-stu-id="0244c-106">In Lync Server 2013 Control Panel, you can use the **Add-in** section of the **Persistent Chat** page to associate URLs with Persistent Chat rooms.</span></span> <span data-ttu-id="0244c-107">Essas URLs aparecem no cliente do Lync 2013 na sala de chat no painel de extensibilidade de conversa.</span><span class="sxs-lookup"><span data-stu-id="0244c-107">These URLs appear in the Lync 2013 client in the chat room in the conversation extensibility pane.</span></span> <span data-ttu-id="0244c-108">Um administrador deve adicionar suplementos à lista de suplementos registrados e os gerentes/autores da sala de chat devem associar salas a um dos suplementos registrados antes que os usuários possam ver essa atualização em seu cliente Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="0244c-108">An administrator must add Add-ins to the list of registered add-ins, and chat room managers/Creators have to associate rooms with one of the registered add-ins before users can see this upgrade in their Lync 2013 client.</span></span>

<span data-ttu-id="0244c-109">Os suplementos são usados para estender a experiência na sala.</span><span class="sxs-lookup"><span data-stu-id="0244c-109">Add-ins are used to extend the in-room experience.</span></span> <span data-ttu-id="0244c-110">Um suplemento típico pode incluir uma URL apontando para um aplicativo do Silverlight que intercepta quando um marcador de ação é publicado em uma sala de chat e mostra o histórico de ações no painel extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="0244c-110">A typical add-in might include a URL pointing to a Silverlight application that intercepts when a stock ticker is posted to a chat room, and shows the stock history in the extensibility pane.</span></span> <span data-ttu-id="0244c-111">Outros exemplos incluem a URL do OneNote 2013 na sala de chat como um suplemento para incluir algum contexto compartilhado, como o "Mais lembrado" ou "Assunto do dia".</span><span class="sxs-lookup"><span data-stu-id="0244c-111">Other examples include embedding a OneNote 2013 URL in the chat room as an add-in to include some shared context, such as "Top of mind" or "Topic of the day."</span></span>

<div>

## <a name="to-configure-add-ins-for-chat-rooms"></a><span data-ttu-id="0244c-112">Para configurar Suplementos para as salas de chat</span><span class="sxs-lookup"><span data-stu-id="0244c-112">To configure Add-ins for chat rooms</span></span>

1.  <span data-ttu-id="0244c-113">A partir de uma conta de usuário com a função CsPersistentChatAdministrator ou CsAdministrator atribuída, faça o logon em qualquer computador na sua implementação interna.</span><span class="sxs-lookup"><span data-stu-id="0244c-113">From a user account that is assigned to the CsPersistentChatAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="0244c-114">No menu **Iniciar** , selecione o painel de controle do Lync Server ou abra uma janela do navegador e, em seguida, insira a URL de administração.</span><span class="sxs-lookup"><span data-stu-id="0244c-114">From the **Start** menu, select the Lync Server Control Panel or open a browser window, and then enter the Admin URL.</span></span> <span data-ttu-id="0244c-115">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0244c-115">For details about the different methods that you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="0244c-116">Você também pode usar cmdlets do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0244c-116">You can also use Windows PowerShell cmdlets.</span></span> <span data-ttu-id="0244c-117">Para obter detalhes, consulte <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">Configurando o servidor de chat persistente usando cmdlets do Windows PowerShell</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="0244c-117">For details, see <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</A> in the Deployment documentation.</span></span>

    
    </div>

3.  <span data-ttu-id="0244c-118">Na barra de navegação esquerda, clique em **Chat Persistente** e depois em **Suplemento**.</span><span class="sxs-lookup"><span data-stu-id="0244c-118">In the left navigation bar, click **Persistent Chat**, and then click **Add-in**.</span></span>
    
    <span data-ttu-id="0244c-119">Para várias implantações de pool do servidor de chat persistente, selecione o pool apropriado na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="0244c-119">For multiple Persistent Chat Server pool deployments, select the appropriate pool from the drop-down list.</span></span>

4.  <span data-ttu-id="0244c-120">Na página  **Suplementos**, clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="0244c-120">On the **Add-in** page, click **New**.</span></span>

5.  <span data-ttu-id="0244c-121">Em **selecionar um serviço**, selecione o serviço correspondente ao pool de servidores de chat persistente em que você precisa criar o suplemento.</span><span class="sxs-lookup"><span data-stu-id="0244c-121">In **Select a Service**, select the service corresponding to the Persistent Chat Server pool where you need to create the Add-in.</span></span> <span data-ttu-id="0244c-122">Suplementos não podem ser movidos de um pool a outro nem compartilhado entre pools diferentes.</span><span class="sxs-lookup"><span data-stu-id="0244c-122">Add-ins cannot be moved from one pool to another or shared between different pools.</span></span>

6.  <span data-ttu-id="0244c-123">Em **Suplementos novos**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0244c-123">In **New Add-in**, do the following:</span></span>
    
      - <span data-ttu-id="0244c-124">Em **Nome**, especifique um nome para o novo suplemento.</span><span class="sxs-lookup"><span data-stu-id="0244c-124">In **Name**, specify a name for the new add-in.</span></span>
    
      - <span data-ttu-id="0244c-p106">Em **URL**, especifique a URL que deve ser associada ao suplemento. As URLs são limitadas aos protocolos http e https.</span><span class="sxs-lookup"><span data-stu-id="0244c-p106">In **URL**, specify the URL to be associated with the add-in. URLs are limited to http and https protocols.</span></span>

7.  <span data-ttu-id="0244c-127">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="0244c-127">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0244c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0244c-128">See Also</span></span>


[<span data-ttu-id="0244c-129">Abrir ferramentas administrativas do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0244c-129">Open Lync Server 2013 administrative tools</span></span>](lync-server-2013-open-lync-server-administrative-tools.md)  


[<span data-ttu-id="0244c-130">Configurando Servidor de Chat Persistente usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0244c-130">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</span></span>](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md)  
  

<span data-ttu-id="0244c-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0244c-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

