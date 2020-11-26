---
title: 'Lync Server 2013: criar um novo filtro de transferência de arquivo para um site específico'
description: 'Lync Server 2013: criar um novo filtro de transferência de arquivo para um site específico.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a new file transfer filter for a specific site
ms:assetid: d0006487-5217-491c-b730-e6c551cd9825
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182589(v=OCS.15)
ms:contentKeyID: 48185577
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d3b5003711c2f2e74b726809fba5da6d9fd0aa57
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432167"
---
# <a name="create-a-new-file-transfer-filter-in-lync-server-2013-for-a-specific-site"></a><span data-ttu-id="4c1b2-103">Criar um novo filtro de transferência de arquivo no Lync Server 2013 para um site específico</span><span class="sxs-lookup"><span data-stu-id="4c1b2-103">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4c1b2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4c1b2-104">

<span> </span></span></span>

<span data-ttu-id="4c1b2-105">_**Tópico da última modificação:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="4c1b2-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="4c1b2-106">Além de modificar o filtro de transferência de arquivo global, você pode configurar filtros de transferência de arquivo personalizados para sites específicos na sua implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4c1b2-106">In addition to modifying the global file transfer filter, you can configure custom file transfer filters for specific sites within your Lync Server 2013 deployment.</span></span> <span data-ttu-id="4c1b2-107">Para obter detalhes sobre a filtragem de transferência de arquivo, consulte [Configurando a transferência de arquivos e a filtragem de URL para mensagens instantâneas (IM) no Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span><span class="sxs-lookup"><span data-stu-id="4c1b2-107">For details about file transfer filtering, see [Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span></span>

<div>

## <a name="to-create-a-file-transfer-filter-for-a-specific-site"></a><span data-ttu-id="4c1b2-108">Para criar um filtro de transferência de arquivo para um site específico</span><span class="sxs-lookup"><span data-stu-id="4c1b2-108">To create a file transfer filter for a specific site</span></span>

1.  <span data-ttu-id="4c1b2-109">Usando uma conta de usuário atribuída à função CsUserAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="4c1b2-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="4c1b2-110">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="4c1b2-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="4c1b2-111">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4c1b2-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="4c1b2-112">Na barra de navegação à esquerda, clique em **mensagens instantâneas e presença** e, em seguida, clique em **filtro de arquivo**.</span><span class="sxs-lookup"><span data-stu-id="4c1b2-112">In the left navigation bar, click **IM and Presence** and then click **File Filter**.</span></span>

4.  <span data-ttu-id="4c1b2-113">Na página **filtro de arquivo** , clique em **novo**.</span><span class="sxs-lookup"><span data-stu-id="4c1b2-113">On the **File Filter** page, click **New**.</span></span>

5.  <span data-ttu-id="4c1b2-114">Na caixa de diálogo **selecionar um site** , clique no site para o qual você deseja criar o filtro de transferência de arquivo e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c1b2-114">In the **Select a Site** dialog box, click the site for which you want to create the file transfer filter, and then click **OK**.</span></span>

6.  <span data-ttu-id="4c1b2-115">Em **novo filtro de arquivo**, clique na caixa de seleção **habilitar filtro de arquivo** .</span><span class="sxs-lookup"><span data-stu-id="4c1b2-115">In **New File Filter**, click the **Enable file filter** check box.</span></span>

7.  <span data-ttu-id="4c1b2-116">Na caixa de listagem suspensa **transferência de arquivo** , clique em **bloquear tudo** ou **bloquear tipos de arquivos específicos**.</span><span class="sxs-lookup"><span data-stu-id="4c1b2-116">In **File transfer** drop-down list box, click **Block All** or **Block specific file types**.</span></span>

8.  <span data-ttu-id="4c1b2-117">Se você clicou em **bloquear tudo**, pule para a etapa 10.</span><span class="sxs-lookup"><span data-stu-id="4c1b2-117">If you clicked **Block All**, skip to step 10.</span></span>

9.  <span data-ttu-id="4c1b2-118">Se você clicou em **bloquear tipos de arquivo específicos**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4c1b2-118">If you clicked **Block specific file types**, do the following:</span></span>
    
    1.  <span data-ttu-id="4c1b2-119">Clique em **selecionar** para modificar a lista padrão de extensões de tipo de arquivo que você deseja bloquear.</span><span class="sxs-lookup"><span data-stu-id="4c1b2-119">Click **Select** to modify the default list of file type extensions that you want to block.</span></span>
    
    2.  <span data-ttu-id="4c1b2-120">Na caixa de diálogo **Selecionar tipo de arquivo** , selecione os tipos de arquivo que você deseja bloquear ou permitir, adicionando ou removendo suas extensões das categorias em **extensões de tipo de arquivo**.</span><span class="sxs-lookup"><span data-stu-id="4c1b2-120">In the **Select File Type** dialog box, select the file types that you want to block or allow by adding or removing their extensions from the categories under **File type extensions**.</span></span>
    
    3.  <span data-ttu-id="4c1b2-121">Se você não vir a extensão para um tipo de arquivo que deseja bloquear, digite a extensão na caixa de texto em **adicionar extensões de tipo de arquivo à lista** e, em seguida, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="4c1b2-121">If you do not see the extension for a file type that you want to block, type the extension in the text box under **Add file type extensions to the list**, and then click **Add**.</span></span>
    
    4.  <span data-ttu-id="4c1b2-122">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c1b2-122">Click **OK**.</span></span>

10. <span data-ttu-id="4c1b2-123">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="4c1b2-123">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4c1b2-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c1b2-124">See Also</span></span>


[<span data-ttu-id="4c1b2-125">Configurar a transferência de arquivos e a filtragem de URL para mensagens instantâneas (IM) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c1b2-125">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)  
[<span data-ttu-id="4c1b2-126">Criar um novo filtro de URL no Lync Server 2013 para manipular hiperlinks em conversas de mensagens instantâneas</span><span class="sxs-lookup"><span data-stu-id="4c1b2-126">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>](lync-server-2013-create-a-new-url-filter-to-handle-hyperlinks-in-im-conversations.md)  
[<span data-ttu-id="4c1b2-127">Modificar o filtro de transferência de arquivo padrão no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c1b2-127">Modify the default file transfer filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-file-transfer-filter.md)  


[<span data-ttu-id="4c1b2-128">Modificar o filtro de URL padrão no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c1b2-128">Modify the default URL filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-url-filter.md)  
  

<span data-ttu-id="4c1b2-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4c1b2-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

